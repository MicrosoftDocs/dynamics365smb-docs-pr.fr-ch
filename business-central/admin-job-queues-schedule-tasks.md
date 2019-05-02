---
title: Planifier des projets à exécuter automatiquement | Microsoft Docs
description: Les tâches planifiées sont gérées par la file d'attente des travaux. Ces projets exécutent des états et des codeunits. Vous pouvez définir des projets à exécuter une fois, ou sur une base récurrente.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/01/2019
ms.author: edupont
ms.openlocfilehash: 384bb86a6d6a7384af287d8bbd13a506e1bfcfe1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820730"
---
# <a name="use-job-queues-to-schedule-tasks"></a><span data-ttu-id="59f3c-105">Utiliser des files d'attente des travaux pour planifier des tâches</span><span class="sxs-lookup"><span data-stu-id="59f3c-105">Use Job Queues to Schedule Tasks</span></span>
<span data-ttu-id="59f3c-106">Des files d'attente des travaux dans [!INCLUDE[d365fin](includes/d365fin_md.md)] permettent aux utilisateurs de planifier et d'exécuter des états et codeunits spécifiques.</span><span class="sxs-lookup"><span data-stu-id="59f3c-106">Job queues in [!INCLUDE[d365fin](includes/d365fin_md.md)] enables users to schedule and run specific reports and codeunits.</span></span> <span data-ttu-id="59f3c-107">Vous pouvez définir des projets à exécuter une fois, ou sur une base récurrente.</span><span class="sxs-lookup"><span data-stu-id="59f3c-107">You can set jobs to run one time, or on a recurring basis.</span></span> <span data-ttu-id="59f3c-108">Par exemple, vous pouvez être amené à exécuter l'état **Vendeurs : Statistiques ventes** chaque semaine pour suivre les ventes hebdomadaires d'un vendeur, ou vous pouvez être amené à exécuter le codeunit **Traiter file att. e-mails serv** chaque jour pour vérifier si des e mails adressés aux clients concernant leurs commandes service sont envoyés en temps utile.</span><span class="sxs-lookup"><span data-stu-id="59f3c-108">For example, you might want to run the **Salesperson - Sales Statistics** report weekly, to track sales by salesperson each week, or you might want to run the **Process Service E-mail Queue** codeunit daily, to make sure pending email messages to customers regarding their service orders are sent out in a timely manner.</span></span>

<span data-ttu-id="59f3c-109">La page **Écritures file d'attente des travaux** répertorie tous les projets existants.</span><span class="sxs-lookup"><span data-stu-id="59f3c-109">The **Job Queue Entries** page lists all existing jobs.</span></span> <span data-ttu-id="59f3c-110">Si vous ajoutez une nouvelle écriture file d'attente des travaux que vous voulez planifier, vous devez spécifier des informations sur le type d'objet à exécuter, par exemple un état ou un codeunit et le nom et l'ID de l'objet que vous voulez exécuter.</span><span class="sxs-lookup"><span data-stu-id="59f3c-110">If you add a new job queue entry that you want to schedule, you must specify information about the type of object you want to run, such as a report or codeunit, and the name and object ID of the object that you want to run.</span></span> <span data-ttu-id="59f3c-111">Vous pouvez également ajouter des paramètres pour spécifier le comportement de la file d'attente des travaux.</span><span class="sxs-lookup"><span data-stu-id="59f3c-111">You can also add parameters to specify the behavior of the job queue entry.</span></span> <span data-ttu-id="59f3c-112">Par exemple, vous pouvez ajouter un paramètre pour envoyer uniquement des commandes vente validées.</span><span class="sxs-lookup"><span data-stu-id="59f3c-112">For example, you can add a parameter to only send posted sales orders.</span></span> <span data-ttu-id="59f3c-113">Vous devez être autorisé à exécuter l'état ou le codeunit spécifié, sans quoi une erreur est renvoyée lors de l'exécution de la file projets.</span><span class="sxs-lookup"><span data-stu-id="59f3c-113">You must have permission to run the particular report or codeunit, or an error will be returned when the job queue is run.</span></span>  

