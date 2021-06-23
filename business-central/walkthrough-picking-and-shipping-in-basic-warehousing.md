---
title: Prélèvement et expédition dans les configurations d’entrepôt de base
description: Dans Business Central, les processus sortants de prélèvement et d’expédition peuvent être effectués de quatre manières, à l’aide de différentes fonctionnalités en fonction du niveau de complexité de l’entrepôt.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: e1763e6288c8b8218955049ba7ef4c461ee5164e
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214668"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="af2a1-103">Procédure pas à pas : Prélèvement et expédition dans les configurations de stockage de base</span><span class="sxs-lookup"><span data-stu-id="af2a1-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

<span data-ttu-id="af2a1-104">Dans [!INCLUDE[prod_short](includes/prod_short.md)], les processus sortants de prélèvement et d’expédition peuvent être effectués de quatre manières, à l’aide de différentes fonctionnalités en fonction du niveau de complexité de l’entrepôt.</span><span class="sxs-lookup"><span data-stu-id="af2a1-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="af2a1-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="af2a1-105">Method</span></span>|<span data-ttu-id="af2a1-106">Processus entrant</span><span class="sxs-lookup"><span data-stu-id="af2a1-106">Inbound process</span></span>|<span data-ttu-id="af2a1-107">Emplacements</span><span class="sxs-lookup"><span data-stu-id="af2a1-107">Bins</span></span>|<span data-ttu-id="af2a1-108">Prélèvements</span><span class="sxs-lookup"><span data-stu-id="af2a1-108">Picks</span></span>|<span data-ttu-id="af2a1-109">Livraisons</span><span class="sxs-lookup"><span data-stu-id="af2a1-109">Shipments</span></span>|<span data-ttu-id="af2a1-110">Niveau de complexité (Voir [Détails de conception : paramètres entrepôt](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="af2a1-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="af2a1-111">A</span><span class="sxs-lookup"><span data-stu-id="af2a1-111">A</span></span>|<span data-ttu-id="af2a1-112">Validation du prélèvement et de l’expédition à partir de la ligne commande</span><span class="sxs-lookup"><span data-stu-id="af2a1-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="af2a1-113">X</span><span class="sxs-lookup"><span data-stu-id="af2a1-113">X</span></span>|||<span data-ttu-id="af2a1-114">2</span><span class="sxs-lookup"><span data-stu-id="af2a1-114">2</span></span>|  
|<span data-ttu-id="af2a1-115">B</span><span class="sxs-lookup"><span data-stu-id="af2a1-115">B</span></span>|<span data-ttu-id="af2a1-116">Validation du prélèvement et de l’expédition à partir d’un document prélèvement stock</span><span class="sxs-lookup"><span data-stu-id="af2a1-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="af2a1-117">X</span><span class="sxs-lookup"><span data-stu-id="af2a1-117">X</span></span>||<span data-ttu-id="af2a1-118">3</span><span class="sxs-lookup"><span data-stu-id="af2a1-118">3</span></span>|  
|<span data-ttu-id="af2a1-119">C</span><span class="sxs-lookup"><span data-stu-id="af2a1-119">C</span></span>|<span data-ttu-id="af2a1-120">Validation du prélèvement et de l’expédition à partir d’un document expédition entrepôt</span><span class="sxs-lookup"><span data-stu-id="af2a1-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="af2a1-121">X</span><span class="sxs-lookup"><span data-stu-id="af2a1-121">X</span></span>|<span data-ttu-id="af2a1-122">5/4/6</span><span class="sxs-lookup"><span data-stu-id="af2a1-122">4/5/6</span></span>|  
|<span data-ttu-id="af2a1-123">J</span><span class="sxs-lookup"><span data-stu-id="af2a1-123">D</span></span>|<span data-ttu-id="af2a1-124">Validation du prélèvement à partir d’un document prélèvement entrepôt et validation de l’expédition à partir d’un document expédition entrepôt</span><span class="sxs-lookup"><span data-stu-id="af2a1-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="af2a1-125">X</span><span class="sxs-lookup"><span data-stu-id="af2a1-125">X</span></span>|<span data-ttu-id="af2a1-126">X</span><span class="sxs-lookup"><span data-stu-id="af2a1-126">X</span></span>|<span data-ttu-id="af2a1-127">5/4/6</span><span class="sxs-lookup"><span data-stu-id="af2a1-127">4/5/6</span></span>|  

<span data-ttu-id="af2a1-128">Pour plus d’informations, reportez\-vous à [Détails de conception : flux de désenlogement](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="af2a1-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="af2a1-129">La procédure pas à pas suivante illustre la méthode B dans la table précédente.</span><span class="sxs-lookup"><span data-stu-id="af2a1-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="af2a1-130">À propos de cette procédure pas à pas</span><span class="sxs-lookup"><span data-stu-id="af2a1-130">About This Walkthrough</span></span>

<span data-ttu-id="af2a1-131">Pour les configurations de stockage de base, lorsqu’un magasin est défini pour exiger un traitement des prélèvements mais pas un traitement des expéditions, vous utilisez la page **Prélèvement stock** pour enregistrer et valider les informations de prélèvement et d’expédition pour vos documents origine sortants.</span><span class="sxs-lookup"><span data-stu-id="af2a1-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="af2a1-132">Le document origine sortant peut être une commande vente, un retour achat, un désenlogement transfert ou un ordre de fabrication avec un besoin de composants.</span><span class="sxs-lookup"><span data-stu-id="af2a1-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="af2a1-133">Cette procédure pas à pas présente les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="af2a1-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="af2a1-134">Configuration du magasin SUD pour les prélèvements stock.</span><span class="sxs-lookup"><span data-stu-id="af2a1-134">Setting up SOUTH location for inventory picks.</span></span>  
- <span data-ttu-id="af2a1-135">Créez une commande vent pour le client 10000 pour 30 lampes Amsterdam.</span><span class="sxs-lookup"><span data-stu-id="af2a1-135">Creating a sales order for customer 10000 for 30 Amsterdam Lamps.</span></span>  
- <span data-ttu-id="af2a1-136">Lancement de la commande vente pour l’activité entrepôt.</span><span class="sxs-lookup"><span data-stu-id="af2a1-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="af2a1-137">Créez un prélèvement stock sur la base d’un document origine lancé.</span><span class="sxs-lookup"><span data-stu-id="af2a1-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="af2a1-138">Enregistrement d’un mouvement entrepôt de l’entrepôt et en même temps validation de l’expédition vente pour la commande vente d’origine.</span><span class="sxs-lookup"><span data-stu-id="af2a1-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="af2a1-139">Rôles</span><span class="sxs-lookup"><span data-stu-id="af2a1-139">Roles</span></span>

<span data-ttu-id="af2a1-140">Cette procédure pas à pas présente les tâches effectuées par les rôles utilisateur suivants :</span><span class="sxs-lookup"><span data-stu-id="af2a1-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="af2a1-141">Gestionnaire d’entrepôt</span><span class="sxs-lookup"><span data-stu-id="af2a1-141">Warehouse Manager</span></span>  
- <span data-ttu-id="af2a1-142">Préparateur de commandes</span><span class="sxs-lookup"><span data-stu-id="af2a1-142">Order Processor</span></span>  
- <span data-ttu-id="af2a1-143">Magasinier</span><span class="sxs-lookup"><span data-stu-id="af2a1-143">Warehouse Worker</span></span>  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a><span data-ttu-id="af2a1-144">Scénario</span><span class="sxs-lookup"><span data-stu-id="af2a1-144">Story</span></span>

<span data-ttu-id="af2a1-145">Ellen, la gestionnaire d’entrepôt de CRONUS, configure l’entrepôt SUD pour le prélèvement de base dans lequel les magasiniers traitent les commandes sortantes individuellement.</span><span class="sxs-lookup"><span data-stu-id="af2a1-145">Ellen, the warehouse manager at CRONUS, sets up SOUTH warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="af2a1-146">Susan, préparatrice de commandes, crée une commande vente pour 30 unités de l’article 1928-S à livrer au client 10000 depuis l’entrepôt SUD.</span><span class="sxs-lookup"><span data-stu-id="af2a1-146">Susan, the order processor, creates a sales order for 30 units of item 1928-S to be shipped to customer 10000 from the SOUTH Warehouse.</span></span> <span data-ttu-id="af2a1-147">Jean, le magasinier, doit s’assurer que l’expédition est préparée et livrée au client.</span><span class="sxs-lookup"><span data-stu-id="af2a1-147">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="af2a1-148">Jean gère toutes les tâches impliquées sur la page **Prélèvement stock**, qui indique automatiquement les endroits où 1928-S est stocké.</span><span class="sxs-lookup"><span data-stu-id="af2a1-148">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where 1928-S is stored.</span></span>

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a><span data-ttu-id="af2a1-149">Configuration des codes emplacement</span><span class="sxs-lookup"><span data-stu-id="af2a1-149">Setting Up the Bin Codes</span></span>
<span data-ttu-id="af2a1-150">Une fois que vous avez configuré le magasin, vous devez ajouter deux emplacements.</span><span class="sxs-lookup"><span data-stu-id="af2a1-150">Once you have the location set up, you must add two bins.</span></span>

#### <a name="to-setup-the-bin-codes"></a><span data-ttu-id="af2a1-151">Pour configurer les codes emplacement</span><span class="sxs-lookup"><span data-stu-id="af2a1-151">To setup the bin codes</span></span>

1. <span data-ttu-id="af2a1-152">Sélectionnez l’action **Emplacements**.</span><span class="sxs-lookup"><span data-stu-id="af2a1-152">Select the **Bins** action.</span></span>
2. <span data-ttu-id="af2a1-153">Créez deux emplacements, avec les codes *S-01-0001* et *S-01-0002*.</span><span class="sxs-lookup"><span data-stu-id="af2a1-153">Create two bins, with the codes *S-01-0001* and *S-01-0002*.</span></span>

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a><span data-ttu-id="af2a1-154">Ajout en tant que magasinier au magasin SUD</span><span class="sxs-lookup"><span data-stu-id="af2a1-154">Making Yourself a Warehouse Employee at Location SOUTH</span></span>

<span data-ttu-id="af2a1-155">Pour utiliser cette fonctionnalité, vous devez vous ajouter au magasin en tant que magasinier.</span><span class="sxs-lookup"><span data-stu-id="af2a1-155">In order to use this functionality, you must add yourself to the location as a warehouse worker.</span></span> 

#### <a name="to-make-yourself-a-warehouse-employee"></a><span data-ttu-id="af2a1-156">Pour vous ajouter en tant que magasinier</span><span class="sxs-lookup"><span data-stu-id="af2a1-156">To make yourself a warehouse employee</span></span>

  1. <span data-ttu-id="af2a1-157">Choisissez l’icône ![Ampoule qui ouvre la fonction de recherche en premier](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Magasiniers**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="af2a1-157">Choose the ![Lightbulb that opens the Tell Me feature first](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="af2a1-158">Choisissez le champ **ID utilisateur** et sélectionnez votre propre compte utilisateur sur la page **Magasiniers**.</span><span class="sxs-lookup"><span data-stu-id="af2a1-158">Choose the **User ID** field, and select your own user account on the **Warehouse Employees** page.</span></span>
  3. <span data-ttu-id="af2a1-159">Dans le champ **Code magasin**, entrez SUD.</span><span class="sxs-lookup"><span data-stu-id="af2a1-159">In the **Location Code** field, choose SOUTH.</span></span>  
  4. <span data-ttu-id="af2a1-160">Sélectionnez le champ **Par défaut**, puis cliquez sur le bouton **Oui**.</span><span class="sxs-lookup"><span data-stu-id="af2a1-160">Select the **Default** field, and then select the **Yes** button.</span></span>  

### <a name="making-item-1928-s-available"></a><span data-ttu-id="af2a1-161">Rendre l’article 1928-S disponible</span><span class="sxs-lookup"><span data-stu-id="af2a1-161">Making Item 1928-S Available</span></span>

<span data-ttu-id="af2a1-162">Pour rend l’article 1928-S disponible dans le magasin SUD, suivez cette procédure :</span><span class="sxs-lookup"><span data-stu-id="af2a1-162">To make item 1928-S available at the SOUTH location follow these steps:</span></span>  

  1. <span data-ttu-id="af2a1-163">Choisissez l’icône ![Ampoule qui ouvre la fonction de recherche en deuxième](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles article**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="af2a1-163">Choose the ![Lightbulb that opens the Tell Me feature second](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="af2a1-164">Ouvrez la feuille par défaut, puis créez deux lignes feuille article avec les informations de date de travail suivantes (23 janvier).</span><span class="sxs-lookup"><span data-stu-id="af2a1-164">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="af2a1-165">Type écriture</span><span class="sxs-lookup"><span data-stu-id="af2a1-165">Entry Type</span></span>|<span data-ttu-id="af2a1-166">Numéro d’article</span><span class="sxs-lookup"><span data-stu-id="af2a1-166">Item Number</span></span>|<span data-ttu-id="af2a1-167">Code magasin</span><span class="sxs-lookup"><span data-stu-id="af2a1-167">Location Code</span></span>|<span data-ttu-id="af2a1-168">Code emplacement</span><span class="sxs-lookup"><span data-stu-id="af2a1-168">Bin Code</span></span>|<span data-ttu-id="af2a1-169">Quantité</span><span class="sxs-lookup"><span data-stu-id="af2a1-169">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="af2a1-170">Positif (ajust.)</span><span class="sxs-lookup"><span data-stu-id="af2a1-170">Positive Adjmt.</span></span>|<span data-ttu-id="af2a1-171">1928-S</span><span class="sxs-lookup"><span data-stu-id="af2a1-171">1928-S</span></span>|<span data-ttu-id="af2a1-172">SUD</span><span class="sxs-lookup"><span data-stu-id="af2a1-172">SOUTH</span></span>|<span data-ttu-id="af2a1-173">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="af2a1-173">S-01-0001</span></span>|<span data-ttu-id="af2a1-174">20</span><span class="sxs-lookup"><span data-stu-id="af2a1-174">20</span></span>|  
        |<span data-ttu-id="af2a1-175">Positif (ajust.)</span><span class="sxs-lookup"><span data-stu-id="af2a1-175">Positive Adjmt.</span></span>|<span data-ttu-id="af2a1-176">1928-S</span><span class="sxs-lookup"><span data-stu-id="af2a1-176">1928-S</span></span>|<span data-ttu-id="af2a1-177">SUD</span><span class="sxs-lookup"><span data-stu-id="af2a1-177">SOUTH</span></span>|<span data-ttu-id="af2a1-178">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="af2a1-178">S-01-0002</span></span>|<span data-ttu-id="af2a1-179">20</span><span class="sxs-lookup"><span data-stu-id="af2a1-179">20</span></span>|  

        <span data-ttu-id="af2a1-180">Par défaut, le champ **Code emplacement** des lignes vente est masqué, vous devez donc l’afficher.</span><span class="sxs-lookup"><span data-stu-id="af2a1-180">By default, the **Bin Code** field on the sales lines are hidden, so you must display it.</span></span> <span data-ttu-id="af2a1-181">Pour cela, vous devez personnaliser la page.</span><span class="sxs-lookup"><span data-stu-id="af2a1-181">To do this you need to personalize the page.</span></span> <span data-ttu-id="af2a1-182">Pour plus d’informations, consultez [Commencer à personnaliser une page au moyen de la bannière Personnalisation](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span><span class="sxs-lookup"><span data-stu-id="af2a1-182">For more information, see [To start personalizing a page through the Personalizing banner](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span></span>

  3. <span data-ttu-id="af2a1-183">Choisissez **Actions**, puis **Validation**, puis **Valider**.</span><span class="sxs-lookup"><span data-stu-id="af2a1-183">Choose **Actions**, then **Posting**, and then choose **Post**.</span></span>  
  4. <span data-ttu-id="af2a1-184">Sélectionnez le bouton **Oui**.</span><span class="sxs-lookup"><span data-stu-id="af2a1-184">Select the **Yes** button.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="af2a1-185">Création de la commande vente</span><span class="sxs-lookup"><span data-stu-id="af2a1-185">Creating the Sales Order</span></span>

<span data-ttu-id="af2a1-186">Les commandes vente sont le type de document d’origine sortant le plus répandu.</span><span class="sxs-lookup"><span data-stu-id="af2a1-186">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="af2a1-187">Pour créer la commande vente</span><span class="sxs-lookup"><span data-stu-id="af2a1-187">To create the sales order</span></span>

1. <span data-ttu-id="af2a1-188">Choisissez l’icône ![Ampoule qui ouvre la fonction de recherche en troisième](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="af2a1-188">Choose the ![Lightbulb that opens the Tell Me feature third](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="af2a1-189">Sélectionnez l’action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="af2a1-189">Choose the **New** action.</span></span>  
3. <span data-ttu-id="af2a1-190">Créez une commande vente pour le client 10000 à la date de travail (23 janvier) comportant la ligne commande vente suivante.</span><span class="sxs-lookup"><span data-stu-id="af2a1-190">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="af2a1-191">Article ;</span><span class="sxs-lookup"><span data-stu-id="af2a1-191">Item</span></span>|<span data-ttu-id="af2a1-192">Code magasin</span><span class="sxs-lookup"><span data-stu-id="af2a1-192">Location Code</span></span>|<span data-ttu-id="af2a1-193">Quantité</span><span class="sxs-lookup"><span data-stu-id="af2a1-193">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="af2a1-194">1928-S</span><span class="sxs-lookup"><span data-stu-id="af2a1-194">1928-S</span></span>|<span data-ttu-id="af2a1-195">SUD</span><span class="sxs-lookup"><span data-stu-id="af2a1-195">SOUTH</span></span>|<span data-ttu-id="af2a1-196">30</span><span class="sxs-lookup"><span data-stu-id="af2a1-196">30</span></span>|  

     <span data-ttu-id="af2a1-197">Informez l’entrepôt que la commande vente est prête pour l’activité entrepôt lorsque la livraison sera faire.</span><span class="sxs-lookup"><span data-stu-id="af2a1-197">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="af2a1-198">Sélectionnez l’action **Lancer**.</span><span class="sxs-lookup"><span data-stu-id="af2a1-198">Choose the **Release** action.</span></span>  

    <span data-ttu-id="af2a1-199">Jean procède au prélèvement et à l’expédition des articles vendus.</span><span class="sxs-lookup"><span data-stu-id="af2a1-199">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="af2a1-200">Prélèvement et expédition d’articles</span><span class="sxs-lookup"><span data-stu-id="af2a1-200">Picking and Shipping Items</span></span>

<span data-ttu-id="af2a1-201">Sur la page **Prélèvement stock**, vous pouvez gérer toutes les activités entrepôt sortantes pour un document d’origine spécifique, tel qu’une commande vente.</span><span class="sxs-lookup"><span data-stu-id="af2a1-201">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="af2a1-202">Pour prélever et expédier des articles</span><span class="sxs-lookup"><span data-stu-id="af2a1-202">To pick and ship items</span></span>

1. <span data-ttu-id="af2a1-203">Choisissez l’icône ![Ampoule qui ouvre la fonction de recherche en quatrième](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Prélèvements stock**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="af2a1-203">Choose the ![Lightbulb that opens the Tell Me feature fourth](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="af2a1-204">Sélectionnez l’action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="af2a1-204">Choose the **New** action.</span></span>  

    <span data-ttu-id="af2a1-205">Assurez-vous que le champ **N°**</span><span class="sxs-lookup"><span data-stu-id="af2a1-205">Make sure that the **No.**</span></span> <span data-ttu-id="af2a1-206">du raccourci **Général** est rempli.</span><span class="sxs-lookup"><span data-stu-id="af2a1-206">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="af2a1-207">Sélectionnez le champ **Document origine**, puis sélectionnez **Commande vente**.</span><span class="sxs-lookup"><span data-stu-id="af2a1-207">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="af2a1-208">Sélectionnez le champ **N° origine**, sélectionnez la ligne correspondant à la vente au client 10000, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="af2a1-208">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="af2a1-209">Sinon, choisissez l’action **Extraire document origine**, puis sélectionnez la commande vente.</span><span class="sxs-lookup"><span data-stu-id="af2a1-209">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="af2a1-210">Choisissez l’action **Remplir qté à traiter**.</span><span class="sxs-lookup"><span data-stu-id="af2a1-210">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="af2a1-211">Sinon, dans le champ **Qté à traiter**, saisissez respectivement 10 et 20 sur les deux lignes prélèvement stock.</span><span class="sxs-lookup"><span data-stu-id="af2a1-211">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="af2a1-212">Choisissez l’action **Valider**, sélectionnez **Expédier**, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="af2a1-212">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="af2a1-213">Les 30 lampes Amsterdam sont à présent enregistrées comme prélevées depuis les emplacements S-01-0001 et S-01-0002, et une écriture comptable article négative est créée pour refléter l’expédition vente validée.</span><span class="sxs-lookup"><span data-stu-id="af2a1-213">The 30 Amsterdam Lamps are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="af2a1-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af2a1-214">See Also</span></span>

[<span data-ttu-id="af2a1-215">Prélever des articles avec les prélèvements stock</span><span class="sxs-lookup"><span data-stu-id="af2a1-215">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="af2a1-216">Prélever des articles pour l’expédition entrepôt</span><span class="sxs-lookup"><span data-stu-id="af2a1-216">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="af2a1-217">Configurer des entrepôts de base avec les zones d’opérations</span><span class="sxs-lookup"><span data-stu-id="af2a1-217">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="af2a1-218">Déplacer les composants vers une zone opérations dans les configurations de stockage de base</span><span class="sxs-lookup"><span data-stu-id="af2a1-218">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="af2a1-219">Prélever pour la fabrication et l’assemblage</span><span class="sxs-lookup"><span data-stu-id="af2a1-219">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="af2a1-220">Déplacer des articles ad hoc dans les configurations de stockage de base</span><span class="sxs-lookup"><span data-stu-id="af2a1-220">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="af2a1-221">Détails de conception : flux de désenlogement</span><span class="sxs-lookup"><span data-stu-id="af2a1-221">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="af2a1-222">Procédures pas à pas liées au processus entreprise</span><span class="sxs-lookup"><span data-stu-id="af2a1-222">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="af2a1-223">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af2a1-223">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
