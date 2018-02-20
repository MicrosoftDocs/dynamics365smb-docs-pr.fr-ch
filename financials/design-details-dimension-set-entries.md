---
title: "Détails de conception : écritures d'ensemble de dimensions | Microsoft Docs"
description: "Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés pour reconcevoir la fonction de stockage et de validation d'écritures de dimension."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 17fd783bd44faa914d473aae35ddc31145c181ef
ms.contentlocale: fr-ch
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="1dfa9-103">Détails de conception : écritures d'ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="1dfa9-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="1dfa9-104">Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés pour reconcevoir le stockage d'entrée de dimension et la fonction de validation dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1dfa9-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the dimension entry storing and posting feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1dfa9-105">La documentation commence par des présentations conceptuelles de la nouvelle conception.</span><span class="sxs-lookup"><span data-stu-id="1dfa9-105">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="1dfa9-106">Alors il explique l'architecture technique pour indiquer la manière dont la nouvelle conception est créée.</span><span class="sxs-lookup"><span data-stu-id="1dfa9-106">Then it explains the technical architecture to show how the redesign is made.</span></span> <span data-ttu-id="1dfa9-107">Enfin, elle fournit des exemples de code pour vous préparer à la migration et à la mise à niveau du code axe.</span><span class="sxs-lookup"><span data-stu-id="1dfa9-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="1dfa9-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="1dfa9-108">In This Section</span></span>  
[<span data-ttu-id="1dfa9-109">Aperçu des écritures de l'ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="1dfa9-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="1dfa9-110">Détails de conception : recherche des croisements analytiques</span><span class="sxs-lookup"><span data-stu-id="1dfa9-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="1dfa9-111">Détails de conception : structure de la table</span><span class="sxs-lookup"><span data-stu-id="1dfa9-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="1dfa9-112">Détails de conception : Codeunit 408 Gestion des axes analytiques</span><span class="sxs-lookup"><span data-stu-id="1dfa9-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="1dfa9-113">Détails de conception : exemples de code de motifs modifiés dans les modifications</span><span class="sxs-lookup"><span data-stu-id="1dfa9-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

