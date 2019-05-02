---
title: Créez une facture vente projet pour facturer un projet| Microsoft Docs
description: Décrit comment facturer des clients pour les coûts au fur et à mesure de l'avancée du projet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 73894bb8c7193d96ca1f4c4f7c8b8394b1f26f5f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820381"
---
# <a name="invoice-jobs"></a><span data-ttu-id="9d244-103">Facturation des projets</span><span class="sxs-lookup"><span data-stu-id="9d244-103">Invoice Jobs</span></span>
<span data-ttu-id="9d244-104">Au cours du projet, les coûts provenant de l'utilisation de ressources, de matières, et d'achats associés au projet peuvent s'accumuler.</span><span class="sxs-lookup"><span data-stu-id="9d244-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="9d244-105">Au fur et à mesure de la progression du projet, ces transactions sont validées dans la feuille projet.</span><span class="sxs-lookup"><span data-stu-id="9d244-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="9d244-106">Il est important que tous les coûts enregistrés dans la feuille projet avant de facturer le client.</span><span class="sxs-lookup"><span data-stu-id="9d244-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

<span data-ttu-id="9d244-107">Vous pouvez facturer l'ensemble du projet à partir de la page **Lignes tâche projet** ou facturer uniquement les lignes facturables sélectionnées sur la page **Lignes planning**.</span><span class="sxs-lookup"><span data-stu-id="9d244-107">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="9d244-108">La facturation peut avoir lieu une fois le projet terminé ou à certains intervalles au cours du projet sur la base d'une prévision de facture.</span><span class="sxs-lookup"><span data-stu-id="9d244-108">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="9d244-109">Si vous sélectionnez **Facturable** dans le champ **Type ligne projet** dans les documents d'achat pour les achats associés au projet, les lignes planning projet prêtes pour facturation sont créées.</span><span class="sxs-lookup"><span data-stu-id="9d244-109">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="9d244-110">Pour en savoir plus, voir [Gérer des fournitures d'un projet](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="9d244-110">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="9d244-111">Pour créer et valider une facture vente projet</span><span class="sxs-lookup"><span data-stu-id="9d244-111">To create and post a job sales invoice</span></span>
<span data-ttu-id="9d244-112">Vous pouvez créer une facture pour un projet ou pour une ou plusieurs tâches projet pour un client lorsque le travail à facturer est terminé ou lorsque la date de facturation dépendante d'une prévision de facture est atteinte.</span><span class="sxs-lookup"><span data-stu-id="9d244-112">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="9d244-113">Sur la page **Projets**, vous pouvez facturer un client en sélectionnant le projet, puis en cliquant sur **Créer une facture vente projet**.</span><span class="sxs-lookup"><span data-stu-id="9d244-113">From the **Jobs** page, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="9d244-114">La procédure suivante explique comment utiliser un traitement par lots pour facturer plusieurs projets.</span><span class="sxs-lookup"><span data-stu-id="9d244-114">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="9d244-115">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projet Créer facture vente**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="9d244-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9d244-116">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="9d244-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="9d244-117">Définissez des filtres si vous souhaitez limiter le nombre de projets que le traitement par lots va traiter.</span><span class="sxs-lookup"><span data-stu-id="9d244-117">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="9d244-118">Pour créer les factures, cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d244-118">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="9d244-119">Pour créer plusieurs factures vente projet à partir de lignes planning projet</span><span class="sxs-lookup"><span data-stu-id="9d244-119">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="9d244-120">Vous pouvez créer une facture à partir des lignes planning projet et indiquer à ce moment-là la quantité de l'article, la ressource ou le compte général sur lequel vous souhaitez facturer.</span><span class="sxs-lookup"><span data-stu-id="9d244-120">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="9d244-121">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="9d244-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="9d244-122">Ouvrez le projet approprié.</span><span class="sxs-lookup"><span data-stu-id="9d244-122">Open a relevant job.</span></span>
3. <span data-ttu-id="9d244-123">Sélectionnez une tâche projet pour laquelle le champ **Type tâche projet** contient **Validation** puis, cliquez sur **Lignes planning projet**.</span><span class="sxs-lookup"><span data-stu-id="9d244-123">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="9d244-124">Dans une ligne planning projet, dans le champ **Qté à transférer à facturer**, saisissez la quantité de l'article, la ressource, le type de compte général sur lequel vous souhaitez facturer.</span><span class="sxs-lookup"><span data-stu-id="9d244-124">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="9d244-125">Cliquez sur **Créer facture vente**.</span><span class="sxs-lookup"><span data-stu-id="9d244-125">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="9d244-126">Sur la page **Projet Créer facture vente**, saisissez la date de validation et si vous souhaitez créer une facture ou ajouter cette facture à une facture existante.</span><span class="sxs-lookup"><span data-stu-id="9d244-126">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="9d244-127">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d244-127">Choose the **OK** button.</span></span>  

    <span data-ttu-id="9d244-128">Dans la ligne planning projet, dans le champ **Qté à transférer à facturer**, vous pouvez visualiser la quantité.</span><span class="sxs-lookup"><span data-stu-id="9d244-128">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="9d244-129">Sur la page **Lignes planning projet**, cliquez sur **Avoirs/Factures vente**.</span><span class="sxs-lookup"><span data-stu-id="9d244-129">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="9d244-130">La page **Facture vente** s'ouvre et affiche la quantité que vous avez transférée à la facture.</span><span class="sxs-lookup"><span data-stu-id="9d244-130">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="9d244-131">Apportez les modifications supplémentaires, puis cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="9d244-131">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="9d244-132">La procédure ci-dessus permet également de créer, de consulter, puis de valider un avoir vente associé à un projet.</span><span class="sxs-lookup"><span data-stu-id="9d244-132">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="9d244-133">Pour calculer et valider les écritures d'achèvement du projet</span><span class="sxs-lookup"><span data-stu-id="9d244-133">To calculate and post job completion entries</span></span>
<span data-ttu-id="9d244-134">À la fin des activités d'un projet (validation et facturation comprises), vous devez le mettre à jour pour définir le **Statut** du projet sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="9d244-134">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="9d244-135">Ensuite, vous devez contrepasser tous les travaux en cours validés antérieurement dans la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="9d244-135">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="9d244-136">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="9d244-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9d244-137">Sélectionnez un projet ouvert, puis cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="9d244-137">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="9d244-138">Dans le champ **Statut**, sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="9d244-138">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="9d244-139">Suivez les étapes d'aide pour calculer et valider les travaux en cours.</span><span class="sxs-lookup"><span data-stu-id="9d244-139">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="9d244-140">Sinon, suivez les étapes 5 et 6 pour le faire manuellement.</span><span class="sxs-lookup"><span data-stu-id="9d244-140">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="9d244-141">Cliquez sur **Calculer TEC**.</span><span class="sxs-lookup"><span data-stu-id="9d244-141">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="9d244-142">Sur la page **Projet Calculer TEC**, renseignez les champs comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9d244-142">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="9d244-143">Les écritures TEC projet créées par le traitement par lots auront la case **Projet terminé** cochée pour indiquer qu'il s'agit d'écritures d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="9d244-143">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="9d244-144">Cliquez sur **Projet Valider TEC en comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="9d244-144">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="9d244-145">Sur la page **Projet Valider TEC en comptabilité**, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="9d244-145">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="9d244-146">Les écritures comptabilité TEC projet créées par le traitement par lots verront la case **Projet terminé** cochée pour indiquer qu'il s'agit d'écritures d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="9d244-146">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d244-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d244-147">See Also</span></span>
[<span data-ttu-id="9d244-148">Gestion des projets</span><span class="sxs-lookup"><span data-stu-id="9d244-148">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="9d244-149">Finances</span><span class="sxs-lookup"><span data-stu-id="9d244-149">Finance</span></span>](finance.md)  
<span data-ttu-id="9d244-150">[Achats](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="9d244-150">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="9d244-151">[Ventes](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="9d244-151">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="9d244-152">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9d244-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  