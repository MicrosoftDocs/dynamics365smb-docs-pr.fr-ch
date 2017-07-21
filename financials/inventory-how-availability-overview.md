---
title: "Obtenir un aperçu des disponibilités| Microsoft Docs"
description: "Vous obtenez des informations sur la disponibilité des articles ou du stock dans tous les magasins, par événement de vente ou d'achat, par période ou par position de l'article sur une nomenclature d'assemblage."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 83af1b6b3a234f67ccc26ee9bba7f5e3e6ff6d77
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-view-the-availability-of-items"></a>Procédure : voir la disponibilité des articles
Dans le contexte d'une tâche professionnelle, vous pouvez obtenir des informations avancées sur la disponibilité et l'emplacement d'un article, par exemple en discutant avec un client à propos d'une date de livraison.

Vous pouvez afficher la disponibilité de tous les articles par emplacement, et vous pouvez afficher la disponibilité de chaque article par événement, par période, ou par magasin. Un événement désigne tout mouvement de stock prévu, par exemple une expédition vente ou une réception enlogement transfert.

> [!NOTE]  
>   Les vues de disponibilité par magasin nécessitent la mise à jour de stock dans plusieurs magasins. Pour plus d'informations, reportez-vous à [Procédure : Configurer des magasins](inventory-how-setup-locations.md).

Dans [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)], les chiffres de disponibilité sont affichés dans deux champs de définition différents.

* Le champ **Quantité disponible** affiche la quantité réelle en fonction des écritures comptables articles validées.
* Le champ **Stock prévisionnel** est calculé et affiche la quantité disponible plus les réceptions planifiées moins les besoins bruts. (Dans [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)], les réceptions planifiées incluent des quantités sur des commandes achat et des ordres de transfert enlogement. Les besoins bruts incluent des quantités sur les commandes vente et les désenlogements transfert.)

> [!TIP]  
>   Le stock prévisionnel disponible s'avère particulièrement utile dans les fenêtres **Disponibilité art. par période** et **Disponibilité article par événement** car ils contiennent l'axe de date.  

> [!NOTE]  
>   Les procédures suivantes décrivent comment afficher des informations avancées sur la disponibilité de la liste des articles et de la fiche article. Vous pouvez également accéder aux informations à partir des lignes de document vente, pour l'article sur la ligne. Pour en savoir plus, voir [Procédure : vendre des produits](sales-how-sell-products.md).

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Pour afficher la disponibilité d'un article en fonction de sa réception ou de sa livraison
Vous pouvez afficher la disponibilité d'un article en fonction des mouvements de stock attendus dans la fenêtre **Disponibilité par événement**.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche d'un article dont vous voulez afficher la disponibilité.
3. Cliquez sur **Disponibilité article par**, puis sur **Événement**.

    La fenêtre **Disponibilité article par événement** indique comment la quantité du stock de l'article se développera dans le temps en fonction des expéditions et des réceptions prévues. La fenêtre fournit une vue condensée qui affiche une ligne d'informations cumulées par intervalle de temps, dans laquelle les quantités de stock sont modifiées. Les intervalles de temps au cours desquels aucun événement ne s'est produit ne sont pas affichés. Vous pouvez développer chaque ligne pour afficher les détails concernant l'événement ou les événements à l'origine de la quantité cumulée figurant sur la ligne.
4. Sélectionnez la valeur dans le champ **Stock prévisionnel** pour afficher les écritures comptables articles ou ouvrez des documents qui constituent la valeur.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>Pour afficher la disponibilité d'un article dans différentes périodes
Vous pouvez visualiser la disponibilité d'un article dans le temps pour les périodes définies dans la fenêtre **Disponibilité art. par période**.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche d'un article dont vous voulez afficher la disponibilité.
3. Cliquez sur **Disponibilité article par**, puis sur **Période**.

    La fenêtre **Disponibilité art. par période** indique comment la quantité du stock de l'article se développera dans le temps, en fonction d'une période que vous sélectionnez, par exemple Jour, Semaine, ou Trimestre.
4. Sélectionnez la valeur dans le champ **Stock prévisionnel** pour afficher les écritures comptables articles ou ouvrez des documents qui constituent la valeur.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>Pour afficher la disponibilité d'un article dans les magasins dans lesquels il est stocké
Vous pouvez afficher la disponibilité d'un article dans les magasins dans lesquels il est stocké dans la fenêtre **Disponibilité art. par magasin**.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche d'un article dont vous voulez afficher la disponibilité.
3. Cliquez sur **Disponibilité article par**, puis sur **Magasin**.

    La fenêtre **Disponibilité art. par magasin** indique comment la quantité du stock de l'article se développera dans le temps, pour chaque magasin où l'article est stocké.
