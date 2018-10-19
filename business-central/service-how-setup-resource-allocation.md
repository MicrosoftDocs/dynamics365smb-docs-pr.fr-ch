---
title: Configurer l'affectation des ressources | Microsoft Docs
description: "Découvrez comment le système peut vous aider à affecter une personne dotée des compétences requises à la fourniture d'un service."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7ce128aa32d650cf756117ab46987167d9a3781a
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---

# <a name="set-up-resource-allocation"></a><span data-ttu-id="4559f-103">Configurer l'affectation des ressources</span><span class="sxs-lookup"><span data-stu-id="4559f-103">Set Up Resource Allocation</span></span>
<span data-ttu-id="4559f-104">Pour assurer la bonne exécution d'une tâche service, il est important de trouver une ressource qualifiée.</span><span class="sxs-lookup"><span data-stu-id="4559f-104">To ensure that a service task is performed well, it's important to find a resource who is qualified to do the work.</span></span> <span data-ttu-id="4559f-105">Vous pouvez configurer [!INCLUDE[d365fin](includes/d365fin_md.md)] de manière à affecter facilement une ressource disposant des compétences appropriées pour le travail.</span><span class="sxs-lookup"><span data-stu-id="4559f-105">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] so that it's easy to allocate someone who has the right skills for the job.</span></span> <span data-ttu-id="4559f-106">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ce processus est appelé _affectation de ressources_.</span><span class="sxs-lookup"><span data-stu-id="4559f-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], we call this _resource allocation_.</span></span> <span data-ttu-id="4559f-107">Vous pouvez affecter des ressources en fonction de leur compétence, de leur disponibilité, ou selon qu'elles se trouvent dans la même zone service que le client.</span><span class="sxs-lookup"><span data-stu-id="4559f-107">You can allocate resources based on their skill, availability, or whether they are in the same service zone as the customer.</span></span> 

<span data-ttu-id="4559f-108">Pour utiliser l'affectation des ressources, vous devez définir :</span><span class="sxs-lookup"><span data-stu-id="4559f-108">To use resource allocation, you must set up:</span></span>  
  
* <span data-ttu-id="4559f-109">Les compétences nécessaires à la réparation et la maintenance des articles de service.</span><span class="sxs-lookup"><span data-stu-id="4559f-109">The skills required to repair and maintain service items.</span></span> <span data-ttu-id="4559f-110">Vous les affectez aux articles de service et aux ressources.</span><span class="sxs-lookup"><span data-stu-id="4559f-110">You assign these to service items and resources.</span></span>  
* <span data-ttu-id="4559f-111">Les régions géographiques, appelées zones, que vous définissez pour votre marché.</span><span class="sxs-lookup"><span data-stu-id="4559f-111">Geographic regions, called zones, that you define for your market.</span></span> <span data-ttu-id="4559f-112">Par exemple, est, ouest, centre, etc.</span><span class="sxs-lookup"><span data-stu-id="4559f-112">For example, East, West, Central, and so on.</span></span> <span data-ttu-id="4559f-113">Vous les affectez aux clients et aux ressources.</span><span class="sxs-lookup"><span data-stu-id="4559f-113">You assign these to customers and resources.</span></span>  
* <span data-ttu-id="4559f-114">Si les compétences ressource et les zones doivent être affichées, et si un avertissement doit être affiché si une ressource non qualifiée ou une ressource qui ne figure pas dans la zone du client est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="4559f-114">Whether to display resource skills and zones, and whether to display a warning if someone chooses unqualified resource, or a resource that is not in the customer zone.</span></span>  

