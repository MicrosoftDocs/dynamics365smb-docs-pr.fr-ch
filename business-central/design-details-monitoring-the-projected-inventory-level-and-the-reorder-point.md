---
title: "Détails de conception - Surveillance du niveau de stock prévisionnel et du point de commande | Microsoft Docs"
description: "Découvrez comment la planification de stock différencie les niveaux de stock prévisionnel des niveaux de stock disponible projeté."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5ee71f3c0a677115bba920e4b6d25eee6342e87e
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Détails de conception : surveillance du niveau de stock prévisionnel et du point de commande
Le stock est un type d'approvisionnement, mais pour la planification de stock, le système de planification différencie deux niveaux de stock :  

* Stock projeté  
* Stock disponible projeté  

## <a name="projected-inventory"></a>Stocks projetés  
Normalement, le stock prévisionnel est la quantité de stock brut, y compris les demandes et approvisionnements du passé même si non validés, au début du processus de planification. Dans le futur, cela devient un niveau de stock prévisionnel mobile qui est mis à jour par les quantités brutes d'un approvisionnement et d'une demande futurs parce que ceux-ci sont saisis suivant le planning (réservés ou affectés autrement).  

Le stock prévisionnel est utilisé par le système de planification pour contrôler le point de commande et pour déterminer la quantité de réapprovisionnement lorsque la méthode de réapprovisionnement Qté maximum est utilisée.  

## <a name="projected-available-inventory"></a>Stock disponible projeté  
Le stock disponible projeté est la partie du stock prévisionnel qui est disponible à un moment donné pour répondre à une demande. Le stock disponible projeté est utilisé par le moteur de planification lors du contrôle du niveau de stock de sécurité.  

Le stock disponible projeté est utilisé par le système de planification pour contrôler le niveau de stock de sécurité, parce que le stock de sécurité doit toujours être disponible pour satisfaire une demande inattendue.  

## <a name="time-buckets"></a>Intervalles de planification  
Posséder un contrôle étroit du stock prévisionnel est crucial pour détecter le moment où le point de commande est atteint et pour calculer la quantité de commande correcte en utilisant la méthode de réapprovisionnement Qté maximum.  

Comme indiqué précédemment, le niveau de stock projeté est calculé au début de la période de planification. Il s'agit d'un niveau brut qui ne tient pas compte des réservations et des ventilations similaires. Pour contrôler ce niveau de stock durant la séquence de planification, le système gère les changements cumulés sur une période de temps, un intervalle de planification. Le système garantit que l'intervalle de planification est au moins d'un jour comme il s'agit de l'unité de temps la plus précise pour une demande ou un événement d'approvisionnement.  

## <a name="determining-the-projected-inventory-level"></a>Déterminer le niveau de stock prévisionnel  
La prochaine séquence décrit la manière dont le niveau de stock prévisionnel est déterminé :  

* Lorsqu'un événement d'approvisionnement, tel qu'une commande achat, a été totalement planifié, il augmente le stock prévisionnel à sa date d'échéance.  
* Lorsqu'un événement de demande a été entièrement satisfait, il ne diminue pas le stock prévisionnel immédiatement. Au lieu de cela, il valide une relance de baisse, qui est un enregistrement interne qui contient la date et la quantité de la contribution au stock prévisionnel.  
* Lorsqu'un événement d'approvisionnement ultérieur est planifié et placé sur la chronologie, les rappels de diminution publiés sont examinés un à un jusqu'à la date d'approvisionnement planifiée tout en mettant à jour le stock prévisionnel. Lors de ce processus, le niveau du point de commande de la relance interne d'augmentation peut être atteint ou dépassé.  
* Si une nouvelle commande approvisionnement est créée, le système vérifie si elle est saisie avant l'approvisionnement actif. Si c'est le cas, le nouvel approvisionnement devient l'approvisionnement actif et la procédure d'équilibrage reprend depuis le début.  

Voici une illustration graphique de ce principe :  

![](media/nav_app_supply_planning_2_projected_inventory.png "NAV_APP_supply_planning_2_projected_inventory")  

1. L'approvisionnement **Sa** de 4 (fixe) clôture la demande **Da** de 3.  
2. CloseDemand : créez une relance de baisse de -3 (pas affiché).  
3. L'approvisionnement **Sa** est clôturé avec un excédent de 1 (plus aucune demande n'existe).  

     Cela augmente le niveau de stock prévisionnel à +4, alors que le stock **disponible** devient -1.  

4. L'approvisionnement suivant **Sb** de 2 (une autre commande) a déjà été placé dans la chronologie.  
5. Le système vérifie s'il y a des relances de sortie précédant **Sb** (il n'y en a pas, donc aucune action n'est prise).  
6. Le système ferme l'approvisionnement **Sb** (plus aucune demande n'existe)—A : en réduisant à 0 (annuler) ou B : en le laissant tel quel.  

     Cela entraîne l'augmentation du niveau de stock projeté (A : +0 => +4 or B : +2 = +6).  

7. Le système effectue un contrôle final : existe-t-il une relance de sortie ? Oui, il y en a un en date du **Da**.  
8. Le système ajoute le rappel de diminution -3 au niveau de stock projeté, soit A : +4 -3 = 1 or B : +6 -3 = +3.  
9. En cas de A, le système crée une commande planifiée en aval qui commence à la date **Da**.  

     Dans le cas de B, le point de commande est atteint et aucune commande n'est créée.  

## <a name="see-also"></a>Voir aussi  
[Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md)   
[Détails de conception : paramètres de planification](design-details-planning-parameters.md)   
[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)

