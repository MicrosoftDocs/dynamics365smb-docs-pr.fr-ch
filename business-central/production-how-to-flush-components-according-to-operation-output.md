---
title: Consommer en aval des composants en fonction de la production réalisée
description: Cette rubrique décrit comment rincer les composants en fonction de la sortie de l’opération ainsi que d’autres méthodes de rinçage impliquées.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/22/2021
ms.author: bholtorf
---
# <a name="flush-components-according-to-operation-output"></a>Consommer en aval des composants en fonction de la production réalisée
Vous pouvez définir différentes stratégies de rinçage, pour automatiser l’enregistrement de la consommation des composants. 

Cette fonctionnalité est utile pour les motifs suivants :  

- **Évaluation du stock**

    Les écritures de valeur de production et de consommation sont créées parallèlement à l’état d’exécution de l’ordre de fabrication. Sans les codes lien gamme, la valeur du stock augmente lorsque la production est validée, puis réduit ultérieurement lorsque la valeur de la consommation des composants est validée en même temps que l’ordre de fabrication terminé.  
- **Disponibilité stock**

    Avec une validation progressive de la consommation, la disponibilité des composants est mieux actualisée, ce qui est important pour conserver l’équilibre interne entre l’offre et la demande. Sans les codes lien gamme, les autres demandeurs du composant peuvent croire qu’il est disponible tant que la validation de sa consommation reste en attente.  
- **À flux tendu**

    Si vous pouvez personnaliser les produits en fonction des demandes client, vous pouvez réduire les rebuts en vous organisant pour que les procédures de travail et les systèmes ne soient modifiés que lorsque c’est nécessaire.  

- **Réduire la saisie de données**

    La possibilité de consommer automatiquement une opération permet d’automatiser tout le processus d’enregistrement de la consommation et de la production. L’inconvénient de la consommation automatique est que vous risquez de ne pas enregistrer précisément voire d’omettre les rebuts.

## <a name="automatic-consumption-posting-flushing-methods"></a>Méthodes de validation de la consommation automatique (consommation)

- Consommation en aval de l’ordre entier  
- Consommation en aval par opération  
- Consommation en amont par opération  
- Consommation en amont de l’ordre entier  

### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Génération d’état automatique - Consommation en aval de l’ordre entier
Si vous consommez en aval l’ordre de fabrication au début du projet, le comportement l’application est très similaire à une consommation manuelle. La principale différence réside dans le fait que la consommation est effectuée automatiquement.  

- Le contenu entier de la nomenclature de production est consommé et déduit du stock lors de l’actualisation de l’ordre de fabrication lancé.  
- La quantité consommée est la quantité par assemblage indiquée dans la nomenclature de production, multipliée par le nombre d’articles parents que vous créez.  
- Il est inutile d’enregistrer des informations dans la feuille consommation si tous les articles doivent être consommés.  
- Lors de la consommation d’articles du stock, le moment où ont lieu les entrées de feuille production est sans importance parce que la feuille production n’a pas d’effet sur ce mode de validation de la consommation.  
- Aucun code lien gamme ne peut être défini.  

La consommation en aval d’une commande entière est appropriée dans des environnements de production présentant les caractéristiques suivantes :  

-   petit nombre de défauts ;  
-   petit nombre d’opérations ;  
-   consommation de composants importante dans les opérations précoces.  

### <a name="automatic-reporting---forward-flushing-by-operation"></a>Génération d’état automatique - Consommation en aval par opération
La consommation par opération permet de déduire le stock durant une opération spécifique dans la gamme de l’article parent. Les matières sont liées à la gamme à l’aide de codes lien gamme qui correspondent aux codes lien gamme appliqués aux composants dans la nomenclature de production.  

La consommation a lieu au démarrage de l’opération auquel le code lien gamme correspond. Le démarrage intervient quand une certaine activité est enregistrée dans la feuille production pour cette opération. Cette activité peut être simplement l’entrée d’un temps de préparation.  

La quantité consommée est calculée pour la quantité par assemblage sur la nomenclature de production multipliée par le nombre d’articles parents créés (quantité prévue).  

