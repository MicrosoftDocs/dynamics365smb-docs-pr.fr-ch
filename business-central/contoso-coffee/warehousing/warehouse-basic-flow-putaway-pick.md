---
title: 'Réception, rangement, prélèvement et expédition dans une configuration d’entrepôt de base'
description: "Dans Business\_Central, les processus entrants et sortants peuvent être effectués de quatre manières, à l’aide de différentes fonctionnalités en fonction du niveau de complexité de l’entrepôt."
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-basic-warehouse-configurations"></a>Procédure pas à pas sur les flux entrants ou sortants dans les configurations entrepôt de base

Cette procédure pas à pas montre comment effectuer des flux entrants et sortants dans la configuration de base : commande par commande. Pour plus d’informations, voir [Présentation des différentes options de configuration](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Conditions préalables
Pour exécuter cette procédure, vous devez faire de vous un magasinier sur le site *ARGENT* en procédant comme suit :  
1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Employés entrepôt**, puis sélectionnez le lien associé.  
2. Choisissez le champ **ID utilisateur** et sélectionnez votre propre compte utilisateur sur la page **Utilisateurs**.  
3. Dans le champ **Code magasin**, entrez *ARGENT*.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Flux entrant : Réception et rangement dans les configurations de stockage de base

Dans [!INCLUDE[prod_short](../../includes/prod_short.md)], les processus entrants de réception et de rangement peuvent être effectués de quatre manières, à l’aide de différentes fonctionnalités en fonction du niveau de complexité de l’entrepôt.  

|Méthode|Processus entrant|Emplacements|Bons de réception|Rangements|Niveau de complexité (Voir [Détails de conception : paramètres entrepôt](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Validation de la réception et du rangement à partir de la ligne commande|X|||2|  
|B|Validation de la réception et du rangement à partir d’un document de rangement stock|||X|3|  
|C|Validation de la réception et du rangement à partir d’un document réception entrepôt||X||5/4/6|  
|J|Validation de la réception d’un document réception entrepôt et validation du rangement à partir d’un document de rangement entrepôt||X|X|5/4/6|  

Pour plus d’informations, reportez\-vous à [Détails de conception : flux d’enlogement](../../design-details-inbound-warehouse-flow.md).  

La procédure pas à pas suivante illustre la méthode B dans la table précédente.  

### <a name="scenario"></a>Scénario
Alicia, l’agent achat, crée une commande achat pour divers grains torréfiés. Lorsque la livraison arrive à l’entrepôt, John, le magasinier, range les articles dans des emplacements adaptés. Lorsque Jean valide le rangement, les articles sont validés comme reçus dans le stock et disponibles à la vente ou à une autre demande.  

### <a name="steps"></a>Étapes
1. Configurez la page **Fiche magasin** pour définir les flux d’entrepôt entrants de la société.  

    1.  Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 2.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Magasins**, puis choisissez le lien associé.  
    2.  Ouvrez la fiche magasin *ARGENT*.  
    3.  Activez la case à cocher **Rangement requis**.  

2. Définissez un emplacement par défaut pour les deux numéros d’article pour contrôler l’endroit où ils sont rangés

    1.  Choisissez l’action **Emplacements** dans la **Fiche magasin**
    2.  Sélectionnez la première ligne, pour l’emplacement *S-1-01*, puis choisissez l’action **Contenu**.  
    3.  Sélectionnez l’action **Nouveau**.  
    4.  Sélectionnez les champs **Fixe** et **Par défaut**.  
    5.  Dans le champ **N° article**, saisissez *WRB-1000*.  

3. Créez la commande achat, qui est le type de document d’origine entrant le plus répandu.  

    1.  Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 3.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes achat**, puis choisissez le lien associé.  
    2.  Sélectionnez l’action **Nouveau**.  
    3.  Créez une commande achat pour le fournisseur 10000 comportant les lignes commande achat suivantes. Utilisez les outils de personnalisation si le champ **Code emplacement** n’est pas visible. Pour plus d’informations, voir [Personnaliser votre espace de travail](../../ui-personalization-user.md). 

    |Article ;|Code magasin|Code emplacement|Quantité|  
    |----------|----------|---------|--------------|  
    |WRB-1000|ARGENT|S-1-01|20|  
    |WRB-1001|ARGENT||30|

    Le code emplacement dans le premier article est rempli conformément à la configuration. Le code emplacement du deuxième article est vide, car il n’a pas de valeurs par défaut. Ne le modifiez pas.  

    4.  Choisissez l’action **Traiter** pour informer l’entrepôt que la commande achat sélectionnée est prête pour l’activité entrepôt lorsque la livraison arrive.  

4. Créer **Rangement stock** pour recevoir et ranger les articles livrés  

    1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 4.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rangements stock**, puis sélectionnez le lien associé.  
    2. Sélectionnez l’action **Nouveau**. 
    3. Sélectionnez *ARGENT*, dans le champ **Code magasin**.
    4. Sélectionnez le champ **Document origine**, puis sélectionnez **Commande achat**.  
    5. Sélectionnez le champ **N° source** , sélectionnez la ligne pour l’achat auprès du fournisseur 10000, puis choisissez le bouton **OK** pour remplir les lignes de rangement en fonction du document source sélectionné.

        Sinon, choisissez l’action **Extraire document origine**, puis sélectionnez la commande achat.  

5. Modifier le rangement stock en fonction du placement réel des articles et valider le document

    Lors du rangement des articles aux emplacements, John a remarqué que l’emplacement par défaut contenait déjà certains articles, il a donc décidé d’utiliser un autre emplacement. John place également d’autres articles dans les emplacements suivants, car la quantité reçue ne correspond pas à la capacité.

    1. Dans la première ligne, modifiez le **Code emplacement** de *S-1-01*, qui a été copié à partir de la commande achat, vers *S-1-02*. 
    2.  Saisissez 20 dans le champ **Quantité à traiter** de la ligne de rangement stock avec l’article WBR-1000.  
    3. Sur la deuxième ligne, saisissez 20 dans le champ **Quantité à traiter** et choisissez l’action **Éclater ligne**. Une nouvelle ligne s’affiche. Il s’agit d’une copie de la ligne d’origine, à la différence près que la quantité que vous avez retirée de la ligne d’origine figure dans le champ **Quantité à traiter**. 
    4. Remplissez les codes emplacements pour l’article WBR-1001 :

    |Article ;|Code emplacement|Quantité|  
    |----------|-------------------|--------------|  
    |WRB-1001|S-1-03|20|  
    |WRB-1001|S-1-04|10|

    5.  Cliquez sur **Valider**, choisissez l’action **Réceptionner**, puis choisissez le bouton **OK**.  

### <a name="results"></a>Résultats
 - les grains torréfiés sont maintenant enregistrés comme rangés dans les emplacements spécifiés
 - le **Rangement stock enreg.** est créé
 - la **Réceptions achat enregistrées** est créée
 - la commande achat a la **Quantité reçue** mise à jour pour les lignes reçues
 - le **Stock** d’articles est augmenté de la quantité choisie
    

## <a name="outbound-flow-picking-and-shipping-in-basic-warehouse-configurations"></a>Flux sortant : Prélèvement et expédition dans les configurations de stockage de base

Dans [!INCLUDE[prod_short](../../includes/prod_short.md)], les processus sortants de prélèvement et d’expédition peuvent être effectués de quatre manières, à l’aide de différentes fonctionnalités en fonction du niveau de complexité de l’entrepôt.  

|Méthode|Processus entrant|Emplacements|Prélèvements|Livraisons|Niveau de complexité (Voir [Détails de conception : paramètres entrepôt](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Validation du prélèvement et de l’expédition à partir de la ligne commande|X|||2|  
|B|Validation du prélèvement et de l’expédition à partir d’un document prélèvement stock||X||3|  
|C|Validation du prélèvement et de l’expédition à partir d’un document expédition entrepôt|||X|5/4/6|  
|J|Validation du prélèvement à partir d’un document prélèvement entrepôt et validation de l’expédition à partir d’un document expédition entrepôt||X|X|5/4/6|  

Pour plus d’informations, reportez\-vous à [Détails de conception : flux de désenlogement](../../design-details-outbound-warehouse-flow.md).  

La procédure pas à pas suivante illustre la méthode B dans la table précédente.

### <a name="scenario-1"></a>Scénario
Susan, préparatrice de commandes, crée une commande client pour divers grains torréfiés et la transmet à l’entrepôt. Jean, le magasinier, doit s’assurer que l’expédition est préparée et livrée au client. Jean gère toutes les tâches impliquées sur la page **Prélèvement stock**, qui indique automatiquement les endroits où les grains torréfiés sont stockés.

### <a name="steps-1"></a>Étapes
C’est une suite de [Flux entrant : Réception et rangement dans les configurations de stockage de base](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Configurez la page **Fiche magasin** pour définir les flux d’entrepôt entrants de la société.  

    1.  Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 5.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Magasins**, puis choisissez le lien associé.  
    2.  Ouvrez la fiche magasin *ARGENT*.  
    3.  Activez la case à cocher **Prélèvement requis**.  

2. Créez la commande client, qui est le type de document d’origine sortant le plus répandu.  

    1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 6.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
    2. Sélectionnez l’action **Nouveau**.  
    3. Créez une commande client pour le client 10000 avec la ligne de commande client suivante.  

    |Article ;|Code magasin|Quantité|  
    |----|-------------|--------|  
    |WRB-1000|ARGENT|20|  
    |WRB-1001|ARGENT|30|  

    Les codes emplacement sont renseignés automatiquement avec les emplacements par défaut.

    4. Choisissez l’action **Créer un rangement/prélèvement stock**.
    5. Activez la case à cocher **Créer prélèvement stock**.  
    6. Cliquez sur le bouton **OK**. Un nouveau prélèvement stock sera créé.

3. Prélever et expédier des articles

    1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 7.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Prélèvements stock**, puis choisissez le lien associé.  
    2. Sélectionnez le prélèvement stock pour les ventes au client 10000
    
    Le prélèvement stock créé a ignoré l’emplacement défini pour l’article *WRB-1000*, car il ne contient pas de stock et a utilisé un autre emplacement. Les deuxièmes lignes, avec l’article *WRB-1001* ont été automatiquement fractionnées pour être prélevées dans plusieurs emplacements.
    
4. Choisissez l’action **Remplir qté à traiter**.  

5. Choisissez l’action **Valider**, sélectionnez **Expédier**, puis cliquez sur le bouton **OK**.  

### <a name="results-1"></a>Résultats
 - les grains torréfiés sont maintenant enregistrés comme prélevés depuis des emplacements spécifiés
 - le **Prélèvement stock enreg.** est créé
 - l’**Expédition vente enregistrée** est créée
 - la commande client a la **Quantité expédiée** mise à jour pour les lignes expédiées
 - le **Stock** d’articles est réduit de la quantité choisie


## <a name="see-also"></a>Voir aussi
[Articles rangés avec rangements stock](../../warehouse-how-to-put-items-away-with-inventory-put-aways.md) 
[Configurer des entrepôts de base avec les zones d’opérations](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) 
[Détails de conception : flux d’enlogement](../../design-details-inbound-warehouse-flow.md) 
[Prélever des articles avec des prélèvements de stock](../../warehouse-how-to-pick-items-with-inventory-picks.md) 
[Détails de conception : flux de désenlogement](../../design-details-outbound-warehouse-flow.md) 
[Voir la disponibilité des articles](../../inventory-how-availability-overview.md) 
