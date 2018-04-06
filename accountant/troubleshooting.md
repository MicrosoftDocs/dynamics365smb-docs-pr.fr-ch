---
title: "Procédures de dépannage et solutions aux problèmes | Microsoft Docs"
description: "Découvrez comment résoudre les problèmes dans Accountant Hub pour Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a9753b00b47fc4d74583482b2da92aae5e2f8a74
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="troubleshooting-included365acclongincludesd365acclongmdmd"></a><span data-ttu-id="13d37-103">Dépannage de [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="13d37-103">Troubleshooting [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span></span>
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

<span data-ttu-id="13d37-104">L'inscription à [!INCLUDE[d365acc](includes/d365acc_md.md)] est simple et peut être effectuée très rapidement.</span><span class="sxs-lookup"><span data-stu-id="13d37-104">Signing up for [!INCLUDE[d365acc](includes/d365acc_md.md)] is easy and can be done very quickly.</span></span> <span data-ttu-id="13d37-105">L'ajout de clients au tableau de bord est également facile, mais cet article traite des problèmes que vous pouvez rencontrer en route.</span><span class="sxs-lookup"><span data-stu-id="13d37-105">Adding clients to the dashboard is also easy, but this article addresses issues that you may have on the way.</span></span>

## <a name="what-email-address-can-i-use-with-included365accincludesd365accmdmd"></a><span data-ttu-id="13d37-106">Quelle adresse e-mail puis-je utiliser avec [!INCLUDE[d365acc](includes/d365acc_md.md)] ?</span><span class="sxs-lookup"><span data-stu-id="13d37-106">What email address can I use with [!INCLUDE[d365acc](includes/d365acc_md.md)]?</span></span>
[!INCLUDE[d365acc](includes/d365acc_md.md)]<span data-ttu-id="13d37-107"> exige que vous utilisiez une adresse e-mail professionnelle ou scolaire pour votre inscription.</span><span class="sxs-lookup"><span data-stu-id="13d37-107"> requires that you use a work or school email address to sign up.</span></span> [!INCLUDE[d365acc](includes/d365acc_md.md)]<span data-ttu-id="13d37-108"> ne prend pas en charge les adresses e-mail fournies par les services de messagerie publics ni les opérateurs de télécommunications.</span><span class="sxs-lookup"><span data-stu-id="13d37-108"> does not support email addresses provided by consumer email services or telecommunication providers.</span></span> <span data-ttu-id="13d37-109">Cela comprend outlook.com, hotmail.com, gmail.com, et d'autres.</span><span class="sxs-lookup"><span data-stu-id="13d37-109">This includes outlook.com, hotmail.com, gmail.com, and others.</span></span>  

<span data-ttu-id="13d37-110">Si vous essayez d'effectuer votre inscription à l'aide d'une adresse e-mail personnelle, vous recevez un message vous demandant d'utiliser une adresse professionnelle ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="13d37-110">If you try to sign up with a personal email address, you will get a message indicating to use a work or school email address.</span></span>  

## <a name="why-cant-i-connect-to-my-clients-data"></a><span data-ttu-id="13d37-111">Pourquoi ne puis-je pas me connecter aux données de mon client ?</span><span class="sxs-lookup"><span data-stu-id="13d37-111">Why can't I connect to my client's data?</span></span>
<span data-ttu-id="13d37-112">Il peut y avoir quelques raisons à cela, notamment :</span><span class="sxs-lookup"><span data-stu-id="13d37-112">There can be a couple of reasons, including the following:</span></span>

- <span data-ttu-id="13d37-113">L'URL dans le champ **URL du client** n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="13d37-113">The URL in the **Client URL** field is not valid</span></span>  

  <span data-ttu-id="13d37-114">Accédez à **Gérer les clients**, ouvrez le client auquel vous ne pouvez pas vous connecter, puis choisissez **Tester l'URL du client**.</span><span class="sxs-lookup"><span data-stu-id="13d37-114">Go to **Manage Clients**, open the client that you cannot connect to, and then choose **Test Client URL**.</span></span>  
- <span data-ttu-id="13d37-115">La société du client est actuellement hors connexion, par exemple si elle est en cours de mise à niveau</span><span class="sxs-lookup"><span data-stu-id="13d37-115">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="13d37-116">Dans votre tableau de bord, choisissez l'élément de menu **Outils**, puis **Vérifier les erreurs**.</span><span class="sxs-lookup"><span data-stu-id="13d37-116">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="13d37-117">Cela ouvre une liste avec des informations techniques vous permettant de contacter votre administrateur si vous voyez des erreurs.</span><span class="sxs-lookup"><span data-stu-id="13d37-117">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="13d37-118">Par exemple, le message d'erreur « Le serveur a rejeté les informations d'identification du client » suggère que vous n'avez pas accès.</span><span class="sxs-lookup"><span data-stu-id="13d37-118">For example, the error message "The server has rejected the client credentials" suggests that you do not have access.</span></span>  
- <span data-ttu-id="13d37-119">Vous n'avez pas reçu d'e-mail de votre client l'invitant à leur [!INCLUDE[d365fin](includes/d365fin_md.md)], ou vous n'avez pas ouvert le lien dans l'e-mail, ou vous n'avez pas accepté l'invitation</span><span class="sxs-lookup"><span data-stu-id="13d37-119">You have not received an email from your client that invites them to their [!INCLUDE[d365fin](includes/d365fin_md.md)], or you did not open the link in the email, or you did not accept the invitation</span></span>

  <span data-ttu-id="13d37-120">Vous devez ouvrir le lien dans l'invitation et accepter les étapes vous ajoutant au [!INCLUDE[d365fin](includes/d365fin_md.md)] de votre client.</span><span class="sxs-lookup"><span data-stu-id="13d37-120">You must open the link in the invitation and accept the steps that adds you to your client's [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="13d37-121">Jusque-là, vous n'avez pas accès à ses données.</span><span class="sxs-lookup"><span data-stu-id="13d37-121">Until then, you do not have access to their data.</span></span>  
- <span data-ttu-id="13d37-122">Vous n'avez pas accès à toutes les sociétés du [!INCLUDE[d365fin](includes/d365fin_md.md)] de votre client</span><span class="sxs-lookup"><span data-stu-id="13d37-122">You do not have access to all companies in your client's [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>

  <span data-ttu-id="13d37-123">Votre client peut avoir plusieurs centres de profit ou plusieurs sociétés dans [!INCLUDE[d365fin](includes/d365fin_md.md)], et votre invitation n'inclut pas toujours toutes les sociétés.</span><span class="sxs-lookup"><span data-stu-id="13d37-123">Your client can have multiple business units or companies in [!INCLUDE[d365fin](includes/d365fin_md.md)], and your invitation does not always include all companies.</span></span> <span data-ttu-id="13d37-124">Communiquez avec votre client pour vous assurer que vous avez accès aux sociétés dans lesquelles le client souhaite que vous travailliez.</span><span class="sxs-lookup"><span data-stu-id="13d37-124">Work with your client to make sure that you have access to the companies that the client wants you to work in.</span></span>  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a><span data-ttu-id="13d37-125">Pourquoi les données ne s'actualisent-elles pas sur mon tableau de bord ?</span><span class="sxs-lookup"><span data-stu-id="13d37-125">Why doesn't the data refresh in my dashboard?</span></span>
<span data-ttu-id="13d37-126">Lorsque vous ajoutez un client ou que vous demandez une actualisation des données, [!INCLUDE[d365acc](includes/d365acc_md.md)] récupère les données.</span><span class="sxs-lookup"><span data-stu-id="13d37-126">When you add a client or request a refresh of the data, [!INCLUDE[d365acc](includes/d365acc_md.md)] fetches the data.</span></span> <span data-ttu-id="13d37-127">Mais vous devez actualiser la fenêtre vous-même, par exemple en choisissant l'action « Afficher à nouveau toutes les sociétés », actualisez la fenêtre du navigateur, quittez le tableau de bord puis retournez-y, ou similaire.</span><span class="sxs-lookup"><span data-stu-id="13d37-127">But you must refresh the window yourself, such as choosing the "Redisplay all companies" action, refresh the browser window, navigate away from the dashboard and then back again, or similar.</span></span> <span data-ttu-id="13d37-128">C'est un problème connu auquel nous travaillons pour l'améliorer dans une mise à jour ultérieure.</span><span class="sxs-lookup"><span data-stu-id="13d37-128">This is a known issue that we are working on improving in a later update.</span></span>  

## <a name="see-also"></a><span data-ttu-id="13d37-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13d37-129">See Also</span></span>
<span data-ttu-id="13d37-130">[Mise en route avec [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="13d37-130">[Get Started with [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span></span>  
<span data-ttu-id="13d37-131">[Ajouter des clients à votre tableau de bord dans [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span><span class="sxs-lookup"><span data-stu-id="13d37-131">[Add Clients to Your Dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span></span>  

