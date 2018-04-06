---
title: "Procédure : Bloquer des articles de stock pour les ventes ou les achats"
description: "Un article peut être signalé comme bloqué pour la vente, bloqué pour l'achat ou bloqué dans tous les cas."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/02/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e6e662ee13db1f9002e1c3e74a0d15e2aa2e2a98
ms.openlocfilehash: 4a64a29e005713b3aa8d839bdb21cff3034edc81
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="block-inventory-items-for-sales-or-purchases"></a><span data-ttu-id="10a37-103">Bloquer des articles de stock pour les ventes ou les achats</span><span class="sxs-lookup"><span data-stu-id="10a37-103">Block Inventory Items for Sales or Purchases</span></span>
<span data-ttu-id="10a37-104">Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], un article peut être signalé comme bloqué pour la vente, bloqué pour l'achat ou bloqué dans tous les cas.</span><span class="sxs-lookup"><span data-stu-id="10a37-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], an item can be marked as blocked for sales, blocked for purchase, or blocked for all purposes.</span></span>  

<span data-ttu-id="10a37-105">Le tableau suivant illustre ce qui se produit lorsque les articles sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="10a37-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="10a37-106">Article marqué comme</span><span class="sxs-lookup"><span data-stu-id="10a37-106">Item marked as</span></span>|<span data-ttu-id="10a37-107">Résultat</span><span class="sxs-lookup"><span data-stu-id="10a37-107">Result</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="10a37-108">**Bloqué à la vente**</span><span class="sxs-lookup"><span data-stu-id="10a37-108">**Sale blocked**</span></span>|<span data-ttu-id="10a37-109">Vous ne pouvez pas utiliser l'article dans un document vente ou dans une feuille article vente.</span><span class="sxs-lookup"><span data-stu-id="10a37-109">You cannot use the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="10a37-110">**Bloqué à l'achat**</span><span class="sxs-lookup"><span data-stu-id="10a37-110">**Purchase blocked**</span></span>|<span data-ttu-id="10a37-111">Vous ne pouvez pas utiliser l'article dans un document achat, dans une feuille article d'achat, ou dans les processus de planification achat.</span><span class="sxs-lookup"><span data-stu-id="10a37-111">You cannot use the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="10a37-112">**Bloqué**</span><span class="sxs-lookup"><span data-stu-id="10a37-112">**Blocked**</span></span>|<span data-ttu-id="10a37-113">Vous ne pouvez pas utiliser l'article pour une transaction d'article.</span><span class="sxs-lookup"><span data-stu-id="10a37-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="10a37-114">Pour plus d'informations sur le blocage d'un article pour quelle que raison possible, voir Fiche article.</span><span class="sxs-lookup"><span data-stu-id="10a37-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-inventory-items-for-sales"></a><span data-ttu-id="10a37-115">Pour bloquer des articles de stock à l'achat</span><span class="sxs-lookup"><span data-stu-id="10a37-115">To block inventory items for sales</span></span>  

1.  <span data-ttu-id="10a37-116">Cliquez sur l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="10a37-116">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="10a37-117">Sélectionnez l'article que vous souhaitez bloquer, puis choisissez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="10a37-117">Select the item that you want to block, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="10a37-118">Pour bloquer l'article sélectionné pour des transactions de vente, dans le raccourci **Prix et vente**, sélectionnez la case à cocher **Vente bloquée**.</span><span class="sxs-lookup"><span data-stu-id="10a37-118">To block the selected item for sales transactions, on the **Prices & Sales** FastTab, select the **Sale blocked** check box.</span></span>  
4.  <span data-ttu-id="10a37-119">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="10a37-119">Choose the **OK** button.</span></span>  

## <a name="to-block-inventory-items-for-purchase"></a><span data-ttu-id="10a37-120">Pour bloquer des articles de stock à la vente</span><span class="sxs-lookup"><span data-stu-id="10a37-120">To block inventory items for purchase</span></span>  

1.  <span data-ttu-id="10a37-121">Cliquez sur l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="10a37-121">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="10a37-122">Sélectionnez l'article que vous souhaitez bloquer, puis choisissez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="10a37-122">Select the item that you want to block, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="10a37-123">Pour bloquer un article pour des transactions d'achat, dans le raccourci **Réapprovisionnement**, sélectionnez la case à cocher **Achat bloqué**.</span><span class="sxs-lookup"><span data-stu-id="10a37-123">To block an item for purchase transactions, on the **Replenishment** FastTab, select the **Purchase blocked** check box.</span></span>  
4.  <span data-ttu-id="10a37-124">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="10a37-124">Choose the **OK** button.</span></span>  

<span data-ttu-id="10a37-125">Vous recevrez un message d'erreur si vous essayez d'effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="10a37-125">You will receive an error message if you try to do the following:</span></span>  

- <span data-ttu-id="10a37-126">Entrez les lignes vente et les lignes achat dans les documents vente et les documents achat pour les articles bloqués.</span><span class="sxs-lookup"><span data-stu-id="10a37-126">Enter sales lines and purchase lines in sales documents and purchase documents for blocked items.</span></span> <span data-ttu-id="10a37-127">Pour plus d'informations, voir la table Ligne Vente et la table Ligne Achat.</span><span class="sxs-lookup"><span data-stu-id="10a37-127">For more information, see the Sales Line table and the Purchase Line table.</span></span>  
- <span data-ttu-id="10a37-128">Créez des lignes dans une feuille article pour les articles bloqués.</span><span class="sxs-lookup"><span data-stu-id="10a37-128">Create new lines in an item journal for blocked items.</span></span> <span data-ttu-id="10a37-129">Pour plus d'informations, reportez-vous à la fenêtre Feuille article.</span><span class="sxs-lookup"><span data-stu-id="10a37-129">For more information, see the Item Journal window.</span></span>  
- <span data-ttu-id="10a37-130">Validez les mouvements de stock pour les articles bloqués.</span><span class="sxs-lookup"><span data-stu-id="10a37-130">Post item transactions for blocked items.</span></span>  

## <a name="see-also"></a><span data-ttu-id="10a37-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10a37-131">See Also</span></span>  
 <span data-ttu-id="10a37-132">[Gestion des stocks, Suisse](swiss-inventory-management.md) </span><span class="sxs-lookup"><span data-stu-id="10a37-132">[Swiss Inventory Management](swiss-inventory-management.md) </span></span>  
 <span data-ttu-id="10a37-133">[Copier des articles existants pour créer de nouveaux articles](how-to-copy-existing-items-to-new-items.md) </span><span class="sxs-lookup"><span data-stu-id="10a37-133">[Copy Existing Items to New Items](how-to-copy-existing-items-to-new-items.md) </span></span>  
 [<span data-ttu-id="10a37-134">Désactiver le suivi des coûts article</span><span class="sxs-lookup"><span data-stu-id="10a37-134">Deactivate Item Cost Tracking</span></span>](how-to-deactivate-item-cost-tracking.md)

