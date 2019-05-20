---
title: Spécifier la mise en page d'un chèque| Microsoft Docs
description: Vous pouvez concevoir et imprimer vos chèques dans différents formats pour respecter des normes.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/24/2019
ms.author: edupont
ms.openlocfilehash: f2b7fa01cff36e3aab335f7d5921954343c69b74
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243610"
---
# <a name="define-check-layouts"></a><span data-ttu-id="02b75-103">Définir les mises en page de chèques</span><span class="sxs-lookup"><span data-stu-id="02b75-103">Define Check Layouts</span></span>
<span data-ttu-id="02b75-104">Vous pouvez concevoir vos chèques de sorte à respecter les normes fixées par les autorités locales.</span><span class="sxs-lookup"><span data-stu-id="02b75-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="02b75-105">Vous pouvez imprimer des images de chèques en anglais, en français ou en espagnol.</span><span class="sxs-lookup"><span data-stu-id="02b75-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="02b75-106">Les chèques sont conçus pour être imprimés aux formats d'image de chèques américains et canadiens, soit au format chèque-talon-chèque, soit au format talon-talon-chèque.</span><span class="sxs-lookup"><span data-stu-id="02b75-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="02b75-107">Pour définir les mises en page de chèques</span><span class="sxs-lookup"><span data-stu-id="02b75-107">To define check layouts</span></span>
1. <span data-ttu-id="02b75-108">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Sélection des états - Compte bancaire**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="02b75-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="02b75-109">Sur la page **Sélection des états : Banque**, dans le champ **Utilisation**, sélectionnez **Chèque**</span><span class="sxs-lookup"><span data-stu-id="02b75-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="02b75-110">Sélectionnez l'un des ID état suivants.</span><span class="sxs-lookup"><span data-stu-id="02b75-110">Select one of the following report IDs.</span></span>

  | <span data-ttu-id="02b75-111">ID état</span><span class="sxs-lookup"><span data-stu-id="02b75-111">Report ID</span></span> | <span data-ttu-id="02b75-112">Nom état</span><span class="sxs-lookup"><span data-stu-id="02b75-112">Report Name</span></span> | <span data-ttu-id="02b75-113">Description</span><span class="sxs-lookup"><span data-stu-id="02b75-113">Description</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="02b75-114">1401</span><span class="sxs-lookup"><span data-stu-id="02b75-114">1401</span></span> |<span data-ttu-id="02b75-115">Activer</span><span class="sxs-lookup"><span data-stu-id="02b75-115">Check</span></span> |<span data-ttu-id="02b75-116">Il s'agit de l'état par défaut.</span><span class="sxs-lookup"><span data-stu-id="02b75-116">This is the default report.</span></span> |
  | <span data-ttu-id="02b75-117">10411</span><span class="sxs-lookup"><span data-stu-id="02b75-117">10411</span></span> |<span data-ttu-id="02b75-118">Chèque (Talon/Talon/Chèque)</span><span class="sxs-lookup"><span data-stu-id="02b75-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="02b75-119">Cet état est conçu pour imprimer des chèques au format talon/talon/chèque.</span><span class="sxs-lookup"><span data-stu-id="02b75-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
  | <span data-ttu-id="02b75-120">10412</span><span class="sxs-lookup"><span data-stu-id="02b75-120">10412</span></span> |<span data-ttu-id="02b75-121">Chèque (Talon/Chèque/Talon)</span><span class="sxs-lookup"><span data-stu-id="02b75-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="02b75-122">Cet état est conçu pour imprimer des chèques au format talon/chèque/talon.</span><span class="sxs-lookup"><span data-stu-id="02b75-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
  | <span data-ttu-id="02b75-123">10413</span><span class="sxs-lookup"><span data-stu-id="02b75-123">10413</span></span> |<span data-ttu-id="02b75-124">Trois chèques par page</span><span class="sxs-lookup"><span data-stu-id="02b75-124">Three Checks per Page</span></span> |<span data-ttu-id="02b75-125">Cet état est conçu pour imprimer trois chèques sur chaque page.</span><span class="sxs-lookup"><span data-stu-id="02b75-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="02b75-126">Une fois que vous avez défini les mises en page de chèques, vous pouvez imprimer des chèques à partir de la page **Feuille paiement**.</span><span class="sxs-lookup"><span data-stu-id="02b75-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="02b75-127">Pour plus d'informations, reportez-vous à [Utilisation des chèques](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="02b75-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="02b75-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02b75-128">See Also</span></span>
[<span data-ttu-id="02b75-129">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="02b75-129">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="02b75-130">[Gestion des comptes bancaires](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="02b75-130">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="02b75-131">Exécution des processus de clôture d'exercice</span><span class="sxs-lookup"><span data-stu-id="02b75-131">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="02b75-132">[Utilisation de [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="02b75-132">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="02b75-133">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="02b75-133">General Business Functionality</span></span>](ui-across-business-areas.md)
