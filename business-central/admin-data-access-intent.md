---
title: "Gérer l’accès intentionnel à la base de données dans Business\_Central"
description: 'Modifiez l’accès intentionnel à la base de données pour les états, les pages API et les requêtes.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9880
ms.date: 04/01/2021
ms.author: jswymer
---
# Gestion de l’accès intentionnel à la base de données

En tant que superutilisateur ou administrateur, vous pouvez modifier l’accès intentionnel à la base de données pour les états, les pages du type API et les requêtes pour améliorer les performances du service.

## Aperçu

[!INCLUDE[prod_short](includes/prod_short.md)] peut être configuré pour utiliser des répliques en lecture seule de la base de données principale (en lecture-écriture). L’utilisation de répliques de la base de données réduit la charge sur la base de données principale. Dans certains cas, cela améliore également les performances lors de l’affichage des données dans le client. Les répliques sont avantageuses pour les objets tels que les états, les requêtes et les pages API, qui permettent uniquement d’afficher les données, et non de les modifier.

Lors de l’exécution des objets, l’accès intentionnel à la base de données détermine s’il faut utiliser une réplique en lecture seule, en cas de disponibilité, ou la base de données principale. Les états, les pages API et les requêtes sont développés avec un accès intentionnel à la base de données prédéfini (voir [Propriété DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

La page **Liste d’accès intentionnels à la base de données** vous permet de remplacer l’accès intentionnel à la base de données prédéfini pour les objets lors de leur exécution.

En termes de base de données, cette fonction est communément appelée *échelle horizontale en lecture*. Pour en savoir plus sur l’échelle horizontale en lecture et l’accès intentionnel aux données dans [!INCLUDE[prod_short](includes/prod_short.md)], consultez [Utilisation de l’échelle horizontale en lecture pour de meilleures performances](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) dans l’aide [!INCLUDE[prod_short](includes/prod_short.md)] sur Developer and Administration.

## Pour modifier l’accès intentionnel à la base de données

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Liste d’accès intentionnels à la base de données**, puis choisissez le lien associé.

    La page répertorie l’ensemble des états, pages et requêtes. La colonne **Accès intentionnel** comprend l’une des valeurs suivantes :

    |**Paramètres**|**Description**|  
    |------------|-------------|  
    |**Par défaut**|Indique que l’objet utilise l’accès intentionnel à la base de données prédéfini.|
    |**Autoriser écriture**|Définit l’objet pour utiliser la base de données principale, permettant à l’utilisateur de modifier les données.|
    |**Lecture seule**|Définit l’objet pour utiliser la réplique de la base de données ; autrement dit, l’utilisateur peut uniquement afficher les données, et non les modifier.|

2. Choisissez l’action **Modifier la liste**.

3. Sur la page **Modifier : liste d’accès intentionnels à la base de données**, modifiez le champ **Accès intentionnel** pour les objets.

    > [!NOTE]
    > Si un objet modifiable, comme la fiche client, est défini sur **Lecture seule**, la base de données principale est toujours utilisée, quelle que soit l’accès intentionnel, permettant aux utilisateurs d’apporter des modifications comme d’habitude.

## Voir la [formation Microsoft](/training/paths/deploy-configure-dynamics-365-business-central/) associée

## Voir aussi
[Fonctionnalités d’entreprise](across-business-functionality.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
