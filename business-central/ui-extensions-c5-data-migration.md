---
title: Utilisation de l'extension C5 Data Migration | Microsoft Docs
description: "Utilisez cette extension pour migrer des clients, des fournisseurs, des articles et des comptes généraux de Microsoft Dynamics C5 2012 vers Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 7fe6393ad43dbad032512b2d6d45cc8ee0392236
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="e4711-103">Extension C5 Data Migration pour Business Central</span><span class="sxs-lookup"><span data-stu-id="e4711-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="e4711-104">Cette extension facilite la migration de clients, de fournisseurs, d'articles et de vos comptes généraux de Microsoft Dynamics C5 2012 vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e4711-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e4711-105">Vous pouvez également migrer des écritures historiques pour des comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="e4711-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="e4711-106">La société dans [!INCLUDE[d365fin](includes/d365fin_md.md)] ne doit pas contenir de données.</span><span class="sxs-lookup"><span data-stu-id="e4711-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="e4711-107">En outre, après avoir commencé une migration, ne créez pas de clients, de fournisseurs, d'articles, ou de comptes jusqu'à la fin de la migration.</span><span class="sxs-lookup"><span data-stu-id="e4711-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

##<a name="what-data-is-migrated"></a><span data-ttu-id="e4711-108">Quelles données sont migrées ?</span><span class="sxs-lookup"><span data-stu-id="e4711-108">What Data is Migrated?</span></span>
<span data-ttu-id="e4711-109">Les données suivantes sont migrées pour chaque entité :</span><span class="sxs-lookup"><span data-stu-id="e4711-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="e4711-110">**Clients**</span><span class="sxs-lookup"><span data-stu-id="e4711-110">**Customers**</span></span>
* <span data-ttu-id="e4711-111">Emplacement</span><span class="sxs-lookup"><span data-stu-id="e4711-111">Location</span></span>
* <span data-ttu-id="e4711-112">Pays</span><span class="sxs-lookup"><span data-stu-id="e4711-112">Country</span></span>
* <span data-ttu-id="e4711-113">Axes client (service, centre, objectif)</span><span class="sxs-lookup"><span data-stu-id="e4711-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="e4711-114">Conditions de livraison</span><span class="sxs-lookup"><span data-stu-id="e4711-114">Shipment method</span></span>
* <span data-ttu-id="e4711-115">Vendeur</span><span class="sxs-lookup"><span data-stu-id="e4711-115">Sales Person</span></span>
* <span data-ttu-id="e4711-116">Conditions de paiement</span><span class="sxs-lookup"><span data-stu-id="e4711-116">Payment terms</span></span>
* <span data-ttu-id="e4711-117">Mode de règlement</span><span class="sxs-lookup"><span data-stu-id="e4711-117">Payment method</span></span>
* <span data-ttu-id="e4711-118">Groupe prix client</span><span class="sxs-lookup"><span data-stu-id="e4711-118">Customer price group</span></span>
* <span data-ttu-id="e4711-119">Remise facture client</span><span class="sxs-lookup"><span data-stu-id="e4711-119">Customer invoice discount</span></span>

