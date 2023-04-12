---
title: "Procédure pas à pas\_: suivi des numéros de série et des numéros de lot"
description: 'Cette rubrique décrit les actions à entreprendre pour empêcher la vente d’un article défectueux, ainsi que la manière de suivre et de rappeler les articles en cas de besoin.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# Procédure pas à pas : suivi des numéros de série et des numéros de lot

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

En cas de produit défectueux, vous devez identifier les erreurs et empêcher les articles concernés d’être vendus. Si des articles défectueux ont déjà été expédiés, vous devez procéder au suivi des destinataires et, au besoin, de rappeler les articles.  

Dans la gestion des défauts, la première chose à faire est de rechercher d’où venaient les articles défectueux et où ils ont été utilisés. Pour ce faire, vous pouvez vous baser sur des données historiques et, pour faciliter votre travail, vous pouvez rechercher l’article en utilisant la page **Traçabilité**.  

Ensuite, déterminez si les articles suivis sont planifiés dans des documents en cours, comme des commandes vente non validées ou des feuilles consommation. Cela s’effectue sur la page **Rechercher des écritures**. Vous pouvez utiliser la fonction Rechercher des écritures pour rechercher tous les types d’enregistrements de données de base.  

## À propos de cette procédure pas à pas

Cette procédure pas à pas explique comment identifier les articles défectueux, leur fournisseur et l’endroit où ils sont utilisés afin que vous puissiez les bloquer ou les rappeler.  

Cette procédure pas à pas présente les tâches suivantes :  

- Traçabilité de l’activité à l’origine.  
- Traçabilité de l’origine à l’activité.  
- Recherche de tous les enregistrements en cours contenant le numéro de série/lot suivi  

## Rôles

Cette procédure pas à pas présente les tâches effectuées par les rôles utilisateur suivants :  

- Contrôleur qualité  
- Gestionnaire d’entrepôt  
- Préparateur de commandes  
- Agent d’achats  

## Conditions préalables

Pour exécuter ce processus pas à pas, vous devez :  

