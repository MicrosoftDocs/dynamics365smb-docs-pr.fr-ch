---
title: Configurer et enregistrer un état intracommunautaire
description: 'Apprendre à configurer les fonctionnalités d’état intracommunautaire, et comment enregistrer les transactions avec des sociétés dans d’autres pays/régions de l’UE.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 8451, 12202, 31077'
ms.date: 05/23/2022
ms.author: bholtorf
---
# Configurer et enregistrer un état intracommunautaire

Toutes les sociétés de l’Union européenne doivent déclarer leurs échanges avec les autres pays/régions de l’Union européenne. Vous devez déclarer les mouvements de marchandises aux autorités statistiques de votre pays/région mensuellement et la déclaration doit être remise aux autorités fiscales. Cette déclaration est appelée D.E.B. La page **Feuille intracomm.** permet de remplir des déclarations D.E.B. périodiques.

[!INCLUDE[intrastat-2022w2](includes/intrastat-2022w2.md)]

## Paramètres obligatoires et facultatifs

> [!IMPORTANT]
> Les fiches client et les fiches fournisseur incluent un champ, **Type de partenaire de déclaration d’échanges de biens**, qui a les mêmes valeurs d’option que le champ **Type de partenaire** : *"" (Vide)*, *Société* et *Personne*. Le champ **Type de partenaire de déclaration d’échanges de biens** a remplacé le champ **Type de partenaire** dans la déclaration d’échanges de biens. **Type de partenaire** est utilisé dans SEPA pour définir le régime des prélèvements SEPA (Base ou B2B). **Type de partenaire de déclaration d’échanges de biens** est utilisé pour la déclaration d’échanges de biens uniquement. De cette façon, vous pouvez spécifier des valeurs différentes pour les deux champs, si nécessaire.
>
> Cependant, notez que si le champ **Type de partenaire de déclaration d’échanges de biens** est laissé vide, la valeur du champ **Type de partenaire** est utilisée pour la déclaration d’échanges de biens.

Avant d’utiliser la feuille intracommunautaire pour enregistrer des informations intracommunautaires, plusieurs éléments doivent être configurés :  

* **Configuration intracomm.**  : la page Configuration intracomm. permet d’activer la D.E.B. et de définir des valeurs par défaut. Vous pouvez spécifier si vous devez enregistrer la D.E.B. à partir des expéditions (répartitions), des réceptions (arrivées) ou des deux, selon les seuils définis par vos réglementations locales. Vous pouvez également définir des types de transaction par défaut pour les documents classiques et de retour, utilisés pour la nature des états de transaction.
* **Modèles de feuilles intracommunautaires** : Vous devez configurer les modèles et les feuilles intracommunautaires que vous utiliserez. Comme l’état intracommunautaire doit être généré mensuellement, vous devez créer 12 feuilles intracommunautaires basées sur le même modèle.  
* **Codes marchandise** : les autorités douanières et fiscales ont établi des codes numériques pour classer les articles et les services. Vous spécifiez ces codes sur les articles.
* **Codes nature de transaction** : les pays et les régions ont différents codes pour les types de transactions intracommunautaires, comme l’achat et la vente ordinaires, l’échange de marchandises retournées et l’échange de marchandises non retournées. Configurez tous les codes qui s’appliquent à votre pays/région. Utilisez ces codes sur le raccourci **International** pour les documents achat et vente, et lorsque vous traitez des retours.

    > [!NOTE]
    > À partir de janvier 2022, les Échanges intracommunautaires exigent un code de nature de transaction différent pour les envois aux particuliers ou aux entreprises non assujetties à la TVA et aux entreprises assujetties à la TVA. Pour se conformer à cette exigence, nous vous recommandons de revoir et/ou d’ajouter de nouveaux codes de nature de transaction dans la page **Types de transactions** selon les exigences de votre pays. Vous devriez également revoir et mettre à jour le champ **Type de partenaire de déclaration d’échanges de biens** sur *Personne* pour les clients particuliers ou les entreprises non assujetties à la TVA dans la page **Client**. Si vous n’êtes pas sûr du type de partenaire de déclaration d’échanges de biens ou de transaction correct à utiliser, nous vous recommandons de demander à un expert dans votre pays ou votre région.

