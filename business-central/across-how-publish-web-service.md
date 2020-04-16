---
title: Exposer des objets en tant que services Web | Microsoft Docs
description: Publiez des objets en tant que services Web afin de les rendre immédiatement disponibles pour votre solution Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 04af1a52bb0a2e14a2775efe6e3a6ccf77441d29
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188507"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="4c6eb-103">Publier un service Web</span><span class="sxs-lookup"><span data-stu-id="4c6eb-103">Publish a Web Service</span></span>

<span data-ttu-id="4c6eb-104">Les services Web sont un moyen pratique de rendre une fonctionnalité d'application disponible à différents systèmes et utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="4c6eb-105">inclut plusieurs objets qui sont exposés par défaut en tant que services Web en raison de l'intégration à d'autres services Microsoft, mais vous pouvez également ajouter d'autres services Web.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-105">includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="4c6eb-106">Vous devez configurer un service Web dans le client [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4c6eb-106">You set up a web service in the [!INCLUDE[d365fin](includes/d365fin_md.md)] client.</span></span> <span data-ttu-id="4c6eb-107">Vous devez ensuite publier le service Web pour le rendre disponible aux demandes de service sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="4c6eb-108">Les utilisateurs peuvent découvrir les services Web en pointant un navigateur sur l'emplacement du serveur et en demandant la liste des services disponibles.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="4c6eb-109">Lorsque vous publiez un service Web, il est immédiatement disponible sur le réseau pour les utilisateurs authentifiés.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="4c6eb-110">Tous les utilisateurs autorisés peuvent accéder aux métadonnées des services Web, mais seuls les utilisateurs ayant les autorisations nécessaires peuvent accéder aux données réelles.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="4c6eb-111">Création et publication d'un service Web</span><span class="sxs-lookup"><span data-stu-id="4c6eb-111">Creating and Publishing a Web Service</span></span>  
<span data-ttu-id="4c6eb-112">Les étapes suivantes expliquent la procédure de création et de publication d'un service Web.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-112">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="4c6eb-113">Création et publication d'un service Web</span><span class="sxs-lookup"><span data-stu-id="4c6eb-113">To create and publish a web service</span></span>  

1. <span data-ttu-id="4c6eb-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Services Web**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4c6eb-115">Sur la page **Services Web**, sélectionnez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-115">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="4c6eb-116">Les types valides pour les services Web SOAP sont **Codeunit** et **Page**.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="4c6eb-117">Les types valides pour les services Web OData sont **Page** et **Requête**.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    > <span data-ttu-id="4c6eb-118">De même, si la base de données contient plusieurs sociétés, vous pouvez choisir un ID objet qui est spécifique à l'une des sociétés.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="4c6eb-119">Enfin, le nom de service est visible par les clients de votre service Web et sert de base pour identifier et distinguer les services Web, il doit donc être explicite.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="4c6eb-120">Activez la case à cocher dans la colonne **Publié**.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-120">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="4c6eb-121">Lorsque vous publiez le service Web, dans les champs **URL OData** et **URL SOAP**, vous pouvez voir les URL générées pour le service Web.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="4c6eb-122">Vous pouvez tester le service Web immédiatement en choisissant les liens figurant dans les champs **URL OData** et **URL SOAP**.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="4c6eb-123">Éventuellement, vous pouvez copier la valeur du champ et pour l'enregistrer pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="4c6eb-124">Pour les codeunits publiés en tant que service Web SOAP, les méthodes exposées dans le codeunit doivent être marquées comme `[External]` dans le code.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-124">For codeunits that are published as a SOAP web service, the methods exposed in the codeunit must be marked as `[External]` in the code.</span></span>

<span data-ttu-id="4c6eb-125">Une fois le service Web publié, il est accessible aux parties externes.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-125">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="4c6eb-126">Vous pouvez vérifier la disponibilité de ce service Web à l'aide d'un navigateur, ou vous pouvez sélectionner le lien dans les champs **URL OData** et **URL SOAP** de la page **Services Web**.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-126">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="4c6eb-127">La procédure suivante indique comment vous pouvez vérifier la disponibilité du service Web pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-127">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="4c6eb-128">Vérification de la disponibilité d'un service Web</span><span class="sxs-lookup"><span data-stu-id="4c6eb-128">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="4c6eb-129">Dans votre navigateur, indiquez l'URL appropriée.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-129">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="4c6eb-130">Le tableau suivant illustre les types d'URL que vous pouvez entrer pour les différents types de services Web.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-130">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="4c6eb-131">Type</span><span class="sxs-lookup"><span data-stu-id="4c6eb-131">Type</span></span>|<span data-ttu-id="4c6eb-132">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c6eb-132">Syntax</span></span>|<span data-ttu-id="4c6eb-133">Exemple :</span><span class="sxs-lookup"><span data-stu-id="4c6eb-133">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="4c6eb-134">SOAP</span><span class="sxs-lookup"><span data-stu-id="4c6eb-134">SOAP</span></span>|<span data-ttu-id="4c6eb-135">https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/</span><span class="sxs-lookup"><span data-stu-id="4c6eb-135">https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/</span></span> |https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument|
    > |<span data-ttu-id="4c6eb-136">OData V4</span><span class="sxs-lookup"><span data-stu-id="4c6eb-136">OData V4</span></span>|<span data-ttu-id="4c6eb-137">https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*</span><span class="sxs-lookup"><span data-stu-id="4c6eb-137">https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*</span></span>|<span data-ttu-id="4c6eb-138">https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument</span><span class="sxs-lookup"><span data-stu-id="4c6eb-138">https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument</span></span><br/>    <span data-ttu-id="4c6eb-139">Le nom de la société respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-139">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="4c6eb-140">Examinez les informations affichées dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-140">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="4c6eb-141">Vérifiez que vous pouvez visualiser le nom du service Web que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-141">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="4c6eb-142">Lorsque vous accédez à un service Web, et que vous souhaitez copier des données vers [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez spécifier le nom de la société.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-142">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="4c6eb-143">Vous pouvez spécifier la société en tant que membre de l'URI comme l'indiquent les exemples, ou vous pouvez spécifier la société comme partie des paramètres de requête.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-143">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="4c6eb-144">Par exemple, les URI suivants pointent vers le même service Web OData et qu'ils sont tous deux des URI valides.</span><span class="sxs-lookup"><span data-stu-id="4c6eb-144">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="4c6eb-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c6eb-145">See Also</span></span>

[<span data-ttu-id="4c6eb-146">Administration</span><span class="sxs-lookup"><span data-stu-id="4c6eb-146">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="4c6eb-147">Services Web Business Central pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="4c6eb-147">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
