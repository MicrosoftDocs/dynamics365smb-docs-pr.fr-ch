---
title: "Créer une facture achat à partir d'une facture vente pour acheter des articles pour une vente | Microsoft Docs"
description: "Depuis une facture vente, pour acheter des biens, vous pouvez créer une facture achat pour un fournisseur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 05/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2d7eb238395a0b1060668996fbbc3e13d9dd8a94
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-purchase-items-for-a-sale"></a><span data-ttu-id="9a11e-103">Procédure : acheter des articles pour une vente</span><span class="sxs-lookup"><span data-stu-id="9a11e-103">How to: Purchase Items for a Sale</span></span>
<span data-ttu-id="9a11e-104">Avec les commandes vente et les factures vente, vous pouvez utiliser des fonctions vous permettant de créer rapidement des documents achat pour des quantités d'articles manquantes requises par la vente.</span><span class="sxs-lookup"><span data-stu-id="9a11e-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="9a11e-105">Vous pouvez utiliser deux fonctions distinctes selon le type document.</span><span class="sxs-lookup"><span data-stu-id="9a11e-105">You can use two different functions depending on the document type.</span></span>
|<span data-ttu-id="9a11e-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="9a11e-106">Function</span></span>|<span data-ttu-id="9a11e-107">Désignation</span><span class="sxs-lookup"><span data-stu-id="9a11e-107">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="9a11e-108">**Créer des commandes achat**</span><span class="sxs-lookup"><span data-stu-id="9a11e-108">**Create Purchase Orders**</span></span>|<span data-ttu-id="9a11e-109">Depuis une commande vente, cette fonction crée une commande achat pour chaque fournisseur des articles de la commande vente.</span><span class="sxs-lookup"><span data-stu-id="9a11e-109">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="9a11e-110">Vous pouvez modifier la quantité d'achat avant de créer les commandes achat.</span><span class="sxs-lookup"><span data-stu-id="9a11e-110">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="9a11e-111">Seules les quantités de vente indisponibles sont proposées.</span><span class="sxs-lookup"><span data-stu-id="9a11e-111">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="9a11e-112">**Créer une facture achat**</span><span class="sxs-lookup"><span data-stu-id="9a11e-112">**Create Purchase Invoice**</span></span>|<span data-ttu-id="9a11e-113">Depuis une commande vente et une facture vente, cette fonction crée une facture achat pour un fournisseur sélectionné pour toutes les lignes ou toutes les lignes sélectionnées sur le document vente.</span><span class="sxs-lookup"><span data-stu-id="9a11e-113">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="9a11e-114">La quantité vendue totale est suggérée.</span><span class="sxs-lookup"><span data-stu-id="9a11e-114">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="9a11e-115">Pour créer une ou plusieurs commandes achat à partir d'une commande vente</span><span class="sxs-lookup"><span data-stu-id="9a11e-115">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="9a11e-116">Pour créer une commande achat pour chaque quantité d'article indisponible de la commande vente, vous utilisez la fonction **Créer des commandes achat**.</span><span class="sxs-lookup"><span data-stu-id="9a11e-116">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="9a11e-117">Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**.</span><span class="sxs-lookup"><span data-stu-id="9a11e-117">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="9a11e-118">Pour plus d'informations, voir [Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="9a11e-118">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

1. <span data-ttu-id="9a11e-119">Sur la page d'accueil, sélectionnez la mosaïque **Commandes vente en cours**.</span><span class="sxs-lookup"><span data-stu-id="9a11e-119">On the Home page, choose the **Ongoing Sales Orders** tile.</span></span>
2. <span data-ttu-id="9a11e-120">Ouvrez une commande vente pour laquelle vous souhaitez acheter des articles.</span><span class="sxs-lookup"><span data-stu-id="9a11e-120">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="9a11e-121">Sélectionnez l'action **Créer des commandes achat**.</span><span class="sxs-lookup"><span data-stu-id="9a11e-121">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="9a11e-122">La fenêtre **Créer des commandes achat** s'ouvre affichant une ligne pour chaque article différent sur la commande vente.</span><span class="sxs-lookup"><span data-stu-id="9a11e-122">The **Create Purchase Orders** window opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="9a11e-123">Les lignes des deux des quantités vendues entièrement disponibles et des quantités vendues indisponibles (grisées) sont affichées par défaut.</span><span class="sxs-lookup"><span data-stu-id="9a11e-123">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="9a11e-124">Vous pouvez choisir l'action **Afficher non disponible** pour afficher uniquement les lignes des quantités vendues indisponibles.</span><span class="sxs-lookup"><span data-stu-id="9a11e-124">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="9a11e-125">Le champ **Quantité à acheter** indique la quantité vendue indisponible par défaut.</span><span class="sxs-lookup"><span data-stu-id="9a11e-125">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="9a11e-126">Pour acheter une autre quantité que la quantité vendue indisponible, modifiez la valeur dans le champ **Quantité à acheter**.</span><span class="sxs-lookup"><span data-stu-id="9a11e-126">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="9a11e-127">Vous pouvez également modifier le champ **Quantité à acheter** sur les lignes grisées bien qu'ils représentent des quantités vendues entièrement disponibles.</span><span class="sxs-lookup"><span data-stu-id="9a11e-127">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="9a11e-128">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a11e-128">Choose the **OK** button.</span></span> 
    
    <span data-ttu-id="9a11e-129">Une commande achat est créée pour chaque fournisseur des articles de la commande vente, notamment toutes les modifications de quantité que vous avez apportées à la fenêtre **Créer des commandes achat**.</span><span class="sxs-lookup"><span data-stu-id="9a11e-129">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made in the **Create Purchase Orders** window.</span></span>
