---
title: Rupture de charge automatique avec prélèvement et rangement dirigé | Microsoft Docs
description: En cas d'utilisation d'un prélèvement et d'un rangement suggérés dans les entrepôts, vous pouvez diviser une unité en unités plus petites lors de la création des instructions entrepôt répondant aux exigences de documents origine, d'ordres de fabrication ou de prélèvements et de rangements internes.
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
ms.openlocfilehash: c328df334d1bb1be33ced814677c3ef3ea634799
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821041"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><span data-ttu-id="bedfc-103">Activer la rupture de charge automatique avec prélèvement et rangement dirigé</span><span class="sxs-lookup"><span data-stu-id="bedfc-103">Enable Automatic Breaking Bulk with Directed Put-away and Pick</span></span>
<span data-ttu-id="bedfc-104">En cas d'utilisation d'un prélèvement et d'un rangement suggérés dans les entrepôts, [!INCLUDE[d365fin](includes/d365fin_md.md)] peut procéder, dans de nombreux cas, à un déconditionnement automatique (division d'une unité en unités plus petites) lorsqu'il crée des instructions entrepôt répondant aux exigences de documents origine, d'ordres de fabrication ou de prélèvements et de rangements internes.</span><span class="sxs-lookup"><span data-stu-id="bedfc-104">For locations that use directed put-away and pick, [!INCLUDE[d365fin](includes/d365fin_md.md)] can, in various situations, automatically breakbulk, that is, break a larger unit of measure into smaller units of measure, when it creates warehouse instructions that fulfill the needs of source documents, production orders, or internal picks and put-aways.</span></span> <span data-ttu-id="bedfc-105">Parfois, le déconditionnement peut également nécessiter le regroupement de petites unités afin de répondre à des demandes sortantes en divisant l'unité la plus grande du document origine ou de l'ordre de fabrication en unités plus petites disponibles dans l'entrepôt.</span><span class="sxs-lookup"><span data-stu-id="bedfc-105">To breakbulk sometimes also means gathering smaller units of measure, if necessary, to meet outbound requests by breaking the larger unit of measure on the source document or production order into the smaller units of measure that are available in the warehouse.</span></span>   

## <a name="breakbulking-in-picks"></a><span data-ttu-id="bedfc-106">Déconditionnement pour prélèvement</span><span class="sxs-lookup"><span data-stu-id="bedfc-106">Breakbulking in Picks</span></span>  
<span data-ttu-id="bedfc-107">Pour stocker des articles dans plusieurs unités et permettre de les combiner automatiquement selon vos besoins au cours du prélèvement, sélectionnez le champ **Autoriser déconditionnement** de la fiche magasin.</span><span class="sxs-lookup"><span data-stu-id="bedfc-107">If you want to store items in several different units of measure and allow them to be automatically combined as needed in the picking process, select the **Allow Breakbulk** field on the location card.</span></span>  

<span data-ttu-id="bedfc-108">Pour répondre à une tâche, le programme recherche automatiquement un article de la même unité.</span><span class="sxs-lookup"><span data-stu-id="bedfc-108">To fulfill a task, the program automatically looks for an item in the same unit of measure.</span></span> <span data-ttu-id="bedfc-109">S'il ne trouve pas ce type d'article et que vous avez sélectionné ce champ, il vous propose de diviser une unité plus grande en fonction de l'unité nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bedfc-109">But if it cannot find this form of the item, and this field is selected, the program will suggest that you break a larger unit of measure into the unit of measure that is needed.</span></span>  

<span data-ttu-id="bedfc-110">Si le système trouve uniquement des unités plus petites, il vous suggère de rassembler des articles afin de répondre à la quantité de l'expédition ou de l'ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="bedfc-110">If the system can only find smaller units of measure, it will suggest that you gather items to fulfill the quantity on the shipment or production order.</span></span> <span data-ttu-id="bedfc-111">En fait, il divise la plus grande unité du document origine en unités de prélèvement plus petites.</span><span class="sxs-lookup"><span data-stu-id="bedfc-111">In effect, it breaks the larger unit of measure on the source document into smaller units for picking.</span></span>  

