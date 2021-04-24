---
title: Envoyer des documents électroniques
description: Découvrez comment envoyer des factures par voie électronique.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8056aa66531740634fb155e0b3b4419a7f014ffc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778387"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="7b3bc-103">Envoyer des documents électroniques</span><span class="sxs-lookup"><span data-stu-id="7b3bc-103">Send Electronic Documents</span></span>

<span data-ttu-id="7b3bc-104">La version générique de [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge l’envoi de factures et d’avoirs électroniques au format PEPPOL, qui est pris en charge par les principaux fournisseurs de services d’échange de documents.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-104">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports sending electronic invoices and credit memos in the PEPPOL format, a format that the largest document exchange service providers support.</span></span> <span data-ttu-id="7b3bc-105">Un fournisseur de services d’échange de documents affecte des documents électroniques entre partenaires commerciaux.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="7b3bc-106">Pour assurer la prise en charge d’autres formats de documents électroniques, vous pouvez utiliser l’infrastructure d’échange de données.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="7b3bc-107">Dans la version générique de [!INCLUDE[prod_short](includes/prod_short.md)], un service d’échange de documents est préconfiguré et prêt à être installé pour votre société.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-107">In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="7b3bc-108">Pour plus d’informations, reportez vous à [Configurer un service d’échange de document](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="7b3bc-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span> <span data-ttu-id="7b3bc-109">Cependant, dans certains cas, vous devez installer une application.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-109">However, in some cases, you must install an app.</span></span> <span data-ttu-id="7b3bc-110">Pour plus d’informations, voir [FAQ Facturation électronique](faq-electronic-invoicing.yml).</span><span class="sxs-lookup"><span data-stu-id="7b3bc-110">For more information, see [Electronic Invoicing FAQ](faq-electronic-invoicing.yml).</span></span>  

 <span data-ttu-id="7b3bc-111">Pour envoyer une facture vente en tant que document PEPPOL électronique, sélectionnez l’option **Document électronique** dans la boîte de dialogue **Valider et envoyer**.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-111">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box.</span></span> <span data-ttu-id="7b3bc-112">Vous pouvez également définir le profil d’envoi de document par défaut du client à partir de cette boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-112">You can also set up the customer's default document sending profile from that dialog box.</span></span> <span data-ttu-id="7b3bc-113">Au préalable, vous devez configurer différentes données de base, telles que les informations sur la société, les clients, les articles, et les unités de mesure.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-113">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="7b3bc-114">Celles-ci sont utilisées pour identifier les partenaires commerciaux et les articles lors de la conversion des données des champs dans [Configurer l’envoi et la réception de documents électroniques](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="7b3bc-114">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="7b3bc-115">Envoyer une facture vente électronique</span><span class="sxs-lookup"><span data-stu-id="7b3bc-115">To send an electronic sales invoice</span></span>

1. <span data-ttu-id="7b3bc-116">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2. <span data-ttu-id="7b3bc-117">Créez une facture vente.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-117">Create a new sales invoice.</span></span>  

3. <span data-ttu-id="7b3bc-118">Lorsque la facture vente est prête à être émise, sélectionnez l’action **Valider et envoyer**.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-118">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="7b3bc-119">Si le profil d’envoi par défaut du client est **Document électronique**, il s’affichera dans la boîte de dialogue **Valider et envoyer une confirmation**.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-119">If the customer's default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box.</span></span> <span data-ttu-id="7b3bc-120">De cette façon, il vous suffit d’opter pour le bouton **Oui** pour valider et envoyer la facture par voie électronique dans le format sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-120">This way, you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4. <span data-ttu-id="7b3bc-121">Dans la boîte de dialogue **Valider et envoyer une confirmation**, cliquez sur le bouton AssistEdit situé à droite du champ **Envoyer le document à**.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-121">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5. <span data-ttu-id="7b3bc-122">Dans la boîte de dialogue **Envoyer le document à**, dans le champ **Document électronique**, sélectionnez **Via le service d’échange de documents**.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-122">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6. <span data-ttu-id="7b3bc-123">Dans le champ **Format**, sélectionnez **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-123">In the **Format** field, choose **PEPPOL**.</span></span>  

7. <span data-ttu-id="7b3bc-124">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-124">Choose the **OK** button.</span></span> <span data-ttu-id="7b3bc-125">La boîte de dialogue **Valider et envoyer une confirmation** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-125">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="7b3bc-126">**Document électronique (PEPPOL)** est ajouté au champ **Envoyer le document à**.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-126">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8. <span data-ttu-id="7b3bc-127">Cliquez sur le bouton **Oui**.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-127">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="7b3bc-128">La facture vente enregistrée est validée et envoyée au client au format PEPPOL.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-128">The sales invoice is posted and sent to the customer in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="7b3bc-129">Vous pouvez également envoyer une facture vente validée en tant que document électronique.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-129">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="7b3bc-130">La procédure est la même que celle décrite dans cette rubrique pour les documents vente non validés.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-130">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="7b3bc-131">Sur la page **Facture vente enregistrée**, sélectionnez l’action **Journal des activités** pour afficher le statut du document électronique.</span><span class="sxs-lookup"><span data-stu-id="7b3bc-131">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="7b3bc-132">Voir la formation associée sur [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="7b3bc-132">See Related Training at [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="7b3bc-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b3bc-133">See Also</span></span>

[<span data-ttu-id="7b3bc-134">Facturer des ventes</span><span class="sxs-lookup"><span data-stu-id="7b3bc-134">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="7b3bc-135">Configurer des profils d’envoi de documents</span><span class="sxs-lookup"><span data-stu-id="7b3bc-135">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="7b3bc-136">Configurer l’envoi et la réception de documents électroniques</span><span class="sxs-lookup"><span data-stu-id="7b3bc-136">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="7b3bc-137">Configurer un service d’échange de document</span><span class="sxs-lookup"><span data-stu-id="7b3bc-137">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="7b3bc-138">Configurer les définitions d’échange de données</span><span class="sxs-lookup"><span data-stu-id="7b3bc-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="7b3bc-139">Échanger des données par voir électronique</span><span class="sxs-lookup"><span data-stu-id="7b3bc-139">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="7b3bc-140">FAQ Facturation électronique</span><span class="sxs-lookup"><span data-stu-id="7b3bc-140">Electronic Invoicing FAQ</span></span>](faq-electronic-invoicing.yml)  
[<span data-ttu-id="7b3bc-141">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="7b3bc-141">General Business Functionality</span></span>](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]