---
title: Bien démarrer avec la création de présentations
description: 'Découvrez comment créer des présentations pour personnaliser l’apparence d’un état lorsqu’il est consulté, imprimé ou enregistré.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/23/2022
ms.author: jswymer
---
# <a name="get-started-creating-report-layouts" />Bien démarrer avec la création de présentations d’état

Business Central est fourni avec de nombreuses présentations intégrées que vous pouvez utiliser dans vos états. Il est possible que d’autres présentations aient été ajoutées avec d’autres extensions. Mais il est également possible de créer vos propres états à partir de zéro ou à partir d’une présentation existante.

> [!IMPORTANT]
> Vous pouvez également utiliser des présentations d’état pour ajouter du contenu aux messages électroniques. Par exemple, les présentations d’état peuvent vous faire gagner du temps et contribuer à assurer la cohérence, car elles réutilisent le même contenu lorsque vous communiquez avec vos clients. Pour utiliser des présentations d’état personnalisées avec le courrier électronique, le type de fichier de la mise en page doit être Word. Vous ne pouvez pas utiliser le type de fichier RDLC. Pour plus d’informations, voir [Configurer des textes et des mises en page d’e-mail réutilisables](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="overview" />Aperçu

Lorsque vous travaillez avec des présentations d’état, il est utile de considérer la présentation comme un fichier importé et affecté à un rapport. Quel que soit le type de présentation, la façon dont vous gérez les présentations dans Business Central est fondamentalement la même. En général, vous allez travailler à partir de la page **Présentations d’état**. La principale différence réside dans la façon dont vous concevez la présentation, qui est effectuée à l’aide du logiciel d’application sur lequel la présentation est construite, comme Word, Excel ou SQL Server Report Builder.

Gardez ce concept en tête. Il existe essentiellement trois ou quatre tâches impliquées dans la configuration d’une présentation sur un état :

1. Décider du type de présentation.
2. Exporter une copie d’une présentation existante à utiliser comme point de départ.
3. Apporter des modifications au fichier de présentation dans l’application appropriée.
4. Ajouter le nouveau fichier de présentation au rapport.

> [!IMPORTANT]
> Vous ne pouvez pas modifier ou remplacer une présentation d’extension, qui est une présentation provenant d’une extension. Vous pouvez uniquement modifier ou remplacer les dispositions définies par l’utilisateur. Sur la page **Présentations d’état**, vous pouvez savoir si la présentation est une présentation d’extension ou une présentation définie par l’utilisateur en regardant la colonne **Extension**. Une présentation d’extension affichera des informations sur l’extension source dans la colonne. La colonne **Extension** sera vide pour une présentation définie par l’utilisateur.
>
> Pour en savoir plus sur la différence entre les présentations d’extension et les présentations définies par l’utilisateur, voir [Source de la présentation](ui-manage-report-layouts.md#layout-sources).

## <a name="get-started" />Démarrer

Les tâches varieront selon le cas. Utilisez le tableau suivant pour vous aider à démarrer.

|Ce que vous voulez faire|Voir...|
|-----------------------|------|
|Déterminer quel est le meilleur type de présentation à utiliser dans mon cas|[Décider du type de présentation souhaité](#decide)|
|Créez une nouvelle présentation pour un état basé sur une présentation existante, en conservant la présentation existante telle quelle.|[Créer une présentation](#create)|
|Apporter des modifications à une présentation existante utilisée dans un état|[Modifier une présentation](#modify)|
|J’ai une nouvelle version d’un fichier de présentation pour un état. Je veux remplacer le fichier de présentation existant.|[Remplacer une présentation](#replace)|
|Basculer la présentation actuelle utilisée par un état vers une autre présentation|[Définition de la présentation utilisée par un état](ui-set-report-layout.md)|
|Modifier le nom et la description d’une présentation|[Renommer une présentation](#rename)|

## <a name="a-namedecideadecide-what-type-of-layout-you-want" /><a name="decide"></a>Décider du type de présentation souhaité

La première chose à faire lors de la création d’une présentation est de décider de la [présentation](ui-manage-report-layouts.md#layout-types) que vous voulez. Vous pouvez choisir entre Word, Excel ou RDLC. Le type de présentation dépendra de l’aspect que vous souhaitez donner à l’état généré. De plus, cela dépend de votre connaissance des logiciels d’application pour créer les présentations, comme Word, Excel et SQL Server Report Builder.

<!--
* The process for setting up Word, Excel, and RDLC layouts on reports is the same. The main difference is in the way you modify the layouts. Excel and Word layouts are typically easier to create and modify than RDLC layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.-->

* Les présentations Excel sont généralement les plus faciles à créer et à modifier car les fonctionnalités de synthèse des données, d’ajout de graphiques et de style sont des fonctionnalités Excel courantes.

* Tous les rapports et documents ne disposent pas d’un jeu de données optimisé pour une utilisation avec une présentation Excel. Par exemple, les agrégations et les calculs complexes fonctionnent mieux avec les présentations RDLC ou Word. Il en est de même pour les documents.

* Si vous ne faites que des changements de style comme le type de police, la taille et les couleurs, une présentation Word est également un bon choix.

* L’ajout de champs de données ou la réorganisation des champs de données dans Word ou RDLC est plus avancé qu’avec Excel.

* Les présentations Word et RDLC sont utiles pour les états qui seront éventuellement imprimés.  

* Les concepts généraux pour les présentations Word et RDLC sont similaires. Cependant, la conception de chaque type présente certaines fonctionnalités qui affectent la manière dont l’état généré s’affiche dans [!INCLUDE[prod_short](includes/prod_short.md)]. Le même rapport peut sembler différent selon que vous utilisez une présentation Word ou une présentation RDLC.

## <a name="a-namecreateacreate-a-new-layout" /><a name="create"></a>Créer une présentation

Il existe deux manières de créer une nouvelle présentation à partir d’une présentation existante. Une façon consiste à enregistrer la présentation existante dans une copie. L’autre méthode consiste à exporter la présentation existante.

## [Copie](#tab/copy)

La copie est un moyen rapide de créer une nouvelle présentation identique à une présentation existante. Une fois que vous avez la copie, vous apporterez des modifications en exportant la présentation. 

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Sélectionnez la présentation que vous souhaitez copier, puis choisissez l’action **Modifier informations**.

    Si vous avez sélectionné une présentation d’extension, vous êtes invité à modifier une copie. Sélectionnez **Oui** pour continuer.

    > [!TIP]
    > Pour vous aider à trouver la présentation, utilisez la case **Rechercher**, le volet **Filtrer** et le tri des colonnes.
3. Modifiez le **Nom de la présentation**.
4. Définissez le bouton bascule **Enregistrer les modifications apportées à une copie** sur **Activé**, puis cliquez sur **OK**

   La nouvelle présentation s’affiche dans la page **Présentations d’état**.
5. Si vous souhaitez apporter des modifications à la nouvelle présentation, consultez [Modifier une présentation existante](#modify).

### [Exportation/Importation](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Sélectionnez la présentation que vous souhaitez copier, puis choisissez l’action **Exporter présentation**.

   Le fichier de présentation sera téléchargé sur votre appareil. 

    > [!TIP]
    > Pour vous aider à trouver la présentation, utilisez la case **Rechercher**, le volet **Filtrer** et le tri des colonnes.

3. Ouvrez le fichier de présentation dans l’application appropriée, telle que Word (pour un fichier .docx) ou Excel (pour un fichier .xlsx).

   Pour plus d’informations, voir :

   * [Utiliser des présentations Word](ui-how-add-fields-word-report-layout.md)
   * [Utilisation des présentations Excel](ui-excel-report-layouts.md)
   * [Utilisation des présentations RDLC](ui-rdlc-report-layouts.md)

   Modifiez le fichier et enregistrez-le.

4. De retour sur les **Présentations d’état**, sélectionnez l’action **Nouvelle présentation**.
5. Renseignez les champs suivants :

   |Champ|Description|Obligatoire|
   |-----|-----------|---------|
   |ID état|Définir l’ID affecté au rapport|oui|
   |Nom de la présentation| Tapez un bref nom descriptif pour la présentation pour vous aider à l’identifier facilement.|oui|
   |Description| Tapez des informations plus détaillées sur la présentation. |non|
   |Options de format|Définissez ce champ pour qu’il corresponde au type de présentation, comme Word, Excel ou RDLC.|oui|

6. Sélectionnez **OK**, puis effectuez une des étapes suivantes pour télécharger le fichier pour le rapport :

   [!INCLUDE[file-upload](includes/file-upload.md)]

   Le fichier sélectionné est chargé dans la présentation et vous revenez à la page **Présentations d’état**.

Si vous voulez voir à quoi ressemble l’état avec la nouvelle présentation, sélectionnez la présentation dans la liste, puis sélectionnez **Exécuter état**.

---

## <a name="a-namemodifyamodify-a-layout" /><a name="modify"></a>Modifier une présentation

Suivez ces étapes pour modifier une présentation existante définie par l’utilisateur.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Sélectionnez la présentation que vous souhaitez modifier, puis choisissez l’action **Exporter présentation**.

   Le fichier de présentation sera téléchargé sur votre appareil. 

   > [!TIP]
   > Pour vous aider à trouver la présentation, utilisez la case **Rechercher**, le volet **Filtrer** et le tri des colonnes.

3. Ouvrez le fichier de présentation dans l’application appropriée, telle que Word (pour un fichier .docx) ou Excel (pour un fichier .xlsx).

   Pour plus d’informations, voir :

   * [Utiliser des présentations Word](ui-how-add-fields-word-report-layout.md)
   * [Utilisation des présentations Excel](ui-excel-report-layouts.md)
   * [Utilisation des présentations RDLC](ui-rdlc-report-layouts.md)

   Modifiez le fichier et enregistrez-le.

4. De retour sur la page **Présentations d’état**, sélectionnez la présentation existante, puis sélectionnez l’action **Remplacer la présentation**.
5. Sélectionnez **OK** > **Choisir** pour ouvrir l’explorateur de fichiers sur votre appareil.
6. Recherchez et sélectionnez le fichier Excel, puis sélectionnez **Ouvrir**.

   Le fichier sélectionné est chargé dans la présentation et vous revenez à la page **Présentations d’état**.
7. Si vous voulez voir à quoi ressemble l’état avec la nouvelle présentation, sélectionnez la présentation dans la liste, puis sélectionnez **Exécuter état**.

## <a name="a-namereplaceareplace-a-layout" /><a name="replace"></a>Remplacer une présentation

Suivez ces étapes pour remplacer le fichier de présentation défini par l’utilisateur existant par un nouveau fichier.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Sélectionnez la présentation existante, puis sélectionnez l’action **Remplacer la présentation**.
3. Sélectionnez **OK** > **Choisir** pour ouvrir l’explorateur de fichiers sur votre appareil.
4. Recherchez et sélectionnez le fichier Excel, puis sélectionnez **Ouvrir**.

   Le fichier sélectionné est chargé dans la présentation et vous revenez à la page **Présentations d’état**.
5. Si vous voulez voir à quoi ressemble l’état avec la nouvelle présentation, sélectionnez la présentation dans la liste, puis sélectionnez **Exécuter état**.

## <a name="a-namerenamearename-a-layout" /><a name="rename"></a>Renommer une présentation

Suivez ces étapes si vous souhaitez modifier le nom et la description d’une présentation définie par l’utilisateur.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Sélectionnez la présentation que vous souhaitez renommer, puis choisissez l’action **Modifier informations**.

    > [!TIP]
    > Pour vous aider à trouver la présentation, utilisez la case **Rechercher**, le volet **Filtrer** et le tri des colonnes.
3. Changez le **Nom de la présentation**, puis cliquez sur **OK**.

## <a name="see-related-microsoft-trainingtrainingmoduleschange-documents-dynamics--business-centralindex" />Voir la [formation Microsoft](/training/modules/change-documents-dynamics-365-business-central/index) associée

## <a name="see-also" />Voir aussi

[Gestion des présentations d’état](ui-manage-report-layouts.md)  
[Utilisation des présentations Word](ui-how-add-fields-word-report-layout.md)  
[Utilisation des présentations Excel](ui-excel-report-layouts.md)  
[Utilisation des états, des traitements par lots et des ports XML](ui-work-report.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
