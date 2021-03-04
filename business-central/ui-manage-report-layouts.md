---
title: Présentations d’état intégrées et personnalisées pour les états et les documents | Microsoft Docs
description: Utilisez des présentations d’états pour personnaliser les documents, par exemple, pour personnaliser la police, le logo, ou la mise en page des fichiers PDF que vous envoyez aux clients.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8a3cfebf90ba639b8d8563ce437c6f5605acf2eb
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756832"
---
# <a name="managing-report-and-document-layouts"></a>Gestion des présentations de rapport et de document
Une présentation de rapport contrôle le contenu et le format du rapport, dont les champs de données d’un ensemble de données de rapport apparaissant sur le rapport et la façon ils sont organisés, le style de texte, les images, et plus encore. À partir de [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez modifier la présentation utilisée sur un rapport, créer une nouvelle présentation ou modifier les présentations existantes.

> [!NOTE]  
>   Dans [!INCLUDE[prod_short](includes/prod_short.md)], le terme « état » couvre également les documents externes, tels que les factures vente et les confirmations de commande que vous envoyez à des clients comme fichiers PDF.

En particulier, une présentation de rapport configure ce qui suit :

* Les champs d’étiquette et de données à inclure à partir de l’ensemble des données du rapport [!INCLUDE[prod_short](includes/prod_short.md)].
* Le format du texte, comme le type, la taille et la couleur de police.
* Le logo de la société et son emplacement.
* Paramètres de page généraux, comme les marges et les images d’arrière-plan.

Un état peut être créé avec plusieurs présentations d’état, que vous pouvez ensuite changer au besoin. Vous pouvez utiliser l’une des présentations d’état intégrées ou vous pouvez créer des présentations d’état personnalisées et les affecter à vos états selon vos besoins. Pour plus d’informations, voir [Créer une présentation de rapport ou de document personnalisée](ui-how-create-custom-report-layout.md).

Il existe deux types de présentations que vous pouvez utiliser pour les états : Word et RDLC.

## <a name="word-report-layout-overview"></a>Aperçu de la présentation d’état Word
Une présentation de rapport Word est basé sur un document Word (type de fichier .docx). Les présentations d’état Word vous permettent de concevoir des présentations d’état à l’aide de Microsoft Word 2013 ou une version ultérieure. Une présentation d’état Word détermine le contenu de l’état, contrôle la manière dont les éléments de contenu sont organisés ainsi que leur apparence. Un document de présentation de rapport Word utilisera généralement des tableaux pour organiser le contenu, dans lequel les cellules peuvent contenir des champs de données, du texte ou des images.

 ![Exemple de document de présentation de rapport Word pour NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")  

## <a name="rdlc-layout-overview"></a>Aperçu de la présentation RDLC
Les présentations RDLC sont basées sur les présentations de définition de rapport client (types de fichier .rdlc or .rdl). Ces présentations sont créées et modifiées à l’aide du Générateur de rapports SQL Server. Le concept des présentations RDLC est similaire à celui des présentations Word, où la présentation définit le format général de l’état et détermine les champs de l’ensemble de données à inclure. La création de présentations RDLC est plus avancée que les présentations Word. Pour plus d’informations, voir [Création de présentations de rapport RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).

## <a name="built-in-and-custom-report-layouts"></a>Présentations d’état intégrées et personnalisées
[!INCLUDE[prod_short](includes/prod_short.md)] inclut plusieurs présentations intégrées. Les présentations intégrées sont des présentations prédéfinies conçues pour des états spécifiques. Les états [!INCLUDE[prod_short](includes/prod_short.md)] comportent une présentation intégrée RDLC ou Word, ou parfois les deux. Vous ne pouvez pas modifier une présentation d’état intégrée à [!INCLUDE[prod_short](includes/prod_short.md)], mais vous pouvez les utilisez comme point de départ pour l’élaboration de vos propres présentations d’état personnalisées.

Les présentations personnalisées sont des présentations de rapport que vous créez pour modifier l’apparence d’un rapport. Vous créez généralement une présentation personnalisée basée sur une présentation intégrée, mais vous pouvez les créer de A à Z ou à partir d’une copie d’une présentation personnalisée existante. Les présentations personnalisées vous permettent d’avoir plusieurs présentations pour le même rapport, que vous choisissez en fonction de vos besoins. Par exemple, vous pouvez avoir différentes présentations pour chaque société [!INCLUDE[prod_short](includes/prod_short.md)] ou vous pouvez avoir plusieurs présentations pour la même société pour des occasions ou événements spécifiques, comme une campagne spéciale ou la période des fêtes.

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a>Décider d’utiliser une présentation d’état Word ou RDLC
Une présentation de rapport peut être basée sur un document Word ou un fichier RDLC. Le choix entre une présentation de rapport Word ou une présentation de rapport RDLC dépendra de la façon dont vous souhaitez que le rapport généré apparaisse et de vos connaissances sur Word et SQL Server Report Builder.

Les concepts généraux pour les présentations Word et RDLC sont très similaires. Cependant, la conception de chaque type présente certaines fonctionnalités qui affectent la manière dont l’état généré s’affiche dans [!INCLUDE[prod_short](includes/prod_short.md)]. Cela signifie que le même rapport peut sembler différent selon que vous utilisez une présentation de rapport Word ou une présentation de rapport RDLC.

Le procédure pour paramétrer des présentations de rapport Word et des présentations de rapport RDLC sur les rapports est la même. La principale différence réside dans la manière dont vous modifiez les présentations. Il est souvent plus facile de créer et de modifier des présentations de rapport Word que des présentations de rapport RDLC car vous pouvez utiliser Word. Les présentations de rapport RDLC sont modifiées à l’aide de SQL Server Report builder qui cible plus d’utilisateurs avancés.

Pour plus d’informations sur la manière d’utiliser l’une ou l’autre présentation, voir [Modifier la présentation actuelle de l’état](ui-how-change-layout-currently-used-report.md).

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi
[Mettre à jour les présentations d’état personnalisées](ui-update-report-layouts.md)  
[Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md)  
[Importer et exporter une présentation d’état ou de document personnalisée](ui-how-import-and-export-report-layout.md)  
[Définir des présentations de document spéciales pour les clients et les fournisseurs](ui-define-customer-vendor-document-layouts.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Utilisation des états, des traitements par lots et des XMLports](ui-work-report.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]