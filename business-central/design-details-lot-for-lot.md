---
title: Détails de conception - Lot pour lot | Microsoft Docs
description: Découvrez comment utiliser la méthode lot pour lot pour déterminer la quantité de commande en fonction de la demande.
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
ms.openlocfilehash: 3b80738be6dfe9d171a3cad56edf56cfa4960180
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/16/2019
ms.locfileid: "938149"
---
# <a name="design-details-lot-for-lot"></a><span data-ttu-id="b9475-103">Détails de conception : lot pour lot</span><span class="sxs-lookup"><span data-stu-id="b9475-103">Design Details: Lot-for-Lot</span></span>
<span data-ttu-id="b9475-104">La méthode lot pour lot est la plus souple, parce que le système réagit uniquement à la demande réelle, de plus il agit sur une demande anticipée à partir de commandes de prévision et de commandes ouvertes, puis détermine la quantité commande en fonction de la demande.</span><span class="sxs-lookup"><span data-stu-id="b9475-104">The lot-for-lot policy is the most flexible because the system only reacts on actual demand, plus it acts on anticipated demand from forecast and blanket orders and then settles the order quantity based on the demand.</span></span> <span data-ttu-id="b9475-105">La méthode lot pour lot visé cible les articles A et B pour lesquels le stock peut être accepté mais doit être évité.</span><span class="sxs-lookup"><span data-stu-id="b9475-105">The lot-for-lot policy is aimed at A- and B-items where inventory can be accepted but should be avoided.</span></span>  

<span data-ttu-id="b9475-106">Par certains côtés, la méthode lot pour lot ressemble à la méthode de commande, mais elle a une approche générique des articles ; elle peut accepter des quantités en stock, et elle groupe une demande et un approvisionnement correspondants dans des intervalles de planification définis par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9475-106">In some ways, the lot-for-lot policy looks like the Order policy, but it has a generic approach to items; it can accept quantities in inventory, and it bundles demand and corresponding supply in time buckets defined by the user.</span></span>  

<span data-ttu-id="b9475-107">L'intervalle de planification est défini dans le champ **Intervalle de planification**.</span><span class="sxs-lookup"><span data-stu-id="b9475-107">The time bucket is defined in the **Time Bucket** field.</span></span> <span data-ttu-id="b9475-108">Le système travaille avec un intervalle de planification minimum d'un jour, car il s'agit de la plus petite unité de temps des événements de demande et d'approvisionnement dans le système (même si, dans la pratique, l'unité de temps des ordres de fabrication et des besoins de composants peuvent être des secondes).</span><span class="sxs-lookup"><span data-stu-id="b9475-108">The system works with a minimum time bucket of one day, since this is the smallest time unit of measure on demand and supply events in the system (although, in practice, the time unit of measure on production orders and component needs can be seconds).</span></span>  

<span data-ttu-id="b9475-109">L'intervalle de planification fixe également des limites lorsque un ordre de fabrication existant doit être replanifié pour répondre à une demande donnée.</span><span class="sxs-lookup"><span data-stu-id="b9475-109">The time bucket also sets limits on when an existing supply order should be rescheduled to meet a given demand.</span></span> <span data-ttu-id="b9475-110">Si l'approvisionnement se trouve dans l'intervalle de planification, il est replanifié en entrée ou en sortie pour répondre à la demande.</span><span class="sxs-lookup"><span data-stu-id="b9475-110">If the supply lies within the time bucket, it will be rescheduled in or out to meet the demand.</span></span> <span data-ttu-id="b9475-111">Sinon, s'il a lieu précédemment, il provoque une accumulation de stock inutile et doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="b9475-111">Otherwise, if it lies earlier, it will cause unnecessary build-up of inventory and should be canceled.</span></span> <span data-ttu-id="b9475-112">S'il se trouve plus tard, une commande approvisionnement est créée à la place.</span><span class="sxs-lookup"><span data-stu-id="b9475-112">If it lies later, a new supply order will be created instead.</span></span>  

<span data-ttu-id="b9475-113">Avec cette méthode, il est également possible de définir un stock de sécurité pour compenser les fluctuations possibles de l'approvisionnement, ou répondre à une demande soudaine.</span><span class="sxs-lookup"><span data-stu-id="b9475-113">With this policy, it is also possible to define a safety stock in order to compensate for possible fluctuations in supply, or to meet sudden demand.</span></span>  

<span data-ttu-id="b9475-114">Étant donné que la quantité de commande approvisionnement est basée sur la demande réelle, il peut sembler raisonnable d'utiliser les modificateurs de commande : arrondir la quantité commandée pour répondre à un multiple spécifié de la commande (ou unité d'achat), augmenter la commande à une quantité de commande minimale spécifiée, ou réduire la quantité à la quantité maximale spécifiée (et ainsi créer deux ou plusieurs approvisionnements pour répondre à la quantité nécessaire totale).</span><span class="sxs-lookup"><span data-stu-id="b9475-114">Because the supply order quantity is based on the actual demand it can make sense to use the order modifiers: round the order quantity up to meet a specified order multiple (or purchase unit of measure), increase the order to a specified minimum order quantity, or decrease the quantity to the specified maximum quantity (and thus create two or more supplies to reach the total needed quantity).</span></span>  

## <a name="see-also"></a><span data-ttu-id="b9475-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9475-115">See Also</span></span>  
<span data-ttu-id="b9475-116">[Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="b9475-116">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="b9475-117">[Détails de conception : paramètres de planification](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="b9475-117">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="b9475-118">[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="b9475-118">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="b9475-119">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="b9475-119">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
