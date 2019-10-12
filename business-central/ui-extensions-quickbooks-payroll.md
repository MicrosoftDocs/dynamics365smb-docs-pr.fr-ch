---
title: Utilisation de l'extension Importer le fichier de paie de QuickBooks | Microsoft Docs
description: Cette rubrique décrit comment utiliser l'extension pour importer des transactions de salaire et de paie à partir de QuickBooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 42514576f7fb9542bbecfbbe8e9ff7996040da9b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311131"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a>Extension Importer le fichier de paie de QuickBooks
Utilisez l'extension d'importation de fichier de paie de QuickBooks pour importer des transactions paie de QuickBooks vers des comptes de comptabilité générale dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Par exemple, cela est utile lorsque vous passez QuickBooks vers [!INCLUDE[d365fin](includes/d365fin_md.md)], ou si vous externalisez votre paie mais que vous souhaitez également en effectuer le suivi dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="steps-to-import-payroll-data"></a>Procédures pour importer des données de paie
La première étape consiste pour vous, ou peut-être votre comptable, à utiliser les fonctionnalités d'exportation dans QuickBooks pour exporter les données de la paie dans un fichier .IIF. La deuxième étape permet d'ouvrir la page **Feuilles comptabilité** dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et d'utiliser l'action **Importer les transactions de paie** pour importer le fichier. Au cours du processus d'importation, vous mappez les comptes généraux de QuickBooks aux comptes correspondants dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. L'étape finale consiste à valider les transactions de paie dans [!INCLUDE[d365fin](includes/d365fin_md.md)] en fonction du mappage de compte. 

Pour plus d'informations, voir [Importer les transactions de paie](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Voir aussi
[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions ](ui-extensions.md)    
[Finances](finance.md)    
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
