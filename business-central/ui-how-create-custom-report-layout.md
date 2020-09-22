---
title: Créer et modifier des présentations personnalisées pour les rapports et les documents| Microsoft Docs
description: Découvrez comment créer vos propres présentations personnalisées qui vous permettent de personnaliser l'apparence d'un rapport lorsqu'il est consulté, imprimé ou enregistré.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 07/22/2020
ms.author: edupont
ms.openlocfilehash: f8d8b40e77e53dad7855721f23cf4cb33a669c4e
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782714"
---
# <a name="create-and-modify-custom-report-layouts"></a>Créer et modifier des présentations de rapport personnalisées

Par défaut, un rapport aura une présentation de rapport intégrée, qui peut être soit une présentation de rapport RDLC ou une présentation de rapport Word, ou les deux. Vous ne pouvez pas modifier les présentations intégrées. Cependant, vous pouvez créer vos propres présentations personnalisées qui vous permettent de modifier l'apparence d'un rapport lorsqu'il est consulté, imprimé ou enregistré. Vous pouvez créer plusieurs présentations de rapport personnalisées pour le même rapport, puis faire basculer la présentation utilisée par un rapport selon vos besoins.

> [!NOTE]  
> Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], le terme « état » couvre également les documents externes, tels que les factures vente et les confirmations de commande que vous envoyez à des clients comme fichiers PDF.

Pour créer une présentation personnalisée, vous pouvez effectuer une copie d'une présentation personnalisée existante ou ajouter une nouvelle présentation personnalisée, qui est le plus souvent basée sur une présentation intégrée. Lorsque vous ajoutez une nouvelle présentation personnalisée, vous pouvez choisir d'ajouter un type de présentation de rapport RDLC, un type de présentation de rapport Word, ou les deux. La nouvelle présentation personnalisée est automatiquement basée sur la présentation intégrée pour le rapport s'il y en a une disponible. S'il n'y a pas de présentation intégrée pour le type, alors une nouvelle présentation vide est créée, que vous devrez modifier et concevoir entièrement. Pour plus d'informations sur les présentations de rapport RDLC et Word, les présentations intégrées et personnalisées, et plus encore, reportez-vous à [Gérer la présentation des états](ui-manage-report-layouts.md).  

> [!TIP]
> Utilisez les tableaux d'analyse pour obtenir un aperçu des données financières enregistrées dans votre plan comptable. Pour plus d'informations, voir [Préparer la génération d'états financiers avec des tableaux d'analyse et des catégories de compte](bi-how-work-account-schedule.md).

Lorsque des présentations de rapport personnalisées sont définies, vous pouvez les sélectionner à partir des fiches client et fournisseur pour spécifier que les présentations sélectionnées sont utilisées pour les documents que vous créez pour le client ou le fournisseur en question. Pour plus d'informations, voir [Définir des présentations de document pour les clients et les fournisseurs](ui-define-customer-vendor-document-layouts.md).

## <a name="to-create-a-custom-layout"></a>Pour créer une présentation personnalisée

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Sélection présentation état**, puis sélectionnez le lien associé.

    La page **Sélection présentation état** répertorie tous les états disponibles pour la société spécifiée dans le champ **Nom de la société** en haut de la page.
2. Définissez le champ **Société** sur la société pour laquelle vous souhaitez créer la présentation de rapport.
3. Sélectionnez la ligne de l'état pour lequel vous souhaitez créer la présentation, puis sélectionnez l'action **Présentations personnalisées**.  

   La page **Présentations état personnalisées** s'affiche et répertorie toutes les présentations personnalisées disponibles pour l'état sélectionné.
4. Si vous souhaitez créer une copie d'une présentation personnalisée existante, sélectionnez cette dernière, puis sélectionnez l'action **Copier**.  

   La copie de la présentation personnalisée s'affiche sur la page **Présentations état personnalisées**. Le terme *Copie* figure dans le champ **Description**.
5. Si vous voulez ajouter une nouvelle présentation personnalisée basée sur une présentation intégrée, procédez comme suit :  
   1. Sélectionnez l'action **Nouveau**. La page **Insérer présentation intégrée pour un état** s'affiche. Les champs **ID** et **Nom** sont automatiquement renseignés.
   2. Pour ajouter un type de présentation état Word, cochez la case **Insérer présentation Word**.
   3. Pour ajouter un type de présentation état RDLC, cochez la case **Insérer présentation RDLC**.
   4. Cliquez sur le bouton **OK**.  

    La nouvelle présentation personnalisée s'affiche désormais sur la page **Présentations état personnalisées**. Si une nouvelle présentation est basée sur une présentation intégrée, les termes **Copie d'une présentation intégrée** figurent dans le champ **Description**. S'il n'y avait aucune présentation intégrée pour l'état, les termes **Nouvelle présentation** figurent dans le champ **Description** de la nouvelle présentation, ce qui indique que la présentation personnalisée est vide.
6. Par défaut, le champ **Nom de la société** est vide, ce qui signifie que la présentation personnalisée est disponible pour l'état dans toutes les sociétés. Afin que la présentation personnalisée soit disponible pour une société spécifique uniquement, sélectionnez **Modifier**, puis définissez le champ **Nom de la société** sur la société que vous souhaitez.

La présentation personnalisée a été créée. Vous pouvez à présent modifier la présentation personnalisée selon vos besoins.

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Modification d'une présentation personnalisée

