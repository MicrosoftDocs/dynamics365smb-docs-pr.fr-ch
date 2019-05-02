---
title: Configurer une société avec RapidStart Services | Microsoft Docs
description: Vous pouvez configurer une nouvelle société dans Business Central avec RapidStart Services, qui est un outil conçu pour réduire les temps de déploiement, améliorer la qualité de l’implémentation, présenter une approche reproductible des implémentations et augmenter la productivité en automatisant et en simplifiant des tâches récurrentes.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 12/07/2018
ms.author: sgroespe
ms.openlocfilehash: d7476674407dd505fafa8e82f3bfecc3aa5a5fee
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820264"
---
# <a name="setting-up-a-company-with-rapidstart-services"></a><span data-ttu-id="9a5f2-103">Configuration d'une société avec RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="9a5f2-103">Setting Up a Company With RapidStart Services</span></span>
<span data-ttu-id="9a5f2-104">Vous pouvez configurer une nouvelle société dans [!INCLUDE[d365fin](includes/d365fin_md.md)] avec RapidStart Services, qui est un outil conçu pour réduire les temps de déploiement, améliorer la qualité de l’implémentation, présenter une approche reproductible des implémentations et augmenter la productivité en automatisant et en simplifiant des tâches récurrentes.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-104">You can set up a new company in [!INCLUDE[d365fin](includes/d365fin_md.md)] with RapidStart Services, which is a tool designed to shorten deployment times, improve quality of implementation, introduce a repeatable approach to implementations, and enhance productivity by automating and simplifying recurring tasks.</span></span>  

<span data-ttu-id="9a5f2-105">RapidStart Services permet d’obtenir une vue d’ensemble du processus de configuration de votre nouvelle société grâce à une feuille dans laquelle vous pouvez configurer les tables souvent impliquées dans le processus de configuration de nouvelles sociétés.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-105">RapidStart Services helps you gain an overview of the setup process of your new company by providing a worksheet in which you can set up the tables often involved in the configuration process of new companies.</span></span> <span data-ttu-id="9a5f2-106">Comme vous effectuez cela, vous pouvez créer un questionnaire pour guider vos clients par le biais de la collecte des informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-106">As you do this, you can create a questionnaire to guide your customers through the collection of setup information.</span></span> <span data-ttu-id="9a5f2-107">Les clients peuvent choisir d’utiliser le questionnaire pour configurer des modules ou d’ouvrir la page de configuration directement et d'y effectuer la configuration.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-107">Your customers have the option of using the questionnaire to set up application areas, or they can open the setup page directly and do the setup there.</span></span> <span data-ttu-id="9a5f2-108">Chose plus importante, RapidStart Services vous aide, en tant que client, à mettre en place la société à l’aide de données de configuration par défaut que vous pouvez ajuster et personnaliser.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-108">Most importantly, RapidStart Services helps you, as a customer, prepare the company with default setup data that you can fine-tune and customize.</span></span> <span data-ttu-id="9a5f2-109">Pour terminer, lorsque vous utilisez RapidStart Services, vous pouvez configurer et migrer les données des clients existants, par exemple la liste des clients ou des articles, vers la nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-109">Lastly, when you use RapidStart Services, you can configure and migrate existing customer data, such as a list of customers or items, into the new company.</span></span>

<span data-ttu-id="9a5f2-110">Vous pouvez utiliser les composants suivants pour accélérer la configuration de votre société :</span><span class="sxs-lookup"><span data-stu-id="9a5f2-110">You can use the following components to speed up your company setup:</span></span>  

-   <span data-ttu-id="9a5f2-111">Assistant Configuration</span><span class="sxs-lookup"><span data-stu-id="9a5f2-111">Configuration wizard</span></span>  
-   <span data-ttu-id="9a5f2-112">Feuille configuration</span><span class="sxs-lookup"><span data-stu-id="9a5f2-112">Configuration worksheet</span></span>  
-   <span data-ttu-id="9a5f2-113">Packages configuration</span><span class="sxs-lookup"><span data-stu-id="9a5f2-113">Configuration packages</span></span>  
-   <span data-ttu-id="9a5f2-114">Modèles de configuration</span><span class="sxs-lookup"><span data-stu-id="9a5f2-114">Configuration templates</span></span>  
-   <span data-ttu-id="9a5f2-115">Questionnaire de configuration</span><span class="sxs-lookup"><span data-stu-id="9a5f2-115">Configuration questionnaire</span></span>  

> [!Note]  
>  <span data-ttu-id="9a5f2-116">Vous devez configurer manuellement d’autres zones de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9a5f2-116">There are areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that you must set up manually.</span></span> <span data-ttu-id="9a5f2-117">Celles-ci incluent l’ajout d’utilisateurs, la configuration de périodes comptables et la configuration d’axes analytiques pour la veille économique.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-117">These include adding users, setting up accounting periods, and setting up dimensions for business intelligence.</span></span> <span data-ttu-id="9a5f2-118">Pour plus d'informations, reportez-vous à [Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md).</span><span class="sxs-lookup"><span data-stu-id="9a5f2-118">For more information, see [Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md).</span></span>

 <span data-ttu-id="9a5f2-119">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-119">The following table describes a sequence of tasks with links to topics that describe them.</span></span>

