---
title: 'Procédure : créer des flux de travail à partir de modèles de flux de travail | Microsoft Docs'
description: Pour gagner du temps lors de la création de workflows, vous pouvez créer des workflows à partir de modèles de workflow existants.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 6b4d09ae0bd0f2def940e2516bdc54bc04f300ca
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188411"
---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="ce009-103">Créer des flux de travail à partir de modèles de flux de travail</span><span class="sxs-lookup"><span data-stu-id="ce009-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="ce009-104">Pour gagner du temps lors de la création de workflows, vous pouvez créer des workflows à partir de modèles de workflow existants.</span><span class="sxs-lookup"><span data-stu-id="ce009-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="ce009-105">Les modèles de workflow sont des workflows non modifiables qui existent dans la version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ce009-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ce009-106">Les codes des modèles de workflow ajoutés par Microsoft ont le préfixe « MS- ».</span><span class="sxs-lookup"><span data-stu-id="ce009-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="ce009-107">Un autre moyen rapide de créer un workflow consiste à importer un workflow existant qui est stocké dans un fichier en dehors de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ce009-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ce009-108">Pour plus d'informations, voir [Exporter et importer des flux de travail](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="ce009-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="ce009-109">Sur la page **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes.</span><span class="sxs-lookup"><span data-stu-id="ce009-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="ce009-110">Chaque étape comprend un événement de workflow modéré par des conditions d'événement, et une réponse de workflow modérée par des options de réponse.</span><span class="sxs-lookup"><span data-stu-id="ce009-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="ce009-111">Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application.</span><span class="sxs-lookup"><span data-stu-id="ce009-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="ce009-112">Pour plus d'informations, voir [Créer des flux de travail](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="ce009-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="ce009-113">Pour créer un workflow à partir d'un modèle de workflow</span><span class="sxs-lookup"><span data-stu-id="ce009-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="ce009-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Flux de travail**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="ce009-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ce009-115">Choisissez l'action **Créer le flux de travail à partir du modèle**.</span><span class="sxs-lookup"><span data-stu-id="ce009-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="ce009-116">La page **Modèles flux de travail** s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="ce009-116">The **Workflow Templates** page opens.</span></span>  
3.  <span data-ttu-id="ce009-117">Sélectionnez un modèle de workflow et cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce009-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="ce009-118">La page **Flux de travail** s'ouvre pour un nouveau flux de travail contenant toutes les informations du modèle sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ce009-118">The **Workflow** page opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="ce009-119">La valeur du champ **Code** est étendue avec « -01 », par exemple, pour indiquer que ce premier workflow est créé à partir du modèle de workflow.</span><span class="sxs-lookup"><span data-stu-id="ce009-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="ce009-120">Créez ensuite le workflow en modifiant les étapes de workflow ou en ajoutant de nouvelles étapes.</span><span class="sxs-lookup"><span data-stu-id="ce009-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="ce009-121">Pour plus d'informations, voir [Créer des flux de travail](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="ce009-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce009-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce009-122">See Also</span></span>  
 <span data-ttu-id="ce009-123">[Créer des workflows](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ce009-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="ce009-124">[Exporter et importer des workflows](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ce009-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="ce009-125">[Afficher des instances d'étape de workflow archivées](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="ce009-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="ce009-126">[Supprimer des workflows](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ce009-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="ce009-127">[Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="ce009-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="ce009-128">[Paramétrage des workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ce009-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="ce009-129">[Utilisation des workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ce009-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="ce009-130">Flux de travail</span><span class="sxs-lookup"><span data-stu-id="ce009-130">Workflow</span></span>](across-workflow.md)   
