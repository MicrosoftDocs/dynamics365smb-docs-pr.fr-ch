---
title: Configurer des conditions de livraison
description: Vous pouvez définir un code pour chacune de vos méthodes d’expédition offertes et saisir les informations qui les concernent.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8390c95083eb02c208e97f0309a725e8ec4d7730
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778587"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="f46a8-103">Configurer des conditions de livraison</span><span class="sxs-lookup"><span data-stu-id="f46a8-103">Set Up Shipment Methods</span></span>

<span data-ttu-id="f46a8-104">Les conditions de livraison dépendent souvent des articles, des clients et des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="f46a8-104">Shipment methods often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="f46a8-105">Par exemple, si le client habite sur une île, il peut choisir d'être toujours livré par voie aérienne ou maritime.</span><span class="sxs-lookup"><span data-stu-id="f46a8-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="f46a8-106">Certains clients peuvent exiger une livraison le lendemain.</span><span class="sxs-lookup"><span data-stu-id="f46a8-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="f46a8-107">Certains voudront peut-être récupérer la commande.</span><span class="sxs-lookup"><span data-stu-id="f46a8-107">Some may want to pick up the order.</span></span> <span data-ttu-id="f46a8-108">Vous pouvez spécifier le type de livraison souhaité sur les fiches client et les fiches fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f46a8-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="f46a8-109">Vous définissez la désignation et le code de chaque condition de livraison sur la page **Conditions de livraison**.</span><span class="sxs-lookup"><span data-stu-id="f46a8-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="f46a8-110">Par exemple, vous définissez le code F.O.B., et saisissez Franco bord dans le champ **Désignation**.</span><span class="sxs-lookup"><span data-stu-id="f46a8-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="f46a8-111">Vous pouvez ensuite saisir ce code dans les champs **Code de méthode de livraison** ailleurs dans le système, par exemple sur une fiche client.</span><span class="sxs-lookup"><span data-stu-id="f46a8-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="f46a8-112">Ensuite, lorsque vous créez des commandes, des factures, des avoirs, etc., le système copie la désignation représentée par le code.</span><span class="sxs-lookup"><span data-stu-id="f46a8-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="f46a8-113">Au besoin, vous pouvez le modifier sur le document.</span><span class="sxs-lookup"><span data-stu-id="f46a8-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-method"></a><span data-ttu-id="f46a8-114">Pour configurer une condition de livraison</span><span class="sxs-lookup"><span data-stu-id="f46a8-114">To set up a shipment method</span></span>

1. <span data-ttu-id="f46a8-115">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Conditions de livraison**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f46a8-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="f46a8-116">Sur la page **Conditions de livraison**, sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="f46a8-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="f46a8-117">Sur la nouvelle ligne, indiquez un code et une description pour les conditions de livraison.</span><span class="sxs-lookup"><span data-stu-id="f46a8-117">On the new line, specify a code and description for the shipment method.</span></span>

> [!TIP]
> <span data-ttu-id="f46a8-118">Si vous utilisez des incoterms, configurez des conditions de livraison pour représenter les règles d’incoterms pertinentes.</span><span class="sxs-lookup"><span data-stu-id="f46a8-118">If you use Incoterms, set up shipment methods to represent the relevant Incoterms rules.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f46a8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f46a8-119">See Also</span></span>

[<span data-ttu-id="f46a8-120">Configurer des transporteurs</span><span class="sxs-lookup"><span data-stu-id="f46a8-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
[<span data-ttu-id="f46a8-121">Suivre des colis</span><span class="sxs-lookup"><span data-stu-id="f46a8-121">Track Packages</span></span>](sales-how-track-packages.md)  
[<span data-ttu-id="f46a8-122">Gestion d’entrepôt</span><span class="sxs-lookup"><span data-stu-id="f46a8-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="f46a8-123">Stock</span><span class="sxs-lookup"><span data-stu-id="f46a8-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="f46a8-124">Configuration de la gestion des entrepôts</span><span class="sxs-lookup"><span data-stu-id="f46a8-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="f46a8-125">Gestion des assemblages</span><span class="sxs-lookup"><span data-stu-id="f46a8-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="f46a8-126">Détails de conception : gestion d’entrepôt</span><span class="sxs-lookup"><span data-stu-id="f46a8-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="f46a8-127">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f46a8-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="f46a8-128">Incoterms sur iccwbo.org</span><span class="sxs-lookup"><span data-stu-id="f46a8-128">Incoterms on iccwbo.org</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]