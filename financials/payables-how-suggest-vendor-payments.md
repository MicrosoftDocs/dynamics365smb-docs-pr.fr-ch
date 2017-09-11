---
title: Utilisez le traitement par lots Proposer paiements fournisseur| Microsoft Docs
description: "Vous pouvez spécifier les paramètres du paiement fournisseur pour obtenir des suggestions ou des propositions pour les paiements échus sous peu ou donnant lieu à une remise."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 50daaf0a9f0d3beb31a75aa8c554c8833b4d2c8e
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-suggest-vendor-payments"></a><span data-ttu-id="88be5-103">Procédure : proposer des paiements fournisseur</span><span class="sxs-lookup"><span data-stu-id="88be5-103">How to: Suggest Vendor Payments</span></span>
<span data-ttu-id="88be5-104">Dans la fenêtre **Feuille paiement**, vous pouvez utiliser le traitement par lots **Proposer paiements fournisseur** pour proposer des lignes paiement.</span><span class="sxs-lookup"><span data-stu-id="88be5-104">In the **Payment Journal** window, you can use the **Suggest Vendor Payments** batch job to suggest payment lines.</span></span> <span data-ttu-id="88be5-105">Des lignes pour des éléments tels que les paiements échus à courte échéance ou les paiements pour lesquels un escompte est disponible, sont proposées en fonction de vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="88be5-105">Lines for things like payments that are due soon, or payments where a payment discount is available, are suggested based on your settings.</span></span>

