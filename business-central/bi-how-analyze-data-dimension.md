---
title: Analyse des données par axe analytique| Microsoft Docs
description: Décrit comment analyser les diverses données métier par axe analytique.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 11/13/2018
ms.author: sgroespe
ms.openlocfilehash: bfb5ce68e4570f4d96a4216ea01f9d1ecc3bc623
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820723"
---
#  <a name="analyze-data-by-dimensions"></a><span data-ttu-id="50d1d-103">Analyse des données par axe analytique</span><span class="sxs-lookup"><span data-stu-id="50d1d-103">Analyze Data by Dimensions</span></span>
<span data-ttu-id="50d1d-104">En analyse financière, un axe correspond à des données que vous pouvez ajouter à une écriture comme une sorte de marqueur.</span><span class="sxs-lookup"><span data-stu-id="50d1d-104">In financial analysis, a dimension is data that you can add to an entry as a kind of marker.</span></span> <span data-ttu-id="50d1d-105">Ces données permettent de regrouper des écritures dotées de caractéristiques similaires, telles que les clients, les régions, les produits et les commerciaux, et de récupérer facilement ces groupes à des fins d'analyse.</span><span class="sxs-lookup"><span data-stu-id="50d1d-105">This data is used to group entries with similar characteristics, such as customers, regions, products, and salesperson, and easily retrieve these groups for analysis.</span></span> <span data-ttu-id="50d1d-106">Les axes peuvent être utilisés sur des écritures de feuilles, de documents et de budgets.</span><span class="sxs-lookup"><span data-stu-id="50d1d-106">Dimensions can be used on entries in journals, documents, and budgets.</span></span> <span data-ttu-id="50d1d-107">Le terme Axe décrit la manière dont l'analyse est effectuée.</span><span class="sxs-lookup"><span data-stu-id="50d1d-107">The term dimension describes how analysis occurs.</span></span> <span data-ttu-id="50d1d-108">Une analyse à deux axes, par exemple, est une analyse des ventes par zone.</span><span class="sxs-lookup"><span data-stu-id="50d1d-108">A two-dimensional analysis, for example, would be sales per area.</span></span> <span data-ttu-id="50d1d-109">Cependant, si vous utilisez plus de deux axes analytiques lors de la création d'une écriture, vous pouvez mener une analyse plus complexe, telle que des ventes par campagne de vente, par groupe client et par zone.</span><span class="sxs-lookup"><span data-stu-id="50d1d-109">However, by using more than two dimensions when creating an entry, you can carry out a more complex analysis, such as sales per sales campaign per customer group per area.</span></span> <span data-ttu-id="50d1d-110">Pour plus d'informations, reportez-vous à [Utilisation des axes](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="50d1d-110">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

<span data-ttu-id="50d1d-111">L'analyse de données par axes vous permet d'obtenir un meilleur aperçu de votre activité commerciale, ce qui vous permet d'évaluer les informations, telles que la mesure du bon fonctionnement de votre société, les domaines dans lesquels elle prospère ou non, et ceux dans lesquels il est nécessaire d'affecter davantage de ressources.</span><span class="sxs-lookup"><span data-stu-id="50d1d-111">Analyzing data by dimensions gives you greater insight into your business, so you can evaluate information, such as how well your business is operating, where it is thriving and where it is not, and where more resources should be allocated.</span></span>

> [!TIP]
> <span data-ttu-id="50d1d-112">Pour analyser rapidement les données transactionnelles par dimensions, vous pouvez filtrer les totaux du plan comptable et les entrées de toutes les pages **Entrées** par dimensions.</span><span class="sxs-lookup"><span data-stu-id="50d1d-112">As a quick way to analyze transactional data by dimensions, you can filter totals in the chart of accounts and entries in all **Entries** pages by dimensions.</span></span> <span data-ttu-id="50d1d-113">Recherchez l'action **Définir le filtre axe**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-113">Look for the **Set Dimension Filter** action.</span></span>

## <a name="to-set-up-an-analysis-view"></a><span data-ttu-id="50d1d-114">Pour configurer une vue d'analyse :</span><span class="sxs-lookup"><span data-stu-id="50d1d-114">To set up an analysis view</span></span>  
<span data-ttu-id="50d1d-115">Les vues analytiques affichent une combinaison sélectionnée d'axes analytiques.</span><span class="sxs-lookup"><span data-stu-id="50d1d-115">An analysis by dimensions displays a selected combination of dimensions.</span></span> <span data-ttu-id="50d1d-116">Vous pouvez stocker et récupérer chaque analyse que vous avez configurée.</span><span class="sxs-lookup"><span data-stu-id="50d1d-116">You can store and retrieve each analysis you have set up.</span></span> <span data-ttu-id="50d1d-117">Les informations de configuration des vues analytiques sont stockées sur des fiches **Vue d'analyse** afin de simplifier une éventuelle analyse ultérieure.</span><span class="sxs-lookup"><span data-stu-id="50d1d-117">The information for setting up an analysis is stored on an **Analysis View** card to simplify future analysis.</span></span>  

1. <span data-ttu-id="50d1d-118">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Vues d'analyse**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="50d1d-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Analysis Views**, and then choose the related link.</span></span>  
2. <span data-ttu-id="50d1d-119">Sur la page **Liste des vues d'analyse**, cliquez sur l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-119">On the **Analysis View List** page, choose the **New** action.</span></span>
3. <span data-ttu-id="50d1d-120">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="50d1d-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="50d1d-121">Pour ajouter des codes axe aux quatre codes du raccourci **Axes analytiques**, cliquez sur **Filtre**, renseignez les champs et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-121">To add other dimension codes in addition to the four on the **Dimensions** FastTab, choose the **Filter** action, fill in the fields, and then choose the **OK** button.</span></span>  
5. <span data-ttu-id="50d1d-122">Pour mettre à jour la vue, choisissez l'action **Mettre à jour**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-122">To update the view, choose the **Update** action.</span></span>

## <a name="to-analyze-by-dimensions"></a><span data-ttu-id="50d1d-123">Pour effectuer une analyse par axe analytique</span><span class="sxs-lookup"><span data-stu-id="50d1d-123">To analyze by dimensions</span></span>
<span data-ttu-id="50d1d-124">La matrice **Vues analytiques** peut vous permettre de consulter les montants de votre comptabilité à l'aide des vues d'analyse que vous avez déjà configurées.</span><span class="sxs-lookup"><span data-stu-id="50d1d-124">You can use the **Analysis by Dimensions** matrix to view the amounts in your general ledger by using the analysis views that you have already set up.</span></span> <span data-ttu-id="50d1d-125">Complétez la page **Vues analytiques** pour définir les éléments affichés dans la matrice, puis choisissez l'action **Afficher matrice** pour afficher la matrice.</span><span class="sxs-lookup"><span data-stu-id="50d1d-125">You fill on the **Analysis by Dimensions** page to define what will be shown in the matrix, and then you choose the **Show Matrix** action to view the matrix.</span></span>  

1. <span data-ttu-id="50d1d-126">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Vues d'analyse**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="50d1d-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Analysis Views**, and then choose the related link.</span></span>  
2. <span data-ttu-id="50d1d-127">Sélectionnez la vue d'analyse appropriée et choisissez l'action **Vues analytiques**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-127">Select the relevant analysis view,  and then choose the **Analysis by Dimensions** action.</span></span>
3. <span data-ttu-id="50d1d-128">Sur la page **Analyse vente par axe analytique**, renseignez les champs pour définir les données affichées et leur présentation.</span><span class="sxs-lookup"><span data-stu-id="50d1d-128">On the **Analysis by Dimensions** page, fill in the fields to define which data is shown and how.</span></span>
4. <span data-ttu-id="50d1d-129">Choisissez l'action **Afficher matrice** pour ouvrir la page matricielle respective de la vue d'analyse définie.</span><span class="sxs-lookup"><span data-stu-id="50d1d-129">Choose the **Show Matrix** action to open the respective matrix page for the defined analysis view.</span></span>
5. <span data-ttu-id="50d1d-130">Pour visualiser la spécification d'un montant affiché sur la page matricielle, sélectionnez le montant à explorer.</span><span class="sxs-lookup"><span data-stu-id="50d1d-130">To see a specification of an amount shown in the matrix page, choose the amount to drill down.</span></span>  

- <span data-ttu-id="50d1d-131">Les colonnes les plus à gauche contiennent des informations basées sur l'option sélectionnée dans le champ **Afficher lignes** de l'en-tête.</span><span class="sxs-lookup"><span data-stu-id="50d1d-131">The leftmost columns contain information based on what you have selected in the **Show as Lines** field in the header.</span></span>  
- <span data-ttu-id="50d1d-132">Les colonnes les plus à droite contiennent des informations basées sur l'option sélectionnée dans le champ **Afficher colonnes** de l'en-tête.</span><span class="sxs-lookup"><span data-stu-id="50d1d-132">The rightmost columns contain information based on to what you have selected in the **Show as Columns** field in the header.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="50d1d-133">Vous ne pouvez pas sélectionner une période plus courte que celle indiquée en tant que compression date sur la fiche **Vue d'analyse**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-133">You cannot select a period length shorter than the period specified for the date compression on the **Analysis View** card.</span></span> <span data-ttu-id="50d1d-134">Les commandes **Jeu suivant** et **Jeu précédent** ne sont pas actives si vous avez sélectionné **Période** dans le champ **Afficher lignes** ou **Afficher colonnes**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-134">The **Next Set** and **Previous Set** commands are inactive if you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="50d1d-135">Vous pouvez utiliser l'état **Axes analytiques - Détail** pour répertorier de manière détaillée les différentes utilisations des axes analytiques sur les écritures au cours d'une période.</span><span class="sxs-lookup"><span data-stu-id="50d1d-135">You can use the **Dimensions - Detail** report to display a detailed classification of how dimensions have been used on entries over a selected period.</span></span> <span data-ttu-id="50d1d-136">Vous pouvez utiliser l'état **Axes analytiques - Total** pour afficher uniquement les montants totaux.</span><span class="sxs-lookup"><span data-stu-id="50d1d-136">You can use the **Dimensions - Total** report to display only the total amounts.</span></span>  

> [!TIP]  
>   <span data-ttu-id="50d1d-137">Vous pouvez également modifier la vue en changeant la valeur des champs **Afficher lignes** et **Afficher colonnes**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-137">You can also change the view by changing the contents of the **Show as Lines** field and **Show as Columns** field.</span></span> <span data-ttu-id="50d1d-138">Pour contrepasser un paramètre de vue, choisissez l'action **Inverser lignes et colonnes**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-138">To reverse a view setting, choose the **Reverse Lines and Columns** action.</span></span>

## <a name="to-update-an-analysis-view"></a><span data-ttu-id="50d1d-139">Pour mettre à jour une vue d'analyse</span><span class="sxs-lookup"><span data-stu-id="50d1d-139">To update an analysis view</span></span>  
<span data-ttu-id="50d1d-140">Les montants affichés sur la page **Vues analytiques** offrent une image de l'état de la société au moment de la dernière mise à jour.</span><span class="sxs-lookup"><span data-stu-id="50d1d-140">The amounts that are displayed on the **Analysis by Dimensions** page give you a picture of the company’s state at the time of the last update.</span></span> <span data-ttu-id="50d1d-141">Pour obtenir une image de l'état actuel, vous devez actualiser la vue d'analyse en exécutant l'option de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="50d1d-141">To get a picture of the current state, you must update the analysis view by running the update function.</span></span>

<span data-ttu-id="50d1d-142">La procédure suivante permet de mettre à jour une vue d'analyse à partir de la page **Vues analytiques**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-142">The following procedure is for updating an analysis view from the **Analysis by Dimensions** page.</span></span> <span data-ttu-id="50d1d-143">Les étapes sont similaires entre les pages **Fiche vue d'analyse** et les pages **Liste des vues d'analyse**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-143">The steps are similar from the **Analysis View Card** and the **Analysis View List** pages.</span></span>  

1. <span data-ttu-id="50d1d-144">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Vues d'analyse**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="50d1d-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Analysis Views**, and then choose the related link.</span></span>
2. <span data-ttu-id="50d1d-145">Sélectionnez la vue d'analyse appropriée et choisissez l'action **Vues analytiques**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-145">Select the relevant analysis view,  and then choose the **Analysis by Dimensions** action.</span></span>
2. <span data-ttu-id="50d1d-146">Sur la page **Vues analytiques**, sélectionnez le champ **Code vue analytique**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-146">On the **Analysis by Dimensions** page, choose the **Analysis View Code** field.</span></span>  
3. <span data-ttu-id="50d1d-147">Sélectionnez la ligne contenant la vue d'analyse appropriée.</span><span class="sxs-lookup"><span data-stu-id="50d1d-147">Select the line with the relevant analysis view.</span></span>  
4. <span data-ttu-id="50d1d-148">Sur la page **Vues analytiques**, sélectionnez la vue d'analyse, puis l'action **Mettre à jour**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-148">On the **Analysis Views** page, select the analysis view, and then choose the **Update** action.</span></span>  

> [!TIP]  
>   <span data-ttu-id="50d1d-149">Si vous activez la case à cocher **Mise à jour à la validation** sur la fiche vue d'analyse, la vue est automatiquement mise à jour lorsqu'une transaction concernée est validée.</span><span class="sxs-lookup"><span data-stu-id="50d1d-149">If you select the **Update on Posting** check box on an analysis view card, the view is automatically updated when an involved transaction is posted.</span></span>

> [!NOTE]  
>   <span data-ttu-id="50d1d-150">Pour mettre à jour tout ou partie des vues d'analyse en même temps, vous devez utiliser le traitement par lots **Mise à jour vues d'analyse**.</span><span class="sxs-lookup"><span data-stu-id="50d1d-150">To update some or all analysis views at the same time, you must use the **Update Analysis Views** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="50d1d-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50d1d-151">See Also</span></span>
[<span data-ttu-id="50d1d-152">Veille économique</span><span class="sxs-lookup"><span data-stu-id="50d1d-152">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="50d1d-153">Finances</span><span class="sxs-lookup"><span data-stu-id="50d1d-153">Finance</span></span>](finance.md)  
[<span data-ttu-id="50d1d-154">Configuration de Finance</span><span class="sxs-lookup"><span data-stu-id="50d1d-154">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="50d1d-155">Les écritures comptables et le plan comptable</span><span class="sxs-lookup"><span data-stu-id="50d1d-155">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="50d1d-156">Utilisation des axes analytiques</span><span class="sxs-lookup"><span data-stu-id="50d1d-156">Working with Dimensions</span></span>](finance-dimensions.md)  
<span data-ttu-id="50d1d-157">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="50d1d-157">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  