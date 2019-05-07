---
title: Pourquoi ne peux pas personnaliser une page | Microsoft Docs
description: Explique pourquoi vous ne pouvez pas personnaliser une page et ce que vous pouvez faire pour la déverrouiller et pouvoir ainsi la personnaliser.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 64995372f68ed2804bc165823dacc34ad6a3194d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "911711"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="5c0bb-103">Pourquoi la personnalisation d'une page est verrouillée</span><span class="sxs-lookup"><span data-stu-id="5c0bb-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="5c0bb-104">Deux conditions vous empêchent de personnaliser une page.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="5c0bb-105">Soit la page est verrouillée (comme indiqué par ![Verrouillage de personnalisation](media/personalization-lock-icon.png "Verrouillage de personnalisation")) ou soit elle est bloquée (comme indiqué par ![Personnalisation bloquée](media/personalization-blocked-icon.png "Personnalisation bloquée")).</span><span class="sxs-lookup"><span data-stu-id="5c0bb-105">Either the page is locked (as indicated by ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) or it is blocked (as indicated by ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked")).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="5c0bb-106">Personnalisation verrouillée</span><span class="sxs-lookup"><span data-stu-id="5c0bb-106">Locked from Personalizing</span></span>

<span data-ttu-id="5c0bb-107">S'il existe une icône ![Verrouillage de personnalisation](media/personalization-lock-icon.png "Verrouillage de personnalisation") dans la bannière **Personnalisation** lorsque vous ouvrez une page (comme illustré), cela signifie que vous ne pouvez pas apporter d'autres modifications de personnalisation à la page.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page (as shown), this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<span data-ttu-id="5c0bb-108">![Verrouillage de personnalisation](media/personalization-locked.png "Verrouillage de personnalisation")</span><span class="sxs-lookup"><span data-stu-id="5c0bb-108">![Personalize Lock](media/personalization-locked.png "Personalize lock")</span></span>


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="5c0bb-109">Deux raisons expliquent cela :</span><span class="sxs-lookup"><span data-stu-id="5c0bb-109">There can be two reasons for this:</span></span>

1. <span data-ttu-id="5c0bb-110">vous avez personnalisé la page auparavant, mais en utilisant une version antérieure du produit.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-110">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="5c0bb-111">Nous avons modifié la manière dont la personnalisation fonctionne en arrière-plan depuis votre dernière personnalisation de la page.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-111">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="5c0bb-112">Malheureusement, l'ancienne méthode et la nouvelle ne sont pas compatibles.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-112">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="5c0bb-113">jusqu'ici, vous n'avez utilisé que [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] pour personnaliser la page.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-113">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="5c0bb-114">Déverrouillage de la page</span><span class="sxs-lookup"><span data-stu-id="5c0bb-114">Unlocking the Page</span></span>

<span data-ttu-id="5c0bb-115">Si vous souhaitez déverrouiller une page et poursuivre sa personnalisation, sélectionnez ![Verrouillage de personnalisation](media/personalization-lock-icon.png "Verrouillage de personnalisation"), puis **Déverrouiller**.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-115">If you want to unlock a page and continue personalizing it, choose ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock"), and then **Unlock**.</span></span>  

<span data-ttu-id="5c0bb-116">Avant de déverrouiller la page, veillez à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="5c0bb-116">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="5c0bb-117">La personnalisation actuelle de la page est désactivée.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-117">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="5c0bb-118">La page reviendra à sa mise en page d'origine et vous devrez recommencer à zéro.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-118">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="5c0bb-119">Dans [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], la page reste telle quelle et n'est pas affectée par les modifications apportées à la nouvelle personnalisation dans le client Business Central.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-119">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="5c0bb-120">En outre, la personnalisation dans [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] et le client Business Central sont entièrement distinctes l'une de l'autre.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-120">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="5c0bb-121">Personnalisation bloquée</span><span class="sxs-lookup"><span data-stu-id="5c0bb-121">Blocked from Personalizing</span></span>

<span data-ttu-id="5c0bb-122">S'il y a une icône ![Personnalisation bloquée](media/personalization-blocked-icon.png "Personnalisation bloquée") dans la bannière Personnalisation, cela signifie que vous ne pouvez pas apporter de personnalisation à la page.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-122">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the Personalizing banner, this means that you are blocked from doing any personalization to the page.</span></span>

<span data-ttu-id="5c0bb-123">![Personnalisation bloquée](media/personalization-blocked.png "Verrouillage de personnalisation")</span><span class="sxs-lookup"><span data-stu-id="5c0bb-123">![Personalize blocked](media/personalization-blocked.png "Personalize lock")</span></span>

<span data-ttu-id="5c0bb-124">La raison à cela n'est autre que le Tableau de bord ou le profil actuellement associé à votre compte d'utilisateur modifie cette page notamment pour votre rôle.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-124">The reason for this is that the Role Center or profile that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="5c0bb-125">Veuillez contacter votre administrateur pour obtenir de l'aide, ou si cela s'avère nécessaire, essayez de passer à un Tableau de bord (depuis [**Mes paramètres**](https://businesscentral.dynamics.com?page=9176 "Accéder directement à votre page Paramètres d'utilisateur dans Business Central")) qui n'inclut pas la personnalisation du rôle pour cette page.</span><span class="sxs-lookup"><span data-stu-id="5c0bb-125">Please contact your administrator for assistance or, if it makes sense, try switching to a Role Center (from  [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central")) that does include role-tailoring for this page.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c0bb-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c0bb-126">See Also</span></span>
[<span data-ttu-id="5c0bb-127">Personnalisation de votre espace de travail</span><span class="sxs-lookup"><span data-stu-id="5c0bb-127">Personalizing Your Workspace</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="5c0bb-128">Gérer la personnalisation</span><span class="sxs-lookup"><span data-stu-id="5c0bb-128">Managing Personalization</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="5c0bb-129">Modification des paramètres de base</span><span class="sxs-lookup"><span data-stu-id="5c0bb-129">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="5c0bb-130">Modification des fonctionnalités affichées</span><span class="sxs-lookup"><span data-stu-id="5c0bb-130">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
