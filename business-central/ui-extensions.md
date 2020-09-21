---
title: Installation d'extensions pour personnaliser Business Central | Microsoft Docs
description: En savoir plus sur l'ajout des fonctionnalités et la personnalisation de Business Central en installant des extensions.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765936"
---
# <a name="customizing-business-central-using-extensions"></a><span data-ttu-id="dd38a-103">Personnalisation de Business Central à l'aide d'extensions</span><span class="sxs-lookup"><span data-stu-id="dd38a-103">Customizing Business Central Using Extensions</span></span>

<span data-ttu-id="dd38a-104">Vous pouvez modifier [!INCLUDE[d365fin](includes/d365fin_md.md)] en installant des extensions qui ajoutent des fonctionnalités, modifient le comportement de l'application, ou vous permettent d'accéder à de nouveaux services en ligne, par exemple.</span><span class="sxs-lookup"><span data-stu-id="dd38a-104">You can change [!INCLUDE[d365fin](includes/d365fin_md.md)] by installing extensions that add functionality, changes behavior, or gives you access to new online services, for example.</span></span>

> [!NOTE]
> <span data-ttu-id="dd38a-105">Pour installer des extensions à partir de AppSource ou ajouter des extensions par locataire, vous devez disposer des autorisations adéquates.</span><span class="sxs-lookup"><span data-stu-id="dd38a-105">To install extensions from AppSource or add per-tenant extensions, you must have the right permissions.</span></span> <span data-ttu-id="dd38a-106">Vous devez être membre du groupe d'utilisateurs D365 EXTENSION MGMT ou disposer du jeu d'autorisations D365 EXTENSION MGMT.</span><span class="sxs-lookup"><span data-stu-id="dd38a-106">You must either be a member of the D365 EXTENSION MGMT user group or you must have the D365 EXTENSION MGMT permission set.</span></span> <span data-ttu-id="dd38a-107">Si vous êtes un administrateur, vous pouvez attribuer des groupes d'utilisateurs et des autorisations à d'autres utilisateurs de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="dd38a-107">If you are an administrator, you can assign user groups and permissions to other users in your company.</span></span><br /><br />
<span data-ttu-id="dd38a-108">Pour utiliser les fonctionnalités fournies par une extension, telles que l'ouverture de pages, la production de rapports, la sélection d'actions, etc., vous devez disposer des jeux d'autorisations installés avec cette extension.</span><span class="sxs-lookup"><span data-stu-id="dd38a-108">To use the functionality that is provided by an extension, such as opening pages, running reports, selecting actions, and so on, you must be assigned the permission sets that are installed as part of the extension.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="dd38a-109">Le chargement des extensions par client et l'installation des extensions AppSource ne sont pas pris en charge via la page **Gestion des extensions** pour les installations sur site.</span><span class="sxs-lookup"><span data-stu-id="dd38a-109">The upload of per-tenant extensions and the installation of AppSource extensions is not supported through the **Extension Management** page for on-premise installations.</span></span>

<span data-ttu-id="dd38a-110">La première fois que vous lancez [!INCLUDE[d365fin](includes/d365fin_md.md)], certaines extensions sont déjà installées.</span><span class="sxs-lookup"><span data-stu-id="dd38a-110">When you first launch [!INCLUDE[d365fin](includes/d365fin_md.md)], some extensions are already installed for you.</span></span> <span data-ttu-id="dd38a-111">Au fil du temps, davantage d'extensions seront disponibles. Il vous appartient de choisir si vous souhaitez les utiliser ou non.</span><span class="sxs-lookup"><span data-stu-id="dd38a-111">Over time, more extensions will be made available to you, and you can then choose if you want to use the extension or not.</span></span>

