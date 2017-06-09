---
title: Axes analytiques| Microsoft Docs
description: "Utilisation des axes analytiques pour l&quot;analyser des données."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7552ee2b3398c203a7f3295f3203c83914fbb15f
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="dimensions"></a>Axes analytiques
Vous pouvez utiliser des axes analytiques pour faciliter l'exécution de l'analyse sur des commandes vente, par exemple. Les axes analytiques sont des attributs et des valeurs qui permettent de catégoriser les écritures afin de pouvoir les suivre et les analyser. Ils peuvent par exemple indiquer de quel projet ou département provient une écriture.  

Vous pouvez également utiliser des axes au lieu de configurer des comptes généraux séparés pour chaque département et projet. Cela donne une bonne opportunité d'analyse, sans créer de plan comptable complexe.  

Un autre exemple consiste à configurer un axe analytique appelé *Département* et utiliser cet axe lorsque vous validez des documents vente. Cela vous permet d'utiliser les outils de veille économique pour savoir quel département a vendu quels articles.
Plus vous utilisez d'axes analytiques, plus vous pouvez baser vos décisions commerciales sur des états détaillés. Par exemple, une seule écriture vente peut comporter plusieurs informations analytiques :  

* Le compte sur lequel la vente de l'article a été validée  
* L'endroit où l'article a été vendu
* Le nom du vendeur
* Le type de client qui a effectué l'achat  

Vous pouvez créer autant d'axes avec autant de valeurs que vous le souhaitez.  

**Remarque** : Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**. Pour plus d'informations, voir [Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="using-dimensions"></a>Utilisation des axes analytiques
Dans un document tel qu'une commande vente, vous pouvez ajouter des informations analytiques pour une seule ligne document et pour le document lui-même. Par exemple, dans la fenêtre **Commande vente**, vous pouvez saisir des sections analytiques pour les deux premiers raccourcis axe directement sur les lignes vente individuelles et ajouter des informations analytiques complémentaires si vous cliquez sur le bouton **Axes analytiques**.  

Si vous travaillez plutôt sur une feuille, vous pouvez également ajouter à une écriture des informations analytiques de la même manière, si vous avez configuré des raccourcis axe en tant que champs directement dans les lignes feuille.  

Vous pouvez configurer des axes analytiques par défaut pour des comptes ou des types de compte, de sorte que les axes et les sections analytiques soient renseignés automatiquement.  

## <a name="dimension-sets"></a>Ensembles de dimensions
Un ensemble de dimensions est une combinaison unique de sections analytiques. Il est stocké comme des écritures de l'ensemble de dimensions dans la base de données. Chaque écriture de l'ensemble de dimensions représente une section analytique unique. L'ensemble de dimensions est identifié par un ID courant, qui est affecté à chaque écriture correspondante qui appartient à l'ensemble de dimensions.  

Lorsque vous créez une ligne de feuille, un en-tête de document ou une ligne de document, vous pouvez spécifier une combinaison de sections analytiques. Au lieu d'enregistrer explicitement chaque section analytique dans la base de données, un ID d'ensemble de dimensions est affecté à la ligne de feuille, à l'en-tête du document ou à la ligne du document pour spécifier l'ensemble de dimensions.  

## <a name="see-also"></a>Voir aussi
[Finance](finance.md)  
[Configuration d'axes](finance-setup-dimensions.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

