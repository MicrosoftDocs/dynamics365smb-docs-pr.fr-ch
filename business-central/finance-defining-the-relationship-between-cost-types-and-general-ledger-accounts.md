---
title: "Définition de la relation entre les types de coûts et les comptes généraux | Microsoft Docs"
description: "Découvrez comment définir la relation entre le type de coût et le compte général."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7709edb214804f52ee9b495c43b5302e2a23bd6b
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a><span data-ttu-id="4177f-103">Définition de la relation entre les types de coûts et les comptes généraux</span><span class="sxs-lookup"><span data-stu-id="4177f-103">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>
<span data-ttu-id="4177f-104">Une relation entre le type de coût et le compte général est créée dans le type de coût et le compte général.</span><span class="sxs-lookup"><span data-stu-id="4177f-104">The relationship between the cost type and the general ledger account is created in the cost type and in the general ledger account.</span></span>  

* <span data-ttu-id="4177f-105">Le champ **Plage compte général** de la table **Type coût** définit les comptes généraux appartenant à un type de coût.</span><span class="sxs-lookup"><span data-stu-id="4177f-105">The **G/L Account Range** field in the **Cost Type** table establishes which general ledger accounts belong to a cost type.</span></span>  
* <span data-ttu-id="4177f-106">Le champ **N° type coût de solde**</span><span class="sxs-lookup"><span data-stu-id="4177f-106">The **Cost Type No.**</span></span> <span data-ttu-id="4177f-107">du plan comptable définit l'appartenance du compte général à un type de coût.</span><span class="sxs-lookup"><span data-stu-id="4177f-107">field in the chart of accounts establishes which cost type a general ledger account belongs to.</span></span>  

<span data-ttu-id="4177f-108">Ces deux champs sont renseignés automatiquement lorsque vous utilisez la fonction **Obtenir les types de coûts à partir du plan comptable**.</span><span class="sxs-lookup"><span data-stu-id="4177f-108">These two fields are filled automatically when you use the **Get Cost Types from Chart of Accounts** function.</span></span>  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a><span data-ttu-id="4177f-109">Relations entre les comptes généraux et les types de coûts</span><span class="sxs-lookup"><span data-stu-id="4177f-109">Relationship Between General Ledger Accounts and Cost Types</span></span>  
<span data-ttu-id="4177f-110">Une relation n:1 existe entre les comptes généraux et les types de coûts.</span><span class="sxs-lookup"><span data-stu-id="4177f-110">There is an n:1 relationship between general ledger accounts and cost types.</span></span> <span data-ttu-id="4177f-111">Plusieurs comptes généraux peuvent appartenir à un type de coût, mais chaque compte général appartient à un seul type de coût.</span><span class="sxs-lookup"><span data-stu-id="4177f-111">Several general ledger accounts can belong to one cost type, but each general ledger account belongs to only one cost type.</span></span> <span data-ttu-id="4177f-112">Le tableau suivant décrit la relation en détails.</span><span class="sxs-lookup"><span data-stu-id="4177f-112">The following table describes the details in the relationship.</span></span>  

|<span data-ttu-id="4177f-113">Relation</span><span class="sxs-lookup"><span data-stu-id="4177f-113">Relationship</span></span>|<span data-ttu-id="4177f-114">**Plage compte général**</span><span class="sxs-lookup"><span data-stu-id="4177f-114">**G/L Account Range**</span></span>|<span data-ttu-id="4177f-115">**N° type coût**</span><span class="sxs-lookup"><span data-stu-id="4177f-115">**Cost Type No.**</span></span>|  
|------------------|------------------------------------------------|-------------------------------------------|  
|<span data-ttu-id="4177f-116">Un compte général pour chaque type de coût</span><span class="sxs-lookup"><span data-stu-id="4177f-116">One general ledger account for each cost type</span></span>|<span data-ttu-id="4177f-117">Un compte général</span><span class="sxs-lookup"><span data-stu-id="4177f-117">One general ledger account</span></span>|<span data-ttu-id="4177f-118">Un type de coût</span><span class="sxs-lookup"><span data-stu-id="4177f-118">One cost type</span></span>|  
|<span data-ttu-id="4177f-119">Plusieurs comptes généraux pour chaque type de coût</span><span class="sxs-lookup"><span data-stu-id="4177f-119">Several general ledger accounts for one cost type</span></span>|<span data-ttu-id="4177f-120">Plage de comptes généraux, par exemple, 7110..7193 pour chaque compte général</span><span class="sxs-lookup"><span data-stu-id="4177f-120">General ledger account range, for example, 7110..7193 for each general ledger account</span></span>|<span data-ttu-id="4177f-121">Pour chaque compte général de la plage, il n'existe qu'un seul type de coût</span><span class="sxs-lookup"><span data-stu-id="4177f-121">For each general ledger account in the range, there is only one cost type</span></span>|  
|<span data-ttu-id="4177f-122">Types de coûts sans comptes généraux correspondants</span><span class="sxs-lookup"><span data-stu-id="4177f-122">Cost types without corresponding general ledger accounts</span></span>|<Empty>||  
|<span data-ttu-id="4177f-123">Comptes généraux dont les écritures ne seront pas transférées</span><span class="sxs-lookup"><span data-stu-id="4177f-123">General ledger accounts whose entries will not be transferred</span></span>||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a><span data-ttu-id="4177f-124">Types de coûts sans relation avec la comptabilité générale</span><span class="sxs-lookup"><span data-stu-id="4177f-124">Cost Types Without a Relationship to the General Ledger</span></span>  
<span data-ttu-id="4177f-125">Un type de coût risque de ne pas afficher une relation avec les comptes généraux si une des conditions suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="4177f-125">A cost type may not have a relationship to general ledger accounts if one of the following conditions is true:</span></span>  

* <span data-ttu-id="4177f-126">Les comptes pour la comptabilité opérationnelle, notamment les intérêts et l'amortissement, prennent uniquement les coûts provenant de la comptabilité opérationnelle.</span><span class="sxs-lookup"><span data-stu-id="4177f-126">Accounts for operational accounting, such as Calc. Interest and Depreciation, only take costs from the operational accounting.</span></span>  
* <span data-ttu-id="4177f-127">Les types de coûts, notamment 9901, 9902 et 9903, dans la base de données [!INCLUDE[d365fin](includes/d365fin_md.md)] servent de comptes de crédit et de débit pour les affectations.</span><span class="sxs-lookup"><span data-stu-id="4177f-127">Helping cost types, such as cost types 9901, 9902, and 9903 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, are used as credit and debit accounts for allocations.</span></span>  
* <span data-ttu-id="4177f-128">Le compte 9920 dans la base de données [!INCLUDE[d365fin](includes/d365fin_md.md)] indique les régularisations réelles qui font état de la différence entre les coûts et les frais provenant de la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="4177f-128">The helping account, 9920 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, contains actual accruals that show the difference between costs and the expense from the general ledger.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4177f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4177f-129">See Also</span></span>  
[<span data-ttu-id="4177f-130">Comptabilité pour les coûts</span><span class="sxs-lookup"><span data-stu-id="4177f-130">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="4177f-131">[Paramétrage du contrôle de gestion](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="4177f-131">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
[<span data-ttu-id="4177f-132">À propos de la comptabilité analytique</span><span class="sxs-lookup"><span data-stu-id="4177f-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="4177f-133">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4177f-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