<span data-ttu-id="dd38a-112">Par exemple, Microsoft propose une extension qui fournit une intégration à PayPal Payments Standard.</span><span class="sxs-lookup"><span data-stu-id="dd38a-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span> <span data-ttu-id="dd38a-113">Cette extension est installée par défaut.</span><span class="sxs-lookup"><span data-stu-id="dd38a-113">This extension is installed by default.</span></span>
<span data-ttu-id="dd38a-114">Si une autre extension proposant une intégration à un autre service de paiement devenait disponible, vous pouvez installer cette nouvelle extension et choisir lequel des deux services vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="dd38a-114">But if another extension is made available that offers integration with another payment service, you can install the new extension and then choose which of the two services to use.</span></span>  

<span data-ttu-id="dd38a-115">La page **Gestion des extensions** vous permet de gérer les extensions.</span><span class="sxs-lookup"><span data-stu-id="dd38a-115">You manage the extensions on the **Extension Management** page.</span></span> <span data-ttu-id="dd38a-116">Vous pouvez accéder à cette page à partir de la page d'accueil.</span><span class="sxs-lookup"><span data-stu-id="dd38a-116">You can access this page from Home.</span></span> <span data-ttu-id="dd38a-117">Sinon, choisissez l'icône **Page ou état pour la recherche** ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") dans le coin supérieur droit, entrez **Extension**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="dd38a-117">Alternatively, choose the **Search for Page or Report** icon ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") in the top right corner, enter **Extension**, and then choose the related link.</span></span> <span data-ttu-id="dd38a-118">Pour plus d’informations, consultez [Installation et désinstallation d’extensions](ui-extensions-install-uninstall.md).</span><span class="sxs-lookup"><span data-stu-id="dd38a-118">For more information, see [Installing and Uninstalling Extensions](ui-extensions-install-uninstall.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="dd38a-119">Si vous voulez accéder à une extension mais que vous ne pouvez pas trouver sa fonctionnalité, vérifiez la page **Gestion des extensions**, si l'extension n'est pas répertoriée, vous pouvez la configurer comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="dd38a-119">If you think you should have access to an extension but you cannot find its functionality, check the **Extension Management** page - if the extension is not listed there, you can install it as described in the following section.</span></span>  

> [!NOTE]  
> <span data-ttu-id="dd38a-120">Les nouvelles extensions ne sont pas disponibles dans AppSource juste après l'annonce d'une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="dd38a-120">New extensions are not available in AppSource immediately after we announce an update.</span></span> <span data-ttu-id="dd38a-121">Vous pouvez vous tenir informé sur les extensions sur le site [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span><span class="sxs-lookup"><span data-stu-id="dd38a-121">You can keep an eye out for the extensions at  [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span></span>

## <a name="see-also"></a><span data-ttu-id="dd38a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd38a-122">See Also</span></span>

[<span data-ttu-id="dd38a-123">Extension de Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="dd38a-123">Extending Dynamics 365 Business Central</span></span>](about-develop-extensions.md)  
[<span data-ttu-id="dd38a-124">Extensions Business Central par d'autres fournisseurs</span><span class="sxs-lookup"><span data-stu-id="dd38a-124">Business Central Extensions by Other Providers</span></span>](ui-extensions-other.md)  
[<span data-ttu-id="dd38a-125">Configurer le service Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="dd38a-125">Set Up the Envestnet Yodlee Bank Feeds Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="dd38a-126">Activer les paiements client via Paypal</span><span class="sxs-lookup"><span data-stu-id="dd38a-126">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md)  
[<span data-ttu-id="dd38a-127">Migration des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="dd38a-127">Migrating Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="dd38a-128">Configuration de l'extension GetAddress.io UK Postal Code</span><span class="sxs-lookup"><span data-stu-id="dd38a-128">Setting Up the GetAddress.io UK Postal Code extension</span></span>](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
<span data-ttu-id="dd38a-129">[Extensions [!INCLUDE[d365fin](includes/d365fin_md.md)] par d'autres fournisseurs](ui-extensions-other.md)</span><span class="sxs-lookup"><span data-stu-id="dd38a-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensions by Other Providers](ui-extensions-other.md)</span></span>  
[<span data-ttu-id="dd38a-130">Mise en route</span><span class="sxs-lookup"><span data-stu-id="dd38a-130">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