## <a name="to-set-up-skills"></a><span data-ttu-id="4559f-115">Pour configurer des compétences</span><span class="sxs-lookup"><span data-stu-id="4559f-115">To set up skills</span></span>
1. <span data-ttu-id="4559f-116">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Compétences**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4559f-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Skills**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4559f-117">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="4559f-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><span data-ttu-id="4559f-118">Pour affecter des compétences aux articles de service et aux ressources</span><span class="sxs-lookup"><span data-stu-id="4559f-118">To assign skills to service items and resources</span></span>
1. <span data-ttu-id="4559f-119">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles de service** ou **Ressources**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4559f-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4559f-120">Ouvrez la fiche de l'article de service ou de la ressource, puis sélectionnez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="4559f-120">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="4559f-121">Pour les articles de service, sélectionnez **Compétences ressource**.</span><span class="sxs-lookup"><span data-stu-id="4559f-121">For service items, choose **Resource Skills**.</span></span>  
    * <span data-ttu-id="4559f-122">Pour les ressources, sélectionnez **Compétences**.</span><span class="sxs-lookup"><span data-stu-id="4559f-122">For resources, choose **Skills**.</span></span>  

## <a name="to-set-up-zones"></a><span data-ttu-id="4559f-123">Pour configurer des zones</span><span class="sxs-lookup"><span data-stu-id="4559f-123">To set up zones</span></span>
1. <span data-ttu-id="4559f-124">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Zones**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4559f-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Zones**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4559f-125">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="4559f-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><span data-ttu-id="4559f-126">Pour affecter des zones aux clients et aux ressources</span><span class="sxs-lookup"><span data-stu-id="4559f-126">To assign zones to customers and resources</span></span> 
1. <span data-ttu-id="4559f-127">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Clients** ou **Ressources**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4559f-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4559f-128">Ouvrez la fiche de l'article de service ou de la ressource, puis sélectionnez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="4559f-128">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="4559f-129">Pour les clients, sélectionnez une zone dans le champ **Code zone service**.</span><span class="sxs-lookup"><span data-stu-id="4559f-129">For customers, choose a zone in the **Service Zone Code** field.</span></span>  
    * <span data-ttu-id="4559f-130">Pour les ressources, sélectionnez l'action **Zones service**.</span><span class="sxs-lookup"><span data-stu-id="4559f-130">For resources, choose the **Service Zones** action.</span></span>  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><span data-ttu-id="4559f-131">Pour spécifier les éléments à afficher lorsqu'une ressource est sélectionnée</span><span class="sxs-lookup"><span data-stu-id="4559f-131">To specify what to show when a resource is chosen</span></span>
1. <span data-ttu-id="4559f-132">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres service**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4559f-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="4559f-133">Dans le champ **Compétences ressources**, sélectionnez l'une des options décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4559f-133">In the **Resource Skills Option** field, choose one of the options described in the following table.</span></span>  
  
    |<span data-ttu-id="4559f-134">**Options**</span><span class="sxs-lookup"><span data-stu-id="4559f-134">**Option**</span></span>|<span data-ttu-id="4559f-135">**Description**</span><span class="sxs-lookup"><span data-stu-id="4559f-135">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="4559f-136">Afficher code seulement</span><span class="sxs-lookup"><span data-stu-id="4559f-136">Code Shown</span></span> | <span data-ttu-id="4559f-137">Affiche le code uniquement.</span><span class="sxs-lookup"><span data-stu-id="4559f-137">Displays the code only.</span></span>|  
    |<span data-ttu-id="4559f-138">Utiliser alertes et afficher</span><span class="sxs-lookup"><span data-stu-id="4559f-138">Warning Displayed</span></span> | <span data-ttu-id="4559f-139">Affiche les informations et un avertissement si vous choisissez une ressource qui n'est pas qualifiée.</span><span class="sxs-lookup"><span data-stu-id="4559f-139">Shows the information and displays a warning if you choose a resource that is not qualified.</span></span>|  
    |<span data-ttu-id="4559f-140">Aucun affichage</span><span class="sxs-lookup"><span data-stu-id="4559f-140">Not Used</span></span> | <span data-ttu-id="4559f-141">N'affiche pas ces informations.</span><span class="sxs-lookup"><span data-stu-id="4559f-141">Does not show this information.</span></span>|  

## <a name="to-update-resource-capacity"></a><span data-ttu-id="4559f-142">Pour mettre à jour la capacité ressource</span><span class="sxs-lookup"><span data-stu-id="4559f-142">To update resource capacity</span></span>  
<span data-ttu-id="4559f-143">Vous devrez peut-être modifier la capacité des ressources.</span><span class="sxs-lookup"><span data-stu-id="4559f-143">You may need to change the capacity of resources.</span></span>  
  
