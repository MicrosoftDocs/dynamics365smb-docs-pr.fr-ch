---
title: Procédure de regroupement des réceptions | Microsoft Docs
description: Si vous voulez facturer plusieurs réceptions achat en une fois, vous pouvez utiliser la fonction Regroupement des réceptions.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0fd1ab354ef642bee9acf64f5f290ea5aad9283c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3190962"
---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="6bc5c-103">Regroupement de bons de réception sur une seule facture</span><span class="sxs-lookup"><span data-stu-id="6bc5c-103">Combine Receipts on a Single Invoice</span></span>
<span data-ttu-id="6bc5c-104">Si vous voulez facturer plusieurs réceptions achat en une fois, vous pouvez utiliser la fonction **Regroupement des réceptions**.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="6bc5c-105">Avant de pouvoir regrouper des réceptions achat, plusieurs réceptions achat du même fournisseur doivent être validées dans la même devise.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="6bc5c-106">En d'autres termes, vous devez avoir renseigné au moins deux commandes achat et les avoir validées comme reçues, mais non facturées.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="6bc5c-107">Lorsque des réceptions achat sont regroupées sur une facture et validées, une facture achat enregistrée est créée pour les lignes facturées.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="6bc5c-108">Le champ **Quantité facturée** de la commande achat d'origine, ou de la commande ouverte achat, est mis à jour en fonction de la quantité facturée.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="6bc5c-109">Comme ce document d'achat d'origine n'est toutefois pas supprimé, même s'il a été entièrement reçu et facturé, vous devez supprimer le document d'achat.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

## <a name="to-combine-receipts"></a><span data-ttu-id="6bc5c-110">Pour regrouper des réceptions</span><span class="sxs-lookup"><span data-stu-id="6bc5c-110">To combine receipts</span></span>  
1. <span data-ttu-id="6bc5c-111">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures achat**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6bc5c-112">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-112">Choose the **New** action.</span></span> <span data-ttu-id="6bc5c-113">Pour plus d'informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="6bc5c-113">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="6bc5c-114">Dans le raccourci **Lignes**, sélectionnez l'action **Extraire lignes réception**.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-114">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="6bc5c-115">Sélectionnez plusieurs lignes réception à inclure dans la facture.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-115">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="6bc5c-116">Si une ligne réception incorrecte a été sélectionnée ou que vous souhaitez recommencer, il vous suffit de supprimer les lignes de la facture achat et d'utiliser à nouveau la fonction **Extraire lignes réception**.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-116">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="6bc5c-117">Pour valider la facture, sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-117">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="6bc5c-118">Pour supprimer des commandes achat ouvertes après la validation de reçus regroupés</span><span class="sxs-lookup"><span data-stu-id="6bc5c-118">To remove open purchase orders after combined receipt posting</span></span>  
1. <span data-ttu-id="6bc5c-119">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer les commandes achat facturées**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="6bc5c-120">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="6bc5c-121">.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-121">.</span></span>
3. <span data-ttu-id="6bc5c-122">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="6bc5c-123">Vous pouvez également supprimer chacune des commandes manuellement.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-123">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="6bc5c-124">Répétez les étapes 1 à 3 pour tous les autres documents affectés, comme des commandes ouvertes achat.</span><span class="sxs-lookup"><span data-stu-id="6bc5c-124">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="6bc5c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bc5c-125">See Also</span></span>  
[<span data-ttu-id="6bc5c-126">Achats</span><span class="sxs-lookup"><span data-stu-id="6bc5c-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="6bc5c-127">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6bc5c-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
