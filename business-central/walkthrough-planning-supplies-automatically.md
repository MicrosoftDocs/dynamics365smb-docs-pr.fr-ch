---
title: "Procédure pas à pas\_: planification automatique des approvisionnements"
description: Cette procédure pas à pas démontre comment utiliser le système de planification de l’approvisionnement pour planifier automatiquement tous les ordres de fabrication et toutes les commandes achat figurant sur différentes commandes vente.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-planning-supplies-automatically"></a><a name="walkthrough-planning-supplies-automatically"></a>Procédure pas à pas : planification automatique des approvisionnements

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Les expressions comme « exécution du planning » et « exécution MRP » se rapportent au calcul du programme directeur de production (PDP) et de la planification des besoins de matières (MRP) en fonction de la demande réelle et projetée.  

-   Le calcul PDP est le calcul de la planification de production principale basé sur la demande réelle et la prévision de la demande. Le calcul PDP est utilisé pour les articles finis disposant de prévisions ou d’une ligne commande vente. Ces articles sont appelés « articles PDP » et identifiés de façon dynamique au début du calcul.  
-   Le calcul MRP est le calcul des besoins matière basé sur la demande réelle de composants et la prévision de la demande au niveau du composant. Le calcul MRP n’est effectué que pour les articles qui ne sont pas des articles PDP. Le but global du calcul MRP est de générer des plans formels en phases, par article, afin de fournir le bon article au bon moment, au bon endroit et dans la bonne quantité.  

 Les algorithmes de planification utilisés pour les calculs PDP et MRP sont identiques. Ils utilisent la présentation au net, la réutilisation des commandes approvisionnement existantes et les messages d’action. Le processus du système de planification examine ce qui est ou sera nécessaire (demande) et ce qui est disponible ou attendu (approvisionnement). Lorsque ces quantités sont déduites l’une de l’autre, des messages d’action s’affichent dans la feuille planning. Ces messages proposent de créer une commande approvisionnement, d’en modifier une (quantité ou date) ou encore d’annuler une commande approvisionnement existante. Les commandes approvisionnement peuvent être des ordres de fabrication, des commandes achat et des ordres de transfert. Pour plus d’informations, voir [Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md).  

 Le résultat de la planification est obtenu en partie grâce aux ensembles d’offre et de demande de la base de données et en partie grâce au paramétrage des fiches point de stock ou des fiches article, des nomenclatures de production et des gammes.  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas
 Cette procédure pas à pas démontre comment utiliser le système de planification de l’approvisionnement pour planifier automatiquement tous les ordres de fabrication et toutes les commandes achat nécessaires à la production de 15 vélos cyclotourisme figurant sur différentes commandes vente. Pour que cette procédure soit claire et réaliste, le nombre de lignes planning a été délimité en filtrant tous les autres ensembles d’offre et de demande de la société fictive CRONUS, à l’exception de la demande de vente pour le magasin EAST.  

 Cette procédure pas à pas présente les tâches suivantes :  

-   création de la commande vente et calcul d’un programme d’approvisionnement complet ;  
-   affichage des paramètres de planification et des écritures chaînage à l’origine des lignes planning ;  
-   création automatique des commandes approvisionnement proposées ;  
-   création de demandes de vente et replanification en conséquence.  

## <a name="roles"></a><a name="roles"></a>Rôles

-   Gestionnaire de production  
-   Agent d’achats  

## <a name="prerequisites"></a><a name="prerequisites"></a>Conditions préalables
 Pour exécuter ce processus pas à pas, vous devez :  

-   utiliser la société fictive CRONUS International Ltd. ;  
-   Modifier plusieurs valeurs de paramétrage des articles en suivant les instructions de la section « Préparation d’exemples de données », dans la suite de cette procédure.  

