---
title: Déplacement d’articles
description: Lorsque les articles sont en stock, il peut être nécessaire de les déplacer entre plusieurs emplacements pour prendre en charge les activités entrepôt quotidiennes permettant de conserver le flux d’articles dans l’entrepôt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7315, 7349, 7351, 7382, 7384, 7386, 7387, 7399, 7400, 9314, 9330, 9345
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 7a44f0b716b219d7c65481c69abb3795129e8147
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511933"
---
# <a name="moving-items"></a>Déplacement d’articles

L’activité entrepôt consistant à déplacer les articles dans l’entrepôt s’exécute différemment selon la configuration des fonctionnalités du module Gestion d’entrepôt. Le niveau de complexité du paramétrage varie : aucune fonctionnalité entrepôt, configurations de stockage de base pour le traitement par commande dans une ou plusieurs activités uniquement, configurations avancées dans lesquelles toutes les activités entrepôt doivent être exécutées dans un flux suggéré. Pour plus d’informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

Dans un entrepôt, il peut être nécessaire de les déplacer entre plusieurs emplacements pour prendre en charge les activités entrepôt quotidiennes permettant de conserver le flux d’articles dans l’entrepôt. Certains mouvements se produisent en relation directe avec les opérations internes ; par exemple, lorsqu’un ordre de fabrication impose que des composants soient livrés ou que des produits finis soient rangés. D’autres mouvements se produisent dans le cadre d’une simple optimisation de l’espace des entrepôts ou en tant que mouvements ad-hoc depuis ou vers des opérations.

Des tâches de mouvement ont lieu régulièrement afin de réapprovisionner les emplacements prélèvement et atelier et modifier les informations relatives au contenu des emplacements.

Si le déplacement a lieu vers d’autres magasins, il a une incidence sur les écritures comptables article et doit donc être effectué dans le cadre d’un ordre de transfert. Pour plus d’informations, voir [Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md).  

Les tâches d’inventaire, d’ajustement et de reclassement liées au stock et de reclassement des articles impliquent des tâches en entrepôt qui doivent être effectuées sur les écritures entrepôt avant qu’elles puissent être synchronisées avec les écritures comptables articles correspondantes. Pour plus d’informations, voir [Inventaire, ajustement et reclassement du stock](inventory-how-count-adjust-reclassify.md)  

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.   

|**Pour**|**Voir**|  
|------------|-------------|  
|Déplacer des articles d’un emplacement à l’autre dans des configurations entrepôt de base à tout moment et sans documents origine.|[Déplacer des articles dans les configurations de stockage de base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Utiliser la feuille mouvement entrepôt pour déplacer des articles dans des configurations d’entrepôt avancées, pour les documents origine et ad hoc.|[Déplacer des articles dans les configurations de stockage avancées](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Ajouter des articles de composant à des opérations internes dans des configurations entrepôt de base en fonction des demandes issues des documents origine de ces opérations.|[Déplacer les composants vers une zone opérations dans les configurations de stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Planifier les emplacements à remplir ou vider pour maintenir un flux efficace (par exemple, vidage d’une zone de stockage en vrac avant une réception importante).|[Planifier des mouvements entrepôt dans la feuille](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Mettre à jour la fréquence de réapprovisionnement des emplacements (emplacements prélèvement, etc.) suite aux fluctuations de la demande.|[Calculer réappro. emplacement](warehouse-how-to-calculate-bin-replenishment.md)|
|Restructurez votre entrepôt avec de nouveaux codes et caractéristiques emplacement et déplacez-les potentiellement autour.|[Restructurer les entrepôts](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Voir aussi

[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de Warehouse Management](warehouse-setup-warehouse.md) 
[Gestion nomenclature d’assemblage](assembly-assemble-items.md)
[Détails de conception : Warehouse Management](design-details-warehouse-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]