---
title: "Tâches d'administration dans Business Central | Microsoft Docs"
description: "Certaines tâches dans Business Central requièrent une administration centrale et une configuration. Découvrez quelles sont ces tâches et ce que vous devez faire."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 05/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 93eced90155b9172595561bfc5b80c3c49ca11bc
ms.contentlocale: fr-ch
ms.lasthandoff: 05/15/2018

---
# <a name="administration"></a>Administration
Les tâches d'administration centrale sont généralement effectuées par une fonction dans la société. La portée de ces tâches peut dépendre de la taille de la société et des responsabilités de l'administrateur. Ces tâches sont notamment la synchronisation de bases de données de gestion de file d'attentes de travaux ou d'e-mails, la configuration utilisateur, la personnalisation d'interface utilisateur, et la gestion des clés de chiffrement.  

Il est important d'entrer des valeurs de configuration correctes dès le début pour garantir le succès de tout nouveau logiciel de gestion. [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut plusieurs guides de configuration qui vous permettent de configurer les données de base. Pour plus d'informations, voir [Configuration de Business Central](setup.md).

Que vous implémentiez les valeurs de configuration à l'aide de RapidStart Services ou que vous les entriez manuellement dans la nouvelle société, vous pouvez justifier vos choix à l'aide de quelques recommandations générales pour les champs de configuration sélectionnés, susceptibles de rendre la solution inefficace en cas de configuration erronée.  

Un super utilisateur ou un administrateur peut configurer une infrastructure d'échange de données pour permettre aux utilisateurs d'exporter et d'importer des données dans des fichiers de banques ou de salaires, par exemple plusieurs processus de gestion d'espèces.

> [!NOTE]
> Vous pouvez configurer une nouvelle société dans [!INCLUDE[d365fin](includes/d365fin_md.md)] avec RapidStart Services, qui est un outil conçu pour réduire les temps de déploiement, améliorer la qualité de l’implémentation, présenter une approche reproductible des implémentations et augmenter la productivité en automatisant et en simplifiant des tâches récurrentes. Pour plus d'informations, voir ## [Configuration d'une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.   

|**Pour**|**Voir**|  
|------------|-------------|  
|Ajouter des utilisateurs, gérer les autorisations et les accès aux données et affecter des rôles.|[Comprendre les profils et les tableaux de bord](admin-users-profiles-roles.md)|  
|Affecter des autorisations aux utilisateurs, modifier les ensembles d'autorisations, et grouper les utilisateurs par autorisations.|[Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md)|
|Classer la sensibilité des données des champs afin de pouvoir répondre aux demandes des sujets des données concernant leurs données personnelles.|[Classification de la sensibilité des données](admin-classifying-data-sensitivity.md)|
|Répondre aux demandes des sujets des données concernant leurs données personnelles.|[Réponse aux demandes relatives aux données personnelles](admin-responding-to-requests-about-personal-data.md)|
|Configurer un nouveau centre de profit à l'aide de modèles|[Création de sociétés](about-new-company.md)|
|Modifiez les champs et les actions affichés dans l'interface utilisateur pour correspondre aux processus entreprise de votre société. |[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md) |
|Suivre les modifications directes des données effectuées par les utilisateurs dans la base de données pour identifier l'origine des erreurs et les modifications de données.|[Journalisation des modifications](across-log-changes.md)|  
|Entrer des demandes ponctuelles ou récurrentes pour exécuter des états ou des codeunits.|[Utilisation des files d'attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)|  
|Gérer, supprimer ou compresser des documents|[Suppression de documents](admin-manage-documents.md)|  
|Afficher des pages, des codeunits et des requêtes comme des services Web.|[Publication d'un service Web](across-how-publish-web-service.md)|
|Dans le cadre de la création d'applications connectées entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et des solutions tierces via les API REST, définissez des modèles qui sont utilisés pour remplir les propriétés vides d'une entité lorsque vous créez une action POST via une API.|[Configuration des modèles d'API](admin-configuring-api-template.md)|

## <a name="see-also"></a>Voir aussi
[Fonctionnalités d'entreprise](across-business-functionality.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Mise en route](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

