---
title: "Procédure pas à pas\_: planification manuelle des approvisionnements"
description: 'Cette procédure pas à pas montre le processus de planification des commandes d’approvisionnement pour répondre à une nouvelle demande, notamment la planification d’un achat, d’un transfert et d’un ordre de fabrication.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-planning-supplies-manually"></a><a name="walkthrough-planning-supplies-manually"></a><a name="walkthrough-planning-supplies-manually"></a>Procédure pas à pas : planification manuelle des approvisionnements

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Cette procédure pas à pas présente le processus de planification des commandes approvisionnement en vue de répondre à la nouvelle demande. Vous pouvez lancer la planification des approvisionnements à des intervalles fixes, par exemple, tous les matins ou tous les lundis, ou lorsque vous recevez une notification du département Ventes ou Production, en fonction du type de demande. Au cours de cette procédure, vous utiliserez la page **Planning commande**, un outil simplifié de planification des approvisionnements basé sur la prise de décision manuelle plutôt que la planification automatique basée sur des paramètres.  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas
 Cette procédure pas à pas présente les tâches suivantes :  

-   planification d’une commande achat pour les composants de production ;  
-   planification d’un ordre de transfert afin de répondre à la demande de vente ;  
-   planification d’un ordre de fabrication pour un article multi-niveaux.  

## <a name="roles"></a><a name="roles"></a><a name="roles"></a>Rôles
 Cette procédure pas à pas présente les tâches effectuées par les rôles utilisateur suivants :  

-   Gestionnaire de production  
-   Agent d’achats  
-   préparateur de commandes vente ;  

## <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Conditions préalables
 Avant de commencer cette procédure pas à pas, vous devez installer la [!INCLUDE[prod_short](includes/prod_short.md)]. Les modifications suivantes doivent être apportées à la base de données :  

-   Supprimez toute commande vente existante de bicyclettes.  
-   Créez une commande vente pour 10 bicyclettes pour le magasin EAST.  
-   Supprimez tous les ordres de fabrication planifiés et planifiés fermes. Ne supprimez pas les ordres démarrés dont les écritures ont déjà été validées.  

 En règle générale, utilisez les données suggérées dans cette procédure pas à pas car elles incluent les enregistrements nécessaires.  

## <a name="story"></a><a name="story"></a><a name="story"></a>Scénario
 Eduardo, Gestionnaire de production dans une petite société manufacturière, est sur le point de planifier les ordres de fabrication et commandes achat en réponse à la demande de vente.  

 Dans la mesure où les produits disposent de peu de niveaux de nomenclature et où le flux de commandes est relativement faible, Eduardo utilise la page **Planification commande** pour créer manuellement les commandes approvisionnement (un niveau de produit à la fois).  

 Dans un environnement de fabrication plus complexe, la feuille planning permet de planifier l’approvisionnement sur la base des paramètres d’article, tels que la période de replanification, le délai de sécurité, le point de commande et les calculs par lots de la demande consolidée à partir de tous les niveaux de produit.  

## <a name="setting-up-the-sample-data"></a><a name="setting-up-the-sample-data"></a><a name="setting-up-the-sample-data"></a>Configuration des exemples de données
 La société de démonstration CRONUS standard dispose actuellement d’un grand nombre de demandes non planifiées. Au cours des différentes tâches de planification de cette procédure pas à pas, vous devrez passer outre le flux commercial réaliste : utilisez la demande dont les dates d’échéance sont ultérieures plutôt que celle dont les dates sont échues.  

## <a name="use-the-order-planning-page"></a><a name="use-the-order-planning-page"></a><a name="use-the-order-planning-page"></a>Utiliser la page Planification commande

La page **Planification commande** est accessible de plusieurs endroits différents :  

-   Production, Planning  
-   Ventes et marketing, Traitement des commandes  
-   Achat, Planning  
-   En outre, vous pouvez ouvrir cette page pour un ordre de fabrication spécifique en choisissant l’action **Planning**.

### <a name="to-use-the-order-planning-page"></a><a name="to-use-the-order-planning-page"></a><a name="to-use-the-order-planning-page"></a>Pour utiliser la page Planification commande :

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Planification commande**, puis choisissez le lien associé.  

     À la première ouverture de la page **Planning commande**, une planification doit être calculée pour afficher la nouvelle demande depuis le dernier calcul.  

