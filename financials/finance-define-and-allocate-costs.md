---
title: "Définition et Répartition des coûts | Microsoft Docs"
description: "Les affectations de coûts déplacent les coûts et les revenus entre les types de coûts, les centres de coûts et les coûts associés. Vous pouvez définir autant d'affectations que nécessaire."
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
ms.openlocfilehash: 050b0bd997629ca189cfbe035e361de7a252d079
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="defining-and-allocating-costs"></a><span data-ttu-id="87205-104">Définition et répartition des coûts</span><span class="sxs-lookup"><span data-stu-id="87205-104">Defining and Allocating Costs</span></span>
<span data-ttu-id="87205-105">Les affectations de coûts déplacent les coûts et les revenus entre les types de coûts, les centres de coûts et les coûts associés.</span><span class="sxs-lookup"><span data-stu-id="87205-105">Cost allocations move costs and revenues between cost types, cost centers, and cost objects.</span></span> <span data-ttu-id="87205-106">Vous pouvez définir autant d'affectations que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="87205-106">You can define as many allocations as you need.</span></span> <span data-ttu-id="87205-107">Chaque affectation comporte les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="87205-107">Each allocation consists of:</span></span>  

-   <span data-ttu-id="87205-108">Une source affectation.</span><span class="sxs-lookup"><span data-stu-id="87205-108">An allocation source.</span></span>  
-   <span data-ttu-id="87205-109">Une ou plusieurs cibles d'affectation.</span><span class="sxs-lookup"><span data-stu-id="87205-109">One or more allocation targets.</span></span>  

<span data-ttu-id="87205-110">La source d'affectation détermine les coûts à affecter, tandis que les cibles d'affectation déterminent l'emplacement des coûts à affecter.</span><span class="sxs-lookup"><span data-stu-id="87205-110">The allocation source establishes which costs must be allocated, and the allocation targets determine where the costs must be allocated.</span></span> <span data-ttu-id="87205-111">Par exemple, les coûts pour le type de coût Fournitures non stockables représentent une source de ventilation.</span><span class="sxs-lookup"><span data-stu-id="87205-111">For example, an allocation source can be the costs for the Electricity and Heating cost type.</span></span> <span data-ttu-id="87205-112">Vous affectez tous les coûts de fournitures non stockables à trois centres de coûts : Atelier, Production, et Vente.</span><span class="sxs-lookup"><span data-stu-id="87205-112">You allocate all electricity and heating costs to three cost centers: Workshop, Production, and Sales.</span></span> <span data-ttu-id="87205-113">Ces centres de coûts sont les cibles d'affectation.</span><span class="sxs-lookup"><span data-stu-id="87205-113">These cost centers are your allocation targets.</span></span>  

<span data-ttu-id="87205-114">Pour chaque source d'affectation, vous définissez un niveau d'affectation, une période de validité et une variante comme identifiant de regroupement.</span><span class="sxs-lookup"><span data-stu-id="87205-114">For each allocation source, you define an allocation level, a validity period, and a variant as grouping identifier.</span></span> <span data-ttu-id="87205-115">Vous pouvez utiliser un traitement par lots pour définir des filtres afin de sélectionner les définitions d'affectation, puis exécuter les affectations des coûts automatiquement.</span><span class="sxs-lookup"><span data-stu-id="87205-115">You can use a batch job to set filters to select allocation definitions and then run cost allocations automatically.</span></span>  

<span data-ttu-id="87205-116">Pour chaque cible d'affectation, vous définissez une base de ventilation.</span><span class="sxs-lookup"><span data-stu-id="87205-116">For each allocation target, you define an allocation base.</span></span> <span data-ttu-id="87205-117">La base de ventilation peut être statique ou dynamique.</span><span class="sxs-lookup"><span data-stu-id="87205-117">The allocation base can be either static or dynamic.</span></span>  

-   <span data-ttu-id="87205-118">Les bases de ventilation statique dépendent d'une valeur définie, par exemple, les mètres carrés utilisés ou un ratio de ventilation prédéfini, comme 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="87205-118">Static allocation bases are based on a definite value, such as square footage or an established allocation ratio, such as 5:2:4.</span></span>  
-   <span data-ttu-id="87205-119">Les bases de ventilation dynamique dépendent de valeurs variables, telles que le nombre de salariés dans un centre de coût ou les revenus de vente d'un coût associé pour une période donnée.</span><span class="sxs-lookup"><span data-stu-id="87205-119">Dynamic allocation bases depend on changeable values, such as the number of employees in a cost center or sales revenue of a cost object throughout a certain time period.</span></span>  

<span data-ttu-id="87205-120">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="87205-120">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="87205-121">À</span><span class="sxs-lookup"><span data-stu-id="87205-121">To</span></span>|<span data-ttu-id="87205-122">Voir</span><span class="sxs-lookup"><span data-stu-id="87205-122">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="87205-123">Configurez la source d'affectation et ses cibles.</span><span class="sxs-lookup"><span data-stu-id="87205-123">Set up allocation source and its targets.</span></span>|[<span data-ttu-id="87205-124">Procédure : configurer la source d'affectation et ses cibles</span><span class="sxs-lookup"><span data-stu-id="87205-124">How to: Set Up Allocation Source and Targets</span></span>](finance-how-to-set-up-allocation-source-and-targets.md)|  
|<span data-ttu-id="87205-125">Configurez plusieurs filtres pour les bases de ventilation dynamique.</span><span class="sxs-lookup"><span data-stu-id="87205-125">Set up various filters for dynamic allocation bases.</span></span>|[<span data-ttu-id="87205-126">Définition de filtres pour les bases de ventilation dynamique</span><span class="sxs-lookup"><span data-stu-id="87205-126">Setting Filters for Dynamic Allocation Bases</span></span>](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|<span data-ttu-id="87205-127">Consultez un exemple sur le mode de définition d'une ventilation statique.</span><span class="sxs-lookup"><span data-stu-id="87205-127">See an example of how to define a static allocation.</span></span>|[<span data-ttu-id="87205-128">Exemple de scénario : Définition des ventilations statiques en fonction du ratio d'affectation</span><span class="sxs-lookup"><span data-stu-id="87205-128">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|<span data-ttu-id="87205-129">Consultez un exemple sur le mode de définition d'une ventilation dynamique.</span><span class="sxs-lookup"><span data-stu-id="87205-129">See an example of how to define a dynamic allocation.</span></span>|[<span data-ttu-id="87205-130">Exemple de scénario : Définition des ventilations dynamiques sur la base des articles vendus</span><span class="sxs-lookup"><span data-stu-id="87205-130">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a><span data-ttu-id="87205-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87205-131">See Also</span></span>  
 <span data-ttu-id="87205-132">[Paramétrage du contrôle de gestion](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="87205-132">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
 <span data-ttu-id="87205-133">[Transfert et validation des écritures de coûts](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="87205-133">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="87205-134">[Comptabilité pour les coûts](finance-manage-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="87205-134">[Accounting for Costs](finance-manage-cost-accounting.md) </span></span>  
 <span data-ttu-id="87205-135">[Terminologie en comptabilité analytique](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="87205-135">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="87205-136">À propos de la comptabilité analytique</span><span class="sxs-lookup"><span data-stu-id="87205-136">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

