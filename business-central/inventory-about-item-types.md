---
title: Comprendre les types d’articles | Microsoft Docs
description: Vous pouvez ajuster l’évaluation du stock d’un article à l’aide des méthodes FIFO ou d’évaluation stock moyen, par exemple, lorsque les coûts article sont modifiés pour des motifs autres que les transactions.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbe603de91c78cf64b2e181136ea6214aa43c5c8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786138"
---
# <a name="about-item-types"></a>À propos des types d’articles
Dans le champ **Type** de la page **Fiche article**, vous pouvez sélectionner ce pourquoi l’article est utilisé dans votre activité et donc la manière dont il est géré dans le système. Trois options existent :

|Option|Objectif courant|
|------|-----------|
|Stock|Une unité réelle, telle qu’une bicyclette, pour la prise en charge totale de l’activité.|
|Hots stock|Une unité réelle, par exemple un boulon, pour une prise en charge limitée de l’activité, par exemple, car l’article est uniquement utilisé en interne et a un coût bas.|
|Service|Une unité de temps de travail, telle qu’une heure de conseil, pour la prise en charge limitée de l’activité.|

Le type **Stock** implique un suivi complet de la quantité et la valeur de stock. Par conséquent, tous les types de transaction article sont pris en charge, et les articles de type Stock peuvent être utilisés avec toutes les fonctionnalités de gestion des articles.

Les types **Service** et **Hors stock** ne requièrent pas le suivi de la quantité et la valeur de stock. Par conséquent, seuls les types de transaction articles et fonctionnalités sélectionnés sont pris en charge.

Les trois types d’article prennent en charge les fonctions suivantes respectivement.

|Type d’article|Ventes|Achats|Consommation de projet|Consommation de service|Consommation d’assemblage|Production Consommation|Résultat d’assemblage|Production|Magasin, Acheminement|Inventaire physique|Réévaluation du stock|Évaluation stock|Traçabilité|Réservation|Entreposage|Planning|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|STOCKS ET EN-COURS|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|
|Hots stock|Oui|Oui|Oui|Oui|Oui|Oui|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|
|Service|Oui|Oui|Oui|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|

## <a name="costing-methods-for-types-of-items"></a>Modes évaluation stock pour les types d’articles
Lorsque vous validez des transactions de stock, les changements de quantité et de valeur en stock sont enregistrés dans les écritures comptables article et les écritures valeur, respectivement. 

Pour les articles de stock, le coût est enregistré dans le champ **Coût total (réel)** sur la page **Écritures valeur**, et lorsqu’il est rapproché des écritures comptables, le coût sera indiqué dans le champ **Coût validé en comptabilité**. Pour plus d’informations, voir [Détails de conception : Évaluation stock](design-details-inventory-costing.md).

Pour les articles hors stock et de service, le coût est enregistré dans le champ **Coût total (non inventoriable)** sur la page **Écritures valeur**. Pour les articles hors stock et de service, le coût est spécifié sur les documents et journaux de vente, d’assemblage et de production. Le coût par défaut peut être spécifié dans le champ **Coût unitaire** sur les pages **Fiche article** et **Point de stock**. Les coûts de ces types d’articles ne sont pas rapprochés des écritures comptables. 

## <a name="catalog-and-service-items"></a>Articles de catalogue et de service
Les articles que vous offrez à vos clients mais que vous ne souhaitez pas gérer dans le système jusqu’à ce que vous commenciez à les vendre peuvent être définis comme des articles de catalogue. Les articles de catalogue ne doivent pas être confondus avec les articles normaux de type Hors-stock. Pour en savoir plus, voir [Utiliser des articles de catalogue](inventory-how-work-nonstock-items.md).

Les articles des clients pour lesquels vous effectuez un service, par exemple une imprimante, sont appelés des articles de service. Les articles de service n’ont rien à voir avec des articles courants ou de catalogue. Cependant, les composants de service peuvent être des articles courants. Pour plus d’informations, voir [Configurer les articles de service et les composants article de service](service-how-setup-service-items.md).

## <a name="see-also"></a>Voir aussi
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Configuration de stock](inventory-setup-inventory.md)  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]