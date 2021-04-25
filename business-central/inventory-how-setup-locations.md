---
title: Configurer une fiche magasin et définir des acheminements de transfert| Microsoft Docs
description: Vous créez une fiche magasin pour chaque emplacement où vous stockez des articles d’inventaire, par exemple, un entrepôt ou un centre de distribution, et configurez des acheminements pour le transfert d’articles entre magasins.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5017df2ba46ba81884b2e99e3ea4a1bb983ea681
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785817"
---
# <a name="set-up-locations"></a><span data-ttu-id="1a24e-103">Configurer des magasins</span><span class="sxs-lookup"><span data-stu-id="1a24e-103">Set Up Locations</span></span>
<span data-ttu-id="1a24e-104">Si vous achetez, enregistrez, ou vendez des articles à plusieurs magasins ou entrepôt, vous devez spécifier chaque magasin avec une fiche magasin et définir des acheminements transfert.</span><span class="sxs-lookup"><span data-stu-id="1a24e-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="1a24e-105">Vous pouvez ensuite créer des lignes de document pour un magasin spécifique, voir la disponibilité par magasin, et transférer le stock entre magasins.</span><span class="sxs-lookup"><span data-stu-id="1a24e-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="1a24e-106">Pour plus d’informations, reportez-vous à [Gestion du stock](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="1a24e-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="to-create-a-location-card"></a><span data-ttu-id="1a24e-107">Pour créer une fiche magasin</span><span class="sxs-lookup"><span data-stu-id="1a24e-107">To create a location card</span></span>
1. <span data-ttu-id="1a24e-108">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Magasins**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="1a24e-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="1a24e-109">Sélectionnez l’action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="1a24e-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="1a24e-110">Sur la page **Fiche magasin**, renseignez les champs comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1a24e-110">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="1a24e-111">Répétez les étapes 2 et 3 pour chaque magasin dans lequel vous souhaitez conserver le stock.</span><span class="sxs-lookup"><span data-stu-id="1a24e-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="1a24e-112">De nombreux champs de la fiche magasin se rapportent à la gestion des articles dans les processus enlogement et désenlogement.</span><span class="sxs-lookup"><span data-stu-id="1a24e-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="1a24e-113">Pour plus d’informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="1a24e-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="1a24e-114">Pour créer un acheminement transfert</span><span class="sxs-lookup"><span data-stu-id="1a24e-114">To create a transfer route</span></span>
1. <span data-ttu-id="1a24e-115">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Acheminements transfert**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="1a24e-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="1a24e-116">Sinon, à partir de n’importe quelle page **Fiche magasin**, cliquez sur **Acheminements transfert**.</span><span class="sxs-lookup"><span data-stu-id="1a24e-116">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="1a24e-117">Sélectionnez l’action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="1a24e-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="1a24e-118">Sur la page **Fiche magasin**, renseignez les champs comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1a24e-118">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="1a24e-119">Vous pouvez à présent transférer des articles en stock entre deux magasins.</span><span class="sxs-lookup"><span data-stu-id="1a24e-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="1a24e-120">Pour plus d’informations, voir [Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="1a24e-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="1a24e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a24e-121">See Also</span></span>
[<span data-ttu-id="1a24e-122">Gestion du stock</span><span class="sxs-lookup"><span data-stu-id="1a24e-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="1a24e-123">[Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="1a24e-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="1a24e-124">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1a24e-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="1a24e-125">Modifier les fonctionnalités affichées</span><span class="sxs-lookup"><span data-stu-id="1a24e-125">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="1a24e-126">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="1a24e-126">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]