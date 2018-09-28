---
title: "Procédure : créer manuellement des relances livraison"
description: "Dans Business Central, vous pouvez créer des relances livraison lorsqu'un achat n'a pas été envoyé comme prévu. Vous pouvez créer une relance livraison unique manuellement, ou vous pouvez générer des relances livraison pour toutes les livraisons échues."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c986e502e646b0f8f3f1d5bea5d40745ae706341
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="create-delivery-reminders-manually"></a><span data-ttu-id="322ec-104">Créer manuellement des relances livraison</span><span class="sxs-lookup"><span data-stu-id="322ec-104">Create Delivery Reminders Manually</span></span>
<span data-ttu-id="322ec-105">Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], vous pouvez créer des relances livraison lorsqu'un achat n'a pas été envoyé comme prévu.</span><span class="sxs-lookup"><span data-stu-id="322ec-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can create delivery reminders when a purchase has not been delivered as expected.</span></span> <span data-ttu-id="322ec-106">Vous pouvez créer une relance livraison unique manuellement, ou vous pouvez générer des relances livraison pour toutes les livraisons échues.</span><span class="sxs-lookup"><span data-stu-id="322ec-106">You can create a single delivery reminder manually, or you can generate delivery reminders for all overdue deliveries.</span></span> <span data-ttu-id="322ec-107">Pour plus d'informations, voir [Générer des relances livraison](how-to-generate-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="322ec-107">For more information, see [Generate Delivery Reminders](how-to-generate-delivery-reminders.md).</span></span>

> [!NOTE]
> <span data-ttu-id="322ec-108">Pour créer des relances livraison, vous devez configurer les propriétés de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="322ec-108">To create delivery reminders, you must set up the delivery reminder properties.</span></span> <span data-ttu-id="322ec-109">Pour plus d'informations, voir [Configurer des relances livraison](how-to-set-up-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="322ec-109">For more information, see [Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md).</span></span>

## <a name="to-create-a-delivery-reminder-manually"></a><span data-ttu-id="322ec-110">Pour créer une relance livraison manuellement</span><span class="sxs-lookup"><span data-stu-id="322ec-110">To create a delivery reminder manually</span></span>  

1.  <span data-ttu-id="322ec-111">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Relance livraison**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="322ec-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delivery Reminder**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="322ec-112">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="322ec-112">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="322ec-113">Dans la fenêtre **Relance livraison**, sur le raccourci **Général**, renseignez les champs comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="322ec-113">In the **Delivery Reminder** window, on the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="322ec-114">Champ</span><span class="sxs-lookup"><span data-stu-id="322ec-114">Field</span></span>|<span data-ttu-id="322ec-115">Désignation</span><span class="sxs-lookup"><span data-stu-id="322ec-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="322ec-116">**N°**</span><span class="sxs-lookup"><span data-stu-id="322ec-116">**No.**</span></span>|<span data-ttu-id="322ec-117">Numéro d'identification unique de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="322ec-117">The unique identification number for the delivery reminder.</span></span>|  
    |<span data-ttu-id="322ec-118">**N° fournisseur**</span><span class="sxs-lookup"><span data-stu-id="322ec-118">**Vendor No.**</span></span>|<span data-ttu-id="322ec-119">Numéro du fournisseur pour lequel vous souhaitez publier la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="322ec-119">The number of the vendor for whom you want to post the delivery reminder.</span></span><br /><br /> <span data-ttu-id="322ec-120">Lorsque vous sélectionnez le numéro de fournisseur, les champs **Nom**, **Adresse**, **CP/Ville** et **Contact** sont renseignés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="322ec-120">When you select the vendor number, the **Name**, **Address**, **Post Code/City**, and **Contact** fields are filled in automatically.</span></span>|  
    |<span data-ttu-id="322ec-121">**Date de validation**</span><span class="sxs-lookup"><span data-stu-id="322ec-121">**Posting Date**</span></span>|<span data-ttu-id="322ec-122">Date de validation de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="322ec-122">The posting date for the delivery reminder.</span></span> <span data-ttu-id="322ec-123">Cette date est copiée dans toutes les écritures comptables de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="322ec-123">This date is copied to all of the delivery reminder ledger entries.</span></span>|  
    |<span data-ttu-id="322ec-124">**Date document**</span><span class="sxs-lookup"><span data-stu-id="322ec-124">**Document Date**</span></span>|<span data-ttu-id="322ec-125">Date du document de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="322ec-125">The document date for the delivery reminder.</span></span> <span data-ttu-id="322ec-126">Cette date est également utilisée pour calculer la date d'échéance pour la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="322ec-126">This date is also used to calculate the due date for the delivery reminder.</span></span> <span data-ttu-id="322ec-127">Vous pouvez modifier la date de validation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="322ec-127">You can modify the posting date if required.</span></span>|  
    |<span data-ttu-id="322ec-128">**Niveau relance**</span><span class="sxs-lookup"><span data-stu-id="322ec-128">**Reminder Level**</span></span>|<span data-ttu-id="322ec-129">Niveau de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="322ec-129">The delivery reminder level.</span></span> <span data-ttu-id="322ec-130">Cette valeur est basée sur le nombre de relances livraison déjà envoyées.</span><span class="sxs-lookup"><span data-stu-id="322ec-130">This value is based on the number of delivery reminders that have already been sent.</span></span> <span data-ttu-id="322ec-131">Pour plus d'informations, voir [Configurer les conditions, niveaux et textes de relance livraison](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="322ec-131">For more information, see [Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span></span>|  
    |<span data-ttu-id="322ec-132">**Code condition relance**</span><span class="sxs-lookup"><span data-stu-id="322ec-132">**Reminder Terms Code**</span></span>|<span data-ttu-id="322ec-133">Spécifiez le code condition relance livraison qui est paramétré pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="322ec-133">Specify the delivery reminder terms code that is set up for the vendor.</span></span>|  
    |<span data-ttu-id="322ec-134">**Date d'échéance**</span><span class="sxs-lookup"><span data-stu-id="322ec-134">**Due Date**</span></span>|<span data-ttu-id="322ec-135">Date d'échéance de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="322ec-135">The due date for the delivery reminder.</span></span>|  

