---
title: Ajout d’un onglet Business Central dans Microsoft Teams
description: Découvrez comment ajouter des onglets dans Teams pour afficher des pages Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/04/2022
ms.custom: bap-template
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records, tab'
---

# <a name="add-business-central-tab-in-microsoft-teams"></a><a name="add-business-central-tab-in-microsoft-teams"></a>Ajout d’un onglet Business Central dans Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

Dans Teams, les onglets apparaissent en haut des canaux et des conversations instantanées, permettant aux participants d’accéder rapidement aux informations pertinentes. Cet article explique différentes façons d’ajouter un onglet qui affiche les données [!INCLUDE [prod_short](includes/prod_short.md)].

![Onglets dans Teams](media/teams-tabs-border.png)

## <a name="about-business-central-tabs"></a><a name="about-business-central-tabs"></a>À propos des onglets Business Central

Un onglet [!INCLUDE [prod_short](includes/prod_short.md)] fournit une vue ciblée de des pages de liste et de carte [!INCLUDE [prod_short](includes/prod_short.md)]. L’onglet n’affiche pas le client web [!INCLUDE [prod_short](includes/prod_short.md)] complet. Il n’y a pas de bordure de navigateur, de bannière [!INCLUDE [prod_short](includes/prod_short.md)] (par exemple avec Tell Me, recherche, aide) ou du contenu de la page uniquement avec menu de navigation supérieur et ses actions. Le contenu est interactif, ce qui signifie que vous pouvez sélectionner des actions et des liens, modifier des données, etc. Vous êtes limité à ce que vous voyez et pouvez faire avec les mêmes autorisations attribuées à votre compte dans [!INCLUDE [prod_short](includes/prod_short.md)].

