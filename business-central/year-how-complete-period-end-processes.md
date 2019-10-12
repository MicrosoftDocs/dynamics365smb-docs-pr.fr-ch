---
title: Activités facultatives pour les périodes de clôture | Microsoft Docs
description: Cette rubrique décrit les processus et les activités facultatifs pour la clôture des périodes comptables dans Business Central.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: 1912a3e1731c2a6a86c5fd5eb93c7e2bf2ff8a1b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313799"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="2ad8b-103">Aperçu des tâches de clôture des périodes comptables</span><span class="sxs-lookup"><span data-stu-id="2ad8b-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2ad8b-104">ne vous oblige pas à clôturer les périodes. Toutefois, il existe de nombreuses activités de clôture de période (fin de mois) que vous pouvez effectuer.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-104">does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="2ad8b-105">Cette rubrique présente un aperçu des activités et des processus facultatifs pour les périodes de clôture.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="2ad8b-106">Écritures comptables</span><span class="sxs-lookup"><span data-stu-id="2ad8b-106">General Ledger</span></span>
* <span data-ttu-id="2ad8b-107">Spécifiez des plages de date de validation à l'échelle du système.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="2ad8b-108">Cela spécifie les dates entre lesquelles les validation sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="2ad8b-109">En fonction des besoins de votre activité, vous pouvez autoriser la validation au début du traitement de clôture d'exercice ou vers la fin.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="2ad8b-110">Pour plus d'informations, reportez vous à [Spécifier des périodes de validation](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="2ad8b-110">For more information, see [Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="2ad8b-111">Effectuez tous les ajustements comptables nécessaires.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="2ad8b-112">Mettez à jour et validez les feuilles abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="2ad8b-113">Exécutez les tableaux d'analyse comme suit :</span><span class="sxs-lookup"><span data-stu-id="2ad8b-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="2ad8b-114">Ouvrez la page **Tableau d'analyse**, puis sélectionnez l'action **Imprimer**.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-114">Open the **Account Schedule** page, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="2ad8b-115">Ventes</span><span class="sxs-lookup"><span data-stu-id="2ad8b-115">Sales and Receivables</span></span>
* <span data-ttu-id="2ad8b-116">Validez l'ensemble des commandes, factures, avoirs et retours vente.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="2ad8b-117">Validez l'ensemble des feuilles règlement.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="2ad8b-118">Mettez à jour et validez les feuilles abonnement associées aux ventes.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="2ad8b-119">Rapprochez la comptabilité client de la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="2ad8b-120">Exécutez le traitement par lots **Supprimer cdes vente facturées**.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="2ad8b-121">Achats</span><span class="sxs-lookup"><span data-stu-id="2ad8b-121">Purchases and Payables</span></span>
* <span data-ttu-id="2ad8b-122">Validez l'ensemble des commandes, factures, avoirs et retours achat.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="2ad8b-123">Validez l'ensemble des feuilles paiement.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-123">Post all payment journals.</span></span>  
* <span data-ttu-id="2ad8b-124">Mettez à jour et validez les feuilles abonnement associées aux achats.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="2ad8b-125">Générez l'état **Comptabilité fournisseur âgée** et rapprochez la comptabilité fournisseur de la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="2ad8b-126">Exécutez le traitement par lots **Supprimer cdes achat facturées**.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<span data-ttu-id="2ad8b-127">COMPTES D'IMMOBILISATIONS</span><span class="sxs-lookup"><span data-stu-id="2ad8b-127">Fixed Assets</span></span>
* <span data-ttu-id="2ad8b-128">Validez que tous les frais de maintenance ont été validés via les feuilles immobilisation ou factures.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-128">Post all maintenance costs have been posted through the fixed asset journals or invoices.</span></span>
* <span data-ttu-id="2ad8b-129">Validez les ajustements.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-129">Post adjustments.</span></span>
* <span data-ttu-id="2ad8b-130">Validez l'appréciation.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-130">Post appreciation.</span></span>
* <span data-ttu-id="2ad8b-131">Validez l'amortissement.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-131">Post depreciation.</span></span>
* <span data-ttu-id="2ad8b-132">Mettez à jour et validez la feuille abonnement immobilisations.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-132">Update and post the recurring fixed asset journal.</span></span>

<span data-ttu-id="2ad8b-133">Intersociétés</span><span class="sxs-lookup"><span data-stu-id="2ad8b-133">Intercompany</span></span>
* <span data-ttu-id="2ad8b-134">Traitement des transactions intersociétés</span><span class="sxs-lookup"><span data-stu-id="2ad8b-134">Process Intercompany Transactions</span></span>

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="2ad8b-135">Calculez et traitez la Sales Tax.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-135">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="2ad8b-136">Renseignez les déclarations de TVA.</span><span class="sxs-lookup"><span data-stu-id="2ad8b-136">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2ad8b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ad8b-137">See Also</span></span>
[<span data-ttu-id="2ad8b-138">Clôture des exercices et des périodes</span><span class="sxs-lookup"><span data-stu-id="2ad8b-138">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="2ad8b-139">Clôture plans</span><span class="sxs-lookup"><span data-stu-id="2ad8b-139">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="2ad8b-140">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2ad8b-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
