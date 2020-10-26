---
title: Procédure de validation des capacités | Microsoft Docs
description: La feuille capacité vous permet de valider les capacités consommées qui ne sont pas affectées à l’ordre de fabrication. Par exemple, les travaux de maintenance doivent être affectés à une capacité, mais non à un ordre de fabrication.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 96ed7af85889c20f9792ce904d1ba30660bf1b76
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919153"
---
# <a name="post-capacities"></a><span data-ttu-id="334ea-104">Valider les capacités</span><span class="sxs-lookup"><span data-stu-id="334ea-104">Post Capacities</span></span>
<span data-ttu-id="334ea-105">La feuille capacité vous permet de valider les capacités consommées qui ne sont pas affectées à l’ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="334ea-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="334ea-106">Par exemple, les travaux de maintenance doivent être affectés à une capacité, mais non à un ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="334ea-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="334ea-107">Pour valider les capacités</span><span class="sxs-lookup"><span data-stu-id="334ea-107">To post capacities</span></span>  
1.  <span data-ttu-id="334ea-108">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles capacité** , puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="334ea-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Capacity Journals** , and then choose the related link.</span></span>  
2.  <span data-ttu-id="334ea-109">Renseignez les champs **Date comptabilisation** et **N° document** .</span><span class="sxs-lookup"><span data-stu-id="334ea-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="334ea-110">Dans le champ **Type** , entrez le type de capacité, **Poste de charge** ou **Centre de charge** , que vous validez.</span><span class="sxs-lookup"><span data-stu-id="334ea-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center** , that you are posting.</span></span>  
4.  <span data-ttu-id="334ea-111">Dans le champ **N°** ,</span><span class="sxs-lookup"><span data-stu-id="334ea-111">In the **No.**</span></span> <span data-ttu-id="334ea-112">saisissez le nom du centre de charge ou du poste de charge.</span><span class="sxs-lookup"><span data-stu-id="334ea-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="334ea-113">Entrez les données nécessaires dans les autres champs, tels que **Heure début** , **Heure fin** , **Quantité** , et **Rebut** .</span><span class="sxs-lookup"><span data-stu-id="334ea-113">Enter the relevant data in the other fields, such as **Starting Time** , **Ending Time** , **Quantity** , and **Scrap** .</span></span>  
6.  <span data-ttu-id="334ea-114">Choisissez l’action **Valider** pour valider les capacités.</span><span class="sxs-lookup"><span data-stu-id="334ea-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="334ea-115">Pour afficher les écritures comptables centre de charge</span><span class="sxs-lookup"><span data-stu-id="334ea-115">To view work center ledger entries</span></span>  
<span data-ttu-id="334ea-116">Sur les pages **Fiche centre de charge** et **Fiche poste de charge** , vous pouvez afficher les capacités validées en tant que résultat des ordres de fabrication terminés.</span><span class="sxs-lookup"><span data-stu-id="334ea-116">In the **Work Center Card** and **Machine Center Card** pages, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="334ea-117">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Centres de charge** , puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="334ea-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers** , and then choose the related link.</span></span>  
2.  <span data-ttu-id="334ea-118">Ouvrez la fiche **Centre de charge** appropriée dans la liste, puis choisissez l’action **Écritures comptables capacité** .</span><span class="sxs-lookup"><span data-stu-id="334ea-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="334ea-119">La page **Écritures comptables capacité** affiche les écritures validées relatives au centre de charge dans l’ordre de leur validation.</span><span class="sxs-lookup"><span data-stu-id="334ea-119">The **Capacity Ledger Entries** page displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="334ea-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="334ea-120">See Also</span></span>  
<span data-ttu-id="334ea-121">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="334ea-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="334ea-122">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="334ea-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="334ea-123">[Planifié](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="334ea-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="334ea-124">Stock</span><span class="sxs-lookup"><span data-stu-id="334ea-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="334ea-125">Achats</span><span class="sxs-lookup"><span data-stu-id="334ea-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="334ea-126">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="334ea-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
