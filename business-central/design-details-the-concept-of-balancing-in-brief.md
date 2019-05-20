---
title: Détails de conception - Le concept d'équilibrage en bref | Microsoft Docs
description: La demande est faite par les clients d'une société. L'approvisionnement est ce que la société peut créer et supprimer pour établir l'équilibre. Le système de planification commence avec la demande indépendante et effectue une traçabilité en amont jusqu'à l'approvisionnement.
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
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 8684389c75299dc57a2056041b50ebde37a0bea1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239306"
---
# <a name="design-details-the-concept-of-balancing-in-brief"></a><span data-ttu-id="a5f92-105">Détails de conception : Le concept d'équilibrage en bref</span><span class="sxs-lookup"><span data-stu-id="a5f92-105">Design Details: The Concept of Balancing in Brief</span></span>
<span data-ttu-id="a5f92-106">La demande est faite par les clients d'une société.</span><span class="sxs-lookup"><span data-stu-id="a5f92-106">Demand is given by a company’s customers.</span></span> <span data-ttu-id="a5f92-107">L'approvisionnement est ce que la société peut créer et supprimer pour établir l'équilibre.</span><span class="sxs-lookup"><span data-stu-id="a5f92-107">Supply is what the company can create and remove to establish balance.</span></span> <span data-ttu-id="a5f92-108">Le système de planification commence avec la demande indépendante et effectue une traçabilité en amont jusqu'à l'approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="a5f92-108">The planning system starts with the independent demand and then tracks backwards to the supply.</span></span>  

 <span data-ttu-id="a5f92-109">Les profils de stock sont utilisés pour contenir des informations sur les demandes et les approvisionnements, les quantités et les délais.</span><span class="sxs-lookup"><span data-stu-id="a5f92-109">The inventory profiles are used to contain information about the demands and supplies, quantities, and timing.</span></span> <span data-ttu-id="a5f92-110">Ces profils constituent essentiellement les deux côtés de l'échelle de contrepartie.</span><span class="sxs-lookup"><span data-stu-id="a5f92-110">These profiles essentially make up the two sides of the balancing scale.</span></span>  

 <span data-ttu-id="a5f92-111">L'objectif du mécanisme de planification est d'équilibrer la demande et l'approvisionnement d'un article pour s'assurer que l'approvisionnement correspond à la demande de manière faisable, telle qu'elle est définie par les paramètres et les règles de planification.</span><span class="sxs-lookup"><span data-stu-id="a5f92-111">The objective of the planning mechanism is to counterbalance the demand and supply of an item to ensure that supply will match demand in a feasible way as defined by the planning parameters and rules.</span></span>  

 <span data-ttu-id="a5f92-112">![Vue d'ensemble de l'équilibrage de la demande et de l'approvisionnement](media/nav_app_supply_planning_2_balancing.png "Vue d'ensemble de l'équilibrage de la demande et de l'approvisionnement")</span><span class="sxs-lookup"><span data-stu-id="a5f92-112">![Overview of supply-demand balancing](media/nav_app_supply_planning_2_balancing.png "Overview of supply-demand balancing")</span></span>  

## <a name="see-also"></a><span data-ttu-id="a5f92-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5f92-113">See Also</span></span>  
 <span data-ttu-id="a5f92-114">[Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="a5f92-114">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="a5f92-115">[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="a5f92-115">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="a5f92-116">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="a5f92-116">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
