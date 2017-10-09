---
title: "Envoyer des documents électroniques | Microsoft Docs"
description: "Découvrez comment envoyer des factures par voie électronique."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c41e8c59ced776591b1740930effa2420803eb65
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-send-electronic-documents"></a><span data-ttu-id="319f8-103">Procédure : envoyer des documents électroniques</span><span class="sxs-lookup"><span data-stu-id="319f8-103">How to: Send Electronic Documents</span></span>
<span data-ttu-id="319f8-104">La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge l'envoi de factures et d'avoirs électroniques au format PEPPOL, qui est pris en charge par les principaux fournisseurs de services d'échange de documents.</span><span class="sxs-lookup"><span data-stu-id="319f8-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="319f8-105">Un fournisseur de services d'échange de documents affecte des documents électroniques entre partenaires commerciaux.</span><span class="sxs-lookup"><span data-stu-id="319f8-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="319f8-106">Pour assurer la prise en charge d'autres formats de documents électroniques, vous pouvez utiliser l'infrastructure d'échange de données.</span><span class="sxs-lookup"><span data-stu-id="319f8-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="319f8-107">Dans la version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)], un service d'échange de documents est préconfiguré et prêt à être installé pour votre société.</span><span class="sxs-lookup"><span data-stu-id="319f8-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="319f8-108">Pour plus d'informations, reportez vous à [Procédure : configurer un service d'échange de document](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="319f8-108">For more information, see [How to: Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="319f8-109">Pour envoyer une facture vente en tant que document électronique PEPPOL, sélectionnez l'option **Document électronique** dans la boîte de dialogue **Valider et envoyer** à partir de laquelle vous pouvez également configurer le profil d'envoi de document par défaut du client.</span><span class="sxs-lookup"><span data-stu-id="319f8-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="319f8-110">Au préalable, vous devez configurer différentes données de base, telles que les informations sur la société, les clients, les articles, et les unités de mesure.</span><span class="sxs-lookup"><span data-stu-id="319f8-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="319f8-111">Celles-ci sont utilisées pour identifier les partenaires commerciaux et les articles lors de la conversion des données des champs dans [Procédure : configurer l'envoi et la réception de documents électroniques](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="319f8-111">These are used to identify the business partners and items when converting data in fields in [How to: Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="319f8-112">Envoyer une facture vente électronique</span><span class="sxs-lookup"><span data-stu-id="319f8-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="319f8-113">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Factures vente**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="319f8-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="319f8-114">Créez une facture vente.</span><span class="sxs-lookup"><span data-stu-id="319f8-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="319f8-115">Lorsque la facture vente est prête à être émise, sous l'onglet **Actions**, dans le groupe **Validation**, sélectionnez **Valider et envoyer**.</span><span class="sxs-lookup"><span data-stu-id="319f8-115">When the sales invoice is ready to be invoiced, on the **Actions** tab, in the **Posting** group, choose **Post and Send**.</span></span>  

     <span data-ttu-id="319f8-116">Si le profil d'envoi par défaut du client est **Document électronique**, il s'affiche dans la boîte de dialogue **Valider et envoyer une confirmation** et il vous suffit de choisir le bouton **Oui** pour valider et envoyer la facture par voie électronique au format sélectionné.</span><span class="sxs-lookup"><span data-stu-id="319f8-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="319f8-117">Dans la boîte de dialogue **Valider et envoyer une confirmation**, cliquez sur le bouton AssistEdit situé à droite du champ **Envoyer le document à**.</span><span class="sxs-lookup"><span data-stu-id="319f8-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="319f8-118">Dans la boîte de dialogue **Envoyer le document à**, dans le champ **Document électronique**, sélectionnez **Via le service d'échange de documents**.</span><span class="sxs-lookup"><span data-stu-id="319f8-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="319f8-119">Dans le champ **Format**, sélectionnez **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="319f8-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="319f8-120">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="319f8-120">Choose the **OK** button.</span></span> <span data-ttu-id="319f8-121">La boîte de dialogue **Valider et envoyer une confirmation** s'affiche.</span><span class="sxs-lookup"><span data-stu-id="319f8-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="319f8-122">**Document électronique (PEPPOL)** est ajouté au champ **Envoyer le document à**.</span><span class="sxs-lookup"><span data-stu-id="319f8-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="319f8-123">Cliquez sur le bouton **Oui**.</span><span class="sxs-lookup"><span data-stu-id="319f8-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="319f8-124">La facture vente enregistrée est validée et envoyée au client en tant que document électronique au format PEPPOL.</span><span class="sxs-lookup"><span data-stu-id="319f8-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="319f8-125">Vous pouvez également envoyer une facture vente validée en tant que document électronique.</span><span class="sxs-lookup"><span data-stu-id="319f8-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="319f8-126">La procédure est la même que celle décrite dans cette rubrique pour les documents vente non validés.</span><span class="sxs-lookup"><span data-stu-id="319f8-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="319f8-127">Dans la fenêtre **Facture vente enregistrée**, sous l'onglet **Actions**, dans le groupe **Général**, sélectionnez **Journal des activités** pour afficher le statut du document électronique.</span><span class="sxs-lookup"><span data-stu-id="319f8-127">In the **Posted Sales Invoice** window, on the **Actions** tab, in the **General** group, choose **Activity Log** to view the status of the electronic document.</span></span> <span data-ttu-id="319f8-128">Pour plus d'informations, voir **Journal des activités**.</span><span class="sxs-lookup"><span data-stu-id="319f8-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="319f8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="319f8-129">See Also</span></span>  
[<span data-ttu-id="319f8-130">Procédure : facturer des ventes</span><span class="sxs-lookup"><span data-stu-id="319f8-130">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="319f8-131">Procédure : configurer des profils d'envoi de documents</span><span class="sxs-lookup"><span data-stu-id="319f8-131">How to: Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="319f8-132">Procédure : Configurer l'envoi et la réception de documents électroniques</span><span class="sxs-lookup"><span data-stu-id="319f8-132">How to: Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="319f8-133">Procédure : configurer un service d'échange de document</span><span class="sxs-lookup"><span data-stu-id="319f8-133">How to: Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="319f8-134">Procédure : configurer les définitions d'échange de données</span><span class="sxs-lookup"><span data-stu-id="319f8-134">How to: Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="319f8-135">Échange de données en tant que documents électroniques</span><span class="sxs-lookup"><span data-stu-id="319f8-135">Exchanging Data as Electronic Documents</span></span>](across-data-exchange.md)  
[<span data-ttu-id="319f8-136">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="319f8-136">General Business Functionality</span></span>](ui-across-business-areas.md)  

