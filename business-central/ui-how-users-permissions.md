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
ms.date: 11/07/2019
ms.author: sgroespe
ms.openlocfilehash: c64a14ed66668f8c3cbe09e8db3430a7dc25db5c
ms.sourcegitcommit: 2a6d629cf290645606356b714a77ef2872bdec64
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 11/07/2019
ms.locfileid: "2774834"
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

Une fois les utilisateurs disposant d'une licence [!INCLUDE[d365fin](includes/d365fin_md.md)] créés dans Office 365, ils peuvent être importés sur la page **Utilisateurs** dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide de l'action **Récupérer des utilisateurs à partir d'Office 365**.

### <a name="to-add-a-user-in-business-central"></a>Pour ajouter un utilisateur dans Business Central
Pour ajouter des utilisateurs à partir du Centre d’administration Microsoft 365 à [!INCLUDE[d365fin](includes/d365fin_md.md)] en ligne, vous utilisez une fonction d'importation dédiée.  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Obtenir les utilisateurs d'Office 365**.

Tout nouvel utilisateur créé pour votre abonnement Office 365 est ajouté à la page **Utilisateurs**. Des ensembles d'autorisations sont affectés aux utilisateurs selon la licence qui leur est affectée dans Office 365. Vous pouvez ensuite affecter des autorisations plus détaillées aux utilisateurs et les organiser en groupes d'utilisateurs pour faciliter la gestion des autorisations. Pour en savoir plus, voir [Pour affecter des ensembles d'autorisations à des utilisateurs](ui-define-granular-permissions.md#to-assign-permission-sets-to-users).

### <a name="to-remove-a-users-access-to-the-system"></a>Pour supprimer l'accès d'un utilisateur au système
Dans les déploiement en ligne, vous pouvez supprimer l'accès d'un utilisateur au système en définissant le champ **État** sur **Désactivé**. Toutes les références à l'utilisateur seront conservées, mais il ne pourra plus se connecter au système et ses sessions actives seront terminées.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
2. Ouvrez la page **Fiche utilisateur** pour l'utilisateur concerné, puis, dans le champ **État**, sélectionnez **Désactivé**.
3. Pour donner à nouveau accès à l'utilisateur, définissez le paramètre du champ **État** sur **Activé**.

En plus de désactiver un utilisateur, vous pouvez annuler l'attribution de la licence d'un utilisateur du Centre d'administration Office 365. L'utilisateur ne peut alors plus se connecter. Pour plus d'informations, voir [Annuler l'attribution de licences aux utilisateurs ](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Pour changer la licence attribuée à un utilisateur
Parfois, vous devrez peut-être modifier la licence attribuée à un utilisateur. Par exemple, si vous décidez d'utiliser le module Gestion des services et que vous devez par conséquent mettre à niveau toutes les licences Essential vers Premium. Ou si la responsabilité d'un utilisateur a changé et que vous devez remplacer une licence de membre d'équipe par Essential.

1. Changez la licence dans le Centre d'administration Office 365. Pour plus d'informations, voir [Ajouter des utilisateurs individuellement ou en bloc à Office 365](https://aka.ms/CreateOffice365Users).
2. Connectez-vous à [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant qu'administrateur.
3. Choisissez l'icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
4. Sur la page **Utilisateurs**, sélectionnez l'option **Actualiser tous les groupes d'utilisateurs**.
Les utilisateurs sont déplacés vers un groupe d'utilisateurs approprié et les ensembles d'autorisations sont mis à jour. Pour plus d'informations, voir [Pour gérer les autorisations via les groupes d'utilisateurs](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Tous les utilisateurs réguliers d'une solution doivent se voir attribuer la même licence, Essential ou Premium.
> Pour obtenir des informations sur la gestion des licences, voir [Guide des licences Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

## <a name="managing-users-and-licenses-in-online-deployments"></a>Gestion des utilisateurs et des licences dans les déploiements en ligne
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
