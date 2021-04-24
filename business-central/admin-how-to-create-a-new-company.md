---
title: Procédure de création d’une société | Microsoft Docs
description: Lorsque vous utilisez RapidStart Services, des tables et des pages sont créées, mais elles ne contiennent pas de données.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c21d86c67c6020d1a32da4816246bc7aaf96c2ca
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779897"
---
# <a name="create-a-new-company"></a><span data-ttu-id="7df6a-103">Créer une société</span><span class="sxs-lookup"><span data-stu-id="7df6a-103">Create a New Company</span></span>
<span data-ttu-id="7df6a-104">Pour utiliser RapidStart Services pour [!INCLUDE[prod_short](includes/prod_short.md)], vous devez d’abord créer une société pour laquelle vous souhaitez effectuer une implémentation client.</span><span class="sxs-lookup"><span data-stu-id="7df6a-104">To use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="7df6a-105">Lorsque vous créez une société, les tables et les pages standard de [!INCLUDE[prod_short](includes/prod_short.md)] sont créées, mais elles ne contiennent pas de données.</span><span class="sxs-lookup"><span data-stu-id="7df6a-105">When you create a new company, the standard [!INCLUDE[prod_short](includes/prod_short.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="7df6a-106">Vous pouvez également appliquer des données de configuration spécifiques à votre société après l’avoir initialisée.</span><span class="sxs-lookup"><span data-stu-id="7df6a-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="7df6a-107">Les informations sont fournies dans un package de configuration, un fichier .rapidstart, qui fournit le contenu sous un format compressé.</span><span class="sxs-lookup"><span data-stu-id="7df6a-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="7df6a-108">Des exemples de packages de configuration, qui comprennent des fichiers spécifiques à un pays/une région, sont inclus avec la société de démonstration CRONUS.</span><span class="sxs-lookup"><span data-stu-id="7df6a-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="7df6a-109">Suivez la procédure suivante pour utiliser l’exemple de package de configuration avec une nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="7df6a-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="7df6a-110">Pour utiliser l’exemple de package de configuration BASICCONFIG</span><span class="sxs-lookup"><span data-stu-id="7df6a-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="7df6a-111">Ouvrez la société CRONUS International Ltd.</span><span class="sxs-lookup"><span data-stu-id="7df6a-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="7df6a-112">Pour plus d’informations, voir [Modifier les paramètres de base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="7df6a-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="7df6a-113">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Packages configuration**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7df6a-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="7df6a-114">Sélectionnez le package BASICCONFIG dans la liste, puis sélectionnez l’action **Exporter package**.</span><span class="sxs-lookup"><span data-stu-id="7df6a-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="7df6a-115">Suivez la procédure suivante pour créer une société, puis utilisez le package BASICCONFIG dans le cadre du processus.</span><span class="sxs-lookup"><span data-stu-id="7df6a-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="7df6a-116">Création d’une nouvelle société</span><span class="sxs-lookup"><span data-stu-id="7df6a-116">To create a new company</span></span>  
1. <span data-ttu-id="7df6a-117">Créez une nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="7df6a-117">Create a new company.</span></span> <span data-ttu-id="7df6a-118">Pour plus d’informations, voir [Création de sociétés dans [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="7df6a-118">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="7df6a-119">Dans le tableau de bord Responsable de l’implémentation de RapidStart Services, vous pouvez maintenant importer le package de configuration que vous avez exporté de la société CRONUS International Ltd.</span><span class="sxs-lookup"><span data-stu-id="7df6a-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="7df6a-120">Une fois que vous avez créé une société, certaines tables se renseignent automatiquement, même si aucun modèle de société n’est appliqué.</span><span class="sxs-lookup"><span data-stu-id="7df6a-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="7df6a-121">Par exemple, vous pouvez consulter les codes standard pour les transactions par lots et la validation sur la page **Code origine**.</span><span class="sxs-lookup"><span data-stu-id="7df6a-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="7df6a-122">Si vous disposez d’une version locale de [!INCLUDE[prod_short](includes/prod_short.md)], consultez cette table en tenant compte d’éventuels problèmes de langue locale.</span><span class="sxs-lookup"><span data-stu-id="7df6a-122">If you provide a local version of [!INCLUDE[prod_short](includes/prod_short.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="7df6a-123">À propos des tables de données</span><span class="sxs-lookup"><span data-stu-id="7df6a-123">About Data Tables</span></span>
<span data-ttu-id="7df6a-124">Les tables de données [!INCLUDE[prod_short](includes/prod_short.md)] existent en deux types de base : principale et Paramètres.</span><span class="sxs-lookup"><span data-stu-id="7df6a-124">[!INCLUDE[prod_short](includes/prod_short.md)], data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="7df6a-125">Lorsque vous paramétrez une configuration de société, vous pouvez utiliser ces types afin de cibler votre stratégie de configuration.</span><span class="sxs-lookup"><span data-stu-id="7df6a-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="7df6a-126">Tables de données principales</span><span class="sxs-lookup"><span data-stu-id="7df6a-126">Master Data Tables</span></span>  
<span data-ttu-id="7df6a-127">Le tableau suivant répertorie certaines tables de données principales.</span><span class="sxs-lookup"><span data-stu-id="7df6a-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="7df6a-128">Lorsque vous lancez une nouvelle société, ces tables sont vides.</span><span class="sxs-lookup"><span data-stu-id="7df6a-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="7df6a-129">N° table</span><span class="sxs-lookup"><span data-stu-id="7df6a-129">Table No.</span></span>|<span data-ttu-id="7df6a-130">Nom de table</span><span class="sxs-lookup"><span data-stu-id="7df6a-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="7df6a-131">15</span><span class="sxs-lookup"><span data-stu-id="7df6a-131">15</span></span>|<span data-ttu-id="7df6a-132">Compte général</span><span class="sxs-lookup"><span data-stu-id="7df6a-132">G/L Account</span></span>|  
|<span data-ttu-id="7df6a-133">18</span><span class="sxs-lookup"><span data-stu-id="7df6a-133">18</span></span>|<span data-ttu-id="7df6a-134">Client</span><span class="sxs-lookup"><span data-stu-id="7df6a-134">Customer</span></span>|  
|<span data-ttu-id="7df6a-135">23</span><span class="sxs-lookup"><span data-stu-id="7df6a-135">23</span></span>|<span data-ttu-id="7df6a-136">Fournisseur</span><span class="sxs-lookup"><span data-stu-id="7df6a-136">Vendor</span></span>|  
|<span data-ttu-id="7df6a-137">27</span><span class="sxs-lookup"><span data-stu-id="7df6a-137">27</span></span>|<span data-ttu-id="7df6a-138">Article</span><span class="sxs-lookup"><span data-stu-id="7df6a-138">Item</span></span>|  
|<span data-ttu-id="7df6a-139">5050</span><span class="sxs-lookup"><span data-stu-id="7df6a-139">5050</span></span>|<span data-ttu-id="7df6a-140">Contact</span><span class="sxs-lookup"><span data-stu-id="7df6a-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="7df6a-141">Tables de données de configuration</span><span class="sxs-lookup"><span data-stu-id="7df6a-141">Setup Data Tables</span></span>  
<span data-ttu-id="7df6a-142">Le tableau suivant répertorie certaines tables de données de configuration à partir desquelles vous capturez les informations de configuration dans le questionnaire de configuration.</span><span class="sxs-lookup"><span data-stu-id="7df6a-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="7df6a-143">Ces tables contiennent des informations de base lors de la création de la société.</span><span class="sxs-lookup"><span data-stu-id="7df6a-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="7df6a-144">N° table</span><span class="sxs-lookup"><span data-stu-id="7df6a-144">Table No.</span></span>|<span data-ttu-id="7df6a-145">Nom de table</span><span class="sxs-lookup"><span data-stu-id="7df6a-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="7df6a-146">98</span><span class="sxs-lookup"><span data-stu-id="7df6a-146">98</span></span>|<span data-ttu-id="7df6a-147">Paramètres comptabilité</span><span class="sxs-lookup"><span data-stu-id="7df6a-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="7df6a-148">311</span><span class="sxs-lookup"><span data-stu-id="7df6a-148">311</span></span>|<span data-ttu-id="7df6a-149">Paramètres ventes</span><span class="sxs-lookup"><span data-stu-id="7df6a-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="7df6a-150">312</span><span class="sxs-lookup"><span data-stu-id="7df6a-150">312</span></span>|<span data-ttu-id="7df6a-151">Paramètres achats</span><span class="sxs-lookup"><span data-stu-id="7df6a-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="7df6a-152">313</span><span class="sxs-lookup"><span data-stu-id="7df6a-152">313</span></span>|<span data-ttu-id="7df6a-153">Paramètres stock</span><span class="sxs-lookup"><span data-stu-id="7df6a-153">Inventory Setup</span></span>|  

<span data-ttu-id="7df6a-154">Outre des tables de données de paramétrage, [!INCLUDE[prod_short](includes/prod_short.md)] dispose également de tables de données de type paramétrage qui spécifient des informations de base sur la société et ses processus entreprise.</span><span class="sxs-lookup"><span data-stu-id="7df6a-154">In addition to setup data tables, [!INCLUDE[prod_short](includes/prod_short.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="7df6a-155">Le tableau suivant répertorie certaines d’entre elles.</span><span class="sxs-lookup"><span data-stu-id="7df6a-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="7df6a-156">N° table</span><span class="sxs-lookup"><span data-stu-id="7df6a-156">Table No.</span></span>|<span data-ttu-id="7df6a-157">Nom de table</span><span class="sxs-lookup"><span data-stu-id="7df6a-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="7df6a-158">3</span><span class="sxs-lookup"><span data-stu-id="7df6a-158">3</span></span>|<span data-ttu-id="7df6a-159">Conditions de paiement</span><span class="sxs-lookup"><span data-stu-id="7df6a-159">Payment Terms</span></span>|  
|<span data-ttu-id="7df6a-160">4</span><span class="sxs-lookup"><span data-stu-id="7df6a-160">4</span></span>|<span data-ttu-id="7df6a-161">Devise</span><span class="sxs-lookup"><span data-stu-id="7df6a-161">Currency</span></span>|  
|<span data-ttu-id="7df6a-162">6</span><span class="sxs-lookup"><span data-stu-id="7df6a-162">6</span></span>|<span data-ttu-id="7df6a-163">Groupes prix client</span><span class="sxs-lookup"><span data-stu-id="7df6a-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="7df6a-164">5700</span><span class="sxs-lookup"><span data-stu-id="7df6a-164">5700</span></span>|<span data-ttu-id="7df6a-165">Point de stock</span><span class="sxs-lookup"><span data-stu-id="7df6a-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="7df6a-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7df6a-166">See Also</span></span>  
[<span data-ttu-id="7df6a-167">Appliquer des configurations aux nouvelles sociétés</span><span class="sxs-lookup"><span data-stu-id="7df6a-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="7df6a-168">Configuration d’une société avec RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="7df6a-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="7df6a-169">Administration</span><span class="sxs-lookup"><span data-stu-id="7df6a-169">Administration</span></span>](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]