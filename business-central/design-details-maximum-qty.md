---
title: "Détails de conception - Qté maximum | Microsoft Docs"
description: "La stratégie Quantité maximum est une manière de mettre à jour le stock à l'aide d'un point de commande."
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
ms.openlocfilehash: a9fd9a2387b209931165cd18bdfb025390778af5
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-maximum-qty"></a><span data-ttu-id="3b970-103">Détails de conception : qté maximum.</span><span class="sxs-lookup"><span data-stu-id="3b970-103">Design Details: Maximum Qty.</span></span>
<span data-ttu-id="3b970-104">La stratégie Quantité maximum est une manière de mettre à jour le stock à l'aide d'un point de commande.</span><span class="sxs-lookup"><span data-stu-id="3b970-104">The Maximum Quantity policy is a way to maintain inventory using a reorder point.</span></span>  
  
 <span data-ttu-id="3b970-105">Tout ce qui concerne la stratégie Qté fixe de commande s'applique également à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3b970-105">Everything regarding the Fixed Reorder Qty. policy also applies to this policy.</span></span> <span data-ttu-id="3b970-106">La seule différence est la quantité de l'approvisionnement proposé.</span><span class="sxs-lookup"><span data-stu-id="3b970-106">The only difference is the quantity of the suggested supply.</span></span> <span data-ttu-id="3b970-107">Lors de l'utilisation de la méthode de quantité maximum, la quantité de réapprovisionnement est définie de façon dynamique en fonction du niveau de stock prévisionnel et diffère donc généralement de commande en commande.</span><span class="sxs-lookup"><span data-stu-id="3b970-107">When using the maximum quantity policy, the reorder quantity will be defined dynamically based on the projected inventory level and will therefore usually differ from order to order.</span></span>  
  
## <a name="calculated-per-time-bucket"></a><span data-ttu-id="3b970-108">Calculé par intervalle de planification</span><span class="sxs-lookup"><span data-stu-id="3b970-108">Calculated per Time Bucket</span></span>  
 <span data-ttu-id="3b970-109">La quantité de réapprovisionnement est déterminée au moment (à la fin d'un intervalle de planification) où le système de planification détecte le que le point de commande a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="3b970-109">The reorder quantity is determined at the point of time (the end of a time bucket) when the planning system detects that the reorder point has been crossed.</span></span> <span data-ttu-id="3b970-110">En même temps, le système mesure l'écart entre le niveau de stock prévisionnel actuel et le stock maximal spécifié.</span><span class="sxs-lookup"><span data-stu-id="3b970-110">At this time, the system measures the gap from the current projected inventory level up to the specified maximum inventory.</span></span> <span data-ttu-id="3b970-111">Cela constitue la quantité à recommander.</span><span class="sxs-lookup"><span data-stu-id="3b970-111">This constitutes the quantity that should be reordered.</span></span> <span data-ttu-id="3b970-112">Le système vérifie ensuite si l'approvisionnement a déjà été commandé ailleurs pour être reçu dans les délais et, si c'est le cas, réduit la quantité de la nouvelle commande d'approvisionnement des quantités déjà commandées.</span><span class="sxs-lookup"><span data-stu-id="3b970-112">The system then checks if supply has already been ordered elsewhere to be received within the lead time and, if so, reduces the quantity of the new supply order by already ordered quantities.</span></span>  
  
 <span data-ttu-id="3b970-113">Le système assure que le stock prévisionnel atteint au moins le niveau du point de commande, dans la cas où l'utilisateur oublierait de spécifier une quantité de stock maximum.</span><span class="sxs-lookup"><span data-stu-id="3b970-113">The system will ensure that the projected inventory at least reaches the reorder point level – in case the user has forgotten to specify a maximum inventory quantity.</span></span>  
  
## <a name="combines-with-order-modifiers"></a><span data-ttu-id="3b970-114">Associe avec les modificateurs d'ordre</span><span class="sxs-lookup"><span data-stu-id="3b970-114">Combines with Order Modifiers</span></span>  
 <span data-ttu-id="3b970-115">En fonction de la configuration, il peut être préférable de combiner la stratégie de la quantité maximum avec des modificateurs de commande pour garantir une quantité de commande minimale ou de l'arrondir au nombre supérieur d'unités d'achat, ou de le diviser en davantage de lots comme défini par la quantité maximum commande.</span><span class="sxs-lookup"><span data-stu-id="3b970-115">Depending on the setup, it may be best to combine the Maximum Quantity policy with order modifiers to ensure a minimum order quantity or round it to an integer number of purchase units of measure, or split it into more lots as defined by the maximum order quantity.</span></span>  
  
## <a name="combines-with-calendars"></a><span data-ttu-id="3b970-116">Combinaison avec des calendriers</span><span class="sxs-lookup"><span data-stu-id="3b970-116">Combines with Calendars</span></span>  
 <span data-ttu-id="3b970-117">Avant de proposer une commande approvisionnement pour répondre à un point de commande, le système de planification vérifie si la commande est planifiée pour un jour chômé, en fonction des calendriers définis dans le champ **Code calendrier principal** des fenêtres **Informations société** et **Fiche magasin**.</span><span class="sxs-lookup"><span data-stu-id="3b970-117">Before suggesting a new supply order to meet a reorder point, the planning system checks if the order is scheduled for a non-working day, according to any calendars that are  defined in the **Base Calendar Code** field in the **Company Information** and **Location Card** windows.</span></span>  
  
 <span data-ttu-id="3b970-118">Si la date prévue est un jour chômé, le système de planification déplace la commande en aval à la date de travail la plus proche.</span><span class="sxs-lookup"><span data-stu-id="3b970-118">If the scheduled date is a non-working day, the planning system moves the order forward to the nearest working date.</span></span> <span data-ttu-id="3b970-119">Cela peut entraîner une commande qui satisfait un point de commande mais ne pas satisfait une certaine demande spécifique.</span><span class="sxs-lookup"><span data-stu-id="3b970-119">This may result in an order that meets a reorder point but does not meet some specific demand.</span></span> <span data-ttu-id="3b970-120">Pour une telle demande non soldée, le système de planification crée un approvisionnement supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="3b970-120">For such unbalanced demand, the planning system creates an extra supply.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b970-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b970-121">See Also</span></span>  
 <span data-ttu-id="3b970-122">[Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="3b970-122">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="3b970-123">[Détails de conception : paramètres de planification](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="3b970-123">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="3b970-124">[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="3b970-124">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="3b970-125">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="3b970-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