* **Modes de transport**: Il existe, de sept codes à un chiffre pour les modes de transport intracommunautaire. **1** Mer, **2** Chemin de fer, **3** Route, **4** Air **5** Voie postale, **7** Transports fixes et **9** Propulsion propre (par exemple le transport en voiture en la conduisant). [!INCLUDE[prod_short](includes/prod_short.md)] ne requiert pas ces codes, cependant, il est préférable que les descriptions offrent une signification similaire.  
* **Régimes** : Vous pouvez les utiliser pour renseigner les descriptions des types de transaction.  
* **Pays d’origine** : Utilisez les codes ISO Alpha à deux lettres pour le pays/la région où le bien a été obtenu ou produit. Si le bien a été produit dans plusieurs pays, le pays/la région d’origine est le dernier pays/la dernière région où il a été transformé de manière significative.
* **Numéro d’identification de TVA de l’opérateur partenaire dans l’État membre d’importation** : Il s’agit du numéro d’identification de TVA de l’opérateur partenaire dans l’État membre d’importation. Le numéro de TVA est également utilisé dans l’échange de données d’exportation intra-UE entre les États membres et permet aux États membres d’attribuer les données reçues à la société importatrice dans leur propre pays/région Les unités chargées des déclarations doivent déclarer le numéro de TVA de l’entreprise qui a déclaré l’acquisition intra-Union de biens dans l’État membre d’importation.

> [!NOTE]
> Le numéro de TVA du partenaire commercial à utiliser peut varier en fonction de la situation commerciale. Par exemple, l’ID à utiliser diffère pour les scénarios tels que les ventes en chaîne, où un fournisseur vend un produit dans un autre pays, puis cette société revend l’article à une autre entreprise dans le même pays, le commerce circulaire, etc. Si vous n’êtes pas sûr du numéro de TVA correct à utiliser, nous vous recommandons de demander à un expert dans votre pays ou votre région.

Éventuellement, vous pouvez également configurer :

* **Dépts destination/provenance** : Vous pouvez les utiliser pour renseigner des informations sur les pays et les régions.  
* **Pays destination/provenance** : Vous pouvez les utiliser pour spécifier les emplacements dans lesquels vous livrez ou recevez des articles vers ou à partir d’autres pays/régions. L’aéroport de Heathrow est un exemple de pays destination/provenance. Vous pouvez saisir des points d’entrée et de sortie sur les documents vente et achat sur le raccourci **International**. Ces informations sont également copiées à partir des écritures article lorsque vous créez la feuille intracomm..  

### Pour configurer des modèles et des feuilles intracommunautaires

Les lots de feuilles intracommunautaires incluent uniquement des écritures articles et non des écritures comptables. Si certaines écritures comptables doivent être inclues dans la D.E.B. vous devez les saisir manuellement. Par exemple, si vous achetez un ordinateur dans un autre pays/région de l’UE, cet ordinateur n’est pas comptabilisé dans le stock, mais validé dans un compte général. Vous devez saisir manuellement ce type d’écriture dans la feuille intracommunautaire.  

Vous pouvez exporter les écritures vers un fichier que vous pouvez envoyer à vos administrations intracommunautaires. Vous pouvez également imprimer un état, saisir manuellement les informations sur les formulaires de vos administrations, et envoyer les informations.

> [!NOTE]
> Nous vous recommandons de configurer un seul lot de feuilles intracommunautaires par mois.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modèles feuille intracomm.**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Créez un modèle pour chaque formulaire de D.E.B que vous utilisez.  
3. Pour créer des lots, sélectionnez l’action **Lots**.  
4. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Créez un modèle pour chaque formulaire de D.E.B que vous utilisez.

> [!NOTE]
> Dans le champ **Période statistique**, entrez la période statistique sous la forme d’un nombre à quatre chiffres, les deux premiers chiffres représentant l’année et les deux suivants, le mois. Par exemple, saisissez 1706 pour juin 2017.

### Pour configurer des modes de transport

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modes de transport**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Pour configurer les champs de la D.E.B. obligatoires

Dans certains pays/régions, tels que l’Espagne et le R-U, les autorités nécessitent que les états Intracomm. comprennent, par exemple, le mode d’expédition des achats ou d’autres valeurs lorsque les ventes sont supérieures à un certain seuil. Sur la page **Configuration intracomm.**, vous pouvez sélectionner pour faire **Paramètres liste de contrôle de la déclaration d’échanges de biens** pour définir les champs obligatoires sur la page **Feuille intracomm.**.

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration intracomm.**, puis choisissez le lien associé.
2. Choisissez l’action **Paramètres liste de contrôle de la déclaration d’échanges de biens**.
3. Sur la page **Paramètres liste de contrôle de la déclaration d’échanges de biens**, sélectionnez dans le champ **Nom de champ** pour prélever le champ de déclaration d’échanges de biens que vous souhaitez rendre obligatoire.

