---
title: Paramétrage de votre navigateur
description: Décrit comment configurer les navigateurs pour qu’ils fonctionnent avec Business Central et les produits qui y sont intégrés.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 01/08/2021
ms.author: jswymer
ms.openlocfilehash: b5083735be31b635cb3fc3ce404e7f182d04640f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384989"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><span data-ttu-id="446eb-103">Configuration et dépannage de votre navigateur pour qu’il fonctionne avec le client Web Business Central</span><span class="sxs-lookup"><span data-stu-id="446eb-103">Setting Up and Troubleshooting Your Browser to Work With Business Central Web Client</span></span>

<span data-ttu-id="446eb-104">Cet article explique comment configurer votre navigateur pour que le [!INCLUDE[web_client](includes/web_client.md)] et toutes ses fonctionnalités fonctionnent correctement.</span><span class="sxs-lookup"><span data-stu-id="446eb-104">This article explains how to set up your browser so that the [!INCLUDE[web_client](includes/web_client.md)] and all its features work properly.</span></span> <span data-ttu-id="446eb-105">Lisez cet article si vous rencontrez des problèmes pour ouvrir le [!INCLUDE[web_client](includes/web_client.md)], car certains problèmes peuvent être causés par les paramètres de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="446eb-105">Read this article if you're having problems opening the [!INCLUDE[web_client](includes/web_client.md)], because some problems may be caused by your browser's settings.</span></span>

<span data-ttu-id="446eb-106">L’article fournit des détails sur la configuration Microsoft Edge, mais les exigences pour JavaScript, les cookies et les fenêtres contextuelles sont les mêmes pour tous les navigateurs pris en charge.</span><span class="sxs-lookup"><span data-stu-id="446eb-106">The article provides details for setting up Microsoft Edge, but the requirements for JavaScript, cookies, and pop-ups are the same for all supported browsers.</span></span> <span data-ttu-id="446eb-107">Pour les autres navigateurs, reportez-vous aux instructions fournies par le fabricant.</span><span class="sxs-lookup"><span data-stu-id="446eb-107">For other browsers, refer to the instructions provided by the manufacturer.</span></span>  

## <a name="use-a-supported-browser"></a><span data-ttu-id="446eb-108">Utiliser un navigateur compatible</span><span class="sxs-lookup"><span data-stu-id="446eb-108">Use a supported browser</span></span>

