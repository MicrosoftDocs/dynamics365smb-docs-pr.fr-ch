---
title: Détails de conception - Le rôle du point de commande | Microsoft Docs
description: Cette rubrique met l'accent sur l'importance de définir un point de commande, afin de déterminer quand commander plus de stock.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 836da35166d947de8c37128d9ed8807914594c55
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "924202"
---
# <a name="design-details-the-role-of-the-reorder-point"></a>Détails de conception : Le rôle du point de commande
En plus de l'équilibrage général de la demande et de l'approvisionnement, le système de planification doit également contrôler les niveaux de stock des articles affectés pour respecter les méthodes de réapprovisionnement définies.  

Un point de commande représente la demande lors d'un délai. Lorsque le stock prévisionnel passe en dessous du niveau de stock défini par le point de commande, il est temps de commander une plus grande quantité. Par ailleurs, le stock doit diminuer progressivement et probablement atteindre zéro (ou le niveau de stock de sécurité), jusqu'à ce que le réapprovisionnement arrive.  

Par conséquent, le système de planification suggère une commande approvisionnement planifiée en aval au moment où le stock projeté passe sous le point de commande.  

Le point de commande indique un certain niveau de stock. Cependant, les niveaux de stock peuvent changer de façon significative au cours de l'intervalle de planification et, par conséquent, le système de planification doit constamment surveiller le stock disponible projeté.  

## <a name="see-also"></a>Voir aussi  
[Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md)   
[Détails de conception : paramètres de planification](design-details-planning-parameters.md)   
[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
