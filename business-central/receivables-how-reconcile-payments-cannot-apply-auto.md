---
title: Utilisation de la fonction Transférer la différence vers un compte pour rapprocher les paiements | Microsoft Docs'
description: Décrit comment traiter les paiements qui ne peuvent pas être lettrés dans un document, par exemple lorsqu'un taux de change entraîne un changement de montants.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 03/05/2019
ms.author: sgroespe
ms.openlocfilehash: 7d952f46d5e688fe1b86077723a0482c91995661
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821275"
---
# <a name="reconcile-payments-that-cannot-be-applied-automatically"></a><span data-ttu-id="72d27-103">Rapprocher les paiements qui ne peuvent pas être lettrés automatiquement</span><span class="sxs-lookup"><span data-stu-id="72d27-103">Reconcile Payments that Cannot be Applied Automatically</span></span>
<span data-ttu-id="72d27-104">Vous serez parfois amené à gérer des paiements sur votre compte bancaire, qui ne peuvent pas être lettrés à un client, un fournisseur ou une écriture comptable compte bancaire ouvertes associées.</span><span class="sxs-lookup"><span data-stu-id="72d27-104">You may sometimes have to handle payments to your bank account that cannot be applied to a related open customer, vendor or bank account ledger entry.</span></span> <span data-ttu-id="72d27-105">Les motifs peuvent être qu'il n'existe dans [!INCLUDE[d365fin](includes/d365fin_md.md)] aucun document auquel le paiement puisse être lettré, ou que le document associé dans [!INCLUDE[d365fin](includes/d365fin_md.md)] affiche un montant différent du montant de la transaction, par exemple, en raison du taux de change.</span><span class="sxs-lookup"><span data-stu-id="72d27-105">Reasons may be that no document exists in [!INCLUDE[d365fin](includes/d365fin_md.md)] that the payment can be applied to, or the related document in [!INCLUDE[d365fin](includes/d365fin_md.md)] has a different amount than the transaction amount, for example, because of currency exchange.</span></span> <span data-ttu-id="72d27-106">Sur la page **Feuille rapprochement bancaire**, tous les montants de transaction pour les paiements qui n'ont pas encore été lettrés s'affichent dans le champ **Différence**, y compris les montants qui ne peuvent pas être lettrés pour des motifs tels que celui qui précède.</span><span class="sxs-lookup"><span data-stu-id="72d27-106">On the **Payment Reconciliation Journal** page, all transaction amounts for payments that are not yet applied appear in the **Difference** field, including amounts that cannot be applied because of reasons such as the above.</span></span>

<span data-ttu-id="72d27-107">Les paiements qui ne peuvent pas être lettrés peuvent apparaître sur les lignes feuille rapprochement bancaire pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="72d27-107">Payments that cannot be applied can appear on payment reconciliation journal lines in the following different ways:</span></span>

* <span data-ttu-id="72d27-108">La valeur du champ **Différence** est égale à celle du champ **Montant transaction**, ce qui indique qu'aucune partie du paiement ne peut être lettrée à une écriture comptable client, fournisseur ou compte bancaire ouverte associée.</span><span class="sxs-lookup"><span data-stu-id="72d27-108">The value in the **Difference** field is equal to the value in the **Transaction Amount** field, which indicates that no part of the payment can be applied to a related open customer, vendor, or bank account ledger entry.</span></span>
* <span data-ttu-id="72d27-109">La valeur du champ **Différence** est inférieure à celle du champ **Montant transaction**, ce qui indique qu'une partie du paiement peut être lettrée à une écriture comptable client, fournisseur ou compte bancaire ouverte associée.</span><span class="sxs-lookup"><span data-stu-id="72d27-109">The value in the **Difference** field is lower than the value in the **Transaction Amount** field, which indicates that a part of the payment can be applied to a related open customer, vendor, or bank account ledger entry.</span></span> <span data-ttu-id="72d27-110">La partie restante du paiement ne peut pas être lettrée et doit être rapprochée manuellement ou en la validant directement sur un compte.</span><span class="sxs-lookup"><span data-stu-id="72d27-110">The remaining part of the payment cannot be applied and must be reconciled manually or by posting it directly to an account.</span></span>

<span data-ttu-id="72d27-111">Pour rapprocher de tels paiements, vous pouvez cliquer sur le bouton **Transférer la différence vers un compte**, puis spécifier sur quel compte le montant du champ **Différence** sera validé lorsque vous validez la feuille rapprochement bancaire.</span><span class="sxs-lookup"><span data-stu-id="72d27-111">To reconcile such payments, you can choose the **Transfer Difference to Account** button and then specify to which account the amount in the **Difference** field will be posted when you post the payment reconciliation journal.</span></span>

> [!TIP]  
>   <span data-ttu-id="72d27-112">Il existe une fonctionnalité similaire permettant de configurer le rapprochement automatique des paiements récurrents qui ne peuvent pas être lettrés aux écritures comptables client, fournisseur ou compte bancaire ouvertes associées.</span><span class="sxs-lookup"><span data-stu-id="72d27-112">Similar functionality exists to set up automatic reconciliation of recurring payments that cannot be applied to related open customer, vendor, or bank account ledger entries.</span></span> <span data-ttu-id="72d27-113">Pour plus d'informations, reportez-vous à [Mapper du texte sur les paiements récurrents aux comptes pour un rapprochement automatique](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).</span><span class="sxs-lookup"><span data-stu-id="72d27-113">For more information, see [Map Text on Recurring Payments to Accounts for Automatic Reconciliation](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).</span></span>

