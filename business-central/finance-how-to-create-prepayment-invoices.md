---
title: 'Procédure : créer des factures d’acompte | Microsoft Docs'
description: Découvrez comment gérer les situations où votre fournisseur ou vous-même exigez un acompte.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 72a073fcde9ddf20df7c138ab544afb6719b93ce
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782178"
---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="f7c66-103">Créer des factures d’acompte</span><span class="sxs-lookup"><span data-stu-id="f7c66-103">Create Prepayment Invoices</span></span>

<span data-ttu-id="f7c66-104">Si vous demandez à vos clients de soumettre le paiement avant de leur expédier une commande, vous pouvez utiliser la fonctionnalité d’acompte.</span><span class="sxs-lookup"><span data-stu-id="f7c66-104">If you require your customers to submit payment before you ship an order to them, you can use the prepayment functionality.</span></span> <span data-ttu-id="f7c66-105">Il en va de même si votre fournisseur vous demande de soumettre un paiement avant de vous expédier une commande.</span><span class="sxs-lookup"><span data-stu-id="f7c66-105">The same applies if your vendor requires you to submit payment before they ship an order to you.</span></span>  

<span data-ttu-id="f7c66-106">Vous pouvez lancer le traitement de l’acompte lorsque vous créez une commande vente ou achat.</span><span class="sxs-lookup"><span data-stu-id="f7c66-106">You can start the prepayment process when you create a sales or purchase order.</span></span> <span data-ttu-id="f7c66-107">Si vous avez un pourcentage acompte par défaut pour ce client ou fournisseur, celui-ci sera automatiquement inclus dans la facture acompte résultante.</span><span class="sxs-lookup"><span data-stu-id="f7c66-107">If you have a default prepayment percentage for this customer or vendor, that will be included automatically in the resulting prepayment invoice.</span></span> <span data-ttu-id="f7c66-108">Vous pouvez également spécifier un pourcentage acompte pour l’ensemble du document.</span><span class="sxs-lookup"><span data-stu-id="f7c66-108">You can also specify a prepayment percentage to the entire document.</span></span>

<span data-ttu-id="f7c66-109">Après avoir créé une commande vente ou achat, vous pouvez créer une facture acompte.</span><span class="sxs-lookup"><span data-stu-id="f7c66-109">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="f7c66-110">Vous pouvez utiliser les pourcentages par défaut pour chaque ligne vente ou achat, ou ajuster le montant en fonction si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f7c66-110">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="f7c66-111">Par exemple, vous pouvez spécifier un montant total pour la facture entière.</span><span class="sxs-lookup"><span data-stu-id="f7c66-111">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="f7c66-112">La procédure suivante décrit comment facturer un acompte pour une commande vente.</span><span class="sxs-lookup"><span data-stu-id="f7c66-112">The following procedure describes how to invoice a prepayment for a sales order.</span></span> <span data-ttu-id="f7c66-113">La procédure est identique pour des commandes achat.</span><span class="sxs-lookup"><span data-stu-id="f7c66-113">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="f7c66-114">Pour créer une facture acompte</span><span class="sxs-lookup"><span data-stu-id="f7c66-114">To create a prepayment invoice</span></span>

1. <span data-ttu-id="f7c66-115">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f7c66-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f7c66-116">Créez une commande vente pour le client approprié.</span><span class="sxs-lookup"><span data-stu-id="f7c66-116">Create a new sales order for the relevant customer.</span></span> <span data-ttu-id="f7c66-117">Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="f7c66-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="f7c66-118">Sur le raccourci **Acompte**, le champ **% acompte** spécifie le pourcentage à utiliser pour calculer le montant acompte.</span><span class="sxs-lookup"><span data-stu-id="f7c66-118">On the **Prepayment** FastTab, the **Prepayment %** field specifies the percentage to use to calculate the prepayment amount.</span></span> <span data-ttu-id="f7c66-119">Si un pourcentage d’acompte par défaut figure sur la fiche client, le champ est renseigné automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f7c66-119">If there is a default prepayment percentage on the customer card, the field is filled in automatically.</span></span> <span data-ttu-id="f7c66-120">Vous pouvez modifier le pourcentage.</span><span class="sxs-lookup"><span data-stu-id="f7c66-120">You can change the percentage.</span></span> <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    <span data-ttu-id="f7c66-121">Choisissez le champ **Compresser acompte** si vous souhaitez créer des lignes sur la facture d’acompte qui combinent des lignes de la commande client si :</span><span class="sxs-lookup"><span data-stu-id="f7c66-121">Choose the **Compress Prepayment** field if you want to create lines on the prepayment invoice that combine lines from the sales order if:</span></span>  

    - <span data-ttu-id="f7c66-122">Elles ont le même compte général pour les acomptes,comme déterminé par les paramètres comptabilisation.</span><span class="sxs-lookup"><span data-stu-id="f7c66-122">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="f7c66-123">Elles sont les mêmes dimensions.</span><span class="sxs-lookup"><span data-stu-id="f7c66-123">They have the same dimensions.</span></span>  

    <span data-ttu-id="f7c66-124">Si vous souhaitez spécifier une facture acompte avec une ligne pour chaque ligne commande vente à laquelle un pourcentage d’acompte est associé, alors ne choisissez pas le champ **Compresser acompte**.</span><span class="sxs-lookup"><span data-stu-id="f7c66-124">If you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage, then do not choose the **Compress Prepayment** field.</span></span>  

    <span data-ttu-id="f7c66-125">La date d’échéance de l’acompte est calculée automatiquement en fonction de la valeur du **Code conditions paiement acompte**.</span><span class="sxs-lookup"><span data-stu-id="f7c66-125">The due date for the prepayment is calculated automatically based on the value of the **Prepmt. Payment Terms Code**.</span></span>

