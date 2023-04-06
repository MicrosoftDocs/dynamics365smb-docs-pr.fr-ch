---
title: Dépannage de l’intégration de Microsoft Teams
description: Découvrez ce que vous pouvez faire en tant qu’administrateur pour contrôler l’intégration Microsoft Teams.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors'
ms.date: 10/01/2021
ms.author: jswymer
---

# Dépannage de l’intégration de Microsoft Teams avec [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Cet article fournit des informations sur la façon d’identifier et de résoudre les problèmes que vous pouvez rencontrer lors de l’utilisation de Microsoft Teams avec[!INCLUDE [prod_short](includes/prod_short.md)], en tant qu’utilisateur ou administrateur typique.

## Le lien de connexion ne fonctionne pas

Si vous essayez de vous connecter à l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams immédiatement après l’installation de l’application et que le lien de connexion ne réagit pas, cela peut être dû au fait que l’application n’a pas complètement terminé l’installation. Pour essayer de résoudre le problème, déconnectez-vous de votre client Teams, puis reconnectez-vous.

## La page Paramètres est vide

Vous devez d’abord vous connecter pour accéder à vos paramètres. Pour vous connecter à l’application, collez un lien vers un enregistrement [!INCLUDE [prod_short.md](includes/prod_short.md)], ou essayez de rechercher des contacts. Ces deux actions vous mèneront à travers une expérience d’inscription, après quoi vous pourrez utiliser la page **Paramètres**.

## J’ai changé d’entreprise, mais ça n’a pas semblé marcher

Après avoir changé d’entreprise sur la page **Paramètres**, vous remarquerez peut-être que la liste déroulante de la boîte de commande indique que vous recherchez toujours la société précédente. Ce problème se produit lorsque vous ouvrez la page **Paramètres** directement à partir de la boîte de commande. Dans ce cas, la société a été modifiée avec succès et vous rechercherez en fait la société vers laquelle vous avez basculé. Le problème est que la liste déroulante de la boîte de commande n’a tout simplement pas encore été mise à jour. Pour que la liste déroulante reflète avec précision l’entreprise dans laquelle vous recherchez, fermez ou détachez [!INCLUDE [prod_short.md](includes/prod_short.md)] à partir de la boîte de commande, puis ouvrez à nouveau l’application.


<!--When you change company from the **Settings** page that you reach from the command box, returning to the command box drop-down continues to show the previous company even though the company was successfully changed. For the drop-down accurately reflect the company you'll search in, you must close or unpin [!INCLUDE [prod_short.md](includes/prod_short.md)] from the command box and then find it again.-->

## Erreur "Une erreur s’est produite" lors de la recherche de contacts

Vous pouvez rencontrer cette erreur lorsque vous recherchez dans une entreprise qui n’a pas été initialisée ou qui ne répond pas. Par exemple, vous ne pouvez pas rechercher dans une nouvelle société d’essai qui n’a pas encore accepté les conditions d’utilisation. Pour résoudre ce problème, essayez de vous connecter au client Web [!INCLUDE [prod_short.md](includes/prod_short.md)], et agissez sur ou fermez toutes les boîtes de dialogue initiales qui apparaissent.

## Erreur « Impossible de trouver l′API de contact/résumé des contacts » lors de la recherche de contacts

Ce problème peut être causé par des personnalisations ou des solutions industrielles qui affectent ou modifient [!INCLUDE [prod_short.md](includes/prod_short.md)], ou qui ne fournissent pas d′API de contact ou de résumé des contacts. Si le problème persiste, contactez l’administrateur ou partenaire d’assistance.

## Aucun de mes liens ne se transforme en fiche 

Si vous rencontrez ce problème, voici quelques choses à essayer :

