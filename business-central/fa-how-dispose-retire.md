---
title: Cession ou annulation d'immobilisations| Microsoft Docs
description: Vous devez valider une valeur de cession lorsque vous ferraillez, vendez, ou annulez une immobilisation.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5897bd38f9cddd9b45d0d9a0b5fd11d5ee0c817b
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="cbde7-103">Céder ou annuler des immobilisations</span><span class="sxs-lookup"><span data-stu-id="cbde7-103">Dispose of or Retire Fixed Assets</span></span>
<span data-ttu-id="cbde7-104">Lorsque vous commercialisez ou cédez une immobilisation, la valeur de cession doit être validée pour calculer et enregistrer le gain ou la perte.</span><span class="sxs-lookup"><span data-stu-id="cbde7-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="cbde7-105">Une écriture cession doit être la dernière écriture validée pour une immobilisation.</span><span class="sxs-lookup"><span data-stu-id="cbde7-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="cbde7-106">Pour les immobilisations partiellement cédées, vous pouvez valider plusieurs écritures cession.</span><span class="sxs-lookup"><span data-stu-id="cbde7-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="cbde7-107">Le total de tous les montants de cession validés doit être un montant crédit.</span><span class="sxs-lookup"><span data-stu-id="cbde7-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="cbde7-108">Si vous négociez une immobilisation en échange d'une autre, vous devez enregistrer à la fois la vente de l'ancienne immobilisation (cession) et l'achat de la nouvelle (acquisition).</span><span class="sxs-lookup"><span data-stu-id="cbde7-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="cbde7-109">Pour en savoir plus, voir [Acquérir des immobilisations](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="cbde7-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="cbde7-110">Valider une cession à partir d'une feuille comptabilisation immobilisation</span><span class="sxs-lookup"><span data-stu-id="cbde7-110">To post a disposal from the fixed asset G/L journal</span></span>
1. <span data-ttu-id="cbde7-111">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Feuille comptabilisation immobilisation**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="cbde7-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="cbde7-112">Créez une feuille comptable initiale et complétez les champs, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="cbde7-112">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="cbde7-113">Dans le champ **Type compta. immo**, sélectionnez **Cession**.</span><span class="sxs-lookup"><span data-stu-id="cbde7-113">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="cbde7-114">Sélectionnez l'action **Insérer contrepartie immo.**.</span><span class="sxs-lookup"><span data-stu-id="cbde7-114">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="cbde7-115">Une seconde ligne feuille est créée pour le compte contrepartie qui est configuré pour la validation de la cession.</span><span class="sxs-lookup"><span data-stu-id="cbde7-115">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="cbde7-116">L'étape 4 ne fonctionne que si vous avez configuré ce qui suit : la fenêtre **Fiche groupe compta. immo.** pour le groupe de validation de l'immobilisation, le champ **Cession immobilisation** contient le compte débit général et le champ **Compte contrepartie cession** contient le compte général auquel vous souhaitez valider les écritures contrepartie pour appréciation.</span><span class="sxs-lookup"><span data-stu-id="cbde7-116">Step 4 only works if you have set up the following: In the **FA Posting Group Card** window for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="cbde7-117">Pour en savoir plus, voir la section « Pour configurer des groupes de validation d'immobilisation » dans [Configurer des informations d'immobilisation générales pour les immobilisations](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="cbde7-117">For more information, see the "To set up fixed asset posting groups" section in [Set Up General Fixed Asset Information](fa-how-setup-general.md).</span></span>  
5. <span data-ttu-id="cbde7-118">Sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="cbde7-118">Choose the **Post** action.</span></span>  

    <span data-ttu-id="cbde7-119">Si vous vendez une immobilisation ou en cédez une partie, vous devez d'abord diviser l'immobilisation avant de pouvoir enregistrer la transaction cession.</span><span class="sxs-lookup"><span data-stu-id="cbde7-119">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="cbde7-120">Pour en savoir plus, voir [Transférer, fractionner ou regrouper les immobilisations](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="cbde7-120">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="cbde7-121">Pour visualiser des écritures comptables cession</span><span class="sxs-lookup"><span data-stu-id="cbde7-121">To view disposal ledger entries</span></span>
<span data-ttu-id="cbde7-122">Lorsque vous vendez ou cédez une immobilisation, la valeur de cession est validée en comptabilité où vous pouvez afficher le résultat.</span><span class="sxs-lookup"><span data-stu-id="cbde7-122">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="cbde7-123">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Immobilisations**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="cbde7-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="cbde7-124">Sélectionnez l'immobilisation pour laquelle vous souhaitez afficher les écritures, puis sélectionnez l'action **Lois d'amortissement**.</span><span class="sxs-lookup"><span data-stu-id="cbde7-124">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="cbde7-125">Sélectionnez la loi d'amortissement pour laquelle vous souhaitez afficher les écritures, puis sélectionnez l'action **Écritures comptables**.</span><span class="sxs-lookup"><span data-stu-id="cbde7-125">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="cbde7-126">Sélectionnez une ligne avec **Cession** dans le champ **Catégorie compta. immo.**, puis sélectionnez l'action **Naviguer**.</span><span class="sxs-lookup"><span data-stu-id="cbde7-126">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Navigate** action.</span></span>  
5. <span data-ttu-id="cbde7-127">Dans la fenêtre **Naviguer**, sélectionnez la ligne d'écriture comptable, puis l'action **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="cbde7-127">In the **Navigate** window, select the general ledger entry line, and then choose the **Show** action.</span></span>  

<span data-ttu-id="cbde7-128">La fenêtre **Écritures comptables** s'ouvre. Vous pouvez y voir les écritures résultant de la validation de la cession.</span><span class="sxs-lookup"><span data-stu-id="cbde7-128">The **General Ledger Entries** window opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cbde7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbde7-129">See Also</span></span>
[<span data-ttu-id="cbde7-130">Immobilisations</span><span class="sxs-lookup"><span data-stu-id="cbde7-130">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="cbde7-131">Paramétrage d'immobilisations</span><span class="sxs-lookup"><span data-stu-id="cbde7-131">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="cbde7-132">Finances</span><span class="sxs-lookup"><span data-stu-id="cbde7-132">Finance</span></span>](finance.md)  
<span data-ttu-id="cbde7-133">[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="cbde7-133">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="cbde7-134">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cbde7-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

