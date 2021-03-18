---
title: Gestion de l’intégration de Microsoft Teams avec Business Central | Microsoft Docs
description: Gérez l’intégration Business Central avec Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 5fc5957695145ad3bbc4225c7c7e18dd7ca0c728
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386314"
---
# <a name="managing-microsoft-teams-integration-with-prod_short"></a>Gestion de l’intégration de Microsoft Teams à [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Cet article fournit un aperçu de ce que vous pouvez faire en tant qu’administrateur pour contrôler l’intégration de Microsoft Teams avec [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="in-microsoft-teams"></a>Dans Microsoft Teams

### <a name="minimum-requirements"></a>Configuration minimale requise

Cette section décrit la configuration minimale requise pour les fonctionnalités de l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour travailler dans Teams.

- Licences requises

    Ce tableau vous donne un aperçu des licences nécessaires pour les fonctionnalités de l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour travailler dans Teams.

    |Quoi|Licence Teams|Licence [!INCLUDE [prod_short](includes/prod_short.md)]|
    |----|---|---|
    |Coller un lien vers un enregistrement [!INCLUDE [prod_short](includes/prod_short.md)] dans une conversation et l’envoyer sous forme de fiche.|![coche](media/check.png "coche")|![coche](media/check.png "coche")|
    |Afficher une fiche d’un enregistrement [!INCLUDE [prod_short](includes/prod_short.md)] dans une conversation.|![coche](media/check.png "coche")||
    |Afficher plus de détails d’une fiche pour un enregistrement [!INCLUDE [prod_short](includes/prod_short.md)] dans une conversation.|![coche](media/check.png "coche")|![coche](media/check.png "coche")|