7. <span data-ttu-id="9a11e-130">Traitez maintenant la ou les commandes achat, par exemple, en modifiant ou en ajoutant des lignes commande achat.</span><span class="sxs-lookup"><span data-stu-id="9a11e-130">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="9a11e-131">Pour plus d'informations, reportez-vous à [Procédure : enregistrer des achats](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="9a11e-131">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="9a11e-132">Pour créer une facture achat à partir d'une commande vente ou une facture vente</span><span class="sxs-lookup"><span data-stu-id="9a11e-132">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="9a11e-133">Pour créer une facture achat unique pour une ou plusieurs lignes d'un document vente en sélectionnant d'abord le fournisseur auquel acheter, vous utilisez la fonction **Créer une facture achat**.</span><span class="sxs-lookup"><span data-stu-id="9a11e-133">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="9a11e-134">Cette fonction crée une facture achat pour la quantité d'articles exacte du document vente sélectionné.</span><span class="sxs-lookup"><span data-stu-id="9a11e-134">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="9a11e-135">Pour modifier la quantité d'achat, vous devez modifier la facture achat après qu'elle soit créée.</span><span class="sxs-lookup"><span data-stu-id="9a11e-135">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="9a11e-136">Sur la page d'accueil, sélectionnez la mosaïque **Factures vente en cours**.</span><span class="sxs-lookup"><span data-stu-id="9a11e-136">On the Home page, choose the **Ongoing Sales Invoices** tile.</span></span>
2. <span data-ttu-id="9a11e-137">Ouvrez une facture vente pour laquelle vous souhaitez acheter des articles.</span><span class="sxs-lookup"><span data-stu-id="9a11e-137">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="9a11e-138">Sélectionnez une ou plusieurs lignes facture vente que vous souhaitez utiliser dans la facture achat.</span><span class="sxs-lookup"><span data-stu-id="9a11e-138">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="9a11e-139">Pour utiliser toutes les lignes facture vente, sélectionnez-les toutes ou ne sélectionnez aucune ligne.</span><span class="sxs-lookup"><span data-stu-id="9a11e-139">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="9a11e-140">Sélectionnez l'action **Créer une facture achat**.</span><span class="sxs-lookup"><span data-stu-id="9a11e-140">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="9a11e-141">Sélectionnez **Toutes les lignes** ou **Lignes sélectionnées**, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a11e-141">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="9a11e-142">Dans la liste des fournisseurs qui s'affiche, sélectionnez le fournisseur dont vous souhaitez acheter tous les articles, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a11e-142">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="9a11e-143">Une facture achat ayant une seule, plusieurs ou toutes les lignes de la facture vente, est créée.</span><span class="sxs-lookup"><span data-stu-id="9a11e-143">A purchase invoice is created that contains one, more, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="9a11e-144">Traitez maintenant la facture achat, par exemple, en modifiant ou en ajoutant des lignes facture achat.</span><span class="sxs-lookup"><span data-stu-id="9a11e-144">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="9a11e-145">Pour plus d'informations, reportez-vous à [Procédure : enregistrer des achats](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="9a11e-145">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9a11e-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a11e-146">See Also</span></span>
[<span data-ttu-id="9a11e-147">Achats</span><span class="sxs-lookup"><span data-stu-id="9a11e-147">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="9a11e-148">Procédure : enregistrer des achats</span><span class="sxs-lookup"><span data-stu-id="9a11e-148">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="9a11e-149">Procédure : facturer des ventes</span><span class="sxs-lookup"><span data-stu-id="9a11e-149">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="9a11e-150">Procédure : enregistrer de nouveaux fournisseurs</span><span class="sxs-lookup"><span data-stu-id="9a11e-150">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="9a11e-151">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9a11e-151">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

