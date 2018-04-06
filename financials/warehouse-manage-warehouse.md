---
title: "Activités entrepôt | Microsoft Docs"
description: "Entre la réception des biens et leur expédition, une série d'activités entrepôt internes a lieu pour assurer un flux efficace dans l'entrepôt, ainsi que pour organiser et mettre à jour les stocks de la société."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: c8d4ee33395c18cb7755fd1877b2af813fb9da43
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="warehouse-management"></a>Gestion d'entrepôt
Entre la réception des biens et leur expédition, une série d'activités entrepôt internes a lieu pour assurer un flux efficace dans l'entrepôt, ainsi que pour organiser et mettre à jour les stocks de la société.

Les activités entrepôt courantes, incluent le rangement d'articles, leur déplacement entre plusieurs entrepôts et leur prélèvement à des fins d'assemblage, de production et d'expédition. Assembler des articles pour des ventes ou le stock peut également être considéré comme des activités entrepôt, mais cela est traité ailleurs. Pour plus d'informations, voir [Gestion des assemblages](assembly-assemble-items.md).  

Dans les entrepôts importants, vous pouvez séparer ces tâches de traitement par département et gérer l'intégration par un flux suggéré. Dans les installations plus simples, le flux est moins formalisé et vous pouvez exécuter les activités entrepôt avec les rangements et prélèvements stock. Pour plus d'informations sur les configurations entrepôt de base et avancées, voir [Détails de conception : vue d'ensemble d'entrepôt](design-details-warehouse-overview.md).

Avant d'effectuer des activités entrepôt, vous devez configurer le système pour la complexité de traitement d'entrepôt appropriée. Pour plus d'informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.   

|**Pour**|**Voir**|  
|------------|-------------|  
|Enregistrer la réception d'articles dans les entrepôts, soit avec une commande achat uniquement, dans les configurations d'emplacement simples, soit avec une réception entrepôt, en cas de traitement d'entrepôt partiellement ou entièrement automatisé dans le magasin.|[Réceptionner des articles](warehouse-how-receive-items.md)|
|Contourner les processus de rangement et de prélèvement pour expédier un article directement de la réception ou fabrication à l'expédition.|[Transborder des articles](warehouse-how-to-cross-dock-items.md)|    
|Ranger les articles provenant des achats, retours vente, transferts ou de la production en fonction du processus d'entrepôt configuré.|[Rangement des articles](warehouse-put-away-items.md)|
|Déplacer des articles d'un emplacement à l'autre dans l'entrepôt.|[Déplacement d'articles](warehouse-move-items.md)|
|Prélever des articles à expédier, transférer ou consommer en assemblage ou production, en fonction du processus d'entrepôt configuré.|[Prélèvement des articles](warehouse-pick-items.md)|
|Enregistrer l'expédition d'articles à partir des entrepôts, soit avec une commande vente uniquement, dans les configurations d'emplacement simples, soit avec une expédition entrepôt, en cas de traitements d'entrepôt partiellement ou entièrement automatisés dans le magasin.|[Expédier des articles](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Voir aussi  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

