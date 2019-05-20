---
title: Détails de conception - Transferts de planification | Microsoft Docs
description: Cette rubrique décrit comment utiliser des ordres de transfert comme source d'approvisionnement lors de la planification des niveaux de stock.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, transfer, sku, locations, warehouse
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 56988064297cac55c48624071a19d510f6126495
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248057"
---
# <a name="design-details-transfers-in-planning"></a>Détails de conception : transferts de planification
Les ordres de transfert sont également une source d'approvisionnement lorsque vous travaillez au niveau des points de stock. Lors de l'utilisation de plusieurs magasins (entrepôts), le système de réapprovisionnement de point de stock peut être défini sur Transfer, ce qui implique que le magasin est réapprovisionné en transférant des biens d'un autre magasin. Dans une situation avec plusieurs entrepôts, les sociétés peuvent avoir une chaîne de transferts où l'approvisionnement vers le magasin VERT est transféré à partir du magasin JAUNE, l'approvisionnement vers JAUNE est transféré depuis ROUGE et ainsi de suite. Au début de la chaîne, il existe un système de réapprovisionnement d'Ordre de fabrication ou d'achat.  

![Exemple de flux de transfert](media/nav_app_supply_planning_7_transfers1.png "Exemple de flux de transfert")  

Lors de la comparaison de la situation où une commande approvisionnement rencontre directement une commande demande avec une situation où la commande vente est livrée à l'aide d'une chaîne de transferts de points de stock, il est évident que la tâche de planification dans la dernière situation peut devenir très complexe. Si la demande est modifiée, cela peut avoir des répercussions sur toute la chaîne, parce que tous les ordres de transfert et la commande achat/l'ordre de fabrication à l'extrémité opposée de la chaîne devront être traités pour rétablir l'équilibre entre la demande et l'approvisionnement.  

![Exemple d'équilibre de l'offre et de la demande dans les transferts](media/nav_app_supply_planning_7_transfers2.png "Exemple d'équilibre de l'offre et de la demande dans les transferts")  

## <a name="why-is-transfer-a-special-case"></a>Pourquoi le transfert est-il un cas spécial ?  
Un ordre de transfert ressemble aux autres ordres du programme. Toutefois, en coulisse, c'est très différent.  

L'un aspect fondamental qui distingue les transferts dans la planification entre les commandes achat et les ordres de fabrication est qu'une ligne transfert représente la demande et l'approvisionnement en même temps. La partie sortante, qui est expédiée à partir de l'ancien magasin, est la demande. La partie entrante, qui doit être reçue au nouveau magasin, est un approvisionnement à ce magasin.  

![Contenu de la page Ordre de transfert](media/nav_app_supply_planning_7_transfers3.png "Contenu de la page Ordre de transfert")  

Cela signifie que lorsque le système traite le côté approvisionnement du transfert, il doit effectuer une modification semblable du côté de la demande.  

## <a name="transfers-are-dependent-demand"></a>Les transferts sont dépendants de la demande  
La demande et l'approvisionnement liés ressemblent un peu aux composants d'une ligne O.F., mais la différence est que les composants se trouvent au niveau de planification suivant et avec un article différent, alors que les deux parties du transfert se trouvent au même niveau, pour un même article.  

Autre similitude importante : les composants représentent une demande dépendante, tout comme la demande de transfert. La demande à partir d'une ligne transfert est dictée par le côté approvisionnement du transfert dans le sens que si l'approvisionnement est modifié, la demande est affectée directement.  

À moins que la flexibilité de planification ne soit None, une ligne de transfert ne doit jamais être traitée en tant que demande indépendante dans la planification.  

Dans la procédure de planification, la demande de transfert doit être prise en compte uniquement après que le côté de l'approvisionnement a été traité par le système de planification. Avant ça, la demande réelle n'est pas connue. La séquence des modifications apportées est donc très importante lorsqu'il s'agit d'ordres de transfert.  

## <a name="planning-sequence"></a>Séquence de planification  
La figure ci-après montre à quoi peut ressembler une chaîne de transferts.  

![Exemple de flux de transfert simple](media/nav_app_supply_planning_7_transfers4.png "Exemple de flux de transfert simple")  

Dans cet exemple, un client commande l'article au magasin VERT. Le magasin VERT est approvisionné via un transfert de l'entrepôt central ROUGE. L'entrepôt central ROUGE est approvisionné par un transfert après production vers le magasin BLEU.  

Dans cet exemple, le système de planification commencera à la demande client et remontera en amont dans la chaîne. Les demandes et approvisionnements seront traités un magasin à la fois.  

