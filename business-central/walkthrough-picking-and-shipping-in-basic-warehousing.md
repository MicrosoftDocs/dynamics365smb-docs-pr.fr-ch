---
title: "Prélèvement et expédition dans les configurations de stockage de base | Microsoft Docs"
description: "Dans Business Central, les processus sortants de prélèvement et d'expédition peuvent être effectués de quatre manières, à l'aide de différentes fonctionnalités en fonction du niveau de complexité de l'entrepôt."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 35eaf9776508d608a48aaa38e6d83ae879cd05af
ms.contentlocale: fr-ch
ms.lasthandoff: 11/26/2018

---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Procédure pas à pas : Prélèvement et expédition dans les configurations de stockage de base
Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les processus sortants de prélèvement et d'expédition peuvent être effectués de quatre manières, à l'aide de différentes fonctionnalités en fonction du niveau de complexité de l'entrepôt.  

|Méthode|Processus entrant|Emplacements|Prélèvements|Livraisons|Niveau de complexité (Voir [Détails de conception : paramètres entrepôt](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Validation du prélèvement et de l'expédition à partir de la ligne commande|X|||2|  
|B|Validation du prélèvement et de l'expédition à partir d'un document prélèvement stock||X||3|  
|C|Validation du prélèvement et de l'expédition à partir d'un document expédition entrepôt|||X|5/4/6|  
|J|Validation du prélèvement à partir d'un document prélèvement entrepôt et validation de l'expédition à partir d'un document expédition entrepôt||X|X|5/4/6|  

Pour plus d'informations, reportez\-vous à [Détails de conception : flux de désenlogement](design-details-outbound-warehouse-flow.md).  

La procédure pas à pas suivante illustre la méthode B dans la table précédente.  

## <a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas  
Pour les configurations de stockage de base, lorsqu'un magasin est défini pour exiger un traitement des prélèvements mais pas un traitement des expéditions, vous utilisez la page **Prélèvement stock** pour enregistrer et valider les informations de prélèvement et d'expédition pour vos documents origine sortants. Le document origine sortant peut être une commande vente, un retour achat, un désenlogement transfert ou un ordre de fabrication avec un besoin de composants.  

Cette procédure pas à pas présente les tâches suivantes :  

-   Configuration du magasin ARGENT pour les prélèvements stock.  
-   Créez une commande vent pour le client 10000 pour 30 haut-parleurs.  
-   Lancement de la commande vente pour l'activité entrepôt.  
-   Créez un prélèvement stock sur la base d'un document origine lancé.  
-   Enregistrement d'un mouvement entrepôt de l'entrepôt et en même temps validation de l'expédition vente pour la commande vente d'origine.  

## <a name="roles"></a>Rôles  
Cette procédure pas à pas présente les tâches effectuées par les rôles utilisateur suivants :  

-   Gestionnaire d'entrepôt  
-   Préparateur de commandes  
-   Magasinier  

## <a name="prerequisites"></a>Conditions préalables  
Pour exécuter ce processus pas à pas, vous devez :  

-   avoir CRONUS International Ltd. installé.  
-   Pour devenir magasinier dans un magasin ARGENT, procédez comme suit :  

    1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Magasiniers**, puis choisissez le lien associé.  
    2.  Choisissez le champ **ID utilisateur** et sélectionnez votre propre compte utilisateur sur la page **Utilisateurs**.  
    3.  Dans le champ **Code magasin**, entrez ARGENT.  
    4.  Sélectionnez le champ **Par défaut**.  

-   Rend l'article LS-81 disponible dans le magasin ARGENT en suivant cette procédure :  

    1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles articles**, puis sélectionnez le lien associé.  
    2.  Ouvrez la feuille par défaut, puis créez deux lignes feuille article avec les informations de date de travail suivantes (23 janvier).  

        |Type écriture|Numéro d'article|Code magasin|Code emplacement|Quantité|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Positif (ajust.)|LS-81|ARGENTE|S-01-0001 **Remarque** : l'emplacement par défaut de l'article dans CRONUS|20|  
        |Positif (ajust.)|LS-81|ARGENTE|S-01-0002|20|  

    3.  Choisissez l'action **Valider**, puis cliquez sur le bouton **Oui**.  

## <a name="story"></a>Scénario  
Ellen, la gestionnaire d'entrepôt de CRONUS, configure l'entrepôt ARGENT pour le prélèvement de base dans lequel les magasiniers traitent les commandes sortantes individuellement. Susan, préparatrice de commandes, crée une commande vente pour 30 unités de l'article LS-81 à livrer au client 10000 depuis l'entrepôt ARGENT. Jean, le magasinier, doit s'assurer que l'expédition est préparée et livrée au client. Jean gère toutes les tâches impliquées sur la page **Prélèvement stock**, qui indique automatiquement les endroits où LS-81 est stocké.  

## <a name="setting-up-the-location"></a>Configuration du magasin  
La configuration de la page **Fiche magasin** définit les flux d'entrepôt de la société.  

### <a name="to-set-up-the-location"></a>Pour configurer le magasin  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Magasins**, puis choisissez le lien associé.  
2.  Ouvrez la fiche magasin ARGENT.  
3.  Activez la case à cocher **Prélèvement requis**.  

## <a name="creating-the-sales-order"></a>Création de la commande vente  
Les commandes vente sont le type de document d'origine sortant le plus répandu.  

### <a name="to-create-the-sales-order"></a>Pour créer la commande vente  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente**, puis sélectionnez le lien associé.  
2.  Sélectionnez l'action **Nouveau**.  
3.  Créez une commande vente pour le client 10000 à la date de travail (23 janvier) comportant la ligne commande vente suivante.  

    |Article ;|Code magasin|Quantité|  
    |----------|-------------------|--------------|  
    |LS_81|ARGENT|30|  

     Informez l'entrepôt que la commande vente est prête pour l'activité entrepôt lorsque la livraison sera faire.  

4.  Sélectionnez l'action **Lancer**.  

    Jean procède au prélèvement et à l'expédition des articles vendus.  

## <a name="picking-and-shipping-items"></a>Prélèvement et expédition d'articles  
Sur la page **Prélèvement stock**, vous pouvez gérer toutes les activités entrepôt sortantes pour un document d'origine spécifique, tel qu'une commande vente.  

### <a name="to-pick-and-ship-items"></a>Pour prélever et expédier des articles  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Prélèvements stock**, puis sélectionnez le lien associé.  
2.  Sélectionnez l'action **Nouveau**.  
3.  Sélectionnez le champ **Document origine**, puis sélectionnez **Commande vente**.  
4.  Sélectionnez le champ **N° origine**, sélectionnez la ligne correspondant à la vente au client 10000, puis cliquez sur le bouton **OK**.  

    Sinon, choisissez l'action **Extraire document origine**, puis sélectionnez la commande vente.  
5.  Choisissez l'action **Remplir qté à traiter**.  

    Sinon, dans le champ **Qté à traiter**, saisissez respectivement 10 et 30 sur les deux lignes prélèvement stock.  
6.  Choisissez l'action **Valider**, sélectionnez **Expédier**, puis cliquez sur le bouton **OK**.  

    Les 30 haut-parleurs sont à présent enregistrés comme prélevés depuis les emplacements S-01-0001 et S-01-0002, et une écriture comptable article négative est créée pour refléter l'expédition vente validée.  

## <a name="see-also"></a>Voir aussi  
 [Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md)   
 [Prélever des articles pour l'expédition entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Configurer des entrepôts de base avec les zones d'opérations](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Déplacer les composants vers une zone opérations dans les configurations de stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Prélever pour la fabrication et l'assemblage](warehouse-how-to-pick-for-production.md)   
 [Déplacer des articles ad hoc dans les configurations de stockage de base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Détails de conception : flux de désenlogement](design-details-outbound-warehouse-flow.md)   
 [Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

