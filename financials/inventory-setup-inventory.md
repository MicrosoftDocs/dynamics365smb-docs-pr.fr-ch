---
title: Configuration de stock| Microsoft Docs
description: "Décrit comment configurer les processus de stock et d'inventaire, y compris les acheminements pour le transfert et les magasins, tels que des entrepôts."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 01/12/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5a667f28bd50bbd1149526e08e0d786da83bc8a6
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-inventory"></a><span data-ttu-id="4c7df-103">Configuration de stock</span><span class="sxs-lookup"><span data-stu-id="4c7df-103">Setting Up Inventory</span></span>
<span data-ttu-id="4c7df-104">Avant de pouvoir gérer les activités entrepôt et les coûts de stock, vous devez configurer les règles et les valeurs qui définissent les stratégies de stock de la société.</span><span class="sxs-lookup"><span data-stu-id="4c7df-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="4c7df-105">Vous pouvez fournir un meilleur service clientèle et optimiser votre chaîne d'approvisionnement en organisant votre stock à différentes adresses.</span><span class="sxs-lookup"><span data-stu-id="4c7df-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="4c7df-106">Vous pouvez ensuite acheter, stocker, ou vendre des articles dans les magasins et transférer des articles en stock entre eux.</span><span class="sxs-lookup"><span data-stu-id="4c7df-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="4c7df-107">Lorsque vous avez configuré votre stock, vous pouvez gérer différents processus associés aux transactions article.</span><span class="sxs-lookup"><span data-stu-id="4c7df-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="4c7df-108">Pour plus d'informations, voir [Gérer le stock](inventory-manage-inventory.md) et [Gestion d'entrepôt](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="4c7df-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="4c7df-109">À</span><span class="sxs-lookup"><span data-stu-id="4c7df-109">To</span></span> | <span data-ttu-id="4c7df-110">Voir</span><span class="sxs-lookup"><span data-stu-id="4c7df-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="4c7df-111">Définir la configuration générale de stock, telles que la souche de numéros et comment utiliser des magasins.</span><span class="sxs-lookup"><span data-stu-id="4c7df-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="4c7df-112">Définir des informations générales relatives aux stocks</span><span class="sxs-lookup"><span data-stu-id="4c7df-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="4c7df-113">Configurez un modèle de distribution efficace avec une combinaison de différents magasins et centres de gestion affectés aux partenaires commerciaux ou aux employés.</span><span class="sxs-lookup"><span data-stu-id="4c7df-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="4c7df-114">Utiliser les centres de gestion</span><span class="sxs-lookup"><span data-stu-id="4c7df-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="4c7df-115">Planifier votre stock dans plusieurs magasins, y compris des acheminements transfert.</span><span class="sxs-lookup"><span data-stu-id="4c7df-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="4c7df-116">Configurer des magasins</span><span class="sxs-lookup"><span data-stu-id="4c7df-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="4c7df-117">Créer des fiches article pour les articles en stock que vous commercialisez.</span><span class="sxs-lookup"><span data-stu-id="4c7df-117">Create item cards for inventory items that you trade in.</span></span> |[<span data-ttu-id="4c7df-118">Enregistrer de nouveaux articles</span><span class="sxs-lookup"><span data-stu-id="4c7df-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="4c7df-119">Définissez plusieurs unités pour un article afin de pouvoir l'utiliser comme UOM secondaire, par exemple pour les transactions de ventes, d'achat ou de production.</span><span class="sxs-lookup"><span data-stu-id="4c7df-119">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="4c7df-120">Configuration d'unités article</span><span class="sxs-lookup"><span data-stu-id="4c7df-120">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="4c7df-121">En complément aux fiches article, enregistrer des informations relatives à vos articles dans un magasin spécifique ou d'une variante spécifique.</span><span class="sxs-lookup"><span data-stu-id="4c7df-121">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="4c7df-122">Configurer des points de stock</span><span class="sxs-lookup"><span data-stu-id="4c7df-122">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="4c7df-123">Affecter des articles aux catégories et leur donner des attributs pour vous aider, vous et vos clients, à trouver des articles.</span><span class="sxs-lookup"><span data-stu-id="4c7df-123">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="4c7df-124">Catégoriser des articles</span><span class="sxs-lookup"><span data-stu-id="4c7df-124">Categorize Items</span></span>](inventory-how-categorize-items.md) |

## <a name="see-also"></a><span data-ttu-id="4c7df-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c7df-125">See Also</span></span>
[<span data-ttu-id="4c7df-126">Gestion du stock</span><span class="sxs-lookup"><span data-stu-id="4c7df-126">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="4c7df-127">Gestion des achats</span><span class="sxs-lookup"><span data-stu-id="4c7df-127">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4c7df-128">[Gestion des ventes](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="4c7df-128">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="4c7df-129">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4c7df-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4c7df-130">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="4c7df-130">General Business Functionality</span></span>](ui-across-business-areas.md)

