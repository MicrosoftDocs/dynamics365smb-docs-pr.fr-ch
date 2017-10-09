---
title: "Détails de conception - Commande | Microsoft Docs"
description: "Cette rubrique fournit des informations sur les liens commande-à-commande dans un environnement de fabrication à la commande."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 24f5c56e9e148128d83593757d820fa62686403e
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-order"></a>Détails de conception : commande
Dans un environnement de fabrication à la commande, un article est acheté ou produit pour couvrir exclusivement une demande spécifique. Généralement, il se rapporte aux articles A, et la motivation pour choisir cette méthode de réapprovisionnement de commande peut être que la demande n'est pas fréquente, le délai de production est insignifiant ou les attributs requis varient.  
  
Le programme crée un lien ordre pour ordre, qui agit en tant que connexion préliminaire entre l'approvisionnement, une commande approvisionnement ou un stock, et la demande qu'il va traiter.  
  
Outre l'utilisation de la méthode de commande, le lien ordre pour ordre peut s'appliquer lors de la planification, comme suit :  
  
* Lors de l'utilisation de la méthode de fabrication Make-to-Order pour créer des ordres de fabrication de type multi-niveau ou projet (la production avait besoin de composants sur le même ordre de fabrication).  
* Lors de l'utilisation de la fonction Sales Order Planning pour créer un ordre de fabrication à partir d'une commande vente.  
  
Même si une société manufacturière se considère comme un environnement de fabrication à la commande, il peut être préférable d'utiliser la méthode de réapprovisionnement Lot pour lot si les articles sont des standards purs sans variation dans les attributs. Par conséquent, le système utilise le stock non planifié et additionne uniquement les commandes vente ayant la même date d'expédition ou faisant partie d'un intervalle de planification défini.  
  
## <a name="order-to-order-links-and-past-due-dates"></a>Liens ordre pour ordre et dates arriérées  
Contrairement à la plupart des ensemble approvisionnement-demande, les commandes liées avec des dates d'échéance antérieures à la date de début de la planification sont entièrement planifiées par le système. La raison commerciale de cette exception est que les ensembles spécifiques approvisionnement-demande doivent être synchronisés jusqu'à l'exécution. Pour plus d'informations sur la zone gelée qui s'applique à la plupart des types de demande-approvisionnement, voir [Détails de conception : traiter les commandes avant la date début de la planification](design-details-dealing-with-orders-before-the-planning-starting-date.md).  
  
## <a name="see-also"></a>Voir aussi  
[Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md)   
[Détails de conception : paramètres de planification](design-details-planning-parameters.md)   
[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
