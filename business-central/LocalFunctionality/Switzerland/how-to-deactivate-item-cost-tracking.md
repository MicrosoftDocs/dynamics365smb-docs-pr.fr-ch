---
title: "Procédure : Désactiver le suivi des coûts article"
description: "Lorsque le stock n'est pas suivi pour un article, le coût article n'est pas forcément suivi, et une écriture comptable article n'est pas forcément créée."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: c6f10f8252c00bf0a599f9fa794ee36c41ce92be
ms.openlocfilehash: abf481ae651863e5ec290aacb58684980c31edbe
ms.contentlocale: fr-ch
ms.lasthandoff: 07/30/2018

---
# <a name="deactivate-item-cost-tracking"></a><span data-ttu-id="37e1e-103">Désactiver le suivi des coûts article</span><span class="sxs-lookup"><span data-stu-id="37e1e-103">Deactivate Item Cost Tracking</span></span>
<span data-ttu-id="37e1e-104">Lorsque le stock n'est pas suivi pour un article, le coût article n'est pas forcément suivi, et une écriture comptable article n'est pas forcément créée.</span><span class="sxs-lookup"><span data-stu-id="37e1e-104">When inventory is not tracked for an item, the item cost does not need to be tracked, and an item ledger entry does not need to be created.</span></span>  

<span data-ttu-id="37e1e-105">Vous pouvez désactiver le coût de l'article suivant pour un article.</span><span class="sxs-lookup"><span data-stu-id="37e1e-105">You can deactivate item cost tracking for an item.</span></span> <span data-ttu-id="37e1e-106">Généralement, le suivi des coûts des articles doit être désactivé pour les articles consommables, tels que les déchets de papier et pour les services comptabilisés comme des articles, tels que les frais de stationnement à tarif fixe.</span><span class="sxs-lookup"><span data-stu-id="37e1e-106">Generally, item cost tracking should be deactivated for consumable items, such as waste paper products and for services that are counted as items, such as flat rate parking fees.</span></span> <span data-ttu-id="37e1e-107">Le suivi du coût des articles devrait être désactivé pour les articles pour lesquels le suivi pourrait être trompeur.</span><span class="sxs-lookup"><span data-stu-id="37e1e-107">Item cost tracking should be deactivated on items for which tracking could be misleading.</span></span> <span data-ttu-id="37e1e-108">Les articles pour lesquels suivre des coûts article a été désactivé sont exclus de la réservation, de la vérification de disponibilité, de la traçabilité et des systèmes de planification matière.</span><span class="sxs-lookup"><span data-stu-id="37e1e-108">Items for which item cost tracking has been deactivated are excluded from reservation, availability check, item tracking, and material planning systems.</span></span>  

## <a name="to-deactivate-item-cost-tracking"></a><span data-ttu-id="37e1e-109">Pour désactiver le suivi des coûts article</span><span class="sxs-lookup"><span data-stu-id="37e1e-109">To deactivate item cost tracking</span></span>  

1.  <span data-ttu-id="37e1e-110">Cliquez sur l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="37e1e-110">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="37e1e-111">Sélectionnez l'article requis, puis cliquez sur l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="37e1e-111">Select the required item, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="37e1e-112">Sur le raccourci **Général**, cochez la case **Pas de stockage**.</span><span class="sxs-lookup"><span data-stu-id="37e1e-112">On the **General** FastTab, select the **No Stockkeeping** check box.</span></span>  

    <span data-ttu-id="37e1e-113">Une écriture comptable article n'est pas créée lorsque vous validez une transaction pour cet article.</span><span class="sxs-lookup"><span data-stu-id="37e1e-113">An item ledger entry will not be created when you post a transaction for this item.</span></span> <span data-ttu-id="37e1e-114">Pour plus d'informations, voir la table Écriture comptable article.</span><span class="sxs-lookup"><span data-stu-id="37e1e-114">For more information, see the Item Ledger Entry table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="37e1e-115">Vous ne pouvez pas sélectionner la case à cocher **Pas de stock** sur un article pour lequel les écritures comptables article ont déjà été validées.</span><span class="sxs-lookup"><span data-stu-id="37e1e-115">You cannot select the **No Stockkeeping** check box on an item for which item ledger entries have already been posted.</span></span>  

4.  <span data-ttu-id="37e1e-116">Choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="37e1e-116">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="37e1e-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37e1e-117">See Also</span></span>  
 [<span data-ttu-id="37e1e-118">Gestion des stocks, Suisse</span><span class="sxs-lookup"><span data-stu-id="37e1e-118">Swiss Inventory Management</span></span>](swiss-inventory-management.md)

