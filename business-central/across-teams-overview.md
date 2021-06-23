---
title: Vue d’ensemble de l’intégration de Business Central et Microsoft Teams | Microsoft Docs
description: Partagez des enregistrements Business Central directement dans une conversation Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: 15a6f009095c2e20cf65d38503a7c737e64e7bb8
ms.sourcegitcommit: 5a916b0aa0a2eef0c22b5722a0af041757e6d7c2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/19/2021
ms.locfileid: "6074702"
---
# <a name="business-central-and-microsoft-teams-integration"></a><span data-ttu-id="7712b-103">Intégration de Business Central et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7712b-103">Business Central and Microsoft Teams Integration</span></span>

[!INCLUDE [online_only](includes/online_only.md)]

<span data-ttu-id="7712b-104">[Microsoft Teams](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams) est un produit Microsoft 365 qui vous permet de vous connecter aux autres, de collaborer facilement et de simplifier votre travail.</span><span class="sxs-lookup"><span data-stu-id="7712b-104">[Microsoft Teams](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams) is a Microsoft 365 product that lets you connect with others, collaborate seamlessly, and simplify work.</span></span> <span data-ttu-id="7712b-105">[!INCLUDE [prod_short](includes/prod_short.md)] propose une application qui connecte Microsoft Teams à vos données métier dans [!INCLUDE [prod_short](includes/prod_short.md)], afin que vous puissiez partager rapidement les détails entre les membres de l’équipe, rechercher des contacts et répondre plus rapidement aux demandes de renseignements.</span><span class="sxs-lookup"><span data-stu-id="7712b-105">[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)] so you can quickly share details across team members, look up contacts, and respond faster to inquiries.</span></span>

<span data-ttu-id="7712b-106">L’application est disponible sur le marché Teams et vous pouvez l’utiliser avec l’application de bureau, mobile ou web Teams.</span><span class="sxs-lookup"><span data-stu-id="7712b-106">The app is available on the Teams marketplace, and you can use it with the Teams desktop, mobile app, or web.</span></span>

## <a name="features-overview"></a><span data-ttu-id="7712b-107">Aperçu des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="7712b-107">Features overview</span></span>

<span data-ttu-id="7712b-108">L'application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams offre les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="7712b-108">The [!INCLUDE [prod_short](includes/prod_short.md)] app for Teams offers the following features.</span></span>

### <a name="look-up-details-of-customers-vendors-and-other-contacts"></a><span data-ttu-id="7712b-109">Rechercher les détails des clients, fournisseurs et autres contacts</span><span class="sxs-lookup"><span data-stu-id="7712b-109">Look up details of customers, vendors, and other contacts</span></span>

