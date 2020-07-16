---
title: Procédure de regroupement des réceptions | Microsoft Docs
description: Si vous voulez facturer plusieurs réceptions achat en une fois, vous pouvez utiliser la fonction Regroupement des réceptions.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/02/2020
ms.author: sgroespe
ms.openlocfilehash: f5b3c47ab430b89c2f747f73bc427e045a902992
ms.sourcegitcommit: 506a433298fc3629231cfa98f64a2d1428094fde
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534686"
---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="0ee95-103">Regroupement de bons de réception sur une seule facture</span><span class="sxs-lookup"><span data-stu-id="0ee95-103">Combine Receipts on a Single Invoice</span></span>

<span data-ttu-id="0ee95-104">Si vous voulez facturer plusieurs réceptions achat en une fois, vous pouvez utiliser la fonction **Regroupement des réceptions**.</span><span class="sxs-lookup"><span data-stu-id="0ee95-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="0ee95-105">Avant de pouvoir regrouper des réceptions achat, plusieurs réceptions achat du même fournisseur doivent être validées dans la même devise.</span><span class="sxs-lookup"><span data-stu-id="0ee95-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="0ee95-106">En d'autres termes, vous devez avoir renseigné au moins deux commandes achat et les avoir validées comme reçues, mais non facturées.</span><span class="sxs-lookup"><span data-stu-id="0ee95-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="0ee95-107">Lorsque des réceptions achat sont regroupées sur une facture et validées, une facture achat enregistrée est créée pour les lignes facturées.</span><span class="sxs-lookup"><span data-stu-id="0ee95-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="0ee95-108">Le champ **Quantité facturée** de la commande achat d'origine, ou de la commande ouverte achat, est mis à jour en fonction de la quantité facturée.</span><span class="sxs-lookup"><span data-stu-id="0ee95-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="0ee95-109">Comme ce document d'achat d'origine n'est toutefois pas supprimé, même s'il a été entièrement reçu et facturé, vous devez supprimer le document d'achat.</span><span class="sxs-lookup"><span data-stu-id="0ee95-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

> [!NOTE]
> <span data-ttu-id="0ee95-110">La facture achat qui en résulte ne peut pas être corrigée ou annulée ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="0ee95-110">The resulting purchase invoice cannot later be corrected or canceled.</span></span> <span data-ttu-id="0ee95-111">Si vous souhaitez modifier une facture achat ainsi créée, vous devez utiliser des avoirs achat.</span><span class="sxs-lookup"><span data-stu-id="0ee95-111">If you want to modify a purchase invoice that is created in this way, you must use purchase credit memos.</span></span> <span data-ttu-id="0ee95-112">Pour plus d'informations, voir [Corriger ou annuler des factures achat impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="0ee95-112">For more information, see [Correct or Cancel Unpaid Purchase Invoices](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span></span>

## <a name="to-combine-receipts"></a><span data-ttu-id="0ee95-113">Pour regrouper des réceptions</span><span class="sxs-lookup"><span data-stu-id="0ee95-113">To combine receipts</span></span>

1. <span data-ttu-id="0ee95-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures achat**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="0ee95-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0ee95-115">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="0ee95-115">Choose the **New** action.</span></span> <span data-ttu-id="0ee95-116">Pour plus d'informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="0ee95-116">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="0ee95-117">Dans le raccourci **Lignes**, sélectionnez l'action **Extraire lignes réception**.</span><span class="sxs-lookup"><span data-stu-id="0ee95-117">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="0ee95-118">Sélectionnez plusieurs lignes réception à inclure dans la facture.</span><span class="sxs-lookup"><span data-stu-id="0ee95-118">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="0ee95-119">Si une ligne réception incorrecte a été sélectionnée ou que vous souhaitez recommencer, il vous suffit de supprimer les lignes de la facture achat et d'utiliser à nouveau la fonction **Extraire lignes réception**.</span><span class="sxs-lookup"><span data-stu-id="0ee95-119">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="0ee95-120">Pour valider la facture, sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="0ee95-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="0ee95-121">Pour supprimer des commandes achat ouvertes après la validation de reçus regroupés</span><span class="sxs-lookup"><span data-stu-id="0ee95-121">To remove open purchase orders after combined receipt posting</span></span>

1. <span data-ttu-id="0ee95-122">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer les commandes achat facturées**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="0ee95-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="0ee95-123">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="0ee95-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="0ee95-124">.</span><span class="sxs-lookup"><span data-stu-id="0ee95-124">.</span></span>
3. <span data-ttu-id="0ee95-125">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ee95-125">Choose the **OK** button.</span></span>  

<span data-ttu-id="0ee95-126">Vous pouvez également supprimer chacune des commandes manuellement.</span><span class="sxs-lookup"><span data-stu-id="0ee95-126">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="0ee95-127">Répétez les étapes 1 à 3 pour tous les autres documents affectés, comme des commandes ouvertes achat.</span><span class="sxs-lookup"><span data-stu-id="0ee95-127">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ee95-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ee95-128">See Also</span></span>

[<span data-ttu-id="0ee95-129">Achats</span><span class="sxs-lookup"><span data-stu-id="0ee95-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="0ee95-130">Corriger ou annuler des factures achat impayées</span><span class="sxs-lookup"><span data-stu-id="0ee95-130">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
<span data-ttu-id="0ee95-131">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0ee95-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
