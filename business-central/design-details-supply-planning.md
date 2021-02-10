---
title: Détails de conception - Planification de l’approvisionnement | Microsoft Docs
description: Cette rubrique donne un aperçu des concepts et principes qui sont utilisés avec les fonctionnalités de planification de l’approvisionnement dans Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, planning, reordering, replenishment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ed874c647dd5c3526df38a3c4d6ee43293737786
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751095"
---
# <a name="design-details-supply-planning"></a><span data-ttu-id="91957-103">Détails de conception : planification de l’approvisionnement</span><span class="sxs-lookup"><span data-stu-id="91957-103">Design Details: Supply Planning</span></span>
<span data-ttu-id="91957-104">Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés dans les fonctions Supply Planning dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="91957-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Supply Planning features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="91957-105">Elle explique comment le système de planification fonctionne et comment modifier les algorithmes pour répondre aux exigences de planification dans différents environnements.</span><span class="sxs-lookup"><span data-stu-id="91957-105">It explains how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span> <span data-ttu-id="91957-106">Elle présente d’abord les concepts centraux de solution, puis décrit la logique du mécanisme central, l’équilibrage d’approvisionnement, avant de continuer pour indiquer la manière dont la planification de stock est exécutée avec l’utilisation des méthodes de réapprovisionnement.</span><span class="sxs-lookup"><span data-stu-id="91957-106">It first introduces central solution concepts and then describes the logic of the central mechanism, supply balancing, before proceeding to explain how inventory planning is performed with the use of reordering policies.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="91957-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="91957-107">In This Section</span></span>  
[<span data-ttu-id="91957-108">Détails de conception : concepts centraux du système de planification</span><span class="sxs-lookup"><span data-stu-id="91957-108">Design Details: Central Concepts of the Planning System</span></span>](design-details-central-concepts-of-the-planning-system.md)  
[<span data-ttu-id="91957-109">Détails de conception : réservation, chaînage et message d’action</span><span class="sxs-lookup"><span data-stu-id="91957-109">Design Details: Reservation, Order Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
[<span data-ttu-id="91957-110">Détails de conception : équilibrage de la demande et de l’approvisionnement</span><span class="sxs-lookup"><span data-stu-id="91957-110">Design Details: Balancing Demand and Supply</span></span>](design-details-balancing-demand-and-supply.md)  
[<span data-ttu-id="91957-111">Détails de conception : gestion des méthodes de réapprovisionnement</span><span class="sxs-lookup"><span data-stu-id="91957-111">Design Details: Handling Reordering Policies</span></span>](design-details-handling-reordering-policies.md)  
[<span data-ttu-id="91957-112">Détails de conception : paramètres de planification</span><span class="sxs-lookup"><span data-stu-id="91957-112">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
[<span data-ttu-id="91957-113">Détails de conception : tableau d’affectation de planification</span><span class="sxs-lookup"><span data-stu-id="91957-113">Design Details: Planning Assignment Table</span></span>](design-details-planning-assignment-table.md)  
[<span data-ttu-id="91957-114">Détails de conception : demande à un magasin vide.</span><span class="sxs-lookup"><span data-stu-id="91957-114">Design Details: Demand at Blank Location</span></span>](design-details-demand-at-blank-location.md)  
[<span data-ttu-id="91957-115">Détails de conception : transferts de planification</span><span class="sxs-lookup"><span data-stu-id="91957-115">Design Details: Transfers in Planning</span></span>](design-details-transfers-in-planning.md)
