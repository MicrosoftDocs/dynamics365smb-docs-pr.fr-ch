---
title: Tâches d’administration dans Business Central | Microsoft Docs
description: Certaines tâches dans Business Central requièrent une administration centrale et une configuration. Découvrez quelles sont ces tâches et ce que vous devez faire.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 60c8af071a4249d55cc92e5c5663ae10e6053d18
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385664"
---
# <a name="administration"></a>Administration

Les tâches d’administration centrale sont généralement effectuées par une fonction dans la société. La portée de ces tâches peut dépendre de la taille de la société et des responsabilités de l’administrateur. Ces tâches sont notamment la gestion de la synchronisation de la base de données des files projets et messages, la configuration des utilisateurs et la personnalisation de l’interface utilisateur.  

Il est important d’entrer des valeurs de configuration correctes dès le début pour garantir le succès de tout nouveau logiciel de gestion. [!INCLUDE[prod_short](includes/prod_short.md)] inclut plusieurs guides de configuration qui vous permettent de configurer les données de base. Pour plus d’informations, voir [Configuration de Business Central](setup.md).

Que vous implémentiez les valeurs de configuration à l’aide de RapidStart Services ou que vous les entriez manuellement dans la nouvelle société, vous pouvez justifier vos choix à l’aide de quelques recommandations générales pour les champs de configuration sélectionnés, susceptibles de rendre la solution inefficace en cas de configuration erronée.  

Un super utilisateur ou un administrateur peut configurer une infrastructure d’échange de données pour permettre aux utilisateurs d’exporter et d’importer des données dans des fichiers de banques ou de salaires, par exemple plusieurs processus de gestion d’espèces. Pour plus d’informations, voir [Échanger des données par voir électronique](across-data-exchange.md).

> [!NOTE]
> Vous pouvez configurer une nouvelle société dans [!INCLUDE[prod_short](includes/prod_short.md)] avec RapidStart Services, qui est un outil conçu pour réduire les temps de déploiement, améliorer la qualité de l’implémentation, présenter une approche reproductible des implémentations et augmenter la productivité en automatisant et en simplifiant des tâches récurrentes. Pour plus d’informations, voir [Configuration d’une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|  
|Définir qui peut se connecter à [!INCLUDE[prod_short](includes/prod_short.md)] en créant des utilisateurs dans le Centre d’administration Microsoft 365 en fonction des licences du produit.|[Créer des utilisateurs en fonction des licences](ui-how-users-permissions.md)|
|Affecter des autorisations aux utilisateurs, modifier les ensembles d’autorisations, et grouper les utilisateurs pour faciliter la gestion des autorisations.|[Attribuer des autorisations aux utilisateurs et aux groupes](ui-how-users-permissions.md)|
|Ajouter des utilisateurs, gérer les autorisations et les accès aux données et affecter des rôles.|[Gérer les profils](admin-users-profiles-roles.md)|
|Gérez les paramètres utilisateur, tels que la société, le rôle, la langue, la région et le fuseau horaire.|[Paramètres utilisateur](admin-manage-user-settings-preferences.md)|
|Configurez les imprimantes et indiquez les états à imprimer sur des imprimantes spécifiques.|[Paramétrage imprimantes](ui-specify-printer-selection-reports.md)|
|Classer la sensibilité des données des champs afin de pouvoir répondre aux demandes des sujets des données concernant leurs données personnelles.|[Classification de la sensibilité des données](admin-classifying-data-sensitivity.md)|
|Répondre aux demandes des sujets des données concernant leurs données personnelles.|[Réponse aux demandes relatives aux données personnelles](admin-responding-to-requests-about-personal-data.md)|
|Configurer un nouveau centre de profit à l’aide de modèles|[Création de sociétés](about-new-company.md)|
|Suivre les modifications directes des données effectuées par les utilisateurs dans la base de données pour identifier l’origine des erreurs et les modifications de données.|[Journalisation des modifications](across-log-changes.md)|  
|Entrer des demandes ponctuelles ou récurrentes pour exécuter des états ou des codeunits.|[Utilisation des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)|  
|Gérer, supprimer ou compresser des documents|[Suppression de documents](admin-manage-documents.md)|  
|Afficher des pages, des codeunits et des requêtes comme des services Web.|[Publication d’un service Web](across-how-publish-web-service.md)|
|Dans le cadre de la création de Connect Apps entre [!INCLUDE[prod_short](includes/prod_short.md)] et des solutions tierces via les API REST, définissez des modèles qui sont utilisés pour remplir les propriétés vides d’une entité lorsque vous créez une action POST via une API.|[Configuration des modèles d’API](admin-configuring-api-template.md)|
|Chiffrez des données sur [!INCLUDE[prod_short](includes/prod_short.md)] Server en générant de nouvelles clés ou en important des clés existantes que vous activez sur le serveur.|[Gestion du chiffrement des données](admin-manage-data-encryption.md)|
|Connectez Dynamics 365 Sales à [!INCLUDE[prod_short](includes/prod_short.md)] pour obtenir l’intégration transparente entre les relations client et le traitement des commandes dans le processus allant du prospect à l’encaissement.|[Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Modifier les champs et les actions affichés dans l’interface utilisateur pour correspondre aux processus entreprise de votre société et étendre la solution avec des applications.|[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|
|Surveillez l’utilisation et dépannez les sessions.|[Télémétrie des environnements dans le centre d’administration de Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Gérez les sessions utilisateur, y compris l’annulation d’une session si l’utilisateur est bloqué.|[Gérer les sessions](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions)|  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Voir aussi

[Fonctionnalités d’entreprise](across-business-functionality.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Mise en route](product-get-started.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]