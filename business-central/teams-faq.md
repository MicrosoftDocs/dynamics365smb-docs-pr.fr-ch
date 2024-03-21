---
title: FAQ Teams
description: "Obtenez des réponses à certaines questions courantes sur l’utilisation de Teams et de Business\_Central."
author: jswymer
ms.author: jswymer
ms.topic: faq
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors'
ms.date: 09/28/2022
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# FAQ Teams

[!INCLUDE [online_only](includes/online_only.md)]

Cet article répond à certaines des questions que vous pourriez vous poser sur l’utilisation de Microsoft Teams et [!INCLUDE [prod_short](includes/prod_short.md)].

## [Général](#tab/general)

### Comment puis-je me connecter à l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] dans Teams ?

Après avoir installé l’application, vous serez invité à vous connecter la première fois pour utiliser l′application, lorsque vous collez un lien [!INCLUDE [prod_short.md](includes/prod_short.md)] vers le chat Teams ou lorsque vous choisissez l’action **Détails** sur une fiche dans Teams. En fonction de votre client Teams, vous devrez peut-être entrer vos informations d’identification que vous utilisez pour accéder à [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Comment puis-je me déconnecter de l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] dans Teams ?

Pour vous déconnecter de votre identité d’utilisateur actuelle dans Teams utilisé pour vous connecter à [!INCLUDE [prod_short.md](includes/prod_short.md)], accédez à n’importe quelle boîte de composition de discussion instantanée, cliquez avec le bouton droite sur l′icône [!INCLUDE [prod_short.md](includes/prod_short.md)] située en dessous et choisissez **Paramètres**. Lorsque la fenêtre apparaît, vérifiez votre identité actuellement connectée, puis choisissez **Déconnexion**.

### L’application pour Teams se connecte-t-elle à [!INCLUDE [prod_short.md](includes/prod_short.md)] en local ? 

Non. L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams ne fonctionne qu’avec [!INCLUDE [prod_short.md](includes/prod_short.md)] en ligne. Il n’y a pas de plan pour soutenir les types de déploiement [!INCLUDE [prod_short.md](includes/prod_short.md)] &mdash; comme en local, en cloud hybride ou en cloud privé&mdash; que Microsoft n’héberge pas ou ne gère pas directement.

### L’application fonctionne-t-elle avec plusieurs entreprises et environnements ? 

Oui. Pour rechercher des contacts dans une autre entreprise, accédez à [Paramètres](across-teams-settings.md). Quand l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] développe un lien dans une fiche, le lien doit contenir l’environnement et les noms de société pour que l’application corresponde à l’enregistrement de la bonne société. Vous pouvez coller des liens vers les entreprises et les environnements auxquels vous avez accès au sein de votre organisation et à partir du compte [!INCLUDE [prod_short.md](includes/prod_short.md)] que vous avez utilisé pour vous connecter. Les participants à la discussion instantanée verront la fiche. Mais ils ne peuvent pas afficher les détails de la fiche à moins d’avoir des autorisations sur la société ou l’environnement où cet enregistrement est stocké.

### Dans quels pays ou régions l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] est-elle disponible ? 

L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams n’est pas limitée par pays ou région. L’application est disponible sur tous les marchés actuellement pris en charge par le marché Teams. 

### Est-ce que l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] fonctionne avec n’importe quelle localisation de [!INCLUDE [prod_short.md](includes/prod_short.md)] ? 

Oui. L’application est conçue pour fonctionner avec toute localisation de [!INCLUDE [prod_short.md](includes/prod_short.md)], que cette localisation soit proposée directement par Microsoft ou via un partenaire. En savoir plus sur [Disponibilité par pays/région et langues prises en charge](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="language"></a>Avec quelles langues l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] est-elle compatible ?

Deux choses déterminent la langue utilisée pour les fiches et les détails des fiches dans Teams :

1. Votre langue dans Teams, que vous pouvez voir à partir des paramètres de votre compte dans Teams. 
2. Votre langue dans [!INCLUDE [prod_short.md](includes/prod_short.md)], dont vous pouvez voir le [!INCLUDE [prod_short.md](includes/prod_short.md)] client Web (voir [Modifier les paramètres de base - Langue](ui-change-basic-settings.md#language)).

Le tableau suivant explique en quoi l’expérience diffère pour les auteurs et les destinataires des messages, en fonction des paramètres de langue et de la disponibilité des langues.

|Qui|Fiche|Détails de la fiche |
|-|----|--------------| 
|Auteur du message |S’affiche dans la langue spécifiée pour vous dans Teams. Si [!INCLUDE [prod_short.md](includes/prod_short.md)] n’est pas compatible avec la même langue, la fiche est affichée en anglais. |S’affiche dans la langue spécifiée pour vous dans [!INCLUDE [prod_short.md](includes/prod_short.md)], ce qui peut inclure des langues provenant d’applications linguistiques fournies par des partenaires. |
|Destinataire du message |S’affiche dans la langue de l’auteur du message. |S’affiche dans la langue spécifiée pour vous dans [!INCLUDE [prod_short.md](includes/prod_short.md)]. |

Pour la liste des langues prises en charge pour [!INCLUDE [prod_short.md](includes/prod_short.md)], voir [Langues prises en charge](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] fonctionne-t-elle avec les solutions sectorielles ?

Oui. Mais seules certaines fonctionnalités de l′application fonctionnent avec [Incorporer des applications](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) :

- L’application fonctionne avec des liens basés sur le modèle **\*.bc.dynamics.com** généralement utilisé avec Intégrer les applications.
- La recherche de contacts n′est pas disponible pour les applications incorporées qui remplacent l′application de base de Microsoft.

### [!INCLUDE [prod_short.md](includes/prod_short.md)] est-il compatible avec l’application mobile Teams ?

Oui. L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] peut être installée à partir de l’application de bureau ou du navigateur Teams, ou par un administrateur pour tous les utilisateurs. Une fois installé, l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] est automatiquement disponible dans Teams pour iOS et Android. Sur les appareils mobiles, vous ne pouvez afficher que les fiches envoyées par d’autres personnes, accéder aux détails ou afficher la fiche pour profiter pleinement de l’expérience de l’application mobile [!INCLUDE [prod_short.md](includes/prod_short.md)]. Vous ne pouvez pas coller des liens qui se développent dans des fiches lors de la rédaction de messages ou la recherche de contacts. Pour en savoir plus sur la configuration minimale requise pour le mobile, voir [Configuration minimale requise pour l’utilisation de Business Central](product-requirements.md).

