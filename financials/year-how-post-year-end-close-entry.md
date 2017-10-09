---
title: "Vérifier et valider l'écriture de clôture d'exercice | Microsoft Docs"
description: "Décrit comment ouvrir la feuille spécifiée dans le traitement par lots Clôturer exercice comptable, puis examiner et valider l'écriture de clôture de fin d'exercice."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 68017b8b031ee4bd368936b6fb4de157328d7030
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-the-year-end-closing-entry"></a><span data-ttu-id="b351b-103">Comment valider l'écriture de clôture d'exercice</span><span class="sxs-lookup"><span data-stu-id="b351b-103">How to: Post the Year-End Closing Entry</span></span>
<span data-ttu-id="b351b-104">Après avoir utilisé le traitement par lots **Solder les comptes de gestion** pour générer les écritures de clôture d'exercice, vous devez ouvrir la feuille spécifiée dans le traitement par lots, puis consulter et valider les écritures.</span><span class="sxs-lookup"><span data-stu-id="b351b-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="b351b-105">Pour valider l'écriture de clôture d'exercice</span><span class="sxs-lookup"><span data-stu-id="b351b-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="b351b-106">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille comptabilité**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="b351b-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="b351b-107">Dans la fenêtre **Feuille comptabilité**, dans le champ **Nom de la feuille**, sélectionnez la feuille qui contient les écritures de clôture.</span><span class="sxs-lookup"><span data-stu-id="b351b-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="b351b-108">Examinez les écritures.</span><span class="sxs-lookup"><span data-stu-id="b351b-108">Review the entries.</span></span>
4. <span data-ttu-id="b351b-109">Pour valider la feuille, sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="b351b-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b351b-110">En cas de détection d'une erreur, un message d'erreur s'affiche.</span><span class="sxs-lookup"><span data-stu-id="b351b-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="b351b-111">Si la validation réussit, les entrées validées sont supprimées de la feuille.</span><span class="sxs-lookup"><span data-stu-id="b351b-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="b351b-112">Une fois la validation terminée, une entrée est validée dans chaque compte résultats, de façon à ce que son solde indique zéro et à ce que les résultats de l'exercice soient transférés vers le bilan.</span><span class="sxs-lookup"><span data-stu-id="b351b-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="b351b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b351b-113">See Also</span></span>
[<span data-ttu-id="b351b-114">Procédure : clôture des périodes comptables</span><span class="sxs-lookup"><span data-stu-id="b351b-114">How to: Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="b351b-115">Clôture plans</span><span class="sxs-lookup"><span data-stu-id="b351b-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="b351b-116">Clôturer exercice comptable</span><span class="sxs-lookup"><span data-stu-id="b351b-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="b351b-117">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b351b-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