![Planification de l'approvisionnement avec transferts](media/nav_app_supply_planning_7_transfers5.png "Planification de l'approvisionnement avec transferts")  

## <a name="transfer-level-code"></a>Code niveau transfert  
L'ordre dans lequel les magasins sont traités dans le système de planification est déterminé par le code niveau de transfert du point de stock.  

Le code de niveau de transfert est un champ interne qui est automatiquement calculé et enregistré sur le point de stock lorsque le point de stock est créé ou modifié. Le calcul s'exécute pour tous les points de stock d'une combinaison donnée article/variante et utilise le code magasin et le code prov. transfert pour déterminer le trajet que la planification doit utiliser en parcourant les points de stock pour s'assurer que toutes les demandes sont traitées.  

Le code de niveau de transfert est de 0 pour les points de stock avec système de réapprovisionnement Purchase ou Prod. Order et est -1 pour le premier niveau de transfert, -2 pour le deuxième et ainsi de suite. Dans la chaîne de transfert décrite précédemment, les niveaux sont donc -1 pour ROUGE et -2 pour VERT, comme l'indiquent la figure suivante.  

![Contenu de la page Fiche point de stock](media/nav_app_supply_planning_7_transfers6.gif "Contenu de la page Fiche point de stock")  

Lors de la mise à jour d'un point de stock, le système de planification détecte si les points de stock avec transfert du système de réapprovisionnement sont configurés avec des références circulaires.  

## <a name="planning-transfers-without-sku"></a>Planifier des transferts sans points de stock  

Même si la fonction Points de stock n'est pas utilisée, il est possible d'utiliser des emplacements et de créer des transferts manuels entre magasins. Pour les sociétés avec des paramètres d'entrepôt moins avancés, le système de planification prend en charge des scénarios où le stock existant est transféré manuellement vers un autre magasin, par exemple pour couvrir une commande vente dans le magasin. Simultanément, le système de planification doit réagir aux modifications de la demande.  

Pour prendre en charge les transferts manuels, la planification analysera les ordres de transfert existants puis planifiera l'ordre dans lequel les magasins doivent être traités. En interne, le système de planification doit s'exécuter avec des points de stock temporaires indiquant les codes de niveau de transfert.  

![Code niveau de transfert](media/nav_app_supply_planning_7_transfers7.png "Code niveau de transfert")  

Si plusieurs transferts dans un magasin donné ont été créés, le premier ordre de transfert définit la direction de planification. Les transferts exécutés dans le sens inverse sont annulées.  

## <a name="changing-quantity-with-reservations"></a>Modification de la quantité avec des réservations  
Lors du changement de quantités sur l'approvisionnement existant, le système de planification prend en compte les réservations dans le sens où la quantité réservée représente la limite inférieure de combien l'approvisionnement peut être réduit.  

Lors du changement de la quantité sur une ligne d'ordre de transfert ligne existante, n'oubliez pas que la limite inférieure est définie comme quantité réservée la plus élevée de la ligne de transfert sortante et entrante.  

Par exemple, si une ligne ordre de transfert de 117 pièces est réservée sur une ligne vente de 46 et une ligne achat de 24, il n'est pas possible de réduire la ligne transfert à moins de 46 pièces, même si cela peut représenter un approvisionnement excédentaire du côté entrant.  

![Réservations de planification de transfert](media/nav_app_supply_planning_7_transfers8.png "Réservations de planification de transfert")  

## <a name="changing-quantity-in-a-transfer-chain"></a>Modification de la quantité dans une chaîne de transfert  
Dans l'exemple suivant, le point de départ est une situation équilibrée avec une chaîne de transfert approvisionnant une commande vente de 27 dans le magasin ROUGE avec une commande achat correspondante dans le magasin BLEU, transférée via le magasin ROSE. Par conséquent, outre les vente et les achats, il existe deux ordres de transfert : BLUE-PINK et PINK-RED.  

![Modification de la quantité dans la planification de transfert 1](media/nav_app_supply_planning_7_transfers9.png "Modification de la quantité dans la planification de transfert 1")  

À présent le gestionnaire dans le magasin ROSE choisit de réserver par rapport à l'achat.  

![Modification de la quantité dans la planification de transfert 2](media/nav_app_supply_planning_7_transfers10.png "Modification de la quantité dans la planification de transfert 2")  

Habituellement, cela signifie que le système de planification ignore la commande achat et la demande de transfert. Tant que l'équilibre est maintenu, il n'y a pas de problème. Mais que se passe-t-il si le client dans un magasin ROUGE regrette en partie sa commande et la modifie à 22 ?  

![Modification de la quantité dans la planification de transfert 3](media/nav_app_supply_planning_7_transfers11.png "Modification de la quantité dans la planification de transfert 3")  

Lorsque le système de planification est à nouveau exécuté, il doit se débarrasser de l'approvisionnement excédentaire. Toutefois, la réservation verrouillera l'achat et le transfert à une quantité de 27.  

![Modification de la quantité dans la planification de transfert 4](media/nav_app_supply_planning_7_transfers12.png "Modification de la quantité dans la planification de transfert 4")  

Le transfert ROUGE-ROSE a été réduit à 22. La partie entrante du transfert BLEU-ROSE n'est pas réservée, mais parce que la partie sortante est réservée, il n'est pas possible de réduire la quantité à un niveau inférieur à 27.  

## <a name="lead-time-calculation"></a>Délai de réappro.  
Lors du calcul de la date d'échéance d'un ordre de transfert, différents types de délai seront pris en compte.  

Les délais qui sont actifs lors de la planification d'un ordre de transfert sont les suivants :  

* Délai de désenlogement  
* Délai d'expédition  
* Délai d'enlogement  
* Sur la ligne planning, les champs suivants sont utilisés pour fournir des informations sur le calcul.  
* Date expédition transfert  
* Date début  
* Date fin  
* Date d'échéance  

La date d'expédition de la ligne transfert sera affichée dans le champ Date expédition transfert, et la date de réception de la ligne transfert sera affichée dans le champ Date d'échéance.  

Les dates début et fin sont utilisées pour décrire la période réelle de transport.  

La figure ci-après montre l'interprétation de la date/heure de début et de la date/heure de fin sur les lignes planning liées aux ordres de transfert.  

![Date et heures centrales dans la planification de transfert](media/nav_app_supply_planning_7_transfers13.png "Date et heures centrales dans la planification de transfert")  

Dans cet exemple, cela signifie que :  

* Date d'expédition + Traitement en sortie = Date début  
* Date début + Délai d'expédition = Date fin  
* Date fin + Traitement entrant = Date de réception  

## <a name="safety-lead-time"></a>Délai de sécurité  
Le champ Délai de sécurité par défaut de la page Paramètres production et le champ associé Délai de sécurité de la fiche article ne sont pas pris en compte dans le calcul d'un ordre de transfert. Toutefois, ce délai de sécurité influence toujours le programme entier comme il affecte l'ordre de réapprovisionnement (achat ou production) au début de la chaîne de transfert lorsque les articles sont mis dans le magasin à partir duquel ils seront transférés.  

![Éléments de la date d'échéance de transfert](media/nav_app_supply_planning_7_transfers14.png "Éléments de la date d'échéance de transfert")  

Sur la ligne O.F., Date fin + Délai de sécurité + Délai enlogement = Date d'échéance.  

Sur la ligne commande achat, Date livraison fournisseur prévue + Délai de sécurité + Délai enlogement = Date réception prévue.  

## <a name="reschedule"></a>Replanifier  
Lors de la replanification d'une ligne de transfert existante, le système de planification doit rechercher la partie sortante et modifier la date/heure de celle-ci. Il est important de noter que si le délai a été défini, il existe un écart entre l'expédition et la réception. Comme indiqué, le délai peut comporter plusieurs éléments, par exemple le temps de transport et le délai entrepôt. Sur un planning, le système de planification remontera dans le temps pendant qu'il équilibre les éléments.  

![Modification de la date d'échéance dans la planification de transfert](media/nav_app_supply_planning_7_transfers15.png "Modification de la date d'échéance dans la planification de transfert")  

Par conséquent, lors de la modification de la date d'échéance sur une ligne transfert, le délai doit être calculée pour mettre à jour la partie sortante du transfert.  

## <a name="seriallot-numbers-in-transfer-chains"></a>Numéros de série/lot dans des chaînes de transfert  
Si la demande indique des numéros de série et/ou de lot, et que le moteur de planification est activé, elle produira des ordres de transfert directement créés. Pour plus d'informations sur ce concept, voir Attributs d'article. Si, cependant, les numéros de série/lot sont supprimées de la demande, les ordres de transfert créés dans la chaîne contiendront toujours les numéros de série/lot et seront donc ignorés lors de la planification (non supprimés).  

## <a name="order-to-order-links"></a>Liens ordre pour ordre  
Dans cet exemple, le point de stock BLEU est installé avec la méthode de réapprovisionnement commande, alors que ROSE et ROUGE utilisent lot pour lot. Lorsqu'une commande vente de 27 est créée sur le magasin ROUGE, elle entraîne une chaîne de transferts, le dernier joint du magasin BLEU étant réservé avec liaison. Dans cet exemple, les réservations ne sont pas des réservations dures créées par le gestionnaire dans le magasin ROSE, mais des liens créés par le système de planification. La différence importante est que le système de planification peut modifier ces derniers.  

![Liens ordre pour ordre dans la planification de transfert](media/nav_app_supply_planning_7_transfers16.png "Liens ordre pour ordre dans la planification de transfert")  

Si la demande est modifiée de 27 à 22, le système réduira la quantité par défaut dans toute la chaîne, et la réservation du lien est également réduite.  

## <a name="see-also"></a>Voir aussi  
[Détails de conception : paramètres de planification](design-details-planning-parameters.md)   
[Détails de conception : tableau d'affectation de planification](design-details-planning-assignment-table.md)   
[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
[Détails de conception : demande à un magasin vide](design-details-demand-at-blank-location.md)   
[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)   
[Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md)   
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