<span data-ttu-id="59f3c-114">Une file d'attente des travaux peut comporter plusieurs écritures correspondant aux projets que la file gère et exécute.</span><span class="sxs-lookup"><span data-stu-id="59f3c-114">A job queue can have many entries, which are the jobs that the queue manages and runs.</span></span> <span data-ttu-id="59f3c-115">Les informations contenues dans les écritures spécifient le codeunit ou l'état exécuté, la date et le nombre de fois de l'exécution d'une écriture, la catégorie dans laquelle le projet s'exécute et comment il s'exécute.</span><span class="sxs-lookup"><span data-stu-id="59f3c-115">Information in the entry specifies what codeunit or report is run, when and how often the entry is run, in what category the job runs, and how it runs.</span></span>  

## <a name="to-set-up-background-posting-with-job-queues"></a><span data-ttu-id="59f3c-116">Pour paramétrer la validation en arrière-plan avec les files d'attente des travaux</span><span class="sxs-lookup"><span data-stu-id="59f3c-116">To set up background posting with job queues</span></span>
<span data-ttu-id="59f3c-117">Les files d'attente des travaux sont un outil efficace pour planifier l'exécution des processus d'entreprises en arrière-plan, par exemple lorsque plusieurs utilisateurs essaient de valider des commandes vente, mais uniquement une commande à la fois.</span><span class="sxs-lookup"><span data-stu-id="59f3c-117">Job queues are an effective tool to schedule the running of business processes in the background, such as when multiple users are trying to post sales orders, but only one order can be processed at a time.</span></span> <span data-ttu-id="59f3c-118">Sinon, vous pouvez planifier des validations à des heures pratiques pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="59f3c-118">Alternatively, you may want to schedule postings for hours when it is convenient for your organization.</span></span> <span data-ttu-id="59f3c-119">Par exemple, il peut sembler raisonnable dans votre activité d'exécuter certaines routines lorsque la plupart de la saisie de données de la journée est achevée.</span><span class="sxs-lookup"><span data-stu-id="59f3c-119">For example, it may make sense in your business to run certain routines when most of the data entry for the day has concluded.</span></span>

<span data-ttu-id="59f3c-120">Vous pouvez obtenir cette opération en configurant la file projets pour exécuter différents états de validation par lots, par exemple, **TPL valider commandes vente**, **TPL valider factures vente**, **TPL valider retours vente** et les états **TPL valider avoirs vente**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-120">You can achieve this by setting the job queue up to run various batch-posting reports, such as the **Batch Post Sales Orders**, **Batch Post Sales Invoices**, **Batch Post Sales Return Orders**, and **Batch Post Sales Credit Memos** reports.</span></span> <span data-ttu-id="59f3c-121">Pour plus d'informations, voir [Pour créer une écriture file d'attente des travaux pour la validation de commande vente en arrière-plan](admin-job-queues-schedule-tasks.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).</span><span class="sxs-lookup"><span data-stu-id="59f3c-121">For more information, see [To create a job queue entry for background sales order posting](admin-job-queues-schedule-tasks.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="59f3c-122">prend en charge la validation en arrière-plan de toutes les ventes, achats, et documents service.</span><span class="sxs-lookup"><span data-stu-id="59f3c-122">supports background posting for all sales, purchasing, and service documents.</span></span>

<span data-ttu-id="59f3c-123">La procédure suivante explique comment configurer la validation en arrière-plan des commandes vente.</span><span class="sxs-lookup"><span data-stu-id="59f3c-123">The following procedure explains how to set up background posting of sales orders.</span></span> <span data-ttu-id="59f3c-124">La procédure est identique pour un achat et un service.</span><span class="sxs-lookup"><span data-stu-id="59f3c-124">The steps are similar for purchasing and service.</span></span>  

