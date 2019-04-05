---
title: Analyse des montants réalisés et des montants budgétés| Microsoft Docs
description: Décrit comment analyser les montants réalisés et les montants budgétés.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: b21354a29c275013b7832459daec392efa6d751d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820215"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="12c5d-103">Analyser les montants réalisés et les montants budgétés</span><span class="sxs-lookup"><span data-stu-id="12c5d-103">Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="12c5d-104">Lors de la collecte, l'analyse, et le partage des données de votre société, vous voyez les montants réels comparés aux montants budgétés de tous les comptes et pour plusieurs périodes.</span><span class="sxs-lookup"><span data-stu-id="12c5d-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="12c5d-105">Pour analyser les montants budgétés, vous devez d'abord créer des budgets comptabilité.</span><span class="sxs-lookup"><span data-stu-id="12c5d-105">To analyze budgeted amounts, you must first create G(L budgets.</span></span> <span data-ttu-id="12c5d-106">Pour plus d'informations, voir [Créer des budgets comptabilité](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="12c5d-106">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="to-view-a-gl-budget"></a><span data-ttu-id="12c5d-107">Pour visualiser un budget comptabilité</span><span class="sxs-lookup"><span data-stu-id="12c5d-107">To view a G/L budget</span></span>
<span data-ttu-id="12c5d-108">Dans un budget doté d'axes, vous pouvez filtrer les écritures et visualiser des budgets spécifiques.</span><span class="sxs-lookup"><span data-stu-id="12c5d-108">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="12c5d-109">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Budgets**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="12c5d-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="12c5d-110">Sur la page **Budgets**, ouvrez le budget que vous souhaitez visualiser.</span><span class="sxs-lookup"><span data-stu-id="12c5d-110">On the **G/L Budgets** page, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="12c5d-111">En haut de la page, renseignez les champs nécessaires pour définir ce qui est affiché.</span><span class="sxs-lookup"><span data-stu-id="12c5d-111">At the top of the page, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="12c5d-112">Si vous avez sélectionné **Période** dans le champ **Afficher lignes** ou **Afficher colonnes**, puis vous devez renseigner le champ **Afficher par**.</span><span class="sxs-lookup"><span data-stu-id="12c5d-112">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="12c5d-113">Si vous n'avez pas sélectionné **Période** dans le champ **Afficher lignes** ou **Afficher colonnes**, entrez la période appropriée dans le champ **Filtre date**.</span><span class="sxs-lookup"><span data-stu-id="12c5d-113">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="12c5d-114">Seules les écritures budget en comptabilité contenant les codes filtre entrés sur le raccourci **Filtres** sont incluses dans le calcul.</span><span class="sxs-lookup"><span data-stu-id="12c5d-114">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="12c5d-115">Les écritures budget contenant d'autres codes filtre ou ne contenant aucun code filtre sont exclues.</span><span class="sxs-lookup"><span data-stu-id="12c5d-115">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="12c5d-116">Tant que le filtre est présent sur la page, le budget n'affiche que les écritures budget contenant ces codes filtre.</span><span class="sxs-lookup"><span data-stu-id="12c5d-116">As long as the filter remains on the page, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="12c5d-117">Si vous souhaitez modifier le budget, vous pouvez modifier les écritures budget.</span><span class="sxs-lookup"><span data-stu-id="12c5d-117">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="12c5d-118">Choisissez un montant pour afficher les écritures Budget sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="12c5d-118">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="12c5d-119">Pour afficher les montants budgétés et réalisés de tous les comptes</span><span class="sxs-lookup"><span data-stu-id="12c5d-119">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="12c5d-120">Vous pouvez afficher des budgets et les comparer aux chiffres réels dans différents modules de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="12c5d-120">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="12c5d-121">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="12c5d-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="12c5d-122">Sur la page **Plan comptable**, choisissez l'action **Réalisé/Budget par compte**.</span><span class="sxs-lookup"><span data-stu-id="12c5d-122">On the **Chart of Accounts** page, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="12c5d-123">En haut de la page, renseignez les champs nécessaires pour définir ce qui est affiché.</span><span class="sxs-lookup"><span data-stu-id="12c5d-123">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="12c5d-124">Pour voir le détail d'un montant affiché, sélectionnez ce champ.</span><span class="sxs-lookup"><span data-stu-id="12c5d-124">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="12c5d-125">Les filtres que vous définissez dans l'en-tête de la page sont appliqués aux écritures comptables et aux écritures budget.</span><span class="sxs-lookup"><span data-stu-id="12c5d-125">The filters you set on the page header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="12c5d-126">Les colonnes les plus à gauche contiennent le plan comptable.</span><span class="sxs-lookup"><span data-stu-id="12c5d-126">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="12c5d-127">Sur les cinq colonnes les plus à droite, les quatre premières affichent les montants crédit et débit budgétés, et réalisés pour chaque compte.</span><span class="sxs-lookup"><span data-stu-id="12c5d-127">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="12c5d-128">La cinquième colonne indique la relation proportionnelle entre les montants budgétés et réalisés sur le compte général.</span><span class="sxs-lookup"><span data-stu-id="12c5d-128">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="12c5d-129">Le champ **Afficher par** de la page **Réalisé/Budget par compte** permet de sélectionner la longueur de la période.</span><span class="sxs-lookup"><span data-stu-id="12c5d-129">Use the **View by** field on the **G/L Balance/Budget** page to select the period length.</span></span> <span data-ttu-id="12c5d-130">Le champ **Afficher en tant que** permet de sélectionner le mode de calcul des montants, à savoir **Solde période** ou **Solde au**.</span><span class="sxs-lookup"><span data-stu-id="12c5d-130">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="12c5d-131">Choisissez **Période précédente** ou **Période suivante** pour changer de période.</span><span class="sxs-lookup"><span data-stu-id="12c5d-131">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="12c5d-132">Pour afficher les montants budgétés et réalisés de plusieurs périodes</span><span class="sxs-lookup"><span data-stu-id="12c5d-132">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="12c5d-133">Au lieu de visualiser les montants budgétés et réalisés de tous les comptes au sein d'une seule période, vous pouvez afficher un certain nombre de périodes pour un seul compte.</span><span class="sxs-lookup"><span data-stu-id="12c5d-133">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="12c5d-134">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="12c5d-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="12c5d-135">Sur la page **Plan comptable**, sélectionnez le compte général approprié, puis choisissez l'action **Réalisé/Budget compte général**.</span><span class="sxs-lookup"><span data-stu-id="12c5d-135">On the **Chart of Accounts** page, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="12c5d-136">En haut de la page, renseignez les champs nécessaires pour définir ce qui est affiché.</span><span class="sxs-lookup"><span data-stu-id="12c5d-136">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="12c5d-137">Pour voir le détail d'un montant affiché, sélectionnez ce champ.</span><span class="sxs-lookup"><span data-stu-id="12c5d-137">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="12c5d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12c5d-138">See Also</span></span>
[<span data-ttu-id="12c5d-139">Veille économique</span><span class="sxs-lookup"><span data-stu-id="12c5d-139">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="12c5d-140">Utilisation des tableaux d'analyse</span><span class="sxs-lookup"><span data-stu-id="12c5d-140">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
[<span data-ttu-id="12c5d-141">Finances</span><span class="sxs-lookup"><span data-stu-id="12c5d-141">Finance</span></span>](finance.md)  
[<span data-ttu-id="12c5d-142">Configuration de Finance</span><span class="sxs-lookup"><span data-stu-id="12c5d-142">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="12c5d-143">Les écritures comptables et le plan comptable</span><span class="sxs-lookup"><span data-stu-id="12c5d-143">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="12c5d-144">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="12c5d-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
