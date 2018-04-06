---
title: "Comment planifier des mouvements entrepôt dans la feuille | Microsoft Docs"
description: "Planifiez les mouvements de la feuille à l'aide de la fonction réapprovisionnement emplacement ou en planifiant manuellement les lignes à créer en tant qu'instructions mouvement."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0f518b96cb21a9637ae9b6e64e4c9e22a5fc6512
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="plan-warehouse-movements-in-worksheets"></a><span data-ttu-id="7389e-103">Planifier des mouvements entrepôt dans la feuille</span><span class="sxs-lookup"><span data-stu-id="7389e-103">Plan Warehouse Movements in Worksheets</span></span>
<span data-ttu-id="7389e-104">Planifiez les mouvements de la feuille à l'aide de la fonction réapprovisionnement emplacement ou en planifiant manuellement les lignes à créer en tant qu'instructions mouvement.</span><span class="sxs-lookup"><span data-stu-id="7389e-104">Plan movements in the worksheet using a bin replenishment function or manually planning the lines that you want to create as movement instructions.</span></span>  

## <a name="to-calculate-a-replenishment-movement"></a><span data-ttu-id="7389e-105">Pour calculer des mouvements de réapprovisionnement</span><span class="sxs-lookup"><span data-stu-id="7389e-105">To calculate a replenishment movement</span></span>  
<span data-ttu-id="7389e-106">Au fur et à mesure que l'entrepôt expédie des articles aux clients, les emplacements les mieux classés contiennent de moins en moins d'articles.</span><span class="sxs-lookup"><span data-stu-id="7389e-106">As the warehouse ships items out to customers, the bins with the highest bin rankings contain fewer and fewer items.</span></span> <span data-ttu-id="7389e-107">Pour remplir ces emplacements prélèvement avec des articles issus d'autres emplacements, exécutez la fonction **Calculer réappro. emplacement** de la fenêtre **Feuille mouvements**.</span><span class="sxs-lookup"><span data-stu-id="7389e-107">To fill up these high-ranking pick bins with items from other bins, run the **Calculate Bin Replenishment** function in the **Movement Worksheet** window</span></span>

