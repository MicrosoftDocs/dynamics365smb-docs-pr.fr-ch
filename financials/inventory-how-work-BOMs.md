---
title: "Utiliser les nomenclatures pour gérer les composants| Microsoft Docs"
description: "Vous créez une nomenclature d'assemblage pour spécifier les composants ou ressources nécessaires pour monter l'article que la nomenclature d'assemblage représente, et vous pouvez afficher les composants d'un élément d'assemblage."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-bills-of-material"></a><span data-ttu-id="4f197-103">Procédure : utiliser les nomenclatures</span><span class="sxs-lookup"><span data-stu-id="4f197-103">How to: Work with Bills of Material</span></span>
> [!NOTE]  
>   <span data-ttu-id="4f197-104">La version actuelle de [!INCLUDE[d365fin](includes/d365fin_md.md)] contient uniquement la première partie de la fonction Gestion des assemblages.</span><span class="sxs-lookup"><span data-stu-id="4f197-104">The current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the first part of the Assembly Management feature.</span></span> <span data-ttu-id="4f197-105">Pour le moment, vous pouvez uniquement créer des nomenclatures d'assemblage et gérer les articles parents associés comme des articles en stock normaux.</span><span class="sxs-lookup"><span data-stu-id="4f197-105">For now, you can only create assembly BOMs and then handle the related parent items as normal inventory items.</span></span> <span data-ttu-id="4f197-106">Dans une mise à jour future, vous pourrez gérer l'assemblage réel des articles à partir des composants, dans les flux Assembler pour stock ou Assembler pour commande, et vous pourrez vendre des composants comme kits.</span><span class="sxs-lookup"><span data-stu-id="4f197-106">In a future update, you can manage the actual assembly of items from components, either in assemble-to-stock or assemble-to-order flows, and you can sell components as kits.</span></span>

<span data-ttu-id="4f197-107">Les nomenclatures permettent de structurer les articles parents que vous vendez sous forme de kits constitués des composants du parent ou que vous assemblez pour commande ou stock.</span><span class="sxs-lookup"><span data-stu-id="4f197-107">You use bills of materials (BOMs) to structure parent items that you sell as kits consisting of the parent's components or that you assemble to order or to stock.</span></span>

<span data-ttu-id="4f197-108">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], une nomenclature est appelée une « nomenclature d'assemblage ».</span><span class="sxs-lookup"><span data-stu-id="4f197-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], a bill of materials is referred to as an "assembly BOM".</span></span> <span data-ttu-id="4f197-109">Les nomenclatures d'assemblage spécifient les composants contenus dans les articles parents.</span><span class="sxs-lookup"><span data-stu-id="4f197-109">Assembly BOMs specify which components are contained in parent items.</span></span> <span data-ttu-id="4f197-110">Dans cette documentation, un article parent est appelé un « article d'assemblage ».</span><span class="sxs-lookup"><span data-stu-id="4f197-110">In this documentation, a parent item is referred to as an "assembly item".</span></span>

<span data-ttu-id="4f197-111">Les nomenclatures d'assemblage contiennent généralement des articles mais peuvent également contenir une ou plusieurs ressources requises pour regrouper les articles d'assemblage.</span><span class="sxs-lookup"><span data-stu-id="4f197-111">Assembly BOMs usually contain items but can also contain one or more resources that are required to put the assembly item together.</span></span>

<span data-ttu-id="4f197-112">Les nomenclatures d'assemblage peuvent être multi-niveaux, ce qui signifie qu'un composant de la nomenclature d'assemblage peut être un élément d'assemblage proprement dit.</span><span class="sxs-lookup"><span data-stu-id="4f197-112">Assembly BOMs can have multiple levels, which means that a component on the assembly BOM can be an assembly item itself.</span></span> <span data-ttu-id="4f197-113">Dans ce cas, le champ **Nomencl d'élément d'assemblage** de la ligne nomenclature d'assemblage contient **Oui**.</span><span class="sxs-lookup"><span data-stu-id="4f197-113">In that case, the **Assembly BOM** field on the assembly BOM line contains **Yes**.</span></span>

