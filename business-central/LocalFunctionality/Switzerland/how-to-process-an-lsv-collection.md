---
title: "Procédure : Traiter un prélèvement LSV"
description: "Vous pouvez utiliser **Feuilles LSV** pour créer et traiter les paiements des clients Lastschrift Verfahren (LSV+). Vous pouvez enregistrer les paiements dans la feuille règlement, créer un fichier LSV, puis imprimer l'ordre de prélèvement."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f68c2c4b2b3747d341e7d99372b2e8f056a06bf1
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="process-an-lsv-collection"></a><span data-ttu-id="d9826-104">Traiter un prélèvement LSV</span><span class="sxs-lookup"><span data-stu-id="d9826-104">Process an LSV Collection</span></span>
<span data-ttu-id="d9826-105">Vous pouvez utiliser **Feuilles LSV** pour créer et traiter les paiements des clients Lastschrift Verfahren (LSV+).</span><span class="sxs-lookup"><span data-stu-id="d9826-105">You can use **LSV Journals** to create and process payments from Lastschrift Verfahren (LSV+) customers.</span></span> <span data-ttu-id="d9826-106">Vous pouvez enregistrer les paiements dans la feuille règlement, créer un fichier LSV, puis imprimer l'ordre de prélèvement.</span><span class="sxs-lookup"><span data-stu-id="d9826-106">You can register these payments in the cash receipt journal, create an LSV file, and then print the collection order.</span></span> <span data-ttu-id="d9826-107">Pour plus d'informations, voir la fenêtre Feuille règlement et [Exporter des paiements en mode LSV](how-to-export-payments-using-lsv.md).</span><span class="sxs-lookup"><span data-stu-id="d9826-107">For more information, see the Cash Receipt Journal window and [Export Payments Using LSV](how-to-export-payments-using-lsv.md).</span></span>  

<span data-ttu-id="d9826-108">Lorsque vous lancez le traitement par lots **Proposition de prélèvement LSV**, chaque prélèvement proposé est enregistrée sur une ligne feuille LSV, et les factures ouvertes sont transférées aux feuilles LSV.</span><span class="sxs-lookup"><span data-stu-id="d9826-108">When you run the **LSV Suggest Collection** batch job, each suggested collection is registered on an LSV journal line, and the open invoices are transferred to the LSV journals.</span></span> <span data-ttu-id="d9826-109">Pour plus d'informations, voir la table Feuille LSV.</span><span class="sxs-lookup"><span data-stu-id="d9826-109">For more information, see the LSV Journal table.</span></span>  

<span data-ttu-id="d9826-110">Vous pouvez afficher, modifier ou supprimer les lignes paiement proposées.</span><span class="sxs-lookup"><span data-stu-id="d9826-110">You can view, edit, or delete the suggested payment lines.</span></span> <span data-ttu-id="d9826-111">Si vous corrigez le montant proposé, la différence est marquée sous la forme d'une remise.</span><span class="sxs-lookup"><span data-stu-id="d9826-111">If you correct the suggested amount, then the difference is marked as a discount.</span></span> <span data-ttu-id="d9826-112">Vous pouvez exécuter le traitement par lots plusieurs fois pour différents groupes de clients.</span><span class="sxs-lookup"><span data-stu-id="d9826-112">You can run the batch job multiple times for different customer groups.</span></span> <span data-ttu-id="d9826-113">Les lignes de suggestion peuvent être placées sur la même feuille.</span><span class="sxs-lookup"><span data-stu-id="d9826-113">The suggestion lines can be placed in the same journal.</span></span>  

## <a name="to-create-an-lsv-collection"></a><span data-ttu-id="d9826-114">Pour créer un prélèvement LSV</span><span class="sxs-lookup"><span data-stu-id="d9826-114">To create an LSV collection</span></span>  

1.  <span data-ttu-id="d9826-115">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Liste feuilles LSV**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="d9826-115">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **LSV Journal List**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d9826-116">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="d9826-116">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="d9826-117">Dans la fenêtre **Liste feuilles LSV**, renseignez les champs requis comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d9826-117">In the **LSV Journal List** window, fill in the required fields as described in the following table.</span></span>  

    |<span data-ttu-id="d9826-118">Champ</span><span class="sxs-lookup"><span data-stu-id="d9826-118">Field</span></span>|<span data-ttu-id="d9826-119">Désignation</span><span class="sxs-lookup"><span data-stu-id="d9826-119">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="d9826-120">**Code banque LSV**</span><span class="sxs-lookup"><span data-stu-id="d9826-120">**LSV Bank Code**</span></span>|<span data-ttu-id="d9826-121">Sélectionnez le code banque LSV pour la banque qui procèdera au prélèvement.</span><span class="sxs-lookup"><span data-stu-id="d9826-121">Select the LSV bank code for the bank that will perform the collection.</span></span>|  
    |<span data-ttu-id="d9826-122">**Description de la feuille LSV**</span><span class="sxs-lookup"><span data-stu-id="d9826-122">**LSV Journal Description**</span></span>|<span data-ttu-id="d9826-123">Permet de saisir une description pour l'écriture.</span><span class="sxs-lookup"><span data-stu-id="d9826-123">Enter a description for the entry.</span></span>|

