---
title: Configurer et traiter une opération de sous-traitance
description: Procédure pas à pas pour apprendre à configurer et traiter une opération de sous-traitance dans Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Configurer et traiter une opération de sous-traitance

Dans cet article, nous vous expliquons comment utiliser les données de démonstration de Contoso Coffee dans la sous-traitance.

## Scénario

Vous êtes planificateur de production chez Contoso Coffee. En raison de contraintes de capacité, vous envisagez de faire appel à un sous-traitant pour produire l’article **SP-SCM1009, Airpot**.

Vous allez donc créer un ordre de fabrication pour 12 unités de l’article SP-SCM1009, Airpot, à l’aide de la gamme SP-SCM1009-SUB-2. Utilisez la proposition de sous-traitance pour générer un bon de commande pour la fabrication, puis terminez l’opération par la réception et la facturation du bon de commande.

## Étapes

1. Créez un nouvel ordre de fabrication pour 12 unités d’article SP-SCM1009, Airpot.

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **O.F. lancé**, puis sélectionnez le lien associé.  

    2. Cliquez sur l’action **Nouveau**, puis renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ  |Valeur  |
        |---------|---------|
        |**Type origine** |Article ;|
        |**N° origine** |SP-SCM1009|
        |**Quantité** |100|
    3. Choisissez l’action **Actualiser O.F.**.  

2. Remplacez la gamme par SP-SCM1009-SUB-2 dans la ligne d’ordre de fabrication, puis actualisez l’ordre de fabrication mais pour la gamme en question uniquement.  

    1. Ajoutez le champ N° de gamme de fabrication aux lignes dans l’ordre de fabrication lancé.<!--in code, this is marked as visible=false-->

    2. Remplacez le champ **N° gamme** *SP-SCM1009-SERIAL* par *SP-SCM1009-SUB-2*.  

    3. Choisissez l’action **Actualiser O.F.**.  

    4. Sur la page de demande **Actualiser O.F.**, effacez les champs **Lignes** et **Besoin composant** afin que la tâche s’exécute uniquement pour la gamme, puis cliquez sur le bouton **OK**.

3. Utilisez la proposition de sous-traitance pour générer un bon de commande pour l’opération sous-traitée sur l’ordre de fabrication que vous avez créé à l’étape 2.  

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Propositions sous-traitance**, puis sélectionnez le lien associé.  

    2. Choisissez l’action **Générer sous-traitances**.

    3. Sélectionnez le champ **Accepter message d’action** de la nouvelle ligne.

    4. Choisissez l’action **Traiter message d’action**.  

    5. Sur la page de demande **Traiter messages d’action - Demande**, acceptez toutes les valeurs par défaut, puis cliquez sur le bouton **OK**.

    6. Une fois le traitement par lots terminé, cliquez sur le bouton **OK** pour fermer la proposition de sous-traitance.  

4. Réceptionnez et facturez la commande achat.  

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes achat**, puis choisissez le lien associé.  

    2. Sur la liste **Commandes achat**, recherchez la commande achat du fournisseur 82000.

    3. Dans le champ **N° facture fournisseur**, entrez *542349*.

    4. Sélectionnez la ligne sur le raccourci **Lignes**, puis définissez le champ **Coût direct** sur *18*.

    5. Sélectionnez l’action **Valider**.  

    6. Dans le message de demande, choisissez l’option **Réceptionner et facturer**.  

La sortie de l’article SP-SCM1009 Airpot est maintenant enregistrée.

## Voir aussi

[Introduction aux données de démonstration Contoso Coffee](../contoso-coffee-intro.md)  