### L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams est-elle identique à l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour iOS et Android ?

Non. L’application pour Teams est un complément pour Microsoft Teams et exclusivement conçue pour la collaboration dans Teams. Sinon, l’application mobile [!INCLUDE [prod_short.md](includes/prod_short.md)] offre une expérience riche avec laquelle vous pouvez utiliser les données [!INCLUDE [prod_short.md](includes/prod_short.md)] sur vos appareils mobiles.

Les utilisateurs mobiles sont encouragés à installer à la fois l’application mobile et l’application pour que Teams tire le meilleur parti de [!INCLUDE [prod_short.md](includes/prod_short.md)]. Avec les deux installés, vous pouvez choisir l’action **Ouvrir dans une nouvelle fenêtre** sur une fiche dans Teams pour ouvrir les détails de la fiche dans l’application mobile [!INCLUDE [prod_short.md](includes/prod_short.md)]. Pour en savoir plus sur l’installation de [!INCLUDE [prod_short.md](includes/prod_short.md)] et les applications mobiles Teams, voir :

- [Obtenir Business Central sur votre périphérique mobile](install-mobile-app.md)
- [Télécharger l’application mobile Teams](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) sur le support Microsoft

### L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] est-elle compatible avec tous les clients Teams ?

Non. L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams n’est pas prise en charge lorsqu’elle est installée en tant que package pour macOS ou Linux. Sur ces plates-formes, vous pouvez accéder à Teams à la place à l’aide d’un navigateur pris en charge.