## <a name="story"></a><a name="story"></a>Scénario
 Le client, Cannon Group PLC, commande cinq vélos cyclotourisme pour une expédition le 05/02/2021 (5 février).  

 Eduardo, Gestionnaire de production, procède à la planification de l’approvisionnement courante pour la première semaine de février 2021. Eduardo filtre sur son propre magasin, EAST, et entre un intervalle de planification de la date de travail du 23/01/2021 au 07/02/2021 avant qu’il ne calcule un programme d’approvisionnement initial.  

 La seule demande cette semaine concerne la commande vente de Cannon Group. Eduardo constate qu’aucune ligne planning ne comporte d’avertissement et il crée des commandes approvisionnement sans modifications pour les lignes planning proposées.  

 Le lendemain, avant que les commandes approvisionnement initiales ne soient démarrées ou comptabilisées, Eduardo est averti qu’un autre client a commandé dix vélos cyclotourisme pour une expédition le 12/02/2021. Eduardo adapte son calcul du programme d’approvisionnement en fonction de la modification de la demande. Ce nouveau calcul aboutit à une planification par écart proposant des changements de temps et de quantités de certaines commandes approvisionnement créées dans un premier temps.  

 Au cours des diverses étapes de la planification, Eduardo recherche les commandes concernées et utilise la fonction Chaînage pour voir quelle demande est couverte par quel approvisionnement.  

## <a name="preparing-sample-data"></a><a name="preparing-sample-data"></a>Préparation d’exemples de données
 Créez des points de stock pour chaque vélo cyclotourisme et une sélection de ses composants, dont les numéros d’article vont de 1001 à 1300. (Certains composants sont exclus pour simplifier les procédures.) Ajustez les paramètres de planification des composants sélectionnés pour présenter un résultat plus transparent.  

### <a name="to-create-stockkeeping-units"></a><a name="to-create-stockkeeping-units"></a>Pour créer des points de stock

1.  Ouvrez la fiche article pour l’article 1001, vélo cyclotourisme.  
2.  Choisissez l’action **Créer point de stock**.  
3.  Sur la page **Créer point de stock**, ne modifiez aucune option ni aucun filtre, puis cliquez sur le bouton **OK**.  
4.  Répétez les étapes 1 à 3 pour chaque article dont le numéro est compris entre 1100 et 1300.  

### <a name="to-change-selected-planning-parameters"></a><a name="to-change-selected-planning-parameters"></a>Pour modifier des paramètres de planification sélectionnés

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Centres de stock**, puis choisissez le lien associé.  
2.  Ouvrez la fiche point de stock EAST de l’article 1100, Roue avant.  
3.  Sur le raccourci **Planifié** renseignez les champs comme indiqué dans le tableau ci-dessous.  

    |Méthode réapprovisionnement|Stock de sécurité|Période de groupement de lots|Période de replanification|  
    |-------------------------------------------|-----------------------------------------------|-------------------------------------------------|---------------------------------------------|  
    |Lot pour lot|Vide|2S|2S|  

4.  Répétez les étapes 2 et 3 pour chaque point de stock dont le numéro est compris entre 1100 et 1300.  

 Vous venez de préparer les données d’exemple de la procédure pas à pas.  

## <a name="creating-a-regenerative-supply-plan"></a><a name="creating-a-regenerative-supply-plan"></a>Création d’un programme d’approvisionnement régénératif
 En réaction à une commande vente pour cinq vélos, Ricardo démarre le processus de planification en définissant les options, filtres et intervalles de planification afin d’exclure toutes les autres demandes sauf celle de la première semaine de février du magasin EAST. Ricardo commence par calculer un programme directeur de production (PDP), puis un programme d’approvisionnement complet pour toute demande de niveau inférieur (MRP).  

### <a name="to-create-the-sales-order"></a><a name="to-create-the-sales-order"></a>Pour créer la commande vente

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2.  Sélectionnez l’action **Nouveau**.  
3.  Sur la page **Commande vente**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Nom donneur d’ordre|Date de préparation|Nombre d’articles|Magasin|Quantité|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Cannon Group.|05/02/2014|1 001|EAST|5|  

4.  Acceptez l’avertissement de disponibilité et choisissez le bouton **Oui** pour enregistrer la nouvelle quantité demandée.  

