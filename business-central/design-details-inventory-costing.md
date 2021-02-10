---
title: Détails de conception - Coûts ajustés | Microsoft Docs
description: Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés dans les fonctions Inventory Costing dans Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 97aa9dc23397403b74fc8f1c65d302733ab3301c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751495"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="7ea58-103">Détails de conception : coûts ajustés</span><span class="sxs-lookup"><span data-stu-id="7ea58-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="7ea58-104">Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés dans les fonctions Inventory Costing dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="7ea58-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="7ea58-105">L’évaluation des coûts de stock, aussi appelé gestion des coûts, se charge de l’enregistrement et de la déclaration des coûts d’exploitation de la société.</span><span class="sxs-lookup"><span data-stu-id="7ea58-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="7ea58-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7ea58-106">In This Section</span></span>  
[<span data-ttu-id="7ea58-107">Détails de conception : modes évaluation stock</span><span class="sxs-lookup"><span data-stu-id="7ea58-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="7ea58-108">Détails de conception : lettrage article</span><span class="sxs-lookup"><span data-stu-id="7ea58-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="7ea58-109">Détails de conception : problème de lettrage article connu</span><span class="sxs-lookup"><span data-stu-id="7ea58-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="7ea58-110">Détails de conception : ajustement des coûts</span><span class="sxs-lookup"><span data-stu-id="7ea58-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="7ea58-111">Détails de conception : date comptabilisation de l’écriture valeur d’ajustement</span><span class="sxs-lookup"><span data-stu-id="7ea58-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="7ea58-112">Détails de conception : validation du coût prévu</span><span class="sxs-lookup"><span data-stu-id="7ea58-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="7ea58-113">Détails de conception : coût moyen</span><span class="sxs-lookup"><span data-stu-id="7ea58-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="7ea58-114">Détails de conception : écart</span><span class="sxs-lookup"><span data-stu-id="7ea58-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="7ea58-115">Détails de conception : arrondi</span><span class="sxs-lookup"><span data-stu-id="7ea58-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="7ea58-116">Détails de conception : composants des coûts</span><span class="sxs-lookup"><span data-stu-id="7ea58-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="7ea58-117">Détails de conception : périodes inventaire</span><span class="sxs-lookup"><span data-stu-id="7ea58-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="7ea58-118">Détails de conception : comptabilisation stock</span><span class="sxs-lookup"><span data-stu-id="7ea58-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="7ea58-119">Détails de conception : validation d’ordre de fabrication</span><span class="sxs-lookup"><span data-stu-id="7ea58-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="7ea58-120">Détails de conception : validation d’ordre d’assemblage</span><span class="sxs-lookup"><span data-stu-id="7ea58-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="7ea58-121">Détails de conception : rapprochement de comptabilité</span><span class="sxs-lookup"><span data-stu-id="7ea58-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="7ea58-122">Détails de conception : comptes de la comptabilité</span><span class="sxs-lookup"><span data-stu-id="7ea58-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="7ea58-123">Détails de conception : évaluation du stock</span><span class="sxs-lookup"><span data-stu-id="7ea58-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="7ea58-124">Détails de conception : réévaluation</span><span class="sxs-lookup"><span data-stu-id="7ea58-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)
