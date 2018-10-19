---
title: "Gérer les utilisateurs et les rôles | Microsoft Docs"
description: "Découvrez comment gérer les utilisateurs et les tableaux de bord dans Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a>Comprendre les utilisateurs, les profils et les tableaux de bord

Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les utilisateurs sont ajoutés par un administrateur qui permet également aux utilisateurs d'accéder aux zones de [!INCLUDE[d365fin](includes/d365fin_md.md)] qu'ils ont besoin dans leur travail.  

L'accès aux fonctionnalités est géré via des *groupes d'utilisateurs* et des *profils*. En tant qu'administrateur, vous pouvez ajouter et supprimer des utilisateurs dans le cadre de votre abonnement [!INCLUDE[d365fin](includes/d365fin_md.md)], et vous pouvez affecter des autorisations aux utilisateurs par le biais des groupes d'utilisateurs.  

## <a name="adding-users"></a>Ajout d'utilisateurs

Pour ajouter des utilisateurs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] online, l'administrateur Office 365 de votre société doit d'abord créer les utilisateurs dans le centre d’administration Office 365. Pour plus d'informations, voir [Ajouter des utilisateurs à Office 365 for business](https://aka.ms/CreateOffice365Users).

Ensuite, l'administrateur peut affecter des autorisations à chaque utilisateur et groupe d'utilisateurs. Pour plus d'informations, voir [Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md).  

### <a name="users-of-on-premises-deployments"></a>Utilisateurs des déploiements sur site

Pour les déploiements sur site de [!INCLUDE[d365fin](includes/d365fin_md.md)], l'administrateur peut choisir entre différents mécanismes d'autorisation d'identification pour les utilisateurs. Ensuite, lorsque vous créez un utilisateur, vous devez fournir différentes informations selon le type d'identification utilisé dans l'instance de [!INCLUDE[server](includes/server.md)] spécifique. Pour plus d'informations, voir [Authentification et informations d'identification](/dynamics365/business-central/dev-itpro/administration/users-credential-types) dans la section Administration du contenu pour développeurs et professionnels de l'informatique de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profils

Un *profil* est affecté à tous les employés de votre société ayant accès à [!INCLUDE[d365fin](includes/d365fin_md.md)], qui leur permet d'accéder à un *Tableau de bord*.

Les profils sont des collections d'utilisateurs [!INCLUDE[d365fin](includes/d365fin_md.md)] qui partagent le même tableau de bord. Un tableau de bord est le point d'entrée et la page d'accueil de [!INCLUDE[d365fin](includes/d365fin_md.md)] qui vous permet d'accéder rapidement à vos tâches les plus importantes et d'afficher diverses informations et divers indicateurs de performance clés sur votre travail.  

> [!NOTE]  
>  Dans la version actuelle de [!INCLUDE[d365fin](includes/d365fin_md.md)] online, vous ne pouvez ni ajouter, ni modifier, ni supprimer des profils.  

## <a name="configuration-and-personalization"></a>Configuration et personnalisation
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
Les utilisateurs personnalisent l'interface utilisateur de leur version personnelle en personnalisant l'interface utilisateur sous leur propre identifiant utilisateur. Cette personnalisation peut être supprimée par l'administrateur. Pour plus d'informations, voir [Personnalisation de votre espace de travail](ui-personalization-user.md).  

## <a name="see-also"></a>Voir aussi  
[Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md)  
[Gérer la personnalisation en tant qu'administrateur](ui-personalization-manage.md)  
[Personnalisation de votre espace de travail](ui-personalization-user.md)  

