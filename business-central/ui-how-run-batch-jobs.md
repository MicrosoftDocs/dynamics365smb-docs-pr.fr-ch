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
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 04ae13561f44d544d38b04e3a881a0e707b441b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760532"
---
# <a name="run-batch-jobs-and-xmlports"></a><span data-ttu-id="7ef7a-103">Exécuter des traitements par lots et des ports XML</span><span class="sxs-lookup"><span data-stu-id="7ef7a-103">Run Batch Jobs and XMLports</span></span>
<span data-ttu-id="7ef7a-104">Un traitement par lots est une routine qui traite les données par lots, par exemple le traitement par lots **Ajuster taux de change**.</span><span class="sxs-lookup"><span data-stu-id="7ef7a-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="7ef7a-105">Certains traitements par lots exécutent des activités périodiques de comptabilité, telles que la clôture des comptes de gestion à la fin d’un exercice comptable.</span><span class="sxs-lookup"><span data-stu-id="7ef7a-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="7ef7a-106">De nombreux traitements par lots exécutent des calculs, telles que le calcul des intérêts de retard, l’ajustement du taux de change et le calcul des prix unitaires.</span><span class="sxs-lookup"><span data-stu-id="7ef7a-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="7ef7a-107">Un traitement par lots est similaire à un état, sauf qu’il utilise les résultats obtenus pour mettre à jour les informations directement plutôt que d’imprimer les résultats.</span><span class="sxs-lookup"><span data-stu-id="7ef7a-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

<span data-ttu-id="7ef7a-108">Vous pouvez planifier l’exécution d’un traitement par lot.</span><span class="sxs-lookup"><span data-stu-id="7ef7a-108">You can schedule when a batch job runs.</span></span> <span data-ttu-id="7ef7a-109">Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="7ef7a-109">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="7ef7a-110">Pour exécuter un traitement par lots</span><span class="sxs-lookup"><span data-stu-id="7ef7a-110">To run a batch job</span></span>
1. <span data-ttu-id="7ef7a-111">Pour ouvrir la page de demande du traitement par lots approprié, choisissez l’icone ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez le nom du traitement par lots, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7ef7a-111">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="7ef7a-112">Si un raccourci **Options** est disponible pour le traitement par lots, renseignez-en les champs pour déterminer les tâches effectuées par le traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="7ef7a-112">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="7ef7a-113">La page peut inclure un ou plusieurs raccourcis avec des filtres que vous pouvez utiliser pour limiter les données incluses dans le traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="7ef7a-113">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="7ef7a-114">Pour cela, entrez des critères dans les filtres suggérés ou ajoutez des filtres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="7ef7a-114">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="7ef7a-115">Pour démarrer le traitement par lots, cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ef7a-115">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ef7a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ef7a-116">See Also</span></span>
[<span data-ttu-id="7ef7a-117">Tri, recherche et filtrage de listes</span><span class="sxs-lookup"><span data-stu-id="7ef7a-117">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="7ef7a-118">Utiliser des files d’attente des travaux pour planifier des tâches</span><span class="sxs-lookup"><span data-stu-id="7ef7a-118">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
<span data-ttu-id="7ef7a-119">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7ef7a-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
