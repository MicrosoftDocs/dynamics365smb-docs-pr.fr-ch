---
title: "Génération des coûts et rapprochement en comptabilité | Microsoft Docs"
description: "À la fin de la période comptable (mensuelle, annuelle, etc.), une série de tâches de contrôle des coûts et d'audit doivent être effectuées pour déclarer une valeur en stock correcte et équilibrée au département Finances. Outre les tâches habituelles de validation qui transfèrent les écritures valeur de chaque article vers les comptes généraux appropriés, l'auditeur ou le contrôleur responsable de cette tâche critique a accès à plusieurs états et fonctions de suivi, ainsi qu'à un outil de rapprochement."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3c3a02aa2251b9b6b18576e9f274d018a617b179
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="reporting-costs-and-reconciling-with-the-general-ledger"></a><span data-ttu-id="075a2-104">Génération des coûts et rapprochement en comptabilité</span><span class="sxs-lookup"><span data-stu-id="075a2-104">Reporting Costs and Reconciling with the General Ledger</span></span>
<span data-ttu-id="075a2-105">À la fin de la période comptable (mensuelle, annuelle, etc.), une série de tâches de contrôle des coûts et d'audit doivent être effectuées pour déclarer une valeur en stock correcte et équilibrée au département Finances.</span><span class="sxs-lookup"><span data-stu-id="075a2-105">At the end of accounting periods, monthly, yearly or other, a sequence of cost control and auditing tasks must be performed to report a correct and balanced inventory value to the finance department.</span></span> <span data-ttu-id="075a2-106">Outre les tâches habituelles de validation qui transfèrent les écritures valeur de chaque article vers les comptes généraux appropriés, l'auditeur ou le contrôleur responsable de cette tâche critique a accès à plusieurs états et fonctions de suivi, ainsi qu'à un outil de rapprochement.</span><span class="sxs-lookup"><span data-stu-id="075a2-106">Apart from the posting routine that transfers the individual item value entries to dedicated general ledger accounts, several reports, tracing functions, and a special reconciliation tool are available to the auditor or controller responsible for this business-critical work.</span></span>  

 <span data-ttu-id="075a2-107">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="075a2-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="075a2-108">**Pour**</span><span class="sxs-lookup"><span data-stu-id="075a2-108">**To**</span></span>|<span data-ttu-id="075a2-109">**Voir**</span><span class="sxs-lookup"><span data-stu-id="075a2-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="075a2-110">Afficher la valeur en stock des articles sélectionnés, y compris les informations sur les quantités et les valeurs des augmentations et des diminutions sur une période donnée.</span><span class="sxs-lookup"><span data-stu-id="075a2-110">View the inventory value of selected items, including information about the quantities and values of increases and decreases in inventory over a selected period.</span></span>|<span data-ttu-id="075a2-111">**État Évaluation du stock**</span><span class="sxs-lookup"><span data-stu-id="075a2-111">**Inventory Valuation** report</span></span>|  
|<span data-ttu-id="075a2-112">Afficher la valeur en stock des ordres de fabrication sélectionnés dans votre stock d'en-cours, telle que les quantités et valeurs de consommation, d'utilisation des capacités et de production dans les ordres de fabrication en cours.</span><span class="sxs-lookup"><span data-stu-id="075a2-112">View the inventory value of selected production orders in your WIP (work in process) inventory, such as the quantities and values of consumption, capacity usage, and output in ongoing production orders.</span></span>|<span data-ttu-id="075a2-113">**Évaluation du stock - État des travaux en cours**</span><span class="sxs-lookup"><span data-stu-id="075a2-113">**Inventory Valuation - WIP** report</span></span>|  
|<span data-ttu-id="075a2-114">Afficher la valeur en stock des articles sélectionnés, y compris leur coût réel et prévu à la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="075a2-114">View the inventory value of selected items, including their actual and expected cost on the date specified.</span></span>|<span data-ttu-id="075a2-115">**Éval. stock - Composante coût**</span><span class="sxs-lookup"><span data-stu-id="075a2-115">**Invt. Valuation - Cost Spec.** report</span></span>|  
|<span data-ttu-id="075a2-116">Utiliser un état pour analyser les raisons des écarts de coûts ou pour obtenir un aperçu du coût des marchandises vendues (CMV).</span><span class="sxs-lookup"><span data-stu-id="075a2-116">Use a report to analyze the reasons for cost variances or to gain insight into the cost shares of sold items (COGS).</span></span>|<span data-ttu-id="075a2-117">État **Analyse des coûts**</span><span class="sxs-lookup"><span data-stu-id="075a2-117">**Cost Shares Breakdown** report</span></span>|  
|<span data-ttu-id="075a2-118">Valider périodiquement les écritures valeur des transactions article de l'écriture inventaire dans les comptes généraux associés pour rapprocher les deux comptabilités.</span><span class="sxs-lookup"><span data-stu-id="075a2-118">Periodically post the value entries of item transactions from the inventory ledger to the related G/L accounts to reconcile the two ledgers.</span></span>|[<span data-ttu-id="075a2-119">Procédure : rapprocher les coûts ajustés avec la comptabilité</span><span class="sxs-lookup"><span data-stu-id="075a2-119">How to: Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="075a2-120">Utiliser une fenêtre pour vérifier le rapprochement de l'écriture inventaire et de la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="075a2-120">Use one window to audit the reconciliation between the inventory ledger and the general ledger.</span></span>|[<span data-ttu-id="075a2-121">Procédure : rapprocher les coûts ajustés avec la comptabilité</span><span class="sxs-lookup"><span data-stu-id="075a2-121">How to: Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="075a2-122">Déterminer le montant TEC devant être valider dans les comptes de bilan pour la génération d'états de clôture d'exercice.</span><span class="sxs-lookup"><span data-stu-id="075a2-122">Determine the WIP amount that needs to be posted to balance sheet accounts for period-end reporting.</span></span>|[<span data-ttu-id="075a2-123">Procédure : surveiller la progression et les performances</span><span class="sxs-lookup"><span data-stu-id="075a2-123">How to: Monitor Job Progress and Performance</span></span>](projects-how-monitor-progress-performance.md)|

## <a name="see-also"></a><span data-ttu-id="075a2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="075a2-124">See Also</span></span>  
[<span data-ttu-id="075a2-125">Configuration de l'évaluation du stock</span><span class="sxs-lookup"><span data-stu-id="075a2-125">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="075a2-126">Gestion des coûts ajustés</span><span class="sxs-lookup"><span data-stu-id="075a2-126">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="075a2-127">Finances</span><span class="sxs-lookup"><span data-stu-id="075a2-127">Finance</span></span>](finance.md)  
<span data-ttu-id="075a2-128">[STOCKS ET EN-COURS](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="075a2-128">[Inventory](inventory-manage-inventory.md) </span></span>  
<span data-ttu-id="075a2-129">[Ventes](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="075a2-129">[Sales](sales-manage-sales.md) </span></span>  
[<span data-ttu-id="075a2-130">Achats</span><span class="sxs-lookup"><span data-stu-id="075a2-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="075a2-131">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="075a2-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

