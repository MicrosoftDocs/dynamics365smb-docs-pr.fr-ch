---
title: "Détails de conception - Coûts ajustés | Microsoft Docs"
description: "Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés dans les fonctions Inventory Costing dans Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 04f41fa7b075692fef8243e24cff1ef3a5ebaf65
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="df11e-103">Détails de conception : coûts ajustés</span><span class="sxs-lookup"><span data-stu-id="df11e-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="df11e-104">Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés dans les fonctions Inventory Costing dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="df11e-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="df11e-105">L'évaluation des coûts de stock, aussi appelé gestion des coûts, se charge de l'enregistrement et de la déclaration des coûts d'exploitation de la société.</span><span class="sxs-lookup"><span data-stu-id="df11e-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="df11e-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="df11e-106">In This Section</span></span>  
[<span data-ttu-id="df11e-107">Détails de conception : modes évaluation stock</span><span class="sxs-lookup"><span data-stu-id="df11e-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="df11e-108">Détails de conception : lettrage article</span><span class="sxs-lookup"><span data-stu-id="df11e-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="df11e-109">Détails de conception : problème de lettrage article connu</span><span class="sxs-lookup"><span data-stu-id="df11e-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="df11e-110">Détails de conception : ajustement des coûts</span><span class="sxs-lookup"><span data-stu-id="df11e-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="df11e-111">Détails de conception : date comptabilisation de l'écriture valeur d'ajustement</span><span class="sxs-lookup"><span data-stu-id="df11e-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="df11e-112">Détails de conception : validation du coût prévu</span><span class="sxs-lookup"><span data-stu-id="df11e-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="df11e-113">Détails de conception : coût moyen</span><span class="sxs-lookup"><span data-stu-id="df11e-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="df11e-114">Détails de conception : écart</span><span class="sxs-lookup"><span data-stu-id="df11e-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="df11e-115">Détails de conception : arrondi</span><span class="sxs-lookup"><span data-stu-id="df11e-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="df11e-116">Détails de conception : composants des coûts</span><span class="sxs-lookup"><span data-stu-id="df11e-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="df11e-117">Détails de conception : périodes inventaire</span><span class="sxs-lookup"><span data-stu-id="df11e-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="df11e-118">Détails de conception : comptabilisation stock</span><span class="sxs-lookup"><span data-stu-id="df11e-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="df11e-119">Détails de conception : validation d'ordre de fabrication</span><span class="sxs-lookup"><span data-stu-id="df11e-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="df11e-120">Détails de conception : validation d'ordre d'assemblage</span><span class="sxs-lookup"><span data-stu-id="df11e-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="df11e-121">Détails de conception : rapprochement de comptabilité</span><span class="sxs-lookup"><span data-stu-id="df11e-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="df11e-122">Détails de conception : comptes de la comptabilité</span><span class="sxs-lookup"><span data-stu-id="df11e-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="df11e-123">Détails de conception : réévaluation</span><span class="sxs-lookup"><span data-stu-id="df11e-123">Design Details: Revaluation</span></span>](design-details-revaluation.md)

