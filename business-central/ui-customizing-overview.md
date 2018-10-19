---
title: Personnalisation de Business Central | Microsoft Docs
description: "En savoir plus sur l'ajout de fonctionnalités et la personnalisation de Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, add-in, extend, customize
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 63ba198a761b0c79c51ac94d36314310e330fc58
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="customizing-business-central"></a><span data-ttu-id="03dcf-103">Personnalisation de Business Central</span><span class="sxs-lookup"><span data-stu-id="03dcf-103">Customizing Business Central</span></span>
<span data-ttu-id="03dcf-104">Il existe différentes méthodes pour personnaliser l'application, afin de donner à vous et vos collègues l'accès aux fonctions, fonctionnalités et données dont vous avez le plus besoin, de la manière la mieux adaptée à vos opérations quotidiennes.</span><span class="sxs-lookup"><span data-stu-id="03dcf-104">There are different ways to customize the application to give you and your colleagues access to the features, functionality, and data that you need most, in a manner that bests suits your daily work.</span></span> <span data-ttu-id="03dcf-105">L'accessibilité aux modifications dépend de ce que vous faites, comme décrit dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="03dcf-105">Those who see the changes will depend on what you do, as described in this table.</span></span>

| <span data-ttu-id="03dcf-106">Ce que vous pouvez faire</span><span class="sxs-lookup"><span data-stu-id="03dcf-106">What you can do</span></span>    |  <span data-ttu-id="03dcf-107">Désignation</span><span class="sxs-lookup"><span data-stu-id="03dcf-107">Description</span></span>  |  <span data-ttu-id="03dcf-108">Qui voit les modifications</span><span class="sxs-lookup"><span data-stu-id="03dcf-108">Who sees the changes</span></span>  |  <span data-ttu-id="03dcf-109">Plus d'informations</span><span class="sxs-lookup"><span data-stu-id="03dcf-109">More information</span></span>  |
|-----|---------------|---------|-------|
|<span data-ttu-id="03dcf-110">Installer une extension</span><span class="sxs-lookup"><span data-stu-id="03dcf-110">Install an extension</span></span>|<span data-ttu-id="03dcf-111">Les extensions sont comme de petites applications qui ajoutent des fonctionnalités, modifient le comportement, donnent accès à de nouveaux services en ligne, etc.</span><span class="sxs-lookup"><span data-stu-id="03dcf-111">Extensions are like small applications that add functionality, change behavior, provide access to new online services, and more.</span></span> <span data-ttu-id="03dcf-112">Par exemple, Microsoft propose une extension qui fournit une intégration à PayPal Payments Standard.</span><span class="sxs-lookup"><span data-stu-id="03dcf-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span>|<span data-ttu-id="03dcf-113">Tous les utilisateurs de toutes les sociétés.</span><span class="sxs-lookup"><span data-stu-id="03dcf-113">All users in all companies.</span></span>|[<span data-ttu-id="03dcf-114">Personnalisation à l'aide d'extensions</span><span class="sxs-lookup"><span data-stu-id="03dcf-114">Customizing Using Extensions</span></span>](ui-extensions.md)|
|<span data-ttu-id="03dcf-115">Modifier les éléments de l'interface utilisateur qui sont visibles.</span><span class="sxs-lookup"><span data-stu-id="03dcf-115">Change which UI elements are visible.</span></span>|<span data-ttu-id="03dcf-116">Le paramètre **Expérience** détermine le nombre de fonctionnalités affichées dans l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="03dcf-116">The **Experience** setting determines how much of the functionality is displayed in the user interface.</span></span> <span data-ttu-id="03dcf-117">Choisissez entre Essentiel et Premium.</span><span class="sxs-lookup"><span data-stu-id="03dcf-117">Choose between Essential and Premium.</span></span>|<span data-ttu-id="03dcf-118">Tous les utilisateurs d'une société spécifique.</span><span class="sxs-lookup"><span data-stu-id="03dcf-118">All users in a specific company.</span></span>|[<span data-ttu-id="03dcf-119">Modification des fonctionnalités affichées</span><span class="sxs-lookup"><span data-stu-id="03dcf-119">Changing Which Features are Displayed</span></span>](ui-experiences.md)|
|<span data-ttu-id="03dcf-120">Personnaliser votre espace de travail</span><span class="sxs-lookup"><span data-stu-id="03dcf-120">Personalize your workspace</span></span>|<span data-ttu-id="03dcf-121">Modifiez la mise en page et le contenu de vos pages.</span><span class="sxs-lookup"><span data-stu-id="03dcf-121">Change the layout and content of your pages.</span></span>|<span data-ttu-id="03dcf-122">Vous uniquement.</span><span class="sxs-lookup"><span data-stu-id="03dcf-122">Only you.</span></span>|[<span data-ttu-id="03dcf-123">Personnalisation de votre espace de travail</span><span class="sxs-lookup"><span data-stu-id="03dcf-123">Personalizing Your Workspace</span></span>](ui-personalization-user.md)|

> [!NOTE]
> <span data-ttu-id="03dcf-124">Tous les descriptions de fonctions de la documentation utilisateur de [!INCLUDE[d365fin](includes/d365fin_md.md)] assument l'expérience **Premium**, ce qui signifie que les descriptions couvrent la portée complète des éléments de l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="03dcf-124">All feature descriptions in user documentation for [!INCLUDE[d365fin](includes/d365fin_md.md)] assumes the **Premium** experience, meaning the descriptions cover the full scope of UI elements.</span></span> <span data-ttu-id="03dcf-125">Par conséquent, les utilisateurs avec l'expérience **Essentiel** peuvent dans certaines rubriques rencontrer des fonctionnalités et des éléments de l'interface utilisateur qui ne sont pas visibles dans leur interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="03dcf-125">Therefore, users with the **Essential** experience may in some topics read about functionality and UI elements that are not visible in their user interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="03dcf-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03dcf-126">See Also</span></span>
<span data-ttu-id="03dcf-127">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="03dcf-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

