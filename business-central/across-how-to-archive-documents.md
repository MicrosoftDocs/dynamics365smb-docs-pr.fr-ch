---
title: "Procédure d'archivage des documents vente et achat | Microsoft Docs"
description: "Vous pouvez archiver des commandes vente et achat, des devis, des retours et des commandes ouvertes, et vous pouvez utiliser le document archivé pour recréer le document d'origine."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a><span data-ttu-id="5a54b-103">Archiver des documents</span><span class="sxs-lookup"><span data-stu-id="5a54b-103">Archive Documents</span></span>
<span data-ttu-id="5a54b-104">Vous pouvez archiver des commandes vente et achat, des devis, des retours et des commandes ouvertes, et vous pouvez utiliser le document archivé pour recréer le document d'origine.</span><span class="sxs-lookup"><span data-stu-id="5a54b-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="5a54b-105">Pour configurer l'archivage automatique des documents</span><span class="sxs-lookup"><span data-stu-id="5a54b-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="5a54b-106">Vous pouvez configurer l'archivage automatique des commandes vente et achat, des devis, des commandes ouvertes et des retours, avant de supprimer des documents.</span><span class="sxs-lookup"><span data-stu-id="5a54b-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="5a54b-107">La procédure suivante décrit comment configurer l'archivage automatique des documents vente.</span><span class="sxs-lookup"><span data-stu-id="5a54b-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="5a54b-108">La procédure est identique pour les documents achat.</span><span class="sxs-lookup"><span data-stu-id="5a54b-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="5a54b-109">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône"), entrez **Paramètres ventes**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="5a54b-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="5a54b-110">Dans la fenêtre **Paramètres ventes**, renseignez les champs comme suit.</span><span class="sxs-lookup"><span data-stu-id="5a54b-110">In the **Sales & Receivables Setup** window, fill in the fields as follows.</span></span>

|<span data-ttu-id="5a54b-111">Champ</span><span class="sxs-lookup"><span data-stu-id="5a54b-111">Field</span></span>|<span data-ttu-id="5a54b-112">Désignation</span><span class="sxs-lookup"><span data-stu-id="5a54b-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="5a54b-113">**Archivage des devis**</span><span class="sxs-lookup"><span data-stu-id="5a54b-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="5a54b-114">**Jamais** pour ne jamais archiver les devis lorsqu'ils sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="5a54b-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="5a54b-115">**Question** pour demander à l'utilisateur s'il souhaite archiver les devis lorsqu'ils sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="5a54b-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="5a54b-116">**Toujours** pour archiver automatiquement les devis lorsqu'ils sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="5a54b-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="5a54b-117">**Archivage des commandes vente ouvertes**</span><span class="sxs-lookup"><span data-stu-id="5a54b-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="5a54b-118">Permet d'archiver automatiquement les commandes ouvertes vente lorsqu'elles sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="5a54b-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="5a54b-119">**Arch. commandes et retours**</span><span class="sxs-lookup"><span data-stu-id="5a54b-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="5a54b-120">Permet d'archiver automatiquement les commandes vente lorsqu'elles sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="5a54b-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="5a54b-121">Pour archiver une commande vente</span><span class="sxs-lookup"><span data-stu-id="5a54b-121">To archive a sales order</span></span>
<span data-ttu-id="5a54b-122">La procédure suivante décrit comment archiver une commande vente.</span><span class="sxs-lookup"><span data-stu-id="5a54b-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="5a54b-123">La procédure est identique pour les commandes, les commandes ouvertes, les retours et les devis.</span><span class="sxs-lookup"><span data-stu-id="5a54b-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="5a54b-124">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="5a54b-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5a54b-125">Ouvrez une commande vente que vous souhaitez archiver.</span><span class="sxs-lookup"><span data-stu-id="5a54b-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="5a54b-126">Sélectionnez l'action **Archiver document**.</span><span class="sxs-lookup"><span data-stu-id="5a54b-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="5a54b-127">La commande vente est archivée.</span><span class="sxs-lookup"><span data-stu-id="5a54b-127">The sales order is archived.</span></span> <span data-ttu-id="5a54b-128">Vous pouvez l'afficher dans la fenêtre **Commandes vente archivées**.</span><span class="sxs-lookup"><span data-stu-id="5a54b-128">You can view it in the **Archived Sales orders** window.</span></span> <span data-ttu-id="5a54b-129">Vous pouvez également l'utiliser pour recréer la commande vente d'origine.</span><span class="sxs-lookup"><span data-stu-id="5a54b-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="5a54b-130">Pour recréer une commande vente à partir de l'archive</span><span class="sxs-lookup"><span data-stu-id="5a54b-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="5a54b-131">La procédure suivante décrit comment recréer une commande vente.</span><span class="sxs-lookup"><span data-stu-id="5a54b-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="5a54b-132">La procédure est identique pour les commandes, les commandes ouvertes, les retours et les devis.</span><span class="sxs-lookup"><span data-stu-id="5a54b-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="5a54b-133">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente archivées**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="5a54b-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="5a54b-134">Sélectionnez la commande vente archivée que vous voulez recréer, puis sélectionnez l'action **Restaurer**.</span><span class="sxs-lookup"><span data-stu-id="5a54b-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="5a54b-135">La commande vente est créée et ajoutée à la fenêtre **Commandes vente**.</span><span class="sxs-lookup"><span data-stu-id="5a54b-135">The sales order is created and added to the **Sales Orders** window.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="5a54b-136">Pour supprimer des commandes vente archivées</span><span class="sxs-lookup"><span data-stu-id="5a54b-136">To delete archived sales orders</span></span>
<span data-ttu-id="5a54b-137">La procédure suivante décrit comment supprimer des commandes vente archivées.</span><span class="sxs-lookup"><span data-stu-id="5a54b-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="5a54b-138">La procédure est identique pour les autres documents achat et vente archivés.</span><span class="sxs-lookup"><span data-stu-id="5a54b-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="5a54b-139">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Supprimer versions cde vente archivées**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="5a54b-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5a54b-140">Dans la fenêtre **Supprimer versions cde vente archivées**, sélectionnez les filtres appropriés.</span><span class="sxs-lookup"><span data-stu-id="5a54b-140">In the **Delete Archived Sales Order Versions** window, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="5a54b-141">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a54b-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a54b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a54b-142">See Also</span></span>
[<span data-ttu-id="5a54b-143">Suivre des lignes document</span><span class="sxs-lookup"><span data-stu-id="5a54b-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="5a54b-144">Ventes</span><span class="sxs-lookup"><span data-stu-id="5a54b-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="5a54b-145">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="5a54b-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="5a54b-146">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5a54b-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

