---
title: Détails de conception - Composants des coûts | Microsoft Docs
description: Les composants de coût sont différents types de coûts qui constituent la valeur d’une entrée de stock ou d’une sortie.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-cost-components"></a>Détails de conception : composants des coûts
Les composants de coût sont différents types de coûts qui constituent la valeur d’une entrée de stock ou d’une sortie.  

 Le tableau suivant montre les différents composants du coût et tous les composants de coût subordonnés dont ils sont composés.  

|Composant du coût|Composant subalterne de coût|Désignation|  
|--------------------|--------------------------------|---------------------------------------|  
|Coût direct|Coût unitaire (prix d’achat direct)|Coûts qui ne peuvent pas être rapportés à des coûts associés.|  
|Coût direct|Frais de transport (frais annexes)|Coûts qui ne peuvent pas être rapportés à des coûts associés.|  
|Coût direct|Frais d’assurance (frais annexes)|Coûts qui ne peuvent pas être rapportés à des coûts associés.|  
|Coût indirect||Coût qui ne peut pas être rapporté à un objet de coût.|  
|Ecart|Écart achat|Différence entre les coûts réel et standard, qui n’est validée que pour les articles utilisant le mode évaluation stock **Standard**.|  
|Ecart|Écart matière|Différence entre les coûts réel et standard, qui n’est validée que pour les articles utilisant le mode évaluation stock **Standard**.|  
|Ecart|Écart opératoire|Différence entre les coûts réel et standard, qui n’est validée que pour les articles utilisant le mode évaluation stock **Standard**.|  
|Ecart|Écart sous-traitance|Différence entre les coûts réel et standard, qui n’est validée que pour les articles utilisant le mode évaluation stock **Standard**.|  
|Ecart|Écart frais gén. opératoires|Différence entre les coûts réel et standard, qui n’est validée que pour les articles utilisant le mode évaluation stock **Standard**.|  
|Ecart|Écart frais généraux production|Différence entre les coûts réel et standard, qui n’est validée que pour les articles utilisant le mode évaluation stock **Standard**.|  
|Réévaluation||Amortissement ou réévaluation de la valeur stock en cours.|  
|Arrondi||Reliquats créés par le mode de calcul de l’évaluation des sorties du stock.|  

> [!NOTE]  
>  Les frais de transport et d’assurance sont des frais annexes qui peuvent être ajoutés au coût d’un article à tout moment. Lorsque vous exécutez le traitement par lots **Ajuster coûts - Écr. article**, la valeur de toute diminution de stock liée est mise à jour en conséquence.  

## <a name="see-also"></a>Voir aussi
 [Détails de conception : évaluation stock](design-details-inventory-costing.md)   
 [Détails de conception : Ecart](design-details-variance.md) [Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
 [Finances](finance.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
