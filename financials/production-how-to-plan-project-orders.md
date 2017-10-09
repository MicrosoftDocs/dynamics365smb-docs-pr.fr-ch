---
title: "Procédure de planification de projets de commandes | Microsoft Docs"
description: "Cette tâche de planification est lancée à partir d'une commande vente et utilise la fenêtre **Planification commande vente**. Une fois que vous avez créé un O.F. projet, vous pouvez le planifier davantage à l'aide de la fenêtre **Planning commande**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 49e3ce0ef80dd54f66565f62616b3b8f2a4aaeaa
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-plan-project-orders"></a><span data-ttu-id="2e132-104">Procédure : planifier les projets de commandes</span><span class="sxs-lookup"><span data-stu-id="2e132-104">How to: Plan Project Orders</span></span>
<span data-ttu-id="2e132-105">Cette tâche de planification est lancée à partir d'une commande vente et utilise la fenêtre **Planification commande vente**.</span><span class="sxs-lookup"><span data-stu-id="2e132-105">This planning task starts from a sales order and uses the **Sales Order Planning** window.</span></span> <span data-ttu-id="2e132-106">Une fois que vous avez créé un O.F. projet, vous pouvez le planifier davantage à l'aide de la fenêtre **Planning commande**.</span><span class="sxs-lookup"><span data-stu-id="2e132-106">Once you have created a project production order, you can plan it further by using the **Order Planning** window.</span></span>  

## <a name="to-create-a-project-production-order"></a><span data-ttu-id="2e132-107">Pour créer un O.F projet</span><span class="sxs-lookup"><span data-stu-id="2e132-107">To create a project production order</span></span>  

1.  <span data-ttu-id="2e132-108">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="2e132-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2e132-109">Sélectionnez la commande vente qui représente le projet de production, puis choisissez l'action **Planning**.</span><span class="sxs-lookup"><span data-stu-id="2e132-109">Select the sales order that represents the production project, and then choose the **Planning** action.</span></span>  
4.  <span data-ttu-id="2e132-110">Dans la fenêtre **Planification commande vente**, choisissez l'action **Créer O.F**.</span><span class="sxs-lookup"><span data-stu-id="2e132-110">In the **Sales Order Planning** window, choose  the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="2e132-111">Dans la fenêtre **Créer commande à partir des ventes**, dans le champ **Type O.F.**, sélectionnez **O.F. projet**.</span><span class="sxs-lookup"><span data-stu-id="2e132-111">In the **Create Order from Sales** window, in the **Order Type** field, select **Project Order**.</span></span>  
6.  <span data-ttu-id="2e132-112">Cliquez sur le bouton **Oui**.</span><span class="sxs-lookup"><span data-stu-id="2e132-112">Choose the **Yes** button.</span></span>  
7.  <span data-ttu-id="2e132-113">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Ordres de fabrication**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="2e132-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Production Orders**, and then choose the related link.</span></span>
8. <span data-ttu-id="2e132-114">Ouvrez l'ordre de fabrication que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="2e132-114">Open the production order just created.</span></span>  

    <span data-ttu-id="2e132-115">Notez que le champ **Type origine** de l'ordre de fabrication indique **En-tête vente** et l'ordre comporte plusieurs lignes, une pour chaque article de la ligne vente à produire.</span><span class="sxs-lookup"><span data-stu-id="2e132-115">Notice that the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  
9. <span data-ttu-id="2e132-116">Sélectionnez l'action **Planification**.</span><span class="sxs-lookup"><span data-stu-id="2e132-116">Choose the **Planning** action.</span></span>
10. <span data-ttu-id="2e132-117">Dans la fenêtre **Planning commande**, choisissez l'action **Actualiser** pour calculer la nouvelle demande.</span><span class="sxs-lookup"><span data-stu-id="2e132-117">In the **Order Planning** window, choose the **Refresh** action to calculate new demand.</span></span>  

<span data-ttu-id="2e132-118">La ligne d'en-tête de commande de la commande projet s'affiche avec toutes les lignes de demandes non satisfaites développées en-dessous.</span><span class="sxs-lookup"><span data-stu-id="2e132-118">The order header line for the project order is displayed with all unfulfilled demand lines expanded under it.</span></span> <span data-ttu-id="2e132-119">Bien que l'ordre de fabrication contienne les lignes de plusieurs articles produits, la demande totale pour toutes les lignes d'O.F. est répertoriée sous une ligne d'en-tête de commande dans la fenêtre **Planning commande** et le nom du client d'origine s'affiche.</span><span class="sxs-lookup"><span data-stu-id="2e132-119">Although the production order contains lines for several produced items, the total demand for all production order lines is listed under one order header line in the **Order Planning** window, and the original customer name is displayed.</span></span> <span data-ttu-id="2e132-120">Vous pouvez maintenant passer à la planification de la demande en vous reportant à la [Procédure : planifier de nouvelles demandes commande par commande](production-how-to-plan-for-new-demand.md).</span><span class="sxs-lookup"><span data-stu-id="2e132-120">You can now proceed to plan for the demand as described in [How to: Plan for New Demand Order by Order](production-how-to-plan-for-new-demand.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2e132-121">Les lignes de demandes de l'ordre de fabrication projet qui ont **Ordre de fabrication** dans leur champ **Système réappro.** représentent des ordres de fabrication sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="2e132-121">Demand lines in the project production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="2e132-122">Après avoir généré ces ordres de fabrication, vous devez à nouveau calculer un planning dans la fenêtre **Planning ordre** pour identifier toute demande de composant non réalisée pour ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="2e132-122">After you have generated these production orders, you must again calculate a plan in the **Order Planning** window to identify any unfulfilled component demand for them.</span></span> <span data-ttu-id="2e132-123">Cela signifie que le lien projet n'est plus visible dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2e132-123">In that case, they are displayed as demand lines under a normal production order header line, meaning, the project relation is no longer visible in the window.</span></span> <span data-ttu-id="2e132-124">Cependant, si vous utilisez la fonctionnalité Chaînage, alors vous pouvez passer en revue les commandes approvisionnement effectuées sous la commande vente d'origine.</span><span class="sxs-lookup"><span data-stu-id="2e132-124">However, if you are using the Order Tracking feature, then you can look back and forth to all supply orders made under the original sales order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2e132-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e132-125">See Also</span></span>
<span data-ttu-id="2e132-126">[Planifié](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="2e132-126">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="2e132-127">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="2e132-127">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="2e132-128">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="2e132-128">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="2e132-129">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="2e132-129">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="2e132-130">Achats</span><span class="sxs-lookup"><span data-stu-id="2e132-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="2e132-131">[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="2e132-131">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="2e132-132">Pratiques de configuration recommandées : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="2e132-132">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="2e132-133">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2e132-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

