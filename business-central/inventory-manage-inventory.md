---
title: Gestion du stock
description: Cet article décrit comment gérer les produits physiques que vous échangez en créant une fiche d’article d’inventaire.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'warehouse, stock'
ms.search.forms: '5804, 2106, 5823, 5751, 5750, 772, 5829, 5828, 513, 304, 40, 38, 167, 117, 5827, 9223, 158, 354, 9152, 286, 5754, 5402, 209, 297, 298, 99000782'
ms.date: 12/19/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Gestion du stock

Pour chaque produit physique que vous commercialisez, vous devez créer une fiche article de type **Stock**. Les articles que vous proposez aux clients, mais que vous n’avez pas en stock, peuvent être enregistrés comme articles de catalogue. Vous pouvez ensuite les convertir en articles stockés, le cas échéant. Vous pouvez augmenter ou diminuer la quantité d’un article en stock en validant directement les écritures comptables de l’article, par exemple, après un inventaire ou si vous n’enregistrez pas les achats.

Les entrées et les sorties de stock sont également évidemment enregistrées lorsque vous validez des documents achat et vente, respectivement. Pour plus d’informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md), [Vendre des produits](sales-how-sell-products.md) et [Facturer des ventes](sales-how-invoice-sales.md). Les transferts entre magasins modifient les quantités en stock dans tous les entrepôts de votre société.

Pour améliorer votre aperçu d’articles et pour vous aider à les trouver, vous pouvez catégoriser les articles et leur donner des attributs pour vos opérations de recherche et de tri.

> [!NOTE]
> Le traitement physique des articles est appelé Activités entrepôt. En savoir plus, consultez la [Vue d’ensemble de Warehouse Management](design-details-warehouse-management.md).

Le planning d’articles pour répondre à la demande est couvert dans le cadre de la fonctionnalité de planning de l’offre. En savoir plus sur [Planification](production-planning.md).  

## Rapprochement stock

Lorsque vous validez des mouvements de stock, tels que des expéditions vente, des factures achat ou des ajustements de stock, les coûts article modifiés sont enregistrés dans les écritures valeur. Pour refléter ces modifications de la valeur stock dans vos livres financiers, les coûts stocks sont automatiquement validés dans les comptes stock associés dans les écritures comptables. Pour chaque mouvement stock que vous validez, les valeurs appropriées sont validées dans le compte stocks, le compte ajustement et le compte validation stock dans la comptabilité. En savoir plus sur [Rapprocher l’évaluation stock avec la comptabilité](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Bien que les coûts soient automatiquement validés en comptabilité, il est malgré tout nécessaire de vous assurer que les coûts des biens sont transmis à la transaction de vente sortante associée, notamment dans les situations où vous vendez des biens avant de facturer l’achat. Il s’agit d’un ajustement des coûts. Le coût des articles est ajusté automatiquement lorsque vous validez des transactions article, mais vous pouvez également les ajuster manuellement. En savoir plus sur [Ajuster les coûts des articles](inventory-how-adjust-item-costs.md).  

## Tâches connexes

Le tableau suivant présente les tâches associées.

|À |Voir |
|---|----|
|Créer des fiches article pour les articles en stock que vous commercialisez.|[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)|
|Structurer les articles parents que vous vendez sous forme de kits constitués des composants du parent ou que vous assemblez pour commande ou stock.|[Utiliser les nomenclatures](inventory-how-work-BOMs.md)|
|Conserver un aperçu des articles et simplifier la recherche et le tri des articles en les organisant par catégorie.|[Catégoriser des articles](inventory-how-categorize-items.md)|
|Affecter des attributs de différents types de valeurs à vos articles pour vous aider à les trier et à les rechercher.|[Utiliser les attributs d’article](inventory-how-work-item-attributes.md)|
|Créer des fiches article spéciales pour les articles que vous proposez aux clients, mais que vous n’avez pas en stock.|[Utiliser des articles de catalogue](inventory-how-work-nonstock-items.md)|
|Exécutez l’inventaire physique de votre stock avec les pages **Commande de stock physique** et **Enregistrement de stock physique**.|[Faire l’inventaire à l’aide de documents](inventory-how-count-inventory-with-documents.md)|
|Effectuer un inventaire physique, faire des ajustements négatifs ou positifs, et modifier des informations, telles que le magasin ou le numéro de lot, sur des écritures comptables article.|[Comptabiliser, ajuster et reclasser le stock avec les feuilles](inventory-how-count-adjust-reclassify.md)|
|Afficher la disponibilité des articles par emplacement, par période, par événement de vente ou d’achat, ou encore en fonction de leur utilisation dans les nomenclatures d’assemblage ou de production.|[Voir la disponibilité des articles](inventory-how-availability-overview.md)|
|Transférer des articles en stock entre des magasins avec des ordres de transfert pour gérer les activités entrepôt ou avec la feuille reclassement.|[Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md)|
|Réserver des articles en stock ou entrants pour les commandes vente, les commandes achat, les commandes service, les ordres de transfert, les ordres d’assemblage ou les ordres de fabrication.|[Réserver des articles](inventory-how-to-reserve-items.md)|
|Configurez la traçabilité afin de pouvoir suivre les numéros de série des articles, par exemple pour suivre les articles en cas de rappel.|[Configuration du suivi des articles avec les numéros lot, de série et paquet](inventory-how-setup-item-tracking.md)|
|Attribuez des numéros de série ou des numéros lot à tout document ou ligne feuille sortant ou entrant.|[Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md)|
|Rechercher où un numéro de série ou de lot a été utilisé dans sa chaîne d’approvisionnement, par exemple dans les situations de rappel.|[Tracer des articles - Articles suivis](inventory-how-to-trace-item-tracked-items.md)|
|Configurer la désignation d’un article propre à un fournisseur ou à un client sur votre fiche article, afin de pouvoir insérer rapidement leur désignation de l’article dans les documents commerciaux.|[Utiliser références article](inventory-how-use-item-cross-refs.md)|
|Bloquez des article pour la saisie dans des lignes de vente ou d’achat, ou pour la validation dans n’importe quelle transaction.|[Bloquer les articles](inventory-how-block-items.md)|
|Gérer les opérations commerciales dans les bureaux de vente, les départements d’achat ou les bureaux de planification d’usine pour plusieurs magasins.|[Utiliser les centres de gestion](inventory-responsibility-centers.md)|
|Utilisez des ressources avec des fonctions spécifiques pour divers services et éléments de service.|[Configuration de l’affectation des ressources](service-how-setup-resource-allocation.md)|

## Voir aussi

[Vue d’ensemble de Warehouse Management](design-details-warehouse-management.md)
[Achat](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
