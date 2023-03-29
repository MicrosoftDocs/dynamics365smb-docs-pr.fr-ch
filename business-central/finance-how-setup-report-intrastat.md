---
title: Paramétrer les états intracommunautaires
description: Découvrez comment configurer les fonctionnalités d’état intracommunautaire pour enregistrer les transactions avec des sociétés dans d’autres pays de l’UE.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# Paramétrer les états intracommunautaires

Toutes les sociétés de l’Union européenne (UE) doivent déclarer leurs échanges avec les autres pays/régions de l’Union européenne. Les sociétés doivent déclarer les mouvements de marchandises aux autorités statistiques de leur pays/région mensuellement et la déclaration doit être remise aux autorités fiscales. Intrastat est le système de collecte des statistiques du commerce des biens au sein de ces pays/régions. Vous utilisez un **État intracommunautaire** pour effectuer des déclarations intracommunautaires périodiques (généralement mensuelles), collecter, enregistrer et déclarer le commerce de marchandises conformément à la législation locale.

La déclaration intracommunautaire Intrastat est basée sur les réglementations de base de l’UE qui s’appliquent à tous les pays ; cependant, dans la pratique, il existe certaines différences au sein des différents pays. Chaque pays a ses règles édictant exactement quoi déclarer et comment.

> [!NOTE]
> Les informations Intrastat ne s’appliquent pas aux mouvements de services entre pays, mais uniquement aux biens (articles et immobilisations). Si le gouvernement local exige l’enregistrement du mouvement des services entre les pays, cela est possible en utilisant la fonctionnalité **Déclaration de service**.
>
> Cette fonctionnalité devrait être disponible à partir de novembre 2022 sous forme d’application sur [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Si vous voulez l’utiliser, vous devrez d’abord l’installer sur la page **Gestion des extensions**.

> [!IMPORTANT]
> Cet article couvre la nouvelle expérience des états intracommunautaires disponible à partir de [!INCLUDE[prod_short](includes/prod_short.md)], version 21. Consultez votre administrateur pour savoir quelle version votre entreprise utilise et pour activer la nouvelle fonctionnalité.
>
> Lisez l’article sur la configuration et l’utilisation des états intracommuncautaires de la version précédente ici : [Configurer et enregistrer un état intracommunautaire](finance-how-setup-report-intrastat-v20.md).

## Activer la nouvelle expérience d’états intracommunautaires

Dans la 2è vague de lancement 2022, [!INCLUDE[prod_short](includes/prod_short.md)] inclut une expérience d’échanges intracommunautaires avec des fonctionnalités étendues. Si la nouvelle fonctionnalité d’états intracommunautaires n’est pas activée dans votre environnement, elle peut être activée manuellement par un administrateur sur la page **Gestion des fonctionnalités**.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Gestion des fonctionnalités**, puis sélectionnez le lien associé.
2. Sur la page **Gestion des fonctionnalités**, sélectionnez la ligne **Mise à jour des fonctionnalités : remplacer la fonctionnalité intracommunautaire existante par la nouvelle extension intracommunautaire**. Découvrez la gestion des fonctionnalités sur [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management) dans le contenu de l’administration.
3. Dans la colonne **Activer pour**, sélectionnez **Tous les utilisateurs**.
4. Lisez l’explication de la façon dont le système sera mis à niveau, puis sélectionnez **Oui** si vous êtes d’accord.
5. Sélectionnez **Suivant** et vous obtiendrez une configuration de base pour les états intracommunautaires. Découvrez plus d’informations sur la configuration des états intracommunautaires dans la section [Configuration des états intracommunautaires](#intrastat-configuration).
6. Une fois la configuration terminée, choisissez **Terminer** pour commencer à utiliser la nouvelle expérience d’états intracommunautaires.

> [!IMPORTANT]
> Gardez à l’esprit que vous ne pouvez pas utiliser les anciennes et les nouvelles expériences en parallèle. Avant d’activer l’extension dans un environnement de production, il est recommandé d’activer et de tester d’abord cette fonctionnalité dans un environnement sandbox avec une copie des données de production avant de procéder dans un environnement de production. Une fois que vous avez activé une nouvelle expérience utilisateur dans votre environnement de production, vous ne pouvez pas revenir à l’ancienne fonctionnalité d’états intracommunautaires.

> [!NOTE]
> Selon l’emplacement de votre entreprise, l’activation de la fonctionnalité décrite ci-dessus sera suffisante. Pour les pays dotés de fonctionnalités spécifiques pour la déclaration intracommunautaire, vous devez activer l’application d’échanges intracommunautaires spécifique au pays en plus de l’extension principale.

## Configuration des états intracommunautaires

Avant de pouvoir utiliser les états intracommunautaires, plusieurs configurations doivent être configurées.

### Paramétrer les déclarations d’échanges intracommunautaires

La page **Paramétrer les déclarations d’échanges intracommunautaires** permet d’activer les états intracommunautaires et de définir des valeurs par défaut. Vous pouvez spécifier si vous devez enregistrer les états intracommunautaires à partir des expéditions (répartitions), des réceptions (arrivées) ou des deux, selon les seuils définis par vos réglementations locales. Vous pouvez également définir des types de transaction par défaut pour les documents classiques et de retour, utilisés pour la nature des états de transaction.

Pour configurer les états intracommunautaires :

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramétrer les déclarations d’échanges intracommunautaires**, puis choisissez le lien associé.
2. Ouvrez le raccourci **Général** et complétez les champs selon les besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Le tableau ci-dessous décrit certains des champs clés :

   | Champ | Désignation |
   | --- | --- |
   | **Déclarer les réceptions** | Spécifie que vous devez inclure les arrivages de marchandises reçues dans les déclarations d’échanges intracomm. |
   | **Déclarer les expéditions** | Spécifie que vous devez inclure les expéditions de marchandises réparties dans les états intracomm. |
   | **Expéditions basées sur**  | Spécifie sur la base de quel code pays les lignes de l’état de déclaration d’échanges de biens sont extraites. Vous pouvez choisir l’une des options : **Pays de vente**, **Pays de facturation** ou **Pays de livraison**. |
   | **N° TVA basé sur** | Spécifie le numéro de taxe à la valeur ajoutée (TVA) du code client/fournisseur qui est utilisé comme base pour l’état intracommunautaire. Vous pouvez choisir l’une des options : **TVA de vente** ou **TVA de facturation**. |
   | **N° TVA société du fichier** | Spécifie comment le numéro d’immatriculation de TVA de la société est exporté vers le fichier d’état intracommunautaire. Vous pouvez choisir l’une des options suivantes : N° Imm. TVA, en ajoutant le code pays de l’UE comme préfixe et en supprimant le code pays de l’UE du numéro de TVA. |
   | **N° TVA fournisseur du fichier** | Spécifie comment le numéro d’immatriculation de TVA du fournisseur est exporté vers le fichier d’état intracommunautaire. Vous pouvez choisir l’une des options suivantes : N° Imm. TVA, en ajoutant le code pays de l’UE comme préfixe et en supprimant le code pays de l’UE du numéro de TVA. |
   | **N° TVA client du fichier** | Spécifie comment le numéro d’immatriculation de TVA du client est exporté vers le fichier d’état intracommunautaire. Vous pouvez choisir l’une des options suivantes : N° Imm. TVA, en ajoutant le code pays de l’UE comme préfixe et en supprimant le code pays de l’UE du numéro de TVA. |
   | **Obtenir TVA partenaire pour** | Spécifie à partir de quel type de ligne de **l’état intracommunautaire** le numéro d’immatriculation de TVA du partenaire est mis à jour. En fonction de vos exigences locales, vous pouvez choisir uniquement pour les réceptions, uniquement pour les expéditions ou pour les deux types de lignes. |
3. Ouvrez le raccourci **Transactions par défaut** et complétez les champs selon les besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Le tableau ci-dessous décrit certains des champs clés :

   | Champ | Désignation |
   | --- | --- |
   | **Type de trans. par défaut** | Spécifie le type de transaction par défaut pour les expéditions vente régulières, les expéditions de service et les réceptions achat enregistrées. |
   | **Type de trans. par défaut – Retours** | Spécifie le type de transaction par défaut pour les retours vente, les retours de service et les retours achat. |
   | **N° TVA privée par défaut** | Spécifie le numéro de TVA de la personne privée par défaut au cas où la personne privée doit avoir un numéro de TVA dédié sur l’état intracommunautaire. |
   | **N° TVA commerciale tierce partie par défaut** | Spécifie le numéro de TVA commerciale de la tierce partie par défaut au cas où vous n’auriez pas son numéro de TVA. |
   | **TVA par défaut pour état inconnu** | Spécifie le numéro de TVA par défaut d’un état inconnu. |
   | **Code pays/région par défaut** | Spécifie le code du pays de réception par défaut. |
4. Ouvrez le raccourci **Génération d’états** et complétez les champs selon les besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Le tableau ci-dessous décrit certains des champs clés :

   | Champ | Désignation |
   | --- | --- |
   | **Code déf. échge données** | Spécifie le code de définition d’échange de données pour générer le fichier intracommunautaire. Cela ne fonctionne que si le champ **Fractionner les fichiers réceptions/expéditions** est défini sur **Non**. |
   | **Fractionner les fichiers réceptions/expéditions** | Indique si les réceptions et les expéditions doivent être enregistrées dans deux fichiers séparés. |
   | **Fichier zip (-s)** | Indique si le fichier d’état (-s) doit être ajouté au fichier .zip. |
   | **Code déf. échange données – Réception** | Spécifie le code de définition d’échange de données pour générer le fichier d’état intracommunautaire pour les biens reçus. Cela ne fonctionne que si le champ **Fractionner les fichiers réceptions/expéditions** est défini sur **Oui**. |
   | **Code déf. échange données – Expédition** | Spécifie le code de définition d’échange de données pour générer le fichier d’état intracommunautaire pour les biens expédiés. Cela ne fonctionne que si le champ **Fractionner les fichiers réceptions/expéditions** est défini sur **Oui**. |
5. Ouvrez le raccourci **Numérotation** pour configurer les **N° intracommunautaires**.

### Configurer un fichier de déclaration

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Définitions d’échange de données**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Sur le raccourci **Général**, décrivez la définition d’échange de données, le type de fichier de données, le séparateur de colonnes, le codeunit associé, XMLport et les autres champs en remplissants les champs.
4. Sur le raccourci **Définitions de ligne**, décrivez le formatage des lignes du fichier de données en remplissant les champs en fonction du champ **Type de ligne**, et où vous devez définir le nombre de colonnes pour cette ligne.
5. Sur le raccourci **Définitions de colonne**, remplissez la ligne pour chaque colonne planifiée. Vous pouvez définir des noms de colonnes, des types de données (*Texte*, *Date* ou *Décimal*), la longueur de la ligne à largeur fixe qui contient la colonne si le fichier est de type Texte fixe, et quelques autres paramètres.
6. Sélectionnez l’action **Mappage des champs**dans le raccourci **Définitions de ligne** pour ouvrir la page **Mappage des champs**.
7. Créez la nouvelle entrée, et sur le raccourci **Général**, sélectionnez **l’ID de table** approprié (pour **Ligne d’état intracommunautaire**, choisissez 4812), puis remplissez d’autres champs :
   1. Spécifiez l’index de clé pour trier les enregistrements source avant l’exportation dans le champ **Index clé**.
   2. Sélectionnez le **Codeunit de mappage** approprié.
8. Sur le raccourci **Mappage des champs**, ajoutez les colonnes que vous avez précédemment configurées dans le raccourci **Définitions de colonne**, puis ajoutez ce qui suit :
   1. Spécifiez **l’ID de champ** pour chacune des colonnes.
   2. Spécifiez la **Règle de transformation** pour chaque colonne dont vous avez besoin. Cela spécifie la règle qui transforme un texte importé en valeur prise en charge avant de pouvoir être mappé dans un champ spécifié dans [!INCLUDE[prod_short](includes/prod_short.md)]. Lorsque vous choisissez une valeur dans ce champ, la valeur exacte est saisie dans le champ **Règle de transformation** dans la table **Tampon correspondance champ échge données** et inversement.
9. Si vous devez regrouper des entrées en fonction de certaines colonnes, sur le raccourci **Groupement de champs**, choisissez les champs que vous souhaitez utiliser pour le regroupement.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] est livré avec la définition d’échange de données préconfigurée pour les états intracommunautaires pour tous les pays pour lesquels la traduction a été faite. Découvrez plus d’informations sur la création d’une définition d’échange de données dans l’article [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).

### Définir les champs obligatoires avec la liste de contrôle des états intracommunautaires

Dans certains pays, les autorités nécessitent que les états intracommunautaires comprennent, par exemple, le mode d’expédition des achats ou d’autres valeurs lorsque les ventes sont supérieures à un certain seuil.

Pour définir des champs et/ou des valeurs obligatoires sur la page **État intracommunautaire** :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration de l’état de déclaration d’échanges de biens**, puis choisissez le lien associé.
2. Choisissez l’action **Liste de contrôle des états intracommunautaires**.
3. Ajoutez les lignes nécessaires à la vérification en suivant les instructions suivantes :
   1. Définissez le champ **N° champ** sur un champ qui doit être vérifié pour une valeur non vide.
   2. Remplissez le champ **Expression de filtre** si nécessaire, selon les règles suivantes :
      1. Lorsque vous ouvrez la **Page de filtres**, choisissez le **Filtre** dont vous avez besoin pour la vérification.
      2. À l’étape suivante, choisissez une valeur liée au **Filtre** que vous avez utilisé.
      3. Si vous avez d’autres filtres à remplir pour ce champ spécifique, vous pouvez ajouter un autre filtre en suivant les mêmes étapes.
      4. Lorsque vous avez fini de saisir les filtres pour le champ choisi, sélectionnez **OK**.
   3. Sélectionnez le champ **Expression filtre inversé** pour indiquer que la vérification des champs n’est exécutée que sur les lignes qui ne correspondent pas à l’expression du filtre. Si la ligne n’est pas filtrée, ce champ est ignoré.

> [!NOTE]
> Lorsque vous ouvrez la **Page des filtres** depuis la ligne **Expression de filtre**, vous pouvez utiliser toutes les expressions de filtre standard liées au champ spécifique que vous souhaitez filtrer.
>
> Faites preuve de prudence lorsqu’il est question de configurer des règles de validation. Elles peuvent varier d’un pays à l’autre.

## Utiliser des codeunits personnalisés dans les états intracommunautaires

Si vous souhaitez modifier le fonctionnement des états intracommunautaires et que la configuration par défaut ne suffit pas, vous pouvez personnaliser le système en étendant les fonctionnalités standard. Si vous avez besoin de modifier davantage le comportement des états intracommunautaires, vous pouvez développer vos propres codeunits. Cependant, lorsque vous créez des codeunits, vous devez apporter des modifications supplémentaires pour les utiliser. Pour configurer le système pour utiliser vos propres objets :

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration des déclarations de TVA**, puis sélectionnez le lien associé.
2. Dans la page **Configuration des déclarations de TVA**, ajoutez une nouvelle ligne.
3. Dans le champ **Type de déclaration de TVA**, choisissez l’option **État intracommunautaire**.
4. Dans le champ **Version de la déclaration de TVA**, indiquez la version de la déclaration.
5. Après cela, vous pouvez ajouter vos codeunits pour les options suivantes : a. Dans le champ **ID Codeunit fonction Proposer lignes**, spécifiez le nouveau codeunit pour suggérer des lignes dans les lignes des états intracommunautaires.
   b. Dans le champ **ID Codeunit de contenu**, spécifiez le nouveau codeunit pour exporter les données sous forme de fichier à l’aide d’une définition d’échange de données.
   c. Dans le champ **ID Codeunit fonction Valider**, spécifiez les nouveaux codeunits pour valider les résultats dans les lignes des états intracommunautaires.

> [!IMPORTANT]
>
> Cette ligne doit être vide si vous utilisez les codeunits standard. Vous ne devez créer une ligne et la configurer que si vous avez développé des codeunits personnalisés.

## Autres configurations des états intracommunautaires

> [!IMPORTANT]
> Les fiches client et les fiches fournisseur incluent un champ, **Type de partenaire de déclaration d’échanges de biens**, qui a les mêmes valeurs d’option que le champ **Type de partenaire** : "" (Vide), *Société* et *Personne*. Le champ **Type de partenaire de déclaration d’échanges de biens** a remplacé le champ **Type de partenaire** dans la déclaration d’échanges de biens. Le champ **Type de partenaire** est utilisé dans l’Espace unique de paiement en euros (SEPA) pour définir le schéma de prélèvement SEPA (Core ou B2B). Le champ **Type de partenaire de déclaration d’échanges de biens** est utilisé pour les états intracommunautaires uniquement. De cette façon, vous pouvez spécifier des valeurs différentes pour les deux champs, si nécessaire.
>
> Si le champ **Type de partenaire de déclaration d’échanges de biens** est laissé vide, la valeur du champ **Type de partenaire** est utilisée pour la déclaration d’échanges de biens.

À l’exception de **Paramétrer les déclarations d’échanges intracommunautaires**, **Définitions d’échange de données**, et **Liste de contrôle des états intracommunautaires**, vous devez également configurer d’autres paramètres :

| Page | Désignation |
| ---- | ----------- |
| **Pays/Régions** | Avant de commencer à utiliser les états intracommunautaires, vous devez également configurer la page **Pays/Régions**. Sur cette page, vous devez ajouter le **Code pays/région de l’UE** et le **Code intracommunautaire** pour spécifier un code pour le pays/la région avec lequel vous commercez, car il sera utilisé dans les états intracommunautaires. |
| **Nomenclatures produits** | Dans de nombreux pays, les autorités douanières et fiscales établissent des codes article à huit chiffres pour divers articles. Pour que les écritures article contiennent les informations nécessaires lorsque le programme les importe dans la ligne feuille intracommunautaire, vous devez entrer le code article dans la page **Nomenclatures produits**. Trouvez les codes des articles avec lesquels votre société travaille et saisissez-les dans la page **Nomenclatures produits**. |
| **Modes de transport** | Il existe sept codes à un chiffre pour les modes de transport intracommunautaire. **1** Mer, **2** Chemin de fer, **3** Route, **4** Air **5** Voie postale, **7** Transports fixes et **9** Propulsion propre (par exemple le transport en voiture en la conduisant). [!INCLUDE[prod_short](includes/prod_short.md)] ne requiert pas ces codes spécifiques, cependant, il est préférable que les descriptions offrent une signification similaire. |
| **Types transaction** | Les pays et les régions ont différents codes pour les types de transactions intracommunautaires, comme l’achat et la vente ordinaires, l’échange de marchandises retournées et l’échange de marchandises non retournées. Configurez tous les codes qui s’appliquent à votre pays/région. Ces codes seront ensuite utilisés sur le raccourci **International** pour les documents achat et vente, et lorsque vous traitez des retours. |
| **Régimes** | Configurez des codes pour compléter les descriptions des types de transaction. |
  > [!NOTE]
  > À partir de janvier 2022, les Échanges intracommunautaires exigent des codes de nature de transaction différent pour les envois aux particuliers ou aux entreprises non assujetties à la TVA et aux entreprises assujetties à la TVA. Pour se conformer à cette exigence, nous vous recommandons de revoir et/ou d’ajouter de nouveaux codes de nature de transaction dans la page **Types de transactions**, selon les exigences de votre pays. Vous devriez également revoir et mettre à jour le champ **Type de partenaire de déclaration d’échanges de biens** sur *Personne* pour les clients particuliers ou les entreprises non assujetties à la TVA dans la page **Client**. Si vous n’êtes pas sûr du type de partenaire de déclaration d’échanges de biens ou de transaction correct à utiliser, nous vous recommandons de demander à un expert dans votre pays ou votre région.

| **Champ** | **Description** |
| --------- | --------------- |
| **Poids net** | Le poids est l’une des configurations de base liées aux états intracommunautaires, car le **Poids total** est obligatoire dans les déclarations. Pour être prêt pour cette exigence, vous devez également remplir le champ **Poids net** sur la fiche de l’article ou de l’immobilisation. |
| **Code pays origine** | Utilisez les codes ISO Alpha à deux lettres sur la fiche article ou immobilisation pour le pays où le bien a été obtenu ou produit. Si le bien a été produit dans plusieurs pays, le pays d’origine est le dernier pays où il a été transformé de manière significative. |
| **Numéro d’identification de TVA de l’opérateur partenaire dans l’État membre d’importation** | Il s’agit du numéro d’identification de TVA de l’opérateur partenaire dans l’État membre d’importation. Le numéro de TVA est également utilisé dans l’échange de données d’exportation intra-UE entre les États membres et permet aux États membres d’attribuer les données reçues à la société importatrice dans leur propre pays. Les unités chargées des déclarations doivent déclarer le numéro de TVA de l’entreprise qui a déclaré l’acquisition intra-Union de biens dans l’État membre d’importation. |

Éventuellement, vous pouvez également configurer :

* **Codes marchandise** : les autorités douanières et fiscales ont établi des codes numériques pour classer les articles et les services. Vous spécifiez ces codes sur les articles.
* **Dépts destination/provenance** : informations supplémentaires sur les pays et les régions.
* **Points d’entrée/sortie** : spécifiez les emplacements dans lesquels vous livrez ou recevez des articles vers ou à partir d’autres pays. Un aéroport est un exemple de point d’entrée ou de sortie. Vous pouvez saisir des points d’entrée et de sortie sur les documents vente et achat sur le raccourci **International**. Ces informations sont également copiées à partir des écritures article lorsque vous créez la feuille intracomm..
* **Unité de mesure supplémentaire** : la quantité de marchandises pour l’état intracommunautaire peut être soit le poids net (en kilogrammes), soit une unité supplémentaire. Si des unités supplémentaires sont requises, vous devez les configurer pour les articles et les immobilisations.

#### Configurer les modes de transport

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modes de transport**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Configurer les codes nature de transaction

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Types de transaction.**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Autres configurations associées

Avant d’utiliser la fonction d’états intracommunautaires, vous devez configurer certains champs sur les fiches article, immobilisation, client et fournisseur.

#### Fiches article

Pour paramétrer toutes les informations nécessaires liées aux états intracommunautaires sur les fiches article :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Sélectionnez l’article que vous souhaitez configurer.
3. Dans le raccourci **Coûts et validation**, remplissez les champs **Nomenclature produits**, **Unité de mesure supplémentaire** et **Code pays/région d’origine**.
4. Développez le raccourci **Stock** et entrez la valeur décimale dans le champ **Poids net**.

> [!NOTE]
> Vous pouvez utiliser différentes unités de mesure comme unité de mesure supplémentaire. Si ce n’est pas la même que **l’Unité de mesure de base**, vous devez configurer cette unité de mesure sur la page **Unités article**.

#### Fiches immobilisation

Pour paramétrer toutes les informations nécessaires liées aux états intracommunautaires sur les fiches immobilisation :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Immobilisations**, puis choisissez le lien associé.
2. Sélectionnez l’immobilisation à configurer.
3. Développez le raccourci **Intracommunautaire** et remplissez les champs **Nomenclature produit**, **Poids net** et **Unité de mesure supplémentaire**.

> [!NOTE]
> Vous pouvez utiliser différentes unités de mesure comme unité de mesure supplémentaire. Mais quel que **Code Unité de mesure** que vous choisissiez, sa **Quantité** dans les états intracommunautaires sera toujours 1.

#### Fiches fournisseur

Avant d’utiliser un fournisseur dans un état intracommunautaire, vous devez disposer d’un **Code pays/région** et d’un **Numéro d’immatriculation de TVA** pour chacun d’eux, en plus d’informations complémentaires sur leur page **Fiche fournisseur** :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Fournisseurs**, puis choisissez le lien associé.
2. Sélectionnez le fournisseur que vous souhaitez configurer.
3. Sur le raccourci **Intracommunautaire**, vous pouvez définir des valeurs par défaut pour les champs **Type de trans. par défaut**, **Type de trans. par défaut - Retours**, et **Mode de transport par défaut**.
4. Dans le raccourci **Paiements** , dans le champ **Type de partenaire de déclaration d’échanges de biens** , indiquez si le fournisseur est une personne ou une entreprise.

#### Fiches client

Avant d’utiliser un client dans un état intracommunautaire, vous devez disposer d’un **Code pays/région** et d’un **Numéro d’immatriculation de TVA** pour chacun d’eux, en plus d’informations complémentaires sur leur page **Fiche client** :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Sélectionnez le client que vous souhaitez configurer.
3. Sur le raccourci **Intracommunautaire**, vous pouvez définir des valeurs par défaut pour les champs **Type de trans. par défaut**, **Type de trans. par défaut - Retours**, et **Mode de transport par défaut**.
4. Dans le raccourci **Paiements** , dans le champ **Type de partenaire de déclaration d’échanges de biens** , indiquez si le fournisseur est une personne ou une entreprise.

#### Exclure des articles et des immobilisations d’un état intracommunautaire

S’il existe une raison pour qu’un article ou une immobilisation spécifique soit exclu de l’état intracommunautaire, vous devez modifier une option sur sa fiche.

##### Exclure un article de l’état intracommunautaire

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Sélectionnez l’article que vous souhaitez configurer.
3. Dans le raccourci **Coûts et validation**, sélectionnez le champ **Exclure de l’état intracommunautaire**.

##### Exclure une immobilisation d’un état intracommunautaire

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Immobilisations**, puis choisissez le lien associé.
2. Sélectionnez l’immobilisation à configurer.
3. Développez le raccourci **Intracommunautaire**, puis sélectionnez le champ **Exclure de l’état intracommunautaire**.

## Configuration d’états intracommunautaires spécifique au pays

Les exigences intracommunautaires sont similaires dans tous les États membres de l’UE, bien qu’il existe des exceptions importantes. En théorie, les règles devraient être appliquées uniformément dans tous les États membres. Cependant, il existe des différences dans leur application car certains États membres fournissent des directives quant à l’application des principes généraux de la réglementation dans des situations particulières. Par exemple, échantillons commerciaux, retour de marchandises, etc. Ces directives peuvent produire des résultats différents pour diverses situations dans les États membres de l’UE. Pour cette raison, certains pays ont des informations spécifiques supplémentaires distinctes des autres pays. Ils ont également un format de fichier différent pour les états.

### Autriche

La déclaration d’échanges communautaires en Autriche nécessite deux fichiers différents pour les réceptions et les expéditions. Pour vérifier que votre configuration est correcte, procédez comme suit :

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrer les déclarations d’échanges intracommunautaires**, puis choisissez le lien associé.  
2. Dans le raccourci **Génération d’états**, vérifiez si **Fractionner les fichiers réceptions/expéditions** est sélectionné. En lien avec cela, vous trouverez deux **Codes déf. échge données** configurés. Le champ **Fichier(s) zip** est également sélectionné pour s’assurer que les fichiers d’état sont ajoutés au fichier zip.

Le processus de travail avec les états intracomm. est le même que la fonctionnalité globale.

<!-- ### Belgium-->

### République tchèque

La nouvelle expérience d’états intracomm. pour la République tchèque sera disponible à partir de la 1ère vague de lancement de 2023. En attendant, vous pouvez continuer à utiliser la fonctionnalité **Feuille intracomm.**.

### Finlande

En Finlande, il y a quelques étapes supplémentaires pour configurer les états intracomm. La déclaration d’échanges communautaires en Finlande nécessite deux fichiers différents pour les réceptions et les expéditions. En lien avec cela, vous trouverez deux **Codes déf. échge données** configurés.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrer les déclarations d’échanges intracommunautaires**, puis choisissez le lien associé.  
2. Sur la page **Paramètres état échanges communautaires**, sur le raccourci **Configuration des fichiers**, renseignez les champs comme indiqué dans le tableau suivant :

    |Champ|Description|  
    |------------------------------------|---------------------------------------|
    | **Code personnalisé**|Spécifie un code personnalisé pour les informations de configuration du fichier d’échanges intracomm.. |
    | **N° de série de l’entreprise**|Spécifie un numéro de série de l’entreprise pour les informations de configuration du fichier d’échanges intracomm.. |

3. Dans le raccourci **Génération d’états**, vérifiez si **Fractionner les fichiers réceptions/expéditions** est sélectionné.

Le processus de travail avec les états intracomm. est le même que la fonctionnalité globale.

<!-- ### Germany-->

### Italie

La nouvelle expérience des états intracomm. pour l’Italie sera disponible à partir de février 2023. En attendant, vous pouvez continuer à utiliser la fonctionnalité **Feuille intracomm.**.

<!-- ### France-->

### Suède

La déclaration d’échanges communautaires en Suède nécessite deux fichiers différents pour les réceptions et les expéditions. Pour vérifier que votre configuration est correcte, procédez comme suit :

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrer les déclarations d’échanges intracommunautaires**, puis choisissez le lien associé.  
2. Dans le raccourci **Génération d’états**, vérifiez si **Fractionner les fichiers réceptions/expéditions** est sélectionné. En lien avec cela, vous trouverez deux **Codes déf. échge données** configurés.

Le processus de travail avec les états intracomm. est le même que dans la fonctionnalité globale.

<!-- ### United Kingdom-->

## Voir la formation associée sur [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## Voir aussi

[Génération d’état intracommunautaire dans Business Central](finance-how-report-intrastat.md)  
[Gestion financière](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