<span data-ttu-id="4f197-114">Des exigences spécifiques s'appliquent aux articles des nomenclatures d'assemblage en ce qui concerne la disponibilité.</span><span class="sxs-lookup"><span data-stu-id="4f197-114">Special requirements apply to items on assembly BOMs with regards to availability.</span></span> <span data-ttu-id="4f197-115">Pour plus d'informations, reportez-vous à la section « Pour afficher la disponibilité d'un article en fonction de son utilisation dans les nomenclatures d'assemblage » dans [Procédure : voir la disponibilité des articles](inventory-how-availability-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4f197-115">For more information, see the "To see the availability of an item by its use in assembly BOMs" section in [How to: View the Availability of Items](inventory-how-availability-overview.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="4f197-116">Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**.</span><span class="sxs-lookup"><span data-stu-id="4f197-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="4f197-117">Pour plus d'informations, voir [Personnalisation de votre expérience Financials](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="4f197-117">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>

## <a name="to-create-an-assembly-bom"></a><span data-ttu-id="4f197-118">Pour créer une nomenclature d'assemblage</span><span class="sxs-lookup"><span data-stu-id="4f197-118">To create an assembly BOM</span></span>
<span data-ttu-id="4f197-119">Pour définir un article parent constitué d'autres articles, et potentiellement des ressources nécessaires pour regrouper les articles parents, vous devez créer une nomenclature d'assemblage.</span><span class="sxs-lookup"><span data-stu-id="4f197-119">To define a parent item that consists of other items, and potentially of resources required to put the parent together, you must create an assembly BOM.</span></span>  

<span data-ttu-id="4f197-120">Il y a deux parties pour créer une nomenclature d'assemblage :</span><span class="sxs-lookup"><span data-stu-id="4f197-120">There are two parts to creating an assembly BOM:</span></span>
- <span data-ttu-id="4f197-121">Configuration d'un nouvel article</span><span class="sxs-lookup"><span data-stu-id="4f197-121">Setting up a new item</span></span>
- <span data-ttu-id="4f197-122">Définition de la structure de la nomenclature de l'article d'assemblage.</span><span class="sxs-lookup"><span data-stu-id="4f197-122">Defining the BOM structure of the assembly item.</span></span>

1. <span data-ttu-id="4f197-123">Configurez un nouvel article.</span><span class="sxs-lookup"><span data-stu-id="4f197-123">Set up a new item.</span></span> <span data-ttu-id="4f197-124">Pour plus d'informations, reportez vous à [Procédure : enregistrer de nouveaux articles](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="4f197-124">For more information, see [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

    <span data-ttu-id="4f197-125">Entrez maintenant les composants ou les ressources de la nomenclature d'assemblage.</span><span class="sxs-lookup"><span data-stu-id="4f197-125">Proceed to enter components or resources on the assembly BOM.</span></span>  
2. <span data-ttu-id="4f197-126">Dans la fenêtre **Fiche article** d'un article d'assemblage, sélectionnez l'action **Assemblage**, puis l'action **Nomencl d'élément d'assemblage**.</span><span class="sxs-lookup"><span data-stu-id="4f197-126">In the **Item Card** window for an assembly item, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
3. <span data-ttu-id="4f197-127">Dans la fenêtre **Nomencl d'élément d'assemblage**, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="4f197-127">In the **Assembly BOM** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a><span data-ttu-id="4f197-128">Pour afficher les composants d'un article d'assemblage indenté selon la structure de la nomenclature</span><span class="sxs-lookup"><span data-stu-id="4f197-128">To view the components of an assembly item indented according to the BOM structure</span></span>
<span data-ttu-id="4f197-129">Dans la fenêtre **Nomencl d'élément d'assemblage**, vous pouvez ouvrir une fenêtre distincte qui affiche les composants et les ressources indentés selon la position de leur nomenclature sous l'article d'assemblage.</span><span class="sxs-lookup"><span data-stu-id="4f197-129">From the **Assembly BOM** window, you can open a separate window that shows the components and any resources indented according to their BOM position under the assembly item.</span></span>

1. <span data-ttu-id="4f197-130">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="4f197-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="4f197-131">Ouvrez la fiche d'un article d'assemblage.</span><span class="sxs-lookup"><span data-stu-id="4f197-131">Open the card for an assembly item.</span></span> <span data-ttu-id="4f197-132">(Le champ **Nomencl d'élément d'assemblage** dans la fenêtre **Articles** contient **Oui**.)</span><span class="sxs-lookup"><span data-stu-id="4f197-132">(The **Assembly BOM** field in the **Items** window contains **Yes**.)</span></span>
3. <span data-ttu-id="4f197-133">Dans la fenêtre **Fiche article**, sélectionnez l'action **Assemblage**, puis l'action **Nomencl d'élément d'assemblage**.</span><span class="sxs-lookup"><span data-stu-id="4f197-133">In the **Item Card** window, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
4. <span data-ttu-id="4f197-134">Dans la fenêtre **Nomencl d'élément d'assemblage**, sélectionnez l'action **Afficher nomenclature**.</span><span class="sxs-lookup"><span data-stu-id="4f197-134">In the **Assembly BOM** window, choose the **Show BOM** action.</span></span>

## <a name="to-buy-sell-or-transfer-assembly-items"></a><span data-ttu-id="4f197-135">Pour acheter, vendre ou transférer des articles d'assemblage</span><span class="sxs-lookup"><span data-stu-id="4f197-135">To buy, sell, or transfer assembly items</span></span>
<span data-ttu-id="4f197-136">Comme la version actuelle de [!INCLUDE[d365fin](includes/d365fin_md.md)] permet uniquement de définir et d'affecter des nomenclatures d'assemblage aux articles, vous pouvez gérer les articles d'assemblage des lignes document comme des articles normaux uniquement.</span><span class="sxs-lookup"><span data-stu-id="4f197-136">Because the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the ability to define and assign assembly BOMs to items, you can handle assembly items on document lines as normal items only.</span></span>

<span data-ttu-id="4f197-137">**Attention** : la quantité en stock des composants de nomenclature ne sera pas ajustée dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="4f197-137">**Caution**: The inventory quantity of BOM components will not be adjusted if you do so.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f197-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f197-138">See Also</span></span>
[<span data-ttu-id="4f197-139">Procédure : enregistrer de nouveaux articles</span><span class="sxs-lookup"><span data-stu-id="4f197-139">How to: Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="4f197-140">[Procédure : voir la disponibilité des articles](inventory-how-availability-overview.md)   </span><span class="sxs-lookup"><span data-stu-id="4f197-140">[How to: View the Availability of Items](inventory-how-availability-overview.md)   </span></span>  
[<span data-ttu-id="4f197-141">Stock</span><span class="sxs-lookup"><span data-stu-id="4f197-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="4f197-142">[Utilisation de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4f197-142">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>

