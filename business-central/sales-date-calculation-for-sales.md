---
title: Calcul de la date des ventes | Microsoft Docs
description: L'application calcule automatiquement la date à laquelle vous devez commander un article pour l'avoir en stock à une certaine date. Il s'agit de la date à laquelle des articles commandés à une date donnée devraient être disponibles pour le prélèvement.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0fa1f07b5da450a2e6f634bda07752efd0e35889
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312259"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="d7e45-104">Calcul de la date des ventes</span><span class="sxs-lookup"><span data-stu-id="d7e45-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d7e45-105">calcule automatiquement la première date possible à laquelle un article d'une ligne commande vente peut être expédié.</span><span class="sxs-lookup"><span data-stu-id="d7e45-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="d7e45-106">Si le client a demandé une date livraison particulière, alors la date à laquelle les articles doivent pouvoir être prélevés est calculée pour permettre une livraison à cette date.</span><span class="sxs-lookup"><span data-stu-id="d7e45-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="d7e45-107">Si le client ne demande pas de date livraison particulière, alors la date à laquelle les articles peuvent être livrés, à partir de la date à laquelle les articles peuvent être prélevés, est calculée.</span><span class="sxs-lookup"><span data-stu-id="d7e45-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="d7e45-108">Calcul d'une date de livraison demandée</span><span class="sxs-lookup"><span data-stu-id="d7e45-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="d7e45-109">Si vous spécifiez une date de livraison demandée sur la ligne vente, cette date devient le point de départ du calcul suivant :</span><span class="sxs-lookup"><span data-stu-id="d7e45-109">If you specify a requested delivery date on the sales order line, that date becomes the starting point for the following calculations.</span></span>

- <span data-ttu-id="d7e45-110">Date livraison demandée - délai d'expédition = date d'expédition planifiée</span><span class="sxs-lookup"><span data-stu-id="d7e45-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="d7e45-111">Date d'expédition + délai désenlogement = date d'expédition planifiée</span><span class="sxs-lookup"><span data-stu-id="d7e45-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="d7e45-112">Si les articles peuvent être prélevés à la date d'expédition, alors le processus vente peut continuer.</span><span class="sxs-lookup"><span data-stu-id="d7e45-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span> <span data-ttu-id="d7e45-113">Sinon, un avertissement de rupture de stock est affiché.</span><span class="sxs-lookup"><span data-stu-id="d7e45-113">Otherwise, a stock-out warning is displayed.</span></span>

> [!Note]
> <span data-ttu-id="d7e45-114">Si votre processus est basé sur un calcul en amont, par exemple, si vous utilisez la date livraison demandée pour obtenir la date livraison planifiée, nous vous recommandons d’utiliser des formules de date ayant des durées fixes, telles que "5D" pendant cinq jours ou "1W" pour une semaine.</span><span class="sxs-lookup"><span data-stu-id="d7e45-114">If your process is based on backward calculation, for example, if you use the requested delivery date to get the planned shipment date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="d7e45-115">Les formules de date sans durée fixe, telles que "CW" pour la semaine en cours ou CM pour le mois en cours, peuvent entraîner des calculs de date incorrects.</span><span class="sxs-lookup"><span data-stu-id="d7e45-115">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="d7e45-116">Pour plus d'informations sur les formules de date, voir [Utilisation de dates civiles et des heures](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="d7e45-116">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="d7e45-117">Calcul de la première date de livraison possible</span><span class="sxs-lookup"><span data-stu-id="d7e45-117">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="d7e45-118">Si vous ne spécifiez aucune date livraison demandée sur la ligne de commande vente ou si la date livraison demandée ne peut pas être respectée, alors la première date à laquelle les articles sont disponibles est calculée.</span><span class="sxs-lookup"><span data-stu-id="d7e45-118">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="d7e45-119">Cette date est ensuite renseignée dans le champ Date d'expédition sur la ligne, et la date à laquelle vous prévoyez d'expédier les articles, ainsi que la date à laquelle ces derniers seront livrés au client sont calculées via les formules suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7e45-119">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="d7e45-120">Date d'expédition + délai désenlogement = date d'expédition planifiée</span><span class="sxs-lookup"><span data-stu-id="d7e45-120">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="d7e45-121">Date livraison planifiée - délai d'expédition = date expédition planifiée</span><span class="sxs-lookup"><span data-stu-id="d7e45-121">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="d7e45-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7e45-122">See Also</span></span>  
 <span data-ttu-id="d7e45-123">[Calcul de la date des achats](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="d7e45-123">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="d7e45-124">Calculer des dates promesse livraison</span><span class="sxs-lookup"><span data-stu-id="d7e45-124">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="d7e45-125">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d7e45-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