<span data-ttu-id="446eb-109">Assurez-vous d’utiliser l’un des navigateurs pris en charge.</span><span class="sxs-lookup"><span data-stu-id="446eb-109">Make sure to use a one of the supported browsers.</span></span> <span data-ttu-id="446eb-110">Voir [Configuration minimale requise pour l’utilisation de Business Central](product-requirements.md#recommended-browsers).</span><span class="sxs-lookup"><span data-stu-id="446eb-110">See [Minimum Requirements for Using Business Central](product-requirements.md#recommended-browsers).</span></span>  

## <a name="allow-javascript-from-business-central"></a><span data-ttu-id="446eb-111">Autoriser JavaScript depuis Business Central</span><span class="sxs-lookup"><span data-stu-id="446eb-111">Allow JavaScript from Business Central</span></span>

<span data-ttu-id="446eb-112">*Problème :*</span><span class="sxs-lookup"><span data-stu-id="446eb-112">*Problem:*</span></span>

<span data-ttu-id="446eb-113">Si le navigateur n’autorise pas JavaScript, vous verrez **NotSupported/DisabledJavaScript** dans la barre d’adresse et un message **HTTP 404.0 - Not Found** lorsque vous essayez d’ouvrir [!INCLUDE[prod_short](includes/prod_short.md)], et le</span><span class="sxs-lookup"><span data-stu-id="446eb-113">If the browser doesn't allow JavaScript, you'll see **NotSupported/DisabledJavaScript** in the address bar and an **HTTP Error 404.0 - Not Found** message when you try to open [!INCLUDE[prod_short](includes/prod_short.md)], and the</span></span> 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

<span data-ttu-id="446eb-114">*Correctif :*</span><span class="sxs-lookup"><span data-stu-id="446eb-114">*Fix:*</span></span>

1. <span data-ttu-id="446eb-115">Dans Microsoft Edge, accédez à **Paramètres** > **Cookies et autorisations du site** > **JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="446eb-115">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **JavaScript**.</span></span>
2. <span data-ttu-id="446eb-116">Exécutez l’une des étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="446eb-116">Do one of the following steps.</span></span> <span data-ttu-id="446eb-117">Choisissez l’étape recommandée par votre organisation :</span><span class="sxs-lookup"><span data-stu-id="446eb-117">Choose the step that is recommended by your organization:</span></span>

    - <span data-ttu-id="446eb-118">Déplacez le bouton bascule **Autorisé** vers la gauche (désactivé).</span><span class="sxs-lookup"><span data-stu-id="446eb-118">Move the **Allowed** toggle to the left (Off).</span></span> <span data-ttu-id="446eb-119">Puis, sélectionnez **Ajouter** et saisissez l’adresse (URL) pour [!INCLUDE[prod_short](includes/prod_short.md)] dans la zone **Site**.</span><span class="sxs-lookup"><span data-stu-id="446eb-119">Then, select **Add** and type the address (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] in the **Site** box.</span></span> <span data-ttu-id="446eb-120">Sélectionnez **Ajouter** lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="446eb-120">Select **Add** when done.</span></span>
    - <span data-ttu-id="446eb-121">Déplacez le bouton bascule **Autorisé** vers la droite (activé).</span><span class="sxs-lookup"><span data-stu-id="446eb-121">Move the **Allowed** toggle to the right (On).</span></span>

## <a name="allow-cookies-from-business-central"></a><span data-ttu-id="446eb-122">Autoriser les cookies depuis Business Central</span><span class="sxs-lookup"><span data-stu-id="446eb-122">Allow cookies from Business Central</span></span>

<span data-ttu-id="446eb-123">*Problème :*</span><span class="sxs-lookup"><span data-stu-id="446eb-123">*Problem:*</span></span>

<span data-ttu-id="446eb-124">Si le navigateur n’autorise pas les cookies, vous obtiendrez l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="446eb-124">If the browser doesn't allow cookies, you'll get the following error:</span></span>

<span data-ttu-id="446eb-125">**Désolé, la page est introuvable. Veuillez vérifier l’adresse et réessayer.**</span><span class="sxs-lookup"><span data-stu-id="446eb-125">**Sorry, the page could not be found. Please check the address and try again.**</span></span> 

<span data-ttu-id="446eb-126">*Correctif :*</span><span class="sxs-lookup"><span data-stu-id="446eb-126">*Fix:*</span></span>

1. <span data-ttu-id="446eb-127">Dans Microsoft Edge, accédez à **Réglages** > **Cookies et autorisations du site** > **Cookies et données de site**.</span><span class="sxs-lookup"><span data-stu-id="446eb-127">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.</span></span>
2. <span data-ttu-id="446eb-128">Déplacez le bouton bascule **Autoriser les sites à enregistrer et lire les données des cookies** vers la droite (activé).</span><span class="sxs-lookup"><span data-stu-id="446eb-128">Move the **Allow sites to save and read cookie data** toggle to the right (On).</span></span>  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a><span data-ttu-id="446eb-129">Autoriser les fenêtres contextuelles depuis Business Central</span><span class="sxs-lookup"><span data-stu-id="446eb-129">Allow pop-ups from Business Central</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="446eb-130">s’intègre à plusieurs produits.</span><span class="sxs-lookup"><span data-stu-id="446eb-130">integrates with several products.</span></span> <span data-ttu-id="446eb-131">Dans certains cas, comme avec Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] s’ouvre, ou « ouvre une fenêtre contextuelle » dans le produit.</span><span class="sxs-lookup"><span data-stu-id="446eb-131">In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product.</span></span> <span data-ttu-id="446eb-132">Cette fonctionnalité nécessite que votre navigateur autorise les fenêtres contextuelles de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="446eb-132">This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="446eb-133">*Problème :*</span><span class="sxs-lookup"><span data-stu-id="446eb-133">*Problem:*</span></span>

<span data-ttu-id="446eb-134">Si des fenêtres contextuelles pour [!INCLUDE[prod_short](includes/prod_short.md)] sont bloquées, vous recevez un message similaire au message suivant :</span><span class="sxs-lookup"><span data-stu-id="446eb-134">If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:</span></span>

<span data-ttu-id="446eb-135">**Un problème est survenu. Votre navigateur bloque peut-être les fenêtres contextuelles nécessaires à Business Central.**</span><span class="sxs-lookup"><span data-stu-id="446eb-135">**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**</span></span>

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
<span data-ttu-id="446eb-136">*Correctif :*</span><span class="sxs-lookup"><span data-stu-id="446eb-136">*Fix:*</span></span>

1. <span data-ttu-id="446eb-137">Dans Microsoft Edge, accédez à **Paramètres** > **Cookies et autorisations du site** > **Fenêtres contextuelles et redirections**.</span><span class="sxs-lookup"><span data-stu-id="446eb-137">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.</span></span>
2. <span data-ttu-id="446eb-138">Déplacez le bouton bascule **Bloqué** vers la droite (activé).</span><span class="sxs-lookup"><span data-stu-id="446eb-138">Move the **Blocked** toggle to the right (On).</span></span>
3. <span data-ttu-id="446eb-139">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="446eb-139">Select **Add**.</span></span> <span data-ttu-id="446eb-140">Dans la zone **Site**, saisissez `https://businesscentral.dynamics.com`, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="446eb-140">In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="446eb-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="446eb-141">See Also</span></span>

[<span data-ttu-id="446eb-142">Résolution des incidents dans Teams</span><span class="sxs-lookup"><span data-stu-id="446eb-142">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]