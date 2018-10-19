---
title: "Gérer les utilisateurs et les rôles | Microsoft Docs"
description: "Découvrez comment gérer les utilisateurs et les tableaux de bord dans Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="83f73-103">Comprendre les utilisateurs, les profils et les tableaux de bord</span><span class="sxs-lookup"><span data-stu-id="83f73-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="83f73-104">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les utilisateurs sont ajoutés par un administrateur qui permet également aux utilisateurs d'accéder aux zones de [!INCLUDE[d365fin](includes/d365fin_md.md)] qu'ils ont besoin dans leur travail.</span><span class="sxs-lookup"><span data-stu-id="83f73-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="83f73-105">L'accès aux fonctionnalités est géré via des *groupes d'utilisateurs* et des *profils*.</span><span class="sxs-lookup"><span data-stu-id="83f73-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="83f73-106">En tant qu'administrateur, vous pouvez ajouter et supprimer des utilisateurs dans le cadre de votre abonnement [!INCLUDE[d365fin](includes/d365fin_md.md)], et vous pouvez affecter des autorisations aux utilisateurs par le biais des groupes d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="83f73-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="83f73-107">Ajout d'utilisateurs</span><span class="sxs-lookup"><span data-stu-id="83f73-107">Adding Users</span></span>

<span data-ttu-id="83f73-108">Pour ajouter des utilisateurs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] online, l'administrateur Office 365 de votre société doit d'abord créer les utilisateurs dans le centre d’administration Office 365.</span><span class="sxs-lookup"><span data-stu-id="83f73-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="83f73-109">Pour plus d'informations, voir [Ajouter des utilisateurs à Office 365 for business](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="83f73-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="83f73-110">Ensuite, l'administrateur peut affecter des autorisations à chaque utilisateur et groupe d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="83f73-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="83f73-111">Pour plus d'informations, voir [Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="83f73-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="83f73-112">Utilisateurs des déploiements sur site</span><span class="sxs-lookup"><span data-stu-id="83f73-112">Users of on-premises deployments</span></span>

<span data-ttu-id="83f73-113">Pour les déploiements sur site de [!INCLUDE[d365fin](includes/d365fin_md.md)], l'administrateur peut choisir entre différents mécanismes d'autorisation d'identification pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="83f73-113">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="83f73-114">Ensuite, lorsque vous créez un utilisateur, vous devez fournir différentes informations selon le type d'identification utilisé dans l'instance de [!INCLUDE[server](includes/server.md)] spécifique.</span><span class="sxs-lookup"><span data-stu-id="83f73-114">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="83f73-115">Pour plus d'informations, voir [Authentification et informations d'identification](/dynamics365/business-central/dev-itpro/administration/users-credential-types) dans la section Administration du contenu pour développeurs et professionnels de l'informatique de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="83f73-115">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="83f73-116">Profils</span><span class="sxs-lookup"><span data-stu-id="83f73-116">Profiles</span></span>

<span data-ttu-id="83f73-117">Un *profil* est affecté à tous les employés de votre société ayant accès à [!INCLUDE[d365fin](includes/d365fin_md.md)], qui leur permet d'accéder à un *Tableau de bord*.</span><span class="sxs-lookup"><span data-stu-id="83f73-117">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="83f73-118">Les profils sont des collections d'utilisateurs [!INCLUDE[d365fin](includes/d365fin_md.md)] qui partagent le même tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="83f73-118">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="83f73-119">Un tableau de bord est le point d'entrée et la page d'accueil de [!INCLUDE[d365fin](includes/d365fin_md.md)] qui vous permet d'accéder rapidement à vos tâches les plus importantes et d'afficher diverses informations et divers indicateurs de performance clés sur votre travail.</span><span class="sxs-lookup"><span data-stu-id="83f73-119">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="83f73-120">Dans la version actuelle de [!INCLUDE[d365fin](includes/d365fin_md.md)] online, vous ne pouvez ni ajouter, ni modifier, ni supprimer des profils.</span><span class="sxs-lookup"><span data-stu-id="83f73-120">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="83f73-121">Configuration et personnalisation</span><span class="sxs-lookup"><span data-stu-id="83f73-121">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
<span data-ttu-id="83f73-122">Les utilisateurs personnalisent l'interface utilisateur de leur version personnelle en personnalisant l'interface utilisateur sous leur propre identifiant utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83f73-122">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="83f73-123">Cette personnalisation peut être supprimée par l'administrateur.</span><span class="sxs-lookup"><span data-stu-id="83f73-123">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="83f73-124">Pour plus d'informations, voir [Personnalisation de votre espace de travail](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="83f73-124">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="83f73-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83f73-125">See Also</span></span>  
[<span data-ttu-id="83f73-126">Gestion des utilisateurs et des autorisations</span><span class="sxs-lookup"><span data-stu-id="83f73-126">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="83f73-127">Gérer la personnalisation en tant qu'administrateur</span><span class="sxs-lookup"><span data-stu-id="83f73-127">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="83f73-128">Personnalisation de votre espace de travail</span><span class="sxs-lookup"><span data-stu-id="83f73-128">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

