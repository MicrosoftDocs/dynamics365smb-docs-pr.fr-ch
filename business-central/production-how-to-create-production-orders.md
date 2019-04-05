---
title: Procédure de création d'en-têtes d'ordre de fabrication | Microsoft Docs
description: Vous pouvez créer manuellement un ordre de fabrication. Pour cela, la première étape est de créer un en-tête O.F.
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
ms.openlocfilehash: 13d699dbeb8fe2c3979a7b6bd330b14f077d2d3c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820482"
---
# <a name="create-production-order-headers"></a><span data-ttu-id="49b38-103">Créer des en-têtes O.F.</span><span class="sxs-lookup"><span data-stu-id="49b38-103">Create Production Order Headers</span></span>
<span data-ttu-id="49b38-104">Vous pouvez créer manuellement un ordre de fabrication. Pour cela, la première étape est de créer un en-tête O.F.</span><span class="sxs-lookup"><span data-stu-id="49b38-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="49b38-105">Les ordres de fabrication sont généralement créés automatiquement par une fonction de planification pour répondre à une demande connue.</span><span class="sxs-lookup"><span data-stu-id="49b38-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="49b38-106">Pour plus d'informations, voir [Planification](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="49b38-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="49b38-107">La procédure suivante s'appuie sur un ordre de fabrication planifié ferme.</span><span class="sxs-lookup"><span data-stu-id="49b38-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="49b38-108">Vous pouvez aussi créer des ordres de fabrication dotés d'un autre statut.</span><span class="sxs-lookup"><span data-stu-id="49b38-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="49b38-109">Pour créer un en-tête O.F.</span><span class="sxs-lookup"><span data-stu-id="49b38-109">To create a production order header</span></span>  
1.  <span data-ttu-id="49b38-110">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **O.F. planifiés fermes**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="49b38-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="49b38-111">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="49b38-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="49b38-112">Dans le champ **N°**,</span><span class="sxs-lookup"><span data-stu-id="49b38-112">In the **No.**</span></span> <span data-ttu-id="49b38-113">insérez le numéro suivant de la souche.</span><span class="sxs-lookup"><span data-stu-id="49b38-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="49b38-114">Dans le champ **Type origine**, sélectionnez la source de l'ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="49b38-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="49b38-115">Vous pouvez choisir de produire une famille d'articles.</span><span class="sxs-lookup"><span data-stu-id="49b38-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="49b38-116">Pour plus d'informations, voir [Utiliser les familles de production](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="49b38-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="49b38-117">Dans le champ **N° origine**, sélectionnez le numéro d'article, la famille, ou l'en-tête vente pour lequel l'ordre de fabrication doit être créé.</span><span class="sxs-lookup"><span data-stu-id="49b38-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="49b38-118">Renseignez les champs **Quantité** et **Délai** en fonction de vos spécifications.</span><span class="sxs-lookup"><span data-stu-id="49b38-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="49b38-119">Lorsque les exigences de production évoluent, comme les composants ou les opérations, vous pouvez replanifier rapidement l'ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="49b38-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="49b38-120">Pour plus d'informations, voir [Replanifier ou actualiser directement des ordres de fabrication](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="49b38-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="49b38-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49b38-121">See Also</span></span>  
<span data-ttu-id="49b38-122">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="49b38-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="49b38-123">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="49b38-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="49b38-124">[Planifié](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="49b38-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="49b38-125">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="49b38-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="49b38-126">Achats</span><span class="sxs-lookup"><span data-stu-id="49b38-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="49b38-127">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="49b38-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
