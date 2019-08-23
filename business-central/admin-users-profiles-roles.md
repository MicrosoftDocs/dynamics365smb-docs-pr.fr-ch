---
title: Gérer les utilisateurs et les rôles | Microsoft Docs
description: Découvrez comment gérer les utilisateurs et les tableaux de bord dans Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 08/02/2019
ms.author: edupont
ms.openlocfilehash: 27a57490101195f8dc05cc39538260e7db5e46af
ms.sourcegitcommit: 5bcc5f95e450ee9a3d9f7a380e592a5e75c4185b
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 08/05/2019
ms.locfileid: "1858235"
---
# <a name="understanding-users-roles-and-profiles"></a><span data-ttu-id="32d80-103">Comprendre les utilisateurs, rôles et profils</span><span class="sxs-lookup"><span data-stu-id="32d80-103">Understanding Users, Roles, and Profiles</span></span>

<span data-ttu-id="32d80-104">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les utilisateurs sont ajoutés par un administrateur qui permet également aux utilisateurs d'accéder aux zones de [!INCLUDE[d365fin](includes/d365fin_md.md)] qu'ils ont besoin dans leur travail.</span><span class="sxs-lookup"><span data-stu-id="32d80-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="32d80-105">L'accès aux fonctionnalités est géré via des *groupes d'utilisateurs* et des *profils (rôles)*.</span><span class="sxs-lookup"><span data-stu-id="32d80-105">Access to functionality is managed through *user groups* and *profiles (roles)*.</span></span> <span data-ttu-id="32d80-106">En tant qu'administrateur, vous pouvez ajouter et supprimer des utilisateurs dans le cadre de votre abonnement [!INCLUDE[d365fin](includes/d365fin_md.md)], et vous pouvez affecter des autorisations aux utilisateurs par le biais des groupes d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="32d80-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="32d80-107">Ajout d'utilisateurs</span><span class="sxs-lookup"><span data-stu-id="32d80-107">Adding Users</span></span>

