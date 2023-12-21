---
title: Analyser les données dans les pages de liste et le requêtes à l’aide du mode d’analyse des données
description: "Découvrez comment utiliser le mode d’analyse des données dans Business\_Central pour analyser les données."
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/05/2023
ms.custom: bap-template
ms.service: dynamics365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-list-page-and-query-data-using-data-analysis-mode"></a>Analyser les données de page de liste et de requête à l’aide du mode d’analyse des données

> **S’APPLIQUE À :** version préliminaire publique dans la 1ère vague de lancement 2023 de Business Central ou ultérieure pour l’analyse des pages de liste ; généralement disponible dans la 2è vague de lancement 2023 de Business Central ou ultérieure pour l’analyse des données des pages de liste et des requêtes.

Dans cet article, vous apprenez à analyser les données des pages de liste et des requêtes à l’aide du *mode d’analyse des données*. Le mode d’analyse des données vous permet d’analyser les données directement à partir de la page, sans avoir à exécuter un rapport ou à changer d’application comme Excel. Il fournit un moyen interactif et polyvalent de calculer, résumer et examiner les données. Plutôt que d’exécuter des rapports à l’aide d’options et de filtres différents, vous pouvez ajouter plusieurs onglets qui représentent différentes tâches ou vues sur les données. Parmi des exemples figurent « Mes clients », « Éléments de suivi », « Fournisseurs récemment ajoutés », « Statistiques des ventes » ou toute autre vue que vous pouvez imaginer.

> [!TIP]
> Une bonne chose à propos du mode d’analyse des données est qu’il ne modifie pas les données sous-jacentes de la page de liste ou de la requête, ni la mise en page de la page ou de la requête lorsqu’elle n’est pas en mode d’analyse des données. Ainsi la meilleure façon d’apprendre ce que vous pouvez faire en mode d’analyse de données est d’essayer des choses.

## <a name="prerequisites"></a>Conditions préalables

- Si vous utilisez Business Central version 22, le mode d’analyse des données est en version préliminaire. Un administrateur doit donc l’activer avant que vous puissiez l’utiliser. Pour l’activer, accédez à la page **Gestion des fonctionnalités** et activez **Mise à jour des fonctionnalités : mode Analyse, analysez rapidement les données directement dans Business Central**. [En savoir plus sur la gestion des fonctionnalités](/dynamics365/business-central/dev-itpro/administration/feature-management).
- Dans la version 23 et les versions ultérieures, votre compte doit disposer de l’ensemble d’autorisations **ANALYSE DES DONNÉES - EXEC** ou inclure l’autorisation d’exécution sur l’objet système **9640 Autoriser le mode d’analyse des données**. En tant qu’administrateur, vous pouvez exclure ces autorisations pour les utilisateurs qui ne doivent pas avoir accès au mode d’analyse.

> [!NOTE]
> Vous remarquerez peut-être que certaines pages de liste n’incluent pas le bouton bascule **Analyser** pour passer en mode d’analyse. La raison en est que les développeurs peuvent désactiver le mode d’analyse sur des pages spécifiques en utilisant la [propriété AnalysisModeEnabled](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) dans AL.

## <a name="get-started"></a>Mise en route

1. Ouvrez la page de liste ou la requête.

   Par exemple, pour utiliser la page **Écritures comptables client**, sélectionnez l’icone en forme de ![Loupe qui ouvre la fenêtre de recherche](media/ui-search/search_small.png) (<kbd>Alt</kbd>+<kbd>Q</kbd>), saisissez *écritures comptables client*, et choisissez le lien associé. 

