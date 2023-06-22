---
title: Détails de conception - Traçabilité et planification | Microsoft Docs
description: 'Puisqu’ils sont enregistrés dans le système de réservation, les numéros de traçabilité sont coordonnés entièrement avec l’enregistrement de chaînage.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-and-planning" />Détails de conception : traçabilité et planification d’article
Puisqu’ils sont enregistrés dans le système de réservation, les numéros de traçabilité sont coordonnés entièrement avec l’enregistrement de chaînage. Cela signifie que les articles qui ont des numéros de suivi de commande peuvent se voir affecter des numéros de suivi d’article. Inversement, les articles qui ont des numéros traçabilité peuvent devenir des enregistrement de chaînage. Pour plus d’informations, voir [Détails de conception : création de traçabilité](design-details-item-tracking-design.md).

Pour plus d’informations sur les systèmes intégrés, voir [Détails de conception : réservations, chaînage et messages d’action](design-details-reservation-order-tracking-and-action-messaging.md).

Comme le chaînage est basé uniquement sur le lettrage d’un article spécifique, la coordination avec des numéros traçabilité s’applique uniquement aux articles qui sont configurés pour utiliser une traçabilité spécifique. Ceci est défini par les champs **N° lot - Traçabilité spéc.** et **N° lot - Traçabilité spéc.** sur la fiche de poste, spécifiant les éléments suivants :

- L’article doit indiquer un numéro de série ou de lot lorsqu’il est validé.
- L’article doit être lettré avec le même numéro de série ou de lot lorsqu’il est validé sortant.

Conformément aux principes standard d’équilibrage de l’approvisionnement/de la demande, le système de planification et la fonction chaînage liée ne met en correspondance qu’un approvisionnement et une demande comportant des numéros traçabilité si l’article en question utilise la traçabilité spécifique. Dans tous les autres cas, les systèmes de planification et de chaînage ignorent les numéros traçabilité lors de l’application d’un approvisionnement pour répondre à une demande ou d’une demande à un approvisionnement. Pour plus d’informations, voir [Détails de conception : réservation, chaînage et message d’action](design-details-reservation-order-tracking-and-action-messaging.md).

Par exemple, lorsque le chaînage existe pour un article donné, cela implique que l’enregistrement de l’article est déjà dans la table **Ecriture réservation**, qui est le cœur du système de réservation, avant que les numéros traçabilité ne soient définis. Par conséquent, les restrictions de couplage suivantes s’appliquent aux numéros de suivi des articles pour le suivi de commande :

- Une demande avec un numéro de série ou un numéro de lot peut couvrir uniquement un approvisionnement de même numéro de série ou de lot.
- Une demande sans numéro de série ou de lot peut couvrir tout approvisionnement, avec ou sans numéro de série ou de lot.

Outre leurs conséquences sur le chaînage dynamique, les restrictions de couplage relatives à la traçabilité n’affectent pas le système de planification de manière significative.

Du côté de l’approvisionnement, un numéro de série ou de lot n’est généralement pas saisi jusqu’à immédiatement avant que la commande soit validée, par exemple une réception achat dans l’entrepôt. En saisissant un numéro de série ou de lot du côté de la demande, comme sur une commande vente, ce numéro de série ou de lot est déjà en stock. Par conséquent, les numéros traçabilité ne sont généralement pas un problème dans la planification de l’approvisionnement.

Pour les articles utilisant la traçabilité, toutes les demandes possédant des numéros de série ou des numéros de lot doivent correspondre à un approvisionnement correspondant. Le plus souvent, il n’apparaît pas raisonnable de regrouper un numéro de série ou de lot particulier, donc la planification des approvisionnements achat ou de production n’est probablement pas affectée. Toutefois, lors du transfert des articles d’un magasin à un autre, il est probable que le transfert soit pour un lot spécifique, donc les approvisionnements de transfert de planification peuvent être affectés par la restriction de couplage spécifique.

Pour plus d’informations, voir [Détails de conception : transferts de planification](design-details-transfers-in-planning.md)

## <a name="balancing-demand-and-supply" />Équilibrage de la demande et de l’approvisionnement
Si un article requiert une traçabilité spécifique, un lien de chaînage est effectué entre toutes les demandes de traçabilité de l’article et n’importe quel approvisionnement de traçabilité correspondant, avec pour seule limitation que l’approvisionnement soit antérieur à la demande. Si, dans ces circonstances, il ne se trouve aucun approvisionnement de traçabilité correspondant à la demande spécifique de traçabilité, un nouvel approvisionnement de traçabilité est créé immédiatement et sans tenir compte de la taille de commande, des paramètres de planification ou de la replanification d’un approvisionnement existant du même numéro de série ou de lot.

Si des numéros traçabilité sont affectés du côté de la demande ou du côté de l’approvisionnement sans nécessiter de traçabilité spécifique, un lien de chaînage est établi entre la demande et cet approvisionnement, sur la base du délai et de la quantité les plus appropriés, comme dans la procédure d’équilibrage habituelle. Le numéro de traçabilité spécifié va dans l’enregistrement de chaînage de la même manière qu’une quantité traçabilité spécifiée définit une extrémité du lien de chaînage. Cela signifie que le numéro de suivi d’article saisi est conservé alors qu’il fait également partie de l’enregistrement de suivi de commande.

Si des numéros traçabilité sont affectés du côté de l’approvisionnement sans nécessiter de traçabilité spécifique, alors cet approvisionnement est considéré comme fixe par le système de planification. Aucun redimensionnement et aucune replanification ne sont proposés pour cet approvisionnement, mais l’approvisionnement est pris en compte lorsque le système de planification tente de répondre aux besoins bruts.

Pour plus d’informations, reportez-vous à [Détails de conception : Équilibrage de la demande et de l’approvisionnement](design-details-balancing-demand-and-supply.md).  

## <a name="see-also" />Voir aussi
[Détails de conception : création de traçabilité](design-details-item-tracking-design.md)  
[Détails de conception : équilibrage de la demande et de l’approvisionnement](design-details-balancing-demand-and-supply.md)  
[Détails de conception : réservation, chaînage et message d’action](design-details-reservation-order-tracking-and-action-messaging.md)   
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
