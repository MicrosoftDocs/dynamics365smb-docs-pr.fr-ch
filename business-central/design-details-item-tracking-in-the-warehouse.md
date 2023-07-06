---
title: "Détails de conception\_: traçabilité dans l’entrepôt"
description: Les documents d’entrepôt entrants et sortants ont une fonctionnalité standard pour l’attribution et la sélection des numéros de traçabilité.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item, tracking, serial number, lot number, outbound documents'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-in-the-warehouse"></a><a name="design-details-item-tracking-in-the-warehouse"></a><a name="design-details-item-tracking-in-the-warehouse"></a>Détails de conception : traçabilité dans l’entrepôt
La gestion de numéro de série et de numéro de lot est surtout une tâche d’entrepôt, et donc tous les documents entrepôt enlogement et désenlogement ont une fonctionnalité standard pour affecter et sélectionner des numéros traçabilité.  

Toutefois, comme le système de réservation est basé sur les écritures comptables article, les documents activité entrepôt qui enregistrent uniquement les écritures entrepôt ne sont pas totalement pris en charge. Comme les réservations et les numéros traçabilité peuvent uniquement être traités au niveau du magasin, pas au niveau de l’emplacement et de la zone, la page **Lignes traçabilité** ne peut pas être ouverte à partir des documents activité entrepôt. Cela s’applique également à la page **Réservation**.  

Une fois qu’un numéro de série ou un numéro de lot a été ajouté à un article d’un entrepôt, il peut être déplacé et reclassé librement au sein de l’entrepôt à l’aide d’une structure de traçabilité distincte, qui n’est pas liée au système de réservation. Les champs **N° de série** et **N° lot** sont consultés directement dans les lignes document entrepôt. Lorsque le numéro de série ou de lot participe ultérieurement à une validation sortante, il est synchronisé avec le système de réservation en tant que partie d’ajustement d’emplacement ordinaire. Pour plus d’informations, voir [Détails de conception : intégration avec le stock](design-details-integration-with-inventory.md).  

Cependant, le système de réservation prend en compte les activités entrepôt pour calculer la disponibilité. Par exemple, des articles qui sont affectés aux prélèvements ou enregistrés comme prélevés, ne peuvent pas être réservés. Pour plus d’informations, voir [Détails de conception : disponibilité de l’entrepôt](design-details-availability-in-the-warehouse.md).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi
[Détails de conception : traçabilité](design-details-item-tracking.md)  
[Détails de conception : intégration avec le stock](design-details-integration-with-inventory.md)  
[Détails de conception : Disponibilité de l’entrepôt](design-details-availability-in-the-warehouse.md)  
[Détails de conception : création de traçabilité](design-details-item-tracking-design.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
