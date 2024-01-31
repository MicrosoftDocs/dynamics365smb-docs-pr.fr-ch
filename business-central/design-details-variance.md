---
title: Détails de conception - Ecart | Microsoft Docs
description: 'L’écart est défini comme la différence entre le coût réel et le coût standard, telle que décrite dans la formule suivante.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Détails de conception : écart
L’écart est défini comme la différence entre le coût réel et le coût standard, telle que décrite dans la formule suivante.  

 coût réel – coût standard = variance  

 Si le coût réel change, par exemple, si vous validez des frais annexes à une date ultérieure, l’écart est mis à jour en conséquence.  

> [!NOTE]  
>  La réévaluation n’affecte pas le calcul d’écart, puisque la réévaluation modifie uniquement la valeur stock.  

## Exemple :  
 L’exemple suivant présente la manière de calculer l’écart pour les articles achetés. Il est basé sur le scénario suivant :  

1.  L’utilisateur achète un article à 90,00 LCY, mais le coût standard est de 100,00 LCY. Par conséquent, l’écart achat net est de -10 DS.  
2.  10,00 DS sont crédités sur le compte écart achat.  
3.  L’utilisateur valide des frais article de 20,00 LCY. Par conséquent, le coût réel passe à 110 DS, et la valeur de l’écart achat passe à 10 DS.  
4.  20,00 DS sont débités sur le compte écart achat. Par conséquent, l’écart achat net est de 10 DS.  
5.  L’utilisateur réévalue l’article de 100,00 LCY à 70,00 LCY. Cela n’affecte pas le calcul d’écart, uniquement la valeur stock.  

 Le tableau suivant montre les écritures valeur résultantes.  

 ![Calcul variance achat.](media/design_details_inventory_costing_11_purchase_variance.png "Calcul variance achat")  

## Déterminer le coût standard  
 Le coût standard est utilisé pour calculer l’écart et le montant à capitaliser. Dans la mesure où le coût standard peut être modifié dans le temps en raison du calcul de mise à jour manuel, vous avez besoin d’un certain point dans le temps où le coût standard est fixe pour le calcul de l’écart. Ce point est pertinent lorsque l’augmentation de stock est facturée. Pour les articles fabriqués ou assemblés, le point auquel le coût standard est déterminé est lorsque le coût est ajusté.  

 Le tableau suivant montre la manière dont les différentes parts de coût sont calculées pour les articles produits et assemblés lorsque vous utilisez la fonction Calculer coût standard.  

|Coût total|Article acheté|Article produit/assemblé|  
|----------------|--------------------|------------------------------|  
|**Coût standard**||Coût matière mono-niveau + Coût opératoire mono-niveau + Coût s/traitance mono-niveau + Frais gén. opérat. mono-niv. + Frais gén. matière mono-niv.|  
|**Coût matière mono-niveau**|Coût unitaire|![Équation 1.](media/design_details_inventory_costing_11_equation_1.png "Équation 1")|  
|**Coût opératoire mono-niveau**|Non applicable|![Équation 2.](media/design_details_inventory_costing_11_equation_2.png "Équation 2")|  
|**Coût s/traitance mono-niveau**|Non applicable|![Équation 3.](media/design_details_inventory_costing_11_equation_3.png "Équation 3")|  
|**Frais gén. opérat. mono-niv.**|Non applicable|![Équation 4.](media/design_details_inventory_costing_11_equation_4.png "Équation 4")|  
|**Frais gén. matière mono-niv.**|Non applicable|(Coût matière mono-niveau + Coût opératoire mono-niveau + Coût s/traitance mono-niveau) * Coût indirect % / 100 + Frais généraux|  
|**Coût matière multi-niveau**|Coût unitaire|![Équation 5.](media/design_details_inventory_costing_11_equation_5.png "Équation 5")|  
|**Coût opératoire multi-niveau**|Non applicable|![Équation 6.](media/design_details_inventory_costing_11_equation_6.png "Équation 6")|  
|**Coût s/traitance multi-niv.**|Non applicable|![Équation 7.](media/design_details_inventory_costing_11_equation_7.png "Équation 7")|  
|**Frais généraux opératoires multi-niveaux**|Non applicable|![Équation 8.](media/design_details_inventory_costing_11_equation_8.png "Équation 8")|  
|**Frais gén. matière multi-niv.**|Non applicable|![Équation 9.](media/design_details_inventory_costing_11_equation_9.png "Équation 9")|  

## Voir aussi  
 [Détails de conception : stock évaluation stock](design-details-inventory-costing.md)   
 [Détails de conception : modes évaluation stock](design-details-costing-methods.md) [Gestion des composants des coûts](finance-manage-inventory-costs.md)  
 [Finances](finance.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]