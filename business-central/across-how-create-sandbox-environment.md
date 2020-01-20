---
title: Créer un environnement Sandbox | Microsoft Docs
description: Créez un environnement à des fins d'exploration, d'apprentissage, de démonstration, de développement et de test.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 12/10/2019
ms.author: solsen
ms.openlocfilehash: 7d189ab6fa5aff518b643c797b7600570fcad43e
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910651"
---
# <a name="creating-a-sandbox-environment-in-include-prodshortincludesprodshortmd"></a><span data-ttu-id="b598a-103">Créeation d'un environnement Sandbox dans [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="b598a-103">Creating a Sandbox Environment in [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="b598a-104">Avec [!INCLUDE [prodshort](includes/prodshort.md)], vous pouvez facilement créer un environnement sûr dans lequel vous pouvez tester, former ou résoudre les problèmes sans perturber les processus de travail ou les données métier de votre société.</span><span class="sxs-lookup"><span data-stu-id="b598a-104">With [!INCLUDE [prodshort](includes/prodshort.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="b598a-105">Cet environnement hors production est appelé *sandbox*.</span><span class="sxs-lookup"><span data-stu-id="b598a-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="b598a-106">Isolé de la production, un environnement Sandbox est l'emplacement où vous pouvez explorer, apprendre, démontrer, développer et tester en toute sécurité le service sans que les données et les paramètres de votre environnement de production en soient affectés.</span><span class="sxs-lookup"><span data-stu-id="b598a-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="b598a-107">Votre administrateur peut créer des environnements sandbox dans le [centre d'administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), mais si vous voulez effectuer un test rapide, vous pouvez créer un environnement sandbox depuis [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="b598a-107">Your administrator can create sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

