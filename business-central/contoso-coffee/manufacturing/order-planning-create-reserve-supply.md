---
title: Utiliser la planification des commandes pour créer et réserver un approvisionnement
description: Procédure pas à pas pour apprendre à utiliser la planification des commandes pour créer l’ordre de fabrication requis pour l’approvisionnement dans Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Procédure pas-à-pas : Utiliser la planification des commandes pour créer et réserver un approvisionnement

Dans cet article, nous vous expliquons comment utiliser les données de démonstration de Contoso Coffee dans la planification des commandes.

## Scénario

Vous êtes planificateur de production chez Contoso Coffee. Vous avez créé un ordre de fabrication pour 100 unités de l’article **SP-SCM1009, Airpot**, et vous souhaitez planifier des produits semi-finis pour cette commande. Vous utilisez la planification des commandes pour créer l’ordre de fabrication requis pour l’approvisionnement. Étant donné que vous créez l’ordre de fabrication pour répondre aux exigences d’une commande spécifique, vous décidez de réserver la production de l’ordre de fabrication.  

## Étapes

1. Créez le nouvel ordre de fabrication lancé pour 100 unités d’article **SP-SCM1009, Airpot**.

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **O.F. lancé**, puis sélectionnez le lien associé.  

    2. Cliquez sur l’action **Nouveau**, puis renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ  |Valeur  |
        |---------|---------|
        |**Type origine** |Article ;|
        |**N° origine** |SP-SCM1009|
        |**Quantité** |100|
    3. Choisissez l’action **Actualiser O.F.**.  

    Notez le numéro de l’ordre de fabrication lancé.

2. Ouvrez la page **Planification commande** et calculez un nouveau plan.

    1. Sélectionnez l’action **Planification**.  

    2. Sur la page **Planning commande**, choisissez l’action **Calculer planning**.  

    3. Faites défiler jusqu’à la ligne de demande qui représente l’ordre de fabrication lancé que vous avez créé précédemment.  

    4. Développez les lignes pour afficher les détails de la ligne demande. Confirmez qu’il s’agit d’une suggestion pour un ordre de fabrication de 100 unités de l’article 1001.  

3. Créez un nouvel ordre de fabrication pour 100 unités d’article **SP-BOM2000, Reservoir Assy.**, et réservez la sortie de cet ordre de fabrication pour le compte de l’ordre parent associé.  

    1. Cochez la case du champ **Réserver** sur la ligne de demande pour les 100 unités de l’article SP-BOM2000.

    2. Sélectionnez l’action **Créer commandes**.  

    3. Définissez le champ **Créer commandes pour** sur *La ligne active*.  

    4. Définissez le champ **Créer un O.F.** sur *Planifié ferme*.

    5. Cliquez sur le bouton **OK** pour créer l’ordre de fabrication.

    6. Sur la page **Planification commande**, confirmez que la ligne de demande pour les 100 unités de l’article 1001 est supprimée.

C’est tout pour la planification des commandes dans [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## Voir aussi

[Introduction aux données de démonstration Contoso Coffee](../contoso-coffee-intro.md)  
[À propos des ordres de fabrication](../../production-about-production-orders.md)  
