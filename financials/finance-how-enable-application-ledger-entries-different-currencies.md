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
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6379aea58ab7943b117e5b19b22f71193290c2cb
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="8c31b-103">Procédure : activer le lettrage d'écritures comptables client en devises différentes</span><span class="sxs-lookup"><span data-stu-id="8c31b-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="8c31b-104">Si vous achetez des produits auprès d'un fournisseur dans une devise et que vous payez ces produits dans une autre devise, vous pouvez lettrer le paiement avec l'achat.</span><span class="sxs-lookup"><span data-stu-id="8c31b-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="8c31b-105">De même, si vous effectuez une vente à un client dans une devise et recevez le règlement dans une autre devise, vous pouvez lettrer le règlement avec la facture vente.</span><span class="sxs-lookup"><span data-stu-id="8c31b-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="8c31b-106">La procédure suivante indique comment configurer cela pour les écritures comptables fournisseur dans la fenêtre **Paramètres achats**.</span><span class="sxs-lookup"><span data-stu-id="8c31b-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="8c31b-107">La configuration est semblable à celle des écritures comptables client dans la fenêtre **Paramètres ventes**.</span><span class="sxs-lookup"><span data-stu-id="8c31b-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="8c31b-108">Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**.</span><span class="sxs-lookup"><span data-stu-id="8c31b-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="8c31b-109">Pour plus d'informations, voir [Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="8c31b-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="8c31b-110">Pour activer le lettrage d'écritures comptables fournisseur en devises différentes</span><span class="sxs-lookup"><span data-stu-id="8c31b-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="8c31b-111">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres achats**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="8c31b-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="8c31b-112">Dans le champ **Lettrage entre devises**, sélectionnez l'une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c31b-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="8c31b-113">Option</span><span class="sxs-lookup"><span data-stu-id="8c31b-113">Option</span></span> | <span data-ttu-id="8c31b-114">Description</span><span class="sxs-lookup"><span data-stu-id="8c31b-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="8c31b-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="8c31b-115">None</span></span> |<span data-ttu-id="8c31b-116">Le lettrage entre devises n'est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="8c31b-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="8c31b-117">Devises U.M.E.</span><span class="sxs-lookup"><span data-stu-id="8c31b-117">EMU</span></span> |<span data-ttu-id="8c31b-118">Le lettrage entre devises UME est autorisé.</span><span class="sxs-lookup"><span data-stu-id="8c31b-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="8c31b-119">Tous</span><span class="sxs-lookup"><span data-stu-id="8c31b-119">All</span></span> |<span data-ttu-id="8c31b-120">Lettrage autorisé entre toutes les devises.</span><span class="sxs-lookup"><span data-stu-id="8c31b-120">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="8c31b-121">Pour configurer des comptes généraux afin d'autoriser les différences d'arrondi des devises</span><span class="sxs-lookup"><span data-stu-id="8c31b-121">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="8c31b-122">Si vous lettrez des écritures dans différentes devises, vous devez configurer les comptes généraux sur lesquels valider les différences d'arrondi.</span><span class="sxs-lookup"><span data-stu-id="8c31b-122">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="8c31b-123">Vous devez configurer les comptes généraux avant de terminer la tâche.</span><span class="sxs-lookup"><span data-stu-id="8c31b-123">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="8c31b-124">Pour plus d'informations, voir [Description des écritures comptables et du plan comptable](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="8c31b-124">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span> 
  
1. <span data-ttu-id="8c31b-125">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Groupes compta. client**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="8c31b-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8c31b-126">Dans les champs **Cpte arr. lettr. dev. débit** et **Cpte arr. lettr. dev. crédit**, saisissez les comptes généraux correspondants pour valider les différences d'arrondi.</span><span class="sxs-lookup"><span data-stu-id="8c31b-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="8c31b-127">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Groupes compta. fournisseur**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="8c31b-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="8c31b-128">Dans les champs **Cpte arr. lettr. dev. débit** et **Cpte arr. lettr. dev. crédit**, saisissez les comptes généraux correspondants pour valider les différences d'arrondi.</span><span class="sxs-lookup"><span data-stu-id="8c31b-128">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8c31b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c31b-129">See Also</span></span>
[<span data-ttu-id="8c31b-130">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="8c31b-130">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="8c31b-131">Gestion des comptes client</span><span class="sxs-lookup"><span data-stu-id="8c31b-131">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="8c31b-132">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8c31b-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