### <a name="to-create-a-regenerative-plan-to-fulfill-demand-at-location-east"></a><a name="to-create-a-regenerative-plan-to-fulfill-demand-at-location-east"></a>Pour créer un planning régénératif afin de répondre à la demande du magasin EAST

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille planning**, puis choisissez le lien associé.  
2.  Choisissez l’action **Calculer planning régénératif**.  
3.  Sur la page **Calc. planning - F. planning**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Calculer planning|Date début|Date de fin|Afficher résultats :|Limiter les totaux à|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**PDP** = Oui<br /><br /> **MRP** = Non|01/23/2021<br /><br /> (date de travail)|02/07/2021|1001..1300|Filtre magasin = EAST|  

4.  Pour démarrer l’’exécution de la planification, cliquez sur le bouton **OK**.  

     Une ligne planning est créée proposant qu’un ordre de fabrication planifié soit émis afin de produire les dix vélos cyclotourisme, article 1001 pour le 05/02/2021, la date d’expédition de la commande vente.  

     Vérifiez ensuite que cette ligne planning est liée à la commande vente de Cannon Group à l’aide de la fonction **Chaînage**, qui lie de manière dynamique la demande à son approvisionnement planifié.  

5.  Sélectionnez la nouvelle ligne planning, puis choisissez l’action **Chaînage**.  
6.  Sur la page **Chaînage** choisissez l’action **Afficher**.  

     La commande vente pour cinq vélos cyclotourisme au client ayant le numéro 10 000 le 05/02/2021 s’affiche.  

7.  Refermez les pages **Commande vente** et **Chaînage**.  

### <a name="to-calculate-mrp-to-include-underlying-component-needs"></a><a name="to-calculate-mrp-to-include-underlying-component-needs"></a>Pour calculer MRP afin d’inclure les besoins en composants sous-jacents

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille planning**, puis choisissez le lien associé.  
2.  Choisissez l’action **Calculer planning régénératif**.  
3.  Sur la page **Calc. planning - F. planning**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Calculer|Date début|Date de fin|Afficher résultats :|Limiter les totaux à :|  
    |---------------|-------------------|-----------------|-------------------|----------------------|  
    |**PDP** = Oui<br /><br /> **MRP** = Oui|01/23/2021|02/07/2021|1001..1300|Filtre magasin = EAST|  

4.  Pour démarrer l’’exécution de la planification, cliquez sur le bouton **OK**.  

     Un total de 14 lignes planning est créé suggérant des commandes approvisionnement pour l’ensemble de la demande représentée par la commande vente des vélos cyclotourisme au magasin EAST.  

## <a name="analyzing-the-planning-result"></a><a name="analyzing-the-planning-result"></a>Analyse du résultat de la planification
 Pour analyser les quantités proposées, Eduardo examine les lignes planning sélectionnées en descendant pour afficher les écritures chaînage et les paramètres de planification.  

 Sur la page **Feuille planning**, notez que dans la colonne **Date d’échéance**, les commandes approvisionnement proposées sont planifiées en amont à partir de la date d’échéance de la commande vente, le 05/02/2021. La chronologie commence avec la ligne planning supérieure par l’ordre de fabrication visant à produire les vélos cyclotourisme terminés. La chronologie se termine sur la ligne planning inférieure par la commande achat de l’un des articles de niveau inférieur, 1255, arrière de douille, prévue le 30/01/2021. Tout comme la ligne planning de l’article 1251, Axe roue arrière, cette ligne représente une commande achat pour les composants dus à la date de début de son parent produit, l’article de sous-assemblage 1250, qui est dû au 02-03-2014. Tout au long de la feuille, vous pouvez voir que tous les articles sous-jacents sont dus à la date de début de leurs parents.  

 La ligne planning de l’article 1300, ensemble chaîne, indique dix pièces. Ceci diffère des cinq pièces que nous prévoyons comme nécessaires pour répondre à la commande vente. Visualisez les écritures chaînage.  