Pour savoir qui peut voir le contenu d’un onglet [!INCLUDE [prod_short](includes/prod_short.md)], voir [Qui peut voir le contenu d’un onglet ?](/dynamics365/business-central/teams-faq?tabs=tabs#who-can-view).

> [!TIP]
> Vous êtes développeur ? Vous pouvez également ajouter des onglets par programmation à l’aide de l’API Microsoft Graph. Pour plus d’informations, voir [Ajout d’onglets Business Central dans Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams-tabs).  

## <a name="prerequisites"></a><a name="prerequisites"></a>Conditions préalables

Pour ajouter un onglet [!INCLUDE [prod_short](includes/prod_short.md)], les conditions suivantes doivent être remplies :

- Vous avez accès à Microsoft Teams.
- Vous devez disposer d’une licence [!INCLUDE [prod_short](includes/prod_short.md)].
- Vous avez installé l’application [!INCLUDE [prod_short](includes/prod_short.md)] dans Teams. Pour plus d’informations, voir [Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md).

Pour afficher un onglet [!INCLUDE [prod_short](includes/prod_short.md)] ajouté par un autre participant dans le canal ou la conversation instantanée, les conditions suivantes doivent être remplies :

- Vous avez accès à Microsoft Teams.
- Vous avez une licence [!INCLUDE [prod_short](includes/prod_short.md)] ou un accès limité à Business Central avec une licence Microsoft 365 uniquement. Pour plus d’informations, voir [Accès à Business Central avec des licences Microsoft 365](admin-access-with-m365-license.md).
- Vous avez installé l’application [!INCLUDE [prod_short](includes/prod_short.md)] dans Teams.

## <a name="add-tab-using-recommended-content"></a><a name="add-tab-using-recommended-content"></a>Ajout d’un onglet en utilisant le contenu recommandé

Utilisez ces étapes pour ajouter un onglet en choisissant ce qu’il faut afficher à partir d’une liste facilement disponible de contenu recommandé basé sur votre centre de rôle, sans quitter Teams. Pour en savoir plus sur le contenu que vous pouvez choisir, consultez [D’où vient le contenu recommandé ?](/dynamics365/business-central/teams-faq?tabs=tabs#where-does-the-recommended-content-come-from).

1. En haut d’un canal ou d’une conversation instantanée dans Teams, sélectionnez **+ Ajouter un onglet**.
2. Dans la case **Rechercher**, saisissez *Business Central*, puis sélectionnez l’icône **[!INCLUDE [prod_short](includes/prod_short.md)]** et attendez que la fenêtre de configuration de l’onglet [!INCLUDE [prod_short](includes/prod_short.md)] s’affiche.

   ![Affiche la fenêtre de configuration de l’onglet Business Central dans Teams](media/teams-bc-tab-config-window.png)

3. L’option **Choisir parmi les contenus recommandés pour** affiche la société dans [!INCLUDE [prod_short](includes/prod_short.md)] avec qui vous travaillez. Si vous souhaitez afficher le contenu d’une autre société, sélectionnez la société actuelle, puis utilisez les options **Environnement** et **Société** pour spécifier la société avec laquelle vous souhaitez travailler.
4. Sélectionnez la flèche vers le bas dans l’option **Contenu de l’onglet** et choisissez le contenu à afficher.

   <!-- The list shows all pages that are bookmarked on your role center in [!INCLUDE [prod_short](includes/prod_short.md)]. To learn more about the content that you can choose from, see [Where does the recommended content come from?](teams-faq.md#recommended-content).-->
5. Certaines pages peuvent inclure différentes vues, qui sont des variantes de la page filtrée pour afficher des données spécifiques. Pour modifier l’affichage du contenu, sélectionnez la flèche vers le bas pour l’option **Vue préférée** et choisissez la vue dans la liste.

   Pour plus d’informations sur les vues, voir [Enregistrer et personnaliser les vues](ui-views.md).
6. Sélectionnez **Publier sur le canal à propos de cet onglet** pour publier automatiquement une annonce dans le canal ou la conversation instantanée Teams pour informer les participants que vous avez ajouté cet onglet.
7. Sélectionnez **Enregistrer**.

## <a name="add-tab-using-a-page-link"></a><a name="add-tab-using-a-page-link"></a>Ajoute d’un onglet à l’aide d’un lien de page

Une autre façon d’ajouter un onglet en utilisant un lien (URL) vers la page que vous souhaitez afficher. Cette méthode est utile quand vous souhaitez afficher un enregistrement ou une page de liste [!INCLUDE [prod_short](includes/prod_short.md)] qui n’est pas mise en signet sur votre tableau de bord.

1. En haut d’un canal ou d’une conversation instantanée dans Teams, sélectionnez **+ Ajouter un onglet**.
2. Dans la zone **Recherche**, tapez *Business Central* et sélectionnez l’icône **[!INCLUDE [prod_short](includes/prod_short.md)]**.
3. Attendez que la fenêtre de configuration de l’onglet [!INCLUDE [prod_short](includes/prod_short.md)] s’affiche, puis sélectionnez **Coller un lien [!INCLUDE [prod_short](includes/prod_short.md)] à la place**.

   ![Affiche la fenêtre de configuration de l’onglet Business Central dans Teams et met en surbrillance l’option de lien](media/teams-bc-tab-config-window-page-link.png)
4. Allez à [!INCLUDE [prod_short](includes/prod_short.md)], et ouvrez la page à afficher dans l’onglet.
5. Copiez le lien vers la page.

   Vous pouvez copier le lien de deux manières. La manière la plus simple et préférée consiste à sélectionner **Partager** ![icône Partager dans Business Central](media/share-icon.png) > **Copier le lien**. L’autre manière consiste à copier l’URL entière à partir de la barre d’adresse du navigateur. Pour en savoir plus sur cette étape, voir [Partage d’enregistrements Business Central et de liens de page](across-working-with-teams.md).

6. Revenez à Teams et collez le lien dans la case **URL**.
7. Dans la case **Nom de l’onglet**, entrez un nom qui s’affichera sur l’onglet.
8. Sélectionnez **Publier sur le canal à propos de cet onglet** pour publier automatiquement une annonce dans le canal ou la conversation instantanée Teams pour informer les participants que vous avez ajouté cet onglet.
9. Sélectionnez **Enregistrer**.

## <a name="add-tab-by-pinning-card-details"></a><a name="add-tab-by-pinning-card-details"></a>Ajout d’un onglet en épinglant les détails de la carte

Utilisez ces étapes pour ajouter un onglet pour un enregistrement qui a été partagé ou collé dans un canal ou une conversation instantanée Teams. Pour savoir comment partager des enregistrements et des liens de page dans Teams, voir [Partager des enregistrements et des liens de page dans Teams](across-working-with-teams.md).

1. Dans Teams, sélectionnez le bouton **Détails** sur la carte.
2. Dans le coin supérieur droit des détails de la carte, sélectionnez l’icône **Épingler en haut de la conversation instantanée** ![icône Épingle pour l’ajout d’un onglet Teams dans Business Central](media/pin-teams.png).

## <a name="change-a-tab-and-its-content"></a><a name="change-a-tab-and-its-content"></a>Modifier un onglet et son contenu

Une fois qu’un onglet a été ajouté, vous pouvez apporter certaines modifications à l’onglet. Par exemple, vous pouvez renommer l’onglet, le déplacer et le supprimer. Vous trouverez ces actions dans les options d’onglet disponibles en sélectionnant la flèche vers le bas de l’onglet.

![Affiche la fenêtre de configuration de l’onglet Business Central dans Teams et le menu d’options de l’onglet](media/teams-bc-tab-config-window-options.png)

Quant au contenu d’un onglet, vous pouvez modifier les données, si vous en avez l’autorisation. Si vous modifiez les données, les autres ne verront pas les modifications jusqu’à ce qu’ils quittent l’onglet et reviennent. Il en va de même pour vous si quelqu’un d’autre apporte des modifications aux données. Vous ne pouvez pas modifier la page qui s’affiche sur l’onglet, il vous suffit donc de supprimer l’onglet et d’en ajouter un autre aux couleurs.

Vous pouvez également modifier votre vue de la page et de ses données, comme le tri et le basculement de la disposition entre les vues de liste et de vignettes. Quand vous effectuez ce type de modifications, elles n’affectent pas ce que les autres voient. Ils verront ce que vous avez initialement publié, jusqu’à ce qu’ils apportent eux-mêmes des modifications similaires.

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Vue d’ensemble de l’intégration de Business Central et Microsoft Teams](across-teams-overview.md)  
[Installation de l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)  
[Partage d’enregistrements et de liens de page Business Central dans Microsoft Teams](across-working-with-teams.md).
[FAQ Teams](teams-faq.md)  
[Recherche de clients, de fournisseurs et autres contacts dans Microsoft Teams](across-search-contacts-teams.md)  
[Modification de la société et d’autres paramètres dans Teams](across-teams-settings.md)  
[Résolution des incidents dans Teams](admin-teams-troubleshooting.md)  
[Développement pour l’intégration de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
