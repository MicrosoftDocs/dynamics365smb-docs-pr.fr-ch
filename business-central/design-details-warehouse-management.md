---
title: Gérer les activités entrepôt
description: 'Outre les réceptions et les expéditions, Business Central prend en charge une série d’activités d’entrepôt internes.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/09/2023
ms.custom: bap-template
---

# <a name="warehouse-management-overview"></a>Vue d’ensemble de la gestion des entrepôts

Deux choses sont importantes pour toutes les entreprises qui transportent physiquement des marchandises dans et hors de leur entrepôt :

* Elles ont une vue d’ensemble des niveaux de stock et du placement des articles dans l’entrepôt.
* Elles peuvent recevoir, prélever et expédier des articles rapidement et avec précision.

Pour aider les entreprises à atteindre ces objectifs, les fonctionnalités d’entrepôt dans [!INCLUDE[prod_short](includes/prod_short.md)] ajoutent les fonctionnalités suivantes à la gestion des stocks :

* Emplacements
* Expéditions entrepôt
* Prélèvements stock
* Feuille mouvement

Implémentez ces fonctionnalités dans différentes combinaisons pour adapter vos processus d’entrepôt à votre entreprise. Permettez une complexité croissante à mesure que votre entreprise se développe et que vos processus évolue.

## <a name="overview-of-different-configuration-options"></a>Aperçu des différentes options de configuration

Vous pouvez configurer les fonctionnalités d’entrepôt de différentes manières. Il est important de choisir les options qui améliorent vos processus sans entraîner de surcharge. Le tableau suivant donne un aperçu des configurations typiques lorsqu’il s’agit de biens physiques.

|Niveau de complexité|Désignation|Paramètres|Code emplacement|Exemple de flux entrant|Exemple de flux sortant|Exemple de flux interne|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Aucune activité entrepôt dédiée.|Validation à partir des ordres et des feuilles.||Facultatif. Contrôlé par le bouton à bascule **Code emplacement obligatoire**.|Commande achat|Commande vente| Ordre de fabrication -> Feuille consommation|  
|Basique|Envoi/réception regroupés pour plusieurs commandes.|**Réception requise**<br>**Expédition requise**.|Facultatif. Contrôlé par le bouton à bascule Code emplacement obligatoire|Commande(s) achat -> Réception entrepôt|Commande vente -> Expédition entrepôt|Comme ci-dessus.|
|Basique|Commande par commande.|Rangement requis ou Prélèvement requis. </br><br/> **REMARQUE** : bien que les paramètres soient appelés **Prélèvement requis** et **Rangement requis**, vous pouvez quand même valider les réceptions et les expéditions directement à partir des documents origine dans les magasins où vous cochez ces cases.|Facultatif. Contrôlé par le bouton à bascule **Code emplacement obligatoire**.|Commande achat -> Rangement stock|Commande vente -> Prélèvement stock|Ordre de fabrication -> Prélèvement stock|
|Avancé|Envoi/réception regroupés pour plusieurs commandes.<br /><br />Activités de prélèvement/rangement regroupées pour plusieurs documents origine.|Réception requise + Rangement requis,</br> Expédition requise + Prélèvement requis|Facultatif. Contrôlé par le bouton à bascule Code emplacement obligatoire|Commande(s) achat -> Réception entrepôt -> Rangement entrepôt|Commande(s) vente -> Expédition(s) entrepôt -> Feuille prélèvement -> Prélèvement(s) entrepôt| Ordre de fabrication -> Feuille prélèvement -> Prélèvement(s) entrepôt -> Feuille consommation|
|Avancé|Comme ci-dessus + activités de prélèvement/rangement dirigées|Prélèvement et rangement dirigés (les boutons à bascule dépendants seront activés automatiquement)|Obligatoire|Comme ci-dessus.|Comme ci-dessus.| Ordre de fabrication -> Feuille prélèvement -> Prélèvement(s) entrepôt -> Feuille consommation|

La complexité augmente avec la taille de votre organisation et le nombre de départements et de personnes impliqués. Un processus peut être simple, par exemple, lorsque la même personne crée et publie un document de vente. Les processus peuvent également être plus complexes et impliquer plusieurs étapes et personnes. Les étapes suivantes sont un exemple de processus plus complexe :

1. Un préparateur de commandes crée une commande vente.
1. Un responsable d’entrepôt crée des instructions de prélèvement.
1. Un magasinier termine le flux en validant l’expédition de l’entrepôt.

