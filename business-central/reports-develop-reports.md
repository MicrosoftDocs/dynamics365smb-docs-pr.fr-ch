---
title: Développement de dispositions de rapports et de jeux de données
description: Fournit une vue des données de Business Central.
author: kennieNP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: bholtorf
ms.search.keywords: feature overview
ms.date: 02/03/2022
ms.author: kepontop
---

# Développement de dispositions de rapports et de jeux de données Business Central

Un rapport dans [!INCLUDE[prod_short](includes/prod_short.md)] se compose d’un objet de rapport qui définit le _jeu de données_ du rapport (quelles sont les données disponibles) et un certain nombre de _dispositions de rapport_ (comment les données sont présentées).  

## Élaboration de dispositions d’état

Vous souhaitez peut-être modifier les dispositions de rapport existantes fournies dans [!INCLUDE[prod_short](includes/prod_short.md)] ? Selon la technologie utilisée pour la disposition, c’est quelque chose que vous pourrez peut-être faire vous-même (dispositions Excel et peut-être aussi Word), ou peut-être avez-vous besoin d’un développeur pour le faire (dispositions RDLC au pixel près).

| À | Voir |
|--|--|
| En savoir plus sur les différents types de dispositions (Word, Excel et RDLC) | [Types de disposition (Word, Excel et RDLC)](ui-manage-report-layouts.md) |
| Découvrez comment vous pouvez créer une disposition de rapport. | [Créer une disposition](ui-how-create-custom-report-layout.md) |
| En savoir plus sur les polices installées dans [!INCLUDE[prod_short](includes/prod_short.md)] Online afin qu’ils puissent être utilisés dans les dispositions de rapport. | [Utilisation des polices dans les dispositions](ui-fonts.md) |
| Pour apprendre à travailler avec les dispositions Word. | [Utilisation des dispositions Word](ui-how-add-fields-word-report-layout.md) |
| Pour savoir comment importer/exporter des fichiers de disposition. | [Importer/exporter une disposition](ui-how-import-and-export-report-layout.md) |
| Pour savoir comment mettre à jour une définition de disposition dans [!INCLUDE[prod_short](includes/prod_short.md)] avec un nouveau fichier de disposition. | [Importer/exporter une disposition](ui-how-import-and-export-report-layout.md) |
| Pour savoir comment modifier la disposition par défaut d’un rapport. | [Modifier la disposition par défaut](ui-how-change-layout-currently-used-report.md) |
<!-- | Pour apprendre à travailler avec les dispositions Excel | [Utilisation des dispositions d’Excel](ui-how-add-fields-word-report-layout.md) | -->

## Élaboration de jeux de données d’état

 Pour modifier les définitions de jeu de données qui définissent les données disponibles dans le rapport, vous avez besoin d’un développeur qui connaît le langage de programmation AL et les outils pour développer des objets de rapport et des extensions de rapport.

| À | Voir |
|--|--|
| Apprenez à programmer des rapports dans AL | [Guide de développement de rapports](/dynamics365/business-central/dev-itpro/developer/devenv-reports) |
| Apprenez à rendre les rapports performants | [Guide de réglage des performances des rapports](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-reports) |

## Voir aussi

[Vue d’ensemble de Business Intelligence et Reporting](reports-use-reports.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]