2.  Choisissez l’action **Calculer planning**.  

     Le système de planification analyse chaque nouvelle demande, telle qu’une nouvelle vente, des modifications de ventes ou des ordres de fabrication.  

     Selon la disponibilité globale, la quantité nécessaire pour chaque ligne commande est calculée. Ce calcul est effectué commande par commande. Cela signifie que la commande dont la ligne demande a la date d’échéance ou la date d’expédition la plus proche sera calculée en premier. Les autres lignes demande seront ensuite calculées dans le même ordre, quelle que soit la date d’échéance ou la date d’expédition.  

3.  Assurez-vous d’agrandir au maximum la page **Planification commande** et de redimensionner les champs des colonnes pour afficher tous les noms de champ par défaut.  

     À la fin du calcul, la page affiche toutes les demandes insatisfaites sous la forme de lignes en-tête commande réduites triées par date de demande la plus proche.  

     Notez que CRONUS inclut plusieurs commandes dont la demande est insatisfaite. Chaque ligne planning en gras représente une commande, une commande vente ou un ordre de fabrication, comprenant au moins une ligne commande avec une disponibilité insuffisante.  

4.  Dans le champ **Afficher la demande en tant que**, sélectionnez le filtre **Toutes les demandes**.  

     Dans le champ **Type de demande**, vous pouvez sélectionner les types de commande à afficher.  

     Les commandes sans problème de disponibilité ne s’affichent pas. Si aucune commande n’existe lors du calcul d’une planification, un message s’affiche et aucune ligne planning n’apparaît.  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><a name="planning-a-purchase-order-to-fulfill-component-demand"></a><a name="planning-a-purchase-order-to-fulfill-component-demand"></a>Planification d’une commande achat pour répondre à une demande de composant
 Dans cette procédure, vous créez une commande achat pour les composants nécessaires à la fabrication.  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a>Pour planifier une commande achat en vue de répondre aux besoins de composants en production :

1.  Développez la première ligne en cliquant sur le symbole +.  
2.  Sélectionnez la première ligne demande, avec l’article **LSU-15**, puis sélectionnez l’action **Afficher document**.  
3.  Fermez l’ordre de fabrication ouvert pour revenir à la page **Planning commande**.  
4.  Dans le champ **Système réappro.**, sélectionnez **Achats**.  

     La valeur par défaut est celle indiquée sur la fiche article (ou la fiche point de stock), mais vous pouvez la modifier et lui attribuer l’une des options suivantes :  

    -   **Achat** : pour créer une commande achat.  
    -   **Transfert** : pour créer un ordre de transfert.  
    -   **O.F** : pour créer un ordre de fabrication.  

5.  Dans le champ **Origine approvisionnement**, sélectionnez l’une des options suivantes en fonction du système de réapprovisionnement sélectionné :  

    -   **Fournisseur** – Pour les achats  
    -   **Magasin** – Pour les transferts  

     Si le champ n’est pas renseigné, un message d’erreur s’affiche lorsque vous tentez de créer les commandes approvisionnement.  

    > [!NOTE]  
    >  Si un numéro fournisseur par défaut pour les composants est configuré sur les fiches article, les lignes sont prédéfinies.  

6.  Sélectionnez le champ **Origine approvisionnement**.  
7.  Sur la page **Catalogue fournisseur articles**, choisissez l’action **Nouveau**, puis sélectionnez le fournisseur **30000**.  
8.  Cliquez sur le bouton **OK** pour revenir à la page **Planning commande**.  
9. Copiez le fournisseur **30000** vers les autres lignes pour les composants « haut-parleurs » correspondant à cet ordre de fabrication.  

     Vous êtes maintenant prêt à créer une commande achat.  

10. Sélectionnez l’action **Créer commandes**. La page **Créer des commandes approvisionnement** s’ouvre.  
11. Sur le raccourci **Planning commande**, dans le champ **Créer commandes pour**, sélectionnez l’option **Commande active**.  
12. Sur le raccourci **Options**, dans le champ **Créer commande achat**, sélectionnez l’option **Créer cdes achat**.  
13. Cliquez sur le bouton **OK** pour créer les commandes achat pour tous les composants de la commande.  

     Les commandes achat sont à présent créées et enregistrées en tant que dernières commandes dans la liste des commandes achat.  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><a name="planning-a-transfer-order-to-fulfill-sales-demand"></a>Planification d’un ordre de transfert pour répondre à une demande de vente
 Dans cette procédure, vous planifiez une demande à partir d’une commande vente. Les lignes demande représentent les lignes vente (et non les lignes composant, comme c’est le cas pour les demandes de production).  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a>Pour planifier un ordre de transfert afin de répondre à la demande de vente :