<span data-ttu-id="e4711-120">Si vous migrez des comptes, les données suivantes sont également migrées :</span><span class="sxs-lookup"><span data-stu-id="e4711-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="e4711-121">Configuration de la validation client</span><span class="sxs-lookup"><span data-stu-id="e4711-121">Customer posting setup</span></span>
* <span data-ttu-id="e4711-122">Nom feuille comptabilité</span><span class="sxs-lookup"><span data-stu-id="e4711-122">General journal batch</span></span>
* <span data-ttu-id="e4711-123">Transactions ouvertes (écritures comptables client)</span><span class="sxs-lookup"><span data-stu-id="e4711-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="e4711-124">**Fournisseurs**</span><span class="sxs-lookup"><span data-stu-id="e4711-124">**Vendors**</span></span>
* <span data-ttu-id="e4711-125">Emplacement</span><span class="sxs-lookup"><span data-stu-id="e4711-125">Location</span></span>
* <span data-ttu-id="e4711-126">Pays</span><span class="sxs-lookup"><span data-stu-id="e4711-126">Country</span></span>
* <span data-ttu-id="e4711-127">Axes fournisseur (service, centre, objectif)</span><span class="sxs-lookup"><span data-stu-id="e4711-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="e4711-128">Remise facture</span><span class="sxs-lookup"><span data-stu-id="e4711-128">Invoice discount</span></span>
* <span data-ttu-id="e4711-129">Conditions de livraison</span><span class="sxs-lookup"><span data-stu-id="e4711-129">Shipment method</span></span>
* <span data-ttu-id="e4711-130">Acheteur</span><span class="sxs-lookup"><span data-stu-id="e4711-130">Purchaser</span></span>
* <span data-ttu-id="e4711-131">Conditions de paiement</span><span class="sxs-lookup"><span data-stu-id="e4711-131">Payment terms</span></span>
* <span data-ttu-id="e4711-132">Mode de règlement</span><span class="sxs-lookup"><span data-stu-id="e4711-132">Payment method</span></span>
* <span data-ttu-id="e4711-133">Remises facture fournisseur</span><span class="sxs-lookup"><span data-stu-id="e4711-133">Vendor invoice discount</span></span>

<span data-ttu-id="e4711-134">Si vous migrez des comptes, les données suivantes sont également migrées :</span><span class="sxs-lookup"><span data-stu-id="e4711-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="e4711-135">Configuration de la validation fournisseur</span><span class="sxs-lookup"><span data-stu-id="e4711-135">Vendor posting setup</span></span>
* <span data-ttu-id="e4711-136">Nom feuille comptabilité</span><span class="sxs-lookup"><span data-stu-id="e4711-136">General journal batch</span></span>
* <span data-ttu-id="e4711-137">Transactions ouvertes (écritures comptables fournisseur)</span><span class="sxs-lookup"><span data-stu-id="e4711-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="e4711-138">**Articles**</span><span class="sxs-lookup"><span data-stu-id="e4711-138">**Items**</span></span>
* <span data-ttu-id="e4711-139">Emplacement</span><span class="sxs-lookup"><span data-stu-id="e4711-139">Location</span></span>
* <span data-ttu-id="e4711-140">Pays</span><span class="sxs-lookup"><span data-stu-id="e4711-140">Country</span></span>
* <span data-ttu-id="e4711-141">Axes article (service, centre, objectif)</span><span class="sxs-lookup"><span data-stu-id="e4711-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="e4711-142">Remises ligne vente</span><span class="sxs-lookup"><span data-stu-id="e4711-142">Sales line discounts</span></span>
* <span data-ttu-id="e4711-143">Groupe remises client</span><span class="sxs-lookup"><span data-stu-id="e4711-143">Customer discount groups</span></span>
* <span data-ttu-id="e4711-144">Groupes remises article</span><span class="sxs-lookup"><span data-stu-id="e4711-144">Item discount groups</span></span>
* <span data-ttu-id="e4711-145">Prix vente</span><span class="sxs-lookup"><span data-stu-id="e4711-145">Sales price</span></span>
* <span data-ttu-id="e4711-146">Nomenclature produits</span><span class="sxs-lookup"><span data-stu-id="e4711-146">Tariff number</span></span>
* <span data-ttu-id="e4711-147">Unités de mesure</span><span class="sxs-lookup"><span data-stu-id="e4711-147">Units of measure</span></span>
* <span data-ttu-id="e4711-148">Code traçabilité</span><span class="sxs-lookup"><span data-stu-id="e4711-148">Item tracking code</span></span>
* <span data-ttu-id="e4711-149">Groupe prix client</span><span class="sxs-lookup"><span data-stu-id="e4711-149">Customer price group</span></span>

