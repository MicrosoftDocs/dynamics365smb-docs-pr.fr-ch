---
title: "Définition des ventilations statiques en fonction du ratio d'affectation | Microsoft Docs"
description: "Le mode de ventilation statique dépend d'une valeur définie, par exemple, les mètres carrés utilisés ou un ratio de ventilation prédéfini, comme 5:2:4."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9b58c3889196cba3a6ddbeb50249a6ae962c4ea1
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a><span data-ttu-id="f08c9-103">Exemple de scénario : Définition des ventilations statiques en fonction du ratio d'affectation</span><span class="sxs-lookup"><span data-stu-id="f08c9-103">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>
<span data-ttu-id="f08c9-104">Le mode de ventilation statique dépend d'une valeur définie, par exemple, les mètres carrés utilisés ou un ratio de ventilation prédéfini, comme 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="f08c9-104">Static allocation method is based on a definite value, such as square meters used, or an established allocation ratio such as 5:2:4.</span></span>  

<span data-ttu-id="f08c9-105">Cette rubrique décrit comment définir trois nouveaux coûts associés pour la cibles d'affectation pour le centre de coûts PROD de la source d'affectation à l'aide d'un ratio de ventilation prédéfini, comme 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="f08c9-105">This topic describes how to define three new allocation target cost objects for the allocation source PROD cost center using the established allocation ratio 5:2:4.</span></span> <span data-ttu-id="f08c9-106">Les trois coûts associés cibles sont ACCESSO, PEINTURE et ACCESSOIRES.</span><span class="sxs-lookup"><span data-stu-id="f08c9-106">The three target cost objects are ACCESSO, PAINT, and FITTINGS.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f08c9-107">L'exemple utilise les données de démonstration dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f08c9-107">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><span data-ttu-id="f08c9-108">Pour définir le centre de coûts PROD de la source d'affectation sur le raccourci Général</span><span class="sxs-lookup"><span data-stu-id="f08c9-108">To define the allocation source PROD cost center on the General FastTab</span></span>  

1.  <span data-ttu-id="f08c9-109">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Affectation des coûts**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f08c9-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Allocation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f08c9-110">Dans la fenêtre **Affectation des coûts**, sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-110">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="f08c9-111">Dans le champ **ID**, appuyez sur Entrée ou saisissez un ID.</span><span class="sxs-lookup"><span data-stu-id="f08c9-111">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="f08c9-112">Dans le champ **Niveau**, saisissez **1**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-112">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="f08c9-113">Dans les champs **Valide à partir de** et **Valide jusque**, entrez les dates appropriées.</span><span class="sxs-lookup"><span data-stu-id="f08c9-113">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="f08c9-114">Dans le champ **Code centre de coûts**, entrez **PROD**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-114">In the **Cost Center Code** field, enter **PROD**.</span></span>  
7.  <span data-ttu-id="f08c9-115">Dans le champ **Type de crédit\\\/coût**, entrez le type de coût **9903**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-115">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><span data-ttu-id="f08c9-116">Pour définir les coûts associés de la cible d'affectation sur le raccourci Lignes</span><span class="sxs-lookup"><span data-stu-id="f08c9-116">To define the allocation target cost objects on the Lines FastTab</span></span>  

