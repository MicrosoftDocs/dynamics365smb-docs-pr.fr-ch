---
title: "Configuration des processus entrepôt | Microsoft Docs"
description: "La stratégie de distribution d'une société se reflète dans la configuration de ses processus entrepôt : cela inclut la définition de la manière dont différents articles sont traités dans différents entrepôts (par exemple, degré de contrôle des emplacements et étendue du flux requis entre les activités entrepôt)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 130d266d5e9ff5a4d862dd9a03a781b57afd52be
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-warehouse-management"></a>Configuration de la gestion des entrepôts
La stratégie de distribution d'une société se reflète dans la configuration de ses processus entrepôt : cela inclut la définition de la manière dont différents articles sont traités dans différents entrepôts (par exemple, degré de contrôle des emplacements et étendue du flux requis entre les activités entrepôt).  

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.   

|**Pour**|**Voir**|  
|------------|-------------|  
|Obtenir un aperçu des capacités de base par rapport à la fonctionnalité de stockage avancée.|[Détails de conception : vue d'ensemble d'entrepôt](design-details-warehouse-overview.md)|  
|Configurer huit types d'emplacement (emplacement prélèvement, par exemple) pour définir les activités circulation associées à chaque type d'emplacement.|[Procédure : configurer des types d'analyse](warehouse-how-to-set-up-bin-types.md)|  
|Créez des emplacements manuellement ou automatiquement avec des informations (nom, souches de numéros et catégorie) sur la base d'un modèle emplacement.|[Procédure : créer des emplacements](warehouse-how-to-create-individual-bins.md)|  
|Définir quels articles vous souhaitez stocker dans un emplacement donné et définir les règles devant être suivies lors du remplissage de l'emplacement avec un article spécifique.|[Procédure : créer le contenu d'un emplacement](warehouse-how-to-set-up-bin-contents.md)|  
|Définir un article de sorte qu'il soit toujours stocké dans un emplacement spécifique.|[Comment affecter des emplacements par défaut à des articles](warehouse-how-to-assign-default-bins-to-items.md)|
|Créer des modèles pour gérer l'emplacement et le mode de rangement des articles dans le cadre du rangement suggéré.|[Procédure : configurer des modèles rangement](warehouse-how-to-set-up-put-away-templates.md)|
|Définir des utilisateurs comme employés d'entrepôts spécifiques.|[Procédure : configurer des employés d'entrepôt](warehouse-how-to-set-up-warehouse-employees.md)|
|Définir différents types d'emplacement dans l'entrepôt pour contrôler l'emplacement des articles sur la base de leur type, priorité ou niveau de traitement.|[Comment configurer des magasins de sorte qu'ils utilisent des emplacements](warehouse-how-to-set-up-locations-to-use-bins.md)|
|Définir des paramètres supplémentaires pour un magasin existant afin de l'activer pour les activités entrepôt.|[Procédure : convertir des magasins existants en magasins entrepôt](warehouse-how-to-convert-existing-locations-to-warehouse-locations.md)|
|Activez le prélèvement, le déplacement et le rangement des ordres d'assemblage ou de fabrication dans des configurations de stockage de base.|[Comment configurer des entrepôts de base avec les zones d'opérations](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|  
|Configurez des articles et des magasins pour la portée de gestion d'entrepôt la plus avancée dans laquelle toutes les activités doivent suivre un flux strict.|[Procédure : configurer des articles et des emplacements pour prélèvement et rangement suggérés](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md)|  
|Définir la date et le mode d'inventaire des articles dans les entrepôts à des fins de maintenance ou de génération d'états financiers.|[Procédure : Inventaire, ajustement ou reclassement du stock](inventory-how-count-adjust-reclassify.md)|
|Permettez aux magasiniers de diviser une unité plus grande en unités de plus petite taille afin de répondre aux besoins des documents origine.|[Procédure : activer la rupture de charge automatique avec prélèvement et rangement dirigé](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)|  
|Configurer l'entrepôt de manière à ce qu'il suggère automatiquement les articles à prélever qui expirent en premier.|[Procédure : activer le prélèvement par FEFO](warehouse-picking-by-fefo.md)|
|Intégrez les lecteurs de code barres à votre solution de gestion d'entrepôt.|[Utilisation des systèmes de saisie automatisée (ADCS)](warehouse-use-automated-data-capture-systems-adcs.md)|  
|Obtenir des conseils relatifs à la réorganisation des magasins, emplacements ou zones pour générer des activités entrepôt plus efficaces.|[Comment restructurer les entrepôts](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Voir aussi  
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

