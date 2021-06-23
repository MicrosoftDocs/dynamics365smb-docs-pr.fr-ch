---
title: Optimisation d’Outlook pour votre boîte de réception professionnelle
description: Découvrez ce que vous pouvez faire pour améliorer l’expérience avec la boîte de réception professionnelle dans Microsoft Outlook.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in
ms.date: 05/12/2021
ms.author: jswymer
ms.openlocfilehash: 2fee1782057d0f45319e4d12d715c2e1e0d3d4a6
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/19/2021
ms.locfileid: "6064871"
---
# <a name="optimizing-outlook-for-your-business-inbox"></a><span data-ttu-id="88ff8-103">Optimisation d’Outlook pour votre boîte de réception professionnelle</span><span class="sxs-lookup"><span data-stu-id="88ff8-103">Optimizing Outlook for Your Business Inbox</span></span> 

<span data-ttu-id="88ff8-104">Cet article traite de ce que vous pouvez faire pour obtenir la meilleure expérience possible avec la boîte de réception professionnelle dans Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="88ff8-104">This article discusses things you can do to get the best possible experience with the Business Inbox in Microsoft Outlook.</span></span> 

## <a name="update-outlook"></a><span data-ttu-id="88ff8-105">Mettre à jour Outlook</span><span class="sxs-lookup"><span data-stu-id="88ff8-105">Update Outlook</span></span>

<span data-ttu-id="88ff8-106">Effectuez une mise à jour vers Outlook version 2012 ou une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="88ff8-106">Update to Outlook version 2012 or newer.</span></span>

> [!NOTE]
> <span data-ttu-id="88ff8-107">Si vous ne pouvez pas mettre à jour Outlook vers la version 2012 ou vers une version ultérieure, assurez-vous au moins de mettre à jour vers la version 1905.</span><span class="sxs-lookup"><span data-stu-id="88ff8-107">If you are unable to update Outlook to version 2012 or later, make sure that you at least update to version 1905.</span></span> <span data-ttu-id="88ff8-108">Cela empêche le complément Outlook de s’exécuter en utilisant les composants Internet Explorer hérités</span><span class="sxs-lookup"><span data-stu-id="88ff8-108">This prevents the Outlook Add-in from running using legacy Internet Explorer components</span></span>

### <a name="how-to-check-your-version-of-outlook"></a><span data-ttu-id="88ff8-109">Comment vérifier votre version d’Outlook</span><span class="sxs-lookup"><span data-stu-id="88ff8-109">How to check your version of Outlook</span></span>

<span data-ttu-id="88ff8-110">Que vous utilisiez Office 2019 ou Microsoft 365, suivez ce guide de support Microsoft pour vérifier votre version d’Outlook :</span><span class="sxs-lookup"><span data-stu-id="88ff8-110">Whether you use Office 2019 or Microsoft 365, follow this Microsoft Support guide to check which version of Outlook you have:</span></span>  

