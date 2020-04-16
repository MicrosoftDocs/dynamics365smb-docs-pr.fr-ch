---
title: Détails de conception - Gestion d'entrepôt | Microsoft Docs
description: Cette rubrique donne un aperçu de la conception, des concepts et des principes associés aux fonctionnalités de gestion d'entrepôt dans Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 91e2f135f97e8d1e80edce3c6e45e08a080e826f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184739"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="4fbcf-103">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="4fbcf-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="4fbcf-104">Cette documentation donne un aperçu des concepts et principes et qui sont utilisés dans les fonctionnalités de Warehouse Management dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4fbcf-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4fbcf-105">Elle explique la conception derrière les fonctions entrepôt centrales et la manière dont l'entreposage s'intègre à d'autres fonctionnalités de chaîne d'approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="4fbcf-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="4fbcf-106">Pour différencier les différents niveaux de complexité de l'entreposage, ces documents sont divisés en deux groupes généraux, les configurations d'entrepôt de base et avancées, indiqués par les titres de section.</span><span class="sxs-lookup"><span data-stu-id="4fbcf-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="4fbcf-107">Cette différenciation unique couvre différents niveaux de complexité tels que définis par les granules produit et la configuration du magasin.</span><span class="sxs-lookup"><span data-stu-id="4fbcf-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="4fbcf-108">Pour plus d'informations, reportez\-vous à [Détails de conception : Paramètres entrepôt](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="4fbcf-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="4fbcf-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4fbcf-109">In This Section</span></span>  
[<span data-ttu-id="4fbcf-110">Détails de conception : vue d'ensemble d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="4fbcf-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="4fbcf-111">Détails de conception : paramètres entrepôt</span><span class="sxs-lookup"><span data-stu-id="4fbcf-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="4fbcf-112">Détails de conception : flux d'enlogement</span><span class="sxs-lookup"><span data-stu-id="4fbcf-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="4fbcf-113">Détails de conception : flux d'entrepôt internes</span><span class="sxs-lookup"><span data-stu-id="4fbcf-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="4fbcf-114">Détails de conception : disponibilité dans l'entrepôt</span><span class="sxs-lookup"><span data-stu-id="4fbcf-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="4fbcf-115">Détails de conception : flux de désenlogement</span><span class="sxs-lookup"><span data-stu-id="4fbcf-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="4fbcf-116">Détails de conception : intégration avec le stock</span><span class="sxs-lookup"><span data-stu-id="4fbcf-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)
