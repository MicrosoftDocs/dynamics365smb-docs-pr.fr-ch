---
title: Importation de nombreuses images d’articles depuis un fichier ZIP| Microsoft Docs
description: Vous pouvez importer plusieurs images d’articles à la fois. Nommez simplement vos fichiers image avec des noms correspondant à vos numéros d’article, comprimez-les en un fichier zip, puis utilisez la page Importer les images d’articles pour gérer quelles images d’articles importer.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4d4221ca3af412cc2548634cc6920f58171233ce
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785938"
---
# <a name="import-multiple-item-pictures"></a><span data-ttu-id="7e878-104">Importer plusieurs images d’article</span><span class="sxs-lookup"><span data-stu-id="7e878-104">Import Multiple Item Pictures</span></span>
<span data-ttu-id="7e878-105">Vous pouvez importer plusieurs images d’articles à la fois.</span><span class="sxs-lookup"><span data-stu-id="7e878-105">You can import multiple item pictures in one go.</span></span> <span data-ttu-id="7e878-106">Nommez simplement vos fichiers image avec des noms correspondant à vos numéros d’article, comprimez-les en un fichier ZIP, puis utilisez la page **Importer les images d’articles** pour gérer quelles images d’articles importer.</span><span class="sxs-lookup"><span data-stu-id="7e878-106">Simply name your picture files with names corresponding to your item numbers, compress them to a ZIP file, and then use the **Import Item Pictures** page to manage which item pictures to import.</span></span>

<span data-ttu-id="7e878-107">Tous les formats de fichier courants sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7e878-107">All common file formats are supported.</span></span>

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><span data-ttu-id="7e878-108">Nommer les fichiers image avec les noms d’article et préparez le fichier ZIP</span><span class="sxs-lookup"><span data-stu-id="7e878-108">To name picture files by the item names and prepare the ZIP file</span></span>
1. <span data-ttu-id="7e878-109">À l’emplacement de stockage de vos images d’article, nommez chaque fichier selon le numéro de l’article concerné.</span><span class="sxs-lookup"><span data-stu-id="7e878-109">At the location where your item pictures are stored, name each files according to the number of the related item.</span></span> <span data-ttu-id="7e878-110">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="7e878-110">For example:</span></span>

    |<span data-ttu-id="7e878-111">N° article</span><span class="sxs-lookup"><span data-stu-id="7e878-111">Item No.</span></span>|<span data-ttu-id="7e878-112">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="7e878-112">File Name</span></span>|
    |-|-|
    |<span data-ttu-id="7e878-113">1000</span><span class="sxs-lookup"><span data-stu-id="7e878-113">1000</span></span>|<span data-ttu-id="7e878-114">1000.bmp</span><span class="sxs-lookup"><span data-stu-id="7e878-114">1000.bmp</span></span>|
    |<span data-ttu-id="7e878-115">1 001</span><span class="sxs-lookup"><span data-stu-id="7e878-115">1001</span></span>|<span data-ttu-id="7e878-116">1001.bmp</span><span class="sxs-lookup"><span data-stu-id="7e878-116">1001.bmp</span></span>|
    |<span data-ttu-id="7e878-117">1002</span><span class="sxs-lookup"><span data-stu-id="7e878-117">1002</span></span>|<span data-ttu-id="7e878-118">1002.bmp</span><span class="sxs-lookup"><span data-stu-id="7e878-118">1002.bmp</span></span>|

2. <span data-ttu-id="7e878-119">Recueillez tous les fichiers dans un fichier ZIP.</span><span class="sxs-lookup"><span data-stu-id="7e878-119">Collect all the files in a ZIP file.</span></span> <span data-ttu-id="7e878-120">Par exemple, dans Windows Explorer, sélectionnez les fichiers, puis choisissez **Envoyer vers**, **Dossier comprimé (zip)**.</span><span class="sxs-lookup"><span data-stu-id="7e878-120">For example, in Windows Explorer, select the files, and then choose **Send to**, **Compressed (zipped) folder**.</span></span>     

## <a name="to-import-item-pictures"></a><span data-ttu-id="7e878-121">Pour importer des images d’article</span><span class="sxs-lookup"><span data-stu-id="7e878-121">To import item pictures</span></span>
1. <span data-ttu-id="7e878-122">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres stock**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7e878-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="7e878-123">Sélectionnez l’action **Importer des images d’article**.</span><span class="sxs-lookup"><span data-stu-id="7e878-123">Choose the **Import Item Pictures** action.</span></span>
3. <span data-ttu-id="7e878-124">Dans le champ **Sélectionner un fichier ZIP**, sélectionnez le dossier ZIP pertinent, puis sélectionnez le bouton **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="7e878-124">In the **Select a ZIP file** field, select the relevant ZIP folder, and then choose the **Open** button.</span></span>

    <span data-ttu-id="7e878-125">Une ligne pour chaque élément et image est créée sur la page **Importer des images d’article**.</span><span class="sxs-lookup"><span data-stu-id="7e878-125">A line for each item and picture is created on the **Import Item Pictures** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e878-126">Pour les fichiers article qui ont déjà une image, la case à cocher **Une image existe déjà** est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7e878-126">For item cards that already have a picture, the **Picture Already Exists** check box is selected.</span></span> <span data-ttu-id="7e878-127">Si vous ne souhaitez pas remplacer les images existantes, décochez la case **Remplacer les images**.</span><span class="sxs-lookup"><span data-stu-id="7e878-127">If you do not want any existing pictures to be replaced, deselect the **Replace Pictures** check box.</span></span> <span data-ttu-id="7e878-128">Si vous ne souhaitez pas remplacer les images existantes individuelles, supprimez les lignes en question.</span><span class="sxs-lookup"><span data-stu-id="7e878-128">If you do not want individual existing pictures to be replaced, delete the lines in question.</span></span>

3. <span data-ttu-id="7e878-129">Sélectionnez l’action **Importer des images**.</span><span class="sxs-lookup"><span data-stu-id="7e878-129">Choose the **Import Pictures** action.</span></span>

<span data-ttu-id="7e878-130">Le champ **Importer le statut** est mis à jour pour montrer si l’importation de l’image a été ignorée ou a bien eu lieu.</span><span class="sxs-lookup"><span data-stu-id="7e878-130">The **Import Status** field is updated to show if the picture import was skipped or completed.</span></span>       

## <a name="see-also"></a><span data-ttu-id="7e878-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e878-131">See Also</span></span>
[<span data-ttu-id="7e878-132">Enregistrer de nouveaux articles</span><span class="sxs-lookup"><span data-stu-id="7e878-132">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="7e878-133">Création des souches de numéros</span><span class="sxs-lookup"><span data-stu-id="7e878-133">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="7e878-134">Stock</span><span class="sxs-lookup"><span data-stu-id="7e878-134">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="7e878-135">Achats</span><span class="sxs-lookup"><span data-stu-id="7e878-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="7e878-136">Ventes</span><span class="sxs-lookup"><span data-stu-id="7e878-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="7e878-137">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7e878-137">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]