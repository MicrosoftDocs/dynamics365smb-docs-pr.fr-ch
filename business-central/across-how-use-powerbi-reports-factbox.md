---
title: Afficher des états Power BI personnalisés| Microsoft
description: Vous pouvez utiliser des états Power BI pour obtenir des informations supplémentaires sur les données dans les listes.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 29c7b7656632d2103a16025848a6ddc82650353e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241617"
---
# <a name="viewing-list-data-in-power-bi-reports-in-business-central"></a>Affichage des données de liste des états Power BI dans Business Central 
[!INCLUDE[d365fin](includes/d365fin_md.md)] inclut un élément de contrôle Récapitulatif sur un certain nombre de pages Liste des clés fournissant des informations supplémentaires sur les données de la liste. Lorsque vous vous déplacez entre les lignes de la liste, l'état est mis à jour et filtré pour l'écriture sélectionnée. Vous pouvez créer des états personnalisés pour qu'ils s'affichent dans ce contrôle, mais il y a certaines règles à suivre lors de la création des états pour s'assurer qu'ils adoptent le comportement souhaité.  

> [!NOTE]  
>   Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Power BI. En outre, vous devez télécharger [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Pour plus d'informations, voir [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="report-data-set"></a>Ensemble de données d'état
Lorsque vous créez l'état dans Power BI Desktop, spécifiez la source de données ou le service Web qui contient les données concernant la liste que vous souhaitez associer à l'état. Par exemple, si vous souhaitez créer un état pour la liste Ventes, assurez-vous que l'ensemble des données contient les informations liées aux ventes.  

Pour filtrer des données sur les états en fonction de l'enregistrement sélectionné dans la page de liste, la clé primaire doit être utilisée comme filtre d'état. Les clés primaires devront faire partie de votre ensemble de données pour que les états soient filtrés correctement. Dans la plupart des cas, la clé primaire de la liste est **N°** .  

## <a name="defining-the-report-filter"></a>Définition du filtre d'état
L'état est nécessaire pour avoir un filtre d'état de base (pas une page ou un filtre visuel, ni un filtre avancé) pour filtrer correctement dans le contrôle Récapitulatif État Power BI. Le filtre qui est transmis à l'état Power BI de chaque page de liste est basé sur la clé primaire, comme décrit dans la section précédente.  

Pour définir un filtre pour l'état, sélectionnez la clé primaire dans la liste des champs disponibles, puis faites glisser ce champ dans la section **Filtre d'état**.  

![Définition du filtre d'état pour l'état Activités Facture vente](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="report-size-and-color"></a>Taille et couleur de l'état
La taille de l'état doit être configurée sur 325 pixels par 310 pixels. Cette opération est requise pour la mise à l'échelle appropriée de l'état dans l'espace disponible autorisé par le contrôle Récapitulatif État Power BI. Pour définir la taille de l'état, placez le focus en dehors de la zone de présentation d'état, puis choisissez l'icône en forme de rouleau de peinture.

![Définition de la largeur et de la hauteur de l'état pour l'état Activités Facture vente](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

Vous pouvez modifier la largeur et la hauteur de l'état en choisissant **Personnalisé** dans le champ **Type**.

De même, si vous souhaitez que l'arrière-plan de l'état se fonde avec la couleur de l'arrière-plan du contrôle Récapitulatif État Power BI, définissez une couleur d'arrière-plan d'état personnalisé de *E5E5E5*. Cette option est facultative.  

## <a name="reports-with-multiple-pages"></a>États avec plusieurs pages
Avec Power BI, vous pouvez créer un seul état avec plusieurs pages. Les visuels que vous souhaitez visualiser dans les pages de liste [!INCLUDE[d365fin](includes/d365fin_md.md)] doivent se trouver sur la première page de l'état dans Power BI.  

> [!NOTE]  
>  Le contrôle Récapitulatif État Power BI affiche uniquement la première page de votre état, pour afficher d'autres pages, vous devez développer l'état et utiliser les onglets situés en bas pour accéder aux autres pages.  

## <a name="saving-your-report"></a>Enregistrement de votre état

Lorsque vous enregistrez votre état, il est recommandé que son nom contienne celui de la page de liste dans laquelle vous souhaitez l'afficher. Par exemple, le mot *Fournisseur* doit se trouver quelque part dans le nom des états que vous souhaitez rendre disponibles dans la liste Fournisseurs.  

Cela n'est pas obligatoire mais ça va accélérer le processus de sélection des états. Lorsque la page de sélection de l'état est ouverte à partir d'une page de liste, nous transférons un filtre basé sur le nom de la page pour limiter les états qui s'affichent.  Vous pouvez supprimer le filtre pour obtenir la liste complète des états disponibles dans Power BI.  

## <a name="troubleshooting"></a>Incident
Cette section fournit une solution de rechange pour les problèmes les plus courants qui apparaissent lorsque vous créez l'état Power BI.  

**L'utilisateur ne voit pas l'état sur la page Sélectionner un état qu'il veut sélectionner** Si vous ne pouvez pas sélectionner un état, une solution consiste à vérifier son nom pour vous assurer qu'il contient le nom de la page de liste. Vous pouvez aussi effacer le filtre pour obtenir la liste complète des états disponibles dans Power BI.  

**L'état est chargé mais il est vide, non filtré ou filtré incorrectement** Vérifiez que le filtre de l'état contient la bonne clé primaire. Dans la plupart des cas, il s'agit du champ **N°**, mais dans la table **Écriture comptable**, vous devez utiliser le champ **N° écriture**.

**L'état est chargé, mais il affiche une page non souhaitée** Vérifiez que la page que vous souhaitez afficher est la première page de votre état.  

**L'état apparaît avec des bordures grises non désirées, il est trop petit ou trop grand**

Vérifiez que la taille de l'état est configurée sur 325 pixels x 310 pixels. Enregistrez l'état, puis actualisez la page de liste.  

## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)  
[Mise en route](product-get-started.md)    
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)    
[Finances](finance.md)  
