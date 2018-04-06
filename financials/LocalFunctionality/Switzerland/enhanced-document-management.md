---
title: "Gestion de documents améliorée"
description: "Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], vous pouvez archiver des documents et suivre le travail dans tous les documents archivés et non archivés."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: bc677eb2b3864e569b6f25a0df68301aee709202
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="enhanced-document-management"></a><span data-ttu-id="4a9f4-103">Gestion de documents améliorée</span><span class="sxs-lookup"><span data-stu-id="4a9f4-103">Enhanced Document Management</span></span>
<span data-ttu-id="4a9f4-104">Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], vous pouvez archiver des documents et suivre le travail dans tous les documents archivés et non archivés.</span><span class="sxs-lookup"><span data-stu-id="4a9f4-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can archive documents and track work across archived and non-archived documents.</span></span>  

## <a name="archiving-documents"></a><span data-ttu-id="4a9f4-105">Archivage de documents</span><span class="sxs-lookup"><span data-stu-id="4a9f4-105">Archiving Documents</span></span>  
 <span data-ttu-id="4a9f4-106">Vous pouvez utiliser la gestion améliorée des documents d'archives pour :</span><span class="sxs-lookup"><span data-stu-id="4a9f4-106">You can use enhanced archive document management to:</span></span>  

- <span data-ttu-id="4a9f4-107">Archiver les commandes ouvertes</span><span class="sxs-lookup"><span data-stu-id="4a9f4-107">Archive blanket orders</span></span>  
- <span data-ttu-id="4a9f4-108">Copier des documents</span><span class="sxs-lookup"><span data-stu-id="4a9f4-108">Copy documents</span></span>  
- <span data-ttu-id="4a9f4-109">Suivre des lignes document</span><span class="sxs-lookup"><span data-stu-id="4a9f4-109">Track document lines</span></span>  

## <a name="archiving-blanket-orders"></a><span data-ttu-id="4a9f4-110">Archivage des commandes ouvertes</span><span class="sxs-lookup"><span data-stu-id="4a9f4-110">Archiving Blanket Orders</span></span>  
<span data-ttu-id="4a9f4-111">Vous pouvez archiver des commandes achat et vente ouvertes, puis utiliser des commandes achat et vente ouvertes archivées pour créer des commandes achat et vente standard.</span><span class="sxs-lookup"><span data-stu-id="4a9f4-111">You can archive blanket sales and purchase orders, and use archived blanket sales and purchase orders to create standard sales and purchase orders.</span></span>  

<span data-ttu-id="4a9f4-112">Vous pouvez archiver automatiquement les éléments suivants chaque fois qu'un devis ou qu'une commande est supprimé(e) :</span><span class="sxs-lookup"><span data-stu-id="4a9f4-112">You can automatically archive the following each time a quote or order is deleted:</span></span>  

- <span data-ttu-id="4a9f4-113">Devis achat et vente</span><span class="sxs-lookup"><span data-stu-id="4a9f4-113">Sales and purchase quotes</span></span>  
- <span data-ttu-id="4a9f4-114">Commandes achat et vente ouvertes</span><span class="sxs-lookup"><span data-stu-id="4a9f4-114">Blanket sales and blanket purchase orders</span></span>  
- <span data-ttu-id="4a9f4-115">Commandes achat et vente</span><span class="sxs-lookup"><span data-stu-id="4a9f4-115">Sales and purchase orders</span></span>  

<span data-ttu-id="4a9f4-116">Vous pouvez supprimer la version archivée des commandes achat ouvertes ou des commandes vente ouvertes qui ont été supprimées à l'aide du traitement par lots **Supprimer versions commande achat ouvertes archivées** ou **Supprimer versions commande vente ouvertes archivées**.</span><span class="sxs-lookup"><span data-stu-id="4a9f4-116">You can delete the archived version of the blanket purchase orders or blanket sales orders that have been deleted using the **Delete Archived Blanket Purchase Order Version** batch job or **Delete Archived Blanket Sales Order Version** batch job.</span></span> <span data-ttu-id="4a9f4-117">En outre, vous pouvez copier les détails d'une commande ouverte archivée dans une commande.</span><span class="sxs-lookup"><span data-stu-id="4a9f4-117">Also, you can copy details from an archived blanket order to an order.</span></span>  

## <a name="tracking-document-lines"></a><span data-ttu-id="4a9f4-118">Suivi des lignes de document</span><span class="sxs-lookup"><span data-stu-id="4a9f4-118">Tracking Document Lines</span></span>  
<span data-ttu-id="4a9f4-119">Vous pouvez sélectionner une ligne de document au sein d'un type de document, puis l'afficher et récupérer les documents associés.</span><span class="sxs-lookup"><span data-stu-id="4a9f4-119">You can select a document line within a document type, and view and retrieve the related documents.</span></span> <span data-ttu-id="4a9f4-120">Vous pouvez suivre les lignes de document provenant de :</span><span class="sxs-lookup"><span data-stu-id="4a9f4-120">You can track document lines from:</span></span>  

- <span data-ttu-id="4a9f4-121">Commandes</span><span class="sxs-lookup"><span data-stu-id="4a9f4-121">Orders</span></span>  
- <span data-ttu-id="4a9f4-122">Commandes archivées</span><span class="sxs-lookup"><span data-stu-id="4a9f4-122">Archived orders</span></span>  
- <span data-ttu-id="4a9f4-123">Commandes ouvertes ;</span><span class="sxs-lookup"><span data-stu-id="4a9f4-123">Blanket orders</span></span>  
- <span data-ttu-id="4a9f4-124">Commandes ouvertes archivées</span><span class="sxs-lookup"><span data-stu-id="4a9f4-124">Archived blanket orders</span></span>  
- <span data-ttu-id="4a9f4-125">Demandes de prix</span><span class="sxs-lookup"><span data-stu-id="4a9f4-125">Quotes</span></span>  
- <span data-ttu-id="4a9f4-126">Devis archivés</span><span class="sxs-lookup"><span data-stu-id="4a9f4-126">Archived quotes</span></span>  
- <span data-ttu-id="4a9f4-127">Expéditions enregistrées</span><span class="sxs-lookup"><span data-stu-id="4a9f4-127">Posted shipments</span></span>  
- <span data-ttu-id="4a9f4-128">Factures enregistrées</span><span class="sxs-lookup"><span data-stu-id="4a9f4-128">Posted invoices</span></span>  

## <a name="see-also"></a><span data-ttu-id="4a9f4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a9f4-129">See Also</span></span>  
 <span data-ttu-id="4a9f4-130">[Créer des commandes vente ouvertes](../../sales-how-to-create-blanket-sales-orders.md) </span><span class="sxs-lookup"><span data-stu-id="4a9f4-130">[Create Blanket Sales Orders](../../sales-how-to-create-blanket-sales-orders.md) </span></span>  
 [<span data-ttu-id="4a9f4-131">Suivre des lignes document</span><span class="sxs-lookup"><span data-stu-id="4a9f4-131">Track Document Lines</span></span>](how-to-track-document-lines.md)

