---
title: Utiliser Invoicing et Finance and Operations, Business edition | Microsoft Docs
description: "Solution de contournement pour accéder à Microsoft Invoicing lorsque vous vous êtes inscrit à Dynamics 365 for Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 803569ed99f00b9055c5a6ec6e4ffae67d9df2bd
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a><span data-ttu-id="7b1ae-103">Utilisation du même compte Office 365 dans [!INCLUDE[d365fin](includes/d365fin_long_md.md)] et Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="7b1ae-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="7b1ae-104">Lorsque vous êtes inscrit à une version d'évaluation avec [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez passer à une phase d'évaluation de 30 jours, démarrer un abonnement ou encore l'arrêter à l'aide de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7b1ae-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7b1ae-105">Dans tous les cas, si vous vous connectez au portail Office, vous verrez une vignette intitulée **Centre d'affaires** sur laquelle vous pouvez cliquer.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-105">In all cases, if you log into the Office Portal, you might see a tile called **Business center** and click it.</span></span> <span data-ttu-id="7b1ae-106">Cela fait partie de l'abonnement Office 365 Business Premium, tous les utilisateurs ne verront donc pas cette vignette dans le portail Office.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="7b1ae-107">Si vous accédez au centre d'affaires, vous verrez une section intitulée **Invoicing**.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-107">If you do access the Business center, you will see a section called **Invoicing**.</span></span> <span data-ttu-id="7b1ae-108">Si vous accédez à cette section, vous verrez un message indiquant que vous ne pouvez pas accéder à Microsoft Invoicing car votre compte est utilisé dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7b1ae-108">If you access that section, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="7b1ae-109">Un message similaire s'affiche si vous installez l'application mobile pour Invoicing.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-109">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="7b1ae-110">Solution de contournement</span><span class="sxs-lookup"><span data-stu-id="7b1ae-110">Workaround</span></span>
<span data-ttu-id="7b1ae-111">Invoicing et [!INCLUDE[d365fin](includes/d365fin_md.md)] ont une plate-forme partagée.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-111">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="7b1ae-112">Cela signifie que vous êtes reconnu en tant qu'utilisateur existant de [!INCLUDE[d365fin](includes/d365fin_md.md)] lorsque vous cliquez sur Invoicing dans le centre d'affaires.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-112">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Business center.</span></span> <span data-ttu-id="7b1ae-113">Invoicing ne peut pas utiliser la même société que [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7b1ae-113">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="7b1ae-114">Vous devrez donc vous connecter à [!INCLUDE[d365fin](includes/d365fin_md.md)] et renommer votre société existante, puis créer une nouvelle société que vous pourrez alors utiliser dans Invoicing.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-114">So you will have to log into [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="7b1ae-115">Aucune donnée n'est déplacée ou remplacée au cours de cette opération.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-115">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="7b1ae-116">Pour renommer votre société</span><span class="sxs-lookup"><span data-stu-id="7b1ae-116">To rename your company</span></span>
1.  <span data-ttu-id="7b1ae-117">Connectez-vous à [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7b1ae-117">Sign in to your [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
2.  <span data-ttu-id="7b1ae-118">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Sociétés**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Companies**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="7b1ae-119">Dans la fenêtre **Sociétés**, sélectionnez le bouton **Modifier la liste**.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-119">In the **Companies** window, choose the **Edit List** button.</span></span>  
4.  <span data-ttu-id="7b1ae-120">Remplacez le nom de l'entrée *Ma société* par un autre nom.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-120">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="7b1ae-121">Patientez quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-121">Wait a number of minutes.</span></span> <span data-ttu-id="7b1ae-122">Nous apporterons plusieurs modifications à la base de données sous-jacente, et cette opération prendra un certain temps.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-122">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
5.  <span data-ttu-id="7b1ae-123">Lorsque le système est à nouveau prêt, sélectionnez le bouton **Créer une nouvelle société**.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-123">When the system is ready again, choose the **Create New Company** button.</span></span>  
6.  <span data-ttu-id="7b1ae-124">Dans la boîte de dialogue qui s'affiche, entrez *Ma société* comme nom et sélectionnez l'option **Production - Données de configuration uniquement**.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-124">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="7b1ae-125">Cette opération prend plusieurs minutes.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-125">This again takes a number of minutes.</span></span> <span data-ttu-id="7b1ae-126">Lorsque le processus est terminé, vous pouvez accéder à Invoicing dans le cadre de votre expérience Office 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-126">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="7b1ae-127">Qu'en est-il de mes données ?</span><span class="sxs-lookup"><span data-stu-id="7b1ae-127">What about my data?</span></span>
<span data-ttu-id="7b1ae-128">Lorsque vous renommez la société d'origine, les tables de la base de données qui stockent vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] existantes sont renommées, mais les données proprement dites sont conservées.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-128">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="7b1ae-129">Si vous utilisez Invoicing et [!INCLUDE[d365fin](includes/d365fin_md.md)], les données sont stockées dans deux conteneurs différents (les deux sociétés).</span><span class="sxs-lookup"><span data-stu-id="7b1ae-129">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="7b1ae-130">Aucun donnée n'est partagée, vous devrez donc gérer les clients et les articles dans les deux sociétés.</span><span class="sxs-lookup"><span data-stu-id="7b1ae-130">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7b1ae-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b1ae-131">See Also</span></span>
[<span data-ttu-id="7b1ae-132">Forum Aux Questions</span><span class="sxs-lookup"><span data-stu-id="7b1ae-132">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="7b1ae-133">Configuration et administration</span><span class="sxs-lookup"><span data-stu-id="7b1ae-133">Setup and Administration</span></span>](admin-setup-and-administration.md)  

