---
title: "Générer des états financiers à l'aide de tableaux d'analyse"
description: "Décrit comment utiliser des tableaux d'analyse pour créer différentes vues et différents états pour l'analyse des données de performances financières."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: f9f5b3a25a24d4d10c80d048153e68030733bf9e
ms.contentlocale: fr-ch
ms.lasthandoff: 04/18/2018

---
# <a name="work-with-account-schedules"></a><span data-ttu-id="f7e33-103">Utilisation des tableaux d'analyse</span><span class="sxs-lookup"><span data-stu-id="f7e33-103">Work with Account Schedules</span></span>
<span data-ttu-id="f7e33-104">Utilisez les tableaux d'analyse pour obtenir un aperçu des données financières enregistrées dans votre plan comptable.</span><span class="sxs-lookup"><span data-stu-id="f7e33-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="f7e33-105">Les tableaux d'analyse analysent les chiffres des comptes généraux et comparent les écritures comptables et les écritures comptables budget.</span><span class="sxs-lookup"><span data-stu-id="f7e33-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="f7e33-106">Les résultats s'affichent dans les graphiques du tableau de bord, dans le plan de trésorerie, par exemple.</span><span class="sxs-lookup"><span data-stu-id="f7e33-106">The results display in charts on your Role Center, such as the Cash Flow chart.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f7e33-107"> fournit des exemples de tableaux d'analyse que vous pouvez utiliser immédiatement, vous pouvez sinon configurer vos propres lignes et colonnes pour spécifier les chiffres à comparer.</span><span class="sxs-lookup"><span data-stu-id="f7e33-107"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="f7e33-108">Par exemple, vous pouvez créer des tableaux d'analyse pour calculer les marges bénéficiaires dans des axes tels que les départements ou les groupes de clients.</span><span class="sxs-lookup"><span data-stu-id="f7e33-108">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="f7e33-109">Vous pouvez créer autant d'états financiers personnalisés que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="f7e33-109">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="f7e33-110">La configuration de tableaux d'analyse exige une compréhension des données financières du plan comptable.</span><span class="sxs-lookup"><span data-stu-id="f7e33-110">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="f7e33-111">Par exemple, vous pouvez afficher les écritures comptables en tant que pourcentages des écritures budget.</span><span class="sxs-lookup"><span data-stu-id="f7e33-111">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="f7e33-112">Cela suppose que les budgets sont créés.</span><span class="sxs-lookup"><span data-stu-id="f7e33-112">This requires that budgets are created.</span></span> <span data-ttu-id="f7e33-113">Pour plus d'informations, voir [Créer des budgets comptabilité](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="f7e33-113">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="f7e33-114">Catégories de compte et tableaux d'analyse</span><span class="sxs-lookup"><span data-stu-id="f7e33-114">Account Categories and Account Schedules</span></span>
<span data-ttu-id="f7e33-115">Vous pouvez utiliser les catégories de compte pour modifier la présentation de vos états financiers.</span><span class="sxs-lookup"><span data-stu-id="f7e33-115">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="f7e33-116">Une fois que vous avez configuré vos catégories de compte dans la fenêtre **Catégories de compte général**, et que vous sélectionnez l'action **Générer les tableaux d'analyse**, les tableaux d'analyse sous-jacents pour les états financiers de base sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f7e33-116">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="f7e33-117">La prochaine fois que vous exécutez l'un de ces états, par exemple le solde relevé, de nouveaux totaux et des sous-entrées sont ajoutés, en fonction de vos modifications.</span><span class="sxs-lookup"><span data-stu-id="f7e33-117">The next time you run one of these reports, such as the balance statement, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="f7e33-118">Pour plus d'informations, reportez-vous à [Les écritures comptables et le plan comptable](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="f7e33-118">For more information, see [The General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="f7e33-119">Pour créer de nouveaux tableaux d'analyse</span><span class="sxs-lookup"><span data-stu-id="f7e33-119">To create new account schedules</span></span>  
 <span data-ttu-id="f7e33-120">Vous pouvez utiliser des tableaux d'analyse pour analyser les chiffres des comptes généraux ou pour comparer les écritures comptables et les écritures comptables budget.</span><span class="sxs-lookup"><span data-stu-id="f7e33-120">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="f7e33-121">Par exemple, vous pouvez afficher les écritures comptables en tant que pourcentages des écritures budget.</span><span class="sxs-lookup"><span data-stu-id="f7e33-121">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="f7e33-122">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Tableaux d'analyse**, puis choisissez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="f7e33-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f7e33-123">Dans la fenêtre **Noms tableaux d'analyse**, choisissez **Nouveau** pour créer un nom pour le tableau d'analyse.</span><span class="sxs-lookup"><span data-stu-id="f7e33-123">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="f7e33-124">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="f7e33-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="f7e33-125">Choisissez l'action **Modifier tableau d'analyse**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-125">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="f7e33-126">Dans la fenêtre **Tableau d'analyse**, renseignez les champs requis.</span><span class="sxs-lookup"><span data-stu-id="f7e33-126">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="f7e33-127">Une fois que vous avez créé un tableau d'analyse et configuré ses lignes, vous devez configurer ses colonnes.</span><span class="sxs-lookup"><span data-stu-id="f7e33-127">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="f7e33-128">Vous pouvez le faire manuellement ou utiliser une présentation colonne prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="f7e33-128">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="f7e33-129">Choisissez l'action **Modifier paramètres présentation colonne**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-129">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="f7e33-130">Dans la fenêtre **Présentation colonne**, renseignez les champs requis.</span><span class="sxs-lookup"><span data-stu-id="f7e33-130">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f7e33-131">Si vous n'avez affecté aucune présentation colonne par défaut au tableau d'analyse, vous devez configurer les colonnes manuellement.</span><span class="sxs-lookup"><span data-stu-id="f7e33-131">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>   

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="f7e33-132">Pour créer une colonne qui calcule des pourcentages</span><span class="sxs-lookup"><span data-stu-id="f7e33-132">To create a column that calculates percentages</span></span>  
<span data-ttu-id="f7e33-133">Il se peut que vous vouliez inclure une colonne dans un tableau d'analyse pour calculer des pourcentages d'un total.</span><span class="sxs-lookup"><span data-stu-id="f7e33-133">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="f7e33-134">Par exemple, si vous avez plusieurs lignes qui ventilent des ventes par dimension, vous pouvez juger utile de disposer d'une colonne indiquant le pourcentage des ventes totales que représente chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="f7e33-134">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="f7e33-135">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Tableaux d'analyse**, puis choisissez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="f7e33-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="f7e33-136">Dans la fenêtre **Noms tableaux d'analyse**, sélectionnez le tableau d'analyse.</span><span class="sxs-lookup"><span data-stu-id="f7e33-136">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="f7e33-137">Choisissez l'action **Modifier tableau d'analyse** pour configurer une ligne de tableau d'analyse et calculer le total sur lequel le pourcentage sera basé.</span><span class="sxs-lookup"><span data-stu-id="f7e33-137">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="f7e33-138">Insérez une ligne juste au-dessus de la première ligne pour laquelle vous voulez afficher un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="f7e33-138">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="f7e33-139">Renseignez les champs de la ligne comme suit : dans le champ **Type totalisation**, entrez **Base de pourcentage**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-139">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="f7e33-140">Dans le champ **Totalisation**, saisissez une formule pour le total sur lequel le pourcentage sera basé.</span><span class="sxs-lookup"><span data-stu-id="f7e33-140">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="f7e33-141">Par exemple, si la ligne 11 contient le total des ventes, saisissez **11**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-141">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="f7e33-142">Choisissez l'action **Modifier paramètres présentation colonne** pour configurer une colonne.</span><span class="sxs-lookup"><span data-stu-id="f7e33-142">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="f7e33-143">Renseignez les champs de la ligne comme suit : dans le champ **Type colonne**, sélectionnez **Formule**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-143">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="f7e33-144">Dans le champ **Formule**, saisissez une formule correspondant au montant pour lequel vous voulez calculer un pourcentage, suivie de %.</span><span class="sxs-lookup"><span data-stu-id="f7e33-144">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="f7e33-145">Par exemple, si le numéro de colonne N contient le solde période, saisissez **N%**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-145">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="f7e33-146">Répétez les étapes 4 à 7 pour chaque groupe de lignes que vous voulez ventiler par pourcentage.</span><span class="sxs-lookup"><span data-stu-id="f7e33-146">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="f7e33-147">Pour configurer des tableaux d'analyse avec des aperçus</span><span class="sxs-lookup"><span data-stu-id="f7e33-147">To set up account schedules with overviews</span></span>  
<span data-ttu-id="f7e33-148">Vous pouvez utiliser un tableau d'analyse pour créer un état comparant les chiffres de la comptabilité et les chiffres budgétés.</span><span class="sxs-lookup"><span data-stu-id="f7e33-148">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="f7e33-149">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Tableaux d'analyse**, puis choisissez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="f7e33-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="f7e33-150">Dans la fenêtre **Noms tableaux d'analyse**, sélectionnez le tableau d'analyse.</span><span class="sxs-lookup"><span data-stu-id="f7e33-150">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="f7e33-151">Choisissez l'action **Modifier tableau d'analyse**</span><span class="sxs-lookup"><span data-stu-id="f7e33-151">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="f7e33-152">Dans la fenêtre **Tableau d'analyse**, sélectionnez le nom du tableau d'analyse souhaité dans le champ **Nom**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-152">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="f7e33-153">Choisissez l'option **Insérer comptes**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-153">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="f7e33-154">Sélectionnez les comptes à inclure dans votre relevé, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-154">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="f7e33-155">Ces comptes sont à présent insérés dans le tableau d'analyse.</span><span class="sxs-lookup"><span data-stu-id="f7e33-155">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="f7e33-156">Si vous le souhaitez, vous pouvez aussi modifier la présentation colonne.</span><span class="sxs-lookup"><span data-stu-id="f7e33-156">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="f7e33-157">Sélectionnez l'action **Présentation**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-157">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="f7e33-158">Sur le raccourci **Filtres axe**, définissez le filtre budget sur le nom du filtre désiré.</span><span class="sxs-lookup"><span data-stu-id="f7e33-158">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="f7e33-159">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7e33-159">Choose the **OK** button.</span></span>  

