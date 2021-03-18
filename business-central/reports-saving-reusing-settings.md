---
title: Appliquer et modifier les paramètres enregistrés dans des états | Microsoft Docs
description: Décrit l'utilisation d'options et filtre prédéfinis pour personnaliser un état, et pour générer les données exactes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 70b3f391c141aa53dcef258a131d6395782a4488
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392564"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><span data-ttu-id="e397b-103">Gérer les paramètres enregistrés pour les états et les traitements par lots</span><span class="sxs-lookup"><span data-stu-id="e397b-103">Manage Saved Settings for Reports and Batch jobs</span></span>
<span data-ttu-id="e397b-104">Lors de l'exécution d'un état, les utilisateurs voient généralement une page qui leur permet de sélectionner des options et de définir des filtres pour modifier les données incluses dans l'état généré.</span><span class="sxs-lookup"><span data-stu-id="e397b-104">When running reports, users are typically presented with a page that lets them select options and set filters to change the data that is included in the generated report.</span></span> <span data-ttu-id="e397b-105">Cette page est appelée la page de demande.</span><span class="sxs-lookup"><span data-stu-id="e397b-105">This page is called the request page.</span></span> <span data-ttu-id="e397b-106">Un état peut inclure un ou plusieurs *paramètres enregistrés* que les utilisateurs peuvent appliquer à l'état à partir de la page de demande.</span><span class="sxs-lookup"><span data-stu-id="e397b-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="e397b-107">Les *Paramètres enregistrés* sont essentiellement des options et des filtres prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="e397b-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="e397b-108">Le fait d'utiliser les paramètres enregistrés est une façon rapide et fiable de générer de façon cohérente des états qui contiennent les données adéquates.</span><span class="sxs-lookup"><span data-stu-id="e397b-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="e397b-109">Pour plus d'informations, voir [Utilisation des paramètres enregistrés](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="e397b-109">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

> [!NOTE]
> <span data-ttu-id="e397b-110">Cette rubrique fait référence surtout aux « états », mais des informations similaires s'appliquent aux traitements par lots.</span><span class="sxs-lookup"><span data-stu-id="e397b-110">This topic refers mainly to "report", but similar information applies to batch jobs.</span></span>

<span data-ttu-id="e397b-111">Si vous avez les bonnes autorisations, vous pouvez visualiser, créer et modifier les paramètres enregistrés pour tous les états pour tous les utilisateurs de la société.</span><span class="sxs-lookup"><span data-stu-id="e397b-111">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in a company.</span></span> <span data-ttu-id="e397b-112">Vous pouvez attribuer les paramètres enregistrés d'un état à des utilisateurs en particulier ou à tous les utilisateurs de la société.</span><span class="sxs-lookup"><span data-stu-id="e397b-112">You can assign saved settings for a report to individual users or to all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="e397b-113">Pour créer et modifier les paramètres enregistrés pour tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e397b-113">To create and modify saved settings for all users</span></span>
<span data-ttu-id="e397b-114">Vous devez gérer les paramètres enregistrés à partir de la page **Paramètres des états**.</span><span class="sxs-lookup"><span data-stu-id="e397b-114">You manage saved settings on the **Reports Settings** page.</span></span> <span data-ttu-id="e397b-115">Deux méthodes sont disponibles pour ouvrir cette page :</span><span class="sxs-lookup"><span data-stu-id="e397b-115">There are two ways to open this page:</span></span>
-   <span data-ttu-id="e397b-116">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres des états**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="e397b-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="e397b-117">Ouvrez un état, sélectionnez la fonction Tell Me dans le champ **Utiliser les valeurs par défaut de**, puis choisissez l'action **Sélectionner dans la liste complète**.</span><span class="sxs-lookup"><span data-stu-id="e397b-117">Open a report, choose the lookup in the **Use default values from** field, and then choose the **Select from full list** action.</span></span>

<span data-ttu-id="e397b-118">La page affiche toutes les entrées de paramètres enregistrés existants pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e397b-118">The page displays all the existing saved settings entries for all users.</span></span> <span data-ttu-id="e397b-119">Si un nom d'utilisateur est indiqué dans le champ **Affecté à**, seul cet utilisateur peut utiliser les paramètres enregistrés pour l'état associé.</span><span class="sxs-lookup"><span data-stu-id="e397b-119">If there is a user name in the **Assigned to** field, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="e397b-120">Si le champ **Partager avec tous les utilisateurs** est coché, tous les utilisateurs peuvent utiliser les paramètres enregistrés pour l'état.</span><span class="sxs-lookup"><span data-stu-id="e397b-120">If there is a check mark in the **Share with all users** field, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="e397b-121">Dans la page **Paramètres de l'état**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="e397b-121">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="e397b-122">Sélectionner l'action **Nouveau** pour créer une nouvelle entrée de paramètres enregistrés.</span><span class="sxs-lookup"><span data-stu-id="e397b-122">Choose the **New** action to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="e397b-123">Sélectionner une entrée de paramètres enregistrés dans la liste, puis choisir l'action **Copier** pour créer une copie.</span><span class="sxs-lookup"><span data-stu-id="e397b-123">Select a saved settings entry from the list, and choose the **Copy** action to create a copy.</span></span>
-   <span data-ttu-id="e397b-124">Sélectionner une entrée de paramètres enregistrés dans la liste, puis choisir l'action **Modifier** pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="e397b-124">Select a saved settings entry from the list, and choose the **Edit** action to modify a saved settings entry.</span></span>

> [!Important]
> <span data-ttu-id="e397b-125">Définir le nom que vous souhaitez affecter à une entrée de paramètres enregistrés.</span><span class="sxs-lookup"><span data-stu-id="e397b-125">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="e397b-126">Si vous créez une entrée de paramètres enregistrés pour tous les utilisateurs et vous lui donnez le même nom que l'entrée de paramètres enregistrés existants qui est affectée à un utilisateur spécifique, alors cet utilisateur ne pourra pas utiliser l'entrée de paramètres enregistrés qui est affectée à tous.</span><span class="sxs-lookup"><span data-stu-id="e397b-126">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="e397b-127">Dans la section **Paramètres enregistrés** dans la page de demande de l'état, l'utilisateur verra deux entrées de paramètres enregistrés avec le même nom.</span><span class="sxs-lookup"><span data-stu-id="e397b-127">In the **Saved Settings** section on the request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="e397b-128">Toutefois, peu importe l'option qu'il choisit, l'entrée de paramètres enregistrés qui lui est spécifique sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="e397b-128">However, no matter which option they choose, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="e397b-129">La fonctionnalité Paramètres enregistrés n'est disponible que pour les états où la propriété [SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) de la page de demande de l'état est définie sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="e397b-129">The Saved Settings feature is available only on reports where the [SaveValues property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) of the report's request page is set to **Yes**.</span></span> <span data-ttu-id="e397b-130">La propriété **SaveValues** est définie dans l'environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="e397b-130">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e397b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e397b-131">See Also</span></span>
[<span data-ttu-id="e397b-132">Utilisation des états, des traitements par lots et des XMLports</span><span class="sxs-lookup"><span data-stu-id="e397b-132">Working with Reports, Batch Jobs, and XMLports</span></span>](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]