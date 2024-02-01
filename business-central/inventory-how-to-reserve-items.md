---
title: "Procédure\_: réserver des articles"
description: 'Découvrez comment réserver des articles pour les commandes vente, les commandes achat et les ordres de fabrication.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: null
ms.search.forms: '498, 497'
ms.date: 09/19/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Réservation des articles

Vous pouvez réserver des articles pour les commandes vente, les commandes service, les ordres d’assemblage, les ordres de transfert et les ordres de fabrication. Vous pouvez également réserver des articles en stock ou entrants sur les lignes document ou les lignes feuille ouvertes. Vous faites cela sur la page **Réservation**.

Chaque ligne que vous ouvrez pour réserver des articles sur la page **Réservation**, que vous ouvrez pour réserver des articles, donne des informations sur un type de ligne (vente, achat ou feuille) ou d’écriture de stock. Les lignes décrivent le nombre d'articles disponibles pour réservation à partir de chaque type de ligne ou d'écriture.

> [!TIP]
> En fonction des quantités que vous avez réservées dans l’inventaire, [!INCLUDE [prod_short](includes/prod_short.md)] affiche un statut sur les documents afin que vous soyez rapidement informé de l’étape suivante. Par exemple, pour indiquer que vous pouvez expédier une commande client ou commencer à travailler sur un ordre de travail, d’assemblage ou de fabrication. Ce statut aide également à réduire le risque d’expéditions partielles accidentelles ou de retards dus à un stock manquant pour les ordres de fabrication et d’assemblage.
>
> Le champ **Réservé à partir du stock** peut vous aider à comprendre si vous pouvez expédier ou prélever une commande ou une ligne de commande spécifique. Pour les lignes, le champ Réservé à partir du stock est disponible dans les récapitulatifs. Pour accéder aux informations de toute la commande, le champ se trouve sur la page **Statistiques**.

## Réserver des articles pour des ventes

Ce qui suit décrit comment réserver des articles pour une commande vente. Les étapes sont similaires à celles des commandes achat, service, ordre de transfert et ordre d’assemblage.
  
1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Choisissez la commande vente.
3. Sur le raccourci **Lignes**, choisissez l’action **Réserver**. La page **Réservation** s’affiche.  
4. Sélectionnez la ligne à partir de laquelle vous souhaitez réserver des articles.  
5. Choisissez l’une des actions suivantes.  

    |**Fonction.**|**Description**|
    |------------------|---------------------|  
    |**Réservation automatique**|Permet de réserver automatiquement des articles sur la page **Réservation**.|  
    |**Réserver à partir de la ligne courante**|Permet de réserver des articles sur la ligne du document que vous avez sélectionnée.|  
    |**Annuler la réservation de la ligne courante**|Permet d’annuler la réservation d’articles sur la ligne du document que vous avez sélectionnée.|

