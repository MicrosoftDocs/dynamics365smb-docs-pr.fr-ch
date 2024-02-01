---
title: Recherche de contacts dans Microsoft Teams
description: "Découvrez comment rechercher des clients, des fournisseurs et d’autres contacts Business\_Central à partir de Microsoft Teams."
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions'
ms.date: 04/12/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a>Recherche de clients, de fournisseurs et autres contacts dans Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]. Introduit dans la 1re vague de lancement 2021.

[!INCLUDE [prod_short](includes/prod_short.md)] dispose d’un système complet de gestion des contacts professionnels qui est essentiel pour les utilisateurs des ventes, des opérations ou d’autres rôles ministériels. Si vous êtes un utilisateur dans l’un de ces rôles, vous devrez souvent rechercher, rencontrer ou démarrer une conversation avec vos fournisseurs, clients et autres contacts. Avec l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams, vous pouvez effectuer ces tâches directement depuis Teams, sans avoir à passer à [!INCLUDE [prod_short](includes/prod_short.md)]. À partir de Teams, vous pouvez :

- Rechercher des contacts [!INCLUDE [prod_short](includes/prod_short.md)] dans la boîte de commande Teams ou dans la zone de rédaction du message. Les contacts peuvent inclure des prospects, des fournisseurs, des clients ou d’autres relations commerciales.
- Partagez un contact sous forme de carte dans une conversation Teams.
- Affichez des détails sur le contact, l′historique des interactions et d′autres informations telles que les paiements impayés ou les documents ouverts.

## <a name="prerequisites"></a>Conditions préalables

- Vous avez accès à Microsoft Teams.
- Vous avez installé l’application [!INCLUDE [prod_short](includes/prod_short.md)] dans Teams. Pour plus d’informations, voir [Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)
- Vous avez un compte [!INCLUDE [prod_short](includes/prod_short.md)] avec accès aux contacts dans au moins une entreprise.

> [!NOTE]
> Que vous recherchiez à partir de la boîte de commande ou de la boîte de rédaction de message, vous pouvez être invité à vous connecter ou à configurer l’application la première fois. Cette étape est nécessaire pour rechercher des contacts dans la bonne entreprise Business Central. Pour plus d’informations sur la configuration de l’application pour choisir votre entreprise, consultez [Modification de la société et d’autres paramètres dans les équipes](across-teams-settings.md).

## <a name="look-up-contacts-from-the-command-box"></a>Rechercher des contacts dans la boîte de commande

La boîte de commande est en haut de chaque écran dans Teams. Il vous permet de rechercher, d’effectuer des actions rapides ou de lancer des applications, comme l’application [!INCLUDE [prod_short](includes/prod_short.md)]. La recherche à partir de la boîte de commande est idéale pour rechercher rapidement des contacts et leurs données associées pour votre propre usage. Par exemple, supposons que vous souhaitiez rechercher l’adresse e-mail d’un fournisseur pour configurer une réunion de calendrier. Ou peut-être souhaitez-vous consulter l’historique des interactions lors d’une réunion avec un client.

1. Dans la zone de commande, saisissez **@Business Central**, puis sélectionnez l’application Business Central dans les résultats.

    ![Ouvrez l’application Business Central pour rechercher des contacts à partir de la boîte de commande.](media/teams-contacts-command-1.png)

2. Dans la zone **Business Central**, commencez à saisir le texte de recherche, comme un nom, une adresse ou un numéro de téléphone.

    Au fur et à mesure de votre saisie, les résultats correspondants s’affichent.

    ![Rechercher des contacts Business Central à partir de la boîte de commande dans Teams.](media/teams-contacts-command-2.png)
3. Sélectionnez un contact parmi les résultats.

    La carte de visite apparaît sous la boîte de commande.

4. Si vous souhaitez ajouter la carte de contact dans une conversation, allez dans le coin supérieur droit de la carte, sélectionnez **... (Plus d’options)** > **Copier**. Ensuite, collez la copie dans la zone de rédaction du message d’une conversation.  

Pour plus d’informations générales sur la zone de commande dans Teams, voir [Teams – Utiliser la boîte de commande](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).

## <a name="look-up-contacts-from-the-message-compose-box"></a>Rechercher des contacts dans la zone de composition de message

L’avantage d’utiliser la boîte de rédaction de message est que vous pouvez ajouter une fiche de contact directement à une conversation, pour que les autres puissent la voir.

1. Sous la zone de rédaction du message, sélectionnez l’icône **Business Central** pour lancer l’application.

    Si vous ne voyez pas l’icône **Business Central**, sélectionnez **... (Extensions de messagerie)**.

    ![Ouvrez l’application Business Central pour rechercher des contacts à partir de la zone de message.](media/teams-contacts-message-box.png)

2. Dans la zone **Business Central**, commencez à saisir le texte de recherche, comme un nom, une adresse ou un numéro de téléphone.

    Au fur et à mesure de votre saisie, les résultats correspondants s’affichent.

    ![Recherchez les contacts Business Central à partir de la zone de message.](media/teams-contacts-5.png)
3. Sélectionnez un contact parmi les résultats.

    La carte de visite apparaît dans la zone de rédaction du message.

    > [!NOTE]
    > La carte de visite n’est pas immédiatement envoyée à la conversation pour que les autres puissent la voir. Vous avez la possibilité de revoir le contenu de la carte et d’ajouter du texte avant ou après celle-ci à votre guise. Ensuite, envoyez votre message au chat lorsque vous êtes prêt.

### <a name="heres-another-way"></a>Voici une autre façon

1. Au lieu d’utiliser l’icône **Business Central**, saisissez **@Business Central** directement dans la zone de rédaction du message.
2. Entrez vos termes de recherche dans la zone.
3. Utilisez les touches fléchées haut et bas du clavier pour choisir un contact, puis appuyez sur <kbd>Entrée</kbd> pour le sélectionner.

## <a name="viewing-contact-card-details"></a>Affichage des détails de la carte de visite

La carte de visite dans Teams vous donne un aperçu rapide du client, du fournisseur ou du contact. La carte est interactive,&mdash;ce qui signifie que vous pouvez afficher plus d’informations ou même modifier un contact en utilisant les boutons **Détails** ou **Contextuel**.

Le bouton **Détails** ouvre une fenêtre dans Teams qui affiche plus d’informations sur le contact, mais pas autant que ce que vous verriez dans [!INCLUDE [prod_short](includes/prod_short.md)]. Pour voir toutes les informations sur un contact dans [!INCLUDE [prod_short](includes/prod_short.md)], sélectionnez **Contextuel**.

La carte de visite fonctionne exactement comme les cartes pour les enregistrements, comme les articles, les clients ou les commandes client. Pour plus d’informations sur les cartes, voir [Afficher les détails de la carte](across-working-with-teams.md#view-card-details).

> [!NOTE]
> Tous les participants à une conversation Teams pourront afficher les fiches des contacts Business Central que vous soumettez à une conversation. Mais pour afficher plus de détails sur les enregistrements, en utilisant les boutons **Détails** ou **Contextuel** sur une fiche, ils auront besoin d’accéder à [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Gestion de l’intégration Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de l’intégration de Business Central et Microsoft Teams](across-teams-overview.md)  
[Installer l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Microsoft Teams](across-install-app-for-teams.md)  
[FAQ Teams](teams-faq.md)  
[Modification de la société et d’autres paramètres dans Teams](across-teams-settings.md)  
[Partager des enregistrements dans Microsoft Teams](across-working-with-teams.md)  
[Résolution des incidents dans Teams](admin-teams-troubleshooting.md)  
[Développement pour l’intégration de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