### Tchéquie

Notamment pour les entreprises tchèques, vous devez également paramétrer des codes marchandise et des codes nature de transaction.  

#### Pour configurer des codes marchandise

Tous les articles que vous achetez ou vendez doivent avoir un code marchandise.  

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Codes marchandise.**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Pour affecter un code marchandise à un article, accédez à la page **Fiche article**, développez le raccourci **Coûts et validation**, puis saisissez le code dans le champ **Code marchandise**.

### Italie

Notamment pour les entreprises italiennes, vous devez également paramétrer des codes marchandise et des codes nature de transaction.  

#### Pour configurer des codes nature de transaction

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Codes nature de transaction.**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Si vous utilisez souvent un code nature de transaction spécifique, vous pouvez le définir comme valeur par défaut. Pour ce faire, accédez à la page **Configuration intracomm.** et choisissez le code.

## Pour enregistrer un état communautaire

Après avoir renseigné la feuille intracommunautaire, vous pouvez exécuter l’action **État : Liste de contrôle** pour vérifier que toutes les informations de la feuille sont correctes. Champs obligatoires que vous avez définis sur la page **Paramètres liste de contrôle de la déclaration d’échanges de biens** qui sont des valeurs manquante, seront affichés dans le récapitulatif des erreurs et d’avertissement de la page **Feuille intracomm.**. Ensuite, vous pouvez imprimer un état intracommunautaire en tant que formulaire, ou créer un fichier à envoyer à l’administration fiscale de votre pays/région.  

### Pour renseigner des feuilles intracommunautaires

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuille intracomm.**, puis choisissez le lien associé.  
2. Sur la page **Feuille intracomm.**, dans le champ **Nom de la feuille**, sélectionnez la feuille concernée, puis sélectionnez **OK**.  
3. Choisissez l’action **Proposer lignes**. Les champs **Date début** et **Date fin** contiennent déjà les dates spécifiées sur la feuille pour la période statistique.  
4. Dans le champ **% régulation coût**, entrez un pourcentage pour couvrir le transport et l’assurance. Lorsque vous saisissez un pourcentage, la valeur du champ **Valeur statistique** de la feuille augmente proportionnellement.  
5. Cliquez sur **OK** pour démarrer le traitement par lots.  

Le traitement par lots récupère toutes les écritures article de la période statistique et les insère sous forme de lignes dans la feuille intracommunautaire. Vous pouvez modifier au besoin les nouvelles lignes.  

> [!IMPORTANT]  
> Le traitement par lots récupère uniquement les écritures qui contiennent un code pays/région pour lequel un code intracommunautaire a été entré dans la page **Pays/Régions**. Vous devez donc entrer les codes intracommunautaires correspondant aux codes pays pour lesquels vous allez lancer le traitement par lots. Le traitement par lots définit le champ **Numéro de TVA du partenaire** sur *QV999999999999* pour les particuliers ou les entreprises non assujetties à la TVA (clients avec le champ **Type de partenaire de déclaration d’échanges de biens** défini sur *Personne*), et il utilise la valeur du champ **Type de transaction** de l’écriture comptable de l’article comptabilisé ou de l’écriture comptable de la tâche.

### Pour modifier les lignes des journaux Échanges intracommunautaires

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuille intracomm.**, puis choisissez le lien associé.  
2. Sur la page **Feuille intracomm.**, dans le champ **Nom de la feuille**, sélectionnez la feuille concernée, puis sélectionnez **OK**.  
3. Utilisez le volet de filtre utilisateur pour filtrer les lignes du journal Échanges intracommunautaires en fonction de certains critères. Par exemple, filtrez les champs **Numéro de TVA du partenaire** avec la valeur *QV999999999999*.
4. Choisissez l’icône **Partager** ![Partager une page dans une autre application.](media/share-icon.png) et sélectionnez **Modifier dans Excel**
5. Dans Excel, modifiez les lignes de journal Échanges intracommunautaires que vous avez filtrées. Par exemple, modifiez les valeurs du champ **Type de transaction**.  
6. Publiez les modifications que vous avez apportées dans Excel dans [!INCLUDE[prod_short](includes/prod_short.md)]

