---
title: Planifications des approvisionnements
description: Préparez un programme exécutable détaillé ainsi que la planification de production de l’assemblage final pour la demande de vente et de production.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.for: '291, 292, 293, 295, 517, 9010, 9038'
ms.date: 04/01/2021
ms.author: edupont
---
# Planning

Les opérations de production nécessaires à la transformation d’entrées en produits finis doivent être planifiées de manière quotidienne ou hebdomadaire en fonction du volume et de la nature des produits. [!INCLUDE[prod_short](includes/prod_short.md)] fournit des fonctionnalités permettant de répondre à la demande réelle et anticipée des ventes, de l’assemblage et de la production, et inclut des fonctionnalités pour une planification de la distribution basée sur les points de stock et les transferts d’emplacement.

> [!NOTE]
> Cette rubrique décrit essentiellement la planification des sociétés impliquées dans la fabrication ou la gestion des assemblages, où les commandes approvisionnement qui en résultent peuvent être des ordres de production, d’assemblage, de transfert ou des commandes achat. L’interface principale de cette tâche de planification est la page **Feuille planning**.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] prend également en charge la planification de l’approvisionnement pour les sociétés de vente en gros, où les commandes approvisionnement qui en résultent peuvent être des ordres de transfert et des commandes achat. L’interface principale de cette tâche de planification est la page **Demande achat**, qui est décrite indirectement dans cette rubrique, car la plupart des fonctionnalités de planification s’appliquent aux deux feuilles.

La planification peut être considérée comme la préparation des commandes approvisionnement requises dans les départements d’achat, d’assemblage ou de fabrication pour répondre à la demande de vente ou d’articles finis. Pour plus d’informations, voir [Achats](purchasing-manage-purchasing.md), [Gestion des assemblages](assembly-assemble-items.md) et [Production](production-manage-manufacturing.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|  
|Apprendre à utiliser le système de planification pour détecter la demande et lui donner la priorité et pour proposer un programme d’approvisionnement équilibré.|[À propos de la fonctionnalité Planification](production-about-planning-functionality.md)|
|Comprendre tous les aspects du système de planification et modifier les algorithmes pour répondre aux exigences de planification dans différents environnements.|[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)|
|Apprendre comment la logique de planification différencie la demande dans les magasins en fonction de la configuration des points de vente de la demande sans code magasin.|[Planification avec/sans magasin](production-planning-with-without-locations.md)|
|Prévoir la demande présentée par les composants vente et fabrication prévus.|[Créer une prévision de la demande](production-how-to-create-a-forecast.md)|  
|Créer des ordres de fabrication de projet ou un à un à partir d’une commande vente pour couvrir la demande exacte des commandes vente.|[Créer des ordres de fabrication à partir de commandes achat](production-how-to-create-production-orders-from-sales-orders.md)|
|Utiliser la page **Planification commande** pour effectuer la planification manuellement pour des ordres de vente ou de fabrication un niveau de nomenclature de production à la fois.|[Planifier de nouvelles demandes commande par commande](production-how-to-plan-for-new-demand.md)|
|Utiliser la page **Feuille planning** pour exécuter les options PDP et MRP pour créer automatiquement un programme d’approvisionnement détaillé à tous les niveaux d’article.|[Exécuter une planification complète et un calcul PDP ou MRP](production-how-to-run-mps-and-mrp.md)|
|Utilisez la page **Demande achat** pour créer automatiquement un programme d’approvisionnement détaillé pour répondre à la demande d’articles réapprovisionnés uniquement par achat ou transfert.|[Demande achat](production-about-planning-functionality.md#requisition-worksheet)|  
|Lancer ou mettre à jour un ordre de fabrication en tant qu’opérations planifiées approximativement dans la planification de production.|[Replanifier ou actualiser directement des ordres de fabrication](production-how-to-replan-refresh-production-orders.md)|
|Recalculer les calendriers de centre de charge ou de poste de charge en raison de changements de planning.|[Pour calculer un calendrier de centre de charge](production-how-to-create-work-center-calendars.md#to-calculate-a-work-center-calendar)|
|Suivre la demande de commande (quantité chaînée), les prévisions, les commandes ouvertes vente ou les paramètres de planification (quantité non chaînée) qui ont donné lieu à la ligne planning en question.|[Suivre les relations entre l’offre et la demande](production-how-track-demand-supply.md)|
|Afficher le stock disponible prévu sous différents types d’affichage et voir quels besoins bruts, réceptions de commandes planifiées et autres événements l’influencent dans le temps.|[Voir la disponibilité des articles](inventory-how-availability-overview.md)|  
<!--|Effectuer des activités de planification sélectionnées, comme la modification ou l’ajout de lignes feuille planning, dans une vue graphique du programme d’approvisionnement.|[Modifier les propositions planning dans une vue graphique](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|-->

## Voir la [formation Microsoft](/training/modules/plan-items-dynamics-365-business-central/) associée

## Voir aussi

[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)  
[Pratiques de configuration recommandées : planification de l’approvisionnement](setup-best-practices-supply-planning.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
