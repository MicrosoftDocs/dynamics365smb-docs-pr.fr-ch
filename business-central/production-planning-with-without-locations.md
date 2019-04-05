---
title: Planification avec/sans magasin | Microsoft Docs
description: il est important de comprendre le fonctionnement de la planification avec/sans codes magasin sur les lignes demande.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 211f990e21c8c0a5c6d1705de5345be20adae4d7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820358"
---
# <a name="planning-with-or-without-locations"></a><span data-ttu-id="c1b5b-103">Planification avec/sans magasin.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-103">Planning With or Without Locations</span></span>
<span data-ttu-id="c1b5b-104">En ce qui concerne la planification avec ou sans code magasin sur les lignes demande, le système opère directement lorsque :</span><span class="sxs-lookup"><span data-stu-id="c1b5b-104">Concerning planning with or without location codes on demand lines, the planning system operates in a straight forward way when:</span></span>  

-   <span data-ttu-id="c1b5b-105">Les lignes demande indiquent systématiquement le code magasin et le système exploite intégralement les points de stock, y compris le paramètre de magasin pertinent.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-105">demand lines always carry location codes and the system fully uses stockkeeping units, including the relevant location setup.</span></span>  
-   <span data-ttu-id="c1b5b-106">Les lignes demande n'indiquent jamais le code magasin et le système n'utilise ni les points stock ni le paramètre de magasin (reportez-vous au dernier cas de figure ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="c1b5b-106">demand lines never carry location codes and the system does not use SKUs or any location setup (see last scenario below).</span></span>  

<span data-ttu-id="c1b5b-107">Toutefois, si les lignes demande indiquent parfois le code magasin, mais pas de manière systématique, le système de planification suit certaines règles en fonction de la configuration.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-107">However, if demand lines sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>  

## <a name="demand-at-location"></a><span data-ttu-id="c1b5b-108">Demande dans le magasin</span><span class="sxs-lookup"><span data-stu-id="c1b5b-108">Demand at Location</span></span>  
<span data-ttu-id="c1b5b-109">Lorsque le système de planification détecte une demande dans un magasin (identifiée par une ligne dotée d'un code magasin), il peut procéder de plusieurs manières en fonction de 3 valeurs critiques.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-109">When the planning system detects demand at a location (a line with a location code), it will behave in different ways depending on 3 critical setup values.</span></span>  

<span data-ttu-id="c1b5b-110">Lors de l'exécution de la planification, le système recherche ces 3 paramètres l'un après l'autre et effectue la planification en conséquence :</span><span class="sxs-lookup"><span data-stu-id="c1b5b-110">During a planning run, the system checks for the 3 setup values in sequence and plans accordingly:</span></span>  

1.  <span data-ttu-id="c1b5b-111">Le champ **Magasin obligatoire** est-il activé ?</span><span class="sxs-lookup"><span data-stu-id="c1b5b-111">Is there a check mark in the **Location Mandatory** field?</span></span>  

    <span data-ttu-id="c1b5b-112">Si oui :</span><span class="sxs-lookup"><span data-stu-id="c1b5b-112">If yes, then:</span></span>  

2.  <span data-ttu-id="c1b5b-113">Existe-t-il un point de stock pour l'article ?</span><span class="sxs-lookup"><span data-stu-id="c1b5b-113">Does SKU exist for the item?</span></span>  

    <span data-ttu-id="c1b5b-114">Si oui :</span><span class="sxs-lookup"><span data-stu-id="c1b5b-114">If yes, then:</span></span>  

    <span data-ttu-id="c1b5b-115">L'article est planifié en fonction des paramètres de planification de la fiche point de stock.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-115">The item is planned according to planning parameters on the SKU card.</span></span>  

    <span data-ttu-id="c1b5b-116">Si non :</span><span class="sxs-lookup"><span data-stu-id="c1b5b-116">If no, then:</span></span>  

3.  <span data-ttu-id="c1b5b-117">Le champ **Mag. composant par déf** contient-il le code magasin demandé ?</span><span class="sxs-lookup"><span data-stu-id="c1b5b-117">Does the **Components at Location** field contain the demanded location code?</span></span>  

    <span data-ttu-id="c1b5b-118">Si oui :</span><span class="sxs-lookup"><span data-stu-id="c1b5b-118">If yes, then:</span></span>  

    <span data-ttu-id="c1b5b-119">L'article est planifié en fonction des paramètres de planification de la fiche article.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-119">The item is planned according to planning parameters on the item card.</span></span>  

    <span data-ttu-id="c1b5b-120">Si non :</span><span class="sxs-lookup"><span data-stu-id="c1b5b-120">If no, then:</span></span>  

    <span data-ttu-id="c1b5b-121">L’article est planifié comme suit : Méthode réapprovisionnement = *Lot pour Lot*, Inclure stock = *Oui*. Tous les autres paramètres de planification ont la valeur Vide.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-121">The item is planned according to: Reordering Policy =  *Lot-for-Lot*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span> <span data-ttu-id="c1b5b-122">(Les articles qui suivent l’*ordre* de la méthode réapprovisionnement continuent à  *le* suivre, tout comme les autres paramètres.)</span><span class="sxs-lookup"><span data-stu-id="c1b5b-122">(Items using reordering policy  *Order* remain using  *Order* as well as the other settings.)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c1b5b-123">Cette solution minimale couvre strictement la demande.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-123">This minimal alternative only covers the exact demand.</span></span> <span data-ttu-id="c1b5b-124">Tout paramètre de planification défini est ignoré.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-124">Any planning parameters defined are ignored.</span></span>  

<span data-ttu-id="c1b5b-125">Consultez les variantes des cas de figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-125">See variations in the scenarios below.</span></span>  

## <a name="demand-at-blank-location"></a><span data-ttu-id="c1b5b-126">Demande dans un magasin blanc</span><span class="sxs-lookup"><span data-stu-id="c1b5b-126">Demand at "Blank Location"</span></span>  
<span data-ttu-id="c1b5b-127">Même si la case à cocher **Magasin obligatoire** est activée, le système autorise la création de lignes demande sans code magasin, ce que l'on appelle également « magasin *VIDE* ».</span><span class="sxs-lookup"><span data-stu-id="c1b5b-127">Even if the **Location Mandatory** check box is selected, the system will allow demand lines to be created without a location code – also referred to as *BLANK* location.</span></span> <span data-ttu-id="c1b5b-128">Il s'agit d'un écart pour le système car il a plusieurs valeurs de paramétrage accordées pour gérez les emplacements (voir ci-dessus) et, par conséquent, le moteur de planification ne crée pas de ligne planning pour une telle ligne demande.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span> <span data-ttu-id="c1b5b-129">Si le champ **Magasin obligatoire** n'est pas sélectionné mais si une des valeurs d'emplacement existe, c'est également considéré comme un écart et le système de planification réagira en proposant la « solution minimale » :</span><span class="sxs-lookup"><span data-stu-id="c1b5b-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, then that is also considered a deviation and the planning system will react by outputting the "minimal alternative":</span></span>   
<span data-ttu-id="c1b5b-130">L'article est planifié comme suit : Méthode réapprovisionnement =  *Lot pour lot* (l' *ordre* conserve la valeur *Ordre)*, Inclure stock =  *Oui*. Tous les autres paramètres de planification ont la valeur Vide.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-130">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains *Order)*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

<span data-ttu-id="c1b5b-131">Consultez les variantes des scénarios de configuration ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-131">See variations in the setup scenarios below.</span></span>  

### <a name="setup-1"></a><span data-ttu-id="c1b5b-132">Configuration 1 :</span><span class="sxs-lookup"><span data-stu-id="c1b5b-132">Setup 1:</span></span>  

-   <span data-ttu-id="c1b5b-133">Magasin obligatoire = *Oui*</span><span class="sxs-lookup"><span data-stu-id="c1b5b-133">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="c1b5b-134">Le point de stock a pour valeur  *ROUGE*</span><span class="sxs-lookup"><span data-stu-id="c1b5b-134">SKU is set up for  *RED*</span></span>  
-   <span data-ttu-id="c1b5b-135">Mag. composant par déf =  *BLEU*</span><span class="sxs-lookup"><span data-stu-id="c1b5b-135">Component at Location =  *BLUE*</span></span>  

#### <a name="case-11-demand-is-at--red-location"></a><span data-ttu-id="c1b5b-136">Situation 1.1 : la demande concerne un magasin  *ROUGE*.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-136">Case 1.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="c1b5b-137">L'article est planifié en fonction des paramètres de planification de la fiche point de stock (y compris, un éventuel transfert).</span><span class="sxs-lookup"><span data-stu-id="c1b5b-137">The item is planned according to planning parameters on the SKU card (including possible transfer).</span></span>  

#### <a name="case-12-demand-is-at--blue-location"></a><span data-ttu-id="c1b5b-138">Situation 1.2 : la demande concerne un magasin  *BLEU*.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-138">Case 1.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="c1b5b-139">L'article est planifié en fonction des paramètres de planification de la fiche article.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-139">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-13-demand-is-at--green-location"></a><span data-ttu-id="c1b5b-140">Situation 1.3 : la demande concerne un magasin  *VERT*.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-140">Case 1.3: Demand is at  *GREEN* location</span></span>  

<span data-ttu-id="c1b5b-141">L'article est planifié comme suit : Méthode réapprovisionnement =  *Lot pour Lot* (l' *ordre* conserve la valeur  *Ordre*), Inclure stock =  *Oui*. Tous les autres paramètres de planification ont la valeur Vide.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-141">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-14-demand-is-at--blank-location"></a><span data-ttu-id="c1b5b-142">Situation 1.4 : la demande concerne un magasin  *BLANC*.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-142">Case 1.4: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="c1b5b-143">L'article n'est pas planifié car aucun magasin n'est défini sur la ligne demande.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-143">The item is not planned because no location is defined on the demand line.</span></span>  

