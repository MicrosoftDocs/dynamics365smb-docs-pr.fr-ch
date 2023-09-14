---
title: Combiner la consommation automatique et la consommation manuelle
description: Procédure pas à pas pour un gestionnaire de production chez Contoso Coffee qui souhaite combiner la consommation automatique et et la consommation manuelle.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Procédure pas à pas : Combiner la consommation automatique et la consommation manuelle

Dans cet article, nous vous expliquons comment utiliser les données de démonstration Contoso Coffee dans la consommation.  

## Scénario

Vous êtes planificateur de production chez Contoso Coffee. Vous devez créer un nouvel ordre de fabrication pour 10 unités de l’article SP-SCM1004, AutoDrip. Certains composants et certaines opérations seront consommés en aval et d’autres consommés en amont en fonction de différentes conditions.

## Étapes

> [Remarque !] N’oubliez pas d’ajuster le stock en validant la feuille article avec les soldes d’ouverture.

1. Créez un ordre de fabrication planifié ferme pour 5 unités de l’article **SP-SCM1004, AutoDrip** à l’emplacement *NORD*. Pour obtenir des conseils, voir [Procédure pas à pas : Créer un ordre de fabrication planifié ferme et le modifier](create-firm-planned-production-order-change.md).  

2. Lancez l’ordre de fabrication.

    1. Choisissez l’action **Modifier statut**.  

    2. Dans la page qui s’affiche, définissez le champ **Nouveau statut** sur *Lancé*, puis choisissez le bouton **Oui**.  

        Un message avec une barre d’état s’affiche et fait référence à la consommation automatique. Il est suivi d’un message de confirmation indiquant que l’ordre est modifié pour avoir le statut *Lancé*.  

    3. Cliquez sur le bouton **OK** pour fermer le message de confirmation.

3. Vérifiez les écritures comptables article et capacité pour l’ordre de fabrication.

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **O.F. lancé**, puis sélectionnez le lien associé.  

    2. Ouvrez l’ordre de fabrication avec les 5 unités de la machine à café AutoDrip.  

    3. Sélectionnez l’action **Écritures comptables article**.  

        L’article **SP-BOM1305 Vis hex m3, zinc** est immédiatement consommé avec la quantité prévue totale. Fermez la page **Écritures comptables article**.  

    4. Choisissez l’action **Écritures comptables capacité**.  Notez qu’une écriture d’opérations d’assemblage du corps a également été effectuée au moment du lancement de la commande. Fermez la fenêtre **Écritures comptables capacité**.

    Vous pouvez consommer manuellement les composants à l’aide de la feuille consommation ou de la feuille production. La consommation manuelle vous permet d’ajuster la quantité avant de valider. Par exemple, si une quantité supplémentaire est nécessaire pour couvrir des matières premières de faible qualité.
4. Consommer les composants manuellement.  
    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille consommation**, puis choisissez le lien associé.  

    2. Choisissez l’action **Calculer consommation**.  

    3. Dans la page de demande **Calculer consommation**, dans le raccourci **Ordre de fabrication**, définissez un filtre pour l’ordre spécifique dans le champ **N° d’ordre**, puis choisissez le bouton **OK**. Après la fermeture de la page de demande de traitement par lots, notez que la page **Feuille consommation** se remplit avec les composants qui nécessitent une consommation manuelle.

    4. Choisissez l’action **Valider**. Fermez la feuille consommation.

5. Enregistrez manuellement la production pour le câblage électrique.  

    Vous devez renseigner manuellement les champs **Temps de préparation** et **Temps d’exécution**. Vous pouvez également spécifier la quantité réellement produite et le rebut. Entrer *3* comme quantité de production et validez la production.

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille production**, puis choisissez le lien associé.  

    2. Sur la page **Feuille production**, créez une ligne feuille.  

    3. Dans le champ **N° d’ordre**, spécifiez l’ordre.  

    4. Choisissez l’action **Éclater gamme**.  

        La page **Feuille production** se remplit avec la ligne d’opération uniquement pour le câblage électrique.

    5. Définissez le champ **Temps d’exécution** sur *10*.  

    6. Remplacez la valeur du champ **Quantité** *5* par *3*.

    7. Choisissez **Valider**.  
    8. Fermez la feuille production.

6. Vérifiez les écritures comptables article pour l’ordre de fabrication.

    1. Dans la page de l’ordre de fabrication, choisissez l’action **Écritures comptables article**.  

    L’article **SP-BOM1302, Affich. panneau conf.** est validé avec une quantité de *3*, sur la base de la production réelle, tandis que l’article **SP-BOM1303, Bouton** est validé avec la quantité prévue totale. Fermez la page **Écritures comptables article**.

7. Terminez l’ordre de fabrication.  

    1. Choisissez l’action **Modifier statut**.
    2. Dans la page qui s’affiche, définissez le champ **Nouveau statut** sur *Terminé*, puis choisissez le bouton **Oui**.  

        Un message s’affiche avec une barre d’état qui reflète la consommation automatique. Il est suivi d’un message de confirmation indiquant que l’ordre est transformé en ordre avec le statut *Terminé*. L’ordre de fabrication terminé a le même numéro que celui qu’il avait avec le statut *Lancé*.
    3. Cliquez sur le bouton **OK** pour fermer le message de confirmation.

8. Vérifiez à nouveau les écritures comptables article et capacité pour l’ordre de fabrication.

    1. Choisissez l’action **Écritures comptables capacité**.  

        L’écriture des opérations de livraison a été réalisée au moment du lancement de la commande. La quantité produite (production) est *5*, quelle que soit la production de l’étape précédente. Fermez la page **Écritures comptables capacité**.

    2. Sélectionnez l’action **Écritures comptables article**.  

        La quantité de l’écriture comptable article du type *Production* est égale à la quantité produite dans l’écriture comptable capacité. La quantité consommée des articles **SP-BOM1301, AutoDrip logement** et **SP-BOM1304, Carafe therm. acier inox** est 5, car la production prévue et la production réelle sont les mêmes. 

    3. Fermez la page **Écritures comptables article**.  

C’est tout pour la consommation manuelle et automatique des composants.

## Voir aussi

[Consommer des composants en fonction de la production réalisée](../../production-how-to-flush-components-according-to-operation-output.md)  
[Introduction aux données de démonstration Contoso Coffee](contoso-coffee-manufacturing-intro.md)  
