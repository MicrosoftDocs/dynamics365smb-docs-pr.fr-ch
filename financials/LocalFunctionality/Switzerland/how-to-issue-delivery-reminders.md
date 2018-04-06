---
title: "Procédure : Émettre des relances livraison"
description: "Après avoir créé des relances livraison, vous devez les émettre et les imprimer afin de pouvoir envoyer des relances aux fournisseurs. Avant d'émettre les relances livraison, vous pouvez imprimer un rapport de test."
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
ms.openlocfilehash: 6abf8039442d60bcf379db823907ff24296b05cb
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="issue-delivery-reminders"></a><span data-ttu-id="615d7-104">Émettre des relances livraison</span><span class="sxs-lookup"><span data-stu-id="615d7-104">Issue Delivery Reminders</span></span>
<span data-ttu-id="615d7-105">Après avoir créé des relances livraison, vous devez les émettre et les imprimer afin de pouvoir envoyer des relances aux fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="615d7-105">After you have created delivery reminders, you must issue and print them so that you can send reminders to vendors.</span></span> <span data-ttu-id="615d7-106">Avant d'émettre les relances livraison, vous pouvez imprimer un rapport de test.</span><span class="sxs-lookup"><span data-stu-id="615d7-106">Before you issue the delivery reminders, you can print a test report.</span></span> <span data-ttu-id="615d7-107">Pour plus d'informations, voir [Imprimer des rapports de test pour les relances livraison](how-to-print-test-reports-for-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="615d7-107">For more information, see [Print Test Reports for Delivery Reminders](how-to-print-test-reports-for-delivery-reminders.md).</span></span>  

<span data-ttu-id="615d7-108">Lorsque vous émettez les relances livraison, des écritures comptables de relance livraison sont créées.</span><span class="sxs-lookup"><span data-stu-id="615d7-108">When you issue the delivery reminders, delivery reminder ledger entries are created.</span></span> <span data-ttu-id="615d7-109">Vous pouvez afficher les écritures comptables créées dans la fenêtre **Écritures comptables relance livraison**.</span><span class="sxs-lookup"><span data-stu-id="615d7-109">You can view the created ledger entries in the **Deliv. Reminder Ledger Entries** window.</span></span>  

## <a name="to-issue-delivery-reminders"></a><span data-ttu-id="615d7-110">Pour émettre des relances livraison</span><span class="sxs-lookup"><span data-stu-id="615d7-110">To issue delivery reminders</span></span>  

1.  <span data-ttu-id="615d7-111">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Relance livraison**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="615d7-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delivery Reminder**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="615d7-112">Dans la fenêtre **Relance livraison**, sélectionnez la relance livraison que vous souhaitez émettre, puis choisissez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="615d7-112">In the **Delivery Reminder** window, select the delivery reminder that you want to issue, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="615d7-113">Sélectionnez l'action **Émettre**.</span><span class="sxs-lookup"><span data-stu-id="615d7-113">Choose the **Issue** action.</span></span>  
4.  <span data-ttu-id="615d7-114">Dans la fenêtre **Émettre relance livraison**, sur le raccourci **Options**, renseignez les champs comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="615d7-114">In the **Issue Delivery Reminder** window, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="615d7-115">Champ</span><span class="sxs-lookup"><span data-stu-id="615d7-115">Field</span></span>|<span data-ttu-id="615d7-116">Désignation</span><span class="sxs-lookup"><span data-stu-id="615d7-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="615d7-117">**Imprimer**</span><span class="sxs-lookup"><span data-stu-id="615d7-117">**Print**</span></span>|<span data-ttu-id="615d7-118">Sélectionnez cette option pour imprimer les relances livraison lorsqu'elles sont émises.</span><span class="sxs-lookup"><span data-stu-id="615d7-118">Select to print the delivery reminders when they are issued.</span></span>|  
    |<span data-ttu-id="615d7-119">**Remplacer date comptabilisation**</span><span class="sxs-lookup"><span data-stu-id="615d7-119">**Replace Posting Date**</span></span>|<span data-ttu-id="615d7-120">Sélectionnez cette option pour remplacer la date de comptabilisation existante pour la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="615d7-120">Select to replace the existing posting date for the delivery reminder.</span></span>|  
    |<span data-ttu-id="615d7-121">**Date de validation**</span><span class="sxs-lookup"><span data-stu-id="615d7-121">**Posting Date**</span></span>|<span data-ttu-id="615d7-122">Date de validation de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="615d7-122">The posting date for the delivery reminder.</span></span><br /><br /> <span data-ttu-id="615d7-123">Cette date de comptabilisation est utilisée pour toutes les relances livraison si vous avez sélectionné la case à cocher **Remplacer date comptabilisation**.</span><span class="sxs-lookup"><span data-stu-id="615d7-123">This posting date is used for all delivery reminders if you have selected the **Replace Posting Date** check box.</span></span> <span data-ttu-id="615d7-124">Si la case à cocher **Remplacer date comptabilisation** est effacée, cette date ne sera utilisée que pour les relances livraison pour lesquelles une date de comptabilisation n'est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="615d7-124">If the **Replace Posting Date** check box is cleared, this date will be used for only those delivery reminders for which a posting date is not available.</span></span>|  

5.  <span data-ttu-id="615d7-125">Éventuellement, dans le raccourci **En-tête de relance livraison**, sélectionnez les filtres appropriés.</span><span class="sxs-lookup"><span data-stu-id="615d7-125">Optionally, on the **Delivery Reminder Header** FastTab, select the appropriate filters.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="615d7-126">Vous pouvez supprimer les filtres et émettre à nouveau les relances livraison en même temps.</span><span class="sxs-lookup"><span data-stu-id="615d7-126">You can remove filters and issue all delivery reminders at the same time.</span></span>  

6.  <span data-ttu-id="615d7-127">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="615d7-127">Choose the **OK** button.</span></span>  

<span data-ttu-id="615d7-128">Vous pouvez afficher les relances émises dans la fenêtre **Relances livraison émises**.</span><span class="sxs-lookup"><span data-stu-id="615d7-128">You can view the issued reminders in the **Issued Delivery Reminder** window.</span></span> <span data-ttu-id="615d7-129">En option, vous pouvez maintenant imprimer une relance livraison.</span><span class="sxs-lookup"><span data-stu-id="615d7-129">Optionally, you can now print a delivery reminder.</span></span>  

## <a name="to-view-delivery-reminder-ledger-entries"></a><span data-ttu-id="615d7-130">Pour afficher des écritures comptables de relance livraison</span><span class="sxs-lookup"><span data-stu-id="615d7-130">To view delivery reminder ledger entries</span></span>  

1.  <span data-ttu-id="615d7-131">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes achat**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="615d7-131">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="615d7-132">Sélectionnez la commande achat pour laquelle vous souhaitez afficher le statut de relance, puis choisissez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="615d7-132">Select the purchase order for which you want to view the reminder status, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="615d7-133">Sélectionnez l'action **Écritures comptables de relance livraison**.</span><span class="sxs-lookup"><span data-stu-id="615d7-133">Choose the **Deliv. Reminder Ledger Entries** action.</span></span>  

<span data-ttu-id="615d7-134">Dans la fenêtre Écritures comptables de relance livraison, vous pouvez afficher les écritures comptables de relance livraison pour la commande achat sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="615d7-134">In the Deliv. Reminder Ledger Entries window, you can view the delivery reminder ledger entries for the selected purchase order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="615d7-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="615d7-135">See Also</span></span>  
 <span data-ttu-id="615d7-136">[relances livraison](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="615d7-136">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="615d7-137">[Générer des relances livraison](how-to-generate-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="615d7-137">[Generate Delivery Reminders](how-to-generate-delivery-reminders.md) </span></span>  
 [<span data-ttu-id="615d7-138">Créer manuellement des relances livraison</span><span class="sxs-lookup"><span data-stu-id="615d7-138">Create Delivery Reminders Manually</span></span>](how-to-create-delivery-reminders-manually.md)

