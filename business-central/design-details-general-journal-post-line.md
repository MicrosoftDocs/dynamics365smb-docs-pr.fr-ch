---
title: Détails de conception - ligne validation de feuille comptabilité | Microsoft Docs
description: Cette rubrique fournit une analyse des concepts et principes qui sont utilisés pour reconcevoir la fonction de ligne validation feuille comptabilité dans Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8492c83437be4cd850bafdaaa5dc70d00a075674
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215243"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="69a93-103">Détails de conception : Ligne validation de feuille comptabilité</span><span class="sxs-lookup"><span data-stu-id="69a93-103">Design Details: General Journal Post Line</span></span>

<span data-ttu-id="69a93-104">Cette documentation fournit une analyse technique détaillée des concepts et principes qui ont été utilisés pour reconcevoir la fonction de ligne validation feuille comptabilité dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="69a93-104">This documentation provides detailed technical insight into the concepts and principles that were used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="69a93-105">La nouvelle conception a rendu le codeunit 12 plus simple et plus facile à modifier.</span><span class="sxs-lookup"><span data-stu-id="69a93-105">The redesign made codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="69a93-106">La documentation commence par des présentations conceptuelles de la nouvelle conception.</span><span class="sxs-lookup"><span data-stu-id="69a93-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="69a93-107">Alors il explique l’architecture technique pour indiquer les modifications découlant de la nouvelle conception.</span><span class="sxs-lookup"><span data-stu-id="69a93-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="69a93-108">Les informations de cette section s’appliquent à la nouvelle conception dans une version antérieure du produit, Microsoft Dynamics NAV 2013 R2.</span><span class="sxs-lookup"><span data-stu-id="69a93-108">The information in this section applies to the redesign in an earlier version of the product, Microsoft Dynamics NAV 2013 R2.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="69a93-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="69a93-109">In This Section</span></span>

[<span data-ttu-id="69a93-110">Aperçu de la ligne validation de feuille comptabilité</span><span class="sxs-lookup"><span data-stu-id="69a93-110">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="69a93-111">Détails de conception : Structure de l’interface de validation</span><span class="sxs-lookup"><span data-stu-id="69a93-111">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="69a93-112">Détails de conception : Structure du moteur de validation</span><span class="sxs-lookup"><span data-stu-id="69a93-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  

## <a name="see-also"></a><span data-ttu-id="69a93-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69a93-113">See Also</span></span>

<span data-ttu-id="69a93-114">[Utilisation de feuilles comptabilité](ui-work-general-journals.md)
[Détails de conception : Ligne validation de feuille comptabilité (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span><span class="sxs-lookup"><span data-stu-id="69a93-114">[Working with General Journals](ui-work-general-journals.md)
[Design Details: General Journal Post Line (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]