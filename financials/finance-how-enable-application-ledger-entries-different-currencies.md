---
title: "Lettrer des écritures dans des devises différentes| Microsoft Docs"
description: "Vous pouvez lettrer des écritures comptables dans différentes devises si vous effectuez une vente à un client dans une devise et recevez le règlement dans une autre devise."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d98fdf358e387be1d53b188cc05c57108e8592b8
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="81446-103">Activer le lettrage d'écritures comptables client en devises différentes</span><span class="sxs-lookup"><span data-stu-id="81446-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="81446-104">Si vous achetez des produits auprès d'un fournisseur dans une devise et que vous payez ces produits dans une autre devise, vous pouvez lettrer le paiement avec l'achat.</span><span class="sxs-lookup"><span data-stu-id="81446-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="81446-105">De même, si vous effectuez une vente à un client dans une devise et recevez le règlement dans une autre devise, vous pouvez lettrer le règlement avec la facture vente.</span><span class="sxs-lookup"><span data-stu-id="81446-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="81446-106">La procédure suivante indique comment configurer cela pour les écritures comptables fournisseur dans la fenêtre **Paramètres achats**.</span><span class="sxs-lookup"><span data-stu-id="81446-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="81446-107">La configuration est semblable à celle des écritures comptables client dans la fenêtre **Paramètres ventes**.</span><span class="sxs-lookup"><span data-stu-id="81446-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="81446-108">Pour activer le lettrage d'écritures comptables fournisseur en devises différentes</span><span class="sxs-lookup"><span data-stu-id="81446-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="81446-109">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres achats**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="81446-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="81446-110">Dans le champ **Lettrage entre devises**, sélectionnez l'une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="81446-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="81446-111">Option</span><span class="sxs-lookup"><span data-stu-id="81446-111">Option</span></span> | <span data-ttu-id="81446-112">Description</span><span class="sxs-lookup"><span data-stu-id="81446-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="81446-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="81446-113">None</span></span> |<span data-ttu-id="81446-114">Le lettrage entre devises n'est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="81446-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="81446-115">Devises U.M.E.</span><span class="sxs-lookup"><span data-stu-id="81446-115">EMU</span></span> |<span data-ttu-id="81446-116">Le lettrage entre devises UME est autorisé.</span><span class="sxs-lookup"><span data-stu-id="81446-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="81446-117">Tous</span><span class="sxs-lookup"><span data-stu-id="81446-117">All</span></span> |<span data-ttu-id="81446-118">Lettrage autorisé entre toutes les devises.</span><span class="sxs-lookup"><span data-stu-id="81446-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="81446-119">Pour configurer des comptes généraux afin d'autoriser les différences d'arrondi des devises</span><span class="sxs-lookup"><span data-stu-id="81446-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="81446-120">Si vous lettrez des écritures dans différentes devises, vous devez configurer les comptes généraux sur lesquels valider les différences d'arrondi.</span><span class="sxs-lookup"><span data-stu-id="81446-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="81446-121">Vous devez configurer les comptes généraux avant de terminer la tâche.</span><span class="sxs-lookup"><span data-stu-id="81446-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="81446-122">Pour plus d'informations, voir [Description des écritures comptables et du plan comptable](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="81446-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="81446-123">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Groupes compta. client**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="81446-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="81446-124">Dans les champs **Cpte arr. lettr. dev. débit** et **Cpte arr. lettr. dev. crédit**, saisissez les comptes généraux correspondants pour valider les différences d'arrondi.</span><span class="sxs-lookup"><span data-stu-id="81446-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="81446-125">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Groupes compta. fournisseur**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="81446-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="81446-126">Dans les champs **Cpte arr. lettr. dev. débit** et **Cpte arr. lettr. dev. crédit**, saisissez les comptes généraux correspondants pour valider les différences d'arrondi.</span><span class="sxs-lookup"><span data-stu-id="81446-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="81446-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81446-127">See Also</span></span>
[<span data-ttu-id="81446-128">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="81446-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="81446-129">Gestion des comptes client</span><span class="sxs-lookup"><span data-stu-id="81446-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="81446-130">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="81446-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

