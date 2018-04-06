---
title: "Procédure pas-à-pas : Créer des prévisions de trésorerie à l'aide des tableaux d'analyse | Microsoft Docs"
description: "Cette procédure pas-à-pas décrit le mode d'utilisation des tableaux d'analyse pour élaborer des prévisions de trésorerie. Les tableaux d'analyse procèdent aux calculs qui ne peuvent pas être effectués directement dans le plan comptable de trésorerie. Dans les tableaux d'analyse, vous pouvez configurer des sous-totaux pour les réceptions et les décaissements de trésorerie. Ces sous-totaux peuvent être inclus dans les nouveaux totaux pour élaborer des prévisions de trésorerie."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 25319bae1d601d6beddca35cf8edc032ac11eda6
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="ac433-106">Procédure pas-à-pas : créer des prévisions de trésorerie à l'aide de tableaux d'analyse</span><span class="sxs-lookup"><span data-stu-id="ac433-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="ac433-107">Cette procédure pas-à-pas décrit le mode d'utilisation des tableaux d'analyse pour élaborer des prévisions de trésorerie.</span><span class="sxs-lookup"><span data-stu-id="ac433-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="ac433-108">Les tableaux d'analyse procèdent aux calculs qui ne peuvent pas être effectués directement dans le plan comptable de trésorerie.</span><span class="sxs-lookup"><span data-stu-id="ac433-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="ac433-109">Dans les tableaux d'analyse, vous pouvez configurer des sous-totaux pour les réceptions et les décaissements de trésorerie.</span><span class="sxs-lookup"><span data-stu-id="ac433-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="ac433-110">Ces sous-totaux peuvent être inclus dans les nouveaux totaux pour élaborer des prévisions de trésorerie.</span><span class="sxs-lookup"><span data-stu-id="ac433-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="ac433-111">À propos de cette procédure pas à pas</span><span class="sxs-lookup"><span data-stu-id="ac433-111">About This Walkthrough</span></span>  
<span data-ttu-id="ac433-112">Cette procédure pas à pas décrit les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="ac433-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="ac433-113">Configuration d'un nouveau nom du tableau d'analyse de trésorerie.</span><span class="sxs-lookup"><span data-stu-id="ac433-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="ac433-114">Configuration de lignes du tableau d'analyse</span><span class="sxs-lookup"><span data-stu-id="ac433-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="ac433-115">Configuration d'une nouvelle présentation de colonne</span><span class="sxs-lookup"><span data-stu-id="ac433-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="ac433-116">Affectation d'une présentation de colonne à un tableau d'analyse.</span><span class="sxs-lookup"><span data-stu-id="ac433-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="ac433-117">Affichage et impression des prévisions de trésorerie.</span><span class="sxs-lookup"><span data-stu-id="ac433-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="ac433-118">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="ac433-118">Prerequisites</span></span>  
<span data-ttu-id="ac433-119">Pour exécuter ce processus pas à pas, vous devez :</span><span class="sxs-lookup"><span data-stu-id="ac433-119">To complete this walkthrough, you will need:</span></span>  

