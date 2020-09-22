---
title: Créez une facture vente projet pour facturer un projet| Microsoft Docs
description: Décrit comment facturer des clients pour les coûts au fur et à mesure de l'avancée du projet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 05/25/2020
ms.author: edupont
ms.openlocfilehash: 66e5dd52eb01e8a396156d0c646a43916fdc0021
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783972"
---
# <a name="invoice-jobs"></a><span data-ttu-id="baf10-103">Facturation des projets</span><span class="sxs-lookup"><span data-stu-id="baf10-103">Invoice Jobs</span></span>
<span data-ttu-id="baf10-104">Au cours du projet, les coûts provenant de l'utilisation de ressources, de matières, et d'achats associés au projet peuvent s'accumuler.</span><span class="sxs-lookup"><span data-stu-id="baf10-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="baf10-105">Au fur et à mesure de la progression du projet, ces transactions sont validées dans la feuille projet.</span><span class="sxs-lookup"><span data-stu-id="baf10-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="baf10-106">Il est important que tous les coûts enregistrés dans la feuille projet avant de facturer le client.</span><span class="sxs-lookup"><span data-stu-id="baf10-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

> [!NOTE]
> <span data-ttu-id="baf10-107">Vous pouvez également acheter des ressources externes non liées à un projet, par exemple pour facturer un fournisseur pour le travail livré.</span><span class="sxs-lookup"><span data-stu-id="baf10-107">You can also purchase external resources unrelated to a job, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="baf10-108">Pour en savoir plus, consultez [Enregistrer des achats](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="baf10-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="baf10-109">Vous pouvez facturer l'ensemble du projet à partir de la page **Lignes tâche projet** ou facturer uniquement les lignes facturables sélectionnées sur la page **Lignes planning**.</span><span class="sxs-lookup"><span data-stu-id="baf10-109">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="baf10-110">La facturation peut avoir lieu une fois le projet terminé ou à certains intervalles au cours du projet sur la base d'une prévision de facture.</span><span class="sxs-lookup"><span data-stu-id="baf10-110">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
> <span data-ttu-id="baf10-111">Si vous sélectionnez **Facturable** dans le champ **Type ligne projet** dans les documents d'achat pour les achats associés au projet, les lignes planning projet prêtes pour facturation sont créées.</span><span class="sxs-lookup"><span data-stu-id="baf10-111">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="baf10-112">Pour en savoir plus, voir [Gérer des fournitures d'un projet](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="baf10-112">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-multiple-job-sales-invoices"></a><span data-ttu-id="baf10-113">Pour créer plusieurs factures vente projet</span><span class="sxs-lookup"><span data-stu-id="baf10-113">To create multiple job sales invoices</span></span>
<span data-ttu-id="baf10-114">Vous pouvez créer une facture pour un projet ou pour une ou plusieurs tâches projet pour un client lorsque le travail à facturer est terminé ou lorsque la date de facturation dépendante d'une prévision de facture est atteinte.</span><span class="sxs-lookup"><span data-stu-id="baf10-114">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="baf10-115">La procédure suivante explique comment utiliser un traitement par lots pour facturer plusieurs projets.</span><span class="sxs-lookup"><span data-stu-id="baf10-115">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="baf10-116">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projet Créer facture vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="baf10-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="baf10-117">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="baf10-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="baf10-118">Définissez des filtres si vous souhaitez limiter le nombre de projets que le traitement par lots va traiter.</span><span class="sxs-lookup"><span data-stu-id="baf10-118">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="baf10-119">Pour créer les factures, cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="baf10-119">Choose the **OK** button to create the invoices.</span></span>  

<span data-ttu-id="baf10-120">Vous pouvez examiner et valider les factures créées dans la fenêtre **Factures vente**.</span><span class="sxs-lookup"><span data-stu-id="baf10-120">You can review and post created invoices in the **Sales Invoices** window.</span></span>

> [!NOTE]
> <span data-ttu-id="baf10-121">Sinon, facturez un client en sélectionnant le projet, puis en choisissant l'action **Créer une facture vente projet**.</span><span class="sxs-lookup"><span data-stu-id="baf10-121">Alternatively, invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a><span data-ttu-id="baf10-122">Pour créer et valider une facture vente projet à partir de lignes planning projet</span><span class="sxs-lookup"><span data-stu-id="baf10-122">To create and post job sales invoice from job planning lines</span></span>
<span data-ttu-id="baf10-123">Vous pouvez créer une facture à partir des lignes planning projet et indiquer à ce moment-là la quantité de l'article, la ressource ou le compte général sur lequel vous souhaitez facturer.</span><span class="sxs-lookup"><span data-stu-id="baf10-123">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="baf10-124">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="baf10-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="baf10-125">Ouvrez le projet approprié.</span><span class="sxs-lookup"><span data-stu-id="baf10-125">Open a relevant job.</span></span>
3. <span data-ttu-id="baf10-126">Sélectionnez une tâche projet pour laquelle le champ **Type tâche projet** contient **Validation** puis, cliquez sur **Lignes planning projet**.</span><span class="sxs-lookup"><span data-stu-id="baf10-126">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="baf10-127">Dans une ligne planning projet, dans le champ **Qté à transférer à facturer**, saisissez la quantité de l'article, la ressource, le type de compte général sur lequel vous souhaitez facturer.</span><span class="sxs-lookup"><span data-stu-id="baf10-127">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="baf10-128">Cliquez sur **Créer facture vente**.</span><span class="sxs-lookup"><span data-stu-id="baf10-128">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="baf10-129">Sur la page **Projet Créer facture vente**, saisissez la date de validation et si vous souhaitez créer une facture ou ajouter cette facture à une facture existante.</span><span class="sxs-lookup"><span data-stu-id="baf10-129">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="baf10-130">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="baf10-130">Choose the **OK** button.</span></span>  
8. <span data-ttu-id="baf10-131">Sur la page **Lignes planning projet**, cliquez sur **Avoirs/Factures vente**.</span><span class="sxs-lookup"><span data-stu-id="baf10-131">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="baf10-132">La page **Facture vente** s'ouvre et affiche la quantité que vous avez transférée à la facture.</span><span class="sxs-lookup"><span data-stu-id="baf10-132">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>
9. <span data-ttu-id="baf10-133">Apportez les modifications supplémentaires, puis cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="baf10-133">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="baf10-134">La procédure ci-dessus permet également de créer, de consulter, puis de valider un avoir vente associé à un projet.</span><span class="sxs-lookup"><span data-stu-id="baf10-134">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="baf10-135">Pour calculer et valider les écritures d'achèvement du projet</span><span class="sxs-lookup"><span data-stu-id="baf10-135">To calculate and post job completion entries</span></span>
<span data-ttu-id="baf10-136">À la fin des activités d'un projet (validation et facturation comprises), vous devez le mettre à jour pour définir le **Statut** du projet sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="baf10-136">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="baf10-137">Ensuite, vous devez contrepasser tous les travaux en cours validés antérieurement dans la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="baf10-137">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="baf10-138">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="baf10-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="baf10-139">Sélectionnez un projet ouvert, puis cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="baf10-139">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="baf10-140">Dans le champ **Statut**, sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="baf10-140">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="baf10-141">Suivez les étapes d'aide pour calculer et valider les travaux en cours.</span><span class="sxs-lookup"><span data-stu-id="baf10-141">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="baf10-142">Sinon, suivez les étapes 5 et 6 pour le faire manuellement.</span><span class="sxs-lookup"><span data-stu-id="baf10-142">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="baf10-143">Cliquez sur **Calculer TEC**.</span><span class="sxs-lookup"><span data-stu-id="baf10-143">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="baf10-144">Sur la page **Projet Calculer TEC**, renseignez les champs comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="baf10-144">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="baf10-145">Les écritures TEC projet créées par le traitement par lots auront la case **Projet terminé** cochée pour indiquer qu'il s'agit d'écritures d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="baf10-145">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="baf10-146">Cliquez sur **Projet Valider TEC en comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="baf10-146">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="baf10-147">Sur la page **Projet Valider TEC en comptabilité**, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="baf10-147">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="baf10-148">Les écritures comptabilité TEC projet créées par le traitement par lots verront la case **Projet terminé** cochée pour indiquer qu'il s'agit d'écritures d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="baf10-148">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="baf10-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="baf10-149">See Also</span></span>
[<span data-ttu-id="baf10-150">Gestion des projets</span><span class="sxs-lookup"><span data-stu-id="baf10-150">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="baf10-151">Finances</span><span class="sxs-lookup"><span data-stu-id="baf10-151">Finance</span></span>](finance.md)  
<span data-ttu-id="baf10-152">[Achats](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="baf10-152">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="baf10-153">[Ventes](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="baf10-153">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="baf10-154">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="baf10-154">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
