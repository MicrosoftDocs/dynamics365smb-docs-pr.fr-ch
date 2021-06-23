---
title: Détails de conception - Planification de l’approvisionnement | Microsoft Docs
description: Cette rubrique donne un aperçu des concepts et principes qui sont utilisés avec les fonctionnalités de planification de l’approvisionnement dans Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, planning, reordering, replenishment
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 78b5700646d95d9cdc38a7a67663473fafddaa2c
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214843"
---
# <a name="design-details-supply-planning"></a><span data-ttu-id="66000-103">Détails de conception : planification de l’approvisionnement</span><span class="sxs-lookup"><span data-stu-id="66000-103">Design Details: Supply Planning</span></span>
<span data-ttu-id="66000-104">Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés dans les fonctions Supply Planning dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="66000-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Supply Planning features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="66000-105">Elle explique comment le système de planification fonctionne et comment modifier les algorithmes pour répondre aux exigences de planification dans différents environnements.</span><span class="sxs-lookup"><span data-stu-id="66000-105">It explains how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span> <span data-ttu-id="66000-106">Elle présente d’abord les concepts centraux de solution, puis décrit la logique du mécanisme central, l’équilibrage d’approvisionnement, avant de continuer pour indiquer la manière dont la planification de stock est exécutée avec l’utilisation des méthodes de réapprovisionnement.</span><span class="sxs-lookup"><span data-stu-id="66000-106">It first introduces central solution concepts and then describes the logic of the central mechanism, supply balancing, before proceeding to explain how inventory planning is performed with the use of reordering policies.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="66000-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="66000-107">In This Section</span></span>  
[<span data-ttu-id="66000-108">Détails de conception : concepts centraux du système de planification</span><span class="sxs-lookup"><span data-stu-id="66000-108">Design Details: Central Concepts of the Planning System</span></span>](design-details-central-concepts-of-the-planning-system.md)  
[<span data-ttu-id="66000-109">Détails de conception : réservation, chaînage et message d’action</span><span class="sxs-lookup"><span data-stu-id="66000-109">Design Details: Reservation, Order Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
[<span data-ttu-id="66000-110">Détails de conception : équilibrage de la demande et de l’approvisionnement</span><span class="sxs-lookup"><span data-stu-id="66000-110">Design Details: Balancing Demand and Supply</span></span>](design-details-balancing-demand-and-supply.md)  
[<span data-ttu-id="66000-111">Détails de conception : gestion des méthodes de réapprovisionnement</span><span class="sxs-lookup"><span data-stu-id="66000-111">Design Details: Handling Reordering Policies</span></span>](design-details-handling-reordering-policies.md)  
[<span data-ttu-id="66000-112">Détails de conception : paramètres de planification</span><span class="sxs-lookup"><span data-stu-id="66000-112">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
[<span data-ttu-id="66000-113">Détails de conception : tableau d’affectation de planification</span><span class="sxs-lookup"><span data-stu-id="66000-113">Design Details: Planning Assignment Table</span></span>](design-details-planning-assignment-table.md)  
[<span data-ttu-id="66000-114">Détails de conception : demande à un magasin vide.</span><span class="sxs-lookup"><span data-stu-id="66000-114">Design Details: Demand at Blank Location</span></span>](design-details-demand-at-blank-location.md)  
[<span data-ttu-id="66000-115">Détails de conception : transferts de planification</span><span class="sxs-lookup"><span data-stu-id="66000-115">Design Details: Transfers in Planning</span></span>](design-details-transfers-in-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]