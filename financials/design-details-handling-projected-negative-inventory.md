---
title: "Détails de conception - Traitement du stock prévisionnel négatif | Microsoft Docs"
description: "Le point de commande exprime la demande anticipée lors du délai de l'article. Lorsque le point de commande est passé, il est temps de commander plus. Mais le stock prévisionnel doit être suffisamment élevé pour couvrir la demande jusqu'à ce que la commande soit reçue. Par ailleurs, le stock de sécurité doit se charger des fluctuations de la demande jusqu'à un niveau de service ciblé."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3436e2a00858a1dbfcbb0a44cb9db32bd7665593
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-handling-projected-negative-inventory"></a>Détails de conception : traitement du stock prévisionnel négatif
Le point de commande exprime la demande anticipée lors du délai de l'article. Lorsque le point de commande est passé, il est temps de commander plus. Mais le stock prévisionnel doit être suffisamment élevé pour couvrir la demande jusqu'à ce que la commande soit reçue. Par ailleurs, le stock de sécurité doit se charger des fluctuations de la demande jusqu'à un niveau de service ciblé.  

 Par conséquent, le système de planification considère comme une urgence si une demande future ne peut pas être servie à partir du stock prévisionnel, ou exprimé d'une autre manière, si le stock prévisionnel devient négatif. Le système traite une telle exception en suggérant une nouvelle commande d'approvisionnement pour satisfaire la partie de la demande qui ne peut pas être satisfaite par le stock ou un autre approvisionnement. La taille de la nouvelle commande approvisionnement ne prend pas en compte le stock maximum ou la quantité de réappro., ni les modificateurs de commande qté maximum commande, qté minimum commande et multiple de commande. Au lieu de cela, elle reflète l'insuffisance exacte.  

 La ligne planning de ce type de commande approvisionnement affiche une icône d'avertissement Urgence, et des informations supplémentaires sont fournies lors de la recherche pour informer l'utilisateur de la situation.  

 Dans la figure suivante, l'approvisionnement D représente une commande d'urgence pour ajuster le stock négatif.  

 ![](media/nav_app_supply_planning_2_negative_inventory.png "NAV_APP_supply_planning_2_negative_inventory")  

1.  L'approvisionnement **A**, stock prévisionnel initial, est inférieur au point de commande.  

2.  Un approvisionnement planifié en aval est créé (**C**).  

     (Quantité = Stock maximum – Niveau de stock projeté)  

3.  L'approvisionnement **A** est clôturé par la demande **B** qui n'est pas totalement couverte.  

     (La demande **B** peut tenter de planifier l'approvisionnement C mais cela ne se produira pas en raison du concept d'intervalle de planification.)  

4.  Un nouvel approvisionnement (**D**) est créé pour couvrir la quantité restante sur demande **B**.  

5.  La demande **B** est clôturée (création d'une relance dans le stock prévisionnel).  

6.  Le nouvel approvisionnement **D** est clôturé.  

7.  Le stock prévisionnel est vérifié ; le point de commande n'a pas été dépassé.  

8.  L'approvisionnement **C** est clôturé (plus aucune demande n'existe).  

9. Vérification finale : aucun relance restante de niveau de stock.  

> [!NOTE]  
>  L'étape 4 indique la manière dont le système réagit dans les versions antérieures à Microsoft Dynamics NAV 2009 SP1.  

 Cela conclut la description des principes centraux en relation avec la planification de stock sur la base de les méthodes de réapprovisionnement. La section suivante décrit les caractéristiques des quatre méthodes de réapprovisionnement prises en charge.  

## <a name="see-also"></a>Voir aussi  
 [Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md)   
 [Détails de conception : paramètres de planification](design-details-planning-parameters.md)   
 [Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
 [Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)