## <a name="breakbulking-in-put-aways"></a><span data-ttu-id="bedfc-112">Déconditionnement pour rangement</span><span class="sxs-lookup"><span data-stu-id="bedfc-112">Breakbulking in Put-aways</span></span>  
<span data-ttu-id="bedfc-113">Au niveau du rangement de l'entrepôt, le programme propose automatiquement des lignes action Emplacement dans l'unité de rangement, par exemple, pièces, même si les articles arrivent dans une unité différente.</span><span class="sxs-lookup"><span data-stu-id="bedfc-113">In the warehouse put-away, the program automatically suggests Place action lines in the put-away unit of measure, for example, pieces, even though the items arrive in a different unit of measure.</span></span>  

## <a name="breakbulking-in-movements"></a><span data-ttu-id="bedfc-114">Déconditionnement pour mouvement</span><span class="sxs-lookup"><span data-stu-id="bedfc-114">Breakbulking in Movements</span></span>  
<span data-ttu-id="bedfc-115">le programme effectue également un déconditionnement automatique au niveau des mouvements de réapprovisionnement, si le champ **Autoriser déconditionnement** est sélectionné sur le raccourci **Option** de la page **Calculer réappro. emplacement**.</span><span class="sxs-lookup"><span data-stu-id="bedfc-115">The program also breakbulks automatically in replenishment movements, if the **Allow Breakbulk** field is selected on the **Option** FastTab on the **Calculate Bin Replenishment** page.</span></span>  

<span data-ttu-id="bedfc-116">Vous pouvez afficher les résultats de la conversion entre deux unités sous forme de lignes déconditionnement intermédiaire dans les instructions rangement, prélèvement, ou mouvement.</span><span class="sxs-lookup"><span data-stu-id="bedfc-116">You can view the results of the conversion process from one unit of measure to another as intermediate breakbulk lines in the put-away, pick, or movement instructions.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bedfc-117">Si vous sélectionnez le champ **Paramétrer filtre déconditionnement** dans l'en-tête instruction entrepôt, le programme masque les lignes déconditionnement chaque fois que la plus grande unité est utilisée dans son intégralité.</span><span class="sxs-lookup"><span data-stu-id="bedfc-117">If you select the **Set Breakbulk Filter** field on the warehouse instruction header, the program will hide the breakbulk lines whenever the larger unit of measure is going to be completely used.</span></span> <span data-ttu-id="bedfc-118">Par exemple, si une palette comprend 12 pièces et que vous allez utiliser les 12 pièces, le prélèvement vous indique de prendre 1 palette et d'y placer les 12 pièces.</span><span class="sxs-lookup"><span data-stu-id="bedfc-118">For example, if a pallet is 12 pieces and you are going to use all 12 pieces, the pick will then direct you to take 1 pallet and place 12 pieces.</span></span> <span data-ttu-id="bedfc-119">Par contre, si vous ne devez prélever que 9 pièces, les lignes déconditionnement ne sont pas masquées, même si vous avez sélectionné le champ **Filtre déconditionnement**, étant donné que vous devez placer les trois pièces restantes dans un autre endroit de l'entrepôt.</span><span class="sxs-lookup"><span data-stu-id="bedfc-119">However, if you have to pick only 9 pieces, then the breakbulk lines will not be hidden, even if you have selected the **Breakbulk Filter** field, because you have to place the remaining three pieces somewhere in the warehouse.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bedfc-120">Pour optimiser l'utilisation des unités dans l'entrepôt (également avec la fonctionnalité de déconditionnement), effectuez dès que vous le pouvez les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="bedfc-120">If you want your units of measure to perform optimally in the warehouse, also in connection with the breakbulk functionality, you should wherever possible try to:</span></span>  
>   
> - <span data-ttu-id="bedfc-121">Configurez l'unité de base d'un article en tant que plus petite unité à gérer dans les processus concernant l'entrepôt.</span><span class="sxs-lookup"><span data-stu-id="bedfc-121">Set up the base unit of measure for an item as the smallest unit of measure that you expect to handle in your warehouse processes.</span></span>  
> - <span data-ttu-id="bedfc-122">Configurez les autres unités de l'article en tant que multiples de l'unité de base.</span><span class="sxs-lookup"><span data-stu-id="bedfc-122">Set up your alternative units of measure for the item as multiples of the base unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bedfc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bedfc-123">See Also</span></span>  
[<span data-ttu-id="bedfc-124">Gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="bedfc-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="bedfc-125">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="bedfc-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="bedfc-126">[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="bedfc-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="bedfc-127">[Gestion des assemblages](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="bedfc-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="bedfc-128">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="bedfc-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="bedfc-129">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bedfc-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
