---
title: "Créer des nouvelles écritures valeur pour des articles dans le stock| Microsoft Docs"
description: "Décrit comment réévaluer ou amortir les entrées valeur d'un ou de plusieurs articles dans le stock en validant leur valeur calculée courante."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d4111c5e1e496b2b47afed2d37533707f1c99a89
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="revalue-inventory"></a><span data-ttu-id="9a8ca-103">Réévaluer le stock</span><span class="sxs-lookup"><span data-stu-id="9a8ca-103">Revalue Inventory</span></span>
<span data-ttu-id="9a8ca-104">Pour réévaluer ou amortir un article ou une écriture comptable article spécifique, vous devez utiliser la feuille réévaluation.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="9a8ca-105">Pour réévaluer le stock</span><span class="sxs-lookup"><span data-stu-id="9a8ca-105">To revalue inventory</span></span>
1. <span data-ttu-id="9a8ca-106">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille réévaluation**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="9a8ca-107">Choisissez l'action **Calculer valeur stock**.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="9a8ca-108">Dans la fenêtre **Calculer valeur stock**, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-108">In the **Calculate Inventory Value** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="9a8ca-109">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="9a8ca-110">Sur chaque ligne de la fenêtre **Feuille réévaluation**, indiquez le nouveau coût unitaire dans le champ **Coût unitaire (réévalué)**.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-110">On each line in the **Revaluation Journal** window, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="9a8ca-111">Vous pouvez aussi indiquer le nouveau montant total dans le champ **Valeur stock (réévaluée)**.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="9a8ca-112">Les champs appropriés sont automatiquement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="9a8ca-113">Remarque : le champ **Montant** affiche la modification réelle de la valeur du stock pour l'écriture comptable article sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="9a8ca-114">Il calcule la différence entre les champs **Valeur stock (calculée)** et **Valeur stock (réévaluée)**.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="9a8ca-115">Lorsque vous avez renseigné toutes les lignes de la feuille réévaluation, choisissez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="9a8ca-116">Les nouvelles écritures valeur sont alors créées pour refléter les réévaluations que vous avez validées.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="9a8ca-117">Vous pouvez visualiser les nouvelles valeurs dans les fiches article concernées.</span><span class="sxs-lookup"><span data-stu-id="9a8ca-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a8ca-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a8ca-118">See Also</span></span>
[<span data-ttu-id="9a8ca-119">Détails de conception : réévaluation</span><span class="sxs-lookup"><span data-stu-id="9a8ca-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="9a8ca-120">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="9a8ca-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="9a8ca-121">Ventes</span><span class="sxs-lookup"><span data-stu-id="9a8ca-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="9a8ca-122">Achats</span><span class="sxs-lookup"><span data-stu-id="9a8ca-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="9a8ca-123">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9a8ca-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

