---
title: "Procédure : Paramétrer l'archivage automatique des documents en Suisse"
description: Vous pouvez configurer l'archivage automatique des documents vente et achat, tels que des devis ou des commandes ouvertes, avant de supprimer des documents.
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
ms.openlocfilehash: 09fca5cba94bed83b862cd8bb9d4b5be895c509d
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-automatic-archiving-of-documents-in-switzerland"></a><span data-ttu-id="78c4b-103">Paramétrer l'archivage automatique des documents en Suisse</span><span class="sxs-lookup"><span data-stu-id="78c4b-103">Set Up Automatic Archiving of Documents in Switzerland</span></span>
<span data-ttu-id="78c4b-104">Vous pouvez configurer l'archivage automatique des documents vente et achat, tels que des devis ou des commandes ouvertes, avant de supprimer des documents.</span><span class="sxs-lookup"><span data-stu-id="78c4b-104">You can set up automatic archiving of sales documents and purchase documents—such as quotes, blanket orders, and orders—before you delete documents.</span></span>  

<span data-ttu-id="78c4b-105">La procédure suivante décrit comment configurer l'archivage automatique des documents vente, mais les mêmes étapes s'appliquent également aux documents achat.</span><span class="sxs-lookup"><span data-stu-id="78c4b-105">The following procedure describes how to set up automatic archiving of sales documents, but the same steps apply to purchase documents.</span></span>  

## <a name="to-set-up-automatic-archiving-of-documents"></a><span data-ttu-id="78c4b-106">Pour configurer l'archivage automatique des documents</span><span class="sxs-lookup"><span data-stu-id="78c4b-106">To set up automatic archiving of documents</span></span>  

1.  <span data-ttu-id="78c4b-107">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône"), entrez **Paramètres ventes**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="78c4b-107">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="78c4b-108">Dans la fenêtre **Paramètres &ventes**, sur le raccourci **Archivage**, renseignez les champs comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="78c4b-108">On the **Sales & Receivables Setup** window, on the **Archiving** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="78c4b-109">Champ</span><span class="sxs-lookup"><span data-stu-id="78c4b-109">Field</span></span>|<span data-ttu-id="78c4b-110">Désignation</span><span class="sxs-lookup"><span data-stu-id="78c4b-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="78c4b-111">**Archivage des devis**</span><span class="sxs-lookup"><span data-stu-id="78c4b-111">**Archiving Sales Quote**</span></span>|<span data-ttu-id="78c4b-112">**Jamais** pour ne jamais archiver les devis lorsqu'ils sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="78c4b-112">**Never** to never archive sales quotes when they are deleted.</span></span><br /><br /> <span data-ttu-id="78c4b-113">-ou-</span><span class="sxs-lookup"><span data-stu-id="78c4b-113">–or–</span></span><br /><br /> <span data-ttu-id="78c4b-114">**Question** pour demander à l'utilisateur s'il souhaite archiver les devis lorsqu'ils sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="78c4b-114">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span><br /><br /> <span data-ttu-id="78c4b-115">-ou-</span><span class="sxs-lookup"><span data-stu-id="78c4b-115">–or–</span></span><br /><br /> <span data-ttu-id="78c4b-116">**Toujours** pour archiver automatiquement les devis lorsqu'ils sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="78c4b-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|  
    |<span data-ttu-id="78c4b-117">**Archivage des commandes vente ouvertes**</span><span class="sxs-lookup"><span data-stu-id="78c4b-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="78c4b-118">Permet d'archiver automatiquement les commandes ouvertes vente lorsqu'elles sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="78c4b-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|  
    |<span data-ttu-id="78c4b-119">**Arch. commandes et retours**</span><span class="sxs-lookup"><span data-stu-id="78c4b-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="78c4b-120">Permet d'archiver automatiquement les commandes vente lorsqu'elles sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="78c4b-120">Select to automatically archive sales orders each time they are deleted.</span></span>|  
    |<span data-ttu-id="78c4b-121">**Journal interaction automatique**</span><span class="sxs-lookup"><span data-stu-id="78c4b-121">**Automatic Interaction Log**</span></span>|<span data-ttu-id="78c4b-122">Sélectionnez cette option pour créer automatiquement une écriture pour le contact dans le journal interaction lorsqu'une commande vente ou une livraison partielle est enregistrée ou lorsqu'un devis est converti en commande vente.</span><span class="sxs-lookup"><span data-stu-id="78c4b-122">Select to automatically create an entry for the contact in the interaction log when a sales order or partial shipment is posted, or when a sales quote is converted into a sales order.</span></span> <span data-ttu-id="78c4b-123">**Remarque :** Ce champ n'est pas disponible sur la page **Paramètres achats**.</span><span class="sxs-lookup"><span data-stu-id="78c4b-123">**Note:**  This field is not available on the **Purchases & Payables Setup** page.</span></span>|  

3.  <span data-ttu-id="78c4b-124">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="78c4b-124">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="78c4b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78c4b-125">See Also</span></span>  
 <span data-ttu-id="78c4b-126">[Documents vente et Documents achat, Suisse](swiss-purchase-documents-and-sales-documents.md) </span><span class="sxs-lookup"><span data-stu-id="78c4b-126">[Swiss Purchase Documents and Sales Documents](swiss-purchase-documents-and-sales-documents.md) </span></span>  
 <span data-ttu-id="78c4b-127">[Importer les codes postaux suisses](how-to-import-swiss-post-codes.md) </span><span class="sxs-lookup"><span data-stu-id="78c4b-127">[Import Swiss Post Codes](how-to-import-swiss-post-codes.md) </span></span>  
 <span data-ttu-id="78c4b-128">[Imprimer la liste des prélèvements de stock d'une commande vente](how-to-print-an-inventory-picking-list-from-a-sales-order.md) </span><span class="sxs-lookup"><span data-stu-id="78c4b-128">[Print an Inventory Picking List from a Sales Order](how-to-print-an-inventory-picking-list-from-a-sales-order.md) </span></span>  
 [<span data-ttu-id="78c4b-129">Imprimer les commandes achat et vente lors d'une validation par lots</span><span class="sxs-lookup"><span data-stu-id="78c4b-129">Print Sales and Purchase Orders During Batch Posting</span></span>](how-to-print-sales-and-purchase-orders-during-batch-posting.md)

