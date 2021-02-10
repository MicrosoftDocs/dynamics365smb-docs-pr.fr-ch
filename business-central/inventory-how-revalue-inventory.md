---
title: Créer des nouvelles écritures valeur pour des articles dans le stock| Microsoft Docs
description: Décrit comment réévaluer ou amortir les entrées valeur d’un ou de plusieurs articles dans le stock en validant leur valeur calculée courante.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2bcd09876f18bb948e060b06199d3d36facaa83f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750070"
---
# <a name="revalue-inventory"></a><span data-ttu-id="a7f17-103">Réévaluer le stock</span><span class="sxs-lookup"><span data-stu-id="a7f17-103">Revalue Inventory</span></span>
<span data-ttu-id="a7f17-104">Pour réévaluer ou amortir un article ou une écriture comptable article spécifique, vous devez utiliser la feuille réévaluation.</span><span class="sxs-lookup"><span data-stu-id="a7f17-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="a7f17-105">Pour réévaluer le stock</span><span class="sxs-lookup"><span data-stu-id="a7f17-105">To revalue inventory</span></span>
1. <span data-ttu-id="a7f17-106">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille réévaluation**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="a7f17-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="a7f17-107">Choisissez l’action **Calculer valeur stock**.</span><span class="sxs-lookup"><span data-stu-id="a7f17-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="a7f17-108">Sur la page **Calculer valeur stock**, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="a7f17-108">On the **Calculate Inventory Value** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="a7f17-109">Choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7f17-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="a7f17-110">Sur chaque ligne de la page **Feuille réévaluation**, indiquez le nouveau coût unitaire dans le champ **Coût unitaire (réévalué)**.</span><span class="sxs-lookup"><span data-stu-id="a7f17-110">On each line on the **Revaluation Journal** page, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="a7f17-111">Vous pouvez aussi indiquer le nouveau montant total dans le champ **Valeur stock (réévaluée)**.</span><span class="sxs-lookup"><span data-stu-id="a7f17-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="a7f17-112">Les champs appropriés sont automatiquement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="a7f17-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="a7f17-113">Remarque : le champ **Montant** affiche la modification réelle de la valeur du stock pour l’écriture comptable article sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="a7f17-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="a7f17-114">Il calcule la différence entre les champs **Valeur stock (calculée)** et **Valeur stock (réévaluée)**.</span><span class="sxs-lookup"><span data-stu-id="a7f17-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="a7f17-115">Lorsque vous avez renseigné toutes les lignes de la feuille réévaluation, choisissez l’action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="a7f17-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="a7f17-116">Les nouvelles écritures valeur sont alors créées pour refléter les réévaluations que vous avez validées.</span><span class="sxs-lookup"><span data-stu-id="a7f17-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="a7f17-117">Vous pouvez visualiser les nouvelles valeurs dans les fiches article concernées.</span><span class="sxs-lookup"><span data-stu-id="a7f17-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7f17-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7f17-118">See Also</span></span>
[<span data-ttu-id="a7f17-119">Détails de conception : réévaluation</span><span class="sxs-lookup"><span data-stu-id="a7f17-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="a7f17-120">Stock</span><span class="sxs-lookup"><span data-stu-id="a7f17-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a7f17-121">Ventes</span><span class="sxs-lookup"><span data-stu-id="a7f17-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="a7f17-122">Achats</span><span class="sxs-lookup"><span data-stu-id="a7f17-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a7f17-123">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a7f17-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
