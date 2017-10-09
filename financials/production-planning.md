---
title: Planification de l'approvisionnement| Microsoft Docs
description: "Préparez un programme exécutable détaillé ainsi que la planification de production de l'assemblage final pour la demande de vente et de production."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b2a4a682100b0963b540f6f032c4b90061265cc1
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="planning"></a>Planning
Les opérations de production nécessaires à la transformation d'entrées en produits finis doivent être planifiées de manière quotidienne ou hebdomadaire en fonction du volume et de la nature des produits. [!INCLUDE[d365fin](includes/d365fin_md.md)] fournit des fonctionnalités permettant de répondre à la demande réelle et anticipée des ventes, de l'assemblage et de la production, et inclut des fonctionnalités pour une planification de la distribution basée sur les points de stock et les transferts d'emplacement.

> [!NOTE]
> Cette rubrique décrit essentiellement la planification des sociétés impliquées dans la fabrication ou la gestion des assemblages, où les commandes approvisionnement qui en résultent peuvent être des ordres de production, d'assemblage, de transfert ou des commandes achat. L'interface principale de cette tâche de planification est la fenêtre **Feuille planning**.

> [!INCLUDE[d365fin](includes/d365fin_md.md)] prend également en charge la planification de l'approvisionnement pour les sociétés de vente en gros, où les commandes approvisionnement qui en résultent peuvent être des ordres de transfert et des commandes achat. L'interface principale de cette tâche de planification est la fenêtre **Demande achat**, qui est décrite indirectement dans cette rubrique, car la plupart des fonctionnalités de planification s'appliquent aux deux feuilles.

Avant de planifier et d'exécuter des ordres de fabrication, vous devez configurer des capacités de production, telles que la création des calendriers usine, des gammes, des nomenclatures et des postes de charge. Pour plus d'informations, voir [Paramétrage de la production](production-configure-production-processes.md).

La planification peut être considérée comme la préparation des commandes approvisionnement requises dans les départements d'assemblage ou de fabrication pour répondre à la demande. Pour plus d'informations, voir [Gestion des assemblages](assembly-assemble-items.md) et [Production](production-manage-manufacturing.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.   

|**Pour**|**Voir**|  
|------------|-------------|  
|Apprendre à utiliser le système de planification pour détecter la demande et lui donner la priorité et pour proposer un programme d'approvisionnement équilibré.|[À propos de la fonctionnalité Planification](production-about-planning-functionality.md)|
|Comprendre tous les aspects du système de planification et modifier les algorithmes pour répondre aux exigences de planification dans différents environnements.|[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)|
|Apprendre comment la logique de planification différencie la demande dans les magasins en fonction de la configuration des points de vente de la demande sans code magasin.|[Planification avec/sans magasin](production-planning-with-without-locations.md).|
|Prévoir la demande de production présentée par les commandes vente et les ordres de fabrication prévus.|[Procédure : créer une prévision production](production-how-to-create-a-forecast.md)|  
|Créer automatiquement des ordres de fabrication un à un à partir d'une commande vente pour couvrir la demande exacte des lignes commande vente.|[Procédure : créer des ordres de fabrication à partir de commandes vente](production-how-to-create-production-orders-from-sales-orders.md)|
|Créer un ordre de fabrication projet directement à partir d'une commande vente multiligne représentant un projet de production.|[Procédure : planifier les projets de commandes](production-how-to-plan-project-orders.md)|
|Utiliser la fenêtre **Planification commande** pour effectuer la planification manuellement pour des ordres de vente ou de fabrication un niveau de nomenclature de production à la fois.|[Procédure : planifier de nouvelles demandes commande par commande](production-how-to-plan-for-new-demand.md)|
|Utiliser la fenêtre **Feuille planning** pour exécuter les options PDP et MRP pour créer automatiquement un programme d'approvisionnement détaillé à tous les niveaux d'article.|[Procédure : exécuter une planification complète et un calcul PDP ou MRP](production-how-to-run-mps-and-mrp.md)|
|Exécuter la demande achat pour créer automatiquement un programme d'approvisionnement détaillé pour répondre à la demande d'articles réapprovisionnés uniquement par achat ou transfert.|Page **Demande achat**|  
|Lancer ou mettre à jour un ordre de fabrication en tant qu'opérations planifiées approximativement dans la planification de production.|[Procédure : replanifier ou actualiser directement des ordres de fabrication](production-how-to-replan-refresh-production-orders.md)|
|Recalculer les calendriers de centre de charge ou de poste de charge en raison de changements de planning.|Section « Pour calculer un calendrier de centre de charge » dans [Procédure : configurer des calendriers usine](production-how-to-create-work-center-calendars.md)|
|Suivre la demande de commande (quantité chaînée), les prévisions, les commandes ouvertes vente ou les paramètres de planification (quantité non chaînée) qui ont donné lieu à la ligne planning en question.|[Procédure : suivre les relations entre l'offre et la demande](production-how-track-demand-supply.md)|
|Afficher le stock disponible prévu sous différents types d'affichage et voir quels besoins bruts, réceptions de commandes planifiées et autres événements l'influencent dans le temps.|[Procédure : voir la disponibilité des articles](inventory-how-availability-overview.md)|  
|Effectuer des activités de planification sélectionnées, comme la modification ou l'ajout de lignes feuille planning, dans une vue graphique du programme d'approvisionnement.|[Procédure : modifier les propositions planning dans une vue graphique](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## <a name="see-also"></a>Voir aussi
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)   
[Pratiques de configuration recommandées : planification de l'approvisionnement](setup-best-practices-supply-planning.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

