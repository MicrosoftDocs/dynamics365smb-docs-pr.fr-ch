---
title: Paramétrer la TVA non déductible
description: Cet article explique comment configurer la TVA non déductible dans Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 04/26/2023
ms.custom: bap-template
---

# Paramétrer la TVA non déductible

La taxe sur la valeur ajoutée (TVA) non déductible est la TVA payable par un acheteur, mais qui n’est pas déductible de la TVA exigible de l’acheteur. Les entreprises peuvent généralement récupérer la TVA sur l’achat de biens et services liés à leurs activités commerciales. Cependant, dans certaines situations, une entreprise supporte la TVA qui n’est pas déductible. Ces situations sont généralement liées aux réglementations locales et peuvent différer d’un pays à l’autre. Cependant, le modèle d’utilisation de la TVA non déductible ou partiellement déductible est similaire. Vous pouvez utiliser la TVA proportionnelle pour calculer la TVA en cas de TVA déductible et non déductible.

En général, la TVA ne peut pas être déduite pour certains achats en raison des facteurs suivants :

- **Le type de biens ou services achetés** – La TVA est totalement ou partiellement non déductible en vertu d’une disposition de la loi sur les biens tels que les voitures, les téléphones portables et les produits alimentaires achetés dans les restaurants.
- **TVA au prorata partiellement déductible** – La TVA est calculée au prorata du ratio entre les opérations de vente pour lesquelles la TVA est due et toutes les opérations qui ont été effectuées. La TVA qui dépasse ce ratio ne peut pas être déduite.

Comme il peut être difficile de savoir où et comment un article est utilisé, vous devez contacter les autorités fiscales locales de votre pays pour déterminer si un pourcentage spécifié de la TVA est déductible en fonction des données historiques. 

> [!IMPORTANT]
> Cette fonctionnalité globale est disponible dans tous les pays où la TVA est activée **à l’exception de la Belgique, de l’Italie, de la Norvège et de l’Espagne**. Ces localisations ont déjà une fonctionnalité locale existante et seront mises à jour à l’avenir. N’exécutez pas cette fonctionnalité dans ces pays, car la procédure de mise à niveau n’existe pas.

## Utilisation de la TVA non déductible

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche 3.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres VAT**, puis sélectionnez le lien associé.
2. Cochez la case **Activer TVA non déductible**.

    > [!IMPORTANT]
    > Une fois que vous avez activé la TVA non déductible, vous ne pouvez pas la désactiver, car la fonctionnalité peut inclure des modifications de données et déclencher une mise à niveau de certaines tables de la base de données. Microsoft vous recommande vivement d’activer et de tester d’abord cette fonctionnalité dans l’environnement de bac à sable avant de l’activer dans l’environnement de production.

3. Configurez la manière dont le système traite les valeurs de TVA non déductible.

    1. Dans le champ **Utiliser pour le coût de l’article**, indiquez si la TVA non déductible doit être ajoutée au coût de l’article lorsque vous achetez des articles. Sinon, la TVA non déductible n’a aucune influence sur le coût de l’article et le montant total est enregistré uniquement au niveau de la comptabilité.
    2. Cochez la case **Utiliser pour le coût de l’immobilisation** pour ajouter la TVA non déductible au coût de l’immobilisation lorsque vous achetez de nouvelles immobilisations. Sinon, la TVA non déductible n’a aucune influence sur le coût de l’immobilisation et le montant total est enregistré uniquement au niveau de la comptabilité.
    3. Cochez la case **Utiliser pour le coût du projet** pour spécifier que la TVA non déductible doit être ajoutée au coût du projet lorsque vous achetez des articles pour le projet. Sinon, la TVA non déductible n’a aucune influence sur le coût du projet et le montant total est enregistré uniquement au niveau de la comptabilité.
    4. Cochez la case **Afficher TVA non déductible sur lignes** pour spécifier que la TVA non déductible doit être affichée sur les pages de ligne de document pour faciliter la manipulation des montants de TVA.

## Utiliser le pourcentage de TVA non déductible

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche 3.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres comptabilisation TVA**, puis sélectionnez le lien associé.
2. Sur la page **Paramètres comptabilisation TVA**, définissez les champs comme indiqué dans le tableau suivant.

    | Champ | Désignation |
    |-------|-------------|
    | Autoriser TVA non déductible | Spécifiez si la TVA non déductible est prise en compte pour la combinaison actuelle d’un groupe comptabilisation marché TVA et d’un groupe comptabilisation produit TVA. |
    | % TVA non déductible | Spécifiez le pourcentage du montant de la transaction auquel la TVA n’est pas lettrée. |
    | Compte TVA achat non déductible | Spécifiez le compte associé au montant de TVA qui n’est pas déduit à cause du type de biens ou services achetés. |

    > [!NOTE]
    > Pour avoir des écritures comptables qui utilisent le compte dédié au lieu du compte vente/achat, vous pouvez laisser le champ **Compte TVA achat non déductible** vide ou définir le champ **Compte général**.

3. Sélectionnez **OK**.

> [!NOTE]
> Vous ne pouvez pas utiliser la TVA non réalisée avec la TVA non déductible.
>
> N’utilisez pas la même valeur **Identifiant TVA** pour la TVA normale où le champ **% TVA non déductible** est défini sur **0** (zéro) et la TVA normale où le champ **% TVA non déductible** est défini sur une valeur non nulle. Sinon, le montant total de la TVA non déductible est calculé de manière incorrecte.

## Voir aussi

[Gestion financière](finance.md)  
[Configurer des méthodes de calcul et de validation de la taxe sur la valeur ajoutée](finance-setup-vat.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
