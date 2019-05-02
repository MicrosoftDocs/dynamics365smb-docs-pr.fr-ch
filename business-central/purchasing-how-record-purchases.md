---
title: Créer une facture achat et enregistrer les achats | Microsoft Docs
description: Décrit comment acheter des articles stock ou service en créant et en validant des factures ou des commandes achat.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: cc0a5e88342e9f4c7493cf9d3390c248e6dd36b9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821187"
---
# <a name="record-purchases"></a><span data-ttu-id="3923e-103">Enregistrer des achats</span><span class="sxs-lookup"><span data-stu-id="3923e-103">Record Purchases</span></span>
<span data-ttu-id="3923e-104">Vous créez une facture achat ou une commande achat pour enregistrer le coût d'achats et suivre les créances.</span><span class="sxs-lookup"><span data-stu-id="3923e-104">You create a purchase invoice or purchase order to record the cost of purchases and to track accounts payable.</span></span> <span data-ttu-id="3923e-105">Si vous devez contrôler un stock, les factures achat et les commandes achat sont également utilisées pour mettre à jour de manière dynamique les niveaux de stock afin que vous puissiez réduire vos coûts et fournir un meilleur service client.</span><span class="sxs-lookup"><span data-stu-id="3923e-105">If you need to control an inventory, purchase invoices and purchase orders are also used to dynamically update inventory levels so that you can minimize your inventory costs and provide better customer service.</span></span> <span data-ttu-id="3923e-106">Le prix d'achat, notamment les frais de service, et les valeurs d'inventaire qui résultent de la validation des factures achat ou des commandes contribuent aux chiffres du profit et à d'autres KPI financiers sur votre Tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="3923e-106">The purchasing costs, including service expenses, and inventory values that result from posting purchase invoices or orders contribute to profit figures and other financial KPIs on your Role Center.</span></span>

> [!NOTE]  
>   <span data-ttu-id="3923e-107">Vous devez utiliser les commandes achat si votre processus de vente exige que vous enregistriez des réceptions partielles d'une quantité de commande, par exemple, si la quantité totale n'était pas disponible auprès du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3923e-107">You must use purchase orders if your purchasing process requires that you record partial receipts of an order quantity, for example, because the full quantity was not available at the vendor.</span></span> <span data-ttu-id="3923e-108">Si vous commercialisez des articles en les livrant directement depuis votre fournisseur auprès de votre client, vous devez également utiliser les commandes achat.</span><span class="sxs-lookup"><span data-stu-id="3923e-108">If you sell items by delivering directly from your vendor to your customer, as a drop shipment, then you must also use purchase orders.</span></span> <span data-ttu-id="3923e-109">Pour plus d'informations, voir [Effectuer des livraisons directes](sales-how-drop-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="3923e-109">For more information, see [Make Drop Shipments](sales-how-drop-shipment.md).</span></span> <span data-ttu-id="3923e-110">Pour tous les autres aspects, les commandes achat fonctionnent de la même manière que les factures achat.</span><span class="sxs-lookup"><span data-stu-id="3923e-110">In all other aspects, purchase orders work the same way as purchase invoices.</span></span> <span data-ttu-id="3923e-111">La procédure suivante se base sur une facture achat.</span><span class="sxs-lookup"><span data-stu-id="3923e-111">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="3923e-112">La procédure est identique pour une commande achat.</span><span class="sxs-lookup"><span data-stu-id="3923e-112">The steps are similar for a purchase order.</span></span>

<span data-ttu-id="3923e-113">Lorsque vous recevez des articles de stock, ou lorsque le service acheté est terminé, vous validez la facture ou une commande achat pour mettre à jour le stock et les enregistrements financiers et pour activer le paiement au fournisseur selon les conditions de paiement.</span><span class="sxs-lookup"><span data-stu-id="3923e-113">When you receive the inventory items, or when the purchased service is completed, you post the purchase invoice or order to update inventory and financial records and to activate payment to the vendor according to the payment terms.</span></span> <span data-ttu-id="3923e-114">Pour plus d'informations, reportez-vous à [Effectuer des paiements](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="3923e-114">For more information, see [Making Payments](payables-make-payments.md).</span></span>

