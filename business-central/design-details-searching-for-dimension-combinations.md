---
title: Détails de conception - recherche des croisements analytiques | Microsoft Docs
description: Lorsque vous fermez une page après avoir modifié un ensemble de dimensions, Business Central évalue si l'ensemble de dimensions modifié existe. Si l'ensemble n'existe pas, un nouvel ensemble est créé et le code de croisement analytique est retourné.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: cde720526fdad4c9e4352f08f649d6bd3fc51540
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "912378"
---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="9621f-104">Détails de conception : recherche des croisements analytiques</span><span class="sxs-lookup"><span data-stu-id="9621f-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="9621f-105">Lorsque vous fermez une page après avoir modifié un ensemble de dimensions, [!INCLUDE[d365fin](includes/d365fin_md.md)] évalue si l'ensemble de dimensions modifié existe.</span><span class="sxs-lookup"><span data-stu-id="9621f-105">When you close a page after you edit a set of dimensions, [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="9621f-106">Si l'ensemble n'existe pas, un nouvel ensemble est créé et le code de croisement analytique est retourné.</span><span class="sxs-lookup"><span data-stu-id="9621f-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="9621f-107">Création d'un arbre de recherche</span><span class="sxs-lookup"><span data-stu-id="9621f-107">Building Search Tree</span></span>  
 <span data-ttu-id="9621f-108">La table 481 **Nœud d'arbre ensemble de dimensions** est utilisé lorsque [!INCLUDE[d365fin](includes/d365fin_md.md)] évalue si un ensemble de dimensions existe déjà dans la table **Écriture de l'ensemble de dimensions** de la table 480.</span><span class="sxs-lookup"><span data-stu-id="9621f-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="9621f-109">L'évaluation est exécutée en parcourant de manière récursive l'arbre de recherche en commençant par le niveau numéroté 0.</span><span class="sxs-lookup"><span data-stu-id="9621f-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="9621f-110">Le plus haut niveau 0 représente un ensemble de dimensions sans les écritures d'ensemble de dimensions.</span><span class="sxs-lookup"><span data-stu-id="9621f-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="9621f-111">Les enfants cet ensemble de dimensions représentent des ensembles de dimensions avec une seule écriture d'ensemble de dimensions.</span><span class="sxs-lookup"><span data-stu-id="9621f-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="9621f-112">Les enfants de ces ensembles de dimensions représentent des ensembles de dimensions avec deux enfants, etc.</span><span class="sxs-lookup"><span data-stu-id="9621f-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="9621f-113">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="9621f-113">Example 1</span></span>  
 <span data-ttu-id="9621f-114">Le schéma suivant représente un arbre de recherche avec six ensembles de dimensions.</span><span class="sxs-lookup"><span data-stu-id="9621f-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="9621f-115">Seule l'écriture d'ensemble de dimensions distinctive est affichée dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="9621f-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="9621f-116">![Exemple de structure arborescente des dimensions](media/nav2013_dimension_tree.png "Exemple de structure arborescente des dimensions")</span><span class="sxs-lookup"><span data-stu-id="9621f-116">![Example of dimension tree structure](media/nav2013_dimension_tree.png "Example of dimension tree structure")</span></span>  

 <span data-ttu-id="9621f-117">Le tableau suivant décrit une liste complète des écritures d'ensemble de dimensions qui constituent chaque ensemble de dimensions.</span><span class="sxs-lookup"><span data-stu-id="9621f-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="9621f-118">Ensembles de dimensions</span><span class="sxs-lookup"><span data-stu-id="9621f-118">Dimension Sets</span></span>|<span data-ttu-id="9621f-119">Écritures de l'ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="9621f-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="9621f-120">Ensemble 0</span><span class="sxs-lookup"><span data-stu-id="9621f-120">Set 0</span></span>|<span data-ttu-id="9621f-121">Aucune</span><span class="sxs-lookup"><span data-stu-id="9621f-121">None</span></span>|  
