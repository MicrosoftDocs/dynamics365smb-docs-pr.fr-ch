---
title: Créer des utilisateurs en fonction des licences
description: "Décrit comment ajouter des utilisateurs à Business\_Central en ligne ou sur site en fonction des licences."
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173'
ms.date: 03/24/2023
ms.author: jswymer
ms.reviewer: jswymer
---
# <a name="create-users-according-to-licenses"></a>Créer des utilisateurs en fonction des licences

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Cet article décrit comment les administrateurs créent des utilisateurs et définissent qui peut se connecter à [!INCLUDE[prod_short](includes/prod_short.md)]. Vous allez également apprendre comment attribuer des autorisations à différents utilisateurs en fonction des licences de produit.

Quand vous créez des utilisateurs dans [!INCLUDE[prod_short](includes/prod_short.md)], vous leur accordez des autorisations via des ensembles d’autorisations. Vous pouvez également organiser les utilisateurs en groupes d’utilisateurs. Les groupes d’utilisateurs facilitent la gestion simultanée des autorisations et autres paramètres pour plusieurs utilisateurs. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).  

Pour plus d’informations sur les différents types de licences et le fonctionnement des licences dans [!INCLUDE[prod_short](includes/prod_short.md)], [téléchargez le Guide des licences Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Le processus de gestion des utilisateurs et des licences varie selon que [!INCLUDE[prod_short](includes/prod_short.md)] est déployé en ligne ou sur site. Pour [!INCLUDE [prod_short](includes/prod_short.md)] en ligne, vous devez ajouter des utilisateurs depuis Microsoft 365. Dans les déploiements sur site, vous pouvez créer, modifier et supprimer directement des utilisateurs.  

## <a name="manage-users-and-licenses-in-online-tenants"></a>Gérer des utilisateurs et des licences dans les abonnés en ligne

Les comptes d’utilisateurs dans [!INCLUDE[prod_short](includes/prod_short.md)] doivent d’abord être créés dans le centre d’administration Microsoft 365. Ces comptes d’utilisateurs ne sont pas exclusifs à Business Central. Si vous souscrivez à d’autres plans, ils peuvent être utilisés pour vous connecter à d’autres applications, telles que Power BI. Pour plus d’informations sur la création d’utilisateurs dans le centre d’administration Microsoft 365, accédez à [Ajouter des utilisateurs dans le centre d’administration Microsoft](/microsoft-365/admin/add-users/add-users).

Votre abonnement à [!INCLUDE[prod_short](includes/prod_short.md)] en ligne définit le nombre de licences utilisateurs [!INCLUDE[prod_short](includes/prod_short.md)] autorisés. Les utilisateurs sont ajoutés à votre abonné dans l’Espace partenaires Microsoft, généralement par votre partenaire Microsoft. Pour plus d’informations, voir [Administration de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Vous attribuez des licences aux utilisateurs en fonction du travail que chacun effectue dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous disposez de plusieurs façons pour attribuer des licences :

- L’administrateur Microsoft 365 de votre société peut le faire dans le [Centre d’administration Microsoft 365](https://admin.microsoft.com). Pour plus d’informations, voir [Ajouter des utilisateurs individuellement ou en bloc à Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Un partenaire Microsoft peut attribuer des licences dans le Centre d’administration Microsoft 365 ou l’Espace partenaires Microsoft. Pour plus d’informations, voir [Tâches de gestion des utilisateurs pour les comptes clients](/partner-center/assign-licenses-to-users) dans l’aide de l’Espace partenaires Microsoft.

Pour plus d’informations, voir [Administration de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) dans l’aide dédiée à l’administration.

Une fois les comptes utilisateur créés dans le centre d’administration Microsoft 365, il existe deux façons de les importer dans Business Central :

- Un compte d’utilisateur est importé automatiquement quand l’utilisateur se connecte à [!INCLUDE [prod_short](includes/prod_short.md)] pour la première fois.

- L’administrateur peut importer des utilisateurs en sélectionnant l’action  **Mettre à jour les utilisateurs à partir de Microsoft 365**  sur la page **Utilisateurs* .

Les deux approches ont leurs propres avantages et vous pouvez les utiliser simultanément. Chaque approche permet aux administrateurs de configurer de manière proactive [!INCLUDE [prod_short](includes/prod_short.md)] pour attribuer les autorisations de démarrage, les groupes d’utilisateurs et les profils d’utilisateurs. L’utilisation de l’action **Mettre à jour les utilisateurs depuis Microsoft 365** donne aux administrateurs plus de contrôle pour ajuster les autorisations, les groupes d’utilisateurs et les profils. C’est une approche idéale quand vous configurez [!INCLUDE [prod_short](includes/prod_short.md)] pour la première fois, avant que des utilisateurs ne se connectent ou au moment de l’ajout d’une nouvelle équipe d’utilisateurs.

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

Les administrateurs peuvent configurer des ensembles d’autorisations et des groupes d’utilisateurs pour chaque licence.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Par exemple, la licence couramment utilisée, *Membre de l’équipe Dynamics 365 Business Central*, possède les ensembles d’autorisations suivants par défaut :

- LIRE D365
- MEMBRE D’ÉQUIPE D365
- MODIFIER DANS EXCEL - AFFICHER
- EXPORTER ÉTAT EXCEL
- LOCAL

D’autres ensembles d’autorisations sont ajoutés automatiquement en fonction des groupes d’utilisateurs affectés à la licence. Au moment de la création d’un utilisateur basé sur cette licence, [!INCLUDE[prod_short](includes/prod_short.md)] attribue les ensembles d’autorisations provenant des groupes d’utilisateurs et les ensembles d’autorisations de la licence. Les mêmes autorisations de démarrage sont attribuées à l’utilisateur si son compte utilisateur a été créé automatiquement dans [!INCLUDE[prod_short](includes/prod_short.md)] ou si l’administrateur a utilisé l’action **Mettre à jour les utilisateurs à partir de Microsoft 365** sur la page **Utilisateurs**.

Si cette configuration par défaut n’est pas la bonne pour un environnement particulier, l’administrateur peut modifier cette configuration. Cependant, les autorisations personnalisées n’affecteront que les nouveaux utilisateurs auxquels cette licence est attribuée. Les autorisations des utilisateurs existants auxquels la licence est attribuée ne sont pas affectées.  

1. Connectez-vous à [!INCLUDE[prod_short](includes/prod_short.md)] en tant qu’administrateur.  
2. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration de licence**, puis sélectionnez le lien associé.  

    <!--Alternatively, if you're already in the **Users** page, you can run the **Update Users from Microsoft 365** guide, and then, on the first page of the guide, choose the **Configure permissions per license** link.-->  
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

> [!IMPORTANT]  
> L’exécution de la synchronisation des utilisateurs depuis Microsoft 365 à l’aide du guide **Mettre à jour les utilisateurs depuis Microsoft 365** , nécessite l’ensemble d’autorisations SUPER.

> [!NOTE]
> Le guide **Mettre à jour les utilisateurs de Microsoft 365** ne met pas à jour les utilisateurs auxquels aucune licence n’a été attribuée, comme une personne qui est administrateur général et administrateur Dynamics 365. Ces utilisateurs mettront à jour la prochaine fois qu’ils se connecteront à l’environnement.

L’étape suivante pour les utilisateurs récemment créés, l’étape suivante consiste à attribuer des groupes d’utilisateurs et des autorisations. Pour plus d’informations, accédez à [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md). Si vous mettez à jour un utilisateur et que la mise à jour inclut un changement de licence, les utilisateurs sont affectés au groupe d’utilisateurs approprié et leurs ensembles d’autorisations sont mis à jour. Pour plus d’informations, voir [Pour gérer les autorisations via les groupes d’utilisateurs](ui-define-granular-permissions.md).  

> [!NOTE]
> Tous les utilisateurs d’un environnement doivent être affectés à la même licence, Essentials ou Premium. Pour plus d’informations sur les licences, accédez au site web [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Pour en savoir plus sur la synchronisation des informations utilisateur avec Microsoft 365, voir la section [Synchronisation avec Microsoft 365](#m365).

> [!NOTE]
> Si vous utilisez un comptable externe pour gérer votre comptabilité et vos états financiers, vous pouvez les inviter à votre [!INCLUDE[prod_short](includes/prod_short.md)] afin qu’ils puissent travailler vous et utiliser vos données fiscales. Pour plus d’informations, voir [Inviter votre comptable externe dans votre Business Central](finance-accounting.md#inviteaccountant).

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

Dans les deux cas, plusieurs paramètres sont appliqués automatiquement. Ces paramètres sont répertoriés dans les deuxième et troisième colonnes du tableau ci-dessous.

Si vous modifiez les informations utilisateur dans Microsoft 365, vous pouvez mettre à jour [!INCLUDE[prod_short](includes/prod_short.md)] pour refléter le changement. Selon ce que vous souhaitez mettre à jour, utilisez l’une des actions sur la page **Utilisateurs**. Les actions sont décrites dans les deux dernières colonnes du tableau ci-dessous.

|Ce qui se produit dans les cas suivants :|Premier utilisateur, première connexion|Mettre à jour les utilisateurs à partir de Microsoft 365|Restaurer les groupes d’utilisateurs par défaut de l’utilisateur|
|-|-|-|-|
|Portée :|Utilisateur actuel|Plusieurs utilisateurs sélectionnés|Un seul utilisateur sélectionné (sauf l’utilisateur actuel)|
|Créez le nouvel utilisateur et attribuez le jeu d’autorisations SUPER.<br /><br /><!--Platform-->|**X**|**X** | | 
|Mettez à jour l’utilisateur en fonction des informations dans Microsoft 365 : Statut, Nom complet, E-mail du contact, adresse e-mail d’authentification.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|
|Synchronisez les plans utilisateur (licences) avec les licences et les rôles attribués dans Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|
|Ajoutez l’utilisateur aux groupes d’utilisateurs en fonction des plans utilisateur actuels. Supprimez l’ensemble d’autorisations SUPER pour tous les utilisateurs autres que le premier utilisateur à se connecter et les [administrateurs](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Au moins une autorisation SUPER est requise.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**<br /><br />Supprime manuellement les groupes d’utilisateurs et les autorisations affectés.|

Les utilisateurs peuvent accéder aux enregistrements de [!INCLUDE[prod_short](includes/prod_short.md)] dans Teams uniquement à l’aide de leur licence Microsoft 365. Quand l’accès est activé pour un environnement, la synchronisation à l’aide de l’action **Mettre à jour les utilisateurs à partir de Microsoft 365** n’inclut pas les utilisateurs qui ne disposent que d’une licence Microsoft 365. Pour inclure ces utilisateurs dans la synchronisation, vous devez d’abord mettre à jour les paramètres d’environnement en attribuant un groupe de sécurité qui contient des utilisateurs avec une licence [!INCLUDE[prod_short](includes/prod_short.md)] et des utilisateurs avec seulement une licence Microsoft 365.

Découvrez comment sécuriser l’accès aux environnements à l’aide de groupes de sécurité sur [Gérer l’accès à l’aide de groupes Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

Obtenez un aperçu de l’accès à [!INCLUDE[prod_short](includes/prod_short.md)] dans Teams avec des licences Microsoft 365 sur [admin-access-with-m365-license](admin-access-with-m365-license.md).

## <a name="manage-users-and-licenses-in-on-premises-deployments"></a>Gérer des utilisateurs et des licences dans les déploiements sur site

Pour les déploiements sur site, le nombre de licences utilisateur est spécifié dans le fichier de licence (.bclicense ou .flf). Lorsqu’un administrateur ou un partenaire Microsoft télécharge le fichier de licence, il peut spécifier les utilisateurs qui peuvent se connecter à [!INCLUDE[prod_short](includes/prod_short.md)].

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
