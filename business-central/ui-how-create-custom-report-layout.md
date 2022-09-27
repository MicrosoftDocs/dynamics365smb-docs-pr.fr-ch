---
title: Créer et modifier des présentations personnalisées pour les rapports et les documents
description: Découvrez comment créer des présentations personnalisées qui vous permettent de personnaliser l’apparence d’un rapport lorsqu’il est consulté, imprimé ou enregistré.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/06/2022
ms.author: edupont
ms.openlocfilehash: 1d9d61ad7a4e9b0b64fd11d8a2c1a29676a8ddb4
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531987"
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>(Hérité) Créer et modifier des présentations de rapport personnalisées

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Par défaut, les rapports ont une présentation de rapport intégrée. La présentation peut être une présentation état RDLC, une présentation état Word, ou les deux. Vous ne pouvez pas modifier les présentations intégrées, mais vous pouvez créer des présentations personnalisées. Un rapport peut avoir plusieurs présentations état personnalisées.

> [!NOTE]  
> Dans [!INCLUDE[prod_short](includes/prod_short.md)], le terme « état » couvre également les documents externes, tels que les factures vente et les confirmations de commande que vous envoyez à des clients comme fichiers PDF.

Pour créer une présentation personnalisée, copiez une présentation personnalisée existante ou ajoutez une nouvelle présentation personnalisée. Les présentations personnalisées sont souvent basées sur une présentation intégrée. Lorsque vous ajoutez une nouvelle présentation personnalisée, vous pouvez choisir d’ajouter un type de présentation de rapport RDLC ou un type de présentation état Word, ou les deux. La nouvelle présentation personnalisée est basée sur la présentation intégrée pour le rapport s’il y en a une disponible. S’il n’y a pas de présentation intégrée pour le type, une nouvelle mise en page vierge est créée. Vous devez modifier et concevoir cette mise en page vierge à partir de zéro. Pour plus d’informations sur les présentations de rapport RDLC et Word, les présentations intégrées et personnalisées, et plus encore, reportez-vous à [Gérer la présentation des états](ui-manage-report-layouts.md).  

> [!TIP]
> Utilisez les tableaux d’analyse pour obtenir un aperçu des données financières enregistrées dans votre plan comptable. Pour plus d’informations, voir [Préparer la génération d’états financiers avec des tableaux d’analyse et des catégories de compte](bi-how-work-account-schedule.md).

Après avoir défini des présentations état personnalisées, vous pouvez les sélectionner sur les pages Fiche client et Fiche fournisseur. Les présentations seront utilisées lorsque vous créerez des documents pour le client ou le fournisseur. Pour plus d’informations, voir [Définir des présentations de document pour les clients et les fournisseurs](ui-define-customer-vendor-document-layouts.md).