> [!CAUTION]  
>   <span data-ttu-id="3923e-115">Ne validez pas une facture achat tant que vous n'avez pas reçu les articles et que vous ne connaissez pas le coût total de l'achat, frais supplémentaires compris.</span><span class="sxs-lookup"><span data-stu-id="3923e-115">Do not post a purchase invoice until you receive the items and know the final cost of the purchase, including any additional charges.</span></span> <span data-ttu-id="3923e-116">Sinon, la valeur du stock et les chiffres du profit peuvent être biaisés.</span><span class="sxs-lookup"><span data-stu-id="3923e-116">Otherwise, your inventory value and profit figures may be skewed.</span></span>

<span data-ttu-id="3923e-117">Vous pouvez facilement corriger ou annuler une facture achat validée avant de payer le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3923e-117">You can easily correct or cancel a posted purchase invoice before you pay the vendor.</span></span> <span data-ttu-id="3923e-118">Cela est utile si vous souhaitez corriger une erreur de saisie ou si vous souhaitez modifier l'achat assez tôt dans le processus de commande.</span><span class="sxs-lookup"><span data-stu-id="3923e-118">This is useful if you want to correct a typing mistake or if you want to change the purchase early in the order process.</span></span> <span data-ttu-id="3923e-119">Pour plus d'informations, voir [Corriger ou annuler des factures achat impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="3923e-119">For more information, see [Correct or Cancel Unpaid Purchase Invoices](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span></span> <span data-ttu-id="3923e-120">Si vous avez déjà payé des articles sur la facture achat validée, vous devez créer un avoir achat pour contrepasser l'achat.</span><span class="sxs-lookup"><span data-stu-id="3923e-120">If you have already paid for items on the posted purchase invoice, then you must create a purchase credit memo to reverse the purchase.</span></span> <span data-ttu-id="3923e-121">Pour plus d'informations, reportez-vous à [Traiter les retours ou annulations d'achats](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="3923e-121">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="3923e-122">La fiche article peut être de type **Stock**, **Service** et **Hors stock** pour spécifier si l'article est une unité de stock physique, une unité de temps de travail ou une unité physique qui n'est pas conservée dans le stock.</span><span class="sxs-lookup"><span data-stu-id="3923e-122">The item card can be of type **Inventory**, **Service**, and **Non-Inventory** to specify if the item is a physical inventory unit, a labor time unit, or a physical unit that is not kept on inventory.</span></span> <span data-ttu-id="3923e-123">Pour plus d'informations, reportez vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="3923e-123">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span> <span data-ttu-id="3923e-124">Le processus de facture achat est identique pour les trois types d'article.</span><span class="sxs-lookup"><span data-stu-id="3923e-124">The purchase invoice process is the same for all three item types.</span></span>

<span data-ttu-id="3923e-125">Vous pouvez remplir les champs relatifs au fournisseur sur la facture achat de deux façons selon que le fournisseur est déjà enregistré ou non.</span><span class="sxs-lookup"><span data-stu-id="3923e-125">You can fill vendor fields on the purchase invoice in two ways depending on whether the vendor is already registered.</span></span>

## <a name="to-create-a-purchase-invoice"></a><span data-ttu-id="3923e-126">Pour créer une facture achat</span><span class="sxs-lookup"><span data-stu-id="3923e-126">To create a purchase invoice</span></span>
1. <span data-ttu-id="3923e-127">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures achat**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3923e-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3923e-128">Dans le champ **Fournisseur**, entrez le nom d'un fournisseur existant.</span><span class="sxs-lookup"><span data-stu-id="3923e-128">In the **Vendor** field, enter the name of an existing vendor.</span></span>

    <span data-ttu-id="3923e-129">D'autres champs de la page **Facture achat** sont désormais renseignés avec les informations standard sur le fournisseur sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3923e-129">Other fields on the **Purchase Invoice** page are now filled with the standard information of the selected vendor.</span></span> <span data-ttu-id="3923e-130">Si le fournisseur n'est pas enregistré, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3923e-130">If the vendor is not registered, then follow these steps:</span></span>