Pour modifier une présentation de rapport, vous devez d'abord exporter la présentation de rapport sous forme de fichier dans un emplacement sur votre ordinateur ou le réseau, puis ouvrir le document exporté et effectuer les modifications. Lorsque vous avez terminé d'apporter les modifications, vous importez la présentation de rapport.

### <a name="to-modify-a-custom-layout"></a>Pour modifier une présentation personnalisée

1.  Vous exportez une présentation personnalisée à partir de la page **Présentations état personnalisées**. Si cette page n'est pas déjà ouverte, recherchez et ouvrez la page **Sélection présentation état**, sélectionnez l'état dont vous souhaitez modifier la présentation, puis choisissez l'action **Présentations personnalisées**.  
2.  Sur la page **Présentations état personnalisées**, sélectionnez la présentation à modifier, choisissez l'action **Exporter présentation**, puis choisissez **Enregistrer** ou **Enregistrer sous** pour enregistrer le document de présentation d'état dans un emplacement sur votre ordinateur ou réseau.  

3.  Ouvrez le document de présentation d'état que vous avez enregistré, puis apportez les modifications.

      Si vous modifiez une présentation Word, ouvrez le document de présentation dans Word. Pour modifier les détails, reportez-vous à la section suivante [Apporter des modifications à la présentation de rapport](ui-how-create-custom-report-layout.md#MakeChangesToLayout).

      Les présentations de rapport RDLC sont plus avancées que les présentations de rapport Word. Pour plus d'informations sur la modification d'une présentation de rapport RDLC, voir [Création de présentations de rapport RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).

      Pensez à enregistrer vos modifications une fois effectuées.

4.  Retournez à la page **Présentations état personnalisées**, sélectionnez la présentation d'état que vous avez exportée et modifiée, puis choisissez l'action **Importer présentation**.  

5. Dans la boîte de dialogue **Importer**, sélectionnez **Choisir** pour rechercher et sélectionner le document de présentation d'état, puis choisissez **Ouvrir**.

##  <a name="create-and-modify-custom-report-layouts"></a><a name="MakeChangesToLayout"></a> Créer et modifier des présentations de rapport personnalisées

Pour apporter des modifications générales de mise en forme et de disposition (par exemple modifier la police texte, ajouter et modifier un tableau ou supprimer un champ de données), utilisez les fonctions de base d'édition de Word, tout comme vous le faites avec n'importe quel document Word.

Si vous créez une présentation de rapport Word de A à Z ou en ajoutant de nouveaux champs de données, commencez par ajouter un tableau comprenant des lignes et colonnes qui finiront par contenir les champs de données.

> [!TIP]  
> Affiche les quadrillages de façon à visualiser les contours des cellules de la table. Pensez à masquer les quadrillages lorsque vous avez terminé l'édition. Pour masquer ou afficher des quadrillages dans la table, sélectionnez la table, puis sous **Mise en page** sous l'onglet **Table**, sélectionnez **Afficher les quadrillages**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Incorporation de polices dans des présentations Word pour des raisons de cohérence

Pour vous assurer que les états affichent et impriment toujours avec les polices prévues, quel que soit l'emplacement où les utilisateurs ouvrent ou impriment des états, vous pouvez incorporer des polices au document Word. Toutefois, sachez qu'incorporer des polices peut augmenter de façon significative la taille des fichiers Word. Pour plus d'informations sur l'incorporation de polices à Word, voir [Incorporer des polices à Word, PowerPoint ou Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="removing-label-and-data-fields-in-word-layouts"></a><a name="RemoveField"></a> Suppression des champs d'étiquette et de données dans les présentations Word

 L'étiquette les champs de données d'un état sont contenus dans des contrôles de contenu dans Word. La figure ci-après illustre un contrôle de contenu lorsqu'il est sélectionné dans le document Word.  

 ![Contrôle de contenu d'un champ dans une présentation état Word](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 Le nom de l'étiquette ou le nom du champ de données s'affiche dans le contrôle de contenu. Dans l'exemple, le nom du champ est CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>Pour supprimer un champ étiquette ou données  

1. Cliquez avec le bouton droit sur le champ que vous voulez supprimer, puis choisissez **Supprimer le contrôle de contenu**.  

     Le contrôle de contenu est supprimé, mais le nom du champ reste sous forme de texte.  

2. Supprimez le texte restant selon vos besoins.  

### <a name="adding-data-fields"></a>Ajout de champs de données

L'ajout de champs de données à partir d'un ensemble des données d'état est une fonction plus avancée qui exige des connaissances sur l'ensemble des données d'état. Pour plus d'informations sur l'ajout de champs pour les données, étiquettes et images, voir [Ajouter des champs à une présentation de rapport Word](ui-how-add-fields-word-report-layout.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Gestion des présentations de rapport](ui-manage-report-layouts.md)  
[Modifier la présentation actuelle de l'état](ui-how-change-layout-currently-used-report.md)  
[Importer et exporter une présentation d'état ou de document personnalisée](ui-how-import-and-export-report-layout.md)  
[Utilisation des états, des traitements par lots et des XMLports](ui-work-report.md)  
[Préparer la génération d'états financiers avec des tableaux d'analyse et des catégories de compte](bi-how-work-account-schedule.md) 
[Veille économique](bi.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
