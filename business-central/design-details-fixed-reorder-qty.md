---
title: Détails de conception - Qté fixe de commande | Microsoft Docs
description: La méthode Qté fixe de commande est liée à la planification du stock des articles C courants (coûts de stock faible, faible risque d'obsolescence, et/ou plusieurs articles). Cette méthode est généralement utilisée conjointement avec un point de commande reflétant la demande anticipée lors du délai de l'article.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: dd8c4b8cdae3e004e30551798e5a68058b5c38fe
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307243"
---
# <a name="design-details-fixed-reorder-qty"></a>Détails de conception : qté fixe de commande.
La méthode Qté fixe de commande est liée à la planification du stock des articles C courants (coûts de stock faible, faible risque d'obsolescence, et/ou plusieurs articles). Cette méthode est généralement utilisée conjointement avec un point de commande reflétant la demande anticipée lors du délai de l'article.  

## <a name="calculated-per-time-bucket"></a>Calculé par intervalle de planification  
 Si le système de planification détecte que le point de commande est atteint ou traversé lors d'un intervalle de planification (cycle de commande), au-dessous ou sur le point de commande au début de la période et au-dessous ou sur le point de commande à la fin de la période, il propose de créer une commande fournisseur de la quantité de la commande spécifiée et ensuite la planifie à partir de la première date après la fin de l'intervalle de planification.  

 Le concept de point de commande délimité par un intervalle de planification réduit le nombre de suggestions d'approvisionnement. Cela reflète un processus manuel d'évaluation fréquente de l'entrepôt pour vérifier le contenu réel des différents emplacements.  

## <a name="creates-only-necessary-supply"></a>Crée uniquement l'approvisionnement nécessaire  
 Avant de proposer une commande approvisionnement pour répondre à un point de commande, le système de planification vérifie si l'approvisionnement a déjà été commandé pour être reçu dans le délai de réapprovisionnement de l'article. Si une commande approvisionnement existante résout le problème en amenant le stock prévisionnel à un niveau égal ou supérieur au point de commande dans le délai, le système ne suggère pas de nouvelle commande approvisionnement.  

 Les commandes approvisionnement qui sont créées spécifiquement pour répondre à un point de commande sont exclues de l'équilibrage ordinaire d'approvisionnement, et ne seront en aucun cas modifiées par la suite. Par conséquent, si un article utilisant un point de commande doit être éliminé (non réapprovisionné), il est recommandé d'étudier les commandes approvisionnement ouvertes manuellement ou de modifier la méthode de réapprovisionnement en Lot pour lot, le système peut alors réduire ou annuler l'approvisionnement superflu.  

## <a name="combines-with-order-modifiers"></a>Associe avec les modificateurs d'ordre  
 Les modificateurs de commande, qté minimum commande, qté maximum commande et multiple de commande, ne doivent pas jouer un grand rôle lorsque la stratégie de quantité fixe de commande est utilisée. Toutefois, le système de planification prend encore ces modificateurs en compte et diminue la quantité commande maximum spécifiée (et crée au moins deux approvisionnements pour atteindre la quantité commande totale), augmente la commande jusqu'à la quantité commande minimum spécifiée ou arrondit la quantité commandée pour répondre à un multiple spécifié de la commande.  

## <a name="combines-with-calendars"></a>Combinaison avec des calendriers  
 Avant de proposer une commande approvisionnement pour répondre à un point de commande, le système de planification vérifie si la commande est planifiée pour un jour chômé, en fonction des calendriers définis dans le champ **Code calendrier principal** des pages **Informations société** et **Fiche magasin**.  

 Si la date prévue est un jour chômé, le système de planification déplace la commande en aval à la date de travail la plus proche. Cela peut entraîner une commande qui satisfait un point de commande mais ne pas satisfait une certaine demande spécifique. Pour une telle demande non soldée, le système de planification crée un approvisionnement supplémentaire.  

## <a name="should-not-be-used-with-forecast"></a>Ne doit pas être utilisé avec la prévision  
 Étant donné que la demande prévue est déjà exprimée au niveau du point de commande il n'est pas nécessaire d'inclure une prévision dans la planification d'un article à l'aide d'un point de commande. S'il est important de baser le programme sur une prévision, utilisez la stratégie lot pour lot.  

## <a name="must-not-be-used-with-reservations"></a>Ne doit pas être utilisé avec les réservations  
 Si l'utilisateur a réservé une quantité, par exemple une quantité dans le stock, pour une certaine demande éloignée, la base de planification est dérangée. Même si le niveau de stock projeté est acceptable par rapport au point de réapprovisionnement, les quantités peuvent ne pas être disponibles. Le système peut essayer de compenser cela en créant des commandes exception ; toutefois, il est conseillé de définir le champ Reserve sur Never pour les articles prévus comme utilisant un point de commande.  

## <a name="see-also"></a>Voir aussi  
 [Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md)   
 [Détails de conception : qté maximum.](design-details-maximum-qty.md)   
 [Détails de conception : paramètres de planification](design-details-planning-parameters.md)   
 [Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
 [Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
