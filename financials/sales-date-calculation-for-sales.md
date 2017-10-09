---
title: Calcul de la date des ventes | Microsoft Docs
description: "Le programme calcule automatiquement la date à laquelle vous devez commander un article pour l'avoir en stock à une certaine date. Il s'agit de la date à laquelle des articles commandés à une date donnée devraient être disponibles pour le prélèvement."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4e8bc9e8b99db8afda83edb4aff13f5daf9f5a31
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="15a73-104">Calcul de la date des ventes</span><span class="sxs-lookup"><span data-stu-id="15a73-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="15a73-105"> calcule automatiquement la première date possible à laquelle un article d'une ligne commande vente peut être expédié.</span><span class="sxs-lookup"><span data-stu-id="15a73-105"> automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="15a73-106">Si le client a demandé une date livraison particulière, alors la date à laquelle les articles doivent pouvoir être prélevés est calculée pour permettre une livraison à cette date.</span><span class="sxs-lookup"><span data-stu-id="15a73-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="15a73-107">Si le client ne demande pas de date livraison particulière, alors la date à laquelle les articles peuvent être livrés, à partir de la date à laquelle les articles peuvent être prélevés, est calculée.</span><span class="sxs-lookup"><span data-stu-id="15a73-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="15a73-108">Calcul d'une date de livraison demandée</span><span class="sxs-lookup"><span data-stu-id="15a73-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="15a73-109">Si vous spécifiez une date de livraison demandée sur la ligne vente, alors cette date est utilisée comme point de départ du calcul suivant :</span><span class="sxs-lookup"><span data-stu-id="15a73-109">If you specify a requested delivery date on the sales order line, then that date is used as the starting point for the following calculations.</span></span>

- <span data-ttu-id="15a73-110">Date livraison demandée - délai d'expédition = date d'expédition planifiée</span><span class="sxs-lookup"><span data-stu-id="15a73-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="15a73-111">Date d'expédition + délai désenlogement = date d'expédition planifiée</span><span class="sxs-lookup"><span data-stu-id="15a73-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="15a73-112">Si les articles peuvent être prélevés à la date d'expédition, alors le processus vente peut continuer.</span><span class="sxs-lookup"><span data-stu-id="15a73-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span>

<span data-ttu-id="15a73-113">Si les articles ne peuvent pas être prélevés à la date d'expédition, alors une alerte rupture de stock est affichée.</span><span class="sxs-lookup"><span data-stu-id="15a73-113">If the items are not available to be picked on the shipment date, then a stock-out warning is displayed.</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="15a73-114">Calcul de la première date de livraison possible</span><span class="sxs-lookup"><span data-stu-id="15a73-114">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="15a73-115">Si vous ne spécifiez aucune date livraison demandée sur la ligne de commande vente ou si la date livraison demandée ne peut pas être respectée, alors la première date à laquelle les articles sont disponibles est calculée.</span><span class="sxs-lookup"><span data-stu-id="15a73-115">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="15a73-116">Cette date est ensuite renseignée dans le champ Date d'expédition sur la ligne, et la date à laquelle vous prévoyez d'expédier les articles, ainsi que la date à laquelle ces derniers seront livrés au client sont calculées via les formules suivantes.</span><span class="sxs-lookup"><span data-stu-id="15a73-116">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="15a73-117">Date d'expédition + délai désenlogement = date d'expédition planifiée</span><span class="sxs-lookup"><span data-stu-id="15a73-117">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="15a73-118">Date livraison planifiée - délai d'expédition = date expédition planifiée</span><span class="sxs-lookup"><span data-stu-id="15a73-118">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="15a73-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15a73-119">See Also</span></span>  
 <span data-ttu-id="15a73-120">[Calcul de la date des achats](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="15a73-120">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="15a73-121">Comment calculer des dates promesse livraison</span><span class="sxs-lookup"><span data-stu-id="15a73-121">How to: Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="15a73-122">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="15a73-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

