---
title: Partage d’enregistrements Business Central dans Microsoft Teams
description: Découvre comment utiliser l’application Business Central pour Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records
ms.date: 05/19/2021
ms.author: jswymer
ms.openlocfilehash: fb134ce04cb6b53f2432f0f371d7ca82411f0cee
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444033"
---
# <a name="sharing-business-central-records-in-microsoft-teams"></a>Partage d’enregistrements Business Central dans Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] propose une application qui connecte Microsoft Teams à vos données métier dans [!INCLUDE [prod_short](includes/prod_short.md)], afin que vous puissiez partager rapidement les détails entre les membres de l’équipe et répondre plus rapidement aux demandes de renseignements. Dans cet article, vous apprendrez à utiliser l’application pour partager des enregistrements [!INCLUDE [prod_short](includes/prod_short.md)], comme un client, une commande client ou une facture, avec des collègues dans une conversation Teams.

## <a name="overview"></a>Aperçu

L’application [!INCLUDE [prod_short](includes/prod_short.md)] vous permet de :

- Copier un lien vers n’importe quel enregistrement Business Central et le coller dans une conversation Teams à partager avec vos collègues. L’application étendra le lien dans une carte interactive compacte qui affiche des informations sur l’enregistrement.
- Une fois dans la conversation, vous et vos collègues pouvez afficher plus de détails sur l’enregistrement, modifier les données et prendre des mesures, sans quitter Teams.

[![Intégration Teams avec Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Conditions préalables

- Vous avez accès à Microsoft Teams.
- Vous avez installé l’application [!INCLUDE [prod_short](includes/prod_short.md)] dans Teams. Pour plus d’informations, voir [Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Tous les participants à une conversation Teams pourront afficher les fiches des enregistrements Business Central que vous soumettez à la conversation. Mais pour afficher plus de détails sur les enregistrements, en utilisant les boutons **Détails** ou **Contextuel** sur une fiche, ils auront besoin d’accéder à [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Gestion de l’intégration Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Inclure une fiche Business Central dans une conversation Teams

1. Connectez-vous à [!INCLUDE [prod_short](includes/prod_short.md)] en utilisant votre navigateur.
2. Ouvrez l’enregistrement que vous souhaitez partager.

    L’application est conçue pour afficher des pages de type fiche à partir de [!INCLUDE [prod_short](includes/prod_short.md)]. Ouvrez une page qui affiche un seul enregistrement, comme un article, un client ou une commande client. Vous ne pouvez pas l’utiliser pour les tableaux de bord ou les pages qui affichent plusieurs enregistrements dans une liste.

3. Copiez l’URL entière de la barre d’adresse du navigateur.

   ![Copiez l’URL de Business Central à partir du navigateur.](media/teams-url-v2.png)
4. Accédez à Teams et démarrez une conversation, qui peut être une discussion avec une personne, un groupe de personnes ou un canal d’équipe.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Collez l’URL dans la zone de message où vous composez un message.

   ![Collez l’URL de Business Central dans Teams.](media/teams-paste-url-v2.png)
6. La première fois que vous collez un lien dans une conversation, vous serez invité à vous connecter à [!INCLUDE [prod_short](includes/prod_short.md)] et à autoriser l’application à récupérer des données. Suivez simplement les instructions à l’écran.

    > [!NOTE]
    > Vous ne devez effectuer cette étape qu’une seule fois.

7. Attendez un moment pendant qu’une fiche soit générée dans la boîte de message.

8. Lorsque la fiche apparaît, examinez attentivement don contenu pour toute information sensible avant d’envoyer le message. Cette étape est importante, car une fois que vous envoyez le message, tous les participants à la conversation peuvent voir la fiche.

9. Si la fiche semble bonne, sélectionnez **Envoyer** pour la soumettre à la conversation.

    > [!TIP]
    > Après l’apparition de la fiche et avant de sélectionner **Envoyer**, vous pouvez supprimer l’URL collée si vous le souhaitez.

10. Pour afficher plus de détails ou apporter des modifications à l’enregistrement montré dans la fiche, sélectionnez **Détails**. Pour plus d’informations, voir la section suivante.

## <a name="view-card-details"></a>Afficher les détails de la fiche

Une fois qu’une fiche a été envoyée à une conversation, tous les participants avec les [autorisations appropriées](admin-teams-integration.md#permissions) peuvent sélectionner **Détails** pour ouvrir une fenêtre qui affiche plus d’informations sur l’enregistrement&mdash; et éventuellement apporter des modifications à l’enregistrement. Peu importe que vous soyez celui qui envoie la fiche ou celui qui la reçoit. La fonctionnalité **Détails** est particulièrement utile pour les destinataires, car elle leur fournit rapidement des informations concises et ciblées sur l’enregistrement, au lieu de devoir scanner l’intégralité de l’enregistrement.

La fenêtre de détails est similaire à ce que vous voyez dans l’enregistrement [!INCLUDE [prod_short](includes/prod_short.md)]. Mais elle est légèrement rognée pour Teams. Lorsque vous avez terminé de consulter et d’apporter des modifications, fermez la fenêtre pour revenir à la conversation Teams.

Voici quelques points à garder à l’esprit lorsque vous travaillez avec les détails de la fiche :

- Pour afficher les détails de la fiche, les utilisateurs doivent avoir une autorisation de lecture sur la page et ses données dans [!INCLUDE [prod_short](includes/prod_short.md)].
- Les fiches des discussions Teams ne sont pas automatiquement mises à jour en fonction des modifications. Toutes les modifications que vous enregistrez dans un enregistrement dans la fenêtre de détails sont enregistrées dans [!INCLUDE [prod_short](includes/prod_short.md)]. Mais la fiche dans Teams n’affichera pas les modifications de la conversion tant que vous n’aurez pas recollé le lien.

Pour en savoir plus sur l’utilisation des fiches et des détails de fiche, consultez [FAQ Teams](teams-faq.md).

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de l’intégration de Business Central et Microsoft Teams](across-teams-overview.md)  
[Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)  
[FAQ Teams](teams-faq.md)  
[Recherche de clients, de fournisseurs et autres contacts dans Microsoft Teams](across-search-contacts-teams.md)  
[Modification de la société et d’autres paramètres dans Teams](across-teams-settings.md)  
[Résolution des incidents dans Teams](admin-teams-troubleshooting.md)  
[Développement pour l’intégration de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]