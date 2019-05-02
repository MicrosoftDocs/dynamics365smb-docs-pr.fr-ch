---
title: Définir une méthode TEC et surveiller la progression du projet | Microsoft Docs
description: Décrit la manière dont vous pouvez créer une méthode de travaux en cours (TEC) et calculer les TEC pour estimer la valeur financière des projets lorsqu'ils sont en cours.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 79e5a1e34fbd6c119be52deec60bba494fdd2671
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821500"
---
# <a name="monitor-job-progress-and-performance"></a><span data-ttu-id="3749e-103">Surveiller la progression et les performances</span><span class="sxs-lookup"><span data-stu-id="3749e-103">Monitor Job Progress and Performance</span></span>
<span data-ttu-id="3749e-104">Au fur et à mesure de la progression du projet, les matières, ressources et autres frais sont consommés et doivent être validés dans le projet.</span><span class="sxs-lookup"><span data-stu-id="3749e-104">As a job progresses, materials, resources, and other expenses are consumed and must be posted to the job.</span></span> <span data-ttu-id="3749e-105">La fonctionnalité Travaux en cours (TEC) permet d'estimer la valeur financière des projets dans la comptabilité au cours des projets.</span><span class="sxs-lookup"><span data-stu-id="3749e-105">Work in Process (WIP) is a feature that enables you to estimate the financial value of jobs in the general ledger while the jobs are ongoing.</span></span> <span data-ttu-id="3749e-106">Dans de nombreux cas, vous pouvez valider les frais pour un projet avant de le facturer.</span><span class="sxs-lookup"><span data-stu-id="3749e-106">In many cases, you might post expenses for a job before invoicing a job.</span></span> <span data-ttu-id="3749e-107">Lorsque seuls les frais sont validés, l'état financier est incorrect.</span><span class="sxs-lookup"><span data-stu-id="3749e-107">When only expenses have been posted, your financial statement will be inaccurate.</span></span> <span data-ttu-id="3749e-108">Pour en savoir plus, reportez-vous à [Comprendre les méthodes TEC](projects-understanding-wip.md).</span><span class="sxs-lookup"><span data-stu-id="3749e-108">For more information, see [Understanding WIP Methods](projects-understanding-wip.md).</span></span>

<span data-ttu-id="3749e-109">Pour effectuer le suivi de la valeur dans la comptabilité, vous pouvez calculer les TEC et valider la valeur en comptabilité.</span><span class="sxs-lookup"><span data-stu-id="3749e-109">To track the value in the general ledger, you can calculate WIP and post the value to the general ledger.</span></span>

<span data-ttu-id="3749e-110">Vous pouvez calculer les TEC sur la base des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3749e-110">You can calculate WIP based on the following:</span></span>

* <span data-ttu-id="3749e-111">Valeur de coût</span><span class="sxs-lookup"><span data-stu-id="3749e-111">Cost Value</span></span>
* <span data-ttu-id="3749e-112">Valeur des ventes</span><span class="sxs-lookup"><span data-stu-id="3749e-112">Sales Value</span></span>
* <span data-ttu-id="3749e-113">Coût identifiable</span><span class="sxs-lookup"><span data-stu-id="3749e-113">Recognizable Cost</span></span>
* <span data-ttu-id="3749e-114">Pourcentage avancement</span><span class="sxs-lookup"><span data-stu-id="3749e-114">Percentage of Completion</span></span>
* <span data-ttu-id="3749e-115">Fin de contrat</span><span class="sxs-lookup"><span data-stu-id="3749e-115">Completed Contract</span></span>

<span data-ttu-id="3749e-116">Pour afficher le résultat avec une autre méthode, vous pouvez modifier la méthode et calculer les TEC de nouveau.</span><span class="sxs-lookup"><span data-stu-id="3749e-116">If you want to view the result using a different method, you can change the method and calculate WIP again.</span></span> <span data-ttu-id="3749e-117">Le calcul des TEC peut être exécuté un nombre illimité de fois.</span><span class="sxs-lookup"><span data-stu-id="3749e-117">There is no limit to the number of times that you calculate WIP.</span></span> <span data-ttu-id="3749e-118">Le TEC est uniquement calculé, il n'est pas validé dans la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="3749e-118">WIP is only calculated, it does not get posted to the general ledger.</span></span> <span data-ttu-id="3749e-119">Une fois les TEC calculés, vous pouvez effectuer une validation dans la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="3749e-119">After you have calculated WIP, you can post to the general ledger.</span></span>

