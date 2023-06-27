---
title: Créer et modifier des présentations personnalisées pour les rapports et les documents
description: 'Découvrez comment créer des présentations personnalisées qui vous permettent de personnaliser l’apparence d’un rapport lorsqu’il est consulté, imprimé ou enregistré.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/06/2022
ms.author: edupont
---
# <a name="legacy-create-and-modify-custom-report-layouts" />(Hérité) Créer et modifier des présentations de rapport personnalisées

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Par défaut, les états ont une présentation intégrée. La présentation d’état peut être de type RDLC, Microsoft Word, ou les deux. Vous ne pouvez pas modifier les présentations intégrées, mais vous pouvez créer des présentations personnalisées. Un rapport peut avoir plusieurs présentations état personnalisées.

> [!NOTE]  
> Dans [!INCLUDE[prod_short](includes/prod_short.md)], le terme « état » couvre également les documents externes, tels que les factures vente et les confirmations de commande que vous envoyez à des clients comme fichiers PDF.

Pour créer une présentation personnalisée, copiez une présentation personnalisée existante ou ajoutez une nouvelle présentation personnalisée. Les présentations personnalisées sont souvent basées sur une présentation intégrée. Lorsque vous ajoutez une nouvelle présentation personnalisée, vous pouvez choisir d’ajouter une présentation d’état de type RDLC ou de type Word, ou les deux. La nouvelle présentation personnalisée est basée sur la présentation intégrée pour le rapport s’il y en a une disponible. S’il n’y a pas de présentation intégrée pour le type, une nouvelle mise en page vierge est créée. Vous devez modifier et concevoir cette mise en page vierge à partir de zéro. Pour plus d’informations sur les présentations d’état RDLC et Word, les présentations intégrées et personnalisées, et plus encore, reportez-vous à [Gérer la présentation des états](ui-manage-report-layouts.md).  

> [!TIP]
> Utilisez les états financiers pour obtenir un aperçu des données financières enregistrées dans votre plan comptable. En savoir plus sur [Préparer Financial Reporting avec des données financières et des catégories de compte](bi-how-work-account-schedule.md).

Après avoir défini des présentations état personnalisées, vous pouvez les sélectionner sur les pages Fiche client et Fiche fournisseur. Les présentations seront utilisées lorsque vous créerez des documents pour le client ou le fournisseur. En savoir plus sur [Définir des présentations de document pour les clients et les fournisseurs](ui-define-customer-vendor-document-layouts.md).

Vous pouvez également utiliser des présentations d’état personnalisées pour ajouter du contenu aux messages électroniques. Les présentations d’état peuvent vous faire gagner du temps et contribuer à assurer la cohérence, car elles réutilisent le même contenu lorsque vous communiquez avec vos clients. Pour utiliser des présentations d’état personnalisées avec le courrier électronique, le type de fichier de la mise en page doit être Word, et non RDLC. En savoir plus sur [Configurer des textes et des mises en page d’e-mail réutilisables](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).

## <a name="create-a-custom-layout" />Créer une présentation personnalisée

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Sélection présentation état**, puis sélectionnez le lien associé.

    La page **Sélection présentation état** répertorie tous les états disponibles pour la société spécifiée dans le champ **Nom de la société** en haut de la page.
2. Dans le champ **Nom de la société**, choisissez la société pour laquelle vous souhaitez créer la présentation d’état.
3. Sélectionnez la ligne de l’état pour lequel vous souhaitez créer la présentation, puis sélectionnez l’action **Présentations personnalisées**.  

   La page **Présentations état personnalisées** s’affiche et répertorie toutes les présentations personnalisées disponibles pour l’état sélectionné.
4. Si vous souhaitez créer une copie d’une présentation personnalisée existante, sélectionnez cette dernière, puis sélectionnez l’action **Copier**.  

   La copie de la présentation personnalisée s’affiche sur la page **Présentations état personnalisées**. Le terme *Copie* figure dans le champ **Description**.
5. Si vous voulez ajouter une nouvelle présentation personnalisée basée sur une présentation intégrée, procédez comme suit :  
   1. Sélectionnez l’action **Nouveau**. La page **Insérer présentation intégrée pour un état** s’affiche avec les champs **ID** et **Nom** automatiquement renseignés dans.
   2. Activez le bouton à bascule **Insérer présentation Word** pour ajouter une présentation état Word personnalisée OU activez le bouton à bascule **Insérer présentation RDLC** pour ajouter une présentation état RDLC personnalisée.
   4. Cliquez sur le bouton **OK**.  

    La nouvelle présentation personnalisée s’affiche désormais sur la page **Présentations état personnalisées**. Si une nouvelle présentation est basée sur une présentation intégrée, les termes **Copie d’une présentation intégrée** figurent dans le champ **Description**. S’il n’y avait aucune présentation intégrée pour l’état, les termes **Nouvelle présentation** figurent dans le champ **Description** de la nouvelle présentation, ce qui indique que la présentation personnalisée est vide.
