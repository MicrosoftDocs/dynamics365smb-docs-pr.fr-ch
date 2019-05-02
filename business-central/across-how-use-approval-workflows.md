---
title: Approuver ou rejeter des documents dans les flux| Microsoft Docs
description: Demander, rejeter, ou déléguer une approbation de, par exemple, un document achat ou vente, dans le cadre d'un flux de travail.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 3b4b4a6d544b594f439b675b88176d942d8cf325
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821086"
---
# <a name="use-approval-workflows"></a><span data-ttu-id="8b85d-103">Utilisation des flux d'approbation</span><span class="sxs-lookup"><span data-stu-id="8b85d-103">Use Approval Workflows</span></span>
<span data-ttu-id="8b85d-104">Lorsqu'un enregistrement, tel qu'un document achat ou une fiche client, doit être approuvé par un membre de votre organisation, vous envoyez une approbation demande achat dans le cadre d'un workflow.</span><span class="sxs-lookup"><span data-stu-id="8b85d-104">When a record, such as a purchase document or a customer card, needs to be approved by someone in your organization, you send an approval request as part of a workflow.</span></span> <span data-ttu-id="8b85d-105">Selon la configuration du workflow, l'approbateur approprié est informé que l'enregistrement requiert son approbation.</span><span class="sxs-lookup"><span data-stu-id="8b85d-105">Based on how the workflow is set up, the appropriate approver is then notified that the record requires their approval.</span></span>

