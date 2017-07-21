---
title: Gestion de l'inventaire| Microsoft Docs
description: "Décrit comment gérer les biens physiques que vous commercialisez, par exemple, la gestion du stock de votre entrepôt."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 920df314dc8b671d4e2d99d8449ee02a74cb9078
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017

---

# <a name="inventory"></a>STOCKS ET EN-COURS
Pour chaque produit physique que vous commercialisez, vous devez créer une fiche article de type **Stock**. Les articles que vous proposez aux clients, mais que vous n'avez pas en stock, peuvent être enregistrés comme articles non stockés. Vous pouvez ensuite les convertir en articles stockés, le cas échéant. Vous pouvez augmenter ou diminuer la quantité d'un article en stock en validant directement les écritures comptables de l'article, par exemple, après un inventaire ou si vous n'enregistrez pas les achats.

Les entrées et les sorties de stock sont également évidemment enregistrées lorsque vous validez des documents achat et vente, respectivement. Pour plus d'informations, reportez-vous à [Procédure : enregistrer des achats](purchasing-how-record-purchases.md), [Procédure : vendre des produits](sales-how-sell-products.md) et à [Procédure : facturer des ventes](sales-how-invoice-sales.md). Les transferts entre magasins modifient les quantités en stock dans tous les entrepôts de votre société.   

Pour accroître votre aperçu d'articles et pour vous aider à les trouver, vous pouvez catégoriser les articles et leur donner des attributs pour vos opérations de recherche et de tri.

Vous devez vous assurer que les coûts des articles sont transmis à la transaction de vente sortante associée, notamment dans les situations où vous vendez des biens avant de facturer l'achat. Il s'agit de l'ajustement des coûts, que vous pouvez effectuer manuellement ou paramétrez pour qu'elle se produire automatiquement lorsque vous validez un mouvement stock.

## <a name="inventory-reconciliation"></a>Rapprochement stock
Lorsque vous validez des mouvements de stock, tels que des expéditions vente, des factures achat ou des ajustements de stock, les coûts article modifiés sont enregistrés dans les écritures valeur. Pour refléter ces modifications de la valeur stock dans vos livres financiers, les coûts stocks sont automatiquement validés dans les comptes stock associés dans les écritures comptables. Pour chaque mouvement stock que vous validez, les valeurs appropriées sont validées dans le compte stocks, le compte ajustement et le compte validation stock dans la comptabilité.

Bien que les coûts soient automatiquement validés en comptabilité, il est malgré tout nécessaire de vous assurer que les coûts des biens sont transmis à la transaction de vente sortante associée, notamment dans les situations où vous vendez des biens avant de facturer l'achat. Il s'agit d'un ajustement des coûts. Le coût des articles est ajusté automatiquement lorsque vous validez des transactions article, mais vous pouvez également les ajuster manuellement. Pour en savoir plus, voir Procédure : Ajuster coûts article.

|À |Voir |
|---|----|
|Créer des fiches article pour les articles en stock que vous commercialisez.|[Procédure : enregistrer de nouveaux articles](inventory-how-register-new-items.md)|
|Structurez les articles parents que vous vendez sous forme de kits constitués des composants du parent ou que vous assemblez pour commande ou stock.|[Procédure : utiliser les nomenclatures](inventory-how-work-BOMs.md)|
|Conservez un aperçu des articles et simplifiez la recherche et le tri des articles en les organisant par catégorie.|[Procédure : catégoriser des articles](inventory-how-categorize-items.md)|
|Affecter des attributs de différents types de valeurs à vos articles pour vous aider à les trier et à les rechercher.|[Procédure : utilisation des attributs d'article](inventory-how-work-item-attributes.md)|
|Créez des fiches article spéciales pour les articles que vous proposez aux clients, mais que vous n'avez pas en stock.|[Procédure : utiliser des articles non stockés](inventory-how-work-nonstock-items.md)|
|Effectuez un inventaire physique, faire des ajustements négatifs ou positifs, et modifiez des informations, telles que le magasin ou le numéro de lot, sur des écritures comptables article.|[Procédure : Inventaire, ajustement et reclassement du stock](inventory-how-count-adjust-reclassify.md)|
|Affichez la disponibilité des articles par emplacement, par période, par événement de vente ou d'achat, ou encore en fonction de leur utilisation dans les nomenclatures d'assemblage.|[Procédure : voir la disponibilité des articles](inventory-how-availability-overview.md)|
|Transférez des articles en stock entre des magasins avec des ordres de transfert pour gérer les activités entrepôt ou avec la feuille reclassement.|[Procédure : transfert de stock entre des magasins](inventory-how-transfer-between-locations.md)|
|Réévaluer ou amortir la valeur d'un ou de plusieurs articles dans le stock en validant leur valeur calculée courante.|[Procédure : réévaluer le stock](inventory-how-revalue-inventory.md)|
|Ajuster les coûts d'article, automatiquement ou manuellement, pour transférer les modifications de coût des écritures entrantes à leurs écritures sortantes associées.|[Procédure : ajustement des coûts article](inventory-how-adjust-item-costs.md)|

## <a name="see-also"></a>Voir aussi  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)    
[Chaîne d'approvisionnement](madeira-supply-chain.md)  
[Utilisation de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
