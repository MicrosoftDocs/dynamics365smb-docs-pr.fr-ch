---
title: Détails de conception - Traitement du stock prévisionnel négatif | Microsoft Docs
description: Le point de commande exprime la demande anticipée lors du délai de l'article. Lorsque le point de commande est passé, il est temps de commander plus. Mais le stock prévisionnel doit être suffisamment élevé pour couvrir la demande jusqu'à ce que la commande soit reçue. Par ailleurs, le stock de sécurité doit se charger des fluctuations de la demande jusqu'à un niveau de service ciblé.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: cfedced3a1e7ccf94294ebd36f4fb5311fd1933e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821415"
---
# <a name="design-details-handling-projected-negative-inventory"></a><span data-ttu-id="86b37-106">Détails de conception : traitement du stock prévisionnel négatif</span><span class="sxs-lookup"><span data-stu-id="86b37-106">Design Details: Handling Projected Negative Inventory</span></span>
<span data-ttu-id="86b37-107">Le point de commande exprime la demande anticipée lors du délai de l'article.</span><span class="sxs-lookup"><span data-stu-id="86b37-107">The reorder point expresses the anticipated demand during the lead time of the item.</span></span> <span data-ttu-id="86b37-108">Lorsque le point de commande est passé, il est temps de commander plus.</span><span class="sxs-lookup"><span data-stu-id="86b37-108">When the reorder point is passed, it is time to order more.</span></span> <span data-ttu-id="86b37-109">Mais le stock prévisionnel doit être suffisamment élevé pour couvrir la demande jusqu'à ce que la commande soit reçue.</span><span class="sxs-lookup"><span data-stu-id="86b37-109">But the projected inventory must be large enough to cover the demand until the new order is received.</span></span> <span data-ttu-id="86b37-110">Par ailleurs, le stock de sécurité doit se charger des fluctuations de la demande jusqu'à un niveau de service ciblé.</span><span class="sxs-lookup"><span data-stu-id="86b37-110">Meanwhile, the safety stock should take care of fluctuations in demand up to a targeted service level.</span></span>  

 <span data-ttu-id="86b37-111">Par conséquent, le système de planification considère comme une urgence si une demande future ne peut pas être servie à partir du stock prévisionnel, ou exprimé d'une autre manière, si le stock prévisionnel devient négatif.</span><span class="sxs-lookup"><span data-stu-id="86b37-111">Consequently, the planning system considers it an emergency if a future demand cannot be served from the projected inventory, or expressed in another way, that the projected inventory goes negative.</span></span> <span data-ttu-id="86b37-112">Le système traite une telle exception en suggérant une nouvelle commande d'approvisionnement pour satisfaire la partie de la demande qui ne peut pas être satisfaite par le stock ou un autre approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="86b37-112">The system deals with such an exception by suggesting a new supply order to meet the part of the demand that cannot be met by inventory or other supply.</span></span> <span data-ttu-id="86b37-113">La taille de la nouvelle commande approvisionnement ne prend pas en compte le stock maximum ou la quantité de réappro., ni les modificateurs de commande qté maximum commande, qté minimum commande et multiple de commande.</span><span class="sxs-lookup"><span data-stu-id="86b37-113">The order size of the new supply order will not take the maximum inventory or the reorder quantity into consideration, nor will it take into consideration the order modifiers Maximum Order Quantity, Minimum Order Quantity, and Order Multiple.</span></span> <span data-ttu-id="86b37-114">Au lieu de cela, elle reflète l'insuffisance exacte.</span><span class="sxs-lookup"><span data-stu-id="86b37-114">Instead, it will reflect the exact deficiency.</span></span>  

 <span data-ttu-id="86b37-115">La ligne planning de ce type de commande approvisionnement affiche une icône d'avertissement Urgence, et des informations supplémentaires sont fournies lors de la recherche pour informer l'utilisateur de la situation.</span><span class="sxs-lookup"><span data-stu-id="86b37-115">The planning line for this type of supply order will display an Emergency warning icon, and additional information will be provided upon lookup to inform the user of the situation.</span></span>  

 <span data-ttu-id="86b37-116">Dans la figure suivante, l'approvisionnement D représente une commande d'urgence pour ajuster le stock négatif.</span><span class="sxs-lookup"><span data-stu-id="86b37-116">In the following illustration, supply D represents an emergency order to adjust for negative inventory.</span></span>  

 <span data-ttu-id="86b37-117">![Suggestion de planification d'urgence pour éviter un stock négatif](media/nav_app_supply_planning_2_negative_inventory.png "Suggestion de planification d'urgence pour éviter un stock négatif")</span><span class="sxs-lookup"><span data-stu-id="86b37-117">![Emergency planning suggestion to avoid negative inventory](media/nav_app_supply_planning_2_negative_inventory.png "Emergency planning suggestion to avoid negative inventory")</span></span>  

1.  <span data-ttu-id="86b37-118">L'approvisionnement **A**, stock prévisionnel initial, est inférieur au point de commande.</span><span class="sxs-lookup"><span data-stu-id="86b37-118">Supply **A**, initial projected inventory, is below reorder point.</span></span>  
2.  <span data-ttu-id="86b37-119">Un approvisionnement planifié en aval est créé (**C**).</span><span class="sxs-lookup"><span data-stu-id="86b37-119">A new forward-scheduled supply is created (**C**).</span></span>  

     <span data-ttu-id="86b37-120">(Quantité = Stock maximum – Niveau de stock projeté)</span><span class="sxs-lookup"><span data-stu-id="86b37-120">(Quantity = Maximum Inventory – Projected Inventory Level)</span></span>  
3.  <span data-ttu-id="86b37-121">L'approvisionnement **A** est clôturé par la demande **B** qui n'est pas totalement couverte.</span><span class="sxs-lookup"><span data-stu-id="86b37-121">Supply **A** is closed by demand **B**, which is not fully covered.</span></span>  

     <span data-ttu-id="86b37-122">(La demande **B** peut tenter de planifier l'approvisionnement C mais cela ne se produira pas en raison du concept d'intervalle de planification.)</span><span class="sxs-lookup"><span data-stu-id="86b37-122">(Demand **B** could try to schedule Supply C in but that will not happen according to the time-bucket concept.)</span></span>  
4.  <span data-ttu-id="86b37-123">Un nouvel approvisionnement (**D**) est créé pour couvrir la quantité restante sur demande **B**.</span><span class="sxs-lookup"><span data-stu-id="86b37-123">New supply (**D**) is created to cover the remaining quantity on Demand **B**.</span></span>  
5.  <span data-ttu-id="86b37-124">La demande **B** est clôturée (création d'une relance dans le stock prévisionnel).</span><span class="sxs-lookup"><span data-stu-id="86b37-124">Demand **B** is closed (creating a reminder to the projected inventory).</span></span>  
6.  <span data-ttu-id="86b37-125">Le nouvel approvisionnement **D** est clôturé.</span><span class="sxs-lookup"><span data-stu-id="86b37-125">The new supply **D** is closed.</span></span>  
7.  <span data-ttu-id="86b37-126">Le stock prévisionnel est vérifié ; le point de commande n'a pas été dépassé.</span><span class="sxs-lookup"><span data-stu-id="86b37-126">Projected Inventory is checked; reorder point has not been crossed.</span></span>  
8.  <span data-ttu-id="86b37-127">L'approvisionnement **C** est clôturé (plus aucune demande n'existe).</span><span class="sxs-lookup"><span data-stu-id="86b37-127">Supply **C** is closed (no more demand exists).</span></span>  
9. <span data-ttu-id="86b37-128">Vérification finale : aucun relance restante de niveau de stock.</span><span class="sxs-lookup"><span data-stu-id="86b37-128">Final check: No outstanding inventory level reminders exist.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="86b37-129">L'étape 4 indique la manière dont le système réagit dans les versions antérieures à Microsoft Dynamics NAV 2009 SP1.</span><span class="sxs-lookup"><span data-stu-id="86b37-129">Step 4 reflects how the system reacts in versions earlier than Microsoft Dynamics NAV 2009 SP1.</span></span>  

 <span data-ttu-id="86b37-130">Cela conclut la description des principes centraux en relation avec la planification de stock sur la base de les méthodes de réapprovisionnement.</span><span class="sxs-lookup"><span data-stu-id="86b37-130">This concludes the description of central principles relating to inventory planning based on reordering policies.</span></span> <span data-ttu-id="86b37-131">La section suivante décrit les caractéristiques des quatre méthodes de réapprovisionnement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="86b37-131">The following section describes the characteristics of the four supported reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="86b37-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86b37-132">See Also</span></span>  
 <span data-ttu-id="86b37-133">[Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="86b37-133">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="86b37-134">[Détails de conception : paramètres de planification](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="86b37-134">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="86b37-135">[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="86b37-135">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="86b37-136">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="86b37-136">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
