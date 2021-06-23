---
title: Recherche d’écritures | Microsoft Docs
description: Cet article décrit comment accéder aux documents et écritures liés
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a29cea15cba15da1bc68816e07f76de59f43958b
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216143"
---
# <a name="finding-related-entries-for-posted-documents"></a><span data-ttu-id="86a07-103">Recherche d’écritures associées pour les documents validés</span><span class="sxs-lookup"><span data-stu-id="86a07-103">Finding Related Entries for Posted Documents</span></span> 

<span data-ttu-id="86a07-104">Dans cet article, vous apprenez à rechercher des documents et des écritures liés les uns aux autres en fonction d’informations communes, telles que :</span><span class="sxs-lookup"><span data-stu-id="86a07-104">In this article, you learn how to find documents and entries that are related to each other based on a common information, like:</span></span>

- <span data-ttu-id="86a07-105">Un numéro de document ou une date comptabilisation</span><span class="sxs-lookup"><span data-stu-id="86a07-105">Document number or posting date</span></span>
- <span data-ttu-id="86a07-106">Type de contact professionnel, numéro ou numéro de document externe</span><span class="sxs-lookup"><span data-stu-id="86a07-106">Business contact type, number, or external document number</span></span>
- <span data-ttu-id="86a07-107">Numéro de série ou numéro de lot de l’article</span><span class="sxs-lookup"><span data-stu-id="86a07-107">Item serial number or lot number</span></span>

<span data-ttu-id="86a07-108">Cette fonctionnalité est très utile pour rechercher les écritures comptables qui résultent de certaines transactions.</span><span class="sxs-lookup"><span data-stu-id="86a07-108">This feature is useful for finding the ledger entries that resulted from certain transactions.</span></span> <span data-ttu-id="86a07-109">Lors d’une recherche par numéros de document, vous pouvez imprimer le résumé à partir de l’état Écritures document.</span><span class="sxs-lookup"><span data-stu-id="86a07-109">When you search by document number, you can print the summary from the Document Entries report.</span></span>

## <a name="get-started"></a><span data-ttu-id="86a07-110">Démarrer</span><span class="sxs-lookup"><span data-stu-id="86a07-110">Get started</span></span>

<span data-ttu-id="86a07-111">La fonctionnalité de recherche d’écritures est facilement disponible sur la plupart des pages qui affichent des documents validés ou des écritures de documents validés, pour les listes et les fiches.</span><span class="sxs-lookup"><span data-stu-id="86a07-111">The find entries feature is readily available on most pages that display posted documents or posted documents entries - for both lists and cards.</span></span> <span data-ttu-id="86a07-112">La première étape consiste donc à ouvrir l’une de ces pages.</span><span class="sxs-lookup"><span data-stu-id="86a07-112">So the first step is open one of these pages.</span></span> <span data-ttu-id="86a07-113">Ensuite, choisissez l’action **Rechercher des écritures** ou appuyez sur les touches Alt+G.</span><span class="sxs-lookup"><span data-stu-id="86a07-113">Then, either choose the **Find Entries** action or press the Alt+G keys.</span></span>

<span data-ttu-id="86a07-114">La page **Rechercher des écritures** comprend tous les documents et écritures liés basés sur le n° document et la date comptabilisation.</span><span class="sxs-lookup"><span data-stu-id="86a07-114">The **Find Entries** page  includes all related documents and entries based on the document no. and posting date.</span></span> <span data-ttu-id="86a07-115">La page est divisée en trois sections :</span><span class="sxs-lookup"><span data-stu-id="86a07-115">The page is divided into three sections:</span></span>

- <span data-ttu-id="86a07-116">La section supérieure affiche les champs et les actions que vous utilisez pour filtrer votre recherche.</span><span class="sxs-lookup"><span data-stu-id="86a07-116">The top section displays fields and actions that you use for filtering your search.</span></span>
- <span data-ttu-id="86a07-117">La section du milieu affiche les documents associés en fonction de la recherche.</span><span class="sxs-lookup"><span data-stu-id="86a07-117">The middle section displays related documents based on the search.</span></span>
- <span data-ttu-id="86a07-118">La section inférieure affiche des informations sur le document source qui a été trouvé lors de la recherche.</span><span class="sxs-lookup"><span data-stu-id="86a07-118">The bottom section displays information about the source document that was found by searching.</span></span>


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a><span data-ttu-id="86a07-119">Rechercher des écritures</span><span class="sxs-lookup"><span data-stu-id="86a07-119">Search for entries</span></span>

<span data-ttu-id="86a07-120">Vous pouvez rechercher des écritures en fonction des informations relatives au document, au contact professionnel ou à la référence d’article.</span><span class="sxs-lookup"><span data-stu-id="86a07-120">You can search for entries based on information about either the document, business contact, or item reference.</span></span> <span data-ttu-id="86a07-121">Pour modifier la recherche, sélectionnez **Actions**, **Rechercher par**, puis l’une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="86a07-121">To change the search, select **Actions**, **Find By**, then one of the following actions:</span></span>

