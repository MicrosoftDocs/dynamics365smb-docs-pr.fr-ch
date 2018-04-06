---
title: "Gérer la personnalisation en tant qu'administrateur dans Financials | Microsoft Docs"
description: "Découvrez comment personnaliser l'interface utilisateur pour l'adapter à votre méthode de travail."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d6ab880e7fbce361863140e634ea065a31e3aa70
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="456a0-103">Gérer la personnalisation en tant qu'administrateur</span><span class="sxs-lookup"><span data-stu-id="456a0-103">Managing Personalization as an Administrator</span></span>
<!--NAV in the Web client-->
<span data-ttu-id="456a0-104">Les utilisateurs peuvent personnaliser leur espace de travail en fonction de leurs propres préférences.</span><span class="sxs-lookup"><span data-stu-id="456a0-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="456a0-105">En tant qu'administrateur, vous pouvez contrôler et gérer la personnalisation en désactivant la capacité des utilisateurs à personnaliser des pages et en effaçant toutes les personnalisations de page effectuées par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="456a0-105">As an administrator, you can control and manage personalization by disabling the ability for users to personalize pages and clearing any page personalizations that users have made.</span></span>

## <a name="disable-personalization-for-a-profile"></a><span data-ttu-id="456a0-106">Désactiver la personnalisation pour un profil</span><span class="sxs-lookup"><span data-stu-id="456a0-106">Disable personalization for a profile</span></span>
<span data-ttu-id="456a0-107">Vous pouvez empêcher tous les utilisateurs appartenant à un profil spécifique de personnaliser leurs pages.</span><span class="sxs-lookup"><span data-stu-id="456a0-107">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>
1.  <span data-ttu-id="456a0-108">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Profils**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="456a0-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profiles**, and then choose the related link.</span></span>
2.  <span data-ttu-id="456a0-109">Sélectionnez dans la liste le profil à modifier.</span><span class="sxs-lookup"><span data-stu-id="456a0-109">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="456a0-110">Activez la case à cocher **Désactiver la personnalisation**, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="456a0-110">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="clear-user-personalizations"></a><span data-ttu-id="456a0-111">Effacer les personnalisations des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="456a0-111">Clear user personalizations</span></span>

<span data-ttu-id="456a0-112">L'effacement de la personnalisation de la page rétablit la page à sa disposition d'origine, antérieure à toute personnalisation.</span><span class="sxs-lookup"><span data-stu-id="456a0-112">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="456a0-113">Il y a deux méthodes pour effacer les personnalisations de page effectuées par les utilisateurs : en utilisant la page **Supprimer la personnalisation utilisateur** et en utilisant la page **Fiche de personnalisation utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="456a0-113">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="456a0-114">Effacer les personnalisations utilisateur à l'aide de la page Supprimer la personnalisation utilisateur</span><span class="sxs-lookup"><span data-stu-id="456a0-114">Clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="456a0-115">La page **Supprimer la personnalisation utilisateur** permet d'effacer les personnalisations par page et par utilisateur individuellement.</span><span class="sxs-lookup"><span data-stu-id="456a0-115">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1.  <span data-ttu-id="456a0-116">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Supprimer la personnalisation utilisateur**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="456a0-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="456a0-117">La page répertorie toutes les pages qui ont été personnalisées et l'utilisateur auquel elles appartiennent.</span><span class="sxs-lookup"><span data-stu-id="456a0-117">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="456a0-118">Une coche dans la colonne **Legacy Personalization** indique si la personnalisation a été effectuée dans une ancienne version de [!INCLUDE[d365fin](includes/d365fin_md.md)], qui a traité la personnalisation de manière différente.</span><span class="sxs-lookup"><span data-stu-id="456a0-118">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="456a0-119">Les utilisateurs qui essaient de personnaliser ces pages sont empêchés de le faire, à moins qu'ils ne choisissent de déverrouiller la page.</span><span class="sxs-lookup"><span data-stu-id="456a0-119">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="456a0-120">Pour plus d'informations, voir [Pourquoi la personnalisation d'une page est bloquée](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="456a0-120">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="456a0-121">Sélectionnez l'écriture à supprimer, puis sélectionnez l'action **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="456a0-121">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="456a0-122">L'utilisateur les verra les modifications lors de sa prochaine connexion.</span><span class="sxs-lookup"><span data-stu-id="456a0-122">The user will see the changes the next time they sign-in.</span></span>

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="456a0-123">Effacer les personnalisations utilisateur à l'aide de la page Fiche de personnalisation utilisateur</span><span class="sxs-lookup"><span data-stu-id="456a0-123">Clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="456a0-124">La page **Fiche de personnalisation utilisateur** permet d'effacer la personnalisation de toutes les pages d'un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="456a0-124">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="456a0-125">Cela nécessite l'autorisation d'écriture dans la table 2000000072 **Profil**.</span><span class="sxs-lookup"><span data-stu-id="456a0-125">This requires write permission to Table 2000000072 **Profile**.</span></span>

1.  <span data-ttu-id="456a0-126">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Personnalisation utilisateur**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="456a0-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="456a0-127">La page **Personnalisation utilisateur** répertorie tous les utilisateurs qui ont potentiellement des pages personnalisées.</span><span class="sxs-lookup"><span data-stu-id="456a0-127">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="456a0-128">Si vous ne trouvez pas un utilisateur dans la liste, cela signifie qu'ils n'a aucune page personnalisée.</span><span class="sxs-lookup"><span data-stu-id="456a0-128">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="456a0-129">Sélectionnez l'utilisateur dans la liste, puis sélectionnez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="456a0-129">Select the user from the list, and then choose the **Edit** action.</span></span>

3.  <span data-ttu-id="456a0-130">Sous l'onglet **Actions**, choisissez **Effacer les pages personnalisées**.</span><span class="sxs-lookup"><span data-stu-id="456a0-130">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="456a0-131">L'utilisateur les verra les modifications lors de sa prochaine connexion.</span><span class="sxs-lookup"><span data-stu-id="456a0-131">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="456a0-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="456a0-132">See Also</span></span>
[<span data-ttu-id="456a0-133">Personnalisation de votre espace de travail</span><span class="sxs-lookup"><span data-stu-id="456a0-133">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="456a0-134">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="456a0-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="456a0-135">Modification des paramètres de base</span><span class="sxs-lookup"><span data-stu-id="456a0-135">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
<span data-ttu-id="456a0-136">[Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="456a0-136">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  

