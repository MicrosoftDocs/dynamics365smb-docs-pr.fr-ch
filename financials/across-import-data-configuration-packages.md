---
title: "Utilisez Excel pour importer des données dans Financials| Microsoft Docs"
description: "Utilisez le package de configuration par défaut pour ajouter des données client dans Excel et les importer ensuite dans Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 591d8100100ee717a932d188a87545fe4098a001
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="94214-103">Importation des données à partir du logiciel de comptabilité hérité à l'aide d'un package de configuration</span><span class="sxs-lookup"><span data-stu-id="94214-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="94214-104">Vous pouvez importer des données de base et des données transactionnelles à partir d'autres systèmes financiers basés sur le package de configuration par défaut dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="94214-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="94214-105">Dans la fenêtre **Packages configuration**, vous pouvez utiliser le package pour importer et valider les données avant d'appliquer le package.</span><span class="sxs-lookup"><span data-stu-id="94214-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!NOTE]  
> <span data-ttu-id="94214-106">Les packages de configuration font partie de RapidStart Services pour [!INCLUDE[d365fin](includes/d365fin_md.md)], une boîte à outils étendue de configuration de nouvelles solutions basées sur les besoins métier et les données de configuration des clients.</span><span class="sxs-lookup"><span data-stu-id="94214-106">Configuration packages are part of RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="94214-107">RapidStart Services offre également une fonctionnalité d'importation des données héritées.</span><span class="sxs-lookup"><span data-stu-id="94214-107">RapidStart Services also offers functionality for import of legacy data.</span></span> <span data-ttu-id="94214-108">Pour plus d'informations, voir [Configuration d'une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="94214-108">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

> [!TIP]  
>   <span data-ttu-id="94214-109">Sinon, utilisez l'assistant de migration de données pour importer des données de QuickBooks ou de Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="94214-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="94214-110">Pour plus d'informations, voir [Migration de données QuickBooks](ui-extensions-quickbooks-data-migration.md) ou [Migration de données Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="94214-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="94214-111">Utilisation de données dans Excel</span><span class="sxs-lookup"><span data-stu-id="94214-111">Working with Data in Excel</span></span>
<span data-ttu-id="94214-112">Lorsque vous exportez le package de configuration par défaut dans Excel, le classeur généré contient une feuille de calcul pour chaque table du package.</span><span class="sxs-lookup"><span data-stu-id="94214-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="94214-113">Pour simplifier vos tâches, vous pouvez mettre à profit les outils de gestion XML qui sont intégrés à Excel.</span><span class="sxs-lookup"><span data-stu-id="94214-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="94214-114">Vous pouvez également utiliser les fonctions intégrées d'Excel pour procéder au formatage des données et placer des données dans la cellule qui convient.</span><span class="sxs-lookup"><span data-stu-id="94214-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="94214-115">Ajoutez par exemple une feuille vide et copiez-y les données héritées.</span><span class="sxs-lookup"><span data-stu-id="94214-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="94214-116">Ensuite, créez une formule Excel permettant d'associer les données de la feuille de calcul de transformation entre les champs de la feuille de calcul exportée et les données héritées du client.</span><span class="sxs-lookup"><span data-stu-id="94214-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="94214-117">Après avoir associé toutes les données, copiez la plage de données dans la feuille de calcul de la table.</span><span class="sxs-lookup"><span data-stu-id="94214-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="94214-118">Ne modifiez pas les colonnes dans les feuilles de calcul.</span><span class="sxs-lookup"><span data-stu-id="94214-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="94214-119">Si elles sont déplacées, modifiées ou supprimées, la feuille de calcul ne peut pas être importée dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="94214-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="94214-120">Tables dans le package de configuration par défaut</span><span class="sxs-lookup"><span data-stu-id="94214-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="94214-121">Le package de configuration par défaut prend en charge les tables suivantes :</span><span class="sxs-lookup"><span data-stu-id="94214-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="94214-122">Conditions de paiement</span><span class="sxs-lookup"><span data-stu-id="94214-122">Payment Terms</span></span>
-   <span data-ttu-id="94214-123">Groupe prix client</span><span class="sxs-lookup"><span data-stu-id="94214-123">Customer Price Group</span></span>
-   <span data-ttu-id="94214-124">Conditions de livraison</span><span class="sxs-lookup"><span data-stu-id="94214-124">Shipment Method</span></span>
-   <span data-ttu-id="94214-125">Vendeur/Acheteur</span><span class="sxs-lookup"><span data-stu-id="94214-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="94214-126">Emplacement</span><span class="sxs-lookup"><span data-stu-id="94214-126">Location</span></span>
-   <span data-ttu-id="94214-127">Compte général</span><span class="sxs-lookup"><span data-stu-id="94214-127">GL Account</span></span>
-   <span data-ttu-id="94214-128">Client</span><span class="sxs-lookup"><span data-stu-id="94214-128">Customer</span></span>
-   <span data-ttu-id="94214-129">Fournisseur</span><span class="sxs-lookup"><span data-stu-id="94214-129">Vendor</span></span>
-   <span data-ttu-id="94214-130">Article</span><span class="sxs-lookup"><span data-stu-id="94214-130">Item</span></span>
-   <span data-ttu-id="94214-131">En-tête vente</span><span class="sxs-lookup"><span data-stu-id="94214-131">Sales Header</span></span>
-   <span data-ttu-id="94214-132">Ligne vente</span><span class="sxs-lookup"><span data-stu-id="94214-132">Sales Line</span></span>
-   <span data-ttu-id="94214-133">En-tête achat</span><span class="sxs-lookup"><span data-stu-id="94214-133">Purchase Header</span></span>
-   <span data-ttu-id="94214-134">Ligne achat</span><span class="sxs-lookup"><span data-stu-id="94214-134">Purchase Line</span></span>
-   <span data-ttu-id="94214-135">Ligne feuille comptabilité</span><span class="sxs-lookup"><span data-stu-id="94214-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="94214-136">Ligne feuille article</span><span class="sxs-lookup"><span data-stu-id="94214-136">Item Journal Line</span></span>
-   <span data-ttu-id="94214-137">Groupe compta. client</span><span class="sxs-lookup"><span data-stu-id="94214-137">Customer Posting Group</span></span>
-   <span data-ttu-id="94214-138">Groupe compta. fournisseur</span><span class="sxs-lookup"><span data-stu-id="94214-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="94214-139">Groupe compta. stock</span><span class="sxs-lookup"><span data-stu-id="94214-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="94214-140">Unité</span><span class="sxs-lookup"><span data-stu-id="94214-140">Unit of Measure</span></span>
-   <span data-ttu-id="94214-141">Groupe compta. marché</span><span class="sxs-lookup"><span data-stu-id="94214-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="94214-142">Groupe compta. produit</span><span class="sxs-lookup"><span data-stu-id="94214-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="94214-143">Paramètres comptabilisation</span><span class="sxs-lookup"><span data-stu-id="94214-143">General Posting Setup</span></span>
-   <span data-ttu-id="94214-144">Secteur</span><span class="sxs-lookup"><span data-stu-id="94214-144">Territory</span></span>
-   <span data-ttu-id="94214-145">Catégorie article</span><span class="sxs-lookup"><span data-stu-id="94214-145">Item Category</span></span>
-   <span data-ttu-id="94214-146">Prix vente</span><span class="sxs-lookup"><span data-stu-id="94214-146">Sales Price</span></span>
-   <span data-ttu-id="94214-147">Prix achat</span><span class="sxs-lookup"><span data-stu-id="94214-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="94214-148">Importation de données client</span><span class="sxs-lookup"><span data-stu-id="94214-148">Importing Customer Data</span></span>
<span data-ttu-id="94214-149">Une fois les données client entrées dans Excel, vous devez les importer dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="94214-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="94214-150">Dans la fenêtre **Packages configuration**, vous devez importer les données à partir du fichier Excel et vous pouvez vérifier leur cohérence avec [!INCLUDE[d365fin](includes/d365fin_md.md)] avant d'appliquer le package.</span><span class="sxs-lookup"><span data-stu-id="94214-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="94214-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94214-151">See Also</span></span>
[<span data-ttu-id="94214-152">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="94214-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="94214-153">Configuration d'une société avec RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="94214-153">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="94214-154">Extension QuickBooks Data Migration</span><span class="sxs-lookup"><span data-stu-id="94214-154">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="94214-155">Extension Dynamics GP Data Migration</span><span class="sxs-lookup"><span data-stu-id="94214-155">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

