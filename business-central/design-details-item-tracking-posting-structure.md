---
title: "Détails de conception\_-\_Structure de validation de traçabilité"
description: Découvrez comment utiliser les écritures comptables article comme principal opérateur des numéros traçabilité dans la structure de validation de traçabilité.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item tracking, posting, inventory'
ms.date: 06/15/2021
ms.author: bholtorf
---
# Détails de conception : structure de validation de traçabilité
Pour s’aligner sur la fonctionnalité d’évaluation du stock et obtenir une solution plus simple et plus robuste, les écritures comptables article sont utilisées comme principal opérateur des numéros de suivi d’article.  
  
Les numéros traçabilité sur les entités réseau de commande et les entités réseau sans rapport avec les commandes sont spécifiés dans la table **Ecriture réservation** (T337). Des numéros traçabilité qui sont liés aux informations historiques sont récupérés directement à partir des écritures comptables article qui sont associées à la transaction en question. Cela signifie que les écritures comptables article reflètent la spécification de suivi d’article de la ligne de commande validée.  
  
La page **Lignes traçabilité** extrait les informations de T337 et les écritures comptables article et les affiche par le biais de la table temporaire, **Spécification traçabilité** (T336). T336 contient également les données temporaires dans la **page lignes traçabilité** pour les quantités de traçabilité article restant à facturer.  
  
## Relation un-à-plusieurs  
La table **Lien écriture article**, qui sert à lier une ligne document validée avec ses écritures comptables article correspondantes, est composée de deux parties principales :  
  
* Un pointeur vers la ligne document validée, le champ **N° ligne commande**. .  
* Un numéro de séquence pointant vers une écriture comptable article, le champ **N° écriture article**.  
  
La fonctionnalité du champ **N° séquence** existant, qui relie une écriture comptable article à une ligne document validé, gère la relation typique un pour un lorsqu’aucun numéro traçabilité n’est indiqué dans la ligne document validé. Si des numéros traçabilité existent, le champ **N° séquence** est laissé vide, et la relation un à plusieurs est gérée par la table **Lien écriture article**. Si la ligne document validée possède des numéros traçabilité mais n’est liée qu’à une seule écriture comptable article, le champ **N° séquence** gère la relation, et le n° d’enregistrement est créé dans la table **Lien écriture article**.  
  
## Codeunits 80 et 90  
Pour répartir les écritures comptables article lors de la validation, le code dans codeunit 80 et codeunit 90 est encerclé par des boucles qui s’exécutent à travers des variables de bilan temporaire global. Ce code appelle codeunit 22 avec une ligne feuille article. Ces variables sont initialisées lorsque les numéros de suivi des articles existent pour la ligne document. Pour garder un code simple, cette structure de bouclage est toujours utilisée. Si aucun numéro traçabilité n’existe pour la ligne document, un enregistrement unique est inséré, et la boucle ne s’exécute qu’une fois.  
  
## Validation de la feuille article  
Des numéros traçabilité sont transférés via des écritures réservation en relation avec l’écriture comptable article, et le bouclage par l’intermédiaire des numéros traçabilité se produit dans le codeunit 22. Ce concept fonctionne de la même manière lorsqu’une ligne feuille article est utilisée indirectement pour valider une commande vente ou achat que lorsqu’une ligne feuille article est utilisée directement. Lorsque la feuille article est utilisée directement, le champ **Lien origine** pointe vers la ligne feuille article elle-même.  
  
## Unité de code 22  
Codeunits 80 et 90 bouclent l’appel du codeunit 22 lors de la validation de facture des numéros traçabilité et lors de la facturation des expéditions ou des réceptions existantes.  
  
Lors de la validation de quantité des numéros traçabilité, le codeunit 22 extrait les numéros traçabilité des écritures dans T337 liées à la validation. Ces écritures sont placées directement sur la ligne feuille article.  
  
Codeunit 22 boucle via les numéros traçabilité et répartit la validation dans les écritures comptables article correspondantes qui contiennent les numéros traçabilité. Les informations sur les écritures comptables article qui sont créées sont renvoyées à T337 à l’aide d’un enregistrement temporaire T336, qui est appelé par une procédure dans le codeunit 22. Cette procédure est déclenchée lorsque le codeunit 22 a terminé son exécution car à ce stade, l’objet du codeunit 22 contient les informations. Lorsque l’enregistrement temporaire T336 est récupéré, les codeunits 80 et 90 créent des enregistrements dans le tableau **Lien écriture article** pour lier les écritures comptables article créées à l’expédition ou la ligne de réception créée. Codeunits 80 ou codeunit 90 convertit ensuite les enregistrements T336 temporaires en enregistrements réels T336 liés à la ligne en question. Cependant, cette conversion se produit uniquement si la ligne document validée n’est pas supprimée, parce qu’elle n’est que partiellement validée.  
  
## Voir aussi  
[Détails de conception : traçabilité](design-details-item-tracking.md)   
[Détails de conception : création de traçabilité](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]