[<span data-ttu-id="88ff8-111">À propos d’Office : quelle version d’Office est-ce que j’utilise ?</span><span class="sxs-lookup"><span data-stu-id="88ff8-111">About Office: What version of Office am I using?</span></span>](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### <a name="how-to-update-outlook"></a><span data-ttu-id="88ff8-112">Comment mettre à jour Outlook</span><span class="sxs-lookup"><span data-stu-id="88ff8-112">How to update Outlook</span></span>

<span data-ttu-id="88ff8-113">Pour mettre à jour Outlook vers la dernière version, suivez ce guide de support Microsoft ou contactez votre administrateur :</span><span class="sxs-lookup"><span data-stu-id="88ff8-113">To update Outlook to the latest version, follow this Microsoft Support guide or contact your administrator:</span></span>

[<span data-ttu-id="88ff8-114">Installer les mises à jour Office</span><span class="sxs-lookup"><span data-stu-id="88ff8-114">Install Office updates</span></span>](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## <a name="install-microsoft-edge-webview2"></a><span data-ttu-id="88ff8-115">Installer Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="88ff8-115">Install Microsoft Edge WebView2</span></span>

<span data-ttu-id="88ff8-116">Assurez-vous que Microsoft Edge WebView2 est installé sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="88ff8-116">Ensure that Microsoft Edge WebView2 is installed on your device.</span></span>

### <a name="how-to-check-if-microsoft-edge-webview2-is-installed"></a><span data-ttu-id="88ff8-117">Comment vérifier si Microsoft Edge WebView2 est installé</span><span class="sxs-lookup"><span data-stu-id="88ff8-117">How to check if Microsoft Edge WebView2 is installed</span></span> 

<span data-ttu-id="88ff8-118">Pour vérifier si Microsoft Edge WebView2 est installé sur un ordinateur, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="88ff8-118">To check if you have Microsoft Edge WebView2 installed on a computer, do the following steps:</span></span>

<span data-ttu-id="88ff8-119">Depuis le menu Démarrer :</span><span class="sxs-lookup"><span data-stu-id="88ff8-119">From Start menu:</span></span>

1. <span data-ttu-id="88ff8-120">Choississez **Démarrer** ![Démarrage de Windows](media/windows-start-icon.png "Icône de démarrage de Windows") > **Paramètres** ![Paramètres Windows](media/windows-settings-icon.png "Icône des paramètres Windows") > **Applications et fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="88ff8-120">Choose **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon") > **Settings** ![Windows Settings](media/windows-settings-icon.png "Windows Settings icon") > **Apps & Features**.</span></span>
2. <span data-ttu-id="88ff8-121">Dans la zone de recherche, tapez **WebView2**.</span><span class="sxs-lookup"><span data-stu-id="88ff8-121">In the search box, type **WebView2**.</span></span> <span data-ttu-id="88ff8-122">Si Microsoft Edge WebView2 est installé, vous verrez une entrée appelée **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="88ff8-122">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

<span data-ttu-id="88ff8-123">Depuis le Panneau de configuration :</span><span class="sxs-lookup"><span data-stu-id="88ff8-123">From Control Panel:</span></span>

1. <span data-ttu-id="88ff8-124">Dans la zone de recherche à côté de **Démarrer** ![Démarrage de Windows](media/windows-start-icon.png "Icône de démarrage de Windows"), tapez **Panneau de commande**, puis sélectionnez le résultat.</span><span class="sxs-lookup"><span data-stu-id="88ff8-124">In the search box next to **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon"), type **Control Panel**, and then select the result.</span></span>
2. <span data-ttu-id="88ff8-125">Choisissez **Programmes** > **Programmes et fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="88ff8-125">Choose **Programs** > **Programs and Features**.</span></span>
3. <span data-ttu-id="88ff8-126">Dans la zone de recherche, tapez **WebView2**.</span><span class="sxs-lookup"><span data-stu-id="88ff8-126">In the search box, type **WebView2**.</span></span> <span data-ttu-id="88ff8-127">Si Microsoft Edge WebView2 est installé, vous verrez une entrée appelée **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="88ff8-127">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

### <a name="how-to-install-microsoft-edge-webview2"></a><span data-ttu-id="88ff8-128">Comment installer Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="88ff8-128">How to install Microsoft Edge WebView2</span></span> 

1. <span data-ttu-id="88ff8-129">À l’aide de votre navigateur, accédez à [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span><span class="sxs-lookup"><span data-stu-id="88ff8-129">Using your browser, go to [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span></span>
2. <span data-ttu-id="88ff8-130">Choisissez **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="88ff8-130">Choose **Download**.</span></span>
3. <span data-ttu-id="88ff8-131">Paramétrez **Sélectionner l’architecture** de manière à correspondre à votre système.</span><span class="sxs-lookup"><span data-stu-id="88ff8-131">Set **Select Architecture** to match your system.</span></span>
4. <span data-ttu-id="88ff8-132">Choisissez **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="88ff8-132">Choose **Download**.</span></span>

> [!NOTE]
> <span data-ttu-id="88ff8-133">Votre organisation peut avoir des restrictions sur les composants pouvant être installés sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="88ff8-133">Your organization may have restriction on which components can be installed on your device.</span></span> <span data-ttu-id="88ff8-134">Contactez votre administrateur pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="88ff8-134">Contact your administrator for assistance.</span></span>

## <a name="use-a-supported-browser"></a><span data-ttu-id="88ff8-135">Utiliser un navigateur compatible</span><span class="sxs-lookup"><span data-stu-id="88ff8-135">Use a supported browser</span></span>

<span data-ttu-id="88ff8-136">Envisagez d’utiliser Outlook sur le web dans l’un des navigateurs pris en charge par Business Central.</span><span class="sxs-lookup"><span data-stu-id="88ff8-136">Consider using Outlook for the Web in one of the browsers supported by Business Central.</span></span> <span data-ttu-id="88ff8-137">Pour consulter la liste des navigateurs pris en charge, consultez [Configuration minimale requise pour l’utilisation de Business Central](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="88ff8-137">For a list of supported browsers, see [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>

## <a name="see-also"></a><span data-ttu-id="88ff8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88ff8-138">See Also</span></span>

[<span data-ttu-id="88ff8-139">Préparation aux activités commerciales</span><span class="sxs-lookup"><span data-stu-id="88ff8-139">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
[<span data-ttu-id="88ff8-140">Obtention de Business Central sur mon périphérique mobile</span><span class="sxs-lookup"><span data-stu-id="88ff8-140">Getting Business Central on my Mobile Device</span></span>](install-mobile-app.md)  
[<span data-ttu-id="88ff8-141">Envoyer des documents par e-mail</span><span class="sxs-lookup"><span data-stu-id="88ff8-141">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="88ff8-142">Finances</span><span class="sxs-lookup"><span data-stu-id="88ff8-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="88ff8-143">Ventes</span><span class="sxs-lookup"><span data-stu-id="88ff8-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="88ff8-144">Achats</span><span class="sxs-lookup"><span data-stu-id="88ff8-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="88ff8-145">Configuration minimale requise pour Outlook</span><span class="sxs-lookup"><span data-stu-id="88ff8-145">Minimum Requirements for Outlook</span></span>](product-requirements.md#outlook)  
[<span data-ttu-id="88ff8-146">Utilisation des compléments dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="88ff8-146">Using add-ins in Outlook on the web</span></span>](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]