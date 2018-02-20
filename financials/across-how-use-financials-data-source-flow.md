---
title: "Connecter vos données avec Flow| Microsoft Docs"
description: "Vous pouvez rendre vos données Financials disponibles sous forme de données sources et spécifier une URL OData de vos services Web pour générer un flux de travail automatisé."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="2dca5-103">Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans un flux automatisé</span><span class="sxs-lookup"><span data-stu-id="2dca5-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="2dca5-104">Vous pouvez utiliser vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant que partie du flux de travail dans Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="2dca5-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="2dca5-105">Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Flow.</span><span class="sxs-lookup"><span data-stu-id="2dca5-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="2dca5-106">Pour ajouter [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données dans Flow</span><span class="sxs-lookup"><span data-stu-id="2dca5-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="2dca5-107">Dans votre navigateur, accédez à [flow.microsoft.com](https://flow.microsoft.com/en-us/), puis connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="2dca5-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="2dca5-108">Choisissez **Mes flux** dans le ruban en haut de la page.</span><span class="sxs-lookup"><span data-stu-id="2dca5-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="2dca5-109">Dans la fenêtre **Mes flux**, cliquez sur l'option **Créer à partir de rien**.</span><span class="sxs-lookup"><span data-stu-id="2dca5-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="2dca5-110">Dans la liste des déclencheurs disponibles, sélectionnez l'un des déclencheurs [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles :</span><span class="sxs-lookup"><span data-stu-id="2dca5-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="2dca5-111">*Lorsqu'un enregistrement est créé*,</span><span class="sxs-lookup"><span data-stu-id="2dca5-111">*When a record is created*,</span></span>  
    <span data-ttu-id="2dca5-112">*Lors de la suppression d'un enregistrement*,</span><span class="sxs-lookup"><span data-stu-id="2dca5-112">*When a record is deleted*,</span></span>  
    <span data-ttu-id="2dca5-113">*Lorsqu'un enregistrement est modifié*,</span><span class="sxs-lookup"><span data-stu-id="2dca5-113">*When a record is modified*,</span></span>  
    <span data-ttu-id="2dca5-114">*Lorsque l'approbation d'un client est exigée*,</span><span class="sxs-lookup"><span data-stu-id="2dca5-114">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="2dca5-115">*Lorsque l'approbation d'un nom feuille comptabilité est exigée*,</span><span class="sxs-lookup"><span data-stu-id="2dca5-115">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="2dca5-116">*Lorsque l'approbation d'une ligne feuille comptabilité est exigée*,</span><span class="sxs-lookup"><span data-stu-id="2dca5-116">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="2dca5-117">*Lorsque l'approbation d'un article est exigée*,</span><span class="sxs-lookup"><span data-stu-id="2dca5-117">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="2dca5-118">*Lorsque l'approbation d'un document achat est exigée*,</span><span class="sxs-lookup"><span data-stu-id="2dca5-118">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="2dca5-119">*Lorsque l'approbation d'un document vente est exigée*, ou</span><span class="sxs-lookup"><span data-stu-id="2dca5-119">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="2dca5-120">*Lorsque l'approbation d'un fournisseur est exigée*.</span><span class="sxs-lookup"><span data-stu-id="2dca5-120">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="2dca5-121">Le flux affiche vous invite à fournir les informations nécessaires pour vous connecter à vos données [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2dca5-121">Flow will prompt you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="2dca5-122">Si vous avez sélectionné l'un des déclencheurs suivants : *Lorsqu'un enregistrement est créé*, *Lorsqu'un enregistrement est modifié* ou *Lors de la suppression d'un enregistrement*, vous devez sélectionner un nom de société et un nom de table.</span><span class="sxs-lookup"><span data-stu-id="2dca5-122">If you selected one of the following triggers: *When a record is created*, *When a record is modified*, or *When a record is deleted*, you must select a company name and table name.</span></span> <span data-ttu-id="2dca5-123">Avec un autre déclencheur, seul le nom de la société est nécessaire pour se connecter.</span><span class="sxs-lookup"><span data-stu-id="2dca5-123">With any other trigger, only the company name is required to connect.</span></span>

   <span data-ttu-id="2dca5-124">Flow affiche la liste des sociétés et des tables disponibles à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2dca5-124">Flow will show a list of companies and tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2dca5-125">Ces tables, ou points de terminaison, représentent tous les services Web que vous avez publiés à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2dca5-125">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="2dca5-126">Sinon, créer une nouvelle URL de service Web dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide de l'option **Créer un ensemble de données** de la page **Services Web**, à l'aide du guide de configuration assistée **Configurer la création d'états** ou en choisissant l'option **Modifier dans Excel** dans n'importe quelle liste.</span><span class="sxs-lookup"><span data-stu-id="2dca5-126">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>

<span data-ttu-id="2dca5-127">À ce stade, vous êtes connecté à vos données Finance and Operations, Business edition et vous êtes prêt à générer votre flux.</span><span class="sxs-lookup"><span data-stu-id="2dca5-127">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="2dca5-128">Pour plus d'informations, voir [Documentation Flow](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="2dca5-128">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="2dca5-129">Pour résoudre les problèmes avec Microsoft Flow, voir [Résolution des problèmes : Intégration à Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="2dca5-129">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2dca5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2dca5-130">See Also</span></span>
<span data-ttu-id="2dca5-131">[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="2dca5-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="2dca5-132">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="2dca5-132">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="2dca5-133">[Gérer les utilisateurs et les autorisations](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="2dca5-133">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="2dca5-134">[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="2dca5-134">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="2dca5-135">Finances</span><span class="sxs-lookup"><span data-stu-id="2dca5-135">Finance</span></span>](finance.md)  