1. <span data-ttu-id="59f3c-125">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres ventes**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="59f3c-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="59f3c-126">Sur la page **Paramètres ventes**, activez la case à cocher **Valider avec la file d'attente des travaux**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-126">On the **Sales & Receivables Setup** page, choose the **Post with Job Queue** check box.</span></span>
3. <span data-ttu-id="59f3c-127">Pour filtrer les écritures de file d'attente des travaux pour la validation de commandes vente, choisissez le champ **Code catégorie de la file d'attente des travaux**, puis sélectionnez la catégorie **Validvent**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-127">To filter to job queue entries for sales order posting, choose the **Job Queue Category Code** field, and then select the **SalesPost** category.</span></span>

    <span data-ttu-id="59f3c-128">Un objet de file d'attente de travaux, codeunit 88 **Validation des ventes via la file d'attente des travaux**, est créé.</span><span class="sxs-lookup"><span data-stu-id="59f3c-128">A job queue object, codeunit 88 **Sales Post via Job Queue**, is created.</span></span> <span data-ttu-id="59f3c-129">Pour l'activer, passez à la page **Écritures file d'attente des travaux**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-129">Proceed to enable it on the **Job Queue Entries** page.</span></span>
4. <span data-ttu-id="59f3c-130">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Écritures file d'attente des travaux**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="59f3c-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Queue Entries**, and then choose the related link.</span></span>
5. <span data-ttu-id="59f3c-131">Sur la page **Écritures file d'attente des travaux**, choisissez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-131">On the **Job Queue Entries** page, choose the **New** action.</span></span>
6. <span data-ttu-id="59f3c-132">Dans le champ **Type objet à exécuter**, sélectionnez **Codeunit**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-132">In the **Object Type to Run** field, select **Codeunit**.</span></span>  
7. <span data-ttu-id="59f3c-133">Dans le champ **ID objet à exécuter**, sélectionnez 88, **Validation des ventes via la file d'attente des travaux**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-133">In the **Object ID to Run** field, select 88, **Sales Post via Job Queue**.</span></span>

    <span data-ttu-id="59f3c-134">Aucune autre champ n'est valable pour ce scénario.</span><span class="sxs-lookup"><span data-stu-id="59f3c-134">No other fields are relevant for this scenario.</span></span>
