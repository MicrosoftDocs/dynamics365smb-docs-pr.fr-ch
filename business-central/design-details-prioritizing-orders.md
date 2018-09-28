---
title: "Détails de conception - Affecter une priorité aux commandes | Microsoft Docs"
description: "Découvrez comment affecter une priorité pour répondre à la demande et l'approvisionnement."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: dc5b3b34979698f05886cdd6f583cda262d82e51
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-prioritizing-orders"></a><span data-ttu-id="7fa09-103">Détails de conception : Affecter une priorité aux commandes</span><span class="sxs-lookup"><span data-stu-id="7fa09-103">Design Details: Prioritizing Orders</span></span>
<span data-ttu-id="7fa09-104">Dans un point de stock donné, la date demandée ou disponible représente la priorité la plus élevée ; la demande du jour doit être traitée avant la demande de la semaine suivante.</span><span class="sxs-lookup"><span data-stu-id="7fa09-104">Within a given SKU, the requested or available date represents the highest priority; the demand of today should be dealt with before the demand of next week.</span></span> <span data-ttu-id="7fa09-105">Mais en plus de cette priorité générale, le système de planification suggère également que le type de demande doit être rempli avant de répondre à une autre demande.</span><span class="sxs-lookup"><span data-stu-id="7fa09-105">But in addition to this overall priority, the planning system will also suggest which type of demand should be fulfilled before fulfilling another demand.</span></span> <span data-ttu-id="7fa09-106">De même, il suggère que la source d'approvisionnement soit lettrée avant d'appliquer d'autres sources d'approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="7fa09-106">Likewise, it will suggest what source of supply should be applied before applying other sources of supply.</span></span> <span data-ttu-id="7fa09-107">Ceci est effectué en fonction des priorités de la commande.</span><span class="sxs-lookup"><span data-stu-id="7fa09-107">This is done according to order priorities.</span></span>  
  
<span data-ttu-id="7fa09-108">La demande et l'approvisionnement chargés contribuent à un profil pour le stock prévisionnel en fonction des priorités suivantes :</span><span class="sxs-lookup"><span data-stu-id="7fa09-108">Loaded demand and supply contribute to a profile for the projected inventory according to the following priorities:</span></span>  
  
