---
title: "Créer une commande vente liée à une commande achat pour une livraison directe | Microsoft Docs"
description: "Décrit comment créer une commande vente liée à une commande achat pour permettre la livraison directe du fournisseur au client."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 990867cb428f860b1001177738d1a027f72485bc
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-make-drop-shipments"></a><span data-ttu-id="71f19-103">Procédure : effectuer des livraisons directes</span><span class="sxs-lookup"><span data-stu-id="71f19-103">How to: Make Drop Shipments</span></span>
<span data-ttu-id="71f19-104">Lors d'une livraison directe, un ou plusieurs articles de l'un de vos fournisseurs sont livrés directement chez l'un de vos clients.</span><span class="sxs-lookup"><span data-stu-id="71f19-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="71f19-105">Lorsqu'une commande vente est marquée pour livraison directe, et lorsque vous créez une commande achat spécifiant le client dans le champ **N° donneur d'ordre**</span><span class="sxs-lookup"><span data-stu-id="71f19-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="71f19-106">, vous pouvez ensuite associer les deux documents et par conséquent informer le fournisseur de procéder directement à l'envoi au client.</span><span class="sxs-lookup"><span data-stu-id="71f19-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="71f19-107">Pour créer une commande vente pour des livraisons directes</span><span class="sxs-lookup"><span data-stu-id="71f19-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="71f19-108">Pour préparer une livraison directe, vous créez une commande vente pour un article, sauf que vous devez indiquer sur la ligne vente que la vente exige la livraison directe.</span><span class="sxs-lookup"><span data-stu-id="71f19-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="71f19-109">Créez une commande vente pour un article.</span><span class="sxs-lookup"><span data-stu-id="71f19-109">Create a sales order for an item.</span></span> <span data-ttu-id="71f19-110">Pour en savoir plus, voir [Procédure : vendre des produits](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="71f19-110">For more information, see [How to: Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="71f19-111">Sur la ligne commande vente pour l'article envoyé, cochez la case **Livraison directe**.</span><span class="sxs-lookup"><span data-stu-id="71f19-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="71f19-112">Utilisez la fonction **Choisir les colonnes** si le champ n'est pas visible.</span><span class="sxs-lookup"><span data-stu-id="71f19-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="71f19-113">Pour plus d'informations, voir [Personnalisation utilisateur](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="71f19-113">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="71f19-114">Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**.</span><span class="sxs-lookup"><span data-stu-id="71f19-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="71f19-115">Pour plus d'informations, voir [Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="71f19-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="71f19-116">Pour créer la commande achat pour livraison directe</span><span class="sxs-lookup"><span data-stu-id="71f19-116">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="71f19-117">Pour préparer une livraison directe pour l'article mis en vente, vous créez une commande achat, comme à l'accoutumée, sauf que vous devez indiquer sur la commande achat qu'elle doit être envoyée à votre client et non pas à vous-même.</span><span class="sxs-lookup"><span data-stu-id="71f19-117">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="71f19-118">Créez une commande achat.</span><span class="sxs-lookup"><span data-stu-id="71f19-118">Create a purchase order.</span></span> <span data-ttu-id="71f19-119">Ne remplissez pas les champs sur les lignes.</span><span class="sxs-lookup"><span data-stu-id="71f19-119">Do not fill any fields on the lines.</span></span> <span data-ttu-id="71f19-120">Pour plus d'informations, reportez-vous à [Procédure : enregistrer des achats](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="71f19-120">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="71f19-121">Dans le champ **N° donneur d'ordre**</span><span class="sxs-lookup"><span data-stu-id="71f19-121">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="71f19-122">, sélectionnez le client auquel vous souhaitez vendre l'article en question.</span><span class="sxs-lookup"><span data-stu-id="71f19-122">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="71f19-123">Choisissez l'action **Livraisons directes**, puis choisissez l'option **Extraire commande vente**.</span><span class="sxs-lookup"><span data-stu-id="71f19-123">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="71f19-124">Dans la fenêtre **Liste des ventes**, sélectionnez la commande vente que vous avez préparée dans la section « Créer une commande vente pour livraison directe ».</span><span class="sxs-lookup"><span data-stu-id="71f19-124">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="71f19-125">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="71f19-125">Choose the **OK** button.</span></span>

<span data-ttu-id="71f19-126">Les informations de ligne de la commande vente sont insérées sur la/les ligne(s) commande achat.</span><span class="sxs-lookup"><span data-stu-id="71f19-126">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="71f19-127">Vous pouvez maintenant informer le fournisseur quant à l'envoi des articles à votre client, par exemple en envoyant la commande achat au format PDF.</span><span class="sxs-lookup"><span data-stu-id="71f19-127">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="71f19-128">Pour afficher la commande achat associée à partir de la commande vente</span><span class="sxs-lookup"><span data-stu-id="71f19-128">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="71f19-129">Sélectionnez la ligne commande vente livraison directe, choisissez l'action **Commande**, puis l'action **Livraison directe** et enfin l'action **Commande achat**.</span><span class="sxs-lookup"><span data-stu-id="71f19-129">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="71f19-130">Pour valider une livraison directe</span><span class="sxs-lookup"><span data-stu-id="71f19-130">To post a drop shipment</span></span>
<span data-ttu-id="71f19-131">Lorsque le fournisseur a expédié les articles, vous pouvez valider la commande vente comme envoyée.</span><span class="sxs-lookup"><span data-stu-id="71f19-131">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="71f19-132">Vous pouvez également valider la commande achat, mais uniquement avec l'option **Réceptionner** jusqu'à ce que la commande vente ait été facturée.</span><span class="sxs-lookup"><span data-stu-id="71f19-132">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="71f19-133">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="71f19-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="71f19-134">Ouvrez les commandes vente que vous avez créées dans la section « Pour créer une commande vente pour une livraison directe ».</span><span class="sxs-lookup"><span data-stu-id="71f19-134">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="71f19-135">Dans le champ **Qté à expédier**, spécifiez la quantité de commandes à envoyer, la quantité de commandes partielles ou totales.</span><span class="sxs-lookup"><span data-stu-id="71f19-135">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="71f19-136">Sélectionnez l'action **Valider** ou **Valider et envoyer**.</span><span class="sxs-lookup"><span data-stu-id="71f19-136">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="71f19-137">Sélectionnez l'option **Livrer** pour facturer ultérieurement ou l'option **Livrer et facturer** pour facturer immédiatement.</span><span class="sxs-lookup"><span data-stu-id="71f19-137">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="71f19-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71f19-138">See Also</span></span>
<span data-ttu-id="71f19-139">[Procédure : créer des commandes spéciales](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="71f19-139">[How to: Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="71f19-140">Procédure : vendre des produits</span><span class="sxs-lookup"><span data-stu-id="71f19-140">How to: Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="71f19-141">Procédure : enregistrer des achats</span><span class="sxs-lookup"><span data-stu-id="71f19-141">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="71f19-142">Ventes</span><span class="sxs-lookup"><span data-stu-id="71f19-142">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="71f19-143">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="71f19-143">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="71f19-144">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="71f19-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