1. <span data-ttu-id="4559f-144">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Capacité ressource**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4559f-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Capacity**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4559f-145">Sélectionnez la ressource, puis l'action **Paramétrage capacité ressource**.</span><span class="sxs-lookup"><span data-stu-id="4559f-145">Choose the resource, and then choose the **Set Capacity** action.</span></span>  
3. <span data-ttu-id="4559f-146">Apportez les modifications, puis sélectionnez **Mettre à jour la capacité**.</span><span class="sxs-lookup"><span data-stu-id="4559f-146">Make the changes, and then choose **Update Capacity**.</span></span>  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><span data-ttu-id="4559f-147">Pour mettre à jour les compétences pour des articles, des articles de service ou des groupes d'articles de service</span><span class="sxs-lookup"><span data-stu-id="4559f-147">To update skills for items, service items, or service item groups</span></span>
<span data-ttu-id="4559f-148">Vous pouvez modifier les codes compétence affectés à des articles, par exemple de **PC** à **PCS**, pour un article, un article de service ou pour tous les articles d'un groupe articles de service.</span><span class="sxs-lookup"><span data-stu-id="4559f-148">If you want to change the skill codes assigned to items, for example from **PC** to **PCS**, you can do so either for an item, service item, or for all items in a service item group.</span></span>  
  
1. <span data-ttu-id="4559f-149">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, **Article de service** ou **Groupe articles de service**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4559f-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** or **Service Item**, or **Service Item Group**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4559f-150">Sélectionnez l'entité à mettre à jour, puis sélectionnez l'action **Compétences ressource**.</span><span class="sxs-lookup"><span data-stu-id="4559f-150">Choose the entity to update, and then choose the **Resource Skills** action.</span></span>  
3. <span data-ttu-id="4559f-151">Sur la ligne contenant le code à modifier, dans le champ **Code compétence**, sélectionnez le code compétence.</span><span class="sxs-lookup"><span data-stu-id="4559f-151">On the line with the code to be changed, in the **Skill Code** field, choose the relevant skill code.</span></span>  
4.  <span data-ttu-id="4559f-152">Si des articles de service sont associés à l'article, une boîte de dialogue incluant les deux options suivantes s'ouvre :</span><span class="sxs-lookup"><span data-stu-id="4559f-152">If the item has associated service items, a dialog box opens with the following two options:</span></span>  
  
    * <span data-ttu-id="4559f-153">Attribue la valeur sélectionnée aux codes compétence : sélectionnez cette option pour remplacer l'ancien code compétence de tous les articles de service associés par le nouveau code.</span><span class="sxs-lookup"><span data-stu-id="4559f-153">Change the skill codes to the selected value: Select this option if you want to replace the old skill code with the new one on all the related service items.</span></span>  
    * <span data-ttu-id="4559f-154">Supprime les codes compétence ou met à jour leur relation : sélectionnez cette option pour modifier le code compétence de l'article uniquement.</span><span class="sxs-lookup"><span data-stu-id="4559f-154">Delete the skill codes or update their relation: Select this option if you want to change the skill code on this item only.</span></span> <span data-ttu-id="4559f-155">Le code compétence des articles de service associés sera réaffecté, c'est-à-dire que le champ **Affecté à partir de** sera mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4559f-155">The skill code on the related service items will be reassigned, that is, the **Assigned From** field will be updated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4559f-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4559f-156">See Also</span></span>
[<span data-ttu-id="4559f-157">Affecter des ressources</span><span class="sxs-lookup"><span data-stu-id="4559f-157">Allocate Resources</span></span>](service-how-to-allocate-resources.md)  
[<span data-ttu-id="4559f-158">Configurer des heures de travail et des heures de service</span><span class="sxs-lookup"><span data-stu-id="4559f-158">Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)  
[<span data-ttu-id="4559f-159">Configurer le reporting panne</span><span class="sxs-lookup"><span data-stu-id="4559f-159">Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md)  
[<span data-ttu-id="4559f-160">Configurer des codes prestations standards</span><span class="sxs-lookup"><span data-stu-id="4559f-160">Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)  
 