## <a name="priorities-on-the-demand-side"></a><span data-ttu-id="7fa09-109">Priorités du côté de la demande</span><span class="sxs-lookup"><span data-stu-id="7fa09-109">Priorities on the Demand Side</span></span>  
1. <span data-ttu-id="7fa09-110">Déjà expédié : écriture comptable article</span><span class="sxs-lookup"><span data-stu-id="7fa09-110">Already shipped: Item Ledger Entry</span></span>  
2. <span data-ttu-id="7fa09-111">Retour achat</span><span class="sxs-lookup"><span data-stu-id="7fa09-111">Purchase Return Order</span></span>  
3. <span data-ttu-id="7fa09-112">Ecriture réservation</span><span class="sxs-lookup"><span data-stu-id="7fa09-112">Sales Order</span></span>  
4. <span data-ttu-id="7fa09-113">Commande service</span><span class="sxs-lookup"><span data-stu-id="7fa09-113">Service Order</span></span>  
5. <span data-ttu-id="7fa09-114">Besoin de composants de production</span><span class="sxs-lookup"><span data-stu-id="7fa09-114">Production Component Need</span></span>  
6. <span data-ttu-id="7fa09-115">Ligne d'ordre d'assemblage</span><span class="sxs-lookup"><span data-stu-id="7fa09-115">Assembly Order Line</span></span>  
7. <span data-ttu-id="7fa09-116">Commande désenlogement transfert</span><span class="sxs-lookup"><span data-stu-id="7fa09-116">Outbound Transfer Order</span></span>  
8. <span data-ttu-id="7fa09-117">Commande ouverte (qui n'a pas déjà été consommée par les commandes vente associées)</span><span class="sxs-lookup"><span data-stu-id="7fa09-117">Blanket Order (that has not already been consumed by related sales orders)</span></span>  
9. <span data-ttu-id="7fa09-118">Prévision (qui n'a pas déjà été consommée par d'autres commandes vente)</span><span class="sxs-lookup"><span data-stu-id="7fa09-118">Forecast (that has not already been consumed by other sales orders)</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="7fa09-119">Les retours achat ne sont généralement pas impliqués dans la planification d'approvisionnement ; ils doivent toujours être réservés à partir du lot qui va être retourné.</span><span class="sxs-lookup"><span data-stu-id="7fa09-119">Purchase returns are usually not involved in supply planning; they should always be reserved from the lot that is going to be returned.</span></span> <span data-ttu-id="7fa09-120">S'il ne sont pas réservés, les retours achat jouent un rôle dans la disponibilité et sont classés en priorité élevée pour éviter que le système de planification suggère une commande approvisionnement uniquement pour servir un retour achat.</span><span class="sxs-lookup"><span data-stu-id="7fa09-120">If not reserved, purchase returns play a role in the availability and are highly prioritized to avoid that the planning system suggests a supply order just to serve a purchase return.</span></span>  
  
## <a name="priorities-on-the-supply-side"></a><span data-ttu-id="7fa09-121">Priorités du côté de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="7fa09-121">Priorities on the Supply Side</span></span>  
1. <span data-ttu-id="7fa09-122">Déjà dans le stock : écriture comptable article (Flexibilité planification = Aucune)</span><span class="sxs-lookup"><span data-stu-id="7fa09-122">Already in inventory: Item Ledger Entry (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="7fa09-123">Retour vente (flexibilité de planification = aucune)</span><span class="sxs-lookup"><span data-stu-id="7fa09-123">Sales Return Order (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="7fa09-124">Enlogement transfert</span><span class="sxs-lookup"><span data-stu-id="7fa09-124">Inbound Transfer Order</span></span>  
4. <span data-ttu-id="7fa09-125">Ordre de fabrication</span><span class="sxs-lookup"><span data-stu-id="7fa09-125">Production Order</span></span>  
5. <span data-ttu-id="7fa09-126">Ordre d'assemblage</span><span class="sxs-lookup"><span data-stu-id="7fa09-126">Assembly Order</span></span>  
6. <span data-ttu-id="7fa09-127">Commande achat</span><span class="sxs-lookup"><span data-stu-id="7fa09-127">Purchase Order</span></span>  
  
## <a name="priority-related-to-the-state-of-demand-and-supply"></a><span data-ttu-id="7fa09-128">Priorité liée à l'état de la demande et de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="7fa09-128">Priority Related to the State of Demand and Supply</span></span>  
<span data-ttu-id="7fa09-129">Outre les priorités accordées par le type d'offre et de demande, l'état actuel des commandes dans le processus d'exécution définit également une priorité.</span><span class="sxs-lookup"><span data-stu-id="7fa09-129">Apart from priorities given by the type of demand and supply, the present state of the orders in the execution process also defines a priority.</span></span> <span data-ttu-id="7fa09-130">Par exemple, les activités entrepôt ont un effet et le statut des commandes vente, des commandes achat, des ordres de transfert, des ordres d'assemblage et des ordres de fabrication est pris en compte :</span><span class="sxs-lookup"><span data-stu-id="7fa09-130">For example, warehouse activities have an impact, and the status of sales, purchase, transfer, assembly, and production orders is taken into account:</span></span>  
  
1. <span data-ttu-id="7fa09-131">En partie géré (flexibilité de planification = Aucune)</span><span class="sxs-lookup"><span data-stu-id="7fa09-131">Partly handled (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="7fa09-132">Déjà en cours de traitement dans l'entrepôt (Flexibilité planification = Aucune)</span><span class="sxs-lookup"><span data-stu-id="7fa09-132">Already in process in the warehouse (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="7fa09-133">Lancé - tous types de commande (flexibilité de planification = illimitée)</span><span class="sxs-lookup"><span data-stu-id="7fa09-133">Released – all order types (Planning Flexibility = Unlimited)</span></span>  
4. <span data-ttu-id="7fa09-134">Ordre de fabrication planifié ferme (flexibilité de planification = illimitée)</span><span class="sxs-lookup"><span data-stu-id="7fa09-134">Firm Planned Production Order (Planning Flexibility = Unlimited)</span></span>  
5. <span data-ttu-id="7fa09-135">Planifié/ouvert - tous types de commande (flexibilité de planification = illimitée)</span><span class="sxs-lookup"><span data-stu-id="7fa09-135">Planned/Open – all order types (Planning Flexibility = Unlimited)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7fa09-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fa09-136">See Also</span></span>  
<span data-ttu-id="7fa09-137">[Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="7fa09-137">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="7fa09-138">[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="7fa09-138">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="7fa09-139">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="7fa09-139">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
