---
title: Obtenir un aperçu des disponibilités
description: 'Vous obtenez des informations sur la disponibilité des articles ou du stock dans tous les magasins, par événement de vente ou d’achat ou par période.'
documentationcenter: ''
author: brentholtorf
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.search.form: '908, 909, 925, 926, 504, 501, 500, 499, 99000896, 342, 515, 5417, 5415, 5871, 5530, 492, 157, 5540, 5416, 5414, 1872, 1873, 99000902, 353, 491, 9231, 5390'
ms.date: 09/21/2022
ms.author: bholtorf
---
# <a name="view-the-availability-of-items"></a>Voir la disponibilité des articles

Dans le contexte d’une tâche professionnelle, vous pouvez obtenir des informations avancées sur la disponibilité et l’emplacement d’un article, par exemple en discutant avec un client à propos d’une date de livraison.

Vous pouvez afficher la disponibilité de tous les articles par magasin, et vous pouvez afficher la disponibilité de chaque article par événement ou par période. Un événement désigne tout mouvement de stock prévu, par exemple une expédition vente ou une réception enlogement transfert.

> [!NOTE]  
>   Les vues de disponibilité par magasin nécessitent la mise à jour de stock dans plusieurs magasins. Pour plus d’informations, reportez-vous à [Configurer des magasins](inventory-how-setup-locations.md).

Si vous utilisez la fonctionnalité entrepôt, la disponibilité varie selon les affectations au niveau de l’emplacement quand des activités entrepôt, par exemple des prélèvements et des mouvements défectueux, se produisent et quand le système de réservation de stock impose des restrictions à respecter. Un algorithme plutôt complexe vérifie que toutes les conditions sont remplies avant d’affecter des quantités aux prélèvements pour les flux sortants. Pour plus d’informations, voir [Détails de conception : disponibilité dans l’entrepôt](design-details-availability-in-the-warehouse.md).

Dans [!INCLUDE[prod_short](includes/prod_short.md)], les chiffres de disponibilité sont généralement affichés dans deux champs de définition différents.

* Le champ **Quantité disponible**, dans certains emplacements nommés **Stock**, affiche la quantité réelle en fonction des écritures comptables articles validées.
* Le champ **Stock prévisionnel** est calculé et affiche la quantité disponible plus les réceptions planifiées moins les besoins bruts. (Dans [!INCLUDE[prod_short](includes/prod_short.md)], les réceptions planifiées incluent des quantités sur des commandes achat et des ordres de transfert enlogement. Les besoins bruts incluent des quantités sur les commandes vente et les désenlogements transfert.)

> [!TIP]  
>   Le stock prévisionnel disponible s’avère particulièrement utile dans les pages **Disponibilité art. par période** et **Disponibilité article par événement**, car ils contiennent l’axe de date.  

> [!NOTE]  
>   Les procédures suivantes décrivent comment afficher des informations avancées sur la disponibilité de la liste des articles et de la fiche article. Vous pouvez également accéder aux informations à partir des lignes de document vente, pour l’article sur la ligne. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Pour afficher la disponibilité d’un article en fonction de sa réception ou de sa livraison

Vous pouvez afficher la disponibilité d’un article en fonction des mouvements de stock attendus sur la page **Disponibilité par événement**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Ouvrez la fiche d’un article dont vous voulez afficher la disponibilité.
3. Cliquez sur **Disponibilité article par**, puis sur **Événement**.

    La page **Disponibilité article par événement** indique comment la quantité du stock de l’article se développera dans le temps en fonction des expéditions et des réceptions prévues. La page fournit une vue condensée qui affiche une ligne d’informations cumulées par intervalle de temps, dans laquelle les quantités de stock sont modifiées. Les intervalles de temps au cours desquels aucun événement ne s’est produit ne sont pas affichés. Vous pouvez développer chaque ligne pour afficher les détails concernant l’événement ou les événements à l’origine de la quantité cumulée figurant sur la ligne.
4. Sélectionnez la valeur dans le champ **Stock prévisionnel** pour afficher les écritures comptables articles ou ouvrez des documents qui constituent la valeur.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>Pour afficher la disponibilité d’un article dans différentes périodes

Vous pouvez visualiser la disponibilité d’un article dans le temps pour les périodes définies sur la page **Disponibilité art. par période**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Ouvrez la fiche d’un article dont vous voulez afficher la disponibilité.
3. Cliquez sur **Disponibilité article par**, puis sur **Période**.

    La page **Disponibilité art. par période** indique comment la quantité du stock de l’article se développera dans le temps, en fonction d’une période que vous sélectionnez, par exemple Jour, Semaine, ou Trimestre.
