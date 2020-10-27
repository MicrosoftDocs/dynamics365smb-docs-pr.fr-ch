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
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989374"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a>Gestion de l’intégration Microsoft Teams avec Business Central

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

Cet article fournit un aperçu de ce que vous pouvez faire en tant qu’administrateur pour contrôler l’intégration de Microsoft Teams avec [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="in-microsoft-teams"></a>Dans Microsoft Teams

### <a name="minimum-requirements"></a>Configuration minimale requise

Cette section décrit la configuration minimale requise pour les fonctionnalités de l’application [!INCLUDE [prodshort](includes/prodshort.md)] pour travailler dans Teams.

- Licences requises

    Ce tableau vous donne un aperçu des licences nécessaires pour les fonctionnalités de l’application [!INCLUDE [prodshort](includes/prodshort.md)] pour travailler dans Teams.

    |Quoi|Licence Teams|Licence Business Central|
    |----|---|---|
    |Coller un lien vers un enregistrement [!INCLUDE [prodshort](includes/prodshort.md)] dans une conversation et l’envoyer sous forme de fiche.|![coche](media/check.png "coche")|![coche](media/check.png "coche")|
    |Afficher une fiche d’un enregistrement [!INCLUDE [prodshort](includes/prodshort.md)] dans une conversation.|![coche](media/check.png "coche")||
    |Afficher plus de détails d’une fiche pour un enregistrement [!INCLUDE [prodshort](includes/prodshort.md)] dans une conversation.|![coche](media/check.png "coche")|![coche](media/check.png "coche")|

- Autoriser les aperçus d’URL

    Le paramètre de stratégie **Autoriser les aperçus d’URL** doit être activé. Sinon, une fiche ne peut pas être générée pour les liens Business Central collés dans une conversation Teams. Pour plus d’informations sur ce paramètre, consultez [Gérer les stratégies de messagerie dans Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-business-central-app-optional"></a>Gérer l’application Business Central (facultatif)

En tant qu’administrateur Teams, vous pouvez gérer toutes les applications de votre organisation, y compris l’application [!INCLUDE [prodshort](includes/prodshort.md)]. Vous pouvez approuver ou installer l’application [!INCLUDE [prodshort](includes/prodshort.md)] pour votre organisation, empêcher l’utilisateur d’installer l’application, etc.

Pour plus d’informations, consultez les articles suivants dans la documentation Microsoft Teams :

- [Gérer vos applications dans le centre d’administration Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Gérer les stratégie de configuration des applications dans Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a>Dans [!INCLUDE [prodshort](includes/prodshort.md)]

### <a name="minimum-requirements"></a>Configuration minimale requise

- Version de [!INCLUDE [prodshort](includes/prodshort.md)] :

    Vague de lancement 2 de 2020 de [!INCLUDE [prodshort](includes/prodshort.md)] (version 17) ou ultérieure. L’intégration de Teams n’est prise en charge que pour [!INCLUDE [prodshort](includes/prodshort.md)] en ligne ; pas en local.

- Le codeunit **2718 Fournisseur résumé page** est publié en tant que service web :

    Ce codeunit est publié en tant que service web par défaut. Le codeunit fait partie de l’application système [!INCLUDE [prodshort](includes/prodshort.md)]. Il est utilisé pour obtenir les données de champ pour une page [!INCLUDE [prodshort](includes/prodshort.md)] ajoutée à une conversation Teams. 

- Autorisations utilisateur :

    Pour la plupart, les pages et les données que les utilisateurs peuvent afficher et modifier dans une conversation Teams sont contrôlées par leurs autorisations dans [!INCLUDE [prodshort](includes/prodshort.md)].
    
    - Pour coller un lien [!INCLUDE [prodshort](includes/prodshort.md)] dans une conversation Teams et le faire développer dans une fiche, les utilisateurs doivent avoir au moins une autorisation de lecture sur la page et ses données.
    - Une fois qu’une fiche est soumise à une conversation, tout utilisateur participant à cette conversation peut afficher cette fiche sans autorisation de Business Central.
    - Pour afficher plus de détails sur une fiche ou ouvrir l’enregistrement dans [!INCLUDE [prodshort](includes/prodshort.md)], les utilisateurs doivent avoir une autorisation de lecture sur la page et ses données.
    - Pour modifier les données, l’utilisateur doit modifier les autorisations.
    
    Pour plus d’informations sur les autorisations, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).

## <a name="see-also"></a>Voir aussi
[Vue d’ensemble de l’intégration de Business Central et Microsoft Teams](across-teams-overview.md)  
[Installer l’application [!INCLUDE [prodshort](includes/prodshort.md)] pour Microsoft Teams](across-install-app-for-teams.md)  
[Développement pour l’intégration de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Mise en route](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
