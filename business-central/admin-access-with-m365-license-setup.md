---
title: Configuration de l’accès avec les licences Microsoft 365
description: Guide sur la façon dont les administrateurs peuvent configurer l’accès à Business Central avec des licences Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 09/28/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.search.form: '9061,'
---
# <a name="set-up-business-central-access-in-teams-with-microsoft-365-licenses"></a>Configuration de l’accès à Business Central dans Teams avec les licences Microsoft 365

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Les administrateurs doivent effectuer plusieurs activités avant que les utilisateurs puissent accéder à [!INCLUDE [prod_short](includes/prod_short.md)] avec leur licence Microsoft 365. Les étapes ci-dessous représentent la configuration minimale requise pour commencer. Pour en savoir plus sur l’accès avec des licences Microsoft 365, accédez à [Accès à Business Central avec des licences Microsoft 365](admin-access-with-m365-license.md).

## <a name="guidelines"></a>Instructions

La configuration de l’accès avec les licences Microsoft 365 implique les tâches suivantes :

|Étape|Tâche|Requis|
|-|-|-|
|0|[Configurez les données de Business Central que les utilisateurs Microsoft 365 sous licence sont autorisés à afficher](#configure-permissions)|![coche](media/check.png "chèque ;")|
|2|[Activer l’accès avec des licences Microsoft 365 sur l’environnement Business Central](#enable-access-with-microsoft-365-licenses)|![coche](media/check.png "chèque ;")|
|3|[Attribuer le groupe de sécurité à l’environnement](#choose-who-gets-access-by-using-security-group)|
|4|[Déploiement de l’application Business Central pour Teams aux utilisateurs](#deploy-the-business-central-app-for-teams)|![coche](media/check.png "chèque ;")|
|5|[Tester la configuration](#test-your-setup)||

> [!TIP]
> Hormis pour la dernière tâche, vous pouvez effectuer les tâches dans n’importe quel ordre. Vous pouvez effectuer des tâches séparément, comme décrit dans les sections qui suivent ou utiliser le guide de configuration assistée **Accès avec des licences Microsoft 365** pour vous les expliquer.
>
> Pour exécuter la configuration assistée, procédez comme suit :
>
> 1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  saisissez **Configuration assistée**, puis choisissez le lien associé.
> 2. Sur la page **Configuration assistée**, accédez à la section **En faire plus avec Business Central** et sélectionnez **Accès avec des licences Microsoft 365**.
> 3. Suivez les instructions.  

## <a name="configure-permissions"></a>Configurer les autorisations

[!INCLUDE [prod_short](includes/prod_short.md)] est sécurisé par conception et minimise les risques en n’accordant aucune autorisation aux utilisateurs Microsoft 365 prêts à l’emploi. Les administrateurs doivent configurer des autorisations d’objet qui déterminent les tables, les pages et les rapports accessibles dans Teams avec seulement une licence Microsoft 365. Ces autorisations sont les autorisations de départ affectées quand un utilisateur se connecte pour la première fois avec sa licence Microsoft 365. 

Pour configurer les autorisations de démarrage :

1. Dans [!INCLUDE [prod_short](includes/prod_short.md)], recherchez **Configuration de la licence**.
2. Sélectionnez la licence Microsoft 365.
3. En haut de la page de licence **Microsoft 365**, sélectionnez l’icône de modification ![icône Modifier](media/edit-pencil.png), puis activez **Personnaliser les autorisations**. 
4. Dans la section **Ensembles d’autorisations personnalisés**, ajoutez les ensembles d’autorisations appropriés et choisissez s’ils s’appliquent à une seule entreprise ou à toutes les entreprises de l’environnement.

Avec cette configuration, les utilisateurs disposant uniquement d’une licence Microsoft 365 sont ajoutés à la liste **Utilisateurs** quand ils accèdent à [!INCLUDE [prod_short](includes/prod_short.md)] pour la première fois. Pour plus d’informations sur les utilisateurs, voir [Création d’utilisateurs conformément aux licences](ui-how-users-permissions.md).

> [!NOTE]
> Pendant la synchronisation de la liste des utilisateurs dans [!INCLUDE [prod_short](includes/prod_short.md)] avec les utilisateurs dans Microsoft 365, seuls les utilisateurs disposant d’une licence [!INCLUDE [prod_short](includes/prod_short.md)] sont ajoutés à la liste des utilisateurs de [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus de contrôle administratif sur les autorisations et les profils, vous pouvez attribuer un groupe de sécurité à l’environnement. Quand les environnements sont sécurisés à l’aide d’un groupe de sécurité et permettent l’accès avec des licences Microsoft 365, l’action **Mettre à jour les utilisateurs à partir de Microsoft 365** sur la page **Utilisateurs** inclura également les utilisateurs qui n’ont qu’une licence Microsoft 365. Pour en savoir plus sur la sécurisation des environnements, consultez [Gestion de l’accès à l’aide de groupes Microsoft Entra](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) dans l’aide aux développeurs et aux professionnels de l’informatique.

> [!TIP]
> Vous cherchez un moyen plus rapide de démarrer quand vous essayez cette fonctionnalité bac à sable ou une société d’évaluation ? Affectez le jeu d’autorisations **Lecture D365**, qui accorde l’autorisation à la plupart des objets.  

Quand vous travaillez avec plusieurs environnements, la configuration de la licence doit être appliquée à chaque environnement et peut être différente sur chaque environnement.

En savoir plus à [Affectation des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md) et [Composition des ensembles d’autorisations](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## <a name="enable-access-with-microsoft-365-licenses"></a>Accorder l’accès avec les licences Microsoft 365

L’accès avec des licences Microsoft 365 est désactivé par défaut. L’accès doit être activé pour chaque environnement indépendamment, donnant le contrôle aux administrateurs et permettant un déploiement par étapes dans toute l’organisation. Vous activez l’accès à l’aide du centre d’administration [!INCLUDE [prod_short](includes/prod_short.md)] : 

1. Dans l’angle supérieur droit, sélectionnez **Paramètres** ![Paramètres.](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord") > **Centre d’administration**.  
2. Dans le centre d’administration, sélectionnez  **Environnements**, puis sélectionnez l’environnement sur lequel vous souhaitez modifier l’accès à la licence. 
3. Sur la page **Détails de l’environnement**, sélectionnez **Modifier** pour le paramètre **Accès avec des licences Microsoft 365**.
4. Dans le volet **Licences Microsoft 365**, activez le bouton de commutateur. 
5. Sélectionnez **Enregistrer** quand vous avez terminé, puis acceptez la confirmation. Le changement entre en vigueur immédiatement.

## <a name="choose-who-gets-access-by-using-security-group"></a>Choisir qui obtient l’accès en utilisant le groupe de sécurité

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Dans le centre d’administration Business Center, un environnement peut être attribué à un ou plusieurs groupes de sécurité pour contrôler l’accès. Vous pouvez attribuer un groupe Microsoft Entra à l’environnement. En attribuant un groupe Microsoft Entra à un environnement, seuls les membres directs et indirects du groupe ont accès à l’environnement. Les membres indirects sont des utilisateurs d’un autre groupe, lui-même membre du groupe affecté à l’environnement. Bien que tous les utilisateurs sous licence dans Microsoft Entra ID sont ajoutés à l’environnement lorsqu’il est synchronisé avec Microsoft 365, seuls les membres du groupe peuvent se connecter. Pour en savoir plus, consultez [Gestion de l’accès à l’aide de groupes Microsoft Entra](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) dans l’aide aux développeurs et aux professionnels de l’informatique.

## <a name="deploy-the-business-central-app-for-teams"></a>Déployer l’application Business Central pour Teams

Pour les titulaires de licence [!INCLUDE [prod_short](includes/prod_short.md)] pour partager des données dans Teams, et pour les titulaires de licence Microsoft 365 pour accéder à ces données, chacun doit avoir installé l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams. Bien que les utilisateurs puissent installer l’application eux-mêmes, il est recommandé aux administrateurs d’utiliser le déploiement centralisé. Le déploiement centralisé vous permet de déployer l’application auprès d’une audience plus large dans toute l’organisation et de minimiser les efforts des utilisateurs individuels. 

Pour savoir comment déployer de manière centralisée l’application [!INCLUDE [prod_short](includes/prod_short.md)] pour Teams, voir [Installation de l’application Business Central à l’aide du déploiement centralisé](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Si vous avez déjà exécuté un déploiement centralisé et que vous n’avez déployé l’application que sur le groupe de sécurité des utilisateurs [!INCLUDE [prod_short](includes/prod_short.md)] sous licence, vous devrez le ré-exécuter pour déployer sur des groupes supplémentaires ou sur l’ensemble de l’organisation, selon la manière dont vous configurez l’accès.

> [!TIP]
> Vous cherchez un moyen plus rapide de démarrer quand vous essayez cette fonctionnalité ? Les utilisateurs test peuvent installer l’application sur [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## <a name="test-your-setup"></a>Test de votre configuration

Pour vérifier que votre configuration est prête pour la production, les étapes suivantes vous aideront à vous assurer que tout fonctionne comme il se doit.

1. Créez ou identifiez deux utilisateurs test (A et B).

   - L’utilisateur test A doit avoir une licence [!INCLUDE [prod_short](includes/prod_short.md)] et une licence Microsoft 365 avec accès à Teams.
   - L’utilisateur de test B ne doit avoir qu’une licence Microsoft 365 avec accès à Teams.

2. Connectez-vous au client web [!INCLUDE [prod_short](includes/prod_short.md)] en tant qu’utilisateur test A.

   1. Ouvrez un enregistrement auquel l’utilisateur de test B doit avoir accès, tel qu’une fiche **Article** dans l’entreprise et l’environnement appropriés.
   2. Sélectionnez **Partager** ![!Action de partage avec d’autres applications sur les pages.](media/share-icon.png) > **Partage avec Teams** pour afficher la fenêtre Partager avec Teams.
   3. Dans le champ **Partager avec**, ajoutez l’utilisateur de test B en tant que destinataire.
   4. Attendez que le lien se développe sur une carte et sélectionnez Partager.

3. Connectez-vous à Microsoft Teams en tant qu’utilisateur test B.

   1. Sélectionnez Conversation instantanée et ouvrez la conversation avec l’utilisateur test A.
   2. Dans le message envoyé par l’utilisateur de test A, sélectionnez le bouton Détails sur la carte. Si le client [!INCLUDE [prod_short](includes/prod_short.md)] est affiché et en lecture seule, votre configuration a réussi.

> [!TIP]
> Un problème est survenu ? Consultez [Résoudre les problèmes d’accès avec les licences Microsoft 365](admin-access-with-m365-license-troubleshooting.md).

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de l’accès à Business Central avec les licences Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Résoudre les problèmes d’accès avec les licences Microsoft 365](admin-access-with-m365-license-troubleshooting.md)  
[Intégration de Business Central et Microsoft Teams](across-teams-overview.md)  
