---
title: Comment configurer des unités article | Microsoft Docs
description: Vous pouvez définir plusieurs unités pour un article afin de pouvoir affecter des unités à l'article.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 10/01/2018
ms.author: SorenGP
ms.openlocfilehash: 376e34074c6ee216b7a9062a42404a8123758598
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821648"
---
# <a name="set-up-item-units-of-measure"></a><span data-ttu-id="3e1f5-103">Configuration d'unités article</span><span class="sxs-lookup"><span data-stu-id="3e1f5-103">Set Up Item Units of Measure</span></span>
<span data-ttu-id="3e1f5-104">Vous pouvez définir plusieurs unités pour un article afin que vous puissiez affecter des unités à l'article aux fins suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e1f5-104">You can set up multiple units of measure for an item so that you can assign units of measure to the item for the following purposes:</span></span>

- <span data-ttu-id="3e1f5-105">Affectez une unité de base sur la fiche article de l'article pour définir la manière dont elle est stockée dans le stock et pour servir de base de conversion aux autres unités.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-105">Assign a base unit of measure on the item’s item card to define how it is stored in inventory and to serve as the conversion basis for alternate units of measure.</span></span>
- <span data-ttu-id="3e1f5-106">Affectez d'autres unités pour les documents d'achat, de production, ou de vente pour spécifier le nombre d'unités de base que vous gérez dans ces processus.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-106">Assign alternate units of measure to purchase, production, or sales documents to specify how many units of the base unit of measure you handle at a time in those processes.</span></span> <span data-ttu-id="3e1f5-107">Par exemple, vous pouvez acheter l'article en palettes et n'utiliser que des pièces individuelles en production.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-107">For example, you may buy the item on pallets and only use single pieces in your production.</span></span>

<span data-ttu-id="3e1f5-108">Si un article est stocké dans une unité mais produit dans une autre, un ordre de fabrication utilisant une unité de lot de fabrication est créé pour calculer la quantité correcte des composants durant le traitement par lots **Actualiser O.F.**.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-108">If an item is stocked in one unit of measure but produced in another, a production order is created that uses a manufacturing batch unit of measure to calculate the correct quantity of the components during the **Refresh Production Order** batch job.</span></span> <span data-ttu-id="3e1f5-109">Une situation dans laquelle un article fabriqué est stocké en pièces mais produit en tonnes est un exemple d'un calcul d'unité de lot de fabrication.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-109">An example of a manufacturing batch unit of measure calculation is when a manufactured item is stocked in pieces but produced in tons.</span></span> <span data-ttu-id="3e1f5-110">Pour plus d'informations, voir [Utiliser les unités de lot de fabrication](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).</span><span class="sxs-lookup"><span data-stu-id="3e1f5-110">For more information, see [Work with Manufacturing Batch Units of Measure](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).</span></span>

## <a name="to-set-up-a-unit-of-measure"></a><span data-ttu-id="3e1f5-111">Pour configurer une unité</span><span class="sxs-lookup"><span data-stu-id="3e1f5-111">To set up a unit of measure</span></span>
1. <span data-ttu-id="3e1f5-112">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="3e1f5-113">Ouvrez la fiche article pour laquelle vous souhaitez configurer des unités de remplacement.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-113">Open the card of the item for which you want to set up alternate units of measure.</span></span>
3. <span data-ttu-id="3e1f5-114">Choisissez l'action **Unités de mesure**.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-114">Choose the **Units of Measure** action.</span></span> <span data-ttu-id="3e1f5-115">La page **Unités article** s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-115">The **Item Units of Measure** page opens.</span></span>
4. <span data-ttu-id="3e1f5-116">Si le champ **Unité de base** de la fiche article est renseigné, cette unité est déjà installée.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-116">If the **Base Unit of Measure** field on the item card is filled, then that unit of measure is already set up.</span></span>
5. <span data-ttu-id="3e1f5-117">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-117">Choose the **New** action.</span></span> <span data-ttu-id="3e1f5-118">Une nouvelle ligne vide est insérée.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-118">A new empty line is inserted.</span></span>
6. <span data-ttu-id="3e1f5-119">Dans le champ **Code**, entrez le nom de l'unité.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-119">In the **Code** field, enter the name of the unit of measure.</span></span> <span data-ttu-id="3e1f5-120">Sinon, sélectionnez le champ pour choisir parmi les codes unité figurant dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-120">Alternatively, choose the field to select from the unit of measure codes that are in the database.</span></span>
7. <span data-ttu-id="3e1f5-121">Dans le champ **Quantité par unité** entrez le nombre d'unités de l'unité de base que la nouvelle unité contient.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-121">In the **Qty. per Unit of Measure** field, enter how many units of the base unit of measure the new unit of measure contains.</span></span>
8. <span data-ttu-id="3e1f5-122">Répétez les étapes 5 à 7 pour définir toutes les autres unités que vous souhaitez utiliser dans les différents processus de cet article.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-122">Repeat steps 5 through 7 to set up all the alternate units of measure that you want to use in different processes for this item.</span></span>

