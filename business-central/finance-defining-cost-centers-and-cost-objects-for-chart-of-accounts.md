---
title: Définition des centres de coûts et des coûts associés pour le plan comptable | Microsoft Docs
description: Vous pouvez transférer automatiquement les écritures de dépenses et de revenus à partir de la comptabilité générale vers la comptabilité analytique, que ce soit pour la validation comptable ou avec un traitement par lots. Lors du transfert, le système transfère uniquement les écritures déjà liées à un centre de coûts ou aux coûts associés. Pour préparer un transfert pertinent, assurez-vous que les centres de coûts et les coûts associés sont définis correctement.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 00c0ac4a37476c2ab21ddc850e80e7abeb5eda18
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "923337"
---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="dbc91-105">Définition des centres de coûts et des coûts associés pour le plan comptable</span><span class="sxs-lookup"><span data-stu-id="dbc91-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="dbc91-106">Vous pouvez transférer automatiquement les écritures de dépenses et de revenus à partir de la comptabilité générale vers la comptabilité analytique, que ce soit pour la validation comptable ou avec un traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="dbc91-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="dbc91-107">Lors du transfert, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfère uniquement les écritures déjà liées à un centre de coûts ou aux coûts associés.</span><span class="sxs-lookup"><span data-stu-id="dbc91-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="dbc91-108">Pour préparer un transfert pertinent, assurez-vous que les centres de coûts et les coûts associés sont définis correctement.</span><span class="sxs-lookup"><span data-stu-id="dbc91-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="dbc91-109">Définition des sections analytiques par défaut pour des comptes généraux</span><span class="sxs-lookup"><span data-stu-id="dbc91-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="dbc91-110">Pour chaque compte général, vous pouvez définir des sections analytiques par défaut dans la table **Affectation analytique**.</span><span class="sxs-lookup"><span data-stu-id="dbc91-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="dbc91-111">L'exemple suivant décrit la configuration requise pour avoir un centre de coût DÉPARTEMENT sans jamais avoir de coûts associés PROJET lors de la validation d'un compte général.</span><span class="sxs-lookup"><span data-stu-id="dbc91-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="dbc91-112">**Code axe analytique**</span><span class="sxs-lookup"><span data-stu-id="dbc91-112">**Dimension Code**</span></span>|<span data-ttu-id="dbc91-113">**Contrôle validation**</span><span class="sxs-lookup"><span data-stu-id="dbc91-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="dbc91-114">Département</span><span class="sxs-lookup"><span data-stu-id="dbc91-114">Department</span></span>|<span data-ttu-id="dbc91-115">Code obligatoire</span><span class="sxs-lookup"><span data-stu-id="dbc91-115">Code Mandatory</span></span>|  
|<span data-ttu-id="dbc91-116">Dossier</span><span class="sxs-lookup"><span data-stu-id="dbc91-116">Project</span></span>|<span data-ttu-id="dbc91-117">Pas de code</span><span class="sxs-lookup"><span data-stu-id="dbc91-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="dbc91-118">Définition des sections analytiques pour les frais généraux et les coûts directs</span><span class="sxs-lookup"><span data-stu-id="dbc91-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="dbc91-119">Vous pouvez transférer des frais généraux à un centre de coûts, et des coûts directs aux coûts associés.</span><span class="sxs-lookup"><span data-stu-id="dbc91-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="dbc91-120">Le tableau suivant décrit comment optimiser la combinaison des valeurs de paramétrage des axes analytiques.</span><span class="sxs-lookup"><span data-stu-id="dbc91-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="dbc91-121">Transférer vers</span><span class="sxs-lookup"><span data-stu-id="dbc91-121">Transfer To</span></span>|<span data-ttu-id="dbc91-122">Validation du centre de coûts</span><span class="sxs-lookup"><span data-stu-id="dbc91-122">Cost Center Posting</span></span>|<span data-ttu-id="dbc91-123">Validation des coûts associés</span><span class="sxs-lookup"><span data-stu-id="dbc91-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="dbc91-124">Centre de coûts</span><span class="sxs-lookup"><span data-stu-id="dbc91-124">Cost Center</span></span>|<span data-ttu-id="dbc91-125">Code obligatoire</span><span class="sxs-lookup"><span data-stu-id="dbc91-125">Code Mandatory</span></span>|<span data-ttu-id="dbc91-126">Pas de code</span><span class="sxs-lookup"><span data-stu-id="dbc91-126">No Code</span></span>|  
|<span data-ttu-id="dbc91-127">Coûts associés</span><span class="sxs-lookup"><span data-stu-id="dbc91-127">Cost Object</span></span>|<span data-ttu-id="dbc91-128">Pas de code</span><span class="sxs-lookup"><span data-stu-id="dbc91-128">No Code</span></span>|<span data-ttu-id="dbc91-129">Code obligatoire</span><span class="sxs-lookup"><span data-stu-id="dbc91-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="dbc91-130">Pour vous assurer que le centre de coûts et les coûts associés prédéfinis et configurés en comptabilité générale sont reportés automatiquement dans la comptabilité analytique, cochez la case **Vérifier validations compta** sur la page Paramètres comptabilité analytique.</span><span class="sxs-lookup"><span data-stu-id="dbc91-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dbc91-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbc91-131">See Also</span></span>  
[<span data-ttu-id="dbc91-132">Comptabilité pour les coûts</span><span class="sxs-lookup"><span data-stu-id="dbc91-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="dbc91-133">Paramétrage du contrôle de gestion</span><span class="sxs-lookup"><span data-stu-id="dbc91-133">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)  
<span data-ttu-id="dbc91-134">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dbc91-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
