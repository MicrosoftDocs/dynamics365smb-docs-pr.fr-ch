---
title: "Clôturer un exercice comptable et des périodes comptables | Microsoft Docs"
description: "Décrit les tâches permettant de clôturer un exercice fiscal ou une période comptable, par exemple, en vérifiant que les documents et les feuilles sont validés et en vérifiant les soldes bancaires."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/07/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7b125edfcfd5e03882568b8ab6eb264418f15bef
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="closing-years-and-periods"></a><span data-ttu-id="4a91f-103">Clôture des exercices et des périodes</span><span class="sxs-lookup"><span data-stu-id="4a91f-103">Closing Years and Periods</span></span>
<span data-ttu-id="4a91f-104">À la fin d'un exercice comptable, vous devez exécuter un certain nombre de tâches administratives, par exemple vous assurer que tous les documents et les feuilles sont validés veillant, que les données de devise sont à jour, que les livres sont clôturés, et plus.</span><span class="sxs-lookup"><span data-stu-id="4a91f-104">At the end of a fiscal year, there are a number of administrative tasks that you have to perform, like making sure all documents and journals are posted, making sure currency data are up-to-date, closing the books, and more.</span></span> <span data-ttu-id="4a91f-105">Les tâches réelles dépendent de votre société.</span><span class="sxs-lookup"><span data-stu-id="4a91f-105">The actual tasks will depend your company.</span></span>

<span data-ttu-id="4a91f-106">Le tableau suivant fournit un aperçu des tâches que vous devez généralement exécuter pour clôturer un exercice et une période comptables.</span><span class="sxs-lookup"><span data-stu-id="4a91f-106">The following table provides an overview of tasks that you typically perform to close a year and period.</span></span>

| <span data-ttu-id="4a91f-107">À</span><span class="sxs-lookup"><span data-stu-id="4a91f-107">To</span></span> | <span data-ttu-id="4a91f-108">Voir</span><span class="sxs-lookup"><span data-stu-id="4a91f-108">See</span></span> |
| --- | --- |
| <span data-ttu-id="4a91f-109">Spécifier des plages de date de validation à l'échelle du système et spécifiques à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4a91f-109">Specify system-wide and user-specific posting date ranges.</span></span> <span data-ttu-id="4a91f-110">En fonction des besoins de votre activité, vous pouvez restreindre les plages de date validation utilisateur au début du traitement de clôture d'exercice ou après ce dernier.</span><span class="sxs-lookup"><span data-stu-id="4a91f-110">Depending on your business needs, you may want to restrict user posting date ranges at the start of the period-end process or after it.</span></span> |[<span data-ttu-id="4a91f-111">Définir des périodes de validation</span><span class="sxs-lookup"><span data-stu-id="4a91f-111">Specify Posting Periods</span></span>](finance-how-specify-posting-periods.md) |
| <span data-ttu-id="4a91f-112">Obtenir un aperçu des activités qui sont généralement effectuées à la fin d'une période, telles que la validation de tous les documents et toutes les feuilles, ou l'exécution de tableaux d'analyse.</span><span class="sxs-lookup"><span data-stu-id="4a91f-112">Get an overview of activities that are commonly performed at the end of a period, such as posting all documents and journals, or running account schedules.</span></span> |[<span data-ttu-id="4a91f-113">Clôture périodes</span><span class="sxs-lookup"><span data-stu-id="4a91f-113">Closing Periods</span></span>](year-how-complete-period-end-processes.md) |
| <span data-ttu-id="4a91f-114">Mettre à jour les taux de change devise des écritures client, fournisseur et compte bancaire validées.</span><span class="sxs-lookup"><span data-stu-id="4a91f-114">Update currency exchange rates and adjust the exchange rates of posted customer, vendor, and bank account entries.</span></span> |[<span data-ttu-id="4a91f-115">Mettre à jour des taux de change devise</span><span class="sxs-lookup"><span data-stu-id="4a91f-115">Update Currency Exchange Rates</span></span>](finance-how-update-currencies.md) |
| <span data-ttu-id="4a91f-116">Ventiler des coûts et des bénéfices dans des comptes et des axes.</span><span class="sxs-lookup"><span data-stu-id="4a91f-116">Allocate costs and income among accounts and dimensions.</span></span> |[<span data-ttu-id="4a91f-117">Répartition des coûts et du revenu</span><span class="sxs-lookup"><span data-stu-id="4a91f-117">Allocating Costs and Income</span></span>](year-allocate-costs-income.md) |
| <span data-ttu-id="4a91f-118">Préparer la déclaration des montants de taxe sur la valeur ajoutée que vous avez recueillis sur les ventes au site Web des autorités fiscales.</span><span class="sxs-lookup"><span data-stu-id="4a91f-118">Prepare to report value-added tax amounts that you have collected for sales to the tax authorities' web service.</span></span> |[<span data-ttu-id="4a91f-119">Procédure : Déclarer la TVA aux autorités fiscales</span><span class="sxs-lookup"><span data-stu-id="4a91f-119">How To: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="4a91f-120">Imprimer des états pour vérifier les soldes des comptes généraux, des comptes client, des comptes fournisseur et des comptes bancaires avant de clôturer une période.</span><span class="sxs-lookup"><span data-stu-id="4a91f-120">Print reports to verify general ledger, customer, vendor and bank account balances before closing a period.</span></span> |[<span data-ttu-id="4a91f-121">Préparation des états préalables à la clôture</span><span class="sxs-lookup"><span data-stu-id="4a91f-121">Preparing Pre-Closing Reports</span></span>](year-prepare-preclose-reports.md) |
| <span data-ttu-id="4a91f-122">Clôturer des périodes et l'exercice comptables, transférer des soldes de comptes de gestion dans des comptes de bilan et valider l'écriture de clôture d'exercice.</span><span class="sxs-lookup"><span data-stu-id="4a91f-122">Close accounting periods and fiscal year, transfer income statement balances to balance sheet accounts and post the year end closing entry.</span></span> |[<span data-ttu-id="4a91f-123">Clôture plans</span><span class="sxs-lookup"><span data-stu-id="4a91f-123">Closing Books</span></span>](year-close-books.md) |
| <span data-ttu-id="4a91f-124">Imprimer des états qui peuvent vous aider à créer des états financiers.</span><span class="sxs-lookup"><span data-stu-id="4a91f-124">Print reports that can assist you in creating financial statements.</span></span> |[<span data-ttu-id="4a91f-125">Préparation des états de clôture</span><span class="sxs-lookup"><span data-stu-id="4a91f-125">Preparing Closing Statements</span></span>](year-prepare-close-statement.md) |

## <a name="see-also"></a><span data-ttu-id="4a91f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a91f-126">See Also</span></span>
[<span data-ttu-id="4a91f-127">Ouvrir un nouvel exercice comptable</span><span class="sxs-lookup"><span data-stu-id="4a91f-127">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="4a91f-128">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4a91f-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

