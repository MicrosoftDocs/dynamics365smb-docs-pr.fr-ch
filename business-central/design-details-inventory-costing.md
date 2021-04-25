---
title: Détails de conception - Coûts ajustés | Microsoft Docs
description: Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés dans les fonctions Inventory Costing dans Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 22d53eac0957321c16d3e35cbf4d8f75d57c1cc5
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786772"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="28a33-103">Détails de conception : coûts ajustés</span><span class="sxs-lookup"><span data-stu-id="28a33-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="28a33-104">Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés dans les fonctions Inventory Costing dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="28a33-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="28a33-105">L’évaluation des coûts de stock, aussi appelé gestion des coûts, se charge de l’enregistrement et de la déclaration des coûts d’exploitation de la société.</span><span class="sxs-lookup"><span data-stu-id="28a33-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="28a33-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="28a33-106">In This Section</span></span>  
[<span data-ttu-id="28a33-107">Détails de conception : modes évaluation stock</span><span class="sxs-lookup"><span data-stu-id="28a33-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="28a33-108">Détails de conception : lettrage article</span><span class="sxs-lookup"><span data-stu-id="28a33-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="28a33-109">Détails de conception : problème de lettrage article connu</span><span class="sxs-lookup"><span data-stu-id="28a33-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="28a33-110">Détails de conception : ajustement des coûts</span><span class="sxs-lookup"><span data-stu-id="28a33-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="28a33-111">Détails de conception : date comptabilisation de l’écriture valeur d’ajustement</span><span class="sxs-lookup"><span data-stu-id="28a33-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="28a33-112">Détails de conception : validation du coût prévu</span><span class="sxs-lookup"><span data-stu-id="28a33-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="28a33-113">Détails de conception : coût moyen</span><span class="sxs-lookup"><span data-stu-id="28a33-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="28a33-114">Détails de conception : écart</span><span class="sxs-lookup"><span data-stu-id="28a33-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="28a33-115">Détails de conception : arrondi</span><span class="sxs-lookup"><span data-stu-id="28a33-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="28a33-116">Détails de conception : composants des coûts</span><span class="sxs-lookup"><span data-stu-id="28a33-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="28a33-117">Détails de conception : périodes inventaire</span><span class="sxs-lookup"><span data-stu-id="28a33-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="28a33-118">Détails de conception : comptabilisation stock</span><span class="sxs-lookup"><span data-stu-id="28a33-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="28a33-119">Détails de conception : validation d’ordre de fabrication</span><span class="sxs-lookup"><span data-stu-id="28a33-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="28a33-120">Détails de conception : validation d’ordre d’assemblage</span><span class="sxs-lookup"><span data-stu-id="28a33-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="28a33-121">Détails de conception : rapprochement de comptabilité</span><span class="sxs-lookup"><span data-stu-id="28a33-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="28a33-122">Détails de conception : comptes de la comptabilité</span><span class="sxs-lookup"><span data-stu-id="28a33-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="28a33-123">Détails de conception : évaluation du stock</span><span class="sxs-lookup"><span data-stu-id="28a33-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="28a33-124">Détails de conception : réévaluation</span><span class="sxs-lookup"><span data-stu-id="28a33-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]