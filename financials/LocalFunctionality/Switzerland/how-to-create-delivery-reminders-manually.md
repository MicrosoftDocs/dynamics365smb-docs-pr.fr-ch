---
title: "Procédure : créer manuellement des relances livraison"
description: Dans ADD INCLUDE<!--[!INCLUDE[navnow](../../includes/how-to-generate-delivery-reminders.md).
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
ms.openlocfilehash: 7e82038dc676da036419b47f9685b3678ce8d06e
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-delivery-reminders-manually"></a><span data-ttu-id="eaf0d-103">Créer manuellement des relances livraison</span><span class="sxs-lookup"><span data-stu-id="eaf0d-103">Create Delivery Reminders Manually</span></span>
<span data-ttu-id="eaf0d-104">Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], vous pouvez créer des relances livraison lorsqu'un achat n'a pas été envoyé comme prévu.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can create delivery reminders when a purchase has not been delivered as expected.</span></span> <span data-ttu-id="eaf0d-105">Vous pouvez créer une relance livraison unique manuellement, ou vous pouvez générer des relances livraison pour toutes les livraisons échues.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-105">You can create a single delivery reminder manually, or you can generate delivery reminders for all overdue deliveries.</span></span> <span data-ttu-id="eaf0d-106">Pour plus d'informations, voir [Générer des relances livraison](how-to-generate-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="eaf0d-106">For more information, see [Generate Delivery Reminders](how-to-generate-delivery-reminders.md).</span></span>

> [!NOTE]
> <span data-ttu-id="eaf0d-107">Pour créer des relances livraison, vous devez configurer les propriétés de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-107">To create delivery reminders, you must set up the delivery reminder properties.</span></span> <span data-ttu-id="eaf0d-108">Pour plus d'informations, voir [Configurer des relances livraison](how-to-set-up-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="eaf0d-108">For more information, see [Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md).</span></span>

## <a name="to-create-a-delivery-reminder-manually"></a><span data-ttu-id="eaf0d-109">Pour créer une relance livraison manuellement</span><span class="sxs-lookup"><span data-stu-id="eaf0d-109">To create a delivery reminder manually</span></span>  

1.  <span data-ttu-id="eaf0d-110">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Relance livraison**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-110">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delivery Reminder**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="eaf0d-111">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="eaf0d-112">Dans la fenêtre **Relance livraison**, sur le raccourci **Général**, renseignez les champs comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-112">In the **Delivery Reminder** window, on the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="eaf0d-113">Champ</span><span class="sxs-lookup"><span data-stu-id="eaf0d-113">Field</span></span>|<span data-ttu-id="eaf0d-114">Désignation</span><span class="sxs-lookup"><span data-stu-id="eaf0d-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="eaf0d-115">**N°**</span><span class="sxs-lookup"><span data-stu-id="eaf0d-115">**No.**</span></span>|<span data-ttu-id="eaf0d-116">Numéro d'identification unique de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-116">The unique identification number for the delivery reminder.</span></span>|  
    |<span data-ttu-id="eaf0d-117">**N° fournisseur**</span><span class="sxs-lookup"><span data-stu-id="eaf0d-117">**Vendor No.**</span></span>|<span data-ttu-id="eaf0d-118">Numéro du fournisseur pour lequel vous souhaitez publier la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-118">The number of the vendor for whom you want to post the delivery reminder.</span></span><br /><br /> <span data-ttu-id="eaf0d-119">Lorsque vous sélectionnez le numéro de fournisseur, les champs **Nom**, **Adresse**, **CP/Ville** et **Contact** sont renseignés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-119">When you select the vendor number, the **Name**, **Address**, **Post Code/City**, and **Contact** fields are filled in automatically.</span></span>|  
    |<span data-ttu-id="eaf0d-120">**Date de validation**</span><span class="sxs-lookup"><span data-stu-id="eaf0d-120">**Posting Date**</span></span>|<span data-ttu-id="eaf0d-121">Date de validation de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-121">The posting date for the delivery reminder.</span></span> <span data-ttu-id="eaf0d-122">Cette date est copiée dans toutes les écritures comptables de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-122">This date is copied to all of the delivery reminder ledger entries.</span></span>|  
    |<span data-ttu-id="eaf0d-123">**Date document**</span><span class="sxs-lookup"><span data-stu-id="eaf0d-123">**Document Date**</span></span>|<span data-ttu-id="eaf0d-124">Date du document de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-124">The document date for the delivery reminder.</span></span> <span data-ttu-id="eaf0d-125">Cette date est également utilisée pour calculer la date d'échéance pour la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-125">This date is also used to calculate the due date for the delivery reminder.</span></span> <span data-ttu-id="eaf0d-126">Vous pouvez modifier la date de validation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-126">You can modify the posting date if required.</span></span>|  
    |<span data-ttu-id="eaf0d-127">**Niveau relance**</span><span class="sxs-lookup"><span data-stu-id="eaf0d-127">**Reminder Level**</span></span>|<span data-ttu-id="eaf0d-128">Niveau de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-128">The delivery reminder level.</span></span> <span data-ttu-id="eaf0d-129">Cette valeur est basée sur le nombre de relances livraison déjà envoyées.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-129">This value is based on the number of delivery reminders that have already been sent.</span></span> <span data-ttu-id="eaf0d-130">Pour plus d'informations, voir [Configurer les conditions, niveaux et textes de relance livraison](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="eaf0d-130">For more information, see [Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span></span>|  
    |<span data-ttu-id="eaf0d-131">**Code condition relance**</span><span class="sxs-lookup"><span data-stu-id="eaf0d-131">**Reminder Terms Code**</span></span>|<span data-ttu-id="eaf0d-132">Spécifiez le code condition relance livraison qui est paramétré pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-132">Specify the delivery reminder terms code that is set up for the vendor.</span></span>|  
    |<span data-ttu-id="eaf0d-133">**Date d'échéance**</span><span class="sxs-lookup"><span data-stu-id="eaf0d-133">**Due Date**</span></span>|<span data-ttu-id="eaf0d-134">Date d'échéance de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-134">The due date for the delivery reminder.</span></span>|  