### <a name="to-view-order-tracking-entries-for-item-1300"></a><a name="to-view-order-tracking-entries-for-item-1300"></a>Pour afficher les écritures chaînage de l’article 1300

1.  Sélectionnez la ligne planning correspondant à l’article 1300, puis choisissez l’action **Chaînage**.  

     Les deux lignes de la page **Chaînage** indiquent que cinq pièces sont suivies depuis la ligne planning (première ligne de chaînage) jusqu’à la commande vente 1001 (deuxième ligne de chaînage). Les cinq dernières pièces indiquées sur la ligne planning ne sont associées à aucune ligne de document, mais bien à un paramètre de planification, à une écriture prévision ou une écriture de commande ouverte. Ces quantités non chaînées sont résumées dans le champ **Quantité non chaînée** dans l’en-tête de la page **Chaînage**.  

2.  Choisissez le champ **Quantité non chaînée**.  

     La page **Éléments planning non chaînés** indique que l’article 1300 utilise un paramètre de planification, Qté minimum commande, de 10,00. Par conséquent, la ligne planning concerne dix pièces au total, mais seulement cinq d’entre elles peuvent être suivies jusqu’à une demande. Les cinq dernières pièces correspondent à une quantité non chaînée afin de satisfaire le paramètre de planification. Revisualisez le paramètre de planification.  

### <a name="to-check-the-planning-parameter"></a><a name="to-check-the-planning-parameter"></a>Pour vérifier les paramètres de planification

1.  Sur la page **Éléments planning non chaînés**, sélectionnez la ligne de chaînage pour l’article 1300.  
2.  Cliquez sur le champ **N° article**, puis choisissez l’action **Avancé**.  
3.  Sur la page **Liste des articles**, choisissez l’action **Points de stock**.  
4.  Sur la page **Liste des points de stock**, ouvrez la fiche point de stock EAST.  
5.  Dans le raccourci **Planning**, notez que le champ **Qté minimum commande** contient 10.  
6.  Refermez toutes les pages, exceptée **Feuille planning**.  

### <a name="to-view-more-order-tracking-entries"></a><a name="to-view-more-order-tracking-entries"></a>Pour afficher des écritures chaînage

1.  Sélectionnez la ligne planning correspondant à l’article 1110, puis choisissez l’action **Chaînage**.  

     La page **Chaînage** indique que cinq jantes sont nécessaires pour chaque ordre de fabrication des roues avant et arrière respectivement.  

     Le même chaînage s’applique aux lignes planning pour les articles 1120, 1160, et 1170. Pour l’article 1120, le champ **Quantité par** dans la nomenclature de production de chaque roue est 50 PCS, ce dont résulte un besoin total de 100.  

     La ligne planning de l’article 1150 pour six pièces semble irrégulière Analysez.  

2.  Sélectionnez la ligne planning correspondant à l’article 1150, puis choisissez l’action **Chaînage**.  

     La page **Chaînage** indique que cinq unités sont suivies pour la roue avant, et une unité est non suivie. Affichez la quantité non chaînée.  

3.  Choisissez le champ **Quantité non chaînée**.  

     La page **Éléments planning non chaînés** indique que l’article 1150 utilise un paramètre de planification, Commandé par, de 2,00, ce qui indique que lorsque l’article est commandé, il doit l’être dans une quantité divisible par 2. Le chiffre le plus proche de 5 divisible par 2 est 6.  

     Le même chaînage s’applique aux lignes planning pour les composants Moyeu avant, les articles 1151 et 1155, mais chaque besoin est multiplié par le pourcentage rebut défini pour l’article 1150 dans le champ **Pourcentage de rebut** de la fiche article.  

 L’analyse du programme d’approvisionnement initial est terminée. Notez que la case à cocher **Accepter message d’action** est activée dans toutes les lignes planning, ce qui indique qu’elles sont prêtes à être converties en commandes approvisionnement.  

