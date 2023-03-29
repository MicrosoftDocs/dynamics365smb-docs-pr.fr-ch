---
title: Exécuter des tâches en arrière-plan et de manière récurrente
description: Configurer la synchronisation des données entre Business Central et Shopify en arrière-plan.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
---

# Exécuter des tâches en arrière-plan

Il est efficace d’exécuter certaines tâches simultanément et de manière automatisée. Vous pouvez effectuer ces tâches en arrière-plan et également définir un calendrier pour les exécuter automatiquement. Pour exécuter des tâches en arrière-plan, deux modes sont pris en charge :

- Les tâches déclenchées manuellement sont planifiées immédiatement via **Écritures file d’attente des travaux**.
- Les tâches récurrentes sont planifiées dans **Écritures file d’attente des travaux**.

## Exécuter des tâches en arrière-plan pour un magasin spécifique

1. Sélectionnez ![l’icône Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez le nom du **Magasin Shopify**, puis choisissez le nom du magasin dans la liste.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser les articles pour ouvrir la page **Fiche magasin Shopify**.
3. Activez **Autoriser les synchronisations en arrière-plan**.

Désormais, lorsque l’action de synchronisation est déclenchée, au lieu d’exécuter une tâche au premier plan, vous serez invité à attendre. Une fois la synchronisation terminée, vous pouvez passer à l’action suivante. La tâche est créée comme **Écriture file d’attente des travaux** et démarre instantanément de manière non bloquante.

## Pour programmer des tâches récurrentes

Vous pouvez programmer les activités récurrentes suivantes pour qu’elles soient exécutées de manière automatisée. Pour plus d’informations sur la planification des tâches, voir [File d’attente](../admin-job-queues-schedule-tasks.md).

|Tâche|Objet|
|------|------------|
|**Synchroniser les commandes à partir de Shopify**|État 30104 Synchroniser les commandes à partir de Shopify|
|**Traiter les commandes Shopify**|État 30103 Créer des commandes vente Shopify|
|**Synchroniser livraisons avec Shopify**|État 30109 Synchroniser livraison avec Shopify|
|**Synchroniser les produits et/ou les prix**|État 30108 Synchroniser les produits Shopify|
|**Synchroniser le stock**|État 30102 Synchroniser le stock avec Shopify|
|**Synchroniser les images**|État 30107 Synchroniser les images Shopify|
|**Synchroniser les clients**|État 30100 Synchroniser les clients Shopify|
|**Synchroniser les paiements**|État 30105 Synchroniser les paiements Shopify|

> [!NOTE]
> Certains éléments peuvent être mis à jour par plusieurs tâches, par exemple lorsque vous importez des commandes, selon le paramétrage dans la **fiche magasin Shopify**, le système peut également importer et mettre à jour des données client et/ou produit. N’oubliez pas d’utiliser la même catégorie de file d’attente pour éviter les conflits.

## Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  
