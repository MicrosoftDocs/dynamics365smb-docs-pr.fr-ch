---
title: Gestion des coûts ajustés | Microsoft Docs
description: La gestion des coûts, aussi appelée comptabilité analytique, se charge de l’enregistrement et de la déclaration des coûts d’exploitation de la société. Cette activité inclut la déclaration des coûts de fabrication et de stock qui constituent la valeur des articles.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c1dc6cade08a3aab9c5d1cda4b6a2c64995988df
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780847"
---
# <a name="managing-inventory-costs"></a>Gestion des coûts ajustés
La gestion des coûts, aussi appelée comptabilité analytique, se charge de l’enregistrement et de la déclaration des coûts d’exploitation de la société. Cette activité inclut la déclaration des coûts de fabrication et de stock qui constituent la valeur des articles.   

Il est essentiel de comprendre les principes suivants : les méthodes d’évaluation des stocks au prix coûtant définissent le mode d’évaluation des articles lors de leur sortie de stock, l’ajustement des coûts met à jour le coût des biens vendus avec les coûts d’achat associés validés après la vente, les valeurs en stock doivent être validées vers les comptes généraux appropriés à des intervalles réguliers.

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

|**Pour**|**Voir**|  
|------------|-------------|  
|Lire différentes informations conceptuelles pour comprendre les principes et définitions qui gouvernent la fonctionnalité Comptabilité des coûts de stock [!INCLUDE[prod_short](includes/prod_short.md)].|[À propos de l’évaluation des coûts de stock](finance-learn-about-costing.md)|  
|Assurez-vous de connaître le coût des articles expédiés en affectant les coûts articles ajoutés, tels que le fret, la manutention, les assurances, et transport, que vous encourez après la vente.|[Utiliser des frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md)|
|En savoir plus sur les mécanismes dans le système d’évaluation.|[Détails de conception : Évaluation stock](design-details-inventory-costing.md)|
|Obtenir des informations sur la manière dont les périodes inventaire permettent à une société de contrôler la valeur du stock dans le temps en définissant des périodes plus courtes qui peuvent être fermées à la validation lorsque la fin de l’exercice comptable approche.|[Utiliser les périodes inventaire](finance-how-to-work-with-inventory-periods.md)|
|Apprendre pourquoi les coûts standard sont souvent utilisés par les sociétés de production comme base d’évaluation pour les composants et les produits finis.|[À propos du calcul des coûts standard](finance-about-calculating-standard-cost.md)|
|Configurer les périodes inventaire, les méthodes d’évaluation des stocks au prix coûtant et les modes d’arrondi.|[Configuration de l’évaluation du stock](finance-set-up-inventory-valuation-and-costing.md)|
|Réévaluer ou amortir la valeur d’un ou de plusieurs articles dans le stock en validant leur valeur calculée courante.|[Réévaluer le stock](inventory-how-revalue-inventory.md)|
|Ajuster les coûts d’article, automatiquement ou manuellement, pour transférer les modifications de coût des écritures entrantes à leurs écritures sortantes associées.|[Ajuster coûts et prix article](inventory-how-adjust-item-costs.md)|
|Utiliser les fonctions d’évaluation des coûts spéciales pour les transactions article quotidiennes dans les opérations liées aux articles.|[Gestion des coûts ajustés et des coûts de fabrication](finance-handle-inventory-and-manufacturing-costs.md)|  
|Actualisez périodiquement les coûts standard des composants, dans les nomenclatures d’assemblage ou de production, et remonter les nouveaux coûts dans l’article parent.|[Mise à jour des coûts standard](finance-how-to-update-standard-costs.md)|
|Visualiser et modifier manuellement certaines écritures lettrage article qui sont créées automatiquement lors des mouvements de stock.|[Supprimer et relettrer des écritures comptables article](finance-how-to-remove-and-reapply-item-entries.md)|
|Effectuer un contrôle de clôture d’exercice et des tâches de création de rapports, tels que le calcul de la valeur du stock et la validation des coûts dans la comptabilité.|[Rapprocher l’évaluation stock avec la comptabilité](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|

## <a name="see-also"></a>Voir aussi  
 [Finances](finance.md)  
 [STOCKS ET EN-COURS](inventory-manage-inventory.md)   
 [Ventes](sales-manage-sales.md)   
 [Achats](purchasing-manage-purchasing.md)  
 [Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]