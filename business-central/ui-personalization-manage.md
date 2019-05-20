---
title: Gérer la personnalisation en tant qu'administrateur dans Business Central | Microsoft Docs
description: Découvrez comment personnaliser l'interface utilisateur pour l'adapter à votre méthode de travail.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250610"
---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="e3702-103">Gérer la personnalisation en tant qu'administrateur</span><span class="sxs-lookup"><span data-stu-id="e3702-103">Managing Personalization as an Administrator</span></span>

<span data-ttu-id="e3702-104"> Les utilisateurs peuvent personnaliser leur espace de travail en fonction de leurs propres préférences.</span><span class="sxs-lookup"><span data-stu-id="e3702-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="e3702-105">En tant qu'administrateur, vous contrôlez et gérez la personnalisation comme suit :</span><span class="sxs-lookup"><span data-stu-id="e3702-105">As an administrator, you control and manage personalization by:</span></span>

-   <span data-ttu-id="e3702-106">En activant ou désactivant la personnalisation pour l'intégralité de l'application (installation locale uniquement).</span><span class="sxs-lookup"><span data-stu-id="e3702-106">Enabling or disabling the personalization feature for the entire the application (on-premises installation only).</span></span>
-   <span data-ttu-id="e3702-107">En activant ou désactivant la personnalisation pour les utilisateurs d'un profil spécifique.</span><span class="sxs-lookup"><span data-stu-id="e3702-107">Enabling or disabling the personalization feature for users of a specific profile.</span></span>
-   <span data-ttu-id="e3702-108">En annulant toute personnalisation de page effectuée par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e3702-108">Clearing any page personalizations that users have made.</span></span>

## <a name="EnablePersonalization"></a><span data-ttu-id="e3702-109">Pour activer ou désactiver la personnalisation (en local uniquement)</span><span class="sxs-lookup"><span data-stu-id="e3702-109">To enable or disable personalization (On-Premises Only)</span></span>

<span data-ttu-id="e3702-110">Par défaut, la personnalisation n'est pas activée dans le client.</span><span class="sxs-lookup"><span data-stu-id="e3702-110">By default, personalization is not enabled in the client.</span></span> <span data-ttu-id="e3702-111">Vous activez ou désactivez la personnalisation en modifiant le fichier de configuration (navesttings.json) de l'instance du serveur Web Business Central qui dessert les clients.</span><span class="sxs-lookup"><span data-stu-id="e3702-111">You enable or disable personalization by modifying the configuration file (navsettings.json) of the Business Central Web Server instance that serves the clients.</span></span>

1. <span data-ttu-id="e3702-112">Pour activer la personnalisation, ajoutez la ligne suivante dans le fichier navsettings.json :</span><span class="sxs-lookup"><span data-stu-id="e3702-112">To enable personalization, add the following line in the navsettings.json file:</span></span>

    ```
    "PersonalizationEnabled": "true"
    ```

    <span data-ttu-id="e3702-113">Pour désactiver la personnalisation, supprimez cette ligne ou changez-la avec :</span><span class="sxs-lookup"><span data-stu-id="e3702-113">To disable personalization, remove this line or change it to:</span></span>

    ```
    "PersonalizationEnabled": "false"
    ```

    <span data-ttu-id="e3702-114">Pour plus d'informations sur la procédure visant à modifier le fichier navsettings.json, reportez-vous à la rubrique [Modifier directement le fichier navsettings.json](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings)</span><span class="sxs-lookup"><span data-stu-id="e3702-114">For more information about how to modify the navsettings.json file, see [Modify the navsettings.json file directly](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span></span>

