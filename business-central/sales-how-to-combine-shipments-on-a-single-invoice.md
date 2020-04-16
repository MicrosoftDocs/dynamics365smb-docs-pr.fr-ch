---
title: 'Procédure : Regroupement de bons de livraison sur une seule facture | Microsoft Docs'
description: Si vous souhaitez facturer plusieurs bons de livraison à la fois, vous pouvez utiliser la fonction de regroupement des bons de livraison.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 52312113328aadb82a1149ecf03b3e870ae3c288
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194874"
---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="38e00-103">Regroupement de bons de livraison sur une seule facture</span><span class="sxs-lookup"><span data-stu-id="38e00-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="38e00-104">Si vous souhaitez facturer plusieurs bons de livraison à la fois, vous pouvez utiliser la fonction de regroupement des bons de livraison.</span><span class="sxs-lookup"><span data-stu-id="38e00-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

 <span data-ttu-id="38e00-105">Pour créer un regroupement de bons de livraison, plusieurs bons de livraison vente doivent avoir été validés pour le même client dans la même devise.</span><span class="sxs-lookup"><span data-stu-id="38e00-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="38e00-106">Autrement dit, vous devez avoir renseigné au moins deux commandes vente et les avoir validées comme étant expédiées, mais pas facturées.</span><span class="sxs-lookup"><span data-stu-id="38e00-106">In other words, you must have filled in two or more sales orders and posted them as shipped, but not invoiced.</span></span> <span data-ttu-id="38e00-107">Vous devez activer la case à cocher **Regrouper les B.L**. sur le raccourci **Expédition** de la fiche **client** pour utiliser la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="38e00-107">To combine shipments, the **Combine Shipments** check box must be selected on the **Shipping** FastTab of the **Customer** card.</span></span>  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="38e00-108">Regrouper manuellement les expéditions sur une seule facture</span><span class="sxs-lookup"><span data-stu-id="38e00-108">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="38e00-109">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="38e00-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="38e00-110">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="38e00-110">Choose the **New** action.</span></span> <span data-ttu-id="38e00-111">Pour plus d'informations, reportez-vous à [Facturer des ventes](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="38e00-111">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="38e00-112">Dans le champ **N° donneur d'ordre**</span><span class="sxs-lookup"><span data-stu-id="38e00-112">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="38e00-113">entrez le client facturé pour les articles expédiés.</span><span class="sxs-lookup"><span data-stu-id="38e00-113">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="38e00-114">Dans le raccourci **Lignes**, sélectionnez l'action **Extraire lignes expédition**.</span><span class="sxs-lookup"><span data-stu-id="38e00-114">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="38e00-115">Sélectionnez la ligne expédition que vous voulez inclure dans la facture :</span><span class="sxs-lookup"><span data-stu-id="38e00-115">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="38e00-116">Pour insérer toutes les lignes, sélectionnez-les toutes et sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="38e00-116">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="38e00-117">Pour insérer des lignes spécifiques, sélectionnez-les et sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="38e00-117">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="38e00-118">Vous pouvez utiliser la touche Ctrl pour sélectionner plusieurs lignes qui ne sont pas séquentielles.</span><span class="sxs-lookup"><span data-stu-id="38e00-118">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="38e00-119">Si une ligne expédition incorrecte a été sélectionnée ou si vous voulez recommencer, supprimez simplement les lignes de la facture, puis exécutez de nouveau la fonction **Extraire lignes expédition**.</span><span class="sxs-lookup"><span data-stu-id="38e00-119">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="38e00-120">Pour valider la facture, sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="38e00-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="38e00-121">Regrouper automatiquement les expéditions sur une seule facture</span><span class="sxs-lookup"><span data-stu-id="38e00-121">To automatically combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="38e00-122">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Regrouper les B.L.**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="38e00-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="38e00-123">La page de sélection du traitement par lots s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="38e00-123">The batch job request page opens.</span></span>  
2. <span data-ttu-id="38e00-124">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="38e00-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="38e00-125">Cochez la case **Validation des factures**.</span><span class="sxs-lookup"><span data-stu-id="38e00-125">Select the **Post Invoices** check box.</span></span>  
4.  <span data-ttu-id="38e00-126">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="38e00-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="38e00-127">Vous devez valider manuellement les avoirs si la case à cocher **Valider avoirs** n'a pas été activée pour le traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="38e00-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="38e00-128">Pour supprimer des commandes vente ouvertes après la validation des expéditions regroupées</span><span class="sxs-lookup"><span data-stu-id="38e00-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="38e00-129">Lorsque des bons de livraison sont regroupés sur une facture et validés, une Facture vente enregistrée est créée pour les lignes facturées.</span><span class="sxs-lookup"><span data-stu-id="38e00-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="38e00-130">Le champ **Quantité facturée** de la commande ouverte vente ou de la commande vente d'origine est mis à jour sur la base de la quantité facturée.</span><span class="sxs-lookup"><span data-stu-id="38e00-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="38e00-131">Lorsque vous facturez des livraisons de cette manière, les commandes à partir desquelles les livraisons ont été validées continuent à exister, même si elles ont été entièrement validées et facturées.</span><span class="sxs-lookup"><span data-stu-id="38e00-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="38e00-132">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Supprimer cdes vente facturées**, puis sélectionnez le lien.</span><span class="sxs-lookup"><span data-stu-id="38e00-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="38e00-133">Dans le champ de filtre **N°**,</span><span class="sxs-lookup"><span data-stu-id="38e00-133">Specify in the **No.**</span></span> <span data-ttu-id="38e00-134">les commandes vente à supprimer.</span><span class="sxs-lookup"><span data-stu-id="38e00-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="38e00-135">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="38e00-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="38e00-136">Il est également possible de supprimer chacune des commandes vente manuellement.</span><span class="sxs-lookup"><span data-stu-id="38e00-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="38e00-137">Répétez les étapes 1 à 3 pour tous les autres documents affectés, comme des commandes ouvertes vente.</span><span class="sxs-lookup"><span data-stu-id="38e00-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="38e00-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38e00-138">See Also</span></span>  
[<span data-ttu-id="38e00-139">Ventes</span><span class="sxs-lookup"><span data-stu-id="38e00-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="38e00-140">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="38e00-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
