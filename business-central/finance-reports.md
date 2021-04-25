---
title: Rapports financiers dans Business Central
description: Découvrez les rapports financiers disponibles dans la version standard de Business Central afin que vous puissiez suivre votre activité.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a36e40796978ddd20df818c3bccb1e148d50a4e1
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783787"
---
# <a name="financial-reports-in-business-central"></a>Rapports financiers dans Business Central

La génération d’états financiers dans [!INCLUDE [prod_short](includes/prod_short.md)] permet aux professionnels de la finance et des affaires de créer, maintenir, déployer et consulter des états financiers. Ils vont au-delà des contraintes des rapports traditionnels pour vous aider à concevoir efficacement divers types de rapports. [!INCLUDE [prod_short](includes/prod_short.md)] comprend plusieurs rapports, fonctions de traçage et outils qui aident les auditeurs ou contrôleurs chargés de rendre compte au service financier. La génération d’états financiers inclut la prise en charge des dimensions, de sorte que les segments de compte ou les dimensions sont immédiatement disponibles. Aucun outil ou étape de configuration supplémentaire n’est requis.  

## <a name="reports"></a>États

Le tableau suivant décrit certains des principaux rapports dans les rapports financiers.

|État |Description  |
|---------|---------|
|**Ajuster coûts : Écr. article** | Ajuste les valeurs d’inventaire des écritures valeur afin que vous utilisiez le coût ajusté correct pour la mise à jour des écritures comptables et que les statistiques vente et profit soient à jour. L’ajustement des coûts transfère les modifications de coût des écritures entrantes, telles que celles des sorties achat ou production, aux écritures sortantes correspondantes, telles que les ventes ou les transferts.  |
|**Balance**| Affiche le plan comptable avec les soldes et les soldes périodes. Vous pouvez choisir de visualiser la balance générale relative à des axes analytiques sélectionnés. Vous pouvez l’utiliser lors de la clôture d’une période comptable ou d’un exercice comptable. |
|**Balance par période**  | Présente le solde d’ouverture par compte général, les mouvements pour la période sélectionnée (mois, trimestre ou année) et le solde de clôture qui en résulte.         |
|**Comparaison balance/budget** | Affiche la balance comparée à un budget. Vous pouvez choisir de visualiser la balance générale relative à des axes analytiques sélectionnés. Vous pouvez l’utiliser lors de la clôture d’une période comptable ou d’un exercice comptable.        |
|**Balance détaillée** |Affiche la balance détaillée pour les écritures comptables sélectionnées. Vous pouvez l’utiliser lors de la clôture d’une période comptable ou d’un exercice comptable. Vous pouvez définir les comptes qui seront inclus dans le rapport en définissant des filtres.         |
|**Balance N/N-1**|Affiche la balance comparée aux chiffres de l’année précédente. Vous pouvez choisir de visualiser la balance générale relative à des axes analytiques sélectionnés. Vous pouvez l’utiliser lors de la clôture d’une période comptable ou d’un exercice comptable. Notez que l’*année précédente* signifie la même période de l’année calendaire précédente.|
|**Tableau d’analyse**|Les tableaux d’analyse peuvent être utilisés pour afficher les comptes généraux d’une manière différente que dans le plan comptable. Par exemple, les tableaux d’analyse peuvent être utilisés pour les rapports qui concernent des chiffres-clés.|
<!--|**Bilan** (Tableau d’analyse ou Excel) ou **Balance** |         |
|**Déclaration des trésoreries** (Tableau d’analyse) |         |
|**Détail/Résumé balance** |         |
|**Comptes de gestion** (Tableau d’analyse ou Excel)||
|**Budget** ||-->

## <a name="tasks"></a>Tâches

Les articles suivants décrivent certaines des tâches clés pour analyser l’état de votre entreprise :

* [Analyser les montants réalisés et les montants budgétés](bi-how-analyze-actual-versus-budget.md)  
* [Préparer Financial Reporting avec des tableaux d’analyse et des catégories de compte](bi-how-work-account-schedule.md)  
* [Configuration et publication des services Web KPI sur la base de tableaux d’analyse](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md)  
* [Analyse des données par axe analytique](bi-how-analyze-data-dimension.md)  
* [Créer des rapports d’analyse](bi-how-create-analysis-views-reports.md)  
* [Création d’états avec XBRL](bi-create-reports-with-xbrl.md)  
* [Gérer l’accès intentionnel à la base de données](admin-data-access-intent.md)  

## <a name="see-also"></a>Voir aussi

[Création des budgets des coûts](finance-create-cost-budgets.md)  
[Déclarer la TVA aux autorités fiscales](finance-how-report-vat.md)  
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Utilisation d’états préalables à la clôture](year-prepare-preclose-reports.md)  
[Préparation des états de clôture](year-prepare-close-statement.md)  
[Analyse des états financiers dans Microsoft Excel](finance-analyze-excel.md)  
[Utilisation des axes analytiques](finance-dimensions.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Finances](finance.md)  
[Vue d’ensemble des fonctionnalités locales](about-localization.md)  
[Expériences de comptable dans [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]