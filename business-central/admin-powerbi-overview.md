---
title: Vue d’ensemble Architecture et composant d’intégration Power BI pour Business Central| Microsoft Docs
description: Il est facile d’obtenir des informations exploitables, de la veille économique et des KPI de vos applications Business Central pour Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 23a0c72775dbddc89a81105de3b2ed79d1f09432
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753785"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a><span data-ttu-id="283a2-103">Vue d’ensemble Architecture et composant d’intégration Power BI pour [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="283a2-103">Power BI Integration Component and Architecture Overview for [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

<span data-ttu-id="283a2-104">Dans cet article, vous découvrirez les différents aspects de l’intégration de Power BI à [!INCLUDE[prod_short](includes/prod_short.md)] pour vous aider à comprendre sa mise en œuvre et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="283a2-104">In this article, you'll learn about the different aspects of Power BI integration with [!INCLUDE[prod_short](includes/prod_short.md)] to help you understand its implementation and use.</span></span>

## <a name="components"></a><span data-ttu-id="283a2-105">Composants</span><span class="sxs-lookup"><span data-stu-id="283a2-105">Components</span></span>

<span data-ttu-id="283a2-106">Le tableau suivant décrit les principaux composants impliqués dans l’intégration Power BI.</span><span class="sxs-lookup"><span data-stu-id="283a2-106">The following table describes the major components involved with Power BI integration.</span></span>

|<span data-ttu-id="283a2-107">Composant</span><span class="sxs-lookup"><span data-stu-id="283a2-107">Component</span></span>|<span data-ttu-id="283a2-108">Description</span><span class="sxs-lookup"><span data-stu-id="283a2-108">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="283a2-109">Power BI</span><span class="sxs-lookup"><span data-stu-id="283a2-109">Power BI</span></span>|<span data-ttu-id="283a2-110">Un service d’hébergement et de gestion des états basé sur le cloud.</span><span class="sxs-lookup"><span data-stu-id="283a2-110">A cloud-based report hosting and management service.</span></span>|
|<span data-ttu-id="283a2-111">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="283a2-111">Power BI Desktop</span></span>|<span data-ttu-id="283a2-112">Un outil de création pour créer des états et des tableaux de bord, et vous permet d’exécuter des états.</span><span class="sxs-lookup"><span data-stu-id="283a2-112">An authoring tool for building reports and dashboards, and allows you to run reports.</span></span> <span data-ttu-id="283a2-113">Il est disponible en téléchargement gratuit sur Microsoft Store et est installé localement.</span><span class="sxs-lookup"><span data-stu-id="283a2-113">It's available as a free download on Microsoft Store and is installed locally.</span></span>|
|[!INCLUDE[prod_short](includes/prod_short.md)]|<span data-ttu-id="283a2-114">Solution en ligne ou sur site avec des connecteurs exposés à Power BI et possibilité d’intégrer une partie de Power BI.</span><span class="sxs-lookup"><span data-stu-id="283a2-114">Online or on-premises solution with connectors exposed to Power BI and the ability to embed a Power BI part.</span></span>|

## <a name="whats-available-from-the-start"></a><span data-ttu-id="283a2-115">Ce qui est disponible dès le départ</span><span class="sxs-lookup"><span data-stu-id="283a2-115">What's available from the start</span></span>

<span data-ttu-id="283a2-116">Le tableau suivant décrit les fonctionnalités disponibles.</span><span class="sxs-lookup"><span data-stu-id="283a2-116">The following table describes available features.</span></span>

