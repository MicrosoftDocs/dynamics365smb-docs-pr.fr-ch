---
title: Enregistrer et ajuster l'utilisation et les prix des ressources| Microsoft Docs
description: Décrit la manière dont vous pouvez enregistrer l'utilisation ou la consommation ressource associée à un projet, de garder la trace et de gérer les coûts, les prix, ainsi que les types de travaux.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: ac15e8f84efba5a46e3d5fc3d0d07f9dceed666a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778868"
---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="0b45f-103">Utiliser des ressources pour des projets</span><span class="sxs-lookup"><span data-stu-id="0b45f-103">Use Resources for Jobs</span></span>
<span data-ttu-id="0b45f-104">Vous devez enregistrer l'utilisation des ressources dans la feuille projet pour suivre les coûts et les prix, ainsi que les types de travaux associés aux projets.</span><span class="sxs-lookup"><span data-stu-id="0b45f-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="0b45f-105">Pour en savoir plus, consultez [Enregistrer l'utilisation pour les projets](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="0b45f-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

> [!NOTE]
> <span data-ttu-id="0b45f-106">Vous pouvez également acheter des ressources externes, par exemple pour facturer un fournisseur pour le travail livré.</span><span class="sxs-lookup"><span data-stu-id="0b45f-106">You can also purchase external resources, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="0b45f-107">Pour en savoir plus, consultez [Enregistrer des achats](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="0b45f-107">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="0b45f-108">Vous pouvez aussi valider l'utilisation d'une ressource sur une feuille ressource.</span><span class="sxs-lookup"><span data-stu-id="0b45f-108">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="0b45f-109">Les écritures validées sur une feuille ressource n'ont aucune incidence sur la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="0b45f-109">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="0b45f-110">Pour affecter des ressources aux projets</span><span class="sxs-lookup"><span data-stu-id="0b45f-110">To assign resources to jobs</span></span>
<span data-ttu-id="0b45f-111">Vous pouvez affecter des ressources aux projets en créant des lignes planning projet pour le projet.</span><span class="sxs-lookup"><span data-stu-id="0b45f-111">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="0b45f-112">Pour plus d'informations, voir [Créer des projets](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="0b45f-112">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="0b45f-113">Pour enregistrer l'utilisation des ressources pour un projet</span><span class="sxs-lookup"><span data-stu-id="0b45f-113">To record resource usage for a job</span></span>
1. <span data-ttu-id="0b45f-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles projet**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="0b45f-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="0b45f-115">Ouvrez la feuille projet appropriée, puis complétez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="0b45f-115">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="0b45f-116">Lorsque la feuille est renseignée, cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="0b45f-116">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="0b45f-117">Pour ajuster le prix des ressources</span><span class="sxs-lookup"><span data-stu-id="0b45f-117">To adjust resource prices</span></span>
<span data-ttu-id="0b45f-118">Si vous souhaitez modifier le coût ou le prix d'un grand nombre de ressources, vous pouvez utiliser un traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="0b45f-118">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="0b45f-119">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Ajuster coûts et prix ressource**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="0b45f-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="0b45f-120">Renseignez les autres champs selon vos besoins, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b45f-120">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0b45f-121">Ce traitement par lots ne crée pas et n'ajuste pas les nouveaux coûts ou prix des ressources.</span><span class="sxs-lookup"><span data-stu-id="0b45f-121">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="0b45f-122">Il modifie uniquement le contenu du champ de la fiche ressource correspondant au champ **Champ à modifier** que vous avez sélectionné dans le traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="0b45f-122">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="0b45f-123">L'ajustement s'appliquant immédiatement aux ressources, vérifiez les facteurs d'ajustement avant de lancer le traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="0b45f-123">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="0b45f-124">Pour obtenir des propositions de modification des prix ressource basées sur les prix secondaires existants</span><span class="sxs-lookup"><span data-stu-id="0b45f-124">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="0b45f-125">Si vous avez déjà configuré des prix secondaires pour un certain nombre de ressources, vous pouvez utiliser le traitement par lots pour configurer des prix ressource secondaires.</span><span class="sxs-lookup"><span data-stu-id="0b45f-125">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="0b45f-126">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Nouv. prix ressource proposés**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="0b45f-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="0b45f-127">Sélectionnez l'action **Prop. modif. prix ress. (prix)**, puis renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="0b45f-127">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="0b45f-128">Choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b45f-128">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="0b45f-129">Lorsque le traitement par lots est terminé, la page **Nouv. prix ressource proposés** affiche les résultats du traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="0b45f-129">When the batch job is finished, the **Resource Price Changes** page shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="0b45f-130">Pour obtenir des propositions de modification des prix ressource basées sur les prix standard :</span><span class="sxs-lookup"><span data-stu-id="0b45f-130">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="0b45f-131">Si vous souhaitez configurer des prix ressource secondaires basés sur les prix standard des fiches ressource, vous pouvez utiliser un traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="0b45f-131">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="0b45f-132">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Nouv. prix ressource proposés**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="0b45f-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="0b45f-133">Sélectionnez l'action **Prop. modif. prix ress. (ress)**, puis renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="0b45f-133">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="0b45f-134">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b45f-134">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="0b45f-135">Lorsque le traitement par lots est terminé, ouvrez la page **Nouv. prix ressource proposés** pour visualiser les résultats du traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="0b45f-135">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="0b45f-136">Pour obtenir des propositions de modification des prix ressource basées sur les prix standard</span><span class="sxs-lookup"><span data-stu-id="0b45f-136">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="0b45f-137">Si vous avez déjà configuré des prix secondaires pour certaines ressources, vous pouvez utiliser le traitement par lots pour configurer des prix ressource secondaires.</span><span class="sxs-lookup"><span data-stu-id="0b45f-137">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="0b45f-138">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Prop. modif. prix ress. (prix)**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="0b45f-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0b45f-139">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="0b45f-139">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="0b45f-140">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b45f-140">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="0b45f-141">Lorsque le traitement par lots est terminé, ouvrez la page **Nouv. prix ressource proposés** pour visualiser les résultats du traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="0b45f-141">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b45f-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b45f-142">See Also</span></span>
[<span data-ttu-id="0b45f-143">Gestion de projets</span><span class="sxs-lookup"><span data-stu-id="0b45f-143">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="0b45f-144">Finances</span><span class="sxs-lookup"><span data-stu-id="0b45f-144">Finance</span></span>](finance.md)  
<span data-ttu-id="0b45f-145">[Achats](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="0b45f-145">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="0b45f-146">[Ventes](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="0b45f-146">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="0b45f-147">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0b45f-147">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