4. Sélectionnez la valeur dans le champ **Stock prévisionnel** pour afficher les écritures comptables articles ou ouvrez des documents qui constituent la valeur.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>Pour afficher la disponibilité d’un article dans les magasins dans lesquels il est stocké

Vous pouvez afficher la disponibilité d’un article dans les magasins dans lesquels il est stocké sur la page **Disponibilité art. par magasin**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Ouvrez la fiche d’un article dont vous voulez afficher la disponibilité.
3. Cliquez sur **Disponibilité article par**, puis sur **Magasin**.

    La page **Disponibilité art. par magasin** indique comment la quantité du stock de l’article se développera dans le temps, pour chaque magasin où l’article est stocké.
4. Sélectionnez la valeur dans le champ **Qté disponible** pour afficher les écritures comptables articles qui constituent la valeur.
5. Sélectionnez la valeur dans le champ **Stock prévisionnel** pour afficher les écritures comptables articles ou ouvrez des documents qui constituent la valeur.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>Pour afficher la disponibilité de tous les articles en fonction des magasins où ils sont stockés

Vous pouvez afficher la disponibilité de tous vos articles dans tous vos magasins sur la page **Articles par magasin**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Cliquez sur **Articles par magasin**.

    La page **Articles par magasin** indique pour tous les articles les quantités disponibles dans chaque magasin.
3. Sélectionnez la valeur dans le champ **Qté disponible** pour afficher les écritures comptables articles qui constituent la valeur.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms"></a>Pour afficher la disponibilité d’un article en fonction de son utilisation dans les nomenclatures d’assemblage ou de production

Si un article figure dans les nomenclatures d’assemblage ou de production, comme article parent ou composant, vous pouvez afficher le nombre d’unités nécessaires sur la page **Disponibilité article par niveau de nomenclature**. La page indique le nombre d’unités d’un article parent vous pouvez réaliser en fonction de la disponibilité des éléments enfants sur les lignes sous-jacentes. Tout article qui a une nomenclature d’assemblage ou de production est affiché sur la page sous forme de ligne réductible. Vous pouvez développer cette ligne pour afficher les composants sous-jacents et les sous-assemblages de niveau inférieur avec leurs propres nomenclatures.

Par exemple, vous pouvez utiliser la page pour déterminer si vous pouvez traiter une commande vente d’un article à une date spécifique, en consultant sa disponibilité actuelle et les quantités que ses composants peuvent fournir. Vous pouvez également utiliser la page pour identifier les goulets d’étranglement dans des nomenclatures associées.

Sur chaque ligne de la page pour les articles parents et les éléments enfants, les champs clés suivants indiquent les chiffres de disponibilité. Vous pouvez utiliser ces chiffres pour promettre le nombre d’unités d’un parent que vous pouvez fournir si vous lancez le processus d’assemblage lié.

|Champ|Désignation|
|------|-----------|
|**Capable de fabriquer le parent**|Indique le nombre d’unités d’un sous-assemblage de l’article supérieur que vous pouvez effectuer. Ce champ indique combien d’unités de l’article parent immédiat vous pouvez assembler. La valeur est basée sur la disponibilité de l’article sur la ligne.|
|**Capable de fabriquer le meilleur article**|Indique le nombre d’unités de l’article supérieur que vous pouvez effectuer. Ce champ indique combien d’unités de l’article de la nomenclature sur la ligne supérieure vous pouvez assembler. La valeur est basée sur la disponibilité de l’article sur la ligne.|

### <a name="to-view-the-availability-of-an-item-according-to-demand-for-its-parent"></a>Pour afficher la disponibilité d’un article en fonction de la demande pour son parent

La page **Disponibilité article par niveau de nomenclature** affiche les informations de l’article figurant sur la fiche ou la ligne document pour laquelle la page est ouverte. l’article est toujours indiqué sur la ligne supérieure. Vous pouvez visualiser les informations d’autres articles ou de tous les articles en changeant la valeur du champ **Filtre article**.

> [!NOTE]  
>   Par défaut, les chiffres de disponibilité dans les lignes présentent la disponibilité globale de tous les articles sous l’article supérieur. Ces chiffres sont affichés dans le champ **Quantité disponible**, et ils concernent l’article de niveau supérieur. Toutefois, les informations sur le nombre de sous-assemblages que vous pouvez effectuer peuvent être erronées. Pour obtenir une véritable indication du nombre de sous-assemblages que vous pouvez effectuer, vous devez désactiver la case à cocher **Afficher disponibilité totale**, puis examiner le chiffre dans le champ **Capable de fabriquer le parent**.

