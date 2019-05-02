---
title: Détails de conception - Vue d'ensemble d'entrepôt | Microsoft Docs
description: Pour prendre en charge la manipulation physique des articles au niveau des zones et emplacements, toutes les informations doivent être suivies pour chaque transaction ou mouvement dans l'entrepôt. Ceci est géré dans la table **Écriture entrepôt**. Chaque transaction est enregistrée dans un historique des transactions entrepôt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/19/2018
ms.author: sgroespe
ms.openlocfilehash: 2d1fc180b971a7a0003847ea6b5830cc124cf5c7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821324"
---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="84586-105">Détails de conception : vue d'ensemble d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="84586-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="84586-106">Pour prendre en charge la manipulation physique des articles au niveau des zones et emplacements, toutes les informations doivent être suivies pour chaque transaction ou mouvement dans l'entrepôt.</span><span class="sxs-lookup"><span data-stu-id="84586-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="84586-107">Ceci est géré dans la table **Écriture entrepôt**.</span><span class="sxs-lookup"><span data-stu-id="84586-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="84586-108">Chaque transaction est enregistrée dans un historique des transactions entrepôt.</span><span class="sxs-lookup"><span data-stu-id="84586-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="84586-109">Les documents d'entrepôt et une feuille entrepôt sont utilisés pour enregistrer des mouvements article dans l'entrepôt.</span><span class="sxs-lookup"><span data-stu-id="84586-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="84586-110">Chaque fois qu'un article dans l'entrepôt est déplacé, accepté, rangé, prélevé, livré ou ajusté, les écritures entrepôt sont enregistrées pour stocker les informations physiques sur la zone, l'emplacement et la quantité.</span><span class="sxs-lookup"><span data-stu-id="84586-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span>

