---
title: Utilisation des présentations Excel
description: Découvrez comment créer et modifier des présentations d’état créées à l’aide d’Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 11/10/2022
ms.author: jswymer
---
# <a name="working-with-microsoft-excel-layouts"></a><a name="working-with-microsoft-excel-layouts"></a>Utilisation des présentations Microsoft Excel

Les présentations d’état de Microsoft Excel sont basées sur les classeurs Excel (fichiers .xlsx). Elles vous permettent de créer des états en utilisant des fonctionnalités Excel familières pour résumer, analyser et présenter des données avec des outils comme des formules, des tableaux croisés dynamiques et des graphiques croisés dynamiques, etc.

![Affiche un exemple de présentation Excel.](media/excel-layout-2.png)

Cet article explique certaines des choses les plus importantes que vous devez savoir pour démarrer avec les présentations Excel.

## <a name="why-use-excel-layouts"></a><a name="why-use-excel-layouts"></a>Pourquoi utiliser des présentations Excel ?

Avantages de l’utilisation des mises en page Excel :

- Vous pouvez créer des états interactifs à l’aide de visualisations telles que des segments.
- Vous pouvez afficher les données brutes de l’ensemble de données de rapport pour vous aider à comprendre comment il fonctionne et d’où proviennent les données sur les visuels.
- Vous pouvez utiliser les fonctionnalités Microsoft Office intégrées pour effectuer un post-traitement sur les rapports rendus, comme :
  - [Protéger les feuilles de travail](https://support.microsoft.com/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Appliquer des étiquettes de sensibilité](https://support.microsoft.com/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Ajouter des commentaires et des notes](https://support.microsoft.com/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Faire des prévisions et des analyses](https://support.microsoft.com/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4)
- Vous pouvez utiliser les compléments installés et les intégrations d’applications, comme les flux Power Automate ou OneDrive.

## <a name="get-started"></a><a name="get-started"></a>Mise en route

Il existe essentiellement deux tâches impliquées dans la configuration d’une présentation Excel sur un état :

1. Créer le nouveau fichier de présentation Excel.
2. Ajouter la nouvelle présentation au rapport.

## <a name="task-1-create-the-excel-layout-file"></a><a name="task-1-create-the-excel-layout-file"></a>Tâche 1 : Créer le fichier de présentation Excel

Il existe trois façons de créer un fichier de présentation Excel pour un rapport, comme expliqué dans cette section.

### [À partir d’un rapport quelconque](#tab/any-report)

Procédez comme suit pour créer une présentation Excel à partir de n’importe quel état, quel que soit le type de présentation actuel. La présentation Excel contiendra la feuille **Données** et le tableau requis, une feuille **Métadonnées de l’état**, et rien d’autre.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Sur la page **Présentations d’état**, sélectionnez une présentation pour l’état, puis choisissez l’action **Exécuter état**.
3. Sur la page de demande d’état, sélectionnez **Envoyer à** > **Document Microsoft Excel (données uniquement)** > **OK**.

   Cette étape télécharge un classeur Excel contenant le jeu de données de l’état.
4. Ouvrez le fichier Excel téléchargé, effectuez vos modifications, puis enregistrez le fichier.

### [À partir d’une autre présentation Excel sur un état](#tab/other-layout)

S’il existe déjà une présentation Excel pour un état, utilisez celle existante comme point de départ. Il existe deux approches pour obtenir une copie de la présentation. Vous pouvez exporter la présentation existante à partir de la page **Présentations d’état** ou télécharger la présentation à partir de la page de demande d’état. Les deux méthodes téléchargent un fichier de présentation Excel qui inclut toutes les feuilles du fichier existant. La différence est qu’à partir de la page de demande, la présentation inclura les données réelles. (Les données ne sont pas obligatoires, mais elles aident lors de la conception de la présentation.)

#### <a name="approach-1-export-the-layout-from-the-report-layouts-page"></a><a name="approach-1-export-the-layout-from-the-report-layouts-page"></a>Approche 1 : Exporter la présentation à partir de la page **Présentations d’état**

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Sélectionnez la mise en page Excel dans la liste, puis choisissez l’action **Exporter présentation** en haut de la page.
3. Ouvrez le fichier Excel, effectuez vos modifications, puis enregistrez le fichier.

#### <a name="approach-2-download-the-layout-from-the-reports-request-page"></a><a name="approach-2-download-the-layout-from-the-reports-request-page"></a>Approche 2 : Téléchargez la présentation à partir de la page de demande de l’état

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Sur la page **Présentations d’état**, sélectionnez une présentation pour l’état, puis choisissez l’action **Exécuter état**.
3. Sur la page de demande de l’état, sélectionnez **Télécharger**.
4. Ouvrez le fichier Excel, effectuez vos modifications, puis enregistrez le fichier.

### [À partir du code AL](#tab/from-code)

Il s’agit de la méthode la plus avancée pour créer une présentation d’état Excel. Elle nécessite une connaissance du code AL, elle cible donc les programmeurs. Avec cette approche, les mises en page Excel, dans ce cas, font partie d’un package d’extension que vous installez. Pour plus d’informations, voir [Création d’une présentation état Excel](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) dans l′aide dédiée aux développeurs et aux professionnels de l’informatique.

---

## <a name="task-2-add-the-excel-layout-to-the-report"></a><a name="task-2-add-the-excel-layout-to-the-report"></a>Tâche 2: Ajouter la présentation Excel à l’état

Une fois que vous avez le fichier de présentation Excel, la tâche suivante consiste à l’ajouter en tant que nouvelle présentation pour l’état.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Sélectionnez **Nouvelle présentation**.
3. Définissez **ID état** sur *État*.
4. Entrez un nom dans **Nom présentation**.
5. Définissez **Options de format** sur **Excel**.
6. Sélectionnez **OK**, puis effectuez une des étapes suivantes pour télécharger le fichier pour le rapport :

   [!INCLUDE[file-upload](includes/file-upload.md)]

   Le fichier sélectionné est chargé dans la présentation et la page **Présentations d’état** s’ouvre.
8. Si vous voulez voir à quoi ressemble l’état avec la nouvelle présentation, sélectionnez la présentation dans la liste, puis sélectionnez **Exécuter état**.

<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet must include a table named **Data**.

**Data** table
  - The **Data** sheet must include a table named **Data**.
  - The table must have at least one column and can only include columns that are also in the report dataset.
  - The table must start in the first cell **A1** of the **Data** sheet.

3. Report metadata 
-->

## <a name="understanding-excel-layouts"></a><a name="understanding-excel-layouts"></a>Comprendre les présentations Excel

Il y a quelques précautions à prendre lorsque vous commencez à créer ou à modifier des présentations Excel. Chaque présentation Excel doit inclure deux éléments : une feuille de **Données** et une table de **Données**. Ces éléments forment la base de la présentation car elles définissent les données métier de Business Central avec lesquelles vous pouvez travailler. On peut comparer la feuille de **Données** à un type de contrat entre la présentation et les données métier. Vous devez utiliser ces données comme source de calculs et de visualisations à présenter sur d’autres feuilles.

Il existe certaines exigences spécifiques à la structure du classeur Excel. Si les conditions ne sont pas remplies, vous aurez des problèmes lors de l’utilisation de la présentation. Le diagramme et le tableau suivants décrivent les éléments d’une présentation Excel et les exigences.

[![Affiche les différents éléments d’une présentation Excel.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Non.|Élément|Désignation|Obligatoire|
|---|-------|----|---|
|0|Feuille de **Données**|<ul><li>Doit avoir le nom **Données**.</li><li>Ne peut inclure qu’une seule table, et la table doit être nommée **Données**.</li></ul>|![Est obligatoire](media/check.png) | 
|2|Table de **Données**|<ul><li>Doit avoir le nom **Données**.</li><li>Doit avoir au moins une colonne.</li><li>Ne peut inclure que les colonnes qui se trouvent dans le jeu de données de l’état.</li><li>Doit commencer dans la première cellule **A1** de la feuille de **Données**.</li></ul>|![Est obligatoire](media/check.png)|
|3|Feuilles de présentation|<ul><li>Utilisées pour présenter des données.</li><li>Les données proviennent de la feuille de **Données**. </li></ul>||
|4|Feuille de **Métadonnées de l’état**|<ul><li>Inclus automatiquement si la présentation a été créée en exportant un autre état au format Excel.</li><li>Contient des informations générales sur l’état.</li><li>Peut être supprimée.</li></ul>|

En résumé, voici ce que vous devriez et ne devriez pas faire sur la feuille **Données** :

- Ne changez pas le nom de la feuille de **Données**, de la table de **Données** ou des colonnes.
- Vous pouvez supprimer ou masquer des colonnes.
- N’ajoutez aucune colonne à moins qu’elle ne soit incluse dans l’ensemble de données de l’état.
- Vous pouvez placer les feuilles dans n’importe quel ordre, avec la feuille **Données** en premier ou en dernier.

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Gestion des présentations d’état](ui-manage-report-layouts.md)  
[Modifier la présentation actuelle de l’état](ui-how-change-layout-currently-used-report.md)  
[Importer et exporter une présentation d’état ou de document personnalisée](ui-how-import-and-export-report-layout.md)  
[Utilisation des états, des traitements par lots et des ports XML](ui-work-report.md)  
[Préparer Financial Reporting avec des données financières et des catégories de compte](bi-how-work-account-schedule.md)  
[Veille économique](bi.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analyse des données de rapport avec Excel](report-analyze-excel.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
