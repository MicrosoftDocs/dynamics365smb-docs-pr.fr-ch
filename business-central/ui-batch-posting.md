---
title: Comment valider plusieurs documents en même temps | Microsoft Docs
description: Au lieu de valider des documents individuels un par un, vous pouvez sélectionner plusieurs documents non validés dans une liste afin de les valider par lots, soit pour une validation immédiate, soit pour qu’elle soit planifiée, par exemple, à la fin de la journée.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1fd25f8b07a359414f62ef4757162f8a73889c27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912736"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="eafcc-103">Valider plusieurs documents en même temps</span><span class="sxs-lookup"><span data-stu-id="eafcc-103">Post Multiple Documents at the Same Time</span></span>

<span data-ttu-id="eafcc-104">Au lieu de valider des documents individuels un par un, vous pouvez sélectionner plusieurs documents non validés dans une liste pour une validation immédiate ou une validation par lot, conformément à une planification, à la fin de la journée, par exemple.</span><span class="sxs-lookup"><span data-stu-id="eafcc-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="eafcc-105">Cela peut être utile si seul un superviseur peut valider des documents créés par d’autres utilisateurs ou pour éviter des problèmes de performance du système liés à la validation pendant les heures de travail.</span><span class="sxs-lookup"><span data-stu-id="eafcc-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="eafcc-106">Pour valider plusieurs commandes achat immédiatement</span><span class="sxs-lookup"><span data-stu-id="eafcc-106">To post multiple purchase orders immediately</span></span>

<span data-ttu-id="eafcc-107">La procédure suivante explique comment valider immédiatement plusieurs commandes achat.</span><span class="sxs-lookup"><span data-stu-id="eafcc-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="eafcc-108">Les étapes sont similaires pour tous les documents achat et vente.</span><span class="sxs-lookup"><span data-stu-id="eafcc-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="eafcc-109">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes achat** , puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="eafcc-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders** , and then choose the related link.</span></span>
2. <span data-ttu-id="eafcc-110">Sur la page **Commandes achat** , sélectionnez toutes les commandes à valider :</span><span class="sxs-lookup"><span data-stu-id="eafcc-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="eafcc-111">Dans le champ **N°** ,</span><span class="sxs-lookup"><span data-stu-id="eafcc-111">In the **No.**</span></span> <span data-ttu-id="eafcc-112">choisissez les trois points verticaux pour ouvrir le menu contextuel, puis choisissez l’action **Sélectionner davantage** .</span><span class="sxs-lookup"><span data-stu-id="eafcc-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="eafcc-113">Cochez la case pour toutes les lignes représentant les commandes que vous souhaitez valider en même temps.</span><span class="sxs-lookup"><span data-stu-id="eafcc-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="eafcc-114">Choisissez l’action **Validation** , puis sélectionnez l’action **Valider** .</span><span class="sxs-lookup"><span data-stu-id="eafcc-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="eafcc-115">Cliquez sur le bouton **Oui** dans le message de confirmation.</span><span class="sxs-lookup"><span data-stu-id="eafcc-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="eafcc-116">Pour valider plusieurs commandes achat par lots</span><span class="sxs-lookup"><span data-stu-id="eafcc-116">To batch post multiple purchase orders</span></span>

<span data-ttu-id="eafcc-117">La procédure suivante explique comment valider plusieurs commandes achat par lots.</span><span class="sxs-lookup"><span data-stu-id="eafcc-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="eafcc-118">Les étapes sont similaires pour tous les documents d’achat et de vente où l’action **Valider par lots** est disponible.</span><span class="sxs-lookup"><span data-stu-id="eafcc-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="eafcc-119">La validation par lots de documents se produit en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="eafcc-119">Batch posting of documents happens in the background.</span></span> <span data-ttu-id="eafcc-120">[!INCLUDE [prodshort](includes/prodshort.md)] en ligne inclut les travaux par défaut pour la publication en arrière-plan et la validation par lots.</span><span class="sxs-lookup"><span data-stu-id="eafcc-120">[!INCLUDE [prodshort](includes/prodshort.md)] online includes default jobs for background posting and batch posting.</span></span> <span data-ttu-id="eafcc-121">Pour en savoir plus, consultez [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="eafcc-121">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="eafcc-122">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes achat** , puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="eafcc-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders** , and then choose the related link.</span></span>  
2. <span data-ttu-id="eafcc-123">Sur la page **Commandes achat** , sélectionnez toutes les commandes à valider :</span><span class="sxs-lookup"><span data-stu-id="eafcc-123">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="eafcc-124">Dans le champ **N°** ,</span><span class="sxs-lookup"><span data-stu-id="eafcc-124">In the **No.**</span></span> <span data-ttu-id="eafcc-125">choisissez les trois points verticaux pour ouvrir le menu contextuel, puis choisissez l’action **Sélectionner davantage** .</span><span class="sxs-lookup"><span data-stu-id="eafcc-125">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="eafcc-126">Cochez la case pour toutes les lignes représentant les commandes que vous souhaitez valider en même temps.</span><span class="sxs-lookup"><span data-stu-id="eafcc-126">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="eafcc-127">Choisissez l’action **Validation** , puis sélectionnez l’action **Valider par lot** .</span><span class="sxs-lookup"><span data-stu-id="eafcc-127">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="eafcc-128">Sur la page **TPL validation commandes achat** , renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="eafcc-128">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="eafcc-129">Cliquez sur le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="eafcc-129">Choose the **OK** button.</span></span>
8. <span data-ttu-id="eafcc-130">Pour afficher les problèmes potentiels survenus lors de l’enregistrement par lots de documents, ouvrez la page **Registre des messages d’erreur** .</span><span class="sxs-lookup"><span data-stu-id="eafcc-130">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="eafcc-131">Les commandes achat seront désormais ajoutées à une entrée de file d’attente de travaux dédiée, qui définit le moment où les documents sont validés.</span><span class="sxs-lookup"><span data-stu-id="eafcc-131">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="eafcc-132">Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="eafcc-132">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="eafcc-133">Si vous sélectionnez **PDF** dans le champ **Type sortie état** , les bons de commande validés avec succès seront disponibles dans la partie **boîte de réception état** de votre tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="eafcc-133">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="eafcc-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eafcc-134">See Also</span></span>

[<span data-ttu-id="eafcc-135">Validation des documents et des feuilles</span><span class="sxs-lookup"><span data-stu-id="eafcc-135">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="eafcc-136">Utiliser des files d’attente des travaux pour planifier des tâches</span><span class="sxs-lookup"><span data-stu-id="eafcc-136">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="eafcc-137">Valider les documents validés</span><span class="sxs-lookup"><span data-stu-id="eafcc-137">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="eafcc-138">Corriger ou annuler des factures achat impayées</span><span class="sxs-lookup"><span data-stu-id="eafcc-138">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="eafcc-139">Recherche de pages et d’informations avec la fonction Tell Me</span><span class="sxs-lookup"><span data-stu-id="eafcc-139">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="eafcc-140">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eafcc-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