1.  <span data-ttu-id="7389e-108">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille mouvement**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="7389e-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7389e-109">Choisissez l'action **Calculer réappro. emplacement**.</span><span class="sxs-lookup"><span data-stu-id="7389e-109">Choose the **Calculate Bin Replenishment** action.</span></span>  

    [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="7389e-110"> crée des lignes indiquant précisément le mode de déplacement des articles des emplacements les moins bien classés vers les emplacements les mieux classés.</span><span class="sxs-lookup"><span data-stu-id="7389e-110"> creates lines that indicate precisely how you should move items from the low-ranking bins to the higher-ranking bins.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="7389e-111">Un mouvement est proposé selon FEFO lorsque vous activez la fonction **Créer mouvement** si les conditions suivantes sont réunies pour un article :</span><span class="sxs-lookup"><span data-stu-id="7389e-111">A movement is suggested according to FEFO when you activate the **Create Movement** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="7389e-112">L'article a une date de péremption.</span><span class="sxs-lookup"><span data-stu-id="7389e-112">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="7389e-113">La case à cocher **Prélèvement selon FEFO** sur la fiche magasin doit être cochée.</span><span class="sxs-lookup"><span data-stu-id="7389e-113">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="7389e-114">La case à cocher **Emplacement obligatoire** de la fiche magasin est cochée.</span><span class="sxs-lookup"><span data-stu-id="7389e-114">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="7389e-115">Les champs **De zone** et **D'emplacement** sont vides.</span><span class="sxs-lookup"><span data-stu-id="7389e-115">The **From Zone** and **From Bin** fields are blank.</span></span>  

    <span data-ttu-id="7389e-116">Pour plus d'informations, voir [Prélèvement par FEFO](warehouse-picking-by-fefo.md).</span><span class="sxs-lookup"><span data-stu-id="7389e-116">For more information, see [Picking by FEFO](warehouse-picking-by-fefo.md).</span></span>  

3.  <span data-ttu-id="7389e-117">Vérifiez ces lignes et modifiez-les si nécessaire, ou supprimez-en certaines si le temps imparti est insuffisant pour les exécuter toutes.</span><span class="sxs-lookup"><span data-stu-id="7389e-117">Look through the lines and change them if necessary, or delete some of them if there is not enough time to perform them all.</span></span>  
4.  <span data-ttu-id="7389e-118">Choisissez l'action **Créer mouvement** pour créer une instruction entrepôt s'adressant aux magasiniers.</span><span class="sxs-lookup"><span data-stu-id="7389e-118">Choose the **Create Movement** action to make a warehouse instruction for action by warehouse employees.</span></span>  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a><span data-ttu-id="7389e-119">Pour déplacer l'intégralité du contenu d'un ou de plusieurs emplacements à l'aide de la fonction Extraire contenu emplacement</span><span class="sxs-lookup"><span data-stu-id="7389e-119">To move the entire contents of one or more bins by using the Get Bin Content function</span></span>  
<span data-ttu-id="7389e-120">Vous pouvez également utiliser la feuille mouvements pour planifier d'autres mouvements de stock dans l'entrepôt.</span><span class="sxs-lookup"><span data-stu-id="7389e-120">You can also use the movement worksheet to plan other movement of inventory within the warehouse.</span></span> <span data-ttu-id="7389e-121">Par exemple, lorsque vous souhaitez placer des articles dans un emplacement pour contrôler la qualité, utilisez la feuille mouvements pour planifier cette action et créez un mouvement pour élaborer des instructions destinées à un employé.</span><span class="sxs-lookup"><span data-stu-id="7389e-121">For example, when you want to place items in a bin for quality control, you can use the movement worksheet to plan this action and then create a movement to make instructions for an employee.</span></span>  

1.  <span data-ttu-id="7389e-122">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille mouvement**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="7389e-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7389e-123">Choisissez l'action **Extraire contenu emplacement**.</span><span class="sxs-lookup"><span data-stu-id="7389e-123">Choose the **Get Bin Content** action.</span></span> <span data-ttu-id="7389e-124">Utilisez le formulaire de sélection pour filtrer les emplacements et les articles que vous souhaitez voir figurer sur les lignes de la feuille mouvement.</span><span class="sxs-lookup"><span data-stu-id="7389e-124">Use the request window to filter which bins and items you want to appear on the movement worksheet lines.</span></span>  
3.  <span data-ttu-id="7389e-125">Renseignez les champs pertinents du formulaire de sélection du traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="7389e-125">Fill in the relevant fields in the batch job request window.</span></span> <span data-ttu-id="7389e-126">Pour visualiser, par exemple, le contenu emplacement de tous les emplacements d'une zone donnée au niveau de l'emplacement, renseignez le champ **Code zone**.</span><span class="sxs-lookup"><span data-stu-id="7389e-126">For example, if you want to see the bin content of all the bins in a certain zone at the location, fill in the **Zone Code** field.</span></span> <span data-ttu-id="7389e-127">Pour extraire les lignes de chaque emplacement qui contient un article spécifique, renseignez le champ **N° article**.</span><span class="sxs-lookup"><span data-stu-id="7389e-127">If you want to retrieve lines for each bin that contains a particular item, fill in the **Item No.** field.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="7389e-128">Vous ne pouvez pas déplacer manuellement des articles vers ou depuis un emplacement de type RECEPTIONNER, car les articles dans ce type d'emplacement doivent être enregistrés comme étant rangés avant de faire partie du stock disponible.</span><span class="sxs-lookup"><span data-stu-id="7389e-128">You cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

4.  <span data-ttu-id="7389e-129">Lorsque vous extrayez plusieurs lignes, sélectionnez **Trier** pour sélectionner une méthode de tri définissant l'ordre d'apparition des lignes dans la feuille, puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="7389e-129">If you are retrieving many lines, choose **Sort** to select a sorting method to determine the order the lines will appear in the worksheet, and then choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="7389e-130">Les lignes mouvement sont récupérées selon FEFO lorsque vous activez la fonction **Extraire contenu emplacement** si les conditions suivantes sont réunies pour un article :</span><span class="sxs-lookup"><span data-stu-id="7389e-130">Movement lines are retrieved according to FEFO when you activate the **Get Bin Content** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="7389e-131">L'article a une date de péremption.</span><span class="sxs-lookup"><span data-stu-id="7389e-131">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="7389e-132">La case à cocher **Prélèvement selon FEFO** sur la fiche magasin doit être cochée.</span><span class="sxs-lookup"><span data-stu-id="7389e-132">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="7389e-133">La case à cocher **Emplacement obligatoire** de la fiche magasin est cochée.</span><span class="sxs-lookup"><span data-stu-id="7389e-133">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="7389e-134">Les champs **De zone** et **D'emplacement** sont vides.</span><span class="sxs-lookup"><span data-stu-id="7389e-134">The **From Zone** and **From Bin** fields are blank.</span></span>  

5.  <span data-ttu-id="7389e-135">Complétez certaines des lignes extraites de manière à indiquer les changements à apporter.</span><span class="sxs-lookup"><span data-stu-id="7389e-135">Complete some of the retrieved lines to reflect the changes you want to make.</span></span> <span data-ttu-id="7389e-136">Pour chaque article à déplacer, vous devez renseigner les champs **N° article**, **Du code emplacement**, **Vers code emplacement** et **Quantité**.</span><span class="sxs-lookup"><span data-stu-id="7389e-136">For each item that you want to move, you must fill in the **Item No.**, **From Bin Code**, **To Bin Code**, and **Quantity** fields.</span></span>  
6.  <span data-ttu-id="7389e-137">Supprimez les lignes incomplètes que vous avez utilisées à des fins d'information.</span><span class="sxs-lookup"><span data-stu-id="7389e-137">Delete the incomplete lines that you used for information.</span></span>  
7.  <span data-ttu-id="7389e-138">Lorsque les lignes de la feuille mouvement correspondent précisément au mouvement devant être effectué par le magasinier, choisissez l'action **Créer mouvement** pour créer les instructions à l'attention de cet employé.</span><span class="sxs-lookup"><span data-stu-id="7389e-138">Once the movement worksheet lines accurately reflect how the movement action should be carried out by the warehouse employee, choose the **Create Movement** action to create the instructions for the employee.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7389e-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7389e-139">See Also</span></span>  
[<span data-ttu-id="7389e-140">Gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="7389e-140">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="7389e-141">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="7389e-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="7389e-142">[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="7389e-142">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="7389e-143">[Gestion des assemblages](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="7389e-143">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="7389e-144">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="7389e-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="7389e-145">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7389e-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

