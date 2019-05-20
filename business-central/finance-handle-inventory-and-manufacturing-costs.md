---
title: Gestion des coûts ajustés et des coûts de fabrication | Microsoft Docs
description: Bien que la comptabilité analytique soit constituée de processus ne nécessitant pas d'interaction utilisateur, telle que le lettrage d'écritures et l'ajustement automatique des coûts, un certain nombre de champs, pages et états sont destinés aux utilisateurs qui gèrent directement ou indirectement le coût des articles ou opérations.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 53f1c002236877f536a85586d0af912d5e9a85c2
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238271"
---
# <a name="handling-inventory-and-manufacturing-costs"></a>Gestion des coûts ajustés et des coûts de fabrication
Bien que la comptabilité analytique soit constituée de processus ne nécessitant pas d'interaction utilisateur, telle que le lettrage d'écritures et l'ajustement automatique des coûts, un certain nombre de champs, pages et états sont destinés aux utilisateurs qui gèrent directement ou indirectement le coût des articles ou opérations.  

 L'affectation de frais annexes aux documents achat est un exemple d'une tâche de comptabilité analytique indirecte. La mise à jour du coût unitaire de l'article d'assemblage ou de nomenclature production est un exemple de tâche de comptabilité analytique directe.  

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.   

|**Pour**|**Voir**|  
|------------|-------------|  
|Mettre à jour périodiquement ou automatiquement le coût unitaire d'un ou plusieurs articles afin de faire suivre toutes les modifications de prix des écritures entrantes, telles que celles des achats ou des sorties de production, vers les écritures sortantes, telles que la consommation ou les transferts.|[Ajuster coûts et prix article](inventory-how-adjust-item-costs.md)|  
|Obtenir un aperçu de la dynamique coût moyen afin de prendre des décisions relatives aux prix ou de suivre les fluctuations des coûts causées par les erreurs de saisie.|[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)|  
|Créer le coût standard d'un article de production en saisissant les trois éléments de coût : le coût matière, le coût opératoire et le coût de sous-traitance.|[À propos du calcul des coûts standard](finance-about-calculating-standard-cost.md)|  
|Calculer le coût unitaire d'un article de nomenclature à partir des coûts unitaires de ses composants sous-jacents.|[Utiliser les nomenclatures](inventory-how-work-BOMs.md)|  
|Terminer le cycle de vie de l'évaluation stock en ajustant les coûts et en rapprochant les écritures valeur de la comptabilité.|[À propos des coûts des O.F. terminés](finance-about-finished-production-order-costs.md)|  
|Modifier la valeur d'un article dans le stock ou la valeur d'une écriture comptable article, telle qu'une transaction achat.|[Réévaluer le stock](inventory-how-revalue-inventory.md)|
|Délettrer manuellement un article ou relettrer des écritures comptables article créées par le programme.|[Supprimer et relettrer des écritures comptables article](finance-how-to-remove-and-reapply-item-entries.md)|  
|Utilisez le champ **Lettrage à partir écriture** dans la feuille article pour créer manuellement un lettrage fixe entre une transaction entrante et la transaction sortante initiale.|[Clôturer les écritures comptables article ouvertes qui résultent d'un lettrage fixe dans la feuille article](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a>Voir aussi  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)
[Détails de conception : Évaluation stock](design-details-inventory-costing.md)
