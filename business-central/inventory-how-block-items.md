---
title: Comment bloquer des articles pour la vente ou pour l'achat
description: Dans Business Central, un article peut être signalé comme bloqué pour la vente, bloqué pour l'achat ou bloqué dans tous les cas.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 0d5ad688cfa6fb58e8383692362105beeee386f8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820430"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="2ec3f-103">Bloquer des articles pour la vente ou pour l'achat</span><span class="sxs-lookup"><span data-stu-id="2ec3f-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="2ec3f-104">Vous pouvez bloquer un article pour la saisie dans des lignes de vente ou d'achat, et vous pouvez le bloquer pour la validation dans n'importe quelle transaction.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="2ec3f-105">Le tableau suivant illustre ce qui se produit lorsque les articles sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="2ec3f-106">Option</span><span class="sxs-lookup"><span data-stu-id="2ec3f-106">Option</span></span>|<span data-ttu-id="2ec3f-107">Désignation</span><span class="sxs-lookup"><span data-stu-id="2ec3f-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="2ec3f-108">**Bloqué à la vente**</span><span class="sxs-lookup"><span data-stu-id="2ec3f-108">**Sales Blocked**</span></span>|<span data-ttu-id="2ec3f-109">Vous ne pouvez pas saisir l'article dans un document vente ou dans une feuille article vente.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="2ec3f-110">**Bloqué à l'achat**</span><span class="sxs-lookup"><span data-stu-id="2ec3f-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="2ec3f-111">Vous ne pouvez pas saisir l'article dans un document achat, dans une feuille article d'achat, ou dans les processus de planification achat.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="2ec3f-112">**Bloqué**</span><span class="sxs-lookup"><span data-stu-id="2ec3f-112">**Blocked**</span></span>|<span data-ttu-id="2ec3f-113">Vous ne pouvez pas utiliser l'article pour une transaction d'article.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="2ec3f-114">Pour plus d'informations sur le blocage d'un article pour quelle que raison possible, voir Fiche article.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="2ec3f-115">Pour bloquer un article pour la saisie sur des lignes vente</span><span class="sxs-lookup"><span data-stu-id="2ec3f-115">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="2ec3f-116">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2ec3f-117">Sélectionnez l'article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué à la vente**.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-117">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="2ec3f-118">Si vous essayez de saisir l'article sur un document vente ou une ligne feuille, vous recevez désormais un message d'erreur indiquant que l'article est bloqué.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-118">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="2ec3f-119">Pour bloquer un article pour la saisie sur des lignes achat</span><span class="sxs-lookup"><span data-stu-id="2ec3f-119">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="2ec3f-120">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2ec3f-121">Sélectionnez l'article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué à l'achat**.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-121">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="2ec3f-122">Si vous essayez de saisir l'article sur un document achat ou une ligne feuille, vous recevez désormais un message d'erreur indiquant que l'article est bloqué.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-122">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="2ec3f-123">Pour bloquer un article à valider</span><span class="sxs-lookup"><span data-stu-id="2ec3f-123">To block an item from being posted</span></span>
1. <span data-ttu-id="2ec3f-124">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="2ec3f-125">Sélectionnez l'article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué**.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-125">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="2ec3f-126">Si vous essayez de valider tout type de transaction pour l'article, un message d'erreur indiquant que l'article est bloqué s'affiche désormais.</span><span class="sxs-lookup"><span data-stu-id="2ec3f-126">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ec3f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ec3f-127">See Also</span></span>  
[<span data-ttu-id="2ec3f-128">Enregistrer de nouveaux articles</span><span class="sxs-lookup"><span data-stu-id="2ec3f-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="2ec3f-129">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="2ec3f-129">Inventory</span></span>](inventory-manage-inventory.md)  
