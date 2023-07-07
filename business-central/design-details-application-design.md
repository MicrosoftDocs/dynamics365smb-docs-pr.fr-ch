---
title: Détails de conception de l’application
description: Ce contenu comprend des informations techniques détaillées sur les fonctionnalités d’application complexes dans Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/26/2021
ms.author: edupont
---
# <a name="application-design-details"></a>Détails de conception de l’application

Les articles de cette section contiennent des informations techniques détaillées sur les fonctionnalités d’application complexes dans [!INCLUDE[prod_short](includes/prod_short.md)].  

Le contenu des détails de conception est destiné aux implémenteurs, développeurs et super utilisateurs qui ont besoin d’une analyse approfondie pour implémenter, personnaliser ou créer les fonctionnalités en question.  

|**Pour**|**Voir**|  
|------------|-------------|  
|Comprenez les mécanismes dans le moteur d’évaluation, comme le mode d’évaluation et l’ajustement des coûts, et pour quels principes de compatibilité ils sont conçus.|[Détails de conception : Évaluation stock](design-details-inventory-costing.md)|  
|Découvrez comment le traitement par lots Ajuster coûts - Écr. article identifie et affecte une date comptabilisation aux écritures valeur que le traitement par lots est sur le point de créer.|[Détails de conception : date comptabilisation de l’écriture valeur d’ajustement](design-details-inventory-adjustment-value-entry-posting-date.md)|
|En savoir plus sur la conception des axes de stockage et validation, notamment des exemples code sur la façon de migrer et mettre à niveau le code axe analytique.|[Détails de conception : écritures d’ensemble de dimensions](design-details-dimension-set-entries-overview.md)|
|En savoir plus sur la manière dont le système de planification fonctionne et comment modifier les algorithmes pour répondre aux exigences de planification dans différents environnements.|[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)|  
|Découvrez comment le système conserve un contrôle constant sur la disponibilité des articles dans l’entrepôt, afin que les commandes sortantes puissent s’écouler efficacement et assurer des livraisons optimales.|[Détails de conception : disponibilité dans l’entrepôt](design-details-availability-in-the-warehouse.md)|
|En savoir plus sur l’historique et la conception actuelle de la fonctionnalité de traçabilité et la manière dont elle s’intègre avec le système de réservation pour inclure les numéros de série/lot dans les calculs de disponibilité.|[Détails de conception : traçabilité](design-details-item-tracking.md)|  
|En savoir plus sur la fonction de ligne validation de feuille comptabilité.|[Détails de conception : Ligne validation de feuille comptabilité](design-details-general-journal-post-line.md)|

## <a name="see-also"></a>Voir aussi

[Planifié](production-planning.md)  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Configuration des modules complexes à l’aide des meilleures pratiques](set-up-complex-application-areas-using-best-practices.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]
