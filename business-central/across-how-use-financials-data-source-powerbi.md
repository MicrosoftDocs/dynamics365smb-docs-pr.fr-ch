---
title: Utilisez les états Business Central dans Power BI | Microsoft Docs
description: Vous pouvez rendre vos données disponibles sous forme de source de données dans Power BI et créer des rapports puissants sur l'état de votre activité.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4f140303f037ea4a914cba1ded44fd453bcdfabb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187907"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="77a08-103">Utilisation de [!INCLUDE [prodlong](includes/prodlong.md)] comme source de données Power BI pour générer des états</span><span class="sxs-lookup"><span data-stu-id="77a08-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="77a08-104">Vous pouvez rendre vos données [!INCLUDE[prodlong](includes/prodlong.md)] disponibles sous forme de source de données dans Power BI et créer des rapports puissants sur l'état de votre activité.</span><span class="sxs-lookup"><span data-stu-id="77a08-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="77a08-105">Vous devez disposer d'un compte valide avec [!INCLUDE[prodshort](includes/prodshort.md)] et avec Power BI.</span><span class="sxs-lookup"><span data-stu-id="77a08-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="77a08-106">Vous devez également télécharger [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span><span class="sxs-lookup"><span data-stu-id="77a08-106">You must also download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span></span> <span data-ttu-id="77a08-107">Pour plus d'informations, voir [Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="77a08-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="77a08-108">Pour ajouter [!INCLUDE[prodshort](includes/prodshort.md)] comme source de données dans Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="77a08-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="77a08-109">Dans Power BI Desktop, dans le volet de navigation de gauche, choisissez **Extraire les données**.</span><span class="sxs-lookup"><span data-stu-id="77a08-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="77a08-110">Sur la page **Extraire les données**, choisissez **Services en ligne**, **Microsoft Dynamics 365 Business Central**, puis cliquez sur le bouton **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="77a08-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="77a08-111">Power BI affiche un assistant qui va vous guider tout au long du processus de connexion, notamment à [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="77a08-111">Power BI displays a wizard that will guide you through the connection process, including signing into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="77a08-112">Choisissez **Se connecter**, puis le compte approprié.</span><span class="sxs-lookup"><span data-stu-id="77a08-112">Choose **Sign in**, and then choose the relevant account.</span></span> <span data-ttu-id="77a08-113">Utilisez le même compte que celui avec lequel vous vous êtes connecté(e) à [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="77a08-113">Use the same account that you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="77a08-114">Cliquez sur le bouton **Connexion** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="77a08-114">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="77a08-115">L'assistant Power BI affiche la liste des sociétés, des environnements et des sources de données Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="77a08-115">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] environments, companies, and data sources.</span></span> <span data-ttu-id="77a08-116">Ces sources de données représentent tous les services web que vous avez publiés à partir de [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="77a08-116">These data sources represent all the web services that you have published from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

    <span data-ttu-id="77a08-117">Vous pouvez également créer une nouvelle URL de service web dans [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="77a08-117">You can also create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] instead.</span></span> <span data-ttu-id="77a08-118">Choisissez l'une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="77a08-118">Choose one of the following methods:</span></span>

      - <span data-ttu-id="77a08-119">Utiliser l'action **Créer un ensemble de données** sur la page **Services web**</span><span class="sxs-lookup"><span data-stu-id="77a08-119">Use the **Create Data Set** action on the **Web Services** page</span></span>
      - <span data-ttu-id="77a08-120">Utiliser le guide de configuration assistée **Configurer la création d'états**</span><span class="sxs-lookup"><span data-stu-id="77a08-120">Use the **Set Up Reporting** Assisted Setup guide</span></span>
      - <span data-ttu-id="77a08-121">Choisir l'action **Modifier dans Excel** dans toutes les listes</span><span class="sxs-lookup"><span data-stu-id="77a08-121">Choose the **Edit in Excel** action in any lists</span></span>

5. <span data-ttu-id="77a08-122">Spécifiez les données à ajouter à votre modèle de données, puis sélectionnez le bouton **Charge**.</span><span class="sxs-lookup"><span data-stu-id="77a08-122">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
6. <span data-ttu-id="77a08-123">Répétez les étapes précédentes pour ajouter des informations [!INCLUDE [prodshort](includes/prodshort.md)] supplémentaires, ou d'autres données, à votre modèle de données Power BI.</span><span class="sxs-lookup"><span data-stu-id="77a08-123">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="77a08-124">Une fois que vous êtes connecté(e) à [!INCLUDE [prodshort](includes/prodshort.md)], vous n'êtes plus invité(e) à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="77a08-124">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="77a08-125">Une fois les données chargées, elles s'affichent dans le volet de navigation à droite dans la page.</span><span class="sxs-lookup"><span data-stu-id="77a08-125">Once the data is loaded, you can see it in the right navigation on the page.</span></span> <span data-ttu-id="77a08-126">Vous êtes connecté(e) à vos données [!INCLUDE [prodshort](includes/prodshort.md)] et vous pouvez commencer à générer votre état Power BI.</span><span class="sxs-lookup"><span data-stu-id="77a08-126">You have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data, and you can begin building your Power BI report.</span></span>  

<span data-ttu-id="77a08-127">Avant de générer votre état, il est préférable d'importer le fichier de thème [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="77a08-127">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="77a08-128">Le fichier de thème crée une palette de couleurs afin de pouvoir établir des états avec le même style de couleur que les applications [!INCLUDE [prodshort](includes/prodshort.md)] sans avoir à définir des couleurs personnalisées pour chaque visuel.</span><span class="sxs-lookup"><span data-stu-id="77a08-128">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="77a08-129">Pour plus d'informations, reportez-vous à la [documentation Power BI](/power-bi/consumer/).</span><span class="sxs-lookup"><span data-stu-id="77a08-129">For more information, see the [Power BI documentation](/power-bi/consumer/).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="77a08-130">Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="77a08-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="77a08-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77a08-131">See Also</span></span>

[<span data-ttu-id="77a08-132">Activation de vos données commerciales pour Power BI</span><span class="sxs-lookup"><span data-stu-id="77a08-132">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="77a08-133">Veille économique</span><span class="sxs-lookup"><span data-stu-id="77a08-133">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="77a08-134">Mise en route</span><span class="sxs-lookup"><span data-stu-id="77a08-134">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="77a08-135">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="77a08-135">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="77a08-136">[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="77a08-136">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="77a08-137">Finances</span><span class="sxs-lookup"><span data-stu-id="77a08-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="77a08-138">Démarrage rapide : Se connecter aux données dans Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="77a08-138">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