## <a name="to-create-a-job-wip-method"></a><span data-ttu-id="3749e-120">Pour créer une méthode TEC projet</span><span class="sxs-lookup"><span data-stu-id="3749e-120">To create a job WIP method</span></span>
<span data-ttu-id="3749e-121">Vous pouvez créer une méthode TEC projet qui reflète les besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3749e-121">You can create a job WIP method that reflects the needs of your organization.</span></span> <span data-ttu-id="3749e-122">Après l'avoir créée, vous pouvez la configurer comme méthode par défaut de calcul TEC projet qui sera utilisée dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3749e-122">After you have created it, you can set it as the default job WIP calculation method that will be used in your organization.</span></span>  

> [!NOTE]
> <span data-ttu-id="3749e-123">Après avoir utilisé la nouvelle méthode pour créer des écritures TEC, vous ne pouvez pas supprimer la méthode ou la modifier.</span><span class="sxs-lookup"><span data-stu-id="3749e-123">After you have used your new method to create WIP entries, you cannot delete the method or modify it.</span></span>  

1. <span data-ttu-id="3749e-124">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Méthodes TEC projet**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3749e-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job WIP Methods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3749e-125">Cliquez sur **Nouveau**, puis renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="3749e-125">Choose the **New** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="3749e-126">Fermez la page.</span><span class="sxs-lookup"><span data-stu-id="3749e-126">Close the page.</span></span>   
4. <span data-ttu-id="3749e-127">Pour faire de cette nouvelle méthode la valeur par défaut, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres projets**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3749e-127">To make this new method the default, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs Setup**, and then choose the related link.</span></span>  
5. <span data-ttu-id="3749e-128">Dans le champ **Méthode TEC par défaut**, choisissez la méthode de la liste.</span><span class="sxs-lookup"><span data-stu-id="3749e-128">In the **Default WIP Method** field, choose the method from the list.</span></span>

## <a name="to-define-a-wip-method-for-a-job"></a><span data-ttu-id="3749e-129">Pour définir une méthode TEC pour un projet</span><span class="sxs-lookup"><span data-stu-id="3749e-129">To define a WIP method for a job</span></span>
<span data-ttu-id="3749e-130">Lorsque vous créez un projet, vous devez spécifier la méthode TEC projet qui s'applique.</span><span class="sxs-lookup"><span data-stu-id="3749e-130">When you create a new job, you must specify which job WIP method that applies.</span></span> <span data-ttu-id="3749e-131">Dans certains cas, quelle méthode TEC projet utilisable a été paramétrée pour vous par défaut.</span><span class="sxs-lookup"><span data-stu-id="3749e-131">In some cases, which Job WIP method that you can use has been set up for you as a default.</span></span>

1. <span data-ttu-id="3749e-132">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3749e-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="3749e-133">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="3749e-133">Choose the **New** action.</span></span> <span data-ttu-id="3749e-134">Pour plus d'informations, voir [Créer des projets](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="3749e-134">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>  
3. <span data-ttu-id="3749e-135">Sur la page **Fiche projet**, dans le champ **Méthode TEC**, sélectionnez une méthode TEC dans la liste.</span><span class="sxs-lookup"><span data-stu-id="3749e-135">On the **Job Card** page, in the **WIP Method** field, select a WIP method from the list.</span></span> <span data-ttu-id="3749e-136">Si une méthode par défaut a été définie, vous pouvez sélectionner une autre option si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3749e-136">If a default method has been defined, you can select another option if needed.</span></span>  

## <a name="to-calculate-wip"></a><span data-ttu-id="3749e-137">Pour calculer les TEC :</span><span class="sxs-lookup"><span data-stu-id="3749e-137">To calculate WIP</span></span>
<span data-ttu-id="3749e-138">Vous pouvez déterminer le montant TEC devant être validé dans les comptes de bilan pour la génération d'états de clôture d'exercice.</span><span class="sxs-lookup"><span data-stu-id="3749e-138">You can determine the WIP amount that is to be posted to balance sheet accounts for the period end reporting.</span></span> <span data-ttu-id="3749e-139">Pour ce faire, utilisez le traitement par lots **Projet Calculer TEC**.</span><span class="sxs-lookup"><span data-stu-id="3749e-139">You use the **Job Calculate WIP** batch job to do this.</span></span>  