<span data-ttu-id="3e1f5-123">Vous pouvez maintenant utiliser les unités de remplacement sur les documents achat, production, et vente.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-123">You can now use the alternate units of measure on purchase, production, and sales documents.</span></span> <span data-ttu-id="3e1f5-124">Pour plus d'informations, voir Saisir des codes unité par défaut pour des transactions d'achat et de vente ou Utiliser l'unité de lot de fabrication.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-124">For more information, see Enter Default Units of Measure Codes for Purchase Transactions and Sales Transactions or Use the Manufacturing Batch Unit of Measure.</span></span>

## <a name="to-set-up-unit-of-measure-translations"></a><span data-ttu-id="3e1f5-125">Pour configurer des traductions d'unités</span><span class="sxs-lookup"><span data-stu-id="3e1f5-125">To set up unit of measure translations</span></span>
<span data-ttu-id="3e1f5-126">Lorsque vous vendez des articles à des clients étrangers, vous pouvez être amené à indiquer l'unité dans leur langue.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-126">When you sell items to foreign customers, you may want to specify the unit of measure in the customer’s language.</span></span> <span data-ttu-id="3e1f5-127">Pour cela, vous devez d'abord configurer les traductions d'unités nécessaires.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-127">You can do this after you have set up the necessary unit of measure translations.</span></span>

1. <span data-ttu-id="3e1f5-128">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Unités de mesure**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Units of Measure**, and then choose the related link.</span></span>
2. <span data-ttu-id="3e1f5-129">Sélectionnez le code pour lequel vous souhaitez définir des traductions, puis cliquez sur **Traductions**.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-129">Select the code for which you want to set up translations, and then choose the **Translations** action.</span></span>
3. <span data-ttu-id="3e1f5-130">Dans le champ **Code langue**, sélectionnez la flèche déroulante pour visualiser la liste des codes langue disponibles.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-130">In the **Language Code** field, select the drop-down arrow to see a list of available language codes.</span></span> <span data-ttu-id="3e1f5-131">Sélectionnez le code langue pour lequel vous souhaitez entrer une traduction, puis choisissez le bouton OK pour copier le code dans le champ.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-131">Select the language code for which you want to enter a translation, and then choose the OK button to copy the code to the field.</span></span>
4. <span data-ttu-id="3e1f5-132">Dans le champ **Désignation**, saisissez le texte approprié.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-132">In the **Description** field, enter the appropriate text.</span></span>
5. <span data-ttu-id="3e1f5-133">Répétez les étapes 2 à 4 pour les codes unité et les langues pour lesquels vous souhaitez indiquer des traductions.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-133">Repeat steps 2 through 4 for the unit of measure codes and the languages for which you want to enter translations.</span></span>

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a><span data-ttu-id="3e1f5-134">Pour entrer un code unité par défaut pour des transactions de ventes et d'achat</span><span class="sxs-lookup"><span data-stu-id="3e1f5-134">To enter a default unit of measure code for sales and purchasing transactions</span></span>
<span data-ttu-id="3e1f5-135">Si vous utilisez habituellement d'autres unités que l'unité de base pour vos achats et vos ventes, vous pouvez indiquer des unités distinctes.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-135">If you usually buy or sell in units different from the base unit of measure, you can specify separate units of measure for purchases and sales.</span></span> <span data-ttu-id="3e1f5-136">Pour cela, vous devez configurer les unités sur la page **Unités article**.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-136">To do this, the units of measure must be set up on the **Item Units of Measure** page.</span></span>

1. <span data-ttu-id="3e1f5-137">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="3e1f5-138">Ouvrez la fiche article appropriée pour laquelle vous souhaitez indiquer un code unité par défaut pour les achats et les ventes.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-138">Open the relevant item card for which you want to specify a default sales or purchase unit of measure code.</span></span>
3. <span data-ttu-id="3e1f5-139">Pour les ventes, sur le raccourci **Facturation**, dans le champ **Unité de vente**, ouvrez la page **Unités article**.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-139">For sales, on the **Invoicing** FastTab, in the **Sales Unit of Measure** field, open the **Item Units of Measure** page.</span></span>
4. <span data-ttu-id="3e1f5-140">Pour les achats, sur le raccourci **Réapprovisionnement**, dans le champ **Unité d'achat**, ouvrez la page **Unités article**.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-140">For purchasing, on the **Replenishment** FastTab, in the **Purch. Unit of Measure** field, open the **Item Units of Measure** page.</span></span>
5. <span data-ttu-id="3e1f5-141">Sélectionnez le code que vous souhaitez configurer comme unité par défaut pour les ventes ou les achats respectivement, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e1f5-141">Select the code you want to set up as the default unit of measure for sales or purchasing respectively, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e1f5-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e1f5-142">See Also</span></span>
[<span data-ttu-id="3e1f5-143">Utiliser les unités de lot de fabrication</span><span class="sxs-lookup"><span data-stu-id="3e1f5-143">Work with Manufacturing Batch Units of Measure</span></span>](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[<span data-ttu-id="3e1f5-144">Gestion du stock</span><span class="sxs-lookup"><span data-stu-id="3e1f5-144">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="3e1f5-145">Gestion des achats</span><span class="sxs-lookup"><span data-stu-id="3e1f5-145">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="3e1f5-146">[Gestion des ventes](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="3e1f5-146">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="3e1f5-147">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3e1f5-147">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>