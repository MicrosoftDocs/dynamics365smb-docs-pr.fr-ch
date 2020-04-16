---
title: Affecter ou modifier des autorisations d'utilisateur | Microsoft Docs
description: Décrit comment ajouter des utilisateurs d'Office 365 à Business Central, puis affecte des autorisations, des droits d'accès, et des paramètres de sécurité.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7509b60a72ee520d7adcd739034e23326882daf1
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195546"
---
# <a name="create-users-according-to-licenses"></a>Créer des utilisateurs en fonction des licences
Cette rubrique décrit comment les administrateurs créent des utilisateurs et définissent qui peut se connecter à [!INCLUDE[d365fin](includes/d365fin_md.md)] et les autorisations accordées à différents types d’utilisateurs selon les licences.

Lorsque vous créez des utilisateurs dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez leur attribuer des autorisations spécifiques au moyen d'ensembles d'autorisations et organiser les utilisateurs en groupes. Les groupes d'utilisateurs facilitent la gestion simultanée des autorisations pour plusieurs utilisateurs. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).  

> [!NOTE]
> Le processus de gestion des utilisateurs et des licences varie selon que [!INCLUDE[d365fin](includes/d365fin_md.md)] est déployé en ligne ou sur site. Par exemple, dans les déploiements en ligne, vous pouvez gérer les utilisateurs uniquement après leur ajout à [!INCLUDE[d365fin](includes/d365fin_md.md)] depuis Office 365. Dans les déploiements sur site, vous pouvez créer, modifier et supprimer directement des utilisateurs.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Gestion des utilisateurs et des licences dans les déploiements en ligne
Dans la version en ligne de [!INCLUDE[d365fin](includes/d365fin_md.md)], le nombre d'utilisateurs est défini par l'abonnement et ajouté à votre abonné dans l'Espace partenaires Microsoft, généralement par votre partenaire Microsoft. Pour plus d'informations, voir [Ajouter un nouveau client](https://docs.microsoft.com/partner-center/add-a-new-customer) et [Créer, suspendre ou annuler des abonnements clients](https://docs.microsoft.com/partner-center/create-a-new-subscription) dans l'aide de l'Espace partenaires Microsoft.

Pour définir qui peut se connecter à [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez attribuer des licences de produit aux utilisateurs en fonction des rôles qu’ils vont jouer dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cela peut être fait des manières suivantes :
- L'administrateur Office 365 de votre société peut le faire dans le [Centre d'administration Microsoft 365](https://admin.microsoft.com). Pour plus d'informations, voir [Ajouter des utilisateurs individuellement ou en bloc à Office 365](https://aka.ms/CreateOffice365Users).  
- Un partenaire Microsoft peut attribuer des licences dans le Centre d'administration Microsoft 365 ou l'Espace partenaires Microsoft. Pour plus d'informations, voir [Tâches de gestion des utilisateurs pour les comptes clients](https://docs.microsoft.com/partner-center/assign-licenses-to-users) dans l'aide de l'Espace partenaires Microsoft.

Pour en savoir plus, consultez [Administration de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) dans l'aide sur Developer and IT Pro.

Une fois une licence [!INCLUDE[d365fin](includes/d365fin_md.md)] attribuée aux utilisateurs dans Office 365, vous pouvez les importer dans la page **Utilisateurs** dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide de l'action **Obtenir de nouveaux utilisateurs à partir d'Office 365**.

### <a name="to-add-a-user-or-update-user-information-in-business-central"></a><a name="adduser"></a>Pour ajouter un utilisateur ou mettre à jour les informations utilisateur dans Business Central
Utilisez des fonctions d'importation dédiées pour ajouter de nouveaux utilisateurs ou mettre à jour les informations utilisateur dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à partir du Centre d'administration Microsoft 365.  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
2. Selon ce que vous souhaitez faire, choisissez l'action **Obtenir de nouveaux utilisateurs à partir d'Office 365** ou **Mettre à jour les utilisateurs à partir d'Office 365**.

Les nouveaux utilisateurs et les nouvelles informations utilisateur dans votre abonnement Office 365 sont ajoutés à la page **Utilisateurs** dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour en savoir plus sur la synchronisation des informations utilisateur avec Office 365, consultez [Synchronisation avec Office 365](ui-how-users-permissions.md#synchronization-with-office-365).

> [!NOTE]
> Si vous utilisez un comptable externe pour gérer votre comptabilité et vos états financiers, vous pouvez les inviter dans votre Business Central afin qu'ils puissent travailler avec vous et utiliser vos données fiscales. Pour plus d'informations, voir [Inviter votre comptable externe dans votre Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-remove-a-users-access-to-the-system"></a>Pour supprimer l'accès d'un utilisateur au système
Dans les déploiements en ligne, vous pouvez supprimer l'accès d'un utilisateur à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Toutes les références à l'utilisateur sont conservées, mais il ne peut plus se connecter et ses sessions actives sont arrêtées.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
2. Ouvrez la page **Fiche utilisateur** pour l'utilisateur concerné, puis, dans le champ **État**, sélectionnez **Désactivé**.
3. Pour donner à nouveau accès à l'utilisateur, définissez le paramètre du champ **État** sur **Activé**.

Vous pouvez également supprimer la licence d'un utilisateur dans le Centre d'administration Microsoft 365. L'utilisateur ne peut alors plus se connecter. Pour en savoir plus, consultez [Supprimer des licences d'utilisateurs](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Pour changer la licence attribuée à un utilisateur
Parfois, vous devrez peut-être modifier la licence attribuée à un utilisateur. Par exemple, si vous décidez d'utiliser le module Gestion des services et que vous devez par conséquent mettre à niveau toutes les licences Essential vers Premium. Ou si la responsabilité d'un utilisateur a changé et que vous devez remplacer une licence de membre d'équipe par Essential.

1. Changez la licence dans le Centre d'administration Microsoft 365. Pour plus d'informations, voir [Ajouter des utilisateurs individuellement ou en bloc à Office 365](https://aka.ms/CreateOffice365Users).
2. Connectez-vous à [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant qu'administrateur.
3. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
4. Sur la page **Utilisateurs**, sélectionnez l'action **Restaurer les groupes d'utilisateurs par défaut de l'utilisateur**.

Les utilisateurs sont déplacés vers un groupe d'utilisateurs approprié et les ensembles d'autorisations sont mis à jour. Pour plus d'informations, voir [Pour gérer les autorisations via les groupes d'utilisateurs](ui-define-granular-permissions.md).

> [!NOTE]
> Tous les utilisateurs doivent être affectés à la même licence, Essential ou Premium. Pour en savoir plus, consultez le guide des licences Microsoft Dynamics 365 Business Central. Le guide est téléchargeable sur le site Internet [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/).

### <a name="synchronization-with-office-365"></a>Synchronisation avec Office 365
Lorsque vous attribuez une licence [!INCLUDE[d365fin](includes/d365fin_md.md)] à un utilisateur dans Office 365, il existe deux façons de créer l'utilisateur dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. 

* L'administrateur peut ajouter l'utilisateur en sélectionnant l'action **Mettre à jour les utilisateurs à partir d'Office 365** sur la page **Utilisateurs**.
* Les informations de licence sont mises à jour automatiquement lors de la première connexion de l'utilisateur.

Dans les deux cas, plusieurs paramètres sont configurés automatiquement. Ceux-ci sont répertoriés dans les deuxième et troisième colonnes du tableau ci-dessous.

Si vous modifiez les informations utilisateur dans Office 365, vous pouvez mettre à jour [!INCLUDE[d365fin](includes/d365fin_md.md)] pour refléter le changement. Selon ce que vous souhaitez mettre à jour, utilisez l'une des actions sur la page **Utilisateurs**. Les actions sont décrites dans les trois dernières colonnes du tableau ci-dessous.

|Ce qui se produit dans les cas suivants :|Premier utilisateur, première connexion|Récupérer des utilisateurs à partir de Office 365|Mettre à jour les utilisateurs à partir de Office 365|Restaurer les groupes d'utilisateurs par défaut de l'utilisateur|Actualiser les groupes d'utilisateurs|
|-|-|-|-|-|-|
|Portée :|Utilisateur actuel|Nouveaux utilisateurs dans Office 365|Plusieurs utilisateurs sélectionnés|Un seul utilisateur sélectionné (sauf l'utilisateur actuel)|Plusieurs utilisateurs sélectionnés|
|Créez le nouvel utilisateur et attribuez le jeu d'autorisations SUPER.<br /><br /><!--Platform-->|**X**|| | | |
|Mettez à jour l'enregistrement utilisateur en fonction des informations réelles dans Office 365 : État, Nom complet, E-mail du contact, E-mail d'authentification.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**| |
|Synchronisez les plans utilisateur (licences) avec les licences et les rôles attribués dans Office 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**| |**X**|**X**|
|Ajoutez l'utilisateur aux groupes d'utilisateurs en fonction des plans utilisateur actuels. Supprimez l'ensemble d'autorisations SUPER pour tous les utilisateurs autres que le premier utilisateur à se connecter et les [administrateurs](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Au moins une autorisation SUPER est requise.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**| |**X**<br /><br />Supprime manuellement les groupes d'utilisateurs et les autorisations affectés.|**X**<br /><br />Mettez à jour les affectations des groupes d'utilisateurs.|

## <a name="the-device-license"></a>Licence d'appareil
La licence d'appareil Dynamics 365 Business Central permet à plusieurs utilisateurs d'utiliser simultanément un appareil couvert par la licence. Par exemple, il peut s'agir d'un appareil de point de vente, d'atelier ou d'entrepôt. Lorsque vous avez acheté un certain nombre de licences d'appareils, jusqu'à ce nombre d'utilisateurs affectés au groupe Utilisateurs d'appareils Dynamics 365 Business Central peuvent se connecter simultanément. Pour en savoir plus, consultez le guide des licences Microsoft Dynamics 365 Business Central. Le guide est téléchargeable sur le site Internet [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/).

L'administrateur Office 365 ou le partenaire Microsoft de votre société peut créer le groupe Utilisateurs d'appareils Dynamics 365 Business Central et ajouter des utilisateurs d'appareils en tant que membres dans le [Centre d'administration Microsoft 365](https://admin.microsoft.com/) ou sur le [Portail Azure](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Restrictions pour l'utilisateur d'appareil
Les utilisateurs disposant de la licence d'appareil ne peuvent pas effectuer les tâches suivantes dans [!INCLUDE[d365fin](includes/d365fin_md.md)] :

- Configurer des travaux pour qu'ils s'exécutent en tant que tâches planifiées dans la file d'attente des travaux. Les utilisateurs d'appareils sont des utilisateurs simultanés et, par conséquent, nous ne pouvons pas garantir que l'utilisateur impliqué est présent dans le système lorsqu'une tâche est exécutée, ce qui est obligatoire.

- Un utilisateur d'appareil ne peut pas être le premier utilisateur à se connecter. Un utilisateur de type Administrateur, Utilisateur complet ou Comptable externe doit se connecter en premier afin de pouvoir configurer [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Administrateurs](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Pour créer un groupe d'utilisateurs d'appareils Dynamics 365 Business Central
1. Dans le Centre d'administration Microsoft 365, accédez à la page **Groupes**.
2. Choisissez l'action **Ajouter un groupe**.
3. Sur la page **Choisir un type de groupe**, choisissez l'action **Sécurité**, puis l'action **Ajouter**.
4. Sur la page **Bases**, saisissez **Utilisateurs d'appareils Dynamics 365 Business Central** comme nom du groupe.
  
   >[!Note]
   >Le nom du groupe doit être orthographié en anglais exactement comme indiqué à l'étape 4, même si vous utilisez une autre langue.
5. Cliquez sur le bouton **Fermer**.

> [!NOTE]
> Vous pouvez également créer un groupe de type Office 365. Pour plus d'informations, voir [Comparer des groupes](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Pour ajouter des membres au groupe
1. Dans le Centre d'administration Microsoft 365, actualisez la page **Groupes** pour faire apparaître votre nouveau groupe.
2. Sélectionnez le groupe **Utilisateurs d'appareils Dynamics 365 Business Central**, puis choisissez l'action **Afficher tout et gérer les membres**.
3. Choisissez l'action **Ajouter des membres**.
4. Sélectionnez les utilisateurs que vous souhaitez ajouter, puis choisissez le bouton **Enregistrer**.
5. Cliquez trois fois sur le bouton **Fermer**.

Vous pouvez ajouter autant d'utilisateurs que vous souhaitez au Groupe d'utilisateurs d'appareils Dynamics 365 Business Central. Cependant, le nombre d'appareils auxquels les utilisateurs peuvent se connecter simultanément est défini par le nombre de licences d'appareils achetées.

> [!NOTE]
> Vous n'avez pas besoin d'attribuer une licence [!INCLUDE[d365fin](includes/d365fin_md.md)] aux utilisateurs qui sont membres du Groupe d'utilisateurs d'appareils Dynamics 365 Business Central.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Gestion des utilisateurs et des licences dans les déploiements sur site
Pour les déploiements sur site, le nombre de licences utilisateur est spécifié dans le fichier de licence (.flf). Lorsqu'un administrateur ou un partenaire Microsoft télécharge le fichier de licence, l'administrateur peut spécifier les utilisateurs qui peuvent se connecter à [!INCLUDE[d365fin](includes/d365fin_md.md)].

Pour les déploiements sur site, l’administrateur crée, édite et supprime les utilisateurs directement à partir de la page **Utilisateurs**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Pour modifier ou supprimer un utilisateur dans un déploiement sur site
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
2. Sélectionnez l'utilisateur que vous souhaitez modifier, puis choisissez l'action **Modifier**.
3. Sur la page **Fiche utilisateur**, modifiez les informations si nécessaire.    
4. Pour supprimer un utilisateur, sélectionnez l'utilisateur que vous souhaitez supprimer, puis choisissez l'action **Supprimer**.

> [!NOTE]
> Pour les déploiements sur site, un administrateur peut spécifier comment authentifier les informations d'identification de l'utilisateur dans l'instance [!INCLUDE[server](includes/server.md)]. Lorsque vous créez un utilisateur, vous fournissez le type d'informations d'identification que vous utilisez.<br /><br />
> Pour en savoir plus, consultez [Authentification et types d'informations d'identification](/dynamics365/business-central/dev-itpro/administration/users-credential-types) dans la section Administration du contenu Developer and IT Pro de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Voir aussi
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  
[Gérer les profils](admin-users-profiles-roles.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Ajouter des utilisateurs à Office 365 pour les entreprises](https://aka.ms/CreateOffice365Users)  
[Sécurité et protection dans Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) dans l'aide sur Developer and IT-Pro