### <a name="setup-2"></a><span data-ttu-id="c1b5b-144">Configuration 2 :</span><span class="sxs-lookup"><span data-stu-id="c1b5b-144">Setup 2:</span></span>  

-   <span data-ttu-id="c1b5b-145">Magasin obligatoire = *Oui*</span><span class="sxs-lookup"><span data-stu-id="c1b5b-145">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="c1b5b-146">Il n 'existe pas de point de stock.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-146">No SKU exists</span></span>  
-   <span data-ttu-id="c1b5b-147">Mag. composant par déf =  *BLEU*</span><span class="sxs-lookup"><span data-stu-id="c1b5b-147">Component at Location =  *BLUE*</span></span>  

#### <a name="case-21-demand-is-at--red-location"></a><span data-ttu-id="c1b5b-148">Situation 2.1 : la demande concerne un magasin  *ROUGE*.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-148">Case 2.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="c1b5b-149">L'article est planifié comme suit : Méthode réapprovisionnement =  *Lot pour Lot* (l' *ordre* conserve la valeur  *Ordre*), Inclure stock =  *Oui*. Tous les autres paramètres de planification ont la valeur Vide.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-149">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-22-demand-is-at--blue-location"></a><span data-ttu-id="c1b5b-150">Situation 2.2 : la demande concerne un magasin  *BLEU*.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-150">Case 2.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="c1b5b-151">L'article est planifié en fonction des paramètres de planification de la fiche article.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-151">The item is planned according to planning parameters on the item card.</span></span>  

