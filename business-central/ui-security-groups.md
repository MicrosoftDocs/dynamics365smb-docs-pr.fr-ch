---
title: Contrôler l’accès à l’aide de groupes de sécurité
description: Cet article explique comment utiliser les groupes de sécurité pour définir les autorisations des utilisateurs.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# Contrôler l’accès à Business Central à l’aide de groupes de sécurité

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Les groupes de sécurité permettent aux administrateurs de gérer plus facilement les autorisations des utilisateurs dans leurs applications Dynamics 365, telles que SharePoint Online, CRM Online et la version en ligne de [!INCLUDE [prod_short](includes/prod_short.md)]. Les administrateurs ajoutent des autorisations à leurs groupes de sécurité et lorsqu’ils ajoutent des utilisateurs au groupe, les autorisations s’appliquent à tous les membres. Par exemple, un administrateur peut créer un groupe de sécurité qui donne aux vendeurs la possibilité de créer et de valider des commandes client. Ou laissez les acheteurs faire de même pour les ordres achat.

Créez vos groupes de sécurité dans votre centre d’administration Microsoft 365 ou Azure Active Directory. Cet article décrit les étapes dans le centre d’administration Microsoft 365, mais les étapes sont similaires dans les deux.

## Ajouter un groupe de sécurité dans le centre d’administration Microsoft 365

1. Dans le centre d’administration Microsoft 365, accédez à la page **Équipes et groupes actifs**.
2. Choisissez **Ajouter un groupe**.
3. Choisissez le type de groupe **Sécurité**, puis choisissez **Suivant**.
4. Précisez les bases de votre groupe.
5. Facultatif : Rendez les membres du groupe disponibles pour l’attribution de rôles. Pour en savoir plus sur les attributions, accédez à [Utiliser les groupes Azure AD pour gérer les attributions de rôles](/azure/active-directory/roles/groups-concept).
6. Ouvrez le groupe, puis utilisez l’onglet **Ajouter des membres** pour inclure des personnes dans le groupe.

## Ajouter un groupe de sécurité dans Business Central

Dans [!INCLUDE [prod_short](includes/prod_short.md)], créez un groupe de sécurité, puis associez-le au groupe de sécurité dans le centre d’administration Microsoft 365. Votre nouveau groupe contient les membres que vous avez ajoutés dans le centre d’administration Microsoft 365.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Groupes de sécurité**, puis choisissez le lien associé.
2. Choisissez **Nouveau** pour créer un groupe.
3. Dans le champ **Nom**, entrez un nom pour le groupe.
4. Dans le champ **Nom du groupe de sécurité AAD** , entrez le nom du groupe de sécurité exactement tel qu’il s’affiche dans le centre d’administration Microsoft 365. [!INCLUDE [prod_short](includes/prod_short.md)] trouve ce groupe et l’associe à ce groupe.

> [!NOTE]
> Les utilisateurs qui s’affichent dans la fiche **Membres** sur le volet Récapitulatif ou la page **Membres du groupe de sécurité** seulement s’ils ont été ajoutés en tant qu’utilisateurs dans [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations sur l’ajout d’utilisateurs, voir [Pour ajouter des utilisateurs ou mettre à jour les informations utilisateur et les attributions de licence dans Business Central](ui-how-users-permissions.md#adduser).  

### Affecter des autorisations au groupe

1. Sur la page **Groupes de sécurité**, choisissez le groupe, puis l’action **Autorisations**.
1. Attribuez des autorisations de la manière suivante :
    * Pour attribuer des ensembles d’autorisations individuellement, dans le champ **Ensemble d’autorisations**, choisissez les autorisations à attribuer.
    * Pour attribuer plusieurs ensembles d’autorisations, choisissez l’action **Sélectionner des ensembles d’autorisations**, puis choisissez les ensembles à attribuer.

## Vérifier les autorisations dans un groupe de sécurité

Sur la page **Groupes de sécurité**, le volet Récapitulatif affiche les **Ensembles d’autorisations** attribués au groupe. Chaque utilisateur répertorié dans la fiche **Membres** a ces autorisations. L’action **Ensemble d’autorisations par groupe de sécurité** fournit une vue plus détaillée. Là, vous pouvez également explorer les autorisations individuelles dans chaque groupe de sécurité.

Les autorisations sont également disponibles sur la page **Utilisateurs**. Le volet Récapitulatif affiche les cartes **Ensembles d’autorisations du groupe de sécurité** et **Appartenances au groupe de sécurité** pour l’utilisateur sélectionné.

## Groupes de sécurité et groupes d’utilisateurs

Si vous avez des groupes d’utilisateurs, vous pouvez convertir les groupes en ensembles d’autorisations dans votre client à l’aide du guide de configuration assistée de la **Migration des groupes d’utilisateurs**. Pour démarrer le guide, sur la page **Gestion des fonctionnalités**, recherchez **Fonctionnalité : Convertir les autorisations de groupe d’utilisateurs**, puis choisissez **Tous les utilisateurs** dans le champ **Activé pour**. Le guide de configuration assistée propose les options suivantes pour la conversion.

|Option  |Description  |
|---------|---------|
|Attribuer à l’utilisateur     | Affectez des autorisations directement aux groupes d’utilisateurs attribués au groupe, puis supprimez les affectations de leur groupe d’utilisateurs.        |
|Convertir en un ensemble d’autorisations     | Créez une autorisation pour les autorisations de chaque groupe d’utilisateurs. Le nouvel ensemble d’autorisations est attribué à tous les membres de chaque groupe d’utilisateurs.          |

## Voir aussi

[Créer des utilisateurs en fonction des licences](ui-how-users-permissions.md)  
[Configuration de l’accès à Business Central dans Teams avec les licences Microsoft 365](admin-access-with-m365-license-setup.md)  
[En savoir plus sur les groupes et les droits d’accès dans Azure Active Directory](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Groupes de sécurité Active Directory](/windows-server/identity/ad-ds/manage/understand-security-groups)  