4.  <span data-ttu-id="322ec-136">Choisissez l'action **Proposer lignes relance**</span><span class="sxs-lookup"><span data-stu-id="322ec-136">Choose the **Suggest Reminder Lines** action</span></span>  

    <span data-ttu-id="322ec-137">S'il existe des livraisons échues du fournisseur spécifié, ces dernières sont ajoutées à la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="322ec-137">If there are overdue deliveries from the specified vendor, these are added to the deliver reminder.</span></span>  

5.  <span data-ttu-id="322ec-138">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="322ec-138">Choose the **OK** button.</span></span>  

    <span data-ttu-id="322ec-139">La relance livraison est créée.</span><span class="sxs-lookup"><span data-stu-id="322ec-139">The delivery reminder is created.</span></span> <span data-ttu-id="322ec-140">Vous pouvez alors émettre et imprimer la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="322ec-140">You can now issue and print the delivery reminder.</span></span>  

## <a name="see-also"></a><span data-ttu-id="322ec-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="322ec-141">See Also</span></span>  
 <span data-ttu-id="322ec-142">[relances livraison](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="322ec-142">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="322ec-143">[Générer des relances livraison](how-to-generate-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="322ec-143">[Generate Delivery Reminders](how-to-generate-delivery-reminders.md) </span></span>  
 <span data-ttu-id="322ec-144">[Configurer des relances livraison](how-to-set-up-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="322ec-144">[Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md) </span></span>  
 <span data-ttu-id="322ec-145">[Configurer les conditions, niveaux et textes de relance livraison.](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span><span class="sxs-lookup"><span data-stu-id="322ec-145">[Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span></span>  
 <span data-ttu-id="322ec-146">[Affecter des codes de relance livraison à des fournisseurs](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="322ec-146">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 <span data-ttu-id="322ec-147">[Émettre des relances livraison](how-to-issue-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="322ec-147">[Issue Delivery Reminders](how-to-issue-delivery-reminders.md) </span></span>  
 [<span data-ttu-id="322ec-148">Imprimer des rapports de test pour les relances livraison</span><span class="sxs-lookup"><span data-stu-id="322ec-148">Print Test Reports for Delivery Reminders</span></span>](how-to-print-test-reports-for-delivery-reminders.md)

