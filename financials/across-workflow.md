---
title: Workflow | Microsoft Docs
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
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f65c0e577e839928809f7afda3dbdb4c9b7702c8
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="workflow"></a><span data-ttu-id="dfd5d-105">Flux de travail</span><span class="sxs-lookup"><span data-stu-id="dfd5d-105">Workflow</span></span>
<span data-ttu-id="dfd5d-106">Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="dfd5d-107">Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="dfd5d-108">Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="dfd5d-109">Dans la fenêtre **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="dfd5d-110">Chaque étape comprend un événement de workflow modéré par des conditions d'événement, et une réponse de workflow modérée par des options de réponse.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="dfd5d-111">Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="dfd5d-112">La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut plusieurs workflows préconfigurés, représentés par des modèles de workflow que vous pouvez copier pour créer des workflows.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="dfd5d-113">Le code des modèles de workflow ajoutés par Microsoft a le préfixe « MS- ».</span><span class="sxs-lookup"><span data-stu-id="dfd5d-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="dfd5d-114">Pour plus d'informations, voir la liste des modèles de workflow dans la fenêtre Modèles flux de travail.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="dfd5d-115">Si un scénario d'entreprise requiert un événement ou une réponse de workflow qui n'est pas pris en charge, un partenaire Microsoft doit l'implémenter en personnalisant le code de l'application.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="dfd5d-116">Pour plus d'informations, voir [Procédure pas à pas : implémentation de nouveaux événements et réponses de flux de travail](https://msdn.microsoft.com/en-us/library/mt574349.aspx) sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](https://msdn.microsoft.com/en-us/library/mt574349.aspx) on MSDN.</span></span>  

 <span data-ttu-id="dfd5d-117">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-117">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="dfd5d-118">**Pour**</span><span class="sxs-lookup"><span data-stu-id="dfd5d-118">**To**</span></span>|<span data-ttu-id="dfd5d-119">**Voir**</span><span class="sxs-lookup"><span data-stu-id="dfd5d-119">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="dfd5d-120">Configurer des utilisateurs du workflow, spécifier comment les utilisateurs sont notifiés et créer des workflows.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-120">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="dfd5d-121">Pour de nouveaux workflows pour des scénarios non pris en charge, implémentez les éléments requis du workflow en personnalisant le code d'application.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-121">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="dfd5d-122">Paramétrage des workflows</span><span class="sxs-lookup"><span data-stu-id="dfd5d-122">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="dfd5d-123">Activer des workflows, agir sur les notifications du workflow, notamment les approbations de demandes et approuver des demandes pour effectuer une étape du workflow.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-123">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="dfd5d-124">Archiver et supprimer des workflows.</span><span class="sxs-lookup"><span data-stu-id="dfd5d-124">Archive and delete workflows.</span></span>|[<span data-ttu-id="dfd5d-125">Utilisation des workflows</span><span class="sxs-lookup"><span data-stu-id="dfd5d-125">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="dfd5d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfd5d-126">See Also</span></span>  
[<span data-ttu-id="dfd5d-127">Ventes</span><span class="sxs-lookup"><span data-stu-id="dfd5d-127">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="dfd5d-128">Achats</span><span class="sxs-lookup"><span data-stu-id="dfd5d-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="dfd5d-129">Gestion des projets</span><span class="sxs-lookup"><span data-stu-id="dfd5d-129">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="dfd5d-130">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dfd5d-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

