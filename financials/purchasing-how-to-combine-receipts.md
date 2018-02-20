---
title: "Procédure de regroupement des réceptions | Microsoft Docs"
description: "Si vous voulez facturer plusieurs réceptions achat en une fois, vous pouvez utiliser la fonction Regroupement des réceptions."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2176baf2947a08785fdf6327b2ebebf35686d04a
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="eaeaf-103">Regroupement de bons de réception sur une seule facture</span><span class="sxs-lookup"><span data-stu-id="eaeaf-103">Combine Receipts on a Single Invoice</span></span>
<span data-ttu-id="eaeaf-104">Si vous voulez facturer plusieurs réceptions achat en une fois, vous pouvez utiliser la fonction **Regroupement des réceptions**.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="eaeaf-105">Avant de pouvoir regrouper des réceptions achat, plusieurs réceptions achat du même fournisseur doivent être validées dans la même devise.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="eaeaf-106">En d'autres termes, vous devez avoir renseigné au moins deux commandes achat et les avoir validées comme reçues, mais non facturées.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="eaeaf-107">Lorsque des réceptions achat sont regroupées sur une facture et validées, une facture achat enregistrée est créée pour les lignes facturées.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="eaeaf-108">Le champ **Quantité facturée** de la commande achat d'origine, ou de la commande ouverte achat, est mis à jour en fonction de la quantité facturée.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="eaeaf-109">Comme ce document d'achat d'origine n'est toutefois pas supprimé, même s'il a été entièrement reçu et facturé, vous devez supprimer le document d'achat.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

## <a name="to-combine-receipts"></a><span data-ttu-id="eaeaf-110">Pour regrouper des réceptions</span><span class="sxs-lookup"><span data-stu-id="eaeaf-110">To combine receipts</span></span>  
1. <span data-ttu-id="eaeaf-111">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Factures achat**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="eaeaf-112">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-112">Choose the **New** action.</span></span> <span data-ttu-id="eaeaf-113">Pour plus d'informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="eaeaf-113">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="eaeaf-114">Dans le raccourci **Lignes**, sélectionnez l'action **Extraire lignes réception**.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-114">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="eaeaf-115">Sélectionnez plusieurs lignes réception à inclure dans la facture.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-115">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="eaeaf-116">Si une ligne réception incorrecte a été sélectionnée ou que vous souhaitez recommencer, il vous suffit de supprimer les lignes de la facture achat et d'utiliser à nouveau la fonction **Extraire lignes réception**.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-116">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="eaeaf-117">Pour valider la facture, sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-117">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="eaeaf-118">Pour supprimer des commandes achat ouvertes après la validation de reçus regroupés</span><span class="sxs-lookup"><span data-stu-id="eaeaf-118">To remove open purchase orders after combined receipt posting</span></span>  
1. <span data-ttu-id="eaeaf-119">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Supprimer les commandes achat facturées**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="eaeaf-120">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="eaeaf-121">.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-121">.</span></span>
3. <span data-ttu-id="eaeaf-122">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="eaeaf-123">Vous pouvez également supprimer chacune des commandes manuellement.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-123">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="eaeaf-124">Répétez les étapes 1 à 3 pour tous les autres documents affectés, comme des commandes ouvertes achat.</span><span class="sxs-lookup"><span data-stu-id="eaeaf-124">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="eaeaf-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaeaf-125">See Also</span></span>  
[<span data-ttu-id="eaeaf-126">Achats</span><span class="sxs-lookup"><span data-stu-id="eaeaf-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="eaeaf-127">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eaeaf-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

