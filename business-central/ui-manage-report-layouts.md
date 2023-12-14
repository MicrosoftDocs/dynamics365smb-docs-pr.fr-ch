---
title: Gestion des présentations de rapport et de document
description: 'Utilisez des présentations d’états pour personnaliser les documents, par exemple, pour personnaliser la police, le logo, ou la mise en page des fichiers PDF que vous envoyez aux clients.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650, 9660'
ms.date: 05/23/2023
ms.author: jswymer
---
# <a name="report-and-document-layouts-overview"></a>Vue d’ensemble des présentations d’état et de document

Une présentation d’état contrôle le contenu et le format du rapport, dont les champs de données d’un ensemble de données d’état apparaissant sur le rapport et la façon ils sont organisés, le style de texte, les images, et plus encore. À partir de [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez modifier la présentation utilisée sur un rapport, créer une nouvelle présentation ou modifier les présentations existantes.

> [!NOTE]  
> Dans [!INCLUDE[prod_short](includes/prod_short.md)], le terme « état » couvre également les documents externes, tels que les factures vente et les confirmations de commande que vous envoyez à des clients comme fichiers PDF.

Vous pouvez également utiliser des présentations d’état pour ajouter du contenu aux messages électroniques. Par exemple, les présentations d’état peuvent vous faire gagner du temps et contribuer à assurer la cohérence, car elles réutilisent le même contenu lorsque vous communiquez avec vos clients. Pour utiliser des présentations d’état personnalisées avec le courrier électronique, le type de fichier de la mise en page doit être Word. Vous ne pouvez pas utiliser le type de fichier RDLC. Pour plus d’informations, voir [Configurer des textes et des mises en page d’e-mail réutilisables](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="introduction"></a>Introduction

Une présentation d’état configure notamment ce qui suit :

* Les champs d’étiquette et de données à inclure à partir de l’ensemble des données du rapport [!INCLUDE[prod_short](includes/prod_short.md)].
* Le format du texte, comme le type, la taille et la couleur de police.
* Le logo de la société et son emplacement.
* Paramètres de page généraux, comme les marges et les images d’arrière-plan.

Un état peut être créé avec plusieurs présentations d’état, que vous pouvez ensuite changer au besoin. 

<!--You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed. For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).-->

Deux aspects importants des présentations d’états influenceront la manière dont vous les utiliserez : le *type de présentation* et la *source de la présentation*. Le type de présentation indique le type de fichier sur lequel la présentation est basée. La source de la présentation indique l’origine de la présentation.

## <a name="layout-types"></a>Types de présentation

Il existe quatre types de présentation que vous pouvez utiliser pour les états : Word, RDLC, Excel et externe.

### <a name="word"></a>Word

Les présentations Word sont basées sur les documents Word (type de fichier .docx). Les présentations Word vous permettent de concevoir des présentations d’état à l’aide de Microsoft Word. Une présentation Word détermine le contenu de l’état, contrôle la manière dont les éléments de contenu sont organisés ainsi que leur apparence. Un document de présentation Word utilisera généralement des tableaux pour organiser le contenu, dans lequel les cellules peuvent contenir des champs de données, du texte ou des images.

[![Exemple de document de présentation état Word pour Business Central.](media/word-layout-overview.png)](media/word-layout-overview.png#lightbox) 

<!--![Example of a word report layout document for Business Central.](media/nav_wordreportlayout_edit_in_word_example.png) -->

Pour plus d’informations, voir [Utiliser des présentations Word](ui-how-add-fields-word-report-layout.md).

### <a name="excel"></a>Excel

Les présentations Excel sont basées sur les classeurs Microsoft Excel (type de fichier .xlsx). Elles vous permettent de créer des états en utilisant des fonctionnalités Excel familières pour résumer, analyser et présenter des données avec des outils comme des formules, des tableaux croisés dynamiques et des graphiques croisés dynamiques, etc.

[![Affiche un exemple de présentation Excel.](media/excel-layout-2.png)](media/excel-layout-2.png#lightbox)

Pour plus d’informations, voir [Utiliser des présentations Excel](ui-excel-report-layouts.md).

### <a name="rdlc"></a>RDLC

Les présentations RDLC sont basées sur les fichiers de présentation de définition d’état client (types de fichier .rdl ou .rdlc). Ces présentations sont créées et modifiées à l’aide du Générateur d’états SQL Server ou Microsoft RDLC Report Designer. Le concept de conception des présentations RDLC est similaire à celui des présentations Word, où la présentation détermine les champs à afficher et leur disposition. Toutefois, la création de présentations RDLC est plus avancée que les présentations Word.

[![Affiche un exemple de présentation RDLC.](media/rdlc-layout-overview.png)](media/rdlc-layout-overview.png#lightbox)

Pour plus d’informations, voir [Utiliser des présentations RDLC](ui-rdlc-report-layouts.md).

### <a name="external"></a>Externe

Un type de présentation externe fait référence à un type avancé spécialement conçu pour des états spécifiques. Les états et les présentations elles-mêmes sont généralement fournies par des partenaires, et non par Microsoft. Le type de fichier réel de la présentation varie selon le fournisseur.

Pour plus d’informations, voir [Développement d’un rendu d’état personnalisé](/dynamics365/business-central/dev-itpro/developer/devenv-report-custom-render).

## <a name="layout-sources"></a>Sources de présentation

En plus du type, les présentations sont divisées en trois catégories, en fonction de leur source ou de leur origine.

* Présentations d’extension

   Les présentations d’extension sont des présentations qui font partie d’une extension qui a été installée sur l’environnement. Ces présentations sont généralement des présentations standard fournies par Microsoft, par exemple, dans l’application de base. Ou, il peut s’agir de présentations incluses dans des extensions d’autres fournisseurs de logiciels. Vous pouvez distinguer les présentations d’extensions sur la page **Présentations d’état** car le nom de l’extension et l’éditeur s’affichent dans la colonne **Extension**.

* Présentations définies par l’utilisateur

   L’autre source de présentation est l’utilisateur final. À partir de Business Central, un utilisateur disposant des autorisations appropriées peut ajouter de nouvelles présentations de différentes manières. Il est par exemple possible de commencer à partir d’une présentation d’extension existante ou d’une autre présentation définie par l’utilisateur. Sur les **Présentations d’état**, la présentation définie par l’utilisateur aura une colonne **Extension** vide.

   Pour plus d’informations, voir [Bien démarrer avec la création de présentations d’état](ui-get-started-layouts.md).

* Présentations personnalisées

  Les présentations personnalisées sont également des présentations créées par les utilisateurs. La différence réside dans le fait que ces présentations sont créées à partir de la page **Présentations d’état personnalisées** héritée, et qu’elles ne peuvent être que de type Word et RDLC. Bien que vous puissiez toujours créer des présentations personnalisées, elles sont progressivement supprimées au profit de présentations définies par l’utilisateur.

  Pour plus d’informations, voir [(Hérité) Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).

Pour obtenir des informations qui vous aideront à choisir le type qui vous convient le mieux, voir [Décider du type de présentation souhaité](ui-get-started-layouts.md#decide).

> [!IMPORTANT]
> Une chose importante à retenir est que vous ne pouvez pas modifier les présentations d’extension à partir du client Business Central. Par exemple, vous n’êtes pas autorisé à modifier le nom ou le type de la présentation, ni à la télécharger et à la remplacer par une autre version. Si vous essayez, vous recevez un message d’erreur. Vous devrez plutôt créer une présentation définie par l’utilisateur ou personnalisée basée sur la présentation d’extension.

<!--
### <a name="built-in-and-custom-report-layouts"></a>Built-in and custom report layouts



[!INCLUDE[prod_short](includes/prod_short.md)] includes several built-in layouts. Built-in layouts are predefined layouts that are designed for specific reports. [!INCLUDE[prod_short](includes/prod_short.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both. You can’t modify a built-in report layout from [!INCLUDE[prod_short](includes/prod_short.md)] but you use them as a starting point for building your own custom report layouts.

Custom layouts are report layouts that you design to change the appearance of a report. You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout. Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed. For example, you can have different layouts for each [!INCLUDE[prod_short](includes/prod_short.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.


Deciding on whether to use a Word, Excel, or RDLC layout type will depend on how you want the generated report to look and your knowledge of tools for creating the layouts, like Word, Excel, and SQL Server Report Builder.

* The general design concepts for Word and RDLC layouts are similar. However each type has certain design features that affect how the generated report appears in [!INCLUDE[prod_short](includes/prod_short.md)]. This means that the same report might look different when using the Word report layout compared to the RDLC report layout.

* The process for setting up Word, Excel, and RDLC report layouts on reports is the same. The main difference is in the way you modify the layouts. Word and especially Excel layouts are typically easier to create and modify than RDLC report layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.

* Not all reports and document have a dataset that is optimized for use with an Excel layout. For example, aggregations and complex calculations work best with RDLC or Word layouts. The same is true for documents.

For information about how to switch the layout currently used on a report, see [Set the Layout Used by a Report](ui-set-report-layout.md).

-->
## <a name="see-also"></a>Voir aussi

[Mise à jour des dispositions de rapport personnalisées](ui-update-report-layouts.md)  
[Création et modification des dispositions de rapport personnalisées](ui-how-create-custom-report-layout.md)  
[Importer et exporter une présentation d’état ou de document personnalisée](ui-how-import-and-export-report-layout.md)  
[Définir des présentations de document spéciales pour les clients et les fournisseurs](ui-define-customer-vendor-document-layouts.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Utiliser des états, des traitements par lots et des XMLports](ui-work-report.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
