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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: fd1929e0a9a491a8197a209f27c4961af6697461
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307195"
---
# <a name="design-details-general-journal-post-line"></a>Détails de conception : Ligne validation de feuille comptabilité
Cette documentation fournit une analyse technique détaillée des concepts et principes qui sont utilisés pour reconcevoir la fonction de ligne validation feuille comptabilité dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. La nouvelle conception rend le codeunit 12 plus simple et plus facile à modifier. La documentation commence par des présentations conceptuelles de la nouvelle conception. Alors il explique l'architecture technique pour indiquer les modifications découlant de la nouvelle conception.  

## <a name="in-this-section"></a>Dans cette section  
[Aperçu de la ligne validation de feuille comptabilité](design-details-general-journal-post-line-overview.md)  
[Détails de conception : Structure de l'interface de validation](design-details-posting-interface-structure.md)  
[Détails de conception : Structure du moteur de validation](design-details-posting-engine-structure.md)  
[Codeunit 12 modifications : variables globales de mappage pour la ligne de validation de feuille comptabilité](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[Codeunit 12 modifications : modifications dans les procédures de validation de feuille comptabilité](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a>Voir aussi  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)