2. <span data-ttu-id="e3702-115">Générez et téléchargez les symboles d'application.</span><span class="sxs-lookup"><span data-stu-id="e3702-115">Generate and download the application symbols.</span></span>

    <span data-ttu-id="e3702-116">Cette étape est facultative, et non requise pour activer la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="e3702-116">This step is optional, and not required to enable personalization.</span></span> <span data-ttu-id="e3702-117">Toutefois, elle veille à ce que les nouvelles pages qui sont créées par les développeurs puissent être personnalisées.</span><span class="sxs-lookup"><span data-stu-id="e3702-117">However, it ensures that new pages that are created by developers can be personalized.</span></span>

    1. <span data-ttu-id="e3702-118">Tout d'abord, vous générez les symboles en exécutant finsql.exe avec la commande `generatesymbolreference`.</span><span class="sxs-lookup"><span data-stu-id="e3702-118">First, you generate the symbols by running finsql.exe with `generatesymbolreference` command.</span></span> <span data-ttu-id="e3702-119">Le fichier finsql.exe se situe dans le dossier d'installation pour le [!INCLUDE[server](includes/server.md)] et Dynamics NAV Development Environment (CSIDE).</span><span class="sxs-lookup"><span data-stu-id="e3702-119">The finsql.exe file is located in the installation folder for the [!INCLUDE[server](includes/server.md)] and Dynamics NAV Development Environment (CSIDE).</span></span> <span data-ttu-id="e3702-120">Pour générer les symboles, ouvrez une invite de commande, passez au répertoire où est enregistré le fichier, et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e3702-120">To generate the symbols, open a command prompt, change to the directory where the file is store, and the run the following command:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    <span data-ttu-id="e3702-121">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e3702-121">For example:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    <span data-ttu-id="e3702-122">Pour plus d'informations, reportez-vous à la rubrique [Exécution de C/SIDE et d'AL Side-by-Side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span><span class="sxs-lookup"><span data-stu-id="e3702-122">For more information, see [Running C/SIDE and AL Side-by-Side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span></span>

    2. <span data-ttu-id="e3702-123">Configurez l'instance [!INCLUDE[nav_server_md](includes/nav_server_md.md)] sur **Activer l'importation des références de symbole d'application au démarrage du serveur** (EnableSymbolLoadingAtServerStartup).</span><span class="sxs-lookup"><span data-stu-id="e3702-123">Configure [!INCLUDE[nav_server_md](includes/nav_server_md.md)] instance to **Enable loading application symbol references at server startup** (EnableSymbolLoadingAtServerStartup).</span></span> <span data-ttu-id="e3702-124">Pour plus d'informations, reportez-vous à la rubrique [Configuration de Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span><span class="sxs-lookup"><span data-stu-id="e3702-124">For more information, see [Configuring Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span></span>

## <a name="to-disable-personalization-for-a-profile"></a><span data-ttu-id="e3702-125">Pour désactiver la personnalisation pour un profil</span><span class="sxs-lookup"><span data-stu-id="e3702-125">To disable personalization for a profile</span></span>

<span data-ttu-id="e3702-126">Vous pouvez empêcher tous les utilisateurs appartenant à un profil spécifique de personnaliser leurs pages.</span><span class="sxs-lookup"><span data-stu-id="e3702-126">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>

1. <span data-ttu-id="e3702-127">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Profils**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="e3702-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="e3702-128">Sélectionnez dans la liste le profil à modifier.</span><span class="sxs-lookup"><span data-stu-id="e3702-128">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="e3702-129">Activez la case à cocher **Désactiver la personnalisation**, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3702-129">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="to-clear-user-personalizations"></a><span data-ttu-id="e3702-130">Pour annuler les personnalisations des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e3702-130">To clear user personalizations</span></span>

<span data-ttu-id="e3702-131">L'effacement de la personnalisation de la page rétablit la page à sa disposition d'origine, antérieure à toute personnalisation.</span><span class="sxs-lookup"><span data-stu-id="e3702-131">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="e3702-132">Il y a deux méthodes pour effacer les personnalisations de page effectuées par les utilisateurs : en utilisant la page **Supprimer la personnalisation utilisateur** et en utilisant la page **Fiche de personnalisation utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="e3702-132">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="e3702-133">Pour annuler les personnalisations effectuées par les utilisateurs à l'aide de la page Supprimer la personnalisation utilisateur</span><span class="sxs-lookup"><span data-stu-id="e3702-133">To clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="e3702-134">La page **Supprimer la personnalisation utilisateur** permet d'effacer les personnalisations par page et par utilisateur individuellement.</span><span class="sxs-lookup"><span data-stu-id="e3702-134">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1. <span data-ttu-id="e3702-135">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer la personnalisation utilisateur**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="e3702-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="e3702-136">La page répertorie toutes les pages qui ont été personnalisées et l'utilisateur auquel elles appartiennent.</span><span class="sxs-lookup"><span data-stu-id="e3702-136">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="e3702-137">Une coche dans la colonne **Personnalisation héritée** indique si la personnalisation a été effectuée dans une ancienne version de [!INCLUDE[d365fin](includes/d365fin_md.md)], qui a traité la personnalisation de manière différente.</span><span class="sxs-lookup"><span data-stu-id="e3702-137">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="e3702-138">Les utilisateurs qui essaient de personnaliser ces pages sont empêchés de le faire, à moins qu'ils ne choisissent de déverrouiller la page.</span><span class="sxs-lookup"><span data-stu-id="e3702-138">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="e3702-139">Pour plus d'informations, voir [Pourquoi la personnalisation d'une page est bloquée](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="e3702-139">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="e3702-140">Sélectionnez l'écriture à supprimer, puis sélectionnez l'action **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="e3702-140">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="e3702-141">L'utilisateur les verra les modifications lors de sa prochaine connexion.</span><span class="sxs-lookup"><span data-stu-id="e3702-141">The user will see the changes the next time they sign-in.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="e3702-142">Pour annuler les personnalisations utilisateur à l'aide de la page Fiche de personnalisation utilisateur</span><span class="sxs-lookup"><span data-stu-id="e3702-142">To clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="e3702-143">La page **Fiche de personnalisation utilisateur** permet d'effacer la personnalisation de toutes les pages d'un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="e3702-143">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="e3702-144">Cela nécessite l'autorisation d'écriture dans la table 2000000072 **Profil**.</span><span class="sxs-lookup"><span data-stu-id="e3702-144">This requires write permission to Table 2000000072 **Profile**.</span></span>

1. <span data-ttu-id="e3702-145">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Personnalisation utilisateur**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="e3702-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="e3702-146">La page **Personnalisation utilisateur** répertorie tous les utilisateurs qui ont potentiellement des pages personnalisées.</span><span class="sxs-lookup"><span data-stu-id="e3702-146">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="e3702-147">Si vous ne trouvez pas un utilisateur dans la liste, cela signifie qu'ils n'a aucune page personnalisée.</span><span class="sxs-lookup"><span data-stu-id="e3702-147">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="e3702-148">Sélectionnez l'utilisateur dans la liste, puis sélectionnez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="e3702-148">Select the user from the list, and then choose the **Edit** action.</span></span>

3. <span data-ttu-id="e3702-149">Sous l'onglet **Actions**, choisissez **Effacer les pages personnalisées**.</span><span class="sxs-lookup"><span data-stu-id="e3702-149">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="e3702-150">L'utilisateur les verra les modifications lors de sa prochaine connexion.</span><span class="sxs-lookup"><span data-stu-id="e3702-150">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3702-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3702-151">See Also</span></span>
[<span data-ttu-id="e3702-152">Personnalisation de votre espace de travail</span><span class="sxs-lookup"><span data-stu-id="e3702-152">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="e3702-153">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e3702-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="e3702-154">Modification des paramètres de base</span><span class="sxs-lookup"><span data-stu-id="e3702-154">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="e3702-155">Modification des fonctionnalités affichées</span><span class="sxs-lookup"><span data-stu-id="e3702-155">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