Le niveau de complexité est également affecté par les types de documents que vous utilisez dans vos activités d’entrepôt. Par exemple, vous pouvez utiliser des documents de réception entrepôt et de rangement entrepôt pour votre flux entrant, mais utiliser des documents de prélèvement stock pour votre flux sortant.

Un autre facteur qui influe sur la complexité est la façon dont votre entrepôt physique est représenté dans [!INCLUDE[prod_short](includes/prod_short.md)]. Learn more at [Modélisation de l’entrepôt physique](#modeling-the-physical-warehouse).

## <a name="modeling-the-physical-warehouse"></a>Modélisation de l’entrepôt physique

Vous disposez de plusieurs options pour représenter la configuration réelle de votre entrepôt dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vos choix déterminent la manière dont vous utiliserez les fonctionnalités de l’entrepôt.

Le placement des articles peut être sur des étagères, dans des magasins ou dans des emplacements, et chaque option présente des avantages et des inconvénients.

### <a name="locations-and-bins"></a>Magasins et emplacements

Pour manipuler des biens physiques, vous devez avoir au moins un magasin. Vous pouvez utiliser plusieurs magasins ou utiliser des emplacements pour modéliser votre entrepôt et votre structure organisationnelle.

En règle générale, les magasins sont le moyen privilégié pour organiser des opérations réparties sur plusieurs zones géographiques. Dans certains cas, cependant, vous souhaiterez peut-être créer plusieurs magasins situés au même endroit. L’utilisation des magasins présente les avantages suivants :

* Accordez l’accès en utilisant les pages **Magasiniers** et **Centres de gestion** pages.
* Définissez les calendriers, les routages et les heures de traitement entrant et sortant pour le calcul et la planification des dates. Pour plus d’informations, voir [À propos de la fonctionnalité Planification](production-about-planning-functionality.md).
* Spécifiez les axes analytiques par défaut et utilisez différentes configurations de validation de stock.
* Configurez les paramètres de planification. Learn more at [Paramètres de planification](production-about-planning-functionality.md#planning-parameters).  
* Utilisez différentes fonctionnalités d’entrepôt pour chaque magasin.

### <a name="shelves-and-bins"></a>Étagères et emplacements

Si vous stockez toujours un article au même endroit, vous pouvez utiliser le champ **N° d’étagère** sur les pages **Fiche article** ou **Fiche point de stock**. Ce champ peut être utilisé comme système d’enregistrement manuel de base dans des environnements sans emplacement. La valeur du champ est copiée à partir de la fiche article vers les lignes document et les états, mais à titre informatif uniquement. La valeur n’est pas utilisée dans les activités d’entrepôt ou dans les calculs de disponibilité.

Les emplacements représentent la structure d’entrepôt de base et sont utilisés pour faire des propositions relatives à l’emplacement des articles :

* Un ou plusieurs emplacements fixes pour un article.
* Les emplacements pour des opérations spécifiques, comme un emplacement d’expédition ou un emplacement de sortie de production.
* Des restrictions de capacité et de poids des emplacements (uniquement pour le rangement et le prélèvement dirigés).
* Classement des emplacements (pour le rangement et le prélèvement dirigés uniquement).

## <a name="typical-warehouse-workflow"></a>Flux de travail typique d’un entrepôt

Le tableau suivant décrit une série de tâches et inclut des liens vers les articles qui les décrivent.

|**À**|**Voir**|  
|------------|-------------|  
|Dans un flux de base, selon le principe de commande par commande, utilisez un rangement stock pour enregistrer la réception des articles dans les magasins, y compris toute réception excédentaire. Ou, si vous regroupez plusieurs commandes dans la réception, utilisez une réception entrepôt.|[Flux entrant](design-details-inbound-warehouse-flow.md)|
|Enregistrez l’expédition des articles à partir des magasins d’entrepôt. Sur le principe de commande par commande, utilisez un prélèvement stock. Ou, si vous regroupez plusieurs commandes dans l’expédition, utilisez une expédition entrepôt.|[Flux sortant](design-details-outbound-warehouse-flow.md)|
|Manipulez les articles dans le magasin d’entrepôt. Par exemple, lorsque vous déplacez des composants vers la production ou effectuez un inventaire physique.|[Flux interne](design-details-internal-warehouse-flows.md)|

Configurez les processus d’entrepôt qui conviennent à votre entreprise. Learn more at [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

## <a name="terminology-related-to-warehouse-management"></a>Terminologie liée à la gestion d’entrepôt

### <a name="complexity-levels"></a>Niveaux de complexité

Nous utilisons les termes « de base » et « avancé » pour différencier les niveaux de complexité. Cette différenciation simple couvre plusieurs niveaux de complexité dans les configurations de magasin, chacune prise en charge par différents documents d’entrepôt. Le niveau d’entreposage le plus avancé est appelé « Rangement et prélèvement dirigés ׃. Pour utiliser le rangement et le prélèvement dirigés pour un emplacement, activez le bouton à bascule **Rangement et prélèvement dirigés** sur la page **Fiche magasin**.

### <a name="warehouse-flows"></a>Flux d’entrepôt

* Flux entrant : déplace les articles vers le magasin d’entrepôt et les rend disponibles, par exemple pour les achats et les transferts entrants.
* Flux sortant : prélève et expédie les articles aux clients ou à d’autres magasins.
* Flux interne : gère les articles au sein d’un magasin. Par exemple, vous déplacez des composants vers la production ou effectuez un inventaire physique.

### <a name="basic-documents"></a>Documents de base

Les documents suivants sont utilisés dans les flux d’entrepôt de base.

* Rangmt stk invent
* Prélvmt invent
* Mouvement de stock
* Feuille article
* Feuille reclassement article

### <a name="advanced-documents"></a>Documents avancés

Les documents suivants sont utilisés dans les flux d’entrepôt avancés.

* Réception entrepôt
* Feuille rangement
* Rangement entrepôt
* Feuille prélèvement
* Prélèvement entrepôt
* Feuille mouvement
* Mouvement entrepôt
* Prélèvement entrepôt interne
* Rangement entrepôt interne
* Feuille création emplacement
* Feuille création contenu emplacement
* Feuille article entrepôt
* Feuilles reclassement article entrepôt

### <a name="pages-and-settings"></a>Pages et paramètres

Cette section décrit les concepts sous-jacents aux pages et paramètres clés pour l’entreposage.

#### <a name="bins-and-bin-content"></a>Emplacements et Contenu emplacement

Un emplacement est un dispositif de stockage conçu pour contenir des éléments discrets. Il s’agit de la plus petite unité de conteneur dans [!INCLUDE[prod_short](includes/prod_short.md)]. Les quantités d’articles dans les emplacements sont appelées *contenu de l’emplacement*. Une recherche à partir du champ **Article** ou du champ **Code emplacement** dans n’importe quel document entrepôt affiche la disponibilité calculée de l’article dans l’emplacement.  

Le contenu de l’emplacement peut être **Fixe**, **Dédié** ou **Par défaut** pour définir comment utiliser le contenu de l’emplacement. Les emplacements sans aucune de ces propriétés sont appelés emplacements *dynamiques*.  

Un emplacement statique contient les articles affectés au code emplacement concerné. La propriété d’emplacement statique garantit que même si l’emplacement est vidé, le contenu de l’emplacement ne disparaît pas. Vous pouvez sélectionner à nouveau l’emplacement dès que son contenu est réapprovisionné.  

Un emplacement dédié contient ce qui peut être prélevé pour la ressource dédiée qui utilise l’emplacement. Par exemple, un poste de charge. Un autre contenu non-prélèvement, tel que les quantités sortantes sur une validation expédition, peut être consommé à partir d’un emplacement dédié. Seul le contenu de l’emplacement pris en compte par l’algorithme **Créer prélèvement** est protégé dans un emplacement dédié.  

[!INCLUDE [prod_short](includes/prod_short.md)] utilise la propriété d’emplacement **Par défaut** pour proposer des emplacements pour les activités de l’entrepôt. Dans les magasins qui utilisent le rangement et le prélèvement dirigés, la propriété d’emplacement par défaut n’est pas utilisée. Dans les magasins où des emplacements sont requis, la propriété indique où placer les articles dans les flux entrants. Dans les flux sortants, la propriété indique l’endroit où prendre des articles.  

> [!NOTE]  
> Si les articles sortants sont stockés dans plusieurs emplacements, les articles sont d’abord pris dans les emplacements non définis par défaut, pour vider le contenu de ces emplacements, puis les articles restants sont pris dans l’emplacement par défaut.  

Il ne peut y avoir qu’un emplacement par défaut par article et par magasin.  

#### <a name="bin-type"></a>Type emplacement

Les magasins qui utilisent le rangement et le prélèvement dirigés peuvent utiliser des types d’emplacement. Les types d’emplacement contrôlent les activités que vous autorisez pour un emplacement. Les types d’emplacement disponibles sont les suivants :  

|Type emplacement|Description|  
|------------------|---------------------------------------|  
|RECEPTION|Articles reçus mais non rangés.|  
|EXPED.|Articles prélevés pour des lignes expédition entrepôt, mais pas encore validés comme expédiés.|  
|RANG.|Généralement, les articles devant être stockés dans de grandes unités, mais auxquels vous ne souhaitez pas accéder à des fins de prélèvement. Ces emplacements ne sont pas utilisés pour le prélèvement, que ce soit pour les ordres de fabrication ou les expéditions ; leur utilisation peut donc être limitée. Ce type d’emplacement est utile lorsque vous achetez une grande quantité d’articles. Les emplacements doivent toujours avoir un rang d’emplacement bas, de sorte que les articles avec des emplacements PUTPICK de rang supérieur soient rangés en premier. Réapprovisionnez régulièrement ce type d’emplacement afin que leurs articles soient disponibles dans des emplacements de type PUTPICK ou PICK.|  
|PRELEVEMT|Articles à utiliser uniquement pour prélever. Vous ne pouvez utiliser les mouvements que pour le réapprovisionnement de ces emplacements, pas pour le rangement.|  
|RANGPRELEV.|Articles dans des emplacements qui sont proposés à la fois pour le rangement et le prélèvement. Les emplacements de ce type ont vraisemblablement un classement différent. Configurez vos emplacements de stockage en vrac avec des classements d’emplacement inférieurs à ceux des emplacements de prélèvement ordinaires ou des emplacements dans votre zone de prélèvement ava.|  
|CQ|Cet emplacement est utilisé pour des ajustements stock, si vous le spécifiez sur la fiche magasin dans le champ **Code empl. ajustement**. Vous pouvez également configurer des emplacements de ce type pour des articles défectueux ou en cours de contrôle. vous pouvez déplacer des articles vers ce type d’emplacement afin que la circulation habituelle des articles ne puisse pas y accéder. **Remarque :** contrairement à tous les autres types d’emplacement, les cases à cocher pour le traitement des articles sont toutes désactivées par défaut pour le type **CQ**. Le contenu que vous placez dans un emplacement CQ est exclu des flux d’article.|  

À l’exception des types d’emplacements PICK, PUTPICK et PUTAWAY, le type d’emplacement définit l’activité autorisée pour un emplacement. Par exemple, vous ne pouvez utiliser qu’un type d’emplacement RECEIVE pour recevoir des articles ou pour en prélever des articles.  

> [!NOTE]  
> Vous devez utiliser des mouvements pour déplacer les articles vers les emplacements RECEIVE et CQ. Utilisez des mouvements pour déplacer des articles des emplacements SHIP et CQ.  

#### <a name="bin-ranking"></a>Priorité emplacement

Dans l’entreposage avancé, vous pouvez automatiser et optimiser la collecte des articles dans les feuilles rangement et prélèvement en classant les emplacements. Les articles sont suggérés pour les prélèvements et les rangements en fonction du rangs des emplacements.

Les procédés de rangement sont optimisés en fonction de la priorité emplacement en suggérant des emplacements de priorité plus élevée avant les emplacements de priorité faible. Les procédés de prélèvement suggèrent en premier les articles ayant le classement d’emplacement le plus élevé dans le contenu d’emplacement. Le réapprovisionnement des emplacements suggère les emplacements de rang inférieur avant les emplacements de rang supérieur.  

Le classement et le contenu des emplacements sont les propriétés de base qui guident les magasiniers dans l’entrepôt.  

#### <a name="bin-setup"></a>Paramétrage emplacement

Dans l’entreposage avancé, vous pouvez spécifier les valeurs de capacité suivantes pour contrôler comment et dans quels emplacements vous stockez les articles :

* Quantité
* Cubage total
* Poids  

Vous pouvez attribuer une unité de mesure de base aux articles. Une unité de mesure de base peut être constituée de pièces, de palettes, de litres, de grammes ou de boîtes. Vous pouvez également créer des unités de mesure plus grandes en fonction de votre unité de mesure de base. Par exemple, si les pièces sont votre unité de mesure de base, une palette peut être égale à 16 pièces.  

Si un article a plusieurs unités de mesure, définissez la quantité maximale pour chaque unité de mesure sur la fiche article. Si vous manipulez un article sous forme de pièces et de palettes, le champ **Qté max.** de la page **Contenu emplacement** pour cet article doit également être défini en pièces et en palettes. Sinon, la quantité autorisée pour cet emplacement n’est pas calculée correctement.  

Avant de paramétrer des restrictions de capacité pour le contenu d’emplacement dans un emplacement, assurez-vous que les unités de mesure et les dimensions de l’article ont été définies dans la fiche article.  

> [!NOTE]  
> Vous ne pouvez utiliser plusieurs unités de mesure que dans les magasins qui utilisent le rangement et le prélèvement dirigés. Dans toutes les autres configurations, les contenus emplacement ne peuvent être que dans l’unité de mesure de base. Dans les transactions avec une unité de mesure supérieure à l’unité de mesure de base de l’article, la quantité est transformée en unité de mesure base.  

#### <a name="zone"></a>Zone

Dans l’entreposage avancé, des emplacements peuvent être groupés en zones pour gérer la manière dont le flux de travail des activités entrepôt est suggéré pour les magasins.  

Une zone peut être une zone de réception ou une zone de stockage, et chaque zone peut comporter un ou plusieurs emplacements.  

La plupart des propriétés affectées à une zone sont affectées aux emplacements créés pour la zone.  

#### <a name="warehouse-class"></a>Classe entrepôt

Dans l’entreposage avancé, vous pouvez affecter des codes de classe d’entrepôt aux entités suivantes : 

* Articles
* Emplacements
* Zones

Les classes d’entrepôt contrôlent où stocker les articles. Vous pouvez diviser une zone en plusieurs classes d’entrepôt. Par exemple, vous pouvez stocker des articles dans la zone de réception dans la classe gelé, dangereux ou autre.

Lorsque vous travaillez sur des classes d’entrepôt avec un emplacement de réception/expédition par défaut, vous devez choisir manuellement les emplacements appropriés dans la réception entrepôt et les lignes expédition.  

En flux entrants, le code classe est uniquement sélectionné sur les lignes entrantes lorsque le code classe article ne correspond pas à l’emplacement de réception par défaut. Si les emplacements par défaut corrects ne sont pas affectés, la quantité ne peut pas être reçue.  

#### <a name="location"></a>Magasin

Un magasin est une structure physique ou un lieu où le stock est reçu, stocké et expédié. Un magasin peut être un entrepôt, une voiture de service, une salle d’exposition, une usine ou une zone d’une usine. Le stock est souvent organisé en emplacements et en zones.

#### <a name="first-expired-first-out"></a>FEFO (First-Expired-First-Out, premier expiré, premier sorti)

Si vous activez la case à cocher **Prélèvement selon FEFO** sur le raccourci **Config. emplacement** de la page **Fiche magasin**, les articles suivis sont prélevés dans le magasin en fonction de leur date d’expiration. Les articles dont les dates de péremption sont les plus proches sont prélevés en premier.  

Les activités d’entrepôt dans tous les document de prélèvement et de mouvement sont triées selon FEFO, à moins que les articles en question n’aient des numéros de série ou de lot affectés. Si une partie seulement de la quantité de la ligne a des numéros de série ou de lot affectés, la quantité restante est triée selon FEFO.  

Lors du prélèvement selon FEFO, les articles qui expirent en premier sont rassemblés dans une liste temporaire de traçabilité en fonction de la date de péremption. Si deux articles ont la même date de péremption, l’article avec le plus petit numéro de lot ou de série est sélectionné en premier. Si les numéros de lot ou de série sont identiques, l’article enregistré en premier est sélectionné en premier. Les critères standard de sélection des articles dans les emplacements prélèvement, par exemple Priorité emplacement et Déconditionnement, sont appliqués à la liste de traçabilité FEFO temporaire.  

#### <a name="put-away-template"></a>Modèle rangement

Les modèles de rangement spécifient un ensemble de règles de priorité qui s’appliquent lorsque vous créez des rangements. Par exemple, un modèle de rangement peut vous obliger à placer des articles dans un emplacement dont le contenu a la même unité de mesure. S’il est impossible de trouver un emplacement similaire d’une capacité suffisante, l’article doit être placé dans un emplacement vide. Vous affectez un modèle de rangement à un article et à un magasin.  

## <a name="see-also"></a>Voir aussi

[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
