---
title: Procédure de création d'une société | Microsoft Docs
description: Lorsque vous utilisez RapidStart Services, des tables et des pages sont créées, mais elles ne contiennent pas de données.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 49b2bb9a59c5bcd5d414b129acffaedfa0d0eaa1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820613"
---
# <a name="create-a-new-company"></a><span data-ttu-id="1182f-103">Créer une société</span><span class="sxs-lookup"><span data-stu-id="1182f-103">Create a New Company</span></span>
<span data-ttu-id="1182f-104">Pour utiliser RapidStart Services pour [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez d'abord créer une société pour laquelle vous souhaitez effectuer une implémentation client.</span><span class="sxs-lookup"><span data-stu-id="1182f-104">To use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="1182f-105">Lorsque vous créez une société, les tables et les pages standard de [!INCLUDE[d365fin](includes/d365fin_md.md)] sont créées, mais elles ne contiennent pas de données.</span><span class="sxs-lookup"><span data-stu-id="1182f-105">When you create a new company, the standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="1182f-106">Vous pouvez également appliquer des données de configuration spécifiques à votre société après l’avoir initialisée.</span><span class="sxs-lookup"><span data-stu-id="1182f-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="1182f-107">Les informations sont fournies dans un package de configuration, un fichier .rapidstart, qui fournit le contenu sous un format compressé.</span><span class="sxs-lookup"><span data-stu-id="1182f-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="1182f-108">Des exemples de packages de configuration, qui comprennent des fichiers spécifiques à un pays/une région, sont inclus avec la société de démonstration CRONUS.</span><span class="sxs-lookup"><span data-stu-id="1182f-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="1182f-109">Suivez la procédure suivante pour utiliser l'exemple de package de configuration avec une nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="1182f-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="1182f-110">Pour utiliser l'exemple de package de configuration BASICCONFIG</span><span class="sxs-lookup"><span data-stu-id="1182f-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="1182f-111">Ouvrez la société CRONUS International Ltd.</span><span class="sxs-lookup"><span data-stu-id="1182f-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="1182f-112">Pour plus d'informations, voir [Modification des paramètres de base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="1182f-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="1182f-113">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Packages configuration**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="1182f-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="1182f-114">Sélectionnez le package BASICCONFIG dans la liste, puis sélectionnez l'action **Exporter package**.</span><span class="sxs-lookup"><span data-stu-id="1182f-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="1182f-115">Suivez la procédure suivante pour créer une société, puis utilisez le package BASICCONFIG dans le cadre du processus.</span><span class="sxs-lookup"><span data-stu-id="1182f-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="1182f-116">Création d'une nouvelle société</span><span class="sxs-lookup"><span data-stu-id="1182f-116">To create a new company</span></span>  
1. <span data-ttu-id="1182f-117">Créez une nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="1182f-117">Create a new company.</span></span> <span data-ttu-id="1182f-118">Pour plus d'informations, voir [Création de sociétés dans [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="1182f-118">For more information, see [Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="1182f-119">Dans le tableau de bord Responsable de l'implémentation de RapidStart Services, vous pouvez maintenant importer le package configuration que vous avez exporté de la société CRONUS International Ltd.</span><span class="sxs-lookup"><span data-stu-id="1182f-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="1182f-120">Une fois que vous avez créé une société, certaines tables se renseignent automatiquement, même si aucun modèle de société n'est appliqué.</span><span class="sxs-lookup"><span data-stu-id="1182f-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="1182f-121">Par exemple, vous pouvez consulter les codes standard pour les transactions par lots et la validation sur la page **Code origine**.</span><span class="sxs-lookup"><span data-stu-id="1182f-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="1182f-122">Si vous disposez d'une version locale de [!INCLUDE[d365fin](includes/d365fin_md.md)], consultez cette table en tenant compte d'éventuels problèmes de langue locale.</span><span class="sxs-lookup"><span data-stu-id="1182f-122">If you provide a local version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="1182f-123">À propos des tables de données</span><span class="sxs-lookup"><span data-stu-id="1182f-123">About Data Tables</span></span>
<span data-ttu-id="1182f-124">Les tables de données [!INCLUDE[d365fin](includes/d365fin_md.md)] existent en deux types de base : principale et Paramètres.</span><span class="sxs-lookup"><span data-stu-id="1182f-124">[!INCLUDE[d365fin](includes/d365fin_md.md)], data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="1182f-125">Lorsque vous paramétrez une configuration de société, vous pouvez utiliser ces types afin de cibler votre stratégie de configuration.</span><span class="sxs-lookup"><span data-stu-id="1182f-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="1182f-126">Tables de données principales</span><span class="sxs-lookup"><span data-stu-id="1182f-126">Master Data Tables</span></span>  
<span data-ttu-id="1182f-127">Le tableau suivant répertorie certaines tables de données principales.</span><span class="sxs-lookup"><span data-stu-id="1182f-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="1182f-128">Lorsque vous lancez une nouvelle société, ces tables sont vides.</span><span class="sxs-lookup"><span data-stu-id="1182f-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="1182f-129">N° table</span><span class="sxs-lookup"><span data-stu-id="1182f-129">Table No.</span></span>|<span data-ttu-id="1182f-130">Nom de table</span><span class="sxs-lookup"><span data-stu-id="1182f-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="1182f-131">15</span><span class="sxs-lookup"><span data-stu-id="1182f-131">15</span></span>|<span data-ttu-id="1182f-132">Compte général</span><span class="sxs-lookup"><span data-stu-id="1182f-132">G/L Account</span></span>|  
|<span data-ttu-id="1182f-133">18</span><span class="sxs-lookup"><span data-stu-id="1182f-133">18</span></span>|<span data-ttu-id="1182f-134">Client</span><span class="sxs-lookup"><span data-stu-id="1182f-134">Customer</span></span>|  
|<span data-ttu-id="1182f-135">23</span><span class="sxs-lookup"><span data-stu-id="1182f-135">23</span></span>|<span data-ttu-id="1182f-136">Fournisseur</span><span class="sxs-lookup"><span data-stu-id="1182f-136">Vendor</span></span>|  
|<span data-ttu-id="1182f-137">27</span><span class="sxs-lookup"><span data-stu-id="1182f-137">27</span></span>|<span data-ttu-id="1182f-138">Article</span><span class="sxs-lookup"><span data-stu-id="1182f-138">Item</span></span>|  
|<span data-ttu-id="1182f-139">5050</span><span class="sxs-lookup"><span data-stu-id="1182f-139">5050</span></span>|<span data-ttu-id="1182f-140">Contact</span><span class="sxs-lookup"><span data-stu-id="1182f-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="1182f-141">Tables de données de configuration</span><span class="sxs-lookup"><span data-stu-id="1182f-141">Setup Data Tables</span></span>  
<span data-ttu-id="1182f-142">Le tableau suivant répertorie certaines tables de données de configuration à partir desquelles vous capturez les informations de configuration dans le questionnaire de configuration.</span><span class="sxs-lookup"><span data-stu-id="1182f-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="1182f-143">Ces tables contiennent des informations de base lors de la création de la société.</span><span class="sxs-lookup"><span data-stu-id="1182f-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="1182f-144">N° table</span><span class="sxs-lookup"><span data-stu-id="1182f-144">Table No.</span></span>|<span data-ttu-id="1182f-145">Nom de table</span><span class="sxs-lookup"><span data-stu-id="1182f-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="1182f-146">98</span><span class="sxs-lookup"><span data-stu-id="1182f-146">98</span></span>|<span data-ttu-id="1182f-147">Paramètres comptabilité</span><span class="sxs-lookup"><span data-stu-id="1182f-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="1182f-148">311</span><span class="sxs-lookup"><span data-stu-id="1182f-148">311</span></span>|<span data-ttu-id="1182f-149">Paramètres ventes</span><span class="sxs-lookup"><span data-stu-id="1182f-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="1182f-150">312</span><span class="sxs-lookup"><span data-stu-id="1182f-150">312</span></span>|<span data-ttu-id="1182f-151">Paramètres achats</span><span class="sxs-lookup"><span data-stu-id="1182f-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="1182f-152">313</span><span class="sxs-lookup"><span data-stu-id="1182f-152">313</span></span>|<span data-ttu-id="1182f-153">Paramètres stock</span><span class="sxs-lookup"><span data-stu-id="1182f-153">Inventory Setup</span></span>|  

<span data-ttu-id="1182f-154">Outre des tables de données de paramétrage, [!INCLUDE[d365fin](includes/d365fin_md.md)] dispose également de tables de données de type paramétrage qui spécifient des informations de base sur la société et ses processus entreprise.</span><span class="sxs-lookup"><span data-stu-id="1182f-154">In addition to setup data tables, [!INCLUDE[d365fin](includes/d365fin_md.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="1182f-155">Le tableau suivant répertorie certaines d'entre elles.</span><span class="sxs-lookup"><span data-stu-id="1182f-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="1182f-156">N° table</span><span class="sxs-lookup"><span data-stu-id="1182f-156">Table No.</span></span>|<span data-ttu-id="1182f-157">Nom de table</span><span class="sxs-lookup"><span data-stu-id="1182f-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="1182f-158">3</span><span class="sxs-lookup"><span data-stu-id="1182f-158">3</span></span>|<span data-ttu-id="1182f-159">Conditions de paiement</span><span class="sxs-lookup"><span data-stu-id="1182f-159">Payment Terms</span></span>|  
|<span data-ttu-id="1182f-160">4</span><span class="sxs-lookup"><span data-stu-id="1182f-160">4</span></span>|<span data-ttu-id="1182f-161">Devise</span><span class="sxs-lookup"><span data-stu-id="1182f-161">Currency</span></span>|  
|<span data-ttu-id="1182f-162">6</span><span class="sxs-lookup"><span data-stu-id="1182f-162">6</span></span>|<span data-ttu-id="1182f-163">Groupes prix client</span><span class="sxs-lookup"><span data-stu-id="1182f-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="1182f-164">5700</span><span class="sxs-lookup"><span data-stu-id="1182f-164">5700</span></span>|<span data-ttu-id="1182f-165">Point de stock</span><span class="sxs-lookup"><span data-stu-id="1182f-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="1182f-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1182f-166">See Also</span></span>  
[<span data-ttu-id="1182f-167">Appliquer des configurations aux nouvelles sociétés</span><span class="sxs-lookup"><span data-stu-id="1182f-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="1182f-168">Configuration d'une société avec RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="1182f-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="1182f-169">Administration</span><span class="sxs-lookup"><span data-stu-id="1182f-169">Administration</span></span>](admin-setup-and-administration.md)
