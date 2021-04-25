---
title: Utilisation de l’extension Importer le fichier de paie de QuickBooks | Microsoft Docs
description: Cette rubrique décrit comment utiliser l’extension pour importer des transactions de salaire et de paie à partir de QuickBooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 838095fe81af36a421a49f19400b0abd5cdce17b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784780"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="e2fd3-103">Extension Importer le fichier de paie de QuickBooks</span><span class="sxs-lookup"><span data-stu-id="e2fd3-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="e2fd3-104">Utilisez l’extension d’importation de fichier de paie de QuickBooks pour importer des transactions paie de QuickBooks vers des comptes de comptabilité générale dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="e2fd3-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="e2fd3-105">Par exemple, cela est utile lorsque vous passez QuickBooks vers [!INCLUDE[prod_short](includes/prod_short.md)], ou si vous externalisez votre paie mais que vous souhaitez également en effectuer le suivi dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="e2fd3-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="e2fd3-106">Procédures pour importer des données de paie</span><span class="sxs-lookup"><span data-stu-id="e2fd3-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="e2fd3-107">La première étape consiste pour vous, ou peut-être votre comptable, à utiliser les fonctionnalités d’exportation dans QuickBooks pour exporter les données de la paie dans un fichier .IIF.</span><span class="sxs-lookup"><span data-stu-id="e2fd3-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="e2fd3-108">La deuxième étape permet d’ouvrir la page **Feuilles comptabilité** dans [!INCLUDE[prod_short](includes/prod_short.md)] et d’utiliser l’action **Importer les transactions de paie** pour importer le fichier.</span><span class="sxs-lookup"><span data-stu-id="e2fd3-108">The second step is to open the **General Journals** page in [!INCLUDE[prod_short](includes/prod_short.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="e2fd3-109">Au cours du processus d’importation, vous mappez les comptes généraux de QuickBooks aux comptes correspondants dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="e2fd3-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="e2fd3-110">L’étape finale consiste à valider les transactions de paie dans [!INCLUDE[prod_short](includes/prod_short.md)] en fonction du mappage de compte.</span><span class="sxs-lookup"><span data-stu-id="e2fd3-110">The final step is to post the payroll transactions in [!INCLUDE[prod_short](includes/prod_short.md)] according to the account mapping.</span></span> 

<span data-ttu-id="e2fd3-111">Pour plus d’informations, voir [Importer les transactions de paie](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="e2fd3-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e2fd3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2fd3-112">See Also</span></span>
<span data-ttu-id="e2fd3-113">[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="e2fd3-113">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="e2fd3-114">[Finances](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="e2fd3-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="e2fd3-115">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e2fd3-115">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]