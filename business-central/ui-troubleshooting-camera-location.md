---
title: 'Dépannage : accès à la caméra et à l’emplacement'
description: Cet article décrit comment résoudre les problèmes d’accès à la caméra et aux informations de localisation dans Business Central.
author: blrobl
ms.author: t-blrobl
ms.date: 10/01/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.openlocfilehash: a29b2ea19d812d60d2824c131e311c34d74612af
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760231"
---
# <a name="troubleshooting-accessing-camera-and-location"></a><span data-ttu-id="68c5d-103">Dépannage : accès à la caméra et à l’emplacement</span><span class="sxs-lookup"><span data-stu-id="68c5d-103">Troubleshooting: Accessing Camera and Location</span></span>

<span data-ttu-id="68c5d-104">Vous pouvez rencontrer des problèmes lorsque vous essayez d’accéder à la caméra et aux informations de localisation d’un appareil à partir de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="68c5d-104">You might come across some issues when trying to access the camera and location information of a device from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="68c5d-105">Vous pouvez trouver les causes possibles de ces problèmes et comment les contourner ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="68c5d-105">You can find the possible causes behind these problems and how to work around them listed below.</span></span>

## <a name="device-must-have-camera-and-location-capabilities"></a><span data-ttu-id="68c5d-106">L’appareil doit avoir des capacités de caméra et de localisation</span><span class="sxs-lookup"><span data-stu-id="68c5d-106">Device must have Camera and Location Capabilities</span></span>

<span data-ttu-id="68c5d-107">Afin d’accéder à la caméra ou à l’emplacement d’un utilisateur à partir d’un appareil, l’appareil doit avoir une caméra physique ou la capacité de récupérer les informations d’emplacement, respectivement.</span><span class="sxs-lookup"><span data-stu-id="68c5d-107">In order to access the camera or a user's location from a device, the device must have a physical camera or the capability to retrieve location information, respectively.</span></span>

<span data-ttu-id="68c5d-108">Si votre appareil possède des capacités de caméra et de localisation, mais que vous rencontrez toujours des problèmes, il est possible que certains pilotes nécessitent une mise à jour ou une réinstallation.</span><span class="sxs-lookup"><span data-stu-id="68c5d-108">If your device has camera and location capabilities but you still encounter problems, it is possible that some drivers need updating or reinstalling.</span></span> <span data-ttu-id="68c5d-109">Même si vous n’êtes pas sûr, nous vous recommandons toujours de mettre à jour le système d’exploitation, les pilotes et le navigateur de votre appareil vers la dernière version pour une expérience optimale.</span><span class="sxs-lookup"><span data-stu-id="68c5d-109">Even if you are unsure, we always recommend you update your device operating system, drivers, and browser to the latest version for the best experience.</span></span>

## <a name="access-permissions-not-enabled"></a><span data-ttu-id="68c5d-110">Autorisations d’accès non activées</span><span class="sxs-lookup"><span data-stu-id="68c5d-110">Access Permissions not Enabled</span></span>

<span data-ttu-id="68c5d-111">Vous devez autoriser l’accès général à la caméra et à l’emplacement depuis les paramètres de confidentialité de votre appareil et donner explicitement l’autorisation de [!INCLUDE[prod_short](includes/prod_short.md)] pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="68c5d-111">You must enable general access to camera and location from your device's privacy settings and explicitly give permission to  [!INCLUDE[prod_short](includes/prod_short.md)] to access them.</span></span> <span data-ttu-id="68c5d-112">Par exemple, pour voir ou modifier les autorisations pour un appareil fonctionnant sous Windows, accédez à **Paramètres**, choisissez **Confidentialité**, puis **Autorisations d’application**.</span><span class="sxs-lookup"><span data-stu-id="68c5d-112">For example, to see or change permissions for a device running on Windows, go to **Settings**, choose **Privacy**, and then **App permissions**.</span></span> 

