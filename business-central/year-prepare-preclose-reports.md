---
title: "Aperçu des états préalables à la clôture pour vérifier la précision de compte | Microsoft Docs"
description: "Fournit un aperçu des états qui vous permettent de vérifier la précision des comptes avant de clôturer les livres à la fin d'un exercice ou d'une période."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 17b01bdec7f5b785b22ad7c295e1c1c3002a4b70
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="using-pre-closing-reports"></a><span data-ttu-id="c2d6c-103">Utilisation d'états préalables à la clôture</span><span class="sxs-lookup"><span data-stu-id="c2d6c-103">Using Pre-Closing Reports</span></span>
<span data-ttu-id="c2d6c-104">Il existe de nombreux états standard qui vous permettent de vérifier la précision des comptes avant de clôturer les livres à la fin d'un exercice ou d'une période.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-104">There are many standard reports that you can use to verify the accuracy of the accounts before closing the books at the end of a year or period.</span></span> <span data-ttu-id="c2d6c-105">Par exemple, vous pouvez utiliser l'état **Clients : Balance** pour vérifier que le solde d'un groupe comptabilisation client est égal au solde du compte général correspondant à une date donnée.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-105">For example, you can use the **Customer - Trial Balance** report to verify that the balance for a customer posting group is equal to the balance on the corresponding general ledger account on a certain date.</span></span>

<span data-ttu-id="c2d6c-106">Le tableau suivant décrit un certain nombre d'états qui peuvent être utiles dans ce processus.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-106">The following table describes a number of reports that may be useful in this process.</span></span>

| <span data-ttu-id="c2d6c-107">Pour</span><span class="sxs-lookup"><span data-stu-id="c2d6c-107">To</span></span> | <span data-ttu-id="c2d6c-108">Afficher ce rapport</span><span class="sxs-lookup"><span data-stu-id="c2d6c-108">See this report</span></span> |
| --- | --- |
| <span data-ttu-id="c2d6c-109">Imprimer un état Balance détaillé pour un ou plusieurs comptes bancaires avec des informations supplémentaires sur des écritures individuelles.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-109">Print a detailed trial balance report for one or more bank accounts with additional information about individual entries.</span></span> |<span data-ttu-id="c2d6c-110">Banque : Grand livre</span><span class="sxs-lookup"><span data-stu-id="c2d6c-110">Bank Acc. - Detail Trial Bal.</span></span> |
| <span data-ttu-id="c2d6c-111">Imprimer un Grand livre pour les clients sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-111">Print a detail trial balance for selected customers.</span></span> |<span data-ttu-id="c2d6c-112">Clients : Balance</span><span class="sxs-lookup"><span data-stu-id="c2d6c-112">Customer - Trial Balance</span></span> |
| <span data-ttu-id="c2d6c-113">Imprimer un Grand livre avec des informations détaillées sur des écritures individuelles pour les clients sélectionnés et durant une période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-113">Print a detail trial balance with detailed information about individual entries, for selected customers during a selected period.</span></span> |<span data-ttu-id="c2d6c-114">Clients : Grand livre client</span><span class="sxs-lookup"><span data-stu-id="c2d6c-114">Customer - Detail Trial Bal.</span></span> |
| <span data-ttu-id="c2d6c-115">Imprimer un Grand livre pour les fournisseurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-115">Print a detail trial balance for selected vendors.</span></span> |<span data-ttu-id="c2d6c-116">Fourn. : Balance</span><span class="sxs-lookup"><span data-stu-id="c2d6c-116">Vendor - Trial Balance</span></span> |
| <span data-ttu-id="c2d6c-117">Imprimer un Grand livre avec des informations détaillées sur des écritures individuelles pour les fournisseurs sélectionnés et durant une période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-117">Print a detail trial balance with detailed information about individual entries, for selected vendors during a selected period.</span></span> |<span data-ttu-id="c2d6c-118">Fourn. : Grand livre fourn.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-118">Vendor - Detail Trial Balance</span></span> |
| <span data-ttu-id="c2d6c-119">Imprimer une balance avec les chiffres de l'exercice en cours et de l'exercice précédent.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-119">Print a trial balance with the current year's and the previous year's figures.</span></span> |<span data-ttu-id="c2d6c-120">Balance de clôture</span><span class="sxs-lookup"><span data-stu-id="c2d6c-120">Closing Trial Balance</span></span> |
| <span data-ttu-id="c2d6c-121">Imprimer un état Grand livre pour les soldes des comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-121">Print a detailed trial balance report for general ledger account balances.</span></span> |<span data-ttu-id="c2d6c-122">Grand livre</span><span class="sxs-lookup"><span data-stu-id="c2d6c-122">Detail Trial Balance</span></span> |
| <span data-ttu-id="c2d6c-123">Imprimer un état Balance comprenant les soldes et les soldes période pour les comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-123">Print a trial balance report with balances and net changes for general ledger accounts.</span></span> |<span data-ttu-id="c2d6c-124">Balance</span><span class="sxs-lookup"><span data-stu-id="c2d6c-124">Trial Balance</span></span> |
| <span data-ttu-id="c2d6c-125">Imprimer une balance pour une société consolidée.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-125">Print a trial balance for a consolidated company.</span></span> |<span data-ttu-id="c2d6c-126">Balance consolidée</span><span class="sxs-lookup"><span data-stu-id="c2d6c-126">Consolidated Trial Balance</span></span> |

<span data-ttu-id="c2d6c-127">Pour afficher un état, sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez le nom tel qu'il s'affiche dans la table, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="c2d6c-127">To see a report, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, type the name as it appears in the table, and then choose the related link.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2d6c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2d6c-128">See Also</span></span>
[<span data-ttu-id="c2d6c-129">Clôture des exercices et des périodes</span><span class="sxs-lookup"><span data-stu-id="c2d6c-129">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="c2d6c-130">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c2d6c-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


