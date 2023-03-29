---
title: "Détails de conception\_: modes évaluation stock"
description: Cette rubrique décrit en quoi le mode évaluation du stock affecte la façon dont les valeurs réelles et budgétées sont capitalisées et prises en compte dans le calcul des coûts.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 03/24/2022
ms.author: bholtorf
---
# Détails de conception : modes évaluation stock

Le mode évaluation stock détermine si une valeur réelle ou budgétée est capitalisée et prise en compte dans le calcul des coûts. Au même titre que la date comptabilisation et la séquence, le mode d’évaluation du stock a une incidence sur l’enregistrement du flux des coûts.

> [!NOTE]
> Vous ne pouvez pas modifier le mode évaluation stock d’un article si des écritures comptables article existent pour l’article. Pour plus d’informations, voir [Détails de conception : Modifier le mode évaluation stock des articles](design-details-changing-costing-methods.md).

Les méthodes suivantes sont prises en charge dans [!INCLUDE[prod_short](includes/prod_short.md)] :  

| Mode évaluation du stock | Description | Quand utiliser |
|--|--|--|
| FIFO | Le coût unitaire d’un article est la valeur réelle de toute réception de l’article, sélectionnée par la règle FIFO.<br /><br /> Dans l’évaluation du stock, nous considérons que les premiers articles stockés sont ceux vendus en premier. | Dans des environnements commerciaux où le coût de produit est stable.<br /><br /> (Lorsque les prix augmentent, le bilan indique une valeur plus élevée. Cela signifie que les impôts à payer augmentent, mais que les cotes de crédit et la capacité à emprunter de la trésorerie s’améliorent.)<br /><br /> Pour les articles à durée de conservation limitée, car les produits les plus anciens doivent être vendus avant que leur date limite de vente ne soit dépassée. |
| LIFO | Le coût unitaire d’un article est la valeur réelle de toute réception de l’article, sélectionnée par la règle LIFO.<br /><br /> Dans l’évaluation du stock, nous considérons que les derniers articles stockés sont ceux vendus en premier. | Interdit dans de nombreux pays/régions, car cela peut être utilisé pour réduire la marge.<br /><br /> (Lorsque les prix augmentent, la valeur du compte de gestion diminue. Cela signifie que les impôts à payer diminuent, mais que la capacité à emprunter de la trésorerie se détériore.) |
| Moyenne | Le coût unitaire d’un article est calculé comme le coût unitaire moyen à chaque moment après un achat.<br /><br /> Pour l’évaluation du stock, on part de l’hypothèse que tous les stocks sont vendus simultanément. | Dans des environnements commerciaux où le coût de produit est instable.<br /><br /> Lorsque les stocks sont compilés ou mélangés ensemble et ne peuvent pas être différenciés (par exemple, des produits chimiques). |
| Spécifique | Le coût unitaire d’un article est le coût exact auquel l’unité particulière a été reçue. | Pour la fabrication ou la transaction d’articles facilement identifiables ayant des coûts unitaires assez élevés.<br /><br /> Pour les articles soumis à une régulation.<br /><br /> Pour les articles ayant des numéros de série. |
| Standard | Le coût unitaire d’un article est prédéfini sur la base d’une estimation.<br /><br /> Lorsque le coût réel est réalisé plus tard, le coût standard doit être ajusté au coût réel à l’aide des valeurs d’écart. | Environnement où le contrôle des coûts est primordial.<br /><br /> Pour la fabrication répétitive, afin d’évaluer les coûts matière directs, les frais de main-d’œuvre directs, et les frais généraux matière.<br /><br /> Environnement où il existe une discipline et du personnel pour le maintien des standards. |

L’image suivante montre la manière dont les coûts circulent dans le stock pour chaque mode d’évaluation du stock.  

![Visualisation des modes évaluation stock.](media/design_details_inventory_costing_7_costing_methods.png "Visualisation des modes évaluation stock")  

Les méthodes d’évaluation du stock diffèrent dans la façon d’évaluer les sorties de stock et d’utiliser le coût réel ou le coût standard comme base d’évaluation. Le tableau suivant explique les différentes caractéristiques. (La méthode LIFO est exclue, car elle est presque identique à la méthode FIFO).  

