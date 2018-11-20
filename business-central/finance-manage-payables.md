---
title: Gestion des comptes fournisseur| Microsoft Docs
description: "Aperçu de la manière de gérer les comptes fournisseurs, y compris les paiements fournisseur, les créditeurs, les dettes, et le solde dû."
services: project-madeira
documentationcenter: 
author: bholtorf
manager: edupont
editor: 
ms.service: dynamics365-business-central
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2018
ms.author: bholtorf
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: cd46393c8e629b1d959c62c001680c692ea3c51f
ms.contentlocale: fr-ch
ms.lasthandoff: 11/20/2018

---
# <a name="managing-payables"></a><span data-ttu-id="6a4de-103">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="6a4de-103">Managing Payables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="6a4de-104">dispose de ce dont vous avez besoin pour gérer efficacement les comptes fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="6a4de-104">has what you need to effectively manage accounts payable.</span></span>  

## <a name="payments"></a><span data-ttu-id="6a4de-105">Paiements</span><span class="sxs-lookup"><span data-stu-id="6a4de-105">Payments</span></span>
<span data-ttu-id="6a4de-106">Il est facile de classer les paiements par ordre de priorité, de prendre en compte les pénalités pour les paiements en retard et de gérer les escomptes pour les paiements anticipés.</span><span class="sxs-lookup"><span data-stu-id="6a4de-106">It's easy to prioritize payments, account for penalties for overdue payments, and handle discounts for early payments.</span></span>

<span data-ttu-id="6a4de-107">Vous pouvez enregistrer les paiements dans une feuille comptabilité, puis imprimer des chèques avant de valider la feuille de paiements.</span><span class="sxs-lookup"><span data-stu-id="6a4de-107">You can record payments in a general journal, and then print checks before posting the payment journal.</span></span>

<span data-ttu-id="6a4de-108">Vous pouvez appliquer des paiements pour clôturer les factures lorsque vous validez le paiement ou après sa validation.</span><span class="sxs-lookup"><span data-stu-id="6a4de-108">You can apply payments to close invoices when you post the payment, or after you post the payment.</span></span> <span data-ttu-id="6a4de-109">Le **Mode de lettrage** spécifié pour le fournisseur (sur la **Fiche fournisseur**) détermine si vous devez effectuer ce lettrage manuellement ou s'il est effectué automatiquement.</span><span class="sxs-lookup"><span data-stu-id="6a4de-109">The **Application Method** specified for the vendor (on the **Vendor Card**) determines whether you apply the payment manually, or automatically.</span></span> <span data-ttu-id="6a4de-110">Vous pouvez toujours lettrer des transactions manuellement.</span><span class="sxs-lookup"><span data-stu-id="6a4de-110">You can always apply transactions manually.</span></span> <span data-ttu-id="6a4de-111">Toutefois, si le mode de lettrage pour le fournisseur est **Au plus ancien** et que vous ne spécifiez pas avec quel document le paiement doit être appliqué, le paiement sera appliqué avec l'écriture ouverte la plus ancienne pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6a4de-111">However, if the application method for the vendor is **Apply to Oldest**, and you do not specify a document to apply the payment to, the payment is applied to the oldest open entry for the vendor.</span></span>

## <a name="suggest-vendor-payments"></a><span data-ttu-id="6a4de-112">Proposer paiements fournisseur</span><span class="sxs-lookup"><span data-stu-id="6a4de-112">Suggest Vendor Payments</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="6a4de-113">peut proposer différents paiements aux fournisseurs, tels que les paiements arrivant à échéance ou les paiements donnant lieu à un escompte.</span><span class="sxs-lookup"><span data-stu-id="6a4de-113">can suggest various payments to vendors, such as payments that will be due soon, or payments where a discount is available.</span></span> <span data-ttu-id="6a4de-114">La proposition de paiement peut tenir compte du montant que vous avez défini comme fonds disponibles pour le paiement, ainsi que de la possibilité d'escompte lors du paiement.</span><span class="sxs-lookup"><span data-stu-id="6a4de-114">The payment suggestion can consider an amount that you specify as available funds for payment, and eligibility for payment discounts.</span></span>

## <a name="issue-checks"></a><span data-ttu-id="6a4de-115">Émettre des chèques</span><span class="sxs-lookup"><span data-stu-id="6a4de-115">Issue Checks</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="6a4de-116">vous permet d'émettre des chèques aux fournisseurs manuellement et par voie électronique.</span><span class="sxs-lookup"><span data-stu-id="6a4de-116">lets you issue checks to vendors manually and electronically.</span></span> <span data-ttu-id="6a4de-117">Vous pouvez effectuer les deux dans la fenêtre **Feuilles paiement**, dans laquelle vous pouvez également annuler des chèques et afficher des écritures comptables chèque.</span><span class="sxs-lookup"><span data-stu-id="6a4de-117">You do both in the **Payment Journals** window, where you can also void checks and view check ledger entries.</span></span>

