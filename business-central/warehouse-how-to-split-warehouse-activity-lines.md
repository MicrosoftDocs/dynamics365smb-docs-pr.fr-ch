---
title: Comment répartir des lignes activité entrepôt | Microsoft Docs
description: Dans le cadre de rangements, mouvements ou prélèvements entrepôt et de rangements et prélèvements stock, des emplacements sont proposés pour le prélèvement et le rangement des articles . Il arrive parfois que la quantité réelle disponible dans l'emplacement soit insuffisante ou que l'espace de l'emplacement proposé soit insuffisant pour le rangement de la quantité nécessaire. Dans ces cas, vous devez répartir la ligne de telle sorte que les articles d'une ligne soient prélevés ou placés dans plusieurs emplacements.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f52eacb4947881391fdfcff57e32435410134287
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247760"
---
# <a name="split-warehouse-activity-lines"></a><span data-ttu-id="43aa7-105">Répartir des lignes activité entrepôt</span><span class="sxs-lookup"><span data-stu-id="43aa7-105">Split Warehouse Activity Lines</span></span>
<span data-ttu-id="43aa7-106">Dans le cadre de rangements, mouvements ou prélèvements entrepôt et de rangements et prélèvements stock, des emplacements sont proposés pour le prélèvement et le rangement des articles .</span><span class="sxs-lookup"><span data-stu-id="43aa7-106">In warehouse put-aways, movements, or picks, and in inventory put-aways and inventory picks, bins are suggested for the picking or putting away of items.</span></span> <span data-ttu-id="43aa7-107">Il arrive parfois que la quantité réelle disponible dans l'emplacement soit insuffisante ou que l'espace de l'emplacement proposé soit insuffisant pour le rangement de la quantité nécessaire.</span><span class="sxs-lookup"><span data-stu-id="43aa7-107">The actual quantity in the bin suggested may not be sufficient, or there is not enough room in the suggested bin to put away the required quantity.</span></span> <span data-ttu-id="43aa7-108">Dans ces cas, vous devez répartir la ligne de telle sorte que les articles d'une ligne soient prélevés ou placés dans plusieurs emplacements.</span><span class="sxs-lookup"><span data-stu-id="43aa7-108">In these cases, you need to split the line, so that the items for one line are either taken from or placed into more than one bin.</span></span>  

<span data-ttu-id="43aa7-109">La procédure suivante s'applique aux documents entrepôt, à savoir les lignes de rangement, de mouvement et de prélèvement entrepôt, ainsi que les lignes de rangement, de mouvement et de prélèvement stock.</span><span class="sxs-lookup"><span data-stu-id="43aa7-109">The following procedure applies to warehouse documents, such as warehouse put-away, movement, and pick lines, or inventory put-away, movement, and pick lines.</span></span>  

## <a name="to-split-warehouse-activity-lines"></a><span data-ttu-id="43aa7-110">Pour éclater des lignes activité entrepôt</span><span class="sxs-lookup"><span data-stu-id="43aa7-110">To split warehouse activity lines</span></span>  
1.  <span data-ttu-id="43aa7-111">Ouvrez une ligne activité entrepôt dans laquelle vous tentez de traiter une quantité insuffisante.</span><span class="sxs-lookup"><span data-stu-id="43aa7-111">Open a warehouse activity line where you are trying to handle an insufficient quantity.</span></span>  
2.  <span data-ttu-id="43aa7-112">Dans le champ **Quantité à traiter**, entrez la quantité réduite que vous pouvez gérer.</span><span class="sxs-lookup"><span data-stu-id="43aa7-112">In the **Qty. to Handle** field, enter the reduced quantity that you are able to handle.</span></span>  
3.  <span data-ttu-id="43aa7-113">Sur le raccourci **Lignes**, choisissez l'action **Actions**, choisissez **Fonctions**, puis choisissez l'action **Eclater ligne**.</span><span class="sxs-lookup"><span data-stu-id="43aa7-113">On the **Lines** FastTab, choose the **Actions** action, choose the **Functions** action, and then choose the **Split Line** action.</span></span> <span data-ttu-id="43aa7-114">Une nouvelle ligne s'affiche. Il s'agit d'une copie de la ligne d'origine, à la différence près que la quantité que vous avez retirée de la ligne d'origine figure dans le champ **Quantité à traiter**.</span><span class="sxs-lookup"><span data-stu-id="43aa7-114">A new line appears, which is a copy of the original line, except that the **Qty. to Handle** field contains the quantity that you removed from the original line.</span></span>  
4.  <span data-ttu-id="43aa7-115">Affectez à cette nouvelle ligne un emplacement approprié, ainsi qu'une zone en cas d'utilisation d'un prélèvement et d'un rangement suggérés, ou continuez à répartir la ligne autant de fois que nécessaire jusqu'à ce que vous ayez trouvé des emplacements appropriés pour toute la quantité.</span><span class="sxs-lookup"><span data-stu-id="43aa7-115">Assign an appropriate bin and, if you are using directed put-away and pick, a zone, to this new line, or continue splitting the line as necessary until you find appropriate bins for all of the quantity.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="43aa7-116">Si, en cas d'utilisation d'un prélèvement et d'un rangement suggérés dans l'entrepôt, vous répartissez les lignes, vous devez bien connaître l'entrepôt et être capable de choisir un emplacement répondant aux conditions de stockage de l'article et aux exigences générales du document entrepôt.</span><span class="sxs-lookup"><span data-stu-id="43aa7-116">If the location uses directed put-away and pick and you split the lines, you must be familiar with the warehouse and be able to choose a bin that matches the storage requirements of the item and that fulfills the general requirements of the warehouse document.</span></span> <span data-ttu-id="43aa7-117">Par exemple, vous n'allez pas répartir une ligne d'un document prélèvement et placer certains articles au niveau du stockage en vrac.</span><span class="sxs-lookup"><span data-stu-id="43aa7-117">For example, you would not split a line on a pick document and place some items in the bulk storage.</span></span>  

## <a name="see-also"></a><span data-ttu-id="43aa7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43aa7-118">See Also</span></span>  
[<span data-ttu-id="43aa7-119">Gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="43aa7-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="43aa7-120">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="43aa7-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="43aa7-121">[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="43aa7-121">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="43aa7-122">[Gestion des assemblages](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="43aa7-122">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="43aa7-123">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="43aa7-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="43aa7-124">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="43aa7-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
