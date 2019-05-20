---
title: "Détails de conception : écritures d'ensemble de dimensions | Microsoft Docs"
description: Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés pour reconcevoir la fonction de stockage et de validation d'écritures de dimension.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c6b66ecee87e1fd128733f541d46b97f44af0453
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242759"
---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="37de6-103">Détails de conception : écritures d'ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="37de6-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="37de6-104">Cette documentation fournit une analyse technique détaillée des concepts et principes du stockage d'entrée de dimension et la fonction de validation dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="37de6-104">This documentation provides detailed technical insight into the concepts and principles of the dimension-entry storing and posting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="37de6-105">La documentation commence par des présentations conceptuelles.</span><span class="sxs-lookup"><span data-stu-id="37de6-105">The documentation starts by describing conceptual overviews.</span></span> <span data-ttu-id="37de6-106">Puis elle explique l'architecture technique.</span><span class="sxs-lookup"><span data-stu-id="37de6-106">Then it explains the technical architecture.</span></span> <span data-ttu-id="37de6-107">Enfin, elle fournit des exemples de code pour vous préparer à la migration et à la mise à niveau du code axe depuis les versions antérieures à Dynamics NAV 2013R2.</span><span class="sxs-lookup"><span data-stu-id="37de6-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade from versions earlier than Dynamics NAV 2013R2.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="37de6-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="37de6-108">In This Section</span></span>  
[<span data-ttu-id="37de6-109">Aperçu des écritures de l'ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="37de6-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="37de6-110">Détails de conception : recherche des croisements analytiques</span><span class="sxs-lookup"><span data-stu-id="37de6-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="37de6-111">Détails de conception : structure de la table</span><span class="sxs-lookup"><span data-stu-id="37de6-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="37de6-112">Détails de conception : Codeunit 408 Gestion des axes analytiques</span><span class="sxs-lookup"><span data-stu-id="37de6-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="37de6-113">Détails de conception : exemples de code de motifs modifiés dans les modifications</span><span class="sxs-lookup"><span data-stu-id="37de6-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