<span data-ttu-id="88be5-106">Pour bénéficier pleinement des lignes proposées, vous devez d'abord attribuer une priorité à vos fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="88be5-106">To benefit fully from suggested lines, you must first prioritize your vendors.</span></span> <span data-ttu-id="88be5-107">Pour plus d'informations, reportez-vous à [Procédure : octroyer une priorité à des fournisseurs](purchasing-how-prioritize-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="88be5-107">For more information, see [How to: Prioritize Vendors](purchasing-how-prioritize-vendors.md).</span></span>  

<span data-ttu-id="88be5-108">Les écritures fournisseur qui ne sont pas **En attente** ne sont pas incluses.</span><span class="sxs-lookup"><span data-stu-id="88be5-108">Vendor entries that are not **On Hold** are not included.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="88be5-109">Si vous souhaitez profiter d'escomptes et que vous avez saisi un montant disponible, ce montant est d'abord utilisé pour :</span><span class="sxs-lookup"><span data-stu-id="88be5-109">If you want to take advantage of payment discounts, and have entered an available amount, the amount will be used for:</span></span>  

* <span data-ttu-id="88be5-110">Les écritures fournisseur échues et prioritaires, par ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="88be5-110">Prioritized overdue vendor entries first in order of priority.</span></span>  
* <span data-ttu-id="88be5-111">Les écritures fournisseur échues et non prioritaires.</span><span class="sxs-lookup"><span data-stu-id="88be5-111">Overdue vendor entries that are not prioritized.</span></span>  
* <span data-ttu-id="88be5-112">Les écritures fournisseur ouvertes donnant lieu à un escompte, dans l'ordre des numéros des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="88be5-112">Open vendor entries that qualify for payment discounts, arranged by vendor number.</span></span>  

## <a name="to-use-the-suggest-vendor-payments-function"></a><span data-ttu-id="88be5-113">Pour utiliser la fonction Proposer paiements fournisseur</span><span class="sxs-lookup"><span data-stu-id="88be5-113">To use the Suggest Vendor Payments function</span></span>
1. <span data-ttu-id="88be5-114">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles paiement**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="88be5-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="88be5-115">Ouvrez la feuille appropriée, puis sélectionnez l'action **Proposer paiements fournisseur**.</span><span class="sxs-lookup"><span data-stu-id="88be5-115">Open the relevant journal, and then choose the **Suggest Vendor Payments** action.</span></span>  
3. <span data-ttu-id="88be5-116">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="88be5-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="88be5-117">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="88be5-117">Choose the **OK** button.</span></span>  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><span data-ttu-id="88be5-118">Pour insérer la date d'échéance comme date comptabilisation sur les lignes feuille paiement</span><span class="sxs-lookup"><span data-stu-id="88be5-118">To insert the due date as posting date on payment journal lines</span></span>
<span data-ttu-id="88be5-119">Lorsque vous utilisez le traitement par lots **Proposer paiements fournisseur** pour créer des lignes de paiement pour vos fournisseurs, vous pouvez remplir deux champs spéciaux pour vous assurer que les lignes générées utilisent la date d'échéance pour calculer la date comptabilisation.</span><span class="sxs-lookup"><span data-stu-id="88be5-119">When you use the **Suggest Vendor Payments** batch job to create payment lines for your vendors, you can fill two special fields to make sure that the generated lines use the due date to calculate the posting date.</span></span> <span data-ttu-id="88be5-120">Ces champs sont **Calculer la date comptabilisation à partir de la date d'échéance doc. lettrage** et **Décalage date d'échéance doc. lettrage**.</span><span class="sxs-lookup"><span data-stu-id="88be5-120">These fields are **Calculate Posting Date from Applies-to-Doc Due Date** and **Applies-to-Doc Due Date Offset**.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="88be5-121">Vous ne pouvez pas utiliser le champ **Calculate Posting Date from Applies-to-Doc Due Date** avec le champ **Find Payment Discounts** ou le champ **Summarize per Vendor**.</span><span class="sxs-lookup"><span data-stu-id="88be5-121">You cannot use the **Calculate Posting Date from Applies-to-Doc Due Date** field together with the **Find Payment Discounts** field or the **Summarize per Vendor** field.</span></span> <span data-ttu-id="88be5-122">Si la date comptabilisation est basée sur la date d'échéance, des escomptes fournisseur risquent de ne pas être calculés correctement, parce que la date comptabilisation peut se trouver après la date d'escompte.</span><span class="sxs-lookup"><span data-stu-id="88be5-122">If the posting date is based on the due date, some payment discounts may not calculate correctly because the posting date is after the payment discount date.</span></span>  

<span data-ttu-id="88be5-123">De plus, si la date comptabilisation calculée se trouve dans le passé, la date de comptabilisation est déplacée à la date de travail, et un message d'avertissement s'affiche.</span><span class="sxs-lookup"><span data-stu-id="88be5-123">Also, if the calculated posting date is in the past, then the posting date is moved up to the work date, and a warning is displayed.</span></span>  

<span data-ttu-id="88be5-124">Vous pouvez aussi créer manuellement des lignes de paiement à l'aide de la date d'échéance pour calculer la date comptabilisation.</span><span class="sxs-lookup"><span data-stu-id="88be5-124">Alternatively, you can manually create payment lines using the due date to calculate the posting date.</span></span> <span data-ttu-id="88be5-125">Une fois que vous avez appliqué les écritures comptables fournisseur, vous pouvez utiliser l'option **Calculer date comptabilisation** pour mettre à jour la date comptabilisation de la ligne feuille à la date d'échéance de la facture achat associée.</span><span class="sxs-lookup"><span data-stu-id="88be5-125">After you apply vendor ledger entries, you can use the **Calculate Posting Date** action to update the posting date on the journal line with the due date of the related purchase invoice.</span></span> <span data-ttu-id="88be5-126">Pour plus d'informations, reportez-vous à [Procédure : Lettrer les achats manuellement](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="88be5-126">For more information, see [How to: Apply Purchase Transactions Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="88be5-127">Si la facture achat est en retard, la date comptabilisation est définie sur la date de travail et la police de la ligne devient rouge.</span><span class="sxs-lookup"><span data-stu-id="88be5-127">If the purchase invoice is overdue, the posting date is set to the work date, and the font on the line becomes red.</span></span>  

## <a name="see-also"></a><span data-ttu-id="88be5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88be5-128">See Also</span></span>
[<span data-ttu-id="88be5-129">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="88be5-129">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="88be5-130">Exécuter des paiements</span><span class="sxs-lookup"><span data-stu-id="88be5-130">Make Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="88be5-131">Utilisation de feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="88be5-131">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="88be5-132">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="88be5-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

