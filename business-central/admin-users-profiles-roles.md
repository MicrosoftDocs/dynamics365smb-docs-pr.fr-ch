---
title: Gérer les utilisateurs et les rôles | Microsoft Docs
description: Découvrez comment gérer les utilisateurs et les tableaux de bord dans Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc52d943938616041881c55f70c510e4c63b5de6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "925392"
---
# <a name="understanding-users-profiles-and-role-centers"></a>Comprendre les utilisateurs, les profils et les tableaux de bord

Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les utilisateurs sont ajoutés par un administrateur qui permet également aux utilisateurs d'accéder aux zones de [!INCLUDE[d365fin](includes/d365fin_md.md)] qu'ils ont besoin dans leur travail.  

L'accès aux fonctionnalités est géré via des *groupes d'utilisateurs* et des *profils*. En tant qu'administrateur, vous pouvez ajouter et supprimer des utilisateurs dans le cadre de votre abonnement [!INCLUDE[d365fin](includes/d365fin_md.md)], et vous pouvez affecter des autorisations aux utilisateurs par le biais des groupes d'utilisateurs.  

## <a name="adding-users"></a>Ajout d'utilisateurs

Pour ajouter des utilisateurs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] online, l'administrateur Office 365 de votre société doit d'abord créer les utilisateurs dans le centre d’administration Office 365. Pour plus d'informations, voir [Ajouter des utilisateurs à Office 365 for business](https://aka.ms/CreateOffice365Users).

Ensuite, l'administrateur peut affecter des autorisations à chaque utilisateur et groupe d'utilisateurs. Pour plus d'informations, voir [Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md).  

Les autorisations les plus puissantes qu'un utilisateur peut avoir est l'ensemble d'autorisations SUPER. Chaque société doit avoir au moins un utilisateur ayant cet ensemble d'autorisations, mais il est recommandé d'attribuer à chaque utilisateur des autorisations correspondant à leurs besoins de travail dans [!INCLUDE[prodshort](includes/prodshort.md)] et pas plus que cela. Cela permet de s'assurer que les utilisateurs ont uniquement accès aux données adéquates pour leur travail, par exemple.  

> [!TIP]
> Il est recommandé de vous assurer que l'administrateur Office 365 a également l'ensemble d'autorisations SUPER dans [!INCLUDE[prodshort](includes/prodshort.md)] car cela facilite de nombreuses tâches administratives, notamment la configuration de l'intégration à d'autres applications.

### <a name="users-of-on-premises-deployments"></a>Utilisateurs des déploiements sur site

Pour les déploiements sur site de [!INCLUDE[d365fin](includes/d365fin_md.md)], l'administrateur peut choisir entre différents mécanismes d'autorisation d'identification pour les utilisateurs. Ensuite, lorsque vous créez un utilisateur, vous devez fournir différentes informations selon le type d'identification utilisé dans l'instance de [!INCLUDE[server](includes/server.md)] spécifique. Pour plus d'informations, voir [Authentification et informations d'identification](/dynamics365/business-central/dev-itpro/administration/users-credential-types) dans la section Administration du contenu pour développeurs et professionnels de l'informatique de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profils

Un *profil* est affecté à tous les employés de votre société ayant accès à [!INCLUDE[d365fin](includes/d365fin_md.md)], qui leur permet d'accéder à un *Tableau de bord*.

Les profils sont des collections d'utilisateurs [!INCLUDE[d365fin](includes/d365fin_md.md)] qui partagent le même tableau de bord. Un tableau de bord est le point d'entrée et la page d'accueil de [!INCLUDE[d365fin](includes/d365fin_md.md)] qui vous permet d'accéder rapidement à vos tâches les plus importantes et d'afficher diverses informations et divers indicateurs de performance clés sur votre travail.  

> [!NOTE]  
>  Dans la version actuelle de [!INCLUDE[d365fin](includes/d365fin_md.md)] online, vous ne pouvez ni ajouter, ni modifier, ni supprimer des profils.  

### <a name="CreateProfile"></a>Créer un profil

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Liste des profils**, puis sélectionnez le lien connexe.  

2.  Sur la page **Liste des profils**, choisissez l'action **Nouveau** pour ouvrir la page **Fiche nouveau profil**.  

3.  Dans le champ **ID profil**, entrez un nom qui décrit le rôle prévu pour les utilisateurs.  

4.  Dans le champ **Description**, entrez une description de l'ID profil, par exemple, **Préparateur de la commande**.  

5.  Définissez le champ **ID Tableau de bord** sur le Tableau de bord à affecter au profil.  

La procédure à suivre pour modifier un profil existant est la même, à la différence près que vous sélectionnez un profil existant dans la page **Liste des profils** au lieu de choisir l'action **Nouveau**.  


### <a name="copy-a-profile"></a>Copier un profil
La copie d'un profil vous permet de gagner du temps si vous voulez utiliser des paramètres similaires pour un profil et modifier uniquement certains paramètres.

1.  Ouvrez le profil que vous voulez copier, puis sélectionnez l'action **Copier le profil**.

2.  Dans le champ **ID nouveau profil**, entrez un nom pour le profil que vous voulez copier.

3.  Définissez le champ **Portée du nouveau profil** comme l'un des éléments suivants :

    - **Système** pour rendre le nouveau profil disponible à toutes les bases de données d'abonné qui utilisent l'application.
    - **Abonné** pour rendre le nouveau profil disponible uniquement à la base de données actuelle de l'abonné.
4. Lorsque vous avez terminé, choisissez le bouton **OK**.

### <a name="ExportImportProfile"></a>Exporter et importer des profils

Vous pouvez exporter et importer des profils en tant que fichiers XML depuis et vers une base de données [!INCLUDE[d365fin](includes/d365fin_md.md)]. L'exportation et l'importation de profils vous permettent de gagner du temps lors de la configuration de l'interface utilisateur, car vous réutilisez une configuration de profil existante au lieu d'en configurer un en partant de zéro. Si vous avez un profil qui est configuré dans une base de données [!INCLUDE[d365fin](includes/d365fin_md.md)] et que vous souhaitez réutiliser tout ou partie de cette configuration dans une autre base de données, vous pouvez exporter le profil vers un fichier XML. Ensuite, vous pouvez importer le fichier XML du profil dans l'autre base de données.

-   Pour exporter un profil, vous pouvez choisir l'action **Exporter les profils** dans la **Liste des profils** ou la page **Fiche profil**, ou vous pouvez rechercher et ouvrir la page **Exporter les profils**. Enregistrez le fichier XML dans un emplacement de votre ordinateur ou du réseau.

-   Pour importer un profil, vous pouvez choisir l'action **Importer les profils** dans la **Liste des profils**, ou vous pouvez rechercher et ouvrir la page **Importer les profils**. 

    > [!NOTE]  
    >  Vous ne pouvez pas importer un profil existant déjà dans la base de données, même si le fichier XML est nommé ou contient un contenu différent. Vous devez supprimer le profil existant avant de pouvoir importer le nouveau profil.


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
