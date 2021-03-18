---
title: Ranger la production
description: Le mode de rangement de la production dépend du mode de configuration de l’entrepôt en tant qu’emplacement.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e97f0e13f7b07ff59fd05908b6a3239d6cf70ebd
ms.sourcegitcommit: 026484766988b8727649c02fc8990b0646999bf1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/04/2021
ms.locfileid: "5498652"
---
# <a name="put-away-production-or-assembly-output"></a>Rangement du résultat de fabrication ou d’assemblage

Le mode de rangement de la production dépend du mode de configuration de l’entrepôt en tant qu’emplacement. Pour plus d’informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).  

Dans les configurations de stockage de base où l’emplacement appelle un traitement de rangement, vous utilisez le document **Rangement stock** pour valider la production et enregistrer le rangement de la production.  

> [!NOTE]  
> Le rangement de stock n’est pas pris en charge pour les processus d’assemblage. Vous publiez un ordre d’assemblage pour enregistrer le résultat. Si vous utilisez des emplacements, vous pouvez déplacer des éléments d’un emplacement à un autre ultérieurement. Pour plus d’informations, voir [Déplacer des articles ad hoc dans les configurations de stockage de base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

Dans les configurations de stockage avancées où l’emplacement nécessite un traitement à la fois de rangement et de réception, vous pouvez créer soit un document rangement interne soit un document mouvement pour ranger la production.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Pour ranger la production avec un rangement stock

La première étape dans la création d’un rangement de production consiste à créer la demande enlogement entrante. Cette demande indique à l’entrepôt que la production de l’O.F ou de l’assemblage est prête à être rangée.

### <a name="to-create-the-inbound-warehouse-request"></a>Pour créer la demande d’enlogement  
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **O.F. lancé**, puis sélectionnez le lien associé.  
2.  Sur l’ordre de fabrication qui est prêt pour rangement, choisissez l’action **Créer demande d’enlogement**.  

> [!NOTE]  
> Vous pouvez également créer la demande d’enlogement entrepôt en choisissant le champ **Créer demande d’enlogement** lors de l’actualisation de l’ordre de fabrication. Pour plus d’informations, voir [Actualiser ou replanifier des ordres de fabrication](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>Pour ranger la production avec un rangement stock  
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Rangement stock**, puis sélectionnez le lien associé.  
2.  Créez un rangement stock. Pour plus d’informations, voir [Ranger des articles avec le rangement stock](warehouse-how-to-put-items-away-with-inventory-put-aways.md)
3.  Pour accéder aux composants de la production de l’O.F., choisissez l’action **Extraire documents origine**, puis sélectionnez l’ordre de fabrication lancé.  
4.  Renseignez les lignes rangement en fonction des besoins.
5.  Lorsque les lignes sont prêtes à être validées, choisissez l’action **Valider**. Les écritures entrepôt nécessaires sont alors créées et la production des articles est validée.  

Vous pouvez également créer un **rangement stock** directement à partir de l’ordre de fabrication de lancé. Pour plus d’informations, voir [Ranger des articles avec le rangement stock](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  

Lorsque vous validez un rangement stock, on suppose que toutes les opérations sont validées en fonction de la gamme standard, à savoir que la quantité produite est validée en fonction de la dernière opération. Vous pouvez utiliser la feuille production pour valider les écarts de quantité produite et les temps d’exécution et de préparation. S’il est nécessaire d’effectuer une validation partielle après la création d’un rangement stock, vous pouvez le faire au niveau des temps de préparation et des quantités pour toutes les opérations, à l’exception de la dernière. Dans ce cas, la dernière opération est contrôlée par le rangement stock.  

Si vous devez juste validé le temps d’exécution ou de préparation de la dernière opération, définissez la quantité produite de la dernière opération sur 0. Vous pouvez également choisir de ne pas valider la dernière ligne en la supprimant  

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>Pour ranger l’assemblage et la production dans les configurations de stockage avancées
Lorsque vous validez l’ordre de fabrication ou d’assemblage dans l’entrepôt configuré pour utiliser le prélèvement et le rangement suggérés, la production est placée dans l’emplacement défini dans l’ordre de fabrication ou d’assemblage. 

Le tableau suivant décrit différentes manières de déplacer des articles dans l’entrepôt avec des configurations avancées où toutes les activités de l’entrepôt doivent être effectuées dans un flux de travail suggéré. 

|**Pour**|**Voir**|  
|------------|-------------|  
|Déplacer des articles avec la feuille mouvement entrepôt.|[Déplacer des articles dans les configurations de stockage avancées](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet)|  
|Créer un rangement interne pour placer les articles fabriqués ou assemblés dans une configuration de stockage avancée.|[Créer un rangement interne](warehouse-how-to-create-put-aways-from-internal-put-aways.md#to-create-an-internal-put-away)|

> [!NOTE]  
> Vous ne pouvez pas saisir le numéro document origine, tel que le N° O.F., rangement interne, rangement ou documents de mouvement pour l’une ou l’autre de ces procédures.  

## <a name="see-also"></a>Voir aussi  
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d’entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
