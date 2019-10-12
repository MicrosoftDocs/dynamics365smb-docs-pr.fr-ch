---
title: Modifier les documents vente et achat validés | Microsoft Docs
description: Découvrez les différentes fonctions de validation pour valider les documents achat et comment mettre à jour les documents validés.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6fbb4e458b0e4f9068b234748a3921dbca6b3222
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300608"
---
# <a name="edit-posted-documents"></a><span data-ttu-id="7dff3-103">Valider les documents validés</span><span class="sxs-lookup"><span data-stu-id="7dff3-103">Edit Posted Documents</span></span>
<span data-ttu-id="7dff3-104">Parfois, vous devez mettre à jour un document validé, car les informations pertinentes pour le document ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="7dff3-104">Sometimes you have to update a posted document because information that is relevant to the document has changed.</span></span> <span data-ttu-id="7dff3-105">Sur un document de vente validé, il peut s'agir du numéro de suivi du colis du transporteur, par exemple.</span><span class="sxs-lookup"><span data-stu-id="7dff3-105">On a posted sales document, this can be the shipping agent's package tracking number, for example.</span></span> <span data-ttu-id="7dff3-106">Sur un document d'achat validé, il peut s'agir d'un texte de référence de paiement.</span><span class="sxs-lookup"><span data-stu-id="7dff3-106">On a posted purchase document, this can be a payment reference text.</span></span>

<span data-ttu-id="7dff3-107">Vous effectuez la modification sur une version modifiable du document d'origine, indiquée par «  **- Mettre à jour** » dans le titre de la page.</span><span class="sxs-lookup"><span data-stu-id="7dff3-107">You perform the change on an editable version of the original document, indicated by "**- Update**" in the page title.</span></span> <span data-ttu-id="7dff3-108">La page contient un sous-ensemble des champs sur le document d'origine, dont certains sont des champs non modifiables affichés uniquement à titre d'information.</span><span class="sxs-lookup"><span data-stu-id="7dff3-108">The page contains a subset of the fields on the original document, of which some are non-editable fields that are shown for information only.</span></span>

<span data-ttu-id="7dff3-109">La fonctionnalité est disponible pour les documents suivants dans les versions de tous les pays :</span><span class="sxs-lookup"><span data-stu-id="7dff3-109">The functionality is available for the following documents in all country versions:</span></span>
- <span data-ttu-id="7dff3-110">Expédition vente enregistrée</span><span class="sxs-lookup"><span data-stu-id="7dff3-110">Posted Sales Shipment</span></span>
- <span data-ttu-id="7dff3-111">Facture achat enregistrée</span><span class="sxs-lookup"><span data-stu-id="7dff3-111">Posted Purchase Invoice</span></span>
- <span data-ttu-id="7dff3-112">Expédition retour enregistrée</span><span class="sxs-lookup"><span data-stu-id="7dff3-112">Posted Return Shipment</span></span>
- <span data-ttu-id="7dff3-113">Réception retour enregistrée</span><span class="sxs-lookup"><span data-stu-id="7dff3-113">Posted Return Receipt</span></span>

<span data-ttu-id="7dff3-114">Les documents supplémentaires suivants peuvent être modifiés dans les versions des pays sélectionnés :</span><span class="sxs-lookup"><span data-stu-id="7dff3-114">The following additional documents can be edited in selected country versions:</span></span>
- <span data-ttu-id="7dff3-115">ES : facture vente enregistrée, avoir vente enregistré, avoir achat validé</span><span class="sxs-lookup"><span data-stu-id="7dff3-115">ES: Posted Sales Invoice, Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="7dff3-116">APAC : avoir vente enregistré, avoir achat validé</span><span class="sxs-lookup"><span data-stu-id="7dff3-116">APAC: Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="7dff3-117">RU : avoir vente enregistré</span><span class="sxs-lookup"><span data-stu-id="7dff3-117">RU: Posted Sales Credit Memo</span></span>
- <span data-ttu-id="7dff3-118">IT : expédition de transfert validée, expédition de service validée</span><span class="sxs-lookup"><span data-stu-id="7dff3-118">IT: Posted Transfer Shipment, Posted Service Shipment</span></span>

## <a name="to-edit-a-posted-sales-shipment"></a><span data-ttu-id="7dff3-119">Pour modifier une expédition vente enregistrée</span><span class="sxs-lookup"><span data-stu-id="7dff3-119">To edit a posted sales shipment</span></span>
<span data-ttu-id="7dff3-120">Ce qui suit explique comment modifier une expédition vente enregistrée</span><span class="sxs-lookup"><span data-stu-id="7dff3-120">The following explains how to edit a posted sales shipment.</span></span> <span data-ttu-id="7dff3-121">Les étapes sont similaires pour les autres documents pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7dff3-121">The steps are similar for the other supported documents.</span></span>

1. <span data-ttu-id="7dff3-122">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Expéditions vente enregistrées**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7dff3-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Shipments**, and then choose the related link.</span></span>
2. <span data-ttu-id="7dff3-123">Sélectionnez le document que vous souhaitez modifier, puis sélectionnez l'action **Mettre à jour le document**.</span><span class="sxs-lookup"><span data-stu-id="7dff3-123">Select the document that you want to edit, and then choose the **Update Document** action.</span></span> <span data-ttu-id="7dff3-124">Sinon, ouvrez le document, puis choisissez l'action.</span><span class="sxs-lookup"><span data-stu-id="7dff3-124">Alternatively, open the document and then choose the action.</span></span>
3. <span data-ttu-id="7dff3-125">Sur la page **Expédition vente enregistrée - Mettre à jour**, modifiez le champ **N° de suivi du colis**</span><span class="sxs-lookup"><span data-stu-id="7dff3-125">On the **Posted Sales Shipment - Update** page, edit the **Package Tracking No.**</span></span> <span data-ttu-id="7dff3-126">par exemple.</span><span class="sxs-lookup"><span data-stu-id="7dff3-126">field, for example.</span></span>
4. <span data-ttu-id="7dff3-127">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="7dff3-127">Choose the **OK** button.</span></span>

<span data-ttu-id="7dff3-128">L'expédition vente enregistrée est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7dff3-128">The posted sales shipment is updated.</span></span>

## <a name="see-also"></a><span data-ttu-id="7dff3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dff3-129">See Also</span></span>
[<span data-ttu-id="7dff3-130">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="7dff3-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
[<span data-ttu-id="7dff3-131">Achats</span><span class="sxs-lookup"><span data-stu-id="7dff3-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="7dff3-132">Validation des documents et des feuilles</span><span class="sxs-lookup"><span data-stu-id="7dff3-132">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="7dff3-133">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7dff3-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
