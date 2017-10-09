---
title: "Détails de conception - Équilibrage de l'approvisionnement avec la demande | Microsoft Docs"
description: "L'élément principal du système de planification implique l'équilibrage de l'approvisionnement et de la demande en proposant des actions utilisateur pour rectifier les commandes approvisionnement en cas de déséquilibre. Cela est opéré par combinaison de variante et magasin."
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
ms.openlocfilehash: 5020c048373f10e72e40f0c9b1e5a11fc45eedb5
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-balancing-supply-with-demand"></a>Détails de conception : équilibrage de l'approvisionnement avec la demande
L'élément principal du système de planification implique l'équilibrage de l'approvisionnement et de la demande en proposant des actions utilisateur pour rectifier les commandes approvisionnement en cas de déséquilibre. Cela est opéré par combinaison de variante et magasin.  
  
Imaginez que chaque profil de stock contient une chaîne d'événements de demande (triés par date et par priorité) et une chaîne correspondante d'événements d'approvisionnement. Chaque événement fait référence à son type origine et à son identification. Les règles pour équilibrer l'article sont simples. Quatre exemples de correspondance entre demande et approvisionnement peuvent apparaître à tout moment dans le processus :  
  
1. Aucune demande ou offre n'existe pour l'article => la planification est terminée (ou ne doit pas démarrer).  
2. La demande existe mais il n'y a pas d'offre => une offre doit être proposée.  
3. L'offre existe mais il n'y a pas de demande correspondante => l'offre doit être annulée.  
4. L'offre et la demande existent => les questions doivent être posées et résolues pour que le système puisse garantir que la demande sera satisfaite et que l'offre est suffisante.  
  
     Si le délai de l'approvisionnement n'est pas approprié, l'approvisionnement peut être replanifié par exemple comme suit :  
  
    1.  Si l'approvisionnement est placé avant la demande, l'approvisionnement peut éventuellement être replanifié en sortie pour que le stock soit le plus bas possible.  
    2.  Si l'approvisionnement est placé après la demande, l'approvisionnement peut éventuellement être replanifié en entrée. Sinon, le système suggère un nouvel approvisionnement.  
    3.  Si l'approvisionnement satisfait la demande à la date, le système de planification peut continuer à chercher si la quantité de l'approvisionnement peut couvrir la demande.  
  
     Une fois que le délai est en place, la quantité appropriée à approvisionner peut être calculée comme suit :  
  
    1.  Si la quantité d'approvisionnement est inférieure à la demande, il est possible que la quantité d'approvisionnement puisse être augmentée (ou pas, si limitée par une stratégie de quantité maximum).  
    2.  Si la quantité d'approvisionnement est supérieure à la demande, il est possible que la quantité d'approvisionnement puisse être diminuée (ou pas, si limitée par une stratégie de quantité minimum).  
  
     A ce stade, l'une de ces deux situations existe :  
  
    1.  La demande actuelle peut être couverte, dans ce cas, elle peut être clôturée et la planification des demandes suivantes peut commencer.  
    2.  L'approvisionnement a atteint son maximum, en laissant une partie de la quantité de demande non couverte. Dans ce cas, le système de planification peut clôturer l'approvisionnement actif et passer au suivant.  
  
 La procédure recommence à la demande suivante et à l'approvisionnement actif ou vice versa. L'approvisionnement actif peut peut-être couvrir cette demande suivante également, ou la demande actuelle n'a pas encore été entièrement couverte.  
  
## <a name="rules-concerning-actions-for-supply-events"></a>Règles en ce qui concerne les actions pour les événements d'approvisionnement  
Lorsque le système de planification effectue un calcul hiérarchisé dans lequel l'approvisionnement doit répondre à la demande, la demande est considérée comme sûr, c'est-à-dire qu'elle se trouve en dehors du contrôle du système de planification. Cependant, le côté approvisionnement peut être géré. Par conséquent, le système de planification suggère de créer de nouvelles commandes approvisionnement, reprogrammant celles existantes et/ou modifiant la quantité de commande. Si une commande approvisionnement existante devient superflue, le système de planification suggère à l'utilisateur de l'annuler.  
  
Si l'utilisateur souhaite exclure une commande approvisionnement existante des propositions planning, il peut déclarer qu'il n'y a pas de flexibilité de planification (flexibilité de planification = Aucune). Ensuite, l'approvisionnement excédentaire à partir de cette commande est utilisé pour répondre à la demande, mais aucune action n'est suggérée.  
  
En général, tous les approvisionnements ont une flexibilité de planification qui est limitée par les conditions de chacune des mesures suggérées.  
  
