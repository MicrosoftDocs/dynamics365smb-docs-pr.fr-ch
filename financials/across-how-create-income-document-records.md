---
title: "Créer des enregistrements de documents entrants| Microsoft Docs"
description: "Vous pouvez créer des enregistrements de documents entrants, tels que des factures électroniques, et gérer des tâches OCR, du commerce électronique, et de l'échange de documents."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 8642f4d904c9a1e7c46846d790fcb2d0837c4cc2
ms.contentlocale: fr-ch
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-incoming-document-records"></a><span data-ttu-id="5c084-103">Procédure : créer des enregistrements document entrant</span><span class="sxs-lookup"><span data-stu-id="5c084-103">How to: Create Incoming Document Records</span></span>
<span data-ttu-id="5c084-104">Dans la fenêtre **Documents entrants**, vous pouvez utiliser différentes fonctions pour examiner les reçus de dépenses, gérer les tâches ROC et convertir les fichiers document entrants, manuellement ou automatiquement, en documents ou lignes feuille appropriés.</span><span class="sxs-lookup"><span data-stu-id="5c084-104">In the **Incoming Documents** window, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="5c084-105">Les fichiers externes peuvent être joints à n'importe quelle étape du processus, notamment en ce qui concerne les documents validés et au fournisseur, au client qui en résulte, et dans les écritures comptables.</span><span class="sxs-lookup"><span data-stu-id="5c084-105">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span>

<span data-ttu-id="5c084-106">Pour enregistrer un document externe dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez d'abord créer ou terminer un enregistrement de document externe.</span><span class="sxs-lookup"><span data-stu-id="5c084-106">To record an external document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first create or complete an incoming document record.</span></span> <span data-ttu-id="5c084-107">Vous pouvez effectuer cette opération manuellement ou prendre une photo du document externe puis créer l'enregistrement document entrant avec le fichier image joint.</span><span class="sxs-lookup"><span data-stu-id="5c084-107">You can do this manually, or you can take a photo of the external document and then create the incoming document record with the image file attached.</span></span>

