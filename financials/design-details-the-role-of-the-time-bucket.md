---
title: "Détails de conception - Le rôle de l'intervalle de planification | Microsoft Docs"
description: "L'objectif de l'intervalle de planification est de collecter les événements de demande dans la fenêtre de temps de manière à effectuer une commande approvisionnement commune."
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
ms.openlocfilehash: eb1b1a401dabe09a77c44558e9f5a83388078aaa
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-the-role-of-the-time-bucket"></a>Détails de conception : Le rôle de l'intervalle de planification
L'objectif de l'intervalle de planification est de collecter les événements de demande dans la fenêtre de temps de manière à effectuer une commande approvisionnement commune.  
  
 Pour les méthodes de réapprovisionnement qui utilisent un point de commande, vous pouvez définir un intervalle de planification. Cela garantit que la demande dans la même période est accumulée avant de vérifier l'impact sur le stock prévisionnel et si le point de commande a été passé. Si le point de commande est passé, une nouvelle commande approvisionnement est planifiée en aval à partir de la fin de la période définie par l'intervalle de planification. Les intervalles de planification débutent à la date de début de la planification.  
  
 Le concept d'intervalle de planification reflète le processus manuel de vérifier le niveau de stock de manière fréquente plutôt que pour chaque transaction. L'utilisateur doit définir la fréquence (l'intervalle de planification). Par exemple, l'utilisateur regroupe les besoins article d'un fournisseur pour passer une commande hebdomadaire.  
  
 ![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")  
  
 L'intervalle de planification est généralement utilisé pour éviter un effet cascade. Par exemple, une ligne équilibrée de demande et d'approvisionnement dans laquelle une demande antérieure est annulée ou une nouvelle demande est créée. Le résultat est que chaque commande approvisionnement (sauf la dernière) est replanifiée.  
  
## <a name="see-also"></a>Voir aussi  
 [Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md)   
 [Détails de conception : paramètres de planification](design-details-planning-parameters.md)   
 [Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
 [Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
