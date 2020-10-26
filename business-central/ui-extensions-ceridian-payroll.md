---
title: Importation des données de paie ou de salaire à l’aide de l’extension Ceridian Payroll | Microsoft Docs
description: Utilisez cette extension pour importer des transactions de paie à partir des services Ceridian HR/Payroll (US) et Ceridian PowerPay (Canada).
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 29dfaaa1cefe2bdc55fd68b1efd752be2c11cbc8
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912379"
---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="e401a-103">Extension Ceridian Payroll</span><span class="sxs-lookup"><span data-stu-id="e401a-103">The Ceridian Payroll Extension</span></span>
<span data-ttu-id="e401a-104">Pour tenir compte des paiements des salaires et des transactions associées, vous devez importer et valider des transactions financières effectuées par votre fournisseur de paie dans la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="e401a-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="e401a-105">Pour cela, vous devez commencer par importer un fichier que vous recevez du fournisseur de paie sur la page **Feuille comptabilité** .</span><span class="sxs-lookup"><span data-stu-id="e401a-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="e401a-106">Vous devez ensuite mapper les comptes externes du fichier de paie aux comptes généraux appropriés.</span><span class="sxs-lookup"><span data-stu-id="e401a-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="e401a-107">Enfin, vous devez valider les transactions de paie en fonction du mappage de compte.</span><span class="sxs-lookup"><span data-stu-id="e401a-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="e401a-108">Pour plus d’informations, voir [Importer les transactions de paie](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="e401a-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="e401a-109">L’extension Ceridian Payroll vous permet d’importer des transactions de paie à partir des services Ceridian HR/Payroll (US) et Ceridian PowerPay (Canada).</span><span class="sxs-lookup"><span data-stu-id="e401a-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="e401a-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e401a-110">See Also</span></span>
<span data-ttu-id="e401a-111">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l’aide des extensions ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="e401a-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="e401a-112">[Finances](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="e401a-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="e401a-113">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e401a-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