8. <span data-ttu-id="59f3c-135">Choisissez l'action **Attribuer le statut Prêt**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-135">Choose the **Set Status to Ready** action.</span></span>
9. <span data-ttu-id="59f3c-136">Pour vérifier que la file d'attente des travaux fonctionne comme prévu, validez une commande vente.</span><span class="sxs-lookup"><span data-stu-id="59f3c-136">To verify that the job queue is working as expected, post a sales order.</span></span> <span data-ttu-id="59f3c-137">Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="59f3c-137">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
10. <span data-ttu-id="59f3c-138">Vérifiez sur la page **Écritures journal file d'attente des travaux** si la commande vente a été validée avec succès.</span><span class="sxs-lookup"><span data-stu-id="59f3c-138">Review on the **Job Queue Log Entries** page if the sales order was posted successfully.</span></span> <span data-ttu-id="59f3c-139">Pour plus d'informations, voir [Pour afficher le statut ou les erreurs dans la fille d'attente](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).</span><span class="sxs-lookup"><span data-stu-id="59f3c-139">For more information, see [To view status or errors in the job queue](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).</span></span>

<span data-ttu-id="59f3c-140">Si vous souhaitez également que des documents vente soient imprimés lorsqu'ils sont validés, sélectionnez la case à cocher **Valider et imprimer avec la file d'attente des travaux** sur la page **Paramètres ventes**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-140">If you also want sales documents to be printed when they are posted, select the **Post & Print with Job Queue** check box on the **Sales & Receivables Setup** page.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="59f3c-141">Si vous paramétrez un projet qui valide et imprime des documents et que l'imprimante affiche une boîte de dialogue, par exemple une demande d'informations d'identification ou un alerte à propos de la quantité faible d'encre, votre document est validé mais non imprimé.</span><span class="sxs-lookup"><span data-stu-id="59f3c-141">If you set up a job that will post and print documents, and the printer displays a dialog box, such as a request for credentials or a warning about low printer ink, your document is posted but not printed.</span></span> <span data-ttu-id="59f3c-142">L'écriture file d'attente de travaux correspondante expire et la valeur du champ **Statut** devient **Erreur**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-142">The corresponding job queue entry eventually times out and the **Status** field is set to **Error**.</span></span> <span data-ttu-id="59f3c-143">Par conséquent, nous vous recommandons de ne pas utiliser une configuration de l'imprimante nécessitant une interaction avec les boîtes de dialogue de l'imprimante relatives à la validation en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="59f3c-143">Accordingly, we recommend that you do not use a printer setup that requires interaction with the display of printer dialog boxes in conjunction with background posting.</span></span>

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a><span data-ttu-id="59f3c-144">Pour créer une écriture file d'attente des travaux pour la validation par lots des commandes vente</span><span class="sxs-lookup"><span data-stu-id="59f3c-144">To create a job queue entry for batch posting of sales orders</span></span>
<span data-ttu-id="59f3c-145">La procédure suivante décrit comment définir le rapport **TPL valider commandes vente** pour une validation automatique des commandes vente lancées à 16 h 00 les jours de semaine.</span><span class="sxs-lookup"><span data-stu-id="59f3c-145">The following procedure shows how to set the **Batch Post Sales Orders** report up to automatically post released sales orders at 4 PM on week days.</span></span>  

1. <span data-ttu-id="59f3c-146">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Écritures file d'attente des travaux**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="59f3c-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Queue Entries**, and then choose the related link.</span></span>  
2. <span data-ttu-id="59f3c-147">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-147">Choose the **New** action.</span></span>  
3. <span data-ttu-id="59f3c-148">Dans le champ **Type objet à exécuter**, sélectionnez **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-148">In the **Object Type to Run** field, select **Report**.</span></span>  
4. <span data-ttu-id="59f3c-149">Dans le champ **ID objet à exécuter**, sélectionnez 296, **TPL valider commandes vente**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-149">In the **Object ID to Run** field, select 296, **Batch Post Sales Orders**.</span></span>
5. <span data-ttu-id="59f3c-150">Activez la case à cocher **Page requête état**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-150">Select the **Report Request Page** check box.</span></span>
6. <span data-ttu-id="59f3c-151">Dans la page de demande **TPL valider commandes vente**, définissez ce qui est inclus lors de la validation automatique des commandes vente, puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-151">In the **Batch Post Sales Orders** request page, define what is included during automatic posting of sales orders, and then choose the **OK** button.</span></span>
7. <span data-ttu-id="59f3c-152">Activez toutes les cases à cocher de **Exécuter le lundi** à **Exécuter le vendredi**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-152">Select all check boxes from **Run on Mondays** through **Run on Fridays**.</span></span>
8. <span data-ttu-id="59f3c-153">Dans le champ **Heure début**, entrez 16 h 00.</span><span class="sxs-lookup"><span data-stu-id="59f3c-153">In the **Starting Time** field, enter 4 PM.</span></span>
9. <span data-ttu-id="59f3c-154">Choisissez l'action **Attribuer le statut Prêt**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-154">Choose the **Set Status to Ready** action.</span></span>

<span data-ttu-id="59f3c-155">Les commandes vente prêtes à la validation sont à présent validées chaque jour de la semaine à 16 h 00.</span><span class="sxs-lookup"><span data-stu-id="59f3c-155">Sales orders that are ready to post will now be posted every week day at 4 PM.</span></span>

> [!NOTE]
> <span data-ttu-id="59f3c-156">Si la file d'attente des travaux ne peut pas valider la commande vente, le statut passe à **Erreur**, et la commande vente est ajoutée à la liste des commandes vente que l'utilisateur doit traiter.</span><span class="sxs-lookup"><span data-stu-id="59f3c-156">If the job queue cannot post the sales order, the status is changed to **Error** and the sales order is added to the list of sales orders that the user must handle manually.</span></span> <span data-ttu-id="59f3c-157">Pour plus d'informations, voir [Pour afficher le statut ou les erreurs dans la fille d'attente](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).</span><span class="sxs-lookup"><span data-stu-id="59f3c-157">For more information, see [To view status or errors in the job queue](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).</span></span>

