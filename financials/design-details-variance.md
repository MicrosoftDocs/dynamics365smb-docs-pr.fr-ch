---
title: "Détails de conception - Ecart | Microsoft Docs"
description: "L'écart est défini comme la différence entre le coût réel et le coût standard, telle que décrite dans la formule suivante."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 04faa28799288e272da93c60cbb90fa19fd190f0
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-variance"></a>Détails de conception : écart
L'écart est défini comme la différence entre le coût réel et le coût standard, telle que décrite dans la formule suivante.  

 coût réel – coût standard = variance  

 Si le coût réel change, par exemple, si vous validez des frais annexes à une date ultérieure, l'écart est mis à jour en conséquence.  

> [!NOTE]  
>  La réévaluation n'affecte pas le calcul d'écart, puisque la réévaluation modifie uniquement la valeur stock.  

## <a name="example"></a>Exemple :  
 L'exemple suivant présente la manière de calculer l'écart pour les articles achetés. Il est basé sur le scénario suivant :  

1.  L'utilisateur achète un article à 90,00 LCY, mais le coût standard est de 100,00 LCY. Par conséquent, l'écart achat net est de -10 DS.  
2.  10,00 DS sont crédités sur le compte écart achat.  
3.  L'utilisateur valide des frais article de 20,00 LCY. Par conséquent, le coût réel passe à 110 DS, et la valeur de l'écart achat passe à 10 DS.  
4.  20,00 DS sont débités sur le compte écart achat. Par conséquent, l'écart achat net est de 10 DS.  
5.  L'utilisateur réévalue l'article de 100,00 LCY à 70,00 LCY. Cela n'affecte pas le calcul d'écart, uniquement la valeur stock.  

 Le tableau suivant montre les écritures valeur résultantes.  

 ![Calcul variance achat](media/design_details_inventory_costing_11_purchase_variance.png "design_details_inventory_costing_11_purchase_variance")  

## <a name="determining-the-standard-cost"></a>Déterminer le coût standard  
 Le coût standard est utilisé pour calculer l'écart et le montant à capitaliser. Dans la mesure où le coût standard peut être modifié dans le temps en raison du calcul de mise à jour manuel, vous avez besoin d'un certain point dans le temps où le coût standard est fixe pour le calcul de l'écart. Ce point est pertinent lorsque l'augmentation de stock est facturée. Pour les articles fabriqués ou assemblés, le point auquel le coût standard est déterminé est lorsque le coût est ajusté.  

 Le tableau suivant montre la manière dont les différentes parts de coût sont calculées pour les articles produits et assemblés lorsque vous utilisez la fonction Calculer coût standard.  

|Coût total|Article acheté|Article produit/assemblé|  
|----------------|--------------------|------------------------------|  
|**Coût standard**||Coût matière mono-niveau + Coût opératoire mono-niveau + Coût s/traitance mono-niveau + Frais gén. opérat. mono-niv. + Frais gén. matière mono-niv.|  
|**Coût matière mono-niveau**|Coût unitaire|![Equation 1](media/design_details_inventory_costing_11_equation_1.png "design_details_inventory_costing_11_equation_1")|  
|**Coût opératoire mono-niveau**|Non applicable|![Equation 2](media/design_details_inventory_costing_11_equation_2.png "design_details_inventory_costing_11_equation_2")|  
|**Coût s/traitance mono-niveau**|Non applicable|![Equation 3](media/design_details_inventory_costing_11_equation_3.png "design_details_inventory_costing_11_equation_3")|  
|**Frais gén. opérat. mono-niv.**|Non applicable|![Equation 4](media/design_details_inventory_costing_11_equation_4.png "design_details_inventory_costing_11_equation_4")|  
|**Frais gén. matière mono-niv.**|Non applicable|(Coût matière mono-niveau + Coût opératoire mono-niveau + Coût s/traitance mono-niveau) * Coût indirect % / 100 + Frais généraux|  
|**Coût matière multi-niveau**|Coût unitaire|![Equation 5](media/design_details_inventory_costing_11_equation_5.png "design_details_inventory_costing_11_equation_5")|  
|**Coût opératoire multi-niveau**|Non applicable|![Equation 6](media/design_details_inventory_costing_11_equation_6.png "design_details_inventory_costing_11_equation_6")|  
|**Coût s/traitance multi-niv.**|Non applicable|![Equation 7](media/design_details_inventory_costing_11_equation_7.png "design_details_inventory_costing_11_equation_7")|  
|**Frais généraux opératoires multi-niveaux**|Non applicable|![Equation 8](media/design_details_inventory_costing_11_equation_8.png "design_details_inventory_costing_11_equation_8")|  
|**Frais gén. matière multi-niv.**|Non applicable|![Equation 9](media/design_details_inventory_costing_11_equation_9.png "design_details_inventory_costing_11_equation_9")|  

## <a name="see-also"></a>Voir aussi  
 [Détails de conception : évaluation stock](design-details-inventory-costing.md)   
 [Détails de conception : Modes évaluation stock](design-details-costing-methods.md) [Gestion des composants des coûts](finance-manage-inventory-costs.md)  
 [Finances](finance.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

