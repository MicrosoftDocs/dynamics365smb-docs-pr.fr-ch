---
title: Aperçu des tâches permettant de gérer la comptabilité fournisseur| Microsoft Docs
description: Décrit les tâches permettant de gérer la comptabilité fournisseur, par exemple, le paiement des créditeurs ou le lettrage de paiements sortants dans la comptabilité pour clôturer des factures ou des avoirs.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 02/08/2019
ms.author: edupont
ms.openlocfilehash: 89678ee0055992a03d4f56ecedf15350f7ad348e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820305"
---
# <a name="managing-payables"></a><span data-ttu-id="37e06-103">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="37e06-103">Managing Payables</span></span>

<span data-ttu-id="37e06-104">Une grande partie de la gestion des comptes fournisseurs consiste à payer vos fournisseurs, ou à rembourse vos salariés de leurs dépenses.</span><span class="sxs-lookup"><span data-stu-id="37e06-104">A big part of managing accounts payable is paying your vendors, or reimbursing your employees for expenses.</span></span> <span data-ttu-id="37e06-105">Vous pouvez utiliser les fonctions pour ajouter des lignes de paiement pour les factures achat échues sur la page **Feuille paiement** .</span><span class="sxs-lookup"><span data-stu-id="37e06-105">You can use functions to add payments lines for purchase invoices that are due on the **Payment Journal** page.</span></span> <span data-ttu-id="37e06-106">Pour effectuer rapidement des transactions bancaires, vous pouvez exporter plusieurs lignes feuille paiement vers un fichier, puis télécharger ensuite ce fichier vers votre banque.</span><span class="sxs-lookup"><span data-stu-id="37e06-106">To send transactions to your bank, you can export multiple payment journal lines to a file, and then upload the file to your bank.</span></span> <span data-ttu-id="37e06-107">Vous pouvez également effectuer des paiements par chèque, notamment pour transmettre des chèques en tant que paiements électroniques.</span><span class="sxs-lookup"><span data-stu-id="37e06-107">You can also make payments by check, including transmitting checks as electronic payments.</span></span>

<span data-ttu-id="37e06-108">Une autre tâche courante consiste à lettrer les paiements sortants à leurs écritures comptables fournisseur ou salarié associées et de ce fait, clôturer les factures achat, les avoirs achat ou les comptes salariés comme payés.</span><span class="sxs-lookup"><span data-stu-id="37e06-108">Another typical task is to apply outgoing payments to their related vendor or employee ledger entries in order to close purchase invoices, purchase credit memos, or employee accounts as paid.</span></span> <span data-ttu-id="37e06-109">Vous pouvez effectuer cette tâche sur la page **Feuille rapprochement bancaire** en important un fichier de relevé bancaire pour enregistrer rapidement les paiements.</span><span class="sxs-lookup"><span data-stu-id="37e06-109">You can do this on the **Payment Reconciliation Journal** page by importing a bank statement file to register the payments.</span></span> <span data-ttu-id="37e06-110">Les paiements sont lettrés aux écritures client, fournisseur ou salarié ouvertes en faisant correspondre le texte de paiement et les informations d'écriture.</span><span class="sxs-lookup"><span data-stu-id="37e06-110">The payments are applied to open vendor, customer, or employee ledger entries by matching payment text and entry information.</span></span> <span data-ttu-id="37e06-111">Il existe plusieurs manières de vérifier et de modifier les correspondances avant de valider la feuille.</span><span class="sxs-lookup"><span data-stu-id="37e06-111">There are various ways to review and change the matches before you post the journal.</span></span> <span data-ttu-id="37e06-112">Vous pouvez choisir de clôturer les écritures comptables compte bancaire ouvertes associées aux écritures comptables lettrées lorsque vous validez la feuille.</span><span class="sxs-lookup"><span data-stu-id="37e06-112">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="37e06-113">Le compte bancaire est automatiquement rapproché lorsque tous les paiements sont lettrés.</span><span class="sxs-lookup"><span data-stu-id="37e06-113">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="37e06-114">Sinon, vous pouvez lettrer les paiements sortants manuellement sur la page **Feuille paiement** ou à partir des écritures comptables fournisseur ou salarié associées.</span><span class="sxs-lookup"><span data-stu-id="37e06-114">Alternatively, you can apply outgoing payments manually on the **Payment Journal** page or from the related vendor or employee ledger entries.</span></span>