Il est recommandé d’utiliser cette technique lorsqu’il y a de nombreuses opérations et que certains composants ne sont nécessaires que vers la fin de la séquence d’assemblage. En réalité, dans le cadre d’une configuration à flux tendu (Just-in-Time, JIT), il se peut que les articles ne soient pas disponibles au début de la RPO.  

Il est possible de consommer des matières durant les opérations à l’aide de codes lien gamme. Il se peut que certains composants ne soient pas utilisés avant les opérations d’assemblage finales, auquel cas ils ne doivent pas être soustraits du stock auparavant.  

### <a name="automatic-reporting---back-flushing-by-operation"></a>Génération d’état automatique - Consommation en amont par opération
La consommation en amont par opération enregistre la consommation après la validation de l’opération dans la feuille production.  

L’avantage de cette méthode est que le nombre de pièces parentes finies dans l’opération est connu.  

Les matières dans la nomenclature de production sont liées aux enregistrements de gamme à l’aide de codes lien gamme. La consommation en amont a lieu lors de la validation d’une opération avec un code lien gamme particulier avec une quantité terminée.  

La quantité consommée est calculée pour la quantité par assemblage sur la nomenclature de production multipliée par le nombre d’articles parents validés comme quantité produite pour cette opération. Cette quantité peut différer de la quantité prévue.  

### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Génération d’état automatique - Consommation en amont de l’ordre entier
Cette méthode de génération d’état ne tient pas compte des codes lien gamme.  

Aucun composant n’est prélevé tant que le statut de l’ordre de fabrication lancé n’est pas *Terminé*. La quantité consommée est calculée pour la quantité par assemblage sur la nomenclature de production multipliée par le nombre d’articles parents terminés et introduits dans le stock.  

La consommation en amont de l’ordre de fabrication tout entier requiert la même configuration que pour la consommation en aval : la méthode de génération d’état doit être définie sur amont dans la fiche article de tous les articles de la nomenclature parente pour que l’état soit généré. En outre, tous les codes lien gamme doivent être supprimés de la nomenclature de production. 



