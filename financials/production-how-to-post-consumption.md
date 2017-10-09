---
title: "Procédure de validation par lots de la consommation | Microsoft Docs"
description: "Si le champ Méthode consommation indique **Manuelle**, vous devez valider les composants manuellement à l'aide d'une feuille consommation."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 29e85f5264f007db3712d4f6227d689b2a3de926
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-batch-post-production-consumption"></a>Procédure : valider par lots la consommation de la production
Si le champ Méthode consommation indique **Manuelle**, vous devez valider les composants manuellement à l'aide d'une feuille consommation.

Vous pouvez également configurer le système pour valider automatiquement (*consommer*) les composants lorsque vous lancez ou terminez des ordres de fabrication. Pour plus d'informations, voir [Activer la consommation en aval des composants en fonction de la production réalisée](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Pour valider la consommation pour une ou plusieurs lignes ordre de fabrication  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille consommation**, puis sélectionnez le lien connexe.  
2.  Renseignez les champs en indiquant les données relatives à l'ordre de fabrication et à la consommation. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Si l'entrepôt dans lequel les composants sont stockés est configuré pour utiliser des emplacements mais pas le traitement de prélèvement, affectez un code emplacement à la ligne feuille pour indiquer d'où les articles doivent être prélevés dans l'entrepôt. Pour plus d'informations, reportez-vous à [Procédure : prélever pour la fabrication ou l'assemblage](warehouse-how-to-pick-for-production.md).  
3.  Choisissez l'action **Valider** pour valider la consommation. Les écritures comptables article associées sont réduites.

## <a name="see-also"></a>Voir aussi  
[Production](production-manage-manufacturing.md)    
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)      
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