<span data-ttu-id="37e06-115">Le tableau suivant décrit une série de tâches associées aux comptes fournisseur et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="37e06-115">The following table describes a sequence of tasks within accounts payable, with links to the topics that describe them.</span></span>

| <span data-ttu-id="37e06-116">Pour</span><span class="sxs-lookup"><span data-stu-id="37e06-116">To</span></span> | <span data-ttu-id="37e06-117">Voir</span><span class="sxs-lookup"><span data-stu-id="37e06-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="37e06-118">Générez les paiements fournisseurs ou les remboursements salariés dus, préparez les paiements par chèque, et exportez les paiements vers un fichier bancaire lors de la validation.</span><span class="sxs-lookup"><span data-stu-id="37e06-118">Generate due vendor payments or employee reimbursements, prepare check payments, and export payments to a bank file when posting.</span></span> |[<span data-ttu-id="37e06-119">Effectuer des paiements</span><span class="sxs-lookup"><span data-stu-id="37e06-119">Making Payments</span></span>](payables-make-payments.md) |
| <span data-ttu-id="37e06-120">Lettrer les paiements fournisseur automatiquement aux factures achat impayées en important un fichier de relevé bancaire.</span><span class="sxs-lookup"><span data-stu-id="37e06-120">Apply vendor payments automatically to unpaid purchase invoices by importing a bank statement file.</span></span> |[<span data-ttu-id="37e06-121">Lettrage automatique des paiements et rapprochement des comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="37e06-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="37e06-122">Lettrer les paiements fournisseur aux factures achat impayées manuellement.</span><span class="sxs-lookup"><span data-stu-id="37e06-122">Apply vendor payments to unpaid purchase invoices manually.</span></span> |[<span data-ttu-id="37e06-123">Rapprocher des paiements fournisseur avec la feuille paiement ou à partir des écritures comptables fournisseur</span><span class="sxs-lookup"><span data-stu-id="37e06-123">Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries</span></span>](payables-how-apply-purchase-transactions-manually.md) |
|<span data-ttu-id="37e06-124">Pour une évaluation de stock correcte, affectez les coûts articles ajoutés, tels que le fret, la manutention, les assurances, et transport, que vous encourez lorsque vous achetez.</span><span class="sxs-lookup"><span data-stu-id="37e06-124">Ensure correct inventory valuation by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing.</span></span>|[<span data-ttu-id="37e06-125">Utiliser Frais annexes pour comptabiliser les coûts commerciaux supplémentaires</span><span class="sxs-lookup"><span data-stu-id="37e06-125">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|
|<span data-ttu-id="37e06-126">Remboursez les frais personnels des salariés pour les activités liées à l'entreprise en effectuant le paiement sur leur compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="37e06-126">Reimburse employees for personal expenses during business activities by making payment to their bank account.</span></span>|[<span data-ttu-id="37e06-127">Enregistrer et rembourser les frais des employés</span><span class="sxs-lookup"><span data-stu-id="37e06-127">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)|

## <a name="see-also"></a><span data-ttu-id="37e06-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37e06-128">See Also</span></span>
[<span data-ttu-id="37e06-129">Achats</span><span class="sxs-lookup"><span data-stu-id="37e06-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="37e06-130">Gestion des comptes client</span><span class="sxs-lookup"><span data-stu-id="37e06-130">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="37e06-131">Utiliser Frais annexes pour comptabiliser les coûts commerciaux supplémentaires</span><span class="sxs-lookup"><span data-stu-id="37e06-131">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)  
[<span data-ttu-id="37e06-132">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="37e06-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="37e06-133">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="37e06-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  