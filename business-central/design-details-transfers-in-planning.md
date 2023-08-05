---
title: "Détails de conception\_: transferts de planification"
description: Découvrez comment utiliser des ordres de transfert comme source d’approvisionnement lors de la planification des niveaux de stock.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.keywords: 'design, transfer, sku, locations, warehouse'
---
# Détails de conception : transferts de planification

Les ordres de transfert sont également une source d’approvisionnement lorsque vous travaillez au niveau des points de stock. Lors de l’utilisation de plusieurs magasins (entrepôts), le système de réapprovisionnement de point de stock peut être défini sur Transfer, ce qui implique que le magasin est réapprovisionné en transférant des biens d’un autre magasin. Dans une situation avec plus d’entrepôts, vous pourriez avoir une chaîne de transferts. L’approvisionnement vers l’emplacement VERT est transféré depuis le JAUNE, l’approvisionnement vers le JAUNE est transféré depuis le ROUGE, et ainsi de suite. Au début de la chaîne, il existe un système de réapprovisionnement par **Ordre de fabrication** ou **Achat**.  

![Exemple de flux de transfert.](media/nav_app_supply_planning_7_transfers1.png "Exemple de flux de transfert")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Si vous comparez les situations suivantes, il est clair que la tâche de planification dans la dernière peut devenir complexe :

* Une commande approvisionnement est directement confrontée à une commande de demande
* Une commande vente est fournie via une chaîne de transferts de points de stock

Si la demande change, cela peut avoir des répercussions sur toute la chaîne. Tous les ordres de transfert, plus l’ordre d’achat et l’ordre de fabrication à l’extrémité opposée de la chaîne, devront être mis à jour pour rééquilibrer la demande et l’offre.  

![Exemple d’équilibre de l’offre et de la demande dans les transferts.](media/nav_app_supply_planning_7_transfers2.png "Exemple d’équilibre de l’offre et de la demande dans les transferts")  

## Pourquoi le transfert est-il un cas spécial ?  

Les ordres de transfert sont similaires aux autres ordres, tels que les ordres d’achat et de fabrication. Toutefois, en coulisse, ils sont différents.  

Une différence est qu’une ligne de transfert représente à la fois la demande et l’offre. La partie sortante qui est expédiée est la demande. La partie entrante qui est reçue au nouveau magasin, est une offre à ce magasin.  

![Contenu de la page Ordre de transfert.](media/nav_app_supply_planning_7_transfers3.png "Contenu de la page Ordre de transfert")  

Lorsque [!INCLUDE [prod_short](includes/prod_short.md)] change le côté offre du transfert, il doit faire un changement similaire du côté demande.  

## Les transferts sont des demandes dépendantes  

La relation entre l’offre et la demande est similaire aux composants sur les lignes d’ordre de fabrication. La différence est que les composants des lignes d’ordre de fabrication se trouvent au niveau de planification suivant et ont un article différent. Les deux parties du transfert sont au même niveau pour le même article.  

Autre similitude importante : les composants et les transferts sont des demandes dépendantes. La demande d’une ligne de transfert est dictée par le côté offre du transfert. Si l’offre change, la demande est directement affectée.

À moins que la flexibilité de planification ne soit Aucune, une ligne de transfert ne doit pas être traitée en tant que demande indépendante dans la planification.  

Dans la procédure de planification, la demande de transfert doit être prise en compte uniquement après que le système de planification a traité le côté de l’offre. Avant que le traitement n’ait lieu, la demande réelle n’est pas connue. La séquence des modifications est importante pour les ordres de transfert.  

## Séquence de planification  

L’image suivante montre un exemple d’une chaîne de transferts.  

![Exemple de flux de transfert simple.](media/nav_app_supply_planning_7_transfers4.png "Exemple de flux de transfert simple")  

Dans cet exemple, un client commande l’article au magasin VERT. Le magasin VERT est approvisionné via un transfert de l’entrepôt central ROUGE. L’entrepôt central ROUGE est approvisionné par un transfert après production vers le magasin BLEU.  

Dans cet exemple, le système de planification commence à la demande client et remonte en amont dans la chaîne. Les demandes et les offres sont traitées pour un magasin à la fois.  

![Planification de l’approvisionnement avec transferts.](media/nav_app_supply_planning_7_transfers5.png "Planification de l’approvisionnement avec transferts")  

## Code niveau transfert  

Le code niveau de transfert du point de stock détermine l’ordre dans lequel le système de planification traite les magasins.  

