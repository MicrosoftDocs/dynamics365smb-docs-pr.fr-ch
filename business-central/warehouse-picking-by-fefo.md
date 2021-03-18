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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ae07bc4f1d9f348f08f591e5e4341938ec4b5f16
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382219"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="83c56-103">Activer le prélèvement d’articles par FEFO</span><span class="sxs-lookup"><span data-stu-id="83c56-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="83c56-104">First-Expired-First-Out (FEFO) est une méthode de tri qui garantit que les articles les plus anciens, ceux qui ont les dates d’expiration les plus anciennes, sont prélevés en premier.</span><span class="sxs-lookup"><span data-stu-id="83c56-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="83c56-105">Cette fonctionnalité ne fonctionne que lorsque les critères suivants sont réunis :</span><span class="sxs-lookup"><span data-stu-id="83c56-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="83c56-106">L’article doit avoir un numéro de série/lot.</span><span class="sxs-lookup"><span data-stu-id="83c56-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="83c56-107">Dans la configuration du code de traçabilité article de l’article, le champ **Traçabilité d’entrepôt par numéro de série** ou le champ **Traçabilité d’entrepôt par numéro de lot** doit être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="83c56-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="83c56-108">L’article doit être validé dans le stock avec une date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="83c56-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="83c56-109">Dans la fiche magasin, la case à cocher **Prélèvement requis** doit être activée.</span><span class="sxs-lookup"><span data-stu-id="83c56-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="83c56-110">Dans la fiche magasin, la case à cocher **Prélèvement selon FEFO** doit être activée.</span><span class="sxs-lookup"><span data-stu-id="83c56-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="83c56-111">Dans la fiche magasin, le champ **Emplacement obligatoire** doit être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="83c56-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="83c56-112">Lorsque tous les critères sont réunis, les articles aux numéros de série/lot à prélever sont triés par ancienneté de prélèvements et mouvements, sauf pour les articles qui utilisent la traçabilité par numéro de série ou de lot.</span><span class="sxs-lookup"><span data-stu-id="83c56-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="83c56-113">Si certains articles avec numéros de série/lot utilisent une traçabilité spécifique, ceux-ci sont respectés en premier et, en dessous, les numéros de série/lot non spécifiques restants sont listés selon FEFO.</span><span class="sxs-lookup"><span data-stu-id="83c56-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="83c56-114">Si deux articles avec des numéros de série ou de lot ont la même date de péremption, l’application sélectionne celui avec le plus petit numéro de lot ou de série.</span><span class="sxs-lookup"><span data-stu-id="83c56-114">If two serial/lot-numbered items have the same expiration date, then application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="83c56-115">Lors du prélèvement des articles avec numéro de série/de lot dans les magasins configurés pour un prélèvement et un rangement suggérés, seules les quantités des emplacements de type *Prélèvement* sont prélevés selon FEFO.</span><span class="sxs-lookup"><span data-stu-id="83c56-115">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="83c56-116">Pour activer des mouvements selon FEFO, sur la page **Mouvement de stock** ou la page **Feuille mouvement**, vous devez laisser le champ **Depuis emplacement** vide.</span><span class="sxs-lookup"><span data-stu-id="83c56-116">To enable movements according to FEFO, either on the **Inventory Movement** page or the **Movement Worksheet** page, you must leave the **From Bin** field empty.</span></span>  
<br /><br />
<span data-ttu-id="83c56-117">Si le champ **Validation de péremption stricte** est sélectionné, seuls les articles non expirés sont inclus dans le prélèvement.</span><span class="sxs-lookup"><span data-stu-id="83c56-117">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="83c56-118">Cela s’applique même si vous n’utilisez pas de prélèvement selon FEFO.</span><span class="sxs-lookup"><span data-stu-id="83c56-118">This applies even if you are not using Pick according to FEFO.</span></span>

## <a name="see-also"></a><span data-ttu-id="83c56-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83c56-119">See Also</span></span>  
<span data-ttu-id="83c56-120">[Prélèvement des articles](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="83c56-120">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="83c56-121">[Prélever des articles pour l’expédition entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="83c56-121">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="83c56-122">[Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="83c56-122">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="83c56-123">Détails de conception : gestion d’entrepôt</span><span class="sxs-lookup"><span data-stu-id="83c56-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="83c56-124">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="83c56-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="83c56-125">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="83c56-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]