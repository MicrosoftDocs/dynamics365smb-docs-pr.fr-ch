---
title: "Procédure de validation des capacités | Microsoft Docs"
description: "La feuille capacité vous permet de valider les capacités consommées qui ne sont pas affectées à l'ordre de fabrication. Par exemple, les travaux de maintenance doivent être affectés à une capacité, mais non à un ordre de fabrication."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6114149372b786c20ee7edbe13022abe688ed9a2
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="post-capacities"></a><span data-ttu-id="3d1a9-104">Valider les capacités</span><span class="sxs-lookup"><span data-stu-id="3d1a9-104">Post Capacities</span></span>
<span data-ttu-id="3d1a9-105">La feuille capacité vous permet de valider les capacités consommées qui ne sont pas affectées à l'ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="3d1a9-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="3d1a9-106">Par exemple, les travaux de maintenance doivent être affectés à une capacité, mais non à un ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="3d1a9-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="3d1a9-107">Pour valider les capacités</span><span class="sxs-lookup"><span data-stu-id="3d1a9-107">To post capacities</span></span>  
1.  <span data-ttu-id="3d1a9-108">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Feuilles temps non productif**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="3d1a9-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3d1a9-109">Renseignez les champs **Date comptabilisation** et **N° document**.</span><span class="sxs-lookup"><span data-stu-id="3d1a9-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="3d1a9-110">Dans le champ **Type**, entrez le type de capacité, **Poste de charge** ou **Centre de charge**, que vous validez.</span><span class="sxs-lookup"><span data-stu-id="3d1a9-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="3d1a9-111">Dans le champ **N°**,</span><span class="sxs-lookup"><span data-stu-id="3d1a9-111">In the **No.**</span></span> <span data-ttu-id="3d1a9-112">saisissez le nom du centre de charge ou du poste de charge.</span><span class="sxs-lookup"><span data-stu-id="3d1a9-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="3d1a9-113">Entrez les données nécessaires dans les autres champs, tels que **Heure début**, **Heure fin**, **Quantité**, et **Rebut**.</span><span class="sxs-lookup"><span data-stu-id="3d1a9-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="3d1a9-114">Choisissez l'action **Valider** pour valider les capacités.</span><span class="sxs-lookup"><span data-stu-id="3d1a9-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="3d1a9-115">Pour afficher les écritures comptables centre de charge</span><span class="sxs-lookup"><span data-stu-id="3d1a9-115">To view work center ledger entries</span></span>  
<span data-ttu-id="3d1a9-116">Dans les fenêtres **Fiche centre de charge** et **Fiche poste de charge**, vous pouvez afficher les capacités validées en tant que résultat des ordres de fabrication terminés.</span><span class="sxs-lookup"><span data-stu-id="3d1a9-116">In the **Work Center Card** and **Machine Center Card** windows, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="3d1a9-117">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Centres de charge**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="3d1a9-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3d1a9-118">Ouvrez la fiche **Centre de charge** appropriée dans la liste, puis choisissez l'action **Écritures comptables capacité**.</span><span class="sxs-lookup"><span data-stu-id="3d1a9-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="3d1a9-119">La fenêtre **Écritures comptables capacité** affiche les écritures validées relatives au centre de charge dans l'ordre de leur validation.</span><span class="sxs-lookup"><span data-stu-id="3d1a9-119">The **Capacity Ledger Entries** window displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="3d1a9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d1a9-120">See Also</span></span>  
<span data-ttu-id="3d1a9-121">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="3d1a9-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="3d1a9-122">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="3d1a9-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="3d1a9-123">[Planifié](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="3d1a9-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="3d1a9-124">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="3d1a9-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="3d1a9-125">Achats</span><span class="sxs-lookup"><span data-stu-id="3d1a9-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="3d1a9-126">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3d1a9-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

