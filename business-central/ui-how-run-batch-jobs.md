---
title: Créer et exécuter un traitement par lots| Microsoft Docs
description: Vous exécutez des traitements par lots pour traiter les données et mettre à jour les informations, par exemple, pour élaborer des activités périodiques de comptabilité, ou effectuer des calculs.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 0b9bf37f9054d767938b851e399a1b2c347f77c3
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "937401"
---
# <a name="run-batch-jobs"></a><span data-ttu-id="76daa-103">Exécuter des traitements par lots</span><span class="sxs-lookup"><span data-stu-id="76daa-103">Run Batch Jobs</span></span>
<span data-ttu-id="76daa-104">Un traitement par lots est une routine qui traite les données par lots, par exemple le traitement par lots **Ajuster taux de change**.</span><span class="sxs-lookup"><span data-stu-id="76daa-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="76daa-105">Certains traitements par lots exécutent des activités périodiques de comptabilité, telles que la clôture des comptes de gestion à la fin d'un exercice comptable.</span><span class="sxs-lookup"><span data-stu-id="76daa-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="76daa-106">De nombreux traitements par lots exécutent des calculs, telles que le calcul des intérêts de retard, l'ajustement du taux de change et le calcul des prix unitaires.</span><span class="sxs-lookup"><span data-stu-id="76daa-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="76daa-107">Un traitement par lots est similaire à un état, sauf qu'il utilise les résultats obtenus pour mettre à jour les informations directement plutôt que d'imprimer les résultats.</span><span class="sxs-lookup"><span data-stu-id="76daa-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="76daa-108">Pour exécuter un traitement par lots</span><span class="sxs-lookup"><span data-stu-id="76daa-108">To run a batch job</span></span>
1. <span data-ttu-id="76daa-109">Pour ouvrir la page de demande du traitement par lots approprié, choisissez l'icone ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez le nom du traitement par lots, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="76daa-109">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="76daa-110">Si un raccourci **Options** est disponible pour le traitement par lots, renseignez-en les champs pour déterminer les tâches effectuées par le traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="76daa-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="76daa-111">La page peut inclure un ou plusieurs raccourcis avec des filtres que vous pouvez utiliser pour limiter les données incluses dans le traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="76daa-111">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="76daa-112">Pour cela, entrez des critères dans les filtres suggérés ou ajoutez des filtres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="76daa-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="76daa-113">Pour démarrer le traitement par lots, cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="76daa-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="76daa-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76daa-114">See Also</span></span>
[<span data-ttu-id="76daa-115">Tri, recherche et filtrage de listes</span><span class="sxs-lookup"><span data-stu-id="76daa-115">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="76daa-116">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="76daa-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