Le code niveau de transfert est un champ interne. Le champ est calculé et stocké sur le point de stock lorsque vous créez ou modifiez le point de stock. Le calcul s’exécute sur tous les points de stock pour une combinaison donnée d’article et de variante d’article. Le calcul utilise le code magasin et le code d’origine du transfert pour déterminer l’itinéraire à utiliser pour les points de stock. Le calcul garantit que toutes les demandes sont traitées.  

Le code niveau de transfert est de 0 pour les points de stock avec système de réapprovisionnement Achat ou Ordre de fabrication, et est -1 pour le premier niveau de transfert, -2 pour le deuxième et ainsi de suite. Dans l’exemple décrit dans la section précédente, les niveaux sont -1 pour ROUGE et -2 pour VERT, comme l’indique la figure suivante.  

![Contenu de la page Fiche point de stock.](media/nav_app_supply_planning_7_transfers6.gif "Contenu de la page Fiche point de stock")  

Lors de la mise à jour d’un point de stock, le système de planification détecte si les systèmes de réapprovisionnement pour les points de stock ont des références circulaires.  

## Planifier des transferts sans point de stock  

Pour les configurations d’entrepôt moins avancées, vous pouvez utiliser des magasins et effectuer des transferts manuels entre les magasins, même si vous n’utilisez pas de points de stock. Par exemple, le transfert peut couvrir une commande vente à cet magasin. Le système de planification réagit aux changements de la demande.  

Pour les transferts manuels, le système de planification analyse les ordres de transfert, puis planifie l’ordre dans lequel traiter les magasins. En interne, le système de planification utilise des points de stock temporaires qui ont des codes niveau de transfert.  

![Code niveau transfert.](media/nav_app_supply_planning_7_transfers7.png "Code niveau transfert")  

S’il existe plusieurs transferts vers un magasin, le premier ordre de transfert définit le sens de la planification. Les transferts en sens inverse sont annulés.  

## Modification de la quantité avec des réservations  

Lors de la modification des quantités d’un approvisionnement, le système de planification prend en compte les réservations. La quantité réservée représente la limite inférieure de réduction de l’offre.  

Lorsque vous modifiez la quantité sur une ligne d’ordre de transfert, gardez à l’esprit la limite inférieure. La limite inférieure est la quantité réservée la plus élevée des lignes de transfert sortantes et entrantes.

Par exemple, une ligne d’ordre de transfert de 117 pièces est réservée pour les lignes suivantes :

* Une ligne de vente de 46
* Une ligne d’achat de 24

Même si le côté entrant peut avoir une offre excédentaire, vous ne pouvez pas réduire la ligne de transfert en dessous de 46.  

![Réservations de planification de transfert.](media/nav_app_supply_planning_7_transfers8.png "Réservations de planification de transfert")  

## Modification de la quantité dans une chaîne de transfert  

Voici un exemple de ce qui se passe lorsque vous modifiez une quantité lors d’un changement de transfert.

Le point de départ est une situation équilibrée avec une chaîne de transfert fournissant une commande client de 27 au magasin ROUGE. Il y a une commande achat correspondante au magasin BLEU. Les deux transferts passent par le magasin ROSE. Il existe deux ordres de transfert, BLEU-ROSE et ROSE-ROUGE.  

![Modification de la quantité dans la planification de transfert 1.](media/nav_app_supply_planning_7_transfers9.png "Modification de la quantité dans la planification de transfert 1")  

À présent, le gestionnaire dans le magasin ROSE choisit de réserver par rapport à l’achat.  

![Modification de la quantité dans la planification de transfert 2.](media/nav_app_supply_planning_7_transfers10.png "Modification de la quantité dans la planification de transfert 2")  

Habituellement, cela signifie que le système de planification ignore la commande achat et la demande de transfert. Tant que l’équilibre est maintenu, il n’y a pas de problème. Mais que se passe-t-il lorsque le magasin ROUGE modifie sa commande de 27 à 22 ?  

![Modification de la quantité dans la planification de transfert 3.](media/nav_app_supply_planning_7_transfers11.png "Modification de la quantité dans la planification de transfert 3")  

Lorsque le système de planification est à nouveau exécuté, il doit se débarrasser de l’approvisionnement excédentaire. Toutefois, la réservation verrouille l’achat et le transfert à une quantité de 27.  

![Modification de la quantité dans la planification de transfert 4.](media/nav_app_supply_planning_7_transfers12.png "Modification de la quantité dans la planification de transfert 4")  

Le transfert ROUGE-ROSE a été réduit à 22. La partie entrante du transfert BLEU-ROSE n’est pas réservée, mais la partie sortante l’est. La réservation signifie que vous ne pouvez pas réduire la quantité en dessous de 27.  

## Calcul du délai  

