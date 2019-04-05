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
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: e39a7efdc796e8745bd9d8f7d74cdcfb171d851f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821656"
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
