---
title: "Configurer une fiche magasin et définir des acheminements de transfert| Microsoft Docs"
description: "Vous créez une fiche magasin pour chaque emplacement où vous stockez des articles d'inventaire, par exemple, un entrepôt ou un centre de distribution, et configurez des acheminements pour le transfert d'articles entre magasins."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a44fccc118d5a52877309f1bf5e635e0f76068c9
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-locations"></a>Configurer des magasins
Si vous achetez, enregistrez, ou vendez des articles à plusieurs magasins ou entrepôt, vous devez spécifier chaque magasin avec une fiche magasin et définir des acheminements transfert.

Vous pouvez ensuite créer des lignes de document pour un magasin spécifique, voir la disponibilité par magasin, et transférer le stock entre magasins. Pour plus d'informations, reportez-vous à [Gestion du stock](inventory-manage-inventory.md).

## <a name="to-create-a-location-card"></a>Pour créer une fiche magasin
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Magasins**, puis sélectionnez le lien connexe.
2. Sélectionnez l'action **Nouveau**.
3. Dans la fenêtre **Fiche magasin**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Répétez les étapes 2 et 3 pour chaque magasin dans lequel vous souhaitez conserver le stock.

> [!NOTE]  
> De nombreux champs de la fiche magasin se rapportent à la gestion des articles dans les processus enlogement et désenlogement. Pour plus d'informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

## <a name="to-create-a-transfer-route"></a>Pour créer un acheminement transfert
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Magasins**, puis sélectionnez le lien connexe.
2. Sinon, à partir de n'importe quelle fenêtre **Fiche magasin**, cliquez sur **Acheminements transfert**.
3. Sélectionnez l'action **Nouveau**.
4. Dans la fenêtre **Fiche magasin**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Vous pouvez à présent transférer des articles en stock entre deux magasins. Pour plus d'informations, voir [Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Voir aussi
[Gestion du stock](inventory-manage-inventory.md)  
[Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md)    
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