- <span data-ttu-id="ac433-120">Installer [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ac433-120">[!INCLUDE[d365fin](includes/d365fin_md.md)] installed.</span></span>  
- <span data-ttu-id="ac433-121">Les lignes de la feuille d'activité de trésorerie sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="ac433-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="ac433-122">Rôles</span><span class="sxs-lookup"><span data-stu-id="ac433-122">Roles</span></span>  
<span data-ttu-id="ac433-123">Cette procédure pas à pas présente les tâches effectuées par le rôle utilisateur suivant :</span><span class="sxs-lookup"><span data-stu-id="ac433-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="ac433-124">Contrôleur</span><span class="sxs-lookup"><span data-stu-id="ac433-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="ac433-125">Scénario</span><span class="sxs-lookup"><span data-stu-id="ac433-125">Story</span></span>  
<span data-ttu-id="ac433-126">Ken est un contrôleur chez CRONUS, chargé d'élaborer des prévisions mensuelles de trésorerie.</span><span class="sxs-lookup"><span data-stu-id="ac433-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="ac433-127">Il inclut les finances, les ventes, les achats et les immobilisations dans les prévisions, puis les présente à CFO Sara dans un souci de visibilité commerciale.</span><span class="sxs-lookup"><span data-stu-id="ac433-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="ac433-128">Configuration d'un nouveau nom du tableau d'analyse</span><span class="sxs-lookup"><span data-stu-id="ac433-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="ac433-129">Un tableau d'analyse est composé d'un nom de tableau d'analyse de trésorerie avec une série de lignes et une présentation de colonne.</span><span class="sxs-lookup"><span data-stu-id="ac433-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="ac433-130">Pour configurer un nouveau nom de tableau d'analyse</span><span class="sxs-lookup"><span data-stu-id="ac433-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="ac433-131">Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Tableaux d'analyse**, puis choisissez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="ac433-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ac433-132">Dans la fenêtre **Noms tableaux d'analyse**, choisissez **Nouveau** pour créer un nom pour le tableau d'analyse de trésorerie.</span><span class="sxs-lookup"><span data-stu-id="ac433-132">In the **Account Schedule Names** window, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="ac433-133">Dans le champ **Nom**, entrez **Prévision**.</span><span class="sxs-lookup"><span data-stu-id="ac433-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="ac433-134">Dans le champ **Description**, entrez **Prévision de trésorerie**.</span><span class="sxs-lookup"><span data-stu-id="ac433-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="ac433-135">Laissez vierges les champs **Présentation colonne par déf.** et **Nom vue d'analyse** .</span><span class="sxs-lookup"><span data-stu-id="ac433-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="ac433-136">Configuration de lignes du tableau d'analyse</span><span class="sxs-lookup"><span data-stu-id="ac433-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="ac433-137">Après la configuration d'un nom de tableau d'analyse, Ken définit chaque ligne qui s'y affiche.</span><span class="sxs-lookup"><span data-stu-id="ac433-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="ac433-138">Ken définit les lignes qui peuvent être affichées dans les états en plus des lignes destinées uniquement au calcul.</span><span class="sxs-lookup"><span data-stu-id="ac433-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="ac433-139">Pour configurer les lignes du tableau d'analyse</span><span class="sxs-lookup"><span data-stu-id="ac433-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="ac433-140">Dans la fenêtre **Noms tableaux d'analyse**, sélectionnez le nouveau nom du tableau d’analyse **Prévision** que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="ac433-140">In the **Account Schedule Names** window, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="ac433-141">Sous l'onglet **Accueil**, dans le groupe **Processus**, choisissez **Modifier tableau d'analyse**.</span><span class="sxs-lookup"><span data-stu-id="ac433-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="ac433-142">Dans la fenêtre **Tableau d'analyse**, entrez chaque ligne, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ac433-142">In the **Account Schedule** window, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ac433-143">À l’aide de la fonction **Insérer des comptes CF**,vous pouvez sélectionner rapidement les comptes de trésorerie à partir du plan comptable de trésorerie et les copier vers les lignes du tableau d’analyse.</span><span class="sxs-lookup"><span data-stu-id="ac433-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="ac433-144">|N° ligne|Description|Type totalisation|Totalisation|Type ligne|Type montant|Afficher|</span><span class="sxs-lookup"><span data-stu-id="ac433-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="ac433-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Montant|Solde période|Écritures|Montant net|Toujours|</span><span class="sxs-lookup"><span data-stu-id="ac433-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="ac433-146">|C20|Montant jusque date|Solde au|Ecritures|Montant net|Toujours|</span><span class="sxs-lookup"><span data-stu-id="ac433-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="ac433-147">|C30|Exercice complet|Exercice complet|Ecritures|Montant net|Toujours|</span><span class="sxs-lookup"><span data-stu-id="ac433-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="ac433-148">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac433-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="ac433-149">Affectation de la présentation de colonne au nom de tableau d'analyse</span><span class="sxs-lookup"><span data-stu-id="ac433-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="ac433-150">Ken est désormais prêt à affecter la présentation de colonne au nom de tableau d'analyse.</span><span class="sxs-lookup"><span data-stu-id="ac433-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="ac433-151">Pour affecter la présentation de colonne au nom de tableau d'analyse</span><span class="sxs-lookup"><span data-stu-id="ac433-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="ac433-152">Dans la fenêtre **Noms tableaux d'analyse**, sélectionnez **Prévision** dans le champ **Nom**.</span><span class="sxs-lookup"><span data-stu-id="ac433-152">In the **Account Schedule Names** window, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="ac433-153">Dans le champ **Présentation colonne par déf.**, sélectionnez la présentation de colonne **Trésorerie** pour la définir par défaut.</span><span class="sxs-lookup"><span data-stu-id="ac433-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="ac433-154">Pour afficher et imprimer les prévisions de trésorerie</span><span class="sxs-lookup"><span data-stu-id="ac433-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="ac433-155">Dans la fenêtre **Noms tableaux d'analyse**, choisissez l'action **Aperçu** pour afficher les prévisions de trésorerie.</span><span class="sxs-lookup"><span data-stu-id="ac433-155">In the **Account Schedule Names** window, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="ac433-156">Dans la fenêtre **Aperçu tableau d'analyse**, vous pouvez sélectionner un montant, puis afficher les écritures de prévisions de trésorerie qui constituent ce montant.</span><span class="sxs-lookup"><span data-stu-id="ac433-156">In the **Acc. Schedule Overview** window, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="ac433-157">En outre, vous pouvez afficher la formule qui est utilisée pour calculer le montant.</span><span class="sxs-lookup"><span data-stu-id="ac433-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="ac433-158">Vous pouvez également filtrer les montants par date et par axe analytique.</span><span class="sxs-lookup"><span data-stu-id="ac433-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="ac433-159">Choisissez l'action **Imprimer** pour imprimer les prévisions de trésorerie.</span><span class="sxs-lookup"><span data-stu-id="ac433-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ac433-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac433-160">See Also</span></span>  
 <span data-ttu-id="ac433-161">[Utilisation des tableaux d'analyse](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="ac433-161">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="ac433-162">Procédures pas à pas liées au processus entreprise</span><span class="sxs-lookup"><span data-stu-id="ac433-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="ac433-163">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ac433-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

