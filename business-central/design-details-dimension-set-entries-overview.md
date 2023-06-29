---
title: Aperçu des écritures de l’ensemble de dimensions
description: Cet article vous donne un aperçu de la manière dont les entrées d’ensemble de dimensions sont stockées et comment elles sont publiées.
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 06/14/2021
ms.author: edupont
---
# <a name="dimension-set-entries-overview"></a><a name="dimension-set-entries-overview"></a>Aperçu des écritures de l’ensemble de dimensions
Cette rubrique décrit comment les écritures de l’ensemble de dimensions sont stockées et validées dans [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="dimension-sets"></a><a name="dimension-sets"></a>Ensembles de dimensions
Un ensemble de dimensions est une combinaison unique de sections analytiques. Il est stocké comme des écritures de l’ensemble de dimensions dans la base de données. Chaque écriture de l’ensemble de dimensions représente une section analytique unique. L’ensemble de dimensions est identifié par un ID courant, qui est affecté à chaque écriture correspondante qui appartient à l’ensemble de dimensions.  

L’exemple suivant présente un ensemble de dimensions constitué de trois écritures. L’ensemble de dimensions est identifié par l’ID 108.  

|ID ensemble de dimensions|Code axe|Code section|Nom de la section analytique|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|ZONE|70|Amérique du Nord|  
|108|GROUPE COMPTABILISATION MARCHÉ|DÉBUT|Accueil|  
|108|DÉPARTEMENT|VENTES|Ventes|  

## <a name="dimension-set-entries"></a><a name="dimension-set-entries"></a>Écritures de l’ensemble de dimensions
Les ensembles de dimensions sont stockés dans la table **Écriture de l’ensemble de dimensions** telles des écritures de l’ensemble de dimensions avec le même ID.  

![Flux des écritures de l’ensemble de dimensions.](media/dimensionentrynav7.png "Flux des écritures de l’ensemble de dimensions")  

Lorsque vous créez une ligne de feuille, un en-tête de document ou une ligne de document, vous pouvez spécifier une combinaison de sections analytiques. Au lieu d’enregistrer explicitement chaque section analytique dans la base de données, un ID d’ensemble de dimensions est affecté à la ligne de feuille, à l’en-tête du document ou à la ligne du document pour spécifier l’ensemble de dimensions.  

Lorsque vous modifiez et fermez la page **Modifier les écritures de l’ensemble de dimensions**, une vérification est exécutée pour voir si la combinaison de sections analytiques existe comme un ensemble de dimensions dans la table. Si la combinaison se produit dans la table, l’ID d’ensemble de dimensions correspondant est affecté à la ligne de feuille, à l’en-tête du document ou à la ligne du document. Sinon, un nouvel ensemble de dimensions est ajouté à la table, et le nouvel ID d’ensemble de dimensions est affecté à la ligne de feuille, à l’en-tête du document ou à la ligne du document.

## <a name="codeunit-408-dimension-management"></a><a name="codeunit-408-dimension-management"></a>Codeunit 408 Gestion des axes analytiques
Codeunit 408 Gestion des axes analytiques est une bibliothèque de fonctions qui gère les tâches courantes qui sont liées aux axes analytiques, tels que copier d’une table à une autre ou d’un document à un autre.

## <a name="performance-improvement"></a><a name="performance-improvement"></a>Amélioration des performances
Pour enregistrer les axes analytiques dans la base de données, l’espace de la base de données est conservé et les performances globales sont améliorées.  

## <a name="see-also"></a><a name="see-also"></a>Voir aussi
[Détails de conception : recherche des croisements analytiques](design-details-searching-for-dimension-combinations.md)   
[Détails de conception : structure de la table](design-details-table-structure.md)   
[Détails de conception : écritures d’ensemble de dimensions](/dynamics365/business-central/design-details-dimension-set-entries-overview)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
