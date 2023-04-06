---
title: "Partage d’enregistrements Business\_Central dans Microsoft Teams"
description: "Découvre comment utiliser l’application Business\_Central pour Microsoft Teams."
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records'
ms.date: 09/22/2022
ms.author: jswymer
---

# Partage d’enregistrements et de liens de page Business Central dans Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] propose plusieurs façons de partager des données Business Central directement dans une conversation Microsoft Teams :

<!-- 
## Overview
In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.
The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:
[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries. In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.

-->
- Une fois l’application [!INCLUDE [prod_short](includes/prod_short.md)] installée dans Teams, vous pouvez inclure une fiche interactive d’enregistrement Business Central dans une conversation Teams.

<!--   Copy a link from any Business Central record, like a customer or sales order, then paste the link into a Teams conversation. The app connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)]. It then expands the link into a compact, interactive card that displays information about the record. Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.

  [![Teams integration with Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)-->

- Avec ou sans l’application [!INCLUDE [prod_short](includes/prod_short.md)] installée, vous pouvez partager un lien entre des pages de Business Central et une conversation Teams.

  <!-- ![!The Share menu displayed on a card.](media/teams-share-link.png "The Share menu displayed on a card.")-->

Les sections suivantes décrivent en détail les différentes méthodes.

## Inclure et afficher une fiche Business Central dans une conversation Teams

Avec l’application Business Central pour Teams, vous pouvez copier un lien à partir de n’importe quel enregistrement Business Central, comme un client ou une commande client, et coller le lien dans une conversation Teams. L’application connecte Microsoft Teams à vos données métier dans [!INCLUDE [prod_short](includes/prod_short.md)]\. Elle développe ensuite le lien en une fiche interactive compacte qui affiche des informations sur l’enregistrement. Une fois dans la conversation, vous et vos collègues pouvez afficher plus de détails sur l’enregistrement, modifier les données et prendre des mesures, sans quitter Teams.

[![Intégration Teams avec Business Central.](media/teams-intro-vBC20.png)](media/teams-intro-vBC20.png#lightbox)

### Conditions préalables

- Vous avez accès à Microsoft Teams.
- Vous avez installé l’application [!INCLUDE [prod_short](includes/prod_short.md)] dans Teams. Pour plus d’informations, voir [Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Tous les participants à une conversation Teams pourront afficher les fiches des enregistrements Business Central que vous soumettez à la conversation. Mais pour afficher plus de détails sur les enregistrements, en utilisant les boutons **Détails** ou **Contextuel** sur une fiche, ils auront besoin d’accéder à [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Gestion de l’intégration Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).

### Inclure une fiche Business Central dans une conversation Teams

1. Connectez-vous à [!INCLUDE [prod_short](includes/prod_short.md)] en utilisant votre navigateur.
2. Ouvrez l’enregistrement que vous souhaitez partager.

    L’application est conçue pour afficher une carte pour presque tous les types de page [!INCLUDE [prod_short](includes/prod_short.md)]. Mais c’est lorsqu’elle est utilisée pour les pages qui affichent un seul enregistrement, tel qu’un article, un client ou une commande client, qu’elle offre la meilleure expérience.
3. Copiez le lien vers la page.

    Vous pouvez copier le lien de deux manières. La manière la plus simple et préférée consiste à sélectionner **Partager** ![Icône Partager dans Business Central](media/share-icon.png) > **Copier le lien**. L’autre manière consiste à copier l’URL entière à partir de la barre d’adresse du navigateur.

    [![Copier l’URL de Business Central à partir du navigateur.](media/teams-copy-link.png)](media/teams-copy-link.png#lightbox)
4. Accédez à Teams et démarrez une conversation, qui peut être une discussion avec une personne, un groupe de personnes ou un canal d’équipe.
5. Collez le lien (URL) dans la zone de message où vous composez un message.

    ![Collez l’URL de Business Central dans Teams.](media/teams-paste-url-v2.png)

    > [!TIP]
    > Si vous recevez un message du type : *Business Central souhaite afficher un aperçu de ce lien.*, cela signifie que l’application Business Central pour Teams n’est pas installée. Pour installer l’application, sélectionnez **Afficher l’aperçu** et suivez les instructions.
6. La première fois que vous collez un lien dans une conversation, vous serez invité à vous connecter à [!INCLUDE [prod_short](includes/prod_short.md)] et à autoriser l’application à récupérer des données. Suivez simplement les instructions à l’écran.

    > [!NOTE]
    > Vous ne devez effectuer cette étape qu’une seule fois.
7. Attendez un moment pendant qu’une fiche soit générée dans la boîte de message.
8. Lorsque la fiche apparaît, examinez attentivement don contenu pour toute information sensible avant d’envoyer le message. Cette étape est importante, car une fois que vous envoyez le message, tous les participants à la conversation peuvent voir la fiche.
9. Si la fiche semble bonne, sélectionnez **Envoyer** pour la soumettre à la conversation.

    > [!TIP]
    > Après l’apparition de la fiche et avant de sélectionner **Envoyer**, vous pouvez supprimer l’URL collée si vous le souhaitez.
10. Pour afficher plus de détails ou apporter des modifications à l’enregistrement montré dans la fiche, sélectionnez **Détails**. Pour plus d’informations, voir la section suivante.

### Afficher les détails de la fiche

Une fois qu’une fiche a été envoyée à une conversation, tous les participants avec les [autorisations appropriées](admin-teams-integration.md#permissions) peuvent sélectionner **Détails** pour ouvrir une fenêtre qui affiche plus d’informations sur l’enregistrement&mdash; et éventuellement apporter des modifications à l’enregistrement. Peu importe que vous soyez celui qui envoie la fiche ou celui qui la reçoit. La fonctionnalité **Détails** est particulièrement utile pour les destinataires, car elle leur fournit rapidement des informations concises et ciblées sur l’enregistrement.

La fenêtre de détails est similaire à ce que vous voyez dans [!INCLUDE [prod_short](includes/prod_short.md)], mais elle se concentre sur la page ou l’enregistrement sur lequel porte la carte. Lorsque vous avez terminé de consulter et d’apporter des modifications, fermez la fenêtre pour revenir à la conversation Teams.

Voici quelques points à garder à l’esprit lorsque vous travaillez avec les détails de la fiche :

- Pour afficher les détails de la fiche, les utilisateurs doivent avoir une autorisation de lecture sur la page et ses données dans [!INCLUDE [prod_short](includes/prod_short.md)]\.
- Les fiches des discussions Teams ne sont pas automatiquement mises à jour en fonction des modifications. Toutes les modifications que vous enregistrez dans un enregistrement dans la fenêtre de détails sont enregistrées dans [!INCLUDE [prod_short](includes/prod_short.md)]\. Mais la fiche dans Teams n’affichera pas les modifications de la conversion tant que vous n’aurez pas recollé le lien.

Pour en savoir plus sur l’utilisation des fiches et des détails de fiche, consultez [FAQ Teams](teams-faq.md).

## <a name="share-link"></a>Partager un lien vers une page entre Business Central et Teams

Directement à partir de la plupart des pages de collection, comme la page **Articles**, et des pages de détails, comme la fiche **Articles**, vous pouvez envoyer un lien vers la page à des destinataires spécifiques dans une conversation Teams. Par exemple, vous pouvez partager un lien vers une vue filtrée de vos enregistrements. Les destinataires peuvent ensuite sélectionner le lien pour ouvrir la page dans [!INCLUDE [prod_short](includes/prod_short.md)]\.

[![!Le menu Partager affiché sur une fiche.](media/teams-share-link-v2.png "Le menu Partager affiché sur une fiche.")](media/teams-share-link-v2.png#lightbox)

### Conditions préalables

- Vous avez accès à Microsoft Teams.
- (Facultatif) Vous avez installé l’application [!INCLUDE [prod_short](includes/prod_short.md)] dans Teams. 

  Une fois l’application installée, les messages que vous envoyez avec le lien incluront également une fiche compacte pour la page. Pour plus d’informations sur l’installation de l’application, consultez [Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md).

### Partager un lien

1. Dans [!INCLUDE [prod_short](includes/prod_short.md)]\, ouvrez la page que vous souhaitez partager.
2. En haut de la page, choisissez l’action ![ !Partager avec d’autres applications sur les pages.](media/share-icon.png) puis **Partager avec Teams**.
3. Si vous y êtes invité, connectez-vous à Teams avec votre nom d’utilisateur et votre mot de passe.
4. Sur la page **Partager avec Teams**, saisissez le nom d’une personne, d’un groupe ou d’un canal auquel vous souhaitez envoyer le message.
5. La zone de message comprendra un lien vers la page. Si l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams est installée, une fiche pour l’enregistrement ou la page lié apparaîtra également dans la boîte de message.

   Ajoutez d’autres informations si vous le souhaitez, puis choisissez **Partager**.
6. Le lien a maintenant été partagé. Si vous voulez aller à la conversation, choisissez **Accéder à Teams**.

## Voir aussi

[Vue d’ensemble de l’intégration de Business Central et Microsoft Teams](across-teams-overview.md)  
[Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)  
[FAQ Teams](teams-faq.md)  
[Recherche de clients, de fournisseurs et autres contacts dans Microsoft Teams](across-search-contacts-teams.md)  
[Modification de la société et d’autres paramètres dans Teams](across-teams-settings.md)  
[Résolution des incidents dans Teams](admin-teams-troubleshooting.md)  
[Développement pour l’intégration de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
