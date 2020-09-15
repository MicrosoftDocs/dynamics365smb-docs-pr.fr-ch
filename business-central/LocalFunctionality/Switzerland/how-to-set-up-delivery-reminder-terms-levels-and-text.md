---
title: 'Procédure : Configurer les conditions, niveaux et textes de relance livraison.'
description: Pour créer des relances livraison, vous devez configurer des conditions de relance livraison, des niveaux de relance livraison et des textes de relance livraison. messages
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
ms.author: edupont
ms.openlocfilehash: 07997f58d13b21572545feb5f801b86ec8bd261c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778195"
---
# <a name="set-up-delivery-reminder-terms-levels-and-text"></a><span data-ttu-id="e0763-104">Configurer les conditions, niveaux et textes de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="e0763-104">Set Up Delivery Reminder Terms, Levels, and Text</span></span>
<span data-ttu-id="e0763-105">Pour créer des relances livraison, vous devez configurer ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="e0763-105">To create delivery reminders, you must set up the following:</span></span>  

- <span data-ttu-id="e0763-106">Conditions de relance livraison</span><span class="sxs-lookup"><span data-stu-id="e0763-106">Delivery reminder terms</span></span>  
- <span data-ttu-id="e0763-107">Niveaux de relance livraison</span><span class="sxs-lookup"><span data-stu-id="e0763-107">Delivery reminder levels</span></span>  
- <span data-ttu-id="e0763-108">Message textuels de relance livraison</span><span class="sxs-lookup"><span data-stu-id="e0763-108">Delivery reminder text messages</span></span>  

<span data-ttu-id="e0763-109">Chaque condition de relance livraison a deux niveaux ou plusieurs niveaux de relance livraison, et pour chaque niveau de relance livraison, vous pouvez spécifier le texte constituant la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="e0763-109">Each delivery reminder term has two or more delivery reminder levels, and for each delivery reminder level, you can specify text that will be part of the delivery reminder.</span></span>  

<span data-ttu-id="e0763-110">Pour plus d'informations, voir [Relances livraison](delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="e0763-110">For more information, see [Delivery Reminders](delivery-reminders.md).</span></span>  

## <a name="to-set-up-delivery-reminder-terms"></a><span data-ttu-id="e0763-111">Pour configurer des conditions de relance livraison</span><span class="sxs-lookup"><span data-stu-id="e0763-111">To set up delivery reminder terms</span></span>  

1.  <span data-ttu-id="e0763-112">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Conditions de relance livraison**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="e0763-112">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delivery Reminder Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e0763-113">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="e0763-113">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="e0763-114">Renseignez les champs comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e0763-114">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="e0763-115">Champ</span><span class="sxs-lookup"><span data-stu-id="e0763-115">Field</span></span>|<span data-ttu-id="e0763-116">Désignation</span><span class="sxs-lookup"><span data-stu-id="e0763-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="e0763-117">**Code**</span><span class="sxs-lookup"><span data-stu-id="e0763-117">**Code**</span></span>|<span data-ttu-id="e0763-118">Code de la condition de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="e0763-118">The code for the delivery reminder term.</span></span> <span data-ttu-id="e0763-119">Vous pouvez entrer 10 caractères alphanumériques maximum.</span><span class="sxs-lookup"><span data-stu-id="e0763-119">You can enter a maximum of 10 alphanumeric characters.</span></span>|  
    |<span data-ttu-id="e0763-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="e0763-120">**Description**</span></span>|<span data-ttu-id="e0763-121">Description de la condition de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="e0763-121">The description for the delivery reminder term.</span></span> <span data-ttu-id="e0763-122">Vous pouvez entrer 30 caractères alphanumériques maximum.</span><span class="sxs-lookup"><span data-stu-id="e0763-122">You can enter a maximum of 30 alphanumeric characters.</span></span>|  
    |<span data-ttu-id="e0763-123">**Nombre max. de relances livraison**</span><span class="sxs-lookup"><span data-stu-id="e0763-123">**Max. No. of Delivery Reminders**</span></span>|<span data-ttu-id="e0763-124">Nombre maximum de relances livraison qui peuvent être créées pour une commande.</span><span class="sxs-lookup"><span data-stu-id="e0763-124">The maximum number of delivery reminders that can be created for an order.</span></span><br /><br /> <span data-ttu-id="e0763-125">**REMARQUE :** C'est le nombre maximal pour tous les niveaux de relance applicable à cette condition de relance.</span><span class="sxs-lookup"><span data-stu-id="e0763-125">**NOTE:** This is the maximum number across all reminder levels for this reminder term.</span></span> <span data-ttu-id="e0763-126">Par exemple, si vous avez configuré trois niveaux, et que vous définissez le **Nombre max. de relances livraison** à 5, la première relance est créée au niveau 1, la seconde au niveau 2, et les trois dernières au niveau 3.</span><span class="sxs-lookup"><span data-stu-id="e0763-126">For example, if you have set up three levels, and you set **Max. No. of Delivery Reminders** to 5, the first reminder is created at level 1, the second at level 2, and the last three at level 3.</span></span>|  

4.  <span data-ttu-id="e0763-127">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0763-127">Choose the **OK** button.</span></span>  

## <a name="to-add-delivery-reminder-levels-to-a-delivery-reminder-term"></a><span data-ttu-id="e0763-128">Pour ajouter des niveaux de relance livraison à une seule condition de relance livraison</span><span class="sxs-lookup"><span data-stu-id="e0763-128">To add delivery reminder levels to a delivery reminder term</span></span>  