|<span data-ttu-id="283a2-117">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="283a2-117">Feature</span></span>|<span data-ttu-id="283a2-118">Support [!INCLUDE[prod_short](includes/prod_short.md)] en ligne ou sur site</span><span class="sxs-lookup"><span data-stu-id="283a2-118">[!INCLUDE[prod_short](includes/prod_short.md)] online or on-premises support</span></span>|
|-------|---------------------|
|<span data-ttu-id="283a2-119">Connecteurs Power BI</span><span class="sxs-lookup"><span data-stu-id="283a2-119">Power BI connectors</span></span>|<span data-ttu-id="283a2-120">Les deux.</span><span class="sxs-lookup"><span data-stu-id="283a2-120">Both.</span></span> <span data-ttu-id="283a2-121">Différents connecteurs pour la solution ligne et la solution sur site.</span><span class="sxs-lookup"><span data-stu-id="283a2-121">Different connectors for online and on-premises.</span></span> <span data-ttu-id="283a2-122">Connecteur identique utilisé pour le service Power BI Desktop et Power BI</span><span class="sxs-lookup"><span data-stu-id="283a2-122">Same connector used for Power BI Desktop and Power BI Service</span></span> |
|<span data-ttu-id="283a2-123">Expérience intégrée pour afficher un état donné dans un Récapitulatif dans [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="283a2-123">Embedded experience for viewing a given report inside a FactBox in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>|<span data-ttu-id="283a2-124">Les deux.</span><span class="sxs-lookup"><span data-stu-id="283a2-124">Both.</span></span> <span data-ttu-id="283a2-125">Nécessite une configuration pour afficher les états sur site.</span><span class="sxs-lookup"><span data-stu-id="283a2-125">Requires configuration to display reports for on-premises.</span></span>|
|<span data-ttu-id="283a2-126">Gestion des états Power BI depuis [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="283a2-126">Power BI report management from [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>|<span data-ttu-id="283a2-127">En ligne</span><span class="sxs-lookup"><span data-stu-id="283a2-127">Online</span></span>|
|<span data-ttu-id="283a2-128">États Power BI par défaut sur les tableaux de bord déployés vers Power BI</span><span class="sxs-lookup"><span data-stu-id="283a2-128">Default Power BI reports on role centers deployed to Power BI</span></span>|<span data-ttu-id="283a2-129">En ligne</span><span class="sxs-lookup"><span data-stu-id="283a2-129">Online</span></span>|
|<span data-ttu-id="283a2-130">Applications Power BI sur Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="283a2-130">Power BI Apps on Microsoft AppSource</span></span>|<span data-ttu-id="283a2-131">En ligne.</span><span class="sxs-lookup"><span data-stu-id="283a2-131">Online.</span></span>|

## <a name="architecture"></a><span data-ttu-id="283a2-132">Architecture</span><span class="sxs-lookup"><span data-stu-id="283a2-132">Architecture</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="283a2-133">s’intègre à Power BI via un connecteur utilisant OData.</span><span class="sxs-lookup"><span data-stu-id="283a2-133">integrates with Power BI through a connector using OData.</span></span> <span data-ttu-id="283a2-134">La source de données pour les états Power BI est exposée comme services Web OData.</span><span class="sxs-lookup"><span data-stu-id="283a2-134">The data source for Power BI reports is exposed as OData web services.</span></span>

![Architecture Power BI pour l’intégration avec Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a><span data-ttu-id="283a2-136">Flux général</span><span class="sxs-lookup"><span data-stu-id="283a2-136">General Flow</span></span>

<span data-ttu-id="283a2-137">Le diagramme suivant illustre le flux de travail de base pour les utilisateurs lors de la connexion de [!INCLUDE[prod_short](includes/prod_short.md)] à Power BI.</span><span class="sxs-lookup"><span data-stu-id="283a2-137">The following diagram illustrates the basic workflow for users when connecting [!INCLUDE[prod_short](includes/prod_short.md)] to Power BI.</span></span>

![Flux de travai Power BI pour l’intégration avec Business Central](./media/power-bi-flow.png)

1. <span data-ttu-id="283a2-139">L’utilisateur s’inscrit à un compte Power BI.</span><span class="sxs-lookup"><span data-stu-id="283a2-139">User signs up for a Power BI account.</span></span>
2. <span data-ttu-id="283a2-140">L’utilisateur se connecte à Power BI depuis [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="283a2-140">User connects to Power BI from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
3. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="283a2-141">vérifie la licence.</span><span class="sxs-lookup"><span data-stu-id="283a2-141">verifies the license.</span></span>
4. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="283a2-142">déploie les états par défaut sur le service Power BI.</span><span class="sxs-lookup"><span data-stu-id="283a2-142">deploys default reports to the Power BI service.</span></span> <span data-ttu-id="283a2-143">Cette étape ne se produit que pour [!INCLUDE[prod_short](includes/prod_short.md)] en ligne.</span><span class="sxs-lookup"><span data-stu-id="283a2-143">This step only happens for [!INCLUDE[prod_short](includes/prod_short.md)] online.</span></span>
5. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="283a2-144">rend les états dans Power BI disponibles pour la sélection dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="283a2-144">makes reports in Power BI available for selection in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="283a2-145">Les états par défaut sont automatiquement affichés dans des parties de Power BI.</span><span class="sxs-lookup"><span data-stu-id="283a2-145">Default reports are automatically displayed in Power BI parts.</span></span>
6. <span data-ttu-id="283a2-146">L’utilisateur crée un état dans Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="283a2-146">User creates a report in Power BI Desktop.</span></span>
7. <span data-ttu-id="283a2-147">L’utilisateur publie l’état vers le service Power BI.</span><span class="sxs-lookup"><span data-stu-id="283a2-147">User publishes the report to the Power BI service.</span></span> <span data-ttu-id="283a2-148">Les états sont ensuite disponibles pour la sélection dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="283a2-148">The reports are then available for selection in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="283a2-149">Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="283a2-149">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="283a2-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="283a2-150">See Also</span></span>

[<span data-ttu-id="283a2-151">Business Central et Power BI</span><span class="sxs-lookup"><span data-stu-id="283a2-151">Business Central and Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="283a2-152">Power BI pour les consommateurs</span><span class="sxs-lookup"><span data-stu-id="283a2-152">Power BI for consumers</span></span>](/power-bi/consumer/end-user-consumer)  
[<span data-ttu-id="283a2-153">Le « nouveau look » du service Power BI</span><span class="sxs-lookup"><span data-stu-id="283a2-153">The 'new look' of the Power BI service</span></span>](/power-bi/service-new-look)  
[<span data-ttu-id="283a2-154">Démarrage rapide : Se connecter aux données dans Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="283a2-154">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
[<span data-ttu-id="283a2-155">Documentation Power BI</span><span class="sxs-lookup"><span data-stu-id="283a2-155">Power BI documentation</span></span>](/power-bi/)  
[<span data-ttu-id="283a2-156">Veille économique</span><span class="sxs-lookup"><span data-stu-id="283a2-156">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="283a2-157">Mise en route</span><span class="sxs-lookup"><span data-stu-id="283a2-157">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="283a2-158">Importation des données métier à partir d’autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="283a2-158">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="283a2-159">[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="283a2-159">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
<span data-ttu-id="283a2-160">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="283a2-160">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
<span data-ttu-id="283a2-161">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données Power Apps](across-how-use-financials-data-source-powerapps.md)</span><span class="sxs-lookup"><span data-stu-id="283a2-161">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power Apps Data Source](across-how-use-financials-data-source-powerapps.md)</span></span>  
<span data-ttu-id="283a2-162">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)] dans Power Automate](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="283a2-162">[Using [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
