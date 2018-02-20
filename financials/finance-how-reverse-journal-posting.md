---
title: "Annuler une validation en validant une écriture opposée| Microsoft Docs"
description: "Si vous avez effectué une validation erronée dans la feuille comptabilité, vous pouvez utiliser la fonction de contrepassation de transaction pour annuler la validation avec une piste d'audit correcte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 92c0bca970250b8f160ecfc15b086963c8693885
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="reverse-postings"></a><span data-ttu-id="1b8b0-103">Inversion d'une validation</span><span class="sxs-lookup"><span data-stu-id="1b8b0-103">Reverse Postings</span></span>
<span data-ttu-id="1b8b0-104">Pour annuler une validation feuille erronée, sélectionnez l'écriture et créez une écriture inverse (écritures identiques aux écritures originales mais avec le signe opposé) portant les mêmes numéro de document et date comptabilisation que l'écriture d'origine.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="1b8b0-105">Une fois l'écriture contrepassée, créez l'écriture correcte.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="1b8b0-106">Vous pouvez uniquement inverser les écritures validées à partir d'une ligne feuille comptabilité.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="1b8b0-107">Une écriture ne peut être contrepassée qu'une fois.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="1b8b0-108">Pour plus d'informations sur la validation d'une feuille comptabilité, voir [Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="1b8b0-108">For more information about posting from a general journal, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="1b8b0-109">Si vous avez effectué une validation de quantité négative incorrecte, comme une commande achat avec, par exemple, un nombre d'articles incorrect et que vous l'avez validée comme étant reçue (mais non facturée), vous pouvez annuler cette validation.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-109">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="1b8b0-110">Si vous avez effectué une validation de quantité positive incorrecte, comme une commande retour achat avec, par exemple, un nombre d'articles incorrect et que vous l'avez validée comme étant livrée (mais non facturée), vous pouvez annuler cette validation.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-110">If you have made an incorrect positive quantity posting, such as a purchase return order with the wrong number of items and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="1b8b0-111">Pour contrepasser la validation feuille d'une écriture comptable</span><span class="sxs-lookup"><span data-stu-id="1b8b0-111">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="1b8b0-112">Vous pouvez inverser des écritures dans toutes les fenêtres **Écritures comptables**.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-112">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="1b8b0-113">La procédure suivante se base sur la fenêtre **Écritures comptables**.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-113">The following procedure is based on the **General Ledger Entries** window.</span></span>
1. <span data-ttu-id="1b8b0-114">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Ecritures comptables**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="1b8b0-115">Sélectionnez l'écriture à contrepasser, puis cliquez sur l'action **Contrepasser la transaction**.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-115">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="1b8b0-116">Notez que cela doit être émis depuis une validation feuille.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-116">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="1b8b0-117">Dans la fenêtre **Contrepasser les écritures de transaction**, sélectionnez l'écriture voulue, puis sélectionnez l'action **Contrepasser**.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-117">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="1b8b0-118">Choisissez le bouton **Oui** dans le message de confirmation.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-118">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="1b8b0-119">Pour annuler une validation de quantité sur une réception d'achat enregistrée</span><span class="sxs-lookup"><span data-stu-id="1b8b0-119">To undo a quantity posting on a posted purchase receipt</span></span>  

1.  <span data-ttu-id="1b8b0-120">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Réceptions achat enregistrées**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1b8b0-121">Ouvrez la réception enregistrée à annuler.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-121">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="1b8b0-122">Sélectionnez la ligne ou les lignes à annuler.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-122">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="1b8b0-123">Choisissez l'action **Annuler réception**.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-123">Choose **Undo Receipt** action.</span></span>

    <span data-ttu-id="1b8b0-124">Une ligne de correction est insérée sous la ligne de la réception sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-124">A corrective line is inserted under the selected receipt line.</span></span>  

    <span data-ttu-id="1b8b0-125">Si la quantité a été reçue dans une réception entrepôt, une ligne de correction est insérée dans la réception entrepôt enregistrée.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-125">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

    <span data-ttu-id="1b8b0-126">Les champs **Quantité reçue** et **Qté reçue non facturée** de la commande achat associée sont remis à zéro.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-126">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="1b8b0-127">Pour annuler, puis effectuer à nouveau la validation de quantité sur les expéditions retour enregistrées</span><span class="sxs-lookup"><span data-stu-id="1b8b0-127">To undo and then redo a quantity posting on a posted return shipment</span></span>

1.  <span data-ttu-id="1b8b0-128">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Expéditions retour enreg.**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1b8b0-129">Ouvrez l'expédition retour validée à annuler.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-129">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="1b8b0-130">Sélectionnez la ligne ou les lignes à annuler.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-130">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="1b8b0-131">Choisissez l'action **Annuler expédition retour**.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-131">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="1b8b0-132">Une ligne de correction est insérée dans le document validé et les champs **Qté retour expédiée** et **Expédition retour non facturée** du retour sont remis à zéro.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-132">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="1b8b0-133">Retournez à présent au retour achat pour une nouvelle validation.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-133">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="1b8b0-134">Dans la fenêtre **Expédition retour enregistrée**, notez le numéro situé dans le champ **N° retour**</span><span class="sxs-lookup"><span data-stu-id="1b8b0-134">In the **Posted Return Shipment** window, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="1b8b0-135">.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-135">field.</span></span>  
6.  <span data-ttu-id="1b8b0-136">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Retours achat**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="1b8b0-137">Ouvrez la commande retour concernée, puis sélectionnez l'action **Rouvrir**.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-137">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="1b8b0-138">Corrigez l'écriture dans le champ **Quantité** et publiez à nouveau le retour achat.</span><span class="sxs-lookup"><span data-stu-id="1b8b0-138">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1b8b0-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b8b0-139">See Also</span></span>
[<span data-ttu-id="1b8b0-140">Valider les transactions directement vers la comptabilité</span><span class="sxs-lookup"><span data-stu-id="1b8b0-140">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="1b8b0-141">Utilisation de feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="1b8b0-141">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="1b8b0-142">Finances</span><span class="sxs-lookup"><span data-stu-id="1b8b0-142">Finance</span></span>](finance.md)  
<span data-ttu-id="1b8b0-143">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1b8b0-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

