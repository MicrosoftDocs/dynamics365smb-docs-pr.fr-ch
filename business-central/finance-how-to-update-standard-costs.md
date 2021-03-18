---
title: 'Procédure : mise à jour des coûts standard | Microsoft Docs'
description: Vous devez régulièrement mettre à jour les coûts standard des composants et remonter les nouveaux coûts dans l’article parent.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: feeeae5202cfc5ab0bccf1552ce74f74708445d3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391539"
---
# <a name="update-standard-costs"></a>Mise à jour des coûts standard
Vous devez régulièrement mettre à jour les coûts standard des composants et remonter les nouveaux coûts dans l’article parent. Le processus comprend généralement les quatre étapes suivantes :  

1.  Mettre à jour les coûts aux niveaux des composants et de la capacité. Pour plus d’informations, voir le traitement par lots **Proposer coût standard article**.  
2.  La consolidation et le calcul multi-niveau des coûts des composants et de capacité permettent de déterminer le coût de fabrication ou d’assemblage des articles.  
3.  Appliquer les coûts standard entrés lorsque vous lancez les traitements par lots précédents. Les coûts standard n’entrent en vigueur que lorsqu’ils sont mis en œuvre. Pour plus d’informations, voir Appliquer nouv. coût standard.  
4.  Appliquer les modifications pour mettre à jour le champ **Coût unitaire** de la fiche article et effectuer une réévaluation du stock. Pour plus d’informations, voir [Réévaluer le stock](inventory-how-revalue-inventory.md).  

Pour plus d’informations, voir [À propos du calcul des coûts standard](finance-about-calculating-standard-cost.md) .  
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
 [Détails de conception : modes évaluation stock](design-details-costing-methods.md) [Finance](finance.md)  
 [Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]