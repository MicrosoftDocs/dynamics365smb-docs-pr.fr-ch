---
title: Utilisation de l'extension Importer le fichier de paie de QuickBooks | Microsoft Docs
description: "Cette rubrique décrit comment utiliser l'extension pour importer des transactions de salaire et de paie à partir de QuickBooks."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 01/09/2019
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 79729b42b660399893aebe1116c80ef3b3209042
ms.openlocfilehash: ac68f8a4d67224ad55b1c34ff9b2e4ffa2c372aa
ms.contentlocale: fr-ch
ms.lasthandoff: 01/15/2019

---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="0b00e-103">Extension Importer le fichier de paie de QuickBooks</span><span class="sxs-lookup"><span data-stu-id="0b00e-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="0b00e-104">Utilisez l'extension d'importation de fichier de paie de QuickBooks pour importer des transactions paie de QuickBooks vers des comptes de comptabilité générale dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0b00e-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0b00e-105">Par exemple, cela est utile lorsque vous passez QuickBooks vers [!INCLUDE[d365fin](includes/d365fin_md.md)], ou si vous externalisez votre paie mais que vous souhaitez également en effectuer le suivi dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0b00e-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="0b00e-106">Procédures pour importer des données de paie</span><span class="sxs-lookup"><span data-stu-id="0b00e-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="0b00e-107">La première étape consiste pour vous, ou peut-être votre comptable, à utiliser les fonctionnalités d'exportation dans QuickBooks pour exporter les données de la paie dans un fichier .IIF.</span><span class="sxs-lookup"><span data-stu-id="0b00e-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="0b00e-108">La deuxième étape permet d'ouvrir la page **Feuilles comptabilité** dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et d'utiliser l'action **Importer les transactions de paie** pour importer le fichier.</span><span class="sxs-lookup"><span data-stu-id="0b00e-108">The second step is to open the **General Journals** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="0b00e-109">Au cours du processus d'importation, vous mappez les comptes généraux de QuickBooks aux comptes correspondants dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0b00e-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0b00e-110">L'étape finale consiste à valider les transactions de paie dans [!INCLUDE[d365fin](includes/d365fin_md.md)] en fonction du mappage de compte.</span><span class="sxs-lookup"><span data-stu-id="0b00e-110">The final step is to post the payroll transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] according to the account mapping.</span></span> 

<span data-ttu-id="0b00e-111">Pour plus d'informations, voir [Importer les transactions de paie](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="0b00e-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0b00e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b00e-112">See Also</span></span>
<span data-ttu-id="0b00e-113">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="0b00e-113">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="0b00e-114">[Finances](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="0b00e-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="0b00e-115">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0b00e-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