1.  Déplacez le pointeur vers la ligne planning correspondant à la commande **2008**.  
2.  Développez la ligne et déplacez le pointeur vers la ligne demande.  

     La commande vente **2008** correspond à dix haut-parleurs, article **LS-120**, commandés par la société John Haddock Insurance Co.  

     Le système de réapprovisionnement et le fournisseur par défaut de l’article s’affichent.  

    > [!NOTE]  
    >  Au bas de la page, quatre champs d’informations s’affichent. Dans le champ **Date dispo. au plus tôt**, les dix pièces nécessaires sont disponibles sur une commande approvisionnement entrante, neuf jours après la date d’échéance actuelle. Si cette date est trop tardive pour le client, le champ **Disponible pour transfert** affiche 13 pièces de l’article provenant d’un autre magasin. Vous devez planifier ce stock.  

3.  Choisissez le champ **Disponible pour transfert** pour ouvrir la page **Obtenir un approvisionnement secondaire**.  
4.  Cliquez sur le bouton **OK** pour réserver les dix articles disponibles.  

    > [!NOTE]  
    >  Dans la ligne demande, l’achat proposé a été remplacé par un transfert à partir du magasin PRINCIPAL. La fonction **Créer commandes** crée un ordre de transfert du magasin PRINCIPAL vers le magasin demandé. Le champ **Articles de substitution** fonctionne de la même manière.  

5.  Sélectionnez l’action **Créer commandes**. La page **Créer des commandes approvisionnement** s’ouvre.  
6.  Sur le raccourci **Planning commande** dans le champ **Créer commandes pour**, sélectionnez l’option **La commande active**.  
7.  Sur le raccourci **Options**, dans le champ **Créer un ordre de transfert**, sélectionnez l’option **Créer ordres transfert**.  
8.  Cliquez sur le bouton **OK** pour créer l’ordre de transfert visant à approvisionner la commande vente.  

     L’ordre de transfert est à présent créé et enregistré en tant que dernier ordre dans la liste des ordres de transfert en cours.  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a>Planification d’un ordre de production multi-niveaux pour répondre à une demande de vente
 Dans cette procédure, vous effectuez une planification en vue de satisfaire la demande de vente pour un article produit avec plusieurs niveaux de produit, chacun d’entre eux créant une demande de production dépendante.  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a>Pour planifier une production multi-niveaux afin de répondre à la demande de vente :

1.  Sélectionnez la ligne planning avec une demande de vente pour la commande **1001**, créée plus tôt comme données préalables.  

     Cette demande est une ligne vente, mais l’article a un système de réapprovisionnement défini sur **O. F.**. Ajoutez ensuite une sonnette supplémentaire au besoin composant de chaque bicyclette.  

2.  Choisissez l’action **Composants** pour ouvrir la page **Composants planning**.  
3.  Sur la ligne correspondant à l’article Sonnerie, remplacez la valeur **1** du champ **Quantité par** par **2**.  
4.  Sur la page **Planification commande**, étudiez les différentes possibilités de planification. Dans ce cas, vous ne disposez pas d’autres moyens d’approvisionnement, ni d’aucun transfert, remplacement ou livraison en retard. Vous devez créer la commande approvisionnement suggérée, à savoir un ordre de fabrication.  
5.  Choisissez l’action **Créer commandes** pour créer l’ordre de fabrication.  

     Sur la page **Planification commande**, vous remarquez que la ligne planning correspondant à la commande vente **1001** n’existe plus et que la demande de vente initiale a été couverte.  

6.  Fermez la page **Planification commande**.  

     Vous pourriez à présent conserver cet affichage et exécuter toutes les tâches de planification. Au lieu de cela, vous devez prendre le rôle Gestionnaire de production en accédant à l’ordre de fabrication que vous venez de créer, puis à la page **Planification commande**.  

 En tant que gestionnaire de production, vous devez maintenant planifier un ordre de fabrication spécifique.  

### <a name="to-plan-a-specific-production-order"></a><a name="to-plan-a-specific-production-order"></a><a name="to-plan-a-specific-production-order"></a>Pour planifier un ordre de fabrication spécifique :

