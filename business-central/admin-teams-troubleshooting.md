---
title: Dépannage de l’intégration de Microsoft Teams
description: Découvrez ce que vous pouvez faire en tant qu’administrateur pour contrôler l’intégration Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 10612a3e5e257969b2daf0839ea0826316a956ee
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046547"
---
# <a name="troubleshooting-microsoft-teams-integration-with-prod_short"></a>Dépannage de l’intégration de Microsoft Teams avec [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Cet article fournit des informations sur la façon d’identifier et de résoudre les problèmes que vous pouvez rencontrer lors de l’utilisation de Microsoft Teams avec[!INCLUDE [prod_short](includes/prod_short.md)], en tant qu’utilisateur ou administrateur typique.

## <a name="none-of-my-links-expand-into-a-card"></a>Aucun de mes liens ne se transforme en fiche 

Si vous rencontrez ce problème, voici quelques choses à essayer :

1. Tout d’abord, assurez-vous que l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams est installée.

    Pour vérifier, connectez-vous à l’application de bureau Teams ou à Teams dans le navigateur. Ensuite, sur le côté gauche, sélectionnez **Applications** et recherchez **[!INCLUDE [prod_short](includes/prod_short.md)]**. Lorsque vous trouvez l’application **[!INCLUDE [prod_short](includes/prod_short.md)]**, sélectionnez-la pour ouvrir la page des détails de l’application. Si le bouton **Ajouter pour moi** s’affiche, alors l’application [!INCLUDE [prod_short](includes/prod_short.md)] n’est pas installée. Pour plus d’informations sur l’installation de l’application, consultez [Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Les utilisateurs invités ne peuvent pas installer immédiatement les applications. Pour plus d’informations sur les utilisateurs invités, consultez notre FAQ sur la collaboration avec les invités. 

2. Ensuite, vérifiez que vous vous êtes connecté avec la bonne identité.

    Dans Teams, accédez à n’importe quelle discussion instantanée et sous la zone de rédaction du message, choisissez l’icône [!INCLUDE [prod_short](includes/prod_short.md)]. Lorsque la fenêtre apparaît, vérifiez si l’utilisateur auquel elle indique que vous êtes connecté correspond à ce que vous utilisez pour vous connecter à [!INCLUDE [prod_short](includes/prod_short.md)].

3. Veillez à ce que le codeunit 2718 **Fournisseur résumé page** soit publié en tant que service web.

    Teams se connecte à [!INCLUDE [prod_short](includes/prod_short.md)] en utilisant un point de terminaison vers ce codeunit sur le service [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations sur la publication des services Web, voir [Publier un service Web](across-how-publish-web-service.md).

4. Votre organisation peut également vous empêcher de coller des liens qui se développent en fiches. Contactez votre administrateur pour comprendre les stratégies d’organisation Teams qui peuvent s’appliquer à vous.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Mon lien ne se développe parfois pas dans une fiche 

Un lien ne se développera pas dans une fiche dans les situations suivantes :

- Le lien cible une page d’un type qui ne représente pas un enregistrement. Par exemple, il peut s’agir d’un lien vers le tableau de bord de [!INCLUDE [prod_short](includes/prod_short.md)]. Vous pouvez vérifier le type de page à l’aide du volet d’inspection de page dans le client Web dans [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations sur l’inspection des pages, voir [Inspection des pages](across-inspect-page.md).
- Le lien cible une page qui (au niveau technique) n’est pas connectée à une table source dans [!INCLUDE [prod_short](includes/prod_short.md)]. Vous pouvez vérifier si une page a une table source à l’aide du volet d’inspection de page dans le client Web dans [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations sur l’inspection des pages, voir [Inspection des pages](across-inspect-page.md). 
- Teams ne prend pas en charge les aperçus de lien dans certaines fonctionnalités. Par exemple, lorsque vous ouvrez une discussion, vous êtes en réunion ou vous êtes invité dans une autre organisation.
- Les équipes abandonnent silencieusement la tentative d’afficher la fiche après 15 secondes, par exemple, en raison de problèmes de réseau.
- Les équipes ne peuvent pas développer le lien si vous avez déjà collé un lien dans la même boîte de rédaction de message et supprimé la fiche.

Le lien doit également contenir toutes les informations nécessaires pour localiser l’enregistrement et afficher la fiche correspondante. Ces informations comprennent :

- Le nom de l’environnement, en l’incluant dans le chemin de l’URL. Si vous ne spécifiez pas le nom de l’environnement, Teams suppose que vous essayez d’atteindre l’environnement nommé « Production ».
- Le nom de l’entreprise, en utilisant le paramètre *company=*
- L’identifiant de la page, en utilisant le paramètre *page=*
- Le signet de l’enregistrement, en utilisant le paramètre *bookmark=*

Par exemple :

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Pour des détails techniques sur les URL [!INCLUDE [prod_short](includes/prod_short.md)], voir [URL du client Web](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) dans l’Aide destinée aux développeurs et aux professionnels de l’informatique [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="the-card-is-displayed-in-the-message-compose-box-but-selecting-the-details-button-does-nothing"></a>La fiche s’affiche dans la zone de rédaction du message, mais la sélection du bouton Détails ne fait rien 

Une fois qu’un lien est développé dans une fiche dans la zone de rédaction du message, vous devez envoyer le message à la discussion instantanée avant de pouvoir utiliser le bouton **Détails**.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a>La fenêtre de détails s’ouvre, mais affiche une erreur avant que les détails ne soient affichés

Ce problème peut être causé par plusieurs facteurs : le manque d’autorisations dans [!INCLUDE [prod_short](includes/prod_short.md)] ou les paramètres du navigateur (lors de l’utilisation de Teams dans le navigateur).

1. Vérifiez vos autorisations dans [!INCLUDE [prod_short](includes/prod_short.md)].

    Pour afficher les détails d’une fiche, [!INCLUDE [prod_short](includes/prod_short.md)] vérifie votre licence et vos autorisations pour afficher cet enregistrement et cette page spécifiques dans l’entreprise et l’environnement spécifiques. Si vous n’êtes pas autorisé pour l’une de ces choses, les messages d’erreur [!INCLUDE [prod_short](includes/prod_short.md)] standard concernant les autorisations apparaissent dans la fenêtre de détails. 

    Pour en savoir plus sur les autorisations, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)

2. Vérifiez les paramètres de votre navigateur si vous utilisez Teams dans le navigateur.

    - Le bloqueur de fenêtres contextuelles de votre navigateur doit être désactivé ou configuré pour autoriser les fenêtres contextuelles depuis les domaines *businesscentral.dynamics.com* ou *bc.dynamics.com*. Pour plus d’informations sur l’autorisation des fenêtres contextuelles pour [!INCLUDE [prod_short](includes/prod_short.md)], voir [Configuration de votre navigateur](across-browser-settings.md#popup).
    - Votre navigateur doit avoir accès au stockage local du navigateur pour les cookies et les préférences pendant que vous travaillez.
    - Évitez d’utiliser la navigation invité ou privée, sauf si nécessaire, car ils rejettent ou bloquent certains contenus dans certains navigateurs.

    Pour plus d’informations sur la configuration minimale requise pour les navigateurs, consultez [Exigences minimales pour l’utilisation de [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams"></a>Je rencontre des problèmes avec la caméra ou l’emplacement dans Teams 

Lors de l’utilisation des fonctionnalités [!INCLUDE [prod_short](includes/prod_short.md)] dans la fenêtre des détails qui nécessitent l’accès à votre emplacement ou à la caméra de votre appareil, vous devez d’abord donner votre consentement pour que Teams puisse accéder à ces fonctionnalités de l’appareil.  

- Pour Teams dans le navigateur, assurez-vous que les paramètres de votre navigateur autorisent l’accès à la caméra et à l’emplacement pour https://teams.microsoft.com. 

- Pour Teams pour iOS ou Android, assurez-vous que les paramètres de votre appareil autorisent l’accès à la caméra et à l’emplacement pour l’application mobile Teams. 

Pour obtenir de l’aide sur la modification de ces paramètres, consultez [Ma caméra ne fonctionne pas dans Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) sur le support Microsoft.

L’application [!INCLUDE [prod_short](includes/prod_short.md)] ne prend pas en charge la localisation dans l’application de bureau Teams. Pour plus d’informations sur l’emplacement, consultez la [FAQ Teams](teams-faq.md#location).

Certains navigateurs, comme le nouveau Microsoft Edge, vous permet de choisir la caméra d’appareil à utiliser lorsque votre appareil prend en charge plusieurs caméras. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>Teams affiche des langues mixtes pour mes fiches et les détails de ma fiche 

Pour que les fiches et les détails des fiches s’affichent de manière cohérente dans la même langue dans Teams, la langue de votre client Teams et la langue que vous utilisez dans le client Web [!INCLUDE [prod_short](includes/prod_short.md)] doit correspondre.

- Pour en savoir plus sur la modification de la langue dans Teams, voir [Modifier les paramètres dans Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) sur le support Microsoft. 

- Pour en savoir plus sur le changement de langue dans [!INCLUDE [prod_short](includes/prod_short.md)], voir [Modifier les paramètres de base - Langue](ui-change-basic-settings.md#language).

Pour plus d’informations sur le fonctionnement des langues entre Teams et [!INCLUDE [prod_short](includes/prod_short.md)], voir [FAQ Teams](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>J’ai modifié un champ dans la fenêtre de détails, mais ma modification n’a pas été enregistrée

Les modifications que vous apportez à un champ dans les fenêtres de détails sont automatiquement enregistrées lorsque vous quittez le champ. Avant de fermer la fenêtre après avoir modifié un champ, assurez-vous d’appuyer sur la touche Tab ou de cliquer/appuyer en dehors du champ.

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de l’intégration [!INCLUDE [prod_short](includes/prod_short.md)] et Microsoft Teams ](across-teams-overview.md)  
[Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)  
[FAQ Teams](teams-faq.md)  
[Développement pour l’intégration de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]