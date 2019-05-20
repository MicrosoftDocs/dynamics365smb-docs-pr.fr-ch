---
title: Procédure d'archivage des documents vente et achat | Microsoft Docs
description: Vous pouvez archiver des commandes vente et achat, des devis, des retours et des commandes ouvertes, et vous pouvez utiliser le document archivé pour recréer le document d'origine.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 32a50a2b1b967fa2f19022ab6e07865716243d8e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245677"
---
# <a name="archive-documents"></a><span data-ttu-id="d334b-103">Archiver des documents</span><span class="sxs-lookup"><span data-stu-id="d334b-103">Archive Documents</span></span>
<span data-ttu-id="d334b-104">Vous pouvez archiver des commandes vente et achat, des devis, des commandes retour, et des commandes ouvertes, par exemple parce que vous voulez enregistrer une copie d'un document pour la réutiliser plus tard.</span><span class="sxs-lookup"><span data-stu-id="d334b-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, for example because you want to save a copy of a document for reuse later.</span></span> <span data-ttu-id="d334b-105">Vous pouvez archiver des documents vente ou achat plusieurs fois, en enregistrant une version archivée différente chaque fois.</span><span class="sxs-lookup"><span data-stu-id="d334b-105">You can archive a sales or purchase document several times, saving a different archived version each time.</span></span>

<span data-ttu-id="d334b-106">Pour les documents archivés où l'original existe et n'est pas validé, vous pouvez utiliser la fonction **Restaurer** pour remplacer l'original par la version archivée du document.</span><span class="sxs-lookup"><span data-stu-id="d334b-106">For archived documents where the original still exists and is not posted, you can use the **Restore** function to overwrite the original with the archived version of the document.</span></span> <span data-ttu-id="d334b-107">Ceci est commode si vous devez restaurer le contenu d'un document à un état précédemment.</span><span class="sxs-lookup"><span data-stu-id="d334b-107">This is practical if you need to restore the contents of a document to an earlier state.</span></span>

