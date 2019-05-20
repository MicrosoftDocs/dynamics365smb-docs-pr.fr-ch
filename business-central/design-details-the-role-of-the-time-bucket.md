---
title: Détails de conception - Le rôle de l'intervalle de planification | Microsoft Docs
description: L'objectif de l'intervalle de planification est de collecter les événements de demande sur la page de temps de manière à effectuer une commande approvisionnement commune.
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
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 54d4a4aed94b562b82d94d6a5a75a3050c054fc3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239329"
---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="aba2c-103">Détails de conception : Le rôle de l'intervalle de planification</span><span class="sxs-lookup"><span data-stu-id="aba2c-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="aba2c-104">L'objectif de l'intervalle de planification est de collecter les événements de demande sur la page de temps de manière à effectuer une commande approvisionnement commune.</span><span class="sxs-lookup"><span data-stu-id="aba2c-104">The purpose of the time bucket is to collect demand events within the time page in order to make a joint supply order.</span></span>  

 <span data-ttu-id="aba2c-105">Pour les méthodes de réapprovisionnement qui utilisent un point de commande, vous pouvez définir un intervalle de planification.</span><span class="sxs-lookup"><span data-stu-id="aba2c-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="aba2c-106">Cela garantit que la demande dans la même période est accumulée avant de vérifier l'impact sur le stock prévisionnel et si le point de commande a été passé.</span><span class="sxs-lookup"><span data-stu-id="aba2c-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="aba2c-107">Si le point de commande est passé, une nouvelle commande approvisionnement est planifiée en aval à partir de la fin de la période définie par l'intervalle de planification.</span><span class="sxs-lookup"><span data-stu-id="aba2c-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="aba2c-108">Les intervalles de planification débutent à la date de début de la planification.</span><span class="sxs-lookup"><span data-stu-id="aba2c-108">The time buckets begin on the planning starting date.</span></span>  

 <span data-ttu-id="aba2c-109">Le concept d'intervalle de planification reflète le processus manuel de vérifier le niveau de stock de manière fréquente plutôt que pour chaque transaction.</span><span class="sxs-lookup"><span data-stu-id="aba2c-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="aba2c-110">L'utilisateur doit définir la fréquence (l'intervalle de planification).</span><span class="sxs-lookup"><span data-stu-id="aba2c-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="aba2c-111">Par exemple, l'utilisateur regroupe les besoins article d'un fournisseur pour passer une commande hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="aba2c-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  

 <span data-ttu-id="aba2c-112">![Exemple d'intervalle de planification dans la planification](media/nav_app_supply_planning_2_reorder_cycle.png "Exemple d'intervalle de planification dans la planification")</span><span class="sxs-lookup"><span data-stu-id="aba2c-112">![Example of time bucket in planning](media/nav_app_supply_planning_2_reorder_cycle.png "Example of time bucket in planning")</span></span>  

 <span data-ttu-id="aba2c-113">L'intervalle de planification est généralement utilisé pour éviter un effet cascade.</span><span class="sxs-lookup"><span data-stu-id="aba2c-113">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="aba2c-114">Par exemple, une ligne équilibrée de demande et d'approvisionnement dans laquelle une demande antérieure est annulée ou une nouvelle demande est créée.</span><span class="sxs-lookup"><span data-stu-id="aba2c-114">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="aba2c-115">Le résultat est que chaque commande approvisionnement (sauf la dernière) est replanifiée.</span><span class="sxs-lookup"><span data-stu-id="aba2c-115">The result would be that every supply order (except the last one) is rescheduled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aba2c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aba2c-116">See Also</span></span>  
 <span data-ttu-id="aba2c-117">[Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="aba2c-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="aba2c-118">[Détails de conception : paramètres de planification](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="aba2c-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="aba2c-119">[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="aba2c-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="aba2c-120">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="aba2c-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
