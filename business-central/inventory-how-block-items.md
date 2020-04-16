---
title: Comment bloquer des articles pour la vente ou pour l'achat
description: Dans Business Central, un article peut être signalé comme bloqué pour la vente, bloqué pour l'achat ou bloqué dans tous les cas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c453a10f30d2a45f6d4641bda8b24ee3659b1a32
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182315"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="f28ea-103">Bloquer des articles pour la vente ou pour l'achat</span><span class="sxs-lookup"><span data-stu-id="f28ea-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="f28ea-104">Vous pouvez bloquer un article pour la saisie dans des lignes de vente ou d'achat, et vous pouvez le bloquer pour la validation dans n'importe quelle transaction.</span><span class="sxs-lookup"><span data-stu-id="f28ea-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="f28ea-105">Le tableau suivant illustre ce qui se produit lorsque les articles sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="f28ea-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="f28ea-106">Option</span><span class="sxs-lookup"><span data-stu-id="f28ea-106">Option</span></span>|<span data-ttu-id="f28ea-107">Désignation</span><span class="sxs-lookup"><span data-stu-id="f28ea-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="f28ea-108">**Bloqué à la vente**</span><span class="sxs-lookup"><span data-stu-id="f28ea-108">**Sales Blocked**</span></span>|<span data-ttu-id="f28ea-109">Vous ne pouvez pas saisir l'article dans un document vente ou dans une feuille article vente.</span><span class="sxs-lookup"><span data-stu-id="f28ea-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="f28ea-110">**Bloqué à l'achat**</span><span class="sxs-lookup"><span data-stu-id="f28ea-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="f28ea-111">Vous ne pouvez pas saisir l'article dans un document achat, dans une feuille article d'achat, ou dans les processus de planification achat.</span><span class="sxs-lookup"><span data-stu-id="f28ea-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="f28ea-112">**Bloqué**</span><span class="sxs-lookup"><span data-stu-id="f28ea-112">**Blocked**</span></span>|<span data-ttu-id="f28ea-113">Vous ne pouvez pas utiliser l'article pour une transaction d'article.</span><span class="sxs-lookup"><span data-stu-id="f28ea-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="f28ea-114">Les articles bloqués peuvent être retournés.</span><span class="sxs-lookup"><span data-stu-id="f28ea-114">Blocked items can be returned.</span></span> <span data-ttu-id="f28ea-115">Cela signifie qu'aucun des paramètres ci-dessus ne s'applique lorsque l'article est utilisé sur des commandes retour et des avoirs.</span><span class="sxs-lookup"><span data-stu-id="f28ea-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="f28ea-116">Lorsque vous utilisez la fonction **Copier à partir du document** pour créer des documents à partir de documents existants, vous êtes averti si des articles sur les lignes du document source sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="f28ea-116">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="f28ea-117">Les lignes de document bloquées sont exclues du nouveau document et une notification affiche une vue d'ensemble de toutes les lignes de document bloquées dans le document source.</span><span class="sxs-lookup"><span data-stu-id="f28ea-117">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="f28ea-118">Pour bloquer un article pour la saisie sur des lignes vente</span><span class="sxs-lookup"><span data-stu-id="f28ea-118">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="f28ea-119">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f28ea-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f28ea-120">Sélectionnez l'article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué à la vente**.</span><span class="sxs-lookup"><span data-stu-id="f28ea-120">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="f28ea-121">Si vous essayez de saisir l'article sur un document vente ou une ligne feuille, vous recevez désormais un message d'erreur indiquant que l'article est bloqué.</span><span class="sxs-lookup"><span data-stu-id="f28ea-121">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="f28ea-122">Pour bloquer un article pour la saisie sur des lignes achat</span><span class="sxs-lookup"><span data-stu-id="f28ea-122">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="f28ea-123">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f28ea-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f28ea-124">Sélectionnez l'article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué à l'achat**.</span><span class="sxs-lookup"><span data-stu-id="f28ea-124">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="f28ea-125">Si vous essayez de saisir l'article sur un document achat ou une ligne feuille, vous recevez désormais un message d'erreur indiquant que l'article est bloqué.</span><span class="sxs-lookup"><span data-stu-id="f28ea-125">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="f28ea-126">Pour bloquer un article à valider</span><span class="sxs-lookup"><span data-stu-id="f28ea-126">To block an item from being posted</span></span>
1. <span data-ttu-id="f28ea-127">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f28ea-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="f28ea-128">Sélectionnez l'article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué**.</span><span class="sxs-lookup"><span data-stu-id="f28ea-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="f28ea-129">Si vous essayez de valider tout type de transaction pour l'article, un message d'erreur indiquant que l'article est bloqué s'affiche désormais.</span><span class="sxs-lookup"><span data-stu-id="f28ea-129">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="f28ea-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f28ea-130">See Also</span></span>  
[<span data-ttu-id="f28ea-131">Enregistrer de nouveaux articles</span><span class="sxs-lookup"><span data-stu-id="f28ea-131">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="f28ea-132">Stock</span><span class="sxs-lookup"><span data-stu-id="f28ea-132">Inventory</span></span>](inventory-manage-inventory.md)  
