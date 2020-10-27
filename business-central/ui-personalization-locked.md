---
title: Pourquoi je ne peux pas personnaliser une page | Microsoft Docs
description: Explique pourquoi vous ne pouvez pas personnaliser une page et ce que vous pouvez faire pour la déverrouiller et pouvoir ainsi la personnaliser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0bd24833f37fe70f8e642685be4d28dbb593a16d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923410"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="75654-103">Pourquoi la personnalisation d’une page est verrouillée</span><span class="sxs-lookup"><span data-stu-id="75654-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="75654-104">Deux conditions vous empêchent de personnaliser une page.</span><span class="sxs-lookup"><span data-stu-id="75654-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="75654-105">La page est verrouillée (comme indiqué par l’icône ![Verrouillage de personnalisation](media/personalization-lock-icon.png "Verrouillage de personnalisation")) ou bloquée (comme indiqué par l’icône ![Personnalisation bloquée](media/personalization-blocked-icon.png "Personnalisation bloquée")).</span><span class="sxs-lookup"><span data-stu-id="75654-105">Either the page is locked (as indicated by the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) icon or it is blocked (as indicated by the ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="75654-106">Personnalisation verrouillée</span><span class="sxs-lookup"><span data-stu-id="75654-106">Locked from Personalizing</span></span>

<span data-ttu-id="75654-107">S’il existe une icône ![Verrouillage de personnalisation](media/personalization-lock-icon.png "Verrouillage de personnalisation") dans la bannière **Personnalisation** lorsque vous ouvrez une page, cela signifie que vous ne pouvez pas apporter d’autres modifications de personnalisation à la page.</span><span class="sxs-lookup"><span data-stu-id="75654-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page, this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="75654-108">Deux raisons expliquent cela :</span><span class="sxs-lookup"><span data-stu-id="75654-108">There can be two reasons for this:</span></span>

1. <span data-ttu-id="75654-109">vous avez personnalisé la page auparavant, mais en utilisant une version antérieure du produit.</span><span class="sxs-lookup"><span data-stu-id="75654-109">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="75654-110">Nous avons modifié la manière dont la personnalisation fonctionne en arrière-plan depuis votre dernière personnalisation de la page.</span><span class="sxs-lookup"><span data-stu-id="75654-110">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="75654-111">Malheureusement, l’ancienne méthode et la nouvelle ne sont pas compatibles.</span><span class="sxs-lookup"><span data-stu-id="75654-111">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="75654-112">jusqu’ici, vous n’avez utilisé que [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] pour personnaliser la page.</span><span class="sxs-lookup"><span data-stu-id="75654-112">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="75654-113">Déverrouillage de la page</span><span class="sxs-lookup"><span data-stu-id="75654-113">Unlocking the Page</span></span>

<span data-ttu-id="75654-114">Si vous souhaitez déverrouiller une page et poursuivre sa personnalisation, sélectionnez l’icône ![Verrouillage de personnalisation](media/personalization-lock-icon.png "Verrouillage de personnalisation"), puis l’action **Déverrouiller** .</span><span class="sxs-lookup"><span data-stu-id="75654-114">If you want to unlock a page and continue personalizing it, choose the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon, and then choose the **Unlock** action.</span></span>  

<span data-ttu-id="75654-115">Avant de déverrouiller la page, veillez à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="75654-115">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="75654-116">La personnalisation actuelle de la page est désactivée.</span><span class="sxs-lookup"><span data-stu-id="75654-116">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="75654-117">La page reviendra à sa mise en page d’origine et vous devrez recommencer à zéro.</span><span class="sxs-lookup"><span data-stu-id="75654-117">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="75654-118">Dans [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], la page reste telle quelle et n’est pas affectée par les modifications apportées à la nouvelle personnalisation dans le client Business Central.</span><span class="sxs-lookup"><span data-stu-id="75654-118">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="75654-119">En outre, la personnalisation dans [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] et le client Business Central sont entièrement distinctes l’une de l’autre.</span><span class="sxs-lookup"><span data-stu-id="75654-119">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="75654-120">Personnalisation bloquée</span><span class="sxs-lookup"><span data-stu-id="75654-120">Blocked from Personalizing</span></span>

<span data-ttu-id="75654-121">S’il y a une icône ![Personnalisation bloquée](media/personalization-blocked-icon.png "Personnalisation bloquée") dans la bannière **Personnalisation** , cela signifie que vous ne pouvez pas apporter de personnalisation à la page.</span><span class="sxs-lookup"><span data-stu-id="75654-121">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the **Personalizing** banner, this means that you are blocked from doing any personalization to the page.</span></span>

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

<span data-ttu-id="75654-122">La raison à cela n’est autre que le Tableau de bord ou le rôle actuellement associé à votre compte d’utilisateur modifie cette page notamment pour votre rôle.</span><span class="sxs-lookup"><span data-stu-id="75654-122">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="75654-123">Contactez votre administrateur pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="75654-123">Contact your administrator for assistance.</span></span> <span data-ttu-id="75654-124">Sinon, essayez de passer à un Tableau de bord qui inclut la personnalisation des rôles pour cette page.</span><span class="sxs-lookup"><span data-stu-id="75654-124">Alternatively, try switching to a Role Center that does include role-tailoring for this page.</span></span> <span data-ttu-id="75654-125">Pour plus d’informations, voir [Modifier les paramètres de base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="75654-125">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="75654-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75654-126">See Also</span></span>
[<span data-ttu-id="75654-127">Personnaliser votre espace de travail</span><span class="sxs-lookup"><span data-stu-id="75654-127">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="75654-128">Personnaliser les pages pour les profils</span><span class="sxs-lookup"><span data-stu-id="75654-128">Customize Pages for Profiles</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="75654-129">Modifier les paramètres de base</span><span class="sxs-lookup"><span data-stu-id="75654-129">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="75654-130">Modifier les fonctionnalités affichées</span><span class="sxs-lookup"><span data-stu-id="75654-130">Change Which Features are Displayed</span></span>](ui-experiences.md)  
