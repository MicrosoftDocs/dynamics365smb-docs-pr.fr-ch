---
title: Définir les documents originaux à afficher | Microsoft Docs
description: Ajustez la vue par défaut des documents entrants, tels que des factures électroniques, afin d'améliorer votre vue d'ensemble des enregistrements traités et non-traités.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 97ca5aab24b04f6c2d0677c6fd9626b93fcd8ca8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821298"
---
# <a name="manage-many-incoming-document-records"></a><span data-ttu-id="d6505-103">Gérer de nombreux enregistrements document entrant</span><span class="sxs-lookup"><span data-stu-id="d6505-103">Manage Many Incoming Document Records</span></span>
<span data-ttu-id="d6505-104">Lors de la création ou du traitement des enregistrements document, le nombre de lignes sur la page **Documents entrants** peut croître de telle façon que vous perdez la vue d'ensemble.</span><span class="sxs-lookup"><span data-stu-id="d6505-104">As you create or process incoming document records, the number of lines on the **Incoming Documents** page may grow to an extent where you lose overview.</span></span> <span data-ttu-id="d6505-105">Par conséquent, vous pouvez définir les enregistrements de documents entrants sur Traité afin de les supprimer de la vue par défaut.</span><span class="sxs-lookup"><span data-stu-id="d6505-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="d6505-106">Lorsque vous choisissez l'action **Afficher tout**, vous pouvez afficher les enregistrements traités et non traités.</span><span class="sxs-lookup"><span data-stu-id="d6505-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d6505-107">Vous ne pouvez pas modifier les informations, joindre des fichiers, ni exécuter d'autres processus sur des enregistrements de documents entrants définis à Traité.</span><span class="sxs-lookup"><span data-stu-id="d6505-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="d6505-108">Vous devez d'abord définir le paramètre à Non traité.</span><span class="sxs-lookup"><span data-stu-id="d6505-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="d6505-109">La case **Traité** est automatiquement cochée sur les champ est sélectionné sur les enregistrements de documents entrants qui ont été traités, mais vous pouvez également cocher ou décocher cette case manuellement.</span><span class="sxs-lookup"><span data-stu-id="d6505-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="d6505-110">En fonction de votre processus entreprise, un enregistrement de document entrant peut être traité si un document connexe a été créé pour celui-ci ou qu'un fichier a été joint.</span><span class="sxs-lookup"><span data-stu-id="d6505-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d6505-111">Lorsque vous ouvrez la page **Documents entrants** avec l'action **Mes documents entrants** sur le Tableau de bord, seuls les enregistrements de documents entrants non traités sont affichés par défaut.</span><span class="sxs-lookup"><span data-stu-id="d6505-111">When you open the **Incoming Documents** page with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="d6505-112">Dans cette rubrique, il s'agit de « la vue par défaut ».</span><span class="sxs-lookup"><span data-stu-id="d6505-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="d6505-113">Pour supprimer les enregistrements de documents entrants de la vue par défaut</span><span class="sxs-lookup"><span data-stu-id="d6505-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="d6505-114">Sur la page **Documents entrants**, sélectionnez une ou plusieurs lignes pour les enregistrements de documents entrants que vous souhaitez supprimer de la vue par défaut.</span><span class="sxs-lookup"><span data-stu-id="d6505-114">On the **Incoming Documents** page, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="d6505-115">Sélectionnez l'action **Défini sur Traité**.</span><span class="sxs-lookup"><span data-stu-id="d6505-115">Choose the **Set to Processed** action.</span></span>

    <span data-ttu-id="d6505-116">Les enregistrements de documents entrants sont supprimés de la vue par défaut, et la case **Traité** est sélectionnée sur les lignes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="d6505-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d6505-117">Vous pouvez également effectuer cette action pour un enregistrement spécifique sur la page **Fiche document entrant**.</span><span class="sxs-lookup"><span data-stu-id="d6505-117">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="d6505-118">Pour afficher tous les enregistrements de documents entrants</span><span class="sxs-lookup"><span data-stu-id="d6505-118">To view all incoming document records</span></span>
1. <span data-ttu-id="d6505-119">Sur la page **Documents entrants**, sélectionnez l'action **Afficher tout**.</span><span class="sxs-lookup"><span data-stu-id="d6505-119">On the **Incoming Documents** page, choose the **Show All** action.</span></span>

<span data-ttu-id="d6505-120">Tous les enregistrements de documents entrants sont affichés, y compris ceux pour lesquels la case **Traité** n'est pas cochée.</span><span class="sxs-lookup"><span data-stu-id="d6505-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="d6505-121">Pour ajouter des enregistrements de documents entrants à la vue par défaut</span><span class="sxs-lookup"><span data-stu-id="d6505-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="d6505-122">Sur la page **Documents entrants**, sélectionnez l'action **Afficher tout**.</span><span class="sxs-lookup"><span data-stu-id="d6505-122">On the **Incoming Documents** page, choose the **Show All** action.</span></span>
2. <span data-ttu-id="d6505-123">Sélectionnez un ou plusieurs lignes pour les enregistrements de documents entrants que vous souhaitez voir apparaître dans la vue par défaut.</span><span class="sxs-lookup"><span data-stu-id="d6505-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="d6505-124">Sélectionnez l'action **Défini sur Non traité**.</span><span class="sxs-lookup"><span data-stu-id="d6505-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="d6505-125">Vous pouvez également effectuer cette action pour un enregistrement spécifique sur la page **Fiche document entrant**.</span><span class="sxs-lookup"><span data-stu-id="d6505-125">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6505-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6505-126">See Also</span></span>
[<span data-ttu-id="d6505-127">Traiter les documents entrants</span><span class="sxs-lookup"><span data-stu-id="d6505-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="d6505-128">Documents entrants</span><span class="sxs-lookup"><span data-stu-id="d6505-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="d6505-129">Achats</span><span class="sxs-lookup"><span data-stu-id="d6505-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="d6505-130">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d6505-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
