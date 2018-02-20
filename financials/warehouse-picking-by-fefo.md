---
title: "Comment activer le prélèvement par FEFO | Microsoft Docs"
description: "First-Expired-First-Out (FEFO) est une méthode de tri qui garantit que les articles les plus anciens, ceux qui ont les dates d'expiration les plus anciennes, sont prélevés en premier."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cc45bf06ab5d12cf393d48b7b1c295db28f56b3b
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="eabbd-103">Activer le prélèvement d'articles par FEFO</span><span class="sxs-lookup"><span data-stu-id="eabbd-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="eabbd-104">First-Expired-First-Out (FEFO) est une méthode de tri qui garantit que les articles les plus anciens, ceux qui ont les dates d'expiration les plus anciennes, sont prélevés en premier.</span><span class="sxs-lookup"><span data-stu-id="eabbd-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="eabbd-105">Cette fonctionnalité ne fonctionne que lorsque les critères suivants sont réunis :</span><span class="sxs-lookup"><span data-stu-id="eabbd-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="eabbd-106">L'article doit avoir un numéro de série/lot.</span><span class="sxs-lookup"><span data-stu-id="eabbd-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="eabbd-107">Dans la configuration du code de traçabilité article de l'article, le champ **Traçabilité d'entrepôt par numéro de série** ou le champ **Traçabilité d'entrepôt par numéro de lot** doit être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="eabbd-107">On the item’s item tracking code setup, the **SN-Specific Warehouse Tracking** field or the **Lot-Specific Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="eabbd-108">L'article doit être validé dans le stock avec une date d'expiration.</span><span class="sxs-lookup"><span data-stu-id="eabbd-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="eabbd-109">Dans la fiche magasin, la case à cocher **Prélèvement requis** doit être activée.</span><span class="sxs-lookup"><span data-stu-id="eabbd-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="eabbd-110">Dans la fiche magasin, la case à cocher **Prélèvement selon FEFO** doit être activée.</span><span class="sxs-lookup"><span data-stu-id="eabbd-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="eabbd-111">Dans la fiche magasin, le champ **Emplacement obligatoire** doit être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="eabbd-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="eabbd-112">Lorsque tous les critères sont réunis, les articles aux numéros de série/lot à prélever sont triés par ancienneté de prélèvements et mouvements, sauf pour les articles qui utilisent la traçabilité par numéro de série ou de lot.</span><span class="sxs-lookup"><span data-stu-id="eabbd-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="eabbd-113">Si certains articles avec numéros de série/lot utilisent une traçabilité spécifique, ceux-ci sont respectés en premier et, en dessous, les numéros de série/lot non spécifiques restants sont listés selon FEFO.</span><span class="sxs-lookup"><span data-stu-id="eabbd-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>  

 <span data-ttu-id="eabbd-114">Si deux articles avec des numéros de série ou de lot ont la même date de péremption, le programme sélectionne celui avec le plus petit numéro de lot ou de série.</span><span class="sxs-lookup"><span data-stu-id="eabbd-114">If two serial/lot-numbered items have the same expiration date, then the program selects the item with the lowest serial or lot number.</span></span> <span data-ttu-id="eabbd-115">Si les numéros de série ou de lot sont identiques, le programme sélectionne l'article enregistré en premier.</span><span class="sxs-lookup"><span data-stu-id="eabbd-115">If the serial or lot numbers are the same, then the program selects the item that was registered first.</span></span>  

> [!NOTE]  
>  -   <span data-ttu-id="eabbd-116">Lors du prélèvement des articles avec numéro de série/de lot dans les magasins configurés pour un prélèvement et un rangement suggérés, seules les quantités des emplacements de type *Prélèvement* sont prélevés selon FEFO.</span><span class="sxs-lookup"><span data-stu-id="eabbd-116">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
> -   <span data-ttu-id="eabbd-117">Pour activer des mouvements selon FEFO, dans la fenêtre **Mouvement de stock** ou la fenêtre **Feuille mouvement** , vous devez laisser le champ **Depuis emplacement** vide.</span><span class="sxs-lookup"><span data-stu-id="eabbd-117">To enable movements according to FEFO, either in the **Inventory Movement** window or the **Movement Worksheet** window, you must leave the **From Bin** field empty.</span></span>  
> -   <span data-ttu-id="eabbd-118">Si le champ **Validation de péremption stricte** est sélectionné, seuls les articles non expirés sont inclus dans le prélèvement.</span><span class="sxs-lookup"><span data-stu-id="eabbd-118">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="eabbd-119">Cela s'applique même si vous n'utilisez pas de prélèvement selon FEFO.</span><span class="sxs-lookup"><span data-stu-id="eabbd-119">This applies even if you are not using Pick according to FEFO.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eabbd-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eabbd-120">See Also</span></span>  
<span data-ttu-id="eabbd-121">[Prélèvement des articles](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="eabbd-121">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="eabbd-122">[Prélever des articles pour l'expédition entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="eabbd-122">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="eabbd-123">[Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="eabbd-123">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="eabbd-124">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="eabbd-124">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="eabbd-125">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="eabbd-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="eabbd-126">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eabbd-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

