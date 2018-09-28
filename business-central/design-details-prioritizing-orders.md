---
title: "Détails de conception - Affecter une priorité aux commandes | Microsoft Docs"
description: "Découvrez comment affecter une priorité pour répondre à la demande et l'approvisionnement."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6e09ad64750493f99210d47516410d8471a83011
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-prioritizing-orders"></a>Détails de conception : Affecter une priorité aux commandes
Dans un point de stock donné, la date demandée ou disponible représente la priorité la plus élevée ; la demande du jour doit être traitée avant la demande de la semaine suivante. Mais en plus de cette priorité générale, le système de planification suggère également que le type de demande doit être rempli avant de répondre à une autre demande. De même, il suggère que la source d'approvisionnement soit lettrée avant d'appliquer d'autres sources d'approvisionnement. Ceci est effectué en fonction des priorités de la commande.  
  
La demande et l'approvisionnement chargés contribuent à un profil pour le stock prévisionnel en fonction des priorités suivantes :  
  
## <a name="priorities-on-the-demand-side"></a>Priorités du côté de la demande  
1. Déjà expédié : écriture comptable article  
2. Retour achat  
3. Ecriture réservation  
4. Commande service  
5. Besoin de composants de production  
6. Ligne d'ordre d'assemblage  
7. Commande désenlogement transfert  
8. Commande ouverte (qui n'a pas déjà été consommée par les commandes vente associées)  
9. Prévision (qui n'a pas déjà été consommée par d'autres commandes vente)  
  
> [!NOTE]  
>  Les retours achat ne sont généralement pas impliqués dans la planification d'approvisionnement ; ils doivent toujours être réservés à partir du lot qui va être retourné. S'il ne sont pas réservés, les retours achat jouent un rôle dans la disponibilité et sont classés en priorité élevée pour éviter que le système de planification suggère une commande approvisionnement uniquement pour servir un retour achat.  
  
## <a name="priorities-on-the-supply-side"></a>Priorités du côté de l'approvisionnement  
1. Déjà dans le stock : écriture comptable article (Flexibilité planification = Aucune)  
2. Retour vente (flexibilité de planification = aucune)  
3. Enlogement transfert  
4. Ordre de fabrication  
5. Ordre d'assemblage  
6. Commande achat  
  
## <a name="priority-related-to-the-state-of-demand-and-supply"></a>Priorité liée à l'état de la demande et de l'approvisionnement  
Outre les priorités accordées par le type d'offre et de demande, l'état actuel des commandes dans le processus d'exécution définit également une priorité. Par exemple, les activités entrepôt ont un effet et le statut des commandes vente, des commandes achat, des ordres de transfert, des ordres d'assemblage et des ordres de fabrication est pris en compte :  
  
1. En partie géré (flexibilité de planification = Aucune)  
2. Déjà en cours de traitement dans l'entrepôt (Flexibilité planification = Aucune)  
3. Lancé - tous types de commande (flexibilité de planification = illimitée)  
4. Ordre de fabrication planifié ferme (flexibilité de planification = illimitée)  
5. Planifié/ouvert - tous types de commande (flexibilité de planification = illimitée)  
  
## <a name="see-also"></a>Voir aussi  
[Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md)   
[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)   
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
