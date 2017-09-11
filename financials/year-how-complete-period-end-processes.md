---
title: "Activités facultatives pour les périodes de clôture | Microsoft Docs"
description: "Cette rubrique décrit les processus et les activités facultatifs pour la clôture des périodes comptables dans Financials."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 678cebc065594ed0ed6fea897676f109ff2c1dce
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="9ae33-103">Aperçu des tâches de clôture des périodes comptables</span><span class="sxs-lookup"><span data-stu-id="9ae33-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9ae33-104"> ne vous oblige pas à clôturer les périodes. Toutefois, il existe de nombreuses activités de clôture de période (fin de mois) que vous pouvez effectuer.</span><span class="sxs-lookup"><span data-stu-id="9ae33-104"> does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="9ae33-105">Cette rubrique présente un aperçu des activités et des processus facultatifs pour les périodes de clôture.</span><span class="sxs-lookup"><span data-stu-id="9ae33-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="9ae33-106">Écritures comptables</span><span class="sxs-lookup"><span data-stu-id="9ae33-106">General Ledger</span></span>
* <span data-ttu-id="9ae33-107">Spécifiez des plages de date de validation à l'échelle du système.</span><span class="sxs-lookup"><span data-stu-id="9ae33-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="9ae33-108">Cela spécifie les dates entre lesquelles les validation sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="9ae33-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="9ae33-109">En fonction des besoins de votre activité, vous pouvez autoriser la validation au début du traitement de clôture d'exercice ou vers la fin.</span><span class="sxs-lookup"><span data-stu-id="9ae33-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="9ae33-110">Pour plus d'informations, reportez vous à [Procédure: spécifier des périodes de validation](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="9ae33-110">For more information, see [How to: Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="9ae33-111">Effectuez tous les ajustements comptables nécessaires.</span><span class="sxs-lookup"><span data-stu-id="9ae33-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="9ae33-112">Mettez à jour et validez les feuilles abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ae33-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="9ae33-113">Exécutez les tableaux d'analyse comme suit :</span><span class="sxs-lookup"><span data-stu-id="9ae33-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="9ae33-114">Ouvrez la fenêtre **Tableau d'analyse**, puis sélectionnez l'action **Imprimer**.</span><span class="sxs-lookup"><span data-stu-id="9ae33-114">Open the **Account Schedule** window, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="9ae33-115">Ventes</span><span class="sxs-lookup"><span data-stu-id="9ae33-115">Sales and Receivables</span></span>
* <span data-ttu-id="9ae33-116">Validez l'ensemble des commandes, factures, avoirs et retours vente.</span><span class="sxs-lookup"><span data-stu-id="9ae33-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="9ae33-117">Validez l'ensemble des feuilles règlement.</span><span class="sxs-lookup"><span data-stu-id="9ae33-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="9ae33-118">Mettez à jour et validez les feuilles abonnement associées aux ventes.</span><span class="sxs-lookup"><span data-stu-id="9ae33-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="9ae33-119">Rapprochez la comptabilité client de la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="9ae33-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="9ae33-120">Exécutez le traitement par lots **Supprimer cdes vente facturées**.</span><span class="sxs-lookup"><span data-stu-id="9ae33-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="9ae33-121">Achats</span><span class="sxs-lookup"><span data-stu-id="9ae33-121">Purchases and Payables</span></span>
* <span data-ttu-id="9ae33-122">Validez l'ensemble des commandes, factures, avoirs et retours achat.</span><span class="sxs-lookup"><span data-stu-id="9ae33-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="9ae33-123">Validez l'ensemble des feuilles paiement.</span><span class="sxs-lookup"><span data-stu-id="9ae33-123">Post all payment journals.</span></span>  
* <span data-ttu-id="9ae33-124">Mettez à jour et validez les feuilles abonnement associées aux achats.</span><span class="sxs-lookup"><span data-stu-id="9ae33-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="9ae33-125">Générez l'état **Comptabilité fournisseur âgée** et rapprochez la comptabilité fournisseur de la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="9ae33-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="9ae33-126">Exécutez le traitement par lots **Supprimer cdes achat facturées**.</span><span class="sxs-lookup"><span data-stu-id="9ae33-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<!-- ### Fixed Assets
* Post all maintenance costs have been posted through the fixed asset journals or invoices.
* Post adjustments.
* Post appreciation.
* Post depreciation.
* Update and post the recurring fixed asset journal.-->

<!--### Intercompany
* Process Intercompany Postings.-->

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="9ae33-127">Calculez et traitez la Sales Tax.</span><span class="sxs-lookup"><span data-stu-id="9ae33-127">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="9ae33-128">Renseignez les déclarations de TVA.</span><span class="sxs-lookup"><span data-stu-id="9ae33-128">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9ae33-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ae33-129">See Also</span></span>
[<span data-ttu-id="9ae33-130">Clôture des exercices et des périodes</span><span class="sxs-lookup"><span data-stu-id="9ae33-130">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="9ae33-131">Clôture plans</span><span class="sxs-lookup"><span data-stu-id="9ae33-131">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="9ae33-132">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9ae33-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

