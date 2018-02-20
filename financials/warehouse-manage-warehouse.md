---
title: "Activités entrepôt | Microsoft Docs"
description: "Entre la réception des biens et leur expédition, une série d'activités entrepôt internes a lieu pour assurer un flux efficace dans l'entrepôt, ainsi que pour organiser et mettre à jour les stocks de la société."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: c8d4ee33395c18cb7755fd1877b2af813fb9da43
ms.contentlocale: fr-ch
ms.lasthandoff: 02/02/2018

---
# <a name="warehouse-management"></a><span data-ttu-id="e42c3-103">Gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="e42c3-103">Warehouse Management</span></span>
<span data-ttu-id="e42c3-104">Entre la réception des biens et leur expédition, une série d'activités entrepôt internes a lieu pour assurer un flux efficace dans l'entrepôt, ainsi que pour organiser et mettre à jour les stocks de la société.</span><span class="sxs-lookup"><span data-stu-id="e42c3-104">After goods are received and before goods are shipped, a series of internal warehouse activities take place to ensure an effective flow through the warehouse and to organize and maintain company inventories.</span></span>

<span data-ttu-id="e42c3-105">Les activités entrepôt courantes, incluent le rangement d'articles, leur déplacement entre plusieurs entrepôts et leur prélèvement à des fins d'assemblage, de production et d'expédition.</span><span class="sxs-lookup"><span data-stu-id="e42c3-105">Typical warehouse activities include putting items away, moving items inside or between warehouses, and picking items for assembly, production, or shipment.</span></span> <span data-ttu-id="e42c3-106">Assembler des articles pour des ventes ou le stock peut également être considéré comme des activités entrepôt, mais cela est traité ailleurs.</span><span class="sxs-lookup"><span data-stu-id="e42c3-106">Assembling items for sale or inventory may also be considered warehouse activities, but these are covered elsewhere.</span></span> <span data-ttu-id="e42c3-107">Pour plus d'informations, voir [Gestion des assemblages](assembly-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="e42c3-107">For more information, see [Assembly Management](assembly-assemble-items.md).</span></span>  

<span data-ttu-id="e42c3-108">Dans les entrepôts importants, vous pouvez séparer ces tâches de traitement par département et gérer l'intégration par un flux suggéré.</span><span class="sxs-lookup"><span data-stu-id="e42c3-108">In large warehouses, these different handling tasks can be separated by departments and the integration managed by a directed workflow.</span></span> <span data-ttu-id="e42c3-109">Dans les installations plus simples, le flux est moins formalisé et vous pouvez exécuter les activités entrepôt avec les rangements et prélèvements stock.</span><span class="sxs-lookup"><span data-stu-id="e42c3-109">In simpler installations, the flow is less formalized and the warehouse activities are performed with so-called inventory put-aways and inventory picks.</span></span> <span data-ttu-id="e42c3-110">Pour plus d'informations sur les configurations entrepôt de base et avancées, voir [Détails de conception : vue d'ensemble d'entrepôt](design-details-warehouse-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e42c3-110">For more information about basic versus advanced warehouse configurations, see [Design Details: Warehouse Overview](design-details-warehouse-overview.md).</span></span>

<span data-ttu-id="e42c3-111">Avant d'effectuer des activités entrepôt, vous devez configurer le système pour la complexité de traitement d'entrepôt appropriée.</span><span class="sxs-lookup"><span data-stu-id="e42c3-111">Before you can perform warehouse activities, you must set the system up for the relevant complexity of warehouse processing.</span></span> <span data-ttu-id="e42c3-112">Pour plus d'informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="e42c3-112">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

 <span data-ttu-id="e42c3-113">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="e42c3-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="e42c3-114">**Pour**</span><span class="sxs-lookup"><span data-stu-id="e42c3-114">**To**</span></span>|<span data-ttu-id="e42c3-115">**Voir**</span><span class="sxs-lookup"><span data-stu-id="e42c3-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="e42c3-116">Enregistrer la réception d'articles dans les entrepôts, soit avec une commande achat uniquement, dans les configurations d'emplacement simples, soit avec une réception entrepôt, en cas de traitement d'entrepôt partiellement ou entièrement automatisé dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="e42c3-116">Record the receipt of items at warehouse locations, either with a purchase order only, in simple location setups, or with a warehouse receipt, in case of semi or fully automated warehouse processing at the location.</span></span>|[<span data-ttu-id="e42c3-117">Réceptionner des articles</span><span class="sxs-lookup"><span data-stu-id="e42c3-117">Receive Items</span></span>](warehouse-how-receive-items.md)|
|<span data-ttu-id="e42c3-118">Contourner les processus de rangement et de prélèvement pour expédier un article directement de la réception ou fabrication à l'expédition.</span><span class="sxs-lookup"><span data-stu-id="e42c3-118">Bypass the put-away and pick processes to expedite an item straight from receiving or production to shipping.</span></span>|[<span data-ttu-id="e42c3-119">Transborder des articles</span><span class="sxs-lookup"><span data-stu-id="e42c3-119">Cross-Dock Items</span></span>](warehouse-how-to-cross-dock-items.md)|    
|<span data-ttu-id="e42c3-120">Ranger les articles provenant des achats, retours vente, transferts ou de la production en fonction du processus d'entrepôt configuré.</span><span class="sxs-lookup"><span data-stu-id="e42c3-120">Put away items received from purchases, sales returns, transfers, or production output according to the configured warehouse process.</span></span>|[<span data-ttu-id="e42c3-121">Rangement des articles</span><span class="sxs-lookup"><span data-stu-id="e42c3-121">Putting Items Away</span></span>](warehouse-put-away-items.md)|
|<span data-ttu-id="e42c3-122">Déplacer des articles d'un emplacement à l'autre dans l'entrepôt.</span><span class="sxs-lookup"><span data-stu-id="e42c3-122">Move items between bins in the warehouse.</span></span>|[<span data-ttu-id="e42c3-123">Déplacement d'articles</span><span class="sxs-lookup"><span data-stu-id="e42c3-123">Moving Items</span></span>](warehouse-move-items.md)|
|<span data-ttu-id="e42c3-124">Prélever des articles à expédier, transférer ou consommer en assemblage ou production, en fonction du processus d'entrepôt configuré.</span><span class="sxs-lookup"><span data-stu-id="e42c3-124">Pick items to be shipped, transferred, or consumed in assembly or production, according to the configured warehouse process.</span></span>|[<span data-ttu-id="e42c3-125">Prélèvement des articles</span><span class="sxs-lookup"><span data-stu-id="e42c3-125">Picking Items</span></span>](warehouse-pick-items.md)|
|<span data-ttu-id="e42c3-126">Enregistrer l'expédition d'articles à partir des entrepôts, soit avec une commande vente uniquement, dans les configurations d'emplacement simples, soit avec une expédition entrepôt, en cas de traitements d'entrepôt partiellement ou entièrement automatisés dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="e42c3-126">Record the shipment of items from warehouse locations, either with a sales order only, in simple location setups, or with a warehouse shipment, in case of semi or fully automated warehouse processes at the location.</span></span>|[<span data-ttu-id="e42c3-127">Expédier des articles</span><span class="sxs-lookup"><span data-stu-id="e42c3-127">Ship Items</span></span>](warehouse-how-ship-items.md)|  

## <a name="see-also"></a><span data-ttu-id="e42c3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e42c3-128">See Also</span></span>  
[<span data-ttu-id="e42c3-129">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="e42c3-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="e42c3-130">[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="e42c3-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="e42c3-131">[Gestion des assemblages](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="e42c3-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="e42c3-132">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="e42c3-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="e42c3-133">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e42c3-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

