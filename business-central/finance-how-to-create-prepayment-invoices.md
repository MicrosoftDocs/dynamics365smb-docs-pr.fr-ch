---
title: "Procédure : créer des factures d'acompte | Microsoft Docs"
description: Découvrez comment gérer les situations où votre fournisseur ou vous-même exigez un acompte.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 96433274efa8ea8f5ec93248f4a7c992e456aa26
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243564"
---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="7e9a4-103">Créer des factures d'acompte</span><span class="sxs-lookup"><span data-stu-id="7e9a4-103">Create Prepayment Invoices</span></span>
<span data-ttu-id="7e9a4-104">Si vous voulez que vos clients fassent des paiements avant de leur expédier une commande ou si votre fournisseur exige que vous fassiez un paiement avant de vous expédier une commande, vous pouvez utiliser la fonctionnalité Acompte.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-104">If you require your customers to submit payment before you ship an order to them, or if your vendor requires you to submit payment before they ship an order to you, you can use the prepayment functionality.</span></span>  

<span data-ttu-id="7e9a4-105">Après avoir créé une commande vente ou achat, vous pouvez créer une facture acompte.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-105">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="7e9a4-106">Vous pouvez utiliser les pourcentages par défaut pour chaque ligne vente ou achat, ou ajuster le montant en fonction si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-106">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="7e9a4-107">Par exemple, vous pouvez spécifier un montant total pour la facture entière.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-107">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="7e9a4-108">La procédure suivante décrit comment facturer un acompte pour des commandes vente.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-108">The following procedure describes how to invoice a prepayment for a sales orders.</span></span> <span data-ttu-id="7e9a4-109">La procédure est identique pour des commandes achat.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-109">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="7e9a4-110">Pour créer une facture acompte</span><span class="sxs-lookup"><span data-stu-id="7e9a4-110">To create a prepayment invoice</span></span>  
1. <span data-ttu-id="7e9a4-111">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7e9a4-112">Créez une commande vente.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-112">Create a new sales order.</span></span> <span data-ttu-id="7e9a4-113">Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="7e9a4-113">For more information, see [sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="7e9a4-114">Sur le raccourci **Acompte** le champ **% acompte** est renseigné automatiquement si un pourcentage d'acompte par défaut figure sur la fiche client.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-114">On the **Prepayment** FastTab, the **Prepayment %** field will be filled in automatically if there is a default prepayment percentage on the customer card.</span></span> <span data-ttu-id="7e9a4-115">Vous pouvez modifier le contenu du champ.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-115">You can change the contents of the field.</span></span> <span data-ttu-id="7e9a4-116">Le pourcentage d'acompte est uniquement copié à partir de l'en-tête vers les lignes qui ne copient pas le pourcentage d'acompte par défaut à partir de l'article.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-116">The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.</span></span>  

    <span data-ttu-id="7e9a4-117">La sélection du champ **Compresser acompte** signifie que les lignes sont combinées sur la facture si :</span><span class="sxs-lookup"><span data-stu-id="7e9a4-117">If the **Compress Prepayment** field is selected, lines will be combined on the invoice if:</span></span>  
    - <span data-ttu-id="7e9a4-118">Elles ont le même compte général pour les acomptes,comme déterminé par les paramètres comptabilisation.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-118">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="7e9a4-119">Elles sont les mêmes dimensions.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-119">They have the same dimensions.</span></span>  

    <span data-ttu-id="7e9a4-120">Laissez le champ vide si vous souhaitez spécifier une facture acompte avec une ligne pour chaque ligne commande vente à laquelle un pourcentage d'acompte est associé.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-120">Leave the field blank if you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage.</span></span>  

3. <span data-ttu-id="7e9a4-121">Renseignez les lignes vente.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-121">Fill in the sales lines.</span></span>  

    <span data-ttu-id="7e9a4-122">Si des pourcentages d'acompte par défaut ont été configurés pour vos articles, ils sont copiés automatiquement dans le champ **% acompte** sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-122">If default prepayment percentages have been set up for your items, they are automatically copied to the **Prepayment %** field on the line.</span></span> <span data-ttu-id="7e9a4-123">Sinon, le pourcentage d'acompte est copié à partir de l'en-tête.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-123">Otherwise, the prepayment percentage is copied from the header.</span></span> <span data-ttu-id="7e9a4-124">Vous pouvez modifier le contenu du champ **% acompte** sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-124">You can change the contents of the **Prepayment %** field on the line.</span></span>  
4. <span data-ttu-id="7e9a4-125">Si vous voulez appliquer un pourcentage d'acompte à la commande entière, modifiez le champ **% acompte** dans l'en\-tête après avoir renseigné les lignes.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-125">If you want to apply one prepayment percentage to the entire order, change the **Prepayment %** field on the header after filling in the lines.</span></span>  
5. <span data-ttu-id="7e9a4-126">Pour visualiser le montant d'acompte total, choisissez l'action **Statistiques**.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-126">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="7e9a4-127">Pour ajuster le montant d'acompte total pour la commande, vous pouvez modifier le contenu du champ **Montant acompte** de la page **Statistiques commande vente**.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-127">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field on the **Sales Order Statistics** page.</span></span>  

    <span data-ttu-id="7e9a4-128">Si le champ **Prix TVA comprise** est sélectionné, le champ **Montant acompte TTC** est modifiable.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-128">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="7e9a4-129">Si vous modifiez la valeur du champ **Montant acompte**, le montant est réparti de façon proportionnelle entre toutes les lignes, à l'exception de celles qui contiennent la valeur **0** dans le champ **% acompte**.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-129">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  
6. <span data-ttu-id="7e9a4-130">Pour effectuer une impression test avant de valider la facture d'acompte, sélectionnez l'action **Acompte**, puis choisissez **Impression test acompte**.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-130">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
7. <span data-ttu-id="7e9a4-131">Pour valider la facture d'acompte, sélectionnez l'action **Acompte**, puis l'action **Valider facture acompte**.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-131">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="7e9a4-132">Pour valider et imprimer la facture acompte, choisissez l'action **Valider et imprimer facture acompte**.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-132">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="7e9a4-133">Vous pouvez émettre des factures acompte supplémentaires pour la commande.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-133">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="7e9a4-134">Pour ce faire, augmentez le montant d'acompte sur une ou plusieurs lignes, ajustez la date document si nécessaire, puis validez la facture acompte.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-134">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="7e9a4-135">Une nouvelle facture est créée pour la différence entre les montants d'acompte facturés et le nouveau montant d'acompte.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-135">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7e9a4-136">Si vous êtes situé en Amérique du Nord, vous ne pouvez pas modifier le pourcentage d'acompte après la facture acompte validée.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-136">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="7e9a4-137">Cela est empêché dans la version nord\-américaine de [!INCLUDE[d365fin](includes/d365fin_md.md)], car le calcul de la taxe sur les ventes est sinon incorrect.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-137">This is prevented in the North American version of [!INCLUDE[d365fin](includes/d365fin_md.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="7e9a4-138">Lorsque vous êtes prêt à valider le reste de la facture, validez-le comme n'importe quelle facture. Le montant d'acompte est automatiquement déduit du montant dû.</span><span class="sxs-lookup"><span data-stu-id="7e9a4-138">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7e9a4-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e9a4-139">See Also</span></span>  
[<span data-ttu-id="7e9a4-140">Facturation d'acomptes</span><span class="sxs-lookup"><span data-stu-id="7e9a4-140">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="7e9a4-141">Procédure pas à pas : configuration et facturation d'acomptes</span><span class="sxs-lookup"><span data-stu-id="7e9a4-141">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="7e9a4-142">Finances</span><span class="sxs-lookup"><span data-stu-id="7e9a4-142">Finance</span></span>](finance.md)  
<span data-ttu-id="7e9a4-143">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7e9a4-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
