---
title: Configurer des groupes remises client
description: Découvrez comment configurer des groupes remises client et créer des remises ligne vente pour ces groupes.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 06/08/2022
ms.author: a-reishima
---
# Configurer des groupes remises client

Vous pouvez définir des remises ligne vente pour un groupe de clients au lieu de les appliquer individuellement.

Les **groupes remises client** fonctionnent de la même manière que les [groupes tarifs client](sales-how-to-set-up-customer-price-groups.md), mais peuvent être combinés avec des groupes remises article pour définir rapidement des remises ligne sur de nombreux articles pour des clients sélectionnés.

## Créer des remises ligne vente pour un groupe de clients

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes remises client**, puis sélectionnez le lien associé.
2. Sur la page **Groupes remises client**, sélectionnez **Nouveau** pour créer un groupe de remises et lui donner un nom dans la colonne **Code** et ajoutez une description.
3. Sélectionnez l’action **Naviguer** et choisissez **Remises ligne vente**.
4. Remplissez la colonne **Code vente** avec le groupe remises que vous avez créé à la page précédente.
5. Dans les champs des différentes lignes, renseignez les valeurs pour **Type** (Article ou groupe remises article), **Code**, **Unité** et **% remise ligne**.
6. Si le groupe de clients doit acheter une quantité minimum pour bénéficier de la remise, renseignez le champ **Quantité minimum**.
7. Si nécessaire, saisissez la **date de début** et la **date de fin** pour le groupe de remises.
8. Le cas échéant, vous pouvez également spécifier le **Code devise** ou le **Code variante** après [avoir personnalisé les colonnes](ui-personalization-user.md).

Répétez les étapes 4 à 8 pour chacun des articles ou chacun des groupes remises article pour lesquels vous souhaitez créer une remise ligne vente.

## Affecter un client à un groupe de remises

Une fois ces groupes remises client définis, vous pouvez entrer les codes groupe remises client sur les fiches client.

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Ouvrez la **fiche client** au client que vous voulez associer à un groupe remises client.
3. Sur le raccourci **Facturation**, dans le champ **Groupe rem. client**, sélectionnez le code groupe.

## Voir aussi

[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Enregistrement des prix de vente spéciaux et des remises](sales-how-record-sales-price-discount-payment-agreements.md)  
[Configuration de groupes tarifs client](sales-how-to-set-up-customer-price-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
