---
title: Comment activer le prélèvement par FEFO | Microsoft Docs
description: First-Expired-First-Out (FEFO) est une méthode de tri qui garantit que les articles les plus anciens, ceux qui ont les dates d’expiration les plus anciennes, sont prélevés en premier.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3a47c9daeeab036055a0644e1b389735f7440106
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784082"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="e8ae0-103">Activer le prélèvement d’articles par FEFO</span><span class="sxs-lookup"><span data-stu-id="e8ae0-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="e8ae0-104">First-Expired-First-Out (FEFO) est une méthode de tri qui garantit que les articles les plus anciens, ceux qui ont les dates d’expiration les plus anciennes, sont prélevés en premier.</span><span class="sxs-lookup"><span data-stu-id="e8ae0-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="e8ae0-105">Cette fonctionnalité ne fonctionne que lorsque les critères suivants sont réunis :</span><span class="sxs-lookup"><span data-stu-id="e8ae0-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="e8ae0-106">L’article doit avoir un numéro de série/lot.</span><span class="sxs-lookup"><span data-stu-id="e8ae0-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="e8ae0-107">Dans la configuration du code de traçabilité article de l’article, le champ **Traçabilité d’entrepôt par numéro de série** ou le champ **Traçabilité d’entrepôt par numéro de lot** doit être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e8ae0-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="e8ae0-108">L’article doit être validé dans le stock avec une date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="e8ae0-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="e8ae0-109">Sur l'emplacement, les boutons de basculement **Prélèvement requis**, **Prélèvement par FEFO**, et **Emplacement obligatoire** doivent être activés.</span><span class="sxs-lookup"><span data-stu-id="e8ae0-109">On the location, the **Require Pick**, **Pick According to FEFO**, and **Bin Mandatory** toggles must be turned on.</span></span>  

 <span data-ttu-id="e8ae0-110">Lorsque tous les critères sont réunis, les articles aux numéros de série/lot à prélever sont triés par ancienneté de prélèvements et mouvements, sauf pour les articles qui utilisent la traçabilité par numéro de série ou de lot.</span><span class="sxs-lookup"><span data-stu-id="e8ae0-110">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="e8ae0-111">Si certains articles avec numéros de série ou lot utilisent une traçabilité spécifique, ceux-ci sont respectés en premier et, en dessous, les numéros de série/lot non spécifiques restants sont listés selon FEFO.</span><span class="sxs-lookup"><span data-stu-id="e8ae0-111">If some serial or lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="e8ae0-112">Si deux articles avec des numéros de série ou de lot ont la même date de péremption, l’application sélectionne celui avec le plus petit numéro de lot ou de série.</span><span class="sxs-lookup"><span data-stu-id="e8ae0-112">If two serial or lot-numbered items have the same expiration date, then the application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="e8ae0-113">Lors du prélèvement des articles avec numéro de série ou lot dans les magasins configurés pour un prélèvement et un rangement suggérés, seules les quantités des emplacements de type *Prélèvement* sont prélevés selon FEFO.</span><span class="sxs-lookup"><span data-stu-id="e8ae0-113">When picking serial or lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="e8ae0-114">Pour activer des mouvements selon FEFO, laissez le champ **D’emplacement** vide sur la page **Mouvement de stock** ou les pages **Feuille mouvement**.</span><span class="sxs-lookup"><span data-stu-id="e8ae0-114">To enable movements according to FEFO, leave the **From Bin** field empty on the **Inventory Movement** page or the **Movement Worksheet** pages.</span></span>  
<br /><br />
<span data-ttu-id="e8ae0-115">Si le champ **Date expiration stricte** est sélectionné sur la **Fiche Code traçabilité**, seuls les articles non expirés seront inclus dans le prélèvement et les lignes seront triées selon le principe FEFO.</span><span class="sxs-lookup"><span data-stu-id="e8ae0-115">If the **Strict Expiration Posting** field is selected on the **Item Tracking Code Card**, only items that are not expired will be included in the pick, and the lines are sorted according to the FEFO principle.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8ae0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8ae0-116">See Also</span></span>  
<span data-ttu-id="e8ae0-117">[Prélèvement des articles](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="e8ae0-117">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="e8ae0-118">[Prélever des articles pour l’expédition entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="e8ae0-118">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="e8ae0-119">[Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="e8ae0-119">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="e8ae0-120">Détails de conception : gestion d’entrepôt</span><span class="sxs-lookup"><span data-stu-id="e8ae0-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="e8ae0-121">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="e8ae0-121">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="e8ae0-122">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e8ae0-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]