3. <span data-ttu-id="3923e-131">Dans le champ **Fournisseur**, entrez le nom du nouveau fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3923e-131">In the **Vendor** field, enter the name of the new vendor.</span></span>
4. <span data-ttu-id="3923e-132">Dans la boîte de dialogue d'enregistrement du nouveau fournisseur, cliquez sur le bouton **Oui**.</span><span class="sxs-lookup"><span data-stu-id="3923e-132">In the dialog box about registering the new vendor, choose the **Yes** button.</span></span>
5. <span data-ttu-id="3923e-133">Sur la page **Sélectionnez un modèle pour un nouveau fournisseur**, sélectionnez un modèle sur lequel baser la nouvelle fiche fournisseur, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="3923e-133">On the **Select a template for a new vendor** page, choose a template to base the new vendor card on, and then choose the **OK** button.</span></span>
6. <span data-ttu-id="3923e-134">Une nouvelle fiche fournisseur préremplie avec les informations sur le modèle fournisseur sélectionné s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="3923e-134">A new vendor card opens, prefilled with the information on the selected vendor template.</span></span> <span data-ttu-id="3923e-135">Le champ **Nom** est prérempli avec le nom du nouveau fournisseur que vous avez saisi sur la facture achat.</span><span class="sxs-lookup"><span data-stu-id="3923e-135">The **Name** field is prefilled with the new vendor’s name that you entered on the purchase invoice.</span></span>
7. <span data-ttu-id="3923e-136">Renseignez les autres champs de la fiche fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3923e-136">Proceed to fill in the remaining fields on the vendor card.</span></span> <span data-ttu-id="3923e-137">Pour plus d'informations, reportez vous à [Enregistrer de nouveaux fournisseurs](purchasing-how-register-new-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="3923e-137">For more information, see [Register New Vendors](purchasing-how-register-new-vendors.md).</span></span>  
8. <span data-ttu-id="3923e-138">Une fois que vous avez terminé la fiche fournisseur, cliquez sur le bouton **OK** pour revenir à la page **Facture achat**.</span><span class="sxs-lookup"><span data-stu-id="3923e-138">When you have completed the vendor card, choose the **OK** button to return to the **Purchase Invoice** page.</span></span>

    <span data-ttu-id="3923e-139">Plusieurs champs de la page **Facture achat** sont renseignés avec les informations que vous avez spécifiées sur la nouvelle fiche fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3923e-139">Several fields on the **Purchase Invoice** page are filled with information that you specified on the new vendor card.</span></span>
9. <span data-ttu-id="3923e-140">Renseignez les champs restants de la page **Facture achat**, selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="3923e-140">Fill in the remaining fields on the **Purchase Invoice** page as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    <span data-ttu-id="3923e-141">Vous êtes maintenant prêt à renseigner les lignes facture achat avec les articles en stock ou les services que vous avez achetés au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3923e-141">You are now ready to fill in the purchase invoice lines with inventory items or services that you have purchased from the vendor.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="3923e-142">Si vous avez défini des lignes achat récurrentes pour le fournisseur, par exemple un ordre de réapprovisionnement mensuel, vous pouvez insérer ces lignes sur la facture par l'intermédiaire de l'action **Extraire les lignes achat récurrentes**.</span><span class="sxs-lookup"><span data-stu-id="3923e-142">If you have set up recurring purchase lines for the vendor, such as a monthly replenishment order, then you can insert these lines on the invoice by choosing the **Get Recurring Purchase Lines** action.</span></span>
10. <span data-ttu-id="3923e-143">Dans le raccourci **Lignes**, dans le champ **N° article**, entrez le numéro d'un article de stock ou d'un service.</span><span class="sxs-lookup"><span data-stu-id="3923e-143">On the **Lines** FastTab, in the **Item No.** field, enter the number of an inventory item or service.</span></span>
11. <span data-ttu-id="3923e-144">Dans le champ **Quantité**, indiquez le nombre d'articles à acheter.</span><span class="sxs-lookup"><span data-stu-id="3923e-144">In the **Quantity** field, enter the number of items to be purchased.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="3923e-145">Pour les articles de type **Service**, la quantité est une unité de temps, telle que les heures, comme indiqué dans le champ **Code unité** de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3923e-145">For items of type **Service**, the quantity is a time unit, such as hours, as indicated in the **Unit of Measure Code** field on the line.</span></span>

    <span data-ttu-id="3923e-146">Le champ **Montant ligne** est mis à jour pour indiquer la valeur du champ **Coût unitaire direct** multipliée par la valeur du champ **Quantité**.</span><span class="sxs-lookup"><span data-stu-id="3923e-146">The **Line Amount** field is updated to show the value in the **Direct Unit Cost** field multiplied by the value in the **Quantity** field.</span></span>

    <span data-ttu-id="3923e-147">Le prix et le montant ligne sont affichés avec ou sans la Sales Tax en fonction de ce que vous avez sélectionné dans le champ **Prix incluant les taxes** de la fiche fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3923e-147">The price and line amount are shown with or without sales tax depending on what you selected in the **Prices Including Tax** field on the vendor card.</span></span>
