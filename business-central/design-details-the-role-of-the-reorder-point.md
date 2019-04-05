---
title: Détails de conception - Le rôle du point de commande | Microsoft Docs
description: Cette rubrique met l'accent sur l'importance de définir un point de commande, afin de déterminer quand commander plus de stock.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: e39a7efdc796e8745bd9d8f7d74cdcfb171d851f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821656"
---
# <a name="design-details-the-role-of-the-reorder-point"></a><span data-ttu-id="5e34b-103">Détails de conception : Le rôle du point de commande</span><span class="sxs-lookup"><span data-stu-id="5e34b-103">Design Details: The Role of the Reorder Point</span></span>
<span data-ttu-id="5e34b-104">En plus de l'équilibrage général de la demande et de l'approvisionnement, le système de planification doit également contrôler les niveaux de stock des articles affectés pour respecter les méthodes de réapprovisionnement définies.</span><span class="sxs-lookup"><span data-stu-id="5e34b-104">In addition to the general balancing of supply and demand, the planning system must also monitor inventory levels for the affected items to respect the defined reordering policies.</span></span>  

<span data-ttu-id="5e34b-105">Un point de commande représente la demande lors d'un délai.</span><span class="sxs-lookup"><span data-stu-id="5e34b-105">A reorder point represents demand during lead time.</span></span> <span data-ttu-id="5e34b-106">Lorsque le stock prévisionnel passe en dessous du niveau de stock défini par le point de commande, il est temps de commander une plus grande quantité.</span><span class="sxs-lookup"><span data-stu-id="5e34b-106">When the projected inventory passes below the inventory level defined by the reorder point, it is time to order more quantity.</span></span> <span data-ttu-id="5e34b-107">Par ailleurs, le stock doit diminuer progressivement et probablement atteindre zéro (ou le niveau de stock de sécurité), jusqu'à ce que le réapprovisionnement arrive.</span><span class="sxs-lookup"><span data-stu-id="5e34b-107">Meanwhile, the inventory is expected to decrease gradually and possibly reach zero (or the safety stock level), until the replenishment arrives.</span></span>  

<span data-ttu-id="5e34b-108">Par conséquent, le système de planification suggère une commande approvisionnement planifiée en aval au moment où le stock projeté passe sous le point de commande.</span><span class="sxs-lookup"><span data-stu-id="5e34b-108">Accordingly, the planning system will suggest a forward-scheduled supply order at the point when the projected inventory passes below the reorder point.</span></span>  

<span data-ttu-id="5e34b-109">Le point de commande indique un certain niveau de stock.</span><span class="sxs-lookup"><span data-stu-id="5e34b-109">The reorder point reflects a certain inventory level.</span></span> <span data-ttu-id="5e34b-110">Cependant, les niveaux de stock peuvent changer de façon significative au cours de l'intervalle de planification et, par conséquent, le système de planification doit constamment surveiller le stock disponible projeté.</span><span class="sxs-lookup"><span data-stu-id="5e34b-110">However, inventory levels can move significantly during the time bucket and, therefore, the planning system must constantly monitor the projected available inventory.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5e34b-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e34b-111">See Also</span></span>  
<span data-ttu-id="5e34b-112">[Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="5e34b-112">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="5e34b-113">[Détails de conception : paramètres de planification](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="5e34b-113">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="5e34b-114">[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="5e34b-114">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="5e34b-115">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="5e34b-115">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
