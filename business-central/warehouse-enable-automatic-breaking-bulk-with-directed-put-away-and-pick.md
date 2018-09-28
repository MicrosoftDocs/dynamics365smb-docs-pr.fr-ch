---
title: "Rupture de charge automatique avec prélèvement et rangement dirigé | Microsoft Docs"
description: "En cas d'utilisation d'un prélèvement et d'un rangement suggérés dans les entrepôts, vous pouvez diviser une unité en unités plus petites lors de la création des instructions entrepôt répondant aux exigences de documents origine, d'ordres de fabrication ou de prélèvements et de rangements internes."
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
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 20293bc9e17fd3fe03466a55d0b74b5104cd17f2
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Activer la rupture de charge automatique avec prélèvement et rangement dirigé
En cas d'utilisation d'un prélèvement et d'un rangement suggérés dans les entrepôts, [!INCLUDE[d365fin](includes/d365fin_md.md)] peut procéder, dans de nombreux cas, à un déconditionnement automatique (division d'une unité en unités plus petites) lorsqu'il crée des instructions entrepôt répondant aux exigences de documents origine, d'ordres de fabrication ou de prélèvements et de rangements internes. Parfois, le déconditionnement peut également nécessiter le regroupement de petites unités afin de répondre à des demandes sortantes en divisant l'unité la plus grande du document origine ou de l'ordre de fabrication en unités plus petites disponibles dans l'entrepôt.   

## <a name="breakbulking-in-picks"></a>Déconditionnement pour prélèvement  
Pour stocker des articles dans plusieurs unités et permettre de les combiner automatiquement selon vos besoins au cours du prélèvement, sélectionnez le champ **Autoriser déconditionnement** de la fiche magasin.  

Pour répondre à une tâche, le programme recherche automatiquement un article de la même unité. S'il ne trouve pas ce type d'article et que vous avez sélectionné ce champ, il vous propose de diviser une unité plus grande en fonction de l'unité nécessaire.  

Si le système trouve uniquement des unités plus petites, il vous suggère de rassembler des articles afin de répondre à la quantité de l'expédition ou de l'ordre de fabrication. En fait, il divise la plus grande unité du document origine en unités de prélèvement plus petites.  

## <a name="breakbulking-in-put-aways"></a>Déconditionnement pour rangement  
Au niveau du rangement de l'entrepôt, le programme propose automatiquement des lignes action Emplacement dans l'unité de rangement, par exemple, pièces, même si les articles arrivent dans une unité différente.  

## <a name="breakbulking-in-movements"></a>Déconditionnement pour mouvement  
le programme effectue également un déconditionnement automatique au niveau des mouvements de réapprovisionnement, si le champ **Autoriser déconditionnement** est sélectionné sur le raccourci **Option** de la fenêtre **Calculer réappro. emplacement**.  

Vous pouvez afficher les résultats de la conversion entre deux unités sous forme de lignes déconditionnement intermédiaire dans les instructions rangement, prélèvement, ou mouvement.  

> [!NOTE]  
>  Si vous sélectionnez le champ **Paramétrer filtre déconditionnement** dans l'en-tête instruction entrepôt, le programme masque les lignes déconditionnement chaque fois que la plus grande unité est utilisée dans son intégralité. Par exemple, si une palette comprend 12 pièces et que vous allez utiliser les 12 pièces, le prélèvement vous indique de prendre 1 palette et d'y placer les 12 pièces. Par contre, si vous ne devez prélever que 9 pièces, les lignes déconditionnement ne sont pas masquées, même si vous avez sélectionné le champ **Filtre déconditionnement**, étant donné que vous devez placer les trois pièces restantes dans un autre endroit de l'entrepôt.  

> [!NOTE]  
>  Pour optimiser l'utilisation des unités dans l'entrepôt (également avec la fonctionnalité de déconditionnement), effectuez dès que vous le pouvez les opérations suivantes :  
>   
> - Configurez l'unité de base d'un article en tant que plus petite unité à gérer dans les processus concernant l'entrepôt.  
> - Configurez les autres unités de l'article en tant que multiples de l'unité de base.  

## <a name="see-also"></a>Voir aussi  
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

