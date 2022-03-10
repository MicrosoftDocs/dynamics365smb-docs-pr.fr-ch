---
title: Créer des ordres de fabrication à partir de commandes achat
description: Découvrez les différentes façons de créer des ordres de fabrication pour les articles produits directement à partir des commandes vente.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000883, 99000884
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 3080556ad69882c533bec3768787784bfdac5c4f
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145539"
---
# <a name="create-production-orders-from-sales-orders"></a>Créer des ordres de fabrication à partir de commandes achat
Vous pouvez créer des ordres de fabrication pour les articles produits directement à partir des commandes vente.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Pour créer un ordre de fabrication à partir d’une commande achat  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2.  Sélectionnez la commande vente pour laquelle vous voulez créer un ordre de fabrication.  
3.  Sélectionnez l’action **Planification**. Sur la page **Planification commande vente**, vous pouvez afficher la disponibilité de l’article de commande vente.  
4.  Sélectionnez l’action **Créer O.F**.  
5.  Sélectionnez le statut et le type de commande.  
6.  Choisissez le bouton **Oui** pour créer un ou plusieurs ordres de fabrication pour les lignes ayant **Ordre de fabrication** dans le champ **Système réapprovisionnement**.


> [!NOTE]  
> Les lignes de demandes de l’ordre de fabrication créé qui ont **Ordre de fabrication** dans le champ **Système réapprovisionnelent** représentent des ordres de fabrication sous-jacents. Après avoir généré ces ordres de fabrication, n’oubliez pas d’identifier toute demande de composant non réalisée pour ceux-ci à l’aide de la page **Planification commande** ou de la fonction **Replanifier** à partir d’ordres créés. 

## <a name="order-type"></a>Type de commande  
Vous pouvez choisir entre deux façons de créer les ordres de fabrication, comme indiqué dans le tableau suivant.

|Option|Description|
|------|-----------|
|O.F. article|Un ordre de fabrication est créé pour chaque ordre de fabrication nécessaire qui est représenté par une ligne dans la fenêtre **Planification commande vente**.|
|O.F. projet|Un ordre de fabrication est créé pour tous les ordres de fabrication nécessaires qui sont représentés par des lignes dans la fenêtre **Planification commande vente**. |

Lorsque vous utilisez des O.F. projet, le champ **Type origine** de l’ordre de fabrication indique **En-tête vente** et l’ordre comporte plusieurs lignes, une pour chaque article de la ligne vente à produire.  


## <a name="see-also"></a>Voir aussi  
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)   
[Pratiques de configuration recommandées : planification de l’approvisionnement](setup-best-practices-supply-planning.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
