---
title: Recherche de contacts dans Microsoft Teams
description: Découvrez comment rechercher des clients, des fournisseurs et d'autres contacts Business Central à partir de Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: 6d094e365ad0c7da73467e5a3160d926902c45d9
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935176"
---
# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a><span data-ttu-id="15c83-103">Recherche de clients, de fournisseurs et autres contacts dans Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="15c83-103">Searching for Customers, Vendors, and Other Contacts from Microsoft Teams</span></span>

<span data-ttu-id="15c83-104">[!INCLUDE [online_only](includes/online_only.md)].</span><span class="sxs-lookup"><span data-stu-id="15c83-104">[!INCLUDE [online_only](includes/online_only.md)].</span></span> <span data-ttu-id="15c83-105">Introduit dans la 1re vague de lancement 2021.</span><span class="sxs-lookup"><span data-stu-id="15c83-105">Introduced in 2021 release wave 1.</span></span>

<span data-ttu-id="15c83-106">[!INCLUDE [prod_short](includes/prod_short.md)] dispose d'un système complet de gestion des contacts professionnels qui est essentiel pour les utilisateurs des ventes, des opérations ou d'autres rôles ministériels.</span><span class="sxs-lookup"><span data-stu-id="15c83-106">[!INCLUDE [prod_short](includes/prod_short.md)] has a comprehensive business contact management system that is essential for users in sales, operations, or other departmental roles.</span></span> <span data-ttu-id="15c83-107">Si vous êtes un utilisateur dans l'un de ces rôles, vous devrez souvent rechercher, rencontrer ou démarrer une conversation avec vos fournisseurs, clients et autres contacts.</span><span class="sxs-lookup"><span data-stu-id="15c83-107">If you're a user in one of these roles, you'll often need to look up, meet, or start a conversation with your vendors, customers, and other contacts.</span></span> <span data-ttu-id="15c83-108">Avec l'application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams, vous pouvez effectuer ces tâches directement depuis Teams, sans avoir à passer à [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="15c83-108">With the [!INCLUDE [prod_short](includes/prod_short.md)] app for Teams, you can do these tasks directly from Teams, without having to switch to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="15c83-109">À partir de Teams, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="15c83-109">From within Teams, you can:</span></span>

- <span data-ttu-id="15c83-110">Rechercher des contacts [!INCLUDE [prod_short](includes/prod_short.md)] dans la boîte de commande Teams ou dans la zone de rédaction du message.</span><span class="sxs-lookup"><span data-stu-id="15c83-110">Look up [!INCLUDE [prod_short](includes/prod_short.md)] contacts from the Teams command box or from the message compose area.</span></span> <span data-ttu-id="15c83-111">Les contacts peuvent inclure des prospects, des fournisseurs, des clients ou d'autres relations commerciales.</span><span class="sxs-lookup"><span data-stu-id="15c83-111">Contacts can include prospects, vendors, customers, or other business relationships.</span></span>
- <span data-ttu-id="15c83-112">Partagez un contact sous forme de carte dans une conversation Teams.</span><span class="sxs-lookup"><span data-stu-id="15c83-112">Share a contact as a card in a Teams conversation.</span></span>
- <span data-ttu-id="15c83-113">Affichez des détails sur le contact, l′historique des interactions et d′autres informations telles que les paiements impayés ou les documents ouverts.</span><span class="sxs-lookup"><span data-stu-id="15c83-113">View details about the contact, interaction history, and other insights like outstanding payments or open documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="15c83-114">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="15c83-114">Prerequisites</span></span>

- <span data-ttu-id="15c83-115">Vous avez accès à Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="15c83-115">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="15c83-116">Vous avez installé l’application [!INCLUDE [prod_short](includes/prod_short.md)] dans Teams.</span><span class="sxs-lookup"><span data-stu-id="15c83-116">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="15c83-117">Pour plus d’informations, voir [Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="15c83-117">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>
- <span data-ttu-id="15c83-118">Vous avez un compte [!INCLUDE [prod_short](includes/prod_short.md)] avec accès aux contacts dans au moins une entreprise.</span><span class="sxs-lookup"><span data-stu-id="15c83-118">You've got a [!INCLUDE [prod_short](includes/prod_short.md)] account with access to contacts in at least one company.</span></span>

> [!NOTE]
> <span data-ttu-id="15c83-119">Que vous recherchiez à partir de la boîte de commande ou de la boîte de rédaction de message, vous pouvez être invité à vous connecter ou à configurer l'application la première fois.</span><span class="sxs-lookup"><span data-stu-id="15c83-119">Whether you searching from the command box or message compose box, you may be asked to sign in or set up the app the first time.</span></span> <span data-ttu-id="15c83-120">Cette étape est nécessaire pour rechercher des contacts dans la bonne entreprise Business Central.</span><span class="sxs-lookup"><span data-stu-id="15c83-120">This step is necessary to search for contacts in the right Business Central company.</span></span> <span data-ttu-id="15c83-121">Pour plus d'informations sur la configuration de l'application pour choisir votre entreprise, consultez [Modification de la société et d'autres paramètres dans les équipes](across-teams-settings.md).</span><span class="sxs-lookup"><span data-stu-id="15c83-121">For information about setting up the app to choose your company, see [Changing Company and Other Settings in Teams](across-teams-settings.md).</span></span>

## <a name="look-up-contacts-from-the-command-box"></a><span data-ttu-id="15c83-122">Rechercher des contacts dans la boîte de commande</span><span class="sxs-lookup"><span data-stu-id="15c83-122">Look up contacts from the command box</span></span>

<span data-ttu-id="15c83-123">La boîte de commande est en haut de chaque écran dans Teams.</span><span class="sxs-lookup"><span data-stu-id="15c83-123">The command box is at the top of every screen in Teams.</span></span> <span data-ttu-id="15c83-124">Il vous permet de rechercher, d'effectuer des actions rapides ou de lancer des applications, comme l'application [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="15c83-124">It lets you search, take quick actions, or launch apps, like the [!INCLUDE [prod_short](includes/prod_short.md)] app.</span></span> <span data-ttu-id="15c83-125">La recherche à partir de la boîte de commande est idéale pour rechercher rapidement des contacts et leurs données associées pour votre propre usage.</span><span class="sxs-lookup"><span data-stu-id="15c83-125">Searching from the command box is great for quickly looking up contacts and their related data for your own use.</span></span> <span data-ttu-id="15c83-126">Par exemple, supposons que vous souhaitiez rechercher l'adresse e-mail d'un fournisseur pour configurer une réunion de calendrier.</span><span class="sxs-lookup"><span data-stu-id="15c83-126">For example, suppose you want to look up an email address of a vendor to set up a calendar meeting.</span></span> <span data-ttu-id="15c83-127">Ou peut-être souhaitez-vous consulter l'historique des interactions lors d'une réunion avec un client.</span><span class="sxs-lookup"><span data-stu-id="15c83-127">Or maybe you want to look up interaction history during a meeting with a customer.</span></span>

1. <span data-ttu-id="15c83-128">Dans la zone de commande, saisissez **@Business Central**, puis sélectionnez l'application Business Central dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="15c83-128">In the command box, type **@Business Central**, then select the Business Central app from the results.</span></span>

    ![Ouvrez l'application Business Central pour rechercher des contacts à partir de la boîte de commande](media/teams-contacts-command-1.png)

2. <span data-ttu-id="15c83-130">Dans la zone **Business Central**, commencez à saisir le texte de recherche, comme un nom, une adresse ou un numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="15c83-130">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="15c83-131">Au fur et à mesure de votre saisie, les résultats correspondants s'affichent.</span><span class="sxs-lookup"><span data-stu-id="15c83-131">As you type, matching results will appear.</span></span>

    ![Rechercher des contacts Business Central à partir de la boîte de commande dans Teams](media/teams-contacts-command-2.png)
3. <span data-ttu-id="15c83-133">Sélectionnez un contact parmi les résultats.</span><span class="sxs-lookup"><span data-stu-id="15c83-133">Select a contact from the results.</span></span>

    <span data-ttu-id="15c83-134">La carte de visite apparaît sous la boîte de commande.</span><span class="sxs-lookup"><span data-stu-id="15c83-134">The contact card appears beneath the command box.</span></span>

4. <span data-ttu-id="15c83-135">Si vous souhaitez ajouter la carte de contact dans une conversation, allez dans le coin supérieur droit de la carte, sélectionnez **... (Plus d'options)** > **Copier**.</span><span class="sxs-lookup"><span data-stu-id="15c83-135">If you want to add the contact card into a conversation, go to the upper right corner of the card, select **... (More options)** > **Copy**.</span></span> <span data-ttu-id="15c83-136">Ensuite, collez la copie dans la zone de rédaction du message d'une conversation.</span><span class="sxs-lookup"><span data-stu-id="15c83-136">Then, paste the copy in the message compose box of a conversation.</span></span>  

<span data-ttu-id="15c83-137">Pour plus d'informations générales sur la zone de commande dans Teams, voir [Teams – Utiliser la boîte de commande](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span><span class="sxs-lookup"><span data-stu-id="15c83-137">For more general information about the command box in Teams, see [Teams - Use the command box](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span></span>

## <a name="look-up-contacts-from-the-message-compose-box"></a><span data-ttu-id="15c83-138">Rechercher des contacts dans la zone de composition de message</span><span class="sxs-lookup"><span data-stu-id="15c83-138">Look up contacts from the message compose box</span></span>

<span data-ttu-id="15c83-139">L'avantage d'utiliser la boîte de rédaction de message est que vous pouvez ajouter une fiche de contact directement à une conversation, pour que les autres puissent la voir.</span><span class="sxs-lookup"><span data-stu-id="15c83-139">The advantage of using the message compose box is that you can add a contact card directly to a conversation, for others to see.</span></span>

1. <span data-ttu-id="15c83-140">Sous la zone de rédaction du message, sélectionnez l'icône **Business Central** pour lancer l'application.</span><span class="sxs-lookup"><span data-stu-id="15c83-140">Beneath to message compose box, select the **Business Central** icon to launch the app.</span></span>

    <span data-ttu-id="15c83-141">Si vous ne voyez pas l'icône **Business Central**, sélectionnez **... (Extensions de messagerie)**.</span><span class="sxs-lookup"><span data-stu-id="15c83-141">If you don't see the **Business Central** icon, select **... (Messaging extensions)**.</span></span>

    ![Ouvrez l'application Business Central pour rechercher des contacts à partir de la zone de message](media/teams-contacts-message-box.png)

2. <span data-ttu-id="15c83-143">Dans la zone **Business Central**, commencez à saisir le texte de recherche, comme un nom, une adresse ou un numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="15c83-143">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="15c83-144">Au fur et à mesure de votre saisie, les résultats correspondants s'affichent.</span><span class="sxs-lookup"><span data-stu-id="15c83-144">As you type, matching results will appear.</span></span>

    ![Rechercher les contacts Business Central à partir de la zone de message](media/teams-contacts-5.png)
3. <span data-ttu-id="15c83-146">Sélectionnez un contact parmi les résultats.</span><span class="sxs-lookup"><span data-stu-id="15c83-146">Select a contact from the results.</span></span>

    <span data-ttu-id="15c83-147">La carte de visite apparaît dans la zone de rédaction du message.</span><span class="sxs-lookup"><span data-stu-id="15c83-147">The contact card appears in the message compose box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="15c83-148">La carte de visite n'est pas immédiatement envoyée à la conversation pour que les autres puissent la voir.</span><span class="sxs-lookup"><span data-stu-id="15c83-148">The contact card isn't sent to the conversation right away for others to see.</span></span> <span data-ttu-id="15c83-149">Vous avez la possibilité de revoir le contenu de la carte et d'ajouter du texte avant ou après celle-ci à votre guise.</span><span class="sxs-lookup"><span data-stu-id="15c83-149">You have the opportunity to review the contents of the card, and add text before or after it as you like.</span></span> <span data-ttu-id="15c83-150">Ensuite, envoyez votre message au chat lorsque vous êtes prêt.</span><span class="sxs-lookup"><span data-stu-id="15c83-150">Then, send your message to the chat when ready.</span></span>

### <a name="heres-another-way"></a><span data-ttu-id="15c83-151">Voici une autre façon</span><span class="sxs-lookup"><span data-stu-id="15c83-151">Here's another way</span></span>

1. <span data-ttu-id="15c83-152">Au lieu d'utiliser l'icône **Business Central**, saisissez **@Business Central** directement dans la zone de rédaction du message.</span><span class="sxs-lookup"><span data-stu-id="15c83-152">Instead of using the **Business Central** icon, type **@Business Central** directly in the message compose box.</span></span>
2. <span data-ttu-id="15c83-153">Entrez vos termes de recherche dans la zone.</span><span class="sxs-lookup"><span data-stu-id="15c83-153">Enter your search terms in the box.</span></span>
3. <span data-ttu-id="15c83-154">Utilisez les touches fléchées haut et bas du clavier pour choisir un contact, puis appuyez sur Entrée pour le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="15c83-154">Use the up and down arrow keys on the keyboard to choose a contact, then press Enter to select it.</span></span>

## <a name="viewing-contact-card-details"></a><span data-ttu-id="15c83-155">Affichage des détails de la carte de visite</span><span class="sxs-lookup"><span data-stu-id="15c83-155">Viewing contact card details</span></span>

<span data-ttu-id="15c83-156">La carte de visite dans Teams vous donne un aperçu rapide du client, du fournisseur ou du contact.</span><span class="sxs-lookup"><span data-stu-id="15c83-156">The contact card in Teams gives you a quick overview of the customer, vendor, or contact.</span></span> <span data-ttu-id="15c83-157">La carte est interactive,&mdash;ce qui signifie que vous pouvez afficher plus d'informations ou même modifier un contact en utilisant les boutons **Détails** ou **Contextuel**.</span><span class="sxs-lookup"><span data-stu-id="15c83-157">The card is interactive&mdash;meaning you can view more information or even modify a contact by using the **Details** or **Pop-out** buttons.</span></span>

<span data-ttu-id="15c83-158">Le bouton **Détails** ouvre une fenêtre dans Teams qui affiche plus d'informations sur le contact, mais pas autant que ce que vous verriez dans [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="15c83-158">The **Details** button opens a window within Teams that displays more information about the contact, but not as much as you'd see in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="15c83-159">Pour voir toutes les informations sur un contact dans [!INCLUDE [prod_short](includes/prod_short.md)], sélectionnez **Contextuel**.</span><span class="sxs-lookup"><span data-stu-id="15c83-159">To see all the information about a contact in [!INCLUDE [prod_short](includes/prod_short.md)], select **Pop-out**.</span></span>

<span data-ttu-id="15c83-160">La carte de visite fonctionne exactement comme les cartes pour les enregistrements, comme les articles, les clients ou les commandes client.</span><span class="sxs-lookup"><span data-stu-id="15c83-160">The contact card works just like cards for records, like items, customers, or sales orders.</span></span> <span data-ttu-id="15c83-161">Pour plus d'informations sur les cartes, voir [Afficher les détails de la carte](across-working-with-teams.md#view-card-details).</span><span class="sxs-lookup"><span data-stu-id="15c83-161">For more information about cards, see [View card details](across-working-with-teams.md#view-card-details).</span></span>

> [!NOTE]
> <span data-ttu-id="15c83-162">Tous les participants à une conversation Teams pourront afficher les fiches des contacts Business Central que vous soumettez à une conversation.</span><span class="sxs-lookup"><span data-stu-id="15c83-162">All participants in a Teams conversation will be able to view cards for Business Central contact that you submit to a conversation.</span></span> <span data-ttu-id="15c83-163">Mais pour afficher plus de détails sur les enregistrements, en utilisant les boutons **Détails** ou **Contextuel** sur une fiche, ils auront besoin d’accéder à [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="15c83-163">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="15c83-164">Pour plus d’informations, voir [Gestion de l’intégration Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="15c83-164">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="see-also"></a><span data-ttu-id="15c83-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15c83-165">See Also</span></span>

[<span data-ttu-id="15c83-166">Vue d’ensemble de l’intégration de Business Central et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="15c83-166">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="15c83-167">[Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="15c83-167">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="15c83-168">FAQ Teams</span><span class="sxs-lookup"><span data-stu-id="15c83-168">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="15c83-169">Résolution des incidents dans Teams</span><span class="sxs-lookup"><span data-stu-id="15c83-169">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="15c83-170">Développement pour l’intégration de Teams</span><span class="sxs-lookup"><span data-stu-id="15c83-170">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]