## <a name="carrying-out-action-messages"></a><a name="carrying-out-action-messages"></a>Exécution de messages d’action
 Eduardo convertit ensuite les lignes planning proposées en commandes approvisionnement à l’aide de la fonction **Traiter msg. action**.  

### <a name="to-automatically-create-the-suggested-supply-orders"></a><a name="to-automatically-create-the-suggested-supply-orders"></a>Pour créer automatiquement les commandes approvisionnement proposées

1.  Activez la case à cocher **Accepter message d’action** sur toutes les lignes planning avec un avertissement de type Exception.  
2.  Choisissez l’action **Traiter message d’action**.  
3.  Sur la page **Traiter msg. action - Planning**, complétez les champs comme indiqué dans le tableau suivant.  

    |Ordre de fabrication|Commande achat|Ordre transfert|  
    |----------------------|--------------------|--------------------|  
    |Planifié ferme|Créer cdes achat|Créer ordres transfert|  

4.  Cliquez sur le bouton **OK** pour créer automatiquement toutes les commandes approvisionnement proposées.  
5.  Refermez la page **Feuille planning** vide.  

 Le calcul initial, l’analyse et la création d’un programme d’approvisionnement pour la demande au magasin EAST la première semaine de février sont terminés. Dans la section suivante, un autre client commande dix vélos cyclotourisme, et Eduardo doit procéder à une nouvelle planification.  

## <a name="creating-a-net-change-plan"></a><a name="creating-a-net-change-plan"></a>Création d’un planning par écart
 Le lendemain, avant même qu’une commande approvisionnement ne soit démarrée ou comptabilisée, une nouvelle commande vente arrive de Libros S.A. pour dix vélos cyclotourisme à livrer le 12/02/2021. Eduardo est averti de cette nouvelle demande et il procède à une nouvelle planification afin d’adapter le programme d’approvisionnement actif. Eduardo ne calcule, à l’aide de la fonction Planning par écart, que les modifications apportées à la demande ou à l’approvisionnement depuis la dernière exécution de la planification. En outre, Eduardo prolonge la période de planification au 14/02/2021 afin d’inclure la nouvelle demande de vente du 12/02/2014.  

 Le système de planification calcule le meilleur moyen de couvrir la demande de ces deux produits identiques, par exemple consolider certaines commandes achat et certains ordres de fabrication, replanifier d’autres commandes et en créer de nouvelles, s’il y a lieu.  

### <a name="to-create-the-new-sales-demand-and-replan-accordingly"></a><a name="to-create-the-new-sales-demand-and-replan-accordingly"></a>Pour créer les demandes de vente et replanifier en conséquence

1.  Sélectionnez l’action **Nouveau**.  
2.  Sur la page **Commande vente**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Nom donneur d’ordre|Date de préparation|Nombre d’articles|Magasin|Quantité|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Libros S.A|02/12/2021|1 001|EAST|10|  

3.  Acceptez l’avertissement de disponibilité et cliquez sur le bouton **Oui** pour enregistrer la quantité demandée.  
4.  Procédez à une replanification afin d’adapter le programme d’approvisionnement actif.  
5.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille planning**, puis choisissez le lien associé.  
6.  Choisissez l’action **Calculer planning par écart**.  
7.  Sur la page **Calc. planning - F. planning**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Calculer planning|Date début|Date de fin|Afficher résultats :|Limiter les totaux à|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**PDP** = Oui<br /><br /> **MRP** = Oui|01/23/2021|02/14/2021|1001..1300|Filtre magasin = EAST|  

