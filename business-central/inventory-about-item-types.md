---
title: Comprendre les types d'articles | Microsoft Docs
description: Vous pouvez ajuster l'évaluation du stock d'un article à l'aide des méthodes FIFO ou d'évaluation stock moyen, par exemple, lorsque les coûts article sont modifiés pour des motifs autres que les transactions.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7e535abbc3fb61a958f63f648cca6694199acdc8
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242437"
---
# <a name="about-item-types"></a>À propos des types d'articles
Dans le champ **Type** de la page **Fiche article**, vous pouvez sélectionner ce pourquoi l'article est utilisé dans votre activité et donc la manière dont il est géré dans le système. Trois options existent :

|Option|Objectif courant|
|------|-----------|
|Stock|Une unité réelle, telle qu'une bicyclette, pour la prise en charge totale de l'activité.|
|Hots stock|Une unité réelle, par exemple un boulon, pour une prise en charge limitée de l'activité, par exemple, car l'article est uniquement utilisé en interne et a un coût bas.|
|Service|Une unité de temps de travail, telle qu'une heure de conseil, pour la prise en charge limitée de l'activité.|

Le type **Stock** implique un suivi complet de la quantité et la valeur de stock. Par conséquent, tous les types de transaction article sont pris en charge, et les articles de type Stock peuvent être utilisés avec toutes les fonctionnalités de gestion des articles.

Les types **Service** et **Hors stock** ne requièrent pas le suivi de la quantité et la valeur de stock. Par conséquent, seuls les types de transaction articles et fonctionnalités sélectionnés sont pris en charge.

Les trois types d'article prennent en charge les fonctions suivantes respectivement.

|Type d'article|Ventes|Achats|Consommation de projet|Consommation de service|Consommation d'assemblage|Production Consommation|Résultat d'assemblage|Production|Magasin, Acheminement|Inventaire physique|Réévaluation du stock|Évaluation stock|Traçabilité|Réservation|Entreposage|Planning|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|STOCKS ET EN-COURS|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|
|Hots stock|Oui|Oui|Oui|Oui|Oui|Oui|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|
|Service|Oui|Oui|Oui|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|

> [!NOTE]
> Les articles que vous offrez à vos clients mais que vous ne souhaitez pas gérer dans le système jusqu'à ce que vous commenciez à les vendre peuvent être définis comme des articles de catalogue. Les articles de catalogue ne doivent pas être confondus avec les articles normaux de type Hors-stock. Pour en savoir plus, voir [Utiliser des articles de catalogue](inventory-how-work-nonstock-items.md).

> [!NOTE]
> Les articles des clients pour lesquels vous effectuez un service, par exemple une imprimante, sont appelés des articles de service. Les articles de service n'ont rien à voir avec des articles courants ou de catalogue. Cependant, les composants de service peuvent être des articles courants. Pour plus d'informations, voir [Configurer les articles de service et les composants article de service](service-how-setup-service-items.md).

## <a name="see-also"></a>Voir aussi
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Configuration de stock](inventory-setup-inventory.md)  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