<span data-ttu-id="59f3c-158">Une fois les files d'attente des travaux configurées et en cours de exécution, le statut est modifié comme suit au cours de chaque période d'abonnement :</span><span class="sxs-lookup"><span data-stu-id="59f3c-158">After job queues are set up and running, the status can change as follows within each recurring period:</span></span>

* <span data-ttu-id="59f3c-159">**En attente**</span><span class="sxs-lookup"><span data-stu-id="59f3c-159">**On Hold**</span></span>  
* <span data-ttu-id="59f3c-160">**Prêt**</span><span class="sxs-lookup"><span data-stu-id="59f3c-160">**Ready**</span></span>  
* <span data-ttu-id="59f3c-161">**En cours**</span><span class="sxs-lookup"><span data-stu-id="59f3c-161">**In Process**</span></span>  
* <span data-ttu-id="59f3c-162">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="59f3c-162">**Error**</span></span>  
* <span data-ttu-id="59f3c-163">**Terminé**</span><span class="sxs-lookup"><span data-stu-id="59f3c-163">**Finished**</span></span>  

<span data-ttu-id="59f3c-164">Une fois qu'un projet s'est terminé correctement, il est supprimé de la liste d'écritures file d'attente des travaux, sauf en cas de projet récurrent.</span><span class="sxs-lookup"><span data-stu-id="59f3c-164">After a job has finished successfully, it is removed from the list of job queue entries unless it is a recurring job.</span></span> <span data-ttu-id="59f3c-165">S'il s'agit d'un projet récurrent, le champ **Heure de début (au plus tôt)** est ajusté pour afficher la prochaine heure d'exécution planifiée pour le projet.</span><span class="sxs-lookup"><span data-stu-id="59f3c-165">If it is a recurring job, the **Earliest Start Time** field is adjusted to show the next time that the job is expected to run.</span></span>  

## <a name="to-view-status-or-errors-in-the-job-queue"></a><span data-ttu-id="59f3c-166">Pour visualiser le statut ou les erreurs dans la file d'attente des travaux</span><span class="sxs-lookup"><span data-stu-id="59f3c-166">To view status or errors in the job queue</span></span>
<span data-ttu-id="59f3c-167">Les données qui sont générées lors de l'exécution d'une file d'attente des travaux sont stockées dans la base de données, de sorte que vous pouvez résoudre les erreurs de la file d'attente des travaux.</span><span class="sxs-lookup"><span data-stu-id="59f3c-167">Data that is generated when a job queue is run is stored in the database, so that you can troubleshoot job queue errors.</span></span>

### <a name="to-view-status-for-any-job"></a><span data-ttu-id="59f3c-168">Pour visualiser le statut de tous les travaux</span><span class="sxs-lookup"><span data-stu-id="59f3c-168">To view status for any job</span></span>
1. <span data-ttu-id="59f3c-169">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Écritures file d'attente des travaux**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="59f3c-169">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Queue Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="59f3c-170">Sur la page **Écritures file d'attente des travaux**, sélectionnez une écriture file d'attente des travaux, puis sélectionnez l'action **Écritures journal**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-170">On the **Job Queue Entries** page, select a job queue entry, and then choose the **Log Entries** action.</span></span>  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a><span data-ttu-id="59f3c-171">Pour afficher un statut dans un document vente ou achat</span><span class="sxs-lookup"><span data-stu-id="59f3c-171">To view status from a sales or purchase document</span></span>
1. <span data-ttu-id="59f3c-172">Dans le document que vous avez essayé de valider avec la file d'attente des travaux, choisissez le champ **Statut de la file d'attente des travaux**, qui contient **Erreur**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-172">From the document that you have tried to post with the job queue, choose the **Job Queue Status** field, which will contain **Error**.</span></span>
2. <span data-ttu-id="59f3c-173">Examinez le message d’erreur et résolvez le problème.</span><span class="sxs-lookup"><span data-stu-id="59f3c-173">Review the error message and fix the problem.</span></span>

