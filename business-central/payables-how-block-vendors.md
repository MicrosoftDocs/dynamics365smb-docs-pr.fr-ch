---
title: Comment bloquer les achats en provenance/vers des fournisseurs
description: Vous pouvez empêcher l’inclusion de fournisseurs dans des transactions, ou simplement bloquer de nouveaux paiements qui leur sont destinés.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: b1dcda8bed565ef37b712daa15554765a3c45846
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380496"
---
# <a name="block-vendors"></a>Bloquer des fournisseurs
Vous pouvez bloquer un fournisseur, par exemple à cause de son insolvabilité, afin que ce fournisseur ne puisse pas être ajouté à des documents achat ou afin d’empêcher que des paiements puissent être validés pour ce fournisseur.

Le tableau suivant décrit les options pour bloquer des fournisseurs.  

|Option|Description|  
|--------------------|------------|  
|**Vide**|Les transactions sont autorisées pour ce fournisseur.|
|**Paiement**|Il est impossible de créer de nouveaux paiements pour ce fournisseur.|  
|**Tous**|Aucune transaction n’est autorisée pour ce fournisseur.|  

## <a name="to-block-a-vendor"></a>Pour bloquer un fournisseur  
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Fournisseurs**, puis sélectionnez le lien associé.
2. Sélectionnez le fournisseur que vous souhaitez bloquer.
3. Dans le champ **Bloqué**, choisissez l’une des options de blocage.

## <a name="see-also"></a>Voir aussi  
[Enregistrer un nouveau fournisseur](purchasing-how-register-new-vendors.md)  
[Effectuer des paiements](payables-make-payments.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]