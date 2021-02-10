---
title: Lettrer des écritures dans des devises différentes| Microsoft Docs
description: Vous pouvez lettrer des écritures comptables dans différentes devises si vous effectuez une vente à un client dans une devise et recevez le règlement dans une autre devise.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 564ac8edfb21573e310a3be3eaa22060d84bef22
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750920"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="f6874-103">Activer le lettrage d’écritures comptables client en devises différentes</span><span class="sxs-lookup"><span data-stu-id="f6874-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="f6874-104">Si vous achetez des produits auprès d’un fournisseur dans une devise et que vous payez ces produits dans une autre devise, vous pouvez lettrer le paiement avec l’achat.</span><span class="sxs-lookup"><span data-stu-id="f6874-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="f6874-105">De même, si vous effectuez une vente à un client dans une devise et recevez le règlement dans une autre devise, vous pouvez lettrer le règlement avec la facture vente.</span><span class="sxs-lookup"><span data-stu-id="f6874-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="f6874-106">La procédure suivante indique comment configurer cela pour les écritures comptables fournisseur sur la page **Paramètres achats**.</span><span class="sxs-lookup"><span data-stu-id="f6874-106">The following procedure describes how to set this up for vendor ledger entries on the **Purchases & Payables Setup** page.</span></span> <span data-ttu-id="f6874-107">La configuration est semblable à celle des écritures comptables client sur la page **Paramètres ventes**.</span><span class="sxs-lookup"><span data-stu-id="f6874-107">The setup is similar for customer ledger entries on the **Sales & Receivables Setup** page.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="f6874-108">Pour activer le lettrage d’écritures comptables fournisseur en devises différentes</span><span class="sxs-lookup"><span data-stu-id="f6874-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="f6874-109">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres achats**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f6874-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f6874-110">Dans le champ **Lettrage entre devises**, sélectionnez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="f6874-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="f6874-111">Option</span><span class="sxs-lookup"><span data-stu-id="f6874-111">Option</span></span> | <span data-ttu-id="f6874-112">Description</span><span class="sxs-lookup"><span data-stu-id="f6874-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="f6874-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="f6874-113">None</span></span> |<span data-ttu-id="f6874-114">Le lettrage entre devises n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="f6874-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="f6874-115">Devises U.M.E.</span><span class="sxs-lookup"><span data-stu-id="f6874-115">EMU</span></span> |<span data-ttu-id="f6874-116">Le lettrage entre devises UME est autorisé.</span><span class="sxs-lookup"><span data-stu-id="f6874-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="f6874-117">Tous</span><span class="sxs-lookup"><span data-stu-id="f6874-117">All</span></span> |<span data-ttu-id="f6874-118">Lettrage autorisé entre toutes les devises.</span><span class="sxs-lookup"><span data-stu-id="f6874-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="f6874-119">Pour configurer des comptes généraux afin d’autoriser les différences d’arrondi des devises</span><span class="sxs-lookup"><span data-stu-id="f6874-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="f6874-120">Si vous lettrez des écritures dans différentes devises, vous devez configurer les comptes généraux sur lesquels valider les différences d’arrondi.</span><span class="sxs-lookup"><span data-stu-id="f6874-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f6874-121">Vous devez configurer les comptes généraux avant de terminer la tâche.</span><span class="sxs-lookup"><span data-stu-id="f6874-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="f6874-122">Pour plus d’informations, voir [Description des écritures comptables et du plan comptable](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="f6874-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="f6874-123">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Groupes comptabilisation client**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f6874-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f6874-124">Dans les champs **Cpte arr. lettr. dev. débit** et **Cpte arr. lettr. dev. crédit**, saisissez les comptes généraux correspondants pour valider les différences d’arrondi.</span><span class="sxs-lookup"><span data-stu-id="f6874-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="f6874-125">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Groupes compta. fournisseur**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f6874-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="f6874-126">Dans les champs **Cpte arr. lettr. dev. débit** et **Cpte arr. lettr. dev. crédit**, saisissez les comptes généraux correspondants pour valider les différences d’arrondi.</span><span class="sxs-lookup"><span data-stu-id="f6874-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6874-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6874-127">See Also</span></span>
[<span data-ttu-id="f6874-128">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="f6874-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="f6874-129">Gestion des comptes client</span><span class="sxs-lookup"><span data-stu-id="f6874-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="f6874-130">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f6874-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
