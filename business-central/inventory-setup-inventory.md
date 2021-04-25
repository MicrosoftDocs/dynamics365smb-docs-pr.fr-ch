---
title: Configuration de stock| Microsoft Docs
description: Décrit comment configurer les processus de stock et d’inventaire, y compris les acheminements pour le transfert et les magasins, tels que des entrepôts.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2798031fcb9796d14daa94d6614bd5da1081d32e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785588"
---
# <a name="setting-up-inventory"></a><span data-ttu-id="e56aa-103">Configuration de stock</span><span class="sxs-lookup"><span data-stu-id="e56aa-103">Setting Up Inventory</span></span>
<span data-ttu-id="e56aa-104">Avant de pouvoir gérer les activités entrepôt et les coûts de stock, vous devez configurer les règles et les valeurs qui définissent les stratégies de stock de la société.</span><span class="sxs-lookup"><span data-stu-id="e56aa-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="e56aa-105">Vous pouvez fournir un meilleur service clientèle et optimiser votre chaîne d’approvisionnement en organisant votre stock à différentes adresses.</span><span class="sxs-lookup"><span data-stu-id="e56aa-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="e56aa-106">Vous pouvez ensuite acheter, stocker, ou vendre des articles dans les magasins et transférer des articles en stock entre eux.</span><span class="sxs-lookup"><span data-stu-id="e56aa-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="e56aa-107">Lorsque vous avez configuré votre stock, vous pouvez gérer différents processus associés aux transactions article.</span><span class="sxs-lookup"><span data-stu-id="e56aa-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="e56aa-108">Pour plus d’informations, voir [Gérer le stock](inventory-manage-inventory.md) et [Gestion d’entrepôt](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="e56aa-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="e56aa-109">À</span><span class="sxs-lookup"><span data-stu-id="e56aa-109">To</span></span> | <span data-ttu-id="e56aa-110">Voir</span><span class="sxs-lookup"><span data-stu-id="e56aa-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="e56aa-111">Définir la configuration générale de stock, telles que la souche de numéros et comment utiliser des magasins.</span><span class="sxs-lookup"><span data-stu-id="e56aa-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="e56aa-112">Définir des informations générales relatives aux stocks</span><span class="sxs-lookup"><span data-stu-id="e56aa-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="e56aa-113">Configurez un modèle de distribution efficace avec une combinaison de différents magasins et centres de gestion affectés aux partenaires commerciaux ou aux employés.</span><span class="sxs-lookup"><span data-stu-id="e56aa-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="e56aa-114">Utiliser les centres de gestion</span><span class="sxs-lookup"><span data-stu-id="e56aa-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="e56aa-115">Planifier votre stock dans plusieurs magasins, y compris des acheminements transfert.</span><span class="sxs-lookup"><span data-stu-id="e56aa-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="e56aa-116">Configurer des magasins</span><span class="sxs-lookup"><span data-stu-id="e56aa-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="e56aa-117">Créez des fiches article pour les articles de stock, hors stock ou service que vous négociez.</span><span class="sxs-lookup"><span data-stu-id="e56aa-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="e56aa-118">Enregistrer de nouveaux articles</span><span class="sxs-lookup"><span data-stu-id="e56aa-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="e56aa-119">Utilisez la fonction **Copier l’élément** pour créer rapidement une nouvelle fiche article basée sur une fiche existante.</span><span class="sxs-lookup"><span data-stu-id="e56aa-119">Use the **Copy Item** function to quickly create a new item card based on an existing one.</span></span>|[<span data-ttu-id="e56aa-120">Copier des articles existants pour créer de nouveaux articles</span><span class="sxs-lookup"><span data-stu-id="e56aa-120">Copy Existing Items to Create New Items</span></span>](inventory-how-copy-items.md)|
|<span data-ttu-id="e56aa-121">Apprendre comment renseigner le champ **Type** sur les fiches article en fonction de l’objectif commercial.</span><span class="sxs-lookup"><span data-stu-id="e56aa-121">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="e56aa-122">À propos des types d’articles</span><span class="sxs-lookup"><span data-stu-id="e56aa-122">About Item Types</span></span>](inventory-about-item-types.md)|
|<span data-ttu-id="e56aa-123">Définissez plusieurs unités pour un article afin de pouvoir l’utiliser comme UOM secondaire, par exemple pour les transactions de ventes, d’achat ou de production.</span><span class="sxs-lookup"><span data-stu-id="e56aa-123">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="e56aa-124">Configuration d’unités article</span><span class="sxs-lookup"><span data-stu-id="e56aa-124">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="e56aa-125">En complément aux fiches article, enregistrer des informations relatives à vos articles dans un magasin spécifique ou d’une variante spécifique.</span><span class="sxs-lookup"><span data-stu-id="e56aa-125">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="e56aa-126">Configurer des points de stock</span><span class="sxs-lookup"><span data-stu-id="e56aa-126">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="e56aa-127">Affecter des articles aux catégories et leur donner des attributs pour vous aider, vous et vos clients, à trouver des articles.</span><span class="sxs-lookup"><span data-stu-id="e56aa-127">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="e56aa-128">Catégoriser des articles</span><span class="sxs-lookup"><span data-stu-id="e56aa-128">Categorize Items</span></span>](inventory-how-categorize-items.md) |
|<span data-ttu-id="e56aa-129">Importez plusieurs images d’article en une seule fois depuis un fichier zip où les fichiers sont nommés selon les numéros d’article.</span><span class="sxs-lookup"><span data-stu-id="e56aa-129">Import multiple item pictures in one go from a zip file where the files are named according to item numbers.</span></span>|[<span data-ttu-id="e56aa-130">Importer plusieurs images d’article</span><span class="sxs-lookup"><span data-stu-id="e56aa-130">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)|
|<span data-ttu-id="e56aa-131">Spécifiez les états par défaut à utiliser pour différents types de documents.</span><span class="sxs-lookup"><span data-stu-id="e56aa-131">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="e56aa-132">Sélection des états dans Business Central</span><span class="sxs-lookup"><span data-stu-id="e56aa-132">Report Selection in Business Central</span></span>](across-report-selections.md)|

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="e56aa-133">Voir la formation associée sur [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="e56aa-133">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="e56aa-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e56aa-134">See Also</span></span>

[<span data-ttu-id="e56aa-135">Gestion du stock</span><span class="sxs-lookup"><span data-stu-id="e56aa-135">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="e56aa-136">Gestion des achats</span><span class="sxs-lookup"><span data-stu-id="e56aa-136">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="e56aa-137">[Gestion des ventes](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="e56aa-137">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="e56aa-138">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e56aa-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="e56aa-139">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="e56aa-139">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]