- Autoriser les aperçus d’URL

    Le paramètre de stratégie **Autoriser les aperçus d’URL** doit être activé. Sinon, une fiche ne peut pas être générée pour les liens [!INCLUDE [prod_short](includes/prod_short.md)] collés dans une conversation Teams. Pour plus d’informations sur ce paramètre, consultez [Gérer les stratégies de messagerie dans Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-prod_short-app-optional"></a>Gestion de l’application [!INCLUDE [prod_short](includes/prod_short.md)] (facultatif)

En tant qu’administrateur Teams, vous pouvez gérer toutes les applications de votre organisation, y compris l’application [!INCLUDE [prod_short](includes/prod_short.md)]. Vous pouvez approuver ou installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour votre organisation, empêcher l’utilisateur d’installer l’application, etc.

Pour plus d’informations, consultez les articles suivants dans la documentation Microsoft Teams :

- [Gérer vos applications dans le centre d’administration Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Gérer les stratégie de configuration des applications dans Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prod_short"></a>Dans [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements"></a>Configuration minimale requise

- Version de [!INCLUDE [prod_short](includes/prod_short.md)] :

    Vague de lancement 2 de 2020 de [!INCLUDE [prod_short](includes/prod_short.md)], mise à jour 17.3 ou ultérieure. L’intégration de Teams n’est prise en charge que pour [!INCLUDE [prod_short](includes/prod_short.md)] en ligne ; pas en local.

- Le codeunit **2718 Fournisseur résumé page** est publié en tant que service web :

    Ce codeunit est publié en tant que service web par défaut. Le codeunit fait partie de l’application système [!INCLUDE [prod_short](includes/prod_short.md)]. Il est utilisé pour obtenir les données de champ pour une page [!INCLUDE [prod_short](includes/prod_short.md)] ajoutée à une conversation Teams. Pour plus d’informations sur la publication des services Web, voir [Publier un service Web](across-how-publish-web-service.md).

- <a name="permissions"></a>Autorisations utilisateur :

    Pour la plupart, les pages et les données que les utilisateurs peuvent afficher et modifier dans une conversation Teams sont contrôlées par leurs autorisations dans [!INCLUDE [prod_short](includes/prod_short.md)].
    
    - Pour coller un lien [!INCLUDE [prod_short](includes/prod_short.md)] dans une conversation Teams et le faire développer dans une fiche, les utilisateurs doivent avoir au moins une autorisation de lecture sur la page et ses données.
    - Une fois qu’une fiche est soumise à une conversation, tout utilisateur participant à cette conversation peut afficher cette fiche sans autorisation de [!INCLUDE [prod_short](includes/prod_short.md)].
    - Pour afficher plus de détails sur une fiche ou ouvrir l’enregistrement dans [!INCLUDE [prod_short](includes/prod_short.md)], les utilisateurs doivent avoir une autorisation de lecture sur la page et ses données.
    - Pour modifier les données, l’utilisateur doit modifier les autorisations.
    
    Pour plus d’informations sur les autorisations, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).

## <a name="managing-privacy-and-compliance"></a>Gestion de la confidentialité et de la conformité 

Microsoft Teams fournit des contrôles étendus pour la conformité et la gestion des données sensibles ou personnellement identifiables&mdash; y compris les données ajoutées aux chats et aux canaux par l’application [!INCLUDE [prod_short](includes/prod_short.md)].

### <a name="understanding-where-prod_short-cards-are-stored"></a>Comprendre où les fiches [!INCLUDE [prod_short](includes/prod_short.md)] sont stockées 

Une fois qu’une fiche est envoyée à une discussion instantanée, la fiche et les champs affichés sur la fiche sont copiés dans Teams. Ces informations sont soumises aux stratégies Teams de votre organisation, telles que les stratégies de conservation des données. Lors de l’affichage des détails de la fiche, aucune des données de la fenêtre de détails n’est stockée dans Teams. Les données restent stockées dans [!INCLUDE [prod_short](includes/prod_short.md)] et ne seront récupérées par Teams que lorsque l’utilisateur choisit d’afficher les détails. 

- Pour en savoir plus sur l’emplacement de stockage de ces données par Teams, consultez [Emplacement des données au format Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Pour en savoir plus sur les stratégies de rétention dans Teams, voir [Stratégies de rétention dans Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Restriction du partage des fiches 

Vous empêchez des utilisateurs ou groupes spécifiques d’envoyer des fiches à des discussions instantanées ou des canaux en définissant des **Aperçus d’URL**. Pour plus d’informations sur ce paramètre, consultez [Gérer les stratégies de messagerie dans Teams](/microsoftteams/messaging-policies-in-teams). 

Vous pouvez également utiliser des barrières d’information pour empêcher des individus ou des groupes de communiquer entre eux. Pour en savoir plus, consultez [Barrières d’information dans Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Les fonctionnalités de prévention de la perte de données dans le centre de sécurité et de conformité Microsoft 365 ne peuvent pas être appliquées spécifiquement aux fiches. Mais ils peuvent être appliqués aux messages de discussion contenant les fiches. Pour suivre les fonctionnalités avancées à venir qui incluent l’activation de DLP pour les fiches, voir [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).

### <a name="responding-to-data-requests"></a>Répondre aux demandes de données

Vous autorisez les membres de l’équipe et les propriétaires d’équipe à supprimer les messages contenant des cartes sensibles en configurant des stratégies de messagerie, telles que : **Les propriétaires peuvent supprimer les messages envoyés** et **Les utilisateurs peuvent supprimer les messages envoyés**. Pour plus d’informations, consultez [Gérer les stratégies de messagerie dans Teams](/microsoftteams/messaging-policies-in-teams).

Les fonctionnalités de recherche de contenu et de conformité à eDiscovery dans le centre de sécurité et de conformité Microsoft 365 ne peuvent pas être appliquées spécifiquement aux fiches. Mais ils peuvent être appliqués aux messages de discussion contenant les fiches. Pour suivre les fonctionnalités de conformité à venir pour les fiches, voir [https://www.microsoft.com/microsoft-365/roadmap?featureid=68875](https://www.microsoft.com/microsoft-365/roadmap?featureid=68875).

Parce que les données de la fiche dans Teams sont une copie des données dans [!INCLUDE [prod_short](includes/prod_short.md)], vous pouvez aussi utiliser les fonctionnalités [!INCLUDE [prod_short](includes/prod_short.md)] pour exporter les données d’un client si demandé. Pour plus d’informations sur la confidentialité dans [!INCLUDE [prod_short](includes/prod_short.md)], voir [FAQ sur la confidentialité pour les clients Business Central](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="see-also"></a>Voir aussi
[Vue d’ensemble de l’intégration [!INCLUDE [prod_short](includes/prod_short.md)] et Microsoft Teams ](across-teams-overview.md)  
[Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)  
[FAQ Teams](teams-faq.md)  
[Résolution des incidents dans Teams](admin-teams-troubleshooting.md)  
[Développement pour l’intégration de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]