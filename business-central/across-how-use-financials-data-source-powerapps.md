---
title: Utilisez vos données pour créer une application | Microsoft Docs
description: Vous pouvez rendre vos données Business Central disponibles sous forme de source de données et spécifier une URL OData de vos services Web pour générer une application métier à l’aide de Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5d2e6b75978d9aced7636b41623365f3d98ed3aa
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754507"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="b03bd-103">Connexion à vos données Business Central pour générer un application professionnelle à l’aide de Power Apps</span><span class="sxs-lookup"><span data-stu-id="b03bd-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="b03bd-104">Vous pouvez rendre vos données [!INCLUDE[prod_short](includes/prod_short.md)] disponibles sous forme de source de données dans Power Apps.</span><span class="sxs-lookup"><span data-stu-id="b03bd-104">You can make your [!INCLUDE[prod_short](includes/prod_short.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="b03bd-105">Vous devez disposer d'un compte valide avec [!INCLUDE[prod_short](includes/prod_short.md)] et avec Power Apps.</span><span class="sxs-lookup"><span data-stu-id="b03bd-105">You must have a valid account with [!INCLUDE[prod_short](includes/prod_short.md)] and with Power Apps.</span></span>  

## <a name="to-add-prod_short-as-a-data-source-in-power-apps"></a><span data-ttu-id="b03bd-106">Pour ajouter [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données dans Power Apps</span><span class="sxs-lookup"><span data-stu-id="b03bd-106">To add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="b03bd-107">Dans votre navigateur, accédez à [powerapps.microsoft.com](https://powerapps.microsoft.com/), puis connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="b03bd-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="b03bd-108">Sur la page d’accueil, dans la section **Commencer à partir des données**, choisissez la vignette **Autres sources de données**.</span><span class="sxs-lookup"><span data-stu-id="b03bd-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="b03bd-109">Cela ouvre Power Apps Studio.</span><span class="sxs-lookup"><span data-stu-id="b03bd-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="b03bd-110">Lors de la première connexion, vous devez spécifier le pays / la région.</span><span class="sxs-lookup"><span data-stu-id="b03bd-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="b03bd-111">Dans la liste des connexions disponibles, choisissez **Business Central**, puis choisissez le bouton **Créer**.</span><span class="sxs-lookup"><span data-stu-id="b03bd-111">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="b03bd-112">Power Apps se connectera à votre [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des informations d’identification avec lesquelles vous vous êtes connecté.</span><span class="sxs-lookup"><span data-stu-id="b03bd-112">Power Apps will connect to your [!INCLUDE[prod_short](includes/prod_short.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="b03bd-113">Si vous n’êtes pas un administrateur de votre [!INCLUDE[prod_short](includes/prod_short.md)], vous devrez peut-être vous connecter avec un autre compte.</span><span class="sxs-lookup"><span data-stu-id="b03bd-113">If you are not an administrator of your [!INCLUDE[prod_short](includes/prod_short.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="b03bd-114">Power Apps affiche la liste *Environnements et des sociétés* disponibles à partir de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b03bd-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b03bd-115">Choisissez l’environnement et la société contenant les données auxquelles vous souhaitez vous connecter, comme *PRODUCTION - Ma société*.</span><span class="sxs-lookup"><span data-stu-id="b03bd-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company*.</span></span>  

5. <span data-ttu-id="b03bd-116">Ensuite, une liste de tables qui sont exposées dans le cadre de l’API pour votre environnement vous sera présentée.</span><span class="sxs-lookup"><span data-stu-id="b03bd-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="b03bd-117">Sélectionnez la table à laquelle vous souhaitez vous connecter, puis choisissez **Connecter**.</span><span class="sxs-lookup"><span data-stu-id="b03bd-117">Select the table that you want to connect to, and then choose **Connect**.</span></span>

<span data-ttu-id="b03bd-118">Ces tables sont exposées en tant que points de terminaison par le connecteur [!INCLUDE[prod_short](includes/prod_short.md)] pour Power Apps.</span><span class="sxs-lookup"><span data-stu-id="b03bd-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prod_short](includes/prod_short.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="b03bd-119">Si vous souhaitez inclure des données d’autres tables de [!INCLUDE[prod_short](includes/prod_short.md)] dans votre application, vous devez faire appel à un développeur pour définir une API personnalisée [!INCLUDE[prod_short](includes/prod_short.md)] et utiliser cette API personnalisée via un connecteur personnalisé dans Power Apps.</span><span class="sxs-lookup"><span data-stu-id="b03bd-119">If you want to include data from other tables in [!INCLUDE[prod_short](includes/prod_short.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prod_short](includes/prod_short.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="b03bd-120">Pour plus d’informations, voir [Créer un connecteur personnalisé à partir de zéro](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="b03bd-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="b03bd-121">À ce stade, vous êtes connecté à vos données [!INCLUDE[prod_short](includes/prod_short.md)] et vous êtes prêt à générer votre application PowerApp.</span><span class="sxs-lookup"><span data-stu-id="b03bd-121">At this point, you have successfully connected to your [!INCLUDE[prod_short](includes/prod_short.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="b03bd-122">Vous pouvez ajouter des écrans supplémentaires et vous connecter à des données supplémentaires à partir de votre [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b03bd-122">You can add additional screens and connect to additional data from your [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b03bd-123">Pour plus d’informations, voir [Créer une application de canevas à partir d’un exemple dans Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="b03bd-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="b03bd-124">Lorsque vous avez conçu et créé votre application, vous pouvez la partager avec vos collègues.</span><span class="sxs-lookup"><span data-stu-id="b03bd-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="b03bd-125">Pour plus d’informations, voir [Enregistrer et publier une application de canevas dans Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="b03bd-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="b03bd-126">Si vous souhaitez vous connecter à [!INCLUDE[prod_short](includes/prod_short.md)] sur site, vous devez choisir le connecteur **Business Central (sur site)** dans l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="b03bd-126">If you want to connect to [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b03bd-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b03bd-127">See Also</span></span>

[<span data-ttu-id="b03bd-128">Créer une application de canevas à partir d’un modèle dans Power Apps</span><span class="sxs-lookup"><span data-stu-id="b03bd-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="b03bd-129">Importation des données métier à partir d’autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="b03bd-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="b03bd-130">[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="b03bd-130">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="b03bd-131">Familiarisation avec le développement d’applications connectées pour Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="b03bd-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
