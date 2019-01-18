---
title: "Comment activer le prélèvement par FEFO | Microsoft Docs"
description: "First-Expired-First-Out (FEFO) est une méthode de tri qui garantit que les articles les plus anciens, ceux qui ont les dates d'expiration les plus anciennes, sont prélevés en premier."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 54857d668cdceb9cc1d4e035a496d621b1d9459b
ms.contentlocale: fr-ch
ms.lasthandoff: 11/26/2018

---
# <a name="enable-picking-items-by-fefo"></a>Activer le prélèvement d'articles par FEFO
First-Expired-First-Out (FEFO) est une méthode de tri qui garantit que les articles les plus anciens, ceux qui ont les dates d'expiration les plus anciennes, sont prélevés en premier.  

 Cette fonctionnalité ne fonctionne que lorsque les critères suivants sont réunis :  

-   L'article doit avoir un numéro de série/lot.  
-   Dans la configuration du code de traçabilité article de l'article, le champ **Traçabilité d'entrepôt par numéro de série** ou le champ **Traçabilité d'entrepôt par numéro de lot** doit être sélectionné.  
-   L'article doit être validé dans le stock avec une date d'expiration.  
-   Dans la fiche magasin, la case à cocher **Prélèvement requis** doit être activée.  
-   Dans la fiche magasin, la case à cocher **Prélèvement selon FEFO** doit être activée.  
-   Dans la fiche magasin, le champ **Emplacement obligatoire** doit être sélectionné.  

 Lorsque tous les critères sont réunis, les articles aux numéros de série/lot à prélever sont triés par ancienneté de prélèvements et mouvements, sauf pour les articles qui utilisent la traçabilité par numéro de série ou de lot.  

> [!NOTE]  
> Si certains articles avec numéros de série/lot utilisent une traçabilité spécifique, ceux-ci sont respectés en premier et, en dessous, les numéros de série/lot non spécifiques restants sont listés selon FEFO.
<br /><br />
Si deux articles avec des numéros de série ou de lot ont la même date de péremption, le programme sélectionne celui avec le plus petit numéro de lot ou de série.
<br /><br />
Lors du prélèvement des articles avec numéro de série/de lot dans les magasins configurés pour un prélèvement et un rangement suggérés, seules les quantités des emplacements de type *Prélèvement* sont prélevés selon FEFO.  
<br /><br />
Pour activer des mouvements selon FEFO, sur la page **Mouvement de stock** ou la page **Feuille mouvement**, vous devez laisser le champ **Depuis emplacement** vide.  
<br /><br />
Si le champ **Validation de péremption stricte** est sélectionné, seuls les articles non expirés sont inclus dans le prélèvement. Cela s'applique même si vous n'utilisez pas de prélèvement selon FEFO.

## <a name="see-also"></a>Voir aussi  
[Prélèvement des articles](warehouse-pick-items.md)   
[Prélever des articles pour l'expédition entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