1. <span data-ttu-id="3749e-140">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projet Calculer TEC**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3749e-140">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Calculate WIP**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3749e-141">Cliquez sur **Calculer TEC**.</span><span class="sxs-lookup"><span data-stu-id="3749e-141">Choose the **Calculate WIP** action.</span></span>
3. <span data-ttu-id="3749e-142">Sur la page **Projet Calculer TEC**, renseignez les champs comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3749e-142">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>
4. <span data-ttu-id="3749e-143">Choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="3749e-143">Choose the **OK** button.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="3749e-144">Le traitement par lots calcule uniquement les TEC.</span><span class="sxs-lookup"><span data-stu-id="3749e-144">The batch job only calculates the WIP.</span></span> <span data-ttu-id="3749e-145">Il n'est pas validé dans la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="3749e-145">It is not posted to the general ledger.</span></span> <span data-ttu-id="3749e-146">Pour ce faire, exécutez le traitement par lots **Valider TEC en compta.** à l'issue du calcul.</span><span class="sxs-lookup"><span data-stu-id="3749e-146">To do so, you must run the **Post WIP to G/L** batch job when you have calculated the WIP.</span></span> <span data-ttu-id="3749e-147">Pour plus d'informations, voir la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="3749e-147">For more information, see the following procedure.</span></span>

## <a name="to-post-wip"></a><span data-ttu-id="3749e-148">Pour valider les TEC</span><span class="sxs-lookup"><span data-stu-id="3749e-148">To post WIP</span></span>
<span data-ttu-id="3749e-149">Quand vous avez calculé les TEC, vous pouvez les valider pour équilibrer les comptes bilan pour le reporting de fin de période.</span><span class="sxs-lookup"><span data-stu-id="3749e-149">When you have calculated WIP, you can post it to balance sheet accounts for the period end reporting.</span></span> <span data-ttu-id="3749e-150">Pour ce faire, utilisez le traitement par lots **Projet Valider TEC en comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="3749e-150">You use the **Job Post WIP to G/L** batch job to do this.</span></span>

1. <span data-ttu-id="3749e-151">Choisissez l'icône de ![l'ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projet Valider TEC en comptabilité**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3749e-151">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Post WIP to G/L**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3749e-152">Sur la page **Projet Valider TEC en comptabilité**, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="3749e-152">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="3749e-153">Choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="3749e-153">Choose the **OK** button.</span></span>

## <a name="to-view-job-usage-estimates-and-post-updates"></a><span data-ttu-id="3749e-154">Pour visualiser les estimations projet et valider les mises à jour</span><span class="sxs-lookup"><span data-stu-id="3749e-154">To view job usage estimates and post updates</span></span>
<span data-ttu-id="3749e-155">Vous pouvez visualiser les activités projet jusqu'à leur achèvement en une étape.</span><span class="sxs-lookup"><span data-stu-id="3749e-155">You can view job usage up to the completion of a project in one step.</span></span> <span data-ttu-id="3749e-156">Pour ce faire, utilisez le traitement par lots **Projet Calc. activité restante** pour toutes les tâches jusqu'à la fin du projet.</span><span class="sxs-lookup"><span data-stu-id="3749e-156">To do so, you use the **Job Calc. Remaining Usage** batch job for all the tasks up to and including the end of a job.</span></span>  

