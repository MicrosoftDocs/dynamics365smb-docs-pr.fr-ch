---
title: "Procédure d'affectation d'emplacements par défaut à des articles | Microsoft Docs"
description: "Si vous utilisez des emplacements dans un magasin, l'affectation d'emplacements par défaut à vos articles peut simplifier considérablement leur processus d'expédition, de réception et de déplacement. Lorsqu'un emplacement par défaut est affecté à un article, cet emplacement est suggéré chaque fois que vous lancez une transaction pour cet article."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2075010c892893d28c7ae3fe627709669bc80a38
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="assign-default-bins-to-items"></a><span data-ttu-id="6e684-104">Affecter des emplacements par défaut à des articles</span><span class="sxs-lookup"><span data-stu-id="6e684-104">Assign Default Bins to Items</span></span>
<span data-ttu-id="6e684-105">Si vous utilisez des emplacements dans un magasin, l'affectation d'emplacements par défaut à vos articles peut simplifier considérablement leur processus d'expédition, de réception et de déplacement.</span><span class="sxs-lookup"><span data-stu-id="6e684-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="6e684-106">Lorsqu'un emplacement par défaut est affecté à un article, cet emplacement est suggéré chaque fois que vous lancez une transaction pour cet article.</span><span class="sxs-lookup"><span data-stu-id="6e684-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="6e684-107">Les emplacements par défaut sont définis dans la fenêtre **Contenu emplacement**.</span><span class="sxs-lookup"><span data-stu-id="6e684-107">Default bins are defined in the **Bin Content** window.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="6e684-108">Pour affecter un emplacement par défaut à un article</span><span class="sxs-lookup"><span data-stu-id="6e684-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="6e684-109">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille création contenu emplacement**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="6e684-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="6e684-110">Renseignez le code emplacement et les informations article pour chaque emplacement que vous souhaitez définir par défaut pour un article.</span><span class="sxs-lookup"><span data-stu-id="6e684-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="6e684-111">Veillez à sélectionner le champ **Valeur par défaut**.</span><span class="sxs-lookup"><span data-stu-id="6e684-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="6e684-112">Choisissez l'action **Créer contenu emplacement**.</span><span class="sxs-lookup"><span data-stu-id="6e684-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="6e684-113">Des emplacements par défaut sont maintenant affectés à votre article.</span><span class="sxs-lookup"><span data-stu-id="6e684-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6e684-114">Lorsqu'un article est rangé, si un emplacement par défaut ne lui est pas affecté, l'emplacement dans lequel l'article est rangé est affecté par défaut.</span><span class="sxs-lookup"><span data-stu-id="6e684-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="6e684-115">Pour modifier l'emplacement par défaut pour un article</span><span class="sxs-lookup"><span data-stu-id="6e684-115">To change the default bin for an item</span></span>  
<span data-ttu-id="6e684-116">Vous pouvez être amené à modifier l'affectation de l'emplacement par défaut pour un article ou à affecter un emplacement par défaut à un nouvel article.</span><span class="sxs-lookup"><span data-stu-id="6e684-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="6e684-117">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Contenu emplacement**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="6e684-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6e684-118">Dans le champ **Filtre magasin**, sélectionnez le code emplacement approprié.</span><span class="sxs-lookup"><span data-stu-id="6e684-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="6e684-119">Recherchez l'écriture indiquant le contenu de l'emplacement par défaut pour cet article et désactivez la case à cocher **Emplacement par déf.**.</span><span class="sxs-lookup"><span data-stu-id="6e684-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="6e684-120">Recherchez la ligne contenu emplacement de l'emplacement que vous souhaitez paramétrer comme étant le nouvel emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="6e684-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="6e684-121">Cochez la case **Emplacement par défaut**.</span><span class="sxs-lookup"><span data-stu-id="6e684-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6e684-122">Lorsqu'un article est rangé pour la première fois, et si un emplacement par défaut ne lui est pas affecté, le système lui affecte comme emplacement par défaut celui dans lequel l'article est rangé.</span><span class="sxs-lookup"><span data-stu-id="6e684-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6e684-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e684-123">See Also</span></span>  
[<span data-ttu-id="6e684-124">Gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="6e684-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="6e684-125">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="6e684-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="6e684-126">[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="6e684-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="6e684-127">[Gestion des assemblages](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="6e684-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="6e684-128">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="6e684-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="6e684-129">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6e684-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

