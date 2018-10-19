---
title: "Procédure de création d'une société | Microsoft Docs"
description: "Lorsque vous utilisez RapidStart Services, des tables et des pages sont créées, mais elles ne contiennent pas de données."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 3b213e85e6b162e875a31f0ab69e3e1f4af9653f
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="create-a-new-company"></a><span data-ttu-id="80ca0-103">Créer une société</span><span class="sxs-lookup"><span data-stu-id="80ca0-103">Create a New Company</span></span>
<span data-ttu-id="80ca0-104">Pour utiliser RapidStart Services pour [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez d'abord créer une société pour laquelle vous souhaitez effectuer une implémentation client.</span><span class="sxs-lookup"><span data-stu-id="80ca0-104">To use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="80ca0-105">Lorsque vous créez une société, les tables et les pages standard de [!INCLUDE[d365fin](includes/d365fin_md.md)] sont créées, mais elles ne contiennent pas de données.</span><span class="sxs-lookup"><span data-stu-id="80ca0-105">When you create a new company, the standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="80ca0-106">Vous pouvez également appliquer des données de configuration spécifiques à votre société après l’avoir initialisée.</span><span class="sxs-lookup"><span data-stu-id="80ca0-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="80ca0-107">Les informations sont fournies dans un package de configuration, un fichier .rapidstart, qui fournit le contenu sous un format compressé.</span><span class="sxs-lookup"><span data-stu-id="80ca0-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="80ca0-108">Des exemples de packages de configuration, qui comprennent des fichiers spécifiques à un pays/une région, sont inclus avec la société de démonstration CRONUS.</span><span class="sxs-lookup"><span data-stu-id="80ca0-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="80ca0-109">Suivez la procédure suivante pour utiliser l'exemple de package de configuration avec une nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="80ca0-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="80ca0-110">Pour utiliser l'exemple de package de configuration BASICCONFIG</span><span class="sxs-lookup"><span data-stu-id="80ca0-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="80ca0-111">Ouvrez la société CRONUS International Ltd.</span><span class="sxs-lookup"><span data-stu-id="80ca0-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="80ca0-112">Pour plus d'informations, voir [Modification des paramètres de base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="80ca0-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="80ca0-113">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Packages configuration**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="80ca0-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="80ca0-114">Sélectionnez le package BASICCONFIG dans la liste, puis sélectionnez l'action **Exporter package**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="80ca0-115">Suivez la procédure suivante pour créer une société, puis utilisez le package BASICCONFIG dans le cadre du processus.</span><span class="sxs-lookup"><span data-stu-id="80ca0-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="80ca0-116">Création d'une nouvelle société</span><span class="sxs-lookup"><span data-stu-id="80ca0-116">To create a new company</span></span>  
1. <span data-ttu-id="80ca0-117">Créez une nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="80ca0-117">Create a new company.</span></span> <span data-ttu-id="80ca0-118">Pour plus d'informations, voir [Création de sociétés dans [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="80ca0-118">For more information, see [Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="80ca0-119">Dans le tableau de bord Responsable de l'implémentation de RapidStart Services, vous pouvez maintenant importer le package configuration que vous avez exporté de la société CRONUS International Ltd.</span><span class="sxs-lookup"><span data-stu-id="80ca0-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="80ca0-120">Une fois que vous avez créé une société, certaines tables se renseignent automatiquement, même si aucun modèle de société n'est appliqué.</span><span class="sxs-lookup"><span data-stu-id="80ca0-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="80ca0-121">Par exemple, vous pouvez consulter les codes standard pour les transactions par lots et la validation dans la fenêtre **Code origine**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-121">For example, you can review the standard codes for posting and batch transactions in the **Source Code** window.</span></span> <span data-ttu-id="80ca0-122">Si vous disposez d'une version locale de [!INCLUDE[d365fin](includes/d365fin_md.md)], consultez cette table en tenant compte d'éventuels problèmes de langue locale.</span><span class="sxs-lookup"><span data-stu-id="80ca0-122">If you provide a local version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="80ca0-123">À propos des tables de données</span><span class="sxs-lookup"><span data-stu-id="80ca0-123">About Data Tables</span></span>
<span data-ttu-id="80ca0-124">Les tables de données [!INCLUDE[d365fin](includes/d365fin_md.md)] existent en deux types de base : principale et Paramètres.</span><span class="sxs-lookup"><span data-stu-id="80ca0-124">[!INCLUDE[d365fin](includes/d365fin_md.md)], data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="80ca0-125">Lorsque vous paramétrez une configuration de société, vous pouvez utiliser ces types afin de cibler votre stratégie de configuration.</span><span class="sxs-lookup"><span data-stu-id="80ca0-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="80ca0-126">Tables de données principales</span><span class="sxs-lookup"><span data-stu-id="80ca0-126">Master Data Tables</span></span>  
<span data-ttu-id="80ca0-127">Le tableau suivant répertorie certaines tables de données principales.</span><span class="sxs-lookup"><span data-stu-id="80ca0-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="80ca0-128">Lorsque vous lancez une nouvelle société, ces tables sont vides.</span><span class="sxs-lookup"><span data-stu-id="80ca0-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="80ca0-129">N° table</span><span class="sxs-lookup"><span data-stu-id="80ca0-129">Table No.</span></span>|<span data-ttu-id="80ca0-130">Nom de table</span><span class="sxs-lookup"><span data-stu-id="80ca0-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="80ca0-131">15</span><span class="sxs-lookup"><span data-stu-id="80ca0-131">15</span></span>|<span data-ttu-id="80ca0-132">Compte général</span><span class="sxs-lookup"><span data-stu-id="80ca0-132">G/L Account</span></span>|  
|<span data-ttu-id="80ca0-133">18</span><span class="sxs-lookup"><span data-stu-id="80ca0-133">18</span></span>|<span data-ttu-id="80ca0-134">Client</span><span class="sxs-lookup"><span data-stu-id="80ca0-134">Customer</span></span>|  
|<span data-ttu-id="80ca0-135">23</span><span class="sxs-lookup"><span data-stu-id="80ca0-135">23</span></span>|<span data-ttu-id="80ca0-136">Fournisseur</span><span class="sxs-lookup"><span data-stu-id="80ca0-136">Vendor</span></span>|  
|<span data-ttu-id="80ca0-137">27</span><span class="sxs-lookup"><span data-stu-id="80ca0-137">27</span></span>|<span data-ttu-id="80ca0-138">Article</span><span class="sxs-lookup"><span data-stu-id="80ca0-138">Item</span></span>|  
|<span data-ttu-id="80ca0-139">5050</span><span class="sxs-lookup"><span data-stu-id="80ca0-139">5050</span></span>|<span data-ttu-id="80ca0-140">Contact</span><span class="sxs-lookup"><span data-stu-id="80ca0-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="80ca0-141">Tables de données de configuration</span><span class="sxs-lookup"><span data-stu-id="80ca0-141">Setup Data Tables</span></span>  
<span data-ttu-id="80ca0-142">Le tableau suivant répertorie certaines tables de données de configuration à partir desquelles vous capturez les informations de configuration dans le questionnaire de configuration.</span><span class="sxs-lookup"><span data-stu-id="80ca0-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="80ca0-143">Ces tables contiennent des informations de base lors de la création de la société.</span><span class="sxs-lookup"><span data-stu-id="80ca0-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="80ca0-144">N° table</span><span class="sxs-lookup"><span data-stu-id="80ca0-144">Table No.</span></span>|<span data-ttu-id="80ca0-145">Nom de table</span><span class="sxs-lookup"><span data-stu-id="80ca0-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="80ca0-146">98</span><span class="sxs-lookup"><span data-stu-id="80ca0-146">98</span></span>|<span data-ttu-id="80ca0-147">Paramètres comptabilité</span><span class="sxs-lookup"><span data-stu-id="80ca0-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="80ca0-148">311</span><span class="sxs-lookup"><span data-stu-id="80ca0-148">311</span></span>|<span data-ttu-id="80ca0-149">Paramètres ventes</span><span class="sxs-lookup"><span data-stu-id="80ca0-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="80ca0-150">312</span><span class="sxs-lookup"><span data-stu-id="80ca0-150">312</span></span>|<span data-ttu-id="80ca0-151">Paramètres achats</span><span class="sxs-lookup"><span data-stu-id="80ca0-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="80ca0-152">313</span><span class="sxs-lookup"><span data-stu-id="80ca0-152">313</span></span>|<span data-ttu-id="80ca0-153">Paramètres stock</span><span class="sxs-lookup"><span data-stu-id="80ca0-153">Inventory Setup</span></span>|  

<span data-ttu-id="80ca0-154">Outre des tables de données de paramétrage, [!INCLUDE[d365fin](includes/d365fin_md.md)] dispose également de tables de données de type paramétrage qui spécifient des informations de base sur la société et ses processus entreprise.</span><span class="sxs-lookup"><span data-stu-id="80ca0-154">In addition to setup data tables, [!INCLUDE[d365fin](includes/d365fin_md.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="80ca0-155">Le tableau suivant répertorie certaines d'entre elles.</span><span class="sxs-lookup"><span data-stu-id="80ca0-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="80ca0-156">N° table</span><span class="sxs-lookup"><span data-stu-id="80ca0-156">Table No.</span></span>|<span data-ttu-id="80ca0-157">Nom de table</span><span class="sxs-lookup"><span data-stu-id="80ca0-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="80ca0-158">3</span><span class="sxs-lookup"><span data-stu-id="80ca0-158">3</span></span>|<span data-ttu-id="80ca0-159">Conditions de paiement</span><span class="sxs-lookup"><span data-stu-id="80ca0-159">Payment Terms</span></span>|  
|<span data-ttu-id="80ca0-160">4</span><span class="sxs-lookup"><span data-stu-id="80ca0-160">4</span></span>|<span data-ttu-id="80ca0-161">Devise</span><span class="sxs-lookup"><span data-stu-id="80ca0-161">Currency</span></span>|  
|<span data-ttu-id="80ca0-162">6</span><span class="sxs-lookup"><span data-stu-id="80ca0-162">6</span></span>|<span data-ttu-id="80ca0-163">Groupes prix client</span><span class="sxs-lookup"><span data-stu-id="80ca0-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="80ca0-164">5700</span><span class="sxs-lookup"><span data-stu-id="80ca0-164">5700</span></span>|<span data-ttu-id="80ca0-165">Point de stock</span><span class="sxs-lookup"><span data-stu-id="80ca0-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="80ca0-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80ca0-166">See Also</span></span>  
[<span data-ttu-id="80ca0-167">Appliquer des configurations aux nouvelles sociétés</span><span class="sxs-lookup"><span data-stu-id="80ca0-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="80ca0-168">Configuration d'une société avec RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="80ca0-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="80ca0-169">Administration</span><span class="sxs-lookup"><span data-stu-id="80ca0-169">Administration</span></span>](admin-setup-and-administration.md)

