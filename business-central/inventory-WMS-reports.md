---
title: États et analyses de stock et d’entrepôt
description: Découvrez les états et analyses de stock et d’entrepôt disponibles dans la version standard de Business Central afin que vous puissiez suivre votre activité.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 'Report_707, Report_716, Report_813, Report_1001, Report_5807, Report_5808, Report_5809, Report_7313, Report_7319, Report_7320'
ms.date: 04/13/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# États et analyses de stock et d’entrepôt

Les états de stock et d’entrepôt dans [!INCLUDE [prod_short](includes/prod_short.md)] permettent aux professionnels des stocks et des affaires d’obtenir des informations et des statistiques sur les activités de stock et d’entrepôt actuelles et passées.  

## États

[!INCLUDE [inventory_WMS_reports](includes/inventory-WMS-reports-include.md)]

## Tâches

Les articles suivants décrivent certaines des tâches clés pour analyser l’état de votre entreprise :

* [Création d’états d’analyse](bi-how-create-analysis-views-reports.md)  
* [Afficher la disponibilité des articles](inventory-how-availability-overview.md)

## Imprimer et scanner des codes-barres

L’utilisation de codes-barres peut vous aider à simplifier vos processus d’entrepôt entrants, sortants et internes. 

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Après avoir installé l’application, vous pouvez utiliser l’action **Imprimer l’étiquette** pour imprimer des codes-barres 1D et 2D à partir des pages répertoriées dans le tableau suivant.

|Page  |Les valeurs des champs que les codes-barres peuvent inclure  |
|---------|---------|
|Articles, Fiche article     |N° article, description et GTIN         |
|Liste de référence d’article, référence d’article     |Numéro d’article, description, unité de mesure et numéro de référence.         |
|Liste d’informations sur le numéro de lot, étiquette du numéro de lot     |Numéro d’article, description et numéro de lot       |
|Étiquette NS     |Numéro d’article, description et numéro de série         |

> [!NOTE]
> Certaines imprimantes et formats de codes-barres/QR nécessitent une implémentation spécifique. Vous devrez peut-être télécharger un autre modèle Word ou cloner le rapport pour créer votre propre version personnalisée.

## Voir aussi

[Configuration de stock](inventory-setup-inventory.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