1. Tout d’abord, assurez-vous que l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams est installée.

    Pour vérifier, connectez-vous à l’application de bureau Teams ou à Teams dans le navigateur. Ensuite, sur le côté gauche, sélectionnez **Applications** et recherchez **[!INCLUDE [prod_short](includes/prod_short.md)]**. Lorsque vous trouvez l’application **[!INCLUDE [prod_short](includes/prod_short.md)]**, sélectionnez-la pour ouvrir la page des détails de l’application. Si le bouton **Ajouter pour moi** s’affiche, alors l’application [!INCLUDE [prod_short](includes/prod_short.md)] n’est pas installée. Pour plus d’informations sur l’installation de l’application, consultez [Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Les utilisateurs invités ne peuvent pas installer immédiatement les applications. Pour plus d’informations sur les utilisateurs invités, consultez notre FAQ sur la collaboration avec les invités. 

2. Ensuite, vérifiez que vous vous êtes connecté avec la bonne identité.

    Dans Teams, accédez à n’importe quelle discussion instantanée et sous la zone de rédaction du message, cliquez avec le bouton droit sur l’icône [!INCLUDE [prod_short](includes/prod_short.md)], puis sur **Paramètres**. Lorsque la fenêtre apparaît, vérifiez si l’utilisateur auquel elle indique que vous êtes connecté correspond à ce que vous utilisez pour vous connecter à [!INCLUDE [prod_short](includes/prod_short.md)].

3. Veillez à ce que le codeunit 2718 **Fournisseur résumé page** soit publié en tant que service web.

    Teams se connecte à [!INCLUDE [prod_short](includes/prod_short.md)] en utilisant un point de terminaison vers ce codeunit sur le service [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations sur la publication des services Web, voir [Publier un service Web](across-how-publish-web-service.md).

4. Votre organisation peut également vous empêcher de coller des liens qui se développent en fiches. Contactez votre administrateur pour comprendre les stratégies d’organisation Teams qui peuvent s’appliquer à vous.

## Mon lien ne se développe parfois pas dans une fiche 

Un lien ne se développera pas dans une fiche dans les situations suivantes :

- Le lien cible une page qui (au niveau technique) n’est pas connectée à une table source dans [!INCLUDE [prod_short](includes/prod_short.md)]. Vous pouvez vérifier si une page a une table source à l’aide du volet d’inspection de page dans le client Web dans [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations sur l’inspection des pages, voir [Inspection des pages](across-inspect-page.md).
- Teams ne prend pas en charge les aperçus de lien dans certaines de ses fonctionnalités. Par exemple, lorsque vous ouvrez une discussion ou vous êtes invité dans une autre organisation.
- Les équipes abandonnent silencieusement la tentative d’afficher la fiche après 15 secondes, par exemple, en raison de problèmes de réseau.
- Les équipes ne peuvent pas développer le lien si vous avez déjà collé un lien dans la même boîte de rédaction de message et supprimé la fiche.

Le lien doit également contenir toutes les informations nécessaires pour localiser l’enregistrement et afficher la fiche correspondante. Ces informations comprennent :

- Le nom de l’environnement, en l’incluant dans le chemin de l’URL. Si vous ne spécifiez pas le nom de l’environnement, Teams suppose que vous essayez d’atteindre l’environnement nommé « Production ».
- Le nom de l’entreprise, en utilisant le paramètre *company=*
- L’identifiant de la page, en utilisant le paramètre*page=*
- Le signet de l’enregistrement, en utilisant le paramètre *bookmark=*

Par exemple :

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Pour des détails techniques sur les URL [!INCLUDE [prod_short](includes/prod_short.md)], voir [URL du client Web](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) dans l’Aide destinée aux développeurs et aux professionnels de l’informatique [!INCLUDE [prod_short](includes/prod_short.md)].

## La fenêtre de détails s’ouvre, mais affiche une erreur avant que les détails ne soient affichés

Ce problème peut être causé par plusieurs facteurs : le manque d’autorisations dans [!INCLUDE [prod_short](includes/prod_short.md)] ou les paramètres du navigateur (lors de l’utilisation de Teams dans le navigateur).

1. Vérifiez vos autorisations dans [!INCLUDE [prod_short](includes/prod_short.md)].

    Pour afficher les détails d’une fiche, [!INCLUDE [prod_short](includes/prod_short.md)] vérifie votre licence et vos autorisations pour afficher cet enregistrement et cette page spécifiques dans l’entreprise et l’environnement spécifiques. Si vous n’êtes pas autorisé pour l’une de ces choses, les messages d’erreur [!INCLUDE [prod_short](includes/prod_short.md)] standard concernant les autorisations apparaissent dans la fenêtre de détails. 

    Pour en savoir plus sur les autorisations, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)

2. Vérifiez les paramètres de votre navigateur si vous utilisez Teams dans le navigateur.

    - Le bloqueur de fenêtres contextuelles de votre navigateur doit être désactivé ou configuré pour autoriser les fenêtres contextuelles depuis les domaines *businesscentral.dynamics.com* ou *bc.dynamics.com*. Pour plus d’informations sur l’autorisation des fenêtres contextuelles pour [!INCLUDE [prod_short](includes/prod_short.md)], voir [Configuration de votre navigateur](across-browser-settings.md#popup).
    - Votre navigateur doit avoir accès au stockage local du navigateur pour les cookies et les préférences pendant que vous travaillez.
    - Évitez d’utiliser la navigation invité ou privée, sauf si nécessaire, car ils rejettent ou bloquent certains contenus dans certains navigateurs.

    Pour plus d’informations sur la configuration minimale requise pour les navigateurs, consultez [Exigences minimales pour l’utilisation de [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## Je rencontre des problèmes avec la caméra ou l’emplacement dans Teams

Lors de l’utilisation des fonctionnalités [!INCLUDE [prod_short](includes/prod_short.md)] dans la fenêtre des détails qui nécessitent l’accès à votre emplacement ou à la caméra de votre appareil, vous devez d’abord donner votre consentement pour que Teams puisse accéder à ces fonctionnalités de l’appareil.  

- Pour Teams dans le navigateur, assurez-vous que les paramètres de votre navigateur autorisent l’accès à la caméra et à l’emplacement pour https://teams.microsoft.com. 

- Pour Teams pour iOS ou Android, assurez-vous que les paramètres de votre appareil autorisent l’accès à la caméra et à l’emplacement pour l’application mobile Teams. 

Pour obtenir de l’aide sur la modification de ces paramètres, consultez [Ma caméra ne fonctionne pas dans Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) sur le support Microsoft.

L’application [!INCLUDE [prod_short](includes/prod_short.md)] ne prend pas en charge la localisation dans l’application de bureau Teams. Pour plus d’informations sur l’emplacement, consultez la [FAQ Teams](teams-faq.md#location).

Certains navigateurs, comme le nouveau Microsoft Edge, vous permet de choisir la caméra d’appareil à utiliser lorsque votre appareil prend en charge plusieurs caméras. 

## Teams affiche des langues mixtes pour mes fiches et les détails de ma fiche

Pour que les fiches et les détails des fiches s’affichent de manière cohérente dans la même langue dans Teams, la langue de votre client Teams et la langue que vous utilisez dans le client Web [!INCLUDE [prod_short](includes/prod_short.md)] doit correspondre.

- Pour en savoir plus sur la modification de la langue dans Teams, voir [Modifier les paramètres dans Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) sur le support Microsoft. 

- Pour en savoir plus sur le changement de langue dans [!INCLUDE [prod_short](includes/prod_short.md)], voir [Modifier les paramètres de base - Langue](ui-change-basic-settings.md#language).

Pour plus d’informations sur le fonctionnement des langues entre Teams et [!INCLUDE [prod_short](includes/prod_short.md)], voir [FAQ Teams](teams-faq.md#language).

## J’ai modifié un champ dans la fenêtre de détails, mais ma modification n’a pas été enregistrée

Les modifications que vous apportez à un champ dans les fenêtres de détails sont automatiquement enregistrées lorsque vous quittez le champ. Avant de fermer la fenêtre après avoir modifié un champ, assurez-vous d’appuyer sur la touche <kbd>Tab</kbd> ou de cliquer/appuyer en dehors du champ.

## Une nouvelle vignette est apparue dans le lanceur d’applications. Comment la supprimer ?

Lorsque vous affichez vos applications sur la page d’accueil Office 365 (https://home.office.com) ou dans le lanceur d’applications, une nouvelle vignette nommée "Connecteur du service d’intégration Teams Business Central" apparaîtra après l’installation de l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams. Cette vignette ne fournit aucune valeur en soi et peut être masquée en toute sécurité.

En tant qu’administrateur, avec des autorisations d’administrateur Azure Active Directory, vous pouvez masquer la vignette en procédant comme suit :

1. Connectez-vous au [centre d’administration Azure Active Directory](https://aad.portal.azure.com/).
2. Sélectionnez **Applications d’entreprise**, puis sélectionnez **Connecteur du service d’intégration Teams Business Central**.
3. Sélectionnez **Propriétés**, puis définissez le bouton bascule **Visible pour les utilisateurs** sur **Non**.
4. Sélectionnez **Enregistrer**.

> [!NOTE]
> Il faudra un certain temps avant que ce changement ne prenne effet.

## Dupliquer du texte dans la fenêtre Partager avec Teams

Lorsque vous collez du texte dans la zone de message de la fenêtre **Partager avec Teams**, le texte est dupliqué. Ce problème est connu de Microsoft et sera résolu dans une mise à jour ultérieure. 

## Impossible de se connecter à la fenêtre Partager avec Teams 

Ce problème peut être causé par diverses raisons. Par exemple, l’identité que vous utilisez pour vous connecter doit avoir accès à Microsoft Teams, par exemple via un abonnement Microsoft 365.

## Mes cartes n’ont plus de bouton de fenêtre contextuelle

À partir d’avril 2022, les liens affichés sous forme de carte compacte dans Teams ne contiendront plus le bouton **Fenêtre contextuelle**. Pour ouvrir la carte dans sa propre fenêtre, choisissez le bouton **Détails**, puis **Ouvrir dans le navigateur** dans le menu des points de suspension (**...**) dans le coin supérieur droit de la fenêtre.

## Impossible d’épingler une carte à l’onglet

Deux raisons expliquent ce problème.

- Si la carte a été partagée à partir de Search ME, elle ne peut pas être épinglée à un onglet. 

- Impossible d’épingler tant que vous n’avez pas ajouté votre premier onglet Business Central. Ce problème est connu dans Teams. 

## Quelqu’un a ajouté un onglet, mais l’onglet ne s’affiche pas pour moi

Ce problème est dû au fait que l’application BC pour Teams n’est pas installée. Seuls ceux qui ont installé l’application verront les onglets Business Central.

## D’autres voient un tri ou une disposition des colonnes différents de ce que voit l’auteur de l’onglet

Ce problème est probablement dû au fait que vous avez partagé une vue de liste qui est une vue personnelle. Dans ce cas, travaillez avec l’administrateur pour créer des vues de liste spécifiques aux rôles qui couvrent les différents rôles dans le canal/la discussion instantanée, ou créez cette vue pour l’ensemble de l’organisation afin que tout le monde puisse obtenir une vue cohérente.


## Voir aussi

[Vue d’ensemble de l’intégration [!INCLUDE [prod_short](includes/prod_short.md)] et Microsoft Teams ](across-teams-overview.md)  
[Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)  
[Recherche de clients, de fournisseurs et autres contacts dans Microsoft Teams](across-search-contacts-teams.md)  
[Partager des enregistrements dans Microsoft Teams](across-working-with-teams.md)  
[FAQ Teams](teams-faq.md)  
[Modification de la société et d’autres paramètres dans Teams](across-teams-settings.md)  
[Développement pour l’intégration de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]