Lors du calcul de la date d’échéance d’un ordre de transfert, différents types de délai seront pris en compte.  

Les délais suivants sont actifs lors de la planification d’un ordre de transfert :  

* Délai de désenlogement  
* Délai d’expédition  
* Délai d’enlogement  

Sur la ligne planning, les champs suivants sont utilisés pour fournir des informations sur le calcul :  

* Date expédition transfert  
* Date de début  
* Date de fin  
* Date d’échéance  

La date d’expédition de la ligne transfert est indiquée dans le champ **Date expédition transfert**. La date de réception de la ligne transfert est indiquée dans le champ **Date d’échéance**.  

Les dates début et fin décrivent la période réelle de transport.  

L’illustration ci-après montre l’interprétation de la date/heure de début et de la date/heure de fin sur les lignes planning pour les ordres de transfert.  

![Date et heures centrales dans la planification de transfert.](media/nav_app_supply_planning_7_transfers13.png "Date et heures centrales dans la planification de transfert")  

L’exemple montre les calculs suivants :  

* Date d’expédition + Traitement en sortie = Date début  
* Date début + Délai d’expédition = Date fin  
* Date fin + Traitement entrant = Date de réception  

## Délai de sécurité  

Le champ **Délai de sécurité par défaut** de la page **Paramètres production** et le champ associé **Délai de sécurité** sur la page **Fiche article** ne sont pas pris en compte dans les calculs d’un ordre de transfert. Cependant, le délai de sécurité influence la planification totale. Le délai de sécurité affecte l’ordre de réapprovisionnement (achat ou production) au début de la chaîne de transfert. C’est le point où les articles ont été placés au magasin d’où ils seront transférés.  

![Éléments de la date d’échéance de transfert.](media/nav_app_supply_planning_7_transfers14.png "Éléments de la date d’échéance de transfert")  

Sur la ligne O.F., Date fin + Délai de sécurité + Délai enlogement = Date d’échéance.  

Sur la ligne commande achat, Date livraison fournisseur prévue + Délai de sécurité + Délai enlogement = Date réception prévue.  

## Replanifier  

Lorsque vous replanifiez une ligne transfert, le système de planification trouve la partie sortante et modifie la date et l’heure.

> [!NOTE]
> Si un délai est défini, il y aura un écart entre l’expédition et la réception. Le délai peut comporter plusieurs éléments, par exemple le temps de transport et le délai entrepôt. Sur un planning, le système de planification remonte dans le temps pendant qu’il équilibre les éléments.  

![Modification de la date d’échéance dans la planification de transfert.](media/nav_app_supply_planning_7_transfers15.png "Modification de la date d’échéance dans la planification de transfert")  

Lors de la modification de la date d’échéance sur une ligne transfert, le délai doit être calculé pour mettre à jour la partie sortante du transfert.  

## Numéros de série et de lot dans des chaînes de transfert  

Si la demande utilise des numéros de série ou de lot et que vous exécutez le moteur de planification, il créera des ordres de transfert. Pour plus d’informations sur ce concept, voir Attributs d’article. Cependant, si les numéros de série ou de lot sont supprimés de la demande, les ordres de transfert utiliseront toujours les numéros de série ou de lot et la planification les ignorera (mais ne les supprimera pas).  

## Liens ordre pour ordre  

Dans cet exemple, le point de stock BLEU est configuré avec une stratégie de réapprovisionnement **Commander**. Les points de stock ROSE et ROUGE ont la stratégie de réapprovisionnement **Lot pour lot**. La création d’une commande vente de 27 au magasin ROUGE entraîne une chaîne de transferts. Le dernier transfert est au magasin BLEU, et il est réservé avec liaison. Dans cet exemple, les réservations ne sont pas des réservations fermes créées par le planificateur au magasin ROSE. Le système de planification crée les liaisons. La différence importante est que le système de planification peut modifier ces derniers.  

![Liens ordre pour ordre dans la planification de transfert.](media/nav_app_supply_planning_7_transfers16.png "Liens ordre pour ordre dans la planification de transfert")  

Si la demande passe de 27 à 22, le système de planification réduira la quantité tout au long de la chaîne. La réserve contraignante est également réduite.  

## Voir aussi  

[Détails de conception : paramètres de planification](design-details-planning-parameters.md)   
[Détails de conception : tableau d’affectation de planification](design-details-planning-assignment-table.md)   
[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
[Détails de conception : Planification avec/sans magasin](production-planning-with-without-locations.md)   
[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)   
[Détails de conception : équilibrage de la demande et de l’approvisionnement](design-details-balancing-demand-and-supply.md)   
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]