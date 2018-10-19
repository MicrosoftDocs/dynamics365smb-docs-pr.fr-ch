---
title: Utilisation de l'extension C5 Data Migration | Microsoft Docs
description: "Utilisez cette extension pour migrer des clients, des fournisseurs, des articles et des comptes généraux de Microsoft Dynamics C5 2012 vers Business Central."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a10c05116e97cdf000bd46258a9d67f4c9910c90
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---

# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="50c1b-103">Extension C5 Data Migration</span><span class="sxs-lookup"><span data-stu-id="50c1b-103">The C5 Data Migration Extension</span></span>
<span data-ttu-id="50c1b-104">Cette extension facilite la migration de clients, de fournisseurs, d'articles et de vos comptes généraux de Microsoft Dynamics C5 2012 vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50c1b-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="50c1b-105">Vous pouvez également migrer des écritures historiques pour des comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="50c1b-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="50c1b-106">La société dans [!INCLUDE[d365fin](includes/d365fin_md.md)] ne doit pas contenir de données.</span><span class="sxs-lookup"><span data-stu-id="50c1b-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="50c1b-107">En outre, après avoir commencé une migration, ne créez pas de clients, de fournisseurs, d'articles, ou de comptes jusqu'à la fin de la migration.</span><span class="sxs-lookup"><span data-stu-id="50c1b-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="50c1b-108">Quelles données sont migrées ?</span><span class="sxs-lookup"><span data-stu-id="50c1b-108">What Data is Migrated?</span></span>
<span data-ttu-id="50c1b-109">Les données suivantes sont migrées pour chaque entité :</span><span class="sxs-lookup"><span data-stu-id="50c1b-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="50c1b-110">**Clients**</span><span class="sxs-lookup"><span data-stu-id="50c1b-110">**Customers**</span></span>
* <span data-ttu-id="50c1b-111">Contacts</span><span class="sxs-lookup"><span data-stu-id="50c1b-111">Contacts</span></span>  
* <span data-ttu-id="50c1b-112">Emplacement</span><span class="sxs-lookup"><span data-stu-id="50c1b-112">Location</span></span>
* <span data-ttu-id="50c1b-113">Pays</span><span class="sxs-lookup"><span data-stu-id="50c1b-113">Country</span></span>
* <span data-ttu-id="50c1b-114">Axes client (service, centre, objectif)</span><span class="sxs-lookup"><span data-stu-id="50c1b-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="50c1b-115">Conditions de livraison</span><span class="sxs-lookup"><span data-stu-id="50c1b-115">Shipment method</span></span>
* <span data-ttu-id="50c1b-116">Vendeur</span><span class="sxs-lookup"><span data-stu-id="50c1b-116">Sales Person</span></span>
* <span data-ttu-id="50c1b-117">Conditions de paiement</span><span class="sxs-lookup"><span data-stu-id="50c1b-117">Payment terms</span></span>
* <span data-ttu-id="50c1b-118">Mode de règlement</span><span class="sxs-lookup"><span data-stu-id="50c1b-118">Payment method</span></span>
* <span data-ttu-id="50c1b-119">Groupe prix client</span><span class="sxs-lookup"><span data-stu-id="50c1b-119">Customer price group</span></span>
* <span data-ttu-id="50c1b-120">Remise facture client</span><span class="sxs-lookup"><span data-stu-id="50c1b-120">Customer invoice discount</span></span>