6. Par défaut, le champ **Nom de la société** est vide, ce qui signifie que la présentation personnalisée est disponible pour l’état dans toutes les sociétés. Afin que la présentation personnalisée soit disponible pour une société spécifique uniquement, sélectionnez **Modifier**, puis définissez le champ **Nom de la société** sur la société que vous souhaitez.

La mise en page personnalisée a été créée et vous pouvez la modifier à votre guise.

> [!TIP]
> Vous pouvez exporter les résultats d’état dans un fichier Microsoft Excel pour afficher l’ensemble de données complet, y compris toutes les colonnes, mais sans la présentation. Le fichier Excel peut vous aider à valider que l’état renvoie les données attendues ou les problèmes de diagnostic. En savoir plus [Analyse des données d’état avec Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout" /><a name="ModifyCustomLayout"></a>Modification d’une présentation personnalisée

Pour modifier une présentation d’état personnalisée, vous devez d’abord exporter la présentation d’état sous forme de fichier vers un emplacement sur votre ordinateur ou réseau. Ensuite, ouvrez le document exporté et apportez les modifications. Lorsque vous avez terminé d’apporter les modifications, vous importez la présentation de rapport.

### <a name="modify-a-custom-layout" />Modifier une présentation personnalisée

1. Exportez une présentation personnalisée à partir de la page **Présentations état personnalisées**. Si cette page n’est pas déjà ouverte, recherchez et ouvrez la page **Sélection présentation état**, sélectionnez l’état dont vous souhaitez modifier la présentation, puis choisissez l’action **Présentations personnalisées**.  
2. Sur la page **Présentations état personnalisées**, sélectionnez la présentation à modifier, choisissez l’action **Exporter présentation**, puis choisissez **Enregistrer** ou **Enregistrer sous** pour enregistrer le document de présentation d’état dans un emplacement sur votre ordinateur ou réseau.  
3. Ouvrez le document de présentation d’état que vous avez enregistré, puis apportez les modifications.

   Si vous modifiez une présentation Word, ouvrez le document de présentation dans Word. En savoir plus sur la modification des états Word sur [Utiliser des présentations Word](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   Les présentations de rapport RDLC sont plus avancées que les présentations de rapport Word. Pour plus d’informations sur la modification d’une présentation d’état RDLC, voir [Création de présentations d’état RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Pensez à enregistrer vos modifications une fois que vous avez terminé.

4. Retournez à la page **Présentations état personnalisées**, sélectionnez la présentation d’état que vous avez exportée et modifiée, puis choisissez l’action **Importer présentation**.  

5. Dans la boîte de dialogue **Importer**, sélectionnez **Choisir** pour rechercher et sélectionner le document de présentation d’état modifié, puis choisissez **Ouvrir**.

> [!IMPORTANT]
> N’oubliez pas d’importer le document de mise en page de rapport que vous avez modifié. Sinon, la nouvelle mise en page du rapport ne sera pas disponible.

<!--
## <a name="create-and-modify-custom-report-layouts" /><a name="MakeChangesToLayout"></a> Create and modify custom report layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### <a name="embedding-fonts-in-word-layouts-for-consistency" />Embedding fonts in Word layouts for consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. Learn more about embedding fonts in Word at [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

### <a name="removing-label-and-data-fields-in-word-layouts" /><a name="RemoveField"></a> Removing label and data fields in Word layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field" />To remove a label or data field

1. Right-click the field you want to delete, then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### <a name="adding-data-fields" />Adding data fields

Adding data fields from a report dataset is more advanced and requires some knowledge of the report dataset. Learn more about adding fields for data, labels, and images at [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/modules/change-documents-dynamics-365-business-central/index) associée

## <a name="see-also" />Voir aussi

[Gestion des présentations d’état](ui-manage-report-layouts.md)  
[Modifier la présentation actuelle de l’état](ui-how-change-layout-currently-used-report.md)  
[Importer et exporter une présentation d’état ou de document personnalisée](ui-how-import-and-export-report-layout.md)  
[Utiliser des états, des traitements par lots et des XMLports](ui-work-report.md)  
[Préparer Financial Reporting avec des données financières et des catégories de compte](bi-how-work-account-schedule.md)  
[Veille économique](bi.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