> [!NOTE]
> Dans les versions de [!INCLUDE[prod_short](includes/prod_short.md)] qui ne prennent pas en charge [**Modifier dans Excel**](across-work-with-excel.md#edit-in-excel) pour les feuilles, créez des packages de configuration pour exporter et importer des lignes feuille intracommunautaire vers Excel. Pour plus d’informations, voir [Migrer des données locales vers Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) dans le contenu d’administration.

### Enregistrer un état intracommunautaire sur un formulaire ou un fichier

Pour obtenir les informations requises sur le formulaire de D.E.B. à partir des autorités statistiques, vous devez imprimer l’état **D.E.B. : Formulaire**. Avant d’effectuer cette opération, vous devez préparer la feuille intracommunautaire et la renseigner. Si vous avez à la fois des transactions d’achat et de vente, vous devez compléter un formulaire distinct pour chaque type et donc imprimer l’état deux fois.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles intracomm.**, puis choisissez le lien associé.  
2. Sur la page **Feuille intracomm.**, choisissez la feuille concernée dans le champ **Nom de la feuille**.  
3. Si ce n’est déjà fait, renseignez la feuille manuellement ou sélectionnez l’action **Proposer lignes**.  
4. Choisissez l’action **Imprime la feuille intracomm.**.  
5. Sur le raccourci **Ligne feuille intracomm.**, ajoutez un filtre **Type**, puis spécifiez s’il s’agit d’une **Réception** ou d’une **Expédition**.  
6. Choisissez **Envoyer à** pour imprimer l’état.  

### Enregistrer un état intracommunautaire sur un fichier

Vous pouvez envoyer la déclaration d’échanges de biens en tant que fichier. Avant de créer le fichier, vous pouvez imprimer la liste de contrôle contenant les mêmes informations que le fichier.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuille intracomm.**, puis choisissez le lien associé.  
2. Sur la page **Feuille intracomm.**, sélectionnez la feuille concernée dans le champ **Nom de la feuille**.  
3. Si ce n’est déjà fait, renseignez la feuille manuellement ou sélectionnez l’action **Proposer lignes**.  
4. Choisissez l’action **Créer fichier**.  
5. Dans la page de tâche par lot, sélectionnez le bouton **OK**.  
6. Choisissez **Enregistrer**.  
7. Sélectionnez l’emplacement d’enregistrement du fichier, entrez son nom, puis choisissez **Enregistrer**.

> [!NOTE]
> Lorsqu’une ligne du rapport de déclaration d’échanges de biens a une unité de mesure supplémentaire, le poids de l’article ne sera pas affiché, car cette valeur n’est pas requise.

## Réorganiser les feuilles intracommunautaires

Parce que vous devez soumettre une D.E.B. chaque mois et créer une feuille pour chaque état, il peut donc exister de nombreuses feuilles. Les lignes feuille ne sont pas supprimées automatiquement. Vous pouvez réorganiser régulièrement les feuilles. Pour cela, il suffit de supprimer les feuilles dont vous n’avez plus besoin. Les lignes de ces feuilles sont également supprimées.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles intracomm.**, puis choisissez le lien associé.  
2. Pour afficher les options, choisissez le champ **Nom de la feuille**.  
3. Cliquez sur les feuilles à supprimer, puis sélectionnez le bouton **Supprimer**.  

## Nomenclatures produits

Dans de nombreux pays/régions, les autorités douanières et fiscales établissent des codes article à huit unités pour divers articles. Pour que les écritures article comportent les informations nécessaires lorsque le programme les importe vers la ligne feuille intracommunautaire, vous devez avoir saisi les informations concernant la nomenclature produit dans la page **Nomenclatures produits**. Trouvez les codes des articles avec lesquels votre société travaille et saisissez-les dans la fenêtre **Nomenclatures produits**.

Ajoutez tous les codes que vous utilisez dans la page **Nomenclatures produit**. Vous devez saisir les codes sur la fiche article avant de commencer à valider. Lorsque vous avez créé ces codes, saisissez-les dans le champ **Nomenclature produits** de la fiche article. Vous devez également renseigner le champ **Poids net** de la fiche article.

## Voir la formation associée sur [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## Voir aussi

[Gestion financière](finance.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