3. <span data-ttu-id="f7c66-126">Renseignez les lignes vente.</span><span class="sxs-lookup"><span data-stu-id="f7c66-126">Fill in the sales lines.</span></span>  

    <span data-ttu-id="f7c66-127">Si vous avez spécifié un pourcentage acompte par défaut soit pour le client, soit sur le raccourci **Acompte** sur ce document, cette valeur est copiée sur chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="f7c66-127">If you have specified a default prepayment percentage either for the customer or on the **Prepayment** FastTab on this document, this value is copied to each line.</span></span> <span data-ttu-id="f7c66-128">Vous pouvez modifier le contenu du champ **% acompte** sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="f7c66-128">You can change the contents of the **Prepayment %** field on the line.</span></span>  

4. <span data-ttu-id="f7c66-129">Pour visualiser le montant d’acompte total, choisissez l’action **Statistiques**.</span><span class="sxs-lookup"><span data-stu-id="f7c66-129">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="f7c66-130">Pour ajuster le montant d’acompte total pour la commande, vous pouvez modifier le contenu du champ **Montant acompte** de la page **Statistiques commande vente**.</span><span class="sxs-lookup"><span data-stu-id="f7c66-130">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field on the **Sales Order Statistics** page.</span></span>  

    <span data-ttu-id="f7c66-131">Si le champ **Prix TVA comprise** est sélectionné, le champ **Montant acompte TTC** est modifiable.</span><span class="sxs-lookup"><span data-stu-id="f7c66-131">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="f7c66-132">Si vous modifiez la valeur du champ **Montant acompte**, le montant est réparti de façon proportionnelle entre toutes les lignes, à l’exception de celles qui contiennent la valeur **0** dans le champ **% acompte**.</span><span class="sxs-lookup"><span data-stu-id="f7c66-132">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  

5. <span data-ttu-id="f7c66-133">Pour effectuer une impression test avant de valider la facture d’acompte, sélectionnez l’action **Acompte**, puis choisissez **Impression test acompte**.</span><span class="sxs-lookup"><span data-stu-id="f7c66-133">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
6. <span data-ttu-id="f7c66-134">Pour valider la facture d’acompte, sélectionnez l’action **Acompte**, puis l’action **Valider facture acompte**.</span><span class="sxs-lookup"><span data-stu-id="f7c66-134">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="f7c66-135">Pour valider et imprimer la facture acompte, choisissez l’action **Valider et imprimer facture acompte**.</span><span class="sxs-lookup"><span data-stu-id="f7c66-135">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="f7c66-136">Vous pouvez émettre des factures acompte supplémentaires pour la commande.</span><span class="sxs-lookup"><span data-stu-id="f7c66-136">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="f7c66-137">Pour ce faire, augmentez le montant d’acompte sur une ou plusieurs lignes, ajustez la date document si nécessaire, puis validez la facture acompte.</span><span class="sxs-lookup"><span data-stu-id="f7c66-137">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="f7c66-138">Une nouvelle facture est créée pour la différence entre les montants d’acompte facturés et le nouveau montant d’acompte.</span><span class="sxs-lookup"><span data-stu-id="f7c66-138">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="f7c66-139">Si vous êtes situé en Amérique du Nord, vous ne pouvez pas modifier le pourcentage d’acompte après la facture acompte validée.</span><span class="sxs-lookup"><span data-stu-id="f7c66-139">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="f7c66-140">Cela est empêché dans la version nord\-américaine de [!INCLUDE[prod_short](includes/prod_short.md)], car le calcul de la taxe sur les ventes est sinon incorrect.</span><span class="sxs-lookup"><span data-stu-id="f7c66-140">This is prevented in the North American version of [!INCLUDE[prod_short](includes/prod_short.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="f7c66-141">Lorsque vous êtes prêt à valider le reste de la facture, validez-le comme n’importe quelle facture. Le montant d’acompte est automatiquement déduit du montant dû.</span><span class="sxs-lookup"><span data-stu-id="f7c66-141">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f7c66-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7c66-142">See Also</span></span>

[<span data-ttu-id="f7c66-143">Facturation d’acomptes</span><span class="sxs-lookup"><span data-stu-id="f7c66-143">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="f7c66-144">Procédure pas à pas : configuration et facturation d’acomptes</span><span class="sxs-lookup"><span data-stu-id="f7c66-144">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="f7c66-145">Finances</span><span class="sxs-lookup"><span data-stu-id="f7c66-145">Finance</span></span>](finance.md)  
<span data-ttu-id="f7c66-146">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7c66-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]