### <a name="setup-3"></a><span data-ttu-id="c1b5b-152">Configuration 3 :</span><span class="sxs-lookup"><span data-stu-id="c1b5b-152">Setup 3:</span></span>  

-   <span data-ttu-id="c1b5b-153">Magasin obligatoire = *Non*</span><span class="sxs-lookup"><span data-stu-id="c1b5b-153">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="c1b5b-154">Il n 'existe pas de point de stock.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-154">No SKU exists</span></span>  
-   <span data-ttu-id="c1b5b-155">Mag. composant par déf =  *BLEU*</span><span class="sxs-lookup"><span data-stu-id="c1b5b-155">Component at Location =  *BLUE*</span></span>  

#### <a name="case-31-demand-is-at--red-location"></a><span data-ttu-id="c1b5b-156">Situation 3.1 : la demande concerne un magasin  *ROUGE*.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-156">Case 3.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="c1b5b-157">L'article est planifié comme suit : Méthode réapprovisionnement =  *Lot pour Lot* (l' *ordre* conserve la valeur  *Ordre*), Inclure stock =  *Oui*. Tous les autres paramètres de planification ont la valeur Vide.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-157">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-32-demand-is-at--blue-location"></a><span data-ttu-id="c1b5b-158">Situation 3.2 : la demande concerne un magasin  *BLEU*.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-158">Case 3.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="c1b5b-159">L'article est planifié en fonction des paramètres de planification de la fiche article.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-159">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-33-demand-is-at--blank-location"></a><span data-ttu-id="c1b5b-160">Situation 3.3 : la demande concerne un magasin  *BLANC*.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-160">Case 3.3: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="c1b5b-161">L'article est planifié comme suit : Méthode réapprovisionnement =  *Lot pour Lot* (l' *ordre* conserve la valeur  *Ordre*), Inclure stock =  *Oui*. Tous les autres paramètres de planification ont la valeur Vide.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-161">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

