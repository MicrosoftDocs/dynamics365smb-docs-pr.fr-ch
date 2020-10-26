---
title: Détails de conception - ligne validation de feuille comptabilité | Microsoft Docs
description: Cette rubrique fournit une analyse des concepts et principes qui sont utilisés pour reconcevoir la fonction de ligne validation feuille comptabilité dans Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: aaffac8fe7e10d0155649c960803f65a8136c46d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911095"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="27cbd-103">Détails de conception : Ligne validation de feuille comptabilité</span><span class="sxs-lookup"><span data-stu-id="27cbd-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="27cbd-104">Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés pour reconcevoir la fonction de ligne validation feuille comptabilité dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="27cbd-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="27cbd-105">La nouvelle conception rend le codeunit 12 plus simple et plus facile à modifier.</span><span class="sxs-lookup"><span data-stu-id="27cbd-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="27cbd-106">La documentation commence par des présentations conceptuelles de la nouvelle conception.</span><span class="sxs-lookup"><span data-stu-id="27cbd-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="27cbd-107">Alors il explique l’architecture technique pour indiquer les modifications découlant de la nouvelle conception.</span><span class="sxs-lookup"><span data-stu-id="27cbd-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="27cbd-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="27cbd-108">In This Section</span></span>  
[<span data-ttu-id="27cbd-109">Aperçu de la ligne validation de feuille comptabilité</span><span class="sxs-lookup"><span data-stu-id="27cbd-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="27cbd-110">Détails de conception : Structure de l’interface de validation</span><span class="sxs-lookup"><span data-stu-id="27cbd-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="27cbd-111">Détails de conception : Structure du moteur de validation</span><span class="sxs-lookup"><span data-stu-id="27cbd-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="27cbd-112">Codeunit 12 modifications : variables globales de mappage pour la ligne de validation de feuille comptabilité</span><span class="sxs-lookup"><span data-stu-id="27cbd-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="27cbd-113">Codeunit 12 modifications : modifications dans les procédures de validation de feuille comptabilité</span><span class="sxs-lookup"><span data-stu-id="27cbd-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="27cbd-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27cbd-114">See Also</span></span>  
[<span data-ttu-id="27cbd-115">Utilisation de feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="27cbd-115">Working with General Journals</span></span>](ui-work-general-journals.md)
