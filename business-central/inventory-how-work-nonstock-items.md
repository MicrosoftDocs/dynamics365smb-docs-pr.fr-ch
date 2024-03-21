---
title: Créer et gérer des articles de catalogue
description: Découvrez comment vendre des articles que vous ne conservez pas dans votre liste d’articles.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.keywords: non-inventoriable
ms.search.forms: '5725, 5726, 5732'
ms.service: dynamics-365-business-central
---

# Utiliser des articles de catalogue

Les articles de catalogue sont des éléments que vous ne gérez pas dans [!INCLUDE[prod_short](includes/prod_short.md)] jusqu’à ce que vous les vendiez. Lorsque vous utilisez l’action **Sélectionner un article de catalogue** pour ajouter un article de catalogue à une ligne d’une commande client, d’un devis ou d’une commande cadre vente, l’article de catalogue est converti en article standard.

> [!NOTE]  
> Vous ne pouvez pas sélectionner d’article de catalogue à partir de la page **Facture vente**.

Un article de catalogue a généralement le numéro d’article du fournisseur qui le fournit. Avant de pouvoir convertir un article de catalogue en article normal, vous devez spécifier comment convertir les numéros d’article du fournisseur en votre numérotation d’article. Pour plus d’informations sur la numérotation des articles, consultez [Spécifier comment les numéros d’article de catalogue sont convertis en votre propre numérotation](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Les articles de catalogue ne doivent pas être confondus avec les articles hors stock, qui sont des articles normaux qui ont le type **Hors stock** pour les conserver hors les calculs de disponibilité et d’évaluation, par exemple parce qu’ils sont uniquement utilisés en interne et ont un coût bas. Pour en savoir plus sur les articles non stockés, accédez à [À propos des types d’articles](inventory-about-item-types.md).

## Créer un article de catalogue

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles de catalogue**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Spécifier comment les numéros d’article de catalogue sont convertis en votre propre numérotation

Avant de pouvoir convertir un article de catalogue en article standard, vous devez spécifier comment convertir les numéros d’article du fournisseur en la structure que vous utilisez pour les numéros d’article.

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Paramètres article de catalogue**, puis choisissez le lien associé.
2. Dans le champ **Format numéro**, choisissez l’option que vous préférez.

## Convertir un article de catalogue en un article normal

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles de catalogue**, puis choisissez le lien associé.
2. Ouvrez la fiche pour un article de catalogue que vous pouvez convertir en un article normal.
3. Sur la page **Fiche article de catalogue**, sélectionnez l’action **Créer un article**.

Une nouvelle fiche article pré-remplie avec les informations de l’article de catalogue ainsi qu’un modèle d’article sont créés. Vous pouvez modifier les informations sur le nouvel article, si nécessaire. Pour en savoir plus sur la création d’articles, consultez [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).

## Pour vendre un article de catalogue et le convertir en article normal

Le processus suivant utilise une commande client, mais les étapes sont les mêmes pour les commandes client ouvertes et les devis.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Commandes vente**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**. Complétez les champs du raccourci **Général** comme pour toute commande vente. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).
3. Sur une nouvelle ligne vente, dans le champ **Type**, sélectionnez **Article**, mais laissez le champ **N°** vide.
4. Choisissez l’action **Ligne**, puis l’action **Sélectionner articles de catalogue**.
5. Sur la page **Articles de catalogue**, sélectionnez l’article de catalogue que vous souhaitez vendre, puis choisissez le bouton **OK**.
6. Lorsque les lignes commande vente sont renseignées, sélectionnez l’action **Valider**.

> [!NOTE]  
> Une référence article est automatiquement créée entre le numéro article fournisseur et votre nouveau numéro article. Pour en savoir plus sur les références d’articles, accédez à [Utiliser les références d’articles](inventory-how-use-item-cross-refs.md).

## Voir aussi

[Enregistrement des nouveaux articles](inventory-how-register-new-items.md)  
[Création des commandes spéciales](sales-how-to-create-special-orders.md)  
[Stock](inventory-manage-inventory.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