<span data-ttu-id="8b85d-106">Vous configurez les flux d'approbation sur la page **Flux de travail**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-106">You set up approval workflows on the **Workflow** page.</span></span> <span data-ttu-id="8b85d-107">Pour plus d'informations, reportez-vous à [Paramétrage des workflows](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="8b85d-107">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>

<span data-ttu-id="8b85d-108">Outre les flux de travail approbation décrits dans cette rubrique, vous pouvez effectuer diverses autres tâches de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="8b85d-108">In addition to approval workflows described in this topic, you can perform various other workflow tasks.</span></span> <span data-ttu-id="8b85d-109">Pour plus d'informations, voir [Utilisation des workflows](across-use-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="8b85d-109">For more information, [Using Workflows](across-use-workflows.md).</span></span>

<span data-ttu-id="8b85d-110">Les flux d'approbation de base pour les documents achat, les documents vente, les feuilles paiement, les fiches client et les fiches article sont prêts à être utilisés dans le cadre de la configuration assistée.</span><span class="sxs-lookup"><span data-stu-id="8b85d-110">Core approval workflows for purchases documents, sales documents, payment journals, customer cards, and item cards are ready to start as assisted setup.</span></span> <span data-ttu-id="8b85d-111">Pour plus d'informations, reportez-vous à [Mise en route](product-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="8b85d-111">For more information, see [Getting Started](product-get-started.md).</span></span>

## <a name="to-request-approval-of-a-record"></a><span data-ttu-id="8b85d-112">Faire une demande d'approbation d'un enregistrement</span><span class="sxs-lookup"><span data-stu-id="8b85d-112">To request approval of a record</span></span>
<span data-ttu-id="8b85d-113">La tâche suivante est effectuée par un utilisateur d'approbation.</span><span class="sxs-lookup"><span data-stu-id="8b85d-113">The following task is performed by an approval user.</span></span>

1. <span data-ttu-id="8b85d-114">Sur la page qui affiche l'enregistrement, sélectionnez l'action **Envoyer demande d'approbation**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-114">on the page that presents the record, choose the **Send Approval Request** action.</span></span>
2. <span data-ttu-id="8b85d-115">Pour afficher toutes vos demandes d'approbation, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Écritures demande d'approbation**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="8b85d-115">To see all your approval requests, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Approval Request Entries**, and then choose the related link.</span></span>  

<span data-ttu-id="8b85d-116">Le statut de l’écriture approbation passe de **Créé** à **Ouvert**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-116">The status of the approval entry is updated from **Created** to **Open**.</span></span> <span data-ttu-id="8b85d-117">Le statut de l'enregistrement, par exemple une facture achat, est mis à jour du statut **Ouvert** à **Approbation en attente** et reste verrouillé au traitement jusqu'à ce que tous les approbateurs aient approuvé l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8b85d-117">The status of the record, for example a purchase invoice, is updated from **Open** to **Pending Approval** and remains locked for processing until all approvers have approved the record.</span></span>

<span data-ttu-id="8b85d-118">Lorsque l'approbateur a approuvé l'enregistrement, le statut passe à **Validé**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-118">When the approver has approved the record, the status changes to **Released**.</span></span> <span data-ttu-id="8b85d-119">Vous pouvez ensuite effectuer vos tâches avec l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8b85d-119">You can then continue your tasks with the record.</span></span>

## <a name="to-cancel-requests-for-approval"></a><span data-ttu-id="8b85d-120">Pour annuler des demandes d'approbation</span><span class="sxs-lookup"><span data-stu-id="8b85d-120">To cancel requests for approval</span></span>
<span data-ttu-id="8b85d-121">La tâche suivante est effectuée par un utilisateur d'approbation doté de droits d'approbation.</span><span class="sxs-lookup"><span data-stu-id="8b85d-121">The following task is performed by an approval user with approver rights.</span></span>

<span data-ttu-id="8b85d-122">Un client peut souhaiter modifier une commande après sa soumission pour approbation.</span><span class="sxs-lookup"><span data-stu-id="8b85d-122">A customer may want to change an order after it has been submitted for approval.</span></span> <span data-ttu-id="8b85d-123">Dans ce cas, vous pouvez annuler le processus d'approbation et apporter les modifications nécessaires à la commande avant de refaire une demande d'approbation.</span><span class="sxs-lookup"><span data-stu-id="8b85d-123">In this case, you can cancel the approval process and make the necessary changes to the order before you request approval again.</span></span>

- <span data-ttu-id="8b85d-124">Sur la page qui affiche l'enregistrement, sélectionnez l'action **Annuler demande d'approbation**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-124">on the page that displays the record, choose the **Cancel Approval Request** action.</span></span>

<span data-ttu-id="8b85d-125">Lorsque la demande d'approbation a été annulée, le statut de l'écriture de l'approbation connexe passe à **Annulé**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-125">When the approval request has been canceled, the status of the related approval entry is changed to **Canceled**.</span></span> <span data-ttu-id="8b85d-126">Le statut de l’enregistrement est mis à jour d'**Approbation en attente** à **Ouvert**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-126">The status of the record is updated from **Pending Approval** to **Open**.</span></span> <span data-ttu-id="8b85d-127">Le processus d'approbation peut alors redémarrer.</span><span class="sxs-lookup"><span data-stu-id="8b85d-127">The approval process can then start again.</span></span>

## <a name="to-approve-or-reject-requests-for-approval"></a><span data-ttu-id="8b85d-128">Pour approuver ou rejeter les demandes d'approbation</span><span class="sxs-lookup"><span data-stu-id="8b85d-128">To approve or reject requests for approval</span></span>
<span data-ttu-id="8b85d-129">La tâche suivante est effectuée par un utilisateur d'approbation doté de droits d'approbation.</span><span class="sxs-lookup"><span data-stu-id="8b85d-129">The following task is performed by an approval user with approver rights.</span></span>

<span data-ttu-id="8b85d-130">Vous pouvez traiter les demandes d'approbation sur la page **Demandes à approuver**, par exemple, afin d'approuver plusieurs demandes à la fois.</span><span class="sxs-lookup"><span data-stu-id="8b85d-130">You can process approval requests on the **Requests to Approve** page, for example to approve multiple requests at a time.</span></span> <span data-ttu-id="8b85d-131">Sinon, vous pouvez traiter chaque demande sur l'enregistrement connexe, par exemple la page **Facture achat**, en sélectionnant le lien dans la notification que vous recevez.</span><span class="sxs-lookup"><span data-stu-id="8b85d-131">Alternatively, you can process each request on the related record, such as the **Purchase Invoice** page, by choosing the link in the notification that you receive.</span></span>

1. <span data-ttu-id="8b85d-132">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Demandes à approuver**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="8b85d-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requests to Approve**, and then choose the related link.</span></span>
2. <span data-ttu-id="8b85d-133">Sélectionnez une ou plusieurs lignes pour l'enregistrement ou les enregistrements que vous voulez approuver ou rejeter.</span><span class="sxs-lookup"><span data-stu-id="8b85d-133">Select one or more lines for the record or records that you want to approve or reject.</span></span>
3. <span data-ttu-id="8b85d-134">Choisissez l'action **Approuver**, **Rejeter** ou **Déléguer**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-134">Choose the **Approve**, **Reject**, or **Delegate** actions.</span></span>

<span data-ttu-id="8b85d-135">Lorsqu'un enregistrement a été approuvé ou rejeté, le statut d'approbation dans le champ **Statut** passe à **Approuvé** ou **Rejeté**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-135">When a record has been approved or rejected, the approval status in the **Status** field changes to **Approved** or **Rejected**.</span></span>

<span data-ttu-id="8b85d-136">Si une hiérarchie d'approbateurs est configurée, le statut enregistrement sera **Approbation en attente** jusqu'à ce que tous les approbateurs aient approuvé l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8b85d-136">If an approver hierarchy is set up, the record status will be **Pending Approval** until all approvers have approved the record.</span></span> <span data-ttu-id="8b85d-137">Le statut de l'enregistrement passe à **Validé**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-137">Then the record status will change to **Released**.</span></span>

<span data-ttu-id="8b85d-138">Simultanément, le statut d'approbation passe de **Créé** à **Ouvert** dès qu'une demande d'approbation est créée pour l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8b85d-138">At the same time, the approval status changes from **Created** to **Open** as soon as an approval request for the record is created.</span></span> <span data-ttu-id="8b85d-139">Si la demande est rejetée, le statut d'approbation passe à **Rejeté**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-139">If the request is rejected, the approval status changes to **Rejected**.</span></span> <span data-ttu-id="8b85d-140">Le statut reste sur **Ouvert** ou **Rejeté** jusqu'à ce que tous les approbateurs aient approuvé la demande.</span><span class="sxs-lookup"><span data-stu-id="8b85d-140">The status remains **Open** or **Rejected** until all approvers have approved the request.</span></span>

## <a name="to-delegate-requests-for-approval"></a><span data-ttu-id="8b85d-141">Pour déléguer des demandes d'approbation</span><span class="sxs-lookup"><span data-stu-id="8b85d-141">To delegate requests for approval</span></span>
<span data-ttu-id="8b85d-142">La tâche suivante est effectuée par un utilisateur d'approbation doté de droits d'approbation.</span><span class="sxs-lookup"><span data-stu-id="8b85d-142">The following task is performed by an approval user with approver rights.</span></span>

<span data-ttu-id="8b85d-143">Pour éviter que des documents ne s'accumulent ou encore bloquent le workflow, l'approbateur et l'administrateur d'approbation peuvent déléguer une demande d'approbation à un approbateur remplaçant.</span><span class="sxs-lookup"><span data-stu-id="8b85d-143">To prevent documents from piling up or otherwise block the workflow, the approver and the approval administrator can delegate an approval request to a substitute approver.</span></span> <span data-ttu-id="8b85d-144">Le remplaçant peut être soit un remplaçant désigné, l'approbateur direct, soit l'administrateur d'approbation, dans cet ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="8b85d-144">The substitute can either be a designated substitute, the direct approver, or the approval administrator, in that order of priority.</span></span> <span data-ttu-id="8b85d-145">Généralement, cette fonction est utilisée si un approbateur est absent et dans l'impossibilité d'approuver des demandes avant la date d'échéance.</span><span class="sxs-lookup"><span data-stu-id="8b85d-145">You typically use this feature if an approver is out of office and is unable to approve requests before the due date.</span></span>

1. <span data-ttu-id="8b85d-146">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Demandes à approuver**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="8b85d-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requests to Approve**, and then choose the related link.</span></span>
2. <span data-ttu-id="8b85d-147">Sélectionnez une ou plusieurs lignes pour les demandes d'approbation à déléguer à un approbateur remplaçant, puis sélectionnez l'action **Déléguer**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-147">Select one or more lines for the approval requests that you want to delegate to a substitute approver, and then choose the **Delegate** action.</span></span>

<span data-ttu-id="8b85d-148">Une notification pour approuver la demande est envoyée à l'approbateur remplaçant.</span><span class="sxs-lookup"><span data-stu-id="8b85d-148">A notification to approve the request is sent to the substitute approver.</span></span>

## <a name="to-manage-overdue-approval-requests"></a><span data-ttu-id="8b85d-149">Pour gérer des demandes d'approbation échues</span><span class="sxs-lookup"><span data-stu-id="8b85d-149">To manage overdue approval requests</span></span>
<span data-ttu-id="8b85d-150">La tâche suivante est effectuée par un utilisateur d'approbation doté de droits d'approbation.</span><span class="sxs-lookup"><span data-stu-id="8b85d-150">The following task is performed by an approval user with approver rights.</span></span>

<span data-ttu-id="8b85d-151">Vous devez rappeler régulièrement aux utilisateurs du workflow d'approbation qu'ils doivent répondre aux demandes d'approbations échues.</span><span class="sxs-lookup"><span data-stu-id="8b85d-151">At regular intervals, you must remind approval workflow users of overdue approval requests that they must react on.</span></span> <span data-ttu-id="8b85d-152">Pour cela, utilisez la fonction **Envoyer des notifications d'approbations échues**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-152">You use the **Send Overdue Approval Notifications** function for this.</span></span>

<span data-ttu-id="8b85d-153">La fonction **Envoyer des notifications d'approbations échues** passe en revue toutes les demandes d'approbation ouvertes qui sont actuellement échues.</span><span class="sxs-lookup"><span data-stu-id="8b85d-153">The **Send Overdue Approval Notifications** function checks for all open approval requests that are currently overdue.</span></span> <span data-ttu-id="8b85d-154">Chaque approbateur ayant au moins une écriture approbation échue reçoit une notification avec la liste de toutes leurs demandes d'approbation échues.</span><span class="sxs-lookup"><span data-stu-id="8b85d-154">Each approver that has at least one overdue approval entry receives a notification with the list of all their overdue approval requests.</span></span> <span data-ttu-id="8b85d-155">La notification est également envoyée à leur approbateur et à tous les demandeurs des approbations échues.</span><span class="sxs-lookup"><span data-stu-id="8b85d-155">The notification is also sent to their approver and all the requesters of the overdue approvals.</span></span> <span data-ttu-id="8b85d-156">Cela est utile si l'écriture d'approbation échue doit être déléguée à un remplaçant.</span><span class="sxs-lookup"><span data-stu-id="8b85d-156">This helps if the overdue approval entry must be delegated to a substitute.</span></span>

1. <span data-ttu-id="8b85d-157">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Demandes approbation échues**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="8b85d-157">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Overdue Approval Requests**, and then choose the related link.</span></span>
2. <span data-ttu-id="8b85d-158">Sur la page **Demandes approbations échues**, sélectionnez l'action **Envoyer les notifications d'approbation échues**.</span><span class="sxs-lookup"><span data-stu-id="8b85d-158">On the **Overdue Approval Requests** page, choose the **Send Overdue Approval Notifications** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b85d-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b85d-159">See Also</span></span>
<span data-ttu-id="8b85d-160">[Ventes](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="8b85d-160">[Sales](sales-manage-sales.md)  </span></span>  
[<span data-ttu-id="8b85d-161">Documents entrants</span><span class="sxs-lookup"><span data-stu-id="8b85d-161">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="8b85d-162">Achats</span><span class="sxs-lookup"><span data-stu-id="8b85d-162">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8b85d-163">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8b85d-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>