Le champ **Goulot d’étranglement** spécifie quel article dans la structure de la nomenclature vous empêche de réaliser une quantité supérieure à la quantité affichée dans le champ **Capable de fabriquer le meilleur article**. Par exemple, l’article goulot d’étranglement peut être un composant achat avec une date de réception prévue qui est trop tardive pour fabriquer des unités supplémentaires de l’élément qui le comporte à la date du champ **Requis par date**.

## <a name="to-view-the-availability-of-an-item-by-its-units-of-measure"></a>Pour afficher la disponibilité d’un article par ses unités de mesure

La page **Disponibilité de l’article par unité de mesure** affiche la disponibilité d’un article dans les différentes unités de mesure dans lesquelles il est stocké.

> [!NOTE]  
> Pour conserver ces informations exactes, vous devez convertir les unités article. Par exemple, si vous achetez un article dans une unité, comme des boîtes, et que vous vendez des articles dans une autre unité, comme des pièces, vous devez utiliser un journal d’articles pour convertir les unités de mesure, ou "déballer" les articles. Vous pouvez utiliser une ligne feuille d’ajustement négatif pour réduire le stock dans l’unité d’achat, par exemple des boîtes, et un ajustement positif pour augmenter le stock dans l’unité de vente, par exemple des pièces. 

## <a name="to-view-the-availability-of-an-item-by-its-variants"></a>Pour afficher la disponibilité d’un article par ses variantes

La page **Dispo. article par variante** présente la disponibilité réelle et projetée d’un article regroupé selon le code variante.

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Ouvrez la fiche d’un article dont vous voulez afficher la disponibilité.
3. Cliquez sur **Disponibilité article par**, puis sur **Variante**.

    La page **Dispo. article par variante** affiche la disponibilité pour chaque variante qui existe pour l’article. La page est vide si aucune variante n’existe pour l’article.

4. Dans le champ **Afficher par**, sélectionnez la durée de la période à afficher.
5. Affichez les chiffres de disponibilité dans les différents champs de quantité pour chaque ligne.

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="assembly-availability-page"></a>Page Disponibilité assemblage

La page **Disponibilité assemblage** affiche des informations de disponibilité détaillées pour l’élément d’assemblage. Elle s’ouvre :

- Automatiquement à partir d’une ligne commande vente dans les scénario Assembler pour commande lorsque vous entrez une quantité à l’origine d’un problème de disponibilité des composants.
- Automatiquement à partir d’un en-tête d’ordre d’assemblage lorsque vous entrez une valeur dans le champ Quantité à l’origine d’un problème de disponibilité des composants.
- Manuellement lorsque vous l’ouvrez à partir d’un ordre d’assemblage. Sur l’onglet Actions , dans le groupe Fonctions, cliquez sur Afficher disponibilité.

Le raccourci **Détails** affiche des informations de disponibilité détaillées pour l’élément d’assemblage, dont la part de la quantité d’ordre d’assemblage pouvant être assemblée d’ici la date d’échéance sur la base de la disponibilité des composants requis. Cela s’affiche dans le champ Capacité d’assembler sur le raccourci Détails .

La valeur du champ **Capacité d’assembler** s’affiche en rouge si la quantité est inférieure à la quantité du champ **Quantité restante** , indiquant ainsi qu’il n’y a pas de suffisamment de composants disponibles pour assembler la quantité totale.

Le raccourci **Lignes** affiche des informations de disponibilité détaillées pour les composants d’assemblage.

Si un ou plusieurs composants d’assemblage ne sont pas disponibles, cela est alors reflété dans le champ **Capacité d’assembler** de la ligne en question comme quantité inférieure à la quantité dans le champ **Quantité restante** sur le raccourci **Détails** .

## <a name="see-also"></a>Voir aussi

[Gestion du stock](inventory-manage-inventory.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser les nomenclatures](inventory-how-work-BOMs.md)  
[Utilisation des nomenclatures d’assemblage](assembly-how-work-assembly-boms.md)  
[Créer des nomenclatures de production](production-how-to-create-production-boms.md)  
[Configurer des magasins](inventory-how-setup-locations.md)  
[Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md)  
[Vendre des produits](sales-how-sell-products.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utiliser Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
