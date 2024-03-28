---
title: "Procédure pas à pas\_: Réception et rangement dans les configurations de stockage de base"
description: Découvrez les différentes façons de gérer les processus entrants pour la réception et le rangement.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Procédure pas à pas : Réception et rangement dans les configurations de stockage de base

Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous recevez des articles et les rangez en utilisant l’une des quatre méthodes décrites dans le tableau suivant.

|Méthode|Processus entrant|Réceptions requises|Rangements requis|Niveau de complexité (pour plus d’informations, consultez [Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Validation de la réception et du rangement à partir de la ligne commande|||Aucune activité entrepôt dédiée.|  
|B|Validation de la réception et du rangement à partir d’un document de rangement stock||Activé|De base : commande par commande.|  
|A|Validation de la réception et du rangement à partir d’un document réception entrepôt|Activé||De base : envoi/réception regroupés pour plusieurs commandes.|  
|J|Validation de la réception d’un document réception entrepôt et validation du rangement à partir d’un document de rangement entrepôt|Activé|Activé|Avancé|  

Learn more at [Flux d’enlogement](design-details-inbound-warehouse-flow.md).

La procédure pas à pas suivante illustre la méthode B dans la table précédente.  

## À propos de cette procédure pas à pas  

Pour les configurations de stockage de base, lorsqu’un magasin est défini pour exiger un traitement des rangements mais pas un traitement des réceptions, utilisez la page **Rangement stock** pour enregistrer et valider les informations de rangement et de réception pour vos documents origine entrants. Les documents suivants sont des documents origine entrants :

* Commande achat
* Retour vente
* Enlogement transfert
* Ordre de fabrication avec sortie prête à être rangée

> [!NOTE]
> Bien que les paramètres soient appelés **Prélèvement requis** et **Rangement requis**, vous pouvez quand même valider les réceptions et les expéditions directement à partir des documents commerciaux origine dans les magasins où vous cochez ces cases.  

Cette procédure pas à pas présente les tâches suivantes :  

* Configurer le magasin ARGENT pour le rangement stock.  
* Configurer le magasin ARGENT pour la gestion d’emplacement.  
* Définir un emplacement par défaut pour l’article LS-81. (LS-75 est déjà défini dans CRONUS).  
* Créer une commande achat de 40 haut-parleurs pour le fournisseur 10000.  
* Vérifier que les emplacements de rangement sont prédéfinis par la configuration.  
* Lancer la commande achat pour l’activité entrepôt.  
* Créer un rangement stock sur la base d’un document origine lancé.  
* Vérifier que les emplacements de rangement sont hérités de la commande achat.  
* Enregistrer le mouvement entrepôt dans l’entrepôt et valider la réception achat pour la commande achat d’origine.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## Rôles  

Les rôles utilisateur suivants effectuent les tâches qui composent cette procédure pas à pas :  

* Gestionnaire d’entrepôt  
* Agent d’achats  
* Magasinier  

## Conditions préalables  

Pour exécuter ce processus pas à pas, vous devez disposer de :  

* données CRONUS International Ltd.  
* être un magasinier à l’emplacement ARGENT. Pour vous configurer, procédez comme suit :  

    1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Employés entrepôt**, puis sélectionnez le lien associé.  
    2. Choisissez le champ **ID utilisateur** et sélectionnez votre compte utilisateur sur la page **Utilisateurs**.  
    3. Dans le champ **Code magasin**, choisissez **ARGENT**.  
    4. Cochez la case **Par défaut**.  

## Scénario  

Ellen, responsable d’entrepôt chez CRONUS International Ltd., crée une commande achat de 10 unités de l’article LS-75 et 30 unités de l’article LS-81 du fournisseur 10000, qui doit être approvisionnée à l’entrepôt ARGENT. Lorsque la livraison arrive à l’entrepôt, Jean, le magasinier, range les articles dans des emplacements par défaut définis pour les articles. Lorsque Jean valide le rangement, les articles sont validés comme étant reçus dans le stock et disponibles à la vente ou pour d’autres demandes.  

## Configuration du magasin  

Les paramètres de la page **Fiche magasin** définissent les flux d’entrepôt de la société.  

### Pour configurer le magasin  

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Magasins**, puis choisissez le lien associé.  
2. Ouvrez la fiche magasin ARGENT.  
3. Activez le bouton à bascule **Rangement requis**.  

    Configurez un emplacement par défaut pour les deux numéros d’article pour contrôler l’endroit où ils sont rangés.  

4. Choisissez l’action **Emplacements**.  
5. Sélectionnez la première ligne, pour l’emplacement **S-01-0001**, puis choisissez l’action **Contenu**.  

    Remarquez sur la page **Contenu emplacement** que l’article **LS-75** est déjà défini comme contenu dans l’emplacement S-01-0001.  

6. Sélectionnez l’action **Nouveau**.  
7. Sélectionnez les champs **Fixe** et **Par défaut**.  
8. Dans le champ **N° article**, saisissez **LS-81**.  

## Créer la commande achat  

Les commandes achat sont le type de document d’origine entrant le plus répandu.  

### Pour créer la commande achat  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes achat**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Créez une commande achat pour le fournisseur 10000 à la date de travail (23 janvier) comportant les lignes commande achat suivantes.  

    |Article ;|Code magasin|Code emplacement|Quantité|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|ARGENT|S-01-0001|10|  
    |LS-81|ARGENT|S-01-0001|30|  

    > [!NOTE]  
    > Le code emplacement est renseigné automatiquement en fonction de la configuration que vous avez créée dans la section [Configuration du magasin](#setting-up-the-location).  

    Ensuite, informez l’entrepôt que la commande achat est prête pour l’activité entrepôt lorsque la livraison arrivera.  

4. Sélectionnez l’action **Lancer**.  

    La livraison des haut-parleurs provenant du fournisseur 10000 est arrivée dans l’entrepôt ARGENT. Jean procède à leur rangement.  

## Recevoir et ranger des articles  

Utilisez la page **Rangement stock** pour gérer toutes les activités entrepôt entrantes pour un document origine spécifique, tel qu’une commande achat.  

### Pour recevoir et ranger des articles  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rangements stock**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Sélectionnez le champ **Document origine**, puis sélectionnez **Commande achat**.  
4. Sélectionnez le champ **N° origine**, sélectionnez la ligne correspondant à l’achat au fournisseur 10000, puis cliquez sur le bouton **OK**.  

    Sinon, choisissez l’action **Extraire document origine**, puis sélectionnez la commande achat.  

5. Choisissez l’action **Remplir qté à traiter**.  

    Sinon, dans le champ **Qté à traiter**, saisissez respectivement 10 et 30 sur les deux lignes rangement stock.  

6. Cliquez sur **Valider**, choisissez l’action **Réceptionner**, puis choisissez le bouton **OK**.  

    Les 40 haut-parleurs sont à présent enregistrés comme rangés dans l’emplacement S-01-0001, et une écriture comptable article positive est créée pour refléter la réception achat validée.  

## Voir aussi  

[Ranger des articles avec le rangement stock](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  
[Configurer des entrepôts de base avec les zones d’opérations](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Prélever pour la fabrication et l’assemblage](warehouse-how-to-pick-for-production.md)  
[Déplacer des articles ad hoc dans les configurations de stockage de base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Détails de conception : flux d’enlogement](design-details-inbound-warehouse-flow.md)  
[Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]