1.  <span data-ttu-id="e0763-129">Dans la page **Conditions de relance livraison**, sélectionnez la condition pour laquelle vous souhaitez configurer des niveaux, puis choisissez l'action **Niveaux**.</span><span class="sxs-lookup"><span data-stu-id="e0763-129">On the **Delivery Reminder Terms** page, select the delivery reminder term for which you want to set up levels, and then choose the **Levels** action.</span></span>  
2.  <span data-ttu-id="e0763-130">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="e0763-130">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="e0763-131">Renseignez les champs comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e0763-131">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="e0763-132">Champ</span><span class="sxs-lookup"><span data-stu-id="e0763-132">Field</span></span>|<span data-ttu-id="e0763-133">Désignation</span><span class="sxs-lookup"><span data-stu-id="e0763-133">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="e0763-134">**N°**</span><span class="sxs-lookup"><span data-stu-id="e0763-134">**No.**</span></span>|<span data-ttu-id="e0763-135">Numéro de niveau de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="e0763-135">The delivery reminder level number.</span></span> <span data-ttu-id="e0763-136">Ce champ est complété automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e0763-136">This field is filled in automatically.</span></span>|  
    |<span data-ttu-id="e0763-137">**Calcul de date d'échéance**</span><span class="sxs-lookup"><span data-stu-id="e0763-137">**Due Date Calculation**</span></span>|<span data-ttu-id="e0763-138">Formule permettant de calculer l'échéance de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="e0763-138">The formula for the due date calculation for the delivery reminder.</span></span> <span data-ttu-id="e0763-139">Vous pouvez saisir une combinaison de chiffres de 0 à 9999 et des codes de date (J pour le jour, JS pour un jour de la semaine, S pour la semaine, M pour le mois, T pour le trimestre ou A pour l'année).</span><span class="sxs-lookup"><span data-stu-id="e0763-139">You can enter a combination of numbers from 0 to 9999, and date codes (D for day, WD for weekday, W for week, M for month, Q for quarter, or Y for year).</span></span> <span data-ttu-id="e0763-140">Les codes de date indiquent le calcul de la date d'échéance de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="e0763-140">The date codes denote the calculation for the delivery reminder due date.</span></span> <span data-ttu-id="e0763-141">Vous pouvez saisi un maximum de 20 caractères pour la formule de calcul de la date d'échéance.</span><span class="sxs-lookup"><span data-stu-id="e0763-141">You can enter a maximum of 20 characters for the due date calculation formula.</span></span>|  

4.  <span data-ttu-id="e0763-142">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0763-142">Choose the **OK** button.</span></span>  

<span data-ttu-id="e0763-143">Pour chaque niveau de relance livraison, vous pouvez définir les messages texte qui sont ajoutés à la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="e0763-143">For each delivery reminder level, you can define text messages that are added to the delivery reminder.</span></span> <span data-ttu-id="e0763-144">Vous pouvez définir le texte de début ajouté avant la description de la commande achat en retard et le texte de fin ajouté après la description de la commande achat en retard.</span><span class="sxs-lookup"><span data-stu-id="e0763-144">You can define beginning text that is added before the description of the overdue purchase order, and ending text that is added after the description of the overdue purchase order.</span></span>  

<span data-ttu-id="e0763-145">La procédure suivante décrit comment configurer des messages texte de début, mais les mêmes étapes s'appliquent également pour configurer des messages texte de fin.</span><span class="sxs-lookup"><span data-stu-id="e0763-145">The following procedure describes how to set up beginning text messages, but the same steps apply for setting up ending text messages.</span></span>  

## <a name="to-set-up-delivery-reminder-text-messages"></a><span data-ttu-id="e0763-146">Pour configurer des messages textuels de relance livraison</span><span class="sxs-lookup"><span data-stu-id="e0763-146">To set up delivery reminder text messages</span></span>  

1.  <span data-ttu-id="e0763-147">Dans la page **Niveaux de relance livraison**, sélectionnez un niveau, puis sélectionnez l'action **Texte de début**.</span><span class="sxs-lookup"><span data-stu-id="e0763-147">On the **Delivery Reminder Levels** page, select a level, and then choose the **Beginning Text** action.</span></span>  
2.  <span data-ttu-id="e0763-148">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="e0763-148">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="e0763-149">Dans le champ **Description**, entrez le message texte de début de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="e0763-149">In the **Description** field, enter the beginning text message for the delivery reminder.</span></span>  
4.  <span data-ttu-id="e0763-150">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0763-150">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e0763-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0763-151">See Also</span></span>  
 <span data-ttu-id="e0763-152">[relances livraison](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="e0763-152">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="e0763-153">[Configurer des relances livraison](how-to-set-up-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="e0763-153">[Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md) </span></span>  
 <span data-ttu-id="e0763-154">[Affecter des codes de relance livraison à des fournisseurs](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="e0763-154">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 <span data-ttu-id="e0763-155">[Créer manuellement des relances livraison](how-to-create-delivery-reminders-manually.md) </span><span class="sxs-lookup"><span data-stu-id="e0763-155">[Create Delivery Reminders Manually](how-to-create-delivery-reminders-manually.md) </span></span>  
 [<span data-ttu-id="e0763-156">Émettre des relances livraison</span><span class="sxs-lookup"><span data-stu-id="e0763-156">Issue Delivery Reminders</span></span>](how-to-issue-delivery-reminders.md)
