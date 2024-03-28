---
title: Créer des fiches article pour des biens ou des services (contient une vidéo)
description: Vous créez des fiches article pour les services que vous vendez en heures et pour les produits physiques. Les exemples incluent les éléments d’assemblage et les produits finis que vous vendez à partir de votre inventaire.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 11/02/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="register-new-items"></a>Enregistrer de nouveaux articles

Les articles, entre autres produits, sont la base de votre activité, les biens ou les services que vous commercialisez. Chaque article doit être enregistré en tant que fiche article.

Les fiches article contiennent les informations nécessaires à l’achat, le stockage, la vente, la livraison et la comptabilisation des articles.

La fiche article peut être de type **Stock**, **Service** ou **Hors stock** pour spécifier si l’article est une unité de stock physique, une unité de temps de travail ou une unité physique qui n’est pas suivie dans le stock. Pour plus d’informations sur les types, voir [À propos des types d’articles](inventory-about-item-types.md).

Un article peut être structuré comme article parent avec les éléments enfants sous-jacents dans une nomenclature. En savoir plus sur les nomenclatures d’élément d’assemblage et les nomenclatures de production dans la section [Utiliser les nomenclatures](inventory-how-work-BOMs.md).

Si vous achetez le même article chez plusieurs fournisseurs, vous pouvez lier ces fournisseurs à la fiche article. La page **Catalogue fournisseur articles** affiche les fournisseurs, de sorte que vous pouvez facilement sélectionner un autre fournisseur.

Les *Articles de catalogue* sont des articles que vous offrez à vos clients, mais que vous ne souhaitez pas gérer dans votre système tant que vous ne les commercialisez pas. Les articles de catalogue ne sont pas des articles normaux de type **Hors-stock**. En savoir plus sur [Utiliser des éléments de catalogue](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Si des modèles article existent pour différents types d’articles, une page s’affiche automatiquement lorsque vous créez une nouvelle fiche article à partir de laquelle vous pouvez sélectionner un modèle article approprié. Si un seul modèle article existe, les nouvelles fiches article utiliseront toujours ce modèle.

La procédure suivante explique comment créer une fiche article à partir de zéro. Vous pouvez également créer de nouvelles fiches d’objets en copiant celles existantes. Pour plus d’informations, voir [Copier des articles existants pour créer de nouveaux articles](inventory-how-copy-items.md).  

<br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card"></a>Pour créer une fiche article

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> Dans le champ **Mode évaluation stock**, vous configurez la façon dont le coût unitaire de l’article est calculé en estimant le flux d’articles dans votre société. Il existe cinq modes évaluation stock disponibles, selon le type d’article. Pour plus d’informations, [Détails de conception : modes évaluation stock](design-details-costing-methods.md).
>
> Si vous sélectionnez **Moyenne**, le coût unitaire de l’article est calculé comme le coût unitaire moyen à chaque moment après un achat. Le stock est évalué avec la supposition que tous les stocks sont vendus simultanément. Avec ce paramètre, vous pouvez choisir le champ **Coût unitaire**, sur la page **Aperçu calc. coût moyen** de la fiche article pour afficher l’historique des transactions à partir duquel est calculé le coût moyen

Vous pouvez afficher ou modifier les prix spécifiques ou les remises accordées, ou que votre vendeur vous accorde, pour l’article si certains critères sont réunis, par exemple le client, la quantité minimum commande ou la date de fin. Pour ce faire, choisissez les actions **Définir les prix spéciaux** ou **Définir les remises spéciales**. Chaque ligne de la page **Prix de vente**, par exemple, représente un prix spécial. Chaque colonne représente un critère qui doit s’appliquer pour accorder à un client le prix spécial que vous entrez dans le champ **Prix unitaire** de la page **Prix de vente**. Pour plus d’informations, voir [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md) ou [Enregistrer les prix d’achat spéciaux et les remises](purchasing-how-record-purchase-price-discount-payment-agreements.md).

L’article est désormais enregistré, et la fiche article est prête à être utilisée sur les documents d’achat et de vente.

Si vous souhaitez utiliser cette fiche article comme modèle lorsque vous créez de nouvelles fiches article, enregistrez-la comme modèle. Pour plus d’informations, reportez-vous à la section suivantes.  

### <a name="to-save-the-item-card-as-a-template"></a>Pour enregistrer la fiche article en tant que modèle

1. Sur la page **Fiche article**, sélectionnez l’action **Sauvegarder comme modèle**. La page **Modèle article** s’ouvre et affiche la fiche article comme modèle.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pour réutiliser les axes analytiques dans les modèles, sélectionnez l’action **Axes analytiques**. La page **Modèles axe** s’ouvre et affiche tous les codes axe qui sont définis pour l’article.
4. Modifiez ou entrez les codes axe s’appliquant aux nouvelles fiches article créées à l’aide du modèle.
5. Lorsque vous terminez le nouveau modèle article, cliquez sur le bouton **OK**.

Le modèle article est ajouté à la liste des modèles article. Vous pouvez ainsi l’utiliser pour créer des fiches article.

### <a name="items-used-in-production-orders"></a>Articles utilisés dans les ordres de fabrication

Si vous souhaitez enregistrer des articles qui sont ensuite utilisés dans des ordres de fabrication, vous spécifiez le système réappro. comme *Ordre de fabrication* sur le raccourci **Réapprovisionnement**. Pour plus d’informations, voir [À propos des ordres de fabrication](production-about-production-orders.md).  

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Pour configurer plusieurs fournisseurs pour un article

Si vous achetez le même article chez plusieurs fournisseurs, vous devez saisir, pour chacun des fournisseurs de cet article des informations concernant, par exemple, ses prix, ses délais, ses escomptes, etc.  

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2. Sélectionnez l’article concerné, puis cliquez sur l’action **Modifier**.  
3. Sélectionnez l’action **Fournisseurs**.  
4. Cliquez sur le champ **N° fournisseur**, puis sélectionnez le fournisseur à paramétrer pour l’article.  
5. De manière facultative, renseignez les autres champs.  
6. Répétez les étapes 2 à 5 pour chaque fournisseur auprès de qui vous souhaitez acheter l’article.

Les fournisseurs s’affichent maintenant sur la page **Catalogue fournisseur articles** (que vous ouvrez à partir de la fiche article), de sorte que vous pouvez facilement sélectionner un autre fournisseur.

## <a name="set-up-item-substitutions"></a>Configuration d’articles de substitution

Vous pouvez configurer des articles pour qu’ils aient des substituts, tels que d’autres articles pouvant être utilisés à la place de l’article d’origine.

### <a name="to-make-an-item-substitution"></a>Pour affecter le statut de substitut à un article

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2. Recherchez l’article concerné, puis cliquez sur le **N° article** pour ouvrir la fiche article.  
3. Choisissez l’action **Association**, puis sélectionnez **Article**, puis **Substitutions** pour ouvrir la page **Saisie de substitution d’article**.  
4. Sélectionnez le champ **N° substitut**, puis sélectionnez l’article de substitution dans la liste.
5. Renseignez ou modifiez les autres champs de la page selon vos besoins.

Lorsque la quantité d’articles requis dépasse la quantité disponible en stock, un message apparaît pour vous informer que des articles de substitution sont disponibles.

> [!NOTE]  
> Sachez que les articles de substitution n’entraîneront pas automatiquement le remplacement d’un article par un autre, par exemple lors de la création d’une commande client ou dans une nomenclature. Au lieu de cela, vous serez alerté du fait qu’un substitut est disponible pour vous.

## <a name="categories-attributes-and-variants"></a>Catégories, attributs et variantes

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

En savoir plus sur les variantes dans la section [Gérer les variantes de produits](inventory-item-variants.md).  

## <a name="delete-item-cards"></a>Supprimer de fiches article

Si vous enregistré une transaction pour un article, vous ne pouvez pas supprimer la carte, car les écritures comptables peuvent être nécessaires pour l’évaluation du stock ou l’audit. Pour supprimer des fiches article avec des écritures comptables, contactez le partenaire Microsoft pour le faire via le code.  

## <a name="manage-inventory-in-warehouses"></a>Gérer le stock des entrepôts

Lorsque vous enregistrez un nouvel article, vous verrez des champs liés à la gestion de l’entrepôt, en particulier sur le raccourci **Entrepôt**. Si votre organisation n’utilise pas les fonctionnalités de gestion d’entrepôt dans [!INCLUDE [prod_short](includes/prod_short.md)], vous pouvez alors ignorer ces champs.  

Si votre organisation configure ultérieurement la gestion des entrepôts, nous vous recommandons de vous assurer que chaque article existant possède les bonnes informations dans les différents champs. De cette façon, les processus d’entrepôt peuvent s’exécuter comme prévu. Ces informations peuvent inclure des champs, tels que **Code classe entrepôt** ou **Code modèle rangement**. Pour plus d’informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).  

