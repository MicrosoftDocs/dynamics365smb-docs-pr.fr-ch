---
title: "Procédure d'ajout de champs à une présentation de rapport Word | Microsoft Docs"
description: "Décrit comment ajouter des champs d'un ensemble de données de rapport à une présentation de rapport Word existante pour un rapport."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 2a3ff313d9c6e8bac1169daba590d2e38c312d87
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="add-fields-to-a-word-report-layout"></a>Ajouter des champs à une présentation de rapport Word
Un ensemble de données de rapport peut être constitué de champs affichant des étiquettes, des données et des images. Cette rubrique décrit la procédure pour ajouter des champs d'un ensemble de données de rapport à une présentation de rapport Word pour un rapport. Vous ajoutez des champs à l'aide du composant XML personnalisé Word pour l'état et en ajoutant des contrôles de contenu qui correspondent aux champs de l'ensemble de données d'état. L'ajout de champs requiert que vous ayez des connaissances sur l'ensemble des données de rapport afin que vous puissiez identifier les champs que vous souhaitez ajouter à la présentation.  
  
> [!NOTE]  
>  Vous ne pouvez pas modifier les présentations de rapport intégrées<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

##  <a name="OpenXMLPart"></a>Pour ouvrir le composant XML personnalisé de l'état dans Word  
  
1.  Si ce n'est pas déjà le cas, ouvrez le document de présentation de rapport Word dans Word.  
  
     Pour plus d'informations, voir [Créer et modifier une présentation de rapport personnalisée](ui-how-create-custom-report-layout.md).  
  