## <a name="to-reconcile-payments-that-cannot-be-applied-automatically"></a><span data-ttu-id="72d27-114">Pour rapprocher les paiements qui ne peuvent pas être lettrés automatiquement</span><span class="sxs-lookup"><span data-stu-id="72d27-114">To reconcile payments that cannot be applied automatically</span></span>
1. <span data-ttu-id="72d27-115">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles rapprochement bancaire**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="72d27-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Reconciliation Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="72d27-116">Ouvrez une feuille de rapprochement de paiement.</span><span class="sxs-lookup"><span data-stu-id="72d27-116">Open a payment reconciliation journal.</span></span> <span data-ttu-id="72d27-117">Pour plus d'informations, voir [Rapprocher les paiements à l'aide du lettrage automatique](receivables-how-reconcile-payments-auto-application.md).</span><span class="sxs-lookup"><span data-stu-id="72d27-117">For more information, see [Reconcile Payments Using Automatic Application](receivables-how-reconcile-payments-auto-application.md).</span></span>
3. <span data-ttu-id="72d27-118">Sélectionnez l'action **Transférer la différence vers un compte**.</span><span class="sxs-lookup"><span data-stu-id="72d27-118">Choose the **Transfer Difference to Account**.</span></span> <span data-ttu-id="72d27-119">La page **Transférer la différence vers un compte** s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="72d27-119">The **Transfer Difference to Account** page opens.</span></span>
4. <span data-ttu-id="72d27-120">Dans le champ **Type compte**, spécifiez le type de compte sur lequel le montant du paiement sera validé.</span><span class="sxs-lookup"><span data-stu-id="72d27-120">In the **Account Type** field, specify if the type of account that the payment amount will be posted to.</span></span>
5. <span data-ttu-id="72d27-121">Dans le champ **N° compte**, spécifiez le compte sur lequel le montant du paiement sera validé.</span><span class="sxs-lookup"><span data-stu-id="72d27-121">In the **Account No.** field, specify the account that the payment amount will be posted to.</span></span>
6. <span data-ttu-id="72d27-122">Dans le champ **Description**, spécifiez le texte qui décrit cette validation de prélèvement.</span><span class="sxs-lookup"><span data-stu-id="72d27-122">In the **Description** field, specify text that describes this direct payment posting.</span></span> <span data-ttu-id="72d27-123">Par défaut, le texte du champ **Texte transaction** de la ligne feuille rapprochement bancaire est inséré.</span><span class="sxs-lookup"><span data-stu-id="72d27-123">By default, the text in the **Transaction Text** field on the payment reconciliation journal line is inserted.</span></span>
7. <span data-ttu-id="72d27-124">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="72d27-124">Choose the **OK** button.</span></span>

<span data-ttu-id="72d27-125">Si la valeur du champ **Différence** est égale à la valeur du champ **Montant transaction** lorsque vous validez la feuille rapprochement bancaire, l'intégralité du paiement sur la ligne feuille sera validé directement dans le compte contrepartie spécifié.</span><span class="sxs-lookup"><span data-stu-id="72d27-125">If the value in the **Difference** field was equal to the value in the **Transaction Amount** field when you post the payment reconciliation journal, the whole payment on the journal line will be posted directly to the specified balancing account.</span></span>

<span data-ttu-id="72d27-126">Si la valeur du champ **Différence** était inférieure à la valeur du champ **Montant transaction**, une ligne feuille supplémentaire est créée avec le même texte et la même date et avec la différence insérée dans le champ **Montant transaction**.</span><span class="sxs-lookup"><span data-stu-id="72d27-126">If the value in the **Difference** field was lower than the value in the **Transaction Amount** field, then an additional journal line will be created with the same text and date and with the difference inserted in the **Transaction Amount** field.</span></span> <span data-ttu-id="72d27-127">Sur la ligne feuille d'origine, la différence est déduite de la valeur du champ **Montant transaction**, et le paiement demeure lettré à son écriture comptable client, fournisseur ou compte bancaire associée.</span><span class="sxs-lookup"><span data-stu-id="72d27-127">On the original journal line, the difference will be deducted from the value in the **Transaction Amount** field, and the payment will remain applied to its related customer, vendor, or bank account ledger entry.</span></span> <span data-ttu-id="72d27-128">Lorsque vous validez la feuille rapprochement bancaire, une partie du paiement est validée en tant que paiement lettré.</span><span class="sxs-lookup"><span data-stu-id="72d27-128">When you post the payment reconciliation journal, one part of the payment will be posted as an applied payment.</span></span> <span data-ttu-id="72d27-129">L'autre partie du paiement est validée directement dans le compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="72d27-129">The other part of the payment will be posted directly to the specified account.</span></span>

## <a name="see-also"></a><span data-ttu-id="72d27-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72d27-130">See Also</span></span>
[<span data-ttu-id="72d27-131">Gestion des comptes client</span><span class="sxs-lookup"><span data-stu-id="72d27-131">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="72d27-132">Ventes</span><span class="sxs-lookup"><span data-stu-id="72d27-132">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="72d27-133">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="72d27-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>