---
title: Utilisation de l'extension Importer le fichier de paie de Quickbooks | Microsoft Docs
description: "Décrit comment utiliser l'extension pour importer des transactions de salaire et de paie à partir du service de paie de Quickbooks."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 03/29/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2b87eaa6bfe53f7b6e119006df9254876f4117a9
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="the-quickbooks-payroll-file-import-extension-to-finance-and-operations-business-edition"></a><span data-ttu-id="946e3-103">L'extension Quickbooks Payroll File Import pour Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="946e3-103">The Quickbooks Payroll File Import Extension to Finance and Operations, Business edition</span></span> 
<span data-ttu-id="946e3-104">Pour tenir compte des paiements des salaires et des transactions associées, vous devez importer et valider des transactions financières effectuées par votre fournisseur de paie dans la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="946e3-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="946e3-105">Pour cela, vous devez commencer par importer un fichier que vous recevez du fournisseur de paie dans la fenêtre **Feuille comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="946e3-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="946e3-106">Vous devez ensuite mapper les comptes externes du fichier de paie aux comptes généraux appropriés.</span><span class="sxs-lookup"><span data-stu-id="946e3-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="946e3-107">Enfin, vous devez valider les transactions de paie en fonction du mappage de compte.</span><span class="sxs-lookup"><span data-stu-id="946e3-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="946e3-108">Pour plus d'informations, voir [Importer les transactions de paie](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="946e3-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="946e3-109">L'extension Importer le fichier de paie de Quickbooks vous permet d'importer la transaction Paie à partir du service de paie de Quickbooks.</span><span class="sxs-lookup"><span data-stu-id="946e3-109">The Quickbooks Payroll File Import extension allows you to import payroll transaction from the Quickbooks Payroll service.</span></span>

## <a name="see-also"></a><span data-ttu-id="946e3-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="946e3-110">See Also</span></span>
<span data-ttu-id="946e3-111">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="946e3-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="946e3-112">[Finances](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="946e3-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="946e3-113">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="946e3-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

