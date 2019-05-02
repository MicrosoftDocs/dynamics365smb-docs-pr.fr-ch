---
title: Vérifier et valider l'écriture de clôture d'exercice | Microsoft Docs
description: Décrit comment ouvrir la feuille spécifiée dans le traitement par lots Clôturer exercice comptable, puis examiner et valider l'écriture de clôture de fin d'exercice.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: cd555cc389ff7d9e306645475ef042f7ee9bc934
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821558"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="011ea-103">Valider l'écriture de clôture d'exercice</span><span class="sxs-lookup"><span data-stu-id="011ea-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="011ea-104">Après avoir utilisé le traitement par lots **Solder les comptes de gestion** pour générer les écritures de clôture d'exercice, vous devez ouvrir la feuille spécifiée dans le traitement par lots, puis consulter et valider les écritures.</span><span class="sxs-lookup"><span data-stu-id="011ea-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="011ea-105">Pour valider l'écriture de clôture d'exercice</span><span class="sxs-lookup"><span data-stu-id="011ea-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="011ea-106">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille comptabilité**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="011ea-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="011ea-107">Sur la page **Feuille comptabilité**, dans le champ **Nom de la feuille**, sélectionnez la feuille qui contient les écritures de clôture.</span><span class="sxs-lookup"><span data-stu-id="011ea-107">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="011ea-108">Examinez les écritures.</span><span class="sxs-lookup"><span data-stu-id="011ea-108">Review the entries.</span></span>
4. <span data-ttu-id="011ea-109">Pour valider la feuille, sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="011ea-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="011ea-110">En cas de détection d'une erreur, un message d'erreur s'affiche.</span><span class="sxs-lookup"><span data-stu-id="011ea-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="011ea-111">Si la validation réussit, les entrées validées sont supprimées de la feuille.</span><span class="sxs-lookup"><span data-stu-id="011ea-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="011ea-112">Une fois la validation terminée, une entrée est validée dans chaque compte résultats, de façon à ce que son solde indique zéro et à ce que les résultats de l'exercice soient transférés vers le bilan.</span><span class="sxs-lookup"><span data-stu-id="011ea-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="011ea-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="011ea-113">See Also</span></span>
[<span data-ttu-id="011ea-114">Clôturer des périodes comptables</span><span class="sxs-lookup"><span data-stu-id="011ea-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="011ea-115">Clôture plans</span><span class="sxs-lookup"><span data-stu-id="011ea-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="011ea-116">Clôturer exercice comptable</span><span class="sxs-lookup"><span data-stu-id="011ea-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="011ea-117">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="011ea-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>