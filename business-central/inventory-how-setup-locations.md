---
title: Configurer une fiche magasin et définir des acheminements de transfert
description: Vous créez une fiche magasin pour chaque emplacement où vous stockez des articles d’inventaire, par exemple, un entrepôt ou un centre de distribution, et configurez des acheminements pour le transfert d’articles entre magasins.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184339"
---
# <a name="set-up-locations"></a><span data-ttu-id="dcbf3-103">Configurer des magasins</span><span class="sxs-lookup"><span data-stu-id="dcbf3-103">Set Up Locations</span></span>

<span data-ttu-id="dcbf3-104">Si vous achetez, enregistrez, ou vendez des articles à plusieurs magasins ou entrepôt, vous devez configurer chaque magasin avec une fiche magasin et définir des acheminements transfert.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-104">If you buy, store, or sell items at more than one place or warehouse, you must set up each location with a location card and define transfer routes.</span></span> <span data-ttu-id="dcbf3-105">[!INCLUDE [prod_short](includes/prod_short.md)] utilise des magasins pour aider à suivre les stocks dans les cas les plus simples et dans les processus d’entrepôt plus complexes.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-105">[!INCLUDE [prod_short](includes/prod_short.md)] uses locations to help keep track of inventory in both simpler cases and the more complex warehouse processes.</span></span>

<span data-ttu-id="dcbf3-106">Vous pouvez ensuite créer des lignes de document pour un magasin spécifique, voir la disponibilité par magasin, et transférer le stock entre magasins.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-106">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="dcbf3-107">Pour plus d’informations, reportez-vous à [Gestion du stock](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="dcbf3-107">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a><span data-ttu-id="dcbf3-108">Fiches magasin</span><span class="sxs-lookup"><span data-stu-id="dcbf3-108">Location cards</span></span>

<span data-ttu-id="dcbf3-109">La fiche magasin spécifie des informations sur un magasin, par exemple un entrepôt ou un centre de distribution.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-109">The location card specifies information about a location, such as a warehouse or distribution center.</span></span> <span data-ttu-id="dcbf3-110">Affectez un nom et un code représentatifs à chaque magasin.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-110">You give each location a name and a code that represents the location.</span></span> <span data-ttu-id="dcbf3-111">Il vous suffit ensuite de saisir le code magasin dans d’autres parties du programme lorsque vous souhaitez enregistrer les transactions d’un magasin en particulier.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-111">You can then enter the location code in other parts of the program when you want to record transactions for a given location.</span></span>  

<span data-ttu-id="dcbf3-112">Vous pouvez entrer des informations sur les emplacements et les règles entrepôt pour chaque magasin.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-112">You can enter information about bins and warehouse policies for each location.</span></span> <span data-ttu-id="dcbf3-113">En fonction des règles entrepôt sélectionnées, vous pouvez utiliser les options du raccourci **Emplacements** pour définir les emplacements utilisés par défaut lorsque vous effectuez des transactions.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-113">Based on the warehouse policies you select, you can use the options on the **Bins** FastTab to define the bins that will be used as default bins when you are performing transactions.</span></span> <span data-ttu-id="dcbf3-114">Si vous utilisez les prélèvement et rangement suggérés, vous pouvez utiliser la plupart des options du raccourci **Config. emplacement** pour définir la façon dont vous souhaitez utiliser les différentes fonctions d’entrepôt avancées.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-114">If you are using directed put-away and pick, you use most of the options on the **Bin Policies** FastTab to define how you would like to use the various advanced warehousing features.</span></span>  

<span data-ttu-id="dcbf3-115">Certains champs d’option sont grisés et désactivés par d’autres paramètres dans la page **Fiche magasin** pour limiter les combinaisons de paramètres non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-115">Some option fields are grayed and disabled by other settings in the **Location Card** page to restrict unsupported setup combinations.</span></span>  

