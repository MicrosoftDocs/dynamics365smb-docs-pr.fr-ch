---
title: "Détails de conception - Gestion des méthodes de réapprovisionnement | Microsoft Docs"
description: "Aperçu des tâches pour définir une méthode de réapprovisionnement dans la planification des approvisionnements."
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
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: fr-ch
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-handling-reordering-policies"></a><span data-ttu-id="d4231-103">Détails de conception : gestion des méthodes de réapprovisionnement</span><span class="sxs-lookup"><span data-stu-id="d4231-103">Design Details: Handling Reordering Policies</span></span>
<span data-ttu-id="d4231-104">Pour qu'un article participe à la planification des approvisionnements, une méthode de regroupement doit être définie.</span><span class="sxs-lookup"><span data-stu-id="d4231-104">For an item to participate in supply planning, a reorder policy must be defined.</span></span> <span data-ttu-id="d4231-105">Les quatre méthodes de réapprovisionnement disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4231-105">The following four reordering policies exist:</span></span>  
  
* <span data-ttu-id="d4231-106">Qté fixe de commande.</span><span class="sxs-lookup"><span data-stu-id="d4231-106">Fixed Reorder Qty.</span></span>  
* <span data-ttu-id="d4231-107">Qté maximum</span><span class="sxs-lookup"><span data-stu-id="d4231-107">Maximum Qty.</span></span>  
* <span data-ttu-id="d4231-108">Commande</span><span class="sxs-lookup"><span data-stu-id="d4231-108">Order</span></span>  
* <span data-ttu-id="d4231-109">Lot pour lot</span><span class="sxs-lookup"><span data-stu-id="d4231-109">Lot-for-Lot</span></span>  
  
<span data-ttu-id="d4231-110">Les méthodes Qté fixe de commande et Qté maximum sont liées à la planification du stock.</span><span class="sxs-lookup"><span data-stu-id="d4231-110">Fixed Reorder Qty. and Maximum Qty. policies relate to inventory planning.</span></span> <span data-ttu-id="d4231-111">Bien que la planification du stock soit techniquement plus simple que la procédure de contrepartie, ces stratégies doivent coexister avec la contrepartie pas à pas de l'approvisionnement et du chaînage.</span><span class="sxs-lookup"><span data-stu-id="d4231-111">Although inventory planning is technically simpler than the balancing procedure, these policies must coexist with the step-by-step balancing of supply and order tracking.</span></span> <span data-ttu-id="d4231-112">Pour contrôler l'intégration entre les deux, et livrer la visibilité dans la logique de planification utilisée, des principes stricts régissent la façon dont les méthodes de réapprovisionnement sont traitées.</span><span class="sxs-lookup"><span data-stu-id="d4231-112">To control the integration between the two, and to provide visibility into the involved planning logic, strict principles govern how reordering policies are handled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d4231-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d4231-113">In This Section</span></span>  
[<span data-ttu-id="d4231-114">Détails de conception : Le rôle du point de commande</span><span class="sxs-lookup"><span data-stu-id="d4231-114">Design Details: The Role of the Reorder Point</span></span>](design-details-the-role-of-the-reorder-point.md)  
[<span data-ttu-id="d4231-115">Détails de conception : surveillance du niveau de stock prévisionnel et du point de commande</span><span class="sxs-lookup"><span data-stu-id="d4231-115">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[<span data-ttu-id="d4231-116">Détails de conception : Le rôle de l'intervalle de planification</span><span class="sxs-lookup"><span data-stu-id="d4231-116">Design Details: The Role of the Time Bucket</span></span>](design-details-the-role-of-the-time-bucket.md)  
[<span data-ttu-id="d4231-117">Détails de conception : rester sous le niveau de dépassement de capacité</span><span class="sxs-lookup"><span data-stu-id="d4231-117">Design Details: Staying under the Overflow Level</span></span>](design-details-staying-under-the-overflow-level.md)  
[<span data-ttu-id="d4231-118">Détails de conception : traitement du stock prévisionnel négatif</span><span class="sxs-lookup"><span data-stu-id="d4231-118">Design Details: Handling Projected Negative Inventory</span></span>](design-details-handling-projected-negative-inventory.md)  
[<span data-ttu-id="d4231-119">Détails de conception : méthodes de réapprovisionnement</span><span class="sxs-lookup"><span data-stu-id="d4231-119">Design Details: Reordering Policies</span></span>](design-details-reordering-policies.md)  
  
## <a name="see-also"></a><span data-ttu-id="d4231-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4231-120">See Also</span></span>  
<span data-ttu-id="d4231-121">[Détails de conception : paramètres de planification](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="d4231-121">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="d4231-122">[Détails de conception : tableau d'affectation de planification](design-details-planning-assignment-table.md) </span><span class="sxs-lookup"><span data-stu-id="d4231-122">[Design Details: Planning Assignment Table](design-details-planning-assignment-table.md) </span></span>  
<span data-ttu-id="d4231-123">[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="d4231-123">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
<span data-ttu-id="d4231-124">[Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="d4231-124">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
[<span data-ttu-id="d4231-125">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="d4231-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
