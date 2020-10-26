---
title: Utiliser la table Référence externe article | Microsoft Docs
description: Définissez des références entre les descriptions que vous et votre fournisseur utilisez pour un article afin que vous puissiez insérer la description d’article du fournisseur dans les documents achat.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 056897c799dd12755432637690446a0797c9f18c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919453"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="59e40-103">Utiliser les références externes article</span><span class="sxs-lookup"><span data-stu-id="59e40-103">Use Item Cross References</span></span>
<span data-ttu-id="59e40-104">Si vous configurez une référence externe entre la désignation article que vous utilisez pour un article et la désignation que le fournisseur de cet article utilise, la désignation de l’article du fournisseur est automatiquement insérée sur les documents achat du fournisseur lorsque vous renseignez le **N° référence externe** .</span><span class="sxs-lookup"><span data-stu-id="59e40-104">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="59e40-105">.</span><span class="sxs-lookup"><span data-stu-id="59e40-105">field.</span></span> <span data-ttu-id="59e40-106">La même fonctionnalité s’applique pour les numéros d’article client sur les documents vente.</span><span class="sxs-lookup"><span data-stu-id="59e40-106">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="59e40-107">Les procédures suivantes décrivent comment utiliser les références externes article côté achat.</span><span class="sxs-lookup"><span data-stu-id="59e40-107">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="59e40-108">La procédure est identique côté achat.</span><span class="sxs-lookup"><span data-stu-id="59e40-108">The steps are similar for the sales side.</span></span>

> [!NOTE]
> <span data-ttu-id="59e40-109">Il est de plus en plus courant que les identificateurs d’articles, tels que les GTIN ou les GUID contiennent 30 caractères ou plus, ce qui est plus que la fonctionnalité actuelle des références croisées d’éléments peut gérer.</span><span class="sxs-lookup"><span data-stu-id="59e40-109">It's becoming more common for item identifiers such as GTINs or GUIDs to contain 30 or more characters, which is more than the current feature for item cross references can handle.</span></span> <span data-ttu-id="59e40-110">Si vous devez utiliser des références contenant plus de 30 caractères, votre administrateur peut activer les fonctionnalité **Écrire des références d’articles plus longues** sur la page [Gestion des fonctionnalités](https://businesscentral.dynamics.com/?page=xzy) (le lien nécessite que vous ayez un client [!INCLUDE[d365fin](includes/d365fin_md.md)]).</span><span class="sxs-lookup"><span data-stu-id="59e40-110">If you need to use references that contain more than 30 characters, your administrator can turn on the **Write longer item references** feature on the [Feature Management](https://businesscentral.dynamics.com/?page=xzy) page (link requires that you have a [!INCLUDE[d365fin](includes/d365fin_md.md)] tenant).</span></span> <span data-ttu-id="59e40-111">La façon dont vous utilisez les références ne change pas, mais les noms d’articles, tels que les pages et les boutons le seront.</span><span class="sxs-lookup"><span data-stu-id="59e40-111">How you use references doesn't change, but the names of things like pages and buttons will.</span></span> <span data-ttu-id="59e40-112">Par exemple, la page **Entrées de références croisées d’article** deviendra la page **Entrées de référence d’article** .</span><span class="sxs-lookup"><span data-stu-id="59e40-112">For example, the **Item Cross-Reference Entries** page will become the **Item Reference Entries** page.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="59e40-113">Pour configurer une référence externe article à la description d’un article fournisseur</span><span class="sxs-lookup"><span data-stu-id="59e40-113">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="59e40-114">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles** , puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="59e40-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** , and then choose the related link.</span></span>
2. <span data-ttu-id="59e40-115">Ouvrez la fiche correspondant à l’article pour lequel vous souhaitez créer une référence externe à la description de l’article que le fournisseur utilise pour cet article.</span><span class="sxs-lookup"><span data-stu-id="59e40-115">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="59e40-116">Choisissez l’action **Références externes** .</span><span class="sxs-lookup"><span data-stu-id="59e40-116">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="59e40-117">Si vous ne trouvez pas l’action **Références externes** , choisissez d’afficher plus d’options, puis recherchez-la sous **Association** > **Article** .</span><span class="sxs-lookup"><span data-stu-id="59e40-117">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Related** > **Item** .</span></span>
  
4. <span data-ttu-id="59e40-118">Sur une nouvelle ligne de la page **Écritures de référence externe article** , renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="59e40-118">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="59e40-119">.</span><span class="sxs-lookup"><span data-stu-id="59e40-119">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="59e40-120">Pour saisir une description de l’article d’un fournisseur sur une commande achat</span><span class="sxs-lookup"><span data-stu-id="59e40-120">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="59e40-121">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes achat** , puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="59e40-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders** , and then choose the related link.</span></span>
2. <span data-ttu-id="59e40-122">Créez une commande achat pour le fournisseur pour lequel vous avez créé une référence externe article dans la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="59e40-122">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="59e40-123">Créez une ligne achat pour l’article pour lequel vous avez créé une référence externe article dans la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="59e40-123">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="59e40-124">Dans le champ **N° type référence externe** ,</span><span class="sxs-lookup"><span data-stu-id="59e40-124">In the **Cross-Reference No.**</span></span> <span data-ttu-id="59e40-125">sélectionnez la référence externe article que vous avez créée, puis choisissez le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="59e40-125">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="59e40-126">Le champ **Description** de la ligne est remplacé par la description d’article du fournisseur, tel que configuré dans l’écriture référence externe article.</span><span class="sxs-lookup"><span data-stu-id="59e40-126">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="59e40-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59e40-127">See Also</span></span>
[<span data-ttu-id="59e40-128">Enregistrer de nouveaux articles</span><span class="sxs-lookup"><span data-stu-id="59e40-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="59e40-129">Stock</span><span class="sxs-lookup"><span data-stu-id="59e40-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="59e40-130">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="59e40-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