<span data-ttu-id="dcbf3-116">Choisissez les actions **Zones** ou **Emplacements** pour visualiser des informations sur les zones et les emplacements qui peuvent être définis pour le magasin.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-116">Choose the **Zones** or **Bins** action to view information about zones and bins that may be defined for the location.</span></span>

### <a name="to-create-a-location-card"></a><span data-ttu-id="dcbf3-117">Pour créer une fiche magasin</span><span class="sxs-lookup"><span data-stu-id="dcbf3-117">To create a location card</span></span>

1. <span data-ttu-id="dcbf3-118">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Magasins**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="dcbf3-119">Sélectionnez l’action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-119">Choose the **New** action.</span></span>
3. <span data-ttu-id="dcbf3-120">Sur la page **Fiche magasin**, renseignez les champs comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-120">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="dcbf3-121">Répétez les étapes 2 et 3 pour chaque magasin dans lequel vous souhaitez conserver le stock.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-121">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="dcbf3-122">De nombreux champs de la fiche magasin se rapportent à la gestion des articles dans les processus enlogement et désenlogement.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-122">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="dcbf3-123">Les champs ne sont pas pertinents pour les entreprises qui n’ont pas besoin des fonctionnalités d’entrepôt plus complexes.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-123">The fields are not relevant for companies that do not require the more complex warehouse functionality.</span></span> <span data-ttu-id="dcbf3-124">Pour plus d’informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="dcbf3-124">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="dcbf3-125">Vous pouvez modifier la configuration d’un magasin ultérieurement, mais vous ne pouvez pas modifier la configuration des magasins qui ont des écritures comptables article.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-125">You can change the configuration of a location later, but you cannot edit the setup of locations that have item ledger entries.</span></span>  

<span data-ttu-id="dcbf3-126">Ensuite, si vous avez plusieurs magasins, vous pouvez définir des acheminements transfert entre les magasins.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-126">Next, if you have multiple locations, you can define transfer routes between locations.</span></span>  

### <a name="to-create-a-transfer-route"></a><span data-ttu-id="dcbf3-127">Pour créer un acheminement transfert</span><span class="sxs-lookup"><span data-stu-id="dcbf3-127">To create a transfer route</span></span>

