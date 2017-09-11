---
title: "Spécifier la mise en page d'un chèque| Microsoft Docs"
description: "Vous pouvez concevoir et imprimer vos chèques dans différents formats pour respecter des normes."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a2db2860846cd9b8010222faf580f0c9889e39a4
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-define-check-layouts"></a><span data-ttu-id="ae786-103">Procédure : définir les mises en page de chèques</span><span class="sxs-lookup"><span data-stu-id="ae786-103">How to: Define Check Layouts</span></span>
<span data-ttu-id="ae786-104">Vous pouvez concevoir vos chèques de sorte à respecter les normes fixées par les autorités locales.</span><span class="sxs-lookup"><span data-stu-id="ae786-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="ae786-105">Vous pouvez imprimer des images de chèques en anglais, en français ou en espagnol.</span><span class="sxs-lookup"><span data-stu-id="ae786-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="ae786-106">Les chèques sont conçus pour être imprimés aux formats d'image de chèques américains et canadiens, soit au format chèque-talon-chèque, soit au format talon-talon-chèque.</span><span class="sxs-lookup"><span data-stu-id="ae786-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="ae786-107">Pour définir les mises en page de chèques</span><span class="sxs-lookup"><span data-stu-id="ae786-107">To define check layouts</span></span>
1. <span data-ttu-id="ae786-108">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Sélection des états - Compte bancaire**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="ae786-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae786-109">Dans la fenêtre **Sélection des états : Banque**,</span><span class="sxs-lookup"><span data-stu-id="ae786-109">In the **Report Selection - Bank Acc.**</span></span> <span data-ttu-id="ae786-110">dans le champ **Utilisation**, sélectionnez **Chèque**.</span><span class="sxs-lookup"><span data-stu-id="ae786-110">window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="ae786-111">Sélectionnez l'un des ID état suivants.</span><span class="sxs-lookup"><span data-stu-id="ae786-111">Select one of the following report IDs.</span></span>

| <span data-ttu-id="ae786-112">ID état</span><span class="sxs-lookup"><span data-stu-id="ae786-112">Report ID</span></span> | <span data-ttu-id="ae786-113">Nom état</span><span class="sxs-lookup"><span data-stu-id="ae786-113">Report Name</span></span> | <span data-ttu-id="ae786-114">Description</span><span class="sxs-lookup"><span data-stu-id="ae786-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ae786-115">1401</span><span class="sxs-lookup"><span data-stu-id="ae786-115">1401</span></span> |<span data-ttu-id="ae786-116">Activer</span><span class="sxs-lookup"><span data-stu-id="ae786-116">Check</span></span> |<span data-ttu-id="ae786-117">Il s'agit de l'état par défaut.</span><span class="sxs-lookup"><span data-stu-id="ae786-117">This is the default report.</span></span> |
| <span data-ttu-id="ae786-118">10401</span><span class="sxs-lookup"><span data-stu-id="ae786-118">10401</span></span> |<span data-ttu-id="ae786-119">Chèque (Talon/Talon/Chèque)</span><span class="sxs-lookup"><span data-stu-id="ae786-119">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="ae786-120">Cet état est conçu pour imprimer des chèques au format talon/talon/chèque.</span><span class="sxs-lookup"><span data-stu-id="ae786-120">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="ae786-121">10411</span><span class="sxs-lookup"><span data-stu-id="ae786-121">10411</span></span> |<span data-ttu-id="ae786-122">Chèque (Talon/Chèque/Talon)</span><span class="sxs-lookup"><span data-stu-id="ae786-122">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="ae786-123">Cet état est conçu pour imprimer des chèques au format chèque/talon/chèque.</span><span class="sxs-lookup"><span data-stu-id="ae786-123">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="ae786-124">Une fois que vous avez défini les mises en page de chèques, vous pouvez imprimer des chèques à partir de la fenêtre **Feuille paiement**.</span><span class="sxs-lookup"><span data-stu-id="ae786-124">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="ae786-125">Pour plus d'informations, reportez-vous à [Procédure : Utilisation de chèques](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="ae786-125">For more information, see [How to: Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ae786-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae786-126">See Also</span></span>
[<span data-ttu-id="ae786-127">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="ae786-127">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="ae786-128">[Gestion des comptes bancaires](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="ae786-128">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="ae786-129">Exécution des processus de clôture d'exercice</span><span class="sxs-lookup"><span data-stu-id="ae786-129">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="ae786-130">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ae786-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ae786-131">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="ae786-131">General Business Functionality</span></span>](ui-across-business-areas.md)