<span data-ttu-id="68c5d-113">Pour les appareils mobiles, vous devez accorder des autorisations d’accès à la caméra et à l’emplacement à l’application mobile [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="68c5d-113">For mobile devices, you must give camera and location access permissions to the [!INCLUDE[prod_short](includes/prod_short.md)] Mobile App.</span></span> <span data-ttu-id="68c5d-114">Pour ce faire pour un appareil iOS, accédez à **Paramètres**, choisissez **Confidentialité**, puis **Caméra** ou **Emplacement**.</span><span class="sxs-lookup"><span data-stu-id="68c5d-114">To do so for an iOS device, go to **Settings**, choose **Privacy**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="68c5d-115">Pour les appareils Android, accédez à **Paramètres**, choisissez **Applications et notifications**, **Avancée**, **Gestionnaire des autorisations**, puis **Caméra** ou **Emplacement**.</span><span class="sxs-lookup"><span data-stu-id="68c5d-115">For Android devices go to **Settings**, choose **Apps & Notifications**, **Advanced**, **Permission Manager**, and then **Camera** or **Location**.</span></span>

<span data-ttu-id="68c5d-116">De plus, si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] dans un navigateur, vous devez également accorder l’autorisation du site [!INCLUDE[prod_short](includes/prod_short.md)] pour accéder à la caméra ou aux informations de localisation.</span><span class="sxs-lookup"><span data-stu-id="68c5d-116">In addition, if you are using [!INCLUDE[prod_short](includes/prod_short.md)] in a browser, you must also grant the [!INCLUDE[prod_short](includes/prod_short.md)] site permission to access the camera or location information.</span></span> <span data-ttu-id="68c5d-117">Pour voir ou modifier les autorisations d’un site dans le navigateur Microsoft Edge, allez à **Paramètres**, choisissez **Autorisations de site**, puis **Caméra** ou **Emplacement**.</span><span class="sxs-lookup"><span data-stu-id="68c5d-117">To see or change a site's permissions in the Microsoft Edge browser, go to **Settings**, choose **Site Permissions**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="68c5d-118">Notez que cela peut être différent pour d’autres navigateurs.</span><span class="sxs-lookup"><span data-stu-id="68c5d-118">Note that this might be different for other browsers.</span></span>

<span data-ttu-id="68c5d-119">Par défaut, l’appareil ou le navigateur affichera une demande d’accès à ces fonctionnalités lorsque l’utilisateur les activera pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="68c5d-119">By default, the device or browser will pop up a request to access these capabilities when the user activates them for the first time.</span></span>

> [!NOTE]  
> <span data-ttu-id="68c5d-120">Certains anciens navigateurs n’accordent pas l’accès à la caméra et à l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="68c5d-120">Some old browsers do not grant access to camera and location.</span></span> <span data-ttu-id="68c5d-121">Par exemple, l’appareil photo n’est pas disponible dans le navigateur Internet Explorer ou Edge hérité.</span><span class="sxs-lookup"><span data-stu-id="68c5d-121">For example, camera is not available in Internet Explorer or the legacy Edge browser.</span></span>

## <a name="web-client-connection-not-secure"></a><span data-ttu-id="68c5d-122">Connexion client Web non sécurisée</span><span class="sxs-lookup"><span data-stu-id="68c5d-122">Web Client Connection not Secure</span></span>

<span data-ttu-id="68c5d-123">Les fonctionnalités de caméra et de localisation ne sont disponibles que lors de l’accès au client Web via des connexions HTTP sécurisées SSL, à l’aide du Schéma d’URI `https://`.</span><span class="sxs-lookup"><span data-stu-id="68c5d-123">The camera and location capabilities are only available when accessing the Web Client through SSL secured HTTP connections, using the `https://` URI scheme.</span></span> 

<span data-ttu-id="68c5d-124">La seule exception est la connexion à `http://localhost`, utilisé à des fins de développement et de test.</span><span class="sxs-lookup"><span data-stu-id="68c5d-124">The only exception is connecting to `http://localhost`, used for development and test purposes.</span></span>


## <a name="working-with-virtualization-technologies"></a><span data-ttu-id="68c5d-125">Utilisation des technologies de virtualisation</span><span class="sxs-lookup"><span data-stu-id="68c5d-125">Working with Virtualization Technologies</span></span>

<span data-ttu-id="68c5d-126">Lors de la connexion à [!INCLUDE[prod_short](includes/prod_short.md)] via Remote Desktop ou une autre virtualisation, l’accès à la caméra ou à l’emplacement peut ne pas être disponible.</span><span class="sxs-lookup"><span data-stu-id="68c5d-126">When connecting to [!INCLUDE[prod_short](includes/prod_short.md)] through Remote Desktop or another virtualization, the access to camera or location might not be available.</span></span> <span data-ttu-id="68c5d-127">Si tel est le cas, utilisez plutôt le système physique.</span><span class="sxs-lookup"><span data-stu-id="68c5d-127">If this is the case, use the physical system instead.</span></span>

## <a name="antivirus-software"></a><span data-ttu-id="68c5d-128">Logiciel antivirus</span><span class="sxs-lookup"><span data-stu-id="68c5d-128">Antivirus Software</span></span>
<span data-ttu-id="68c5d-129">Certains logiciels antivirus bloquent l’accès à la caméra et à l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="68c5d-129">Some antivirus software block access to camera and location by default.</span></span> <span data-ttu-id="68c5d-130">N’oubliez pas de vérifier les paramètres de votre logiciel antivirus.</span><span class="sxs-lookup"><span data-stu-id="68c5d-130">Remember to check your antivirus software settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="68c5d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68c5d-131">See Also</span></span>
[<span data-ttu-id="68c5d-132">Implémentation de la caméra dans AL</span><span class="sxs-lookup"><span data-stu-id="68c5d-132">Implementing the Camera in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[<span data-ttu-id="68c5d-133">Implémentation de l’emplacement dans AL</span><span class="sxs-lookup"><span data-stu-id="68c5d-133">Implementing the Location in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)