-   **Replanifier en dehors** : La date à partir d'une commande approvisionnement existante peut être planifiée en dehors pour satisfaire la date d'échéance de demande à moins que :  
  
    -   Il représente le stock (toujours au jour zéro).  
    -   Elle a un ordre pour ordre lié à une autre demande.  
    -   Il se trouve hors de la fenêtre de replanification définie avant l'intervalle de planification.  
    -   Il existe un approvisionnement plus proche qui peut être utilisé.  
    -   Par ailleurs, l'utilisateur peut choisir de ne pas replanifier pour les raisons suivantes :  
    -   La commande approvisionnement a déjà été liée à une autre demande à une date précédente.  
    -   La replanification nécessaire est si minime que l'utilisateur la trouve négligeable.  
  
-   **Replanifier dans** : La date à partir d'une commande approvisionnement existante peut être replanifiée dans, sauf dans les conditions suivantes :  
  
    -   Elle est directement liée à une autre demande.  
    -   Il se trouve hors de la fenêtre de replanification définie avant l'intervalle de planification.  
  
> [!NOTE]  
>  Lors de la planification d'un article utilisant un point de commande, la commande approvisionnement peut toujours être planifiée si nécessaire. Ceci est courant dans les commandes approvisionnement planifiées déclenchées par un point de commande.  
  
-   **Augmenter la quantité** : il est possible d'augmenter la quantité d'une commande approvisionnement existante pour répondre à la demande sauf si la commande approvisionnement est directement liée à une demande par un lien ordre pour ordre.  
  
> [!NOTE]  
>  Bien qu'il soit possible d'augmenter la commande approvisionnement, elle peut être limité en raison d'une quantité maximum commande définie par l'utilisateur.  
  
-   **Diminuer la quantité** : une commande approvisionnement existante avec un excédent par rapport à la demande existante peut être diminuée pour répondre à la demande.  
  
> [!NOTE]  
>  Bien que la quantité puisse être diminuée, il peut y avoir encore des excédents par rapport à la demande en raison d'une quantité minimum commande définie ou d'une valeur Commandé par.  
  
-   **Annuler** : comme un incident spécial de l'action de diminuer la quantité, la commande approvisionnement peut être annulée si elle a été diminuée à zéro.  
-   **Nouveau** : si aucune commande approvisionnement n'existe déjà, ou si une existante ne peut pas être modifiée pour satisfaire la quantité nécessaire à la date d'échéance demandée, une nouvelle commande approvisionnement est suggérée.  
  
## <a name="determining-the-supply-quantity"></a>Déterminer la quantité d'approvisionnement  
Les paramètres de planification définis par l'utilisateur contrôlent la quantité suggérée de chaque commande approvisionnement.  
  
Lorsque le système de planification calcule la quantité d'une nouvelle commande approvisionnement ou la modification de quantité d'une commande existante, la quantité proposée n'est pas forcément identique à ce qui est vraiment demandé.  
  
Si un stock maximum ou une quantité de commande fixe sont sélectionnés, la quantité proposée peut être augmentée pour répondre à cette quantité fixe ou au stock maximum. Si une méthode de réapprovisionnement utilise un point de commande, la quantité peut être augmentée au moins pour répondre au point de commande.  
  
 La quantité proposée peut être modifiée dans cette séquence :  
  
1. Diminuer à la quantité maximum commande (le cas échéant).  
2. Jusqu'à la quantité de commande minimale.  
3. Jusqu'à répondre à la commande multiple la plus proche. (Si des paramètres sont erronés, cela peut enfreindre la quantité de commande maximale).  
  
## <a name="order-tracking-links-during-planning"></a>Liens de chaînage lors de la planification  
En ce qui concerne le chaînage lors de la planification, il est important de mentionner que le système de planification réarrange les liens de chaînage créés de façon dynamique pour les combinaisons de article/variante/magasin.  
  
Deux raisons expliquent cela :  
  
-   Le système de planification doit pouvoir justifier ses propositions ; que toute demande a été couverte, et qu'aucune commande approvisionnement n'est superflue.  
-   Les liens de chaînage créés de façon dynamique doivent être rééquilibrés régulièrement.  
  
Avec le temps, les liens de chaînage dynamiques deviennent déséquilibrés puisque le réseau de chaînage entier n'est pas réorganisé tant qu'un événement de demande ou d'approvisionnement n'est pas réellement clôturé.  
  
Avant d'équilibrer un approvisionnement par demande, le programme supprime les liens de chaînage existants. Puis au cours de la procédure de contrepartie, lorsqu'un événement de demande ou d'approvisionnement est clôturé, il crée de nouveaux liens de suivi de commande entre la demande et l'approvisionnement.  
  
> [!NOTE]  
>  Même si l'article n'est pas configuré pour le chaînage dynamique, le système planifié crée des liens de chaînage équilibrés comme expliqué ci-dessus.  
  
## <a name="see-also"></a>Voir aussi  
[Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md)   
[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)   
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
