---
title: FAQ Teams
description: Obtenez des réponses à certaines questions courantes sur l’utilisation de Teams et de Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors
ms.date: 03/04/2021
ms.author: jswymer
ms.openlocfilehash: d95e97a232cfb7fda8f40f68875b747723abbd4b
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573391"
---
# <a name="teams-faq"></a>FAQ Teams

[!INCLUDE [online_only](includes/online_only.md)]

Cet article répond à certaines des questions que vous pourriez vous poser sur l’utilisation de Teams et [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[Général](#tab/general)

### <a name="how-do-i-sign-in-to-the-prod_shortmd-app-in-teams"></a>Comment puis-je me connecter à l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] dans Teams ? 

Après avoir installé l’application, vous serez invité à vous connecter la première fois que vous collez un lien [!INCLUDE [prod_short.md](includes/prod_short.md)] vers le chat Teams ou lorsque vous choisissez l’action **Détails** sur une fiche dans Teams. En fonction de votre client Teams, vous devrez peut-être entrer vos informations d’identification que vous utilisez pour accéder à [!INCLUDE [prod_short.md](includes/prod_short.md)]. 

### <a name="how-do-i-sign-out-of-the-prod_shortmd-app-in-teams"></a>Comment puis-je me déconnecter de l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] dans Teams ? 

Pour vous déconnecter de votre identité d’utilisateur actuelle dans Teams utilisé pour vous connecter à [!INCLUDE [prod_short.md](includes/prod_short.md)], accédez à n’importe quelle boîte de composition de discussion instantanée et choisissez l’icône [!INCLUDE [prod_short.md](includes/prod_short.md)] en dessous. Lorsque la fenêtre apparaît, vérifiez votre identité actuellement connectée, puis choisissez **Déconnexion**. Si vous utilisez Teams dans le navigateur, vous serez également déconnecté de tout client Web [!INCLUDE [prod_short.md](includes/prod_short.md)] dans la même fenêtre de navigateur.

### <a name="does-the-app-for-teams-connect-to-prod_shortmd-on-premises"></a>L’application pour Teams se connecte-t-elle à [!INCLUDE [prod_short.md](includes/prod_short.md)] en local ? 

Non. L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams ne fonctionne qu’avec [!INCLUDE [prod_short.md](includes/prod_short.md)] en ligne. Il n’y a pas de plans pour soutenir les types de déploiement [!INCLUDE [prod_short.md](includes/prod_short.md)] &mdash; comme en local, cloud hybride ou cloud privé&mdash; que Microsoft n’héberge pas ou ne gère pas directement.

### <a name="does-the-app-work-with-multiple-companies-and-environments"></a>L’application fonctionne-t-elle avec plusieurs entreprises et environnements ? 

Oui. Quand l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] développe un lien dans une fiche, le lien doit contenir l’environnement et les noms de société pour que l’application corresponde à l’enregistrement de la bonne société. Vous pouvez coller des liens vers les entreprises et les environnements auxquels vous avez accès au sein de votre organisation et à partir du compte [!INCLUDE [prod_short.md](includes/prod_short.md)] que vous avez utilisé pour vous connecter. Les participants à la discussion instantanée verront la fiche. Mais ils ne peuvent pas afficher les détails de la fiche à moins d’avoir des autorisations sur la société ou l’environnement où cet enregistrement est stocké.

### <a name="in-which-countries-or-regions-is-the-prod_shortmd-app-available"></a>Dans quels pays ou régions l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] est-elle disponible ? 

L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams n’est pas limitée par pays ou région. L’application est disponible sur tous les marchés actuellement pris en charge par le marché Teams. 

### <a name="does-the-prod_shortmd-app-work-with-any-localization-of-prod_shortmd"></a>Est-ce que l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] fonctionne avec n’importe quelle localisation de [!INCLUDE [prod_short.md](includes/prod_short.md)] ? 

Oui. L’application est conçue pour fonctionner avec toute localisation de [!INCLUDE [prod_short.md](includes/prod_short.md)], que cette localisation soit proposée directement par Microsoft ou via un partenaire. Pour plus d’informations, voir [Disponibilité par pays/région et langues prises en charge](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="which-languages-does-the-prod_shortmd-app-support"></a><a name="language"></a>Avec quelles langues l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] est-elle compatible ?

Deux choses déterminent la langue utilisée pour les fiches et les détails des fiches dans Teams :

1. Votre langue dans Teams, que vous pouvez voir à partir des paramètres de votre compte dans Teams. 
2. Votre langue dans [!INCLUDE [prod_short.md](includes/prod_short.md)], dont vous pouvez voir le [!INCLUDE [prod_short.md](includes/prod_short.md)] client Web (voir [Modifier les paramètres de base - Langue](ui-change-basic-settings.md#language)).

Le tableau suivant explique en quoi l’expérience diffère pour les auteurs et les destinataires des messages, en fonction des paramètres de langue et de la disponibilité des langues.

|Qui|Fiche|Détails de la fiche |
|-|----|--------------| 
|Auteur du message |S’affiche dans la langue spécifiée pour vous dans Teams. Si [!INCLUDE [prod_short.md](includes/prod_short.md)] n’est pas compatible avec la même langue, la fiche est affichée en anglais. |S’affiche dans la langue spécifiée pour vous dans [!INCLUDE [prod_short.md](includes/prod_short.md)].  laquelle peut inclure des langues issues d’applications linguistiques fournies par des partenaires. |
|Destinataire du message |S’affiche dans la langue de l’auteur du message. |S’affiche dans la langue spécifiée pour vous dans [!INCLUDE [prod_short.md](includes/prod_short.md)]. |

Pour la liste des langues prises en charge pour [!INCLUDE [prod_short.md](includes/prod_short.md)], voir [Langues prises en charge](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### <a name="does-the-business-central-app-work-with-industry-solutions"></a>L’application Business Central fonctionne-t-elle avec les solutions sectorielles ?

Oui. L’application fonctionne avec des liens basés sur le modèle **\*.bc.dynamics.com** généralement utilisé avec [Intégrer les applications](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview).

### <a name="where-can-i-find-teams-integration-inside-the-prod_shortmd-web-client"></a>Où puis-je trouver l’intégration Teams dans le client Web [!INCLUDE [prod_short.md](includes/prod_short.md)] ? 

Il n’y a actuellement aucune intégration des contrôles Teams ou présence de fonctionnalités Teams dans le client Web [!INCLUDE [prod_short.md](includes/prod_short.md)] ou autres clients.

### <a name="does-prod_shortmd-work-with-the-teams-mobile-app"></a>[!INCLUDE [prod_short.md](includes/prod_short.md)] est-il compatible avec l’application mobile Teams ?

Oui. L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] peut être installée à partir de l’application de bureau ou du navigateur Teams, ou par un administrateur pour tous les utilisateurs. Une fois installé, l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] est automatiquement disponible dans Teams pour iOS et Android. Sur les appareils mobiles, vous pouvez afficher les fiches envoyées par d’autres personnes, accéder aux détails ou afficher la fiche pour profiter pleinement de l’expérience de l’application mobile [!INCLUDE [prod_short.md](includes/prod_short.md)]. Cependant, vous ne pouvez pas coller des liens qui se développent dans des fiches lors de la rédaction de messages. Pour connaître la configuration minimale requise pour le mobile, consultez [Configuration minimale requise pour l’utilisation de Business Central](product-requirements.md).

### <a name="is-the-prod_shortmd-app-for-teams-the-same-as-the-prod_shortmd-app-for-ios-and-android"></a>L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams est-elle identique à l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour iOS et Android ?

Non. L’application pour Teams est un complément pour Microsoft Teams et exclusivement conçue pour des expériences collaboratives qui s’illuminent dans Teams. D’autre part, l’application mobile [!INCLUDE [prod_short.md](includes/prod_short.md)] offre une expérience riche avec laquelle vous pouvez utiliser les données [!INCLUDE [prod_short.md](includes/prod_short.md)] sur vos appareils mobiles.

Les utilisateurs mobiles sont encouragés à installer à la fois l’application mobile et l’application pour que Teams tire le meilleur parti de [!INCLUDE [prod_short.md](includes/prod_short.md)]. Avec les deux installés, vous pouvez choisir l’action **Ouvrir dans une nouvelle fenêtre** sur une fiche dans Teams pour ouvrir les détails de la fiche dans l’application mobile [!INCLUDE [prod_short.md](includes/prod_short.md)]. Pour plus d’informations sur l’installation de [!INCLUDE [prod_short.md](includes/prod_short.md)] et les applications mobiles Teams, voir :

- [Obtenir Business Central sur votre périphérique mobile](install-mobile-app.md)
- [Télécharger l’application mobile Teams](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) sur le support Microsoft

### <a name="does-the-prod_shortmd-app-work-in-all-teams-clients"></a>L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] est-elle compatible avec tous les clients Teams ?

Non. L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams n’est pas prise en charge lorsqu’elle est installée en tant que package pour macOS ou Linux. Sur ces plates-formes, vous pouvez accéder à Teams à la place à l’aide d’un navigateur pris en charge.

Pour connaître la configuration minimale requise dans [!INCLUDE [prod_short.md](includes/prod_short.md)], voir [Configuration minimale requise pour l’utilisation de Business Central](product-requirements.md#teams).

Pour plus d’informations sur le choix des clients Teams et comment les installer, voir [Obtenir des clients pour Microsoft Teams](/microsoftteams/get-clients) dans la documentation Teams.

### <a name="which-teams-client-is-best-for-prod_shortmd"></a>Quel client Teams convient le mieux à [!INCLUDE [prod_short.md](includes/prod_short.md)] ?

Il n’y a que des différences et limitations mineures entre les clients Teams qui peuvent avoir des répercussions sur votre expérience avec l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams. Lors du choix d’un client Teams, tenez compte des éléments suivants :

- La caméra et l’emplacement ne sont pas accessibles à partir de la fenêtre de détails dans l’application de bureau Teams 
- En utilisant Microsoft Edge avec Teams dans le navigateur, vous pouvez facilement travailler sur plusieurs identités et comptes en vous connectant à Teams à partir de différents profils. Pour en savoir plus sur l’utilisation des profils dans Microsoft Edge, voir [Se connecter et créer plusieurs profils Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) sur le support Microsoft.

### <a name="what-is-the-best-way-for-me-to-demonstrate-prod_shortmd-and-microsoft-teams-to-prospective-customers"></a>Quelle est la meilleure façon pour moi de démontrer [!INCLUDE [prod_short.md](includes/prod_short.md)] et Microsoft Teams aux clients potentiels ?

Si vous êtes un partenaire revendeur, vous souhaiterez peut-être disposer d’un environnement dans lequel vous pourrez montrer aux prospects dans le cadre de démonstrations avant-vente. Pour éviter d’affecter Microsoft Teams dans votre organisation, vous pouvez obtenir un compte de démonstration Microsoft 365 sur [https://aka.ms/CDX](https://aka.ms/CDX). Ce compte vous donne le contrôle total d’une organisation Azure indépendante qui comprend Microsoft Teams et [!INCLUDE [prod_short.md](includes/prod_short.md)]. Pour plus d’informations, voir [Préparer les environnements de démonstration de Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### <a name="does-the-prod_shortmd-app-for-teams-cater-for-my-customization-and-personalization"></a>L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams prend-elle en charge ma personnalisation et la personnalisation ?

L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams peut afficher des fiches pour des liens vers des pages client et des tables dans [!INCLUDE [prod_short.md](includes/prod_short.md)], comme les pages et les tables provenant de vos propres extensions personnalisées ou depuis AppSource.

Les champs affichés sur une fiche dans Teams peuvent également être impactés par les personnalisations [!INCLUDE [prod_short.md](includes/prod_short.md)] installées pour votre organisation. Les fiches ne prennent en compte aucune personnalisation spécifique au rôle ni aucune personnalisation utilisateur. Cependant, la fenêtre des détails de la fiche affiche les détails de l’enregistrement tels que vous les verriez dans [!INCLUDE [prod_short.md](includes/prod_short.md)], y compris les extensions, les personnalisations de rôle et la personnalisation de l’utilisateur.

### <a name="how-do-the-permissions-required-by-the-app-affect-my-privacy"></a>Comment les autorisations requises par l’application affectent-elles ma confidentialité ?

Avant d’installer l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams, vous pouvez consulter les autorisations minimales requises pour que l’application fonctionne. En installant l’application, vous acceptez que l’application soit autorisée à recevoir les messages et les données que vous lui fournissez, et Teams est autorisé à stocker et à traiter ces messages.

Aussi certaines fonctionnalités [!INCLUDE [prod_short.md](includes/prod_short.md)] nécessitent l’ouverture de liens externes ou l’accès à votre caméra ou à votre emplacement géographique. Par exemple, supposons que vous vouliez capturer une photo d’une facture d’achat pour la traiter. L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] n’utilise pas ces fonctions sans votre consentement et elles ne sont utilisées que par des fonctionnalités spécifiques de la fenêtre **Détails**. Lorsque vous utilisez l’une de ces fonctionnalités pour la première fois, Teams affiche une boîte de dialogue vous demandant d’accorder l’accès aux fonctionnalités requises de l’appareil.

- Dans le bureau Teams, vous examinez et ajustez les autorisations des applications à partir de la fenêtre **Paramètres**. Sélectionnez votre photo de profil en haut de l’application, sélectionnez **Paramètres** > **Autorisations**, puis sélectionnez l’application [!INCLUDE [prod_short.md](includes/prod_short.md)].

- Pour Teams dans le navigateur et Teams pour iOS ou Android, vous pouvez consulter ou ajuster les autorisations à partir des paramètres de votre navigateur ou de votre appareil.

> [!NOTE]
> Les fonctionnalités [!INCLUDE [prod_short.md](includes/prod_short.md)] qui vous demandent des autorisations dépendent des applications complémentaires et des personnalisations appliquées à l’environnement [!INCLUDE [prod_short.md](includes/prod_short.md)] auquel vous vous connectez.

### <a name="where-can-i-learn-about-my-privacy"></a>Où puis-je en savoir plus sur ma confidentialité ? 

Vous pouvez découvrir comment Microsoft gère vos données dans la [Déclaration de confidentialité Microsoft](https://go.microsoft.com/fwlink/?linkid=2030602). 

Contactez votre administrateur pour savoir comment votre organisation gère la confidentialité de vos données.

### <a name="how-do-i-uninstall-the-prod_shortmd-app-for-teams"></a>Comment puis-je me déconnecter de l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] dans Teams ?

Pour supprimer l’application que vous avez installée pour vous-même, accédez à n’importe quelle zone de rédaction de discussion instantanée, recherchez l’icône [!INCLUDE [prod_short.md](includes/prod_short.md)] en dessous, cliquez avec le bouton droit sur l’icône et choisissez Désinstaller.  

### <a name="will-microsoft-continue-to-improve-the-prod_shortmd-app-for-teams"></a>Microsoft continuera-t-il à améliorer l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams ?

Chez Microsoft, nous écoutons constamment les commentaires de notre communauté diverse d’utilisateurs et prenons les mesures nécessaires pour agir sur les principales propositions de la communauté. Pour en savoir plus sur la prochaine étape pour l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams, consultez le [Plan de version de Dynamics 365](https://aka.ms/dynamics365releaseplan).

Si vous souhaitez participer à l’amélioration de l’application pour Teams, ou si vous avez une excellente idée qui vous aiderait à simplifier votre travail ou vos expériences collaboratives dans Teams, ajoutez une idée ou votez pour des idées existantes sur [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="working-with-cards"></a>[Utiliser les fiches](#tab/cards)

### <a name="which-types-of-links-does-the-app-support"></a>Quels types de liens l’application prend-elle en charge ?

L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams réagit à la plupart des liens du client Web [!INCLUDE [prod_short.md](includes/prod_short.md)]. Lorsque le lien fait référence à un seul enregistrement sur une page, la fiche affiche les champs de cet enregistrement. Les types de page pris en charge incluent : 

- Pages de fiche, telles que la fiche Article
- Pages de document, telles que le document commande vente
- Pages ListPlus qui représentent un seul enregistrement composé d’autres enregistrements, comme un relevé de rapprochement de compte bancaire
- Pages de liste simples où un enregistrement n’offre pas la possibilité d’accéder à une page de détails distincte, telle que la liste des codes postaux

Lors du collage d’un lien vers l’URL du client Web racine, tel que https://businesscentral.dynamics.com, la fiche affiche plutôt des informations pour aider les nouveaux utilisateurs à commencer à accéder à [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="how-do-i-delete-a-card-i-sent-to-a-chat"></a>Comment supprimer une fiche que j’ai envoyée dans le cadre d’une discussion instantanée ? 

Vous ne pouvez pas supprimer une fiche que vous avez déjà envoyée pour chatter. Mais vous pouvez supprimer l’intégralité du message dont fait partie la fiche.

En tant qu’auteur du message, vous pouvez supprimer tous les messages que vous avez envoyés aux fiches avec une personne, un groupe ou une chaîne&mdash; sauf si votre administrateur a mis en place des stratégies empêchant la suppression des messages. Si vous modérez une chaîne en tant que propriétaire de chaîne, votre administrateur peut également vous avoir autorisé à supprimer tous les messages de la chaîne, y compris les messages envoyés par d’autres utilisateurs.

La suppression d’un message contenant une fiche ne supprime ni n’affecte aucune donnée [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="do-cards-always-show-up-to-date-information"></a>Les fiches affichent-elles toujours des informations à jour ?

Non. Les valeurs de champ sur une carte dans Teams, y compris les images, sont basées sur les données disponibles lorsque cette fiche a été envoyée à la discussion instantanée. Les fiches [!INCLUDE [prod_short.md](includes/prod_short.md)] ne s’actualisent pas automatiquement dans Teams. 

### <a name="will-others-see-my-card-if-they-dont-have-the-prod_shortmd-app-for-teams"></a>Les autres verront-ils ma fiche s’ils n’ont pas l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams ? 

Lorsque vous rédigez et envoyez un message à la discussion instantanée qui inclut une fiche, tous les utilisateurs verront la fiche, même s’ils n’ont pas installé l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams.

### <a name="how-do-i-find-out-which-company-a-card-in-teams-belongs-to"></a>Comment savoir à quelle entreprise appartient une carte dans Teams ?

Si vous travaillez avec des entreprises [!INCLUDE [prod_short.md](includes/prod_short.md)], demandez à votre administrateur d’activer un badge d’entreprise pour chaque entreprise. Lorsqu’il est activé, cet indice voyant apparaît dans n’importe quelle fenêtre de détails dans Teams et affiche la société et l’environnement auxquels appartient l’enregistrement. Pour savoir comment configurer le badge d’entreprise, voir [Pour afficher un badge d’entreprise pour un accès rapide aux informations de la société](ui-change-basic-settings.md#badge).

## <a name="working-with-card-details"></a>[Utiliser les détails de la fiche](#tab/carddetails)

### <a name="where-is-the-save-button-in-the-details-window-in-teams"></a>Où se trouve le bouton Enregistrer dans la fenêtre des détails dans Teams ?

[!INCLUDE [prod_short.md](includes/prod_short.md)] enregistre automatiquement les modifications que vous apportez à n’importe quel champ dès que vous quittez le champ. Pour quitter un champ, cliquez/appuyez n’importe où en dehors du champ ou utilisez la touche Tab pour passer au champ suivant. Lorsque les données apparaissent dans une boîte de dialogue de la fenêtre de détails, vous devrez peut-être choisir le bouton **OK** pour que [!INCLUDE [prod_short.md](includes/prod_short.md)] enregistre vos modifications.

### <a name="if-i-choose-to-view-details-for-a-card-will-other-users-see-my-details-window"></a>Si je choisis d’afficher les détails d’une fiche, les autres utilisateurs verront-ils ma fenêtre de détails ?

Non. Bien que tous les participants à la discussion instantanée puissent voir la fiche elle-même, la fenêtre de détails n’apparaît que pour vous sur votre appareil lorsque vous choisissez **Détails**. Les autres utilisateurs doivent choisir **Détails** s’ils souhaitent afficher la fenêtre de détails sur leur appareil.

### <a name="can-i-start-a-teams-call-from-the-details-window-in-teams"></a>Puis-je démarrer un appel Teams à partir de la fenêtre de détails dans Teams ?

Oui. Vous pouvez démarrer un appel en choisissant le numéro de numérotation associé dans un champ de numéro de téléphone, tel que **N° téléphone mobile** sur la fiche **Contact**. Teams doit être votre application de numérotation désignée.

Pour appeler des lignes fixes et des téléphones mobiles locaux ou internationaux à partir de Teams, vous devez disposer d’une licence Teams pour les appels d’entreprise. En outre, vous devez configurer Teams comme solution d’appel. Pour en savoir plus, consultez [Planifier votre solution vocale Teams](/microsoftteams/cloud-voice-landing-page) dans la documentation Teams.

### <a name="can-i-print-documents-from-the-details-window-in-teams"></a>Puis-je imprimer des documents à partir de la fenêtre de détails dans Teams ?

Oui. Vous imprimez des états et d’autres documents à l’aide de la fonctionnalité d’impression [!INCLUDE [prod_short.md](includes/prod_short.md)] standard et toute imprimante compatible cloud configurée sur la page **Gestion des imprimantes** dans [!INCLUDE [prod_short.md](includes/prod_short.md)]. Vous ne pouvez pas imprimer depuis Teams vers des imprimantes locales connues de votre appareil client, telles que des imprimantes sur lesquelles vous imprimez généralement à partir de votre navigateur. Pour cette raison, vous ne pouvez pas imprimer à partir de la fenêtre d’aperçu de l’état, mais uniquement à partir de la page principale de demande de l’état, directement sur vos imprimantes cloud.

Pour plus d’informations sur la configuration des imprimantes cloud, voir [Configurer les imprimantes](ui-specify-printer-selection-reports.md).

### <a name="can-i-access-the-camera-from-the-details-window-in-teams"></a>Puis-je accéder à la caméra à partir de la fenêtre de détails dans Teams ?

Oui. Toutes les fonctionnalités [!INCLUDE [prod_short.md](includes/prod_short.md)] de la fenêtre de détails qui utilisent la caméra sont disponibles sur tous les clients Teams.

### <a name="can-i-access-my-location-from-the-details-window-in-teams"></a><a name="location"></a>Puis-je accéder à mon emplacement depuis la fenêtre de détails dans Teams ?

Si vous utilisez des fonctionnalités dans [!INCLUDE [prod_short.md](includes/prod_short.md)] qui accède à vos coordonnées de localisation actuelles, comme avec des fiches, vous devez utiliser Teams dans le navigateur ou l’application mobile Teams. La localisation n’est pas disponible lors de l’utilisation de l’application de bureau Teams. 

## <a name="collaborating-with-guests"></a>[Collaborer avec les invités ](#tab/collaborating)

### <a name="can-i-share-cards-with-users-outside-my-organization"></a>Puis-je partager des fiches avec des utilisateurs extérieurs à mon organisation ?

Oui. Lorsque vous rédigez et envoyez un message comprenant une fiche, tous les destinataires de la discussion instantanée verront la fiche&mdash; même s’ils sont invités ou externes à votre organisation. Les invités peuvent également ouvrir la fenêtre des détails s’ils ont reçu l’autorisation d’accéder à ces données dans [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="is-the-experience-any-different-for-users-that-are-guests"></a>L’expérience est-elle différente pour les utilisateurs qui sont des invités ?

Oui. Inviter des utilisateurs invités extérieurs à votre organisation à participer à une discussion instantanée ou à un canal leur donne une expérience similaire, mais pas identique, par rapport aux utilisateurs de votre organisation. Lorsqu’un invité reçoit un message contenant une fiche, il peut le consulter. Les invités peuvent également ouvrir la fenêtre des détails s’ils ont reçu l’autorisation d’accéder à ces données dans [!INCLUDE [prod_short.md](includes/prod_short.md)] et assigné une licence [!INCLUDE [prod_short.md](includes/prod_short.md)] au sein de votre organisation. Lorsqu’un invité rédige un message, des liens vers votre [!INCLUDE [prod_short.md](includes/prod_short.md)] ne se développeront pas en fiches.

Pour en savoir plus sur les autres similitudes et différences entre les invités et les membres de l’équipe, voir [Expérience client dans Teams](/MicrosoftTeams/guest-experience) dans la documentation Teams.

### <a name="how-does-a-guest-user-install-the-prod_shortmd-app"></a>Comment un utilisateur invité installe-t-il l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] ? 

Les invités n’ont pas accès au marché des applications pour installer eux-mêmes des applications. Cependant, l’application peut être automatiquement installée pour eux en fonction des politiques de votre organisation. Une autre façon pour un utilisateur invité d’installer l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] consiste à recevoir un message de discussion instantanée qui comprend une fiche [!INCLUDE [prod_short.md](includes/prod_short.md)]. Dans ce cas, l’utilisateur choisit le bouton **Détails** ou le menu de la fiche, puis installe l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] à utiliser avec votre organisation. Après avoir installé l’application, un utilisateur ne reçoit automatiquement aucune autorisation pour accéder aux données de votre [!INCLUDE [prod_short.md](includes/prod_short.md)].

<!--TODO - check with Mike on this -->
---

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de l’intégration [!INCLUDE [prod_short](includes/prod_short.md)] et Microsoft Teams ](across-teams-overview.md)  
[Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)  
[Résolution des incidents dans Teams](admin-teams-troubleshooting.md)  
[Développement pour l’intégration de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]