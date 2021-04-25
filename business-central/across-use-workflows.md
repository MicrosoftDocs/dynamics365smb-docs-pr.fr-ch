---
title: Utilisation des workflows
description: Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Découvrez les différentes étapes à suivre pour commencer à utiliser les workflows.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 92b32957bb7b20dda304be8a99bb17c5c5947498
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787022"
---
# <a name="using-workflows"></a><span data-ttu-id="e723e-104">Utilisation des workflows</span><span class="sxs-lookup"><span data-stu-id="e723e-104">Using Workflows</span></span>
<span data-ttu-id="e723e-105">Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e723e-105">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="e723e-106">Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e723e-106">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="e723e-107">Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow.</span><span class="sxs-lookup"><span data-stu-id="e723e-107">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="e723e-108">Avant de pouvoir commencer à utiliser des workflows, vous devez configurer des utilisateurs de workflow, créer les workflows, potentiellement précédés d’une personnalisation de code et spécifier la manière dont les utilisateurs reçoivent les notifications.</span><span class="sxs-lookup"><span data-stu-id="e723e-108">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="e723e-109">Pour plus d’informations, reportez-vous à [Paramétrage des workflows](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="e723e-109">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e723e-110">Les étapes d’un workflow traitent en général des utilisateurs qui demandent l’approbation des tâches et des approbateurs qui acceptent ou rejettent les demandes d’approbations.</span><span class="sxs-lookup"><span data-stu-id="e723e-110">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="e723e-111">Par conséquent, la plupart des rubriques sur l’utilisation des workflows concernent les approbations.</span><span class="sxs-lookup"><span data-stu-id="e723e-111">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="e723e-112">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="e723e-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="e723e-113">**Pour**</span><span class="sxs-lookup"><span data-stu-id="e723e-113">**To**</span></span>|<span data-ttu-id="e723e-114">**Voir**</span><span class="sxs-lookup"><span data-stu-id="e723e-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="e723e-115">Définissez un workflow pour démarrer lorsque le premier événement de point d’entrée se produit.</span><span class="sxs-lookup"><span data-stu-id="e723e-115">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="e723e-116">Activer des workflows</span><span class="sxs-lookup"><span data-stu-id="e723e-116">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="e723e-117">Demander l’approbation d’une tâche, en tant qu’approbateur, accepter, décliner ou déléguer des approbations, et envoyer ou afficher des notifications d’approbation.</span><span class="sxs-lookup"><span data-stu-id="e723e-117">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="e723e-118">Utilisation des flux d’approbation</span><span class="sxs-lookup"><span data-stu-id="e723e-118">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="e723e-119">Créez des étapes de workflow qui limitent l’utilisation d’un certain type d’enregistrement avant qu’un certain événement ne se produise, par exemple que l’enregistrement est approuvé.</span><span class="sxs-lookup"><span data-stu-id="e723e-119">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="e723e-120">Restreindre et autoriser l’utilisation d’un enregistrement</span><span class="sxs-lookup"><span data-stu-id="e723e-120">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="e723e-121">Affichez les instances d’étape du workflow dont le statut est Terminé.</span><span class="sxs-lookup"><span data-stu-id="e723e-121">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="e723e-122">Afficher des instances d’étape de workflow archivées</span><span class="sxs-lookup"><span data-stu-id="e723e-122">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="e723e-123">Supprimez un workflow que vous êtes sûr de ne plus utiliser.</span><span class="sxs-lookup"><span data-stu-id="e723e-123">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="e723e-124">Supprimer des workflows</span><span class="sxs-lookup"><span data-stu-id="e723e-124">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="e723e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e723e-125">See Also</span></span>  
<span data-ttu-id="e723e-126">[Paramétrage des workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e723e-126">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="e723e-127">[Flux de travail](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="e723e-127">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="e723e-128">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e723e-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]