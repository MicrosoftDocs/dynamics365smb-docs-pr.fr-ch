---
title: Configuration d&quot;axes| Microsoft Docs
description: "Vous pouvez définir les axes et les sections analytiques que vous souhaitez utiliser pour classer des feuilles et des documents par catégorie, comme des commandes vente et achat."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/28/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0da77c5be3b49f715384752ad61fc072aea8525c
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-dimensions"></a>Configuration d'axes
Vous pouvez définir les axes et les sections analytiques pour classer des feuilles et des documents par catégorie, comme des commandes vente et achat. La fenêtre **Axes analytiques** permet de créer une ligne pour chaque axe, par exemple *Projet*, *Département*, *Zone* et *Commercial*.

Vous pouvez également définir des valeurs pour des axes. Il peut par exemple s'agir de départements de votre société. Les sections analytiques peuvent être paramétrées sous forme de structure hiérarchique similaire au plan comptable, de manière à ce que les données puissent être réparties en plusieurs niveaux de granularité et à ce que des sous-ensembles de sections analytiques puissent être totalisés. Vous pouvez définir autant d'axes et de sections analytiques que nécessaire, tous les membres de votre société peuvent les utiliser.

Vous pouvez également configurer des axes principaux et des raccourcis axe :  

* Les **axes principaux** sont utilisés comme filtres, dans les états et les traitements par lots. Vous pouvez uniquement utiliser deux axes principaux, choisissez donc des axes que vous utilisez souvent.
* Les **raccourcis axe** sont disponibles sous forme de champ dans les lignes feuille et document. Vous pouvez en créer six au maximum.  

**Remarque** : Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**. Pour plus d'informations, voir [Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Configurer des axes analytiques par défaut pour les clients, les fournisseurs, et d'autres comptes
Vous pouvez attribuer un axe analytique par défaut pour un compte spécifique. L'axe est copié sur la feuille ou le document lorsque vous saisissez le numéro de compte dans une ligne, mais vous pouvez supprimer ou modifier le code sur la ligne si nécessaire. Vous pouvez également rendre un axe analytique obligatoire pour valider une écriture avec un type de compte spécifique.  

## <a name="translate-the-names-of-dimensions"></a>Traduire le nom des axes
Lorsque vous créez un axe analytique, et notamment un raccourci axe, ce que vous créez réellement est un en-tête personnalisé de champ ou de colonne. Si votre activité est internationale, vous pouvez fournir des traductions pour le nom de l'axe. Les documents qui contiennent l'axe utiliseront le nom traduit, le cas échéant.   

## <a name="example"></a>Exemple :
Imaginons que votre société souhaite suivre les transactions selon la structure organisationnelle et les situations géographiques. Pour ce faire, vous pouvez configurer deux axes dans la fenêtre **Axe analytique** :

* **REGION**  
* **DEPARTEMENT**  

| Code | Name | Libellé code | Libellé filtre |
| --- | --- | --- | --- |
| REGION |Région |Zone de recouvrement |Filtre zone |
| DEPARTEMENT |Département |Code emplacement immo |Filtre département |

Pour **ZONE**, vous pouvez ajouter les sections analytiques suivantes :

| Code | Name | Type section |
| --- | --- | --- |
| 10 |Amériques |Début total |
| 2.0 |Amérique du Nord |Standard |
| 30 |Pacifique |Standard |
| 40 |Amérique du Sud |Standard |
| 50 |Amériques, Total |Fin total |
| 60 |Europe |Début total |
| 70 |INTRA |Standard |
| 80 |Non-UE |Standard |
| 90 |Europe, Total |Fin total |

Pour les deux zones géographiques principales, Amériques et Europe, ajoutez des sous-catégories pour les régions en mettant les sections analytiques en retrait. Cela vous permet de déclarer les ventes ou les dépenses dans les régions, et d'obtenir les totaux des zones géographiques plus étendues. Vous pouvez également choisir d'utiliser les pays ou les régions en tant que sections analytiques, ou des régions ou des villes, en fonction de votre entreprise.  
**Remarque** : pour configurer une hiérarchie, veillez à trier les codes dans l'ordre alphabétique. Ceci inclut les codes des sections analytiques fournis dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Pour **DÉPARTEMENT**, vous pouvez ajouter les sections analytiques suivantes :

| Code | Name | Type section |
| --- | --- | --- |
| ADMIN |Administration |Standard |
| FABR |Fabrication |Standard |
| VENTES |Ventes |Standard |

Avec ce paramétrage, vous devez ensuite ajouter les deux axes en tant qu'axes analytiques principaux dans la fenêtre **Paramètres comptabilité**. Cela signifie que vous pouvez utiliser ZONE et DÉPARTEMENT comme filtres pour les écritures comptables de la comptabilité, ainsi que dans tous les états et les tableaux d'analyse. Les deux axes principaux sont mis à disposition automatiquement pour être utilisés dans les lignes écriture et les en-têtes document comme raccourcis axe.  

Avec ce paramétrage, vous pouvez commencer à ajouter des axes analytiques aux documents et aux feuilles. Pour plus d'informations, voir [Axes analytiques](finance-dimensions.md).  

## <a name="see-also"></a>Voir aussi
[Axes analytiques](finance-dimensions.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

