---
title: Utiliser la table Référence externe article | Microsoft Docs
description: Si vous configurez une référence externe entre la désignation article que vous utilisez pour un article et la désignation que le fournisseur de cet article utilise, la désignation de l'article du fournisseur est automatiquement insérée sur les documents achat du fournisseur lorsque vous renseignez le **N° référence externe**. .
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ca9f31b737fbd81bd1abba2a942301d0c9c919a6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "927117"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="dbb66-104">Utiliser les références externes article</span><span class="sxs-lookup"><span data-stu-id="dbb66-104">Use Item Cross References</span></span>
<span data-ttu-id="dbb66-105">Si vous configurez une référence externe entre la désignation article que vous utilisez pour un article et la désignation que le fournisseur de cet article utilise, la désignation de l'article du fournisseur est automatiquement insérée sur les documents achat du fournisseur lorsque vous renseignez le **N° référence externe**.</span><span class="sxs-lookup"><span data-stu-id="dbb66-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="dbb66-106">.</span><span class="sxs-lookup"><span data-stu-id="dbb66-106">field.</span></span> <span data-ttu-id="dbb66-107">La même fonctionnalité s'applique pour les numéros d'article client sur les documents vente.</span><span class="sxs-lookup"><span data-stu-id="dbb66-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="dbb66-108">Les procédures suivantes décrivent comment utiliser les références externes article côté achat.</span><span class="sxs-lookup"><span data-stu-id="dbb66-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="dbb66-109">La procédure est identique côté achat.</span><span class="sxs-lookup"><span data-stu-id="dbb66-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="dbb66-110">Pour configurer une référence externe article à la description d'un article fournisseur</span><span class="sxs-lookup"><span data-stu-id="dbb66-110">To set up an item cross reference to a vendor's item description</span></span>
1. <span data-ttu-id="dbb66-111">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="dbb66-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="dbb66-112">Ouvrez la fiche correspondant à l'article pour lequel vous souhaitez créer une référence externe à la description de l'article que le fournisseur utilise pour cet article.</span><span class="sxs-lookup"><span data-stu-id="dbb66-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="dbb66-113">Choisissez l'action **Références externes**.</span><span class="sxs-lookup"><span data-stu-id="dbb66-113">Choose the **Cross References** action.</span></span>
4. <span data-ttu-id="dbb66-114">Sur une nouvelle ligne de la page **Écritures de référence externe article**, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="dbb66-114">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="dbb66-115">.</span><span class="sxs-lookup"><span data-stu-id="dbb66-115">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="dbb66-116">Pour saisir une description de l'article d'un fournisseur sur une commande achat</span><span class="sxs-lookup"><span data-stu-id="dbb66-116">To enter a vendor's item description on a purchase order</span></span>
1. <span data-ttu-id="dbb66-117">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes achat**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="dbb66-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="dbb66-118">Créez une commande achat pour le fournisseur pour lequel vous avez créé une référence externe article dans la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="dbb66-118">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="dbb66-119">Créez une ligne achat pour l'article pour lequel vous avez créé une référence externe article dans la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="dbb66-119">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="dbb66-120">Dans le champ **N° type référence externe**,</span><span class="sxs-lookup"><span data-stu-id="dbb66-120">In the **Cross-Reference No.**</span></span> <span data-ttu-id="dbb66-121">sélectionnez la référence externe article que vous avez créée, puis choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbb66-121">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="dbb66-122">Le champ **Description** de la ligne est remplacé par la description d'article du fournisseur, tel que configuré dans l'écriture référence externe article.</span><span class="sxs-lookup"><span data-stu-id="dbb66-122">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbb66-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbb66-123">See Also</span></span>
[<span data-ttu-id="dbb66-124">Enregistrer de nouveaux articles</span><span class="sxs-lookup"><span data-stu-id="dbb66-124">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="dbb66-125">Inventaire</span><span class="sxs-lookup"><span data-stu-id="dbb66-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="dbb66-126">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dbb66-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