## <a name="the-my-job-queue-part"></a><span data-ttu-id="59f3c-174">Composant Ma file d'attente des travaux</span><span class="sxs-lookup"><span data-stu-id="59f3c-174">The My Job Queue Part</span></span>
<span data-ttu-id="59f3c-175">Le composant **Ma file d'attente des travaux** sur votre Tableau de bord répertorie les écritures files d'attente des travaux commencées par vous, mais qui ne sont pas terminées.</span><span class="sxs-lookup"><span data-stu-id="59f3c-175">The **My Job Queue** part on your Role Center shows the job queues entries that you have started, but which are not yet finished.</span></span> <span data-ttu-id="59f3c-176">Par défaut, le composant n'est pas visible et vous devez donc l'ajouter à votre tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="59f3c-176">By default, the part is not visible, so you have to add it to your Role Center.</span></span> <span data-ttu-id="59f3c-177">Pour plus d'informations, voir [Modification des paramètres de base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="59f3c-177">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

<span data-ttu-id="59f3c-178">Le composant indique les documents avec votre ID dans le champ **Code utilisateur affecté** en cours de traitement ou en attente, y compris ceux associés à la validation en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="59f3c-178">The part shows which documents with your ID in the **Assigned User ID** field are being processed or are queued, including those related to background posting.</span></span> <span data-ttu-id="59f3c-179">Le composant peut vous indiquer rapidement s’il y a eu une erreur lors de la validation d’un document ou s’il existe des erreurs dans une écriture de file projet.</span><span class="sxs-lookup"><span data-stu-id="59f3c-179">The part can tell you at a glance whether there has been an error in the posting of a document or if there are errors in a job queue entry.</span></span> <span data-ttu-id="59f3c-180">Il vous permet également d'annuler une validation de document en cas de non exécution.</span><span class="sxs-lookup"><span data-stu-id="59f3c-180">The part also lets you cancel a document posting if it is not running.</span></span>

### <a name="to-view-an-error-from-the-my-job-queue-part"></a><span data-ttu-id="59f3c-181">Pour afficher une erreur dans le composant Ma file d’attente des travaux</span><span class="sxs-lookup"><span data-stu-id="59f3c-181">To view an error from the My Job Queue part</span></span>
1. <span data-ttu-id="59f3c-182">Sur une écriture indiquant le statut **Erreur**, sélectionnez l'action **Afficher erreur**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-182">On an entry with the status **Error**, choose the **Show Error** action.</span></span>
2. <span data-ttu-id="59f3c-183">Examinez le message d’erreur et résolvez le problème.</span><span class="sxs-lookup"><span data-stu-id="59f3c-183">Review the error message and fix the problem.</span></span>

## <a name="security"></a><span data-ttu-id="59f3c-184">Sécurité</span><span class="sxs-lookup"><span data-stu-id="59f3c-184">Security</span></span>  
<span data-ttu-id="59f3c-185">Les écritures file d'attente des travaux s'exécutent sur la base d'autorisations.</span><span class="sxs-lookup"><span data-stu-id="59f3c-185">Job queue entries run based on permissions.</span></span> <span data-ttu-id="59f3c-186">Ces autorisations doivent permettre l'exécution de l'état ou du codeunit.</span><span class="sxs-lookup"><span data-stu-id="59f3c-186">Those permissions must allow the execution of the report or codeunit.</span></span>  