1.  Ouvrez l’ordre de fabrication **101001** pour dix bicyclettes, créé à l’aide de la fonction **Créer commandes**.  
2.  Ouvrez la page **Composants O.F.** pour vérifier que la sonnette supplémentaire figure dans l’ordre de fabrication.  
3.  Sélectionnez l’action **Planification**.  

     La page **Planning commande** s’ouvre dans une vue qui est toujours filtrée en fonction de la demande de production spécifique. La demande de vente ne s’affiche pas. Vous devez calculer une planification avant de pouvoir visualiser les demandes supplémentaires.  

4.  Choisissez l’action **Calculer planning**.  

     Remarque : quatre nouveaux ordres de fabrication s’affichent en tant que demande de production non planifiée issue de la commande **101001**. Les nouvelles lignes représentent la nouvelle demande de production de produits semi-finis que vous devez créer pour produire la commande.  

5.  Choisissez l’action **Développer tout** pour obtenir un aperçu de la demande de production correspondant aux ordres de fabrication.  

     Pour indiquer des informations supplémentaires sur les lignes demande, vous pouvez ajouter les champs **Quantité demandée** et **Qté demande disponible** à votre affichage.  

     Vous devez à présent approvisionner dix unités de chaque composant.  

     Notez que quatre des lignes demande ont pour système de réapprovisionnement O. F. Ces quatre produits semi-finis représentent le deuxième niveau de produit de la bicyclette.  

     Les paramètres de réapprovisionnement par défaut étant déjà renseignés, vous pouvez créer les commandes.  

6.  Sélectionnez l’action **Créer commandes**.  

     Avant de cliquer sur le bouton **OK**, observez attentivement le texte sous le raccourci **Planning commande**. Ce texte est important, car il vous permet de savoir que la bicyclette possède plusieurs composants produits (ou produits semi-finis) dans sa structure produit qui peuvent être demandés lorsque vous créez cet ordre de fabrication.  

7.  Sur la page **Créer des commandes approvisionnement**, dans le champ **Créer commandes pour**, sélectionnez l’option **Toutes les lignes**, puis cliquez sur le bouton **OK** pour créer des ordres de fabrication pour le deuxième niveau de produit de la commande.  

     Remarquez que la demande de production de niveau supérieur pour l’ordre de fabrication 101001 n’existe plus. Cela signifie que la demande de production initiale des produits semi-finis a été planifiée.  

     Sur la page **Planification commande**, recalculez une planification pour planifier la structure de la bicyclette.  

8.  Choisissez l’action **Calculer planning** pour recalculer le planning selon les instructions du texte d’aide incorporé.  

     Les deux nouvelles lignes représentent la demande de production supplémentaire issue des produits semi-finis planifiés au cours de l’étape précédente. Il est recommandé de créer deux ordres de fabrication pour approvisionner les moyeux des roues, à savoir un ordre pour les 10 moyeux avant et un autre pour les 10 moyeux arrière.  

9. Choisissez l’action **Développer tout** pour obtenir un aperçu de la demande correspondant aux deux ordres de fabrication.  

     Le programme d’approvisionnement proposé indique que quatre commandes achat seront créées pour les composants. Vous décidez de créer les commandes suggérées.  

10. Sélectionnez l’action **Créer commandes**.  
11. Dans le champ **Créer commandes pour**, sélectionnez l’option **Toutes les lignes**, puis cliquez sur le bouton **OK**. Vérifiez s’il existe une demande supplémentaire pour la production de l’article parent, la bicyclette, qui est vendue dans le cadre de la commande vente 1001.  
12. Choisissez l’action **Calculer planning**.  

     Le message indique que tous les articles requis sont à présent approvisionnés. Vérifiez les ordres de fabrication planifiés fermes qui ont été créés.  

13. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. planifiés fermes**, puis sélectionnez le lien associé.  

     Sur la page **O. F. planifiés fermes**, passez en revue la planification des heures de début et de fin de chaque commande par rapport à la structure produit. Les composants de niveau inférieur sont produits en premier. Par conséquent, vous devez planifier des commandes multi-niveaux conformément aux instructions de ce flux de planification.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi
 [Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)   
<!--  [Walkthrough: Planning Supplies Automatically](walkthrough-planning-supplies-automatically.md) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
