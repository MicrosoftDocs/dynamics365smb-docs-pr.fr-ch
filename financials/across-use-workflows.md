---
title: Utilisation des workflows | Microsoft Docs
description: "Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a42e336dba385cbf24c19702ad64d76b26c15104
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="using-workflows"></a><span data-ttu-id="07b6f-105">Utilisation des workflows</span><span class="sxs-lookup"><span data-stu-id="07b6f-105">Using Workflows</span></span>
<span data-ttu-id="07b6f-106">Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="07b6f-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="07b6f-107">Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="07b6f-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="07b6f-108">Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow.</span><span class="sxs-lookup"><span data-stu-id="07b6f-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="07b6f-109">Avant de pouvoir commencer à utiliser des workflows, vous devez configurer des utilisateurs de workflow, créer les workflows, potentiellement précédés d'une personnalisation de code et spécifier la manière dont les utilisateurs reçoivent les notifications.</span><span class="sxs-lookup"><span data-stu-id="07b6f-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="07b6f-110">Pour plus d'informations, reportez-vous à [Paramétrage des workflows](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="07b6f-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="07b6f-111">Les étapes d'un workflow traitent en général des utilisateurs qui demandent l'approbation des tâches et des approbateurs qui acceptent ou rejettent les demandes d'approbations.</span><span class="sxs-lookup"><span data-stu-id="07b6f-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="07b6f-112">Par conséquent, la plupart des rubriques sur l'utilisation des workflows concernent les approbations.</span><span class="sxs-lookup"><span data-stu-id="07b6f-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="07b6f-113">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="07b6f-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="07b6f-114">**Pour**</span><span class="sxs-lookup"><span data-stu-id="07b6f-114">**To**</span></span>|<span data-ttu-id="07b6f-115">**Voir**</span><span class="sxs-lookup"><span data-stu-id="07b6f-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="07b6f-116">Définissez un workflow pour démarrer lorsque le premier événement de point d'entrée se produit.</span><span class="sxs-lookup"><span data-stu-id="07b6f-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="07b6f-117">Procédure : Activer des workflows</span><span class="sxs-lookup"><span data-stu-id="07b6f-117">How to: Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="07b6f-118">Demander l'approbation d'une tâche, en tant qu'approbateur, accepter, décliner ou déléguer des approbations, et envoyer ou afficher des notifications d'approbation.</span><span class="sxs-lookup"><span data-stu-id="07b6f-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="07b6f-119">Procédure : utilisation des flux d'approbation</span><span class="sxs-lookup"><span data-stu-id="07b6f-119">How to: Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="07b6f-120">Créez des étapes de workflow qui limitent l'utilisation d'un certain type d'enregistrement avant qu'un certain événement ne se produise, par exemple que l'enregistrement est approuvé.</span><span class="sxs-lookup"><span data-stu-id="07b6f-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="07b6f-121">Procédure : restreindre et autoriser l'utilisation d'un enregistrement</span><span class="sxs-lookup"><span data-stu-id="07b6f-121">How to: Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="07b6f-122">Affichez les instances d'étape du workflow dont le statut est Terminé.</span><span class="sxs-lookup"><span data-stu-id="07b6f-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="07b6f-123">Procédure : afficher des instances d'étape de workflow archivées</span><span class="sxs-lookup"><span data-stu-id="07b6f-123">How to: View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="07b6f-124">Supprimez un workflow que vous êtes sûr de ne plus utiliser.</span><span class="sxs-lookup"><span data-stu-id="07b6f-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="07b6f-125">Procédure : supprimer des workflows</span><span class="sxs-lookup"><span data-stu-id="07b6f-125">How to: Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="07b6f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07b6f-126">See Also</span></span>  
<span data-ttu-id="07b6f-127">[Paramétrage des workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="07b6f-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="07b6f-128">[Flux de travail](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="07b6f-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="07b6f-129">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="07b6f-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

