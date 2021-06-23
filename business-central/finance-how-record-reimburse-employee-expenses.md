---
title: Enregistrer et rembourser les frais personnels des salariés pour les activités commerciales
description: Validez les dépenses des employés avec la feuille comptabilité sur le compte de l’employé et validez par la suite un paiement sur le compte bancaire de l’employé pour rembourser les frais liés à l’entreprise.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dd4ce755e3414f19ae501c1d437f3e1d78d565a1
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184414"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="1e9d4-103">Enregistrer et rembourser les frais des employés</span><span class="sxs-lookup"><span data-stu-id="1e9d4-103">Record and Reimburse Employees' Expenses</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="1e9d4-104">prend en charge les transactions des employés de la même manière que pour les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-104">supports transactions for employees in a similar way as for vendors.</span></span> <span data-ttu-id="1e9d4-105">Par conséquent, les groupes comptabilisation des salariés existent pour s’assurer que les écritures comptables d’un salarié sont validées dans les comptes appropriés de la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="1e9d4-106">Les transactions des employés ne peuvent être validées que dans la devise société.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="1e9d4-107">Les paiements de remboursement aux employés ne prennent pas en charge les remises et les écarts de règlement.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="1e9d4-108">Si les salariés dépensent leur propre argent pendant les activités commerciales, vous pouvez valider les frais sur le compte du salarié.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="1e9d4-109">Vous pouvez ensuite rembourser le salarié en faisant un paiement sur le compte bancaire du salarié, de la même façon que vous payez des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>  

> [!TIP]
> <span data-ttu-id="1e9d4-110">Cet article explique comment enregistrer les frais dans les livres et comment rembourser l’employé.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-110">This article explains how to record the expense in the books and how to reimburse the employee.</span></span> <span data-ttu-id="1e9d4-111">Votre organisation peut avoir un portail ou une application où les employés peuvent soumettre leurs notes de frais.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-111">Your organization may have a portal or app where employees can submit their expense reports.</span></span>

<span data-ttu-id="1e9d4-112">[!INCLUDE [prod_short](includes/prod_short.md)] est suffisamment flexible pour s’adapter à de nombreuses pratiques différentes.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-112">[!INCLUDE [prod_short](includes/prod_short.md)] is flexible enough to suit many different practices.</span></span> <span data-ttu-id="1e9d4-113">Les numéros de compte exacts à utiliser dépendent de la configuration et des processus de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-113">The exact account numbers to use depends on your organization's configuration and processes.</span></span>  

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="1e9d4-114">Pour enregistrer les frais des salariés</span><span class="sxs-lookup"><span data-stu-id="1e9d4-114">To record an employee's expense</span></span>

<span data-ttu-id="1e9d4-115">Validez les frais salarié sur la page **Feuille comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-115">You post employees' expenses on the **General Journal** page.</span></span>

1. <span data-ttu-id="1e9d4-116">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles comptabilité**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1e9d4-117">Ouvrez la feuille comptabilité appropriée.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-117">Open the relevant general journal batch.</span></span> <span data-ttu-id="1e9d4-118">Pour plus d’informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="1e9d4-118">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="1e9d4-119">Sur une nouvelle ligne feuille, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-119">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="1e9d4-120">Répétez l’étape 3 pour tous les frais que le salarié a supportés.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-120">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="1e9d4-121">Si vous souhaitez saisir les lignes de dépenses au-dessus d’une ligne compte contrepartie du compte bancaire de l’employé, activez la case à cocher **Suggérer le montant contrepartie** de la ligne pour votre lot sur la page **Noms feuilles comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-121">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="1e9d4-122">Puis le champ **Montant** de la ligne compte contrepartie est automatiquement prérempli avec la valeur requise pour équilibrer les dépenses.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-122">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="1e9d4-123">Choisissez l’action **Valider** pour enregistrer les frais sur le compte du salarié.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-123">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="1e9d4-124">Pour rembourser un employé</span><span class="sxs-lookup"><span data-stu-id="1e9d4-124">To reimburse an employee</span></span>

<span data-ttu-id="1e9d4-125">Vous remboursez des salariés en validant les paiements sur leur compte bancaire sur la page **Feuille paiement**.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-125">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>  

1. <span data-ttu-id="1e9d4-126">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles paiement**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="1e9d4-127">Ouvrez la feuille comptabilité paiement appropriée.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-127">Open the relevant payment journal batch.</span></span> <span data-ttu-id="1e9d4-128">Pour plus d’informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="1e9d4-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="1e9d4-129">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-129">Fill in the fields as necessary.</span></span> <span data-ttu-id="1e9d4-130">Pour plus d’informations, reportez-vous à [Effectuer des paiements](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="1e9d4-130">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="1e9d4-131">Sinon, choisissez l’action **Proposer paiements aux salariés** pour insérer automatiquement des lignes feuille pour les remboursements salarié en attente.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-131">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="1e9d4-132">Sélectionnez l’action **Valider** pour enregistrer le remboursement.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-132">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="1e9d4-133">Pour rapprocher les remboursements avec les écritures comptables du salarié</span><span class="sxs-lookup"><span data-stu-id="1e9d4-133">To reconcile reimbursements with employee ledger entries</span></span>

<span data-ttu-id="1e9d4-134">Appliquez les paiements des employés à leurs écritures comptables salariés ouvertes de la même façon que vous le faites pour les paiements des fournisseurs, par exemple sur la page **Feuille rapprochement bancaire**, en fonction des écritures de relevé bancaire connexes.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-134">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="1e9d4-135">Pour plus d’informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="1e9d4-135">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="1e9d4-136">Sinon, vous pouvez effectuer une application manuelle sur la page **Écritures comptables salariés**.</span><span class="sxs-lookup"><span data-stu-id="1e9d4-136">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="1e9d4-137">Pou plus d’informations, voir [Rapprocher des paiements fournisseur avec la feuille paiement ou à partir des écritures comptables fournisseur](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="1e9d4-137">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="1e9d4-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e9d4-138">See Also</span></span>

[<span data-ttu-id="1e9d4-139">Valider les transactions directement vers la comptabilité</span><span class="sxs-lookup"><span data-stu-id="1e9d4-139">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="1e9d4-140">Utilisation de feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="1e9d4-140">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="1e9d4-141">Contrepasser une validation feuille et annuler les réceptions/envois</span><span class="sxs-lookup"><span data-stu-id="1e9d4-141">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="1e9d4-142">Finances</span><span class="sxs-lookup"><span data-stu-id="1e9d4-142">Finance</span></span>](finance.md)  
<span data-ttu-id="1e9d4-143">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1e9d4-143">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]