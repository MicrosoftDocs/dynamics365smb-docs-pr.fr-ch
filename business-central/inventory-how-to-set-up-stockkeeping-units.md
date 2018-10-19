---
title: "Procédure de configuration des points de stock | Microsoft Docs"
description: "Vous pouvez utiliser des points de stock pour enregistrer des informations relatives à vos articles pour un code magasin ou variante donné."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 3c368af3347c72f2cf355876ed5574151095f993
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="399d9-103">Configurer des points de stock</span><span class="sxs-lookup"><span data-stu-id="399d9-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="399d9-104">Vous pouvez utiliser des points de stock pour enregistrer des informations relatives à vos articles pour un code magasin ou variante donné.</span><span class="sxs-lookup"><span data-stu-id="399d9-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="399d9-105">Les points de stock représentent un supplément des fiches article.</span><span class="sxs-lookup"><span data-stu-id="399d9-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="399d9-106">Ils ne les remplacent pas, bien qu'ils soient liés à ces documents.</span><span class="sxs-lookup"><span data-stu-id="399d9-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="399d9-107">Les points de stock vous permettent de différencier des informations relatives à un article pour un magasin donné, comme un entrepôt ou un centre de distribution, ou une variante donnée, comme plusieurs numéros d'étagère et plusieurs informations de réapprovisionnement, pour un même article.</span><span class="sxs-lookup"><span data-stu-id="399d9-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="399d9-108">Pour configurer un point de stock</span><span class="sxs-lookup"><span data-stu-id="399d9-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="399d9-109">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Points de stock**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="399d9-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="399d9-110">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="399d9-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="399d9-111">Renseignez les champs de la fiche.</span><span class="sxs-lookup"><span data-stu-id="399d9-111">Fill in the fields on the card.</span></span> <span data-ttu-id="399d9-112">Les champs suivants sont nécessaires : **N° article**, **Code magasin** et/ou **Code variante**.</span><span class="sxs-lookup"><span data-stu-id="399d9-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="399d9-113">Après avoir configuré le premier point de stock pour un article, la case à cocher **Point de stock** sur la fiche **Article** est activée.</span><span class="sxs-lookup"><span data-stu-id="399d9-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="399d9-114">Pour créer plusieurs points de stock pour un article, utilisez le traitement par lots **Créer point de stock**.</span><span class="sxs-lookup"><span data-stu-id="399d9-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="399d9-115">Les informations de la fiche **Point de stock** sont prioritaires par rapport à celles de la fiche **Article**.</span><span class="sxs-lookup"><span data-stu-id="399d9-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>  

## <a name="see-also"></a><span data-ttu-id="399d9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="399d9-116">See Also</span></span>  
[<span data-ttu-id="399d9-117">Enregistrer de nouveaux articles</span><span class="sxs-lookup"><span data-stu-id="399d9-117">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="399d9-118">Configuration de la gestion des entrepôts</span><span class="sxs-lookup"><span data-stu-id="399d9-118">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="399d9-119">Gestion d’entrepôt</span><span class="sxs-lookup"><span data-stu-id="399d9-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="399d9-120">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="399d9-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="399d9-121">[Gestion des assemblages](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="399d9-121">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="399d9-122">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="399d9-122">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="399d9-123">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="399d9-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

