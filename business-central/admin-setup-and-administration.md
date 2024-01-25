---
title: Tâches administratives dans Business Central
description: Certaines tâches dans Business Central requièrent une administration centrale et une configuration. Découvrez quelles sont ces tâches et ce que vous devez faire.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/11/2023
ms.custom: bap-template
---
# Tâches d’administration

Les tâches d’administration centrale sont généralement effectuées par une fonction dans la société. La portée de ces tâches peut dépendre de la taille de la société et des responsabilités de l'administrateur. Ces tâches sont notamment la gestion de la synchronisation de la base de données des files projets et messages, la configuration des utilisateurs et la personnalisation de l’interface utilisateur.  

Il est important d’entrer des valeurs de configuration correctes dès le début pour garantir le succès de tout nouveau logiciel de gestion. [!INCLUDE[prod_short](includes/prod_short.md)] inclut plusieurs guides de configuration qui vous permettent de configurer les données de base. Pour plus d’informations, voir [Configuration de Business Central](setup.md).

> [!NOTE]
> Utilisez les outils de migration des données pour migrer les données existantes vers [!INCLUDE [prod_short](includes/prod_short.md)] en ligne. Sinon, vous pouvez configurer une nouvelle société dans [!INCLUDE[prod_short](includes/prod_short.md)] avec les packages de configuration pour réduire les temps de déploiement, améliorer la qualité de l’implémentation, présenter une approche reproductible des implémentations et augmenter la productivité en automatisant et en simplifiant les tâches récurrentes. Pour plus d’informations, voir [Migrer des données locales vers Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data).

Vous pouvez justifier vos décisions de configuration à l’aide de recommandations générales pour les champs de configuration sélectionnés connus pour éventuellement entraîner l’inefficacité de la solution en cas de mauvaise définition.  

Un super utilisateur ou un administrateur peut configurer une infrastructure d’échange de données pour permettre aux utilisateurs d’exporter et d’importer des données dans des fichiers de banques ou de salaires, par exemple plusieurs processus de gestion d’espèces. Pour plus d’informations, voir [Échanger des données par voir électronique](across-data-exchange.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les articles qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|
|Définir qui peut se connecter à [!INCLUDE[prod_short](includes/prod_short.md)] en créant des utilisateurs dans le Centre d’administration Microsoft 365 en fonction des licences du produit.|[Créer des utilisateurs en fonction des licences](ui-how-users-permissions.md)|
|Affecter des autorisations aux utilisateurs, modifier les ensembles d’autorisations, et grouper les utilisateurs pour faciliter la gestion des autorisations.|[Attribuer des autorisations aux utilisateurs et aux groupes](ui-how-users-permissions.md)|
|Ajouter des utilisateurs, gérer les autorisations et les accès aux données et affecter des rôles.|[Gérer les profils](admin-users-profiles-roles.md)|
|Gérez les paramètres utilisateur, tels que la société, le rôle, la langue, la région et le fuseau horaire.|[Paramètres utilisateur](admin-manage-user-settings-preferences.md)|
|Configurez les imprimantes et indiquez les états à imprimer sur des imprimantes spécifiques.|[Paramétrage imprimantes](ui-specify-printer-selection-reports.md)|
|Classer la sensibilité des données des champs afin de pouvoir répondre aux demandes des sujets des données concernant leurs données personnelles.|[Classifier la sensibilité des données](admin-classifying-data-sensitivity.md)|
|Répondre aux demandes des sujets des données concernant leurs données personnelles.|[Répondre aux demandes relatives aux données personnelles](admin-responding-to-requests-about-personal-data.md)|
|Configurer un nouveau centre de profit à l’aide de modèles|[Créer de nouvelles sociétés](about-new-company.md)|
|Suivre les modifications directes des données effectuées par les utilisateurs dans la base de données pour identifier l’origine des erreurs et les modifications de données.|[Journalisation des modifications](across-log-changes.md)|  
|Entrer des demandes ponctuelles ou récurrentes pour exécuter des états ou des codeunits.|[Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)|  
|Gérer, supprimer ou compresser des documents|[Supprimer des documents](admin-manage-documents.md)|  
|Afficher des pages, des codeunits et des requêtes comme des services Web.|[Publier un service Web](across-how-publish-web-service.md)|
|Dans le cadre de la création de Connect Apps entre [!INCLUDE[prod_short](includes/prod_short.md)] et des solutions tierces via les API REST, définissez des modèles qui sont utilisés pour remplir les propriétés vides d’une entité lorsque vous créez une action POST via une API.|[Configurer des modèles d’API](admin-configuring-api-template.md)|
|Chiffrez des données sur [!INCLUDE[prod_short](includes/prod_short.md)] Server en générant de nouvelles clés ou en important des clés existantes que vous activez sur le serveur.|[Gérer le chiffrement des données](admin-manage-data-encryption.md)|
|Connectez Dynamics 365 Sales à [!INCLUDE[prod_short](includes/prod_short.md)] pour obtenir l’intégration transparente entre les relations client et le traitement des commandes dans le processus allant du prospect à l’encaissement.|[Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Modifier les champs et les actions affichés dans l’interface utilisateur pour correspondre aux processus entreprise de votre société et étendre la solution avec des applications.|[Personnaliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|

## Administration dans le centre d’administration

Les administrateurs internes et délégués ont accès au centre d’administration [!INCLUDE [prod_short](includes/prod_short.md)] où ils peuvent configurer, surveiller et résoudre les problèmes des environnements [!INCLUDE [prod_short](includes/prod_short.md)]. Le tableau suivant décrit quelques-unes des tâches clés, avec des liens vers les articles qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|
|Découvrir les outils disponibles pour vous aider à résoudre les problèmes.|[Support technique](/dynamics365/business-central/dev-itpro/technical-support)|
|Surveiller l’utilisation et dépanner les sessions|[Télémétrie des environnements dans le centre d’administration de Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Gérez les sessions utilisateur, y compris l’annulation d’une session si l’utilisateur est bloqué.|[Gérer des sessions](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions)|
|Configurer l’abonné pour envoyer les données de télémétrie à Azure Application Insights pour une meilleure analyse et résolution des problèmes.|[Activer l’envoi de télémétrie à Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights)|

## Voir aussi

[Fonctionnalités d’entreprise](across-business-functionality.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