<span data-ttu-id="59f3c-187">Lorsqu'une file d'attente des travaux est activée manuellement, elle s'exécute avec les informations d'identification de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="59f3c-187">When a job queue is activated manually, it is run with the credentials of the user.</span></span> <span data-ttu-id="59f3c-188">Lorsqu'une file d'attente des travaux est activée en tant que tâche planifiée, elle s'exécute avec les informations d'identification de l'instance du serveur.</span><span class="sxs-lookup"><span data-stu-id="59f3c-188">When a job queue is activated as a scheduled task, it is run with the credentials of the server instance.</span></span> <span data-ttu-id="59f3c-189">Un projet s'exécute avec les informations d'identification de la file d'attente des travaux qui l'active.</span><span class="sxs-lookup"><span data-stu-id="59f3c-189">When a job is run, it is run with the credentials of the job queue that activates it.</span></span> <span data-ttu-id="59f3c-190">L'utilisateur qui a créé cette écriture file d'attente des travaux doit toutefois disposer d'autorisations.</span><span class="sxs-lookup"><span data-stu-id="59f3c-190">However, the user who created that job queue entry must also have permissions.</span></span> <span data-ttu-id="59f3c-191">Lorsqu'un projet est exécuté dans la session utilisateur (par exemple, durant la validation en arrière plan), il est exécuté avec les informations d'identification de l'utilisateur qui a créé ce projet.</span><span class="sxs-lookup"><span data-stu-id="59f3c-191">When a job is “run in user session” (such as during background posting), it is run with the credentials of the user who created that job.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="59f3c-192">Si vous utilisez l'ensemble d'autorisations SUPER qui est fourni avec [!INCLUDE[d365fin](includes/d365fin_md.md)], les utilisateurs et vous-même disposez des autorisations pour exécuter tous les objets.</span><span class="sxs-lookup"><span data-stu-id="59f3c-192">If you use the SUPER permissions set that comes with [!INCLUDE[d365fin](includes/d365fin_md.md)], you and your users have permissions to run all objects.</span></span> <span data-ttu-id="59f3c-193">Dans ce cas, l'accès accordé à chaque utilisateur est uniquement limité par les autorisations relatives aux données.</span><span class="sxs-lookup"><span data-stu-id="59f3c-193">In this case, access for each user is only limited by permissions for data.</span></span>  

## <a name="using-job-queues-effectively"></a><span data-ttu-id="59f3c-194">Utilisation efficace des files d'attente des travaux</span><span class="sxs-lookup"><span data-stu-id="59f3c-194">Using Job Queues Effectively</span></span>  
<span data-ttu-id="59f3c-195">L'enregistrement des écritures file d'attente des travaux possède plusieurs champs dont l'objectif est d'exécuter des paramètres dans un codeunit que vous avez indiqué comme devant être exécuté avec une file d'attente des travaux.</span><span class="sxs-lookup"><span data-stu-id="59f3c-195">The job queue entry record has many fields whose purpose is to carry parameters into a codeunit that you have specified to be run with a job queue.</span></span> <span data-ttu-id="59f3c-196">Cela signifie également que les codeunits devant être exécutés via la file d'attente des travaux doivent être indiqués avec l'enregistrement des écritures file d'attente des travaux en tant que paramètre dans le déclencheur **OnRun**.</span><span class="sxs-lookup"><span data-stu-id="59f3c-196">This also means that codeunits that are to be run via the job queue must be specified with the Job Queue Entry record as a parameter in the **OnRun** trigger.</span></span> <span data-ttu-id="59f3c-197">Un niveau de sécurité supplémentaire est ainsi assuré, car les utilisateurs ne peuvent pas exécuter de codeunits aléatoires via la file d'attente des travaux.</span><span class="sxs-lookup"><span data-stu-id="59f3c-197">This helps provide an extra level of security, as this prevents users from running random codeunits via the job queue.</span></span> <span data-ttu-id="59f3c-198">Si l'utilisateur doit transmettre des paramètres à un état, il n'a d'autre choix que celui d'inclure l'exécution de l'état dans un codeunit, lequel analyse ensuite les paramètres d'entrée et les intègre dans l'état avant de l'exécuter.</span><span class="sxs-lookup"><span data-stu-id="59f3c-198">If the user must pass parameters to a report, the only way to do this is by wrapping the report execution into a codeunit, which then parses the input parameters and enters them into the report before executing it.</span></span>  

## <a name="see-also"></a><span data-ttu-id="59f3c-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59f3c-199">See Also</span></span>  
[<span data-ttu-id="59f3c-200">Administration</span><span class="sxs-lookup"><span data-stu-id="59f3c-200">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="59f3c-201">Configuration de Business Central</span><span class="sxs-lookup"><span data-stu-id="59f3c-201">Setting Up Business Central</span></span>](setup.md)  
[<span data-ttu-id="59f3c-202">Modification des paramètres de base</span><span class="sxs-lookup"><span data-stu-id="59f3c-202">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  