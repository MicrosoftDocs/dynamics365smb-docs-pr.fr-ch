---
title: Utiliser les axes analytiques| Microsoft Docs
description: "Utilisez les axes analytiques pour classer des écritures par catégorie, par exemple, par service ou le projet, afin de facilement suivre et analyser les données."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/16/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b7b69b3419520c482cbe6a84494bbac7ef35bea1
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="working-with-dimensions"></a>Utilisation des axes analytiques
Vous pouvez utiliser des axes analytiques pour faciliter l'exécution de l'analyse sur des commandes vente, par exemple. Les axes analytiques sont des attributs et des valeurs qui permettent de catégoriser les écritures afin de pouvoir les suivre et les analyser. Ils peuvent par exemple indiquer de quel projet ou département provient une écriture.  

Vous pouvez également utiliser des axes au lieu de configurer des comptes généraux séparés pour chaque département et projet. Cela donne une bonne opportunité d'analyse, sans créer de plan comptable complexe. Pour plus d'informations, reportez-vous à [Veille économique](bi.md).

Un autre exemple consiste à configurer un axe analytique appelé *Département* et utiliser cet axe lorsque vous validez des documents vente. Cela vous permet d'utiliser les outils de veille économique pour savoir quel département a vendu quels articles.
Plus vous utilisez d'axes analytiques, plus vous pouvez baser vos décisions commerciales sur des états détaillés. Par exemple, une seule écriture vente peut comporter plusieurs informations analytiques :  

* Le compte sur lequel la vente de l'article a été validée  
* L'endroit où l'article a été vendu
* Le nom du vendeur
* Le type de client qui a effectué l'achat  

> [!NOTE]  
>   Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**. Pour plus d'informations, voir [Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="analyzing-by-dimensions"></a>Analyse par axe analytique
La fonctionnalité Axes analytiques joue un rôle important dans la veille économique, par exemple en définissant des vues d'analyse. Pour plus d'informations, reportez vous à [Procédure : analyser des données par axe analytique](bi-how-analyze-data-dimension.md).

## <a name="dimension-sets"></a>Ensembles de dimensions
Un ensemble de dimensions est une combinaison unique de sections analytiques. Il est stocké comme des écritures de l'ensemble de dimensions dans la base de données. Chaque écriture de l'ensemble de dimensions représente une section analytique unique. L'ensemble de dimensions est identifié par un ID courant, qui est affecté à chaque écriture correspondante qui appartient à l'ensemble de dimensions.  

Lorsque vous créez une ligne de feuille, un en-tête de document ou une ligne de document, vous pouvez spécifier une combinaison de sections analytiques. Au lieu d'enregistrer explicitement chaque section analytique dans la base de données, un ID d'ensemble de dimensions est affecté à la ligne de feuille, à l'en-tête du document ou à la ligne du document pour spécifier l'ensemble de dimensions.  

## <a name="setting-up-dimensions"></a>Configuration d'axes
Vous pouvez définir les axes et les sections analytiques pour classer des feuilles et des documents par catégorie, comme des commandes vente et achat. La fenêtre **Axes analytiques** permet de créer une ligne pour chaque axe, par exemple *Projet*, *Département*, *Zone* et *Commercial*.

Vous pouvez également définir des valeurs pour des axes. Il peut par exemple s'agir de départements de votre société. Les sections analytiques peuvent être paramétrées sous forme de structure hiérarchique similaire au plan comptable, de manière à ce que les données puissent être réparties en plusieurs niveaux de granularité et à ce que des sous-ensembles de sections analytiques puissent être totalisés. Vous pouvez définir autant d'axes et de sections analytiques que nécessaire, tous les membres de votre société peuvent les utiliser.

Vous pouvez également configurer des axes principaux et des raccourcis axe :  

* Les **axes principaux** sont utilisés comme filtres, dans les états et les traitements par lots. Vous pouvez uniquement utiliser deux axes principaux, choisissez donc des axes que vous utilisez souvent.
* Les **raccourcis axe** sont disponibles sous forme de champ dans les lignes feuille et document. Vous pouvez en créer six au maximum.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Paramétrage des axes analytiques par défaut pour les clients, les fournisseurs, et d'autres comptes
Vous pouvez attribuer un axe analytique par défaut pour un compte spécifique. L'axe est copié sur la feuille ou le document lorsque vous saisissez le numéro de compte dans une ligne, mais vous pouvez supprimer ou modifier le code sur la ligne si nécessaire. Vous pouvez également rendre un axe analytique obligatoire pour valider une écriture avec un type de compte spécifique.  

### <a name="translating-the-names-of-dimensions"></a>Traduction des nom des axes analytiques
Lorsque vous créez un axe analytique, et notamment un raccourci axe, ce que vous créez réellement est un en-tête personnalisé de champ ou de colonne. Si votre activité est internationale, vous pouvez fournir des traductions pour le nom de l'axe. Les documents qui contiennent l'axe utiliseront le nom traduit, le cas échéant.   

### <a name="example-of-dimension-setup"></a>Exemple de paramétrage d'axe analytique
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
> [!NOTE]  
>   Pour configurer une hiérarchie, veillez à trier les codes dans l'ordre alphabétique. Ceci inclut les codes des sections analytiques fournis dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Pour **DÉPARTEMENT**, vous pouvez ajouter les sections analytiques suivantes :

| Code | Name | Type section |
| --- | --- | --- |
| ADMIN |Administration |Standard |
| FABR |Fabrication |Standard |
| VENTES |Ventes |Standard |

Avec ce paramétrage, vous devez ensuite ajouter les deux axes en tant qu'axes analytiques principaux dans la fenêtre **Paramètres comptabilité**. Cela signifie que vous pouvez utiliser ZONE et DÉPARTEMENT comme filtres pour les écritures comptables de la comptabilité, ainsi que dans tous les états et les tableaux d'analyse. Les deux axes principaux sont mis à disposition automatiquement pour être utilisés dans les lignes écriture et les en-têtes document comme raccourcis axe.  

## <a name="using-dimensions"></a>Utilisation des axes analytiques
Dans un document tel qu'une commande vente, vous pouvez ajouter des informations analytiques pour une seule ligne document et pour le document lui-même. Par exemple, dans la fenêtre **Commande vente**, vous pouvez saisir des sections analytiques pour les deux premiers raccourcis axe directement sur les lignes vente individuelles et ajouter des informations analytiques complémentaires si vous cliquez sur le bouton **Axes analytiques**.  

Si vous travaillez plutôt sur une feuille, vous pouvez également ajouter à une écriture des informations analytiques de la même manière, si vous avez configuré des raccourcis axe en tant que champs directement dans les lignes feuille.  

Vous pouvez configurer des axes analytiques par défaut pour des comptes ou des types de compte, de sorte que les axes et les sections analytiques soient renseignés automatiquement.  

## <a name="see-also"></a>Voir aussi
[Veille économique](bi.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