12. <span data-ttu-id="3923e-148">Dans le champ **Montant remise facture**, entrez un montant qui doit être déduit de la valeur indiquée dans le champ **Total TTC** au bas de la facture.</span><span class="sxs-lookup"><span data-stu-id="3923e-148">In the **Invoice Discount Amount** field, enter an amount that should be deducted from the value shown in the **Total Incl. Tax** field at the bottom of the invoice.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="3923e-149">Si vous avez défini des remises facture pour le fournisseur, le pourcentage spécifié est automatiquement inséré dans le champ **% remise facture fournisseur** si les critères sont réunis, et le montant associé est inséré dans le champ **Montant remise facture**.</span><span class="sxs-lookup"><span data-stu-id="3923e-149">If you have set up invoice discounts for the vendor, then the specified percentage value is automatically inserted in the **Vendor Invoice Discount %** field if the criteria are met, and the related amount is inserted in the **Invoice Discount Amount** field.</span></span>
13. <span data-ttu-id="3923e-150">Lorsque vous recevez les articles ou services achetés, sélectionnez **Valider**.</span><span class="sxs-lookup"><span data-stu-id="3923e-150">When you receive the purchased items or services, choose **Post**.</span></span>

<span data-ttu-id="3923e-151">L'achat est désormais visible dans le stock et les enregistrements financiers, et le paiement fournisseur est activé.</span><span class="sxs-lookup"><span data-stu-id="3923e-151">The purchase is now reflected in inventory and financial records, and the vendor payment is activated.</span></span> <span data-ttu-id="3923e-152">La facture achat est supprimée de la liste des factures achat et remplacée par un nouveau document dans la liste des factures achat validées.</span><span class="sxs-lookup"><span data-stu-id="3923e-152">The purchase invoice is removed from the list of purchase invoices and replaced with a new document in the list of posted purchase invoices.</span></span>

## <a name="see-also"></a><span data-ttu-id="3923e-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3923e-153">See Also</span></span>
[<span data-ttu-id="3923e-154">Achats</span><span class="sxs-lookup"><span data-stu-id="3923e-154">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="3923e-155">Définition des achats</span><span class="sxs-lookup"><span data-stu-id="3923e-155">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="3923e-156">Demander des devis</span><span class="sxs-lookup"><span data-stu-id="3923e-156">Request Quotes</span></span>](purchasing-how-request-quotes.md)  
[<span data-ttu-id="3923e-157">Acheter des articles pour une vente</span><span class="sxs-lookup"><span data-stu-id="3923e-157">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="3923e-158">Enregistrer un nouveau fournisseur</span><span class="sxs-lookup"><span data-stu-id="3923e-158">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
[<span data-ttu-id="3923e-159">Préparer des livraisons directes</span><span class="sxs-lookup"><span data-stu-id="3923e-159">Prepare Drop Shipments</span></span>](sales-how-drop-shipment.md)  
<span data-ttu-id="3923e-160">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3923e-160">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>