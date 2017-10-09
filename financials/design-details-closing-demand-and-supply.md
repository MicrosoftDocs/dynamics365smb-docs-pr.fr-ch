---
title: "Détails de conception - Clôture de la demande et de l'approvisionnement | Microsoft Docs"
description: "Cette rubrique suggère des tâches à effectuer une fois les procédures d'équilibrage d'approvisionnement exécutées."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, planning, example, closing, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0796865fa5b04630cc3ac68a63cc8113664a2d24
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-closing-demand-and-supply"></a>Détails de conception : clôture de la demande et de l'approvisionnement
Lorsque les procédures d'équilibre d'approvisionnement ont été réalisées, il existe trois situations de fin possibles :  
  
* La quantité et la date requises des événements de demande ont été respectées et leur planification peut être clôturée. L'événement d'approvisionnement est encore ouvert et peut couvrir la demande suivante, donc la procédure de contrepartie peut recommencer avec l'événement d'approvisionnement actif et la demande suivante.  
* La commande approvisionnement ne peut pas être modifiée pour couvrir l'ensemble de la demande. L'événement demande est encore ouvert, avec une certaine quantité non couverte qui peut être couverte par l'événement suivant d'approvisionnement. Ainsi, l'événement d'approvisionnement actuel est fermé, donc l'acte d'équilibrage peut recommencer avec la demande actuelle et l'événement d'approvisionnement suivant.  
* L'ensemble de la demande a été couvert ; il n'existe aucune demande suivante (ou il n'y a pas de demande du tout). S'il y a un approvisionnement excédentaire, il peut être diminué (ou annulé), puis être clôturé. Il est possible que des événements d'approvisionnement supplémentaires existent plus loin dans la chaîne, et ils doivent également être annulés.  
  
Enfin, le système de planification crée un lien de chaînage entre l'approvisionnement et la demande.  
  
## <a name="creating-the-planning-line-suggested-action"></a>Création de la ligne planning (action suggérée)  
Si une action quelconque (Nouveau, Changer qté, Replanifier, Replanifier et changer qté ou Annuler) est suggérée pour modifier la commande approvisionnement, le système de planification crée une ligne planning dans la feuille planning. En raison du chaînage, la ligne planification est créée non seulement lorsque l'événement d'approvisionnement est clôturé, mais également si l'événement de demande est clôturé, même si l'événement d'approvisionnement est encore ouvert et qu'il peut être soumis à des modifications supplémentaires lorsque l'événement de demande suivant est traité. Cela signifie qu'après sa création, la ligne de planification peut être modifiée à nouveau.  
  
Pour réduire l'accès aux bases de données lors du traitement des ordres de fabrication, la ligne de planification peut être maintenue dans trois niveaux, tout en visant à effectuer le niveau de maintenance le moins exigeant :  
  
* Créer uniquement la ligne planning avec la date d'échéance et la quantité actuelles mais sans gamme et composants.  
* Inclure la gamme : la gamme planifiée est présentée avec le calcul des dates et heures de début et de fin. Ceci est exigeant en termes d'accès aux bases de données. Pour déterminer les dates de fin et d'échéance, il peut être nécessaire de calculer ceci même si l'événement d'approvisionnement n'a pas été clôturé (dans le cas d'une planification en aval).  
* Inclure l'éclatement de la nomenclature : ceci peut attendre juste avant que l'événement approvisionnement soit clôturé.  
  
Cela conclut les descriptions de la manière dont la demande et l'approvisionnement sont chargés, priorisés et équilibrés par le système de planification. En association avec cette activité de planification des approvisionnements, le système doit veiller à ce que le niveau de stock requis de chaque article soit maintenu en fonction de ses méthodes de réapprovisionnement.  
  
## <a name="see-also"></a>Voir aussi  
[Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md)   
[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)   
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
