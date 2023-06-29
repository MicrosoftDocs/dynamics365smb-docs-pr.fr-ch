---
title: Prélèvement et expédition dans les configurations d’entrepôt de base
description: Cet article décrit différents niveaux de complexité dans les processus de prélèvement et d’expédition.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Procédure pas à pas : Prélèvement et expédition dans les configurations de stockage de base

Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous prélevez et expédiez des articles en utilisant l’une des quatre méthodes décrites dans le tableau suivant.

|Méthode|Processus sortant|Prélèvement requis|Expédition requise|Niveau de complexité (pour plus d’informations, consultez [Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Validation du prélèvement et de l’expédition à partir de la ligne commande|||Aucune activité entrepôt dédiée.|  
|B|Validation du prélèvement et de l’expédition à partir d’un document prélèvement stock|Activé||De base : commande par commande.|  
|A|Validation du prélèvement et de l’expédition à partir d’un document expédition entrepôt||Activé|De base : envoi/réception regroupés pour plusieurs commandes.|  
|J|Validation du prélèvement à partir d’un document prélèvement entrepôt, et validation de l’expédition à partir d’un document expédition entrepôt|Activé|Activé|Avancé|  

Learn more at [Flux de désenlogement](design-details-outbound-warehouse-flow.md).

La procédure pas à pas suivante illustre la méthode B dans la table précédente.  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas

Pour les configurations de stockage de base, lorsqu’un magasin est défini pour exiger un traitement des prélèvements mais pas un traitement des expéditions, vous utilisez la page **Prélèvement stock** pour enregistrer et valider les informations de prélèvement et d’expédition pour vos documents origine sortants. Le document origine sortant peut être une commande vente, un retour achat, un désenlogement transfert ou un ordre de fabrication avec un besoin de composants.  

Cette procédure pas à pas présente les tâches suivantes :  

- Configuration du magasin SUD pour les prélèvements stock.  
- Créez une commande vent pour le client 10000 pour 30 lampes Amsterdam.  
- Lancement de la commande vente pour l’activité entrepôt.  
- Créez un prélèvement stock sur la base d’un document origine lancé.  
- Enregistrement d’un mouvement entrepôt de l’entrepôt et en même temps validation de l’expédition vente pour la commande vente d’origine.  

## <a name="roles"></a><a name="roles"></a>Rôles

Cette procédure pas à pas présente les tâches effectuées par les rôles utilisateur suivants :  

- Gestionnaire d’entrepôt  
- Préparateur de commandes  
- Magasinier  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a><a name="story"></a>Scénario

Ellen, la gestionnaire d’entrepôt de CRONUS, configure l’entrepôt SUD pour le prélèvement de base dans lequel les magasiniers traitent les commandes sortantes individuellement. Susan, préparatrice de commandes, crée une commande vente pour 30 unités de l’article 1928-S à livrer au client 10000 depuis l’entrepôt SUD. Jean, le magasinier, doit s’assurer que l’expédition est préparée et livrée au client. Jean gère toutes les tâches impliquées sur la page **Prélèvement stock**, qui indique automatiquement les endroits où 1928-S est stocké.

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a><a name="setting-up-the-bin-codes"></a>Configuration des codes emplacement

Une fois que vous avez configuré le magasin, vous devez ajouter deux emplacements.

#### <a name="to-setup-the-bin-codes"></a><a name="to-setup-the-bin-codes"></a>Pour configurer les codes emplacement

1. Sélectionnez l’action **Emplacements**.
2. Créez deux emplacements, avec les codes *S-01-0001* et *S-01-0002*.

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a><a name="making-yourself-a-warehouse-employee-at-location-south"></a>Ajout en tant que magasinier au magasin SUD

Pour utiliser cette fonctionnalité, vous devez vous ajouter au magasin en tant que magasinier. 

#### <a name="to-make-yourself-a-warehouse-employee"></a><a name="to-make-yourself-a-warehouse-employee"></a>Pour vous ajouter en tant que magasinier

  1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche pour la première fois.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Employés entrepôt**, puis sélectionnez le lien associé.  
  2. Choisissez le champ **ID utilisateur** et sélectionnez votre propre compte utilisateur sur la page **Magasiniers**.
  3. Dans le champ **Code magasin**, entrez SUD.  
  4. Sélectionnez le champ **Par défaut**, puis cliquez sur le bouton **Oui**.  

### <a name="making-item-1928-s-available"></a><a name="making-item-1928-s-available"></a>Rendre l’article 1928-S disponible

Pour rend l’article 1928-S disponible dans le magasin SUD, suivez cette procédure :  

  1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche pour la deuxième fois.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles article**, puis choisissez le lien associé.  
  2. Ouvrez la feuille par défaut, puis créez deux lignes feuille article avec les informations de date de travail suivantes (23 janvier).  

        |Type écriture|Numéro d’article|Code magasin|Code emplacement|Quantité|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Positif (ajust.)|1928-S|SUD|S-01-0001|20|  
        |Positif (ajust.)|1928-S|SUD|S-01-0002|20|  

        Par défaut, le champ **Code emplacement** des lignes vente est masqué, vous devez donc l’afficher. Pour cela, vous devez personnaliser la page. Pour plus d’informations, consultez [Commencer à personnaliser une page au moyen de la bannière Personnalisation](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

  3. Choisissez **Actions**, puis **Validation**, puis **Valider**.  
  4. Sélectionnez le bouton **Oui**.  

## <a name="creating-the-sales-order"></a><a name="creating-the-sales-order"></a>Création de la commande vente

Les commandes vente sont le type de document d’origine sortant le plus répandu.  

### <a name="to-create-the-sales-order"></a><a name="to-create-the-sales-order"></a>Pour créer la commande vente

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche pour la troisième fois.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Créez une commande vente pour le client 10000 à la date de travail (23 janvier) comportant la ligne commande vente suivante.  

    |Article ;|Code magasin|Quantité|  
    |----|-------------|--------|  
    |1928-S|SUD|30|  

     Informez l’entrepôt que la commande vente est prête pour l’activité entrepôt lorsque la livraison sera faire.  

4. Sélectionnez l’action **Lancer**.  

    Jean procède au prélèvement et à l’expédition des articles vendus.  

## <a name="picking-and-shipping-items"></a><a name="picking-and-shipping-items"></a>Prélèvement et expédition d’articles

Sur la page **Prélèvement stock**, vous pouvez gérer toutes les activités entrepôt sortantes pour un document d’origine spécifique, tel qu’une commande vente. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><a name="to-pick-and-ship-items"></a>Pour prélever et expédier des articles

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche pour la quatrième fois.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Prélèvements stock**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  

    Assurez-vous que le champ **N°** du raccourci **Général** est rempli.
3. Sélectionnez le champ **Document origine**, puis sélectionnez **Commande vente**.  
4. Sélectionnez le champ **N° origine**, sélectionnez la ligne correspondant à la vente au client 10000, puis cliquez sur le bouton **OK**.  

    Sinon, choisissez l’action **Extraire document origine**, puis sélectionnez la commande vente.  
5. Choisissez l’action **Remplir qté à traiter**.  

    Sinon, dans le champ **Qté à traiter**, saisissez respectivement 10 et 20 sur les deux lignes prélèvement stock.  
6. Choisissez l’action **Valider**, sélectionnez **Expédier**, puis cliquez sur le bouton **OK**.  

    Les 30 lampes Amsterdam sont à présent enregistrées comme prélevées depuis les emplacements S-01-0001 et S-01-0002, et une écriture comptable article négative est créée pour refléter l’expédition vente validée.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/paths/pick-ship-items-business-central/) associée

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Prélever des articles pour l’expédition entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Configurer des entrepôts de base avec les zones d’opérations](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Prélever pour la fabrication et l’assemblage](warehouse-how-to-pick-for-production.md)  
[Déplacer des articles ad hoc dans les configurations de stockage de base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Détails de conception : flux de désenlogement](design-details-outbound-warehouse-flow.md)  
[Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