<span data-ttu-id="7712b-110">Où que vous soyez dans Teams, vous pouvez rechercher des détails sur les clients, les fournisseurs et autres contacts [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="7712b-110">No matter where you are in Teams, you can look up details about customers, vendors, and other [!INCLUDE [prod_short](includes/prod_short.md)] contacts.</span></span> <span data-ttu-id="7712b-111">Cette fonctionnalité vous permet non seulement d'afficher des informations générales sur les contacts, mais donne également accès à l'historique des interactions, aux documents associés, etc.</span><span class="sxs-lookup"><span data-stu-id="7712b-111">This feature not only lets you view general information about contacts, but also gives access to interaction history, related documents, and more.</span></span>

 <span data-ttu-id="7712b-112">[![Rechercher des contacts Business Central à partir de la boîte de commande Teams](media/teams-contacts-overview.png)](media/teams-contacts-overview.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="7712b-112">[![Look up Business Central contacts from Teams command box](media/teams-contacts-overview.png)](media/teams-contacts-overview.png#lightbox)</span></span>

<span data-ttu-id="7712b-113">Vous pouvez également partager des détails de contact dans une conversation.</span><span class="sxs-lookup"><span data-stu-id="7712b-113">You can also share contact details in a conversation.</span></span> <span data-ttu-id="7712b-114">De là, les participants ont également accès à encore plus de détails sur le contact.</span><span class="sxs-lookup"><span data-stu-id="7712b-114">From there, participants have access to even more details about the contact as well.</span></span>

 <span data-ttu-id="7712b-115">[![Rechercher des contacts Business Central à partir de la boîte de composition Teams](media/teams-contacts.png)](media/teams-contacts.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="7712b-115">[![Look up Business Central contacts from Teams compose box](media/teams-contacts.png)](media/teams-contacts.png#lightbox)</span></span>

<span data-ttu-id="7712b-116">Pour plus d’informations, reportez-vous à la [Recherche de doublons de contact dans Microsoft Teams](across-search-contacts-teams.md).</span><span class="sxs-lookup"><span data-stu-id="7712b-116">For more information, see [Searching for Contacts from Microsoft Teams](across-search-contacts-teams.md).</span></span>

### <a name="share-records-in-conversations"></a><span data-ttu-id="7712b-117">Partager des enregistrements dans les conversations</span><span class="sxs-lookup"><span data-stu-id="7712b-117">Share records in conversations</span></span>

<span data-ttu-id="7712b-118">Copier un lien vers n’importe quel enregistrement Business Central et le coller dans une conversation Teams à partager avec vos collègues.</span><span class="sxs-lookup"><span data-stu-id="7712b-118">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="7712b-119">L’application étendra le lien dans une carte interactive compacte qui affiche des informations sur l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="7712b-119">The app will then expand the link into a compact, interactive card that displays information about the record.</span></span>

<span data-ttu-id="7712b-120">[![Intégration Teams avec Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="7712b-120">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

<span data-ttu-id="7712b-121">Une fois dans la conversation, vous et vos collègues pouvez afficher plus de détails sur l’enregistrement, modifier les données et prendre des mesures, sans quitter Teams.</span><span class="sxs-lookup"><span data-stu-id="7712b-121">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action - without leaving Teams.</span></span>

<span data-ttu-id="7712b-122">Pour plus d’informations, consultez [Partager des enregistrements dans Microsoft Teams](across-working-with-teams.md).</span><span class="sxs-lookup"><span data-stu-id="7712b-122">For more information, see [Share Records in Microsoft Teams](across-working-with-teams.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="7712b-123">Démarrer</span><span class="sxs-lookup"><span data-stu-id="7712b-123">Get Started</span></span>

1. <span data-ttu-id="7712b-124">Un compte d'utilisateur [!INCLUDE [prod_short](includes/prod_short.md)] Online est requis pour l'application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams.</span><span class="sxs-lookup"><span data-stu-id="7712b-124">A [!INCLUDE [prod_short](includes/prod_short.md)] online user account is required for [!INCLUDE [prod_short](includes/prod_short.md)] app for Teams.</span></span>

    <span data-ttu-id="7712b-125">Si vous n’êtes pas certain de disposer d’un compte ou si vous ne connaissez pas vos informations d’identification pour vous connecter, contactez l’administrateur de votre société pour vous aider à commencer.</span><span class="sxs-lookup"><span data-stu-id="7712b-125">If you’re not sure whether you have an account, or if you don’t know your credentials for signing in, contact your company administrator to help you get started.</span></span>

    > [!TIP]
    > <span data-ttu-id="7712b-126">Si votre organisation n'a pas d'abonnement [!INCLUDE [prod_short](includes/prod_short.md)], vous pouvez vous inscrire pour un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7712b-126">If your organization doesn't have a [!INCLUDE [prod_short](includes/prod_short.md)] subscription, you can sign up for a free trial.</span></span> <span data-ttu-id="7712b-127">Pour plus d’informations, voir [Mise en route avec une version d'essai](across-preview.md#getting-started-with-a-trial).</span><span class="sxs-lookup"><span data-stu-id="7712b-127">For more information, see [Getting Started with a Trial](across-preview.md#getting-started-with-a-trial).</span></span>

2. <span data-ttu-id="7712b-128">En tant qu’administrateur, consultez [Gestion de l’intégration de Microsoft Teams avec Business Central](admin-teams-integration.md) pour obtenir des informations sur la manière dont les utilisateurs peuvent travailler avec [!INCLUDE [prod_short](includes/prod_short.md)] et Teams.</span><span class="sxs-lookup"><span data-stu-id="7712b-128">As an administrator, see [Managing Microsoft Teams Integration with Business Central](admin-teams-integration.md) for information about getting users set up to work with [!INCLUDE [prod_short](includes/prod_short.md)] and Teams.</span></span>
3. <span data-ttu-id="7712b-129">Installer une application [!INCLUDE [prod_short](includes/prod_short.md)] dans Teams.</span><span class="sxs-lookup"><span data-stu-id="7712b-129">Install [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="7712b-130">Voir [Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md).</span><span class="sxs-lookup"><span data-stu-id="7712b-130">See [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md).</span></span>
4. <span data-ttu-id="7712b-131">Une fois l’application installée, vous êtes prêt à partir.</span><span class="sxs-lookup"><span data-stu-id="7712b-131">Once the app is installed, you're ready to go.</span></span> <span data-ttu-id="7712b-132">Consultez [Recherche de clients, de fournisseurs et d’autres contacts dans Microsoft Teams](across-search-contacts-teams.md) ou [Partager des enregistrements dans Microsoft Teams](across-working-with-teams.md).</span><span class="sxs-lookup"><span data-stu-id="7712b-132">See [Searching for Customers, Vendors, and Other Contacts from Microsoft Teams](across-search-contacts-teams.md) and [Share Records in Microsoft Teams](across-working-with-teams.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="7712b-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7712b-133">See Also</span></span>

[<span data-ttu-id="7712b-134">FAQ Teams</span><span class="sxs-lookup"><span data-stu-id="7712b-134">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="7712b-135">Résolution des incidents dans Teams</span><span class="sxs-lookup"><span data-stu-id="7712b-135">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="7712b-136">Développement pour l’intégration de Teams</span><span class="sxs-lookup"><span data-stu-id="7712b-136">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)
  
## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]