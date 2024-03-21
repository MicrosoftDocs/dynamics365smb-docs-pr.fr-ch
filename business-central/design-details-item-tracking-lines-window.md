---
title: "Détails de conception\_: page Lignes traçabilité"
description: Découvrez comment gérer le flux de numéros de série et de lot dans votre stock à l’aide de la page Lignes traçabilité.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, inventory, item, tracking, serial number, lot number'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Détails de conception : page Lignes traçabilité
Les enregistrements de traçabilité et de réservation sont créés dans le système de réservation, et leur disponibilité est calculée de façon dynamique. Les données qui sont saisies sur la page **Lignes traçabilité** sont gérées dans une version temporaire de la table **Spécification traçabilité**. Lorsque la page est fermée, les données actives sont validées dans le tableau **Écriture réservation** et les données historiques sont validées dans le tableau **Spécification traçabilité**. Pour plus d’informations, voir [Détails de conception : comparaison entre écritures traçabilité actives et historiques](design-details-active-versus-historic-item-tracking-entries.md).  
  
Les recherches sur les champs **N° de série** et **N° lot** montrent une disponibilité sur la base des deux tables **Écriture comptable article** et **Écriture réservation**, sans le filtre date. La matrice des champs de quantité figurant dans l’en-tête de la page **Lignes traçabilité** affiche de façon dynamique les quantités et les sommes des numéros traçabilité qui sont saisis dans les lignes de la page. Les quantités doivent être égales à celles qui figurent dans la ligne document, comme l’indique la valeur **0** dans les champs **Non défini** de l’en-tête de la page.  
  
Pour coordonner le flux des numéros de série et de lot par le stock, les règles suivantes existent pour saisir des données sur la page **Lignes traçabilité** :  
  
* Pour les lignes traçabilité entrantes et sortantes, vous ne pouvez pas entrer de numéro de série, avec ou sans numéro de lot, plusieurs fois dans la même instance de la page **Lignes traçabilité**. Si vous essayez de saisir une combinaison de numéros de série ou de numéros de lot qui est déjà présente sur la page, un message d’erreur bloque la saisie de données.  
* Pour les lignes traçabilité entrantes, vous ne pouvez pas valider le document connexe si un article de la même variante et avec le même numéro de série est déjà en stock. Si vous essayez de valider une ligne positive pour un article de stock avec une variante et un n° de série identiques, un message d’erreur bloque la validation. Toutefois, pour les lignes traçabilité entrantes et sortantes sur les documents en cours, vous pouvez prendre la même combinaison de numéros de série ou de numéros de lot qui se rapportent à différentes lignes document origine, c.-à-d., existant dans différentes instances de la page **Lignes traçabilité** jusqu’à ce que le document connexe soit validé.  
* Si l’article est configuré pour la traçabilité spécifique au numéro de série ou de lot, vous ne pouvez pas valider une ligne de document sortant sauf si un article avec le numéro de série ou de lot défini apparaît dans le stock. Si vous essayez de valider une ligne de document sortant pour un article avec un n° de série lot non présent dans le stock, un message d’erreur bloque la validation.  
  
Les règles de saisie des données de la page **Lignes traçabilité** prennent également en charge les principes de couplage qui gouvernent le chaînage, la planification et la réservation. Pour plus d’informations, reportez\-vous à [Détails de conception : traçabilité et réservations](design-details-item-tracking-and-planning.md).  
  
## Voir aussi  
[Détails de conception : traçabilité](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]