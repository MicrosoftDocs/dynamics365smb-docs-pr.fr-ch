---
title: 'Réception, rangement, prélèvement et expédition dans une configuration d’entrepôt mixte'
description: 'Les processus entrants et sortants peuvent être effectués de différentes manières, en fonction du niveau de complexité de l’entrepôt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 12/07/2023
ms.author: bholtorf
---

# Procédure pas à pas sur les flux entrants ou sortants dans les configurations entrepôt avancées

Cette procédure pas à pas montre comment effectuer des flux entrants et sortants dans la configuration avancée : Prélèvement et rangement dirigés. Pour plus d’informations, voir [Présentation des différentes options de configuration](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## Conditions préalables  
Pour exécuter cette procédure, vous devez faire de vous un magasinier sur le site *BLANC* en procédant comme suit :  
1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Employés entrepôt**, puis sélectionnez le lien associé.  
2. Choisissez le champ **ID utilisateur** et sélectionnez votre propre compte utilisateur sur la page **Utilisateurs**.  
3. Dans le champ **Code magasin**, entrez BLANC.  
4. Activez le bouton à bascule **Par défaut**.


## Scénario  
Ellen, la responsable de l’entrepôt, utilise la fonctionnalité de transbordement et de réapprovisionnement des emplacements pour accélérer les délais de réception et d’expédition.  

## Étapes

1. Créez une expédition entrepôt.  

    1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 2.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
    2. Sélectionnez la commande du client 10000 pour l’emplacement BLANC. Le numéro de commande externe est *W-1*.
    3. Choisissez l’action **Créer expédition entrepôt** pour créer une expédition entrepôt pour la commande client sélectionnée.
    4. Choisissez l’action **Traiter** pour informer l’entrepôt que l’expédition client est prête pour l’activité entrepôt.  

2. Définir des emplacements pour l’article pour contrôler l’endroit où il est rangé 

    1.  Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 3.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
    2.  Sélectionnez *WRB-1000*, puis sélectionnez l’action **Contenus emplacement**.  
    3.  Sélectionnez l’action **Nouveau**. Ajoutez deux lignes.
    
    |Article|Code magasin|Code emplacement|Corrigé|Unité de mesure|
    |----------|----------|---------|---|------|  
    |WRB-1000|BLANC|W-05-0001|Oui|SAC|  
    |WRB-1000|BLANC|W-05-0002|Oui|SAC|

3. Créez une réception entrepôt.  

    1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 4.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes achat**, puis choisissez le lien associé.  
    2. Sélectionnez la commande du fournisseur 10000 pour l’emplacement BLANC. Le numéro de commande fournisseur est *W-2*. Utilisez les outils de personnalisation si le **N° de commande fournisseur** n’est pas visible. Pour plus d’informations, voir [Personnaliser votre espace de travail](../../ui-personalization-user.md).
    3. Choisissez l’action **Créer réception entrepôt** pour créer une réception entrepôt pour la commande achat sélectionnée.


4. Vérifier si des commandes sortantes nécessitent des articles reçus et valider la réception
    1. Choisissez l’action **Calculer transbordement**. Cela remplit une colonne **Quantité à transborder**.
    2. Entrez 0 dans le champ **Quantité à transborder** dans la ligne avec l’article *WRB-1000*, car vous ne prévoyez pas de remballer dans la zone de réception.
    3. Sélectionnez l’action **Valider la réception**.

5. Enregistrer le rangement entrepôt
    1. Utiliser l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 5.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rangement entrepôt**, puis sélectionnez le lien associé.
    2. Localiser le document de rangement entrepôt créé à partir de votre reçu d’entrepôt et l’ouvrir
    3. Sur la page **Rangement entrepôt**, consulter la section **Lignes**

    A ce stade, la logique de capacité de l’emplacement est révélée. les lignes de rangement entrepôt ont trois lignes pour l’article *WRB-1000* :
    - Une ligne de prélèvement pour déplacer les quantités reçues depuis l’emplacement de réception (W-08-0001)
    - Une ligne de placement qui déplace un SAC dans l’un des emplacements fixes configurés (W-05-0001)
    - Une ligne de placement qui déplace un autre SAC dans un autre emplacement fixe (W-05-0002). En effet, un emplacement fixe unique ne peut pas contenir la quantité totale de réception.

    Puisque ce rangement contient des lignes de transbordement, vous voyez trois lignes pour l’article *WRB-1001* :
    -  Une ligne de prélèvement pour déplacer les quantités reçues depuis l’emplacement de réception (W-08-0001)
    -  Une ligne de placement pour les 2 dans l’emplacement de transbordement
    -  Une ligne de placement pour la quantité restante dans l’emplacement de stockage

    4. Choisissez l’action **Enregistrer rangement**.


6. Définir des emplacements de prélèvement pour l’article pour contrôler l’emplacement où il est prélevé 

    1.  Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 6.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Magasins**, puis choisissez le lien associé.  
    2.  Ouvrez la fiche magasin *BLANC*.  
    3.  Choisissez l’action **Emplacements** dans la **Fiche magasin**
    4.  Sélectionnez l’emplacement *W-02-0001*, puis sélectionnez l’action **Contenus**.  
    5.  Sélectionnez l’action **Nouveau**.  
    6.  Activez le bouton à bascule **Fixe**.  
    7.  Dans le champ **N° article**, saisissez *WRB-1000*. 
    8.  Dans le champ **Quantité min.**, saisissez *2*. 
    9.  Dans le champ **Quantité max.**, saisissez *10*. 

    Utilisez les outils de personnalisation si les champs **Quantité min.** et **Quantité max.** ne sont pas visibles. Pour plus d’informations, voir [Personnaliser votre espace de travail](../../ui-personalization-user.md). 

7. Réorganisez l’entrepôt en déplaçant les articles de la zone de stockage en vrac vers la zone de prélèvement, afin d’optimiser le temps de prélèvement.

    1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 7.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles mouvement**, puis choisissez le lien associé
    2. Choisissez l’action **Calculer réappro. emplacement**. 

    La feuille de calcul de l’entrepôt avec la proposition de déplacement de l’article *WRB-1000* du stockage en vrac vers la zone de prélèvement est créée.

    3. Choisissez l’action **Créer mouvement** et confirmez pour créer le document.
    4.  Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 8.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Mouvements entrepôt**, puis sélectionnez le lien associé
    5.  Ouvrez le mouvement d’entrepôt que vous avez créé, passez en revue la section **Lignes**

     À ce stade, la fonctionnalité Déconditionnement s’affiche. Il y a quatre lignes :
    - Une ligne pour sortir un SAC de l’emplacement de stockage en vrac
    - Une ligne pour remettre les 48 pièces en stock dans le même emplacement. 
    - Une ligne pour sortir 10 pièces de l’emplacement de stockage en vrac
    - Une ligne pour placer les 10 pièces dans l’emplacement de prélèvement

    6.  Sélectionnez l’action **Enregistrer mouvement**.

8. Créer prélèvements entrepôt

    1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 9.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles prélèvement**, puis choisissez le lien associé
    2. Choisissez l’action **Obtenir les documents d’entrepôt** , sélectionnez la ligne de la commande client pour le client 10000, puis choisissez le bouton **OK** pour remplir les lignes de la feuille de calcul en fonction du document sélectionné.

    3. Inspectez le champ **Quantité à l’emplacement de transbordement**. 

    4. Choisissez l’action **Créer prélèvement**.
    5. Confirmez tous les paramètres de prélèvement nécessaires, par exemple, activez le bouton à bascule **Par zone de départ**. Cliquez sur le bouton **OK**.
    
    Vous recevez un message de confirmation avec les numéros de prélèvement. Il y a deux prélèvements, car certains articles sont situés dans la zone de transbordement, à proximité de la zone d’expédition, et il serait logique de les traiter séparément.

9.  Enregistrer les prélèvements d’entrepôt
    1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 10.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Prélèvements entrepôt**, puis choisissez le lien associé.
    2. Localisez les prélèvements que vous avez créés et ouvrez-les.
    3. Choisissez l’action **Enregistrer prélèvement**.
    4. Répétez l’opération pour le deuxième prélèvement

10. Valider l’expédition entrepôt
    
    1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 11.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Expédition entrepôt**, puis choisissez le lien associé.
    2. Sur la page Rangement entrepôt, consulter la section **Lignes**. Une fois le prélèvement d’entrepôt enregistré, l’expédition d’entrepôt est mise à jour avec le champ **Quantité à expédier** renseigné.
    3. Sélectionnez ensuite l’action **Valider expédition**.
    4. Confirmez l’option **Expédier**.


## Résultats
- la **Réception entrepôt enregistrée** est créée
- le **Rangement entrepôt enreg.** est créé    
- la **Réceptions achat enregistrées** est créée    
- la **Commande achat** a la **Quantité reçue** mise à jour pour les lignes reçues
- le **Mouvement entrepôt enreg.** est créé
- le **Prélèvement entrepôt enreg.** est créé
- l’**Expédition entrepôt enregistrée** est créée
- l’**Expédition vente enregistrée** est créée
- la **Commande client** a la **Quantité expédiée** mise à jour pour les lignes expédiées
- le **Stock** d’articles est augmenté de tout reliquat non expédié



## Voir aussi
[Recevoir des articles](../../warehouse-how-receive-items.md) 
[Détails de conception : Flux d’enlogement](../../design-details-inbound-warehouse-flow.md) 
[Expédier les articles](../../warehouse-how-ship-items.md) 
[Prélever les articles pour expédition entrepôt](../../warehouse-how-to-pick-items-for-warehouse-shipment.md) 
[Détails de conception : Flux de désenlogement](../../design-details-outbound-warehouse-flow.md) 
[Afficher la disponibilité des articles](../../inventory-how-availability-overview.md) 
