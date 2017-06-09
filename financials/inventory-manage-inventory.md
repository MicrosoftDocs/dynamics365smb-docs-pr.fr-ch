---
title: Stock| Microsoft Docs
description: "Décrit comment gérer les articles physiques."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b53cae82cfa532fb0620cc9e1f305216c2321785
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017

---

# <a name="inventory"></a>STOCKS ET EN-COURS
Pour chaque produit physique que vous commercialisez, vous devez créer une fiche article de type **Stock**. Les articles que vous proposez aux clients, mais que vous n'avez pas en stock, peuvent être enregistrés comme articles non stockés. Vous pouvez ensuite les convertir en articles stockés, le cas échéant. Vous pouvez augmenter ou diminuer la quantité d'un article en stock en validant directement les écritures comptables de l'article, par exemple, après un inventaire ou si vous n'enregistrez pas les achats.

Les entrées et les sorties de stock sont également évidemment enregistrées lorsque vous validez des documents achat et vente, respectivement. Pour plus d'informations, reportez-vous à [Procédure : enregistrer des achats](purchasing-how-record-purchases.md), [Procédure : vendre des produits](sales-how-sell-products.md) et à [Procédure : facturer des ventes](sales-how-invoice-sales.md). Les transferts entre magasins modifient les quantités en stock dans tous les entrepôts de votre société.   

Pour accroître votre aperçu d'articles et pour vous aider à les trouver, vous pouvez catégoriser les articles et leur donner des attributs pour vos opérations de recherche et de tri.

Vous devez vous assurer que les coûts des articles sont transmis à la transaction de vente sortante associée, notamment dans les situations où vous vendez des biens avant de facturer l'achat. Il s'agit de l'ajustement des coûts, que vous pouvez effectuer manuellement ou paramétrez pour qu'elle se produire automatiquement lorsque vous validez un mouvement stock.

Les modifications de la valeur stock découlant de la vente sont automatiquement rapprochées avec vos livres financiers lorsque vous validez des transactions article.

|Pour |Voir |
|---|----|
|Créer des fiches article pour les articles en stock que vous commercialisez.|[Procédure : enregistrer de nouveaux articles](inventory-how-register-new-items.md)|
|Structurez les articles parents que vous vendez sous forme de kits constitués des composants du parent ou que vous assemblez pour commande ou stock.|[Procédure : utiliser les nomenclatures](inventory-how-work-BOMs.md)|
|Conservez un aperçu des articles et simplifiez la recherche et le tri des articles en les organisant par catégorie.|[Procédure : catégoriser des articles](inventory-how-categorize-items.md)|
|Affecter des attributs de différents types de valeurs à vos articles pour vous aider à les trier et à les rechercher.|[Procédure : utilisation des attributs d'article](inventory-how-work-item-attributes.md)|
|Créez des fiches article spéciales pour les articles que vous proposez aux clients, mais que vous n'avez pas en stock.|[Procédure : utiliser des articles non stockés](inventory-how-work-nonstock-items.md)|
|Augmenter ou réduire la quantité en stock d'un article, par exemple après un inventaire ou comme moyen simple d'enregistrer les réceptions achat.|[Procédure : ajuster le stock](inventory-how-adjust-inventory.md)|
|Affichez la disponibilité des articles par emplacement, par période, par événement de vente ou d'achat, ou encore en fonction de leur utilisation dans les nomenclatures d'assemblage.|[Procédure : obtenir un aperçu des disponibilités](inventory-how-availability-overview.md)|
|Transférez des articles en stock entre des magasins avec des ordres de transfert pour gérer les activités entrepôt ou avec la feuille reclassement.|[Procédure : transfert de stock entre des magasins](inventory-how-transfer-between-locations.md)|
|Réévaluer ou amortir la valeur d'un ou de plusieurs articles dans le stock en validant leur valeur calculée courante.|[Procédure : réévaluer le stock](inventory-how-revalue-inventory.md)|
|Ajuster les coûts d'article, automatiquement ou manuellement, pour transférer les modifications de coût des écritures entrantes à leurs écritures sortantes associées.|[Procédure : ajustement des coûts article](inventory-how-adjust-item-costs.md)|
|Découvrez comment les modifications de la valeur stock découlant de la vente sont automatiquement rapprochées avec vos livres financiers.|[Avancé : Rapprochement compta](advanced-inventory-reconciliation.md).|

## <a name="see-also"></a>Voir aussi  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)    
[Chaîne d'approvisionnement](madeira-supply-chain.md)  
[Utilisation de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
