---
title: Afficher les états Power BI personnalisés pour les données Business Central | Microsoft Docs
description: Vous pouvez utiliser des états Power BI pour obtenir des informations supplémentaires sur les données dans les listes.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 04c0c5d203e78c2ae0be48609a5ee90f45b83c6f
ms.sourcegitcommit: 0fb6952376d853a878ed33257e73aadc03b95572
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968401"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prodshort"></a>Création d’états Power BI pour afficher les données de liste dans [!INCLUDE[prodshort](includes/prodshort.md)]

[!INCLUDE[prodlong](includes/prodlong.md)] inclut un élément de contrôle Récapitulatif sur un certain nombre de pages Liste des clés fournissant des informations supplémentaires sur les données de la liste. Lorsque vous vous déplacez entre les lignes de la liste, l’état est mis à jour et filtré pour l’écriture sélectionnée. Vous pouvez créer des états personnalisés à afficher dans ce contrôle. Cependant, il y a quelques règles à suivre pour s’assurer que les états fonctionnent comme prévu.  

## <a name="prerequisites"></a>Conditions préalables

- Un compte Power BI.
- Power BI Desktop.

Pour plus d’informations sur la mise en route, voir [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md).

## <a name="defining-the-report-data-set"></a>Définition de l’ensemble de données d’état

Spécifiez la source de données qui contient les données liées à la liste. Par exemple, pour créer un état pour la liste Ventes, assurez-vous que l’ensemble des données contient les informations liées aux ventes.  

## <a name="defining-the-report-filter"></a>Définition du filtre d’état

Pour mettre à jour les données de l’enregistrement sélectionné dans la liste, vous ajoutez un filtre à l’état. Le filtre doit inclure un champ de la source de données utilisée comme *clé primaire* . Dans la plupart des cas, la clé primaire de la liste est **N°** .

Pour définir un filtre pour l’état, sélectionnez la clé primaire dans la liste des champs disponibles, puis faites glisser ce champ dans la section **Filtre d’état** . Le filtre doit être un filtre de rapport de base défini pour toutes les pages. Il ne peut pas s’agir d’un filtre de page, visuel ou avancé.

![Définition du filtre d’état pour l’état Activités Facture vente](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a>Définition de la taille et de la couleur de l’état

La taille de l’état doit être configurée sur 325 pixels par 310 pixels. Cette taille offre une mise à l’échelle appropriée de l’état dans l’espace disponible du contrôle Récapitulatif Power BI dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour définir la taille de l’état, placez le focus en dehors de la zone de présentation d’état, puis choisissez l’icône en forme de rouleau de peinture.

![Définition de la largeur et de la hauteur de l’état pour l’état Activités Facture vente](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Vous pouvez modifier la largeur et la hauteur de l’état en choisissant **Personnalisé** dans le champ **Type** .

Si vous souhaitez que l’arrière-plan de l’état se fonde avec la couleur de l’arrière-plan du contrôle Récapitulatif Power BI, définissez une couleur d’arrière-plan d’état personnalisé de *#FFFFFF* . 

## <a name="using-reports-with-multiple-pages"></a>Utilisation des états avec plusieurs pages

Avec Power BI, vous pouvez créer un seul état avec plusieurs pages. Cependant, pour les états qui s’affichent avec des pages de liste, nous recommandons une seule page. Le Récapitulatif Power BI n’affiche que la première page de votre état.

## <a name="naming-the-report"></a>Définition du nom de l’état

Donnez à l’état un nom contenant le nom de la page de liste associée à l’état. Par exemple, si l’état concerne la page de liste **Fournisseur** , incluez le mot *fournisseur* quelque part dans le nom.  

Cette convention de désignation de nom n’est pas obligatoire. Cependant, il permet de sélectionner plus rapidement des états dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lorsque la page de sélection de l’état s’ouvre à partir d’une page de liste, elle est automatiquement filtrée en fonction du nom de la page. Ce filtrage est effectué pour limiter les états affichés. Vous pouvez aussi effacer le filtre pour obtenir la liste complète des états disponibles dans Power BI.  

## <a name="fixing-problems"></a>Résolution des problèmes

Cette section fournit une solution de rechange pour les problèmes les plus courants qui apparaissent lorsque vous créez l’état Power BI.  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a>Vous ne pouvez pas voir d’état sur la page Sélectionner un état.

C’est probablement parce que le nom de l’état ne contient pas le nom de la page de liste. Effacez le filtre pour obtenir la liste complète des états disponibles dans Power BI.  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>L’état est chargé, mais vide, non filtré ou filtré incorrectement.

Vérifiez que le filtre de l’état contient la bonne clé primaire. Dans la plupart des cas, il s’agit du champ **N°** , mais dans la table **Écriture comptable** , vous devez utiliser le champ **N° écriture** .

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>L’état est chargé, mais il affiche une page à laquelle vous ne vous attendiez pas.

Vérifiez que la page que vous souhaitez afficher est la première page de votre état.  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>L’état apparaît avec des bordures grises non désirées, il est trop petit ou trop grand.

Vérifiez que la taille de l’état est configurée sur 325 pixels x 310 pixels. Enregistrez l’état, puis actualisez la page de liste.  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Activation de vos données métier pour Power BI](admin-powerbi.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)  
[Mise en route](product-get-started.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finances](finance.md)  