4. Sélectionnez la valeur dans le champ **Qté disponible** pour afficher les écritures comptables articles qui constituent la valeur.
5. Sélectionnez la valeur dans le champ **Stock prévisionnel** pour afficher les écritures comptables articles ou ouvrez des documents qui constituent la valeur.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>Pour afficher la disponibilité de tous les articles en fonction des magasins où ils sont stockés
Vous pouvez afficher la disponibilité de tous vos articles dans tous vos magasins dans la fenêtre **Articles par magasin**.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.
2. Cliquez sur **Articles par magasin**.

    La fenêtre **Articles par magasin** indique pour tous les articles les quantités disponibles dans chaque magasin.
3. Sélectionnez la valeur dans le champ **Qté disponible** pour afficher les écritures comptables articles qui constituent la valeur.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-boms"></a>Pour afficher la disponibilité d'un article en fonction de son utilisation dans les nomenclatures d'assemblage
Si un article existe dans les nomenclatures d'assemblage, comme article parent ou composant, vous pouvez afficher le nombre d'unités nécessaires dans la fenêtre **Disponibilité article par niveau de nomenclature**. La fenêtre indique le nombre d'unités d'un parent vous pouvez réaliser en fonction de la disponibilité des éléments enfants sur les lignes sous-jacentes. Tout article qui a une nomenclature d'assemblage est affiché dans la fenêtre sous forme de ligne pliante. Vous pouvez développer cette ligne pour afficher les composants sous-jacents et les sous-assemblages de niveau inférieur avec leurs propres nomenclatures.

Vous pouvez utiliser la fenêtre pour savoir si vous pouvez traiter une commande vente d'un article à une date spécifique, en consultant sa disponibilité actuelle et les quantités que ses composants peuvent fournir. Vous pouvez également utiliser la fenêtre pour identifier les goulets d'étranglement dans des nomenclatures d'assemblage associées.

Sur chaque ligne de la fenêtre pour les articles parents et les éléments enfants, les champs clés suivants indiquent les chiffres de disponibilité. Vous pouvez utiliser ces chiffres pour promettre le nombre d'unités d'un parent que vous pouvez fournir si vous lancez le processus d'assemblage lié.

|Champ|Désignation|
|------|-----------|
|**Capable de fabriquer le parent**|Indique le nombre d'unités d'un sous-assemblage de l'article supérieur que vous pouvez effectuer. Ce champ indique combien d'unités de l'article parent immédiat vous pouvez assembler. La valeur est basée sur la disponibilité de l'article sur la ligne.|
|**Capable de fabriquer le meilleur article**|Indique le nombre d'unités de l'article supérieur que vous pouvez effectuer. Ce champ indique combien d'unités de l'article de la nomenclature sur la ligne supérieure vous pouvez assembler. La valeur est basée sur la disponibilité de l'article sur la ligne.|

La fenêtre **Disponibilité article par niveau de nomenclature** affiche les informations de l'article figurant sur la fiche ou la ligne document pour laquelle la fenêtre est ouverte. l'article est toujours indiqué sur la ligne supérieure. Vous pouvez visualiser les informations d'autres articles ou de tous les articles en changeant la valeur du champ **Filtre article**.

> [!NOTE]  
>   Par défaut, les chiffres de disponibilité dans les lignes présentent la disponibilité globale de tous les articles sous l'article supérieur. Ces chiffres sont affichés dans le champ **Quantité disponible**, et ils concernent l'article de niveau supérieur. Toutefois, les informations sur le nombre de sous-assemblages que vous pouvez effectuer peuvent être erronées. Pour obtenir une véritable indication du nombre de sous-assemblages que vous pouvez effectuer, vous devez désactiver la case à cocher **Afficher disponibilité totale**, puis examiner le chiffre dans le champ **Capable de fabriquer le parent**.

Le champ **Goulot d'étranglement** spécifie quel article dans la structure de la nomenclature vous empêche de réaliser une quantité supérieure à la quantité affichée dans le champ **Capable de fabriquer le meilleur article**. Par exemple, l'article goulot d'étranglement peut être un composant achat avec une date de réception prévue qui est trop tardive pour fabriquer des unités supplémentaires de l'élément qui le comporte à la date du champ **Requis par date**.

## <a name="see-also"></a>Voir aussi
[Gestion du stock](inventory-manage-inventory.md)  
[Procédure : utiliser les nomenclatures](inventory-how-work-BOMs.md)    
[Procédure : configurer des magasins](inventory-how-setup-locations.md)  
[Procédure : transfert de stock entre des magasins](inventory-how-transfer-between-locations.md)  
[Procédure : vendre des produits](sales-how-sell-products.md)      
[Chaîne d'approvisionnement](madeira-supply-chain.md)  
[Utilisation de Financials](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

