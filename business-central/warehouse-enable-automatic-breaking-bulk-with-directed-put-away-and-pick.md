---
title: Rupture de charge avec prélèvement et rangement dirigé
description: 'Découvrez comment activer la rupture de charge automatique avec prélèvement et rangement dirigé, ainsi que le déconditionnement pour prélèvement, rangement, mouvement, etc.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '5703, 7352'
ms.date: 11/04/2022
ms.author: bholtorf
---
# Activer la rupture de charge automatique avec prélèvement et rangement dirigé

En cas d’utilisation d’un prélèvement et d’un rangement suggérés dans les entrepôts, [!INCLUDE[prod_short](includes/prod_short.md)] peut diviser des unités plus grandes en unités plus petites pendant la création des instructions entrepôt répondant aux exigences de documents origine, d’ordres de fabrication ou de prélèvements et de rangements internes. Le déconditionnement peut également signifier rassembler des articles dans des unités de mesure plus petites pour égaler la quantité d’une unité de mesure plus grande sur un document source ou un ordre de fabrication.

## Déconditionnement pour prélèvements  

Pour stocker des articles dans plusieurs unités à un emplacement et permettre de les combiner automatiquement au cours du prélèvement, activer le bouton de bascule **Autoriser déconditionnement** de la fiche Carte du magasin. Ensuite, pour répondre à une tâche, [!INCLUDE [prod_short](includes/prod_short.md)] recherchera automatiquement un article de la même unité. S’il n’en trouve pas, [!INCLUDE [prod_short](includes/prod_short.md)] suggérera que vous divisiez une plus grande unité de mesure dans l’unité de mesure qui est nécessaire.  

Si seules des unités plus petites sont disponibles, [!INCLUDE [prod_short](includes/prod_short.md)] vous suggère de rassembler des articles afin de répondre à la quantité de l’expédition ou de l’ordre de fabrication. En fait, il divise la plus grande unité du document origine en unités de prélèvement plus petites.  

## Déconditionnement pour rangement  

Dans les rangements des entrepôts, [!INCLUDE [prod_short](includes/prod_short.md)] suggère Placer les lignes d’action dans l’unité de mesure de rangement. Par exemple, il peut suggérer des pièces même si les articles arrivent dans une unité de mesure différente.  

## Déconditionnement pour mouvement  

[!INCLUDE [prod_short](includes/prod_short.md)] peut également se déconditionner dans les mouvements de réapprovisionnement si le bouton de basculement **Autoriser le déconditionnement** sur la page **Calculer le réapprovisionnement du bac** est activé.  

Vous pouvez afficher les résultats de la conversion entre deux unités sous forme de lignes déconditionnement intermédiaire dans les instructions rangement, prélèvement, ou mouvement.  

> [!NOTE]  
> Si vous sélectionnez le champ **Paramétrer filtre déconditionnement** dans l’en-tête instruction entrepôt, l’application masque les lignes déconditionnement chaque fois que la plus grande unité est utilisée dans son intégralité. Par exemple, si une palette comprend 12 pièces et que vous utiliserez les 12 pièces, le prélèvement vous indique de prendre 1 palette et d’y placer les 12 pièces. Cependant, si vous ne devez choisir que 9 pièces, les lignes de marchandises diverses ne sont pas masquées, même si vous avez sélectionné le champ **Filtre de déconditionnement**. Les lignes ne sont pas masquées, car vous devez placer les trois pièces restantes quelque part dans l’entrepôt.  

> [!NOTE]  
> Pour optimiser l’utilisation des unités dans l’entrepôt (également avec le déconditionnement), effectuez dès que vous le pouvez ce qui suit :  
>
> - Configurez l’unité de base d’un article en tant que plus petite unité à gérer dans les processus concernant l’entrepôt.  
> - Configurez les autres unités de l’article en tant que multiples de l’unité de base.  

## Voir aussi  

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de Warehouse Management](warehouse-setup-warehouse.md) 
[Gestion des assemblages](assembly-assemble-items.md)
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]