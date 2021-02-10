---
title: Utiliser des schémas XML pour préparer des définitions d’échange de données
description: Utilisez des schémas XML pour configurer l’infrastructure d’échange de documents.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 78aa941b8b886ed37dbed0d83a35d13b0e427421
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754632"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="60bd4-103">Utiliser des schémas XML pour préparer des définitions d’échange de données</span><span class="sxs-lookup"><span data-stu-id="60bd4-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>

<span data-ttu-id="60bd4-104">Pour activer l’importation/exportation des données dans des fichiers XML à travers l’infrastructure d’échange de données de [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez utiliser des schémas XML pour définir les éléments de données à échanger avec [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="60bd4-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[prod_short](includes/prod_short.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="60bd4-105">Vous effectuez ce travail sur la page **Visionneuse de schéma XML** en chargeant le fichier de schéma XML, en sélectionnant les éléments de données appropriés, puis en initialisant une définition d’échange de données.</span><span class="sxs-lookup"><span data-stu-id="60bd4-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing a data exchange definition.</span></span>  

 <span data-ttu-id="60bd4-106">Lorsque vous avez défini quels éléments de données inclure selon le schéma XML, vous pouvez utiliser l’action **Générer définition d’échange de données** pour initialiser une définition d’échange de données basée sur les éléments de données sélectionnés, que vous complétez dans l’infrastructure d’échange de données.</span><span class="sxs-lookup"><span data-stu-id="60bd4-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="60bd4-107">Cela crée un enregistrement sur la page **Définitions échange comptabilité** où vous continuez en définissant quels éléments de la liste des fichiers correspondent à quels champs dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="60bd4-107">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="60bd4-108">Pour plus d’informations, voir [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="60bd4-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="60bd4-109">Cette rubrique contient les procédures suivantes :</span><span class="sxs-lookup"><span data-stu-id="60bd4-109">This topic contains the following procedures:</span></span>  

- <span data-ttu-id="60bd4-110">Charger un fichier de schéma XML</span><span class="sxs-lookup"><span data-stu-id="60bd4-110">To load an XML schema file</span></span>  

- <span data-ttu-id="60bd4-111">Sélectionner ou supprimer des nœuds dans un schéma XML</span><span class="sxs-lookup"><span data-stu-id="60bd4-111">To select or clear nodes in an XML schema</span></span>  

- <span data-ttu-id="60bd4-112">Générer une définition d’échange de données basée sur un schéma XML</span><span class="sxs-lookup"><span data-stu-id="60bd4-112">To generate a data exchange definition that is based on an XML schema</span></span>  

## <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="60bd4-113">Charger un fichier de schéma XML</span><span class="sxs-lookup"><span data-stu-id="60bd4-113">To load an XML schema file</span></span>

1. <span data-ttu-id="60bd4-114">Assurez-vous que le fichier de schéma XML approprié est disponible.</span><span class="sxs-lookup"><span data-stu-id="60bd4-114">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="60bd4-115">L’extension du fichier est .xsd.</span><span class="sxs-lookup"><span data-stu-id="60bd4-115">The file extension is .xsd.</span></span>  

2. <span data-ttu-id="60bd4-116">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Schémas XML**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="60bd4-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3. <span data-ttu-id="60bd4-117">Sélectionnez l’action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="60bd4-117">Choose the **New** action.</span></span>  

4. <span data-ttu-id="60bd4-118">Renseignez les champs comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="60bd4-118">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="60bd4-119">Champ</span><span class="sxs-lookup"><span data-stu-id="60bd4-119">Field</span></span>|<span data-ttu-id="60bd4-120">Désignation</span><span class="sxs-lookup"><span data-stu-id="60bd4-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="60bd4-121">**Code**</span><span class="sxs-lookup"><span data-stu-id="60bd4-121">**Code**</span></span>|<span data-ttu-id="60bd4-122">Indiquez un code pour identifier le schéma XML.</span><span class="sxs-lookup"><span data-stu-id="60bd4-122">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="60bd4-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="60bd4-123">**Description**</span></span>|<span data-ttu-id="60bd4-124">Spécifiez une description du schéma XML.</span><span class="sxs-lookup"><span data-stu-id="60bd4-124">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="60bd4-125">Le champ **Espace de noms cible** spécifie un espace de noms dans le fichier de schéma XML qui a été chargé pour la ligne.</span><span class="sxs-lookup"><span data-stu-id="60bd4-125">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5. <span data-ttu-id="60bd4-126">Sélectionnez l’action **Charger le schéma**, puis sélectionnez le fichier de schéma XML.</span><span class="sxs-lookup"><span data-stu-id="60bd4-126">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="60bd4-127">Lorsque le fichier est chargé, les autres champs de la ligne sont renseignés à l’aide des informations du fichier, et la case **Le schéma est chargé** est cochée.</span><span class="sxs-lookup"><span data-stu-id="60bd4-127">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="60bd4-128">L’arborescence du schéma XML chargé est réduite par défaut.</span><span class="sxs-lookup"><span data-stu-id="60bd4-128">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="60bd4-129">Vous développez chaque nœud en choisissant le bouton **+** sur le nœud.</span><span class="sxs-lookup"><span data-stu-id="60bd4-129">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="60bd4-130">Pour développer tous les nœuds, sélectionnez **Développer tout** sur le ruban.</span><span class="sxs-lookup"><span data-stu-id="60bd4-130">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="60bd4-131">Sélectionner ou supprimer des nœuds dans un schéma XML</span><span class="sxs-lookup"><span data-stu-id="60bd4-131">To select or clear nodes in an XML schema</span></span>  

1. <span data-ttu-id="60bd4-132">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Visionneuse de schéma XML**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="60bd4-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2. <span data-ttu-id="60bd4-133">Renseignez les champs de l’en-tête, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="60bd4-133">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="60bd4-134">Champ</span><span class="sxs-lookup"><span data-stu-id="60bd4-134">Field</span></span>|<span data-ttu-id="60bd4-135">Désignation</span><span class="sxs-lookup"><span data-stu-id="60bd4-135">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="60bd4-136">**Code schéma XML**</span><span class="sxs-lookup"><span data-stu-id="60bd4-136">**XML Schema Code**</span></span>|<span data-ttu-id="60bd4-137">Spécifiez le fichier de schéma XML que vous avez chargé à l’étape 5 dans la section « Charger un fichier de schéma XML ».</span><span class="sxs-lookup"><span data-stu-id="60bd4-137">Specify the XML schema file that you loaded in step 5 in the "To load an XML schema file" section.</span></span>|  
    |<span data-ttu-id="60bd4-138">**Nouveau n° de XMLport**</span><span class="sxs-lookup"><span data-stu-id="60bd4-138">**New XMLport No.**</span></span>|<span data-ttu-id="60bd4-139">Spécifiez le numéro du XMLport qui est créé pour ce schéma XML lorsque vous sélectionnez l’action **Générer XMLport**.</span><span class="sxs-lookup"><span data-stu-id="60bd4-139">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="60bd4-140">Les lignes sont à présent remplies avec des nœuds représentant tous les éléments figurant dans le schéma XML.</span><span class="sxs-lookup"><span data-stu-id="60bd4-140">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="60bd4-141">Les nœuds des éléments qui sont obligatoires selon le schéma XML sont activés par défaut.</span><span class="sxs-lookup"><span data-stu-id="60bd4-141">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3. <span data-ttu-id="60bd4-142">Sur la première ligne, dans la colonne **Nom noeud**, développez le nœud **Document**, puis développez progressivement les nœuds sous-jacents que vous souhaitez examiner.</span><span class="sxs-lookup"><span data-stu-id="60bd4-142">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="60bd4-143">Sinon, cliquez avec le bouton droit sur un nœud, puis choisissez **Développer tout**.</span><span class="sxs-lookup"><span data-stu-id="60bd4-143">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4. <span data-ttu-id="60bd4-144">Sélectionnez l’une des actions suivantes pour modifier les nœuds qui sont affichés.</span><span class="sxs-lookup"><span data-stu-id="60bd4-144">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="60bd4-145">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="60bd4-145">**Action**</span></span>|<span data-ttu-id="60bd4-146">Désignation</span><span class="sxs-lookup"><span data-stu-id="60bd4-146">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="60bd4-147">**Afficher tout**</span><span class="sxs-lookup"><span data-stu-id="60bd4-147">**Show All**</span></span>|<span data-ttu-id="60bd4-148">Tous les nœuds sont affichés.</span><span class="sxs-lookup"><span data-stu-id="60bd4-148">All nodes are shown.</span></span>|  
    |<span data-ttu-id="60bd4-149">**Masquer non obligatoire**</span><span class="sxs-lookup"><span data-stu-id="60bd4-149">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="60bd4-150">Seuls les nœuds représentant les éléments qui sont obligatoires selon le schéma XML sont affichés.</span><span class="sxs-lookup"><span data-stu-id="60bd4-150">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="60bd4-151">Les nœuds sont généralement indiqués par un **1** dans le champ **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="60bd4-151">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="60bd4-152">Choisissez **Afficher tout** pour rétablir l’affichage.</span><span class="sxs-lookup"><span data-stu-id="60bd4-152">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="60bd4-153">**Masquer non sélectionné**</span><span class="sxs-lookup"><span data-stu-id="60bd4-153">**Hide Non-Selected**</span></span>|<span data-ttu-id="60bd4-154">Seuls les nœuds dont la case à cocher **Sélectionné** est activée sont affichés.</span><span class="sxs-lookup"><span data-stu-id="60bd4-154">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="60bd4-155">Choisissez **Afficher tout** pour rétablir l’affichage.</span><span class="sxs-lookup"><span data-stu-id="60bd4-155">Choose **Show All** to reverse the view.</span></span>|  

5. <span data-ttu-id="60bd4-156">Choisissez l’action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="60bd4-156">Choose the **Edit** action.</span></span>  

6. <span data-ttu-id="60bd4-157">Dans le champ **Sélectionné**, spécifiez pour chaque nœud si vous souhaitez que l’élément soit pris en charge dans la définition d’échange de données pour le fichier bancaire SEPA connexe.</span><span class="sxs-lookup"><span data-stu-id="60bd4-157">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="60bd4-158">Lorsque vous sélectionnez un nœud enfant obligatoire, tous les nœuds parents au-dessus de lui sont également sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="60bd4-158">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7. <span data-ttu-id="60bd4-159">Sélectionnez l’action **Sélectionner tous les éléments obligatoires** pour resélectionner tous les nœuds représentant des éléments qui sont obligatoires en fonction du schéma XML.</span><span class="sxs-lookup"><span data-stu-id="60bd4-159">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8. <span data-ttu-id="60bd4-160">Sélectionnez l’action **Désélectionner tout** pour désactiver toutes les options.</span><span class="sxs-lookup"><span data-stu-id="60bd4-160">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="60bd4-161">Le champ **Choix** spécifie que le nœud a deux ou plusieurs nœuds frère qui fonctionnent comme options.</span><span class="sxs-lookup"><span data-stu-id="60bd4-161">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="60bd4-162">Générer une définition d’échange de données basée sur un schéma XML</span><span class="sxs-lookup"><span data-stu-id="60bd4-162">To generate a data exchange definition that is based on an XML schema</span></span>  

1. <span data-ttu-id="60bd4-163">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Schémas XML**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="60bd4-163">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2. <span data-ttu-id="60bd4-164">Sélectionnez le schéma XML approprié, puis sélectionnez l’action **Ouvrir la visionneuse de schéma XML**.</span><span class="sxs-lookup"><span data-stu-id="60bd4-164">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3. <span data-ttu-id="60bd4-165">Assurez-vous que les nœuds appropriés sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="60bd4-165">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="60bd4-166">Pour plus d’informations, reportez-vous à la section « Sélectionner ou supprimer des nœuds dans un schéma XML ».</span><span class="sxs-lookup"><span data-stu-id="60bd4-166">For more information, see the "To select or clear nodes in an XML schema" section.</span></span>  

4. <span data-ttu-id="60bd4-167">Sur la page **Visionneuse de schéma XML**, sélectionnez l’action **Générer définition d’échange de données**.</span><span class="sxs-lookup"><span data-stu-id="60bd4-167">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="60bd4-168">Une définition d’échange de données est créée sur la page **Définitions échange comptabilité**, que vous pouvez renseigner en indiquant quels éléments du fichier correspondent à quels champs de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="60bd4-168">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="60bd4-169">Pour plus d’informations, voir [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="60bd4-169">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="60bd4-170">Vous pouvez également utiliser la fonction **Extraire structure de fichiers** de la page **Définitions échange comptabilité**, qui utilise la fonctionnalité de la page **Visionneuse de schéma XML** pour préremplir le raccourci **Définitions colonne**.</span><span class="sxs-lookup"><span data-stu-id="60bd4-170">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

> [!NOTE]
> <span data-ttu-id="60bd4-171">Dans la vague 1 du lancement de la version 2019 et versions antérieures, vous pouviez générer un XMLport basé sur le schéma, puis l’importer dans votre solution.</span><span class="sxs-lookup"><span data-stu-id="60bd4-171">In 2019 release wave 1 and earlier versions, you could generate an XMLport that was based on the schema and then import that into your solution.</span></span> <span data-ttu-id="60bd4-172">Cela n’est plus possible.</span><span class="sxs-lookup"><span data-stu-id="60bd4-172">This is no longer supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="60bd4-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60bd4-173">See Also</span></span>

[<span data-ttu-id="60bd4-174">Configurer les définitions d’échange de données</span><span class="sxs-lookup"><span data-stu-id="60bd4-174">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="60bd4-175">Exporter des paiements vers un fichier bancaire</span><span class="sxs-lookup"><span data-stu-id="60bd4-175">Export Payments to a Bank File</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[<span data-ttu-id="60bd4-176">Recouvrement de paiements par prélèvement automatique SEPA</span><span class="sxs-lookup"><span data-stu-id="60bd4-176">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="60bd4-177">À propos de l’infrastructure d’échange de données</span><span class="sxs-lookup"><span data-stu-id="60bd4-177">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  