2.  Afficher l'onglet **Développeur** dans le ruban de Microsoft Word.  
  
     Par défaut, l'onglet **Développeur** n'est pas affiché dans le ruban. Pour plus d'informations, voir [Afficher l'onglet Développeur sur le ruban](https://go.microsoft.com/fwlink/?LinkID=389631).  
  
3.  Sous l'onglet **Développeur**, sélectionnez **Volet de mappage XML**.  
  
4.  Dans le volet **Mappage XML**, dans la liste déroulante **Partie XML personnalisée**, choisissez la partie XML personnalisée pour le rapport ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->, qui est généralement le dernier de la liste. Le nom de la partie XML personnalisée présente le format suivant :  
  
     urn:microsoft-dynamics-nav/reports/*report_name*/*ID*  
  
     *report_name* est le nom qui est affecté au rapport<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.  
  
     *ID* est le numéro d'identification de l'état.  
  
     Après avoir sélectionné la partie XML personnalisée, le volet de mappage XML affiche les étiquettes et les contrôles de champ disponibles pour le rapport.  
  
### <a name="to-add-a-label-or-data-field"></a>Pour ajouter un champ étiquette ou données  
  
1.  Placez votre curseur dans le document dans lequel vous souhaitez ajouter le contrôle.  
  
2.  Dans le volet **Mappage XML**, cliquez avec le bouton droit sur le contrôle que vous souhaitez ajouter, sélectionnez **Insérer contrôle de contenu**, puis sélectionnez **Texte brut**.  
  
    > [!NOTE]  
    >  Vous ne pouvez pas ajouter un champ en tapant manuellement le nom du champ de l'ensemble de données dans le contrôle de contenu. Vous devez utiliser le volet **Mappage XML** pour mapper les champs.  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a>Pour ajouter des lignes à répétition des champs de données pour créer une liste  
  
1.  Dans un tableau, ajoutez une ligne de tableau incluant une colonne pour chaque champ dont vous souhaitez qu'il soit répété.  
  
     Cette ligne agira comme un espace réservé pour les champs de répétition.  
  
2.  Sélectionnez toute la ligne.  
  
3.  Dans le volet **Mappage XML**, cliquez avec le bouton droit sur le contrôle qui correspond à l'élément de données de rapport qui contient les champs que vous souhaitez voir répétés, sélectionnez **Insérer contrôle de contenu**, puis sélectionnez **Répéter**.  
  
4.  Ajoutez les champs de répétition à la ligne comme suit :  
  
    1.  Placez votre pointeur dans une colonne.  
  
    2.  Dans le volet **Mappage XML**, cliquez avec le bouton droit sur le contrôle que vous souhaitez ajouter, sélectionnez **Insérer contrôle de contenu**, puis sélectionnez **Texte brut**.  
  
    3.  Pour chaque champ, répétez les étapes a et b.  
  
## <a name="adding-image-fields"></a>Ajout de champs d'image  
 Un ensemble de données de rapport peut inclure un champ qui contient une image, par exemple un logo de la société ou une photo d'un article. Pour ajouter une image de l'ensemble de données d'état, vous insérez un contrôle de contenu **Image**.  
  
 Les images s'alignent dans le coin supérieur gauche du contrôle de contenu et sont automatiquement redimensionnés proportionnellement conformément à la limite du contrôle de contenu.  
  
> [!IMPORTANT]  
>  Vous ne pouvez ajouter que des images dont le format est pris en charge par Word (par ex., .bmp, .jpeg et .png). Si vous ajoutez une image dont le format n'est pas pris en charge par Word, vous obtenez une erreur lorsque vous exécutez le rapport à partir du client ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->.  
  
#### <a name="to-add-an-image"></a>Pour ajouter une image  
  
1.  Placez votre pointeur dans le document dans lequel vous souhaitez ajouter le contrôle.  
  
2.  Dans le volet **Mappage XML**, cliquez avec le bouton droit sur le contrôle que vous souhaitez ajouter, sélectionnez **Insérer contrôle de contenu**, puis sélectionnez **Image**.  
  
3.  Pour développer ou réduire la taille de l'image, faites glisser une poignée de redimensionnement pour l'éloigner ou la rapprocher du centre du contrôle de contenu.  

## <a name="custom-xml-part-overview"></a>Aperçu des parties XML personnalisées
Les présentations de rapport Word sont basées sur des *parties XML personnalisées*. Une partie XML personnalisée pour un rapport regroupe des éléments qui correspondent aux éléments de données, colonnes et étiquettes comprenant l'ensemble de données du rapport. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->La partie XML personnalisée est utilisée pour associer les données dans un rapport lorsque le rapport est exécuté.

  
### <a name="xml-structure-of-custom-xml-part"></a>Structure XML du composant XML personnalisé  
Le tableau suivant fournit un aperçu simplifié du XML d'une partie XML personnalisée.  
  
|Éléments XML|Désignation|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|En-tête|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|Spécification de l'espace de noms XML. `<reportname>` est le nom affecté au rapport. `<id>` est l'identifiant affecté au rapport.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Contient toutes les étiquettes pour le rapport.<!--OnPren The element includes labels that are related to columns that have the [IncludeCaption Property](../FullExperience/Name%20Property-duplicate.md).--><br />-   Les éléments d'étiquette associés aux colonnes sont au format `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />-  Les éléments d'étiquette sont au format `<LabelName>LabelName</LableName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Les étiquettes sont répertoriées par ordre alphabétique.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Données article et colonnes de haut niveau. Les colonnes sont répertoriées par ordre alphabétique.<!--OnPrem <br /><br /> The element names and values are determined by the [Name Property-duplicate](../FullExperience/Name%20Property-duplicate.md) of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Les données article et colonnes imbriquées dans les données article de haut niveau. Les colonnes sont répertoriées par ordre alphabétique sous chaque donnée.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Élément de clôture.|  
  
### <a name="custom-xml-part-in-word"></a>Partie XML personnalisée dans Word  
 Dans Word, vous ouvrez la partie XML personnalisée dans le volet **Mappage XML** puis utilisez le volet pour mapper les éléments aux contrôles de contenu dans le document Word. Le volet **Mappage XML** est accessible depuis l'onglet **Développeur** (pour plus d'informations, voir [Afficher l'onglet Développeur sur le ruban](https://go.microsoft.com/fwlink/?LinkID=389631)).  
  
 Les éléments figurant dans le volet de **Mappage XML** s'affichent dans une structure qui est similaire à la source XML. Les champs d'étiquette sont rassemblés sous un élément **Étiquettes** commun et les données article et colonnes sont organisées dans une structure hiérarchique qui correspond à la source XML, avec les colonnes répertoriées dans l'ordre alphabétique. Les éléments sont identifiés par leur nom tel que défini par la propriété Name dans Report Dataset Designer dans ADD INCLUDE<!--[!INCLUDE[nav_dev_short](../../includes/nav_dev_short_md.md)]-->.  
  
 La figure ci-après illustre la partie XML personnalisée simple de la section précédente dans le volet **Mappage XML** d'un document Word.  
  
 ![Clip du volet Mappage XML dans Word](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
-   Pour ajouter une étiquette ou un champ à la présentation, vous insérez un contrôle de contenu qui correspond à l'élément dans le volet **Mappage XML**.  
  
-   Pour créer des lignes de colonnes à répétition, insérez un contrôle de contenu **Répétition** pour l'élément d'article parent, puis ajoutez le contrôle de contenu pour les colonnes.  
  
-   Pour les étiquettes, le texte qui apparaît dans le rapport généré est la valeur de la propriété **Légende** pour le champ dans le tableau données d'article (si l'étiquette est liée à la colonne dans l'ensemble des données de rapport) ou une étiquette dans le Report Label Designer (si l'étiquette n'est pas liée à une colonne dans l'ensemble de données).  
  
-   La langue de l'étiquette qui s'affiche lorsque vous exécutez l'état dépend du paramétrage de langue de l'objet d'état. <!--OnPrem For more information, see [Multiple Document Languages](../FullExperience/Viewing%20the%20Application%20in%20Different%20Languages.md).-->  
  
## <a name="see-also"></a>Voir aussi  
 [Créer et modifier une présentation de rapport personnalisée](ui-how-create-custom-report-layout.md)   
