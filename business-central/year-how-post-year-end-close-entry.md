---
title: Valider l’écriture de clôture d’exercice
description: Décrit comment ouvrir la feuille spécifiée dans le traitement par lots Clôturer exercice comptable, puis examiner et valider l’écriture de clôture de fin d’exercice.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5c822685ae5723bc6b13f9fedad45dbddefdb956
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776607"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="f3947-103">Valider l’écriture de clôture d’exercice</span><span class="sxs-lookup"><span data-stu-id="f3947-103">Post the Year-End Closing Entry</span></span>

<span data-ttu-id="f3947-104">Après avoir utilisé le traitement par lots **Solder les comptes de gestion** pour générer les écritures de clôture d’exercice, vous devez ouvrir la feuille spécifiée dans le traitement par lots, puis consulter et valider les écritures.</span><span class="sxs-lookup"><span data-stu-id="f3947-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>  

> [!TIP]
> <span data-ttu-id="f3947-105">En fonction des processus de travail de votre organisation, vous pouvez choisir de clôturer ou non les périodes comptables et les exercices dans [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="f3947-105">Depending on your organizations work processes, you can choose to close or not close accounting periods and fiscal years in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="f3947-106">La procédure suivante suppose que vous avez clôturé l’exercice en utilisant l’option *Périodes comptables*, généré une écriture de clôture d’exercice à l’aide du traitement par lots **Clôturer exercice comptable** et que vous êtes maintenant prêt à valider l’écriture de clôture d’exercice avec la compensation des écritures de compte de fonds propres.</span><span class="sxs-lookup"><span data-stu-id="f3947-106">The following procedure assumes that you have closed the fiscal year using the *Accounting Periods* option, generated a year-end closing entry using the **Close Income Statement** batch job, and are now ready to post the year-end closing entry along with the offsetting equity account entries.</span></span> <span data-ttu-id="f3947-107">Votre organisation peut choisir de travailler différemment, par exemple valider l’écriture de clôture d’exercice dans le cadre de la clôture de l’exercice comptable.</span><span class="sxs-lookup"><span data-stu-id="f3947-107">Your organization can choose to work differently, such as post the year-end closing entry as part of closing the fiscal year.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="f3947-108">Pour valider l’écriture de clôture d’exercice</span><span class="sxs-lookup"><span data-stu-id="f3947-108">To post the year end closing entry</span></span>

1. <span data-ttu-id="f3947-109">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille comptabilité**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f3947-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="f3947-110">Sur la page **Feuille comptabilité**, dans le champ **Nom de la feuille**, sélectionnez la feuille qui contient les écritures de clôture.</span><span class="sxs-lookup"><span data-stu-id="f3947-110">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="f3947-111">Examinez les écritures.</span><span class="sxs-lookup"><span data-stu-id="f3947-111">Review the entries.</span></span>
4. <span data-ttu-id="f3947-112">Pour valider la feuille, sélectionnez l’action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="f3947-112">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
> <span data-ttu-id="f3947-113">En cas de détection d’une erreur, un message d’erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f3947-113">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="f3947-114">Si la validation réussit, les entrées validées sont supprimées de la feuille.</span><span class="sxs-lookup"><span data-stu-id="f3947-114">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="f3947-115">Une fois la validation terminée, une entrée est validée dans chaque compte résultats, de façon à ce que son solde indique zéro et à ce que les résultats de l’exercice soient transférés vers le bilan.</span><span class="sxs-lookup"><span data-stu-id="f3947-115">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3947-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3947-116">See Also</span></span>

[<span data-ttu-id="f3947-117">Clôturer des périodes comptables</span><span class="sxs-lookup"><span data-stu-id="f3947-117">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="f3947-118">Clôture plans</span><span class="sxs-lookup"><span data-stu-id="f3947-118">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="f3947-119">Clôturer exercice comptable</span><span class="sxs-lookup"><span data-stu-id="f3947-119">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="f3947-120">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f3947-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]