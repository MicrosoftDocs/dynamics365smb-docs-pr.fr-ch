---
title: Configurer des modèles rangement
description: Utilisez des modèles de rangement pour que les emplacements les plus appropriés pour vos articles vous soient suggérés à tout moment.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7312, 7313, 7314, 7321, 7322, 7323, 7329'
ms.date: 06/25/2021
ms.author: bholtorf
---
# Configurer des modèles rangement

A l’aide de la fonctionnalité de prélèvement et de rangement suggérés, l’emplacement le mieux approprié à vos articles à un moment donné est suggéré, en fonction du modèle rangement configuré pour l’entrepôt, des priorités affectées aux emplacements et des quantités minimale et maximale définies pour les emplacements associés.  

Vous pouvez configurer un certain nombre de modèles rangement et en sélectionner un pour gérer les rangements dans votre entrepôt. Vous pouvez également sélectionner un modèle rangement pour un article ou un point de stock disposant d’exigences spéciales en matière de rangement.  

## Pour configurer des modèles rangement

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modèles rangement**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Entrez un code représentant l’identifiant unique du modèle que vous allez créer.  
4. Saisissez éventuellement une brève description.  
5. Renseignez la première ligne avec les exigences emplacement auxquelles vous souhaitez qu’il soit répondu d’abord lors de la proposition d’un rangement.

    Par exemple, si vous souhaitez que la méthode de rangement par défaut soit basée sur des emplacements fixes, choisissez le champ **Rechercher empl. statique**. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. Renseignez la deuxième ligne avec les exigences emplacement auxquelles on doit répondre ensuite lors de la recherche d’un emplacement de rangement. La deuxième ligne est utilisée uniquement si un emplacement répondant aux exigences de la première ligne ne peut être trouvé.  
7. Continuez à renseigner les lignes jusqu’à ce que vous ayez décrit tous les placements acceptables à utiliser au cours du rangement.  
8. Sur la dernière ligne du modèle rangement, cochez la case **Rechercher empl. Dynamique**.  

Vous pouvez créer plusieurs modèles rangement et les appliquer comme vous le souhaitez. On se réfère d’abord au modèle rangement sélectionné éventuel pour l’article ou le point de stock. Si ces champs ne sont pas renseignés, alors le modèle rangement sélectionné pour l’entrepôt sur le raccourci **Config. emplacement** de la fiche magasin sera utilisé.  

## Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
