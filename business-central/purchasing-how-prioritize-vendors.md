---
title: "Affecter un niveau de priorité à un fournisseur | Microsoft Docs"
description: "Vous pouvez affecter des numéros à vos fournisseurs pour les classer par ordre de priorité et faciliter des propositions de paiement dans Business Central."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: cb3556c9bd8fb893448d61c4e8f18131b96a9841
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="prioritize-vendors"></a>Octroyer une priorité aux fournisseurs
[!INCLUDE[d365fin](includes/d365fin_md.md)] peut proposer différents paiements aux fournisseurs, par exemple les paiements arrivant à échéance ou les paiements donnant lieu à un escompte. Pour plus d'informations, reportez vous à [Proposer des paiements fournisseur](payables-how-suggest-vendor-payments.md).

Tout d'abord, vous devez attribuer une priorité à vos fournisseurs en leur affectant des numéros.

## <a name="to-prioritize-vendors"></a>Pour octroyer une priorité à des fournisseurs
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Fournisseurs**, puis sélectionnez le lien associé.
2. Sélectionnez le fournisseur approprié, puis sélectionnez **Modifier**.
3. Dans le champ **Priorité**, entrez un numéro.

[!INCLUDE[d365fin](includes/d365fin_md.md)] donne le degré de priorité le plus élevé au chiffre le plus bas, excepté 0. Ainsi, si vous utilisez 1, 2 et 3, le chiffre 1 a le degré de priorité le plus élevé.

Si vous ne souhaitez pas attribuer de priorité à un fournisseur, laissez le champ **Priorité** blanc. Par la suite, lorsque vous utilisez la fonction de proposition de paiements, ce fournisseur est répertorié après tous les fournisseurs possédant un numéro prioritaire. Vous pouvez saisir autant de niveaux de priorité que nécessaire.

## <a name="see-also"></a>Voir aussi
[Définition des achats](purchasing-setup-purchasing.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

