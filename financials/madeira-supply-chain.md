---
title: "Fonctionnalité de chaîne d'approvisionnement prise en charge par Financials| Microsoft Docs"
description: "Obtenez un aperçu des produits et renseignez-vous sur les concepts et processus principaux de chaîne d'approvisionnement qui font partie de la solution ERP."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product overview, ERP
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 3bae84075dc505aa9318590b1fac06e4844ffafe
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017

---
# <a name="overview-of-supply-chain-functionality"></a><span data-ttu-id="13da1-103">Aperçu de la fonctionnalité de chaîne d'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="13da1-103">Overview of Supply Chain Functionality</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="13da1-104"> prend en charge les processus courants de chaîne d'approvisionnement, mais limités aux besoins des sociétés de vente en gros et de distribution sans gestion des entrepôts.</span><span class="sxs-lookup"><span data-stu-id="13da1-104"> supports common supply chain processes, although limited to the needs of wholesale and distribution companies without managed warehouse handling.</span></span>

<span data-ttu-id="13da1-105">Outre les documents facture vente, vous pouvez gérer votre traitement de la commande avec des commandes vente vous autorisant à expédier certains articles de la quantité commandée, par exemple, parce que la quantité totale n'est pas immédiatement disponible.</span><span class="sxs-lookup"><span data-stu-id="13da1-105">In addition to sales invoice documents, you can manage your order fulfillment with sales orders allowing you to ship parts of an order quantity, for example, because the full quantity is not available at once.</span></span> <span data-ttu-id="13da1-106">Vous pouvez faire livrer des articles directement d'un fournisseur à un client en liant la commande vente à la commande achat associée.</span><span class="sxs-lookup"><span data-stu-id="13da1-106">You can have items drop shipped directly from a vendor to a customer by linking the sales order to the related purchase order.</span></span>

<span data-ttu-id="13da1-107">Les quantités en stock sont dynamiquement mises à jour lorsque vous vendez ou achetez des articles, et les informations ou les avertissements de disponibilité sont affichés à l'intention du vendeur de plusieurs manières.</span><span class="sxs-lookup"><span data-stu-id="13da1-107">Your inventory quantities are dynamically updated as you sell and buy items, and availability information or warnings are shown to sales people in several ways.</span></span> <span data-ttu-id="13da1-108">Vous pouvez ajuster les quantités en stock manuellement en validant directement dans les écritures comptables articles, par exemple, après un inventaire.</span><span class="sxs-lookup"><span data-stu-id="13da1-108">You can adjust inventory quantities manually by posting directly to the item ledger entries, for example, after a physical count.</span></span> <span data-ttu-id="13da1-109">Vous pouvez offrir et vendre des articles à vos clients sans tenir compte du stock associé.</span><span class="sxs-lookup"><span data-stu-id="13da1-109">You can offer and sell items to your customers without maintaining inventory for them.</span></span> <span data-ttu-id="13da1-110">Pour inclure des articles non stockés à votre processus de chaîne d'approvisionnement, il vous suffit de les convertir en articles normaux.</span><span class="sxs-lookup"><span data-stu-id="13da1-110">If you want to include such nonstock items to your supply chain process, you simply convert them to normal items.</span></span>

<span data-ttu-id="13da1-111">Outre les documents facture achat, vous pouvez gérer votre côté de l'approvisionnement avec les commandes achat permettant d'enregistrer les réceptions partielles d'une quantité de commande.</span><span class="sxs-lookup"><span data-stu-id="13da1-111">In addition to purchase invoice documents, you can manage your supply side with purchase orders allowing you to record partial receipts of an order quantity.</span></span> <span data-ttu-id="13da1-112">Une fonction de planification des approvisionnements simplifiée vous permet de lancer un achat directement à partir de la facture vente qui requiert des articles.</span><span class="sxs-lookup"><span data-stu-id="13da1-112">A simple supply planning function allows you to initiate a purchase directly from the sales invoice that requires the items.</span></span>

<span data-ttu-id="13da1-113">Les documents vente et achat peuvent être validés comme étant expédiés ou uniquement reçus ou expédiés ou reçus et facturés, ce qui vous permet de répartir les responsabilités des préparateurs de commandes et des rôles de comptabilité.</span><span class="sxs-lookup"><span data-stu-id="13da1-113">Both sales and purchase documents can be posted as shipped or received only or as shipped or received and invoiced, allowing you to split the responsibilities of order processors and accounting roles.</span></span>

<span data-ttu-id="13da1-114">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="13da1-114">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="13da1-115">Pour</span><span class="sxs-lookup"><span data-stu-id="13da1-115">To</span></span> | <span data-ttu-id="13da1-116">Voir</span><span class="sxs-lookup"><span data-stu-id="13da1-116">See</span></span> |
| --- | --- |
| <span data-ttu-id="13da1-117">Enregistrer les nouveaux clients, effectuer les offres de vente, vendre les produits sur les commandes ou les factures, par exemple sous forme de livraisons directes, et gérer les retours vente.</span><span class="sxs-lookup"><span data-stu-id="13da1-117">Register new customers, make sales offers, sell products on orders or invoices, for example as drop shipments, and manage sales returns.</span></span> |[<span data-ttu-id="13da1-118">Ventes</span><span class="sxs-lookup"><span data-stu-id="13da1-118">Sales</span></span>](sales-manage-sales.md) |
| <span data-ttu-id="13da1-119">Enregistrer les nouveaux fournisseurs, acheter des articles sur les commandes ou les factures, par exemple initiés à partir d'une facture vente, et gérer les retours achat.</span><span class="sxs-lookup"><span data-stu-id="13da1-119">Register new vendors, purchase items on orders or invoices, for example initiated from a sales invoice, and manage purchase returns.</span></span> |[<span data-ttu-id="13da1-120">Achats</span><span class="sxs-lookup"><span data-stu-id="13da1-120">Purchasing</span></span>](purchasing-manage-purchasing.md) |
| <span data-ttu-id="13da1-121">Enregistrer de nouveaux produits physiques ou services, ajuster les quantités en stock, et gérer la valeur stock en validant les coûts ajustés en comptabilité.</span><span class="sxs-lookup"><span data-stu-id="13da1-121">Register new physical or service products, adjust inventory quantities, and manage the inventory value by posting adjusted costs to the general ledger.</span></span> |[<span data-ttu-id="13da1-122">Stock</span><span class="sxs-lookup"><span data-stu-id="13da1-122">Inventory</span></span>](inventory-manage-inventory.md) |

## <a name="see-also"></a><span data-ttu-id="13da1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13da1-123">See Also</span></span>
[<span data-ttu-id="13da1-124">Définition des ventes</span><span class="sxs-lookup"><span data-stu-id="13da1-124">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="13da1-125">[Gestion des comptes client](receivables-manage-receivables.md)   </span><span class="sxs-lookup"><span data-stu-id="13da1-125">[Managing Receivables](receivables-manage-receivables.md)   </span></span>  
[<span data-ttu-id="13da1-126">Définition des achats</span><span class="sxs-lookup"><span data-stu-id="13da1-126">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
<span data-ttu-id="13da1-127">[Gestion des comptes fournisseur](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="13da1-127">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="13da1-128">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="13da1-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="13da1-129">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="13da1-129">General Business Functionality</span></span>](ui-across-business-areas.md)