<span data-ttu-id="f7e33-160">Vous pouvez maintenant copier et coller votre budget dans un classeur.</span><span class="sxs-lookup"><span data-stu-id="f7e33-160">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="f7e33-161">Comparaison de périodes comptables à l'aide de formules de période</span><span class="sxs-lookup"><span data-stu-id="f7e33-161">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="f7e33-162">Votre tableau d'analyse peut comparer les résultats de différentes périodes comptables, par exemple ce mois et le même mois l'année précédente.</span><span class="sxs-lookup"><span data-stu-id="f7e33-162">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="f7e33-163">Pour ce faire, vous ajoutez une colonne avec le champ **Formule période comparaison**, puis définissez ce champ sur une formule de période.</span><span class="sxs-lookup"><span data-stu-id="f7e33-163">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="f7e33-164">Une période comptable ne doit pas correspondre au calendrier, mais chaque exercice doit avoir le même nombre de périodes comptables, même si chaque période peut varier.</span><span class="sxs-lookup"><span data-stu-id="f7e33-164">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f7e33-165"> utilise la formule de période pour calculer le montant de la période de comparaison en fonction de la période représentée dans le filtre date du formulaire de sélection de l'état.</span><span class="sxs-lookup"><span data-stu-id="f7e33-165"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="f7e33-166">La période de comparaison est basée sur la période de la date de début du filtre de date.</span><span class="sxs-lookup"><span data-stu-id="f7e33-166">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="f7e33-167">Les abréviations utilisées pour les spécifications de période sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f7e33-167">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f7e33-168">Abréviation</span><span class="sxs-lookup"><span data-stu-id="f7e33-168">Abbreviation</span></span></th>
<th><span data-ttu-id="f7e33-169">Désignation</span><span class="sxs-lookup"><span data-stu-id="f7e33-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7e33-170">P</span><span class="sxs-lookup"><span data-stu-id="f7e33-170">P</span></span></p></td>
<td><p><span data-ttu-id="f7e33-171">Période.</span><span class="sxs-lookup"><span data-stu-id="f7e33-171">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e33-172">DP</span><span class="sxs-lookup"><span data-stu-id="f7e33-172">LP</span></span></p></td>
<td><p><span data-ttu-id="f7e33-173">Dernière période de l'exercice, du semestre ou du trimestre.</span><span class="sxs-lookup"><span data-stu-id="f7e33-173">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e33-174">FP</span><span class="sxs-lookup"><span data-stu-id="f7e33-174">CP</span></span></p></td>
<td><p><span data-ttu-id="f7e33-175">Fin de période de l'exercice, du semestre ou du trimestre.</span><span class="sxs-lookup"><span data-stu-id="f7e33-175">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e33-176">EC</span><span class="sxs-lookup"><span data-stu-id="f7e33-176">FY</span></span></p></td>
<td><p><span data-ttu-id="f7e33-177">Exercice comptable.</span><span class="sxs-lookup"><span data-stu-id="f7e33-177">Fiscal year.</span></span> <span data-ttu-id="f7e33-178">Par exemple, EC[1..3] désigne le premier trimestre de l'exercice courant.</span><span class="sxs-lookup"><span data-stu-id="f7e33-178">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f7e33-179">Exemples de formule :</span><span class="sxs-lookup"><span data-stu-id="f7e33-179">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f7e33-180">Formule</span><span class="sxs-lookup"><span data-stu-id="f7e33-180">Formula</span></span></th>
<th><span data-ttu-id="f7e33-181">Désignation</span><span class="sxs-lookup"><span data-stu-id="f7e33-181">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7e33-182">&lt;Vide&gt;</span><span class="sxs-lookup"><span data-stu-id="f7e33-182">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="f7e33-183">Période en cours</span><span class="sxs-lookup"><span data-stu-id="f7e33-183">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e33-184">-1P</span><span class="sxs-lookup"><span data-stu-id="f7e33-184">-1P</span></span></p></td>
<td><p><span data-ttu-id="f7e33-185">Période précédente</span><span class="sxs-lookup"><span data-stu-id="f7e33-185">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e33-186">-1EC[1..DP]</span><span class="sxs-lookup"><span data-stu-id="f7e33-186">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="f7e33-187">Ensemble de l'exercice comptable précédent</span><span class="sxs-lookup"><span data-stu-id="f7e33-187">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e33-188">-1EC</span><span class="sxs-lookup"><span data-stu-id="f7e33-188">-1FY</span></span></p></td>
<td><p><span data-ttu-id="f7e33-189">Période de l'exercice comptable précédent équivalente à la période en cours</span><span class="sxs-lookup"><span data-stu-id="f7e33-189">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e33-190">-1EC[1..3]</span><span class="sxs-lookup"><span data-stu-id="f7e33-190">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="f7e33-191">Premier trimestre de l'exercice comptable précédent</span><span class="sxs-lookup"><span data-stu-id="f7e33-191">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7e33-192">-1EC[1..FP]</span><span class="sxs-lookup"><span data-stu-id="f7e33-192">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="f7e33-193">Du début de l'exercice comptable précédent à la fin de la période de l'exercice comptable précédent incluse</span><span class="sxs-lookup"><span data-stu-id="f7e33-193">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7e33-194">-1EC[FP..DP]</span><span class="sxs-lookup"><span data-stu-id="f7e33-194">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="f7e33-195">De la fin de période de l'exercice précédent à la dernière période de l'exercice comptable précédent incluse</span><span class="sxs-lookup"><span data-stu-id="f7e33-195">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f7e33-196">Pour effectuer des calculs basés par périodes, vous devez entrer une formule dans le champ **Formule date comparaison** à la place.</span><span class="sxs-lookup"><span data-stu-id="f7e33-196">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="f7e33-197">Il n'est pas toujours transparent de déterminer les périodes à comparer, car vous pouvez définir un filtre date sur un état qui couvre des dates différentes des périodes comptables représentées dans les données du plan comptable.</span><span class="sxs-lookup"><span data-stu-id="f7e33-197">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="f7e33-198">Par exemple, vous créez un tableau d'analyse dans lequel vous souhaitez comparer cette période avec la même période l'année précédente. Vous définissez le champ **Filtre période date comparaison** sur *-1EC*.</span><span class="sxs-lookup"><span data-stu-id="f7e33-198">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="f7e33-199">Ensuite, vous exécutez l'état le 28 février et définissez le filtre date sur Janvier et février.</span><span class="sxs-lookup"><span data-stu-id="f7e33-199">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="f7e33-200">Par conséquent, le tableau d'analyse compare les mois de janvier et février de cette année au mois de janvier de l'année précédente, qui est la seule période comptable terminée des deux pour l'année précédente.</span><span class="sxs-lookup"><span data-stu-id="f7e33-200">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="f7e33-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7e33-201">See Also</span></span>
[<span data-ttu-id="f7e33-202">Veille économique</span><span class="sxs-lookup"><span data-stu-id="f7e33-202">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="f7e33-203">Finances</span><span class="sxs-lookup"><span data-stu-id="f7e33-203">Finance</span></span>](finance.md)  
[<span data-ttu-id="f7e33-204">Configuration de Finance</span><span class="sxs-lookup"><span data-stu-id="f7e33-204">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="f7e33-205">Les écritures comptables et le plan comptable</span><span class="sxs-lookup"><span data-stu-id="f7e33-205">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="f7e33-206">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7e33-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

