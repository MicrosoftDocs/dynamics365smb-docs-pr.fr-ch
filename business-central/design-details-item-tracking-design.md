---
title: Détails de conception – création de traçabilité
description: "Cette rubrique décrit la conception de la traçabilité dans Business\_Central au fur et à mesure de son évolution dans les versions de produit."
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item, tracking, tracing'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-design"></a>Détails de conception : création de traçabilité

Traçabilité dans [!INCLUDE[prod_short](includes/prod_short.md)] commencé avec [!INCLUDE [navnow_md](includes/navnow_md.md)]. La fonctionnalité de traçabilité se trouve dans une structure d’objet distincte avec des liens complexes vers les documents validés et les écritures comptables article, et elle est intégrée au système de réservation, qui gère la réservation, le suivi des commandes et la messagerie d’action. Pour plus d’informations, voir [Détails de conception : réservations, suivi de commande et messages d’action](design-details-reservation-order-tracking-and-action-messaging.md) dans les détails de conception de la planification des approvisionnements.  

Ce design incorpore les écritures traçabilité dans les calculs de disponibilité totaux dans tout le système, y compris la planification, la fabrication, et l’entreposage. Les numéros de série et lot sont appliqués aux écritures comptables article pour assurer un accès simple aux données historiques pour la traçabilité. Avec la 1re vague de lancement 2021, la traçabilité dans [!INCLUDE [prod_short](includes/prod_short.md)] comprend les numéros de paquets.  

Avec l’ajout de numéros de série, lot et de paquets, le système de réservation gère les attributs d’article permanents tout en gérant également les liens intermittents entre l’approvisionnement et la demande sous la forme d’écritures de suivi de commande et d’écritures de réservation. Il existe une autre caractéristique qui différencie les numéros de série ou de lot des données de réservation conventionnelles : leur validation peut être effectuée partiellement ou en totalité. Par conséquent, le tableau **Écriture réservation** (T337) s’exécute à présent avec un tableau lié, le tableau **Spécification traçabilité** (T336), qui gère et affiche l’ajout à travers les quantités de suivi article validées. Pour plus d’informations, voir [Détails de conception : comparaison entre écritures traçabilité actives et historiques](design-details-active-versus-historic-item-tracking-entries.md).  

Le schéma suivant explique la conception de la fonctionnalité de traçabilité dans [!INCLUDE[prod_short](includes/prod_short.md)].  

![Exemple de flux de traçabilité.](media/design_details_item_tracking_design.png "Exemple de flux de traçabilité")  

L’objet de validation principal est remodelé pour gérer la sous-classification unique d’une ligne document sous forme de numéros de série ou de lot, et des tables de lien spéciales sont ajoutées pour créer une relation un à plusieurs entre les documents validés et leurs écritures comptables article et écritures comptables de valeur divisées.  

Codeunit 22, **Feuille article – Valider ligne**, fractionne alors la validation en fonction des numéros traçabilité qui sont indiqués sur la ligne document. Chaque numéro traçabilité unique sur la ligne crée sa propre écriture comptable article pour l’article. Cela signifie que le lien de la ligne de document validée vers les écritures comptables article associées est à présent une relation une-à-plusieurs. Cette relation est traitée par les tableaux de relation de suivi d’article suivants.  

|Champ|Désignation|  
|---------------|---------------------------------------|  
|**Lien écriture article** (T6507)|Relie les lignes expédiées ou reçues avec des écritures comptables article|  
|**Lien écriture valeur** (T6508)|Relie les lignes facturées aux écritures valeur|  

Pour plus d’informations, reportez-vous à [Détails de conception : structure de validation de traçabilité](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a>Voir aussi

[Détails de conception : traçabilité](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
