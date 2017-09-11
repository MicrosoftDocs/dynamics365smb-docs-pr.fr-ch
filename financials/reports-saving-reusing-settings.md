---
title: "Appliquer et modifier les paramètres enregistrés dans des états | Microsoft Docs"
description: "Décrit l'utilisation d'options et filtre prédéfinis pour personnaliser un état, et pour générer les données exactes."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9e5f7417579a5ba0629032cf9fa664e0060b9cbf
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017

---
# <a name="saved-settings-on-reports"></a><span data-ttu-id="7d4fd-103">Paramètres enregistrés dans les états</span><span class="sxs-lookup"><span data-stu-id="7d4fd-103">Saved Settings on Reports</span></span>
<span data-ttu-id="7d4fd-104">En fonction de l'état exécuté, vous pouvez bénéficier d'une page qui vous laisse définir certaines options et certains filtres pour modifier les données incluses dans l'état généré.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-104">Depending on the report that is run, you might be presented with a page that lets you to set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="7d4fd-105">Cette page est connue comme la page de demande de l'état.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-105">This page is known as the report request page.</span></span> <span data-ttu-id="7d4fd-106">Un état peut inclure un ou plusieurs *paramètres enregistrés* que vous pouvez appliquer à l'état à partir de la page de demande.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-106">A report can include one or more *saved settings* that you can apply to the report from the request page.</span></span> <span data-ttu-id="7d4fd-107">Les *Paramètres enregistrés* sont essentiellement des options et des filtres prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="7d4fd-108">Le fait d'utiliser les paramètres enregistrés est une façon rapide et fiable de générer de façon cohérente des états qui contiennent les données adéquates.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span>

<span data-ttu-id="7d4fd-109">Vous pouvez voir les paramètres enregistrés qui sont à votre disposition pour un état dans la section **Paramètres enregistrés** de la page de demande de l'état.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-109">You can see the saved settings that are available to you for a report in **Saved Settings** section of the report request page.</span></span>  

## <a name="to-apply-saved-settings-to-a-report"></a><span data-ttu-id="7d4fd-110">Pour appliquer des paramètres enregistrés à un état</span><span class="sxs-lookup"><span data-stu-id="7d4fd-110">To apply saved settings to a report</span></span>
1. <span data-ttu-id="7d4fd-111">Ouvrez l'état.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-111">Open the report.</span></span>

   <span data-ttu-id="7d4fd-112">La page de demande de l'état s'affiche.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-112">The report request page appears.</span></span>    
2. <span data-ttu-id="7d4fd-113">Dans la section **Paramètres enregistrés** de la page, définissez le champ **Nom** dans les paramètres enregistrés que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-113">In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.</span></span>

   <span data-ttu-id="7d4fd-114">La section **Paramètres enregistrés** apparaît uniquement si l'état a été exécuté avant ou s'il y a des écritures de paramètres enregistrées.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-114">The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries.</span></span> <span data-ttu-id="7d4fd-115">L'écriture de paramètres enregistrés appelée **Options et filtres récemment utilisés** est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-115">The saved settings entry called **Last used options and filters** is always available.</span></span> <span data-ttu-id="7d4fd-116">Ces paramètres sont les valeurs d'option et de filtre qui ont été utilisées la dernière fois que vous avez exécuté l'état.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-116">These settings are the option and filter values that were used the last time you ran the report.</span></span>

## <a name="administer-saved-report-settings-for-users"></a><span data-ttu-id="7d4fd-117">Administrer les paramètres d'état enregistrés pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7d4fd-117">Administer saved report settings for users</span></span>
<span data-ttu-id="7d4fd-118">Si vous avez les bonnes autorisations, vous pouvez visualiser, créer et modifier les paramètres enregistrés pour tous les états pour tous les utilisateurs de la société.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-118">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="7d4fd-119">Vous pouvez attribuer les paramètres enregistrés d'un état à des utilisateurs en particulier ou à tous les utilisateurs de la société.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-119">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<span data-ttu-id="7d4fd-120">Vous gérez les paramètres enregistrés à partir de la page 1506 **Paramètres des états**.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-120">You manage saved settings from page 1506 **Reports Settings**.</span></span> <span data-ttu-id="7d4fd-121">Pour ouvrir cette page, sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres de l'état**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-121">To open this page, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Settings**, and then choose the related link.</span></span>

<span data-ttu-id="7d4fd-122">Sur la page **Paramètres d'état**, vous pouvez créer de nouveaux paramètres à partir de zéro ou vous pouvez effectuer une copier et modifier des paramètres existants.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-122">From the **Report Settings** page, you can create a new settings from scratch or you can make a copy and modify existing settings.</span></span> <span data-ttu-id="7d4fd-123">Pour modifier les options et les filtres pour un paramètre, sélectionnez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-123">To modify the options and filters for a settings, choose the **Edit** action.</span></span>

<span data-ttu-id="7d4fd-124">**Remarque :**</span><span class="sxs-lookup"><span data-stu-id="7d4fd-124">**Notes:**</span></span>

* <span data-ttu-id="7d4fd-125">la fonctionnalité des paramètres enregistrés des états n'est appropriée que lorsque la propriété SaveValues de la page de demande est définie sur Oui.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-125">The saved settings feature on reports is only relevant when the SaveValues property of the request page is set to Yes.</span></span> <span data-ttu-id="7d4fd-126">La propriété SaveValues est définie dans l'environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-126">The SaveValues property property is set in the development environment.</span></span>
* <span data-ttu-id="7d4fd-127">Si vous créez un article de paramètres enregistrés pour tous les utilisateurs, et qu'il porte le même nom que les paramètres enregistrés existants pour un utilisateur spécifique, alors cet utilisateur ne pourra pas utiliser les paramètres enregistrés affectés à tous.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-127">If you create a saved settings item for all users, and it has the same name as an existing saved settings for a specific user, then that user will not be able to use the saved settings that is assigned to everyone.</span></span>  <span data-ttu-id="7d4fd-128">Dans le champ Paramètres enregistrés de la page de demande d'état, l'utilisateur verra deux options de paramètres enregistrées avec le même nom.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-128">In the Saved Settings field on the report request page, the user will see two saved settings options with the same name.</span></span> <span data-ttu-id="7d4fd-129">Toutefois, peu importe l'option qu'il choisit, les paramètres enregistrés qui lui sont spécifiques seront utilisés.</span><span class="sxs-lookup"><span data-stu-id="7d4fd-129">However, no matter which option he chooses, the user-specific saved settings will be used.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d4fd-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d4fd-130">See Also</span></span>
[<span data-ttu-id="7d4fd-131">Planifier un état à exécuter</span><span class="sxs-lookup"><span data-stu-id="7d4fd-131">Schedule a Rpeort to Run</span></span>](ui-schedule-report.md)  

