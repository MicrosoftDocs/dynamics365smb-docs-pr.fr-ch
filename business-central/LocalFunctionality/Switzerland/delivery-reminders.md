---
title: relances livraison
description: Les relances livraison sont utilisées pour suivre les envois des fournisseurs en retard et pour rappeler aux fournisseurs les livraisons en retard.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d5b40092eada7db36be3f70b7be244750d5704b7
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3777846"
---
# <a name="delivery-reminders"></a>relances livraison
Les relances livraison sont utilisées pour suivre les envois des fournisseurs en retard et pour rappeler aux fournisseurs les livraisons en retard. Pour créer des relances livraison, vous devez configurer ce qui suit :  

- Conditions de relance livraison  

    Les conditions de relance livraison sont identifiées par un code qui doit être affecté aux fournisseurs. Pour utiliser plusieurs combinaisons de paramètres, vous devez configurer un code pour chaque paramètre séparément. Vous pouvez configurer autant de conditions relance livraison que vous le souhaitez.  

- Niveaux de relance livraison  

    Pour chaque condition de relance livraison, vous devez au préalable configurer des niveaux de relance livraison. Ces niveaux déterminent la fréquence à laquelle les relances livraison peuvent être créées pour une condition spécifique. Le niveau 1 correspond à la première relance créée pour une livraison échue. Le niveau 2 correspond à la deuxième relance livraison, etc. Lorsque les relances livraison sont créées, le nombre de relances créées précédemment est pris en compte, et le nombre actuel est utilisé pour appliquer des conditions.  

- Message textuels de relance livraison  

    Vous devez configurer des messages texte de relance livraison pour chaque niveau de relance livraison. Il existe deux types de messages texte de relance livraison : début et fin. Le message texte de début est imprimé dans la section En-tête, avant la liste des écritures marquées pour la relance. Le message texte fin est imprimé après cette liste.  

Pour plus d'informations, voir [Configurer les conditions, niveaux et textes de relance livraison](how-to-set-up-delivery-reminder-terms-levels-and-text.md).  

Après avoir configuré les conditions de livraison, vous devez affecter les codes condition de relance livraison aux fournisseurs. Pour plus d'informations, voir [Affecter les codes condition de relance livraison aux fournisseurs](how-to-assign-delivery-reminder-codes-to-vendors.md).  

Vous pouvez créer les relances livraison manuellement ou automatiquement. Vous pouvez utiliser le traitement par lots **Créer une relance livraison** pour créer des relances livraison automatiquement. Ce traitement par lots permet de sélectionner des commandes achat pour lesquelles des relances livraison doivent être créées. Pour plus d'informations, voir [Générer des relances livraison](how-to-issue-delivery-reminders.md).  

Vous pouvez également suivre les documents en rapport avec les lignes commande achat et les lignes commande vente.  

[!INCLUDE[d365fin](../../includes/d365fin_md.md)] fournit les états suivants :  

- **Relance livraison publiée** - Pour afficher les relances livraison des fournisseurs.  
- **Relance livraison - Test** - Pour vérifier les relances livraison avant de les valider.  

Pour plus d'informations, voir [Imprimer des rapports de test pour les relances livraison](how-to-print-test-reports-for-delivery-reminders.md).  

## <a name="see-also"></a>Voir aussi  
 [Configurer des relances livraison](how-to-set-up-delivery-reminders.md)   
 [Configurer les conditions, niveaux et textes de relance livraison.](how-to-set-up-delivery-reminder-terms-levels-and-text.md)   
 [Affecter des codes de relance livraison à des fournisseurs](how-to-assign-delivery-reminder-codes-to-vendors.md)   
 [Générer des relances livraison](how-to-generate-delivery-reminders.md)   
 [Créer manuellement des relances livraison](how-to-create-delivery-reminders-manually.md)   
 [Émettre des relances livraison](how-to-issue-delivery-reminders.md)   
 [Imprimer des rapports de test pour les relances livraison](how-to-print-test-reports-for-delivery-reminders.md)
