---
title: Configurer les documents entrants| Microsoft Docs
description: Utilisez la fonctionnalité Documents entrants pour créer des documents électroniques, gérer des tâches OCR, importer des factures, et convertir des fichiers images.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0a33652ac230e63607957916308ee960d14a2b47
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188483"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="0da1a-103">Configurer des documents entrants</span><span class="sxs-lookup"><span data-stu-id="0da1a-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="0da1a-104">Si vous créez des lignes feuille comptabilité à partir des enregistrements de documents entrants, vous devez spécifier sur la page **Paramètres des documents entrants** quels modèle et nom de feuille utiliser.</span><span class="sxs-lookup"><span data-stu-id="0da1a-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="0da1a-105">Si vous ne souhaitez pas que les utilisateurs créent des factures ou des lignes feuille comptabilité à partir d'enregistrements document entrant, sauf si les documents ont été préalablement approuvés, vous devez paramétrer des approbateurs de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="0da1a-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="0da1a-106">Pour convertir les fichiers PDF et image en documents électroniques que vous pouvez convertir, par exemple, en factures achat dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez d'abord configurer la fonctionnalité OCR et activer le service.</span><span class="sxs-lookup"><span data-stu-id="0da1a-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="0da1a-107">Une fois que la fonctionnalité Documents entrants est configurée, vous pouvez utiliser différentes fonctions pour examiner les reçus de dépenses, gérer les tâches ROC et convertir les fichiers document entrants, manuellement ou automatiquement, en documents ou lignes feuille appropriés.</span><span class="sxs-lookup"><span data-stu-id="0da1a-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="0da1a-108">Les fichiers externes peuvent être joints à n'importe quelle étape du processus, notamment en ce qui concerne les documents validés et au fournisseur, au client qui en résulte, et dans les écritures comptables.</span><span class="sxs-lookup"><span data-stu-id="0da1a-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="0da1a-109">Pour plus d'informations, voir la section [Traitement des documents entrants](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="0da1a-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="0da1a-110">Configurer la fonctionnalité Documents entrants</span><span class="sxs-lookup"><span data-stu-id="0da1a-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="0da1a-111">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres des documents entrants**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="0da1a-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="0da1a-112">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="0da1a-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="0da1a-113">Configurer des approbateurs d'enregistrements document entrant</span><span class="sxs-lookup"><span data-stu-id="0da1a-113">To set up approvers of incoming document records</span></span>
<span data-ttu-id="0da1a-114">Les approbateurs de documents entrants doivent être paramétrés comme des utilisateurs de flux de travail approbation.</span><span class="sxs-lookup"><span data-stu-id="0da1a-114">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="0da1a-115">Avant de pouvoir créer des workflows qui impliquent des étapes d'approbation, vous devez configurer les utilisateurs du workflow qui sont impliqués dans les processus d'approbation.</span><span class="sxs-lookup"><span data-stu-id="0da1a-115">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="0da1a-116">Sur la page **Paramètres utilisateur d'approbation**, vous pouvez également définir les limites pour des types spécifiques de demandes et définir des approbateurs remplaçants à qui des demandes d'approbation sont déléguées lorsque l'approbateur initial est absent.</span><span class="sxs-lookup"><span data-stu-id="0da1a-116">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="0da1a-117">Pour plus d'informations, voir [Configurer des utilisateurs d'approbation](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="0da1a-117">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="0da1a-118">Configurer un service ROC</span><span class="sxs-lookup"><span data-stu-id="0da1a-118">To set up an OCR service</span></span>
1. <span data-ttu-id="0da1a-119">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres service OCR**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="0da1a-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="0da1a-120">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="0da1a-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="0da1a-121">Vos données de connexion sont automatiquement chiffrées.</span><span class="sxs-lookup"><span data-stu-id="0da1a-121">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="0da1a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0da1a-122">See Also</span></span>
[<span data-ttu-id="0da1a-123">Traiter les documents entrants</span><span class="sxs-lookup"><span data-stu-id="0da1a-123">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="0da1a-124">Documents entrants</span><span class="sxs-lookup"><span data-stu-id="0da1a-124">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="0da1a-125">Achats</span><span class="sxs-lookup"><span data-stu-id="0da1a-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="0da1a-126">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0da1a-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
