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
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989451"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="9e663-103">Utilisation des données Business Central dans Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9e663-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="9e663-104">[!INCLUDE [prodshort](includes/prodshort.md)] propose une application qui connecte Microsoft Teams à vos données métier dans [!INCLUDE [prodshort](includes/prodshort.md)], afin que vous puissiez partager rapidement les détails entre les membres de l’équipe et répondre plus rapidement aux demandes de renseignements.</span><span class="sxs-lookup"><span data-stu-id="9e663-104">[!INCLUDE [prodshort](includes/prodshort.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prodshort](includes/prodshort.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="9e663-105">Dans cet article, vous apprendrez à utiliser l’application pour partager des données [!INCLUDE [prodshort](includes/prodshort.md)] avec des collègues dans une conversation Teams.</span><span class="sxs-lookup"><span data-stu-id="9e663-105">In this article, you'll learn how to use the app to share [!INCLUDE [prodshort](includes/prodshort.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="9e663-106">Aperçu</span><span class="sxs-lookup"><span data-stu-id="9e663-106">Overview</span></span>

<span data-ttu-id="9e663-107">L’application [!INCLUDE [prodshort](includes/prodshort.md)] vous permet de :</span><span class="sxs-lookup"><span data-stu-id="9e663-107">The [!INCLUDE [prodshort](includes/prodshort.md)] app lets you:</span></span>

- <span data-ttu-id="9e663-108">Copier un lien vers n’importe quel enregistrement Business Central et le coller dans une conversation Teams à partager avec vos collègues.</span><span class="sxs-lookup"><span data-stu-id="9e663-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="9e663-109">Le lien étendra cela dans une carte interactive compacte qui affiche des informations sur l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9e663-109">The link will expand that into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="9e663-110">Une fois dans la conversation, vous et vos collègues pouvez afficher plus de détails sur l’enregistrement, modifier les données et prendre des mesures, sans quitter Teams.</span><span class="sxs-lookup"><span data-stu-id="9e663-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action - without leaving Teams.</span></span>

