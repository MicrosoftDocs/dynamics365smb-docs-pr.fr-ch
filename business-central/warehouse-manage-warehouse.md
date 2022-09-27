---
title: Gérer les activités entrepôt
description: Entre la réception des biens et leur expédition, une série d’activités entrepôt internes a lieu pour assurer un flux efficace dans l’entrepôt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5774, 5776, 5777, 5785, 5793, 5797, 7318, 7364, 7401, 8909, 9000, 9008, 9009, 9050, 9053, 9056
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: c08331889a0a94e8760b8104b8d5769ea5d0edbf
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529800"
---
# <a name="warehouse-management"></a>Gestion d’entrepôt

Entre la réception des biens et leur expédition, une série d’activités entrepôt internes a lieu pour assurer un flux efficace dans l’entrepôt, ainsi que pour organiser et mettre à jour les stocks de la société.

Les activités entrepôt courantes, incluent le rangement d’articles, leur déplacement entre plusieurs entrepôts et leur prélèvement à des fins d’assemblage, de production et d’expédition. Assembler des articles pour des ventes ou le stock peut également être considéré comme des activités entrepôt, mais cela est traité ailleurs. Pour plus d’informations, voir [Gestion des assemblages](assembly-assemble-items.md).  

Dans les entrepôts importants, vous pouvez séparer ces tâches de traitement par département et gérer l’intégration par un flux suggéré. Dans les installations plus simples, le flux est moins formalisé et vous pouvez exécuter les activités entrepôt avec les rangements et prélèvements stock. Pour plus d’informations sur les configurations entrepôt de base et avancées, voir [Détails de conception : vue d’ensemble d’entrepôt](design-details-warehouse-overview.md).

Avant d’effectuer des activités entrepôt, vous devez configurer le système pour la complexité de traitement d’entrepôt appropriée. Pour plus d’informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

Les tâches d’inventaire, d’ajustement et de reclassement liées au stock et de reclassement des articles impliquent des tâches en entrepôt qui doivent être effectuées sur les écritures entrepôt avant qu’elles puissent être synchronisées avec les écritures comptables articles correspondantes. Pour plus d’informations, voir [Inventaire, ajustement et reclassement du stock](inventory-how-count-adjust-reclassify.md).

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.   

|**Pour**|**Voir**|  
|------------|-------------|  
|Enregistrer la réception (notamment la sur-réception) d’articles dans les entrepôts, soit avec une commande achat uniquement, dans les configurations de magasin simples, soit avec une réception entrepôt, en cas de traitement d’entrepôt partiellement ou entièrement automatisé dans le magasin.|[Réceptionner des articles](warehouse-how-receive-items.md)|
|Contourner les processus de rangement et de prélèvement pour expédier un article directement de la réception ou fabrication à l’expédition.|[Transborder des articles](warehouse-how-to-cross-dock-items.md)|
|Ranger les articles provenant des achats, retours vente, transferts ou de la production en fonction du processus d’entrepôt configuré.|[Rangement des articles](warehouse-put-away-items.md)|
|Déplacer des articles d’un emplacement à l’autre dans l’entrepôt.|[Déplacement d’articles](warehouse-move-items.md)|
|Prélever des articles à expédier, transférer ou consommer en assemblage ou production, en fonction du processus d’entrepôt configuré.|[Prélèvement des articles](warehouse-pick-items.md)|
|Enregistrer l’expédition d’articles à partir des entrepôts, soit avec une commande vente uniquement, dans les configurations d’emplacement simples, soit avec une expédition entrepôt, en cas de traitements d’entrepôt partiellement ou entièrement automatisés dans le magasin.|[Expédier des articles](warehouse-how-ship-items.md)|  

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/get-started-warehouse-management/) associée

## <a name="see-also"></a>Voir aussi

[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Détails de conception : Warehouse Management](design-details-warehouse-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
