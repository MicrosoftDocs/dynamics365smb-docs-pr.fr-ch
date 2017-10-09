---
title: "Procédure : supprimer des workflows | Microsoft Docs"
description: "Si vous êtes certain qu'un workflow n'est plus utilisé, vous pouvez le supprimer. Toutes les instances d'étape de workflow définies dans le workflow doivent avoir le statut **Terminé**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d1b7b29735983e2de0bdaf5d382679d9546a6278
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-delete-workflows"></a><span data-ttu-id="36560-104">Procédure : supprimer des workflows</span><span class="sxs-lookup"><span data-stu-id="36560-104">How to: Delete Workflows</span></span>
<span data-ttu-id="36560-105">Si vous êtes certain qu'un workflow n'est plus utilisé, vous pouvez le supprimer.</span><span class="sxs-lookup"><span data-stu-id="36560-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="36560-106">Toutes les instances d'étape de workflow définies dans le workflow doivent avoir le statut **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="36560-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="36560-107">Lorsque vous supprimez un workflow, toutes les informations contenues dans le workflow seront perdues.</span><span class="sxs-lookup"><span data-stu-id="36560-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="36560-108">Dans la fenêtre **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes.</span><span class="sxs-lookup"><span data-stu-id="36560-108">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="36560-109">Chaque étape comprend un événement de workflow modéré par des conditions d'événement, et une réponse de workflow modérée par des options de réponse.</span><span class="sxs-lookup"><span data-stu-id="36560-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="36560-110">Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application.</span><span class="sxs-lookup"><span data-stu-id="36560-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="36560-111">Pour plus d'informations, reportez\-vous à [Procédure : créer des flux de travail](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="36560-111">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="36560-112">Pour supprimer un workflow</span><span class="sxs-lookup"><span data-stu-id="36560-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="36560-113">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Flux de travail**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="36560-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="36560-114">Sélectionnez le workflow à supprimer.</span><span class="sxs-lookup"><span data-stu-id="36560-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="36560-115">Cliquez sur l'action **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="36560-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="36560-116">Sinon, ouvrez le workflow à supprimer.</span><span class="sxs-lookup"><span data-stu-id="36560-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="36560-117">Dans la fenêtre **Workflow**, sélectionnez l'action **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="36560-117">In the **Workflow** window, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="36560-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36560-118">See Also</span></span>  
 <span data-ttu-id="36560-119">[Procédure : créer des workflows](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="36560-119">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="36560-120">[Procédure : Activer des workflows](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="36560-120">[How to: Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="36560-121">[Procédure : afficher des instances d'étape de workflow archivées](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="36560-121">[How to: View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="36560-122">[Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="36560-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="36560-123">[Paramétrage des workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="36560-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="36560-124">[Utilisation des workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="36560-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="36560-125">Flux de travail</span><span class="sxs-lookup"><span data-stu-id="36560-125">Workflow</span></span>](across-workflow.md)   