Pour connaître la configuration minimale requise dans [!INCLUDE [prod_short.md](includes/prod_short.md)], voir [Configuration minimale requise pour l’utilisation de Business Central](product-requirements.md#teams).

Pour plus d’informations sur le choix des clients Teams et comment les installer, voir [Obtenir des clients pour Microsoft Teams](/microsoftteams/get-clients) dans la documentation Teams.

### Quel client Teams convient le mieux à [!INCLUDE [prod_short.md](includes/prod_short.md)] ?

Il n’y a que des différences et limitations mineures entre les clients Teams qui peuvent avoir des répercussions sur votre expérience avec l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams. Lors du choix d’un client Teams, tenez compte des éléments suivants :

- La caméra et l’emplacement ne sont pas accessibles à partir de la fenêtre de détails dans l’application de bureau Teams.
- Les numéros de téléphone ne peuvent pas être activés à partir de la fenêtre de détails dans Teams pour iOS, Android ou dans le navigateur.
- En utilisant Microsoft Edge avec Teams dans le navigateur, vous pouvez facilement travailler sur plusieurs identités et comptes en vous connectant à Teams à partir de différents profils. Pour en savoir plus sur l’utilisation des profils dans Microsoft Edge, voir [Se connecter et créer plusieurs profils Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) sur le support Microsoft.

### Quelle est la meilleure façon pour moi de démontrer [!INCLUDE [prod_short.md](includes/prod_short.md)] et Microsoft Teams aux clients potentiels ?

Si vous êtes un partenaire revendeur, vous souhaiterez peut-être disposer d’un environnement dans lequel vous pourrez montrer aux prospects dans le cadre de démonstrations avant-vente. Pour éviter d’affecter Microsoft Teams dans votre organisation, vous pouvez obtenir un compte de démonstration Microsoft 365 sur [https://aka.ms/CDX](https://aka.ms/CDX). Ce compte vous donne le contrôle total d’une organisation Azure indépendante qui comprend Microsoft Teams et [!INCLUDE [prod_short.md](includes/prod_short.md)]. Pour plus d’informations, voir [Préparer les environnements de démonstration de Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams prend-elle en charge ma personnalisation et la personnalisation ?

L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams peut afficher des fiches pour des liens vers des pages client et des tables dans [!INCLUDE [prod_short.md](includes/prod_short.md)], comme les pages et les tables provenant de vos propres extensions personnalisées ou depuis AppSource.

Les champs affichés sur une fiche dans Teams peuvent également être impactés par les personnalisations [!INCLUDE [prod_short.md](includes/prod_short.md)] installées pour votre organisation. Les fiches ne prennent en compte aucune personnalisation spécifique au rôle ni aucune personnalisation utilisateur. Cependant, la fenêtre des détails de la fiche affiche les détails de l’enregistrement tels que vous les verriez dans [!INCLUDE [prod_short.md](includes/prod_short.md)], y compris les extensions, les personnalisations de rôle et la personnalisation de l’utilisateur.

Lorsque vous recherchez des contacts, les champs qui correspondent dans la table **Contacts** et les champs affichés dans les résultats de la recherche ne sont affectés par aucune personnalisation ou personnalisation.

### Comment les autorisations requises par l’application affectent-elles ma confidentialité ?

Avant d’installer l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams, vous pouvez consulter les autorisations minimales requises pour que l’application fonctionne. En installant l’application, vous acceptez que l’application soit autorisée à recevoir les messages et les données que vous lui fournissez, et Teams est autorisé à stocker et à traiter ces messages.

Aussi certaines fonctionnalités [!INCLUDE [prod_short.md](includes/prod_short.md)] nécessitent l’ouverture de liens externes ou l’accès à votre caméra ou à votre emplacement géographique. Supposons que vous vouliez capturer une photo d’une facture d’achat pour la traiter. L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] n’utilise pas ces fonctions sans votre consentement et elles ne sont utilisées que par des fonctionnalités spécifiques de la fenêtre **Détails**. Lorsque vous utilisez l’une de ces fonctionnalités pour la première fois, Teams affiche une boîte de dialogue vous demandant d’accorder l’accès aux fonctionnalités requises de l’appareil.

- Dans le bureau Teams, vous examinez et ajustez les autorisations des applications à partir de la fenêtre **Paramètres**. Sélectionnez votre photo de profil en haut de l’application, sélectionnez **Paramètres** > **Autorisations**, puis sélectionnez l’application [!INCLUDE [prod_short.md](includes/prod_short.md)].

- Pour Teams dans le navigateur et Teams pour iOS ou Android, vous pouvez consulter ou ajuster les autorisations à partir des paramètres de votre navigateur ou de votre appareil.

> [!NOTE]
> Les fonctionnalités [!INCLUDE [prod_short.md](includes/prod_short.md)] qui vous demandent des autorisations dépendent des applications complémentaires et des personnalisations appliquées à l’environnement [!INCLUDE [prod_short.md](includes/prod_short.md)] auquel vous vous connectez.

### Où puis-je en savoir plus sur ma confidentialité ? 

Vous pouvez découvrir comment Microsoft gère vos données dans la [Déclaration de confidentialité Microsoft](https://go.microsoft.com/fwlink/?linkid=2030602). 

Contactez votre administrateur pour savoir comment votre organisation gère la confidentialité de vos données.

### Comment puis-je me déconnecter de l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] dans Teams ?

Pour supprimer l’application que vous avez installée pour vous-même, accédez à n’importe quelle zone de rédaction de discussion instantanée, recherchez l’icône [!INCLUDE [prod_short.md](includes/prod_short.md)] en dessous, cliquez avec le bouton droit sur l’icône et choisissez **Désinstaller**.  

### Microsoft continuera-t-il à améliorer l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams ?

Chez Microsoft, nous écoutons constamment les commentaires de notre communauté diverse d’utilisateurs et prenons les mesures nécessaires pour agir sur les principales propositions de la communauté. Pour en savoir plus sur la prochaine étape pour l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams, consultez le [Plan de versions de Dynamics 365](/dynamics365-release-plan/2021wave1/).

Si vous souhaitez participer à l’amélioration de l’application pour Teams, ou si vous avez une idée qui vous aiderait à simplifier votre travail ou vos expériences collaboratives dans Teams, ajoutez une idée ou votez pour des idées existantes sur [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

### Où puis-je trouver l’intégration Teams dans le client web Business Central ? 

Pour en savoir plus sur les fonctionnalités du client web lié à Teams, consultez la section [Partager des enregistrements et des liens de page dans Microsoft Teams](across-working-with-teams.md#share-link).

## [Onglets Business Central](#tab/tabs)

### <a name="who-can-view"></a>Qui peut voir le contenu d’un onglet ?

Toute personne de votre conversation instantanée ou canal :

1. Doit disposer de l’application Business Central pour Teams installée.
2. Doit être doté d’une licence Business Central ou d’un accès à Business Central octroyé à l’aide de sa licence Microsoft 365.
3. Doit disposer d’autorisations d’afficher les données sur la page.

### <a name=#recommended-content></a>D’où provient le contenu recommandé ?

Le contenu recommandé au sein duquel vous pouvez choisir l’option **Contenu de l’onglet** sur un onglet est basé sur votre tableau de bord. Le contenu recommandé ne comprend que des pages de liste, telles que Clients, Commandes client et Fournisseurs, et non la page de carte individuelle comme un client ou un fournisseur spécifique.

Plus précisément, le contenu recommandé comprend :

- Des actions dans le menu de navigation au-dessus du tableau de bord
- Toutes les pages de liste que vous avez mises en signet.
- Si une page de liste propose différentes vues, y compris les vues que vous avez créées, vous pouvez également choisir parmi ces vues

Vous pouvez ajouter des pages de liste au contenu recommandé en ajoutant des signets. Vous pouvez également supprimer le contenu recommandé en supprimant les signets. Pour savoir comment ajouter ou supprimer des signets, voir [Ajouter un signet à une page ou à un état sur votre tableau de bord](ui-bookmarks.md).

Si vous changez d’environnement ou d’entreprise dans l’option d’onglet, le contenu recommandé sera modifié en fonction du tableau de bord et des signets de l’environnement et de l’entreprise vers lesquels vous basculez.

### Quand je crée un onglet, cela accorde-t-il des autorisations aux personnes du canal ou de la conversation instantanée ?

Non. La création d’onglets n’affecte pas les autorisations et les utilisateurs doivent déjà avoir l’autorisation d’accéder à ces données quand ils accèdent à l’onglet.

### Puis-je discuter à côté d’un onglet ?

Oui. Utilisez l’icône de conversation instantanée pour démarrer la conversation. Ce fil de conversation instantanée est alors associé à l’onglet. 

### Si je supprime un onglet d’une conversation instantanée ou d’un canal, des données Business Central sont-elles supprimées ?

Non.

### Puis-je renommer un onglet en toute sécurité ?

Oui. Le contenu de l’onglet n’est pas lié au nom réel de l’onglet. Renommer à volonté ! 

### J’ai besoin de travailler sur plusieurs tâches dans différentes fenêtres. Puis-je le faire ?

Oui. Vous pouvez faire apparaître l’onglet dans sa propre fenêtre de navigateur pour afficher le client web Business Central. 

### Puis-je ajouter ou épingler un onglet dans les réunions Teams ?

Non. L’application Business Central pour Teams ne prend pas en charge les onglets dans les réunions.

### Impossible d’ajouter un onglet si vous utilisez des URL d’ISV comme *.bc.dynamics.com (mais peut épingler)

Non pris en charge.

### Quand j’effectue des actions dans l’onglet, telles que la navigation, le tri, l’application d’un filtre ou la recherche, les autres utilisateurs voient-ils mes modifications ?

Non. Seules les modifications de champ ou les actions en cours affectent la façon dont les autres voient le contenu de l’onglet.

### Le contenu de l’onglet s’actualise-t-il automatiquement ? Sinon, comment puis-je l’actualiser ?

Le contenu ne s’actualise pas automatiquement, et il n’y a actuellement pas de bouton d’actualisation. La meilleure façon d’actualiser le contenu pour s’assurer qu’il est conforme aux données est de quitter l’onglet, puis de revenir. 

### Cela affiche-t-il les listes et les enregistrements de mes personnalisations et modules complémentaires ?

Oui. 

### Quand j’ajoute un onglet, les utilisateurs le verront-ils dans ma langue ?

Non. Chaque utilisateur affiche le contenu de l’onglet dans les paramètres de langue, de région et de fuseau horaire de Business Central. 

### Puis-je avoir plusieurs onglets pointant vers différents contenus ?

Oui.

### Puis-je également ajouter des onglets pour discuter avec une seule personne ?

Oui, tant que la conversation instantanée n’est pas un brouillon (c’est-à-dire qu’aucun message n’a été envoyé pour lancer cette conversation instantanée) et que l’autre personne a également installé l’application Business Central.

### Puis-je changer d’entreprise dans un onglet ?

Non. 

### Est-ce différent de l’utilisation de la capacité générique de Teams pour créer un onglet qui héberge un site web ?

Oui. Nous ne vous recommandons pas d’utiliser cette approche. Dans de nombreux cas, c’la ne fonctionne pas pour Business Central.

## [Recherche de contacts](#tab/contacts)

### Dans quelles tables l′application recherche-t-elle ?

Lors de la recherche de contacts à partir de l′application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams, vos termes de recherche sont mis en correspondance avec les enregistrements de la table **Contacts** en [!INCLUDE [prod_short.md](includes/prod_short.md)]. 

### Dans quels champs de la table des contacts, puis-je effectuer une recherche ?

Lorsque vous tapez vos termes de recherche dans le champ de recherche, les termes sont mis en correspondance avec la plupart des champs de la table **Contacts**. Les champs incluent, par exemple, les champs **Numéro**, **Nom**, **Adresse**, **N° de téléphone** ou **N° de téléphone portable** et **E-mail**. 

Les termes de recherche ne correspondent à aucun champ personnalisé ajouté à la table **Contacts** par les applications et les extensions.

### Les résultats de recherche incluent-ils des entreprises et des personnes ?

Oui. Dans [!INCLUDE [prod_short.md](includes/prod_short.md)], les contacts peuvent être de type **Société** ou saisissez **Personne**, où une ou plusieurs personnes peuvent être associées à une entreprise. Dans les résultats de recherche, les entreprises et les personnes ont des icônes différentes.

### Les contacts de toute relation d′affaires apparaissent-ils dans les résultats ?

Oui. Certains contacts peuvent représenter des clients ou des fournisseurs, ou les deux. D′autres contacts sans relation d′affaires définie représentent généralement des clients potentiels. Contacts avec d′autres relation d′affaires, y compris les relations personnalisées que vous avez configurées dans [!INCLUDE [prod_short.md](includes/prod_short.md)], sera également affiché dans les résultats de la recherche.

### Puis-je consulter les coordonnées lors des réunions ?

Oui. Vous pouvez rechercher les informations de contact, l′historique des interactions et les documents associés pour votre client ou fournisseur lors d′une réunion Teams ou appeler pendant la réunion, sans quitter Teams.

En fait, vous pouvez rechercher les détails de contact de n′importe où dans Teams à l′aide de la boîte de commande. Vous pouvez, par exemple, rechercher des détails de contact dans le calendrier Teams pour vous aider à configurer des réunions.

### Comment afficher mes dernières interactions avec un contact ?

La fenêtre de détails d′un contact affiche les Écritures journal interaction. Les Écritures journal interaction fournissent l′historique des interactions que votre organisation a eues avec le contact spécifique. Les interactions peuvent inclure des e-mails que vous avez échangés, des appels que vous avez reçus ou des documents que vous avez envoyés.

Pour que les interactions soient affichées, [!INCLUDE [prod_short.md](includes/prod_short.md)] doit être configuré pour suivre les interactions. Pour en savoir plus sur la journalisation des interactions, voir [Enregistrer les interactions avec les contacts](marketing-interactions.md).

### Comment enregistrer un appel ou une réunion Teams en tant qu′interaction ?

Dans la fenêtre des détails d′un contact, recherchez l′action **Créer une interaction** et choisissez parmi les appels entrants ou sortants comme modèles interaction. Vous pouvez également créer vos propres modèles interaction personnalisés spécifiquement pour une utilisation avec les conversations Teams.

### Puis-je appeler un contact de l′application [!INCLUDE [prod_short.md](includes/prod_short.md)] Teams ?

[!INCLUDE [prod_short.md](includes/prod_short.md)] a une intégration limitée aux capacités d′appel Teams. Il n′est pas possible de démarrer instantanément un appel VOIP à partir de la carte de contact ou de la fenêtre des détails du contact. Cependant, lorsque vous affichez les détails du contact dans l′application de bureau Teams, vous pouvez sélectionner le champ de numéro de téléphone pour composer ce numéro si Teams est configuré comme votre application de numérotation par défaut sur votre appareil. Pour composer des numéros de téléphone fixe ou mobile à l′aide du PSTN, le système téléphonique traditionnel, Teams nécessite que vous disposiez de l′application Microsoft 365 Business Voice. Pour en savoir plus, consultez [Qu′est-ce que Microsoft 365 Business Voice ?](/MicrosoftTeams/business-voice/whats-business-voice).

### Comment afficher les documents récents d′un client ou d′un fournisseur ?

[!INCLUDE [prod_short.md](includes/prod_short.md)] associe généralement un contact à un enregistrement client ou fournisseur qui à son tour est lié à des enregistrements de transaction commerciale, tels que des devis ou des factures d′achat. Pour afficher les documents associés à un contact, accédez à la fenêtre de détails du contact, choisissez la valeur de champ **Relation d′affaires** ou utilisez les actions pour accéder au client ou au fournisseur associé. Sur la page du client ou du fournisseur, développez le volet Récapitulatif pour afficher les statistiques de divers documents dans lesquels vous pouvez explorer. Votre expérience peut différer en fonction de vos personnalisations et de votre personnalisation.

### Comment rechercher des contacts à l′aide de caractères spéciaux ?

Vous pouvez entrer des critères de recherche en utilisant presque tous les caractères Unicode. Cependant, [!INCLUDE [prod_short.md](includes/prod_short.md)] réserve les symboles suivants pour d′autres utilisations : **=**, **.**, **\*** et **@**. L′utilisation de ces symboles dans vos termes de recherche peut ne pas donner les résultats escomptés. Si vous ne voyez pas les résultats attendus, placez les symboles dans vos termes de recherche entre guillemets simples, par exemple, **Contoso’=’2**.

### Comment puis-je rechercher des contacts stockés dans une autre entreprise ?

L′application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams peut rechercher des clients, des fournisseurs et d′autres contacts dans une entreprise à la fois.  
Pour rechercher des contacts stockés dans une autre société [!INCLUDE [prod_short.md](includes/prod_short.md)], ouvrez [Paramètres](across-teams-settings.md), puis changez l′environnement et l′entreprise à partir de là.

### Les contacts [!INCLUDE [prod_short.md](includes/prod_short.md)] sont-ils différents de ceux de l′écran des contacts Teams ?

Oui. Contacts stockés dans [!INCLUDE [prod_short.md](includes/prod_short.md)] représentent les contacts professionnels disponibles pour votre organisation. Ce sont des contacts avec lesquels vous avez une relation d′affaires établie et bien définie, ou des contacts qui représentent des clients potentiels. Ces contacts sont généralement des contacts externes. En comparaison, les contacts affichés dans la liste de contacts d′appels Teams sont vos propres contacts. Ces contacts ne sont pas nécessairement partagés avec d′autres membres de votre organisation et représentent généralement des contacts internes à votre organisation.

### [!INCLUDE [prod_short.md](includes/prod_short.md)] synchronise-t-il les contacts avec Teams ?

Non. Contacts stockés dans [!INCLUDE [prod_short.md](includes/prod_short.md)] restent séparés de vos contacts stockés dans Teams.
Il n′est actuellement pas prévu de synchroniser les deux listes ensemble.

### Quelle est la version minimale de [!INCLUDE [prod_short.md](includes/prod_short.md)] pour la recherche de contacts ?

La recherche de contacts nécessite que vous ayez installé l′application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams version 1.0.4 ou ultérieure, et vous vous connectez aux environnements [!INCLUDE [prod_short.md](includes/prod_short.md)] de la version 18 ou ultérieure.

### Puis-je effectuer une recherche à partir de mon appareil mobile ?

La recherche de contacts n′est pas disponible dans Teams pour iOS et Teams pour Android en ce moment.

### De quelles autorisations ai-je besoin pour la recherche de contacts ?

Pour rechercher des contacts, vous devez disposer d′une autorisation au niveau de l′objet sur la table **Contacts** dans la société [!INCLUDE [prod_short.md](includes/prod_short.md)] recherchée. Pour afficher la fenêtre de détails d′un contact, vous devez au moins obtenir une autorisation de lecture sur la page **Contact** dans la société [!INCLUDE [prod_short.md](includes/prod_short.md)] et tout autre objet connexe.

### Puis-je utiliser la recherche de contacts si je suis un administrateur délégué ?

Oui. Vous pouvez également rechercher des contacts et des détails de contact si vous disposez d′un rôle d′administrateur délégué dans une organisation.

### La recherche de contacts est-elle affectée par les limites de l′API ?

Oui. La recherche de contacts dans Teams est basée sur les API [!INCLUDE [prod_short.md](includes/prod_short.md)] v2.0 et soumis à toutes les limites d′API qui gèrent l′utilisation. Vous pouvez en savoir plus sur les limites sur [Limites actuelles de l′API](/dynamics-nav/api-reference/v2.0/dynamics-current-limits).

### Pourquoi me demande-t-il parfois de configurer l′application ?

Après vous être connecté à l′application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams pour la première fois, l′application tentera de déterminer votre entreprise préférée dans [!INCLUDE [prod_short.md](includes/prod_short.md)]. Si l′application ne parvient pas à déterminer l′entreprise, vous devrez peut-être accéder aux **Paramètres** et choisissez l′entreprise dans laquelle vous souhaitez effectuer la recherche. Cette situation se produit, par exemple, si vous avez accès à plusieurs entreprises dans les environnements de votre organisation. Dans ce cas, vous devrez choisir une entreprise avant de pouvoir commencer la recherche.  

L′application peut également vous demander de visiter les **Paramètres** si vous n′avez pas d′abonnement [!INCLUDE [prod_short.md](includes/prod_short.md)], si aucun environnement [!INCLUDE [prod_short.md](includes/prod_short.md)] n′apparaît ou votre compte n′a pas de licence [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Je voudrais rechercher des éléments ou des enregistrements d′autres tables. Puis-je faire cela depuis Teams ?

La recherche dans d′autres tables n′est pas possible pour le moment. L′application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams recherche uniquement dans la liste de contacts [!INCLUDE [prod_short.md](includes/prod_short.md)], qui peut inclure des fournisseurs, des clients et d′autres contacts.

Si vous souhaitez voir les fonctionnalités de recherche évoluer pour inclure d′autres tableaux, nous encourageons notre communauté à ajouter une idée ou à voter pour des idées existantes sur https://aka.ms/BusinessCentralIdeas.

## [Utiliser les fiches](#tab/cards)

### Quels types de liens l’application prend-elle en charge ?

L’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams réagit à la plupart des liens du client Web [!INCLUDE [prod_short.md](includes/prod_short.md)]. Lorsque le lien fait référence à un seul enregistrement sur une page, la fiche affiche les champs de cet enregistrement. Les types de page pris en charge incluent : 

- Pages de fiche, telles que la fiche Article
- Pages de document, telles que le document commande vente
- Pages ListPlus qui représentent un seul enregistrement composé d’autres enregistrements, comme un relevé de rapprochement de compte bancaire
- Pages de liste simples où un enregistrement n’offre pas la possibilité d’accéder à une page de détails distincte, telle que la liste des codes postaux

Lors du collage d’un lien vers l’URL du client Web racine, tel que https://businesscentral.dynamics.com, la fiche affiche plutôt des informations pour aider les nouveaux utilisateurs à commencer à accéder à [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Comment supprimer une fiche que j’ai envoyée dans le cadre d’une discussion instantanée ?

Vous ne pouvez pas supprimer une fiche que vous avez déjà envoyée pour chatter. Mais vous pouvez supprimer l’intégralité du message dont fait partie la fiche.

En tant qu’auteur du message, vous pouvez supprimer tous les messages que vous avez envoyés aux fiches avec une personne, un groupe ou une chaîne&mdash; sauf si votre administrateur a mis en place des stratégies empêchant la suppression des messages. Si vous modérez une chaîne en tant que propriétaire de chaîne, votre administrateur peut également vous avoir autorisé à supprimer tous les messages de la chaîne, y compris les messages envoyés par d’autres utilisateurs.

La suppression d’un message contenant une fiche ne supprime ni n’affecte aucune donnée [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Les fiches affichent-elles toujours des informations à jour ?

Non. Les valeurs de champ sur une carte dans Teams, y compris les images, sont basées sur les données disponibles lorsque cette fiche a été envoyée à la discussion instantanée. Les fiches [!INCLUDE [prod_short.md](includes/prod_short.md)] ne s’actualisent pas automatiquement dans Teams. 

### Pourquoi les fiches n’affichent-elles pas plus d’informations au lieu d’afficher uniquement le nom de la page et le bouton Détails ?

Un administrateur peut avoir configuré l’intégration Teams afin que les fiches n’affichent pas de données sur les enregistrements. Pour plus d’informations, voir [Afficher ou masquer les données d’enregistrement sur les fiches](admin-teams-integration.md#show-or-hide-record-data-on-cards).

### Les autres verront-ils ma fiche s’ils n’ont pas l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams ? 

Lorsque vous rédigez et envoyez un message à la discussion instantanée qui inclut une fiche, tous les utilisateurs verront la fiche,&mdash;même s’ils n’ont pas installé l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams.

### Comment savoir à quelle entreprise appartient une carte dans Teams ?

Si vous travaillez avec des entreprises [!INCLUDE [prod_short.md](includes/prod_short.md)], demandez à votre administrateur d’activer un badge d’entreprise pour chaque entreprise. Lorsqu’il est activé, cet indice voyant apparaît dans n’importe quelle fenêtre de détails dans Teams et affiche la société et l’environnement auxquels appartient l’enregistrement. Pour savoir comment configurer un badge d’entreprise, voir [Afficher un badge d’entreprise](admin-company-information.md#badge).

## [Utiliser les détails de fiche](#tab/carddetails)

### Où se trouve le bouton Enregistrer dans la fenêtre des détails dans Teams ?

[!INCLUDE [prod_short.md](includes/prod_short.md)] enregistre automatiquement les modifications que vous apportez à n’importe quel champ dès que vous quittez le champ. Pour quitter un champ, cliquez/appuyez n’importe où en dehors du champ ou utilisez la touche Tab pour passer au champ suivant. Lorsque les données apparaissent dans une boîte de dialogue de la fenêtre de détails, vous devrez peut-être choisir le bouton **OK** pour que [!INCLUDE [prod_short.md](includes/prod_short.md)] enregistre vos modifications.

### Si je choisis d’afficher les détails d’une fiche, les autres utilisateurs verront-ils ma fenêtre de détails ?

Non. Bien que tous les participants à la discussion instantanée ou une réunion puissent voir la fiche elle-même, la fenêtre de détails n’apparaît que pour vous sur votre appareil lorsque vous choisissez **Détails**. Les autres utilisateurs doivent choisir **Détails** s’ils souhaitent afficher la fenêtre de détails sur leur appareil.

### Puis-je démarrer un appel Teams à partir de la fenêtre de détails dans Teams ?

Oui. Si vous utilisez l′application de bureau Teams, démarrer un appel en choisissant le numéro associé dans un champ de numéro de téléphone, tel que **N° téléphone mobile** sur la fiche **Contact**. Teams doit être votre application de numérotation désignée.

Pour appeler des lignes fixes et des téléphones mobiles locaux ou internationaux, Teams nécessite que vous disposiez d’une licence Business Voice pour les appels d’entreprise. En outre, vous devez configurer Teams comme solution d’appel. Pour en savoir plus, consultez [Planifier votre solution vocale Teams](/microsoftteams/cloud-voice-landing-page) dans la documentation Teams.

### Puis-je imprimer des documents à partir de la fenêtre de détails dans Teams ?

Oui. Vous imprimez des états et d’autres documents à l’aide de la fonctionnalité d’impression [!INCLUDE [prod_short.md](includes/prod_short.md)] standard et toute imprimante compatible cloud configurée sur la page **Gestion des imprimantes** dans [!INCLUDE [prod_short.md](includes/prod_short.md)]. Vous ne pouvez pas imprimer depuis Teams vers des imprimantes locales connues de votre appareil client, telles que des imprimantes sur lesquelles vous imprimez généralement à partir de votre navigateur. Pour cette raison, vous ne pouvez pas imprimer à partir de la fenêtre d’aperçu de l’état, mais uniquement à partir de la page principale de demande de l’état, directement sur vos imprimantes cloud.

Pour plus d’informations sur la configuration des imprimantes cloud, voir [Configurer les imprimantes](ui-specify-printer-selection-reports.md).

### Puis-je accéder à la caméra à partir de la fenêtre de détails dans Teams ?

Oui. Toutes les fonctionnalités [!INCLUDE [prod_short.md](includes/prod_short.md)] de la fenêtre de détails qui utilisent la caméra sont disponibles sur tous les clients Teams.

### <a name="location"></a>Puis-je accéder à mon emplacement depuis la fenêtre de détails dans Teams ?

Si vous utilisez des fonctionnalités dans [!INCLUDE [prod_short.md](includes/prod_short.md)] qui accède à vos coordonnées de localisation actuelles, comme avec des fiches, vous devez utiliser Teams dans le navigateur ou l’application mobile Teams. La localisation n’est pas disponible lors de l’utilisation de l’application de bureau Teams.

### Comment ouvrir les détails dans une nouvelle fenêtre ?

L’affichage de la fenêtre de détails en tant que fenêtre séparée est utile pour le multitâche ou pour pouvoir travailler avec des données d’entreprise tout en pouvant utiliser le chat Teams et d’autres fonctions Teams. Pour ouvrir les détails dans sa propre fenêtre, choisissez **Ouvrir dans le navigateur** dans le menu des points de suspension (**...**) dans le coin supérieur droit de la fenêtre.

## [Collaborer avec les invités](#tab/collaborating)

### Puis-je partager des fiches avec des utilisateurs extérieurs à mon organisation ?

Oui. Lorsque vous rédigez et envoyez un message comprenant une fiche, tous les destinataires de la discussion instantanée verront la fiche&mdash; même s’ils sont invités ou externes à votre organisation. Les invités peuvent également ouvrir la fenêtre des détails s’ils ont reçu l’autorisation d’accéder à ces données dans [!INCLUDE [prod_short.md](includes/prod_short.md)].

### L’expérience est-elle différente pour les utilisateurs qui sont des invités ?

Oui. Inviter des utilisateurs invités extérieurs à votre organisation à participer à une discussion instantanée ou à un canal leur donne une expérience similaire, mais pas identique, par rapport aux utilisateurs de votre organisation. Lorsqu’un invité reçoit un message contenant une fiche, il peut le consulter. Les invités peuvent également ouvrir la page des détails s’ils ont reçu l’autorisation d’accéder à ces données dans [!INCLUDE [prod_short.md](includes/prod_short.md)] et ont une licence [!INCLUDE [prod_short.md](includes/prod_short.md)] attribuée au sein de votre organisation.

Si vous choisissez le lien Détails sur n’importe quelle fiche Business Central, vous serez connecté à l’environnement à partir duquel la fiche a été partagée, en supposant que vous avez l’autorisation d’accéder à l’environnement.

Les utilisateurs invités ne sont pas autorisés à utiliser la recherche de contacts, car elle est liée au locataire d’origine et nous ne prenons actuellement pas en charge un tel scénario de délégation.

Lorsqu’un invité rédige un message, des liens vers son [!INCLUDE [prod_short.md](includes/prod_short.md)] ou le vôtre ne se développeront pas en fiches.

Pour en savoir plus sur les autres similitudes et différences entre les invités et les membres de l’équipe, consultez [Expérience client dans Teams](/MicrosoftTeams/guest-experience) dans la documentation Teams.

### Comment un utilisateur invité installe-t-il l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] ? 

Les invités n’ont pas accès au marché des applications pour installer eux-mêmes des applications. Cependant, l’application peut être automatiquement installée pour eux en fonction des politiques de votre organisation. Une autre façon pour un utilisateur invité d’installer l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] consiste à recevoir un message de discussion instantanée qui comprend une fiche [!INCLUDE [prod_short.md](includes/prod_short.md)]. Dans ce cas, l’utilisateur choisit le bouton **Détails** ou le menu de la fiche, puis installe l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] à utiliser avec votre organisation. Après avoir installé l’application, un utilisateur ne reçoit automatiquement aucune autorisation pour accéder aux données de votre [!INCLUDE [prod_short.md](includes/prod_short.md)].

## [Partager avec Teams](#tab/share)

### Est-ce que Partager avec Teams envoie une carte compacte ? 

Oui. Le lien se développera automatiquement dans une carte si vous avez installé l’application Business Central pour Teams. 

### Les destinataires recevront-ils le message de ma part ou de celle d’un compte de service Business Central ? 

Lorsque vous utilisez Partager avec Teams, le message est envoyé à une personne, un groupe ou un canal, comme si vous aviez envoyé le message vous-même depuis l’intérieur de Microsoft Teams. Les destinataires voient le message de votre part sur leur client Teams préféré et ils peuvent réagir et répondre comme ils le feraient normalement à un message de votre part. 

### Est-ce que Partager avec Teams est disponible dans Business Central sur site ? 

Non. De même manière que l’application [!INCLUDE [prod_short.md](includes/prod_short.md)] pour Teams, cette fonctionnalité est uniquement disponible pour le client web dans [!INCLUDE [prod_short.md](includes/prod_short.md)] en ligne. Il n’y a pas de plans pour soutenir les types de déploiement [!INCLUDE [prod_short.md](includes/prod_short.md)] &mdash; comme en local, cloud hybride ou cloud privé&mdash; que Microsoft n’héberge pas ou ne gère pas directement.

### Est-ce que Partager avec teams accorde des autorisations aux destinataires ? 

Non. Lorsque vous partagez avec une personne, un groupe ou un canal, les autorisations ne sont pas affectées. Les utilisateurs qui ont déjà l’autorisation d’afficher la page et les données ciblées par le lien peuvent le faire. Pour les utilisateurs qui n’ont pas l’autorisation d’afficher cette page et ces données, ou qui n’ont pas de licence [!INCLUDE [prod_short.md](includes/prod_short.md)], un message d’erreur s’affiche. 
 
### Dois-je installer l’application de bureau Teams pour utiliser Partager avec Teams ? 

Non. Tout ce dont vous avez besoin est un compte valide qui a accès à Microsoft Teams. 

### Est-ce que Partager avec Teams est disponible dans tous les clients Business Central ? 

À l’heure actuelle, Partager avec Teams est disponible dans le client Web de bureau, dans la fenêtre de détails de Teams et lors de l’ouverture d’une page dans une nouvelle fenêtre à partir du complément Outlook.

### Où puis-je trouver Partager avec Teams dans Business Central ? 

L’action **Partager avec Teams** se trouve dans le menu **Partager** de toutes les pages, telles que les pages de fiche et de document, les pages de liste ou de feuille de calcul, y compris les pages personnalisées. L’action n’est pas disponible dans les boîtes de dialogue ou les pages affichées comme boîtes de dialogue, telles que les pages de recherche ou les assistants.

---
## Voir aussi

[Vue d’ensemble de l’intégration [!INCLUDE [prod_short](includes/prod_short.md)] et Microsoft Teams ](across-teams-overview.md)  
[Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)  
[Recherche de clients, de fournisseurs et autres contacts dans Microsoft Teams](across-search-contacts-teams.md)  
[Partager des enregistrements dans Microsoft Teams](across-working-with-teams.md)  
[Résolution des incidents dans Teams](admin-teams-troubleshooting.md)  
[Modification de la société et d’autres paramètres dans Teams](across-teams-settings.md)  
[Développement pour l’intégration de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
