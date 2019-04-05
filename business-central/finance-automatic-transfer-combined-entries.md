---
title: Transfert automatique et écritures combinées | Microsoft Docs
description: En comptabilité analytique, vous pouvez transférer les écritures comptables vers un type de coût à l'aide d'une validation combinée. Vous pouvez spécifier si un type de coût reçoit des écritures combinées dans le champ **Combiner écritures** dans la définition du type de coût. Le tableau suivant décrit les différentes options.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 6f58e569bea6a42a9ee695095ce308e7a69e2a8d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820411"
---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="75552-105">Transfert automatique et écritures combinées</span><span class="sxs-lookup"><span data-stu-id="75552-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="75552-106">En comptabilité analytique, vous pouvez transférer les écritures comptables vers un type de coût à l'aide d'une validation combinée.</span><span class="sxs-lookup"><span data-stu-id="75552-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="75552-107">Vous pouvez spécifier si un type de coût reçoit des écritures combinées dans le champ **Combiner écritures** dans la définition du type de coût.</span><span class="sxs-lookup"><span data-stu-id="75552-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="75552-108">Le tableau suivant décrit les différentes options.</span><span class="sxs-lookup"><span data-stu-id="75552-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="75552-109">Combiner des écritures</span><span class="sxs-lookup"><span data-stu-id="75552-109">Combine entries</span></span>|<span data-ttu-id="75552-110">Désignation</span><span class="sxs-lookup"><span data-stu-id="75552-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="75552-111">Aucune</span><span class="sxs-lookup"><span data-stu-id="75552-111">None</span></span>|<span data-ttu-id="75552-112">Chaque écriture comptable est transférée individuellement vers le type de coût correspondant.</span><span class="sxs-lookup"><span data-stu-id="75552-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="75552-113">Jour</span><span class="sxs-lookup"><span data-stu-id="75552-113">Day</span></span>|<span data-ttu-id="75552-114">Les écritures comptables, dont la date de validation est identique, sont transférées en une seul écriture vers le type de coût correspondant.</span><span class="sxs-lookup"><span data-stu-id="75552-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="75552-115">Mois</span><span class="sxs-lookup"><span data-stu-id="75552-115">Month</span></span>|<span data-ttu-id="75552-116">Toutes les écritures comptables du même mois calendaire sont transférées en une seul écriture vers le type de coût correspondant.</span><span class="sxs-lookup"><span data-stu-id="75552-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="75552-117">Si vous avez coché la case **Transférer automatiquement à partir de la compta** sur la page **Paramètres comptabilité analytique**, [!INCLUDE[d365fin](includes/d365fin_md.md)] met à jour la comptabilité analytique après chaque validation comptable.</span><span class="sxs-lookup"><span data-stu-id="75552-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="75552-118">Les écritures combinées ne sont pas possibles.</span><span class="sxs-lookup"><span data-stu-id="75552-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="75552-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75552-119">See Also</span></span>  
 <span data-ttu-id="75552-120">[Transfert et validation des écritures de coûts](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="75552-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="75552-121">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="75552-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
