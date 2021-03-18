---
title: Comment configurer des modèles rangement | Microsoft Docs
description: A l’aide de la fonctionnalité de prélèvement et de rangement suggérés, l’emplacement le mieux approprié à vos articles à un moment donné est suggéré, en fonction du modèle rangement configuré pour l’entrepôt, des priorités affectées aux emplacements et des quantités minimale et maximale définies pour les emplacements associés.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6b6064bbad133ca521e5cb44667b9ead1368c1e0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382370"
---
# <a name="set-up-put-away-templates"></a>Configurer des modèles rangement

A l’aide de la fonctionnalité de prélèvement et de rangement suggérés, l’emplacement le mieux approprié à vos articles à un moment donné est suggéré, en fonction du modèle rangement configuré pour l’entrepôt, des priorités affectées aux emplacements et des quantités minimale et maximale définies pour les emplacements associés.  

Vous pouvez configurer un certain nombre de modèles rangement et en sélectionner un pour gérer les rangements dans votre entrepôt. Vous pouvez également sélectionner un modèle rangement pour un article ou un point de stock disposant d’exigences spéciales en matière de rangement.  

## <a name="to-set-up-put-away-templates"></a>Pour configurer des modèles rangement

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Modèles rangement**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Entrez un code représentant l’identifiant unique du modèle que vous allez créer.  
4. Saisissez éventuellement une brève description.  
5. Renseignez la première ligne avec les exigences emplacement auxquelles vous souhaitez qu’il soit répondu d’abord lors de la proposition d’un rangement.

    Par exemple, si vous souhaitez que la méthode de rangement par défaut soit basée sur des emplacements fixes, choisissez le champ **Rechercher empl. statique**. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. Renseignez la deuxième ligne avec les exigences emplacement auxquelles on doit répondre ensuite lors de la recherche d’un emplacement de rangement. La deuxième ligne est utilisée uniquement si un emplacement répondant aux exigences de la première ligne ne peut être trouvé.  
7. Continuez à renseigner les lignes jusqu’à ce que vous ayez décrit tous les placements acceptables à utiliser au cours du rangement.  
8. Sur la dernière ligne du modèle rangement, cochez la case **Rechercher empl. Dynamique**.  

Vous pouvez créer plusieurs modèles rangement et les appliquer comme vous le souhaitez. On se réfère d’abord au modèle rangement sélectionné éventuel pour l’article ou le point de stock. Si ces champs ne sont pas renseignés, alors le modèle rangement sélectionné pour l’entrepôt sur le raccourci **Config. emplacement** de la fiche magasin sera utilisé.  

## <a name="see-also"></a>Voir aussi

[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Détails de conception : gestion d’entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]