8.  Pour démarrer l’’exécution de la planification, cliquez sur le bouton **OK**.  

 Un total de 14 lignes planning est créé. Notez que sur la première ligne planning, le champ **Message d’action** affiche **Nouveau**, le champ **Quantité**, 10 et le champ **Date d’échéance**, 12/02/2021. Cette nouvelle ligne pour l’article parent supérieur, 1001, vélo cyclotourisme, est créée car l’article utilise une méthode réapprovisionnement de la **commande**, ce qui signifie qu’il doit être approvisionné selon une relation biunivoque envers sa demande, la commande vente de dix pièces.  

 Les deux lignes planning suivantes concernent les ordres de fabrication des roues des vélos cyclotourisme. Chaque commande existante de cinq, dans le champ **Quantité initiale**, passe à 15 dans le champ **Quantité**. Les deux dates d’échéance des deux ordres de fabrication sont inchangées, comme indiqué dans le champ **Message d’action** qui contient **Changer qté**. Cela vaut également pour la ligne planning de l’article 1300, sauf que son multiple commande de 10,00 arrondit la demande suivie de 15 pièces à 20.  

 Toutes les autres lignes planning ont un message d’action **Replanifier & changer qté**. Ceci signifie que, outre le fait de voir leur quantité augmentée, les dates d’échéance sont déplacées par rapport au programme d’approvisionnement afin d’inclure la quantité supplémentaire au temps de production disponible (capacité). Les composants achetés sont replanifiés et augmentés pour répondre aux ordres de fabrication. Analysez la nouvelle planification.  

## <a name="analyzing-the-changed-planning-result"></a><a name="analyzing-the-changed-planning-result"></a>Analyse du résultat de la planification modifié
 Étant donné que tous les articles lot pour lot planifiés du filtre, 1100 à 1300, ont une période de replanification de deux semaines, toutes leurs commandes approvisionnement existantes sont modifiées pour répondre à la nouvelle demande, qui a lieu dans la période de deux semaines spécifiée.  

 Plusieurs lignes planning sont simplement multipliées par trois pour fournir trois 15 vélos au lieu de 5, et les dates d’échéance sont remontées dans le temps pour fournir les quantités augmentées au plus tard à la date d’expédition de la commande vente à Cannon Group. Pour ces lignes planning, toutes les quantités peuvent être chaînées. Les autres lignes planning sont augmentées de dix pièces, et leurs dates d’échéance sont déplacées. Pour ces lignes planning, une partie des quantités est non chaînée en raison de différents paramètres de planification. Visualisez certaines de ces écritures chaînage.  

### <a name="to-view-order-tracking-entries-for-item-1250"></a><a name="to-view-order-tracking-entries-for-item-1250"></a>Pour afficher les écritures chaînage de l’article 1250

1.  Sélectionnez la ligne planning correspondant à l’article 1250, puis choisissez l’action **Chaînage**.  

     Les sept lignes de la page **Chaînage** indiquent que cinq et dix pièces sont chaînées pour la roue arrière pour les vélos cyclotourisme respectivement sur les deux commandes vente.  

     Les cinq dernières pièces sont non chaînées. Analysez.  

2.  Choisissez le champ **Quantité non chaînée**.  

     La page **Éléments planning non chaînés** indique que l’article 1250 utilise un paramètre de planification, Commandé par, de 10,00. Par conséquent, la ligne planning concerne 20 pièces au total pour approcher le besoin réel en arrondissant au nombre le plus proche divisible par 10. Les cinq dernières pièces correspondent à une quantité non chaînée afin de satisfaire le paramètre de planification.  

3.  Refermez toutes les pages, exceptée **Feuille planning**.  

### <a name="to-view-an-existing-order"></a><a name="to-view-an-existing-order"></a>Pour afficher une commande existante

1.  Dans la ligne planning de l’article 1250, sélectionnez le champ **N° ordre référence** .  
2.  Sur la page **O.F. planifié ferme** pour le moyeu arrière. La commande existante pour dix pièces, que vous avez créée dans la première exécution de la planification, s’ouvre.  
3.  Fermez l’ordre de production planifié ferme.  

 La procédure pas à pas, relative au mode d’utilisation du système de planification permettant de détecter automatiquement la demande, de calculer les commandes approvisionnement adéquates en fonction de la demande et des paramètres de planification, puis de créer automatiquement différents types de commandes approvisionnement avec les dates et quantités appropriées, est terminée.  

## <a name="see-also"></a><a name="see-also"></a>Voir aussi
 [Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)   
<!--  [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)    -->
 [Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