- La société [!INCLUDE[prod_short](includes/prod_short.md)].  
<!-- - To create new items and several business transactions by following the [Prepare Sample Data](walkthrough-tracing-serial-lot-numbers.md#prepare-sample-data).   -->

## Scénario

Ricardo, le contrôleur qualité, se charge d’un retour vente de l’article 1002, vélo de course. Le client, Selangorian Ltd., s’est plaint de fissures au niveau des joints de soudure. Les ingénieurs du contrôle qualité ont confirmé que le cadre du vélo renvoyé est défectueux. Le contrôleur qualité doit maintenant déterminer :  

- le lot de cadres défectueux ;  
- la commande achat sur laquelle le lot défectueux apparaît.  

Dans le département des ventes, le contrôleur qualité sait que le vélo de course renvoyé, l’article 1002, porte le numéro de série SN1. En utilisant cette information de base, ils doivent déterminer l’endroit où le vélo de course fini a été utilisé en dernier, puis ils doivent remonter jusqu’à l’origine pour connaître le numéro de lot duquel le composant défectueux provient.  

Les résultats de cette première tâche de traçabilité permettent d’identifier les cadres défectueux et le fournisseur qui les a vendus. Ensuite, mais toujours dans la même procédure de traçabilité générale, le contrôleur qualité doit trouver tous les vélos de course vendus qui sont équipés d’un cadre provenant du lot défectueux, de manière à pouvoir stopper ou rappeler ces commandes. Enfin, le contrôleur qualité doit trouver des documents ouverts dans lesquels le lot défectueux est utilisé afin d’empêcher d’autres transactions.  

Les deux premières tâches de gestion des défauts sont exécutées sur la page **Traçabilité**. La dernière tâche est réalisée sur la page **Rechercher des écritures** en association avec la page **Traçabilité**.  

## Préparation d’exemples de données

Vous devez créer les nouveaux articles suivants :  

- 2000, Cadre de course : traçabilité spécifique au lot, composant de 1002  
- 1002, Vélo de course : traçabilité spécifique au numéro de série  

Ensuite, vous devez créer plusieurs transactions d’achat, de production et de vente avec les deux articles.  

### Pour créer les articles  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **N°**, , entrez **2000**, puis complétez les champs suivants.  

    |Désignation|Unité de base|Groupe. Groupe compta. produit|Groupe compta. produit TVA|Groupe compta. stock|Code traçabilité|  
    |-----------|--------------------|------------------------|-----------------------|--------------------|------------------|  
    |Cadre de course|PCS|MAT PREM|VAT25|MAT PREM|LOTALL|  

    > [!NOTE]  
    >  Pour entrer l’unité de base, cliquez sur le bouton **Nouveau**, puis sélectionnez **PSC** sur la page **Unités article**.  

4. Tous les autres champs contiennent des données par défaut acceptables ou ne doivent pas être remplis.  
5. Cliquez sur le bouton **OK** pour créer la première fiche article, 2000.  
6. Choisissez **Nouveau**.  
7. Dans le champ **N°**, , entrez **1002**, puis complétez les champs suivants.  

    |Désignation|Unité de base|Groupe. Groupe compta. produit|Groupe compta. produit TVA|Groupe compta. stock|Système réappro.|Code traçabilité|  
    |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|--------------------------|------------------------|  
    |Vélo de course|PCS|DÉTAIL|VAT25|TERMINÉ|O. F.|SNALL|  

    > [!NOTE]  
    >  Pour entrer l’unité de base, cliquez sur le bouton **Nouveau**, puis sélectionnez **PSC** sur la page **Unités article**.  

    Ensuite, définissez les paramètres production de l’article.

8. Sous l’onglet **Réapprovisionnement** , entrez **1000** dans le champ **N° gamme**.  
9. Choisissez le champ **N° nomenclature de production**, puis sélectionnez **Avancé**.  
10. Sur la page **Liste nomenclatures production**, choisissez la première ligne, **1000**, puis sélectionnez l’action **Modifier**.  
11. Sur la page **Nomenclature de production**, modifiez la valeur du champ **Statut** en **Modification en cours**.  
12. Accédez à une ligne vide, entrez **2000** dans le champ **N°** puis entrez **1** dans le champ **Quantité par**.  
13. Modifiez la valeur du champ **Statut** en **Validée**.  
14. Cliquez sur le bouton **OK** pour insérer la nomenclature de production dans la fiche article et fermer la page **Nomenclature de production**.  

    Ensuite, acheter des cadres de course de Custom Metals Incorporated.  

### Pour acheter des composants

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes achat**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Créez une commande achat pour le fournisseur, Custom Metals Incorporated, en renseignant les champs ligne suivants.  

    |Article|Quantité|N° lot|  
    |----|--------|-------|  
    |2000|10|LOT1|  

4. Pour saisir le numéro de lot, choisissez l’action **Lignes traçabilité**.  
5. Sur la page **Lignes traçabilité**, renseignez les champs **N° lot** et **Quantité (Base)**, puis fermez la page.  
6. Dans le champ **N° facture fournisseur**, entrez une valeur.  
7. Cliquez sur **Valider**, choisissez l’option **Réceptionner et facturer**, puis cliquez sur le bouton **OK**.  

    Ensuite, achetez des cadres de course de Coolwood Technologies.  
8. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes achat**, puis choisissez le lien associé.  
9. Sélectionnez l’action **Nouveau**.
10. Créez une commande achat pour le fournisseur, Coolwood Technologies, en renseignant les champs ligne suivants.  

    |Article ;|Quantité|N° lot|  
    |----------|--------------|-------------|  
    |2000|11|LOT2|  

11. Pour entrer le numéro de lot, dans le raccourci **Lignes**, dans le groupe **Ligne**, choisissez l’action **Lignes traçabilité**.  
12. Sur la page **Lignes traçabilité**, renseignez les champs **N° lot** et **Quantité (Base)**, puis fermez la page.  
13. Dans le champ **N° facture fournisseur**, entrez une valeur.  
14. Cliquez sur **Valider**, choisissez l’option **Réceptionner et facturer**, puis cliquez sur le bouton **OK**.  

    Ensuite, deux produisez vélos de course, SN2 et SN1.  

### Pour produire des produits finis

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. lancés**, puis sélectionnez le lien associé.  
2. Choisissez le groupe **Nouveau**.  
3. Créez un ordre de fabrication lancé en renseignant les champs suivants.  

    |N° origine|Quantité|N° de série|  
    |----------|--------|----------|  
    |1002|2|NS1|  
    |1002|2|NS2|  

4. Choisissez l’action **Actualiser O.F.**, puis choisissez le bouton **OK** pour remplir la ligne.  
5. Pour saisir les numéros de série, choisissez l’action **Lignes traçabilité**.  
6. Sur la page **Lignes traçabilité**, renseignez les champs **N° série** et **Quantité (Base)**, puis fermez la page.  

    Ensuite, validez la consommation des cadres de course dans le LOT1.  
7. Sur la page **O.F. lancé**, choisissez l’action **Feuille production**.  
8. Sur la page **Feuille production**, sélectionnez la ligne consommation pour l’article 2000, choisissez l’action **Lignes traçabilité**.
9. Sur la page **Lignes traçabilité**, sélectionnez le champ **N° lot**, choisissez **LOT1**, puis sélectionnez le bouton **OK** button.  
10. Ne modifiez pas les autres valeurs par défaut sur la page **Feuille production**, et sélectionnez l’action **Valider**.  

    Ensuite, deux produisez vélos de course supplémentaires, SN4 et SN3.  

11. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. lancés**, puis sélectionnez le lien associé.  
12. Sélectionnez l’action **Nouveau**.  
13. Créez un ordre de fabrication lancé en renseignant les champs suivants sur l’en-tête.  

    |N° origine|Quantité|N° de série|  
    |----------------|--------------|----------------|  
    |1002|2|SN3|  
    |1002|2|SN4|  

14. Choisissez l’action **Actualiser O.F.** pour remplir la ligne.  
15. Pour saisir les numéros de série, choisissez l’action **Lignes traçabilité**, puis les numéros figurant sur deux lignes dans le champ **N° de série** de la page **Lignes traçabilité**.  

    Ensuite, validez plus de consommation des cadres de course dans le LOT1.  
16. Sur la page **O.F. lancé**, choisissez l’action **Feuille production**.  
17. Sur la page **Feuille production**, sélectionnez la ligne consommation pour l’article 2000, choisissez l’action **Lignes traçabilité**.
18. Sur la page **Lignes traçabilité**, sélectionnez le champ **N° lot**, choisissez **LOT1**, puis sélectionnez le bouton **OK** button.  
19. Ne modifiez pas les autres valeurs par défaut sur la page **Feuille production**, et sélectionnez l’action **Valider**.  

    Vous avez créé quatre vélos de course, SN1 à SN4, et utilisé quatre des dix cadres de course du LOT1, deux pour chaque ordre de fabrication.  

20. Fermez la feuille production et les ordres de fabrication.  

    Ensuite, vendez les vélos de course. Vendez d’abord le vélo de course portant le SN1 à Selangorian Ltd.  

### Pour vendre des articles finis

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2.  Choisissez l’action **Nouveau**, puis créez une commande vente en renseignant les champs suivants.  

    |Client|Article ;|Qté|N° de série|  
    |--------------|----------|----------|----------------|  
    |Soleil et étoiles SARL|1002|1|NS1|  

3.  Pour saisir le numéro de série, choisissez l’action **Lignes traçabilité**, puis le numéro figurant dans le champ **N° de série** de la page **Lignes traçabilité**.  
4.  Cliquez sur **Valider**, choisissez l’option **Livrer et facturer**, puis cliquez sur le bouton **OK**.  

    Ensuite, vendez le vélo de course portant le SN2 au Cannon Group PLC.  

5.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
6.  Choisissez l’action **Nouveau**, puis créez une commande vente en renseignant les champs suivants.  

    |Client|Article ;|Qté|N° de série|  
    |--------------|----------|----------|----------------|  
    |Cannon group PLC.|1002|1|NS2|  

7.  Pour saisir le numéro de série, choisissez l’action **Lignes traçabilité**, puis le numéro figurant dans le champ **N° de série** de la page **Lignes traçabilité**.  
8.  Cliquez sur **Valider**, choisissez l’option **Livrer et facturer**, puis cliquez sur le bouton **OK**.  

    Enfin, vendez séparément quelques cadres de course. Cannon Group PLC commande également quatre cadres de course distincts pour leur propre chaîne de montage.  

9. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
10. Choisissez l’action **Nouveau**, puis créez une commande vente en renseignant les champs suivants.  

    |Client|Article ;|Qté|N° de série|  
    |--------------|----------|----------|----------------|  
    |Cannon group PLC.|2000|5|LOT1|  

11. Pour saisir le numéro de série, dans le raccourci **Lignes**, dans le groupe **Ligne**, sélectionnez l’action **Lignes traçabilité**, puis le numéro dans le champ **N° de série** de la page **Lignes traçabilité**.  

    > [!NOTE]  
    >  Ne validez pas la dernière commande vente pour les cinq cadres de course.  

    Vous avez terminé de préparer les données de démonstration des fonctions Traçabilité et Rechercher des écritures.  

## Traçabilité de l’activité à l’origine

 Dans le département des ventes, le contrôleur qualité sait que le vélo de course renvoyé, l’article 1002, porte le numéro de série SN1. En utilisant cette information de base, ils peuvent déterminer l’endroit où le vélo de course a été utilisé en dernier, dans ce cas, sur l’expédition vente de Selangorian Ltd. Il doit ensuite remonter jusqu’à l’origine pour connaître le numéro de lot duquel le composant défectueux provient.  

### Pour déterminer de quel lot le cadre défectueux provient et qui la fournit

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Traçabilité**, puis choisissez le lien associé.  
2.  Sur la page **Traçabilité**, entrez **SN1** dans le champ **Filtre n° de série**, puis entrez **1002** dans le champ **Filtre article**.  
3.  Conservez les paramètres par défaut de **Article suivi uniquement** dans le champ **Afficher composants** et conservez la méthode de suivi par défaut **Utilisation \- Origine** dans **Méthode de suivi**.  
4.  Choisissez l’action **Suivi**.  

    Remarque : un en-tête d’expédition vente correspond aux critères de recherche. Avant de continuer le suivi, vérifiez que l’expédition correspond à l’envoi du vélo de course défectueux à Selangorian Ltd.  

5.  Sélectionnez la ligne de suivi, puis sélectionnez l’action **Afficher document**.  

    Poursuivez maintenant la traçabilité de l’origine de l’expédition vente du vélo de course portant le numéro SN1.  
6.  Choisissez l’icône + dans les lignes de suivi pour développer progressivement et remonter dans l’enchaînement de transactions d’où provient l’expédition vente.  

    Vous pouvez suivre l’historique des transactions suivant :  

    - Le premier document validé en amont dans l’enchaînement de transactions est la validation des sorties de SN1 à partir du premier O.F. lancé.  
    - Le document validé suivant en amont est la validation de la consommation à partir du premier O.F. lancé. Dans ce cas, le contrôleur qualité constate qu’un cadre de course du LOT1 a été utilisé.  
    - Le document validé situé le plus bas dans cet enchaînement est la réception achat validée sur laquelle les cadres de course du LOT1 ont été entrés dans le stock.  

    Le contrôleur qualité a maintenant déterminé le lot de cadres de course défectueux et ils peuvent rechercher la dernière ligne de suivi pour connaître leur fournisseur, dans ce cas Custom Metals Incorporated.  

    > [!NOTE]  
    >  Ne modifiez plus le résultat de la traçabilité, car vous allez l’utiliser dans la prochaine section.  

     La première tâche de gestion des défauts à l’aide de la page **Traçabilité** est à présent terminée. Le contrôleur qualité doit maintenant déterminer si d’autres documents validés ont traité des cadres de course du LOT1.  

## Traçabilité de l’origine à l’activité

 Le contrôleur qualité a déterminé que les cadres de course défectueux provenaient du LOT1. Ils doivent maintenant retrouver les autres vélos de course équipés d’un cadre provenant du lot défectueux afin de pouvoir stopper ou rappeler ces vélos.  

 Une manière de préparer cette tâche de suivi sur la page **Traçabilité** est d’entrer manuellement LOT1 dans le champ **Filtre n° lot** et 2000 dans le champ **Filtre article**. Toutefois, cette procédure pas-à-pas utilisera la fonction **Opposé suivi - Ligne d’origine** .  

### Pour trouver toutes les activités du lot défectueux  

1.  Sur la page **Traçabilité**, sélectionnez la ligne de la réception achat (la dernière ligne de suivi), choisissez **Opposé suivi - Ligne d’origine**.  

    Le résultat du suivi est maintenant basé sur le filtres de la ligne de suivi pour la réception achat, LOT1 et article 2000, et sur la méthode de suivi **Origine - Activité**.  

    Pour obtenir une vue d’ensemble de toutes les activités de l’article 2000 avec le LOT1, continuez de développer toutes les lignes de suivi.  

2.  Sélectionnez l’action **Développer tout**.  

    Les quatre premières lignes de suivi se rapportent à l’expédition vente à Selangorian Ltd., qui est déjà résolue. La dernière ligne indique qu’un autre vélo de course, SN2, a été produit dans le même O.F. lancé, puis vendu et expédié dans le cadre d’une autre expédition vente.  

    Le contrôleur qualité en informe immédiatement le département des ventes afin qu’il puisse envoyer un rappel du vélo de course défectueux au client, Cannon Group PLC.  

    Au même moment, ils constatent dans les trois dernières lignes de suivi que deux autres articles, SN3 et SN4, ont été fabriqués avec les cadres de course du LOT1. Ils peuvent bloquer ces articles dans le stock.  

    Ainsi se termine la deuxième tâche de gestion des défauts à l’aide de la page **Traçabilité**. Étant donné que la page **Traçabilité** est basée uniquement sur des écritures validées, le contrôleur qualité doit poursuivre jusqu’à la page **Rechercher des écritures** pour vérifier que le LOT1 n’est pas utilisé dans des documents qui ne sont pas validés.  

## Rechercher tous les enregistrements d’un numéro de série/lot

 La page **Traçabilité** a permis au contrôleur qualité de constater que le LOT1 contenait les cadres de course défectueux, d’en découvrir le fournisseur ainsi que la transaction validée dans laquelle ils avaient été utilisés. Ils doivent maintenant déterminer si le LOT1 apparaît dans des documents ouverts en intégrant les résultats du suivi dans la page **Rechercher des écritures** dans laquelle ils peuvent faire une recherche sur l’ensemble des enregistrements de base de données.  

### Pour rechercher toutes les occurrences du LOT1 dans les enregistrements non validés, comme les commandes ouvertes  

1.  Sur la page **Traçabilité**, sélectionnez la première ligne de suivi, c’est-à-dire la réception achat du LOT1.  
2.  Sélectionnez l’action **Rechercher des écritures**.  

    La page **Rechercher des écritures** contient déjà des filtres de recherche basés sur le résultat du suivi du LOT1. Le contrôleur qualité constate que la majorité des enregistrements se rapportent à des documents déjà identifiés sur la page **Traçabilité**. Par exemple, la dernière ligne de la fenêtre Rechercher des écritures de type O.F. fait référence aux deux O.F. lancés qui ont consommé les cadres de course du LOT1.  

    Toutefois, la seconde ligne de la fenêtre Rechercher des écritures de type **Ligne vente** est une ligne document non validée. Par conséquent, le contrôleur qualité continue ses recherches.  

3.  Pour ouvrir l’enregistrement de ligne vente, sélectionnez la seconde ligne de la fenêtre Rechercher des écritures, choisissez l’action **Afficher**. Sinon, choisissez la valeur dans le champ **Nombre d’enregistrements**.  

    Dans ce cas, le contrôleur qualité constate une ligne vente ouverte pour les cadres de course défectueux. Ils suggèrent immédiatement au département des ventes l’annulation de cette commande et la création d’un autre O.F., basé sur des cadres de course non défectueux.  

 Ainsi se termine la procédure pas à pas sur l’utilisation de la page **Rechercher des écritures** pour la gestion des défauts en association avec la page **Traçabilité**.  

## Voir la [formation Microsoft](/training/paths/use-serial-lot-numbers/) associée

## Voir aussi

[Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md)  
[Tracer des articles - Articles suivis](inventory-how-to-trace-item-tracked-items.md)  
[Rechercher des écritures](ui-find-entries.md)  
[Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
