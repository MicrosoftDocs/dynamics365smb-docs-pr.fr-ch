---
title: "Aperçu des écritures de l'ensemble de dimensions | Microsoft Docs"
description: "Cette rubrique décrit comment les écritures de l'ensemble de dimensions sont stockées et validées dans Dynamics 365."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 927ec8c1379a3f03d5bd377e6cd3d21c66691a00
ms.contentlocale: fr-ch
ms.lasthandoff: 11/22/2018

---
# <a name="dimension-set-entries-overview"></a>Aperçu des écritures de l'ensemble de dimensions
Cette rubrique décrit comment les écritures de l'ensemble de dimensions sont stockées et validées dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="dimension-sets"></a>Ensembles de dimensions  
Un ensemble de dimensions est une combinaison unique de sections analytiques. Il est stocké comme des écritures de l'ensemble de dimensions dans la base de données. Chaque écriture de l'ensemble de dimensions représente une section analytique unique. L'ensemble de dimensions est identifié par un ID courant, qui est affecté à chaque écriture correspondante qui appartient à l'ensemble de dimensions.  

L'exemple suivant présente un ensemble de dimensions constitué de trois écritures. L'ensemble de dimensions est identifié par l'ID 108.  

|ID ensemble de dimensions|Code axe|Code section|Nom de la section analytique|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|ZONE|70|Amérique du Nord|  
|108|GROUPE COMPTABILISATION MARCHÉ|DÉBUT|Accueil|  
|108|DÉPARTEMENT|VENTES|Ventes|  

## <a name="dimension-set-entries"></a>Écritures de l'ensemble de dimensions  
Les ensembles de dimensions sont stockés dans la table **Écriture de l'ensemble de dimensions** telles des écritures de l'ensemble de dimensions avec le même ID.  

![Flux d'écritures d'ensemble de dimensions](media/dimensionentrynav7.png "Flux d'écritures d'ensemble de dimensions")  

Lorsque vous créez une ligne de feuille, un en-tête de document ou une ligne de document, vous pouvez spécifier une combinaison de sections analytiques. Au lieu d'enregistrer explicitement chaque section analytique dans la base de données, un ID d'ensemble de dimensions est affecté à la ligne de feuille, à l'en-tête du document ou à la ligne du document pour spécifier l'ensemble de dimensions.  

Lorsque vous modifiez et fermez la page **Modifier les écritures de l'ensemble de dimensions**, une vérification est exécutée pour voir si la combinaison de sections analytiques existe comme un ensemble de dimensions dans la table. Si la combinaison se produit dans la table, l'ID d'ensemble de dimensions correspondant est affecté à la ligne de feuille, à l'en-tête du document ou à la ligne du document. Sinon, un nouvel ensemble de dimensions est ajouté à la table, et le nouvel ID d'ensemble de dimensions est affecté à la ligne de feuille, à l'en-tête du document ou à la ligne du document.  

## <a name="performance-improvement"></a>Amélioration des performances  
Pour enregistrer les axes analytiques dans la base de données, l'espace de la base de données est conservé et les performances globales sont améliorées.  

## <a name="see-also"></a>Voir aussi  
[Détails de conception : recherche des croisements analytiques](design-details-searching-for-dimension-combinations.md)   
[Détails de conception : structure de la table](design-details-table-structure.md)   
[Détails de conception : Codeunit 408 Gestion des axes analytiques](design-details-codeunit-408-dimension-management.md)   
[Détails de conception : exemples de code de motifs modifiés dans les modifications](design-details-code-examples-of-changed-patterns-in-modifications.md)   
[Détails de conception : écritures d'ensemble de dimensions](design-details-dimension-set-entries.md)   