|Catégorie|FIFO|Moyenne|Standard|Spécifique|  
|-|----------|-------------|--------------|--------------|  
|Caractéristiques générales|Facile à comprendre|Sur la base des options de période : **Jour**/**Semaine**/**Mois**/**Trimestre**/**Période comptable**.<br /><br /> Peut être calculé par article ou par article/magasin/variante.|Facile à utiliser, mais requiert une maintenance qualifiée.|Requiert une traçabilité à la fois sur les transactions entrante et sortante.<br /><br /> Généralement utilisé pour les articles fabriqués de série.|  
|Lettrage/Ajustement|Le lettrage effectue le suivi de **la quantité restante**.<br /><br /> L’ajustement transfère les coûts en fonction de l’application de quantité.|Le lettrage effectue le suivi de la **quantité restante**.<br /><br /> Les coûts sont calculés et transférés par **date d’évaluation**.|Le lettrage effectue le suivi de la **quantité restante**.<br /><br /> Le lettrage est basé sur la méthode FIFO.|Tous les lettrages sont fixes.|  
|Réévaluation|Réévalue uniquement la quantité facturée.<br /><br /> Peut être effectué par article ou par écriture comptable article.<br /><br /> Peut être fait à une date antérieure.|Réévalue uniquement la quantité facturée.<br /><br /> Peut être effectué par article uniquement.<br /><br /> Peut être fait à une date antérieure.|Réévalue les quantités facturées et non facturées.<br /><br /> Peut être effectué par article ou par écriture comptable article.<br /><br /> Peut être fait à une date antérieure.|Réévalue uniquement la quantité facturée.<br /><br /> Peut être effectué par article ou par écriture comptable article.<br /><br /> Peut être fait à une date antérieure.|  
|Charges diverses de gestion|Si vous antidatez une sortie de stock, les écritures existantes ne sont PAS relettrées pour présenter un flux de coût FIFO correct.|Si vous antidatez une entrée ou une sortie de stock, le coût moyen est recalculé, et toutes les écritures affectées sont ajustées.<br /><br /> Si vous modifiez la période ou un type de calcul, toutes les écritures affectées doivent être ajustées.|Utilisez la page **Feuille standard** pour régulièrement mettre à jour et rouler les coûts standard.<br /><br /> N’est PAS pris en charge par le point de stock.<br /><br /> Aucun enregistrement historique n’existe pour les coûts standard.|Vous pouvez utiliser le suivi d’article spécifique sans utiliser le mode d’évaluation spécifique. Alors le coût ne suit PAS le numéro de lot, mais l’acceptation du coût du mode d’évaluation sélectionné.|  

## Exemple :

Cette section donne des exemples de la manière dont les divers modes d’évaluation affectent la valeur stock.  

Le tableau suivant montre les entrées et les sorties de stock sur lesquels les exemples sont basés.  

|Date comptabilisation|Quantité|Numéro de la séquence|  
|------------------|--------------|---------------|  
|01/01/20|1|1|  
|01/01/20|1|2|  
|01/01/20|1|3|  
|01/02/20|-1|4|  
|01/03/20|-1|5|  
|01/04/20|-1|6|  

> [!NOTE]  
> La quantité qui en résulte dans le stock est égale à zéro. Par conséquent, la valeur du stock doit également être zéro, quel que soit le mode évaluation stock.  

### Effet des modes évaluation stock sur l’évaluation des entrées de stock  

Pour les articles utilisant les modes évaluation stock qui utilisent le coût réel comme base d’évaluation (**FIFO**, **LIFO**, **Moyenne** ou **Spécifique**), les entrées de stock sont évaluées au coût d’acquisition de l’article.  

- **Standard**  

    Pour les articles qui utilisent le mode d’évaluation du stock **Standard**, les entrées de stock sont évaluées au coût standard actuel de l’article.  

#### Standard  

Pour les articles qui utilisent le mode d’évaluation stock **Standard**, les entrées de stock sont évaluées au coût standard actuel de l’article.  

### Effet des modes évaluation stock sur l’évaluation des sorties de stock

