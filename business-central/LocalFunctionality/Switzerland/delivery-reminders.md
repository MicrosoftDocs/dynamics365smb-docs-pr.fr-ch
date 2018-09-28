---
title: relances livraison
description: "Les relances livraison sont utilisées pour suivre les envois des fournisseurs en retard et pour rappeler aux fournisseurs les livraisons en retard."
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
ms.openlocfilehash: 7b2634ba14ec0429ebc24bcf59f6d9cedeba7754
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="delivery-reminders"></a><span data-ttu-id="f649f-103">relances livraison</span><span class="sxs-lookup"><span data-stu-id="f649f-103">Delivery Reminders</span></span>
<span data-ttu-id="f649f-104">Les relances livraison sont utilisées pour suivre les envois des fournisseurs en retard et pour rappeler aux fournisseurs les livraisons en retard.</span><span class="sxs-lookup"><span data-stu-id="f649f-104">Delivery reminders are used to track overdue vendor shipments, and to remind vendors about overdue deliveries.</span></span> <span data-ttu-id="f649f-105">Pour créer des relances livraison, vous devez configurer ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="f649f-105">To create delivery reminders, you must set up the following:</span></span>  

- <span data-ttu-id="f649f-106">Conditions de relance livraison</span><span class="sxs-lookup"><span data-stu-id="f649f-106">Delivery reminder terms</span></span>  

    <span data-ttu-id="f649f-107">Les conditions de relance livraison sont identifiées par un code qui doit être affecté aux fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="f649f-107">Delivery reminder terms are identified by a code that must be assigned to vendors.</span></span> <span data-ttu-id="f649f-108">Pour utiliser plusieurs combinaisons de paramètres, vous devez configurer un code pour chaque paramètre séparément.</span><span class="sxs-lookup"><span data-stu-id="f649f-108">To use more than one combination of settings, you must set up a code for each setting separately.</span></span> <span data-ttu-id="f649f-109">Vous pouvez configurer autant de conditions relance livraison que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="f649f-109">You can set up any number of delivery reminder terms.</span></span>  

- <span data-ttu-id="f649f-110">Niveaux de relance livraison</span><span class="sxs-lookup"><span data-stu-id="f649f-110">Delivery reminder levels</span></span>  

    <span data-ttu-id="f649f-111">Pour chaque condition de relance livraison, vous devez au préalable configurer des niveaux de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="f649f-111">For every delivery reminder term, you must set up delivery reminder levels.</span></span> <span data-ttu-id="f649f-112">Ces niveaux déterminent la fréquence à laquelle les relances livraison peuvent être créées pour une condition spécifique.</span><span class="sxs-lookup"><span data-stu-id="f649f-112">These levels determine how often delivery reminders can be created for a specific term.</span></span> <span data-ttu-id="f649f-113">Le niveau 1 correspond à la première relance créée pour une livraison échue.</span><span class="sxs-lookup"><span data-stu-id="f649f-113">Level 1 is the first delivery reminder that you create for an overdue delivery.</span></span> <span data-ttu-id="f649f-114">Le niveau 2 correspond à la deuxième relance livraison, etc.</span><span class="sxs-lookup"><span data-stu-id="f649f-114">Level 2 is the second delivery reminder, and so on.</span></span> <span data-ttu-id="f649f-115">Lorsque les relances livraison sont créées, le nombre de relances créées précédemment est pris en compte, et le nombre actuel est utilisé pour appliquer des conditions.</span><span class="sxs-lookup"><span data-stu-id="f649f-115">When delivery reminders are created, the number of reminders that were created previously is considered, and the current number is used to apply terms.</span></span>  

- <span data-ttu-id="f649f-116">Message textuels de relance livraison</span><span class="sxs-lookup"><span data-stu-id="f649f-116">Delivery reminder texts messages</span></span>  

    <span data-ttu-id="f649f-117">Vous devez configurer des messages texte de relance livraison pour chaque niveau de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="f649f-117">You must set up delivery reminder text messages for every delivery reminder level.</span></span> <span data-ttu-id="f649f-118">Il existe deux types de messages texte de relance livraison : début et fin.</span><span class="sxs-lookup"><span data-stu-id="f649f-118">There are two types of delivery reminder text messages: beginning and ending.</span></span> <span data-ttu-id="f649f-119">Le message texte de début est imprimé dans la section En-tête, avant la liste des écritures marquées pour la relance.</span><span class="sxs-lookup"><span data-stu-id="f649f-119">The beginning text message is printed under the header section, before the list of entries that are marked for reminder.</span></span> <span data-ttu-id="f649f-120">Le message texte fin est imprimé après cette liste.</span><span class="sxs-lookup"><span data-stu-id="f649f-120">The ending text message is printed after this list.</span></span>  