### <a name="setup-4"></a><span data-ttu-id="c1b5b-162">Configuration 4 :</span><span class="sxs-lookup"><span data-stu-id="c1b5b-162">Setup 4:</span></span>  

-   <span data-ttu-id="c1b5b-163">Magasin obligatoire = *Non*</span><span class="sxs-lookup"><span data-stu-id="c1b5b-163">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="c1b5b-164">Il n 'existe pas de point de stock.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-164">No SKU exists</span></span>  
-   <span data-ttu-id="c1b5b-165">Mag. composant par déf =  *VIDE*</span><span class="sxs-lookup"><span data-stu-id="c1b5b-165">Component at Location =  *BLANK*</span></span>  

#### <a name="case-41-demand-is-at--blue-location"></a><span data-ttu-id="c1b5b-166">Situation 4.1 : la demande concerne un magasin  *BLEU*.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-166">Case 4.1: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="c1b5b-167">L'article est planifié comme suit : Méthode réapprovisionnement =  *Lot pour Lot* (l' *ordre* conserve la valeur  *Ordre*), Inclure stock =  *Oui*. Tous les autres paramètres de planification ont la valeur Vide.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-167">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-42-demand-is-at--blank-location"></a><span data-ttu-id="c1b5b-168">Situation 4.2 : la demande concerne un magasin  *BLANC*.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-168">Case 4.2: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="c1b5b-169">L'article est planifié en fonction des paramètres de planification de la fiche article.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-169">The item is planned according to planning parameters on the item card.</span></span>  

<span data-ttu-id="c1b5b-170">Comme vous pouvez le voir au dernier cas de figure, le seul moyen d'obtenir des résultats corrects pour une ligne demande sans code magasin consiste à désactiver toutes les valeurs de configuration relatives aux magasins.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-170">As you can see from the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="c1b5b-171">De la même manière, le seul moyen d'obtenir des résultats de planification stables pour les demandes dans des magasins consiste à utiliser des points de stock.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-171">Similarly, the only way to get stable planning results for demand at locations is to use stockkeeping units.</span></span>  

<span data-ttu-id="c1b5b-172">Par conséquent, si vous planifiez souvent des demandes dans des magasins, il est fortement recommandé d'utiliser la fonctionnalité des points de stock.</span><span class="sxs-lookup"><span data-stu-id="c1b5b-172">Therefore, if you often plan for demand at locations, it is strongly advised to use the Stockkeeping Units feature.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c1b5b-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1b5b-173">See Also</span></span>
<span data-ttu-id="c1b5b-174">[Planifié](production-planning.md)  </span><span class="sxs-lookup"><span data-stu-id="c1b5b-174">[Planning](production-planning.md)  </span></span>  
[<span data-ttu-id="c1b5b-175">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="c1b5b-175">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="c1b5b-176">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="c1b5b-176">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="c1b5b-177">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="c1b5b-177">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c1b5b-178">Achats</span><span class="sxs-lookup"><span data-stu-id="c1b5b-178">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c1b5b-179">[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="c1b5b-179">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="c1b5b-180">Pratiques de configuration recommandées : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="c1b5b-180">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="c1b5b-181">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c1b5b-181">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