> [!NOTE]
> <span data-ttu-id="b598a-108">Techniquement, les environnements sandbox sont très différents des environnements de production, même si votre administrateur crée un sandbox incluant des données de production.</span><span class="sxs-lookup"><span data-stu-id="b598a-108">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="b598a-109">Vous ne pouvez pas utiliser un sandbox à des fins d'évaluation, et vous ne pouvez pas demander une exportation de base de données, par exemple.</span><span class="sxs-lookup"><span data-stu-id="b598a-109">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="b598a-110">Si vous souhaitez créer un sandbox à des fins d'évaluation, votre administrateur peut créer un environnement de production dédié dans le centre d'administration.</span><span class="sxs-lookup"><span data-stu-id="b598a-110">If you want to create a sandbox for benchmarking, your administrator can create a dedicated production environment in the administration center.</span></span> <span data-ttu-id="b598a-111">Pour plus d'informations, voir [Types d'environnements](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span><span class="sxs-lookup"><span data-stu-id="b598a-111">For more information, see [Types of environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-include-prodshortincludesprodshortmd"></a><span data-ttu-id="b598a-112">Pour créer un environnement sandbox dans votre [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="b598a-112">To create a sandbox environment in your [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

1. <span data-ttu-id="b598a-113">Connectez-vous à votre instance de production de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b598a-113">Sign in to your production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

2. <span data-ttu-id="b598a-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Environnement sandbox**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="b598a-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="b598a-115">Cliquez sur le bouton **Créer**.</span><span class="sxs-lookup"><span data-stu-id="b598a-115">Choose the **Create** button.</span></span>  

    <span data-ttu-id="b598a-116">Un autre onglet avec [!INCLUDE[d365fin](includes/d365fin_md.md)] s'ouvre à l'endroit où vous pouvez terminer la configuration de votre environnement Sandbox.</span><span class="sxs-lookup"><span data-stu-id="b598a-116">Another tab with [!INCLUDE[d365fin](includes/d365fin_md.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="b598a-117">Si le bloqueur de fenêtres publicitaires est activé dans votre navigateur, modifiez-le pour autoriser les URL provenant de l'adresse \*.businesscentral.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="b598a-117">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="b598a-118">Lorsque l'environnement Sandbox est prêt, vous êtes redirigé vers l'assistant Bienvenue de l'environnement Sandbox.</span><span class="sxs-lookup"><span data-stu-id="b598a-118">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="b598a-119">Vous pouvez choisir le bouton **En savoir plus** pour en savoir plus sur les scénarios de développeur que vous pouvez essayer dans un environnement sandbox, ou choisir le bouton **Fermer** pour passer au Tableau de bord de votre instance sandbox [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b598a-119">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>

<span data-ttu-id="b598a-120">En haut du tableau de bord, une notification s'affiche pour vous informer qu'il s'agit d'un environnement Sandbox.</span><span class="sxs-lookup"><span data-stu-id="b598a-120">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="b598a-121">Vous pouvez également voir le type de l'environnement dans la barre de titre du client.</span><span class="sxs-lookup"><span data-stu-id="b598a-121">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="b598a-122">Un environnement Sandbox créé de cette manière ne contient que les données de démonstration par défaut pour l'entreprise CRONUS.</span><span class="sxs-lookup"><span data-stu-id="b598a-122">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="b598a-123">Aucune donnée n'est copiée ou autrement transférée à partir de l'environnement de production.</span><span class="sxs-lookup"><span data-stu-id="b598a-123">No data is copied or otherwise transferred from the production environment.</span></span><br /><br />
> <span data-ttu-id="b598a-124">Vous pouvez également créer un environnement Sandbox contenant les données de production.</span><span class="sxs-lookup"><span data-stu-id="b598a-124">You can also create a sandbox environment containing the production data.</span></span> <span data-ttu-id="b598a-125">Vous devez le faire via le Centre d'administration.</span><span class="sxs-lookup"><span data-stu-id="b598a-125">You must do this through the administration center.</span></span> <span data-ttu-id="b598a-126">Pour plus d'informations, voir [Gestion des environnements](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) dans l'aide sur Developer and IT Pro.</span><span class="sxs-lookup"><span data-stu-id="b598a-126">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the Developer and IT-Pro help.</span></span>

<span data-ttu-id="b598a-127">À tout moment, vous pouvez revenir à la page **Environnement Sandbox** et réinitialiser l'environnement Sandbox.</span><span class="sxs-lookup"><span data-stu-id="b598a-127">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>

> [!NOTE]  
> <span data-ttu-id="b598a-128">La réinitialisation de l'environnement Sandbox entraîne sa suppression complète et sa recréation avec les données de démonstration par défaut.</span><span class="sxs-lookup"><span data-stu-id="b598a-128">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="b598a-129">Un administrateur peut limiter ou même bloquer l'accès de certains utilisateurs à l'environnement sandbox.</span><span class="sxs-lookup"><span data-stu-id="b598a-129">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="b598a-130">Ceci peut être effectué à l'aide des fonctions de sécurité standard du produit, telles que la fiche utilisateur, les groupes d'utilisateurs et les ensembles d'autorisations.</span><span class="sxs-lookup"><span data-stu-id="b598a-130">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="b598a-131">Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="b598a-131">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="b598a-132">Fonctionnalités avancées de l'environnement Sandbox</span><span class="sxs-lookup"><span data-stu-id="b598a-132">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="b598a-133">L'environnement sandbox n'est pas moins utile, car il comprend quelques fonctionnalités pratiques.</span><span class="sxs-lookup"><span data-stu-id="b598a-133">The sandbox environment is not least useful because it includes a couple of handy features.</span></span>

### <a name="designer"></a><span data-ttu-id="b598a-134">Concepteur</span><span class="sxs-lookup"><span data-stu-id="b598a-134">Designer</span></span>

<span data-ttu-id="b598a-135">Dans un environnement sandbox, la fonctionnalité **Concepteur** est activée.</span><span class="sxs-lookup"><span data-stu-id="b598a-135">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="b598a-136">Vous pouvez activer la fonctionnalité Éditeur en sélectionnant l'icône de conception ![Concepteur](./media/across-sandbox/sandbox-inclient-design-icon.png) sur une page, ou en choisissant l'option de menu **Conception** dans le menu Paramètres ![Paramètres ](media/ui-experience/settings_icon_small.png).</span><span class="sxs-lookup"><span data-stu-id="b598a-136">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a><span data-ttu-id="b598a-137">Pour activer l'expérience utilisateur avancée</span><span class="sxs-lookup"><span data-stu-id="b598a-137">To enable the advanced user experience</span></span>
<span data-ttu-id="b598a-138">Il est possible d'activer et de tester la fonctionnalité complète de la version standard de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans un abonné Sandbox en définissant le champ **Expérience** sur la page **Informations société**.</span><span class="sxs-lookup"><span data-stu-id="b598a-138">It is possible to enable and try the full functionality of the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="b598a-139">Après avoir activé l'expérience utilisateur *Premium*, vous avez accès à tous les profils (rôles) et tableaux de bord standard dans la version standard.</span><span class="sxs-lookup"><span data-stu-id="b598a-139">After you have enabled the *Premium* user experience, you get access to all the standard profiles (roles) and Role Centers in the standard version.</span></span> <span data-ttu-id="b598a-140">Vous pouvez également créer une société d'évaluation qui est entièrement configurée, notamment les données de démonstration et l'accès aux zones avancées du produit.</span><span class="sxs-lookup"><span data-stu-id="b598a-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span> <span data-ttu-id="b598a-141">Vous pouvez également contacter un partenaire revendeur pour une démonstration des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="b598a-141">Alternatively, contact a reselling partner for a demonstration of the capabilities.</span></span> <span data-ttu-id="b598a-142">Pour plus d'informations, voir [Comment trouver un partenaire revendeur ?](across-faq.md#findpartner).</span><span class="sxs-lookup"><span data-stu-id="b598a-142">For more information, see [How do I find a reselling partner?](across-faq.md#findpartner).</span></span>  

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a><span data-ttu-id="b598a-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b598a-143">See Also</span></span>

<span data-ttu-id="b598a-144">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b598a-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="b598a-145">Versions d'évaluation et abonnements [[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="b598a-145">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="b598a-146">Gestion des environnements dans le centre d'administration de Business Central</span><span class="sxs-lookup"><span data-stu-id="b598a-146">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
