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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3e972ae6532c9531845e2739237b6ccb94d14c12
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="delete-workflows"></a><span data-ttu-id="62fb9-104">Supprimer des workflows</span><span class="sxs-lookup"><span data-stu-id="62fb9-104">Delete Workflows</span></span>
<span data-ttu-id="62fb9-105">Si vous êtes certain qu'un workflow n'est plus utilisé, vous pouvez le supprimer.</span><span class="sxs-lookup"><span data-stu-id="62fb9-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="62fb9-106">Toutes les instances d'étape de workflow définies dans le workflow doivent avoir le statut **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="62fb9-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="62fb9-107">Lorsque vous supprimez un workflow, toutes les informations contenues dans le workflow seront perdues.</span><span class="sxs-lookup"><span data-stu-id="62fb9-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="62fb9-108">Dans la fenêtre **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes.</span><span class="sxs-lookup"><span data-stu-id="62fb9-108">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="62fb9-109">Chaque étape comprend un événement de workflow modéré par des conditions d'événement, et une réponse de workflow modérée par des options de réponse.</span><span class="sxs-lookup"><span data-stu-id="62fb9-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="62fb9-110">Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application.</span><span class="sxs-lookup"><span data-stu-id="62fb9-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="62fb9-111">Pour plus d'informations, voir [Créer des flux de travail](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="62fb9-111">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="62fb9-112">Pour supprimer un workflow</span><span class="sxs-lookup"><span data-stu-id="62fb9-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="62fb9-113">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Flux de travail**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="62fb9-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="62fb9-114">Sélectionnez le workflow à supprimer.</span><span class="sxs-lookup"><span data-stu-id="62fb9-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="62fb9-115">Cliquez sur l'action **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="62fb9-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="62fb9-116">Sinon, ouvrez le workflow à supprimer.</span><span class="sxs-lookup"><span data-stu-id="62fb9-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="62fb9-117">Dans la fenêtre **Workflow**, sélectionnez l'action **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="62fb9-117">In the **Workflow** window, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="62fb9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62fb9-118">See Also</span></span>  
 <span data-ttu-id="62fb9-119">[Créer des workflows](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="62fb9-119">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="62fb9-120">[Activer des workflows](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="62fb9-120">[Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="62fb9-121">[Afficher des instances d'étape de workflow archivées](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="62fb9-121">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="62fb9-122">[Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="62fb9-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="62fb9-123">[Paramétrage des workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="62fb9-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="62fb9-124">[Utilisation des workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="62fb9-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="62fb9-125">Flux de travail</span><span class="sxs-lookup"><span data-stu-id="62fb9-125">Workflow</span></span>](across-workflow.md)   

