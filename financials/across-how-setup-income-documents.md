---
title: Configurer les documents entrants| Microsoft Docs
description: "Utilisez la fonctionnalité Documents entrants pour créer des documents électroniques, gérer des tâches OCR, importer des factures, et convertir des fichiers images."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ad534c9d60bbf3805f701eec6295084f6121a6d0
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="dab04-103">Configurer des documents entrants</span><span class="sxs-lookup"><span data-stu-id="dab04-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="dab04-104">Si vous créez des lignes feuille comptabilité à partir des enregistrements de documents entrants, vous devez spécifier dans la fenêtre **Paramètres des documents entrants** quels modèle et nom de feuille utiliser.</span><span class="sxs-lookup"><span data-stu-id="dab04-104">If you create general journal lines from incoming document records, you must specify in the **Incoming Documents Setup** window which journal template and batch to use.</span></span>

<span data-ttu-id="dab04-105">Si vous ne souhaitez pas que les utilisateurs créent des factures ou des lignes feuille comptabilité à partir d'enregistrements de documents entrants, sauf si les documents ont été préalablement approuvés, vous devez paramétrer des approbateurs dans la fenêtre **Approbateurs de document entrant**.</span><span class="sxs-lookup"><span data-stu-id="dab04-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers in the **Incoming Document Approvers** window.</span></span>

<span data-ttu-id="dab04-106">Pour convertir les fichiers PDF et image en documents électroniques que vous pouvez convertir, par exemple, en factures achat dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez d'abord configurer la fonctionnalité OCR et activer le service.</span><span class="sxs-lookup"><span data-stu-id="dab04-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="dab04-107">Une fois que la fonctionnalité Documents entrants est configurée, vous pouvez utiliser différentes fonctions pour examiner les reçus de dépenses, gérer les tâches ROC et convertir les fichiers document entrants, manuellement ou automatiquement, en documents ou lignes feuille appropriés.</span><span class="sxs-lookup"><span data-stu-id="dab04-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="dab04-108">Les fichiers externes peuvent être joints à n'importe quelle étape du processus, notamment en ce qui concerne les documents validés et au fournisseur, au client qui en résulte, et dans les écritures comptables.</span><span class="sxs-lookup"><span data-stu-id="dab04-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="dab04-109">Pour plus d'informations, voir la section [Traitement des documents entrants](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="dab04-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="dab04-110">Configurer la fonctionnalité Documents entrants</span><span class="sxs-lookup"><span data-stu-id="dab04-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="dab04-111">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres des documents entrants**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="dab04-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="dab04-112">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="dab04-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="dab04-113">Configurer des approbateurs d'enregistrements document entrant</span><span class="sxs-lookup"><span data-stu-id="dab04-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="dab04-114">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres des documents entrants**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="dab04-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dab04-115">Dans la fenêtre **Paramètres des documents entrants**, sélectionnez l'action **Approbateurs**.</span><span class="sxs-lookup"><span data-stu-id="dab04-115">In the **Incoming Documents Setup** window, choose the **Approvers** action.</span></span>

    <span data-ttu-id="dab04-116">La fenêtre **Approbateurs de document entrant** affiche tous les utilisateurs configurés dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="dab04-116">The **Incoming Document Approvers** window shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="dab04-117">Sélectionnez un ou plusieurs utilisateurs pouvant approuver un document entrant pour qu'un document ou une ligne feuille connexe puisse être créée.</span><span class="sxs-lookup"><span data-stu-id="dab04-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="dab04-118">Lorsque des approbateurs ont été configurés dans la fenêtre **Approbateurs de document entrant**, seuls ces utilisateurs peuvent approuver un document entrant si la case **Exiger une approbation pour créer** est cochée dans la fenêtre **Paramètres des documents entrants**.</span><span class="sxs-lookup"><span data-stu-id="dab04-118">When approvers have been set up in the **Incoming Document Approvers** window, only those users can approve an incoming document if the **Require Approval To Create** check box in the **Incoming Documents Setup** window is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="dab04-119">Ce paramétrage d'approbation n'est pas lié aux flux d'approbation.</span><span class="sxs-lookup"><span data-stu-id="dab04-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="dab04-120">Pour plus d'informations, reportez-vous à [Utilisation des flux d'approbation](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="dab04-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="dab04-121">Configurer un service ROC</span><span class="sxs-lookup"><span data-stu-id="dab04-121">To set up an OCR service</span></span>
1. <span data-ttu-id="dab04-122">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres service OCR**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="dab04-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="dab04-123">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="dab04-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a><span data-ttu-id="dab04-124">Chiffrer les informations de connexion</span><span class="sxs-lookup"><span data-stu-id="dab04-124">To encrypt your login information</span></span>
<span data-ttu-id="dab04-125">Il est recommandé de protéger les informations de connexion que vous saisissez dans la fenêtre **Paramètres service OCR**.</span><span class="sxs-lookup"><span data-stu-id="dab04-125">It is recommended that you protect the logon information that you enter in the **OCR Service Setup** window.</span></span> <span data-ttu-id="dab04-126">Vous pouvez chiffrer des données sur le serveur en générant de nouvelles clés de chiffrement ou en important des clés existantes que vous activez sur l'instance de serveur qui est connectée à la base de données.</span><span class="sxs-lookup"><span data-stu-id="dab04-126">You can encrypt data on the server by generating new or importing existing encryption keys that you enable on the server instance that connects to the database.</span></span>

1. <span data-ttu-id="dab04-127">Dans la fenêtre **Paramètres service OCR**, sélectionnez l'action **Gestion du chiffrement**.</span><span class="sxs-lookup"><span data-stu-id="dab04-127">In the **OCR Service Setup** window, choose the **Encryption Management** action.</span></span>
2. <span data-ttu-id="dab04-128">Dans la fenêtre **Gestion du chiffrement des données**, activez le chiffrement de vos données.</span><span class="sxs-lookup"><span data-stu-id="dab04-128">In the **Data Encryption Management** window, enable encryption of your data.</span></span>

## <a name="see-also"></a><span data-ttu-id="dab04-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dab04-129">See Also</span></span>
[<span data-ttu-id="dab04-130">Traiter les documents entrants</span><span class="sxs-lookup"><span data-stu-id="dab04-130">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="dab04-131">Documents entrants</span><span class="sxs-lookup"><span data-stu-id="dab04-131">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="dab04-132">Achats</span><span class="sxs-lookup"><span data-stu-id="dab04-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="dab04-133">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dab04-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