<span data-ttu-id="50c1b-121">Si vous migrez des comptes, les données suivantes sont également migrées :</span><span class="sxs-lookup"><span data-stu-id="50c1b-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="50c1b-122">Configuration de la validation client</span><span class="sxs-lookup"><span data-stu-id="50c1b-122">Customer posting setup</span></span>
* <span data-ttu-id="50c1b-123">Nom feuille comptabilité</span><span class="sxs-lookup"><span data-stu-id="50c1b-123">General journal batch</span></span>
* <span data-ttu-id="50c1b-124">Transactions ouvertes (écritures comptables client)</span><span class="sxs-lookup"><span data-stu-id="50c1b-124">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="50c1b-125">**Fournisseurs**</span><span class="sxs-lookup"><span data-stu-id="50c1b-125">**Vendors**</span></span>
* <span data-ttu-id="50c1b-126">Contacts</span><span class="sxs-lookup"><span data-stu-id="50c1b-126">Contacts</span></span>
* <span data-ttu-id="50c1b-127">Emplacement</span><span class="sxs-lookup"><span data-stu-id="50c1b-127">Location</span></span>
* <span data-ttu-id="50c1b-128">Pays</span><span class="sxs-lookup"><span data-stu-id="50c1b-128">Country</span></span>
* <span data-ttu-id="50c1b-129">Axes fournisseur (service, centre, objectif)</span><span class="sxs-lookup"><span data-stu-id="50c1b-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="50c1b-130">Remise facture</span><span class="sxs-lookup"><span data-stu-id="50c1b-130">Invoice discount</span></span>
* <span data-ttu-id="50c1b-131">Conditions de livraison</span><span class="sxs-lookup"><span data-stu-id="50c1b-131">Shipment method</span></span>
* <span data-ttu-id="50c1b-132">Acheteur</span><span class="sxs-lookup"><span data-stu-id="50c1b-132">Purchaser</span></span>
* <span data-ttu-id="50c1b-133">Conditions de paiement</span><span class="sxs-lookup"><span data-stu-id="50c1b-133">Payment terms</span></span>
* <span data-ttu-id="50c1b-134">Mode de règlement</span><span class="sxs-lookup"><span data-stu-id="50c1b-134">Payment method</span></span>
* <span data-ttu-id="50c1b-135">Remises facture fournisseur</span><span class="sxs-lookup"><span data-stu-id="50c1b-135">Vendor invoice discount</span></span>

<span data-ttu-id="50c1b-136">Si vous migrez des comptes, les données suivantes sont également migrées :</span><span class="sxs-lookup"><span data-stu-id="50c1b-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="50c1b-137">Configuration de la validation fournisseur</span><span class="sxs-lookup"><span data-stu-id="50c1b-137">Vendor posting setup</span></span>
* <span data-ttu-id="50c1b-138">Nom feuille comptabilité</span><span class="sxs-lookup"><span data-stu-id="50c1b-138">General journal batch</span></span>
* <span data-ttu-id="50c1b-139">Transactions ouvertes (écritures comptables fournisseur)</span><span class="sxs-lookup"><span data-stu-id="50c1b-139">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="50c1b-140">**Articles**</span><span class="sxs-lookup"><span data-stu-id="50c1b-140">**Items**</span></span>
* <span data-ttu-id="50c1b-141">Emplacement</span><span class="sxs-lookup"><span data-stu-id="50c1b-141">Location</span></span>
* <span data-ttu-id="50c1b-142">Pays</span><span class="sxs-lookup"><span data-stu-id="50c1b-142">Country</span></span>
* <span data-ttu-id="50c1b-143">Axes article (service, centre, objectif)</span><span class="sxs-lookup"><span data-stu-id="50c1b-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="50c1b-144">Remises ligne vente</span><span class="sxs-lookup"><span data-stu-id="50c1b-144">Sales line discounts</span></span>
* <span data-ttu-id="50c1b-145">Groupe remises client</span><span class="sxs-lookup"><span data-stu-id="50c1b-145">Customer discount groups</span></span>
* <span data-ttu-id="50c1b-146">Groupes remises article</span><span class="sxs-lookup"><span data-stu-id="50c1b-146">Item discount groups</span></span>
* <span data-ttu-id="50c1b-147">Prix vente</span><span class="sxs-lookup"><span data-stu-id="50c1b-147">Sales price</span></span>
* <span data-ttu-id="50c1b-148">Nomenclature produits</span><span class="sxs-lookup"><span data-stu-id="50c1b-148">Tariff number</span></span>
* <span data-ttu-id="50c1b-149">Unités de mesure</span><span class="sxs-lookup"><span data-stu-id="50c1b-149">Units of measure</span></span>
* <span data-ttu-id="50c1b-150">Code traçabilité</span><span class="sxs-lookup"><span data-stu-id="50c1b-150">Item tracking code</span></span>
* <span data-ttu-id="50c1b-151">Groupe prix client</span><span class="sxs-lookup"><span data-stu-id="50c1b-151">Customer price group</span></span>
* <span data-ttu-id="50c1b-152">Nomenclatures d'élément d'assemblage</span><span class="sxs-lookup"><span data-stu-id="50c1b-152">Assembly BOMs</span></span>

