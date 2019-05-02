---
title: Détails de conception - Compta. stock | Microsoft Docs
description: Chaque mouvement stock, par exemple une réception achat ou une expédition vente, valide deux écritures de différents types.
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
ms.openlocfilehash: 80c2912836d8f11a8e3cf869b9412ad9ed66ca54
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821224"
---
# <a name="design-details-inventory-posting"></a><span data-ttu-id="16260-103">Détails de conception : comptabilisation stock</span><span class="sxs-lookup"><span data-stu-id="16260-103">Design Details: Inventory Posting</span></span>
<span data-ttu-id="16260-104">Chaque mouvement stock, par exemple une réception achat ou une expédition vente, valide deux écritures de différents types.</span><span class="sxs-lookup"><span data-stu-id="16260-104">Each inventory transaction, such as a purchase receipt or a sales shipment, posts two entries of different types.</span></span>  

|<span data-ttu-id="16260-105">Type écriture</span><span class="sxs-lookup"><span data-stu-id="16260-105">Entry type</span></span>|<span data-ttu-id="16260-106">Désignation</span><span class="sxs-lookup"><span data-stu-id="16260-106">Description</span></span>|  
|----------------|---------------------------------------|  
|<span data-ttu-id="16260-107">Quantité</span><span class="sxs-lookup"><span data-stu-id="16260-107">Quantity</span></span>|<span data-ttu-id="16260-108">Reflète la modification de la quantité en stock.</span><span class="sxs-lookup"><span data-stu-id="16260-108">Reflects the change of quantity in inventory.</span></span> <span data-ttu-id="16260-109">Ces informations sont stockées dans les écritures comptables article.</span><span class="sxs-lookup"><span data-stu-id="16260-109">This information is stored in item ledger entries.</span></span><br /><br /> <span data-ttu-id="16260-110">Accompagné des écritures lettrage article.</span><span class="sxs-lookup"><span data-stu-id="16260-110">Accompanied by item application entries.</span></span>|  
|<span data-ttu-id="16260-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="16260-111">Value</span></span>|<span data-ttu-id="16260-112">Reflète la modification de la valeur stock.</span><span class="sxs-lookup"><span data-stu-id="16260-112">Reflects the change of inventory value.</span></span> <span data-ttu-id="16260-113">Ces informations sont stockées dans les écritures valeur.</span><span class="sxs-lookup"><span data-stu-id="16260-113">This information is stored in value entries.</span></span><br /><br /> <span data-ttu-id="16260-114">Chaque écriture comptable article ou écriture comptable capacité peut posséder une ou plusieurs écritures valeur.</span><span class="sxs-lookup"><span data-stu-id="16260-114">One or more value entries can exist for each item ledger entry or capacity ledger entry.</span></span><br /><br /> <span data-ttu-id="16260-115">Pour plus d'informations sur les écritures de valeur de capacité liées à l'utilisation des ressources de production ou d'assemblage, reportez\-vous à [Détails de conception : validation d'ordre de fabrication](design-details-production-order-posting.md).</span><span class="sxs-lookup"><span data-stu-id="16260-115">For information about capacity value entries related to the use of production or assembly resources, see [Design Details: Production Order Posting](design-details-production-order-posting.md).</span></span>|  

 <span data-ttu-id="16260-116">En rapport avec les validations de quantité, les écritures lettrage article existent pour lier l'entrée de stock avec la sortie de stock.</span><span class="sxs-lookup"><span data-stu-id="16260-116">In relation to quantity postings, item application entries exist to link inventory increase with inventory decrease.</span></span> <span data-ttu-id="16260-117">Cela permet au moteur d'évaluation de transférer les cous des augmentations aux diminutions liées et vice versa.</span><span class="sxs-lookup"><span data-stu-id="16260-117">This enables the costing engine to forward costs from increases to the related decreases and vice versa.</span></span> <span data-ttu-id="16260-118">Pour plus d'informations, voir [Détails de conception : traçabilité](design-details-item-application.md).</span><span class="sxs-lookup"><span data-stu-id="16260-118">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span>  

 <span data-ttu-id="16260-119">Les écritures comptables article, les écritures valeur, ainsi que les écritures lettrage article sont créées suite à la validation d'une ligne feuille article, soit indirectement lors de la validation d'une ligne commande, soit directement sur la page feuille article.</span><span class="sxs-lookup"><span data-stu-id="16260-119">Item ledger entries, value entries, and item application entries are created as a result of posting an item journal line, either indirectly by posting an order line or directly in the Item Journal page.</span></span>  

 <span data-ttu-id="16260-120">À intervalles réguliers, les écritures valeur créées parmi les écritures comptables d'inventaire sont validées en comptabilité pour rapprocher les deux comptabilités à des fins de contrôle financier.</span><span class="sxs-lookup"><span data-stu-id="16260-120">At regular intervals, value entries that are created in the inventory ledger are posted to the general ledger to reconcile the two ledgers for financial control reasons.</span></span> <span data-ttu-id="16260-121">Pour plus d'informations, voir [Détails de conception : rapprochement de comptabilité](design-details-reconciliation-with-the-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="16260-121">For more information, see [Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md).</span></span>  

 <span data-ttu-id="16260-122">![Flux d'écriture lors du rapprochement du stock avec la comptabilité](media/design_details_inventory_costing_1_entry_flow.png "Flux d'écriture lors du rapprochement du stock avec la comptabilité")</span><span class="sxs-lookup"><span data-stu-id="16260-122">![Entry flow when reconciling inventory with G/L](media/design_details_inventory_costing_1_entry_flow.png "Entry flow when reconciling inventory with G/L")</span></span>  

## <a name="example"></a><span data-ttu-id="16260-123">Exemple :</span><span class="sxs-lookup"><span data-stu-id="16260-123">Example</span></span>  
 <span data-ttu-id="16260-124">L'exemple suivant indique comment les écritures comptables article, les écritures valeur et les écritures lettrage article créent des écritures comptables.</span><span class="sxs-lookup"><span data-stu-id="16260-124">The following example shows how item ledger entries, value entries, and item application entries result in general ledger entries.</span></span>  

 <span data-ttu-id="16260-125">Vous validez une commande achat comme reçue et facturée pour 10 articles avec un coût unitaire direct de 7 LCY et des frais généraux d'1 LCY.</span><span class="sxs-lookup"><span data-stu-id="16260-125">You post a purchase order as received and invoiced for 10 items with a direct unit cost of LCY 7 and an overhead rate of LCY 1.</span></span> <span data-ttu-id="16260-126">La date comptabilisation est 01-01-20.</span><span class="sxs-lookup"><span data-stu-id="16260-126">The posting date is 01-01-20.</span></span> <span data-ttu-id="16260-127">Les écritures suivantes sont créées.</span><span class="sxs-lookup"><span data-stu-id="16260-127">The following entries are created.</span></span>  

 <span data-ttu-id="16260-128">**Écritures comptables article**</span><span class="sxs-lookup"><span data-stu-id="16260-128">**Item Ledger Entries**</span></span>  

|<span data-ttu-id="16260-129">Date comptabilisation</span><span class="sxs-lookup"><span data-stu-id="16260-129">Posting Date</span></span>|<span data-ttu-id="16260-130">Type écriture</span><span class="sxs-lookup"><span data-stu-id="16260-130">Entry Type</span></span>|<span data-ttu-id="16260-131">Coût total (réel)</span><span class="sxs-lookup"><span data-stu-id="16260-131">Cost Amount (Actual)</span></span>|<span data-ttu-id="16260-132">Quantité</span><span class="sxs-lookup"><span data-stu-id="16260-132">Quantity</span></span>|<span data-ttu-id="16260-133">Numéro de la séquence</span><span class="sxs-lookup"><span data-stu-id="16260-133">Entry No.</span></span>|  
|------------------|----------------|----------------------------|--------------|---------------|  
|<span data-ttu-id="16260-134">01/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-134">01-01-20</span></span>|<span data-ttu-id="16260-135">Achats</span><span class="sxs-lookup"><span data-stu-id="16260-135">Purchase</span></span>|<span data-ttu-id="16260-136">80,00</span><span class="sxs-lookup"><span data-stu-id="16260-136">80.00</span></span>|<span data-ttu-id="16260-137">10</span><span class="sxs-lookup"><span data-stu-id="16260-137">10</span></span>|<span data-ttu-id="16260-138">1</span><span class="sxs-lookup"><span data-stu-id="16260-138">1</span></span>|  

 <span data-ttu-id="16260-139">**Ecritures valeur**</span><span class="sxs-lookup"><span data-stu-id="16260-139">**Value Entries**</span></span>  

|<span data-ttu-id="16260-140">Date comptabilisation</span><span class="sxs-lookup"><span data-stu-id="16260-140">Posting Date</span></span>|<span data-ttu-id="16260-141">Type écriture</span><span class="sxs-lookup"><span data-stu-id="16260-141">Entry Type</span></span>|<span data-ttu-id="16260-142">Coût total (réel)</span><span class="sxs-lookup"><span data-stu-id="16260-142">Cost Amount (Actual)</span></span>|<span data-ttu-id="16260-143">N° écriture comptable article</span><span class="sxs-lookup"><span data-stu-id="16260-143">Item Ledger Entry No.</span></span>|<span data-ttu-id="16260-144">Numéro de la séquence</span><span class="sxs-lookup"><span data-stu-id="16260-144">Entry No.</span></span>|  
|------------------|----------------|----------------------------|---------------------------|---------------|  
|<span data-ttu-id="16260-145">01/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-145">01-01-20</span></span>|<span data-ttu-id="16260-146">Coût direct</span><span class="sxs-lookup"><span data-stu-id="16260-146">Direct Cost</span></span>|<span data-ttu-id="16260-147">70,00</span><span class="sxs-lookup"><span data-stu-id="16260-147">70.00</span></span>|<span data-ttu-id="16260-148">1</span><span class="sxs-lookup"><span data-stu-id="16260-148">1</span></span>|<span data-ttu-id="16260-149">1</span><span class="sxs-lookup"><span data-stu-id="16260-149">1</span></span>|  
|<span data-ttu-id="16260-150">01/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-150">01-01-20</span></span>|<span data-ttu-id="16260-151">Coût indirect</span><span class="sxs-lookup"><span data-stu-id="16260-151">Indirect Cost</span></span>|<span data-ttu-id="16260-152">10,00</span><span class="sxs-lookup"><span data-stu-id="16260-152">10.00</span></span>|<span data-ttu-id="16260-153">1</span><span class="sxs-lookup"><span data-stu-id="16260-153">1</span></span>|<span data-ttu-id="16260-154">2</span><span class="sxs-lookup"><span data-stu-id="16260-154">2</span></span>|  

 <span data-ttu-id="16260-155">**Écritures lettrage article**</span><span class="sxs-lookup"><span data-stu-id="16260-155">**Item Application Entries**</span></span>  

|<span data-ttu-id="16260-156">Numéro de la séquence</span><span class="sxs-lookup"><span data-stu-id="16260-156">Entry No.</span></span>|<span data-ttu-id="16260-157">N° écriture comptable article</span><span class="sxs-lookup"><span data-stu-id="16260-157">Item Ledger Entry No.</span></span>|<span data-ttu-id="16260-158">N° écriture article entrant</span><span class="sxs-lookup"><span data-stu-id="16260-158">Inbound Item Entry No.</span></span>|<span data-ttu-id="16260-159">N° écriture article sortant</span><span class="sxs-lookup"><span data-stu-id="16260-159">Outbound Item Entry No.</span></span>|<span data-ttu-id="16260-160">Quantité</span><span class="sxs-lookup"><span data-stu-id="16260-160">Quantity</span></span>|  
|---------------|---------------------------|----------------------------|-----------------------------|--------------|  
|<span data-ttu-id="16260-161">1</span><span class="sxs-lookup"><span data-stu-id="16260-161">1</span></span>|<span data-ttu-id="16260-162">1</span><span class="sxs-lookup"><span data-stu-id="16260-162">1</span></span>|<span data-ttu-id="16260-163">1</span><span class="sxs-lookup"><span data-stu-id="16260-163">1</span></span>|<span data-ttu-id="16260-164">0</span><span class="sxs-lookup"><span data-stu-id="16260-164">0</span></span>|<span data-ttu-id="16260-165">10</span><span class="sxs-lookup"><span data-stu-id="16260-165">10</span></span>|  

 <span data-ttu-id="16260-166">Ensuite, vous validez une vente de 10 unités de l'article avec une date validation de 15/01/20.</span><span class="sxs-lookup"><span data-stu-id="16260-166">Next, you post a sale of 10 units of the item with a posting date of 01-15-20.</span></span>  

 <span data-ttu-id="16260-167">**Écritures comptables article**</span><span class="sxs-lookup"><span data-stu-id="16260-167">**Item Ledger Entries**</span></span>  

|<span data-ttu-id="16260-168">Date comptabilisation</span><span class="sxs-lookup"><span data-stu-id="16260-168">Posting Date</span></span>|<span data-ttu-id="16260-169">Type écriture</span><span class="sxs-lookup"><span data-stu-id="16260-169">Entry Type</span></span>|<span data-ttu-id="16260-170">Coût total (réel)</span><span class="sxs-lookup"><span data-stu-id="16260-170">Cost Amount (Actual)</span></span>||<span data-ttu-id="16260-171">Quantité</span><span class="sxs-lookup"><span data-stu-id="16260-171">Quantity</span></span>|<span data-ttu-id="16260-172">Numéro de la séquence</span><span class="sxs-lookup"><span data-stu-id="16260-172">Entry No.</span></span>|  
|------------------|----------------|----------------------------|-|--------------|---------------|  
|<span data-ttu-id="16260-173">15/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-173">01-15-20</span></span>|<span data-ttu-id="16260-174">Vente</span><span class="sxs-lookup"><span data-stu-id="16260-174">Sale</span></span>|<span data-ttu-id="16260-175">-80,00</span><span class="sxs-lookup"><span data-stu-id="16260-175">-80.00</span></span>||<span data-ttu-id="16260-176">-10</span><span class="sxs-lookup"><span data-stu-id="16260-176">-10</span></span>|<span data-ttu-id="16260-177">2</span><span class="sxs-lookup"><span data-stu-id="16260-177">2</span></span>|  

 <span data-ttu-id="16260-178">**Ecritures valeur**</span><span class="sxs-lookup"><span data-stu-id="16260-178">**Value Entries**</span></span>  

|<span data-ttu-id="16260-179">Date comptabilisation</span><span class="sxs-lookup"><span data-stu-id="16260-179">Posting Date</span></span>|<span data-ttu-id="16260-180">Type écriture</span><span class="sxs-lookup"><span data-stu-id="16260-180">Entry Type</span></span>|<span data-ttu-id="16260-181">Coût total (réel)</span><span class="sxs-lookup"><span data-stu-id="16260-181">Cost Amount (Actual)</span></span>|<span data-ttu-id="16260-182">N° écriture comptable article</span><span class="sxs-lookup"><span data-stu-id="16260-182">Item Ledger Entry No.</span></span>|<span data-ttu-id="16260-183">Numéro de la séquence</span><span class="sxs-lookup"><span data-stu-id="16260-183">Entry No.</span></span>|  
|------------------|----------------|----------------------------|---------------------------|---------------|  
|<span data-ttu-id="16260-184">15/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-184">01-15-20</span></span>|<span data-ttu-id="16260-185">Coût direct</span><span class="sxs-lookup"><span data-stu-id="16260-185">Direct Cost</span></span>|<span data-ttu-id="16260-186">-80,00</span><span class="sxs-lookup"><span data-stu-id="16260-186">-80.00</span></span>|<span data-ttu-id="16260-187">2</span><span class="sxs-lookup"><span data-stu-id="16260-187">2</span></span>|<span data-ttu-id="16260-188">3</span><span class="sxs-lookup"><span data-stu-id="16260-188">3</span></span>|  

 <span data-ttu-id="16260-189">**Écritures lettrage article**</span><span class="sxs-lookup"><span data-stu-id="16260-189">**Item Application Entries**</span></span>  

|<span data-ttu-id="16260-190">Numéro de la séquence</span><span class="sxs-lookup"><span data-stu-id="16260-190">Entry No.</span></span>|<span data-ttu-id="16260-191">N° écriture comptable article</span><span class="sxs-lookup"><span data-stu-id="16260-191">Item Ledger Entry No.</span></span>|<span data-ttu-id="16260-192">N° écriture article entrant</span><span class="sxs-lookup"><span data-stu-id="16260-192">Inbound Item Entry No.</span></span>|<span data-ttu-id="16260-193">N° écriture article sortant</span><span class="sxs-lookup"><span data-stu-id="16260-193">Outbound Item Entry No.</span></span>|<span data-ttu-id="16260-194">Quantité</span><span class="sxs-lookup"><span data-stu-id="16260-194">Quantity</span></span>|  
|---------------|---------------------------|----------------------------|-----------------------------|--------------|  
|<span data-ttu-id="16260-195">2</span><span class="sxs-lookup"><span data-stu-id="16260-195">2</span></span>|<span data-ttu-id="16260-196">2</span><span class="sxs-lookup"><span data-stu-id="16260-196">2</span></span>|<span data-ttu-id="16260-197">1</span><span class="sxs-lookup"><span data-stu-id="16260-197">1</span></span>|<span data-ttu-id="16260-198">2</span><span class="sxs-lookup"><span data-stu-id="16260-198">2</span></span>|<span data-ttu-id="16260-199">-10</span><span class="sxs-lookup"><span data-stu-id="16260-199">-10</span></span>|  

 <span data-ttu-id="16260-200">À la fin de la période comptable, vous exécutez le traitement par lots **Valider coûts ajustés** pour effectuer un rapprochement entre ces mouvements de stock et la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="16260-200">At the end of the accounting period, you run the **Post Inventory Cost to G/L** batch job to reconcile these inventory transactions with the general ledger.</span></span>  

 <span data-ttu-id="16260-201">Pour plus d'informations, voir [Détails de conception : comptes de la comptabilité](design-details-accounts-in-the-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="16260-201">For more information, see [Design Details: Accounts in the General Ledger](design-details-accounts-in-the-general-ledger.md).</span></span>  

 <span data-ttu-id="16260-202">Les tables suivantes indiquent le résultat du rapprochement des mouvements de stock de cet exemple avec la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="16260-202">The following tables show the result of reconciling the inventory transactions in this example with the general ledger.</span></span>  

 <span data-ttu-id="16260-203">**Ecritures valeur**</span><span class="sxs-lookup"><span data-stu-id="16260-203">**Value Entries**</span></span>  

|<span data-ttu-id="16260-204">Date comptabilisation</span><span class="sxs-lookup"><span data-stu-id="16260-204">Posting Date</span></span>|<span data-ttu-id="16260-205">Type écriture</span><span class="sxs-lookup"><span data-stu-id="16260-205">Entry Type</span></span>|<span data-ttu-id="16260-206">Coût total (réel)</span><span class="sxs-lookup"><span data-stu-id="16260-206">Cost Amount (Actual)</span></span>|<span data-ttu-id="16260-207">Coût validé en comptabilité</span><span class="sxs-lookup"><span data-stu-id="16260-207">Cost Posted to G/L</span></span>|<span data-ttu-id="16260-208">N° écriture comptable article</span><span class="sxs-lookup"><span data-stu-id="16260-208">Item Ledger Entry No.</span></span>|<span data-ttu-id="16260-209">Numéro de la séquence</span><span class="sxs-lookup"><span data-stu-id="16260-209">Entry No.</span></span>|  
|------------------|----------------|----------------------------|-------------------------|---------------------------|---------------|  
|<span data-ttu-id="16260-210">01/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-210">01-01-20</span></span>|<span data-ttu-id="16260-211">Coût direct</span><span class="sxs-lookup"><span data-stu-id="16260-211">Direct Cost</span></span>|<span data-ttu-id="16260-212">70,00</span><span class="sxs-lookup"><span data-stu-id="16260-212">70.00</span></span>|<span data-ttu-id="16260-213">70,00</span><span class="sxs-lookup"><span data-stu-id="16260-213">70.00</span></span>|<span data-ttu-id="16260-214">1</span><span class="sxs-lookup"><span data-stu-id="16260-214">1</span></span>|<span data-ttu-id="16260-215">1</span><span class="sxs-lookup"><span data-stu-id="16260-215">1</span></span>|  
|<span data-ttu-id="16260-216">01/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-216">01-01-20</span></span>|<span data-ttu-id="16260-217">Coût indirect</span><span class="sxs-lookup"><span data-stu-id="16260-217">Indirect Cost</span></span>|<span data-ttu-id="16260-218">10,00</span><span class="sxs-lookup"><span data-stu-id="16260-218">10.00</span></span>|<span data-ttu-id="16260-219">10,00</span><span class="sxs-lookup"><span data-stu-id="16260-219">10.00</span></span>|<span data-ttu-id="16260-220">1</span><span class="sxs-lookup"><span data-stu-id="16260-220">1</span></span>|<span data-ttu-id="16260-221">2</span><span class="sxs-lookup"><span data-stu-id="16260-221">2</span></span>|  
|<span data-ttu-id="16260-222">15/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-222">01-15-20</span></span>|<span data-ttu-id="16260-223">Coût direct</span><span class="sxs-lookup"><span data-stu-id="16260-223">Direct Cost</span></span>|<span data-ttu-id="16260-224">-80,00</span><span class="sxs-lookup"><span data-stu-id="16260-224">-80.00</span></span>|<span data-ttu-id="16260-225">-80,00</span><span class="sxs-lookup"><span data-stu-id="16260-225">-80.00</span></span>|<span data-ttu-id="16260-226">2</span><span class="sxs-lookup"><span data-stu-id="16260-226">2</span></span>|<span data-ttu-id="16260-227">3</span><span class="sxs-lookup"><span data-stu-id="16260-227">3</span></span>|  

 <span data-ttu-id="16260-228">**Écritures comptables**</span><span class="sxs-lookup"><span data-stu-id="16260-228">**General Ledger Entries**</span></span>  

|<span data-ttu-id="16260-229">Date comptabilisation</span><span class="sxs-lookup"><span data-stu-id="16260-229">Posting Date</span></span>|<span data-ttu-id="16260-230">Compte général</span><span class="sxs-lookup"><span data-stu-id="16260-230">G/L Account</span></span>|<span data-ttu-id="16260-231">N° compte (démonstration Fr-FR)</span><span class="sxs-lookup"><span data-stu-id="16260-231">Account No. (En-US Demo)</span></span>||<span data-ttu-id="16260-232">Montant</span><span class="sxs-lookup"><span data-stu-id="16260-232">Amount</span></span>|<span data-ttu-id="16260-233">Numéro de la séquence</span><span class="sxs-lookup"><span data-stu-id="16260-233">Entry No.</span></span>|  
|------------------|------------------|---------------------------------|-|------------|---------------|  
|<span data-ttu-id="16260-234">01/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-234">01-01-20</span></span>|<span data-ttu-id="16260-235">[Compte stocks]</span><span class="sxs-lookup"><span data-stu-id="16260-235">[Inventory Account]</span></span>|<span data-ttu-id="16260-236">2 130</span><span class="sxs-lookup"><span data-stu-id="16260-236">2130</span></span>||<span data-ttu-id="16260-237">70,00</span><span class="sxs-lookup"><span data-stu-id="16260-237">70.00</span></span>|<span data-ttu-id="16260-238">1</span><span class="sxs-lookup"><span data-stu-id="16260-238">1</span></span>|  
|<span data-ttu-id="16260-239">01/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-239">01-01-20</span></span>|<span data-ttu-id="16260-240">[Compte coût direct lettré]</span><span class="sxs-lookup"><span data-stu-id="16260-240">[Direct Cost Applied Account]</span></span>|<span data-ttu-id="16260-241">7 291</span><span class="sxs-lookup"><span data-stu-id="16260-241">7291</span></span>||<span data-ttu-id="16260-242">-70,00</span><span class="sxs-lookup"><span data-stu-id="16260-242">-70.00</span></span>|<span data-ttu-id="16260-243">2</span><span class="sxs-lookup"><span data-stu-id="16260-243">2</span></span>|  
|<span data-ttu-id="16260-244">01/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-244">01-01-20</span></span>|<span data-ttu-id="16260-245">[Compte stocks]</span><span class="sxs-lookup"><span data-stu-id="16260-245">[Inventory Account]</span></span>|<span data-ttu-id="16260-246">2 130</span><span class="sxs-lookup"><span data-stu-id="16260-246">2130</span></span>||<span data-ttu-id="16260-247">10,00</span><span class="sxs-lookup"><span data-stu-id="16260-247">10.00</span></span>|<span data-ttu-id="16260-248">3</span><span class="sxs-lookup"><span data-stu-id="16260-248">3</span></span>|  
|<span data-ttu-id="16260-249">01-01-07</span><span class="sxs-lookup"><span data-stu-id="16260-249">01-01-07</span></span>|<span data-ttu-id="16260-250">[Compte frais généraux lettrés]</span><span class="sxs-lookup"><span data-stu-id="16260-250">[Overhead Applied Account]</span></span>|<span data-ttu-id="16260-251">7 292</span><span class="sxs-lookup"><span data-stu-id="16260-251">7292</span></span>||<span data-ttu-id="16260-252">-10,00</span><span class="sxs-lookup"><span data-stu-id="16260-252">-10.00</span></span>|<span data-ttu-id="16260-253">4</span><span class="sxs-lookup"><span data-stu-id="16260-253">4</span></span>|  
|<span data-ttu-id="16260-254">15/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-254">01-15-20</span></span>|<span data-ttu-id="16260-255">[Compte stocks]</span><span class="sxs-lookup"><span data-stu-id="16260-255">[Inventory Account]</span></span>|<span data-ttu-id="16260-256">2 130</span><span class="sxs-lookup"><span data-stu-id="16260-256">2130</span></span>||<span data-ttu-id="16260-257">-80,00</span><span class="sxs-lookup"><span data-stu-id="16260-257">-80.00</span></span>|<span data-ttu-id="16260-258">5</span><span class="sxs-lookup"><span data-stu-id="16260-258">5</span></span>|  
|<span data-ttu-id="16260-259">15/01/20</span><span class="sxs-lookup"><span data-stu-id="16260-259">01-15-20</span></span>|<span data-ttu-id="16260-260">[Compte variation stock]</span><span class="sxs-lookup"><span data-stu-id="16260-260">[COGS Account]</span></span>|<span data-ttu-id="16260-261">7 290</span><span class="sxs-lookup"><span data-stu-id="16260-261">7290</span></span>||<span data-ttu-id="16260-262">80,00</span><span class="sxs-lookup"><span data-stu-id="16260-262">80.00</span></span>|<span data-ttu-id="16260-263">6</span><span class="sxs-lookup"><span data-stu-id="16260-263">6</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="16260-264">La date comptabilisation des écritures comptables est la même que pour les écritures valeur associées.</span><span class="sxs-lookup"><span data-stu-id="16260-264">The posting date of the general ledger entries is the same as for the related value entries.</span></span>  
>   
>  <span data-ttu-id="16260-265">Le champ **Coût validé en comptabilité** de la table **Ecritures valeur** est renseigné.</span><span class="sxs-lookup"><span data-stu-id="16260-265">The **Cost Posted to G/L** field in the **Value Entry** table is filled.</span></span>  

 <span data-ttu-id="16260-266">La relation entre les écritures valeur et les écritures comptables est stockée dans la table **Compta. Relation écritures article**.</span><span class="sxs-lookup"><span data-stu-id="16260-266">The relation between value entries and general ledger entries is stored in the **G/L - Item Ledger Relation** table.</span></span>  

 <span data-ttu-id="16260-267">**Liens écritures dans la comptabilité – Table Écriture comptable article**</span><span class="sxs-lookup"><span data-stu-id="16260-267">**Relation Entries in the G/L – Item Ledger Relation table**</span></span>  

|<span data-ttu-id="16260-268">N° séquence compta.</span><span class="sxs-lookup"><span data-stu-id="16260-268">G/L Entry No.</span></span>|<span data-ttu-id="16260-269">N° écriture valeur</span><span class="sxs-lookup"><span data-stu-id="16260-269">Value Entry No.</span></span>|<span data-ttu-id="16260-270">N° hist. transaction compta.</span><span class="sxs-lookup"><span data-stu-id="16260-270">G/L Register No.</span></span>|  
|--------------------|---------------------|-----------------------|  
|<span data-ttu-id="16260-271">1</span><span class="sxs-lookup"><span data-stu-id="16260-271">1</span></span>|<span data-ttu-id="16260-272">1</span><span class="sxs-lookup"><span data-stu-id="16260-272">1</span></span>|<span data-ttu-id="16260-273">1</span><span class="sxs-lookup"><span data-stu-id="16260-273">1</span></span>|  
|<span data-ttu-id="16260-274">2</span><span class="sxs-lookup"><span data-stu-id="16260-274">2</span></span>|<span data-ttu-id="16260-275">1</span><span class="sxs-lookup"><span data-stu-id="16260-275">1</span></span>|<span data-ttu-id="16260-276">1</span><span class="sxs-lookup"><span data-stu-id="16260-276">1</span></span>|  
|<span data-ttu-id="16260-277">3</span><span class="sxs-lookup"><span data-stu-id="16260-277">3</span></span>|<span data-ttu-id="16260-278">2</span><span class="sxs-lookup"><span data-stu-id="16260-278">2</span></span>|<span data-ttu-id="16260-279">1</span><span class="sxs-lookup"><span data-stu-id="16260-279">1</span></span>|  
|<span data-ttu-id="16260-280">4</span><span class="sxs-lookup"><span data-stu-id="16260-280">4</span></span>|<span data-ttu-id="16260-281">2</span><span class="sxs-lookup"><span data-stu-id="16260-281">2</span></span>|<span data-ttu-id="16260-282">1</span><span class="sxs-lookup"><span data-stu-id="16260-282">1</span></span>|  
|<span data-ttu-id="16260-283">5</span><span class="sxs-lookup"><span data-stu-id="16260-283">5</span></span>|<span data-ttu-id="16260-284">3</span><span class="sxs-lookup"><span data-stu-id="16260-284">3</span></span>|<span data-ttu-id="16260-285">1</span><span class="sxs-lookup"><span data-stu-id="16260-285">1</span></span>|  
|<span data-ttu-id="16260-286">6</span><span class="sxs-lookup"><span data-stu-id="16260-286">6</span></span>|<span data-ttu-id="16260-287">3</span><span class="sxs-lookup"><span data-stu-id="16260-287">3</span></span>|<span data-ttu-id="16260-288">1</span><span class="sxs-lookup"><span data-stu-id="16260-288">1</span></span>|  

## <a name="assembly-and-production-posting"></a><span data-ttu-id="16260-289">Validation d'assemblage et de production</span><span class="sxs-lookup"><span data-stu-id="16260-289">Assembly and Production Posting</span></span>  
<span data-ttu-id="16260-290">Les écritures comptables capacité et ressource représentent le délai qui est validé comme étant consommé dans la production ou l'assemblage.</span><span class="sxs-lookup"><span data-stu-id="16260-290">Capacity and resource ledger entries represent the time that is posted as consumed in production or assembly.</span></span> <span data-ttu-id="16260-291">Ces coûts opératoires sont validés comme écritures valeur en comptabilité en même temps que les coûts matière impliqués dans une structure similaire telle que décrite pour les écritures comptables article de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="16260-291">These process costs are posted as value entries to the general ledger along with the involved material costs in a similar structure as described for item ledger entries in this topic.</span></span>  

<span data-ttu-id="16260-292">Pour plus d'informations, voir [Détails de conception : modes évaluation stock](design-details-assembly-order-posting.md).</span><span class="sxs-lookup"><span data-stu-id="16260-292">For more information, see [Design Details: Assembly Order Posting](design-details-assembly-order-posting.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="16260-293">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16260-293">See Also</span></span>  
 <span data-ttu-id="16260-294">[Détails de conception : évaluation stock](design-details-inventory-costing.md) </span><span class="sxs-lookup"><span data-stu-id="16260-294">[Design Details: Inventory Costing](design-details-inventory-costing.md) </span></span>  
 <span data-ttu-id="16260-295">[Détails de conception : comptes de la comptabilité](design-details-accounts-in-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="16260-295">[Design Details: Accounts in the General Ledger](design-details-accounts-in-the-general-ledger.md) </span></span>  
 <span data-ttu-id="16260-296">[Détails de conception : Ajustement des coûts](design-details-cost-components.md) [Gestion des composants des coûts](finance-manage-inventory-costs.md)</span><span class="sxs-lookup"><span data-stu-id="16260-296">[Design Details: Cost Components](design-details-cost-components.md) [Managing Inventory Costs](finance-manage-inventory-costs.md)</span></span>  
 [<span data-ttu-id="16260-297">Finances</span><span class="sxs-lookup"><span data-stu-id="16260-297">Finance</span></span>](finance.md)  
 <span data-ttu-id="16260-298">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="16260-298">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>