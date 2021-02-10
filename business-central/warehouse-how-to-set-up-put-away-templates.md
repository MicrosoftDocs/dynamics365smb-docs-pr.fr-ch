---
title: Comment configurer des modèles rangement | Microsoft Docs
description: A l’aide de la fonctionnalité de prélèvement et de rangement suggérés, l’emplacement le mieux approprié à vos articles à un moment donné est suggéré, en fonction du modèle rangement configuré pour l’entrepôt, des priorités affectées aux emplacements et des quantités minimale et maximale définies pour les emplacements associés.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b2f31804dace5371da17a4c6e1eeaaac24815c6f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755951"
---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="46c34-103">Configurer des modèles rangement</span><span class="sxs-lookup"><span data-stu-id="46c34-103">Set Up Put-away Templates</span></span>

<span data-ttu-id="46c34-104">A l’aide de la fonctionnalité de prélèvement et de rangement suggérés, l’emplacement le mieux approprié à vos articles à un moment donné est suggéré, en fonction du modèle rangement configuré pour l’entrepôt, des priorités affectées aux emplacements et des quantités minimale et maximale définies pour les emplacements associés.</span><span class="sxs-lookup"><span data-stu-id="46c34-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="46c34-105">Vous pouvez configurer un certain nombre de modèles rangement et en sélectionner un pour gérer les rangements dans votre entrepôt.</span><span class="sxs-lookup"><span data-stu-id="46c34-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="46c34-106">Vous pouvez également sélectionner un modèle rangement pour un article ou un point de stock disposant d’exigences spéciales en matière de rangement.</span><span class="sxs-lookup"><span data-stu-id="46c34-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="46c34-107">Pour configurer des modèles rangement</span><span class="sxs-lookup"><span data-stu-id="46c34-107">To set up put-away templates</span></span>

1. <span data-ttu-id="46c34-108">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Modèles rangement**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="46c34-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="46c34-109">Sélectionnez l’action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="46c34-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="46c34-110">Entrez un code représentant l’identifiant unique du modèle que vous allez créer.</span><span class="sxs-lookup"><span data-stu-id="46c34-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4. <span data-ttu-id="46c34-111">Saisissez éventuellement une brève description.</span><span class="sxs-lookup"><span data-stu-id="46c34-111">Enter a short description, if you wish.</span></span>  
5. <span data-ttu-id="46c34-112">Renseignez la première ligne avec les exigences emplacement auxquelles vous souhaitez qu’il soit répondu d’abord lors de la proposition d’un rangement.</span><span class="sxs-lookup"><span data-stu-id="46c34-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>

    <span data-ttu-id="46c34-113">Par exemple, si vous souhaitez que la méthode de rangement par défaut soit basée sur des emplacements fixes, choisissez le champ **Rechercher empl. statique**.</span><span class="sxs-lookup"><span data-stu-id="46c34-113">For example, if want the default put-away method to be based on fixed bins, then choose the **Find Fixed Bin** field.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="46c34-114">Renseignez la deuxième ligne avec les exigences emplacement auxquelles on doit répondre ensuite lors de la recherche d’un emplacement de rangement.</span><span class="sxs-lookup"><span data-stu-id="46c34-114">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="46c34-115">La deuxième ligne est utilisée uniquement si un emplacement répondant aux exigences de la première ligne ne peut être trouvé.</span><span class="sxs-lookup"><span data-stu-id="46c34-115">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7. <span data-ttu-id="46c34-116">Continuez à renseigner les lignes jusqu’à ce que vous ayez décrit tous les placements acceptables à utiliser au cours du rangement.</span><span class="sxs-lookup"><span data-stu-id="46c34-116">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8. <span data-ttu-id="46c34-117">Sur la dernière ligne du modèle rangement, cochez la case **Rechercher empl. Dynamique**.</span><span class="sxs-lookup"><span data-stu-id="46c34-117">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="46c34-118">Vous pouvez créer plusieurs modèles rangement et les appliquer comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="46c34-118">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="46c34-119">On se réfère d’abord au modèle rangement sélectionné éventuel pour l’article ou le point de stock.</span><span class="sxs-lookup"><span data-stu-id="46c34-119">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="46c34-120">Si ces champs ne sont pas renseignés, alors le modèle rangement sélectionné pour l’entrepôt sur le raccourci **Config. emplacement** de la fiche magasin sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="46c34-120">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="46c34-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46c34-121">See Also</span></span>

[<span data-ttu-id="46c34-122">Gestion d’entrepôt</span><span class="sxs-lookup"><span data-stu-id="46c34-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="46c34-123">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="46c34-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="46c34-124">Configuration de la gestion des entrepôts</span><span class="sxs-lookup"><span data-stu-id="46c34-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="46c34-125">Gestion des assemblages</span><span class="sxs-lookup"><span data-stu-id="46c34-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="46c34-126">Détails de conception : gestion d’entrepôt</span><span class="sxs-lookup"><span data-stu-id="46c34-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="46c34-127">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="46c34-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