## <a name="planning"></a>Planification

Lorsque votre entreprise utilise les processus de planification des approvisionnements dans [!INCLUDE [prod_short](includes/prod_short.md)], vous devez remplir les champs correspondants sur le raccourci **Planification**. Pour une introduction à la zone de planification, voir [Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md).  

Pour des exemples d’utilisation des champs du raccourci **Planification**, voir [Configurer des recommandations : paramètres de planification](setup-best-practices-planning-parameters.md).  

## <a name="see-also"></a>Voir aussi

[Stock](inventory-manage-inventory.md)  
[Configuration des unités de mesure](inventory-how-setup-units-of-measure.md)  
[Gestion des variantes de produits](inventory-item-variants.md)  
[Paramétrer les états intracommunautaires](finance-how-setup-report-intrastat.md#other-intrastat-configurations)  
[Rapprocher l’évaluation stock avec la comptabilité](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Création des souches de numéros](ui-create-number-series.md)  
[Configuration de groupes comptabilisation](finance-posting-groups.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[À propos de la fonctionnalité Planification](production-about-planning-functionality.md)  
[Pratiques de configuration recommandées : paramètres de planification](setup-best-practices-planning-parameters.md)  
[Pratiques de configuration recommandées : planification de l’approvisionnement](setup-best-practices-supply-planning.md)  
[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)  
[Détails de conception : équilibrage de la demande et de l’approvisionnement](design-details-balancing-demand-and-supply.md)  
[Détails de conception : paramètres de planification](design-details-planning-parameters.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