4.  <span data-ttu-id="d9826-124">Sélectionnez l'écriture feuille LSV requise, puis sélectionnez l'action **Proposition de prélèvement LSV** pour créer les paiements de prélèvement automatique par LSV+.</span><span class="sxs-lookup"><span data-stu-id="d9826-124">Select the required LSV journal entry, and then choose the **LSV Suggest Collection** action to create the payments to be collected automatically by LSV+.</span></span>  
5.  <span data-ttu-id="d9826-125">Dans la fenêtre **Proposition de prélèvement LSV**, sur le raccourci **Options**, renseignez les champs comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d9826-125">In the **LSV Suggest Collection** window, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="d9826-126">Champ</span><span class="sxs-lookup"><span data-stu-id="d9826-126">Field</span></span>|<span data-ttu-id="d9826-127">Désignation</span><span class="sxs-lookup"><span data-stu-id="d9826-127">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="d9826-128">**N°**</span><span class="sxs-lookup"><span data-stu-id="d9826-128">**No.**</span></span>|<span data-ttu-id="d9826-129">Entrez le numéro de feuille LSV.</span><span class="sxs-lookup"><span data-stu-id="d9826-129">Enter the LSV journal number.</span></span>|  
    |<span data-ttu-id="d9826-130">**Date d'échéance début**</span><span class="sxs-lookup"><span data-stu-id="d9826-130">**From due date**</span></span>|<span data-ttu-id="d9826-131">Spécifiez la date d'échéance début des écritures ouvertes à proposer pour le prélèvement.</span><span class="sxs-lookup"><span data-stu-id="d9826-131">Specify the starting due date of open entries to be suggested for collection.</span></span>|  
    |<span data-ttu-id="d9826-132">**Date d'échéance fin**</span><span class="sxs-lookup"><span data-stu-id="d9826-132">**To due date**</span></span>|<span data-ttu-id="d9826-133">Spécifiez la date d'échéance fin des écritures ouvertes à proposer pour le prélèvement.</span><span class="sxs-lookup"><span data-stu-id="d9826-133">Specify the ending due date of open entries to be suggested for collection.</span></span>|  
    |<span data-ttu-id="d9826-134">**Date de prélèvement**</span><span class="sxs-lookup"><span data-stu-id="d9826-134">**Collection date**</span></span>|<span data-ttu-id="d9826-135">Spécifiez la date à laquelle le prélèvement est clôturé.</span><span class="sxs-lookup"><span data-stu-id="d9826-135">Specify the date on which the collection closes.</span></span> <span data-ttu-id="d9826-136">L'ordre LSV+ doit être envoyé au moins trois jours bancaires avant la date de prélèvement.</span><span class="sxs-lookup"><span data-stu-id="d9826-136">The LSV+ order must be submitted at least three banking days before the collection date.</span></span>|  

6.  <span data-ttu-id="d9826-137">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9826-137">Choose the **OK** button.</span></span>  

<span data-ttu-id="d9826-138">Toutes les lignes sont été transférées à la feuille LSV.</span><span class="sxs-lookup"><span data-stu-id="d9826-138">All related lines are transferred to the LSV journal.</span></span> <span data-ttu-id="d9826-139">Après avoir effectué le prélèvement LSV, vous pouvez visualiser, vérifier ou modifier les paiements proposés dans la fenêtre **Feuille LSV**.</span><span class="sxs-lookup"><span data-stu-id="d9826-139">After processing the LSV collection, you can view, check, or edit the suggested payments in the **LSV Journal** window.</span></span> <span data-ttu-id="d9826-140">Pour plus d'informations, voir la table Ligne feuille LSV.</span><span class="sxs-lookup"><span data-stu-id="d9826-140">For more information, see the LSV Journal Line table.</span></span>  

## <a name="to-manage-suggested-payments"></a><span data-ttu-id="d9826-141">Pour gérer les paiements proposés</span><span class="sxs-lookup"><span data-stu-id="d9826-141">To manage suggested payments</span></span>  

1.  <span data-ttu-id="d9826-142">Dans la fenêtre **Liste feuilles LSV**, sélectionnez l'écriture feuille requise, puis sélectionnez l'action **Ligne feuille LSV**.</span><span class="sxs-lookup"><span data-stu-id="d9826-142">In the **LSV Journal List** window, select the required journal entry, and then choose the **LSV Journal Line** action.</span></span>  

    <span data-ttu-id="d9826-143">Vous pouvez visualiser et modifier les paiements proposés dans cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d9826-143">You can view and modify the suggested payments in this window.</span></span> <span data-ttu-id="d9826-144">Vous pouvez saisir les paiements requis manuellement.</span><span class="sxs-lookup"><span data-stu-id="d9826-144">You can enter the required payments manually.</span></span> <span data-ttu-id="d9826-145">Pour les nouvelles lignes feuille, le champ **Statut LSV** est défini sur **Ouvrir** pour indiquer que la facture est impayée.</span><span class="sxs-lookup"><span data-stu-id="d9826-145">For new journal lines, the **LSV Status** field is set to **Open** to indicate that the invoice is unpaid.</span></span>  

3.  <span data-ttu-id="d9826-146">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9826-146">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d9826-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9826-147">See Also</span></span>  
 <span data-ttu-id="d9826-148">[Paiements électroniques à l'aide de LSV+, Suisse](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="d9826-148">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 <span data-ttu-id="d9826-149">[Fermer prélèvement LSV](how-to-close-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="d9826-149">[Close an LSV Collection](how-to-close-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="d9826-150">[Valider des paiements LSV+](how-to-post-lsv-payments.md) </span><span class="sxs-lookup"><span data-stu-id="d9826-150">[Post LSV+ Payments](how-to-post-lsv-payments.md) </span></span>  
 [<span data-ttu-id="d9826-151">Exporter des paiements en mode LSV</span><span class="sxs-lookup"><span data-stu-id="d9826-151">Export Payments Using LSV</span></span>](how-to-export-payments-using-lsv.md)

