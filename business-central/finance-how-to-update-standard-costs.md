---
title: 'Procédure : mise à jour des coûts standard | Microsoft Docs'
description: Vous devez régulièrement mettre à jour les coûts standard des composants et remonter les nouveaux coûts dans l’article parent.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: faa5b0f7ffc30d0f575f9b6e61d925f9606b4581
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750670"
---
# <a name="update-standard-costs"></a><span data-ttu-id="bc73a-103">Mise à jour des coûts standard</span><span class="sxs-lookup"><span data-stu-id="bc73a-103">Update Standard Costs</span></span>
<span data-ttu-id="bc73a-104">Vous devez régulièrement mettre à jour les coûts standard des composants et remonter les nouveaux coûts dans l’article parent.</span><span class="sxs-lookup"><span data-stu-id="bc73a-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="bc73a-105">Le processus comprend généralement les quatre étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc73a-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="bc73a-106">Mettre à jour les coûts aux niveaux des composants et de la capacité.</span><span class="sxs-lookup"><span data-stu-id="bc73a-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="bc73a-107">Pour plus d’informations, voir le traitement par lots **Proposer coût standard article**.</span><span class="sxs-lookup"><span data-stu-id="bc73a-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="bc73a-108">La consolidation et le calcul multi-niveau des coûts des composants et de capacité permettent de déterminer le coût de fabrication ou d’assemblage des articles.</span><span class="sxs-lookup"><span data-stu-id="bc73a-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="bc73a-109">Appliquer les coûts standard entrés lorsque vous lancez les traitements par lots précédents.</span><span class="sxs-lookup"><span data-stu-id="bc73a-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="bc73a-110">Les coûts standard n’entrent en vigueur que lorsqu’ils sont mis en œuvre.</span><span class="sxs-lookup"><span data-stu-id="bc73a-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="bc73a-111">Pour plus d’informations, voir Appliquer nouv. coût standard.</span><span class="sxs-lookup"><span data-stu-id="bc73a-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="bc73a-112">Appliquer les modifications pour mettre à jour le champ **Coût unitaire** de la fiche article et effectuer une réévaluation du stock.</span><span class="sxs-lookup"><span data-stu-id="bc73a-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="bc73a-113">Pour plus d’informations, voir [Réévaluer le stock](inventory-how-revalue-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="bc73a-113">For more information, see [Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="bc73a-114">Pour plus d’informations, voir [À propos du calcul des coûts standard](finance-about-calculating-standard-cost.md) .</span><span class="sxs-lookup"><span data-stu-id="bc73a-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="bc73a-115">Pour mettre à jour des coûts standard</span><span class="sxs-lookup"><span data-stu-id="bc73a-115">To update standard costs</span></span>  
1.  <span data-ttu-id="bc73a-116">Exécutez le traitement par lots **Ajuster coûts - Écr. article**.</span><span class="sxs-lookup"><span data-stu-id="bc73a-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="bc73a-117">Exécutez le traitement par lots **Valider coûts ajustés**.</span><span class="sxs-lookup"><span data-stu-id="bc73a-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="bc73a-118">Ouvrez la **Feuille coût standard** et utilisez une ou plusieurs des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc73a-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="bc73a-119">Exécutez le traitement par lots **Proposer coût standard article**.</span><span class="sxs-lookup"><span data-stu-id="bc73a-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="bc73a-120">Vérifiez les résultats et apportez des modifications si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bc73a-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="bc73a-121">Exécutez le traitement par lots **Suggérer le coût standard de la capacité**.</span><span class="sxs-lookup"><span data-stu-id="bc73a-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="bc73a-122">Vérifiez les résultats et apportez des modifications si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bc73a-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="bc73a-123">Exécutez le traitement par lots **Calculer coût std multi-niv.**.</span><span class="sxs-lookup"><span data-stu-id="bc73a-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="bc73a-124">Vérifiez les résultats et apportez des modifications si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bc73a-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="bc73a-125">Exécutez le traitement par lots **Appliquer nouv. coût standard**.</span><span class="sxs-lookup"><span data-stu-id="bc73a-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="bc73a-126">Vérifiez et validez la page **Feuille réévaluation** renseignée avec les entrées des étapes précédentes de ce processus.</span><span class="sxs-lookup"><span data-stu-id="bc73a-126">Review and post the **Revaluation Journal** page, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bc73a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc73a-127">See Also</span></span>  
 <span data-ttu-id="bc73a-128">[À propos du calcul des coûts standard](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="bc73a-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="bc73a-129">[Gestion des coûts ajustés](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="bc73a-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="bc73a-130">[Détails de conception : modes évaluation stock](design-details-costing-methods.md) [Finance](finance.md)</span><span class="sxs-lookup"><span data-stu-id="bc73a-130">[Design Details: Costing Methods](design-details-costing-methods.md) [Finance](finance.md)</span></span>  
 <span data-ttu-id="bc73a-131">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bc73a-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