|<span data-ttu-id="9a5f2-120">**Pour**</span><span class="sxs-lookup"><span data-stu-id="9a5f2-120">**To**</span></span>|<span data-ttu-id="9a5f2-121">**Voir**</span><span class="sxs-lookup"><span data-stu-id="9a5f2-121">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="9a5f2-122">Configurer l'interface utilisateur principale de RapidStart Services.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-122">Set up the main user interface of RapidStart Services.</span></span>|[<span data-ttu-id="9a5f2-123">Utiliser le tableau de bord Responsable de l'implémentation de RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="9a5f2-123">Use the RapidStart Services Implementer Role Center</span></span>](admin-how-to-use-the-rapidstart-services-role-center-to-track-progress.md)|  
|<span data-ttu-id="9a5f2-124">Créer une société et importer les données de configuration et les modèles de base.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-124">Create a new company and import basic setup data and templates.</span></span>|[<span data-ttu-id="9a5f2-125">Configurer une société</span><span class="sxs-lookup"><span data-stu-id="9a5f2-125">Set Up Company Configuration</span></span>](admin-set-up-company-configuration.md)|  
|<span data-ttu-id="9a5f2-126">Déployer le package configuré vers votre client pour l'implémentation.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-126">Deploy the configured package to your customer for implementation.</span></span>|[<span data-ttu-id="9a5f2-127">Appliquer des configurations aux nouvelles sociétés</span><span class="sxs-lookup"><span data-stu-id="9a5f2-127">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)|
|<span data-ttu-id="9a5f2-128">Définir et valider les valeurs de configuration de votre client pour toutes les zones de base, telles que les informations sur la société, la comptabilité, le stock, les ventes ou la fabrication.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-128">Define and validate your customer’s setup values for all core areas, such as company information, general ledger, inventory, sales, or manufacturing.</span></span>|[<span data-ttu-id="9a5f2-129">Collecter les valeurs de configuration client</span><span class="sxs-lookup"><span data-stu-id="9a5f2-129">Gather Customer Setup Values</span></span>](admin-gather-customer-setup-values.md)|  
|<span data-ttu-id="9a5f2-130">Configurer les enregistrements de données de base à l'aide de modèles pour préparer la migration des données client existantes.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-130">Configure core master data records using templates to prepare to migrate existing customer data.</span></span>|[<span data-ttu-id="9a5f2-131">Préparer la migration des données client</span><span class="sxs-lookup"><span data-stu-id="9a5f2-131">Prepare to Migrate Customer Data</span></span>](admin-use-templates-to-prepare-customer-data-for-migration.md)|  
|<span data-ttu-id="9a5f2-132">Définir les tables et les champs, valider les données client existantes et migrer les données vers la base de données [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9a5f2-132">Define tables and fields, validate existing customer data, and migrate data into the [!INCLUDE[d365fin](includes/d365fin_md.md)] database.</span></span>|[<span data-ttu-id="9a5f2-133">Migrer des données client</span><span class="sxs-lookup"><span data-stu-id="9a5f2-133">Migrate Customer Data</span></span>](admin-migrate-customer-data.md)|
|<span data-ttu-id="9a5f2-134">Préparez-vous à réutiliser des configurations d'entreprise dans d'autres sociétés.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-134">Prepare to reuse company configurations in other companies.</span></span>|[<span data-ttu-id="9a5f2-135">Créer des packages configuration de société personnalisés</span><span class="sxs-lookup"><span data-stu-id="9a5f2-135">Create Custom Company Configuration Packages</span></span>](admin-how-to-create-custom-company-configuration-packages.md)|
|<span data-ttu-id="9a5f2-136">Rechercher des solutions aux problèmes connus dans le kit d’outils RapidStart Services.</span><span class="sxs-lookup"><span data-stu-id="9a5f2-136">Find solutions to known issues in the RapidStart Services toolkit.</span></span>|[<span data-ttu-id="9a5f2-137">Conseils : RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="9a5f2-137">Tips and Tricks: RapidStart Services</span></span>](admin-tips-and-tricks-rapidstart-services.md)|  

## <a name="see-also"></a><span data-ttu-id="9a5f2-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a5f2-138">See Also</span></span>  
[<span data-ttu-id="9a5f2-139">Administration</span><span class="sxs-lookup"><span data-stu-id="9a5f2-139">Administration</span></span>](admin-setup-and-administration.md)  
<span data-ttu-id="9a5f2-140">[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="9a5f2-140">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="9a5f2-141">Configurer des domaines d'application complexes à l'aide des meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="9a5f2-141">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)   