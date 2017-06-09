---
title: "Configuration d&quot;une analyse de trésorerie| Microsoft Docs"
description: "Décrit comment configurer les graphiques Cycle trésorerie, Revenus et dépenses, Trésorerie et Prévision de trésorerie pour analyser les mouvements de trésorerie passés et futurs, entrants et sortants de votre société."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.date: 03/28/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e07f32dcc3a50e07c5dea48600f7e3dbcd6088a9
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-cash-flow-analysis"></a>Configuration d'une analyse de trésorerie
Si vous souhaitez de l'aide pour décider quelles opérations effectuer avec votre trésorerie, consultez les graphiques dans le tableau de bord Comptable :  

* **Cycle trésorerie**  
* **Revenus et dépenses**  
* **Trésorerie**  
* **Prévisions de la trésorerie**  

Cette rubrique décrit d'où proviennent les données dans les graphiques et, si nécessaire, quoi faire pour commencer à utiliser les graphiques.  

## <a name="the-cash-cycle-and-income--expense-charts"></a>Les graphiques Cycle trésorerie et Revenus et dépenses
Les graphiques **Cycle trésorerie** et **Revenus et dépenses** sont prêts à être utilisés, en fonction du plan comptable et des tableaux d'analyse. Les données sont issues de ces comptes, et les états financiers calculent les relations entre les ventes et les créances. Certains comptes et états financiers sont fournis. Vous pouvez les utiliser tels quels, les modifier, puis en ajouter de nouveaux. Si vous ajoutez des comptes généraux à votre plan comptable, par exemple, en les important de QuickBooks, vous devez les associer aux comptes sur la page **Tableaux d'analyse** pour les noms de tableaux d'analyse :  

| Nom tableau d'analyse | Emplacement d'utilisation |
| --- | --- |
| **I_CACYCLE** |Cycle trésorerie |
| **I_CASHFLOW** |Trésorerie |
| **I_INCEXP** |Revenus et dépenses |
| **I_MINTRIAL** |Comme compte de gestion si vous n'utilisez pas le plan comptable |

**Remarque** : il est conseillé de conserver les calculs qui sont fournis pour le tableau d'analyse.  

Saisissez les comptes dans le champ **Totalisation** pour **Total produits**, **Total clients**, **Total fournisseurs** et **Stock total**. Pour mapper à une plage de comptes, ou à plusieurs comptes spécifiques, entrez les numéros de compte séparés par « .. ». ou par une barre verticale, respectivement. Par exemple, **1111..4444** ou **2222|3333|5555**.  

**Astuce** : vérifiez votre mappage en choisissant l'option **Aperçu**.  

## <a name="set-up-the-cash-flow-chart"></a>Configurer le plan comptable de trésorerie
Le plan comptable de trésorerie est basé sur ce qui suit :  

* Un plan comptable de trésorerie.
* Un ou plusieurs paramétrages de trésorerie. Ils spécifient les comptes à utiliser pour les écritures comptables, les achats, les ventes, les services et les immobilisations.  

Pour vous aider à poursuivre, certains comptes et paramétrages de trésorerie sont fournis. Vous pouvez en ajouter, en modifier ou en supprimer.  

Pour les configurer, recherchez **comptes de trésorerie**, choisissez le lien, puis renseignez les champs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Répétez ces étapes pour **paramètres trésorerie**.  

## <a name="set-up-cash-flow-forecasts"></a>Configurer les prévisions de trésorerie
Le graphique **Prévision de trésorerie** utilise les comptes de trésorerie, les paramétrages de trésorerie et les prévisions de trésorerie. Certains comptes sont fournis, cependant, vous pouvez définir les vôtres à l'aide d'un guide de configuration assistée. Le guide vous aide à spécifier des éléments, tels que la fréquence de mise à jour des prévisions, les comptes sur lesquels les baser, les informations concernant l'échéance de paiement des taxes et s'il convient d'utiliser [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite).  

Les prévisions de trésorerie peuvent utiliser Cortana Intelligence pour inclure des documents contenant une date d'échéance future. Le résultat est une prévision plus complète. La connexion à Cortana Intelligence est déjà configurée pour vous. Vous devez juste l'activer. Lorsque vous vous connectez à [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], une notification s'affiche dans une barre bleue et inclut un lien vers le paramétrage par défaut de trésorerie. La notification s'affiche une seule fois. Si vous la fermez, mais décidez d'activer Cortana Intelligence, vous pouvez utiliser le guide de configuration assistée ou un processus manuel.  

**Remarque :** sinon, vous pouvez utiliser votre propre service Web prévisionnel. Pour plus d'informations, voir [Créer et utiliser votre propre service Web prévisionnel pour des prévisions de trésorerie](#AnchorText).  

Pour utiliser le guide de configuration assistée :  

1. Dans le tableau de bord Comptable, sous le graphique **Prévisions de trésorerie**, sélectionnez l'action **Ouvrir la configuration assistée**.  
2. Complétez les champs de chaque étape du guide.  
3. Dans la page d'accueil, choisissez **Prévision de trésorerie** au-dessus du graphique, puis **Recalculer la prévision**.  

Pour utiliser une procédure manuelle :  

1. Dans le tableau de bord Comptable, recherchez **Paramètres trésorerie**, puis sélectionnez le lien associé.  
2. Développez le raccourci **Cortana Intelligence**, puis cochez la case **Cortana Intelligence activé**.  
3. Dans la page d'accueil, choisissez **Prévision de trésorerie** au-dessus du graphique, puis **Recalculer la prévision**.  

**Astuce :** tenez compte de la durée des périodes utilisée par le service lors de ses calculs. Plus vous fournissez de données, plus les prévisions seront précises. En outre, soyez prudent en ce qui concerne les grands écarts entre les périodes. Cela aura également un impact sur les prévisions. Si Cortana Intelligence ne trouve pas suffisamment de données ou si les données varient considérablement, le service ne fera pas de prévisions.  

## <a name="AnchorText"> </a>Créer et utiliser votre propre service Web prévisionnel pour des prévisions de trésorerie
Vous pouvez aussi utiliser votre propre service Web prévisionnel basé sur un modèle public intitulé **Modèle de prévision pour Microsoft Dynamics 365 for Financials**. Ce modèle prévisionnel est disponible en ligne dans la galerie Cortana Intelligence. Pour utiliser le modèle, procédez comme suit :  

1. Ouvrez un navigateur et accédez à la [Galerie Cortana Intelligence](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Recherchez **Modèle prévisionnel pour Microsoft Dynamics 365 pour les finances**, puis ouvrez-le dans Azure Machine Learning Studio.  
3. Utilisez votre compte Microsoft pour enregistrer un espace de travail, puis copiez le modèle.  
4. Exécutez le modèle, et publiez-le comme service Web.  
5. Notez l'URL d'API et la clé d'API. Vous allez utiliser ces informations d'identification pour une configuration de trésorerie.  
6. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Paramètres trésorerie**, puis sélectionnez le lien associé.  
7. Développez le raccourci **Cortana Intelligence**, puis complétez les champs.  

## <a name="see-also"></a>Voir aussi
[Analyse de la trésorerie dans votre société](finance-analyze-cash-flow.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

