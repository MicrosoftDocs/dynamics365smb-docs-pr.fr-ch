---
title: "Détails de conception - Le concept d'équilibrage en bref | Microsoft Docs"
description: "La demande est faite par les clients d'une société. L'approvisionnement est ce que la société peut créer et supprimer pour établir l'équilibre. Le système de planification commence avec la demande indépendante et effectue une traçabilité en amont jusqu'à l'approvisionnement."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ffaa6b174d495b4a22423cabd13b74025db021ed
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-concept-of-balancing-in-brief"></a>Détails de conception : Le concept d'équilibrage en bref
La demande est faite par les clients d'une société. L'approvisionnement est ce que la société peut créer et supprimer pour établir l'équilibre. Le système de planification commence avec la demande indépendante et effectue une traçabilité en amont jusqu'à l'approvisionnement.  
  
 Les profils de stock sont utilisés pour contenir des informations sur les demandes et les approvisionnements, les quantités et les délais. Ces profils constituent essentiellement les deux côtés de l'échelle de contrepartie.  
  
 L'objectif du mécanisme de planification est d'équilibrer la demande et l'approvisionnement d'un article pour s'assurer que l'approvisionnement correspond à la demande de manière faisable, telle qu'elle est définie par les paramètres et les règles de planification.  
  
 ![](media/nav_app_supply_planning_2_balancing.png "NAV_APP_supply_planning_2_balancing")  
  
## <a name="see-also"></a>Voir aussi  
 [Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md)   
 [Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)   
 [Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
