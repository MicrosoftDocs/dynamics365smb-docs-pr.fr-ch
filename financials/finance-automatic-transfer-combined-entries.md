---
title: "Transfert automatique et écritures combinées | Microsoft Docs"
description: "En comptabilité analytique, vous pouvez transférer les écritures comptables vers un type de coût à l'aide d'une validation combinée. Vous pouvez spécifier si un type de coût reçoit des écritures combinées dans le champ **Combiner écritures** dans la définition du type de coût. Le tableau suivant décrit les différentes options."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f4796d9796788d2fbbf5706688aec75a4ed9a6d8
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="5bd26-105">Transfert automatique et écritures combinées</span><span class="sxs-lookup"><span data-stu-id="5bd26-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="5bd26-106">En comptabilité analytique, vous pouvez transférer les écritures comptables vers un type de coût à l'aide d'une validation combinée.</span><span class="sxs-lookup"><span data-stu-id="5bd26-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="5bd26-107">Vous pouvez spécifier si un type de coût reçoit des écritures combinées dans le champ **Combiner écritures** dans la définition du type de coût.</span><span class="sxs-lookup"><span data-stu-id="5bd26-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="5bd26-108">Le tableau suivant décrit les différentes options.</span><span class="sxs-lookup"><span data-stu-id="5bd26-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="5bd26-109">Combiner des écritures</span><span class="sxs-lookup"><span data-stu-id="5bd26-109">Combine entries</span></span>|<span data-ttu-id="5bd26-110">Désignation</span><span class="sxs-lookup"><span data-stu-id="5bd26-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="5bd26-111">Aucune</span><span class="sxs-lookup"><span data-stu-id="5bd26-111">None</span></span>|<span data-ttu-id="5bd26-112">Chaque écriture comptable est transférée individuellement vers le type de coût correspondant.</span><span class="sxs-lookup"><span data-stu-id="5bd26-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="5bd26-113">Jour</span><span class="sxs-lookup"><span data-stu-id="5bd26-113">Day</span></span>|<span data-ttu-id="5bd26-114">Les écritures comptables, dont la date de validation est identique, sont transférées en une seul écriture vers le type de coût correspondant.</span><span class="sxs-lookup"><span data-stu-id="5bd26-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="5bd26-115">Mois</span><span class="sxs-lookup"><span data-stu-id="5bd26-115">Month</span></span>|<span data-ttu-id="5bd26-116">Toutes les écritures comptables du même mois calendaire sont transférées en une seul écriture vers le type de coût correspondant.</span><span class="sxs-lookup"><span data-stu-id="5bd26-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="5bd26-117">Si vous avez coché la case **Transférer automatiquement à partir de la compta** dans la fenêtre **Paramètres comptabilité analytique**, [!INCLUDE[d365fin](includes/d365fin_md.md)] met à jour la comptabilité analytique après chaque validation comptable.</span><span class="sxs-lookup"><span data-stu-id="5bd26-117">If you have selected the **Auto Transfer from G/L** check box in the **Cost Accounting Setup** window, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="5bd26-118">Les écritures combinées ne sont pas possibles.</span><span class="sxs-lookup"><span data-stu-id="5bd26-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5bd26-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bd26-119">See Also</span></span>  
 <span data-ttu-id="5bd26-120">[Transférer les écritures comptables vers les écritures de coûts](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="5bd26-120">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="5bd26-121">[Critères de transfert des écritures comptables vers les écritures de coûts](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="5bd26-121">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="5bd26-122">[Résultats du transfert](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="5bd26-122">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 [<span data-ttu-id="5bd26-123">Transfert et validation des écritures de coûts</span><span class="sxs-lookup"><span data-stu-id="5bd26-123">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  
 <span data-ttu-id="5bd26-124">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5bd26-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

