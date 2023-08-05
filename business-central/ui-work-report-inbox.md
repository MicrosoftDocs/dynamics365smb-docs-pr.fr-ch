---
title: Partager et exporter des états avec la boîte de réception état
description: 'Utilisez la page Boîte de réception état pour télécharger, partager et exporter des états dans Business Central.'
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, dataset, export, report inbox, onedrive,'
ms.search.form: 680
ms.date: 08/08/2022
ms.author: a-reishima
---
# Partager et exporter des états avec la boîte de réception état

La page **Boîte de réception état** répertorie les états planifiés générés par l’utilisateur dans [!INCLUDE[prod_short](includes/prod_short.md)], et peut être utilisée non seulement pour accéder aux états générés, mais également pour partager et ouvrir des fichiers dans OneDrive for Business.

> [!TIP]
> Les actions suivantes sont également disponibles dans la partie **Boîte de réception état** dans le tableau de bord. Si la pièce ne s’affiche pas dans votre interface, découvrez comment personnaliser votre tableau de bord ici : [Personnaliser votre espace de travail](ui-personalization-user.md).

## Télécharger les états générés

Pour enregistrer les états précédents, ouvrez la page **Boîte de réception état** en suivant ces étapes :

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Boîte de réception état**, puis choisissez le lien associé.  
2. Sur la page **Boîte de réception état**, choisissez l’état souhaité.

> [!NOTE]
> La page ne répertorie pas les états précédents générés à l’aide de l’action **Imprimer** ou enregistré sous forme de fichier sur le menu **États**.
>
> Les fichiers générés sont enregistrés au format défini lors de la planification de l‘état et peuvent être modifiés sur la page **Écritures de la file d’attente des travaux**, ainsi que la récurrence et d’autres paramètres. Découvrez comment modifier le format du fichier d’état et définir des options supplémentaires sur [Gérer les états récurrents planifiés](ui-work-report.md#manage-scheduled-recurring-reports).

## Ouvrir les états générés dans OneDrive

Pour exporter le fichier d’état vers Microsoft OneDrive for Business, sélectionnez l’état sur la page **Boîte de réception état** et choisissez l’action **Ouvrir dans OneDrive**. L’état est ensuite copié dans le dossier [!INCLUDE[prod_short](includes/prod_short.md)] dans OneDrive et ouvert sur une nouvelle fenêtre de navigateur, où vous pouvez imprimer et gérer le fichier du document.

> [!IMPORTANT]
>
> Les états devant expirer sur la page **Planifier un état** et copié dans OneDrive ne sont pas automatiquement supprimés du dossier partagé.

## Partager les états planifiés

Le partage d’états avec des collaborateurs est également possible sur la page **Boîte de réception état**. Sélectionnez l’état et choisissez l’action **Partager**. Sur la page **Envoyer un lien**, sélectionnez qui peut ouvrir le fichier, définissez les autorisations de modification, puis choisissez **Envoyer** pour envoyer un lien pour accéder au rapport enregistré.

> [!NOTE]
> En apprendre davantage sur l’intégration OneDrive et les fonctionnalités sur [!INCLUDE[prod_short](includes/prod_short.md)], y compris la configuration initiale et les options permettant de gérer les conflits de noms de fichiers, lisez l’article [Ouverture et partage de fichiers dans OneDrive](across-share-onedrive.md).
>
> Utiliser l’action **Partager** rend le fichier d’état généré accessible aux autres utilisateurs uniquement sur OneDrive for Business et ne répertorie pas l’état planifié sur leur **Boîte de réception état**.

## Voir la formation associée sur [Microsoft Learn](/learn/paths/build-reports/).

## Voir aussi

[Exécuter et imprimer des états](ui-work-report.md)  
[États disponibles dans [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Utiliser les états dans le travail quotidien](reports-use-reports.md)  
[Vue d’ensemble de Business Intelligence et Reporting](reports-bi-reporting.md)  
[Paramétrage imprimantes](ui-specify-printer-selection-reports.md)  
[Utiliser les dates civiles et les heures](ui-enter-date-ranges.md)  
[Gestion des présentations d’état et de document](ui-manage-report-layouts.md)  
[Intégration de [!INCLUDE[prod_short](includes/prod_short.md)] et de OneDrive](across-onedrive-overview.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