<span data-ttu-id="3749e-157">Cela vous permet de suivre vos estimations initiales, de les comparer aux résultats réels, ainsi que d'apporter des modifications et d'ajouter de nouvelles écritures, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="3749e-157">This lets you track and compare your original estimates against actual results and make modifications or new entries as needed.</span></span> <span data-ttu-id="3749e-158">Par exemple, alors que vous aviez estimé qu'un projet nécessitait 10 heures de travail, vous en avez effectué 15.</span><span class="sxs-lookup"><span data-stu-id="3749e-158">For example, you may have estimated that a job required 10 hours, and to date, it has taken 15 hours.</span></span> <span data-ttu-id="3749e-159">Vous pouvez ajouter les cinq heures supplémentaires à la ligne feuille existante ou créer une ligne feuille pour les déclarer en tant qu'heures supplémentaires, ce qui constitue un autre type de tâche.</span><span class="sxs-lookup"><span data-stu-id="3749e-159">You can add the extra five hours to the existing journal line or create a new journal line to report these five hours as overtime, which is another work type.</span></span> <span data-ttu-id="3749e-160">Le coût et le prix appropriés sont calculés. Vous pouvez les valider dans la feuille.</span><span class="sxs-lookup"><span data-stu-id="3749e-160">The appropriate cost and price are calculated, and you can then post to the journal.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="3749e-161">Les écritures article créent des écritures comptables article et diminuent les articles en stock.</span><span class="sxs-lookup"><span data-stu-id="3749e-161">Item entries create item ledger entries and reduce the inventory quantity.</span></span> <span data-ttu-id="3749e-162">Le traitement par lots **Valider coûts ajustés** permet de transférer le coût du stock à la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="3749e-162">The **Post Inventory Cost to G/L** batch job transfers the cost from inventory to the general ledger.</span></span> <span data-ttu-id="3749e-163">Les écritures ressource créent des écritures comptables ressource.</span><span class="sxs-lookup"><span data-stu-id="3749e-163">Resource entries create resource ledger entries.</span></span>  

1. <span data-ttu-id="3749e-164">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles activité projet**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3749e-164">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3749e-165">Sélectionnez une feuille projet appropriée, puis cliquez sur l'action **Calc. activité restante**.</span><span class="sxs-lookup"><span data-stu-id="3749e-165">Select a relevant job journal, and then choose the **Calc. Remaining Usage** action.</span></span>  
3. <span data-ttu-id="3749e-166">Sur la page **Projet Calc. activité restante**, entrez le numéro et la date de comptabilisation du document devant être insérés dans la feuille, puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="3749e-166">On the **Job Calc. Remaining Usage** page, enter the document number and posting date that is to be inserted in the journal, and then choose the **OK** button.</span></span>  
4. <span data-ttu-id="3749e-167">Mettez à jour la feuille avec toutes les modifications qui peuvent être nécessaires.</span><span class="sxs-lookup"><span data-stu-id="3749e-167">Update the journal with any modifications that may be needed.</span></span>  
5. <span data-ttu-id="3749e-168">Sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="3749e-168">Choose the **Post**.</span></span>

## <a name="to-view-job-ledger-entries"></a><span data-ttu-id="3749e-169">Pour visualiser des écritures comptables projet</span><span class="sxs-lookup"><span data-stu-id="3749e-169">To view job ledger entries</span></span>
<span data-ttu-id="3749e-170">Toutes les écritures liées à des projets sont enregistrées dans des historiques des transactions projet et sont numérotées de manière séquentielle à partir de 1.</span><span class="sxs-lookup"><span data-stu-id="3749e-170">All job-related entries are recorded in job registers and are numbered sequentially, starting with 1.</span></span> <span data-ttu-id="3749e-171">L'historique des transactions projet permet d'obtenir un aperçu de toutes les écritures comptables projet.</span><span class="sxs-lookup"><span data-stu-id="3749e-171">From the job register, you can get an overview of all job ledger entries.</span></span>    

1. <span data-ttu-id="3749e-172">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Hist. transactions projet**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3749e-172">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Registers**, and then choose the related link.</span></span>
2. <span data-ttu-id="3749e-173">Sélectionnez un historique approprié, puis cliquez sur **Écritures projet**</span><span class="sxs-lookup"><span data-stu-id="3749e-173">Select a relevant register, and then choose **Job Ledger** action.</span></span>

<span data-ttu-id="3749e-174">Sur la page **Écritures comptables projet** vous pouvez passer en revue les écritures associées à un projet.</span><span class="sxs-lookup"><span data-stu-id="3749e-174">On the **Job Ledger Entries** page you can review the entries that are associated with any job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3749e-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3749e-175">See Also</span></span>
<span data-ttu-id="3749e-176">[Gestion des projets](projects-manage-projects.md)
[Gestion de l'évaluation stock](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="3749e-176">[Managing Projects](projects-manage-projects.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
[<span data-ttu-id="3749e-177">Finances</span><span class="sxs-lookup"><span data-stu-id="3749e-177">Finance</span></span>](finance.md)  
<span data-ttu-id="3749e-178">[Achats](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="3749e-178">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="3749e-179">[Ventes](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="3749e-179">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="3749e-180">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3749e-180">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  