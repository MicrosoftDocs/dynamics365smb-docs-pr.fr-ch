---
title: "Emettre, imprimer et annuler des chèques| Microsoft Docs"
description: "Décrit comment émettre des chèques à l'aide de la feuille paiement, imprimer des chèques, et annuler ou afficher les écritures comptables chèque dans Dynamics 365."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 85e5cd61571ec6e571a44e39f397bd370112dd5c
ms.contentlocale: fr-ch
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-work-with-checks"></a><span data-ttu-id="3c6a5-103">Procédure : utilisation des chèques</span><span class="sxs-lookup"><span data-stu-id="3c6a5-103">How to: Work With Checks</span></span>
<span data-ttu-id="3c6a5-104">Vous pouvez émettre des chèques par voie électronique et manuelle dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3c6a5-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3c6a5-105">Ces deux méthodes utilisent la feuille paiement pour émettre des chèques aux fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="3c6a5-106">Vous pouvez également annuler des chèques et afficher les écritures comptables chèque.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="3c6a5-107">La procédure d'émission de chèques propose des paiements, crée des écritures comptables et imprime les chèques informatiques.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-107">The process of issuing checks suggests payments, creates ledger entries, and prints the computer checks.</span></span>

> [!NOTE]  
>   <span data-ttu-id="3c6a5-108">Pour s'assurer que la banque efface uniquement les chèques et les montants validés, vous pouvez envoyer un fichier contenant des informations de paiement, du chèque et du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-108">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="3c6a5-109">Pour plus d'informations, reportez-vous à [Procédure : exporter des fichiers Positive Pay](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="3c6a5-109">For more information, see [How to: Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="3c6a5-110">Votre imprimante doit être correctement configurée pour les formulaires chèque, et vous devez définir la mise en page de chèque à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-110">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="3c6a5-111">Pour plus d'informations, reportez-vous à [Procédure : définir les mises en page de chèques](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="3c6a5-111">For more information, see [How to: Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-issue-checks"></a><span data-ttu-id="3c6a5-112">Pour émettre des chèques</span><span class="sxs-lookup"><span data-stu-id="3c6a5-112">To issue checks</span></span>
1. <span data-ttu-id="3c6a5-113">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles paiement**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="3c6a5-114">Remplissez la feuille avec les paiements appropriés, par exemple à l'aide de la fonction Proposer paiements fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-114">Fill in the journal with relevant payments, for example by using the Suggest Vendor Payments function.</span></span> <span data-ttu-id="3c6a5-115">Pour plus d'informations, reportez vous à [Procédure : proposer des paiements fournisseur](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="3c6a5-115">For more information, see [How to: Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>
3. <span data-ttu-id="3c6a5-116">Dans le champ **Mode émission paiement** des lignes feuille pour le paiement que vous souhaitez effectuer avec des chèques, sélectionnez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="3c6a5-116">In the **Bank Payment Type** field on journal lines for payment that you want to make with checks, select one of the following options:</span></span>

   * <span data-ttu-id="3c6a5-117">**Informatique** : sélectionnez cette option si vous souhaitez imprimer un chèque du montant de la ligne feuille paiement.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-117">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="3c6a5-118">Vous devez imprimer les chèques avant de pouvoir valider les lignes feuille.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-118">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="3c6a5-119">Vous pouvez uniquement sélectionner **Informatique** si le **Type compte contrepartie** ou le **Type compte** est **Compte bancaire**.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-119">You can only select **Computer Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>
   * <span data-ttu-id="3c6a5-120">**Manuel** : sélectionnez cette option si vous avez créé un chèque manuellement et que vous souhaitez créer une écriture comptable chèque correspondante de ce montant.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-120">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="3c6a5-121">Si vous utilisez cette option, vous ne pouvez pas imprimer de chèque à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3c6a5-121">By using this option, you cannot print checks from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3c6a5-122">Vous pouvez uniquement sélectionner **Manuel** si le **Type compte contrepartie** ou le **Type compte** est **Compte bancaire**.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-122">You can only select **Manual Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>

     > [!NOTE]  
>   <span data-ttu-id="3c6a5-123">Vous devez imprimer les chèques informatiques avant de valider les lignes feuille correspondantes.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-123">You must print computer checks before you post the related journal lines.</span></span>
4. <span data-ttu-id="3c6a5-124">Dans le cas de chèques informatiques, sélectionnez **Imprimer chèque**.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-124">In case of computer checks, choose **Print Check**.</span></span>
5. <span data-ttu-id="3c6a5-125">Dans la fenêtre **Chèque**, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-125">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. <span data-ttu-id="3c6a5-126">Cliquez sur le bouton **Imprimer**.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-126">Choose the **Print** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="3c6a5-127">Si vous voulez imprimer des chèques en plusieurs devises sur des comptes bancaires différents, vous devez exécuter le traitement par lots **Imprimer chèque** pour chacune de ces devises et préciser le compte bancaire concerné.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-127">If you want to print checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="3c6a5-128">Pour annuler des chèques imprimés qui ne sont pas validés</span><span class="sxs-lookup"><span data-stu-id="3c6a5-128">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="3c6a5-129">Vous pouvez annuler des chèques non validés après leur impression par l'intermédiaire de l'action **Annuler chèque** de la fenêtre **Feuille paiement**.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-129">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="3c6a5-130">Dans la fenêtre **Feuille paiement**, sélectionnez **Annuler chèque**, puis sélectionnez les chèques à annuler.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-130">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="3c6a5-131">Pour annuler des chèques</span><span class="sxs-lookup"><span data-stu-id="3c6a5-131">To void checks</span></span>
<span data-ttu-id="3c6a5-132">Lorsque des paiements par chèque ont été validés, vous pouvez uniquement annuler des chèques à partir des écritures comptables banque ainsi obtenues.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-132">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="3c6a5-133">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="3c6a5-134">Sélectionnez le compte bancaire approprié, sélectionnez l'action **Modifier**, puis l'action **Écritures comptables chèque**.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-134">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="3c6a5-135">Dans la fenêtre **Écritures comptables chèque**, sélectionnez l'action **Annuler chèque**.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-135">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="3c6a5-136">Cochez la case **Annuler chèque uniquement**.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-136">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="3c6a5-137">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c6a5-137">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c6a5-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c6a5-138">See Also</span></span>
[<span data-ttu-id="3c6a5-139">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="3c6a5-139">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="3c6a5-140">Paramétrage des opérations bancaires</span><span class="sxs-lookup"><span data-stu-id="3c6a5-140">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="3c6a5-141">Procédure : exporter des fichiers Positive Pay</span><span class="sxs-lookup"><span data-stu-id="3c6a5-141">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="3c6a5-142">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3c6a5-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