<span data-ttu-id="50c1b-153">Si vous migrez des comptes, les données suivantes sont également migrées :</span><span class="sxs-lookup"><span data-stu-id="50c1b-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="50c1b-154">Configuration de la validation de stock</span><span class="sxs-lookup"><span data-stu-id="50c1b-154">Inventory posting setup</span></span>
* <span data-ttu-id="50c1b-155">Paramètres comptabilisation</span><span class="sxs-lookup"><span data-stu-id="50c1b-155">General posting setup</span></span>
* <span data-ttu-id="50c1b-156">Nom feuille article</span><span class="sxs-lookup"><span data-stu-id="50c1b-156">Item journal batch</span></span>
* <span data-ttu-id="50c1b-157">Transactions ouvertes (écritures comptables article)</span><span class="sxs-lookup"><span data-stu-id="50c1b-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="50c1b-158">S'il existe des transactions ouvertes qui utilisent des devises étrangères, les taux de change pour les devises sont également migrés.</span><span class="sxs-lookup"><span data-stu-id="50c1b-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="50c1b-159">Les autres taux de change ne sont pas migrés.</span><span class="sxs-lookup"><span data-stu-id="50c1b-159">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="50c1b-160">**Plan comptable**</span><span class="sxs-lookup"><span data-stu-id="50c1b-160">**Chart of Accounts**</span></span>  
* <span data-ttu-id="50c1b-161">Dimensions standard : département, centre de coût, objectif</span><span class="sxs-lookup"><span data-stu-id="50c1b-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="50c1b-162">Transactions comptables historiques</span><span class="sxs-lookup"><span data-stu-id="50c1b-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="50c1b-163">Les transactions comptables historiques sont traitées un peu différemment.</span><span class="sxs-lookup"><span data-stu-id="50c1b-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="50c1b-164">Lorsque vous migrez des données, vous définissez un paramètre **Période courante**.</span><span class="sxs-lookup"><span data-stu-id="50c1b-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="50c1b-165">Ce paramètre spécifie comment traiter les transactions comptables.</span><span class="sxs-lookup"><span data-stu-id="50c1b-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="50c1b-166">Les transactions postérieures à cette date sont migrées individuellement.</span><span class="sxs-lookup"><span data-stu-id="50c1b-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="50c1b-167">Les transactions antérieures à cette date sont regroupées par compte et migrées en tant que montant unique.</span><span class="sxs-lookup"><span data-stu-id="50c1b-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="50c1b-168">Par exemple, supposons qu'il existe des transactions en 2015, 2016, 2017, 2018 et que vous spécifiez le 01 janvier 2017 dans le champ Période courante.</span><span class="sxs-lookup"><span data-stu-id="50c1b-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="50c1b-169">Pour chaque compte, les montants des transactions effectuées au plus tard le 31 décembre 2106 sont regroupés sur une ligne feuille comptabilité unique pour chaque compte général.</span><span class="sxs-lookup"><span data-stu-id="50c1b-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="50c1b-170">Toutes les transactions postérieures à cette date sont migrées individuellement.</span><span class="sxs-lookup"><span data-stu-id="50c1b-170">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="50c1b-171">Pour migrer des données</span><span class="sxs-lookup"><span data-stu-id="50c1b-171">To migrate data</span></span>
<span data-ttu-id="50c1b-172">Quelques étapes suffisent pour exporter des données de C5 et les importer dans [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="50c1b-172">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="50c1b-173">Dans C5, utilisez la fonctionnalité **Exporter la base de données** pour exporter les données.</span><span class="sxs-lookup"><span data-stu-id="50c1b-173">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="50c1b-174">Envoyez ensuite le fichier d'exportation vers un fichier compressé (zippé).</span><span class="sxs-lookup"><span data-stu-id="50c1b-174">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="50c1b-175">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Migration des données**, puis sélectionnez **Migration des données**.</span><span class="sxs-lookup"><span data-stu-id="50c1b-175">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="50c1b-176">Exécutez les étapes du guide de configuration assistée.</span><span class="sxs-lookup"><span data-stu-id="50c1b-176">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="50c1b-177">Veillez à choisir **Importer à partir de Microsoft Dynamcis C5 2012** comme source de données.</span><span class="sxs-lookup"><span data-stu-id="50c1b-177">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="50c1b-178">Les sociétés ajoutent souvent des champs pour personnaliser C5 pour leur activité spécifique.</span><span class="sxs-lookup"><span data-stu-id="50c1b-178">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="50c1b-179">n'effectue pas la migration de données à partir des champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="50c1b-179">does not migrate data from custom fields.</span></span> <span data-ttu-id="50c1b-180">En outre, la migration échouera si vous avez plus de 10 champs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="50c1b-180">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="50c1b-181">Affichage du statut de la migration</span><span class="sxs-lookup"><span data-stu-id="50c1b-181">Viewing the Status of the Migration</span></span>
<span data-ttu-id="50c1b-182">Utilisez la fenêtre **Vue d’ensemble de la migration des données** pour contrôler la réussite de la migration.</span><span class="sxs-lookup"><span data-stu-id="50c1b-182">Use the **Data Migration Overview** window to monitor the success of the migration.</span></span> <span data-ttu-id="50c1b-183">La page affiche des informations telles que le nombre d'entités incluses dans la migration, le statut de la migration, ainsi que le nombre d'articles qui ont été migrés et l'état de réussite de leur migration.</span><span class="sxs-lookup"><span data-stu-id="50c1b-183">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="50c1b-184">Elle affiche également le nombre d'erreurs, ce qui vous permet d'étudier ce qui ne s'est pas passé correctement et, si possible, d'accéder facilement à l'entité pour résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="50c1b-184">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="50c1b-185">Pour plus d'informations, voir la section suivante de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="50c1b-185">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="50c1b-186">Pendant que vous attendez les résultats de la migration, vous devez actualiser la page pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="50c1b-186">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="50c1b-187">Comment éviter la double validation</span><span class="sxs-lookup"><span data-stu-id="50c1b-187">How to Avoid Double-Posting</span></span>
<span data-ttu-id="50c1b-188">Pour éviter la double validation en comptabilité, les comptes de contrepartie suivants sont utilisés pour les transactions ouvertes :</span><span class="sxs-lookup"><span data-stu-id="50c1b-188">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="50c1b-189">Pour les fournisseurs, nous utilisons le compte Comptabilité fournisseur dans le groupe comptabilisation fournisseur.</span><span class="sxs-lookup"><span data-stu-id="50c1b-189">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="50c1b-190">Pour les clients, nous utilisons le compte Comptabilité client dans le groupe comptabilisation client.</span><span class="sxs-lookup"><span data-stu-id="50c1b-190">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="50c1b-191">Pour les articles, nous créons un paramètre comptabilisation où le compte ajustement est le compte spécifié comme compte stock dans les paramètres comptabilisation stock.</span><span class="sxs-lookup"><span data-stu-id="50c1b-191">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="50c1b-192">Correction des erreur</span><span class="sxs-lookup"><span data-stu-id="50c1b-192">Correcting Errors</span></span>
<span data-ttu-id="50c1b-193">Si quelque chose se passe mal et qu'une erreur survient, le champ **Statut** affiche **Terminé avec des erreurs**, et le champ **Nombre d'erreurs** en indique le nombre.</span><span class="sxs-lookup"><span data-stu-id="50c1b-193">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="50c1b-194">Pour afficher la liste des erreurs, vous pouvez ouvrir la fenêtre **Erreurs de migration des données** en sélectionnant :</span><span class="sxs-lookup"><span data-stu-id="50c1b-194">To view a list of the errors, you can open the **Data Migration Errors** window by choosing:</span></span>  

* <span data-ttu-id="50c1b-195">le nombre dans le champ **Nombre d'erreurs** pour l'entité.</span><span class="sxs-lookup"><span data-stu-id="50c1b-195">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="50c1b-196">l'entité, puis l'action **Afficher les erreurs**.</span><span class="sxs-lookup"><span data-stu-id="50c1b-196">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="50c1b-197">Dans la fenêtre **Erreurs de migration des données**, pour corriger une erreur vous pouvez sélectionner un message d'erreur, puis **Modifier l'enregistrement** pour afficher les données migrées pour l'entité.</span><span class="sxs-lookup"><span data-stu-id="50c1b-197">In the **Data Migration Errors** window, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="50c1b-198">Si vous avez plusieurs erreurs à résoudre, vous pouvez choisir **Erreurs de correction en bloc** pour modifier les entités dans la liste.</span><span class="sxs-lookup"><span data-stu-id="50c1b-198">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="50c1b-199">Vous devez toujours ouvrir les enregistrements individuellement si l'erreur est due à une écriture associée.</span><span class="sxs-lookup"><span data-stu-id="50c1b-199">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="50c1b-200">Par exemple, un fournisseur ne sera pas migré si une adresse e-mail de l'un de ses contacts a un format non valide.</span><span class="sxs-lookup"><span data-stu-id="50c1b-200">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="50c1b-201">Après avoir corrigé une ou plusieurs erreurs, vous pouvez sélectionner **Migrer** pour migrer uniquement les entités que vous avez corrigées, sans entièrement redémarrer la migration.</span><span class="sxs-lookup"><span data-stu-id="50c1b-201">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="50c1b-202">Si vous avez corrigé plusieurs erreur, vous pouvez utiliser la fonctionnalité **Sélectionner davantage** pour sélectionner plusieurs lignes à migrer.</span><span class="sxs-lookup"><span data-stu-id="50c1b-202">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="50c1b-203">Sinon, s'il existe des erreurs qu'il n'est pas important de corriger, vous pouvez les sélectionner, puis cliquer sur **Ignorer les sélections**.</span><span class="sxs-lookup"><span data-stu-id="50c1b-203">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="50c1b-204">Si vous avez des articles inclus dans une nomenclature, vous pouvez être amené à effectuer la migration plus d'une fois si l'article d'origine n'est pas créé avant les variantes qui y font référence.</span><span class="sxs-lookup"><span data-stu-id="50c1b-204">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="50c1b-205">Si une variante article est créée en premier lieu, la référence à l'article d'origine peut entraîner un message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="50c1b-205">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="50c1b-206">Vérifier les données après avoir effectué une migration</span><span class="sxs-lookup"><span data-stu-id="50c1b-206">Verifying Data After Migrating</span></span>
<span data-ttu-id="50c1b-207">Si vous souhaitez vérifier que vos données ont été migrées correctement, vous pouvez consulter les pages suivantes dans C5 et [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50c1b-207">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="50c1b-208">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="50c1b-208">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="50c1b-209">Traitement par lots à utiliser</span><span class="sxs-lookup"><span data-stu-id="50c1b-209">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="50c1b-210">Écritures client</span><span class="sxs-lookup"><span data-stu-id="50c1b-210">Customer Entries</span></span>| <span data-ttu-id="50c1b-211">Feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="50c1b-211">General Journals</span></span>| <span data-ttu-id="50c1b-212">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="50c1b-212">CUSTMIGR</span></span> |
|<span data-ttu-id="50c1b-213">Écritures fournisseur</span><span class="sxs-lookup"><span data-stu-id="50c1b-213">Vendor Entries</span></span>| <span data-ttu-id="50c1b-214">Feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="50c1b-214">General Journals</span></span>| <span data-ttu-id="50c1b-215">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="50c1b-215">VENDMIGR</span></span>|
|<span data-ttu-id="50c1b-216">Ecritures article</span><span class="sxs-lookup"><span data-stu-id="50c1b-216">Item Entries</span></span>| <span data-ttu-id="50c1b-217">Feuilles article</span><span class="sxs-lookup"><span data-stu-id="50c1b-217">Item Journals</span></span>| <span data-ttu-id="50c1b-218">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="50c1b-218">ITEMMIGR</span></span> |
|<span data-ttu-id="50c1b-219">Écritures comptables</span><span class="sxs-lookup"><span data-stu-id="50c1b-219">G/L Entries</span></span>| <span data-ttu-id="50c1b-220">Feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="50c1b-220">General Journals</span></span>| <span data-ttu-id="50c1b-221">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="50c1b-221">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="50c1b-222">Arrêter la migration des données</span><span class="sxs-lookup"><span data-stu-id="50c1b-222">Stopping Data Migration</span></span>
<span data-ttu-id="50c1b-223">Vous pouvez arrêter de migrer les données en sélectionnant **Arrêter toutes les migrations**.</span><span class="sxs-lookup"><span data-stu-id="50c1b-223">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="50c1b-224">Si vous le faites, toutes les migrations en attente sont également arrêtées.</span><span class="sxs-lookup"><span data-stu-id="50c1b-224">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="50c1b-225">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50c1b-225">See Also</span></span>
<span data-ttu-id="50c1b-226">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="50c1b-226">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="50c1b-227">Mise en route</span><span class="sxs-lookup"><span data-stu-id="50c1b-227">Getting Started</span></span>](product-get-started.md)

