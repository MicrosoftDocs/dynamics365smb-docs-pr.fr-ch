---
title: Paramétrer l'amortissement| Microsoft Docs
description: Vous spécifiez dans une loi d'amortissement comment vous souhaitez amortir ou déprécier les immobilisations.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: d417db84cf45356925cf52a36ba08e478b8ee6b9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821027"
---
# <a name="set-up-fixed-asset-depreciation"></a><span data-ttu-id="aa650-103">Configurer un amortissement immobilisation</span><span class="sxs-lookup"><span data-stu-id="aa650-103">Set Up Fixed Asset Depreciation</span></span>
 <span data-ttu-id="aa650-104">Vous pouvez utiliser plusieurs méthodes d'amortissement pour préparer les états financiers et les déclarations de revenus.</span><span class="sxs-lookup"><span data-stu-id="aa650-104">You can use various methods of depreciation for preparing financial statements and income tax returns.</span></span> <span data-ttu-id="aa650-105">De nombreuses sociétés de grande taille utilisent la méthode de l'amortissement linéaire dans leurs états financiers car elle permet généralement la déclaration des bénéfices supérieurs.</span><span class="sxs-lookup"><span data-stu-id="aa650-105">Many large corporations use straight-line depreciation in their financial statements because this generally permits reporting higher earnings.</span></span> <span data-ttu-id="aa650-106">Toutefois, dans le cadre de l'impôt sur le revenu, la plupart des entreprises utilise une méthode d'amortissement accélérée.</span><span class="sxs-lookup"><span data-stu-id="aa650-106">For income tax purposes, however, many businesses use an accelerated depreciation method.</span></span> <span data-ttu-id="aa650-107">Pour en savoir plus, voir [Méthodes d'amortissement](fa-depreciation-methods.md).</span><span class="sxs-lookup"><span data-stu-id="aa650-107">For more information, see [Depreciation Methods](fa-depreciation-methods.md).</span></span>

 <span data-ttu-id="aa650-108">Lorsque vous avez créé les lois d'amortissement nécessaires, vous devez en attribuer au moins une à chaque immobilisation.</span><span class="sxs-lookup"><span data-stu-id="aa650-108">When you have created the relevant depreciation books, you must assign one or more depreciation books to each fixed asset.</span></span> <span data-ttu-id="aa650-109">La loi d'amortissement attribuée à une immobilisation est désignée comme loi d'amortissement immobilisation.</span><span class="sxs-lookup"><span data-stu-id="aa650-109">A depreciation book that is assigned to a fixed asset is referred to as a fixed asset depreciation book.</span></span> <span data-ttu-id="aa650-110">Par conséquent, la page pour les lois d'amortissement attribuées est intitulée **Lois d'amortissement immo.**.</span><span class="sxs-lookup"><span data-stu-id="aa650-110">Accordingly, the page for assigned depreciation books is called **FA Depreciation Books**.</span></span>

## <a name="to-create-a-depreciation-book"></a><span data-ttu-id="aa650-111">Pour créer une loi d'amortissement</span><span class="sxs-lookup"><span data-stu-id="aa650-111">To create a depreciation book</span></span>
<span data-ttu-id="aa650-112">Dans une loi d'amortissement immobilisation, vous spécifiez comment les immobilisations sont amorties.</span><span class="sxs-lookup"><span data-stu-id="aa650-112">In a fixed asset depreciation book, you specify how fixed assets are depreciated.</span></span> <span data-ttu-id="aa650-113">Pour prendre en charge plusieurs méthodes d'amortissement, vous pouvez paramétrer plusieurs lois d'amortissement.</span><span class="sxs-lookup"><span data-stu-id="aa650-113">To accommodate various methods of depreciation, you can set up multiple depreciation books.</span></span>  

1. <span data-ttu-id="aa650-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Lois d'amortissement**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="aa650-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Depreciation Books**, and then choose the related link.</span></span>
2. <span data-ttu-id="aa650-115">Sur la page **Liste des lois d'amortissement**, sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="aa650-115">On the **Depreciation Books List** page, choose the **New** action.</span></span>
3. <span data-ttu-id="aa650-116">Sur la page **Fiche loi d'amortissement**, renseignez les champs comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="aa650-116">On the **Depreciation Book Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   <span data-ttu-id="aa650-117">Vous pouvez enregistrer les transactions immobilisation sur la page **Feuille compta. immo.** ou sur la page **Feuille immo.**, selon que les transactions sont destinées pour des rapports financiers ou pour la gestion interne.</span><span class="sxs-lookup"><span data-stu-id="aa650-117">You can record fixed asset transactions on the **Fixed Asset G/L Journal** page or on the **Fixed Asset Journal** page, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="aa650-118">Procédez comme suit pour définir quel type de feuille est utilisé pour les différentes activités immobilisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="aa650-118">Follow the next step to define which type of journal is used for the different fixed asset activities by default.</span></span>
4. <span data-ttu-id="aa650-119">Sur le raccourci **Intégration**, cochez la case pour chaque activité immobilisation dont vous souhaitez valider les transactions via la page **Feuille compta. immo.**.</span><span class="sxs-lookup"><span data-stu-id="aa650-119">On the **Integration** FastTab, select the check box for each fixed asset activity whose transactions you want to post using the **Fixed Asset G/L Journal** page.</span></span>
5. <span data-ttu-id="aa650-120">Répétez les étapes 2 à 4 pour chaque méthode d'amortissement ou méthode de validation que vous souhaitez attribuer à des immobilisations en tant que loi d'amortissement.</span><span class="sxs-lookup"><span data-stu-id="aa650-120">Repeat steps 2 through 4 for each depreciation method or posting method that you want to assign to fixed assets as a depreciation book.</span></span>

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a><span data-ttu-id="aa650-121">Pour attribuer une loi d'amortissement à une immobilisation</span><span class="sxs-lookup"><span data-stu-id="aa650-121">To assign a depreciation book to a fixed asset</span></span>
1. <span data-ttu-id="aa650-122">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Immobilisations**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="aa650-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="aa650-123">Sélectionnez l'immobilisation pour laquelle vous souhaitez configurer une loi d'amortissement.</span><span class="sxs-lookup"><span data-stu-id="aa650-123">Select the fixed asset that you want to set up a fixed asset depreciation book for.</span></span>
3. <span data-ttu-id="aa650-124">Sur le raccourci **Loi d'amortissement**, renseignez les champs, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="aa650-124">On the **Depreciation Book** FastTab, fill in the fields as necessary.</span></span>
4. <span data-ttu-id="aa650-125">Si vous devez assigner plus d'une loi d'amortissement à l'immobilisation, sélectionnez l'action **Ajouter davantage de lois d'amortissement**.</span><span class="sxs-lookup"><span data-stu-id="aa650-125">If you need to assign more than one depreciation book to the fixed asset, choose the **Add More Depreciation Books** action.</span></span>
5. <span data-ttu-id="aa650-126">Sinon, sélectionnez l'action **Lois d'amortissement** pour spécifier une, voire plusieurs lois d'amortissement immobilisation.</span><span class="sxs-lookup"><span data-stu-id="aa650-126">Alternatively, choose the **Depreciation Books** action to specify one or more fixed asset depreciation books.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="aa650-127">Lorsque vous utilisez la méthode manuelle d'amortissement, vous devez saisir l'amortissement manuellement dans la feuille comptabilisation immobilisation.</span><span class="sxs-lookup"><span data-stu-id="aa650-127">When you use the manual depreciation method, you must enter depreciation manually in the fixed asset G/L journal.</span></span> <span data-ttu-id="aa650-128">La fonction **Calculer amortissement** ignore les immobilisations qui utilisent la méthode d'amortissement manuelle.</span><span class="sxs-lookup"><span data-stu-id="aa650-128">The **Calculate Depreciation** function omits fixed assets that use the manual depreciation method.</span></span> <span data-ttu-id="aa650-129">Vous pouvez recourir à cette méthode pour les immobilisations qui ne font pas l'objet d'un amortissement, par exemple les terrains.</span><span class="sxs-lookup"><span data-stu-id="aa650-129">You can use this method for assets that are not subject to depreciation, such as land.</span></span>

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a><span data-ttu-id="aa650-130">Pour attribuer une loi d'amortissement à plusieurs immobilisations avec un traitement par lots</span><span class="sxs-lookup"><span data-stu-id="aa650-130">To assign a depreciation book to multiple fixed assets with a batch job</span></span>
<span data-ttu-id="aa650-131">Si vous voulez associer une loi d'amortissement à plusieurs immobilisations, vous pouvez utiliser le traitement par lots **Créer plans amortissement** pour créer des lois d'amortissement d'immobilisation.</span><span class="sxs-lookup"><span data-stu-id="aa650-131">If you want to assign a depreciation book to several fixed assets, you can use the **Create FA Depreciation Books** batch job to create fixed asset depreciation books.</span></span>  

1. <span data-ttu-id="aa650-132">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Immobilisations**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="aa650-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="aa650-133">Sélectionnez l'immobilisation à laquelle vous souhaitez attribuer une loi d'amortissement, puis sélectionnez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="aa650-133">Select the fixed asset that you want to set up a assign a depreciation book to, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="aa650-134">Sur la page **Fiche livre d'amortissement**, sélectionnez l'action **Créer plans amortissement**.</span><span class="sxs-lookup"><span data-stu-id="aa650-134">On the **Depreciation Book Card** page, choose the **Create FA Depreciation Books** action.</span></span>
4. <span data-ttu-id="aa650-135">Sur la page **Créer plans amortissement immo.**, renseignez le champ **Loi d'amortissement**.</span><span class="sxs-lookup"><span data-stu-id="aa650-135">On the **Create FA Depreciation Books** page, fill in the **Depreciation Book** field.</span></span>
5. <span data-ttu-id="aa650-136">Choisissez le champ **Copier immo. n°**, puis sélectionnez le numéro de l'immobilisation à utiliser comme base pour créer de nouvelles lois d'amortissement d'immobilisation.</span><span class="sxs-lookup"><span data-stu-id="aa650-136">Choose the **Copy from FA No.** field, and then select the fixed asset number that you want to use as the basis for creating new fixed asset depreciation books.</span></span>

    <span data-ttu-id="aa650-137">Si vous renseignez ce champ, les champs d'amortissement des nouvelles lois d'amortissement d'immobilisation contiennent les mêmes informations que ceux de la loi d'amortissement d'immobilisation que vous copiez.</span><span class="sxs-lookup"><span data-stu-id="aa650-137">If you fill in this field, the depreciation fields in the new fixed asset depreciation books will contain the same information as the corresponding fields in the fixed asset depreciation book that you copy from.</span></span> <span data-ttu-id="aa650-138">N'entrez rien dans ce champ si vous souhaitez créer de nouvelles lois d'amortissement d'immobilisation avec des champs d'amortissement vides.</span><span class="sxs-lookup"><span data-stu-id="aa650-138">Leave the field blank if you want to create new fixed asset depreciation books with empty depreciation fields.</span></span>  
6. <span data-ttu-id="aa650-139">Sur le raccourci **Immo.**, vous pouvez positionner un filtre afin de sélectionner les immobilisations pour lesquelles vous souhaitez créer des lois d'amortissement immobilisation.</span><span class="sxs-lookup"><span data-stu-id="aa650-139">On the **Fixed Asset** FastTab, you can set a filter to select the assets that you want to create the fixed asset depreciation books for.</span></span>
7. <span data-ttu-id="aa650-140">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa650-140">Choose the **OK** button.</span></span>

## <a name="to-set-up-depreciation-posting-types"></a><span data-ttu-id="aa650-141">Pour configurer les types de validation amortissement</span><span class="sxs-lookup"><span data-stu-id="aa650-141">To set up depreciation posting types</span></span>
<span data-ttu-id="aa650-142">Pour chaque loi d'amortissement, vous devez définir la manière dont vous souhaitez que [!INCLUDE[d365fin](includes/d365fin_md.md)] gère les différents types de validation.</span><span class="sxs-lookup"><span data-stu-id="aa650-142">For each depreciation book, you must set up how you want [!INCLUDE[d365fin](includes/d365fin_md.md)] to handle various posting types.</span></span> <span data-ttu-id="aa650-143">Par exemple, vous devez indiquer s'il s'agit d'un débit ou d'un crédit et si le type de validation doit être inclus dans la base d'amortissement.</span><span class="sxs-lookup"><span data-stu-id="aa650-143">For example, whether posting should be debit or credit and whether the posting type should be included in the depreciable basis.</span></span>  

1. <span data-ttu-id="aa650-144">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Lois d'amortissement**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="aa650-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Depreciation Books**, and then choose the related link.</span></span>  
2. <span data-ttu-id="aa650-145">Sélectionnez la loi d'amortissement que vous souhaitez configurer, puis sélectionnez l'action **Type paramètre compta. immo.**.</span><span class="sxs-lookup"><span data-stu-id="aa650-145">Select the depreciation book that you want to set up, and them choose the **FA Posting Type Setup** action.</span></span>
3. <span data-ttu-id="aa650-146">Sur la page **Type paramètre compta. immo.**, renseignez les champs, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="aa650-146">On the **FA Posting Type Setup** page, fill in the fields as necessary.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="aa650-147">Vous ne pouvez pas insérer ni supprimer de lignes sur la page **Type paramètre compta. immo**.</span><span class="sxs-lookup"><span data-stu-id="aa650-147">You cannot insert or delete lines on the **FA Posting Type Setup** page.</span></span> <span data-ttu-id="aa650-148">Vous ne pouvez modifier que les lignes existantes.</span><span class="sxs-lookup"><span data-stu-id="aa650-148">You can only modify the existing lines.</span></span>

<span data-ttu-id="aa650-149">Il est recommandé de ne pas modifier les paramètres des lois d'amortissement pour lesquelles des écritures ont déjà été validées.</span><span class="sxs-lookup"><span data-stu-id="aa650-149">We recommend that you do not change the setup for depreciation books for entries that have already been posted.</span></span> <span data-ttu-id="aa650-150">Les modifications apportées n'ont pas d'incidence sur les écritures déjà validées, ce qui rendrait les statistiques des lois d'amortissement inexactes.</span><span class="sxs-lookup"><span data-stu-id="aa650-150">Changes will not affect the entries that are already posted, which would make depreciation book statistics misleading.</span></span>

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a><span data-ttu-id="aa650-151">Pour configurer les modèles par défaut et les lots pour l'amortissement immobilisation</span><span class="sxs-lookup"><span data-stu-id="aa650-151">To set up default templates and batches for fixed asset depreciation</span></span>
<span data-ttu-id="aa650-152">Pour chaque loi d'amortissement, vous définissez une configuration par défaut de modèles et de feuilles.</span><span class="sxs-lookup"><span data-stu-id="aa650-152">For each depreciation book, you define a default setup of templates and batches.</span></span> <span data-ttu-id="aa650-153">Vous devez utiliser ces valeurs par défaut pour dupliquer les lignes d'une feuille vers une autre, créer des lignes feuille à l'aide du traitement par lots **Calculer amortissement** ou **Actualiser immobilisations**, dupliquer des coûts d'acquisition dans la feuille assurance.</span><span class="sxs-lookup"><span data-stu-id="aa650-153">You use these defaults to duplicate lines from one journal to another, create journal lines using the **Calculate Depreciation** or **Index Fixed Assets** batch jobs, duplicate acquisition costs in the insurance journal.</span></span>  

1. <span data-ttu-id="aa650-154">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Lois d'amortissement**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="aa650-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Depreciation Books**, and then choose the related link.</span></span>  
2. <span data-ttu-id="aa650-155">Sélectionnez la loi d'amortissement pour laquelle vous souhaitez définir les feuilles par défaut, puis sélectionnez l'action **Configuration feuille immo.**.</span><span class="sxs-lookup"><span data-stu-id="aa650-155">Select the depreciation book that you want to define default journals for, and then choose the **FA Journal Setup** action.</span></span>  
3. <span data-ttu-id="aa650-156">Pour avoir une configuration par défaut pour chaque utilisateur, choisissez le champ **Code utilisateur** à sélectionner à partir de la page **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="aa650-156">If you want to have a default setup for each user, choose the **User ID** field to select from the **Users** page.</span></span>  
4. <span data-ttu-id="aa650-157">Dans les autres champs, sélectionnez le modèle feuille ou la feuille qui doit être utilisé(e) par défaut.</span><span class="sxs-lookup"><span data-stu-id="aa650-157">In the other fields, select the journal template or journal batch that must be used by default.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aa650-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa650-158">See Also</span></span>
[<span data-ttu-id="aa650-159">Paramétrage d'immobilisations</span><span class="sxs-lookup"><span data-stu-id="aa650-159">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="aa650-160">COMPTES D'IMMOBILISATIONS</span><span class="sxs-lookup"><span data-stu-id="aa650-160">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="aa650-161">Finances</span><span class="sxs-lookup"><span data-stu-id="aa650-161">Finance</span></span>](finance.md)  
[<span data-ttu-id="aa650-162">Mise en route</span><span class="sxs-lookup"><span data-stu-id="aa650-162">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="aa650-163">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aa650-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>