---
title: Gestion des stocks, Suisse
description: Les améliorations comprennent les fonctions spéciales de gestion des stocks en Suisse.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 31830644e2de5878b5e5b383aade8ef4864b0291
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382686"
---
# <a name="swiss-inventory-management"></a><span data-ttu-id="32f8a-103">Gestion des stocks, Suisse</span><span class="sxs-lookup"><span data-stu-id="32f8a-103">Swiss Inventory Management</span></span>
[!INCLUDE[prod_short](../../includes/prod_short.md)] <span data-ttu-id="32f8a-104">comprend les améliorations apportées à la gestion des stocks en Suisse.</span><span class="sxs-lookup"><span data-stu-id="32f8a-104">includes Swiss enhancements to inventory management.</span></span> <span data-ttu-id="32f8a-105">Notamment :</span><span class="sxs-lookup"><span data-stu-id="32f8a-105">This includes the following:</span></span>  

- <span data-ttu-id="32f8a-106">Génération d'état détaillé.</span><span class="sxs-lookup"><span data-stu-id="32f8a-106">Detailed reporting.</span></span>  <span data-ttu-id="32f8a-107">Pour plus d'informations, voir État Stock - Statistiques vente et État Stock - Liste.</span><span class="sxs-lookup"><span data-stu-id="32f8a-107">For more information, see the Inventory - Sales Statistics report and the Inventory - List report.</span></span>  
- <span data-ttu-id="32f8a-108">Possibilité de suivre une facture pour plusieurs expéditions.</span><span class="sxs-lookup"><span data-stu-id="32f8a-108">The ability to track an invoice with multiple shipments.</span></span>  
- <span data-ttu-id="32f8a-109">Y compris un code d'emplacement de fiche article en tant que code d'emplacement par défaut pour les lignes de vente et les feuilles articles.</span><span class="sxs-lookup"><span data-stu-id="32f8a-109">Including an item card location code as the default location code for sales lines and item journals.</span></span> <span data-ttu-id="32f8a-110">Pour plus d'informations, reportez-vous à [Configurer des magasins](../../inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="32f8a-110">For more information, see [Set Up Locations](../../inventory-how-setup-locations.md).</span></span>

## <a name="managing-item-details"></a><span data-ttu-id="32f8a-111">Gestion des détails article</span><span class="sxs-lookup"><span data-stu-id="32f8a-111">Managing Item Details</span></span>  
<span data-ttu-id="32f8a-112">Les sociétés peuvent avoir différents entrepôts pour différentes catégories de produits.</span><span class="sxs-lookup"><span data-stu-id="32f8a-112">Companies can have different warehouses for different product categories.</span></span> <span data-ttu-id="32f8a-113">Dans ce cas, vous devez utiliser le code d'emplacement par défaut récupéré à partir de la fiche article.</span><span class="sxs-lookup"><span data-stu-id="32f8a-113">In such cases, you must use the default location code retrieved from the item card.</span></span> <span data-ttu-id="32f8a-114">Lorsque vous définissez un code d'emplacement pour un article, il est transféré vers les lignes de vente et les feuilles article en tant que code d'emplacement d'article par défaut.</span><span class="sxs-lookup"><span data-stu-id="32f8a-114">When you define a location code for an item, it is transferred to the sales lines and item journals as a default item location code.</span></span> <span data-ttu-id="32f8a-115">Pour plus d'informations, voir la table Ligne feuille article et Ligne vente.</span><span class="sxs-lookup"><span data-stu-id="32f8a-115">For more information, see the Sales Line and the Item Journal Line table.</span></span>  

<span data-ttu-id="32f8a-116">Les informations, telles que le numéro du client, le code adresse destinataire et le code personne des ventes client, sont enregistrées dans les écritures comptables article.</span><span class="sxs-lookup"><span data-stu-id="32f8a-116">Additional information, such as customer number, ship-to address code, and customer sales person code, is stored in item ledger entries.</span></span> <span data-ttu-id="32f8a-117">Ces informations vous permettent de créer des critères de rapport personnalisés, tels que le revenu par client et les dispositions relatives aux articles ou aux ventes pour les commerciaux.</span><span class="sxs-lookup"><span data-stu-id="32f8a-117">This information helps you to create customized reporting criteria, such as revenue per customer, and item or sales provisions for sales people.</span></span> <span data-ttu-id="32f8a-118">Pour plus d'informations, voir la table Écriture comptable article.</span><span class="sxs-lookup"><span data-stu-id="32f8a-118">For more information, see the Item Ledger Entry table.</span></span>  

## <a name="invoices-with-multiple-shipments"></a><span data-ttu-id="32f8a-119">Factures pour plusieurs expéditions</span><span class="sxs-lookup"><span data-stu-id="32f8a-119">Invoices with Multiple Shipments</span></span>  
<span data-ttu-id="32f8a-120">Si plusieurs expéditions ont été validées pour un client, vous pouvez créer une facture regroupée avec la fonction **Extraire lignes expédition**.</span><span class="sxs-lookup"><span data-stu-id="32f8a-120">If multiple shipments have been posted for a customer, then you can create a combined invoice with the **Get Shipment Lines** function.</span></span> <span data-ttu-id="32f8a-121">Pour plus d'informations, voir la page Extraire lignes expédition.</span><span class="sxs-lookup"><span data-stu-id="32f8a-121">For more information, see the Get Shipment Lines page.</span></span> <span data-ttu-id="32f8a-122">Lorsque vous utilisez cette fonction, le texte créé sur les lignes de facture inclut des informations sur le numéro d'expédition et la date d'expédition.</span><span class="sxs-lookup"><span data-stu-id="32f8a-122">When you use this function, the text created on the invoice lines includes information about the shipment number and the shipment date.</span></span> <span data-ttu-id="32f8a-123">Par exemple, le texte peut paraître comme Expédition N°</span><span class="sxs-lookup"><span data-stu-id="32f8a-123">For example, the text could appear as Shipment No.</span></span> <span data-ttu-id="32f8a-124">102040 sur 25.01.01.</span><span class="sxs-lookup"><span data-stu-id="32f8a-124">102040 of 25.01.01.</span></span> <span data-ttu-id="32f8a-125">Cela vous permet de suivre facilement les factures avec plusieurs expéditions.</span><span class="sxs-lookup"><span data-stu-id="32f8a-125">This allows you to easily track invoices with multiple shipments.</span></span>  

## <a name="see-also"></a><span data-ttu-id="32f8a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32f8a-126">See Also</span></span>  
 <span data-ttu-id="32f8a-127">[Fonctionnalité locale, Suisse](switzerland-local-functionality.md) </span><span class="sxs-lookup"><span data-stu-id="32f8a-127">[Switzerland Local Functionality](switzerland-local-functionality.md) </span></span>  
 [<span data-ttu-id="32f8a-128">Configurer des magasins</span><span class="sxs-lookup"><span data-stu-id="32f8a-128">Set Up Locations</span></span>](../../inventory-how-setup-locations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]