<span data-ttu-id="84586-111">La table **Contenu emplacement** est utilisée pour gérer l'ensemble des axes analytiques du contenu d'un emplacement par article, par exemple, l'unité de mesure, la quantité maximum et la quantité minimum.</span><span class="sxs-lookup"><span data-stu-id="84586-111">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="84586-112">La table **Contenu emplacement** affiche également des champs de flux vers les écritures entrepôt, des instruction entrepôt et des lignes feuille entrepôt, ce qui garantit que la disponibilité d'un article par emplacement et d'un emplacement pour un article peut être calculée rapidement.</span><span class="sxs-lookup"><span data-stu-id="84586-112">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="84586-113">Pour plus d'informations, voir [Détails de conception : disponibilité dans l'entrepôt](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="84586-113">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="84586-114">Lorsque les validations article se produisent en dehors du module d'entrepôt, un emplacement d'ajustement par défaut par magasin est utilisé pour synchroniser des écritures d'entrepôt avec les écritures de stock.</span><span class="sxs-lookup"><span data-stu-id="84586-114">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="84586-115">Au cours de l'inventaire de l'entrepôt, toutes les différences entre les quantités calculées et les quantités comptées sont enregistrées dans l'emplacement ajustement puis validées comme écritures comptables articles de correction.</span><span class="sxs-lookup"><span data-stu-id="84586-115">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="84586-116">Pour plus d'informations, voir [Détails de conception : intégration avec le stock](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="84586-116">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="84586-117">La figure suivante présente les flux d'entrepôt courants.</span><span class="sxs-lookup"><span data-stu-id="84586-117">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="84586-118">![Vue d'ensemble des processus entrepôt](media/design_details_warehouse_management_overview.png "Vue d'ensemble des processus entrepôt")</span><span class="sxs-lookup"><span data-stu-id="84586-118">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "Overview of warehouse processes")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="84586-119">Entreposage de base ou avancé</span><span class="sxs-lookup"><span data-stu-id="84586-119">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="84586-120">La fonctionnalité d'entrepôt dans [!INCLUDE[d365fin](includes/d365fin_md.md)] peut être implémentée dans différents niveaux de complexité, selon les processus d'une société et le volume de commande.</span><span class="sxs-lookup"><span data-stu-id="84586-120">Warehouse functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="84586-121">La principale différence est que les activités sont effectuées par commande dans l'entreposage de base, alors qu'elles sont regroupées pour plusieurs commandes dans l'entreposage avancé.</span><span class="sxs-lookup"><span data-stu-id="84586-121">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="84586-122">Pour différencier les différents niveaux de complexité, ces documents font référence à deux dénominations générales de base, Basic et Advanced Warehousing.</span><span class="sxs-lookup"><span data-stu-id="84586-122">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="84586-123">Cette différenciation unique couvre plusieurs niveaux de complexité tels que définis par les granules produit et la configuration du magasin, chacun étant pris en charge par différents documents d'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="84586-123">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="84586-124">Pour plus d'informations, reportez\-vous à [Détails de conception : Paramètres entrepôt](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="84586-124">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="84586-125">Le niveau le plus avancé de l'entreposage est appelé « Installations WMS » dans cette documentation, étant donné que ce niveau requiert le granule le plus avancé, Warehouse Management Systems (systèmes de gestion d'entrepôt).</span><span class="sxs-lookup"><span data-stu-id="84586-125">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="84586-126">Les différents documents de l'interface utilisateur suivants sont utilisés dans l'entreposage de base et avancé.</span><span class="sxs-lookup"><span data-stu-id="84586-126">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="84586-127">Documents de base de l'interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="84586-127">Basic UI Documents</span></span>  

-   <span data-ttu-id="84586-128">**Rangmt stk invent**</span><span class="sxs-lookup"><span data-stu-id="84586-128">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="84586-129">**Prélvmt invent**</span><span class="sxs-lookup"><span data-stu-id="84586-129">**Inventory Pick**</span></span>  
-   <span data-ttu-id="84586-130">**Mouvement de stock**</span><span class="sxs-lookup"><span data-stu-id="84586-130">**Inventory Movement**</span></span>  
-   <span data-ttu-id="84586-131">**Feuille article**</span><span class="sxs-lookup"><span data-stu-id="84586-131">**Item Journal**</span></span>  
-   <span data-ttu-id="84586-132">**Feuille reclassement article**</span><span class="sxs-lookup"><span data-stu-id="84586-132">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="84586-133">(Divers états)</span><span class="sxs-lookup"><span data-stu-id="84586-133">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="84586-134">Documents d'interface utilisateur avancés</span><span class="sxs-lookup"><span data-stu-id="84586-134">Advanced UI Documents</span></span>  

-   <span data-ttu-id="84586-135">**Réception entrepôt**</span><span class="sxs-lookup"><span data-stu-id="84586-135">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="84586-136">**Feuille rangement**</span><span class="sxs-lookup"><span data-stu-id="84586-136">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="84586-137">**Rangement entrepôt**</span><span class="sxs-lookup"><span data-stu-id="84586-137">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="84586-138">**Feuille prélèvement**</span><span class="sxs-lookup"><span data-stu-id="84586-138">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="84586-139">**Prélèvement entrepôt**</span><span class="sxs-lookup"><span data-stu-id="84586-139">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="84586-140">**Feuille mouvement**</span><span class="sxs-lookup"><span data-stu-id="84586-140">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="84586-141">**Mouvement entrepôt**</span><span class="sxs-lookup"><span data-stu-id="84586-141">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="84586-142">**Prélèvement interne entrepôt**</span><span class="sxs-lookup"><span data-stu-id="84586-142">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="84586-143">**Rangement interne entrepôt**</span><span class="sxs-lookup"><span data-stu-id="84586-143">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="84586-144">**Feuille création emplacement**</span><span class="sxs-lookup"><span data-stu-id="84586-144">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="84586-145">**Feuille création contenu emplacement**</span><span class="sxs-lookup"><span data-stu-id="84586-145">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="84586-146">**Feuille article entrep.**</span><span class="sxs-lookup"><span data-stu-id="84586-146">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="84586-147">**Feuille reclassement article entrepôt**</span><span class="sxs-lookup"><span data-stu-id="84586-147">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="84586-148">(Divers états)</span><span class="sxs-lookup"><span data-stu-id="84586-148">(Various reports)</span></span>  

<span data-ttu-id="84586-149">Pour plus d'informations sur chaque document, reportez-vous aux rubriques correspondantes de la page.</span><span class="sxs-lookup"><span data-stu-id="84586-149">For more information about each document, see the respective page topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="84586-150">Terminologie</span><span class="sxs-lookup"><span data-stu-id="84586-150">Terminology</span></span>  
<span data-ttu-id="84586-151">Pour s'aligner avec les concepts financiers d'achats et de ventes, la documentation d'entrepôt [!INCLUDE[d365fin](includes/d365fin_md.md)] fait référence aux termes suivants pour la circulation des articles dans l'entrepôt.</span><span class="sxs-lookup"><span data-stu-id="84586-151">To align with the financial concepts of purchases and sales, [!INCLUDE[d365fin](includes/d365fin_md.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="84586-152">Terme</span><span class="sxs-lookup"><span data-stu-id="84586-152">Term</span></span>|<span data-ttu-id="84586-153">Désignation</span><span class="sxs-lookup"><span data-stu-id="84586-153">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="84586-154">Flux entrant</span><span class="sxs-lookup"><span data-stu-id="84586-154">Inbound flow</span></span>|<span data-ttu-id="84586-155">Articles qui se déplacent dans l'entrepôt, par exemple les achats et les enlogements transfert.</span><span class="sxs-lookup"><span data-stu-id="84586-155">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="84586-156">Flux interne</span><span class="sxs-lookup"><span data-stu-id="84586-156">Internal flow</span></span>|<span data-ttu-id="84586-157">Articles qui se déplacent dans l'entrepôt, par exemple les composants de production et la production.</span><span class="sxs-lookup"><span data-stu-id="84586-157">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="84586-158">Flux sortant</span><span class="sxs-lookup"><span data-stu-id="84586-158">Outbound flow</span></span>|<span data-ttu-id="84586-159">Articles qui se déplacent hors de l'entrepôt, par exemple les ventes et les désenlogements transfert.</span><span class="sxs-lookup"><span data-stu-id="84586-159">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="84586-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84586-160">See Also</span></span>  
 [<span data-ttu-id="84586-161">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="84586-161">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)