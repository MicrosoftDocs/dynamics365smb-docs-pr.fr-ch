---
title: Procédure d'utilisation des familles d'articles dans la production | Microsoft Docs
description: Lorsque vous personnalisez un calendrier principal pour votre société ou pour l'un de ses partenaires commerciaux, votre tâche consiste essentiellement à modifier le statut des jours ouvrés et chômés.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 9400e2cc52501b333f71368af556fdeacb1f10c5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784047"
---
# <a name="work-with-production-families"></a><span data-ttu-id="41bed-103">Utiliser les familles de production</span><span class="sxs-lookup"><span data-stu-id="41bed-103">Work with Production Families</span></span>
<span data-ttu-id="41bed-104">Une famille de production est un groupe d'articles distincts dont la relation repose sur la similitude de leur processus de fabrication.</span><span class="sxs-lookup"><span data-stu-id="41bed-104">A production family is a group of individual items whose relationship is based on the similarity of their manufacturing processes.</span></span> <span data-ttu-id="41bed-105">Si vous formez des familles de production, certains articles peuvent être fabriqués plusieurs fois au cours d'une production, ce qui optimise la consommation de matière.</span><span class="sxs-lookup"><span data-stu-id="41bed-105">By forming production families, some items can be manufactured twice or more in one production, which will optimize material consumption.</span></span>

<span data-ttu-id="41bed-106">Dans le champ **Quantité** de la page **Famille**, entrez la quantité à produire lorsque l'ensemble de la famille a été fabriquée une fois.</span><span class="sxs-lookup"><span data-stu-id="41bed-106">In the **Quantity** field on the **Family** page, you enter the quantity that will be produced when the whole family has been manufactured once.</span></span>

## <a name="example"></a><span data-ttu-id="41bed-107">Exemple :</span><span class="sxs-lookup"><span data-stu-id="41bed-107">Example</span></span>
<span data-ttu-id="41bed-108">Dans les processus de découpe, quatre pièces du même article et dix pièces d'un autre peuvent être fabriquées simultanément à partir d'une plaque.</span><span class="sxs-lookup"><span data-stu-id="41bed-108">In punching processes, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span> <span data-ttu-id="41bed-109">La machine à découpe découpe les 14 pièces en une seule fois.</span><span class="sxs-lookup"><span data-stu-id="41bed-109">The punching machine will punch all 14 pieces in one step.</span></span>

<span data-ttu-id="41bed-110">Le regroupement d'éléments en familles de production permet de réduire la quantité perte car ce qui devrait normalement constituer un rebut définitif, lors de la fabrication de grosses pièces, est utilisé pour fabriquer de petits articles.</span><span class="sxs-lookup"><span data-stu-id="41bed-110">Forming production families reduces the scrap quantity because what would normally be leftover scrap, when producing big pieces, will be used instead to produce small items.</span></span>

## <a name="to-set-up-a-production-family"></a><span data-ttu-id="41bed-111">Pour configurer une famille de production</span><span class="sxs-lookup"><span data-stu-id="41bed-111">To set up a production family</span></span>
1. <span data-ttu-id="41bed-112">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Familles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="41bed-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Families**, and then choose the related link.</span></span>
2. <span data-ttu-id="41bed-113">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="41bed-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a><span data-ttu-id="41bed-114">Pour produire selon une famille de production</span><span class="sxs-lookup"><span data-stu-id="41bed-114">To produce based on a production family</span></span>
1. <span data-ttu-id="41bed-115">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **O.F. planifiés fermes**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="41bed-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="41bed-116">Créez un ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="41bed-116">Create a new production order.</span></span> <span data-ttu-id="41bed-117">Pour plus d'informations, voir [Créer des ordres de fabrication](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="41bed-117">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>
3. <span data-ttu-id="41bed-118">Dans le champ **Type origine**, sélectionnez **Famille**.</span><span class="sxs-lookup"><span data-stu-id="41bed-118">In the **Source Type** field, select **Family**.</span></span>  
4. <span data-ttu-id="41bed-119">Dans le champ **N° origine**, sélectionnez la famille de production appropriée.</span><span class="sxs-lookup"><span data-stu-id="41bed-119">In the **Source No.** field, select the relevant production family.</span></span>

## <a name="see-also"></a><span data-ttu-id="41bed-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41bed-120">See Also</span></span>
[<span data-ttu-id="41bed-121">Créer des nomenclatures de production</span><span class="sxs-lookup"><span data-stu-id="41bed-121">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="41bed-122">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="41bed-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="41bed-123">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="41bed-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="41bed-124">[Planifié](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="41bed-124">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="41bed-125">Stock</span><span class="sxs-lookup"><span data-stu-id="41bed-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="41bed-126">Achats</span><span class="sxs-lookup"><span data-stu-id="41bed-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="41bed-127">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="41bed-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