Vous pouvez également utiliser des présentations d’état personnalisées pour ajouter du contenu aux messages électroniques. Les présentations d’état peuvent vous faire gagner du temps et contribuer à assurer la cohérence, car elles réutilisent le même contenu lorsque vous communiquez avec vos clients. Pour utiliser des présentations d’état personnalisées avec le courrier électronique, le type de fichier de la mise en page doit être Word. Vous ne pouvez pas utiliser le type de fichier RDLC. Pour plus d’informations, voir [Configurer des textes et des mises en page d’e-mail réutilisables](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="to-create-a-custom-layout"></a>Pour créer une présentation personnalisée

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Sélection présentation état**, puis sélectionnez le lien associé.

    La page **Sélection présentation état** répertorie tous les états disponibles pour la société spécifiée dans le champ **Nom de la société** en haut de la page.
2. Dans le champ **Nom de la société**, choisissez la société pour laquelle vous souhaitez créer la présentation de rapport.
3. Sélectionnez la ligne de l’état pour lequel vous souhaitez créer la présentation, puis sélectionnez l’action **Présentations personnalisées**.  

   La page **Présentations état personnalisées** s’affiche et répertorie toutes les présentations personnalisées disponibles pour l’état sélectionné.
4. Si vous souhaitez créer une copie d’une présentation personnalisée existante, sélectionnez cette dernière, puis sélectionnez l’action **Copier**.  

   La copie de la présentation personnalisée s’affiche sur la page **Présentations état personnalisées**. Le terme *Copie* figure dans le champ **Description**.
5. Si vous voulez ajouter une nouvelle présentation personnalisée basée sur une présentation intégrée, procédez comme suit :  
   1. Sélectionnez l’action **Nouveau**. La page **Insérer présentation intégrée pour un état** s’affiche. Les champs **ID** et **Nom** sont automatiquement renseignés.
   2. Pour ajouter un type de présentation état Word, activez la case **Insérer présentation Word**.
   3. Pour ajouter un type de présentation état RDLC, activez la case **Insérer présentation RDLC**.
   4. Cliquez sur le bouton **OK**.  

    La nouvelle présentation personnalisée s’affiche désormais sur la page **Présentations état personnalisées**. Si une nouvelle présentation est basée sur une présentation intégrée, les termes **Copie d’une présentation intégrée** figurent dans le champ **Description**. S’il n’y avait aucune présentation intégrée pour l’état, les termes **Nouvelle présentation** figurent dans le champ **Description** de la nouvelle présentation, ce qui indique que la présentation personnalisée est vide.
6. Par défaut, le champ **Nom de la société** est vide, ce qui signifie que la présentation personnalisée est disponible pour l’état dans toutes les sociétés. Afin que la présentation personnalisée soit disponible pour une société spécifique uniquement, sélectionnez **Modifier**, puis définissez le champ **Nom de la société** sur la société que vous souhaitez.

La présentation personnalisée a été créée. Vous pouvez à présent modifier la présentation personnalisée selon vos besoins.

> [!TIP]
> Vous pouvez exporter les résultats du rapport dans un fichier Excel pour afficher l’ensemble de données complet, y compris toutes les colonnes, mais sans la présentation. Le fichier Excel peut vous aider à valider que le rapport renvoie les données attendues ou les problèmes de diagnostic. Pour plus d’informations, consultez [Analyse des données de rapport avec Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Modification d’une présentation personnalisée

Pour modifier une présentation de rapport, vous devez d’abord exporter la présentation de rapport sous forme de fichier vers un emplacement sur votre ordinateur ou réseau. Ensuite, ouvrez le document exporté et apportez les modifications. Lorsque vous avez terminé d’apporter les modifications, vous importez la présentation de rapport.

### <a name="to-modify-a-custom-layout"></a>Pour modifier une présentation personnalisée

1. Vous exportez une présentation personnalisée à partir de la page **Présentations état personnalisées**. Si cette page n’est pas déjà ouverte, recherchez et ouvrez la page **Sélection présentation état**, sélectionnez l’état dont vous souhaitez modifier la présentation, puis choisissez l’action **Présentations personnalisées**.  
2. Sur la page **Présentations état personnalisées**, sélectionnez la présentation à modifier, choisissez l’action **Exporter présentation**, puis choisissez **Enregistrer** ou **Enregistrer sous** pour enregistrer le document de présentation d’état dans un emplacement sur votre ordinateur ou réseau.  
3. Ouvrez le document de présentation de rapport que vous avez enregistré puis apportez les modifications.

   Si vous modifiez une présentation Word, ouvrez le document de présentation dans Word. Pour plus de détails sur l’édition, voir [Utiliser des dispositions Word](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   Les présentations de rapport RDLC sont plus avancées que les présentations de rapport Word. Pour plus d’informations sur la modification d’une présentation de rapport RDLC, voir [Création de présentations de rapport RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Pensez à enregistrer vos modifications une fois que vous avez terminé.

4. Retournez à la page **Présentations état personnalisées**, sélectionnez la présentation d’état que vous avez exportée et modifiée, puis choisissez l’action **Importer présentation**.  

5. Dans la boîte de dialogue **Importer**, sélectionnez **Choisir** pour rechercher et sélectionner le document de présentation d’état modifié, puis choisissez **Ouvrir**.

> [!IMPORTANT]
> N’oubliez pas d’importer le document de mise en page de rapport que vous avez modifié. Sinon, la nouvelle mise en page du rapport ne sera pas disponible.

<!--
##  <a name="MakeChangesToLayout"></a> Create and Modify Custom Report Layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word, like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### Embedding Fonts in Word Layouts for Consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. For more information about embedding fonts in Word, see [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Removing Label and Data Fields in Word Layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### To remove a label or data field  

1. Right-click the field that you want to delete, and then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### Adding data fields

Adding data fields from a report dataset is a more advanced and requires some knowledge of the report dataset. For information about adding fields for data, labels, data, and images, see [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/change-documents-dynamics-365-business-central/index) associée

## <a name="see-also"></a>Voir aussi

[Gestion des présentations d’état](ui-manage-report-layouts.md)  
[Modifier la présentation actuelle de l’état](ui-how-change-layout-currently-used-report.md)  
[Importer et exporter une présentation d’état ou de document personnalisée](ui-how-import-and-export-report-layout.md)  
[Utiliser des états, des traitements par lots et des XMLports](ui-work-report.md)  
[Préparer Financial Reporting avec des tableaux d’analyse et des catégories de compte](bi-how-work-account-schedule.md)  
[Veille économique](bi.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
