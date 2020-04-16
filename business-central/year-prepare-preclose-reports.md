---
title: Aperçu des états préalables à la clôture pour vérifier la précision de compte | Microsoft Docs
description: Fournit un aperçu des états qui vous permettent de vérifier la précision des comptes avant de clôturer les livres à la fin d'un exercice ou d'une période.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: b45fe3d89502e5a4e42bc43cc4679afe1b13699d
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191706"
---
# <a name="using-pre-closing-reports"></a><span data-ttu-id="e2d1f-103">Utilisation d'états préalables à la clôture</span><span class="sxs-lookup"><span data-stu-id="e2d1f-103">Using Pre-Closing Reports</span></span>
<span data-ttu-id="e2d1f-104">Il existe de nombreux états standard qui vous permettent de vérifier la précision des comptes avant de clôturer les livres à la fin d'un exercice ou d'une période.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-104">There are many standard reports that you can use to verify the accuracy of the accounts before closing the books at the end of a year or period.</span></span> <span data-ttu-id="e2d1f-105">Par exemple, vous pouvez utiliser l'état **Clients : Balance** pour vérifier que le solde d'un groupe comptabilisation client est égal au solde du compte général correspondant à une date donnée.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-105">For example, you can use the **Customer - Trial Balance** report to verify that the balance for a customer posting group is equal to the balance on the corresponding general ledger account on a certain date.</span></span>

<span data-ttu-id="e2d1f-106">Le tableau suivant décrit un certain nombre d'états qui peuvent être utiles dans ce processus.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-106">The following table describes a number of reports that may be useful in this process.</span></span>

| <span data-ttu-id="e2d1f-107">Pour</span><span class="sxs-lookup"><span data-stu-id="e2d1f-107">To</span></span> | <span data-ttu-id="e2d1f-108">Afficher ce rapport</span><span class="sxs-lookup"><span data-stu-id="e2d1f-108">See this report</span></span> |
| --- | --- |
| <span data-ttu-id="e2d1f-109">Imprimer un état Balance détaillé pour un ou plusieurs comptes bancaires avec des informations supplémentaires sur des écritures individuelles.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-109">Print a detailed trial balance report for one or more bank accounts with additional information about individual entries.</span></span> |<span data-ttu-id="e2d1f-110">Banque : Grand livre</span><span class="sxs-lookup"><span data-stu-id="e2d1f-110">Bank Acc. - Detail Trial Bal.</span></span> |
| <span data-ttu-id="e2d1f-111">Imprimer un Grand livre pour les clients sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-111">Print a detail trial balance for selected customers.</span></span> |<span data-ttu-id="e2d1f-112">Clients : Balance</span><span class="sxs-lookup"><span data-stu-id="e2d1f-112">Customer - Trial Balance</span></span> |
| <span data-ttu-id="e2d1f-113">Imprimer un Grand livre avec des informations détaillées sur des écritures individuelles pour les clients sélectionnés et durant une période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-113">Print a detail trial balance with detailed information about individual entries, for selected customers during a selected period.</span></span> |<span data-ttu-id="e2d1f-114">Clients : Grand livre client</span><span class="sxs-lookup"><span data-stu-id="e2d1f-114">Customer - Detail Trial Bal.</span></span> |
| <span data-ttu-id="e2d1f-115">Imprimer un Grand livre pour les fournisseurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-115">Print a detail trial balance for selected vendors.</span></span> |<span data-ttu-id="e2d1f-116">Fourn. : Balance</span><span class="sxs-lookup"><span data-stu-id="e2d1f-116">Vendor - Trial Balance</span></span> |
| <span data-ttu-id="e2d1f-117">Imprimer un Grand livre avec des informations détaillées sur des écritures individuelles pour les fournisseurs sélectionnés et durant une période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-117">Print a detail trial balance with detailed information about individual entries, for selected vendors during a selected period.</span></span> |<span data-ttu-id="e2d1f-118">Fourn. : Grand livre fourn.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-118">Vendor - Detail Trial Balance</span></span> |
| <span data-ttu-id="e2d1f-119">Imprimer une balance avec les chiffres de l'exercice en cours et de l'exercice précédent.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-119">Print a trial balance with the current year's and the previous year's figures.</span></span> |<span data-ttu-id="e2d1f-120">Balance de clôture</span><span class="sxs-lookup"><span data-stu-id="e2d1f-120">Closing Trial Balance</span></span> |
| <span data-ttu-id="e2d1f-121">Imprimer un état Grand livre pour les soldes des comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-121">Print a detailed trial balance report for general ledger account balances.</span></span> |<span data-ttu-id="e2d1f-122">Grand livre</span><span class="sxs-lookup"><span data-stu-id="e2d1f-122">Detail Trial Balance</span></span> |
| <span data-ttu-id="e2d1f-123">Imprimer un état Balance comprenant les soldes et les soldes période pour les comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-123">Print a trial balance report with balances and net changes for general ledger accounts.</span></span> |<span data-ttu-id="e2d1f-124">Balance</span><span class="sxs-lookup"><span data-stu-id="e2d1f-124">Trial Balance</span></span> |
| <span data-ttu-id="e2d1f-125">Imprimer une balance pour une société consolidée.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-125">Print a trial balance for a consolidated company.</span></span> |<span data-ttu-id="e2d1f-126">Balance consolidée</span><span class="sxs-lookup"><span data-stu-id="e2d1f-126">Consolidated Trial Balance</span></span> |

<span data-ttu-id="e2d1f-127">Pour visualiser un état, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez le nom qui s'affiche dans la table, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="e2d1f-127">To see a report, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, type the name as it appears in the table, and then choose the related link.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2d1f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2d1f-128">See Also</span></span>
[<span data-ttu-id="e2d1f-129">Clôture des exercices et des périodes</span><span class="sxs-lookup"><span data-stu-id="e2d1f-129">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="e2d1f-130">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e2d1f-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