> [!NOTE]  
> Si des lignes traçabilité article existent pour la commande vente, le système de réservation vous fera suivre une procédure spéciale : Pour plus d’informations, voir la section [Pour réserver un numéro de série ou de lot particulier](inventory-how-to-reserve-items.md#reserve-a-specific-serial-or-lot-number).  

## Réserver un article pour une ligne O.F.

Vous pouvez réserver des articles pour des ordres de fabrication. Vous devez distinguer les lignes O.F., qui correspondant à l’article parent, des composants O.F.

La procédure suivante s’appuie sur un ordre de fabrication planifié ferme.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. planifié ferme**, puis sélectionnez le lien associé.  
2. Ouvrez l’O.F. planifié ferme pour lequel vous souhaitez réserver des articles parents.  
3. Sélectionnez la ligne ordre de fabrication concernée.  
4. Sur le raccourci **Lignes**, choisissez l’action **Réserver**.
5. Sur la page **Réservation**, sélectionnez la ligne **Ligne vente, commande**, puis sélectionnez l’action **Réserver à partir de la ligne courante**.  

La quantité entrée dans la ligne O.F. planifié ferme est désormais réservée.

## Réserver des articles pour des composants O.F.

Vous pouvez réserver des articles pour des ordres de fabrication. Vous devez distinguer les lignes O.F., qui correspondant à l’article parent, des composants O.F.

La procédure suivante s’appuie sur un ordre de fabrication planifié ferme.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. planifié ferme**, puis sélectionnez le lien associé.  
2. Ouvrez l’O.F. planifié ferme pour lequel vous souhaitez réserver des articles composant.  
3. Sélectionnez la ligne ordre de fabrication concernée.  
4. Sur le raccourci **Lignes**, choisissez **Ligne**, puis **Composants**.  
5. Sélectionnez la ligne de composant appropriée.  
6. Sur le raccourci **Lignes**, choisissez l’action **Réserver**.  
7. Sur la page **Réservation**, sélectionnez une ligne, puis sélectionnez l’action **Réserver à partir de la ligne courante**.  

La quantité entrée dans la ligne de composant production planifié ferme est désormais réservée.

## Réserver des articles en bloc

Utilisez la page **Feuille réservation** pour réserver et affecter des marchandises entrantes en bloc. Par exemple, les réservations en bloc peuvent aider à garantir que les quantités sont disponibles pour vos commandes vente et vos ordres de fabrication. Vous pouvez avoir plusieurs traitements par lots pour différents objectifs. Par exemple, vous pouvez affecter des ordres de production chaque semaine mais les réserver chaque jour pour la vente.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Feuille réservation**, puis choisissez le lien associé.  
2. Choisissez l’action **Obtenir la demande**, puis spécifiez le type de demande que vous souhaitez réserver à partir de l’inventaire disponible.
3. Dans le champ **Réservé à partir du stock**, choisissez l’une des options suivantes :
    
   |Champ  |Désignation  |
   |---------|---------|
   |Vide     | La quantité restante n’est pas réservée du tout, ou elle est réservée à partir d’autres documents origine, comme les commandes achat.        |
   |COMPLET    |  La quantité restante est entièrement réservée à partir de l’inventaire disponible.       |
   |Partiel     | La quantité restante est partiellement réservée à partir de l’inventaire disponible.        |

4. Renseignez les champs selon vos besoins. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
5. Facultatif : pour affecter les articles immédiatement, choisissez l’action **Affecter**.
6. Sur la page **Stratégie d’affectation**, choisissez une stratégie pour chaque étape

   |Stratégie d’affectation  |Désignation  |
   |---------|---------|
   |Basique     | Affecte un stock à une demande s’il n’y a pas de conflits et que la demande peut être entièrement couverte. Par exemple, vous avez une commande client A avec une quantité de 10 et un projet avec une quantité de 7. Si vous en avez 20 en stock, les deux demandes reçoivent la quantité complète. Si votre stock est de 12, aucun stock n’est affecté. Vous devez affecter manuellement la quantité.        |
   |Répartir    | Distribue le stock disponible à la demande de manière équitable. Par exemple, vous avez une commande client avec une quantité de 10 et un projet avec une quantité de 7. Si votre niveau de stock est de 20, alors les deux demandes reçoivent la quantité complète. Si votre stock est de 12, alors les deux demandes obtiennent 6.        |

7. Pour réserver toutes les lignes où **Accepter** est activé, choisissez l’action **Créer une réservation**.
    
## Modifier une réservation

Vous pouvez modifier une réservation d’article.

1. À partir de la ligne document à partir de laquelle vous avez fait la réservation, dans le raccourci **Lignes**, choisissez l’action **Réserver**.  
2. Sur la page **Réservation**, choisissez l’action **Écritures réservation**.
3. Sur la page **Écritures réservation**, mettez à jour le champ **Quantité** de la ligne à modifier.
4. Confirmez le message qui suit en cliquant sur le bouton **OK**.

## Annuler des réservations

Vous pouvez annuler une réservation d’article.

1. À partir de la ligne document à partir de laquelle vous souhaitez annuler une réservation, dans le raccourci **Lignes**, choisissez l’action **Réserver**.  
2. Sur la page **Réservation**, choisissez l’action **Écritures réservation**.  
3. Sur la page **Écritures réservation**, choisissez l’action **Annuler la réservation**.  
4. Confirmez le message qui suit en cliquant sur le bouton **Oui**.  

## Réserver un numéro de série ou de lot particulier

À partir des documents sortants pour les articles suivis, comme des commandes vente ou des listes de composants de production, vous pouvez réserver des numéros de série ou de lot spécifiques. Par exemple, réserver des numéros de série ou de lot spécifiques peut être utile dans les situations suivantes :

* Si des composants de production d’un lot spécifique sont nécessaires pour garantir la cohérence avec les lots de production précédents.
* Parce qu’un client a demandé un numéro de série spécifique. 

Pour plus d’informations, voir [Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md).

Il s’agit d’une réservation spécifique, parce que vous réservez à partir de la quantité de l’article X qui appartient au Lot X. Si vous réservez seulement à partir des quantités de l’article X, la réservation est normale, non spécifique. En savoir plus sur [Détails de conception – Traçabilité et réservations](design-details-item-tracking-and-reservations.md).

La procédure suivante se base sur une commande vente.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Créez une ligne commande vente d’un article suivi.  
3. Affectez des numéros de série et de lot à la ligne commande vente. Pour plus d’informations, voir [Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md).
4. Sur la ligne commande vente, sélectionnez l’action **Réserver**.  
5. Cliquez sur le bouton **Oui** pour réserver des numéros de série ou de lot spécifiques.  
6. Sur la page **Liste traçabilité**, sélectionnez la combinaison de numéros de série et de lot que vous venez d’affecter.  
7. Cliquez sur le bouton **OK** pour ouvrir une page **Réservation** affichant uniquement l’approvisionnement portant le numéro de traçabilité spécifié. S’il y a des réservations non spécifiques sur l’un des numéros traçabilité que vous avez spécifiés pour cette ligne, vous êtes informé que la quantité a déjà été réservée.  
8. Sélectionnez l’action **Réservation automatique** ou **Réserver à partir de la ligne courante** pour créer la réservation sur les numéros traçabilité spécifiques.

## Voir aussi

[Stock](inventory-manage-inventory.md)  
[Détails de conception : réservation, chaînage et message d’action](design-details-reservation-order-tracking-and-action-messaging.md)  
[Détails de conception : traçabilité et réservations](design-details-item-tracking-and-reservations.md)  
[Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
