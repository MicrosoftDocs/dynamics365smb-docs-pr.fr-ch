---
title: 'Procédure pas à pas : Réception et rangement dans les configurations de stockage de base'
description: Dans Business Central, les processus entrants de réception et de rangement peuvent être effectués de quatre manières, à l’aide de différentes fonctionnalités en fonction du niveau de complexité de l’entrepôt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c79891af3fbf85b78439cd66d02eafb6ff82c6ca
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772019"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Procédure pas à pas : Réception et rangement dans les configurations de stockage de base

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

Dans [!INCLUDE[prod_short](includes/prod_short.md)], les processus entrants de réception et de rangement peuvent être effectués de quatre manières, à l’aide de différentes fonctionnalités en fonction du niveau de complexité de l’entrepôt.  

|Méthode|Processus entrant|Emplacements|Bons de réception|Rangements|Niveau de complexité (Voir [Détails de conception : paramètres entrepôt](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Validation de la réception et du rangement à partir de la ligne commande|X|||2|  
|B|Validation de la réception et du rangement à partir d’un document de rangement stock|||X|3|  
|C|Validation de la réception et du rangement à partir d’un document réception entrepôt||X||5/4/6|  
|J|Validation de la réception d’un document réception entrepôt et validation du rangement à partir d’un document de rangement entrepôt||X|X|5/4/6|  

Pour plus d’informations, reportez\-vous à [Détails de conception : flux d’enlogement](design-details-inbound-warehouse-flow.md).  

La procédure pas à pas suivante illustre la méthode B dans la table précédente.  

## <a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas  
Pour les configurations de stockage de base, lorsqu’un magasin est défini pour exiger un traitement des rangements mais pas un traitement des réceptions, vous utilisez la page **Rangement stock** pour enregistrer et valider les informations de rangement et de réception pour vos documents origine entrants. Le document origine entrant peut être une commande achat, un retour vente, un enlogement transfert ou un ordre de fabrication dont la production est prête à être rangée.

> [!NOTE]
> Bien que les paramètres soient appelés **Prélèvement requis** et **Rangement requis**, vous pouvez quand même valider les réceptions et les expéditions directement à partir des documents commerciaux origine dans les magasins où vous cochez ces cases.  

Cette procédure pas à pas présente les tâches suivantes.  

-   Configuration du magasin ARGENT pour le rangement stock.  
-   Configuration du magasin ARGENT pour la gestion d’emplacement.  
-   Définissez un emplacement par défaut pour l’article LS-81. (LS-75 est déjà défini dans CRONUS).  
-   Créez une commande achat pour le fournisseur 10000 pour 40 haut-parleurs.  
-   Vérifier que les emplacements de rangement sont prédéfinis par la configuration.  
-   Lancement de la commande achat pour l’activité entrepôt.  
-   Créez un rangement stock sur la base d’un document origine lancé.  
-   Vérifier que les emplacements de rangement sont hérités de la commande achat.  
-   Enregistrement d’un mouvement entrepôt dans l’entrepôt et en même temps validation de la réception achat pour la commande achat d’origine.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a>Rôles  
Cette procédure pas à pas présente les tâches effectuées par les rôles utilisateur suivants :  

-   Gestionnaire d’entrepôt  
-   Agent d’achats  
-   Magasinier  

## <a name="prerequisites"></a>Conditions préalables  
Pour exécuter ce processus pas à pas, vous devez :  

-   avoir CRONUS International Ltd. installé.  
-   Pour devenir magasinier dans un magasin ARGENT, procédez comme suit :  

    1.  Choisissez l’icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Magasiniers**, puis sélectionnez le lien associé.  
    2.  Choisissez le champ **ID utilisateur** et sélectionnez votre propre compte utilisateur sur la page **Utilisateurs**.  
    3.  Dans le champ **Code magasin**, entrez ARGENT.  
    4.  Sélectionnez le champ **Par défaut**.  

## <a name="story"></a>Scénario  
Ellen, responsable d’entrepôt chez CRONUS International Ltd., crée une commande achat de 10 unités de l’article LS-75 et 30 unités de l’article LS-81 du fournisseur 10000, qui doit être approvisionnée à l’entrepôt ARGENT. Lorsque la livraison arrive à l’entrepôt, Jean, le magasinier, range les articles dans des emplacements par défaut définis pour les articles. Lorsque Jean valide le rangement, les articles sont validés comme étant reçus dans le stock et disponibles à la vente ou pour d’autres demandes.  

## <a name="setting-up-the-location"></a>Configuration du magasin  
 La configuration de la page **Fiche magasin** définit les flux d’entrepôt de la société.  

### <a name="to-set-up-the-location"></a>Pour configurer le magasin  

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Magasins**, puis sélectionnez le lien associé.  
2.  Ouvrez la fiche magasin ARGENT.  
3.  Activez la case à cocher **Rangement requis**.  

    Configurez un emplacement par défaut pour les deux numéros d’article pour contrôler l’endroit où ils sont rangés.  

4.  Choisissez l’action **Emplacements**.  
5.  Sélectionnez la première ligne, pour l’emplacement S-01-0001, puis choisissez l’action **Contenu**.  

    Remarquez sur la page **Contenu emplacement** que l’article LS-75 est déjà défini comme contenu dans l’emplacement S-01-0001.  

6.  Sélectionnez l’action **Nouveau**.  
7.  Sélectionnez les champs **Fixe** et **Par défaut**.  
8.  Dans le champ **N° article**, saisissez LS-81.  

## <a name="creating-the-purchase-order"></a>Création des commandes achat  
Les commandes achat sont le type de document d’origine entrant le plus répandu.  

### <a name="to-create-the-purchase-order"></a>Pour créer la commande achat  

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes achat**, puis sélectionnez le lien associé.  
2.  Sélectionnez l’action **Nouveau**.  
3.  Créez une commande achat pour le fournisseur 10000 à la date de travail (23 janvier) comportant les lignes commande achat suivantes.  

    |Article ;|Code magasin|Code emplacement|Quantité|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|ARGENT|S-01-0001|10|  
    |LS-81|ARGENT|S-01-0001|30|  

    > [!NOTE]  
    >  Le code emplacement est renseigné automatiquement en fonction de la configuration de la section « Configuration du magasin ».  

    Informez l’entrepôt que la commande achat est prête pour l’activité entrepôt lorsque la livraison sera faire.  

4.  Sélectionnez l’action **Lancer**.  

    La livraison des haut-parleurs provenant du fournisseur 10000 est arrivée dans l’entrepôt ARGENT. Jean procède à leur rangement.  

## <a name="receiving-and-putting-the-items-away"></a>Réception et rangement des articles  
Sur la page **Rangement stock**, vous pouvez gérer toutes les activités entrepôt entrantes pour un document d’origine spécifique, tel qu’une commande achat.  

### <a name="to-receive-and-put-the-items-away"></a>Pour recevoir et ranger des articles  

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Rangements stock**, puis sélectionnez le lien associé.  
2.  Sélectionnez l’action **Nouveau**.  
3.  Sélectionnez le champ **Document origine**, puis sélectionnez **Commande achat**.  
4.  Sélectionnez le champ **N° origine**, sélectionnez la ligne correspondant à l’achat au fournisseur 10000, puis cliquez sur le bouton **OK**.  

    Sinon, choisissez l’action **Extraire document origine**, puis sélectionnez la commande achat.  

5.  Choisissez l’action **Remplir qté à traiter**.  

    Sinon, dans le champ **Qté à traiter**, saisissez respectivement 10 et 30 sur les deux lignes rangement stock.  

6.  Cliquez sur **Valider**, choisissez l’action **Réceptionner**, puis choisissez le bouton **OK**.  

    Les 40 haut-parleurs sont à présent enregistrés comme rangés dans l’emplacement S-01-0001, et une écriture comptable article positive est créée pour refléter la réception achat validée.  

## <a name="see-also"></a>Voir aussi  
 [Ranger des articles avec le rangement stock](warehouse-how-to-put-items-away-with-inventory-put-aways.md)   
 [Configurer des entrepôts de base avec les zones d’opérations](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Déplacer les composants vers une zone opérations dans les configurations de stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Prélever pour la fabrication et l’assemblage](warehouse-how-to-pick-for-production.md)   
 [Déplacer des articles ad hoc dans les configurations de stockage de base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Détails de conception : flux d’enlogement](design-details-inbound-warehouse-flow.md)   
 [Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)  
 [Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]