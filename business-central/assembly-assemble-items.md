---
title: Gestion des assemblages | Microsoft Docs
description: "Gérez les sociétés qui fournissent des produits à leurs clients en combinant des composants dans des processus simples sans recourir aux fonctionnalités de fabrication, mais avec des fonctions permettant d'assembler les articles. Ces fonctions s'intègrent à celles existantes : ventes, planification, réservations et entreposage."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4ce03eb7a3685f53869795ded646ef6917a1730a
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="assembly-management"></a>Gestion des assemblages
Pour prendre en charge les sociétés qui fournissent des produits à leurs clients en combinant des composants dans des processus simples sans recourir aux fonctionnalités de fabrication, [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut des fonctions permettant d'assembler les articles. Ces fonctions s'intègrent à celles existantes \(ventes, planification, réservations et entreposage\).  

 Un élément d'assemblage est défini comme un article pouvant être vendu contenant une nomenclature d'assemblage. Pour plus d'informations, reportez-vous à [Utiliser les nomenclatures](inventory-how-work-BOMs.md).

 Les ordres d'assemblage sont des ordres internes, tout comme les ordres de fabrication, qui permettent de gérer le processus d'assemblage et pour lier les besoins de vente aux activités entrepôt impliquées. Les ordres d'assemblage diffèrent des autres types de commande parce qu'ils impliquent à la fois la production et la consommation lors de la validation. L'en-tête d'ordre d'assemblage se comporte de façon similaire à une ligne commande vente, et les lignes d'ordre d'assemblage ont un comportement semblable aux lignes feuille consommation.  

 Pour prendre en charge une stratégie de stock juste-à-temps (JIT) et permettre la personnalisation des produits conformément aux demandes client, il est possible de créer des ordres d'assemblage et de les lier automatiquement dès que la ligne commande vente est créée. Le lien entre la demande de vente et l'approvisionnement d'assemblage permet aux préparateurs de commandes vente de personnaliser l'élément d'assemblage à la volée, d'établir les dates de livraison en fonction de la disponibilité des composants, et de valider la production et l'expédition de l'article assemblé directement à partir de l'interface de commande vente. Pour plus d'informations, reportez-vous à [Vente d'articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).  

 Sur une ligne commande vente, vous pouvez vendre une quantité disponible et qui doit être prélevée à partir du stock conjointement à une quantité qui doit être assemblée pour commande. Certaines règles existent pour gérer la répartition de ces quantités afin de s'assurer que les quantités à assembler pour commande sont prioritaires sur les quantités en stock lors d'expéditions partielles. Pour plus d'informations, voir la section « Scénarios de combinaison » dans [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md).  

 Il existe une fonctionnalité spéciale qui permet de gérer l'expédition des quantités à assembler pour commande. Lorsqu'une quantité à assembler pour commande est prête à être expédiée, le magasinier responsable valide un prélèvement stock pour la ou les lignes commande vente concernées. Cela crée un mouvement de stock pour les composants et valide le résultat d'assemblage et l'expédition de la commande. Pour plus d'informations, reportez-vous à la section « Traitement des articles à assembler pour commande dans les prélèvements stock » dans [Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.   

|**Pour**|**Voir**|  
|------------|-------------|  
|En savoir plus sur la différence entre l'assemblage des articles juste avant l'expédition des commandes vente et l'assemblage des articles destinés au stockage.|[Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Renseignez les champs des fiches magasin et des paramètres stock pour définir le flux des articles vers et depuis le département d'assemblage.|[Configurer des entrepôts de base avec les zones d'opérations](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Personnalisez un élément d'assemblage sur la demande d'un client au cours du processus de vente, et convertissez-le en vente après acceptation.|[Établissement d'un devis de vente Assembler pour commande](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Combinez les composants pour créer un article dans un processus simple, dans le cadre d'une commande ou d'un stock.|[Assembler des articles](assembly-how-to-assemble-items.md)|  
|Vendez les éléments d'assemblage qui ne sont pas disponibles actuellement en créant un ordre d'assemblage associé pour fournir la quantité totale ou partielle de la commande vente.|[Vente d'articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md)|
|Si certains articles à assembler pour commande sont déjà en stock, vous pouvez déduire cette quantité de l'ordre d'assemblage et la réserver dans le stock.|[Vente d'articles en stock dans des flux à assembler pour commande](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Lorsque vous vendez des éléments d'assemblage du stock et que tous les articles ne sont pas disponibles, vous pouvez lancer un ordre d'assemblage automatiquement pour fournir une partie ou l'ensemble de la quantité sur commande vente.|[Vente simultanée d'articles à assembler pour commande et d'articles en stock](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Annulez un ordre d'assemblage validé, par exemple parce que la facture a été validée avec des erreurs qui doivent être corrigées.|[Annuler la validation d'assemblage](assembly-how-to-undo-assembly-posting.md)|
|En savoir plus sur la différence entre les nomenclatures d'assemblage et les nomenclatures de production et les différences de traitement impliquées.|[Utiliser les nomenclatures](inventory-how-work-BOMs.md)|
|Apprendre la manière dont la consommation d'assemblage et la production sont traitées lorsque vous validez des ordres d'assemblage, et découvrir comment les coûts ressource et article sont traités et distribués aux écritures comptables.|[Détails de conception : validation d'ordre d'assemblage](design-details-assembly-order-posting.md)|  

## <a name="see-also"></a>Voir aussi  
[Utiliser les nomenclatures](inventory-how-work-BOMs.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

