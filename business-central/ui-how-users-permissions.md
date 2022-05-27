---
title: Créer des utilisateurs en fonction des licences
description: Décrit comment ajouter des utilisateurs à Business Central en ligne ou sur site en fonction des licences.
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173
ms.date: 05/09/2022
ms.author: edupont
ms.openlocfilehash: 77a58c9e4cfc5e9a744d66d0f6b62c06cb430d6b
ms.sourcegitcommit: 2fa712d0aabe4287ebd4454c28d142d6baf045a0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/09/2022
ms.locfileid: "8729816"
---
# <a name="create-users-according-to-licenses"></a>Créer des utilisateurs en fonction des licences

Cet article décrit comment les administrateurs créent des utilisateurs et définissent qui peut se connecter à [!INCLUDE[prod_short](includes/prod_short.md)]. Il explique également comment attribuer des autorisations à différents types d’utilisateurs en fonction des licences de produit.

Lorsque vous créez des utilisateurs dans [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez leur attribuer des autorisations au moyen d’ensembles d’autorisations et organiser les utilisateurs en groupes. Les groupes d’utilisateurs facilitent la gestion simultanée des autorisations pour plusieurs utilisateurs. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).  

Pour plus d’informations sur les différents types de licences et le fonctionnement des licences dans [!INCLUDE[prod_short](includes/prod_short.md)], [téléchargez le Guide des licences Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Le processus de gestion des utilisateurs et des licences varie selon que [!INCLUDE[prod_short](includes/prod_short.md)] est déployé en ligne ou sur site. Pour [!INCLUDE [prod_short](includes/prod_short.md)] en ligne, vous devez ajouter des utilisateurs depuis Microsoft 365. Dans les déploiements sur site, vous pouvez créer, modifier et supprimer directement des utilisateurs.  

## <a name="manage-users-and-licenses-in-online-tenants"></a>Gérer des utilisateurs et des licences dans les abonnés en ligne

Votre abonnement à [!INCLUDE[prod_short](includes/prod_short.md)] en ligne définit le nombre d’utilisateurs autorisés. Les utilisateurs sont ajoutés à votre abonné dans l’Espace partenaires Microsoft, généralement par votre partenaire Microsoft. Pour plus d’informations, voir [Administration de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Vous attribuez des licences produit aux utilisateurs en fonction du travail que chacun effectue dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous disposez de plusieurs façons pour attribuer des licences :

- L’administrateur Microsoft 365 de votre société peut le faire dans le [Centre d’administration Microsoft 365](https://admin.microsoft.com). Pour plus d’informations, voir [Ajouter des utilisateurs individuellement ou en bloc à Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Un partenaire Microsoft peut attribuer des licences dans le Centre d’administration Microsoft 365 ou l’Espace partenaires Microsoft. Pour plus d’informations, voir [Tâches de gestion des utilisateurs pour les comptes clients](/partner-center/assign-licenses-to-users) dans l’aide de l’Espace partenaires Microsoft.

Pour plus d’informations, voir [Administration de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) dans l’aide dédiée à l’administration.

> [!NOTE]
> Après avoir ajouté des utilisateurs dans le Centre d’administration Microsoft 365, nous vous recommandons de mettre à jour les informations utilisateur dans [!INCLUDE[prod_short](includes/prod_short.md)] dès que possible. Il est facile de tenir à jour les informations des utilisateurs et de garantir qu’ils peuvent toujours se connecter. Pour plus d’informations, voir [Pour ajouter des utilisateurs ou mettre à jour les informations utilisateur et les attributions de licence dans Business Central](#adduser).<br>
>
> La mise à jour des informations utilisateur est particulièrement importante si vous avez personnalisé des ensembles d’autorisations pour la licence. Si un nouvel utilisateur tente de se connecter à [!INCLUDE[prod_short](includes/prod_short.md)] avant d’y être ajouté, il ne pourra peut-être pas le faire. Pour plus d’informations, voir [Configurer les autorisations en fonction des licences](#licensespermissions).
>
> Cependant, les utilisateurs qui rencontrent ce problème ne sont pas réellement bloqués. Ils peuvent soit utiliser l’action **Revenir au début** ou simplement se connecter à nouveau pour résoudre le problème.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Pour plus d’informations, voir [Accès administrateur délégué à Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

### <a name="configure-permissions-based-on-licenses"></a><a name="licensespermissions"></a>Configurer les autorisations en fonction des licences

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Les administrateurs peuvent configurer des ensembles d’autorisations et des groupes d’utilisateurs en fonction des différents types de licence.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Par exemple, la licence couramment utilisée, *Dynamics 365 Business Central Team Member*, a les groupes d’utilisateurs *Membre de l’équipe D365* et *Action d’exportation Excel* plus les ensembles d’autorisations suivants définis par défaut :

- LIRE D365
- MEMBRE D’ÉQUIPE D365
- MODIFIER DANS EXCEL - AFFICHER
- EXPORTER ÉTAT EXCEL
- LOCAL

Si cette configuration par défaut n’est pas la bonne pour un abonné particulier, l’administrateur peut modifier cette configuration. Cependant, les autorisations personnalisées n’affecteront que les nouveaux utilisateurs auxquels cette licence est attribuée. Les autorisations des utilisateurs existants auxquels la licence est attribuée ne sont pas affectées.  

1. Connectez-vous à [!INCLUDE[prod_short](includes/prod_short.md)] en tant qu’administrateur.  
2. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration de licence**, puis sélectionnez le lien associé.  

    Sinon, si vous êtes déjà dans la page **Utilisateurs**, vous pouvez exécuter le guide **Mettre à jour les utilisateurs à partir de Microsoft 365**, puis, sur la première page du guide, choisissez le lien **Configurer les autorisations par licence**.  
3. Dans la page **Configuration de licence**, choisissez la licence que vous souhaitez personnaliser, puis choisissez l’action **Configurer**.  
4. Choisissez le champ **Personnaliser les autorisations** pour activer la personnalisation, puis apportez les modifications appropriées.  

    Dans notre exemple, l’administrateur souhaite supprimer l’autorisation de modification dans Excel, il supprime donc le groupe d’utilisateurs *Action d’exportation Excel* de la licence Team Member. À l’avenir, les nouveaux utilisateurs auxquels la licence Team Member est attribuée n’auront pas la possibilité d’exporter les données vers Excel. Si l’organisation change d’avis à leur sujet, elle peut simplement revenir sur la page **Configuration de licence** et désactiver la personnalisation pour ce type de licence.  

> [!IMPORTANT]
> Cette personnalisation des autorisations ne prend effet que pour les nouveaux utilisateurs auxquels vous attribuez la licence correspondante. Les utilisateurs existants ne sont pas mis à jour. Nous vous recommandons de personnaliser les autorisations avant de commencer à attribuer des licences utilisateur dans le Centre d’administration Microsoft 365.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Pour ajouter des utilisateurs ou mettre à jour les informations utilisateur et les attributions de licence dans Business Central

Après avoir ajouté des utilisateurs ou modifié les informations utilisateur dans le centre d’administration Microsoft 365, vous pouvez importer rapidement les informations utilisateur dans [!INCLUDE[prod_short](includes/prod_short.md)]. L’importation inclut les attributions de licence.  

1. Connectez-vous à [!INCLUDE[prod_short](includes/prod_short.md)] en tant qu’administrateur.
2. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Utilisateurs**, puis choisissez le lien associé.  
3. Choisissez **Mettre à jour les utilisateurs depuis Microsoft 365**.

Pour les nouveaux utilisateurs, l’étape suivante consiste à attribuer des groupes d’utilisateurs et des autorisations. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md). Si vous mettez à jour les informations utilisateur et que la mise à jour inclut un changement de licence, les utilisateurs sont affectés au groupe d’utilisateurs approprié et leurs ensembles d’autorisations sont mis à jour. Pour plus d’informations, voir [Pour gérer les autorisations via les groupes d’utilisateurs](ui-define-granular-permissions.md).  

> [!NOTE]
> Tous les utilisateurs d’un environnement doivent être affectés à la même licence, Essential ou Premium. Pour en savoir plus, consultez le guide des licences Microsoft Dynamics 365 Business Central. Le guide est téléchargeable sur le site Internet [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Pour en savoir plus sur la synchronisation des informations utilisateur avec Microsoft 365, consultez la section [Synchronisation avec Microsoft 365](#m365).

> [!NOTE]
> Si vous utilisez un comptable externe pour gérer votre comptabilité et vos états financiers, vous pouvez les inviter dans votre Business Central afin qu’ils puissent travailler avec vous et utiliser vos données fiscales. Pour plus d’informations, voir [Inviter votre comptable externe dans votre Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Pour supprimer l’accès d’un utilisateur au système

Vous pouvez supprimer l’accès d’un utilisateur à [!INCLUDE[prod_short](includes/prod_short.md)] en ligne. Toutes les références à l’utilisateur sont conservées. Cependant, l’utilisateur ne peut pas se connecter et les sessions actives de l’utilisateur sont arrêtées.

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Utilisateurs**, puis choisissez le lien associé.
2. Ouvrez la page **Fiche utilisateur** pour l’utilisateur concerné, puis, dans le champ **Statut**, sélectionnez **Désactivé**.
3. Pour donner à nouveau accès à l’utilisateur, définissez le paramètre du champ **Statut** sur **Activé**.

Vous pouvez également supprimer la licence d’un utilisateur dans le Centre d’administration Microsoft 365. L’utilisateur ne peut alors plus se connecter. Pour en savoir plus, consultez [Supprimer des licences d’utilisateurs](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Synchronisation avec Microsoft 365

Lorsque vous attribuez une licence [!INCLUDE[prod_short](includes/prod_short.md)] à un utilisateur dans Microsoft 365, il existe deux façons de créer l’utilisateur dans [!INCLUDE[prod_short](includes/prod_short.md)].  

- L’administrateur peut ajouter l’utilisateur en choisissant l’action **Mettre à jour les utilisateurs à partir de Microsoft 365** sur la page **Utilisateurs**, comme décrit dans la section [Pour ajouter un utilisateur ou mettre à jour les informations utilisateur dans Business Central](#adduser).
- Les informations de licence sont mises à jour automatiquement lors de la première connexion de l’utilisateur.

Dans les deux cas, plusieurs paramètres sont configurés automatiquement. Ces paramètres sont répertoriés dans les deuxième et troisième colonnes du tableau ci-dessous.

Si vous modifiez les informations utilisateur dans Microsoft 365, vous pouvez mettre à jour [!INCLUDE[prod_short](includes/prod_short.md)] pour refléter le changement. Selon ce que vous souhaitez mettre à jour, utilisez l’une des actions sur la page **Utilisateurs**. Les actions sont décrites dans les trois dernières colonnes du tableau ci-dessous.

> [!NOTE]
> Les actions décrites dans le tableau suivant sont exactes, cependant, la seule dont vous ayez besoin est **Mettre à jour les utilisateurs depuis Microsoft 365**, qui a été ajoutée pour simplifier le processus. Les autres actions seront supprimées dans une future version de [!INCLUDE[prod_short](includes/prod_short.md)].

|Ce qui se produit dans les cas suivants :|Premier utilisateur, première connexion|Récupérer des utilisateurs à partir de Microsoft 365|Mettre à jour les utilisateurs à partir de Microsoft 365|Restaurer les groupes d’utilisateurs par défaut de l’utilisateur|Actualiser les groupes d’utilisateurs|Mettre à jour l’utilisateur à partir de Microsoft 365|
|-|-|-|-|-|-|-|
|Portée :|Utilisateur actuel|Nouveaux utilisateurs dans Microsoft 365|Plusieurs utilisateurs sélectionnés|Un seul utilisateur sélectionné (sauf l’utilisateur actuel)|Plusieurs utilisateurs sélectionnés|Plusieurs utilisateurs sélectionnés|
|Créez le nouvel utilisateur et attribuez le jeu d’autorisations SUPER.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Mettez à jour l’utilisateur en fonction des informations dans Microsoft 365 : Statut, Nom complet, E-mail du contact, adresse e-mail d’authentification.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Synchronisez les plans utilisateur (licences) avec les licences et les rôles attribués dans Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Ajoutez l’utilisateur aux groupes d’utilisateurs en fonction des plans utilisateur actuels. Supprimez l’ensemble d’autorisations SUPER pour tous les utilisateurs autres que le premier utilisateur à se connecter et les [administrateurs](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Au moins une autorisation SUPER est requise.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Supprime manuellement les groupes d’utilisateurs et les autorisations affectés.|**X**<br /><br />Mettez à jour les affectations des groupes d’utilisateurs.| |

<!--
## The Device License
This section has been moved to [Licensing in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).
-->

## <a name="manage-users-and-licenses-in-on-premises-deployments"></a>Gérer des utilisateurs et des licences dans les déploiements sur site

Pour les déploiements sur site, le nombre de licences utilisateur est spécifié dans le fichier de licence (.flf). Lorsqu’un administrateur ou un partenaire Microsoft télécharge le fichier de licence, il peut spécifier les utilisateurs qui peuvent se connecter à [!INCLUDE[prod_short](includes/prod_short.md)].

Pour les déploiements sur site, l’administrateur crée, édite et supprime les utilisateurs directement à partir de la page **Utilisateurs**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Pour modifier ou supprimer un utilisateur dans un déploiement sur site

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Utilisateurs**, puis choisissez le lien associé.
2. Sélectionnez l’utilisateur que vous souhaitez modifier, puis choisissez l’action **Modifier**.
3. Sur la page **Fiche utilisateur**, modifiez les informations si nécessaire.  
4. Pour supprimer un utilisateur, sélectionnez l’utilisateur que vous souhaitez supprimer, puis choisissez l’action **Supprimer**.

> [!NOTE]
> Pour les déploiements sur site, un administrateur peut spécifier comment authentifier les informations d’identification de l’utilisateur dans l’instance [!INCLUDE[server](includes/server.md)]. Lorsque vous créez un utilisateur, vous fournissez le type d’informations d’identification que vous utilisez.
>
> Pour plus d’informations, consultez [Authentification et types d’informations d’identification](/dynamics365/business-central/dev-itpro/administration/users-credential-types) dans l’aide dédiée à l’administration pour [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Voir aussi

[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  
[Gérer les profils](admin-users-profiles-roles.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Gestion des licences dans Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Ajouter des utilisateurs à Microsoft 365 pour les entreprises](/microsoft-365/admin/add-users/add-users)  
[Sécurité et protection dans Business Central (contenu d’administration)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Affecter un ID télémétrie aux utilisateurs](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]