4.  <span data-ttu-id="eaf0d-135">Choisissez l'action **Proposer lignes relance**</span><span class="sxs-lookup"><span data-stu-id="eaf0d-135">Choose the **Suggest Reminder Lines** action</span></span>  

    <span data-ttu-id="eaf0d-136">S'il existe des livraisons échues du fournisseur spécifié, ces dernières sont ajoutées à la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-136">If there are overdue deliveries from the specified vendor, these are added to the deliver reminder.</span></span>  

5.  <span data-ttu-id="eaf0d-137">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-137">Choose the **OK** button.</span></span>  

    <span data-ttu-id="eaf0d-138">La relance livraison est créée.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-138">The delivery reminder is created.</span></span> <span data-ttu-id="eaf0d-139">Vous pouvez alors émettre et imprimer la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-139">You can now issue and print the delivery reminder.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eaf0d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaf0d-140">See Also</span></span>  
 <span data-ttu-id="eaf0d-141">[relances livraison](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="eaf0d-141">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="eaf0d-142">[Générer des relances livraison](how-to-generate-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="eaf0d-142">[Generate Delivery Reminders](how-to-generate-delivery-reminders.md) </span></span>  
 <span data-ttu-id="eaf0d-143">[Configurer des relances livraison](how-to-set-up-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="eaf0d-143">[Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md) </span></span>  
 <span data-ttu-id="eaf0d-144">[Configurer les conditions, niveaux et textes de relance livraison.](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span><span class="sxs-lookup"><span data-stu-id="eaf0d-144">[Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span></span>  
 <span data-ttu-id="eaf0d-145">[Affecter des codes de relance livraison à des fournisseurs](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="eaf0d-145">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 <span data-ttu-id="eaf0d-146">[Émettre des relances livraison](how-to-issue-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="eaf0d-146">[Issue Delivery Reminders](how-to-issue-delivery-reminders.md) </span></span>  
 [<span data-ttu-id="eaf0d-147">Imprimer des rapports de test pour les relances livraison</span><span class="sxs-lookup"><span data-stu-id="eaf0d-147">Print Test Reports for Delivery Reminders</span></span>](how-to-print-test-reports-for-delivery-reminders.md)

