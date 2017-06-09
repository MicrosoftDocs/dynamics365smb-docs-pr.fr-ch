---
title: "Procédure : octroyer une priorité à des fournisseurs| Microsoft Docs"
description: "Procédure : octroyer une priorité à des fournisseurs"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ae80ae9ecc15838b59999ded775c7fa0063c8a54
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-prioritize-vendors"></a>Procédure : octroyer une priorité à des fournisseurs
[!INCLUDE[d365fin](includes/d365fin_md.md)] peut proposer différents paiements aux fournisseurs, par exemple les paiements arrivant à échéance ou les paiements donnant lieu à un escompte. Pour plus d'informations, reportez vous à [Procédure : proposer des paiements fournisseur](payables-how-suggest-vendor-payments.md).

Tout d'abord, vous devez attribuer une priorité à vos fournisseurs en leur affectant des numéros.

## <a name="to-prioritize-vendors"></a>Pour octroyer une priorité à des fournisseurs
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Fournisseurs**, puis sélectionnez le lien associé.
2. Sélectionnez le fournisseur approprié, puis sélectionnez **Modifier**.
3. Dans le champ **Priorité**, entrez un numéro.

[!INCLUDE[d365fin](includes/d365fin_md.md)] donne le degré de priorité le plus élevé au chiffre le plus bas, excepté 0. Ainsi, si vous utilisez 1, 2 et 3, le chiffre 1 a le degré de priorité le plus élevé.

Si vous ne souhaitez pas attribuer de priorité à un fournisseur, laissez le champ **Priorité** blanc. Par la suite, lorsque vous utilisez la fonction de proposition de paiements, ce fournisseur est répertorié après tous les fournisseurs possédant un numéro prioritaire. Vous pouvez saisir autant de niveaux de priorité que nécessaire.

## <a name="see-also"></a>Voir aussi
[Définition des achats](purchasing-setup-purchasing.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

