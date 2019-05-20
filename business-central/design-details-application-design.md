---
title: Détails de conception | Microsoft Docs
description: Ce contenu comprend des informations techniques détaillées sur les fonctionnalités d'application complexes dans Business Central.
author: SorenGP
documentationcenter: ''
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e16ebdd8fc7b1b147b17d395241b6e67bb008fd1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244025"
---
# <a name="design-details"></a><span data-ttu-id="cde7a-103">Détails de conception</span><span class="sxs-lookup"><span data-stu-id="cde7a-103">Design Details</span></span>
<span data-ttu-id="cde7a-104">Ce contenu comprend des informations techniques détaillées sur les fonctionnalités d'application complexes dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="cde7a-104">This content contains detailed technical information about complex application features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

 <span data-ttu-id="cde7a-105">Le contenu des détails de conception est destiné aux implémenteurs, développeurs et super utilisateurs qui ont besoin d'une analyse approfondie pour implémenter, personnaliser ou créer les fonctionnalités en question.</span><span class="sxs-lookup"><span data-stu-id="cde7a-105">Design details content is aimed at implementers, developers, and super users who need deeper insight to implement, customize, or set up the features in question.</span></span>  

|<span data-ttu-id="cde7a-106">**Pour**</span><span class="sxs-lookup"><span data-stu-id="cde7a-106">**To**</span></span>|<span data-ttu-id="cde7a-107">**Voir**</span><span class="sxs-lookup"><span data-stu-id="cde7a-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="cde7a-108">En savoir plus sur la manière dont le système de planification fonctionne et comment modifier les algorithmes pour répondre aux exigences de planification dans différents environnements.</span><span class="sxs-lookup"><span data-stu-id="cde7a-108">Learn how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="cde7a-109">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="cde7a-109">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|  
|<span data-ttu-id="cde7a-110">Comprenez les mécanismes dans le moteur d'évaluation, comme le mode d'évaluation et l'ajustement des coûts, et pour quels principes de compatibilité ils sont conçus.</span><span class="sxs-lookup"><span data-stu-id="cde7a-110">Understand mechanisms in the costing engine, such as costing method and cost adjustment, and which accounting principles they are designed for.</span></span>|[<span data-ttu-id="cde7a-111">Détails de conception : évaluation stock</span><span class="sxs-lookup"><span data-stu-id="cde7a-111">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  
|<span data-ttu-id="cde7a-112">En savoir plus sur les principes centraux derrière les fonctions entrepôt avancées et de base et comment elles s'intègrent avec d'autres fonctionnalités de chaîne d'approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="cde7a-112">Learn about central principles behind advanced and basic warehouse features and how they integrate with other supply chain features.</span></span>|[<span data-ttu-id="cde7a-113">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="cde7a-113">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)|  
|<span data-ttu-id="cde7a-114">En savoir plus sur l'historique et la conception actuelle de la fonctionnalité de traçabilité et la manière dont elle s'intègre avec le système de réservation pour inclure les numéros de série/lot dans les calculs de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="cde7a-114">Learn about historic and the current design of item tracking functionality and how it integrates with the reservation system to include serial/lot numbers in availability calculations.</span></span>|[<span data-ttu-id="cde7a-115">Détails de conception : traçabilité</span><span class="sxs-lookup"><span data-stu-id="cde7a-115">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)|  
|<span data-ttu-id="cde7a-116">En savoir plus sur la fonction de ligne validation de feuille comptabilité, y compris les simplifications récentes apportées à la conception du codeunit 12.</span><span class="sxs-lookup"><span data-stu-id="cde7a-116">Learn about the General Journal Posting Line feature, including recent simplifications to the design of codeunit 12.</span></span>|[<span data-ttu-id="cde7a-117">Détails de conception : Ligne validation de feuille comptabilité</span><span class="sxs-lookup"><span data-stu-id="cde7a-117">Design Details: General Journal Post Line</span></span>](design-details-general-journal-post-line.md)|
|<span data-ttu-id="cde7a-118">En savoir plus sur la conception des axes de stockage et validation, notamment des exemples code sur la façon de migrer et mettre à niveau le code axe analytique.</span><span class="sxs-lookup"><span data-stu-id="cde7a-118">Learn about the design for storing and posting dimensions, including code examples on how to migrate and upgrade dimension code.</span></span>|[<span data-ttu-id="cde7a-119">Détails de conception : écritures d'ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="cde7a-119">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)| 

## <a name="see-also"></a><span data-ttu-id="cde7a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cde7a-120">See Also</span></span>  
 <span data-ttu-id="cde7a-121">[Planifié](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="cde7a-121">[Planning](production-planning.md) </span></span>  
 <span data-ttu-id="cde7a-122">[Gestion des coûts ajustés](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="cde7a-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="cde7a-123">[Gestion d'entrepôt](warehouse-manage-warehouse.md) </span><span class="sxs-lookup"><span data-stu-id="cde7a-123">[Warehouse Management](warehouse-manage-warehouse.md) </span></span>  
 [<span data-ttu-id="cde7a-124">Configuration des modules complexes à l'aide des meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="cde7a-124">Setting Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="cde7a-125">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cde7a-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

 ## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
