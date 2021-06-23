---
title: Créer des ordres de fabrication à partir de commandes achat
description: Vous pouvez créer des ordres de fabrication à partir de commandes achat.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115251"
---
# <a name="create-production-orders-from-sales-orders"></a><span data-ttu-id="5f693-103">Créer des ordres de fabrication à partir de commandes achat</span><span class="sxs-lookup"><span data-stu-id="5f693-103">Create Production Orders from Sales Orders</span></span>
<span data-ttu-id="5f693-104">Vous pouvez créer des ordres de fabrication pour les articles produits directement à partir des commandes vente.</span><span class="sxs-lookup"><span data-stu-id="5f693-104">You can create production orders for produced items directly from sales orders.</span></span>  

## <a name="to-create-a-production-order-from-a-sales-order"></a><span data-ttu-id="5f693-105">Pour créer un ordre de fabrication à partir d’une commande achat</span><span class="sxs-lookup"><span data-stu-id="5f693-105">To create a production order from a sales order</span></span>  

1.  <span data-ttu-id="5f693-106">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="5f693-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5f693-107">Sélectionnez la commande vente pour laquelle vous voulez créer un ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="5f693-107">Select the sales order you want to create a production order for.</span></span>  
3.  <span data-ttu-id="5f693-108">Sélectionnez l’action **Planification**.</span><span class="sxs-lookup"><span data-stu-id="5f693-108">Choose the **Planning** action.</span></span> <span data-ttu-id="5f693-109">Sur la page **Planification commande vente**, vous pouvez afficher la disponibilité de l’article de commande vente.</span><span class="sxs-lookup"><span data-stu-id="5f693-109">On the **Sales Order Planning** page, you can view the availability of the sales order item.</span></span>  
4.  <span data-ttu-id="5f693-110">Sélectionnez l’action **Créer O.F**.</span><span class="sxs-lookup"><span data-stu-id="5f693-110">Choose the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="5f693-111">Sélectionnez le statut et le type de commande.</span><span class="sxs-lookup"><span data-stu-id="5f693-111">Select the status and order type.</span></span>  
6.  <span data-ttu-id="5f693-112">Choisissez le bouton **Oui** pour créer un ou plusieurs ordres de fabrication pour les lignes ayant **Ordre de fabrication** dans le champ **Système réapprovisionnement**.</span><span class="sxs-lookup"><span data-stu-id="5f693-112">Choose the **Yes** button to create one or more production orders for the lines that have **Prod. Order** in their **Replenishment System** field.</span></span>


> [!NOTE]  
> <span data-ttu-id="5f693-113">Les lignes de demandes de l’ordre de fabrication créé qui ont **Ordre de fabrication** dans le champ **Système réapprovisionnelent** représentent des ordres de fabrication sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="5f693-113">Demand lines in the created production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="5f693-114">Après avoir généré ces ordres de fabrication, n’oubliez pas d’identifier toute demande de composant non réalisée pour ceux-ci à l’aide de la page **Planification commande** ou de la fonction **Replanifier** à partir d’ordres créés.</span><span class="sxs-lookup"><span data-stu-id="5f693-114">After you have generated these production orders, remember to identify any unfulfilled component demand for them using the **Order Planning** page or the **Replan** function from created orders.</span></span> 

## <a name="order-type"></a><span data-ttu-id="5f693-115">Type de commande</span><span class="sxs-lookup"><span data-stu-id="5f693-115">Order type</span></span>  
<span data-ttu-id="5f693-116">Vous pouvez choisir entre deux façons de créer les ordres de fabrication, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5f693-116">You can choose between two ways to create the production orders as outlined in the following table.</span></span>

|<span data-ttu-id="5f693-117">Option</span><span class="sxs-lookup"><span data-stu-id="5f693-117">Option</span></span>|<span data-ttu-id="5f693-118">Description</span><span class="sxs-lookup"><span data-stu-id="5f693-118">Description</span></span>|
|------|-----------|
|<span data-ttu-id="5f693-119">O.F. article</span><span class="sxs-lookup"><span data-stu-id="5f693-119">Item Order</span></span>|<span data-ttu-id="5f693-120">Un ordre de fabrication est créé pour chaque ordre de fabrication nécessaire qui est représenté par une ligne dans la fenêtre **Planification commande vente**.</span><span class="sxs-lookup"><span data-stu-id="5f693-120">One production order is created for each needed production order that is represented by a line in the **Sales Order Planning** window.</span></span>|
|<span data-ttu-id="5f693-121">O.F. projet</span><span class="sxs-lookup"><span data-stu-id="5f693-121">Project Order</span></span>|<span data-ttu-id="5f693-122">Un ordre de fabrication est créé pour tous les ordres de fabrication nécessaires qui sont représentés par des lignes dans la fenêtre **Planification commande vente**.</span><span class="sxs-lookup"><span data-stu-id="5f693-122">One production order is created for all needed production orders order that are represented by lines in the **Sales Order Planning** window.</span></span> |

<span data-ttu-id="5f693-123">Lorsque vous utilisez des O.F. projet, le champ **Type origine** de l’ordre de fabrication indique **En-tête vente** et l’ordre comporte plusieurs lignes, une pour chaque article de la ligne vente à produire.</span><span class="sxs-lookup"><span data-stu-id="5f693-123">When you use project orders, the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  


## <a name="see-also"></a><span data-ttu-id="5f693-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f693-124">See Also</span></span>  
[<span data-ttu-id="5f693-125">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="5f693-125">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="5f693-126">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="5f693-126">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="5f693-127">Stock</span><span class="sxs-lookup"><span data-stu-id="5f693-127">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="5f693-128">Achats</span><span class="sxs-lookup"><span data-stu-id="5f693-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="5f693-129">[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="5f693-129">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="5f693-130">Pratiques de configuration recommandées : planification de l’approvisionnement</span><span class="sxs-lookup"><span data-stu-id="5f693-130">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="5f693-131">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5f693-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
