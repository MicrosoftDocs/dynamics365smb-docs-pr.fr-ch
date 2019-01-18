---
title: "Procédure : mise à jour des coûts standard | Microsoft Docs"
description: "Vous devez régulièrement mettre à jour les coûts standard des composants et remonter les nouveaux coûts dans l'article parent."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 88e715ddd2c60c3eb780ffe71d80676fdea00209
ms.contentlocale: fr-ch
ms.lasthandoff: 11/22/2018

---
# <a name="update-standard-costs"></a>Mise à jour des coûts standard
Vous devez régulièrement mettre à jour les coûts standard des composants et remonter les nouveaux coûts dans l'article parent. Le processus comprend généralement les quatre étapes suivantes :  

1.  Mettre à jour les coûts aux niveaux des composants et de la capacité. Pour plus d'informations, voir le traitement par lots **Proposer coût standard article**.  
2.  La consolidation et le calcul multi-niveau des coûts des composants et de capacité permettent de déterminer le coût de fabrication ou d'assemblage des articles.  
3.  Appliquer les coûts standard entrés lorsque vous lancez les traitements par lots précédents. Les coûts standard n'entrent en vigueur que lorsqu'ils sont mis en œuvre. Pour plus d'informations, voir Appliquer nouv. coût standard.  
4.  Appliquer les modifications pour mettre à jour le champ **Coût unitaire** de la fiche article et effectuer une réévaluation du stock. Pour plus d'informations, voir [Réévaluer le stock](inventory-how-revalue-inventory.md).  

Pour plus d'informations, voir [À propos du calcul des coûts standard](finance-about-calculating-standard-cost.md) .  
## <a name="to-update-standard-costs"></a>Pour mettre à jour des coûts standard  
1.  Exécutez le traitement par lots **Ajuster coûts - Écr. article**.  
2.  Exécutez le traitement par lots **Valider coûts ajustés**.  
3.  Ouvrez la **Feuille coût standard** et utilisez une ou plusieurs des fonctions suivantes :  

    1.  Exécutez le traitement par lots **Proposer coût standard article**.  
    2.  Vérifiez les résultats et apportez des modifications si nécessaire.  
    3.  Exécutez le traitement par lots **Suggérer le coût standard de la capacité**.  
    4.  Vérifiez les résultats et apportez des modifications si nécessaire.
    5. Exécutez le traitement par lots **Calculer coût std multi-niv.**.
    6.  Vérifiez les résultats et apportez des modifications si nécessaire.
    7.  Exécutez le traitement par lots **Appliquer nouv. coût standard**.  
4.  Vérifiez et validez la page **Feuille réévaluation** renseignée avec les entrées des étapes précédentes de ce processus.  

## <a name="see-also"></a>Voir aussi  
 [À propos du calcul des coûts standard](finance-about-calculating-standard-cost.md)   
 [Gestion des coûts ajustés](finance-manage-inventory-costs.md)   
 [Détails de conception : modes évaluation stock](design-details-costing-methods.md) [[Finance](finance.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

