---
title: Gestion de l'inventaire| Microsoft Docs
description: Décrit comment gérer les biens physiques que vous commercialisez, par exemple, la gestion du stock de votre entrepôt.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 03/11/2019
ms.author: sgroespe
ms.openlocfilehash: dc32b5e210332fe0fd73b6423441cb66a5c171fb
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/19/2019
ms.locfileid: "852485"
---
# <a name="inventory"></a>STOCKS ET EN-COURS
Pour chaque produit physique que vous commercialisez, vous devez créer une fiche article de type **Stock**. Les articles que vous proposez aux clients, mais que vous n'avez pas en stock, peuvent être enregistrés comme articles de catalogue. Vous pouvez ensuite les convertir en articles stockés, le cas échéant. Vous pouvez augmenter ou diminuer la quantité d'un article en stock en validant directement les écritures comptables de l'article, par exemple, après un inventaire ou si vous n'enregistrez pas les achats.

Les entrées et les sorties de stock sont également évidemment enregistrées lorsque vous validez des documents achat et vente, respectivement. Pour plus d'informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md), [Vendre des produits](sales-how-sell-products.md) et  [Facturer des ventes](sales-how-invoice-sales.md). Les transferts entre magasins modifient les quantités en stock dans tous les entrepôts de votre société.   

Pour accroître votre aperçu d'articles et pour vous aider à les trouver, vous pouvez catégoriser les articles et leur donner des attributs pour vos opérations de recherche et de tri.

> [!NOTE]
> Le traitement physique des articles est appelé Activités entrepôt. Pour plus d'informations, voir [Gestion d'entrepôt](warehouse-manage-warehouse.md).

## <a name="inventory-reconciliation"></a>Rapprochement stock
Lorsque vous validez des mouvements de stock, tels que des expéditions vente, des factures achat ou des ajustements de stock, les coûts article modifiés sont enregistrés dans les écritures valeur. Pour refléter ces modifications de la valeur stock dans vos livres financiers, les coûts stocks sont automatiquement validés dans les comptes stock associés dans les écritures comptables. Pour chaque mouvement stock que vous validez, les valeurs appropriées sont validées dans le compte stocks, le compte ajustement et le compte validation stock dans la comptabilité. Pour plus d'informations, voir [Rapprocher les coûts ajustés avec la comptabilité](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Bien que les coûts soient automatiquement validés en comptabilité, il est malgré tout nécessaire de vous assurer que les coûts des biens sont transmis à la transaction de vente sortante associée, notamment dans les situations où vous vendez des biens avant de facturer l'achat. Il s'agit d'un ajustement des coûts. Le coût des articles est ajusté automatiquement lorsque vous validez des transactions article, mais vous pouvez également les ajuster manuellement. Pour en savoir plus, voir [Ajuster coûts article](inventory-how-adjust-item-costs.md).

|À |Voir |
|---|----|
|Créer des fiches article pour les articles en stock que vous commercialisez.|[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)|
|Structurer les articles parents que vous vendez sous forme de kits constitués des composants du parent ou que vous assemblez pour commande ou stock.|[Utiliser les nomenclatures](inventory-how-work-BOMs.md)|
|Conserver un aperçu des articles et simplifier la recherche et le tri des articles en les organisant par catégorie.|[Catégoriser des articles](inventory-how-categorize-items.md)|
|Affecter des attributs de différents types de valeurs à vos articles pour vous aider à les trier et à les rechercher.|[Utiliser les attributs d'article](inventory-how-work-item-attributes.md)|
|Créer des fiches article spéciales pour les articles que vous proposez aux clients, mais que vous n'avez pas en stock.|[Utiliser des articles de catalogue](inventory-how-work-nonstock-items.md)|
|Effectuer un inventaire physique, faire des ajustements négatifs ou positifs, et modifier des informations, telles que le magasin ou le numéro de lot, sur des écritures comptables article.|[Inventaire, ajustement et reclassement du stock](inventory-how-count-adjust-reclassify.md)|
|Afficher la disponibilité des articles par emplacement, par période, par événement de vente ou d'achat, ou encore en fonction de leur utilisation dans les nomenclatures d'assemblage ou de production.|[Voir la disponibilité des articles](inventory-how-availability-overview.md)|
|Transférer des articles en stock entre des magasins avec des ordres de transfert pour gérer les activités entrepôt ou avec la feuille reclassement.|[Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md)|
|Réserver des articles en stock ou entrants pour les commandes vente, les commandes achat, les commandes service, les ordres d'assemblage ou les ordres de fabrication.|[Réserver des articles](inventory-how-to-reserve-items.md)|
|Configurer la désignation propre à un fournisseur ou à un client pour un article, afin de pouvoir insérer facilement leur désignation de l'article dans les documents commerciaux.|[Utiliser les références externes article](inventory-how-use-item-cross-refs.md)|
|Affecter des numéros de série ou de lot à n'importe quel document ou ligne feuille entrant ou sortant, par exemple pour suivre les articles dans le cas d'un rappel.|[Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md)|
|Configurer la désignation d'un article propre à un fournisseur ou à un client sur votre fiche article, afin de pouvoir insérer rapidement leur désignation de l'article dans les documents commerciaux.|[Utiliser les références externes article](inventory-how-use-item-cross-refs.md)|
|Rechercher où un numéro de série ou de lot a été utilisé dans sa chaîne d'approvisionnement, par exemple dans les situations de rappel.|[Tracer des articles - Articles suivis](inventory-how-to-trace-item-tracked-items.md)|
|Bloquez des article pour la saisie dans des lignes de vente ou d'achat, ou pour la validation dans n'importe quelle transaction.|[Bloquer les articles](inventory-how-block-items.md)|
|Gérer les opérations commerciales dans les bureaux de vente, les départements d'achat ou les bureaux de planification d'usine pour plusieurs magasins.|[Utiliser les centres de gestion](inventory-responsibility-centers.md)|

## <a name="see-also"></a>Voir aussi  
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)    
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