1.  <span data-ttu-id="f08c9-117">Sur la première ligne facture, dans le champ **Type coût cible**, saisissez **9903**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-117">On the first line, in the **Target Cost Type** field, enter **9903**.</span></span>  
2.  <span data-ttu-id="f08c9-118">Sur la première ligne facture, dans le champ **Coûts associés cibles**, saisissez **ACCESSO**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-118">On the first line, in the **Target Cost Object** field, select **ACCESSO**.</span></span>  
3.  <span data-ttu-id="f08c9-119">Sur la première ligne, dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d'affectation de tous les coûts cumulés.</span><span class="sxs-lookup"><span data-stu-id="f08c9-119">On the first line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
4.  <span data-ttu-id="f08c9-120">Sur la première ligne, dans le champ **Base**, sélectionnez **Statique** pour utiliser le mode de ventilation statique.</span><span class="sxs-lookup"><span data-stu-id="f08c9-120">On the first line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
5.  <span data-ttu-id="f08c9-121">Sur la première ligne, dans le champ **Part**, saisissez le ratio d'affectation **5**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-121">On the first line, in the **Share** field, enter the allocation ratio **5**.</span></span>  
6.  <span data-ttu-id="f08c9-122">Sur la deuxième ligne, dans le champ **Type coût cible**, saisissez **9903**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-122">On the second line, in the **Target Cost Type** field, enter **9903**.</span></span>  
7.  <span data-ttu-id="f08c9-123">Sur la deuxième ligne, dans le champ **Coûts associés cibles**, saisissez **PEINTURE**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-123">On the second line, in the **Target Cost Object** field, select **PAINT**.</span></span>  
8.  <span data-ttu-id="f08c9-124">Sur la deuxième ligne, dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d'affectation de tous les coûts cumulés.</span><span class="sxs-lookup"><span data-stu-id="f08c9-124">On the second line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
9. <span data-ttu-id="f08c9-125">Sur la deuxième ligne, dans le champ **Base**, sélectionnez **Statique** pour utiliser le mode de ventilation statique.</span><span class="sxs-lookup"><span data-stu-id="f08c9-125">On the second line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
10. <span data-ttu-id="f08c9-126">Sur la deuxième ligne, dans le champ **Part**, saisissez le ratio d'affectation **2**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-126">On the second line, in the **Share** field, enter the allocation ratio **2**.</span></span>  
11. <span data-ttu-id="f08c9-127">Sur la troisième ligne, dans le champ **Type coût cible**, saisissez **9903**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-127">On the third line, in the **Target Cost Type** field, enter **9903**.</span></span>  
12. <span data-ttu-id="f08c9-128">Sur la troisième ligne facture, dans le champ **Coûts associés cibles**, saisissez **ACCESSOIRES**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-128">On the third line, in the **Target Cost Object** field, select **FITTINGS**.</span></span>  
13. <span data-ttu-id="f08c9-129">Sur la troisième ligne, dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d'affectation de tous les coûts cumulés.</span><span class="sxs-lookup"><span data-stu-id="f08c9-129">On the third line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
14. <span data-ttu-id="f08c9-130">Sur la troisième ligne, dans le champ **Base**, sélectionnez **Statique** pour utiliser le mode de ventilation statique.</span><span class="sxs-lookup"><span data-stu-id="f08c9-130">On the third line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
15. <span data-ttu-id="f08c9-131">Sur la troisième ligne, dans le champ **Part**, saisissez le ratio d'affectation **4**.</span><span class="sxs-lookup"><span data-stu-id="f08c9-131">On the third line, in the **Share** field, enter the allocation ratio **4**.</span></span>  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="f08c9-132">calcule automatiquement le champ **Pour cent** à l'aide d'un pourcentage qui dépend de ces trois ratios d'affectation saisis dans le champ **Part** pour chacune des trois lignes.</span><span class="sxs-lookup"><span data-stu-id="f08c9-132">automatically calculates the **Percent** field using a percentage rate that is dependent on all three allocation ratios that are entered in the **Share** field for all three lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f08c9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f08c9-133">See Also</span></span>  
<span data-ttu-id="f08c9-134">[Configurer la source d'affectation et ses cibles](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="f08c9-134">[Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
<span data-ttu-id="f08c9-135">[Définition et répartition des coûts](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="f08c9-135">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
<span data-ttu-id="f08c9-136">[Exemple de scénario : définition des ventilations dynamiques sur la base des articles vendus](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span><span class="sxs-lookup"><span data-stu-id="f08c9-136">[Scenario Example: Defining Dynamic Allocations Based on Items Sold](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span></span>  
[<span data-ttu-id="f08c9-137">Définition et répartition des coûts</span><span class="sxs-lookup"><span data-stu-id="f08c9-137">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)

