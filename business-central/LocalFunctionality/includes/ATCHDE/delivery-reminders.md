---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1e7cb126ea06d96bd130d644948d08fd7e2e1a11
ms.sourcegitcommit: 428f180604e5afcf94fa0e92a0615f58c88e13cd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/02/2020
ms.locfileid: "3959654"
---
Les relances livraison sont utilisées pour suivre les envois des fournisseurs en retard et pour rappeler aux fournisseurs les livraisons en retard. Pour créer des relances livraison, vous devez configurer ce qui suit :

- Conditions de relance livraison  

    Les conditions de relance livraison sont identifiées par un code qui doit être affecté aux fournisseurs. Pour utiliser plusieurs combinaisons de paramètres, vous devez configurer un code pour chaque paramètre séparément. Vous pouvez configurer autant de conditions relance livraison que vous le souhaitez.  

- Niveaux de relance livraison  

    Pour chaque condition de relance livraison, vous devez au préalable configurer des niveaux de relance livraison. Ces niveaux déterminent la fréquence à laquelle les relances livraison peuvent être créées pour une condition spécifique. Le niveau 1 correspond à la première relance créée pour une livraison échue. Le niveau 2 correspond à la deuxième relance livraison, etc. Lorsque les relances livraison sont créées, le nombre de relances créées précédemment est pris en compte, et le nombre actuel est utilisé pour appliquer des conditions.  

- Message textuels de relance livraison  

    Vous devez configurer des messages texte de relance livraison pour chaque niveau de relance livraison. Il existe deux types de messages texte de relance livraison : début et fin. Le message texte de début est imprimé dans la section En-tête, avant la liste des écritures marquées pour la relance. Le message texte fin est imprimé après cette liste.  

Après avoir configuré les conditions, les niveaux et les textes de livraison, vous devez affecter les codes relance livraison appropriés à vos fournisseurs.  

Vous pouvez créer les relances livraison manuellement ou automatiquement. Vous pouvez utiliser le traitement par lots **Créer une relance de livraison** pour créer des relances livraison automatiquement de sorte que vous pouvez sélectionner les commandes achat pour lesquelles des relances livraison doivent être créées.  

Vous pouvez également suivre les documents en rapport avec les lignes commande achat et les lignes commande vente.  

[!INCLUDE[d365fin](../../../includes/d365fin_md.md)] fournit les états suivants :  

- **Relance livraison publiée** - Pour afficher les relances livraison des fournisseurs.  
- **Relance livraison - Test** - Pour vérifier les relances livraison avant de les valider.  
