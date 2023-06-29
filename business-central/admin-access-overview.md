---
title: Gérer l’accès à Business Central
description: Les administrateurs utilisent une approche en couches pour contrôler l’accès à Business Central et à ses fonctionnalités.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: overview
ms.date: 04/04/2023
ms.custom: bap-template
---

# <a name="manage-access-to-business-central"></a><a name="manage-access-to-business-central"></a>Gérer l’accès à Business Central

Cet article fournit aux administrateurs et aux développeurs d’application une vue d’ensemble globale sur la façon de contrôler l’accès à [!INCLUDE [prod_short](includes/prod_short.md)] et à ses fonctionnalités. Utilisez les liens pour accéder à d’autres articles qui fournissent plus de détails sur les sujets.

## <a name="layered-access"></a><a name="layered-access"></a>Accès en couches

[!INCLUDE [prod_short](includes/prod_short.md)] utilise une approche en couches de la sécurité des applications, comme indiqué dans le diagramme suivant. Pour en savoir plus sur chaque couche, consultez [Sécurité des applications dans Business Central](/dynamics365/business-central/dev-itpro/security/security-application).

:::image type="content" source="media/security-overview.png" alt-text="Sécurité des applications en couches dans Business Central.":::

## <a name="licenses"></a><a name="licenses"></a>Licences

Attribuez aux utilisateurs de [!INCLUDE [prod_short](includes/prod_short.md)] une licence **Dynamics 365 Business Central** afin qu’ils puissent visualiser, modifier et agir sur leurs données métier à partir de n’importe quelle interface utilisateur. Pour en savoir plus sur les licences, consultez [Licences dans Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).

Cependant, les utilisateurs qui ont occasionnellement besoin d’un accès en lecture seule aux informations de [!INCLUDE [prod_short](includes/prod_short.md)] peuvent utiliser une licence **Microsoft 365**. Pour en savoir plus sur l’octroi d’un accès limité, consultez [Accès à Business Central avec des licences Microsoft 365](admin-access-with-m365-license.md).

Pour obtenir des informations détaillées sur les différents types de licences et le fonctionnement des licences dans [!INCLUDE[prod_short](includes/prod_short.md)], [téléchargez le Guide des licences Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

## <a name="business-central-administrator-tasks"></a><a name="business-central-administrator-tasks"></a>Tâches de l’administrateur de Business Central

Le tableau suivant répertorie la façon dont les administrateurs peuvent contrôler l’accès à [!INCLUDE [prod_short](includes/prod_short.md)] et aux fonctionnalités que les utilisateurs utilisent. Certaines des tâches aident également à maintenir à jour les paramètres d’accès.

|Tâche| En savoir plus |
|--|--|--|
|Chaque personne doit avoir un compte d’utilisateur avant de pouvoir se connecter à [!INCLUDE [prod_short](includes/prod_short.md)]. La manière la plus simple de configurer des utilisateurs consiste à les ajouter un par un dans le [centre d’administration Microsoft 365](https://go.microsoft.com/fwlink/p/?linkid=2024339). |[Ajouter des utilisateurs et attribuer des licences en même temps](/microsoft-365/admin/add-users/add-users)|
|Gérez l’accès pour tous les utilisateurs au niveau de l’environnement. Créez un groupe de sécurité Azure Active Directory (Azure AD) et affectez-le à l’environnement.<br><br> Vous pouvez également utiliser des groupes de sécurité pour gérer l’accès de groupes d’utilisateurs spécifiques. | [Gérer l’accès aux environnements](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access)<br><br>[Contrôler l’accès à Business Central à l’aide de groupes de sécurité](ui-security-groups.md) |
|Créez des utilisateurs dans [!INCLUDE [prod_short](includes/prod_short.md)] et définissez qui peut se connecter. | [Création des utilisateurs en fonction des licences](ui-how-users-permissions.md) |
|En combinaison avec les licences utilisateur, les autorisations définissent les objets auxquels un utilisateur peut accéder dans chaque base de données ou environnement. Spécifiez si les utilisateurs peuvent lire, modifier ou saisir des données dans les objets de la base de données. |[Affectation des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)|
|Si un comptable externe gère vos registres et vos états financiers, invitez-le dans [!INCLUDE [prod_short](includes/prod_short.md)]. Il pourra travailler plus étroitement avec vous sur vos données fiscales.|[Expériences de comptable dans [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)|
|Si vous êtes un partenaire revendeur de [!INCLUDE [prod_short](includes/prod_short.md)], vous pouvez envoyer un e-mail à un client pour demander une relation de revendeur. Vous pouvez inclure des privilèges d’administration déléguée pour Azure Active Directory et Microsoft 365 dans l’e-mail.| [Accès de l’administrateur délégué à Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin)|
|Une balise de service Azure représente un groupe d’adresses IP d’où peut provenir le trafic d’un service ou vers lesquelles il peut être redirigé. Utilisez des balises de service pour configurer des pare-feux pour autoriser le trafic uniquement à partir de certains services. La balise **Dynamics365BusinessCentral** vous permet d’utiliser les règles du pare-feu et du groupe de sécurité réseau pour restreindre le trafic vers et depuis [!INCLUDE [prod_short](includes/prod_short.md)].| [Balises du service de sécurité Azure](/dynamics365/business-central/dev-itpro/security/security-service-tags)|
|Lorsque vous utilisez l’authentification Azure Active Directory avec [!INCLUDE [prod_short](includes/prod_short.md)], nous vous recommandons de tirer parti de l’[authentification multifacteur (MFA) Azure AD](/azure/active-directory/authentication/concept-mfa-howitworks). L’authentification MFA protège davantage l’accès à l’application et aux données.|[Authentification multifacteur pour Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/security/multifactor-authentication)|

## <a name="business-central-developer-tasks"></a><a name="business-central-developer-tasks"></a>Tâches du développeur de Business Central

Les développeurs peuvent également gérer l’accès à [!INCLUDE [prod_short](includes/prod_short.md)]. Par exemple, les développeurs et les administrateurs peuvent créer et connecter des applications à [!INCLUDE [prod_short](includes/prod_short.md)] qui profitent à l’entreprise :  

* Rationaliser les processus métier
* Améliorer les interactions avec les clients
* Prendre de meilleures décisions, plus rapidement

Le tableau suivant contient des liens vers des informations sur la façon d’accorder aux applications et aux extensions l’accès aux données de [!INCLUDE [prod_short](includes/prod_short.md)].

| Tâche | En savoir plus |
|--|--|
|Les deux grands concepts pour définir l’accès aux fonctionnalités sont les droits et les autorisations. Les droits offrent un large accès aux objets en fonction des licences ou des rôles Azure Active Directory. Les autorisations et les ensembles d’autorisations vous permettent d’affiner l’accès aux objets. |[Présentation des droits et des ensembles d’autorisations](/dynamics365/business-central/dev-itpro/developer/devenv-entitlements-and-permissionsets-overview)|

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Sécurité dans Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)