<span data-ttu-id="e4711-150">Si vous migrez des comptes, les données suivantes sont également migrées :</span><span class="sxs-lookup"><span data-stu-id="e4711-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="e4711-151">Configuration de la validation de stock</span><span class="sxs-lookup"><span data-stu-id="e4711-151">Inventory posting setup</span></span>
* <span data-ttu-id="e4711-152">Paramètres comptabilisation</span><span class="sxs-lookup"><span data-stu-id="e4711-152">General posting setup</span></span>
* <span data-ttu-id="e4711-153">Nom feuille article</span><span class="sxs-lookup"><span data-stu-id="e4711-153">Item journal batch</span></span>
* <span data-ttu-id="e4711-154">Transactions ouvertes (écritures comptables article)</span><span class="sxs-lookup"><span data-stu-id="e4711-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="e4711-155">S'il existe des transactions ouvertes qui utilisent des devises étrangères, les taux de change pour les devises sont également migrés.</span><span class="sxs-lookup"><span data-stu-id="e4711-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="e4711-156">Les autres taux de change ne sont pas migrés.</span><span class="sxs-lookup"><span data-stu-id="e4711-156">Other exchange rates are not migrated.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="e4711-157">Pour migrer des données</span><span class="sxs-lookup"><span data-stu-id="e4711-157">To migrate data</span></span>
<span data-ttu-id="e4711-158">Quelques étapes suffisent pour exporter des données de C5 et les importer dans [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="e4711-158">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="e4711-159">Dans C5, utilisez la fonctionnalité **Exporter la base de données** pour exporter les données.</span><span class="sxs-lookup"><span data-stu-id="e4711-159">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="e4711-160">Envoyez ensuite le fichier d'exportation vers un fichier compressé (zippé).</span><span class="sxs-lookup"><span data-stu-id="e4711-160">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="e4711-161">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), saisissez **Migration de données**, puis sélectionnez **Migration de données**.</span><span class="sxs-lookup"><span data-stu-id="e4711-161">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="e4711-162">Exécutez les étapes du guide de configuration assistée.</span><span class="sxs-lookup"><span data-stu-id="e4711-162">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="e4711-163">Veillez à choisir **Importer à partir de Microsoft Dynamcis C5 2012** comme source de données.</span><span class="sxs-lookup"><span data-stu-id="e4711-163">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="e4711-164">Les sociétés ajoutent souvent des champs pour personnaliser C5 pour leur activité spécifique.</span><span class="sxs-lookup"><span data-stu-id="e4711-164">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="e4711-165"> n'effectue pas la migration de données à partir des champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="e4711-165"> does not migrate data from custom fields.</span></span> <span data-ttu-id="e4711-166">En outre, la migration échouera si vous avez plus de 10 champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="e4711-166">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="e4711-167">Affichage du statut de la migration</span><span class="sxs-lookup"><span data-stu-id="e4711-167">Viewing the Status of the Migration</span></span>
<span data-ttu-id="e4711-168">Utilisez la page **Vue d’ensemble de la migration des données** pour contrôler la réussite de la migration.</span><span class="sxs-lookup"><span data-stu-id="e4711-168">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="e4711-169">La page affiche des informations telles que le nombre d'entités incluses dans la migration, le statut de la migration, ainsi que le nombre d'articles qui ont été migrés et l'état de réussite de leur migration.</span><span class="sxs-lookup"><span data-stu-id="e4711-169">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="e4711-170">Elle affiche également le nombre d'erreurs, ce qui vous permet d'étudier ce qui ne s'est pas passé correctement et, si possible, d'accéder facilement à l'entité pour résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="e4711-170">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="e4711-171">Pour plus d'informations, voir la section suivante de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e4711-171">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="e4711-172">Pendant que vous attendez les résultats de la migration, vous devez actualiser la page pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="e4711-172">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="e4711-173">Correction des erreur</span><span class="sxs-lookup"><span data-stu-id="e4711-173">Correcting Errors</span></span>
<span data-ttu-id="e4711-174">Si quelque chose se passe mal et qu'une erreur survient, le champ **Statut** affiche **Terminé avec des erreurs**, et le champ **Nombre d'erreurs** en indique le nombre.</span><span class="sxs-lookup"><span data-stu-id="e4711-174">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="e4711-175">Pour afficher la liste des erreurs, vous pouvez ouvrir la page **Erreurs de migration des données** en sélectionnant :</span><span class="sxs-lookup"><span data-stu-id="e4711-175">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="e4711-176">le nombre dans le champ **Nombre d'erreurs** pour l'entité.</span><span class="sxs-lookup"><span data-stu-id="e4711-176">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="e4711-177">l'entité, puis l'action **Afficher les erreurs**.</span><span class="sxs-lookup"><span data-stu-id="e4711-177">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="e4711-178">Dans la page **Erreurs de migration des données**, pour corriger une erreur vous pouvez sélectionner un message d'erreur, puis **Modifier l'enregistrement** pour ouvrir une page qui affiche les données migrées pour l'entité.</span><span class="sxs-lookup"><span data-stu-id="e4711-178">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="e4711-179">Après avoir corrigé une ou plusieurs erreurs, vous pouvez sélectionner **Migrer** pour migrer uniquement les entités que vous avez corrigées, sans entièrement redémarrer la migration.</span><span class="sxs-lookup"><span data-stu-id="e4711-179">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="e4711-180">Si vous avez corrigé plusieurs erreur, vous pouvez utiliser la fonctionnalité **Sélectionner davantage** pour sélectionner plusieurs lignes à migrer.</span><span class="sxs-lookup"><span data-stu-id="e4711-180">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="e4711-181">Sinon, s'il existe des erreurs qu'il n'est pas important de corriger, vous pouvez les sélectionner, puis cliquer sur **Ignorer les sélections**.</span><span class="sxs-lookup"><span data-stu-id="e4711-181">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="e4711-182">Si vous avez des articles inclus dans une nomenclature, vous pouvez être amené à effectuer la migration plus d'une fois si l'article d'origine n'est pas créé avant les variantes qui y font référence.</span><span class="sxs-lookup"><span data-stu-id="e4711-182">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="e4711-183">Si une variante article est créée en premier lieu, la référence à l'article d'origine peut entraîner un message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="e4711-183">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="e4711-184">Vérifier les données après avoir effectué une migration</span><span class="sxs-lookup"><span data-stu-id="e4711-184">Verifying Data After Migrating</span></span>
<span data-ttu-id="e4711-185">Si vous souhaitez vérifier que vos données ont été migrées correctement, vous pouvez consulter les pages suivantes dans C5 et [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e4711-185">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="e4711-186">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="e4711-186">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="e4711-187">Écritures client</span><span class="sxs-lookup"><span data-stu-id="e4711-187">Customer Entries</span></span>| <span data-ttu-id="e4711-188">Feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="e4711-188">General Journals</span></span>|
|<span data-ttu-id="e4711-189">Écritures fournisseur</span><span class="sxs-lookup"><span data-stu-id="e4711-189">Vendor Entries</span></span>| <span data-ttu-id="e4711-190">Feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="e4711-190">General Journals</span></span>|
|<span data-ttu-id="e4711-191">Ecritures article</span><span class="sxs-lookup"><span data-stu-id="e4711-191">Item Entries</span></span>| <span data-ttu-id="e4711-192">Feuilles article</span><span class="sxs-lookup"><span data-stu-id="e4711-192">Item Journals</span></span>|

<span data-ttu-id="e4711-193">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], le lot des données migrées est nommé **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="e4711-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span>

## <a name="stopping-data-migration"></a><span data-ttu-id="e4711-194">Arrêter la migration des données</span><span class="sxs-lookup"><span data-stu-id="e4711-194">Stopping Data Migration</span></span>
<span data-ttu-id="e4711-195">Vous pouvez arrêter de migrer les données en sélectionnant **Arrêter toutes les migrations**.</span><span class="sxs-lookup"><span data-stu-id="e4711-195">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="e4711-196">Si vous le faites, toutes les migrations en attente sont également arrêtées.</span><span class="sxs-lookup"><span data-stu-id="e4711-196">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4711-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4711-197">See Also</span></span>
<span data-ttu-id="e4711-198">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e4711-198">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="e4711-199">Mise en route</span><span class="sxs-lookup"><span data-stu-id="e4711-199">Getting Started</span></span>](product-get-started.md) 

