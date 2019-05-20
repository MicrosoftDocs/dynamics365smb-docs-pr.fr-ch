---
title: 'Procédure : exporter et importer des flux de travail | Microsoft Docs'
description: Pour transférer des workflows vers d'autres bases de données Business Central, par exemple pour gagner du temps lors de la création de workflows, vous pouvez exporter et importer des workflows.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 046bdd181d6673338813cbc0c4ea4b570c7a4cd3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245610"
---
# <a name="export-and-import-workflows"></a><span data-ttu-id="d6ab5-103">Exporter et importer des workflows</span><span class="sxs-lookup"><span data-stu-id="d6ab5-103">Export and Import Workflows</span></span>
<span data-ttu-id="d6ab5-104">Pour transférer des workflows vers d'autres bases de données [!INCLUDE[d365fin](includes/d365fin_md.md)], par exemple pour gagner du temps lors de la création de workflows, vous pouvez exporter et importer des workflows.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="d6ab5-105">Un autre moyen rapide de créer des workflows consiste à les créer à partir de modèles de workflow.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="d6ab5-106">Pour plus d'informations, reportez-vous à la rubrique [Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="d6ab5-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="d6ab5-107">Sur la page **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-107">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="d6ab5-108">Chaque étape comprend un événement de workflow modéré par des conditions d'événement, et une réponse de workflow modérée par des options de réponse.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="d6ab5-109">Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="d6ab5-110">Pour plus d'informations, voir [Créer des flux de travail](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="d6ab5-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="d6ab5-111">Pour exporter un workflow</span><span class="sxs-lookup"><span data-stu-id="d6ab5-111">To export a workflow</span></span>  
1.  <span data-ttu-id="d6ab5-112">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Flux de travail**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d6ab5-113">Sélectionnez un flux de travail, puis sélectionnez l'action **Exporter vers un fichier**.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="d6ab5-114">Sur la page **Exporter fichier**, cliquez sur le bouton **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-114">On the **Export File** page, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="d6ab5-115">Sur la page **Exporter**, sélectionnez un emplacement de fichier, puis choisissez le bouton **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-115">On the **Export** page, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="d6ab5-116">Pour importer un workflow</span><span class="sxs-lookup"><span data-stu-id="d6ab5-116">To import a workflow</span></span>  
1.  <span data-ttu-id="d6ab5-117">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Flux de travail**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d6ab5-118">Choisissez l'action **Importer à partir d'un fichier**.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="d6ab5-119">Sur la page **Importer**, sélectionnez le fichier XML contenant le flux de travail, puis choisissez le bouton **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-119">On the **Import** page, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="d6ab5-120">Si le code du workflow existe déjà dans la base de données, les étapes du workflow sont remplacées avec celles du workflow importé.</span><span class="sxs-lookup"><span data-stu-id="d6ab5-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d6ab5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6ab5-121">See Also</span></span>  
 <span data-ttu-id="d6ab5-122">[Créer des workflows](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d6ab5-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="d6ab5-123">[Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="d6ab5-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="d6ab5-124">[Afficher des instances d'étape de workflow archivées](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="d6ab5-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="d6ab5-125">[Supprimer des workflows](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d6ab5-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="d6ab5-126">[Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="d6ab5-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="d6ab5-127">[Paramétrage des workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d6ab5-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="d6ab5-128">[Utilisation des workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d6ab5-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="d6ab5-129">Flux de travail</span><span class="sxs-lookup"><span data-stu-id="d6ab5-129">Workflow</span></span>](across-workflow.md)   