<span data-ttu-id="9e663-111">[![Intégration Teams avec Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="9e663-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9e663-112">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="9e663-112">Prerequisites</span></span>

- <span data-ttu-id="9e663-113">Vous avez accès à Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="9e663-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="9e663-114">Vous avez installé l’application [!INCLUDE [prodshort](includes/prodshort.md)] dans Teams.</span><span class="sxs-lookup"><span data-stu-id="9e663-114">You've installed the [!INCLUDE [prodshort](includes/prodshort.md)] app in Teams.</span></span> <span data-ttu-id="9e663-115">Pour plus d’informations, voir [Installer l’application [!INCLUDE [prodshort](includes/prodshort.md)] pour Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="9e663-115">For more information, see [Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="9e663-116">Tous les participants à une conversation Teams pourront afficher les fiches des enregistrements Business Central que vous soumettez à la conversation.</span><span class="sxs-lookup"><span data-stu-id="9e663-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="9e663-117">Mais pour afficher plus de détails sur les enregistrements, en utilisant les boutons **Détails** ou **Contextuel** sur une fiche, ils auront besoin d’accéder à [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="9e663-117">But to view more details about records, by using the **Details** or **Pop-out** buttons on a card, they'll need access to [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="9e663-118">Pour plus d’informations, voir [Gestion de l’intégration Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="9e663-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="9e663-119">Inclure une fiche Business Central dans une conversation Teams</span><span class="sxs-lookup"><span data-stu-id="9e663-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="9e663-120">Connectez-vous à [!INCLUDE [prodshort](includes/prodshort.md)] en utilisant votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="9e663-120">Sign in to [!INCLUDE [prodshort](includes/prodshort.md)] using your browser.</span></span>
2. <span data-ttu-id="9e663-121">Ouvrez l’enregistrement que vous souhaitez partager.</span><span class="sxs-lookup"><span data-stu-id="9e663-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="9e663-122">L’application est conçue pour afficher des pages de type fiche à partir de [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="9e663-122">The app is designed to display card type pages from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="9e663-123">Ouvrez une page qui affiche un seul enregistrement, comme un article, un client ou une commande client.</span><span class="sxs-lookup"><span data-stu-id="9e663-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="9e663-124">Vous ne pouvez pas l’utiliser pour les tableaux de bord ou les pages qui affichent plusieurs enregistrements dans une liste.</span><span class="sxs-lookup"><span data-stu-id="9e663-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="9e663-125">Copiez l’URL entière de la barre d’adresse du navigateur.</span><span class="sxs-lookup"><span data-stu-id="9e663-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Copier l’URL de Business Central à partir du navigateur](media/teams-url.png)
4. <span data-ttu-id="9e663-127">Accédez à Teams et démarrez une conversation, qui peut être une discussion avec une personne, un groupe de personnes ou un canal d’équipe.</span><span class="sxs-lookup"><span data-stu-id="9e663-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="9e663-128">Collez l’URL dans la zone où vous ajoutez un message.</span><span class="sxs-lookup"><span data-stu-id="9e663-128">Paste the URL into the box where you add a message.</span></span>

   ![Coller l’URL de Business Central dans Teams](media/teams-paste-url.png)
6. <span data-ttu-id="9e663-130">La première fois que vous collez un lien dans une conversation, vous serez invité à vous connecter à [!INCLUDE [prodshort](includes/prodshort.md)] et à autoriser l’application à récupérer des données.</span><span class="sxs-lookup"><span data-stu-id="9e663-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prodshort](includes/prodshort.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="9e663-131">Suivez simplement les instructions à l’écran.</span><span class="sxs-lookup"><span data-stu-id="9e663-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9e663-132">Vous ne devez effectuer cette étape qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="9e663-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="9e663-133">Attendez un moment pendant qu’une fiche soit générée dans la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="9e663-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="9e663-134">Lorsque la fiche apparaît, examinez attentivement don contenu pour toute information sensible avant d’envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="9e663-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="9e663-135">Cette étape est importante, car une fois que vous envoyez le message, tous les participants à la conversation peuvent voir la fiche.</span><span class="sxs-lookup"><span data-stu-id="9e663-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="9e663-136">Si la fiche semble bonne, sélectionnez **Envoyer** pour la soumettre à la conversation.</span><span class="sxs-lookup"><span data-stu-id="9e663-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="9e663-137">Après l’apparition de la fiche et avant de sélectionner **Envoyer** , vous pouvez supprimer l’URL collée si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="9e663-137">After the card appears, and before you select **Send** , you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="9e663-138">Pour afficher plus de détails ou apporter des modifications à l’enregistrement, sélectionnez **Détails** .</span><span class="sxs-lookup"><span data-stu-id="9e663-138">To view more details or make changes to the record, select **Details** .</span></span>

    <span data-ttu-id="9e663-139">La page de détails est similaire à ce que vous voyez dans [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="9e663-139">The details page is similar to what you'd see in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="9e663-140">Mais elle est légèrement rognée pour Teams.</span><span class="sxs-lookup"><span data-stu-id="9e663-140">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="9e663-141">Lorsque vous avez terminé de consulter et d’apporter des modifications, fermez la fenêtre pour revenir à la conversation Teams.</span><span class="sxs-lookup"><span data-stu-id="9e663-141">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9e663-142">Les modifications que vous apportez ne seront pas reflétées dans la fiche avant la prochaine fois que vous collerez son lien dans une conversation.</span><span class="sxs-lookup"><span data-stu-id="9e663-142">Any changes you make won't be reflected in the card until the next time you paste its link in a conversation.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e663-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e663-143">See Also</span></span>

[<span data-ttu-id="9e663-144">Vue d’ensemble de l’intégration de Business Central et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9e663-144">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="9e663-145">[Installer l’application [!INCLUDE [prodshort](includes/prodshort.md)] pour Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="9e663-145">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="9e663-146">Développement pour l’intégration de Teams</span><span class="sxs-lookup"><span data-stu-id="9e663-146">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="9e663-147">Mise en route</span><span class="sxs-lookup"><span data-stu-id="9e663-147">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
