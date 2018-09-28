---
title: "Gestion des coûts ajustés | Microsoft Docs"
description: "La gestion des coûts, aussi appelée comptabilité analytique, se charge de l'enregistrement et de la déclaration des coûts d'exploitation de la société. Cette activité inclut la déclaration des coûts de fabrication et de stock qui constituent la valeur des articles."
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
ms.openlocfilehash: 088b8fdb11c32594499af752d5c6be652e2f69a6
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="managing-inventory-costs"></a><span data-ttu-id="b211e-104">Gestion des coûts ajustés</span><span class="sxs-lookup"><span data-stu-id="b211e-104">Managing Inventory Costs</span></span>
<span data-ttu-id="b211e-105">La gestion des coûts, aussi appelée comptabilité analytique, se charge de l'enregistrement et de la déclaration des coûts d'exploitation de la société.</span><span class="sxs-lookup"><span data-stu-id="b211e-105">Cost management, also referred to as “costing”, is concerned with recording and reporting business operating costs.</span></span> <span data-ttu-id="b211e-106">Cette activité inclut la déclaration des coûts de fabrication et de stock qui constituent la valeur des articles.</span><span class="sxs-lookup"><span data-stu-id="b211e-106">It includes the reporting of manufacturing costs and inventory costs, that is, the value of items.</span></span>   

<span data-ttu-id="b211e-107">Il est essentiel de comprendre les principes suivants : les méthodes d'évaluation des stocks au prix coûtant définissent le mode d'évaluation des articles lors de leur sortie de stock, l'ajustement des coûts met à jour le coût des biens vendus avec les coûts d'achat associés validés après la vente, les valeurs en stock doivent être validées vers les comptes généraux appropriés à des intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="b211e-107">Central principles to understand are that costing methods define how items are valued when they leave inventory, that cost adjustment updates the cost of goods sold with related purchase costs posted after the sale, and that inventory values must be posted to dedicated G/L accounts at regular intervals.</span></span>

<span data-ttu-id="b211e-108">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="b211e-108">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="b211e-109">**Pour**</span><span class="sxs-lookup"><span data-stu-id="b211e-109">**To**</span></span>|<span data-ttu-id="b211e-110">**Voir**</span><span class="sxs-lookup"><span data-stu-id="b211e-110">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="b211e-111">Lire différentes informations conceptuelles pour comprendre les principes et définitions qui gouvernent la fonctionnalité Comptabilité des coûts de stock [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b211e-111">Read various conceptual information to understand the principles and definitions that govern the inventory costing accounting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>|[<span data-ttu-id="b211e-112">À propos de l'évaluation des coûts de stock</span><span class="sxs-lookup"><span data-stu-id="b211e-112">About Inventory Costing</span></span>](finance-learn-about-costing.md)|  
|<span data-ttu-id="b211e-113">Configurer les périodes inventaire, les méthodes d'évaluation des stocks au prix coûtant et les modes d'arrondi.</span><span class="sxs-lookup"><span data-stu-id="b211e-113">Set up inventory periods, costing methods, and rounding methods.</span></span>|[<span data-ttu-id="b211e-114">Configuration de l'évaluation du stock</span><span class="sxs-lookup"><span data-stu-id="b211e-114">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)|
|<span data-ttu-id="b211e-115">Réévaluer ou amortir la valeur d'un ou de plusieurs articles dans le stock en validant leur valeur calculée courante.</span><span class="sxs-lookup"><span data-stu-id="b211e-115">Appreciate or depreciate the value of one or more items in inventory by posting their current, calculated value.</span></span>|[<span data-ttu-id="b211e-116">Réévaluer le stock</span><span class="sxs-lookup"><span data-stu-id="b211e-116">Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="b211e-117">Ajuster les coûts d'article, automatiquement ou manuellement, pour transférer les modifications de coût des écritures entrantes à leurs écritures sortantes associées.</span><span class="sxs-lookup"><span data-stu-id="b211e-117">Adjust item costs, either automatically or manually, to forward cost changes from inbound entries to their related outbound entries.</span></span>|[<span data-ttu-id="b211e-118">Ajuster coûts et prix article</span><span class="sxs-lookup"><span data-stu-id="b211e-118">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|
|<span data-ttu-id="b211e-119">Utiliser les fonctions d'évaluation des coûts spéciales pour les transactions article quotidiennes dans les opérations liées aux articles.</span><span class="sxs-lookup"><span data-stu-id="b211e-119">Use special costing functions for every-day item transactions in the item operations.</span></span>|[<span data-ttu-id="b211e-120">Gestion des coûts ajustés et des coûts de fabrication</span><span class="sxs-lookup"><span data-stu-id="b211e-120">Handling Inventory and Manufacturing Costs</span></span>](finance-handle-inventory-and-manufacturing-costs.md)|  
|<span data-ttu-id="b211e-121">Actualisez périodiquement les coûts standard des composants, dans les nomenclatures d'assemblage ou de production, et remonter les nouveaux coûts dans l'article parent.</span><span class="sxs-lookup"><span data-stu-id="b211e-121">Periodically update the standard costs of components, in assembly or production BOMs, and roll the new costs up to the parent item.</span></span>|[<span data-ttu-id="b211e-122">Mise à jour des coûts standard</span><span class="sxs-lookup"><span data-stu-id="b211e-122">Update Standard Costs</span></span>](finance-how-to-update-standard-costs.md)|
|<span data-ttu-id="b211e-123">Effectuer un contrôle de clôture d'exercice et des tâches de création de rapports, tels que le calcul de la valeur du stock et la validation des coûts dans la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="b211e-123">Perform period-end control and reporting tasks, such calculate the value of inventory and post costs to the general ledger.</span></span>|[<span data-ttu-id="b211e-124">Génération des coûts et rapprochement en comptabilité</span><span class="sxs-lookup"><span data-stu-id="b211e-124">Reporting Costs and Reconciling with the General Ledger</span></span>](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|<span data-ttu-id="b211e-125">En savoir plus sur les mécanismes dans le système d'évaluation.</span><span class="sxs-lookup"><span data-stu-id="b211e-125">Learn about all mechanisms in the costing system.</span></span>|[<span data-ttu-id="b211e-126">Détails de conception : évaluation stock</span><span class="sxs-lookup"><span data-stu-id="b211e-126">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  

## <a name="see-also"></a><span data-ttu-id="b211e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b211e-127">See Also</span></span>  
 [<span data-ttu-id="b211e-128">Finances</span><span class="sxs-lookup"><span data-stu-id="b211e-128">Finance</span></span>](finance.md)  
 <span data-ttu-id="b211e-129">[STOCKS ET EN-COURS](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="b211e-129">[Inventory](inventory-manage-inventory.md) </span></span>  
 <span data-ttu-id="b211e-130">[Ventes](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="b211e-130">[Sales](sales-manage-sales.md) </span></span>  
 [<span data-ttu-id="b211e-131">Achats</span><span class="sxs-lookup"><span data-stu-id="b211e-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="b211e-132">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b211e-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