Par exemple, si un ordre de fabrication de 800 mètres nécessite pour son exécution 8 kilogrammes d’un composant, lorsque vous validez 200 mètres de production, 2 kilogrammes sont automatiquement validés comme étant consommés. Pour y parvenir, combinez la méthode de consommation en amont et les codes lien gamme pour que la quantité consommée par chaque opération soit proportionnelle à la production réelle de cette opération terminée. Pour les articles créés avec la méthode de consommation en amont le comportement par défaut est de calculer et de valider la consommation de composants lorsque vous affectez à l’ordre de fabrication lancé le statut **Terminé**. Si vous définissez également les codes lien gamme, le calcul et la validation ont lieu lorsque chaque opération est terminée et la quantité effectivement consommée au cours de l’opération est validée. Pour plus d’informations, reportez-vous à [Créer des gammes](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Pour consommer en aval des composants en fonction de la production réalisée

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2.  Choisissez l’action **Modifier**.  
3.  Sur le raccourci **Réapprovisionnement**, dans le champ **Méthode consommation**, sélectionnez **En amont**.  

    > [!NOTE]  
    >  Sélectionnez **Prélèvement + Amont** si le composant est utilisé dans un magasin configuré pour un prélèvement et un rangement suggérés.  

4.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Gammes**, puis sélectionnez le lien associé.  
5.  Définir les codes lien gamme pour chaque opération qui consomme le composant. Pour plus d’informations, reportez-vous à [Créer des gammes](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > N’utilisez pas le même lien de gamme pour différentes opérations dans la gamme, car cela entraînera l’enregistrement de la consommation de composant pour chaque opération liée.  
6.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Nomenclature de production**, puis choisissez le lien associé.  
7.  Associe aux codes lien gamme de chaque instance du composant l’opération dans laquelle il est consommé.

La consommation sera affichée automatiquement lorsque vous enregistrez la sortie. Pour plus d’informations, voir [Valider par lots la production et les temps d’exécution](production-how-to-post-output-quantity.md)

## <a name="flushing-methods"></a>Méthodes consommation

Le tableau suivant décrit les options de méthode consommation disponibles que vous pouvez spécifier sur les cartes **Article** et **Unité de gestion des stocks**.

|Option|Description|
|------------|-------------|  
|Manuel|Requiert d’entrer et de valider manuellement la consommation dans la feuille consommation.|
|Aval|Valide automatiquement la consommation en fonction des lignes composant O.F. <br><br>Par défaut, la validation de la consommation de composants se produit lorsque vous basculez le statut de l’ordre de fabrication sur **Lancé**. Toutefois, si vous utilisez le champ Code **lien gamme** sur lignes composant O.F., la validation est effectuée par opération lorsque l’opération commence. Pour plus d’informations, reportez-vous à [Comment créer des liens gamme](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Remarque**<br>Pour la consommation en aval, la validation propre à chaque opération que vous obtenez avec des codes lien gamme est basée sur la quantité prévue définie sur la ligne composant. Pour plus d’informations sur la consommation en aval propre à l’opération sur la production réelle, reportez-vous à la description de **Amont** dans cette rubrique.<br><br>Si le magasin ou les ressources utilisant ce composant sont créées avec une structure d’emplacement par défaut, l’article est consommé à partir du **Code emplacement atelier ouvert**. Pour plus d’informations, voir [Procédure : configurer des entrepôts de base avec les zones d’opérations](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Important** <br>La consommation en aval se produit aussi lorsque vous choisissez **Actualiser** sur un ordre de fabrication lancé créé à partir de zéro. Sur ces écritures arrondies des O.F. lancés directement créés, vous ne pouvez pas modifier les informations sur les emplacements car les lignes composant O.F. sont générées lors de l’actualisation de la commande avec consommation en aval simultanée des composants. Toutefois, si vous souhaitez modifier les informations d’emplacement sur les lignes composant O.F. avant que la consommation en aval se produise, cette commande doit être créée avec le statut *Planifié* ou *Planifié ferme*.|
|Amont|Calcule et valide automatiquement la consommation en fonction des lignes composant O.F.<br><br> Par défaut, le calcul et la validation de la consommation de composants se produit lorsque vous basculez le statut de l’ordre de fabrication sur **Terminé**. Toutefois, si vous utilisez le champ **Code lien gamme** sur lignes composant O.F., le calcul et la validation sont effectués à la fin de chaque opération.<br><br> **Remarque** <br>Les codes de consommation en amont et de lien gamme peuvent être combinés afin que la quantité consommée par opération soit proportionnelle à la production réelle de cette opération. Pour plus d’informations, voir [Procédure : consommer en aval des composants en fonction de la production réalisée](#to-flush-components-according-to-operation-output).<br><br> Si le magasin ou le poste de charge utilisant ce composant sont créées avec une structure d’emplacement par défaut, l’article est consommé à partir du **Code emplacement atelier ouvert**.|
|Prélèvement + Aval|Identique à la méthode de consommation aval, sauf qu’elle ne fonctionne que pour les magasins qui utilisent une configuration d’entrepôt avancée ou une configuration d’entrepôt de base avec des emplacements obligatoires.<br><br> La consommation est calculée et validée à partir de l’emplacement défini dans le champ **Code empl. des consommations** sur le magasin ou le poste de charge après le prélèvement du composant de l’entrepôt.<br><br> **Remarque** <br>Si un composant est configuré avec le prélèvement et la méthode de consommation en aval, vous ne pouvez pas avoir un code lien gamme pour une opération configurée avec la méthode de consommation en aval. Le composant est ensuite automatiquement consommé lorsque l’opération commence, rendant impossible toute demande d’activité de prélèvement.|
|Prélèvement + Amont|Identique à la méthode de consommation amont, sauf qu’elle ne fonctionne que pour les magasins qui utilisent une configuration d’entrepôt avancée ou une configuration d’entrepôt de base avec des emplacements obligatoires.<br><br> La consommation est calculée et validée à partir de l’emplacement défini dans le champ **Code empl. des consommations** sur le magasin ou le poste de charge après le prélèvement du composant de l’entrepôt.|

## <a name="see-also"></a>Voir aussi

[Créer des nomenclatures de production](production-how-to-create-production-boms.md)  
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)  
[Planifié](production-planning.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