|<span data-ttu-id="86a07-122">Action</span><span class="sxs-lookup"><span data-stu-id="86a07-122">Action</span></span>|<span data-ttu-id="86a07-123">Description</span><span class="sxs-lookup"><span data-stu-id="86a07-123">Description</span></span>|
|------|-----------|
|<span data-ttu-id="86a07-124">Rechercher par document</span><span class="sxs-lookup"><span data-stu-id="86a07-124">Find by Document</span></span>|<span data-ttu-id="86a07-125">Affichez les écritures en fonction d’un numéro de document ou d’une date comptabilisation spécifique.</span><span class="sxs-lookup"><span data-stu-id="86a07-125">View entries based on a specific document number or posting date.</span></span>|
|<span data-ttu-id="86a07-126">Contact professionnel</span><span class="sxs-lookup"><span data-stu-id="86a07-126">Business Contact</span></span> |<span data-ttu-id="86a07-127">Affichez les écritures en fonction d’un type de contact spécifique, d’un numéro de contact, et/ou d’un numéro de document externe.</span><span class="sxs-lookup"><span data-stu-id="86a07-127">View entries based on a specific contact type, contact number, anr/or external document number.</span></span> <span data-ttu-id="86a07-128">Vous pouvez saisir des informations qui ont été affectées par un fournisseur ou un client.</span><span class="sxs-lookup"><span data-stu-id="86a07-128">You can enter document information that was assigned by a vendor or a customer.</span></span> <span data-ttu-id="86a07-129">Utilisez les champs disponibles pour rechercher des documents du fournisseur en utilisant les numéros que le fournisseur a affecté aux documents.</span><span class="sxs-lookup"><span data-stu-id="86a07-129">Use the available fields to search for vendor documents by using the numbers that the vendor has assigned the documents.</span></span>|
|<span data-ttu-id="86a07-130">Référence d’article</span><span class="sxs-lookup"><span data-stu-id="86a07-130">Item reference</span></span>|<span data-ttu-id="86a07-131">Afficher les écritures en fonction d’un n° de série ou d’un n° lot.</span><span class="sxs-lookup"><span data-stu-id="86a07-131">View entires based on a serial number or lot number.</span></span> <span data-ttu-id="86a07-132">Vous pouvez spécifier le n° de série ou lot, ou un filtre sur le n° de série ou lot à rechercher.</span><span class="sxs-lookup"><span data-stu-id="86a07-132">You can enter the lot number or serial number, or filter on the lot number or serial number that you want to search for.</span></span> <span data-ttu-id="86a07-133">Cette action est utile pour voir où un numéro de traçabilité spécifique a été utilisé, de quel vendeur il provient ou à quel client il a été vendu.</span><span class="sxs-lookup"><span data-stu-id="86a07-133">This action is useful to see where a specific item tracking number was used, what vendor it came from, or what customer it was sold to.</span></span>|

<span data-ttu-id="86a07-134">Après avoir effectué une sélection, entrez les informations de recherche pertinentes dans les champs d’en haut.</span><span class="sxs-lookup"><span data-stu-id="86a07-134">After you make a selection, enter the relevant search information in the fields at the top.</span></span> <span data-ttu-id="86a07-135">Utilisez les info-bulles sur les champs pour vous aider.</span><span class="sxs-lookup"><span data-stu-id="86a07-135">Use the tooltips on the fields to help.</span></span> <span data-ttu-id="86a07-136">Lorsque vous avez terminé, choisissez **Rechercher** pour lancer la recherche.</span><span class="sxs-lookup"><span data-stu-id="86a07-136">When you're finished, choose **Find** to start the search.</span></span> <span data-ttu-id="86a07-137">Si vous modifiez l’un des filtres, vous devez cliquer sur **Rechercher** à nouveau.</span><span class="sxs-lookup"><span data-stu-id="86a07-137">If you change any of the filters, you have to choose **Find** again.</span></span>

> [!TIP]
> <span data-ttu-id="86a07-138">Pour consulter quelques exemples d’utilisation de **Recherche des écritures**, voir [Tracer des articles - Articles suivis](inventory-how-to-trace-item-tracked-items.md)</span><span class="sxs-lookup"><span data-stu-id="86a07-138">For a couple examples about using **Find Entries**, see [Trace Item-Tracked Items](inventory-how-to-trace-item-tracked-items.md)</span></span> <!--and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md). -->

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="86a07-139">Voir la formation associée sur [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="86a07-139">See Related Training at [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="86a07-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86a07-140">See Also</span></span>

[<span data-ttu-id="86a07-141">Utilisation de Business Central</span><span class="sxs-lookup"><span data-stu-id="86a07-141">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="86a07-142">Ajouter une action de page à votre Tableau de bord</span><span class="sxs-lookup"><span data-stu-id="86a07-142">Add a Page Action to Your Role Center</span></span>](ui-bookmarks.md)  
[<span data-ttu-id="86a07-143">Tracer des articles - Articles suivis</span><span class="sxs-lookup"><span data-stu-id="86a07-143">Trace Item-Tracked Items</span></span>](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
