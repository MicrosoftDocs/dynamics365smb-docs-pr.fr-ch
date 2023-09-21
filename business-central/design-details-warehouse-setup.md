---
title: "Détails de conception\_: paramètres entrepôt"
description: 'La fonctionnalité d’entrepôt contient différents niveaux de complexité, qui sont largement définis par la configuration des bacs sur les cartes de localisation.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
---
# <a name="design-details-warehouse-setup"></a>Détails de conception : paramètres entrepôt

La fonctionnalité d’entrepôt dans [!INCLUDE[prod_short](includes/prod_short.md)] contient différents niveaux de complexité, tels que définis par les autorisations de licence dans les granules proposés. Le niveau de complexité dans une solution entrepôt est en grande partie défini par le paramétrage des emplacements sur les fiches magasin, qui est lui-même contrôlé par licence afin que l’accès aux champs de configuration de l’emplacement soit défini par la licence. En outre, les objets applicatifs de la licence déterminent le document d’interface utilisateur à utiliser pour les activités entrepôt prises en charge.  
<!--
The following warehouse-related granules exist:  

- Basic Inventory (4010)  
- Bin (4170)  
- Put Away (4180)  
- Warehouse Receipt (4190)  
- Pick (4200)  
- Warehouse Shipment (4210)  
- Warehouse Management Systems (4620)  
- Internal Picks and Put-aways (4630)  
- Automated Data Capture System (4640)
- Bin Setup (4660)  

