---
title: "Procédure de validation par lots de la consommation | Microsoft Docs"
description: "Si le champ Méthode consommation indique **Manuelle**, vous devez valider les composants manuellement à l'aide d'une feuille consommation."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b7799e652394e8b9b96a168c0cb8945ec332734e
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="14463-103">Valider par lots la consommation de la production</span><span class="sxs-lookup"><span data-stu-id="14463-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="14463-104">Si le champ Méthode consommation indique **Manuelle**, vous devez valider les composants manuellement à l'aide d'une feuille consommation.</span><span class="sxs-lookup"><span data-stu-id="14463-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="14463-105">Vous pouvez également configurer le système pour valider automatiquement (*consommer*) les composants lorsque vous lancez ou terminez des ordres de fabrication.</span><span class="sxs-lookup"><span data-stu-id="14463-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="14463-106">Pour plus d'informations, voir [Activer la consommation en aval des composants en fonction de la production réalisée](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="14463-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="14463-107">Pour valider la consommation pour une ou plusieurs lignes ordre de fabrication</span><span class="sxs-lookup"><span data-stu-id="14463-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="14463-108">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille consommation**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="14463-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="14463-109">Renseignez les champs en indiquant les données relatives à l'ordre de fabrication et à la consommation.</span><span class="sxs-lookup"><span data-stu-id="14463-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="14463-110">Si l'entrepôt dans lequel les composants sont stockés est configuré pour utiliser des emplacements mais pas le traitement de prélèvement, affectez un code emplacement à la ligne feuille pour indiquer d'où les articles doivent être prélevés dans l'entrepôt.</span><span class="sxs-lookup"><span data-stu-id="14463-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="14463-111">Pour plus d'informations, voir [Prélever pour la fabrication ou l'assemblage](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="14463-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="14463-112">Choisissez l'action **Valider** pour valider la consommation.</span><span class="sxs-lookup"><span data-stu-id="14463-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="14463-113">Les écritures comptables article associées sont réduites.</span><span class="sxs-lookup"><span data-stu-id="14463-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="14463-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14463-114">See Also</span></span>  
<span data-ttu-id="14463-115">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="14463-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="14463-116">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="14463-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="14463-117">[Planifié](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="14463-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="14463-118">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="14463-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="14463-119">Achats</span><span class="sxs-lookup"><span data-stu-id="14463-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="14463-120">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="14463-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

