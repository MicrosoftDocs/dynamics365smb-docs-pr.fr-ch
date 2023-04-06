---
title: Comprendre les types d’articles
description: 'Vous pouvez ajuster l’évaluation du stock d’un article à l’aide des méthodes FIFO ou d’évaluation stock moyen, lorsque les coûts article sont modifiés pour des motifs autres que les transactions.'
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 06/16/2021
ms.author: edupont
---
# À propos des types d’articles
Dans le champ **Type** de la page **Fiche article**, vous pouvez sélectionner ce pourquoi l’article est utilisé dans votre activité, ce qui a une incidence sur le niveau de gestion que vous pouvez exercer sur l’article en stock. Le tableau suivant répertorie et décrit les trois types d’éléments disponibles.

|Option|Objectif courant|
|------|-----------|
|Stock|Les objets physiques, tels que les vélos, les téléphones et les bureaux, pour lesquels vous souhaitez pouvoir utiliser tous les processus de stock. Cela peut également inclure des éléments non physiques, tels que des licences logicielles et des abonnements, si les éléments ont des numéros d’identification, tels que des numéros de série. Vous pouvez suivre entièrement les valeurs et la disponibilité des articles dans l’inventaire.|
|Hots stock|En règle générale, les articles hors stock sont des objets physiques, tels que des boulons ou des stylos, qu’une entreprise consomme mais ne souhaite pas suivre entièrement dans le stock. Par exemple, parce que ce sont des articles qui ne coûtent pas cher et qu’ils ne sont utilisés qu’en interne.|
|Service|Une unité de temps de travail, telle qu’une heure de conseil, pour la prise en charge limitée de l’activité.|

> [!NOTE]
> Les types **Service** et **Hors stock** ne prennent pas en charge le suivi des quantités et les valeurs de stock. Seuls les types de transaction articles et fonctionnalités sélectionnés sont pris en charge.

Le tableau suivant répertorie les fonctions que les trois types d’article prennent en charge.

|Type d’article|Ventes|Achats|Consommation de projet|Consommation de service|Consommation d’assemblage|Production Consommation|Résultat d’assemblage|Production|Magasin, Acheminement|Inventaire physique|Réévaluation du stock|Évaluation stock|Traçabilité|Réservation|Entreposage|Planification|Planning commande|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Stock|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|Oui|
|Hors stock|Oui|Oui|Oui|Oui|Oui|Oui|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|Oui|
|Service|Oui|Oui|Oui|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|Non|Oui|

## Modes évaluation stock pour les types d’articles
Lorsque vous validez des transactions de stock, les changements de quantité et de valeur en stock sont enregistrés dans les écritures comptables article et les écritures valeur, respectivement. 

Pour les articles de stock, le coût est enregistré dans le champ **Coût total (réel)** sur la page **Écritures valeur**, et lorsqu’il est rapproché des écritures comptables, le coût sera indiqué dans le champ **Coût validé en comptabilité**. Pour plus d’informations, voir [Détails de conception : Évaluation stock](design-details-inventory-costing.md).

Pour les articles hors stock et de service, le coût est enregistré dans le champ **Coût total (non inventoriable)** sur la page **Écritures valeur**. Pour les articles hors stock et de service, le coût est spécifié sur les documents et journaux de vente, d’assemblage et de production. Le coût par défaut peut être spécifié dans le champ **Coût unitaire** sur les pages **Fiche article** et **Point de stock**. Les coûts de ces types d’articles ne sont pas rapprochés des écritures comptables. 

## Articles de catalogue et de service
Les articles que vous offrez à vos clients mais que vous ne souhaitez pas gérer dans le système jusqu’à ce que vous commenciez à les vendre peuvent être définis comme des articles de catalogue. Les articles de catalogue ne doivent pas être confondus avec les articles normaux de type Hors-stock. Pour en savoir plus, voir [Utiliser des articles de catalogue](inventory-how-work-nonstock-items.md).

Les articles des clients pour lesquels vous effectuez un service, par exemple une imprimante, sont appelés des articles de service. Les articles de service n’ont rien à voir avec des articles courants ou de catalogue. Cependant, les composants de service peuvent être des articles courants. Pour plus d’informations, voir [Configurer les articles de service et les composants article de service](service-how-setup-service-items.md).

## Voir aussi
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Configuration de stock](inventory-setup-inventory.md)  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Stock](inventory-manage-inventory.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
