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
# <a name="design-details-general-journal-post-line"></a>Détails de conception : Ligne validation de feuille comptabilité

Cette documentation fournit une analyse technique détaillée des concepts et principes qui ont été utilisés pour reconcevoir la fonction de ligne validation feuille comptabilité dans [!INCLUDE[prod_short](includes/prod_short.md)]. La nouvelle conception a rendu le codeunit 12 plus simple et plus facile à modifier. La documentation commence par des présentations conceptuelles de la nouvelle conception. Alors il explique l’architecture technique pour indiquer les modifications découlant de la nouvelle conception.  

> [!IMPORTANT]
> Les informations de cette section s’appliquent à la nouvelle conception dans une version antérieure du produit, Microsoft Dynamics NAV 2013 R2.

## <a name="in-this-section"></a>Dans cette section

[Aperçu de la ligne validation de feuille comptabilité](design-details-general-journal-post-line-overview.md)  
[Détails de conception : Structure de l’interface de validation](design-details-posting-interface-structure.md)  
[Détails de conception : Structure du moteur de validation](design-details-posting-engine-structure.md)  

## <a name="see-also"></a>Voir aussi

[Utilisation de feuilles comptabilité](ui-work-general-journals.md)
[Détails de conception : Ligne validation de feuille comptabilité (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)  

[!INCLUDE[footer-include](includes/footer-banner.md)]