2. Dans la barre d’action en haut de la page, activez le commutateur à bascule **Analyser**.

    Le mode d’analyse des données ouvre les données dans une expérience optimisée pour l’analyse des données.  En mode d’analyse de données, la barre d’action normale est remplacée par une barre de mode d’analyse de données spéciale. La figure suivante illustre les différentes zones d’une page en mode analyse de données.

   [![Affiche une vue d’ensemble d’une page sur le mode d’analyse des données](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Chaque domaine est expliqué dans les sections qui suivent.

3. Utilisez les différentes zones pour manipuler, résumer et analyser les données. Reportez-vous aux sections qui suivent pour plus d’informations.

4. Lorsque vous souhaitez quitter le mode d’analyse, désactivez l’interrupteur à bascule **Analyser**.

   Les onglets d’analyse que vous avez ajoutés restent jusqu’à ce que vous les supprimiez. Ainsi, si vous revenez au mode d’analyse des données, vous les voyez exactement telles que vous les avez laissées.

> [!NOTE]
> Les données affichées en mode analyse sont contrôlées par les filtres ou les vues définis sur la page de liste. Cela vous permet de pré-filtrer les données avant d’entrer en mode d’analyse.

## <a name="work-with-data-analysis-mode"></a>Utiliser le mode d’analyse des données

Dans le mode d’analyse des données, la page est divisée en deux zones :

- La zone principale, qui comprend la zone de données (1), la barre de résumé (2) et la barre d’onglets (5)
- La zone de manipulation des données, qui se compose de deux volets : les colonnes (3) et les filtres d’analyse (4).

### <a name="data-area-1"></a>Zone de données (1)

La zone de données est l’endroit où les lignes et les colonnes de la page de liste ou de la requête sont affichées et où les données sont résumées. La zone de données offre un moyen polyvalent de contrôler la disposition des colonnes et un moyen rapide d’obtenir un résumé des données. Pour les colonnes contenant des valeurs numériques, la somme de toutes les valeurs de la colonne s’affiche dans une dernière ligne, sauf si vous avez défini des groupes de lignes. Dans ce cas, les sommes s’affichent comme un sous-total pour les groupes.  

![Affiche une vue d’ensemble de la zone de données sur une page dans le mode d’analyse des données](media/analysis-mode-data-area.png)

- Pour déplacer une colonne, sélectionnez-la et faites-la glisser là où elle a le plus de sens dans votre analyse.
- Cliquez avec le bouton droit sur la colonne ou survolez-la et sélectionnez l’icône de menu ![Affiche l’icône sur une colonne en mode analyse de données qui ouvre un menu d’actions](media/analysis-mode-column-menu-icon.png) pour accéder à plusieurs actions que vous pouvez effectuer sur les colonnes. Par exemple :

  - Pour épingler une colonne à gauche ou à droite de la zone de données afin qu’elle ne sorte pas de l’écran lorsque vous faites défiler, sélectionnez ![Affiche l’icône sur une colonne en mode analyse de données qui ouvre un menu d‘actions](media/analysis-mode-column-menu-icon.png) > **Épingler la colonne** > **Épingler à gauche** la partie colonne.
  - Définissez des filtres de données directement sur la définition de colonne au lieu d’aller dans les volets **Filtres d’analyse**. Vous pouvez toujours consulter les détails des données associées et pour chaque ligne, et ouvrir la fiche pour en savoir plus sur une entité donnée.
- Utilisez la zone de données pour interagir avec les données. Pour les colonnes qui contiennent des valeurs numériques sommables, vous pouvez obtenir des statistiques descriptives sur un ensemble de champs en les marquant. Les statistiques apparaissent dans la barre d’état (2) en bas de la page.
- Exportez les données au format Excel ou csv. Faites un clic droit sur la zone de données ou sur une sélection de cellules à exporter.

### <a name="summary-bar-2"></a>Barre récapitulative (2)

La barre de résumé se trouve en bas de la page et affiche des statistiques sur les données de la page de liste ou de la requête. Lorsque vous interagissez avec des colonnes dont les valeurs peuvent être additionnées, comme la sélection de plusieurs lignes dans une colonne qui affiche des montants, les données sont mises à jour.

![Affiche une vue d’ensemble d’une barre récapitulative sur le mode d’analyse des données](media/analysis-mode-totals-row.png)

La table suivante décrit les différents nombres affichés dans la zone des totaux :

|Nombre|Description|
|-|-|
|Lignes|Le nombre de lignes sélectionnées par rapport au nombre total de lignes disponibles. |
|Nombre total de lignes|Le nombre de lignes dans la liste ou la requête non filtrée.|
|Filtré|Le nombre de lignes affichées suite aux filtres appliqués à la liste ou à la requête.|
|Moyenne|La valeur moyenne dans tous les champs sommables sélectionnés.|
|Nombre|Le nombre de lignes sélectionnées.|
|Min|La valeur minimale dans tous les champs sommables sélectionnés.|
|Max|La valeur maximale dans tous les champs sommables sélectionnés.|
|Somme|La somme totale de toutes les valeurs dans les champs sommables sélectionnés.|

### <a name="columns-3"></a>Colonnes (3)

Les **Colonnes** est l’un des deux volets qui fonctionnent ensemble pour définir votre analyse. L’autre zone est le volet **Filtres d’analyse**. Le volet **Colonnes** est utilisé pour résumer les données. Utilisez le volet **Colonnes** pour définir les colonnes à inclure dans l’analyse.

![Affiche une vue d’ensemble du volet de colonnes dans le mode d’analyse des données](media/analysis-mode-columns-2.png)

|Dépts destination/provenance|Description|
|-|-|
|Rechercher/cocher ou effacer toutes les cases|Recherchez des colonnes. Activez cette case à cocher pour sélectionner/effacer toutes les colonnes.|
|Cases à cocher|Cette zone comprend une case à cocher pour chaque champ de la table source de la liste ou de la requête. Utilisez cette zone pour modifier les colonnes affichées. Cochez une case pour afficher la colonne du champ sur la page ; décochez la case pour masquer la colonne. |
|Groupes de lignes|Utilisez cette zone pour regrouper et additionner les données par un ou plusieurs champs. Vous ne pouvez inclure que des champs non numériques, tels que des champs de texte, de date et d’heure. Les groupes de lignes sont souvent utilisés en mode pivot.|
|Valeurs|Utilisez cette zone pour spécifier les champs pour lesquels vous souhaitez un total. Vous ne pouvez inclure que des champs contenant des nombres pouvant être additionnés ; par exemple, pas les champs de texte, de date ou d’heure.|

Pour déplacer un champ d’une zone à une autre, sélectionnez l’icône de saisie ![Affiche une vue d’ensemble d’une page sur le mode d’analyse](media/column-grab-icon.png) en regard de la colonne dans la liste et faites glisser dans la zone cible. Vous ne pouvez pas déplacer un champ dans une zone où cela n’est pas autorisé.

### <a name="analysis-filters-4"></a>Filtres d’analyse (4)

Le volet **Filtres d’analyse** vous permet de définir d’autres filtres de données sur les colonnes pour limiter les entrées dans la liste. Définissez des filtres sur les colonnes pour limiter les entrées de la liste et les sommes suivantes aux seules entrées qui vous intéressent en fonction des critères que vous définissez. Par exemple, supposons que vous ne vous intéressiez qu’aux données d’un client spécifique ou aux commandes client qui dépassent un montant spécifique. Pour définir un filtre, sélectionnez la colonne, choisissez l’opération de comparaison dans la liste (comme **Égal à** ou **Commence par**), puis entrez la valeur.

![Affiche une vue d’ensemble du volet de filtres dans le mode d’analyse](media/analysis-mode-filters.png)

> [!NOTE]
> Les filtres supplémentaires s’appliquent uniquement à l’onglet d’analyse en cours. Cela vous permet de définir exactement les filtres de données supplémentaires qui sont nécessaires pour une analyse spécifique.

### <a name="tabs-5"></a>Onglets (5)

La zone des onglets en haut vous permet de créer différentes configurations (colonnes et filtres d’analyse) sur des onglets séparés, où vous pouvez manipuler les données sur les onglets indépendamment les unes des autres. Il y a toujours au moins un onglet, appelé **Analyse 1** par défaut. L’ajout d’onglets supplémentaires est utile pour enregistrer les configurations d’analyse fréquemment utilisées sur un jeu de données. Par exemple, vous pouvez avoir des onglets pour analyser les données en mode pivot et d’autres onglets qui filtrent sur un sous-ensemble de lignes. Certains onglets peuvent afficher une vue détaillée avec de nombreuses colonnes, tandis que d’autres n’affichent que quelques colonnes clés.

Voici quelques conseils sur l’utilisation de plusieurs onglets d’analyse :

- Pour ajouter un nouvel onglet, sélectionnez le grand signe **+** en regard du dernier onglet d’analyse.
- Sélectionnez la flèche vers le bas sur un onglet pour accéder à une liste d’actions que vous pouvez effectuer sur un onglet, comme renommer, dupliquer, supprimer et déplacer.

   - **Supprimer** supprime l’onglet actuellement ouvert. **Supprimer tout** supprime tous les onglets que vous avez ajoutés, à l’exception de l’onglet **Analyse 1** par défaut.
- Vous ne pouvez pas supprimer complètement l’**Analyse 1**, mais vous pouvez la renommer en utilisant l’action **Renommer** et effacer les modifications que vous avez apportées en utilisant **Supprimer** ou **Supprimer tout**.  

- Les onglets d’analyse que vous avez ajoutés et restent configurés jusqu’à ce que vous les supprimiez. Ainsi, si vous revenez au mode d’analyse des données, vous les voyez exactement telles que vous les avez laissées.

   > [!TIP]
   > Les onglets que vous configurez ne sont visibles que par vous. Les autres utilisateurs ne verront que les onglets qu’ils ont configurés.
- Vous pouvez copier les onglets d’analyse. La copie peut être utile si vous souhaitez expérimenter la modification d’un onglet sans modifier l’original, ou si vous souhaitez créer différentes variantes de la même analyse.


## <a name="date-hierarchies"></a>Hiérarchies de dates

En mode analyse, les champs de date de l’ensemble de données sont générés dans une hiérarchie Année-Trimestre-Mois de trois champs distincts. Cette hiérarchie est basée sur le calendrier normal, et non sur les calendriers fiscaux définis dans Business Central.

Les champs supplémentaires sont nommés _\<field name\> Année_, _\<field name\> Trimestre_, et _\<field name\> Mois_. Par exemple, si l’ensemble de données comprend un champ appelé _Date de publication_, alors la hiérarchie de dates correspondante est constituée de champs appelés _Année de la date de publication_, _Trimestre de la date de publication_, et _Mois de la date de publication_.

> [!NOTE]
> La hiérarchie des dates ne s’applique actuellement qu’aux champs de type date, pas aux champs de type datetime.

## <a name="pivot-mode"></a>Mode Pivot

Vous pouvez utiliser le mode pivot pour analyser une grande quantité de données numériques, en sous-totalisant les données par catégories et sous-catégories. Le mode pivot ressemble aux [tableaux croisés dynamiques dans Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Pour activer et désactiver le mode pivot, faites glisser le commutateur **Mode pivot** dans le volet **Colonnes** (3). Lorsque vous activez le mode pivot, la zone **Étiquettes de colonne** s’affiche dans le volet. Utilisez la zone **Étiquettes de colonne** pour regrouper les totaux des lignes en catégories. Les champs que vous ajoutez à la zone **Étiquettes de colonne** s’affichent sous forme de colonnes dans la zone de données (1).

Créer l’analyse des données en mode pivot implique de déplacer les champs dans les trois zones : **Groupes de lignes**, **Étiquettes de colonnes**, et **Valeurs**. La figure suivante illustre où les champs correspondent à la zone de données (1), où `sum` représente les données calculées, et éventuellement **Valeurs**.

<table>
<tr><th></th><th>Étiquette de la colonne</th><th></th><th>Étiquette de la colonne</th><th></th></tr>
<tr><th>Groupe de lignes</th><th>Valeur</th><th>Valeur</th><th>Valeur</th><th>Valeur</th></tr>
<tr><td>ligne</td><td>somme</td><td>somme</td><td>somme</td><td>somme</td></tr>
<tr><td>ligne</td><td>somme</td><td>somme</td><td>somme</td><td>somme</td></tr>
<tr><td>ligne</td><td>somme</td><td>somme</td><td>somme</td><td>somme</td></tr>
<tr><td>ligne</td><td>somme</td><td>somme</td><td>somme</td><td>somme</td></tr>
</table>

> [!TIP]
> Les colonnes qui n’ont que quelques valeurs possibles sont les meilleures candidates à utiliser dans la colonne **Valeurs**.


## <a name="analyze-large-amounts-of-data"></a>Analyser de grandes quantités de données

Si l’ensemble de données que vous souhaitez analyser dépasse 100 000 lignes, nous vous suggérons de passer en mode d’analyse qui est optimisé pour les grands ensembles de données. Il existe actuellement deux limitations si vous passez à ce mode : 

- Le formatage des champs des quatre types de données suivants peut changer : 

   - devise 
   - décimales (toujours affichées avec deux décimales) 
   - dates (toujours affichées au format AAAA-MM-JJ)
   - fuseaux horaires
- Les champs utilisés en mode dynamique et ajoutés aux étiquettes de colonnes doivent avoir un faible nombre de valeurs distinctes.

   Si vous activez le mode dynamique et faites glisser un champ dans la zone **Étiquettes de colonne**, où les données sous-jacentes de ce champ comportent trop de valeurs distinctes, l’onglet du navigateur peut ne plus répondre et finir par se fermer, vous obligeant à recommencer dans une nouvelle session. Dans ce cas, n’activez pas le mode dynamique sur ce champ ou définissez un filtre sur le champ avant de l’ajouter à la zone **Étiquettes de colonne**.

## <a name="share-data-analysis"></a>Partager l’analyse des données

Après avoir préparé une analyse dans un onglet, vous pouvez la partager sous forme de lien avec vos collègues et d’autres personnes de votre organisation directement à partir du client. Seuls les destinataires disposant de l’autorisation d’accès à l’entreprise et aux données peuvent utiliser le lien.

1. Dans l’onglet Analyse, sélectionnez la pointe de la flèche vers le bas, puis sélectionnez **Copier le lien**.

   ![Affiche l’action pour copier une analyse](media/copy-analysis.svg)

   La boîte de dialogue **Lien vers \<tab name\>** s’ouvre.

1. Par défaut, l’analyse que vous partagez est liée à la page ou à la requête dans la société dans laquelle vous travaillez actuellement, ce qui est indiqué par `company=<company_name>` dans le champ URL en regard du bouton **Copier**. Si vous souhaitez envoyer un lien vers une analyse qui n’est pas associée à une société spécifique, définissez le champ **Société** sur **Ne pas lier à une société spécifique**.

   ![Affiche la boîte de dialogue Copier le lien pour un onglet d’analyse](media/analysis-link-copied.svg)

1. Sélectionnez **Copier**.

1. Collez le lien dans le média de communication de votre choix, par exemple Word, Outlook, Teams, OneNote, etc. 

2. Une fois reçus, les destinataires peuvent ensuite sélectionner le lien et ouvrir l’analyse pour la page ou la requête dans Business Central. Ils sont invités à spécifier un nom pour le nouvel onglet d’analyse créé.  

## <a name="limitations-in-2023-release-wave-1-preview"></a>Limitations de la 1ère vague de lancement 2023 (version préliminaire)

La version préliminaire publique de cette fonctionnalité présente les limitations suivantes :

- La vue du mode d’analyse a actuellement une limite de 100 000 lignes. Si vous dépassez cette limite, vous recevez un message vous en informant. Pour contourner cette limitation, définissez des filtres sur la page avant de passer en mode d’analyse, si cela est possible. Par exemple, vous voulez peut-être analyser un certain groupe de clients ou vous voulez uniquement les données de l’année en cours. Vous pouvez également choisir une vue prédéfinie si cela convient à votre analyse.
- La fonctionnalité de partage de l’analyse des données n’est pas disponible.
- La possibilité d’enregistrer les options d’analyse de données préférées sur les pages de liste et d’enregistrer les menus d’analyse par onglet d’analyse n’est pas actuellement disponible.

## <a name="see-also"></a>Voir aussi

[Analyse de données ad hoc](reports-adhoc-analysis.md)  
[Affichage et modification dans Excel](across-work-with-excel.md)  
