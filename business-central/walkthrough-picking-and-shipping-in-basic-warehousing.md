---
title: Prélèvement et expédition dans les configurations de stockage de base | Microsoft Docs
description: Dans Business Central, les processus sortants de prélèvement et d’expédition peuvent être effectués de quatre manières, à l’aide de différentes fonctionnalités en fonction du niveau de complexité de l’entrepôt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 96a837eaded2cf9be5e1fabb4d7f81415a171f96
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393464"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="082f8-103">Procédure pas à pas : Prélèvement et expédition dans les configurations de stockage de base</span><span class="sxs-lookup"><span data-stu-id="082f8-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

<span data-ttu-id="082f8-104">Dans [!INCLUDE[prod_short](includes/prod_short.md)], les processus sortants de prélèvement et d’expédition peuvent être effectués de quatre manières, à l’aide de différentes fonctionnalités en fonction du niveau de complexité de l’entrepôt.</span><span class="sxs-lookup"><span data-stu-id="082f8-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="082f8-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="082f8-105">Method</span></span>|<span data-ttu-id="082f8-106">Processus entrant</span><span class="sxs-lookup"><span data-stu-id="082f8-106">Inbound process</span></span>|<span data-ttu-id="082f8-107">Emplacements</span><span class="sxs-lookup"><span data-stu-id="082f8-107">Bins</span></span>|<span data-ttu-id="082f8-108">Prélèvements</span><span class="sxs-lookup"><span data-stu-id="082f8-108">Picks</span></span>|<span data-ttu-id="082f8-109">Livraisons</span><span class="sxs-lookup"><span data-stu-id="082f8-109">Shipments</span></span>|<span data-ttu-id="082f8-110">Niveau de complexité (Voir [Détails de conception : paramètres entrepôt](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="082f8-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="082f8-111">A</span><span class="sxs-lookup"><span data-stu-id="082f8-111">A</span></span>|<span data-ttu-id="082f8-112">Validation du prélèvement et de l’expédition à partir de la ligne commande</span><span class="sxs-lookup"><span data-stu-id="082f8-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="082f8-113">X</span><span class="sxs-lookup"><span data-stu-id="082f8-113">X</span></span>|||<span data-ttu-id="082f8-114">2</span><span class="sxs-lookup"><span data-stu-id="082f8-114">2</span></span>|  
|<span data-ttu-id="082f8-115">B</span><span class="sxs-lookup"><span data-stu-id="082f8-115">B</span></span>|<span data-ttu-id="082f8-116">Validation du prélèvement et de l’expédition à partir d’un document prélèvement stock</span><span class="sxs-lookup"><span data-stu-id="082f8-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="082f8-117">X</span><span class="sxs-lookup"><span data-stu-id="082f8-117">X</span></span>||<span data-ttu-id="082f8-118">3</span><span class="sxs-lookup"><span data-stu-id="082f8-118">3</span></span>|  
|<span data-ttu-id="082f8-119">C</span><span class="sxs-lookup"><span data-stu-id="082f8-119">C</span></span>|<span data-ttu-id="082f8-120">Validation du prélèvement et de l’expédition à partir d’un document expédition entrepôt</span><span class="sxs-lookup"><span data-stu-id="082f8-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="082f8-121">X</span><span class="sxs-lookup"><span data-stu-id="082f8-121">X</span></span>|<span data-ttu-id="082f8-122">5/4/6</span><span class="sxs-lookup"><span data-stu-id="082f8-122">4/5/6</span></span>|  
|<span data-ttu-id="082f8-123">J</span><span class="sxs-lookup"><span data-stu-id="082f8-123">D</span></span>|<span data-ttu-id="082f8-124">Validation du prélèvement à partir d’un document prélèvement entrepôt et validation de l’expédition à partir d’un document expédition entrepôt</span><span class="sxs-lookup"><span data-stu-id="082f8-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="082f8-125">X</span><span class="sxs-lookup"><span data-stu-id="082f8-125">X</span></span>|<span data-ttu-id="082f8-126">X</span><span class="sxs-lookup"><span data-stu-id="082f8-126">X</span></span>|<span data-ttu-id="082f8-127">5/4/6</span><span class="sxs-lookup"><span data-stu-id="082f8-127">4/5/6</span></span>|  

<span data-ttu-id="082f8-128">Pour plus d’informations, reportez\-vous à [Détails de conception : flux de désenlogement](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="082f8-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="082f8-129">La procédure pas à pas suivante illustre la méthode B dans la table précédente.</span><span class="sxs-lookup"><span data-stu-id="082f8-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="about-this-walkthrough"></a><span data-ttu-id="082f8-130">À propos de cette procédure pas à pas</span><span class="sxs-lookup"><span data-stu-id="082f8-130">About This Walkthrough</span></span>

<span data-ttu-id="082f8-131">Pour les configurations de stockage de base, lorsqu’un magasin est défini pour exiger un traitement des prélèvements mais pas un traitement des expéditions, vous utilisez la page **Prélèvement stock** pour enregistrer et valider les informations de prélèvement et d’expédition pour vos documents origine sortants.</span><span class="sxs-lookup"><span data-stu-id="082f8-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="082f8-132">Le document origine sortant peut être une commande vente, un retour achat, un désenlogement transfert ou un ordre de fabrication avec un besoin de composants.</span><span class="sxs-lookup"><span data-stu-id="082f8-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="082f8-133">Cette procédure pas à pas présente les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="082f8-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="082f8-134">Configuration du magasin ARGENT pour les prélèvements stock.</span><span class="sxs-lookup"><span data-stu-id="082f8-134">Setting up SILVER location for inventory picks.</span></span>  
- <span data-ttu-id="082f8-135">Créez une commande vent pour le client 10000 pour 30 haut-parleurs.</span><span class="sxs-lookup"><span data-stu-id="082f8-135">Creating a sales order for customer 10000 for 30 loudspeakers.</span></span>  
- <span data-ttu-id="082f8-136">Lancement de la commande vente pour l’activité entrepôt.</span><span class="sxs-lookup"><span data-stu-id="082f8-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="082f8-137">Créez un prélèvement stock sur la base d’un document origine lancé.</span><span class="sxs-lookup"><span data-stu-id="082f8-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="082f8-138">Enregistrement d’un mouvement entrepôt de l’entrepôt et en même temps validation de l’expédition vente pour la commande vente d’origine.</span><span class="sxs-lookup"><span data-stu-id="082f8-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a><span data-ttu-id="082f8-139">Rôles</span><span class="sxs-lookup"><span data-stu-id="082f8-139">Roles</span></span>

<span data-ttu-id="082f8-140">Cette procédure pas à pas présente les tâches effectuées par les rôles utilisateur suivants :</span><span class="sxs-lookup"><span data-stu-id="082f8-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="082f8-141">Gestionnaire d’entrepôt</span><span class="sxs-lookup"><span data-stu-id="082f8-141">Warehouse Manager</span></span>  
- <span data-ttu-id="082f8-142">Préparateur de commandes</span><span class="sxs-lookup"><span data-stu-id="082f8-142">Order Processor</span></span>  
- <span data-ttu-id="082f8-143">Magasinier</span><span class="sxs-lookup"><span data-stu-id="082f8-143">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="082f8-144">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="082f8-144">Prerequisites</span></span>

<span data-ttu-id="082f8-145">Pour exécuter ce processus pas à pas, vous devez :</span><span class="sxs-lookup"><span data-stu-id="082f8-145">To complete this walkthrough, you will need:</span></span>  

- <span data-ttu-id="082f8-146">Pour [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, une société basée sur l’option **Évaluation avancée - exemples de données complètes** dans un environnement sandbox.</span><span class="sxs-lookup"><span data-stu-id="082f8-146">For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment.</span></span> <span data-ttu-id="082f8-147">Pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site, CRONUS International Ltd. installé.</span><span class="sxs-lookup"><span data-stu-id="082f8-147">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS International Ltd. installed.</span></span>  
- <span data-ttu-id="082f8-148">Pour devenir magasinier dans un magasin ARGENT, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="082f8-148">To make yourself a warehouse employee at the location SILVER by following these steps:</span></span>  

  1. <span data-ttu-id="082f8-149">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Magasiniers**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="082f8-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="082f8-150">Choisissez le champ **ID utilisateur** et sélectionnez votre propre compte utilisateur sur la page **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="082f8-150">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
  3. <span data-ttu-id="082f8-151">Dans le champ **Code magasin**, entrez ARGENT.</span><span class="sxs-lookup"><span data-stu-id="082f8-151">In the **Location Code** field, enter SILVER.</span></span>  
  4. <span data-ttu-id="082f8-152">Sélectionnez le champ **Par défaut**.</span><span class="sxs-lookup"><span data-stu-id="082f8-152">Select the **Default** field.</span></span>  

- <span data-ttu-id="082f8-153">Rend l’article LS-81 disponible dans le magasin ARGENT en suivant cette procédure :</span><span class="sxs-lookup"><span data-stu-id="082f8-153">Make item LS-81 available at SILVER location by following these steps:</span></span>  

  1. <span data-ttu-id="082f8-154">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles article**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="082f8-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="082f8-155">Ouvrez la feuille par défaut, puis créez deux lignes feuille article avec les informations de date de travail suivantes (23 janvier).</span><span class="sxs-lookup"><span data-stu-id="082f8-155">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="082f8-156">Type écriture</span><span class="sxs-lookup"><span data-stu-id="082f8-156">Entry Type</span></span>|<span data-ttu-id="082f8-157">Numéro d’article</span><span class="sxs-lookup"><span data-stu-id="082f8-157">Item Number</span></span>|<span data-ttu-id="082f8-158">Code magasin</span><span class="sxs-lookup"><span data-stu-id="082f8-158">Location Code</span></span>|<span data-ttu-id="082f8-159">Code emplacement</span><span class="sxs-lookup"><span data-stu-id="082f8-159">Bin Code</span></span>|<span data-ttu-id="082f8-160">Quantité</span><span class="sxs-lookup"><span data-stu-id="082f8-160">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="082f8-161">Positif (ajust.)</span><span class="sxs-lookup"><span data-stu-id="082f8-161">Positive Adjmt.</span></span>|<span data-ttu-id="082f8-162">LS-81</span><span class="sxs-lookup"><span data-stu-id="082f8-162">LS-81</span></span>|<span data-ttu-id="082f8-163">ARGENT</span><span class="sxs-lookup"><span data-stu-id="082f8-163">SILVER</span></span>|<span data-ttu-id="082f8-164">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="082f8-164">S-01-0001</span></span>|<span data-ttu-id="082f8-165">20</span><span class="sxs-lookup"><span data-stu-id="082f8-165">20</span></span>|  
        |<span data-ttu-id="082f8-166">Positif (ajust.)</span><span class="sxs-lookup"><span data-stu-id="082f8-166">Positive Adjmt.</span></span>|<span data-ttu-id="082f8-167">LS-81</span><span class="sxs-lookup"><span data-stu-id="082f8-167">LS-81</span></span>|<span data-ttu-id="082f8-168">ARGENT</span><span class="sxs-lookup"><span data-stu-id="082f8-168">SILVER</span></span>|<span data-ttu-id="082f8-169">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="082f8-169">S-01-0002</span></span>|<span data-ttu-id="082f8-170">20</span><span class="sxs-lookup"><span data-stu-id="082f8-170">20</span></span>|  

  3. <span data-ttu-id="082f8-171">Choisissez l’action **Valider**, puis cliquez sur le bouton **Oui**.</span><span class="sxs-lookup"><span data-stu-id="082f8-171">Choose the **Post** action, and then select the **Yes** button.</span></span>  

## <a name="story"></a><span data-ttu-id="082f8-172">Scénario</span><span class="sxs-lookup"><span data-stu-id="082f8-172">Story</span></span>

<span data-ttu-id="082f8-173">Ellen, la gestionnaire d’entrepôt de CRONUS, configure l’entrepôt ARGENT pour le prélèvement de base dans lequel les magasiniers traitent les commandes sortantes individuellement.</span><span class="sxs-lookup"><span data-stu-id="082f8-173">Ellen, the warehouse manager at CRONUS, sets up SILVER warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="082f8-174">Susan, préparatrice de commandes, crée une commande vente pour 30 unités de l’article LS-81 à livrer au client 10000 depuis l’entrepôt ARGENT.</span><span class="sxs-lookup"><span data-stu-id="082f8-174">Susan, the order processor, creates a sales order for 30 units of item LS-81 to be shipped to customer 10000 from the SILVER Warehouse.</span></span> <span data-ttu-id="082f8-175">Jean, le magasinier, doit s’assurer que l’expédition est préparée et livrée au client.</span><span class="sxs-lookup"><span data-stu-id="082f8-175">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="082f8-176">Jean gère toutes les tâches impliquées sur la page **Prélèvement stock**, qui indique automatiquement les endroits où LS-81 est stocké.</span><span class="sxs-lookup"><span data-stu-id="082f8-176">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where LS-81 is stored.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="082f8-177">Configuration du magasin</span><span class="sxs-lookup"><span data-stu-id="082f8-177">Setting Up the Location</span></span>

<span data-ttu-id="082f8-178">La configuration de la page **Fiche magasin** définit les flux d’entrepôt de la société.</span><span class="sxs-lookup"><span data-stu-id="082f8-178">The setup of the **Location Card** page defines the company's warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="082f8-179">Pour configurer le magasin</span><span class="sxs-lookup"><span data-stu-id="082f8-179">To set up the location</span></span>

1. <span data-ttu-id="082f8-180">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Magasins**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="082f8-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2. <span data-ttu-id="082f8-181">Ouvrez la fiche magasin ARGENT.</span><span class="sxs-lookup"><span data-stu-id="082f8-181">Open the SILVER location card.</span></span>  
3. <span data-ttu-id="082f8-182">Sur le raccourci **Entrepôt**, cochez la case **Prélèvement requis**.</span><span class="sxs-lookup"><span data-stu-id="082f8-182">On the **Warehouse** FastTab, choose the **Require Pick** check box.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="082f8-183">Création de la commande vente</span><span class="sxs-lookup"><span data-stu-id="082f8-183">Creating the Sales Order</span></span>

<span data-ttu-id="082f8-184">Les commandes vente sont le type de document d’origine sortant le plus répandu.</span><span class="sxs-lookup"><span data-stu-id="082f8-184">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="082f8-185">Pour créer la commande vente</span><span class="sxs-lookup"><span data-stu-id="082f8-185">To create the sales order</span></span>

1. <span data-ttu-id="082f8-186">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="082f8-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="082f8-187">Sélectionnez l’action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="082f8-187">Choose the **New** action.</span></span>  
3. <span data-ttu-id="082f8-188">Créez une commande vente pour le client 10000 à la date de travail (23 janvier) comportant la ligne commande vente suivante.</span><span class="sxs-lookup"><span data-stu-id="082f8-188">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="082f8-189">Article ;</span><span class="sxs-lookup"><span data-stu-id="082f8-189">Item</span></span>|<span data-ttu-id="082f8-190">Code magasin</span><span class="sxs-lookup"><span data-stu-id="082f8-190">Location Code</span></span>|<span data-ttu-id="082f8-191">Quantité</span><span class="sxs-lookup"><span data-stu-id="082f8-191">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="082f8-192">LS_81</span><span class="sxs-lookup"><span data-stu-id="082f8-192">LS_81</span></span>|<span data-ttu-id="082f8-193">ARGENT</span><span class="sxs-lookup"><span data-stu-id="082f8-193">SILVER</span></span>|<span data-ttu-id="082f8-194">30</span><span class="sxs-lookup"><span data-stu-id="082f8-194">30</span></span>|  

     <span data-ttu-id="082f8-195">Informez l’entrepôt que la commande vente est prête pour l’activité entrepôt lorsque la livraison sera faire.</span><span class="sxs-lookup"><span data-stu-id="082f8-195">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="082f8-196">Sélectionnez l’action **Lancer**.</span><span class="sxs-lookup"><span data-stu-id="082f8-196">Choose the **Release** action.</span></span>  

    <span data-ttu-id="082f8-197">Jean procède au prélèvement et à l’expédition des articles vendus.</span><span class="sxs-lookup"><span data-stu-id="082f8-197">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="082f8-198">Prélèvement et expédition d’articles</span><span class="sxs-lookup"><span data-stu-id="082f8-198">Picking and Shipping Items</span></span>

<span data-ttu-id="082f8-199">Sur la page **Prélèvement stock**, vous pouvez gérer toutes les activités entrepôt sortantes pour un document d’origine spécifique, tel qu’une commande vente.</span><span class="sxs-lookup"><span data-stu-id="082f8-199">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="082f8-200">Pour prélever et expédier des articles</span><span class="sxs-lookup"><span data-stu-id="082f8-200">To pick and ship items</span></span>

1. <span data-ttu-id="082f8-201">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Prélèvements stock**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="082f8-201">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="082f8-202">Sélectionnez l’action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="082f8-202">Choose the **New** action.</span></span>  

    <span data-ttu-id="082f8-203">Assurez-vous que le champ **N°**</span><span class="sxs-lookup"><span data-stu-id="082f8-203">Make sure that the **No.**</span></span> <span data-ttu-id="082f8-204">du raccourci **Général** est rempli.</span><span class="sxs-lookup"><span data-stu-id="082f8-204">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="082f8-205">Sélectionnez le champ **Document origine**, puis sélectionnez **Commande vente**.</span><span class="sxs-lookup"><span data-stu-id="082f8-205">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="082f8-206">Sélectionnez le champ **N° origine**, sélectionnez la ligne correspondant à la vente au client 10000, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="082f8-206">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="082f8-207">Sinon, choisissez l’action **Extraire document origine**, puis sélectionnez la commande vente.</span><span class="sxs-lookup"><span data-stu-id="082f8-207">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="082f8-208">Choisissez l’action **Remplir qté à traiter**.</span><span class="sxs-lookup"><span data-stu-id="082f8-208">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="082f8-209">Sinon, dans le champ **Qté à traiter**, saisissez respectivement 10 et 20 sur les deux lignes prélèvement stock.</span><span class="sxs-lookup"><span data-stu-id="082f8-209">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="082f8-210">Choisissez l’action **Valider**, sélectionnez **Expédier**, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="082f8-210">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="082f8-211">Les 30 haut-parleurs sont à présent enregistrés comme prélevés depuis les emplacements S-01-0001 et S-01-0002, et une écriture comptable article négative est créée pour refléter l’expédition vente validée.</span><span class="sxs-lookup"><span data-stu-id="082f8-211">The 30 loudspeakers are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="082f8-212">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="082f8-212">See Also</span></span>

[<span data-ttu-id="082f8-213">Prélever des articles avec les prélèvements stock</span><span class="sxs-lookup"><span data-stu-id="082f8-213">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="082f8-214">Prélever des articles pour l’expédition entrepôt</span><span class="sxs-lookup"><span data-stu-id="082f8-214">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="082f8-215">Configurer des entrepôts de base avec les zones d’opérations</span><span class="sxs-lookup"><span data-stu-id="082f8-215">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="082f8-216">Déplacer les composants vers une zone opérations dans les configurations de stockage de base</span><span class="sxs-lookup"><span data-stu-id="082f8-216">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="082f8-217">Prélever pour la fabrication et l’assemblage</span><span class="sxs-lookup"><span data-stu-id="082f8-217">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="082f8-218">Déplacer des articles ad hoc dans les configurations de stockage de base</span><span class="sxs-lookup"><span data-stu-id="082f8-218">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="082f8-219">Détails de conception : flux de désenlogement</span><span class="sxs-lookup"><span data-stu-id="082f8-219">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="082f8-220">Procédures pas à pas liées au processus entreprise</span><span class="sxs-lookup"><span data-stu-id="082f8-220">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="082f8-221">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="082f8-221">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]