<span data-ttu-id="d334b-108">Pour les documents archivés où l'original est désactivé, vous pouvez réutiliser le contenu qu'en copiant les données, par exemple avec la fonction **Copier document**.</span><span class="sxs-lookup"><span data-stu-id="d334b-108">For archived documents where the original is deleted, you can only reuse the content by copying the data, for example with the **Copy Document** function.</span></span>   

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="d334b-109">Pour configurer l'archivage automatique des documents</span><span class="sxs-lookup"><span data-stu-id="d334b-109">To set up automatic document archiving</span></span>  
<span data-ttu-id="d334b-110">Vous pouvez configurer l'archivage automatique des commandes vente et achat, des devis, des commandes ouvertes et des retours, avant de supprimer des documents.</span><span class="sxs-lookup"><span data-stu-id="d334b-110">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="d334b-111">La procédure suivante décrit comment configurer l'archivage automatique des documents vente.</span><span class="sxs-lookup"><span data-stu-id="d334b-111">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="d334b-112">La procédure est identique pour les documents achat.</span><span class="sxs-lookup"><span data-stu-id="d334b-112">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="d334b-113">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres ventes**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="d334b-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="d334b-114">Sur la page **Paramètres ventes**, renseignez les champs comme suit.</span><span class="sxs-lookup"><span data-stu-id="d334b-114">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="d334b-115">Champ</span><span class="sxs-lookup"><span data-stu-id="d334b-115">Field</span></span>|<span data-ttu-id="d334b-116">Désignation</span><span class="sxs-lookup"><span data-stu-id="d334b-116">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="d334b-117">**Archivage des devis**</span><span class="sxs-lookup"><span data-stu-id="d334b-117">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="d334b-118">**Jamais** pour ne jamais archiver les devis lorsqu'ils sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="d334b-118">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="d334b-119">**Question** pour demander à l'utilisateur s'il souhaite archiver les devis lorsqu'ils sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="d334b-119">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="d334b-120">**Toujours** pour archiver automatiquement les devis lorsqu'ils sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="d334b-120">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="d334b-121">**Archivage des commandes vente ouvertes**</span><span class="sxs-lookup"><span data-stu-id="d334b-121">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="d334b-122">Permet d'archiver automatiquement les commandes ouvertes vente lorsqu'elles sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="d334b-122">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="d334b-123">**Arch. commandes et retours**</span><span class="sxs-lookup"><span data-stu-id="d334b-123">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="d334b-124">Permet d'archiver automatiquement les commandes vente lorsqu'elles sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="d334b-124">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="d334b-125">Pour archiver une commande vente</span><span class="sxs-lookup"><span data-stu-id="d334b-125">To archive a sales order</span></span>
<span data-ttu-id="d334b-126">La procédure suivante décrit comment archiver une commande vente.</span><span class="sxs-lookup"><span data-stu-id="d334b-126">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="d334b-127">La procédure est identique pour les commandes, les commandes ouvertes, les retours et les devis.</span><span class="sxs-lookup"><span data-stu-id="d334b-127">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="d334b-128">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="d334b-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d334b-129">Ouvrez une commande vente que vous souhaitez archiver.</span><span class="sxs-lookup"><span data-stu-id="d334b-129">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="d334b-130">Sélectionnez l'action **Archiver document**.</span><span class="sxs-lookup"><span data-stu-id="d334b-130">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="d334b-131">La commande vente est archivée.</span><span class="sxs-lookup"><span data-stu-id="d334b-131">The sales order is archived.</span></span> <span data-ttu-id="d334b-132">Vous pouvez l'afficher sur la page **Commandes vente archivées**.</span><span class="sxs-lookup"><span data-stu-id="d334b-132">You can view it on the **Archived Sales orders** page.</span></span>

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a><span data-ttu-id="d334b-133">Pour restaurer une commande vente non validée depuis les archives</span><span class="sxs-lookup"><span data-stu-id="d334b-133">To restore a non-posted sales order from the archive</span></span>
<span data-ttu-id="d334b-134">La procédure suivante décrit comment insérer le contenu d'une commande vente archivée dans la commande vente d'origine.</span><span class="sxs-lookup"><span data-stu-id="d334b-134">The following procedure describes how to bring the contents of an archived sales order back to the original sales order.</span></span> <span data-ttu-id="d334b-135">Cela n'est possible que lorsque le document source n'a pas été validé.</span><span class="sxs-lookup"><span data-stu-id="d334b-135">This is only possible when the original document has not been posted.</span></span> <span data-ttu-id="d334b-136">La procédure est identique pour les commandes, les commandes ouvertes, les retours et les devis.</span><span class="sxs-lookup"><span data-stu-id="d334b-136">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1. <span data-ttu-id="d334b-137">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente archivées**, et sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="d334b-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="d334b-138">Sélectionnez la commande vente archivée, ou une version de celle-ci, que vous voulez restaurer, puis sélectionnez l'action **Restaurer**.</span><span class="sxs-lookup"><span data-stu-id="d334b-138">Select the archived sales order, or version of it, that you want to restore, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="d334b-139">Le contenu de la commande vente d'origine est remplacé par celui de la version archivée sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d334b-139">The contents of the original sales order is replaced with that of the selected archived version.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="d334b-140">Pour supprimer des commandes vente archivées</span><span class="sxs-lookup"><span data-stu-id="d334b-140">To delete archived sales orders</span></span>
<span data-ttu-id="d334b-141">La procédure suivante décrit comment supprimer des commandes vente archivées.</span><span class="sxs-lookup"><span data-stu-id="d334b-141">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="d334b-142">La procédure est identique pour les autres documents achat et vente archivés.</span><span class="sxs-lookup"><span data-stu-id="d334b-142">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="d334b-143">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer versions cde vente archivées**, et sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="d334b-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d334b-144">Sur la page **Supprimer versions cde vente archivées**, sélectionnez les filtres appropriés.</span><span class="sxs-lookup"><span data-stu-id="d334b-144">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="d334b-145">Choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="d334b-145">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="d334b-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d334b-146">See Also</span></span>
[<span data-ttu-id="d334b-147">Suivre des lignes document</span><span class="sxs-lookup"><span data-stu-id="d334b-147">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="d334b-148">Ventes</span><span class="sxs-lookup"><span data-stu-id="d334b-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="d334b-149">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="d334b-149">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="d334b-150">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d334b-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
