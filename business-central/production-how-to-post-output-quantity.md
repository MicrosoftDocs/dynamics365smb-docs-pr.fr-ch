---
title: Procédure de validation par lots de la production et des temps d’exécution | Microsoft Docs
description: La quantité produite représente l’avancée des travaux en prenant en compte la quantité achevée.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: db613df030a739ac8899b3cea19e89f17dcfe53e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916590"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="7945d-103">Valider par lots la production et les temps d’exécution</span><span class="sxs-lookup"><span data-stu-id="7945d-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="7945d-104">La quantité produite représente l’avancée des travaux en prenant en compte la quantité achevée.</span><span class="sxs-lookup"><span data-stu-id="7945d-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="7945d-105">Le stock est automatiquement mis à jour lorsque vous validez la quantité produite durant la dernière opération.</span><span class="sxs-lookup"><span data-stu-id="7945d-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="7945d-106">Pour valider les quantités produites pour une ou plusieurs lignes ordre de fabrication</span><span class="sxs-lookup"><span data-stu-id="7945d-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="7945d-107">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille production** , puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7945d-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal** , and then choose the related link.</span></span>  
2. <span data-ttu-id="7945d-108">Renseignez les champs en indiquant les données relatives à la fabrication et à la production.</span><span class="sxs-lookup"><span data-stu-id="7945d-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="7945d-109">Si l’opération est achevée, sélectionnez le champ **Terminé** .</span><span class="sxs-lookup"><span data-stu-id="7945d-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="7945d-110">Si l’entrepôt dans lequel les articles doivent être rangés utilise des emplacements mais pas le traitement de rangement, affectez un code emplacement à la ligne feuille pour indiquer l’endroit où les articles doivent être placés dans l’entrepôt.</span><span class="sxs-lookup"><span data-stu-id="7945d-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="7945d-111">Pour plus d’informations, voir [Rangement du résultat de fabrication ou d’assemblage](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="7945d-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="7945d-112">Choisissez l’action **Valider** pour valider les opérations.</span><span class="sxs-lookup"><span data-stu-id="7945d-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="7945d-113">La quantité produite est validée.</span><span class="sxs-lookup"><span data-stu-id="7945d-113">The output quantity will be posted.</span></span> <span data-ttu-id="7945d-114">L’article peut être expédié.</span><span class="sxs-lookup"><span data-stu-id="7945d-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="7945d-115">Pour valider les temps d’exécution pour une ou plusieurs lignes ordre de fabrication</span><span class="sxs-lookup"><span data-stu-id="7945d-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="7945d-116">Le temps d’exécution représente l’avancement des travaux en prenant en compte le temps de travail nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7945d-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="7945d-117">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille production** , puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7945d-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal** , and then choose the related link.</span></span>  
2. <span data-ttu-id="7945d-118">Renseignez les champs en indiquant les données relatives à la fabrication et à la production.</span><span class="sxs-lookup"><span data-stu-id="7945d-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="7945d-119">Si l’opération est achevée, sélectionnez le champ **Terminé** .</span><span class="sxs-lookup"><span data-stu-id="7945d-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="7945d-120">Choisissez l’action **Valider** pour valider le temps passé par opération.</span><span class="sxs-lookup"><span data-stu-id="7945d-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="7945d-121">Les écritures comptables capacité sont mises à jour pour les centres ou postes de charge utilisés.</span><span class="sxs-lookup"><span data-stu-id="7945d-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="7945d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7945d-122">See Also</span></span>  
<span data-ttu-id="7945d-123">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="7945d-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="7945d-124">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="7945d-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="7945d-125">[Planifié](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="7945d-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="7945d-126">Stock</span><span class="sxs-lookup"><span data-stu-id="7945d-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="7945d-127">Achats</span><span class="sxs-lookup"><span data-stu-id="7945d-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="7945d-128">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7945d-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