## <a name="export-payments-to-a-bank-file"></a><span data-ttu-id="6a4de-118">Exporter des paiements vers un fichier bancaire</span><span class="sxs-lookup"><span data-stu-id="6a4de-118">Export Payments to a Bank File</span></span>
<span data-ttu-id="6a4de-119">Lorsque vous êtes prêt à régler un fournisseur, dans la fenêtre **Feuille paiement**, vous pouvez exporter un fichier contenant les informations de paiement sur les lignes feuille.</span><span class="sxs-lookup"><span data-stu-id="6a4de-119">When you are ready to pay a vendor, from the **Payment Journal** window you can export a file with the payment information from the journal lines.</span></span> <span data-ttu-id="6a4de-120">Vous pouvez ensuite transférer le fichier à votre banque électronique afin qu'elle traite les transferts d'argent.</span><span class="sxs-lookup"><span data-stu-id="6a4de-120">You can then upload the file to your electronic bank to process the money transfers.</span></span>

<span data-ttu-id="6a4de-121">Si vous ne souhaitez pas valider une ligne feuille paiement pour un paiement exporté, par exemple parce que vous attendez la confirmation de la banque que la transaction a été traitée, vous pouvez simplement supprimer la ligne feuille.</span><span class="sxs-lookup"><span data-stu-id="6a4de-121">If you do not want to post a payment journal line for an exported payment, for example because you are waiting for the bank to confirm the transaction, just delete the journal line.</span></span> <span data-ttu-id="6a4de-122">Par la suite, lorsque vous créez une ligne feuille paiement pour payer le montant ouvert de la facture, le champ **Montant total exporté** affiche la quantité du montant ayant déjà été exportée.</span><span class="sxs-lookup"><span data-stu-id="6a4de-122">Later, when you create a payment journal line to pay the remaining amount on the invoice, the **Total Exported Amount** field shows how much of the payment amount has already been exported.</span></span> <span data-ttu-id="6a4de-123">En outre, vous pouvez rechercher des informations détaillées concernant le total exporté en cliquant sur le bouton **Écritures reg. virement**.</span><span class="sxs-lookup"><span data-stu-id="6a4de-123">Also, you can find detailed information about the exported total by choosing the **Credit Transfer Reg. Entries** button.</span></span>

<span data-ttu-id="6a4de-124">Si vous attendez que votre banque confirme le traitement des transactions pour valider les paiements, il existe deux méthodes d'éviter de réexporter par erreur les paiements pour les documents ouverts :</span><span class="sxs-lookup"><span data-stu-id="6a4de-124">If you wait to post payments until after your bank confirms that it has processed transactions, there are two ways to avoid accidentally re-exporting payments for open documents:</span></span>  

* <span data-ttu-id="6a4de-125">Dans une feuille paiement avec les lignes paiement proposées, vous pouvez trier soit la colonne **Exporté dans fichier paiement** soit la colonne **Montant total exporté**, puis supprimer les propositions de paiement pour les factures ouvertes pour lesquelles les paiements ont déjà été effectués et pour lesquelles vous ne souhaitez pas effectuer de paiements.</span><span class="sxs-lookup"><span data-stu-id="6a4de-125">In a payment journal with suggested payment lines, sort on either the **Exported to Payment File** or **Total Exported Amount** columns, and then delete payment suggestions for open invoices for which payments have already been made and you do not want to make payments for.</span></span>

    <span data-ttu-id="6a4de-126">**Remarque** : vous pouvez être amené à ajouter ces colonnes à la liste.</span><span class="sxs-lookup"><span data-stu-id="6a4de-126">**Note** You might have to add these columns to the list.</span></span> <span data-ttu-id="6a4de-127">Pour plus d'informations, voir [Personnalisation de votre espace de travail](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="6a4de-127">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  
* <span data-ttu-id="6a4de-128">Sinon, dans le traitement par lots **Proposer paiements fournisseur**, où vous spécifiez les paiements à insérer dans la feuille de paiement, vous pouvez spécifier de ne pas insérer de lignes feuille pour les paiements qui ont déjà été exportés en cochant la case **Ignorer les paiements exportés**.</span><span class="sxs-lookup"><span data-stu-id="6a4de-128">Alternatively, on the **Suggest Vendor Payments** batch job, where you specify the payments to include in the payment journal, you can specify not to insert journal lines for payments that have already been exported by choosing the **Skip Exported Payments** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a4de-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a4de-129">See Also</span></span>
[<span data-ttu-id="6a4de-130">Modes de règlement</span><span class="sxs-lookup"><span data-stu-id="6a4de-130">Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="6a4de-131">Finances</span><span class="sxs-lookup"><span data-stu-id="6a4de-131">Finance</span></span>](finance.md)  
<span data-ttu-id="6a4de-132">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6a4de-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

