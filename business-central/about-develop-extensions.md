---
title: "Personnaliser Dynamics 365 Business Central | Microsoft Docs"
description: "Concevoir, présenter et promouvoir vos applications et extensions pour Business Central."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5f3557de5d69b8f64f85fabe4a60ecbddef276eb
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="extending-included365finlongincludesd365finlongmdmd"></a><span data-ttu-id="59cc8-103">Extension de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="59cc8-103">Extending [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="59cc8-104">Il existe de nombreux avantages à utiliser [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] comme plateforme pour les constructeurs d'applications :</span><span class="sxs-lookup"><span data-stu-id="59cc8-104">There are plenty of benefits of using [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] as a platform for App builders:</span></span>

* <span data-ttu-id="59cc8-105">[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] enrichie, une solution Microsoft en ligne prouvée, avec votre expertise</span><span class="sxs-lookup"><span data-stu-id="59cc8-105">Enrich [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], a proven Microsoft online solution, with your expertise</span></span>  
* <span data-ttu-id="59cc8-106">Profitez de la marque Business Central – marque que des millions d'utilisateurs connaissent et à laquelle ils font confiance</span><span class="sxs-lookup"><span data-stu-id="59cc8-106">Leverage the Business Central brand – a brand that millions of users know and trust</span></span>  
* <span data-ttu-id="59cc8-107">Atteignez plus de clients pour vos applications d'entreprise avec [Microsoft AppSource](https://appsource.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="59cc8-107">Reach more customers for your business apps with [Microsoft AppSource](https://appsource.microsoft.com/)</span></span>  
* <span data-ttu-id="59cc8-108">Faites-en plus avec une plate-forme qui fournit une expérience moderne et offre une évolutivité</span><span class="sxs-lookup"><span data-stu-id="59cc8-108">Achieve more with a platform that delivers a modern experience and offers scale</span></span>  
* <span data-ttu-id="59cc8-109">Associée à des applications professionnelles intelligentes telles que PowerApps, Flow, Power BI, Cortana Intelligence et bien d'autres encore</span><span class="sxs-lookup"><span data-stu-id="59cc8-109">Bundle with intelligent business apps such as PowerApps, Flow, Power BI, Cortana Intelligence, and many more</span></span>  

## <a name="to-bring-your-included365finincludesd365finmdmd-app-into-appsource"></a><span data-ttu-id="59cc8-110">Pour mettre l'application [!INCLUDE[d365fin](includes/d365fin_md.md)] dans AppSource :</span><span class="sxs-lookup"><span data-stu-id="59cc8-110">To bring your [!INCLUDE[d365fin](includes/d365fin_md.md)] app into AppSource:</span></span>
+ <span data-ttu-id="59cc8-111">Créez vos comptes</span><span class="sxs-lookup"><span data-stu-id="59cc8-111">Create your accounts</span></span>  
<span data-ttu-id="59cc8-112">Nous voulons que vous ayez accès à tous les outils nécessaires !</span><span class="sxs-lookup"><span data-stu-id="59cc8-112">We want you to have access to all the necessary tools!</span></span> <span data-ttu-id="59cc8-113">Vous devez disposer d'un ID Microsoft Partner Network, d'un compte développeur et d'un compte PSBC.</span><span class="sxs-lookup"><span data-stu-id="59cc8-113">You must have a Microsoft Partner Network ID, a Developer account, and a PSBC account.</span></span>
<span data-ttu-id="59cc8-114">Pour plus d'informations sur la manière dont vous pouvez obtenir vos comptes, accédez au document [Créez vos comptes.pdf](https://go.microsoft.com/fwlink/?linkid=841514) à partir du centre de téléchargement .</span><span class="sxs-lookup"><span data-stu-id="59cc8-114">For more information about how you can get your accounts in place, get the [Create your accounts.pdf](https://go.microsoft.com/fwlink/?linkid=841514) document from the Download Center.</span></span>

+ <span data-ttu-id="59cc8-115">Faites-nous part de vos idées d'application</span><span class="sxs-lookup"><span data-stu-id="59cc8-115">Engage with us about your app idea</span></span>  
<span data-ttu-id="59cc8-116">Partagez vos idées d'application [!INCLUDE[d365fin](includes/d365fin_md.md)] avec nous sur Microsoft AppSource !</span><span class="sxs-lookup"><span data-stu-id="59cc8-116">Share your [!INCLUDE[d365fin](includes/d365fin_md.md)] app idea with us on Microsoft AppSource!</span></span> <span data-ttu-id="59cc8-117">Après nous avoir envoyé votre idée, nous vous contacterons et nous vous fournirons tout ce dont vous avez besoin pour commencer à travailler sur votre application.</span><span class="sxs-lookup"><span data-stu-id="59cc8-117">After submitting your idea, we will engage with you and provide you with everything you need to start working on your app.</span></span>
<span data-ttu-id="59cc8-118">Pour plus d'informations sur toutes les étapes, accédez au document [Faites-nous part de vos idées d'application.pdf](https://go.microsoft.com/fwlink/?linkid=841515) à partir du centre de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="59cc8-118">For more information about all the steps, get the [Engage with us about your app idea document.pdf](https://go.microsoft.com/fwlink/?linkid=841515) document from the Download Center.</span></span>

+ <span data-ttu-id="59cc8-119">Développez les aspects techniques de votre application</span><span class="sxs-lookup"><span data-stu-id="59cc8-119">Develop the technical aspects of your app</span></span>    
<span data-ttu-id="59cc8-120">Après avoir configuré votre propre environnement de développement d'application, vous pouvez développer votre application.</span><span class="sxs-lookup"><span data-stu-id="59cc8-120">After you have set up your own app development environment, you can develop your app.</span></span>
<span data-ttu-id="59cc8-121">Pour plus d'informations sur tout que vous devez savoir sur la manière de développer les aspects techniques de votre application [!INCLUDE[d365fin](includes/d365fin_md.md)], accédez au document [Développez les aspects techniques de votre application.pdf](https://go.microsoft.com/fwlink/?linkid=841516) à partir du centre de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="59cc8-121">For more information about everything you need to know about how to develop the technical aspects of your [!INCLUDE[d365fin](includes/d365fin_md.md)] app, get the [Develop the technical aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) document from the Download Center.</span></span>

+ <span data-ttu-id="59cc8-122">Développez les aspects marketing de votre application</span><span class="sxs-lookup"><span data-stu-id="59cc8-122">Develop the marketing aspects of your app</span></span>  
<span data-ttu-id="59cc8-123">Si vous vous contentez de faire la liste des fonctions et des fonctionnalités de votre application, vous n'allez pas convertir les prospects en acheteurs.</span><span class="sxs-lookup"><span data-stu-id="59cc8-123">Simply listing your app's features and functionality will not convert prospects to buyers.</span></span> <span data-ttu-id="59cc8-124">Pour plus d'informations sur la meilleure façon de commercialiser votre application dans le marketplace AppSource, accédez au document [Développez les aspects marketing de votre application.pdf](https://go.microsoft.com/fwlink/?linkid=841518) à partir du centre de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="59cc8-124">For more information about how to best market your app in the AppSource marketplace, get the [Develop the marketing aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) from the Download Center.</span></span>

+ <span data-ttu-id="59cc8-125">Publiez votre application</span><span class="sxs-lookup"><span data-stu-id="59cc8-125">Publish your app</span></span>  
<span data-ttu-id="59cc8-126">Avant de publier votre application, nous collaborerons avec vous pour garantir qu'elle tient dans Microsoft AppSource et dans votre propre page de destination !</span><span class="sxs-lookup"><span data-stu-id="59cc8-126">Before we publish, we will collaborate with you to ensure that your app stands out on Microsoft AppSource and on your own landing page!</span></span> <span data-ttu-id="59cc8-127">Nous devons valider votre application pour garantir qu'elle soit bien commercialisée, fiable et à jour.</span><span class="sxs-lookup"><span data-stu-id="59cc8-127">We need to validate your app to ensure it is marketed well, trustworthy, and up to date.</span></span>
<span data-ttu-id="59cc8-128">Pour plus d'informations sur le processus de validation et la publication de votre application, accédez au document [Publiez votre application.pdf](https://go.microsoft.com/fwlink/?linkid=841517) à partir du centre de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="59cc8-128">For more information about the validation process and how to publish your app, get the [Publish your app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) document from the Download Center.</span></span>

## <a name="learn-more-about-extensions-v20"></a><span data-ttu-id="59cc8-129">En savoir plus sur les extensions v2.0</span><span class="sxs-lookup"><span data-stu-id="59cc8-129">Learn more about extensions v2.0</span></span>
<span data-ttu-id="59cc8-130">Les nouveaux outils de développement, qui vous permettent de créer des extensions v2.0, sont actuellement en prévisualisation et seront bientôt activés dans le service Business Central.</span><span class="sxs-lookup"><span data-stu-id="59cc8-130">The new development tools, which enable to you to build extensions v2.0, are currently in preview and will be enabled in the Business Central  service soon.</span></span> <span data-ttu-id="59cc8-131">Si vous souhaitez déjà vous familiariser avec les nouveaux outils ou en savoir plus sur les extensions 2.0, consultez [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).</span><span class="sxs-lookup"><span data-stu-id="59cc8-131">If you already want to familiarize yourself with the new tools or learn more about extensions 2.0, have a look at [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).</span></span>  

## <a name="need-help"></a><span data-ttu-id="59cc8-132">Besoin d'aide ?</span><span class="sxs-lookup"><span data-stu-id="59cc8-132">Need help?</span></span>
<span data-ttu-id="59cc8-133">Si vous souhaitez un accompagnement, vous pouvez contacter un expert du domaine d'application de la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="59cc8-133">If you would like some coaching, you can contact an app subject matter expert from the following list:</span></span>

* <span data-ttu-id="59cc8-134">Logiciels prêts pour le Cloud, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span><span class="sxs-lookup"><span data-stu-id="59cc8-134">Cloud Ready Software, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span></span>  
* <span data-ttu-id="59cc8-135">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span><span class="sxs-lookup"><span data-stu-id="59cc8-135">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span></span>

<span data-ttu-id="59cc8-136">Les partenaires dans cette liste :</span><span class="sxs-lookup"><span data-stu-id="59cc8-136">Partners in this list:</span></span>

* <span data-ttu-id="59cc8-137">Sont listés alphabétiquement</span><span class="sxs-lookup"><span data-stu-id="59cc8-137">Are listed alphabetically</span></span>  
* <span data-ttu-id="59cc8-138">Aident ou ont aidé au moins trois partenaires à mettre des applications dans Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="59cc8-138">Are assisting or have assisted a minimum of three partners with bringing apps into Microsoft AppSource</span></span>  
* <span data-ttu-id="59cc8-139">Ont un service packagé disponible (et répertorié dans leur site Web) offrant des conseils sur l'application qu'ils offrent</span><span class="sxs-lookup"><span data-stu-id="59cc8-139">Have a packaged service available (and listed on their website) about the app guidance that they provide</span></span>  

<span data-ttu-id="59cc8-140">Si vous pensez que vous devez être répertorié en tant que partenaire de service d'application, contactez [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="59cc8-140">If you believe you should be listed as an app service partner, don't hesitate to reach out to [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="questions"></a><span data-ttu-id="59cc8-141">Vous avez des questions ?</span><span class="sxs-lookup"><span data-stu-id="59cc8-141">Questions?</span></span>
<span data-ttu-id="59cc8-142">Cette [FAQ](https://go.microsoft.com/fwlink/?linkid=841520) répond aux questions courantes que vous pourriez avoir sur les applications pour [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="59cc8-142">This [FAQ](https://go.microsoft.com/fwlink/?linkid=841520) responds to the most common questions you might have about apps for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="59cc8-143">Si vous avez d'autres questions, n'hésitez pas à contacter votre représentant local Microsoft ou envoyez un e-mail à [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="59cc8-143">If you have further questions, don't hesitate to contact your local Microsoft representative or email [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="further-resources"></a><span data-ttu-id="59cc8-144">Autres ressources</span><span class="sxs-lookup"><span data-stu-id="59cc8-144">Further Resources</span></span>
<span data-ttu-id="59cc8-145">Vous trouverez d'autres ressources pour le développement d'application dans notre [page de rubrique DLP](https://mbspartner.microsoft.com/BFI/Topic/76) page de rubrique DLP.</span><span class="sxs-lookup"><span data-stu-id="59cc8-145">Please find further resources for app development on our [DLP topic page](https://mbspartner.microsoft.com/BFI/Topic/76) DLP topic page.</span></span> <span data-ttu-id="59cc8-146">Quelques-unes sont répertoriées ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="59cc8-146">Some selected ones are available below:</span></span>
-   [<span data-ttu-id="59cc8-147">Enregistrement de l'utilisateur et facturation ultérieure </span><span class="sxs-lookup"><span data-stu-id="59cc8-147">User Registration and Subsequent Billing </span></span>](http://download.microsoft.com/download/3/2/0/320D0286-8810-4A8F-B7DD-523ED87D441B/FAQ on apps for Dynamics 365 for Financials.pdf)



## <a name="see-also"></a><span data-ttu-id="59cc8-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59cc8-148">See Also</span></span>
[<span data-ttu-id="59cc8-149">Mise en route</span><span class="sxs-lookup"><span data-stu-id="59cc8-149">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="59cc8-150">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="59cc8-150">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[https://appsource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365-for-financials&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