<span data-ttu-id="f649f-121">Pour plus d'informations, voir [Configurer les conditions, niveaux et textes de relance livraison](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="f649f-121">For more information, see [Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span></span>  

<span data-ttu-id="f649f-122">Après avoir configuré les conditions de livraison, vous devez affecter les codes condition de relance livraison aux fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="f649f-122">After you have set up the delivery terms, you must assign the delivery reminder term codes to vendors.</span></span> <span data-ttu-id="f649f-123">Pour plus d'informations, voir [Affecter les codes condition de relance livraison aux fournisseurs](how-to-assign-delivery-reminder-codes-to-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="f649f-123">For more information, see [Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md).</span></span>  

<span data-ttu-id="f649f-124">Vous pouvez créer les relances livraison manuellement ou automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f649f-124">You can create delivery reminders manually or automatically.</span></span> <span data-ttu-id="f649f-125">Vous pouvez utiliser le traitement par lots **Créer une relance livraison** pour créer des relances livraison automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f649f-125">You can use the **Create Delivery Reminder** batch job to create delivery reminders automatically.</span></span> <span data-ttu-id="f649f-126">Ce traitement par lots permet de sélectionner des commandes achat pour lesquelles des relances livraison doivent être créées.</span><span class="sxs-lookup"><span data-stu-id="f649f-126">This batch job allows you to select the purchase orders for which delivery reminders must be created.</span></span> <span data-ttu-id="f649f-127">Pour plus d'informations, voir [Générer des relances livraison](how-to-issue-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="f649f-127">For more information, see [Generate Delivery Reminders](how-to-issue-delivery-reminders.md).</span></span>  

<span data-ttu-id="f649f-128">Vous pouvez également suivre les documents en rapport avec les lignes commande achat et les lignes commande vente.</span><span class="sxs-lookup"><span data-stu-id="f649f-128">You can also track documents in relation to purchase order lines and sales order lines.</span></span>  

[!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="f649f-129">fournit les états suivants :</span><span class="sxs-lookup"><span data-stu-id="f649f-129"> provides the following reports:</span></span>  

- <span data-ttu-id="f649f-130">**Relance livraison publiée** - Pour afficher les relances livraison des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="f649f-130">**Issued Delivery Reminder** - To view the delivery reminders for vendors.</span></span>  
- <span data-ttu-id="f649f-131">**Relance livraison - Test** - Pour vérifier les relances livraison avant de les valider.</span><span class="sxs-lookup"><span data-stu-id="f649f-131">**Delivery Reminder - Test** - To verify the delivery reminders before you issue them.</span></span>  

<span data-ttu-id="f649f-132">Pour plus d'informations, voir [Imprimer des rapports de test pour les relances livraison](how-to-print-test-reports-for-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="f649f-132">For more information, see [Print Test Reports for Delivery Reminders](how-to-print-test-reports-for-delivery-reminders.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="f649f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f649f-133">See Also</span></span>  
 <span data-ttu-id="f649f-134">[Configurer des relances livraison](how-to-set-up-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="f649f-134">[Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md) </span></span>  
 <span data-ttu-id="f649f-135">[Configurer les conditions, niveaux et textes de relance livraison.](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span><span class="sxs-lookup"><span data-stu-id="f649f-135">[Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span></span>  
 <span data-ttu-id="f649f-136">[Affecter des codes de relance livraison à des fournisseurs](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="f649f-136">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 <span data-ttu-id="f649f-137">[Générer des relances livraison](how-to-generate-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="f649f-137">[Generate Delivery Reminders](how-to-generate-delivery-reminders.md) </span></span>  
 <span data-ttu-id="f649f-138">[Créer manuellement des relances livraison](how-to-create-delivery-reminders-manually.md) </span><span class="sxs-lookup"><span data-stu-id="f649f-138">[Create Delivery Reminders Manually](how-to-create-delivery-reminders-manually.md) </span></span>  
 <span data-ttu-id="f649f-139">[Émettre des relances livraison](how-to-issue-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="f649f-139">[Issue Delivery Reminders](how-to-issue-delivery-reminders.md) </span></span>  
 [<span data-ttu-id="f649f-140">Imprimer des rapports de test pour les relances livraison</span><span class="sxs-lookup"><span data-stu-id="f649f-140">Print Test Reports for Delivery Reminders</span></span>](how-to-print-test-reports-for-delivery-reminders.md)

