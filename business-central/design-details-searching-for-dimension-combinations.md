---
title: Détails de conception - recherche des croisements analytiques | Microsoft Docs
description: "Lorsque vous fermez une page après avoir modifié un ensemble de dimensions, Business\_Central évalue si l’ensemble de dimensions modifié existe. Si l’ensemble n’existe pas, un nouvel ensemble est créé et le code de croisement analytique est retourné."
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
---
# Détails de conception : recherche des croisements analytiques
Lorsque vous fermez une page après avoir modifié un ensemble de dimensions, [!INCLUDE[prod_short](includes/prod_short.md)] évalue si l’ensemble de dimensions modifié existe. Si l’ensemble n’existe pas, un nouvel ensemble est créé et le code de croisement analytique est retourné.  

## Création d’un arbre de recherche  
 La table 481 **Nœud d’arbre ensemble de dimensions** est utilisé lorsque [!INCLUDE[prod_short](includes/prod_short.md)] évalue si un ensemble de dimensions existe déjà dans la table **Écriture de l’ensemble de dimensions** de la table 480. L’évaluation est exécutée en parcourant de manière récursive l’arbre de recherche en commençant par le niveau numéroté 0. Le plus haut niveau 0 représente un ensemble de dimensions sans les écritures d’ensemble de dimensions. Les enfants cet ensemble de dimensions représentent des ensembles de dimensions avec une seule écriture d’ensemble de dimensions. Les enfants de ces ensembles de dimensions représentent des ensembles de dimensions avec deux enfants, etc.  

### Exemple 1  
 Le schéma suivant représente un arbre de recherche avec six ensembles de dimensions. Seule l’écriture d’ensemble de dimensions distinctive est affichée dans le schéma.  

 ![Exemple de structure arborescente des dimensions.](media/nav2013_dimension_tree.png "Exemple de structure arborescente des dimensions")  

 Le tableau suivant décrit une liste complète des écritures d’ensemble de dimensions qui constituent chaque ensemble de dimensions.  

|Ensembles de dimensions|Écritures de l’ensemble de dimensions|  
|--------------------|---------------------------|  
|Ensemble 0|Aucune|  
|Ensemble 1|AREA 30|  
|Ensemble 2|AREA 30, DEPT ADM|  
|Ensemble 3|AREA 30, DEPT PROD|  
|Ensemble 4|AREA 30, DEPT ADM, PROJ VW|  
|Ensemble 5|AREA 40|  
|Ensemble 6|AREA 40, PROJ VW|  

### Exemple 2  
 Cet exemple montre la manière dont [!INCLUDE[prod_short](includes/prod_short.md)] évalue si un ensemble de dimensions constitué des écritures de l’ensemble de dimensions AREA 40, DEPT PROD existe.  

 D’abord, [!INCLUDE[prod_short](includes/prod_short.md)] met également à jour la table **Nœud d’arbre ensemble de dimensions** pour s’assurer que l’arbre de recherche ressemble au schéma suivant. Ainsi, l’ensemble de dimensions 7 devient un enfant de l’ensemble de dimensions 5.  

 ![Exemple de structure arborescente des dimensions dans NAV 2013.](media/nav2013_dimension_tree_example2.png "Exemple de structure arborescente des dimensions dans NAV 2013")  

### Recherche de l’ID ensemble de dimensions  
 Au niveau conceptuel, **Code parent**, **Dimension** et **Section analytique**, dans l’arbre de recherche, sont combinés et sont utilisés comme clé primaire, car [!INCLUDE[prod_short](includes/prod_short.md)] parcourt l’arborescence dans le même ordre que les écritures analytiques. La fonction GET (enregistrement) est utilisée pour rechercher l’ID de l’ensemble de dimensions L’exemple de code suivant indique comment trouver l’ID d’ensemble de dimensions lorsqu’il existe trois sections analytiques.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

Toutefois, pour préserver la capacité de [!INCLUDE[prod_short](includes/prod_short.md)] à renommer à la fois un axe et une section analytique, la table 349 **Section analytique** est étendue avec un champ d’entier **ID section analytique**. Cette table convertit la paire de champs **Axe analytique** et **Section analytique** sur une valeur entière. Lorsque vous renommez la dimension et la valeur de dimension, la valeur d’entier n’est pas modifiée.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## Voir aussi
    
 [Détails de conception : écritures d’ensemble de dimensions](/dynamics365/business-central/design-details-dimension-set-entries-overview)   
 [Aperçu des écritures de l’ensemble de dimensions](design-details-dimension-set-entries-overview.md)   
 [Détails de conception : structure de la table](design-details-table-structure.md)   
 


[!INCLUDE[footer-include](includes/footer-banner.md)]