---
title: Clôturer des périodes comptables pour un exercice comptable | Microsoft Docs
description: Décrit comment clôturer les périodes comptables de l’exercice comptable.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a26baaf947fdac133e3bfcd50489d680231d9971
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786697"
---
# <a name="close-accounting-periods"></a><span data-ttu-id="d53d1-103">Clôturer des périodes comptables</span><span class="sxs-lookup"><span data-stu-id="d53d1-103">Close Accounting Periods</span></span>
<span data-ttu-id="d53d1-104">Lorsqu’un exercice comptable est terminé, vous devez clôturer les périodes qui le composent.</span><span class="sxs-lookup"><span data-stu-id="d53d1-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="d53d1-105">Pour clôturer des périodes comptables</span><span class="sxs-lookup"><span data-stu-id="d53d1-105">To close accounting periods</span></span>
1. <span data-ttu-id="d53d1-106">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Périodes comptables**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="d53d1-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="d53d1-107">Sur la page **Périodes comptables**, sélectionnez l’action **Clôturer exercice**.</span><span class="sxs-lookup"><span data-stu-id="d53d1-107">On the **Accounting Periods** page, choose the **Close Year** action.</span></span>

    <span data-ttu-id="d53d1-108">Si plusieurs exercices comptables sont ouverts, le plus ancien est automatiquement sélectionné pour être clôturé.</span><span class="sxs-lookup"><span data-stu-id="d53d1-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="d53d1-109">Un message identifiant l’exercice qu’il compte clôturer s’affiche et indique les conséquences de la clôture.</span><span class="sxs-lookup"><span data-stu-id="d53d1-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="d53d1-110">Pour clôturer l’exercice, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="d53d1-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="d53d1-111">L’exercice comptable est désormais clôturé, et les champs **Fermé** et **Verrouillage date** sont sélectionnés pour toutes les périodes de l’exercice.</span><span class="sxs-lookup"><span data-stu-id="d53d1-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="d53d1-112">Vous ne pouvez pas rouvrir l’exercice comptable ni supprimer la coche des champs **Fermé** et **Verrouillage date**.</span><span class="sxs-lookup"><span data-stu-id="d53d1-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d53d1-113">Vous ne pouvez pas clôturer un exercice comptable avant d’en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="d53d1-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="d53d1-114">Sachez que lorsqu’un exercice comptable est clôturé, vous ne pouvez pas modifier la date début de l’exercice comptable suivant.</span><span class="sxs-lookup"><span data-stu-id="d53d1-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="d53d1-115">Même si un exercice comptable a été clôturé, vous pouvez toujours y valider des écritures.</span><span class="sxs-lookup"><span data-stu-id="d53d1-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="d53d1-116">Dans ce cas, les écritures sont marquées comme validées dans un exercice comptable clôturé et le champ **Ecr. exercice précédent** est activé.</span><span class="sxs-lookup"><span data-stu-id="d53d1-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="d53d1-117">Une fois qu’un exercice comptable a été clôturé, vous devez clôturer les comptes de gestion et transférer les résultats de l’exercice sur un compte du bilan.</span><span class="sxs-lookup"><span data-stu-id="d53d1-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="d53d1-118">Vous pouvez répéter cette opération chaque fois que vous validez dans l’exercice comptable clôturé.</span><span class="sxs-lookup"><span data-stu-id="d53d1-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="d53d1-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d53d1-119">See Also</span></span>

[<span data-ttu-id="d53d1-120">Clôture plans</span><span class="sxs-lookup"><span data-stu-id="d53d1-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="d53d1-121">Valider l’écriture de clôture d’exercice</span><span class="sxs-lookup"><span data-stu-id="d53d1-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="d53d1-122">Utiliser des périodes et exercices comptables</span><span class="sxs-lookup"><span data-stu-id="d53d1-122">Work with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)  
<span data-ttu-id="d53d1-123">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d53d1-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]