- **FIFO**  

    Pour les articles utilisant le mode évaluation stock **FIFO**, les articles achetés en premier sont toujours les premiers vendus (numéros de séquence 3, 2 et 1, dans cet exemple). Par conséquent, les sorties de stock sont évaluées en prenant en compte la valeur de la première entrée de stock.  

     La valeur sortie stock est calculée à l’aide de la valeur des premières acquisitions de stock.  

     Le tableau suivant montre la manière dont les sorties de stock sont évaluées pour le mode d’évaluation du stock **FIFO**.  

    |Date comptabilisation|Quantité|Coût total (réel)|Numéro de la séquence|  
    |------------------|--------------|----------------------------|---------------|  
    |01/02/20|-1|-10,00|4|  
    |01/03/20|-1|-20,00|5|  
    |01/04/20|-1|-30,00|6|  

- **LIFO**  

    Pour les articles utilisant le mode évaluation stock **LIFO**, les articles achetés le plus récemment sont toujours les premiers vendus (numéros de séquence 3, 2 et 1, dans cet exemple). Par conséquent, les sorties de stock sont évaluées en prenant en compte la valeur de la dernière entrée de stock.  

     La valeur sortie stock est calculée à l’aide de la valeur des acquisitions de stock les plus récentes.  

     Le tableau suivant montre la manière dont les sorties de stock sont évaluées pour le mode d’évaluation du stock **LIFO**.  

    |Date comptabilisation|Quantité|Coût total (réel)|Numéro de la séquence|  
    |------------|--------|--------------------|---------|  
    |01/02/20|-1|-30,00|4|  
    |01/03/20|-1|-20,00|5|  
    |01/04/20|-1|-10,00|6|  

- **Moyenne**  

    Pour les articles qui utilisent le mode d’évaluation du stock **Moyen**, les sorties de stock sont évaluées en calculant la moyenne pondérée du stock restant au dernier jour de la période coût moyen dans laquelle la sortie de stock a été validée. Pour plus d’informations, voir [Détails de conception : coût moyen](design-details-average-cost.md).  

     Le tableau suivant montre la manière dont les sorties de stock sont évaluées pour le mode d’évaluation du stock **Moyen**.  

    | Date comptabilisation | Quantité | Coût total (réel) | Numéro de la séquence |
    |--|--|--|--|
    | 01/02/20 | -1 | -20,00 | 4 |
    | 01/03/20 | -1 | -20,00 | 5 |
    | 01/04/20 | -1 | -20,00 | 6 |

- **Standard**  

    Pour les articles utilisant le mode évaluation stock **Standard**, les sorties de stock sont évaluées de manière similaire au mode évaluation stock **FIFO**, sauf que l’évaluation est basée sur un coût standard, pas sur le coût réel.  

    Le tableau suivant montre la manière dont les sorties de stock sont évaluées pour le mode d’évaluation du stock **Standard**.  

    |Date comptabilisation|Quantité|Coût total (réel)|Numéro de la séquence|  
    |------------------|--------------|----------------------------|---------------|  
    |01/02/20|-1|-15,00|4|  
    |01/03/20|-1|-15,00|5|  
    |01/04/20|-1|-15,00|6|  

- **Spécifique**  

    Les modes d’évaluation du stock partent du principe que les coûts vont de l’entrée de stock vers la sortie de stock. Toutefois, si plus d’informations précises sur le flux des coûts ont été créées, vous pouvez remplacer cette supposition en créant un lettrage fixe entre les écritures. Un lettrage fixe crée un lien entre une sortie de stock et une entrée de stock spécifique, et supervise le flux des coûts en conséquence.  

    Pour les articles utilisant le mode évaluation stock **Spécifique**, les sorties de stock sont évaluées en fonction de l’entrée de stock qui est liée par le lettrage fixe.  

    Le tableau suivant montre la manière dont les sorties de stock sont évaluées pour le mode d’évaluation du stock **Spécifique**.  

    |Date comptabilisation|Quantité|Coût total (réel)|Ecriture lettrage|Numéro de la séquence|
    |------------|--------|--------------------|----------------|---------|  
    |01/02/20|-1|-20,00|**2**|4|  
    |01/03/20|-1|-10,00|**1**|5|  
    |01/04/20|-1|-30,00|**3**|6|  

## Voir aussi

 [Détails de conception : évaluation stock](design-details-inventory-costing.md)   
 [Détails de conception : écart](design-details-variance.md)   
 [Détails de conception : coût moyen](design-details-average-cost.md)   
 [Détails de conception : lettrage article](design-details-item-application.md)  
 [Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
 [Finances](finance.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]