For more information about each granule, see [[!INCLUDE[prod_short](includes/prod_short.md)] Price Sheets](https://go.microsoft.com/fwlink/?LinkId=238341) (requires PartnerSource account). -->

Le tableau suivant indique les granules requis pour définir les différents niveaux de complexité entrepôt, les documents de l’interface utilisateur qui prennent en charge chaque niveau, et les codes magasin qui reflètent ces niveaux dans la base de données de démonstration [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE [locations-cronus](includes/locations-cronus.md)]

|Niveau de complexité|Description|Document d’interface utilisateur|Exemple d’emplacement|Granule minimum requis|  
|----------------|-----------|-----------|---------------|---------------------------|  
|1|Aucune activité entrepôt dédiée.<br /><br /> Validation recevoir/expédier à partir des commandes.|Commande|BLEU|Stock de base|  
|2|Aucune activité entrepôt dédiée.<br /><br /> Validation recevoir/expédier à partir des commandes.<br /><br /> Code emplacement requis.|Commande, avec un code emplacement|ARGENTE|Stock de base/Emplacement|  
|3 <br /><br /> **REMARQUE** : bien que les paramètres soient appelés **Prélèvement requis** et **Rangement requis**, vous pouvez quand même valider les réceptions et les expéditions directement à partir des documents commerciaux origine dans les magasins où vous cochez ces cases.|Activité entrepôt de base, par commande.<br /><br /> Validation recevoir/expédier à partir des documents rangement/prélèvement stock. <br /><br /> Code emplacement requis.|Rangement stock/mouvement stock/prélèvement stock, avec le code emplacement|(ARGENT + Rangement requis ou Rangement requis)|Stock de base/Emplacement/Rangement/Prélèvement|  
|4|Activité entrepôt avancée pour plusieurs ordres/commandes.<br /><br /> Validation recevoir/expédier consolidée en fonction des enregistrements de rangement/prélèvement dans l’entrepôt.|Réception entrepôt/Stockage en entrepôt/Prélèvement entrepôt/Expédition entrepôt/Feuille prélèvement|VERT|Stock de base/Réception entrepôt/Rangement/Prélèvement/Expédition entrepôt|  
|5|Activité entrepôt avancée pour plusieurs ordres/commandes.<br /><br /> Validation recevoir/expédier consolidée en fonction des enregistrements de rangement/prélèvement dans l’entrepôt.<br /><br /> Code emplacement requis.|Réception entrepôt/Stockage en entrepôt/Prélèvement entrepôt/Expédition entrepôt/Feuille prélèvement/Feuille stockage, avec code d’emplacement|(VERT + Emplacement obligatoire)|Stock de base/Emplacement/Réception entrepôt/Rangement/Prélèvement/Expédition entrepôt|  
|6 <br /><br /> **Remarque** : ce niveau est appelé « WMS », car il requiert le granule le plus avancé, Warehouse Management Systems.|Activité entrepôt avancée pour plusieurs ordres/commandes<br /><br /> Validation recevoir/expédier consolidée en fonction des enregistrements de rangement/prélèvement dans l’entrepôt<br /><br /> Code emplacement requis.<br /><br /> Le code zone/classe est facultatif.<br /><br /> Magasiniers dirigés par flux de travail<br /><br /> Planification de réapprovisionnement des emplacements<br /><br /> Priorité emplacement<br /><br /> Paramétrage emplacement par capacité<br /><br /> Insertion <!-- Hand-held device integration -->|Réception entrepôt/Rangement entrepôt/Prélèvement entrepôt/Expédition entrepôt/Mouvement entrepôt/Feuille prélèvement/Feuille rangement/Entrepôt interne. Prélèvement/Rangement entrepôt interne, avec code d’emplacement/classe/zone<br /><br /> Différentes feuilles pour la gestion d’emplacement<br /><br /> Écrans ADCS|BLANC|Stock de base/Emplacement/Rangement/Réception entrepôt/Prélèvement/Expédition entrepôt/Systèmes de gestion d’entrepôt/Prélèvement interne et rangements/Paramétrage emplacement<!-- Automated Data Capture System/ -->Paramétrage emplacement|  

Pour des exemples d’utilisation des documents de l’interface utilisateur par niveau de complexité entrepôt, voir [Détails de conception : flux d’enlogement](design-details-inbound-warehouse-flow.md).  

## <a name="bin-and-bin-content"></a>Emplacement et Contenu emplacement

Un emplacement est un dispositif de stockage conçu pour contenir des éléments discrets. Il s’agit de la plus petite unité de conteneur dans [!INCLUDE[prod_short](includes/prod_short.md)]. Les quantités d’articles dans des emplacements sont appelées contenu de l’emplacement. Une recherche à partir du champ **Article** ou du champ **Code emplacement** dans n’importe quel document entrepôt affiche la disponibilité calculée de l’article dans l’emplacement.  

Le contenu d’un emplacement peut se voir affecter une propriété fixe, dédiée ou par défaut, pour définir la manière dont le contenu de l’emplacement peut être utilisé. Les emplacements sans aucune de ces propriétés sont appelés emplacements dynamiques.  

Un emplacement statique contient les articles affectés au code emplacement concerné. La propriété d’emplacement fixe garantit que même si le contenu de l’emplacement est momentanément vidé, le contenu de l’emplacement ne disparaît pas et l’emplacement est donc sélectionné de nouveau dès qu’il est réapprovisionné.  

Un emplacement dédié contient ce qui peut être prélevé pour la ressource dédiée, par exemple un poste de charge, qui utilise l’emplacement en question. Un autre contenu non-prélèvement, tel que les quantités sortantes sur une validation expédition, peut encore être consommé à partir d’un emplacement dédié. Seul le contenu de l’emplacement pris en compte par l’algorithme **Créer prélèvement** est protégé dans un emplacement dédié.  

La propriété de l’emplacement par défaut est utilisée par le système pour proposer des emplacements pour les activités de l’entrepôt. Dans des magasins WMS, la propriété de l’emplacement par défaut n’est pas utilisée. Dans les magasins où des emplacements sont requis, la propriété est utilisée dans des flux entrants pour indiquer l’endroit où placer les articles. Dans les flux de désenlogement, la propriété est utilisée pour indiquer l’endroit où prendre des articles.  

> [!NOTE]  
>  Si les articles sortants sont stockés dans plusieurs emplacements, les articles sont d’abord pris dans les emplacements non définis par défaut, pour vider le contenu de ces emplacements, puis les articles restants sont pris dans l’emplacement par défaut.  

Il ne peut y avoir qu’un emplacement par défaut par article par magasin.  

## <a name="bin-type"></a>Type emplacement

Dans des installations WMS, vous pouvez définir les activités entrepôt qui sont permises pour un emplacement en lui affectant un type. Les types d’emplacement suivants existent :  

|Type emplacement|Désignation|  
|------------------|---------------------------------------|  
|RECEPTION|Articles enregistrés comme étant reçus, mais pas encore rangés.|  
|EXPEDITION|Les articles prélevés pour des lignes expédition entrepôt, mais pas encore validés en tant qu’articles expédiés.|  
|RANG.|Généralement, les articles devant être stockés dans de grandes unités, mais auxquels vous ne souhaitez pas accéder à des fins de prélèvement. Étant donné que ces emplacements ne sont pas utilisés pour le prélèvement, que ce soit pour des ordres de fabrication ou des expéditions, l’utilisation d’un emplacement de type Rangement risque d’être limitée, mais ce type d’emplacement peut se révéler utile si vous avez acheté une grande quantité d’articles. La priorité emplacement des emplacements de ce type doit toujours être peu élevée. Ainsi, lors du rangement des articles reçus, ce sont les emplacements RANGPRELEV. de priorité plus élevée associés à l’article concerné qui sont utilisés. Lorsque vous utilisez ce type d’emplacement, vous devez régulièrement procéder au réapprovisionnement des emplacements, afin que les articles stockés dans ces emplacements puissent également être disponibles dans les emplacements de type RANGPRELEV. ou PRELEV.|  
|PRELEV.|Articles à utiliser uniquement pour prélever. Le réapprovisionnement de ces emplacements peut uniquement être effectué par mouvement, non par rangement.|  
|RANGPRELEV.|Articles dans des emplacements qui sont proposés à la fois pour les fonctions de rangement et de prélèvement. Les emplacements de ce type ont vraisemblablement un classement différent. Vous pouvez configurer vos emplacements de stockage en vrac comme ce type d’emplacement avec un classement peu élevé par rapport à vos emplacements prélèvement ordinaires ou vos emplacements prélèvement en aval.|  
|CQ|Cet emplacement est utilisé pour des ajustements stock, si vous le spécifiez sur la fiche magasin dans le champ **Code empl. ajustement**. Vous pouvez également configurer des emplacements de ce type pour des articles défectueux ou en cours de contrôle. vous pouvez déplacer des articles vers ce type d’emplacement afin que la circulation habituelle des articles ne puisse pas y accéder. **Remarque :** contrairement à tous les autres types d’emplacement, les cases à cocher pour le traitement des articles sont toutes désactivées par défaut pour le type **CQ**. Cela signifie que tout contenu que vous placez dans un emplacement de type CQ est exclu des flux d’articles.|  

Pour tous les types d’emplacement, à l’exception de PRELEV, RANGPRELEV et RANGEMENT, aucune autre activité n’est autorisée pour l’emplacement que celle définie par son type d’emplacement. Par exemple, un emplacement de type **Réception** peut être utilisé uniquement pour y recevoir des articles ou pour en prélever des articles.  

> [!NOTE]  
> Un mouvement ne peut être effectué que vers des emplacements de type RECEPT. et CQ. De même, seuls des mouvements peuvent être effectués à partir des emplacements de type EXPED. et CQ.  

## <a name="bin-ranking"></a>Priorité emplacement

Dans l’entreposage avancé, vous pouvez automatiser et optimiser la façon de collecter les articles dans des feuilles de rangement et de prélèvement en classant les emplacements par ordre de priorité, de sorte que le programme propose de prendre ou de placer ces articles en fonction des critères de priorité pour utiliser l’espace de l’entrepôt de manière optimale.  

Les procédés de rangement sont optimisés en fonction de la priorité emplacement en suggérant des emplacements de priorité plus élevée avant les emplacements de priorité faible. De même, des procédés de prélèvement sont optimisés en proposant d’abord les articles du contenu des emplacements à priorité élevée. De plus, des réapprovisionnements d’emplacement sont suggérés à partir des emplacements de faible priorité à ceux de niveau élevé.  

La priorité emplacement ainsi que les informations relatives au contenu d’emplacement sont les propriétés de base permettant aux utilisateurs d’insérer des articles dans l’entrepôt.  

## <a name="bin-setup"></a>Paramétrage emplacement
Dans l’entreposage avancé, des emplacements peuvent être paramétrés à l’aide des valeurs de capacité, telles que la quantité, le volume total, ainsi que le poids pour contrôler quels articles sont enregistrés dans l’emplacement et comment.  

Sur chaque fiche article, vous pouvez affecter une unité de mesure de l’article, par exemple des pièces, palettes, litres, grammes ou boîtes. Vous pouvez également avoir une base UOM pour un article et spécifier de plus grands UOM basés dessus. Par exemple, vous pouvez définir une palette égale à 16 pièces, ce qui est l’unité de base.  

Si vous souhaitez définir une quantité maximum pour un article spécifique à enregistrer dans un emplacement particulier et que l’article a plusieurs unités, vous devez définir la quantité maximum de chaque unité qui existe dans la fiche article. Par conséquent, si un article a été configuré pour être traité en tant que pièces et palettes, le champ **Qté max.** de la page **Contenu emplacement** pour cet article doit également être considéré en tant que pièces et palettes. Sinon, la quantité autorisée pour cet emplacement n’est pas calculée correctement.  

Avant de paramétrer des restrictions de capacité pour le contenu d’emplacement dans un emplacement, vous devez d’abord vous assurer que les unités et les dimensions de l’article ont été définies dans la fiche article.  

> [!NOTE]  
> Il est possible d’utiliser plusieurs unités dans les installations WMS. Dans toutes les autres configurations, les contenus emplacement ne peuvent être que dans l’unité de base. Dans toutes les transactions avec une unité supérieure à l’unité de base de l’article, la quantité est transformée en unité de base.  

## <a name="zone"></a>Zone

Dans l’entreposage avancé, des emplacements peuvent être groupés dans des zones pour gérer la manière dont le flux de travail des activités entrepôt est suggéré.  

Une zone peut être une zone de réception ou une zone de stockage, et chaque zone peut comporter un ou plusieurs emplacements.  

La plupart des propriétés affectées à une zone par défaut sont affectées à l’emplacement qui est créé à partir de cette zone.  

## <a name="class"></a>Classe
Dans l’entreposage avancé, vous pouvez affecter des codes classe entrepôt aux articles, aux emplacements et aux zones pour contrôler l’endroit où les différentes classes d’article sont stockées, telles que les produits gelés. Vous pouvez diviser une zone en plusieurs classes d’entrepôt. Par exemple, des articles figurant dans la zone de réception peuvent être enregistrés comme gelés, dangereux ou autre classe.  

Lorsque vous travaillez sur des classes d’entrepôt et un emplacement de réception/expédition par défaut, vous devez renseigner manuellement les emplacements appropriés dans la réception entrepôt et des lignes expédition.  

En flux entrants, le code classe est uniquement sélectionné sur les lignes entrantes lorsque le code classe article ne correspond pas à l’emplacement de réception par défaut. Si les emplacements par défaut corrects ne sont pas affectés, la quantité ne peut pas être reçue.  

## <a name="location"></a>Magasin

Un magasin est une structure ou un lieu physique où le stock est reçu, conservé et expédié. Il est éventuellement organisé sous forme d’emplacements. Un magasin peut être un entrepôt, une voiture de service, une salle d’exposition, une usine ou une zone dans une usine.  

## <a name="first-expired-first-out"></a>FEFO (First-Expired-First-Out, premier expiré, premier sorti)

Si vous activez la case à cocher **Prélèvement selon FEFO** sur le raccourci **Config. emplacement** de la fiche magasin, les articles suivis sont prélevés en fonction de leur date d’expiration. Les articles dont les dates de péremption sont les plus proches sont prélevés en premier.  

Les activités d’entrepôt dans tous les document de prélèvement et de mouvement sont triées selon FEFO, à moins que les articles en question n’aient déjà des numéros de série/lot affectés. Si une partie seulement de la quantité de la ligne a déjà des numéros de série/lot affectés, la quantité restante à prélever est triée selon FEFO.  

Lors du prélèvement selon FEFO, les articles disponibles qui expirent en premier sont rassemblés dans une liste temporaire de traçabilité en fonction de la date d’expiration. Si deux articles ont la même date de péremption, l’article avec le plus petit numéro de lot ou de série est sélectionné en premier. Si les numéros de lot ou de série sont identiques, l’article enregistré en premier est sélectionné en premier. Les critères standard de sélection des articles dans les emplacements prélèvement, par exemple Priorité emplacement et Déconditionnement, sont appliqués à cette liste de traçabilité FEFO temporaire.  

## <a name="put-away-template"></a>Modèle rangement

Le modèle rangement peut être affecté à un article et à un magasin. Le modèle rangement spécifie un ensemble de règles classées par priorité qui doivent être respectées lors de la création de rangements. Par exemple, un modèle de rangement peut exiger que l’article soit situé dans un emplacement dont le contenu correspond à l’unité, et si un emplacement similaire comportant suffisamment de capacité est introuvable, alors l’article doit être placé dans un emplacement vide.  

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Détails de conception : disponibilité dans l’entrepôt](design-details-availability-in-the-warehouse.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