|<span data-ttu-id="9621f-122">Ensemble 1</span><span class="sxs-lookup"><span data-stu-id="9621f-122">Set 1</span></span>|<span data-ttu-id="9621f-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="9621f-123">AREA 30</span></span>|  
|<span data-ttu-id="9621f-124">Ensemble 2</span><span class="sxs-lookup"><span data-stu-id="9621f-124">Set 2</span></span>|<span data-ttu-id="9621f-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="9621f-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="9621f-126">Ensemble 3</span><span class="sxs-lookup"><span data-stu-id="9621f-126">Set 3</span></span>|<span data-ttu-id="9621f-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="9621f-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="9621f-128">Ensemble 4</span><span class="sxs-lookup"><span data-stu-id="9621f-128">Set 4</span></span>|<span data-ttu-id="9621f-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="9621f-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="9621f-130">Ensemble 5</span><span class="sxs-lookup"><span data-stu-id="9621f-130">Set 5</span></span>|<span data-ttu-id="9621f-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="9621f-131">AREA 40</span></span>|  
|<span data-ttu-id="9621f-132">Ensemble 6</span><span class="sxs-lookup"><span data-stu-id="9621f-132">Set 6</span></span>|<span data-ttu-id="9621f-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="9621f-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="9621f-134">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="9621f-134">Example 2</span></span>  
 <span data-ttu-id="9621f-135">Cet exemple montre la manière dont [!INCLUDE[d365fin](includes/d365fin_md.md)] évalue si un ensemble de dimensions constitué des écritures de l'ensemble de dimensions AREA 40, DEPT PROD existe.</span><span class="sxs-lookup"><span data-stu-id="9621f-135">This example shows how [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="9621f-136">D'abord, [!INCLUDE[d365fin](includes/d365fin_md.md)] met également à jour la table **Nœud d'arbre ensemble de dimensions** pour s'assurer que l'arbre de recherche ressemble au schéma suivant.</span><span class="sxs-lookup"><span data-stu-id="9621f-136">First, [!INCLUDE[d365fin](includes/d365fin_md.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="9621f-137">Ainsi, l'ensemble de dimensions 7 devient un enfant de l'ensemble de dimensions 5.</span><span class="sxs-lookup"><span data-stu-id="9621f-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="9621f-138">![Exemple de structure arborescente des dimensions dans NAV 2013](media/nav2013_dimension_tree_example2.png "Exemple de structure arborescente des dimensions dans NAV 2013")</span><span class="sxs-lookup"><span data-stu-id="9621f-138">![Example of dimension tree structure in NAV 2013](media/nav2013_dimension_tree_example2.png "Example of dimension tree structure in NAV 2013")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="9621f-139">Recherche de l'ID ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="9621f-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="9621f-140">Au niveau conceptuel, **Code parent**, **Dimension** et **Section analytique**, dans l'arbre de recherche, sont combinés et sont utilisés comme clé primaire, car [!INCLUDE[d365fin](includes/d365fin_md.md)] parcourt l'arborescence dans le même ordre que les écritures analytiques.</span><span class="sxs-lookup"><span data-stu-id="9621f-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[d365fin](includes/d365fin_md.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="9621f-141">La fonction GET (enregistrement) est utilisée pour rechercher l'ID de l'ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="9621f-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="9621f-142">L'exemple de code suivant indique comment trouver l'ID d'ensemble de dimensions lorsqu'il existe trois sections analytiques.</span><span class="sxs-lookup"><span data-stu-id="9621f-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

<span data-ttu-id="9621f-143">Toutefois, pour préserver la capacité de [!INCLUDE[d365fin](includes/d365fin_md.md)] à renommer à la fois un axe et une section analytique, la table 349 **Section analytique** est étendue avec un champ d'entier **ID section analytique**.</span><span class="sxs-lookup"><span data-stu-id="9621f-143">However, to preserve the ability of [!INCLUDE[d365fin](includes/d365fin_md.md)] to rename both a dimension and a dimension value, table 349, **Dimension Value**, is extended with an integer field, **Dimension Value ID**.</span></span> <span data-ttu-id="9621f-144">Cette table convertit la paire de champs **Axe analytique** et **Section analytique** sur une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="9621f-144">This table converts the field pair, **Dimension** and **Dimension Value**, to an integer value.</span></span> <span data-ttu-id="9621f-145">Lorsque vous renommez la dimension et la valeur de dimension, la valeur d'entier n'est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="9621f-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="9621f-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9621f-146">See Also</span></span>  
 <span data-ttu-id="9621f-147">[Fonction GET (Enregistrement)](/dynamics-nav/GET-Function--Record-)  </span><span class="sxs-lookup"><span data-stu-id="9621f-147">[GET Function (Record)](/dynamics-nav/GET-Function--Record-)  </span></span>  
 <span data-ttu-id="9621f-148">[Détails de conception : écritures d'ensemble de dimensions](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="9621f-148">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="9621f-149">[Aperçu des écritures de l'ensemble de dimensions](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="9621f-149">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="9621f-150">[Détails de conception : structure de la table](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="9621f-150">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 <span data-ttu-id="9621f-151">[Détails de conception : Codeunit 408 Gestion des axes analytiques](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="9621f-151">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
 [<span data-ttu-id="9621f-152">Détails de conception : exemples de code de motifs modifiés dans les modifications</span><span class="sxs-lookup"><span data-stu-id="9621f-152">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
