---
title: "Configuration de l'évaluation du stock | Microsoft Docs"
description: "Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f6d1d0da42bbc6bf186845648552eb639731759f
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a><span data-ttu-id="d0633-103">Configuration de l'évaluation du stock</span><span class="sxs-lookup"><span data-stu-id="d0633-103">Setting Up Inventory Valuation and Costing</span></span>
<span data-ttu-id="d0633-104">Pour vous assurer que les coûts ajustés sont enregistrés correctement, vous devez configurer plusieurs champs et fenêtres avant de commencer à effectuer des transactions article.</span><span class="sxs-lookup"><span data-stu-id="d0633-104">To make sure that inventory costs are recorded correctly, you must set up various fields and windows before you begin to make item transactions.</span></span>

<span data-ttu-id="d0633-105">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="d0633-105">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="d0633-106">**Pour**</span><span class="sxs-lookup"><span data-stu-id="d0633-106">**To**</span></span>|<span data-ttu-id="d0633-107">**Voir**</span><span class="sxs-lookup"><span data-stu-id="d0633-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="d0633-108">Configurer une méthode d'évaluation des stocks au prix coûtant pour chaque article pour régir la manière dont son coût entrant est utilisé pour évaluer la valeur du stock et le coût des biens vendus.</span><span class="sxs-lookup"><span data-stu-id="d0633-108">Set a costing method for each item to govern how its incoming cost is used to assess inventory value and the cost of goods sold.</span></span>|[<span data-ttu-id="d0633-109">Enregistrer de nouveaux articles</span><span class="sxs-lookup"><span data-stu-id="d0633-109">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="d0633-110">S'assurer que les coûts sont automatiquement validés dans la comptabilité lorsqu'un mouvement de stock est validé.</span><span class="sxs-lookup"><span data-stu-id="d0633-110">Ensure that the cost is automatically posted to the general ledger whenever an inventory transaction is posted.</span></span>|<span data-ttu-id="d0633-111">Champ **Compta. coûts automatique** de la page **Paramètres stock**</span><span class="sxs-lookup"><span data-stu-id="d0633-111">**Automatic Cost Posting** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="d0633-112">S'assurer que les coûts prévus sont validés dans la comptabilité afin de visualiser, à partir des comptes généraux en attente, une estimation des montants dus et du coût des articles échangés avant qu'ils ne soient effectivement facturés.</span><span class="sxs-lookup"><span data-stu-id="d0633-112">Ensure that expected costs are posted to the general ledger to see from the interim G/L accounts an estimate of the amounts due and the cost of the traded items before they are actually invoiced.</span></span>|<span data-ttu-id="d0633-113">Champ **Compta. coûts prévus** de la page **Paramètres stock**</span><span class="sxs-lookup"><span data-stu-id="d0633-113">**Expected Cost Posting to G/L** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="d0633-114">Configurer le système afin d'ajuster automatiquement toute modification des coûts chaque fois que vous validez des mouvements de stock.</span><span class="sxs-lookup"><span data-stu-id="d0633-114">Set the system up to adjust for any cost changes automatically every time you post inventory transactions.</span></span>|[<span data-ttu-id="d0633-115">Ajuster coûts et prix article</span><span class="sxs-lookup"><span data-stu-id="d0633-115">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="d0633-116">Définir si le coût moyen doit être calculé uniquement par article ou par article pour chaque référence SKU et pour chaque variante de l'article.</span><span class="sxs-lookup"><span data-stu-id="d0633-116">Define if the average cost is to be calculated per item only or per item for each stockkeping unit and for each variant of the item.</span></span>|<span data-ttu-id="d0633-117">Champ **Type calcul coût moyen** de la page **Paramètres stock**</span><span class="sxs-lookup"><span data-stu-id="d0633-117">**Average Cost Calc. Type** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="d0633-118">Sélectionner la période que le programme doit utiliser pour calculer le coût moyen pondéré des articles qui utilisent la méthode évaluation stock Moyen.</span><span class="sxs-lookup"><span data-stu-id="d0633-118">Select the period of time you would like the program to use for calculating the weighted average cost of items that use the average costing method.</span></span>|<span data-ttu-id="d0633-119">Champ **Période coût moyen** de la page **Paramètres stock**</span><span class="sxs-lookup"><span data-stu-id="d0633-119">**Average Cost Period** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="d0633-120">Définir des périodes inventaire pour contrôler la valeur du stock dans le temps en refusant d'accorder la validation de transactions lorsque les périodes inventaire sont clôturées.</span><span class="sxs-lookup"><span data-stu-id="d0633-120">Define inventory periods to control inventory value over time by disallowing transaction posting in closed inventory periods.</span></span>|[<span data-ttu-id="d0633-121">Utiliser les périodes inventaire</span><span class="sxs-lookup"><span data-stu-id="d0633-121">Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="d0633-122">S'assurer que les retours vente sont rapprochés des transactions sortantes afin de préserver la valeur du stock.</span><span class="sxs-lookup"><span data-stu-id="d0633-122">Ensure that sales returns are applied to the original outbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="d0633-123">Champ**Coût retour identique obligatoire** de la page **Ventes**</span><span class="sxs-lookup"><span data-stu-id="d0633-123">**Exact Cost Reversing Mandatory** field in the **Sales & Receivables** page</span></span>|  
|<span data-ttu-id="d0633-124">S'assurer que les retours achat sont rapprochés des transactions entrantes afin de préserver la valeur du stock.</span><span class="sxs-lookup"><span data-stu-id="d0633-124">Ensure that purchase returns are applied to the original inbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="d0633-125">Champ**Coût retour identique obligatoire** de la page **Achats**</span><span class="sxs-lookup"><span data-stu-id="d0633-125">**Exact Cost Reversing Mandatory** field in the **´Purchases & Payables** page</span></span>|
|<span data-ttu-id="d0633-126">Configurer les règles d'arrondi à appliquer lors de l'ajustement ou de la proposition des prix article et lors de l'ajustement ou de la proposition des coûts standard.</span><span class="sxs-lookup"><span data-stu-id="d0633-126">Set up the rounding rules to apply when adjusting or suggesting item prices and when adjusting or suggesting standard costs.</span></span>|<span data-ttu-id="d0633-127">Page **Mode arrondi**</span><span class="sxs-lookup"><span data-stu-id="d0633-127">**Rounding Method** page</span></span>|  

## <a name="see-also"></a><span data-ttu-id="d0633-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0633-128">See Also</span></span>  
[<span data-ttu-id="d0633-129">Gestion des coûts ajustés</span><span class="sxs-lookup"><span data-stu-id="d0633-129">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="d0633-130">Utilisation de Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="d0633-130">Working with Finance and Operations, Business edition</span></span>](ui-work-product.md)  
[<span data-ttu-id="d0633-131">Finances</span><span class="sxs-lookup"><span data-stu-id="d0633-131">Finance</span></span>](finance.md)  

