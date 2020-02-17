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
ms.date: 01/06/2020
ms.author: sgroespe
ms.openlocfilehash: e07636b6211eb57205d41d982bfbfb4bc2d5b330
ms.sourcegitcommit: 0cb8a646dcba8f6d6336ebd008587874d25f4629
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030067"
---
# <a name="create-users-according-to-licenses"></a>Créer des utilisateurs en fonction des licences
La section suivante explique comment, en tant qu’administrateur, créer des utilisateurs et définir qui peut se connecter à [!INCLUDE[d365fin](includes/d365fin_md.md)], et quels droits fondamentaux différents types d’utilisateurs ont selon les licences.

Lorsque les utilisateurs sont créés dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez procéder à l’affectation d’autorisations spécifiques à des utilisateurs via des ensembles d’autorisations et à leur organisation en groupes d’utilisateurs pour faciliter la gestion des autorisations. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).  

> [!NOTE]
> Le processus de gestion des utilisateurs et des licences varie selon que votre solution est déployée en ligne ou sur site. Par exemple, dans les déploiements en ligne, vous pouvez uniquement désactiver et activer un utilisateur ajouté une fois à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dans les déploiements sur site, vous pouvez créer, modifier et supprimer des utilisateurs.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Gestion des utilisateurs et des licences dans les déploiements en ligne
Dans [!INCLUDE[d365fin](includes/d365fin_md.md)]en ligne, le nombre d'utilisateurs est défini par l'abonnement et ajouté à votre abonné dans l'Espace partenaires Microsoft, généralement par votre partenaire Microsoft. Pour plus d'informations, voir [Ajouter un nouveau client ](https://docs.microsoft.com/partner-center/add-a-new-customer)et [Créer, suspendre ou annuler des abonnements clients ](https://docs.microsoft.com/partner-center/create-a-new-subscription)dans l'aide de l'Espace partenaires Microsoft.

Pour définir qui peut se connecter à [!INCLUDE[d365fin](includes/d365fin_md.md)], les licences de produit doivent être attribuées aux utilisateurs en fonction des rôles qu’ils vont jouer dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cela peut être fait des manières suivantes :
- L'administrateur Office 365 de votre société peut le faire dans le [Centre d'administration Microsoft 365](https://admin.microsoft.com). Pour plus d'informations, voir [Ajouter des utilisateurs individuellement ou en bloc à Office 365](https://aka.ms/CreateOffice365Users).  
- Un partenaire Microsoft peut attribuer des licences dans le Centre d'administration Microsoft 365 ou l'Espace partenaires Microsoft. Pour plus d'informations, voir [Tâches de gestion des utilisateurs pour les comptes clients ](https://docs.microsoft.com/partner-center/assign-licenses-to-users) dans l'aide de l'Espace partenaires Microsoft.

Pour plus d'informations, voir [Administration de Business Central Online ](/dynamics365/business-central/dev-itpro/administration/tenant-administration)dans Aide dédiée à l'équipe IT et aux développeurs.

Une fois les utilisateurs disposant d'une licence [!INCLUDE[d365fin](includes/d365fin_md.md)] créés dans Office 365, ils peuvent être importés dans la page **Utilisateurs** dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide de l'action **Obtenir de nouveaux utilisateurs à partir de Office 365**.

### <a name="to-add-a-user-in-business-central"></a>Pour ajouter un utilisateur dans Business Central
Pour ajouter des utilisateurs à partir du Centre d’administration Microsoft 365 à [!INCLUDE[d365fin](includes/d365fin_md.md)] en ligne, vous utilisez une fonction d'importation dédiée.  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
2. Choisissez l'action **Obtenir de nouveaux utilisateurs à partir de Office 365**.

Tout nouvel utilisateur créé pour votre abonnement Office 365 est ajouté à la page **Utilisateurs**. Des ensembles d'autorisations sont affectés aux utilisateurs selon la licence qui leur est affectée dans Office 365. Vous pouvez ensuite affecter des autorisations plus détaillées aux utilisateurs et les organiser en groupes d'utilisateurs pour faciliter la gestion des autorisations. Pour en savoir plus, voir [Pour affecter des ensembles d'autorisations à des utilisateurs](ui-define-granular-permissions.md#to-assign-permission-sets-to-users).

> [!NOTE]
> Si vous utilisez un comptable externe pour gérer votre comptabilité et vos états financiers, vous pouvez les inviter dans votre Business Central afin qu'ils puissent travailler avec vous et utiliser vos données fiscales. Pour plus d'informations, voir [Inviter votre comptable externe dans votre Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-remove-a-users-access-to-the-system"></a>Pour supprimer l'accès d'un utilisateur au système
Dans les déploiement en ligne, vous pouvez supprimer l'accès d'un utilisateur au système en définissant le champ **État** sur **Désactivé**. Toutes les références à l'utilisateur seront conservées, mais il ne pourra plus se connecter au système et ses sessions actives seront terminées.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
2. Ouvrez la page **Fiche utilisateur** pour l'utilisateur concerné, puis, dans le champ **État**, sélectionnez **Désactivé**.
3. Pour donner à nouveau accès à l'utilisateur, définissez le paramètre du champ **État** sur **Activé**.

En plus de désactiver un utilisateur, vous pouvez annuler l'attribution de la licence d'un utilisateur dans le Centre d'administration Microsoft 365. L'utilisateur ne peut alors plus se connecter. Pour plus d'informations, voir [Annuler l'attribution de licences aux utilisateurs ](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Pour changer la licence attribuée à un utilisateur
Parfois, vous devrez peut-être modifier la licence attribuée à un utilisateur. Par exemple, si vous décidez d'utiliser le module Gestion des services et que vous devez par conséquent mettre à niveau toutes les licences Essential vers Premium. Ou si la responsabilité d'un utilisateur a changé et que vous devez remplacer une licence de membre d'équipe par Essential.

1. Changez la licence dans le Centre d'administration Microsoft 365. Pour plus d'informations, voir [Ajouter des utilisateurs individuellement ou en bloc à Office 365](https://aka.ms/CreateOffice365Users).
2. Connectez-vous à [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant qu'administrateur.
3. Choisissez l'icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
4. Sur la page **Utilisateurs**, sélectionnez l'action **Restaurer les groupes d'utilisateurs par défaut de l'utilisateur**.

Les utilisateurs sont déplacés vers un groupe d'utilisateurs approprié et les ensembles d'autorisations sont mis à jour. Pour plus d'informations, voir [Pour gérer les autorisations via les groupes d'utilisateurs](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Tous les utilisateurs réguliers d'une solution doivent se voir attribuer la même licence, Essential ou Premium.
> Pour obtenir des informations sur la gestion des licences, voir [Guide des licences Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

### <a name="synchronization-with-office-365"></a>Synchronisation avec Office 365
Lorsqu'une licence est attribuée à un utilisateur dans Office 365, il existe deux façons de créer l'utilisateur dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le système le fait automatiquement lorsque l'utilisateur se connecte pour la première fois, ou l'administrateur peut ajouter l'utilisateur en choisissant l'action **Récupérer des utilisateurs à partir de Office 365** dans la page **Utilisateurs**.

Dans les deux cas, plusieurs paramètres supplémentaires sont configurés automatiquement. Ceux-ci sont répertoriés dans les deuxième et troisième colonnes du tableau ci-dessous.

Si vous modifiez par la suite l'utilisateur dans Office 365 et si vous devez synchroniser les modifications dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez effectuer différentes actions sur la page **Utilisateurs** en fonction de ce que vous souhaitez synchroniser. Celles-ci sont répertoriées dans les trois dernières colonnes du tableau ci-dessous.

|Ce qui se produit dans les cas suivants :|Première connexion|Récupérer des utilisateurs à partir de Office 365|Mettre à jour les utilisateurs à partir de Office 365|Restaurer les groupes d'utilisateurs par défaut de l'utilisateur|Actualiser les groupes d'utilisateurs|
|-|-|-|-|-|-|
|Portée :|Utilisateur actuel|Nouveaux utilisateurs dans Office 365|Plusieurs utilisateurs sélectionnés|Un seul utilisateur sélectionné (sauf l'utilisateur actuel)|Plusieurs utilisateurs sélectionnés|
|Créez le nouvel utilisateur et attribuez le jeu d'autorisations SUPER.<br /><br />Plateforme|**X**|**X**| | | |
|Mettez à jour l'enregistrement utilisateur en fonction des informations réelles dans Office 365 : État, Nom complet, E-mail du contact, E-mail d'authentification.<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph|**X**|**X**|**X**|**X**| |
|Synchronisez les plans utilisateur (licences) avec les licences et les rôles attribués dans Office 365.<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans|**X**|**X**| |**X**|**X**|
|Ajoutez l'utilisateur aux groupes d'utilisateurs en fonction des plans utilisateur actuels. Révoquez l'ensemble d'autorisations SUPER. (Au moins une autorisation SUPER est nécessaire. Ne révoquez pas à partir des [administrateurs](/dynamics365/business-central/dev-itpro/administration/tenant-administration).)<br /><br />Codeunit « Gestionnaire des autorisations ». AddUserToDefaultUserGroups|**X**|**X**| |**X**<br /><br />Remplacement : supprimez l'utilisateur des autres groupes. Supprimez manuellement les ensembles d'autorisations attribués.|**X**<br /><br />Ajout : conservez l'appartenance actuelle au groupe d'utilisateurs et les ensembles d'autorisations attribués intacts. N'ajoutez un utilisateur aux groupes que si cela est nécessaire.|

## <a name="the-device-license"></a>Licence d'appareil
Avec la licence d'appareil Dynamics 365 Business Central, plusieurs utilisateurs peuvent utiliser un appareil sous licence avec la licence d'appareil pour employer un appareil de point de vente, un appareil d'atelier ou un appareil d'entrepôt. Pour plus d'informations, voir [Guide des licences Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

La licence d'appareil est implémentée comme un modèle d'utilisateur simultané. Lorsque vous avez acheté un nombre X de licences d'appareils, jusqu'à X utilisateurs du groupe désigné appelé Utilisateurs d'appareils Dynamics 365 Business Central peuvent se connecter simultanément.

Le partenaire Microsoft ou l'administrateur Office 365 de votre société doit créer le groupe d'appareils désigné et ajouter des utilisateurs d'appareils en tant que membres de ce groupe. Ils peuvent le faire dans le [Centre d'administration Microsoft 365](https://admin.microsoft.com/) ou sur le [Portail Azure](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Restrictions pour l'utilisateur d'appareil
Les utilisateurs disposant de la licence d'appareil ne peuvent pas effectuer les tâches suivantes dans [!INCLUDE[d365fin](includes/d365fin_md.md)] :

-   Configurer des travaux pour qu'ils s'exécutent en tant que tâches planifiées dans la file d'attente des travaux. Les utilisateurs d'appareils sont des utilisateurs simultanés et, par conséquent, nous ne pouvons pas garantir que l'utilisateur impliqué est présent dans le système lorsqu'une tâche est exécutée, ce qui est obligatoire.

-   Un utilisateur d'appareil ne peut pas être le premier utilisateur à se connecter. Un utilisateur de type Administrateur, Utilisateur complet ou Comptable externe doit se connecter en premier afin de pouvoir configurer [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Administrateurs](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Pour créer un groupe d'utilisateurs d'appareils Dynamics 365 Business Central
1.  Dans le Centre d'administration Microsoft 365, accédez à la page **Groupes**.
2.  Choisissez l'action **Ajouter un groupe**.
3.  Sur la page **Choisir un type de groupe**, choisissez l'action **Sécurité**, puis l'action **Ajouter**.
4.  Sur la page **Bases**, tapez *Utilisateurs d'appareils Dynamics 365 Business Central* comme nom du groupe.

    > [!Note]
    > Le nom du groupe doit être orthographié exactement comme ci-dessus, également dans une configuration non anglaise.
5. Cliquez sur le bouton **Fermer**.

> [!NOTE]
> Vous pouvez également créer un groupe de type Office 365. Pour plus d'informations, voir [Comparer des groupes](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Pour ajouter des membres au groupe
1.  Dans le Centre d'administration Microsoft 365, actualisez la page **Groupes** pour faire apparaître votre nouveau groupe.
2.  Sélectionnez le groupe **Utilisateurs d'appareils Dynamics 365 Business Central**, puis choisissez l'action **Afficher tout et gérer les membres**.
3.  Choisissez l'action **Ajouter des membres**.
4.  Sélectionnez les utilisateurs que vous souhaitez ajouter, puis choisissez le bouton **Enregistrer**.
5.  Cliquez trois fois sur le bouton **Fermer**.

Vous pouvez ajouter autant d'utilisateurs que vous souhaitez au Groupe d'utilisateurs d'appareils Dynamics 365 Business Central. Le nombre d'appareils auxquels les utilisateurs peuvent se connecter simultanément est défini par le nombre de licences d'appareils achetées.

> [!NOTE]
> Vous n'avez pas besoin d'attribuer une licence [!INCLUDE[d365fin](includes/d365fin_md.md)] aux utilisateurs qui sont membres du Groupe d'utilisateurs d'appareils Dynamics 365 Business Central.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Gestion des utilisateurs et des licences dans les déploiements sur site
Pour les déploiements sur site, un certain nombre d'utilisateurs sous licence est spécifié dans le fichier de licence (.flf). Lorsque l'administrateur ou le partenaire Microsoft télécharge le fichier de licence, l'administrateur peut spécifier les utilisateurs qui peuvent se connecter à [!INCLUDE[d365fin](includes/d365fin_md.md)].

Pour les déploiements sur site, l’administrateur crée, édite et supprime les utilisateurs directement à partir de la page **Utilisateurs**.

### <a name="to-edit-or-delete-a-user-on-premises"></a>Pour modifier ou supprimer un utilisateur sur site
1. Choisissez l'icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
2. Sélectionnez l'utilisateur que vous souhaitez modifier, puis choisissez l'action **Modifier**.
3. Sur la page **Fiche utilisateur**, modifiez les informations si nécessaire.    
4. Pour supprimer un utilisateur, sélectionnez l'utilisateur que vous souhaitez supprimer, puis choisissez l'action **Supprimer**.

> [!NOTE]
> Pour les déploiements sur site de [!INCLUDE[d365fin](includes/d365fin_md.md)], l'administrateur peut choisir entre différents mécanismes d'autorisation d'identification pour les utilisateurs. Ensuite, lorsque vous créez un utilisateur, vous devez fournir différentes informations selon le type d'identification utilisé dans l'instance de [!INCLUDE[server](includes/server.md)] spécifique.<br /><br />
> Pour plus d'informations, voir [Authentification et informations d'identification](/dynamics365/business-central/dev-itpro/administration/users-credential-types) dans la section Administration du contenu pour développeurs et professionnels de l'informatique de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Voir aussi
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  
[Gérer les profils](admin-users-profiles-roles.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Ajouter des utilisateurs à Office 365 for business](https://aka.ms/CreateOffice365Users)  
[Guide des licences Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing)  
[Sécurité et protection dans Business Central ](/dynamics365/business-central/dev-itpro/security/security-and-protection)dans Aide dédiée à l'équipe IT et aux développeurs
