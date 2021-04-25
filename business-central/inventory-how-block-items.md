---
title: Comment bloquer des articles pour la vente ou pour l’achat
description: Vous pouvez empêcher qu’un article soit utilisé, par exemple, dans des documents de vente ou d’achat.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4bc130d6982d969084f7fcbf3618893978317f36
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786113"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="7a11e-103">Bloquer des articles pour la vente ou pour l’achat</span><span class="sxs-lookup"><span data-stu-id="7a11e-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="7a11e-104">Vous pouvez bloquer un article pour la saisie sur des lignes de documents de vente ou d’achat, et vous pouvez le bloquer pour la validation dans n’importe quelle transaction.</span><span class="sxs-lookup"><span data-stu-id="7a11e-104">You can block an item from being entered on lines in sales or purchase documents, and you can block it from being posted in any transaction.</span></span> <span data-ttu-id="7a11e-105">Par exemple, cela est utile lorsqu’un article présente un défaut connu.</span><span class="sxs-lookup"><span data-stu-id="7a11e-105">For example, this is useful when an item has a known defect.</span></span> <span data-ttu-id="7a11e-106">Si quelqu’un choisit un article bloqué sur un document de vente ou d’achat, un message l’informera que l’article est bloqué.</span><span class="sxs-lookup"><span data-stu-id="7a11e-106">If someone chooses a blocked item on a sales or purchase document a message will inform them that the item is blocked.</span></span>

<span data-ttu-id="7a11e-107">Le tableau suivant décrit ce qui se produit lorsque les articles sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="7a11e-107">The following table describes what occurs when items are blocked.</span></span>  

|<span data-ttu-id="7a11e-108">Option</span><span class="sxs-lookup"><span data-stu-id="7a11e-108">Option</span></span>|<span data-ttu-id="7a11e-109">Description</span><span class="sxs-lookup"><span data-stu-id="7a11e-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="7a11e-110">**Bloqué à la vente**</span><span class="sxs-lookup"><span data-stu-id="7a11e-110">**Sales Blocked**</span></span>|<span data-ttu-id="7a11e-111">Vous ne pouvez pas saisir l’article dans un document vente ou dans une feuille article vente.</span><span class="sxs-lookup"><span data-stu-id="7a11e-111">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="7a11e-112">**Bloqué à l’achat**</span><span class="sxs-lookup"><span data-stu-id="7a11e-112">**Purchasing Blocked**</span></span>|<span data-ttu-id="7a11e-113">Vous ne pouvez pas saisir l’article dans un document achat, dans une feuille article d’achat, ou dans les processus de planification achat.</span><span class="sxs-lookup"><span data-stu-id="7a11e-113">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="7a11e-114">**Bloqué**</span><span class="sxs-lookup"><span data-stu-id="7a11e-114">**Blocked**</span></span>|<span data-ttu-id="7a11e-115">Vous ne pouvez pas utiliser l’article pour une transaction d’article.</span><span class="sxs-lookup"><span data-stu-id="7a11e-115">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="7a11e-116">Les articles bloqués peuvent être retournés.</span><span class="sxs-lookup"><span data-stu-id="7a11e-116">Blocked items can be returned.</span></span> <span data-ttu-id="7a11e-117">Cela signifie qu’aucun des paramètres ci-dessus ne s’applique lorsque l’article est utilisé sur des commandes retour et des avoirs.</span><span class="sxs-lookup"><span data-stu-id="7a11e-117">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="7a11e-118">Lorsque vous utilisez la fonction **Copier à partir du document** pour créer des documents à partir de documents existants, vous êtes averti si des articles sur les lignes du document source sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="7a11e-118">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="7a11e-119">Les lignes de document bloquées sont exclues du nouveau document et une notification affiche une vue d’ensemble de toutes les lignes de document bloquées dans le document source.</span><span class="sxs-lookup"><span data-stu-id="7a11e-119">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="7a11e-120">Pour bloquer un article pour la saisie sur des lignes vente</span><span class="sxs-lookup"><span data-stu-id="7a11e-120">To block an item from being entered on sales lines</span></span>  
1.  <span data-ttu-id="7a11e-121">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7a11e-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7a11e-122">Sélectionnez l’article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué à la vente**.</span><span class="sxs-lookup"><span data-stu-id="7a11e-122">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="7a11e-123">Pour bloquer un article pour la saisie sur des lignes achat</span><span class="sxs-lookup"><span data-stu-id="7a11e-123">To block an item from being entered on purchase lines</span></span>  
1.  <span data-ttu-id="7a11e-124">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7a11e-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7a11e-125">Sélectionnez l’article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué à l’achat**.</span><span class="sxs-lookup"><span data-stu-id="7a11e-125">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="7a11e-126">Pour bloquer un article à valider</span><span class="sxs-lookup"><span data-stu-id="7a11e-126">To block an item from being posted</span></span>
1. <span data-ttu-id="7a11e-127">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7a11e-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="7a11e-128">Sélectionnez l’article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué**.</span><span class="sxs-lookup"><span data-stu-id="7a11e-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a11e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a11e-129">See Also</span></span>  
[<span data-ttu-id="7a11e-130">Enregistrer de nouveaux articles</span><span class="sxs-lookup"><span data-stu-id="7a11e-130">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="7a11e-131">Stock</span><span class="sxs-lookup"><span data-stu-id="7a11e-131">Inventory</span></span>](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]