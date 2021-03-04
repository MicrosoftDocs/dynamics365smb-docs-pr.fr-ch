---
title: Définir les Paramètres stock généraux
description: Décrit comment définir la Paramètres stock généraux afin que vous puissiez gérer votre entrepôt et votre stock.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e3ecf8d206e50244c19a820bdb67d2992cbefe36
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746381"
---
# <a name="set-up-general-inventory-information"></a>Définir des informations générales relatives aux stocks

Vous pouvez spécifier des paramètres de stock généraux sur la page **Paramètres stock**.

## <a name="to-set-up-general-inventory-information"></a>Pour définir des informations générales relatives aux stocks

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres stock**, puis sélectionnez le lien associé.
2. Sur la page **Paramètres stock**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Pour des informations détaillées sur les champs de coût, **Compta. coûts automatique**, **Compta. coûts prévus** et **Mode évaluation stock par défaut**, consultez [Rapprocher les coûts ajustés avec la comptabilité](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Détails de conception : coûts ajustés](design-details-inventory-costing.md) et [Détails de conception : validation du coût prévu](design-details-expected-cost-posting.md). Pour plus d’informations sur les coûts en général, voir [Gestion des coûts](finance-manage-inventory-costs.md).  

Vous pouvez inclure un délai entrepôt par défaut pour votre stock sur la page **Paramètres stock** ou pour votre magasin dans le calcul de la promesse de livraison sur la ligne achat. Pour plus d’informations, voir [Calculer des dates promesse livraison](sales-how-to-calculate-order-promising-dates.md).  

> [!NOTE]
> Le bouton de basculement **Ajustement automatique des coûts** est activé par défaut pour garantir que les valeurs du stock soient toujours correctes dans la Comptabilité, qui à son tour maintient vos statistiques vente et profit à jour. Les modifications de coût des écritures entrantes, telles que celles des sorties achat ou production, sont affectées aux écritures sortantes correspondantes, telles que les ventes ou les transferts. Ceci est utile pour les nouveaux clients et petites entreprises [!INCLUDE[prod_short](includes/prod_short.md)] avec des niveaux de mouvements de stock relativement bas. Cependant, à mesure que l’entreprise se développe et que les niveaux de stock augmentent, cela peut ralentir les performances du système. Pour minimiser les performances réduites lors de la validation, sélectionnez une option de temps pour définir jusqu’où dans le passé depuis la date de travail une transaction entrante peut se produire pour déclencher potentiellement l’ajustement des entrées de valeur sortantes associées. Sinon, vous pouvez ajuster manuellement les coûts à intervalles réguliers avec le Traitement par lots Ajuster coûts - Écr. article.

## <a name="see-also"></a>Voir aussi
[Configuration du stock](inventory-setup-inventory.md)  
[Détails de conception : modes évaluation stock](design-details-costing-methods.md)    
[Gestion du stock](inventory-manage-inventory.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Fonctionnalités marché](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]