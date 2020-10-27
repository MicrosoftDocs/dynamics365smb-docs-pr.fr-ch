---
title: Utiliser les données Business Central dans Microsoft Teams| Microsoft Docs
description: Découvre comment utiliser l’application Business Central pour Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989451"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Utilisation des données Business Central dans Microsoft Teams

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

[!INCLUDE [prodshort](includes/prodshort.md)] propose une application qui connecte Microsoft Teams à vos données métier dans [!INCLUDE [prodshort](includes/prodshort.md)], afin que vous puissiez partager rapidement les détails entre les membres de l’équipe et répondre plus rapidement aux demandes de renseignements. Dans cet article, vous apprendrez à utiliser l’application pour partager des données [!INCLUDE [prodshort](includes/prodshort.md)] avec des collègues dans une conversation Teams.

## <a name="overview"></a>Aperçu

L’application [!INCLUDE [prodshort](includes/prodshort.md)] vous permet de :

- Copier un lien vers n’importe quel enregistrement Business Central et le coller dans une conversation Teams à partager avec vos collègues. Le lien étendra cela dans une carte interactive compacte qui affiche des informations sur l’enregistrement.
- Une fois dans la conversation, vous et vos collègues pouvez afficher plus de détails sur l’enregistrement, modifier les données et prendre des mesures, sans quitter Teams.

[![Intégration Teams avec Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Conditions préalables

- Vous avez accès à Microsoft Teams.
- Vous avez installé l’application [!INCLUDE [prodshort](includes/prodshort.md)] dans Teams. Pour plus d’informations, voir [Installer l’application [!INCLUDE [prodshort](includes/prodshort.md)] pour Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Tous les participants à une conversation Teams pourront afficher les fiches des enregistrements Business Central que vous soumettez à la conversation. Mais pour afficher plus de détails sur les enregistrements, en utilisant les boutons **Détails** ou **Contextuel** sur une fiche, ils auront besoin d’accéder à [!INCLUDE [prodshort](includes/prodshort.md)]. Pour plus d’informations, voir [Gestion de l’intégration Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Inclure une fiche Business Central dans une conversation Teams

1. Connectez-vous à [!INCLUDE [prodshort](includes/prodshort.md)] en utilisant votre navigateur.
2. Ouvrez l’enregistrement que vous souhaitez partager.

    L’application est conçue pour afficher des pages de type fiche à partir de [!INCLUDE [prodshort](includes/prodshort.md)]. Ouvrez une page qui affiche un seul enregistrement, comme un article, un client ou une commande client. Vous ne pouvez pas l’utiliser pour les tableaux de bord ou les pages qui affichent plusieurs enregistrements dans une liste.

3. Copiez l’URL entière de la barre d’adresse du navigateur.

   ![Copier l’URL de Business Central à partir du navigateur](media/teams-url.png)
4. Accédez à Teams et démarrez une conversation, qui peut être une discussion avec une personne, un groupe de personnes ou un canal d’équipe.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Collez l’URL dans la zone où vous ajoutez un message.

   ![Coller l’URL de Business Central dans Teams](media/teams-paste-url.png)
6. La première fois que vous collez un lien dans une conversation, vous serez invité à vous connecter à [!INCLUDE [prodshort](includes/prodshort.md)] et à autoriser l’application à récupérer des données. Suivez simplement les instructions à l’écran.

    > [!NOTE]
    > Vous ne devez effectuer cette étape qu’une seule fois.

7. Attendez un moment pendant qu’une fiche soit générée dans la boîte de message.

8. Lorsque la fiche apparaît, examinez attentivement don contenu pour toute information sensible avant d’envoyer le message. Cette étape est importante, car une fois que vous envoyez le message, tous les participants à la conversation peuvent voir la fiche.

9. Si la fiche semble bonne, sélectionnez **Envoyer** pour la soumettre à la conversation.

    > [!TIP]
    > Après l’apparition de la fiche et avant de sélectionner **Envoyer** , vous pouvez supprimer l’URL collée si vous le souhaitez.

10. Pour afficher plus de détails ou apporter des modifications à l’enregistrement, sélectionnez **Détails** .

    La page de détails est similaire à ce que vous voyez dans [!INCLUDE [prodshort](includes/prodshort.md)]. Mais elle est légèrement rognée pour Teams. Lorsque vous avez terminé de consulter et d’apporter des modifications, fermez la fenêtre pour revenir à la conversation Teams.

    > [!NOTE]
    > Les modifications que vous apportez ne seront pas reflétées dans la fiche avant la prochaine fois que vous collerez son lien dans une conversation.

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de l’intégration de Business Central et Microsoft Teams](across-teams-overview.md)  
[Installer l’application [!INCLUDE [prodshort](includes/prodshort.md)] pour Microsoft Teams](across-install-app-for-teams.md)  
[Développement pour l’intégration de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Mise en route](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
