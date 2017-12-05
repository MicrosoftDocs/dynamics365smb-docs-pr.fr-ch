---
title: "Détails de conception - Équilibrage la demande et de l'approvisionnement | Microsoft Docs"
description: "Pour comprendre comment fonctionne le système de planification, il est nécessaire de comprendre les objectifs priorisés du système de planification, dont les plus importants sont de s'assurer que toute demande est satisfaite par suffisamment d'approvisionnement et n'importe quel approvisionnement atteint un but."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: af9569114cfbe2d48be3a7514cc5c2bb48bd48ca
ms.contentlocale: fr-ch
ms.lasthandoff: 11/10/2017

---
# <a name="design-details-balancing-demand-and-supply"></a><span data-ttu-id="053ef-103">Détails de conception : équilibrage de la demande et de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="053ef-103">Design Details: Balancing Demand and Supply</span></span>
<span data-ttu-id="053ef-104">Pour comprendre comment fonctionne le système de planification, il est nécessaire de comprendre les objectifs priorisés du système de planification, dont les plus importants sont de s'assurer que :</span><span class="sxs-lookup"><span data-stu-id="053ef-104">To understand how the planning system works, it is necessary to understand the prioritized goals of the planning system, the most important of which are to ensure that:</span></span>  

- <span data-ttu-id="053ef-105">La demande sera satisfaite par une offre suffisante.</span><span class="sxs-lookup"><span data-stu-id="053ef-105">Any demand will be met by sufficient supply.</span></span>  
- <span data-ttu-id="053ef-106">Tout approvisionnement répond à une finalité.</span><span class="sxs-lookup"><span data-stu-id="053ef-106">Any supply serves a purpose.</span></span>  

 <span data-ttu-id="053ef-107">En général, ces objectifs sont atteints en équilibrant l'approvisionnement avec la demande.</span><span class="sxs-lookup"><span data-stu-id="053ef-107">Generally, these goals are achieved by balancing supply with demand.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="053ef-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="053ef-108">In This Section</span></span>  
[<span data-ttu-id="053ef-109">Détails de conception : demande et approvisionnement</span><span class="sxs-lookup"><span data-stu-id="053ef-109">Design Details: Demand and Supply</span></span>](design-details-demand-and-supply.md)  
[<span data-ttu-id="053ef-110">Détails de conception : Le concept d'équilibrage en bref</span><span class="sxs-lookup"><span data-stu-id="053ef-110">Design Details: The Concept of Balancing in Brief</span></span>](design-details-the-concept-of-balancing-in-brief.md)  
[<span data-ttu-id="053ef-111">Détails de conception : traiter les commandes avant la date début de la planification</span><span class="sxs-lookup"><span data-stu-id="053ef-111">Design Details: Dealing with Orders Before the Planning Starting Date</span></span>](design-details-dealing-with-orders-before-the-planning-starting-date.md)  
[<span data-ttu-id="053ef-112">Détails de conception : chargement des profils de stock</span><span class="sxs-lookup"><span data-stu-id="053ef-112">Design Details: Loading the Inventory Profiles</span></span>](design-details-loading-the-inventory-profiles.md)  
[<span data-ttu-id="053ef-113">Détails de conception : Affecter une priorité aux commandes</span><span class="sxs-lookup"><span data-stu-id="053ef-113">Design Details: Prioritizing Orders</span></span>](design-details-prioritizing-orders.md)  
[<span data-ttu-id="053ef-114">Détails de conception : équilibrage de l'approvisionnement avec la demande</span><span class="sxs-lookup"><span data-stu-id="053ef-114">Design Details: Balancing Supply with Demand</span></span>](design-details-balancing-supply-with-demand.md)  
[<span data-ttu-id="053ef-115">Détails de conception : clôture de la demande et de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="053ef-115">Design Details: Closing Demand and Supply</span></span>](design-details-closing-demand-and-supply.md)  

## <a name="see-also"></a><span data-ttu-id="053ef-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="053ef-116">See Also</span></span>  
 <span data-ttu-id="053ef-117">[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="053ef-117">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 <span data-ttu-id="053ef-118">[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="053ef-118">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="053ef-119">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="053ef-119">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

