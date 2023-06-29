---
title: "Détails de conception\_:\_arrondi"
description: Des reliquats d’arrondi peuvent se produire lorsque vous évaluez le coût d’une sortie de stock qui est mesurée dans une quantité différente de l’entrée de stock correspondante.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-rounding"></a><a name="design-details-rounding"></a>Détails de conception : arrondi
Des reliquats d’arrondi peuvent se produire lorsque vous évaluez le coût d’une sortie de stock qui est mesurée dans une quantité différente de l’entrée de stock correspondante. Les reliquats d’arrondi sont calculés pour tous les modes d’évaluation du stock lorsque vous exécutez le traitement par lots **Ajuster coûts - Écr. article**.  

 Lorsque vous utilisez le mode d’évaluation moyen, le montant résiduel est calculé et enregistré sur une base cumulative écriture par écriture.  

 Lorsque vous utilisez un mode d’évaluation autre qu’Average, le montant résiduel est calculé lorsque l’augmentation de stock a été totalement appliquée, c’est-à-dire lorsque la quantité restante pour l’augmentation de stock est égale à zéro. Une écriture distincte est ensuite créée pour l’arrondi résiduel, et la date de comptabilisation de l’écriture arrondie représente la date de comptabilisation de la dernière écriture valeur facturée de l’entrée de stock.  

## <a name="example"></a><a name="example"></a>Exemple :
 L’exemple suivant présente la manière dont les différents reliquats d’arrondi sont traités pour le mode évaluation stock moyen et pour le mode évaluation stock non moyen, respectivement. Dans les deux cas, le traitement par lots **Ajuster coûts - Écr. article** a été exécuté.  

 Le tableau suivant répertorie les écritures comptables article sur lesquelles l’exemple est basé.  

|Date comptabilisation|Quantité|Numéro de la séquence|  
|------------------|--------------|---------------|  
|01/01/20|3|1|  
|01/02/20|-1|2|  
|01/03/20|-1|3|  
|01/04/20|-1|4|  

 Pour un article utilisant le mode évaluation stock moyen, l’arrondi résiduel (1/300) est calculé avec la première diminution (numéro de séquence 2) et est reporté sur le numéro de séquence 3. Par conséquent, le numéro de séquence 3 est évalué à –3,34.  

 Le tableau suivant montre les écritures valeur résultantes.  

|Date comptabilisation|Quantité|Coût total (réel)|N° écriture comptable article|Numéro de la séquence|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01/01/20|3|10|1|1|  
|01/02/20|-1|-3,33|2|2|  
|01/03/20|-1|-3,34|3|3|  
|01/04/20|-1|-3,33|4|4|  

 Pour un article utilisant un mode évaluation stock autre que moyen, l’arrondi résiduel (0,01) est calculé lorsque la quantité restante pour l’entrée de stock est égale à zéro. Le montant résiduel a une écriture distincte (numéro 5).  

 Le tableau suivant montre les écritures valeur résultantes.  

|Date comptabilisation|Quantité|Coût total (réel)|N° écriture comptable article|Numéro de la séquence|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01/01/20|3|10|1|1|  
|01/02/20|-1|-3,33|2|2|  
|01/03/20|-1|-3,33|3|3|  
|01/04/20|-1|-3,33|4|4|  
|01/01/20|0|-0,01|1|5|  

## <a name="see-also"></a><a name="see-also"></a>Voir aussi
 [Détails de conception : évaluation stock](design-details-inventory-costing.md)   
 [Détails de conception : ajustement des coûts](design-details-cost-adjustment.md)   
 [Détails de conception : Modes évaluation stock](design-details-costing-methods.md) [Gestion des composants des coûts](finance-manage-inventory-costs.md)  
 [Finances](finance.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