<span data-ttu-id="32d80-108">Pour ajouter des utilisateurs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] online, l'administrateur Office 365 de votre société doit d'abord créer les utilisateurs dans le centre d’administration Office 365.</span><span class="sxs-lookup"><span data-stu-id="32d80-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="32d80-109">Pour plus d'informations, voir [Ajouter des utilisateurs à Office 365 for business](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="32d80-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="32d80-110">Ensuite, l'administrateur peut affecter des autorisations à chaque utilisateur et groupe d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="32d80-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="32d80-111">Pour plus d'informations, voir [Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="32d80-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

<span data-ttu-id="32d80-112">Les autorisations les plus puissantes qu'un utilisateur peut avoir est l'ensemble d'autorisations SUPER.</span><span class="sxs-lookup"><span data-stu-id="32d80-112">The most powerful permissions that a user can have is the SUPER permission set.</span></span> <span data-ttu-id="32d80-113">Chaque société doit avoir au moins un utilisateur ayant cet ensemble d'autorisations, mais il est recommandé d'attribuer à chaque utilisateur des autorisations correspondant à leurs besoins de travail dans [!INCLUDE[prodshort](includes/prodshort.md)] et pas plus que cela.</span><span class="sxs-lookup"><span data-stu-id="32d80-113">Each company must have at least one user with this permission set, but it is a best practice to give each user permissions that match their work needs in [!INCLUDE[prodshort](includes/prodshort.md)] and not more than that.</span></span> <span data-ttu-id="32d80-114">Cela permet de s'assurer que les utilisateurs ont uniquement accès aux données adéquates pour leur travail, par exemple.</span><span class="sxs-lookup"><span data-stu-id="32d80-114">This helps ensure that users only have access to data that is relevant to their work, for example.</span></span>  

> [!TIP]
> <span data-ttu-id="32d80-115">Il est recommandé de vous assurer que l'administrateur Office 365 a également l'ensemble d'autorisations SUPER dans [!INCLUDE[prodshort](includes/prodshort.md)] car cela facilite de nombreuses tâches administratives, notamment la configuration de l'intégration à d'autres applications.</span><span class="sxs-lookup"><span data-stu-id="32d80-115">It's a best practice to make sure that the Office 365 administrator also has the SUPER permission set in [!INCLUDE[prodshort](includes/prodshort.md)] because that makes many administrative tasks easier, including setting up integration with other apps.</span></span>

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="32d80-116">Utilisateurs des déploiements sur site</span><span class="sxs-lookup"><span data-stu-id="32d80-116">Users of on-premises deployments</span></span>

<span data-ttu-id="32d80-117">Pour les déploiements sur site de [!INCLUDE[d365fin](includes/d365fin_md.md)], l'administrateur peut choisir entre différents mécanismes d'autorisation d'identification pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="32d80-117">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="32d80-118">Ensuite, lorsque vous créez un utilisateur, vous devez fournir différentes informations selon le type d'identification utilisé dans l'instance de [!INCLUDE[server](includes/server.md)] spécifique.</span><span class="sxs-lookup"><span data-stu-id="32d80-118">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="32d80-119">Pour plus d'informations, voir [Authentification et informations d'identification](/dynamics365/business-central/dev-itpro/administration/users-credential-types) dans la section Administration du contenu pour développeurs et professionnels de l'informatique de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="32d80-119">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles-roles"></a><span data-ttu-id="32d80-120">Profils (Rôles)</span><span class="sxs-lookup"><span data-stu-id="32d80-120">Profiles (Roles)</span></span>

<span data-ttu-id="32d80-121">Un rôle est affecté à tous les employés de votre société ayant accès à [!INCLUDE[d365fin](includes/d365fin_md.md)], qui leur permet d'accéder à un *Tableau de bord*.</span><span class="sxs-lookup"><span data-stu-id="32d80-121">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a role that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="32d80-122">Les profils sont des collections d'utilisateurs [!INCLUDE[d365fin](includes/d365fin_md.md)] qui partagent le même rôle.</span><span class="sxs-lookup"><span data-stu-id="32d80-122">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same role.</span></span> <span data-ttu-id="32d80-123">Un tableau de bord est le point d'entrée et la page d'accueil de [!INCLUDE[d365fin](includes/d365fin_md.md)] qui vous permet d'accéder rapidement à vos tâches les plus importantes et d'afficher diverses informations et divers indicateurs de performance clés sur votre travail.</span><span class="sxs-lookup"><span data-stu-id="32d80-123">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="32d80-124">Dans la version actuelle de [!INCLUDE[d365fin](includes/d365fin_md.md)] online, vous ne pouvez ni ajouter, ni modifier, ni supprimer des profils.</span><span class="sxs-lookup"><span data-stu-id="32d80-124">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

### <a name="CreateProfile"></a><span data-ttu-id="32d80-125">Pour créer un profil</span><span class="sxs-lookup"><span data-stu-id="32d80-125">To create a profile</span></span>

1.  <span data-ttu-id="32d80-126">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Profils**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="32d80-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profiles**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="32d80-127">Sur la page **Profils**, choisissez l'action **Nouveau** pour ouvrir la page **Fiche nouveau profil**.</span><span class="sxs-lookup"><span data-stu-id="32d80-127">On the **Profiles** page, choose the **New** action to open the **New Profile Card** page.</span></span>  

3.  <span data-ttu-id="32d80-128">Dans le champ **ID profil**, entrez un nom qui décrit le rôle prévu pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="32d80-128">In the **Profile ID** field, enter a name that describes the intended role of the users.</span></span>  

4.  <span data-ttu-id="32d80-129">Dans le champ **Description**, entrez une description de l'ID profil, par exemple, **Préparateur de la commande**.</span><span class="sxs-lookup"><span data-stu-id="32d80-129">In the **Description** field, enter a description of the Profile ID, for example, **Order Processor**.</span></span>  

5.  <span data-ttu-id="32d80-130">Définissez le champ **ID Tableau de bord** sur le Tableau de bord à affecter au profil.</span><span class="sxs-lookup"><span data-stu-id="32d80-130">Set the **Role Center ID** field to the Role Center that you want to assign to the profile.</span></span>  

<span data-ttu-id="32d80-131">La procédure à suivre pour modifier un profil existant est la même, à la différence près que vous sélectionnez un profil existant dans la page **Profils** au lieu de choisir l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="32d80-131">The procedure for modifying an existing profile is the same, except you select an existing profile on the **Profiles** page instead of choosing the **New** action.</span></span>  


### <a name="copy-a-profile"></a><span data-ttu-id="32d80-132">Copier un profil</span><span class="sxs-lookup"><span data-stu-id="32d80-132">Copy a profile</span></span>
<span data-ttu-id="32d80-133">La copie d'un profil vous permet de gagner du temps si vous voulez utiliser des paramètres similaires pour un profil et modifier uniquement certains paramètres.</span><span class="sxs-lookup"><span data-stu-id="32d80-133">Copying a profile can save you time if you want to use similar settings on a profile and you only want to change a few settings.</span></span>

1.  <span data-ttu-id="32d80-134">Ouvrez le profil que vous voulez copier, puis sélectionnez l'action **Copier le profil**.</span><span class="sxs-lookup"><span data-stu-id="32d80-134">Open the profile that you want to copy, and then choose the **Copy Profile** action.</span></span>

2.  <span data-ttu-id="32d80-135">Dans le champ **ID nouveau profil**, entrez un nom pour le profil que vous voulez copier.</span><span class="sxs-lookup"><span data-stu-id="32d80-135">In **New Profile ID** field, enter a name for the profile that you want to copy.</span></span>

3.  <span data-ttu-id="32d80-136">Définissez le champ **Portée du nouveau profil** comme l'un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="32d80-136">Set the **New Profile Scope** field to one of the following:</span></span>

    - <span data-ttu-id="32d80-137">**Système** pour rendre le nouveau profil disponible à toutes les bases de données d'abonné qui utilisent l'application.</span><span class="sxs-lookup"><span data-stu-id="32d80-137">**System** to make the new profile available to all tenant databases that use the application.</span></span>
    - <span data-ttu-id="32d80-138">**Abonné** pour rendre le nouveau profil disponible uniquement à la base de données actuelle de l'abonné.</span><span class="sxs-lookup"><span data-stu-id="32d80-138">**Tenant** to make the new profile available to just the current tenant database.</span></span>
4. <span data-ttu-id="32d80-139">Lorsque vous avez terminé, choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="32d80-139">Choose the **OK** button when done.</span></span>

### <a name="ExportImportProfile"></a><span data-ttu-id="32d80-140">Exporter et importer des profils</span><span class="sxs-lookup"><span data-stu-id="32d80-140">Export and import profiles</span></span>

<span data-ttu-id="32d80-141">Vous pouvez exporter et importer des profils en tant que fichiers XML depuis et vers une base de données [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="32d80-141">You can export and import profiles as XML files to and from the a [!INCLUDE[d365fin](includes/d365fin_md.md)] database.</span></span> <span data-ttu-id="32d80-142">L'exportation et l'importation de profils vous permettent de gagner du temps lors de la configuration de l'interface utilisateur, car vous réutilisez une configuration de profil existante au lieu d'en configurer un en partant de zéro.</span><span class="sxs-lookup"><span data-stu-id="32d80-142">Exporting and importing a profile can save you time when configuring the user interface because you reuse an existing profile configuration instead of having to configure a profile from scratch.</span></span> <span data-ttu-id="32d80-143">Si vous avez un profil qui est configuré dans une base de données [!INCLUDE[d365fin](includes/d365fin_md.md)] et que vous souhaitez réutiliser tout ou partie de cette configuration dans une autre base de données, vous pouvez exporter le profil vers un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="32d80-143">If you have a profile that is configured in a [!INCLUDE[d365fin](includes/d365fin_md.md)] database and you would like to reuse all or some of the same profile configurations in another database, you can export the profile to an XML file.</span></span> <span data-ttu-id="32d80-144">Ensuite, vous pouvez importer le fichier XML du profil dans l'autre base de données.</span><span class="sxs-lookup"><span data-stu-id="32d80-144">Then, you can import the profile XML file into the other database.</span></span>

-   <span data-ttu-id="32d80-145">Pour exporter un profil, vous pouvez choisir l'action **Exporter les profils** dans la **Liste des profils** ou la page **Fiche profil**, ou vous pouvez rechercher et ouvrir la page **Exporter les profils**.</span><span class="sxs-lookup"><span data-stu-id="32d80-145">To export a profile, you can either choose the **Export Profiles** action from the **Profile List** or **Profile Card** page or you can search for and open the **Export Profiles** page.</span></span> <span data-ttu-id="32d80-146">Enregistrez le fichier XML dans un emplacement de votre ordinateur ou du réseau.</span><span class="sxs-lookup"><span data-stu-id="32d80-146">Save the XML file to a location on your computer or network.</span></span>

-   <span data-ttu-id="32d80-147">Pour importer un profil, vous pouvez choisir l'action **Importer les profils** dans la **Liste des profils**, ou vous pouvez rechercher et ouvrir la page **Importer les profils**.</span><span class="sxs-lookup"><span data-stu-id="32d80-147">To import a profile, you can either choose the **Import Profile** action from the **Profile List** page, or you can search for and open the **Import Profiles** page.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="32d80-148">Vous ne pouvez pas importer un profil existant déjà dans la base de données, même si le fichier XML est nommé ou contient un contenu différent.</span><span class="sxs-lookup"><span data-stu-id="32d80-148">You cannot import a profile that already exists in the database, even though the XML file is named differently or has different content.</span></span> <span data-ttu-id="32d80-149">Vous devez supprimer le profil existant avant de pouvoir importer le nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="32d80-149">You must delete the existing profile before you can import the new profile.</span></span>


## <a name="configuration-and-personalization"></a><span data-ttu-id="32d80-150">Configuration et personnalisation</span><span class="sxs-lookup"><span data-stu-id="32d80-150">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

<span data-ttu-id="32d80-151">Les utilisateurs personnalisent l'interface utilisateur de leur version personnelle en personnalisant l'interface utilisateur sous leur propre identifiant utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32d80-151">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="32d80-152">Cette personnalisation peut être supprimée par l'administrateur.</span><span class="sxs-lookup"><span data-stu-id="32d80-152">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="32d80-153">Pour plus d'informations, voir [Personnalisation de votre espace de travail](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="32d80-153">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="32d80-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32d80-154">See Also</span></span>  
[<span data-ttu-id="32d80-155">Gestion des utilisateurs et des autorisations</span><span class="sxs-lookup"><span data-stu-id="32d80-155">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="32d80-156">Gérer la personnalisation en tant qu'administrateur</span><span class="sxs-lookup"><span data-stu-id="32d80-156">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="32d80-157">Personnalisation de votre espace de travail</span><span class="sxs-lookup"><span data-stu-id="32d80-157">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