1. <span data-ttu-id="dcbf3-128">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Acheminements transfert**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="dcbf3-129">Sinon, à partir de n’importe quelle page **Fiche magasin**, cliquez sur **Acheminements transfert**.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-129">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="dcbf3-130">Sélectionnez l’action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-130">Choose the **New** action.</span></span>
4. <span data-ttu-id="dcbf3-131">Sur la page **Fiche magasin**, renseignez les champs comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-131">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="dcbf3-132">Vous pouvez à présent transférer des articles en stock entre deux magasins.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-132">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="dcbf3-133">Pour plus d’informations, voir [Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="dcbf3-133">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="bins"></a><span data-ttu-id="dcbf3-134">Emplacements</span><span class="sxs-lookup"><span data-stu-id="dcbf3-134">Bins</span></span>

<span data-ttu-id="dcbf3-135">Les emplacements représentent la structure d’entrepôt de base et sont utilisés pour faire des propositions relatives à l’emplacement des articles.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-135">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="dcbf3-136">Lorsque vous avez créé vos emplacements, vous pouvez définir précisément le contenu que vous souhaitez placer dans chacun d’entre eux, ou l’emplacement peut être utilisé en tant qu’emplacement dynamique sans contenu spécifié.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-136">When you have created your bins, you can define precisely the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span> <span data-ttu-id="dcbf3-137">Les emplacements sont principalement utilisés dans les opérations d’entrepôt de base et avancées.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-137">Bins are predominantly used in basic and advance warehouse operations.</span></span> <span data-ttu-id="dcbf3-138">Si vous gérez les stocks dans une configuration plus simple, vous n’avez probablement pas besoin d’emplacements.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-138">If you manage inventory in a more simple setup, you probably do not need bins.</span></span>

<span data-ttu-id="dcbf3-139">Pour utiliser la fonctionnalité d’emplacement liée au magasin, vous devez d’abord activer la fonctionnalité sur la fiche **magasin** en sélectionnant le champ **Emplacement obligatoire** sur le raccourci **Entrepôt**.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-139">To use the bin functionality at a location, you first activate the functionality on the **Location** card by selecting the **Bins Mandatory** field on the **Warehouse** FastTab.</span></span> <span data-ttu-id="dcbf3-140">Ensuite, vous définissez la circulation des articles dans le magasin en spécifiant les codes emplacement dans les champs de configuration qui représentent les différents flux.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-140">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>

> [!NOTE]
> <span data-ttu-id="dcbf3-141">Avant de pouvoir spécifier les codes emplacement sur la fiche magasin, il convient de les créer.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-141">Before you can specify bin codes on the location card, the bin codes must be created.</span></span>

<span data-ttu-id="dcbf3-142">Pour plus d’informations, voir [Créer des emplacements](warehouse-how-to-create-individual-bins.md) et [Configurer des types d’emplacement](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="dcbf3-142">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md) and [Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

## <a name="zones"></a><span data-ttu-id="dcbf3-143">Zones</span><span class="sxs-lookup"><span data-stu-id="dcbf3-143">Zones</span></span>

<span data-ttu-id="dcbf3-144">Si vous souhaitez structurer vos emplacements en zones, vous pouvez le faire dans la page **Zones**.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-144">If you want to structure your bins under zones, you can do that in the **Zones** page.</span></span>

<span data-ttu-id="dcbf3-145">[!INCLUDE [prod_short](includes/prod_short.md)] copie les champs que vous définissez pour une zone donnée dans les emplacements qui s’y trouvent.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-145">[!INCLUDE [prod_short](includes/prod_short.md)] copies the fields that you set for any particular zone to the bins within it.</span></span> <span data-ttu-id="dcbf3-146">Cela signifie que vous pouvez affecter une zone à un emplacement ou à un modèle d’emplacement (filtre de création d’emplacement) et que plusieurs autres champs sont ensuite renseignés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-146">This way, you can assign a zone to a bin or a bin template (bin creation filter), and several other fields are then filled in automatically.</span></span>

<span data-ttu-id="dcbf3-147">Toutefois, vous pouvez choisir de configurer une seule zone et d’organiser votre entrepôt uniquement en fonction des emplacements.</span><span class="sxs-lookup"><span data-stu-id="dcbf3-147">However, you can choose to set up just one zone and to organize your warehouse according to bins alone.</span></span> <span data-ttu-id="dcbf3-148">Pour plus d’informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="dcbf3-148">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="dcbf3-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcbf3-149">See Also</span></span>

[<span data-ttu-id="dcbf3-150">Gestion du stock</span><span class="sxs-lookup"><span data-stu-id="dcbf3-150">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="dcbf3-151">Transfert de stock entre des magasins</span><span class="sxs-lookup"><span data-stu-id="dcbf3-151">Transfer Inventory Between Locations</span></span>](inventory-how-transfer-between-locations.md)  
[<span data-ttu-id="dcbf3-152">Créer emplacements</span><span class="sxs-lookup"><span data-stu-id="dcbf3-152">Create Bins</span></span>](warehouse-how-to-create-individual-bins.md)  
[<span data-ttu-id="dcbf3-153">Configurer des types d’emplacement</span><span class="sxs-lookup"><span data-stu-id="dcbf3-153">Set Up Bin Types</span></span>](warehouse-how-to-set-up-bin-types.md)  
[<span data-ttu-id="dcbf3-154">Configuration de la gestion des entrepôts</span><span class="sxs-lookup"><span data-stu-id="dcbf3-154">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
<span data-ttu-id="dcbf3-155">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dcbf3-155">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="dcbf3-156">Modifier les fonctionnalités affichées</span><span class="sxs-lookup"><span data-stu-id="dcbf3-156">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="dcbf3-157">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="dcbf3-157">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]