<span data-ttu-id="5c084-108">Avant d'utiliser la fonctionnalité Documents entrants, vous devez exécuter la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="5c084-108">Before you can use the Incoming Documents feature, you must perform the required setup.</span></span> <span data-ttu-id="5c084-109">Pour plus d'informations, reportez vous à [Procédure : configurer des documents entrants](across-how-setup-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="5c084-109">For more information, see [How to: Set Up Incoming Documents](across-how-setup-income-documents.md).</span></span>

## <a name="to-approve-or-reject-an-incoming-document"></a><span data-ttu-id="5c084-110">Approbation ou rejet d'un document entrant</span><span class="sxs-lookup"><span data-stu-id="5c084-110">To approve or reject an incoming document</span></span>
<span data-ttu-id="5c084-111">Si vous souhaitez autoriser des utilisateurs à créer des factures ou des lignes feuille comptabilité à partir d'enregistrements document entrant, sauf s'ils sont approbateurs, vous pouvez configurer des approbateurs qui doivent approuver les enregistrements avant de pouvoir être traités.</span><span class="sxs-lookup"><span data-stu-id="5c084-111">If you do want to allow users to create invoices or general journal lines from incoming document records unless they are approved, you can set up approvers who must approve the records before they can be processed.</span></span>

1. <span data-ttu-id="5c084-112">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Documents entrants**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="5c084-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="5c084-113">Sélectionnez la ligne contenant le document à approuver ou rejeter, puis sélectionnez l'action **Approuver** or **Rejeter**.</span><span class="sxs-lookup"><span data-stu-id="5c084-113">Select the line with the document that you want to approve or reject, and then choose the **Approve** or **Reject** actions.</span></span>

<span data-ttu-id="5c084-114">Si vous approuvez l'enregistrement document entrant, la case à cocher **Lancé** de la ligne document entrant est activée.</span><span class="sxs-lookup"><span data-stu-id="5c084-114">If you approve the incoming document record, the **Released** check box on the incoming document line is selected.</span></span> <span data-ttu-id="5c084-115">L'utilisateur chargé de créer, par exemple, des factures achat peut continuer à traiter l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="5c084-115">The user in charge of creating, for example, purchase invoices can proceed to process the record.</span></span>

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="5c084-116">Pour créer un enregistrement de document entrant en prenant une photo</span><span class="sxs-lookup"><span data-stu-id="5c084-116">To create an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="5c084-117">La procédure suivante s'applique uniquement aux clients disposant de tablettes et de téléphones équipés de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5c084-117">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="5c084-118">Dans la barre d'application, sélectionnez la mosaïque **Créer le document entrant à partir de l'appareil photo**, puis passez à l'étape 4.</span><span class="sxs-lookup"><span data-stu-id="5c084-118">On the app bar, choose the **Create Incoming Document from Camera** tile, and then go to step 4.</span></span>
2. <span data-ttu-id="5c084-119">Sinon, dans la barre d'application, cliquez sur le bouton Options, choisissez **Documents entrants**, puis **Tous**.</span><span class="sxs-lookup"><span data-stu-id="5c084-119">Alternatively, on the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
3. <span data-ttu-id="5c084-120">Dans la fenêtre **Documents entrants**, sélectionnez le bouton de sélection, puis **Créer à partir de l'appareil photo**.</span><span class="sxs-lookup"><span data-stu-id="5c084-120">In the **Incoming Documents** window, choose the ellipsis button, and then choose **Create from Camera**.</span></span> <span data-ttu-id="5c084-121">L'appareil photo de la tablette ou du téléphone est activé.</span><span class="sxs-lookup"><span data-stu-id="5c084-121">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="5c084-122">Prenez une photo d'un document, tel qu'un reçu d'achat, que vous souhaitez traiter en tant que document entrant, puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c084-122">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="5c084-123">Un enregistrement de document entrant est créé, avec l'image jointe.</span><span class="sxs-lookup"><span data-stu-id="5c084-123">A new incoming document record is created, with the image attached.</span></span>

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="5c084-124">Pour joindre une image à un enregistrement de document entrant en prenant une photo</span><span class="sxs-lookup"><span data-stu-id="5c084-124">To attach an image to an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="5c084-125">La procédure suivante s'applique uniquement aux clients disposant de tablettes et de téléphones équipés de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5c084-125">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="5c084-126">Dans la barre d'application, cliquez sur le bouton Options, choisissez **Documents entrants**, puis **Tous**.</span><span class="sxs-lookup"><span data-stu-id="5c084-126">On the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
2. <span data-ttu-id="5c084-127">Ouvrez la fiche de l'enregistrement de document entrant existant.</span><span class="sxs-lookup"><span data-stu-id="5c084-127">Open the card for an existing incoming document record.</span></span>
3. <span data-ttu-id="5c084-128">Dans la fenêtre **Document entrant**, sélectionnez le bouton de sélection, puis **Joindre l'image de l'appareil photo**.</span><span class="sxs-lookup"><span data-stu-id="5c084-128">In the **Incoming Document** window, choose the ellipsis button, and then choose **Attach Image from Camera**.</span></span> <span data-ttu-id="5c084-129">L'appareil photo de la tablette ou du téléphone est activé.</span><span class="sxs-lookup"><span data-stu-id="5c084-129">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="5c084-130">Prenez une photo d'un document, tel qu'un reçu d'achat, que vous souhaitez traiter en tant que document entrant, puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c084-130">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="5c084-131">L'image est jointe à l'enregistrement de document entrant.</span><span class="sxs-lookup"><span data-stu-id="5c084-131">The image is attached to the incoming document record.</span></span>

## <a name="to-create-an-incoming-document-record-manually"></a><span data-ttu-id="5c084-132">Pour créer un enregistrement document entrant manuellement</span><span class="sxs-lookup"><span data-stu-id="5c084-132">To create an incoming document record manually</span></span>
1. <span data-ttu-id="5c084-133">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Documents entrants**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="5c084-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="5c084-134">Choisissez l'action **Créer à partir d'un fichier**.</span><span class="sxs-lookup"><span data-stu-id="5c084-134">Choose the **Create from File** action.</span></span>  
3. <span data-ttu-id="5c084-135">Dans la fenêtre **Insérer un fichier**, sélectionnez un fichier, puis choisissez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="5c084-135">In the **Insert File** window, select a file, and then choose **Open**.</span></span> <span data-ttu-id="5c084-136">Le fichier est automatiquement joint.</span><span class="sxs-lookup"><span data-stu-id="5c084-136">The file is automatically attached.</span></span>
4. <span data-ttu-id="5c084-137">Sinon, choisissez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="5c084-137">Alternatively, choose the **New** action.</span></span>
5. <span data-ttu-id="5c084-138">Pour joindre un fichier, choisissez l'action **Joindre fichier**.</span><span class="sxs-lookup"><span data-stu-id="5c084-138">To attach a file, choose the **Attach File** action.</span></span>
6. <span data-ttu-id="5c084-139">Dans la fenêtre **Insérer un fichier**, sélectionnez le fichier qui représente le document entrant concerné, puis choisissez le bouton **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="5c084-139">In the **Insert File** window, select the file that represents the incoming document in question, and then choose the **Open** button.</span></span>
7. <span data-ttu-id="5c084-140">Dans la fenêtre **Document entrant**, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="5c084-140">In the **Incoming Document** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="5c084-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c084-141">See Also</span></span>
[<span data-ttu-id="5c084-142">Traiter les documents entrants</span><span class="sxs-lookup"><span data-stu-id="5c084-142">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="5c084-143">Documents entrants</span><span class="sxs-lookup"><span data-stu-id="5c084-143">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="5c084-144">Achats</span><span class="sxs-lookup"><span data-stu-id="5c084-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="5c084-145">[Utilisation de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5c084-145">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>

