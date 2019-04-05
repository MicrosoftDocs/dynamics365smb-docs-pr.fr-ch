---
title: Détails de conception - Traiter les commandes avant la date début de la planification | Microsoft Docs
description: Cette rubrique décrit les règles appliquées par la planification aux commandes dans la zone gelée.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 9fee9eff60b441ef2d4782a77a6fbbbe8b01af03
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821121"
---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a>Détails de conception : traiter les commandes avant la date début de la planification
Pour éviter qu'un programme d'approvisionnement affiche des suggestions impossibles et donc inutiles, le système de planification considère la période jusqu'à la date de début de la planification comme une zone gelée pour laquelle rien n'est programmé. La règle suivante s'applique à la zone gelée :  

L'ensemble de l'offre et de la demande antérieur à la date de début de la période de planification sera considéré comme faisant partie du stock ou comme étant expédié.  

Par conséquent, le système de planification, à quelques exceptions près, ne va suggérer aucune modification des commandes approvisionnement de la zone gelée. Par ailleurs, aucun lien de chaînage n'est créé ou mis à jour pour cette période.  

Les exceptions à cette règle sont les suivantes :  

* Si le stock disponible projeté, y compris la somme de la demande et de l'approvisionnement dans la zone gelée, est inférieur à zéro.  
* Si les numéros de série/lot sont nécessaires sur la ou les commandes antidatées.  
* Si l'ensemble demande-approvisionnement est lié par une stratégie ordre pour ordre.  

Si le stock disponible d'origine est inférieur à zéro, le système de planification suggère une commande approvisionnement d'urgence la veille de la période de planification pour couvrir la quantité manquante. Par conséquent, le stock disponible projeté est toujours au moins à zéro lorsque la planification de la période future commence. La ligne planning de cette commande approvisionnement affiche une icône d'avertissement Urgence et des informations supplémentaires sont fournies lors de la recherche.  

## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Les numéros de série et/ou de lot et les liens ordre pour ordre sont exempts de la zone gelée  
Si les numéros de série/lot sont requis ou si un lien ordre pour ordre existe, le système de planification ignore la zone gelée et incorpore ces quantités antidatées à partir de la date début et propose éventuellement des actions de correction si la demande et l'approvisionnement ne sont pas synchronisés. La raison commerciale de ce principe est que ces ensembles approvisionnement-demande spécifiques doivent correspondre pour garantir que cette demande spécifique soit satisfaite.  

## <a name="see-also"></a>Voir aussi  
[Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md)   
[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)   
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
