---
title: "Procédure : configurer des magasins| Microsoft Docs"
description: "Décrit comment créer une fiche magasin pour chaque emplacement ou entrepôt dans lequel vous stockez les articles en stock, y compris les règles sur la procédure de transfert des articles depuis ou vers chaque magasin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 03/28/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 9a71dfc20cde7469772d438a0fbb520fbb0bbd9a
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-locations"></a>Comment configurer des magasins
Si vous achetez, enregistrez, ou vendez des articles à plusieurs magasins ou entrepôt, vous devez spécifier chaque magasin avec une fiche magasin et définir des acheminements transfert.

Vous pouvez ensuite créer des lignes de document pour un magasin spécifique, voir la disponibilité par magasin, et transférer le stock entre magasins. Pour plus d'informations, reportez-vous à [Gestion du stock](inventory-manage-inventory.md).

**Remarque** : Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**. Pour plus d'informations, voir [Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-create-a-location-card"></a>Pour créer une fiche magasin
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Magasins**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Dans la fenêtre **Fiche magasin**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Répétez les étapes 2 et 3 pour chaque magasin dans lequel vous souhaitez conserver le stock.

## <a name="to-create-a-transfer-route"></a>Pour créer un acheminement transfert
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Acheminements transfert**, puis sélectionnez le lien associé.
2. Sinon, à partir de n'importe quelle fenêtre **Fiche magasin**, cliquez sur **Acheminements transfert**.
3. Sélectionnez l'action **Nouveau**.
4. Dans la fenêtre **Fiche magasin**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Vous pouvez à présent transférer des articles en stock entre deux magasins. Pour plus d'informations, voir [Procédure : Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Voir aussi
[Gestion du stock](inventory-manage-inventory.md)  
[Chaîne d'approvisionnement](madeira-supply-chain.md)  
[Procédure : transfert de stock entre des magasins](inventory-how-transfer-between-locations.md)    
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Personnalisation de votre [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

