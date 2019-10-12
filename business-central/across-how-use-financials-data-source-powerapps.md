---
title: Utilisez vos données pour créer une application | Microsoft Docs
description: Vous pouvez rendre vos données Business Central disponibles sous forme de source de données et spécifier une URL OData de vos services Web pour générer une application métier à l'aide de PowerApps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305052"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a><span data-ttu-id="59c93-103">Connexion à vos données Business Central pour générer un application professionnelle à l'aide de PowerApps</span><span class="sxs-lookup"><span data-stu-id="59c93-103">Connecting to Your Business Central Data to Build a Business App Using PowerApps</span></span>
<span data-ttu-id="59c93-104">Vous pouvez rendre vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles sous forme de source de données dans PowerApps.</span><span class="sxs-lookup"><span data-stu-id="59c93-104">You can make your [!INCLUDE[d365fin](includes/d365fin_md.md)] data available as a data source in PowerApps.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="59c93-105">Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec PowerApps.</span><span class="sxs-lookup"><span data-stu-id="59c93-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with PowerApps.</span></span>  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a><span data-ttu-id="59c93-106">Pour ajouter [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données dans PowerApps</span><span class="sxs-lookup"><span data-stu-id="59c93-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in PowerApps</span></span>
1. <span data-ttu-id="59c93-107">Dans votre navigateur, accédez à [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), puis connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="59c93-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="59c93-108">Sur la page d'accueil, choisissez **Applications**, **Créez une application** et **Canevas** pour créer une application de canevas.</span><span class="sxs-lookup"><span data-stu-id="59c93-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="59c93-109">Cette application sera conçue pour être utilisée sur un appareil mobile, mais vous pouvez également choisir d'utiliser un autre modèle.</span><span class="sxs-lookup"><span data-stu-id="59c93-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="59c93-110">L'étape suivante pour créer un PowerApp consiste à sélectionner vos données.</span><span class="sxs-lookup"><span data-stu-id="59c93-110">The next step to create a PowerApp is to select your data.</span></span> <span data-ttu-id="59c93-111">Cliquez sur l'icône représentant une flèche et choisissez l'option **Nouvelle connexion** dans le coin supérieur gauche de la page.</span><span class="sxs-lookup"><span data-stu-id="59c93-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="59c93-112">Dans la liste des connexions disponibles, choisissez **Business Central**, puis choisissez le bouton **Créer**.</span><span class="sxs-lookup"><span data-stu-id="59c93-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="59c93-113">PowerApps se connectera à votre [!INCLUDE [prodshort](includes/prodshort.md)] à l'aide des informations d'identification avec lesquelles vous vous êtes connecté.</span><span class="sxs-lookup"><span data-stu-id="59c93-113">PowerApps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="59c93-114">Si vous n'êtes pas un administrateur de votre [!INCLUDE [prodshort](includes/prodshort.md)], vous devrez peut-être vous connecter avec un autre compte.</span><span class="sxs-lookup"><span data-stu-id="59c93-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4.  <span data-ttu-id="59c93-115">PowerApps affiche la liste *Environnements et des sociétés* disponibles à partir de [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="59c93-115">PowerApps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="59c93-116">Choisissez l'environnement et la société contenant les données auxquelles vous souhaitez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="59c93-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="59c93-117">Une liste d’API est ensuite présentée.</span><span class="sxs-lookup"><span data-stu-id="59c93-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="59c93-118">Sélectionnez l'**API**à laquelle vous voulez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="59c93-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="59c93-119">Ces tables font partie de l'API [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="59c93-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="59c93-120">Il n'est pas nécessaire de configurer les points de terminaison vous-même, le connecteur [!INCLUDE [prodshort](includes/prodshort.md)] pour PowerApps s'en charge à votre place.</span><span class="sxs-lookup"><span data-stu-id="59c93-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for PowerApps does it for you.</span></span>  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

<span data-ttu-id="59c93-121">À ce stade, vous êtes connecté à vos données [!INCLUDE [prodshort](includes/prodshort.md)] et vous êtes prêt à générer votre application PowerApp.</span><span class="sxs-lookup"><span data-stu-id="59c93-121">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="59c93-122">Vous pouvez ajouter des écrans supplémentaires et vous connecter à des données supplémentaires à partir de votre [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="59c93-122">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="59c93-123">Pour plus d'informations, voir [Créer une application de canevas à partir d'un modèle dans PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="59c93-123">For more information, see [Create a canvas app from a template in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="59c93-124">Lorsque vous avez conçu et créé votre application, vous pouvez la partager avec vos collègues.</span><span class="sxs-lookup"><span data-stu-id="59c93-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="59c93-125">Pour plus d'informations, voir [Enregistrer et publier une application de canevas dans PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="59c93-125">For more information, see [Save and publish a canvas app in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="59c93-126">Si vous souhaitez vous connecter à [!INCLUDE [prodshort](includes/prodshort.md)] sur site, vous devez choisir le connecteur **Business Central (sur site)** dans l'étape 3.</span><span class="sxs-lookup"><span data-stu-id="59c93-126">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="59c93-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59c93-127">See Also</span></span>

[<span data-ttu-id="59c93-128">Créer une application de canevas à partir d'un modèle dans PowerApps</span><span class="sxs-lookup"><span data-stu-id="59c93-128">Create a canvas app from a template in PowerApps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="59c93-129">Mise en route</span><span class="sxs-lookup"><span data-stu-id="59c93-129">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="59c93-130">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="59c93-130">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="59c93-131">[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="59c93-131">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="59c93-132">Finances</span><span class="sxs-lookup"><span data-stu-id="59c93-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="59c93-133">Familiarisation avec le développement d'applications connectées pour Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="59c93-133">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
