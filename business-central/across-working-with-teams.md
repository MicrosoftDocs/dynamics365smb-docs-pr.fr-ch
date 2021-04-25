---
title: Utiliser les données Business Central dans Microsoft Teams| Microsoft Docs
description: Découvre comment utiliser l’application Business Central pour Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: e20208d50eb65f1a92e6661396bf53007ab88eb8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786897"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="b3788-103">Utilisation des données Business Central dans Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b3788-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [online_only](includes/online_only.md)]

<span data-ttu-id="b3788-104">[!INCLUDE [prod_short](includes/prod_short.md)] propose une application qui connecte Microsoft Teams à vos données métier dans [!INCLUDE [prod_short](includes/prod_short.md)], afin que vous puissiez partager rapidement les détails entre les membres de l’équipe et répondre plus rapidement aux demandes de renseignements.</span><span class="sxs-lookup"><span data-stu-id="b3788-104">[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="b3788-105">Dans cet article, vous apprendrez à utiliser l’application pour partager des données [!INCLUDE [prod_short](includes/prod_short.md)] avec des collègues dans une conversation Teams.</span><span class="sxs-lookup"><span data-stu-id="b3788-105">In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="b3788-106">Aperçu</span><span class="sxs-lookup"><span data-stu-id="b3788-106">Overview</span></span>

<span data-ttu-id="b3788-107">L’application [!INCLUDE [prod_short](includes/prod_short.md)] vous permet de :</span><span class="sxs-lookup"><span data-stu-id="b3788-107">The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:</span></span>

- <span data-ttu-id="b3788-108">Copier un lien vers n’importe quel enregistrement Business Central et le coller dans une conversation Teams à partager avec vos collègues.</span><span class="sxs-lookup"><span data-stu-id="b3788-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="b3788-109">L’application étendra le lien dans une carte interactive compacte qui affiche des informations sur l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3788-109">The app will then expand the link into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="b3788-110">Une fois dans la conversation, vous et vos collègues pouvez afficher plus de détails sur l’enregistrement, modifier les données et prendre des mesures, sans quitter Teams.</span><span class="sxs-lookup"><span data-stu-id="b3788-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.</span></span>

<span data-ttu-id="b3788-111">[![Intégration Teams avec Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="b3788-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b3788-112">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="b3788-112">Prerequisites</span></span>

- <span data-ttu-id="b3788-113">Vous avez accès à Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b3788-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="b3788-114">Vous avez installé l’application [!INCLUDE [prod_short](includes/prod_short.md)] dans Teams.</span><span class="sxs-lookup"><span data-stu-id="b3788-114">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="b3788-115">Pour plus d’informations, voir [Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="b3788-115">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="b3788-116">Tous les participants à une conversation Teams pourront afficher les fiches des enregistrements Business Central que vous soumettez à la conversation.</span><span class="sxs-lookup"><span data-stu-id="b3788-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="b3788-117">Mais pour afficher plus de détails sur les enregistrements, en utilisant les boutons **Détails** ou **Contextuel** sur une fiche, ils auront besoin d’accéder à [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b3788-117">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b3788-118">Pour plus d’informations, voir [Gestion de l’intégration Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="b3788-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="b3788-119">Inclure une fiche Business Central dans une conversation Teams</span><span class="sxs-lookup"><span data-stu-id="b3788-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="b3788-120">Connectez-vous à [!INCLUDE [prod_short](includes/prod_short.md)] en utilisant votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="b3788-120">Sign in to [!INCLUDE [prod_short](includes/prod_short.md)] using your browser.</span></span>
2. <span data-ttu-id="b3788-121">Ouvrez l’enregistrement que vous souhaitez partager.</span><span class="sxs-lookup"><span data-stu-id="b3788-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="b3788-122">L’application est conçue pour afficher des pages de type fiche à partir de [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b3788-122">The app is designed to display card type pages from [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b3788-123">Ouvrez une page qui affiche un seul enregistrement, comme un article, un client ou une commande client.</span><span class="sxs-lookup"><span data-stu-id="b3788-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="b3788-124">Vous ne pouvez pas l’utiliser pour les tableaux de bord ou les pages qui affichent plusieurs enregistrements dans une liste.</span><span class="sxs-lookup"><span data-stu-id="b3788-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="b3788-125">Copiez l’URL entière de la barre d’adresse du navigateur.</span><span class="sxs-lookup"><span data-stu-id="b3788-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Copier l’URL de Business Central à partir du navigateur](media/teams-url-v2.png)
4. <span data-ttu-id="b3788-127">Accédez à Teams et démarrez une conversation, qui peut être une discussion avec une personne, un groupe de personnes ou un canal d’équipe.</span><span class="sxs-lookup"><span data-stu-id="b3788-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="b3788-128">Collez l’URL dans la zone de message où vous composez un message.</span><span class="sxs-lookup"><span data-stu-id="b3788-128">Paste the URL in the message box where you compose a message.</span></span>

   ![Coller l’URL de Business Central dans Teams](media/teams-paste-url-v2.png)
6. <span data-ttu-id="b3788-130">La première fois que vous collez un lien dans une conversation, vous serez invité à vous connecter à [!INCLUDE [prod_short](includes/prod_short.md)] et à autoriser l’application à récupérer des données.</span><span class="sxs-lookup"><span data-stu-id="b3788-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prod_short](includes/prod_short.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="b3788-131">Suivez simplement les instructions à l’écran.</span><span class="sxs-lookup"><span data-stu-id="b3788-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b3788-132">Vous ne devez effectuer cette étape qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="b3788-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="b3788-133">Attendez un moment pendant qu’une fiche soit générée dans la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="b3788-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="b3788-134">Lorsque la fiche apparaît, examinez attentivement don contenu pour toute information sensible avant d’envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="b3788-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="b3788-135">Cette étape est importante, car une fois que vous envoyez le message, tous les participants à la conversation peuvent voir la fiche.</span><span class="sxs-lookup"><span data-stu-id="b3788-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="b3788-136">Si la fiche semble bonne, sélectionnez **Envoyer** pour la soumettre à la conversation.</span><span class="sxs-lookup"><span data-stu-id="b3788-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="b3788-137">Après l’apparition de la fiche et avant de sélectionner **Envoyer**, vous pouvez supprimer l’URL collée si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="b3788-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="b3788-138">Pour afficher plus de détails ou apporter des modifications à l’enregistrement montré dans la fiche, sélectionnez **Détails**.</span><span class="sxs-lookup"><span data-stu-id="b3788-138">To view more details or make changes to the record shown in the card, select **Details**.</span></span> <span data-ttu-id="b3788-139">Pour plus d’informations, voir la section suivante.</span><span class="sxs-lookup"><span data-stu-id="b3788-139">For more information, see the next section.</span></span>

## <a name="view-card-details"></a><span data-ttu-id="b3788-140">Afficher les détails de la fiche</span><span class="sxs-lookup"><span data-stu-id="b3788-140">View card details</span></span>

<span data-ttu-id="b3788-141">Une fois qu’une fiche a été envoyée à une conversation, tous les participants avec les [autorisations appropriées](admin-teams-integration.md#permissions) peuvent sélectionner **Détails** pour ouvrir une fenêtre qui affiche plus d’informations sur l’enregistrement&mdash; et éventuellement apporter des modifications à l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3788-141">Once a card's been sent to a conversation, all participants with the [proper permissions](admin-teams-integration.md#permissions) can select **Details** to open a window that displays more information about the record&mdash;and possibly make changes to the record.</span></span> <span data-ttu-id="b3788-142">Peu importe que vous soyez celui qui envoie la fiche ou celui qui la reçoit.</span><span class="sxs-lookup"><span data-stu-id="b3788-142">It doesn't matter if you're the one sending the card or the one receiving the card.</span></span> <span data-ttu-id="b3788-143">La fonctionnalité **Détails** est particulièrement utile pour les destinataires, car elle leur fournit rapidement des informations concises et ciblées sur l’enregistrement, au lieu de devoir scanner l’intégralité de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b3788-143">The **Details** feature is especially useful to recipients, because it quickly provides them with concise, targeted information about the record, as opposed to having to scan the full record.</span></span>

<span data-ttu-id="b3788-144">La fenêtre de détails est similaire à ce que vous voyez dans l’enregistrement [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b3788-144">The details window is similar to what you'd see in [!INCLUDE [prod_short](includes/prod_short.md)] the record.</span></span> <span data-ttu-id="b3788-145">Mais elle est légèrement rognée pour Teams.</span><span class="sxs-lookup"><span data-stu-id="b3788-145">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="b3788-146">Lorsque vous avez terminé de consulter et d’apporter des modifications, fermez la fenêtre pour revenir à la conversation Teams.</span><span class="sxs-lookup"><span data-stu-id="b3788-146">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

<span data-ttu-id="b3788-147">Voici quelques points à garder à l’esprit lorsque vous travaillez avec les détails de la fiche :</span><span class="sxs-lookup"><span data-stu-id="b3788-147">Here are a couple things to keep in mind when working with the card details:</span></span>

- <span data-ttu-id="b3788-148">Pour afficher les détails de la fiche, les utilisateurs doivent avoir une autorisation de lecture sur la page et ses données dans [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b3788-148">To open the card details, users must have permission on the page and its data in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>
- <span data-ttu-id="b3788-149">Les fiches des discussions Teams ne sont pas automatiquement mises à jour en fonction des modifications.</span><span class="sxs-lookup"><span data-stu-id="b3788-149">Cards in Teams chats aren't automatically updated to changes.</span></span> <span data-ttu-id="b3788-150">Toutes les modifications que vous enregistrez dans un enregistrement dans la fenêtre de détails sont enregistrées dans [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b3788-150">Any changes you save to a record in the details window are saved in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b3788-151">Mais la fiche dans Teams n’affichera pas les modifications de la conversion tant que vous n’aurez pas recollé le lien.</span><span class="sxs-lookup"><span data-stu-id="b3788-151">But the card in Teams won't show the changes in the conversion, until you paste the link again.</span></span>

<span data-ttu-id="b3788-152">Pour en savoir plus sur l’utilisation des fiches et des détails de fiche, consultez [FAQ Teams](teams-faq.md).</span><span class="sxs-lookup"><span data-stu-id="b3788-152">To learn more about working with cards and card details, see [Teams FAQ](teams-faq.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b3788-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3788-153">See Also</span></span>

[<span data-ttu-id="b3788-154">Vue d’ensemble de l’intégration de Business Central et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b3788-154">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="b3788-155">[Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="b3788-155">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="b3788-156">FAQ Teams</span><span class="sxs-lookup"><span data-stu-id="b3788-156">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="b3788-157">Résolution des incidents dans Teams</span><span class="sxs-lookup"><span data-stu-id="b3788-157">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="b3788-158">Développement pour l’intégration de Teams</span><span class="sxs-lookup"><span data-stu-id="b3788-158">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]