---
title: Détails de conception - Méthodes de réapprovisionnement | Microsoft Docs
description: Cette rubrique donne un aperçu des méthodes de réapprovisionnement.
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
ms.openlocfilehash: a48e2998195bccb4ac877e8339612f6cfabb0f3b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303067"
---
# <a name="design-details-reordering-policies"></a>Détails de conception : méthodes de réapprovisionnement
Les méthodes de réapprovisionnement définissent la quantité à commander lorsque l'article doit être réapprovisionné. Quatre différentes méthodes de réapprovisionnement existent.  

## <a name="fixed-reorder-qty"></a>Qté fixe de commande.
La méthode Qté fixe de commande est liée à la planification du stock des articles C courants (coûts de stock faible, faible risque d'obsolescence, et/ou plusieurs articles). Cette méthode est généralement utilisée conjointement avec un point de commande reflétant la demande anticipée lors du délai de l'article.  

### <a name="calculated-per-time-bucket"></a>Calculé par intervalle de planification  
 Si le système de planification détecte que le point de commande est atteint ou traversé lors d'un intervalle de planification (cycle de commande), au-dessous ou sur le point de commande au début de la période et au-dessous ou sur le point de commande à la fin de la période, il propose de créer une commande fournisseur de la quantité de la commande spécifiée et ensuite la planifie à partir de la première date après la fin de l'intervalle de planification.  

 Le concept de point de commande délimité par un intervalle de planification réduit le nombre de suggestions d'approvisionnement. Cela reflète un processus manuel d'évaluation fréquente de l'entrepôt pour vérifier le contenu réel des différents emplacements.  

### <a name="creates-only-necessary-supply"></a>Crée uniquement l'approvisionnement nécessaire  
 Avant de proposer une commande approvisionnement pour répondre à un point de commande, le système de planification vérifie si l'approvisionnement a déjà été commandé pour être reçu dans le délai de réapprovisionnement de l'article. Si une commande approvisionnement existante résout le problème en amenant le stock prévisionnel à un niveau égal ou supérieur au point de commande dans le délai, le système ne suggère pas de nouvelle commande approvisionnement.  

 Les commandes approvisionnement qui sont créées spécifiquement pour répondre à un point de commande sont exclues de l'équilibrage ordinaire d'approvisionnement, et ne seront en aucun cas modifiées par la suite. Par conséquent, si un article utilisant un point de commande doit être éliminé (non réapprovisionné), il est recommandé d'étudier les commandes approvisionnement ouvertes manuellement ou de modifier la méthode de réapprovisionnement en Lot pour lot, le système peut alors réduire ou annuler l'approvisionnement superflu.  

### <a name="combines-with-order-modifiers"></a>Associe avec les modificateurs d'ordre  
 Les modificateurs de commande, qté minimum commande, qté maximum commande et multiple de commande, ne doivent pas jouer un grand rôle lorsque la stratégie de quantité fixe de commande est utilisée. Toutefois, le système de planification prend encore ces modificateurs en compte et diminue la quantité commande maximum spécifiée (et crée au moins deux approvisionnements pour atteindre la quantité commande totale), augmente la commande jusqu'à la quantité commande minimum spécifiée ou arrondit la quantité commandée pour répondre à un multiple spécifié de la commande.  

### <a name="combines-with-calendars"></a>Combinaison avec des calendriers  
 Avant de proposer une commande approvisionnement pour répondre à un point de commande, le système de planification vérifie si la commande est planifiée pour un jour chômé, en fonction des calendriers définis dans le champ **Code calendrier principal** des pages **Informations société** et **Fiche magasin**.  

 Si la date prévue est un jour chômé, le système de planification déplace la commande en aval à la date de travail la plus proche. Cela peut entraîner une commande qui satisfait un point de commande mais ne pas satisfait une certaine demande spécifique. Pour une telle demande non soldée, le système de planification crée un approvisionnement supplémentaire.  

### <a name="should-not-be-used-with-forecast"></a>Ne doit pas être utilisé avec la prévision  
 Étant donné que la demande prévue est déjà exprimée au niveau du point de commande il n'est pas nécessaire d'inclure une prévision dans la planification d'un article à l'aide d'un point de commande. S'il est important de baser le programme sur une prévision, utilisez la stratégie lot pour lot.  

### <a name="must-not-be-used-with-reservations"></a>Ne doit pas être utilisé avec les réservations  
 Si l'utilisateur a réservé une quantité, par exemple une quantité dans le stock, pour une certaine demande éloignée, la base de planification est dérangée. Même si le niveau de stock projeté est acceptable par rapport au point de réapprovisionnement, les quantités peuvent ne pas être disponibles. Le système peut essayer de compenser cela en créant des commandes exception ; toutefois, il est conseillé de définir le champ Reserve sur Never pour les articles prévus comme utilisant un point de commande.

## <a name="maximum-qty"></a>Qté maximum
La stratégie Quantité maximum est une manière de mettre à jour le stock à l'aide d'un point de commande.  

Tout ce qui concerne la stratégie Qté fixe de commande s'applique également à cette méthode. La seule différence est la quantité de l'approvisionnement proposé. Lors de l'utilisation de la méthode de quantité maximum, la quantité de réapprovisionnement est définie de façon dynamique en fonction du niveau de stock prévisionnel et diffère donc généralement de commande en commande.  

### <a name="calculated-per-time-bucket"></a>Calculé par intervalle de planification  
La quantité de réapprovisionnement est déterminée au moment (à la fin d'un intervalle de planification) où le système de planification détecte le que le point de commande a été dépassé. En même temps, le système mesure l'écart entre le niveau de stock prévisionnel actuel et le stock maximal spécifié. Cela constitue la quantité à recommander. Le système vérifie ensuite si l'approvisionnement a déjà été commandé ailleurs pour être reçu dans les délais et, si c'est le cas, réduit la quantité de la nouvelle commande d'approvisionnement des quantités déjà commandées.  

Le système assure que le stock prévisionnel atteint au moins le niveau du point de commande, dans le cas où l'utilisateur oublierait de spécifier une quantité de stock maximum.  

### <a name="combines-with-order-modifiers"></a>Associe avec les modificateurs d'ordre  
En fonction de la configuration, il peut être préférable de combiner la stratégie de la quantité maximum avec des modificateurs de commande pour garantir une quantité de commande minimale ou de l'arrondir au nombre supérieur d'unités d'achat, ou de le diviser en davantage de lots comme défini par la quantité maximum commande.  

### <a name="combines-with-calendars"></a>Combinaison avec des calendriers  
Avant de proposer une commande approvisionnement pour répondre à un point de commande, le système de planification vérifie si la commande est planifiée pour un jour chômé, en fonction des calendriers définis dans le champ **Code calendrier principal** des pages **Informations société** et **Fiche magasin**.  

Si la date prévue est un jour chômé, le système de planification déplace la commande en aval à la date de travail la plus proche. Cela peut entraîner une commande qui satisfait un point de commande mais ne pas satisfait une certaine demande spécifique. Pour une telle demande non soldée, le système de planification crée un approvisionnement supplémentaire.

## <a name="order"></a>Ordre
Dans un environnement de fabrication à la commande, un article est acheté ou produit pour couvrir exclusivement une demande spécifique. Généralement, il se rapporte aux articles A, et la motivation pour choisir cette méthode de réapprovisionnement de commande peut être que la demande n'est pas fréquente, le délai de production est insignifiant ou les attributs requis varient.  

L'application crée un lien ordre pour ordre, qui agit en tant que connexion préliminaire entre l'approvisionnement, une commande approvisionnement ou un stock, et la demande qu'il va traiter.  

Outre l'utilisation de la méthode de commande, le lien ordre pour ordre peut s'appliquer lors de la planification, comme suit :  

* Lors de l'utilisation de la méthode de fabrication Make-to-Order pour créer des ordres de fabrication de type multi-niveau ou projet (la production avait besoin de composants sur le même ordre de fabrication).  
* Lors de l'utilisation de la fonction Sales Order Planning pour créer un ordre de fabrication à partir d'une commande vente.  

Même si une société manufacturière se considère comme un environnement de fabrication à la commande, il peut être préférable d'utiliser la méthode de réapprovisionnement Lot pour lot si les articles sont des standards purs sans variation dans les attributs. Par conséquent, le système utilise le stock non planifié et additionne uniquement les commandes vente ayant la même date d'expédition ou faisant partie d'un intervalle de planification défini.  

### <a name="order-to-order-links-and-past-due-dates"></a>Liens ordre pour ordre et dates arriérées  
Contrairement à la plupart des ensembles approvisionnement-demande, les commandes liées avec des dates d'échéance antérieures à la date de début de la planification sont entièrement planifiées par le système. La raison commerciale de cette exception est que les ensembles spécifiques approvisionnement-demande doivent être synchronisés jusqu'à l'exécution. Pour plus d'informations sur la zone gelée qui s'applique à la plupart des types de demande-approvisionnement, voir [Détails de conception : traiter les commandes avant la date début de la planification](design-details-dealing-with-orders-before-the-planning-starting-date.md).

## <a name="lot-for-lot"></a>Lot pour lot
La méthode lot pour lot est la plus souple, parce que le système réagit uniquement à la demande réelle, de plus il agit sur une demande anticipée à partir de commandes de prévision et de commandes ouvertes, puis détermine la quantité commande en fonction de la demande. La méthode lot pour lot visé cible les articles A et B pour lesquels le stock peut être accepté mais doit être évité.  

Par certains côtés, la méthode lot pour lot ressemble à la méthode de commande, mais elle a une approche générique des articles ; elle peut accepter des quantités en stock, et elle groupe une demande et un approvisionnement correspondants dans des intervalles de planification définis par l'utilisateur.  

L'intervalle de planification est défini dans le champ **Intervalle de planification**. Le système travaille avec un intervalle de planification minimum d'un jour, car il s'agit de la plus petite unité de temps des événements de demande et d'approvisionnement dans le système (même si, dans la pratique, l'unité de temps des ordres de fabrication et des besoins de composants peuvent être des secondes).  

L'intervalle de planification fixe également des limites lorsqu'un ordre de fabrication existant doit être replanifié pour répondre à une demande donnée. Si l'approvisionnement se trouve dans l'intervalle de planification, il est replanifié en entrée ou en sortie pour répondre à la demande. Sinon, s'il a lieu précédemment, il provoque une accumulation de stock inutile et doit être annulé. S'il se trouve plus tard, une commande approvisionnement est créée à la place.  

Avec cette méthode, il est également possible de définir un stock de sécurité pour compenser les fluctuations possibles de l'approvisionnement, ou répondre à une demande soudaine.  

Étant donné que la quantité de commande approvisionnement est basée sur la demande réelle, il peut sembler raisonnable d'utiliser les modificateurs de commande : arrondir la quantité commandée pour répondre à un multiple spécifié de la commande (ou unité d'achat), augmenter la commande à une quantité de commande minimale spécifiée, ou réduire la quantité à la quantité maximale spécifiée (et ainsi créer deux ou plusieurs approvisionnements pour répondre à la quantité nécessaire totale).

## <a name="see-also"></a>Voir aussi  
[Détails de conception : paramètres de planification](design-details-planning-parameters.md)   
[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
