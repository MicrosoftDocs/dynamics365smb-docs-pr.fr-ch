---
title: Contrôler l’accès à l’aide de groupes de sécurité
description: Cet article explique comment utiliser les groupes de sécurité pour définir les autorisations des utilisateurs.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 11/29/2023
---

# Contrôler l’accès à Business Central à l’aide de groupes de sécurité

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Les groupes de sécurité permettent aux administrateurs de simplifier la gestion des autorisations des utilisateurs. Par exemple, pour [!INCLUDE [prod_short](includes/prod_short.md)] en ligne, ils sont réutilisables dans les applications Dynamics 365, telles que SharePoint Online, CRM Online et [!INCLUDE [prod_short](includes/prod_short.md)]. Les administrateurs ajoutent des autorisations à leurs groupes de sécurité [!INCLUDE [prod_short](includes/prod_short.md)] et lorsqu’ils ajoutent des utilisateurs au groupe, les autorisations s’appliquent à tous les membres. Par exemple, un administrateur peut créer un groupe de sécurité [!INCLUDE [prod_short](includes/prod_short.md)] qui donne aux vendeurs la possibilité de créer et de valider des commandes client. Ou laissez les acheteurs faire de même pour les ordres achat.

## Business Central Online et support local

Vous pouvez utiliser des groupes de sécurité pour les versions en ligne et locale de [!INCLUDE [prod_short](includes/prod_short.md)]. Selon la version de votre produit, créez des groupes de l’une des solutions suivantes :

* Pour la version en ligne, utilisez les groupes de sécurité Microsoft Entra. Pour en savoir plus sur la création du groupe, accédez à [Créer, modifier ou supprimer un groupe de sécurité dans le centre d’administration Microsoft 365](/microsoft-365/admin/email/create-edit-or-delete-a-security-group).
* Sur site, les groupes de sécurité ne sont pris en charge que si le déploiement utilise l’authentification Windows. Pour créer des groupes de sécurité locale, utilisez les groupes Windows Active Directory. Pour en savoir plus, accédez à [Créer un compte de groupe dans Windows Active Directory](/windows/security/operating-system-security/network-security/windows-firewall/create-a-group-account-in-active-directory). 

Puis, créez un groupe de sécurité correspondant dans [!INCLUDE [prod_short](includes/prod_short.md)], et associez-le au groupe créé. Pour en savoir plus, consultez [Ajouter un groupe de sécurité dans Business Central](#add-a-security-group-in-business-central).

> [!NOTE]
> Si vous avez configuré un type d’utilisateur spécial avec un type de licence de groupe Windows dans une version [!INCLUDE [prod_short](includes/prod_short.md)] locale antécédente à la première vague de lancement 2023, lorsque vous mettez à niveau [!INCLUDE [prod_short](includes/prod_short.md)] convertit l’utilisateur à un groupe de sécurité. Le nouveau groupe de sécurité porte le même nom que le nom du groupe Windows. Le groupe de sécurité vous donne un meilleur aperçu des membres du groupe et de leurs autorisations effectives.

## Ajouter un groupe de sécurité dans Business Central

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Groupes de sécurité**, puis choisissez le lien associé.
1. Choisissez **Nouveau** pour créer un groupe.
1. Créez le lien vers votre groupe, comme suit :

    * Pour [!INCLUDE [prod_short](includes/prod_short.md)] Online, choisissez le groupe dans le champ **Nom du groupe de sécurité Microsoft Entra**.
    * Pour [!INCLUDE [prod_short](includes/prod_short.md)] local, choisissez le groupe dans le champ **Nom du groupe Windows** .

> [!NOTE]
> Les utilisateurs qui s’affichent dans la fiche **Membres** sur le volet Récapitulatif ou la page **Membres du groupe de sécurité** seulement s’ils ont été ajoutés en tant qu’utilisateurs dans [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations sur l’ajout d’utilisateurs, voir [Pour ajouter des utilisateurs ou mettre à jour les informations utilisateur et les attributions de licence dans Business Central](ui-how-users-permissions.md#adduser).  

### Attribuer des autorisations à un groupe de sécurité

1. Sur la page **Groupes de sécurité**, choisissez le groupe, puis l’action **Autorisations**.
1. Attribuez des autorisations de la manière suivante :

    * Pour attribuer des ensembles d’autorisations individuellement, dans le champ **Ensemble d’autorisations**, choisissez les autorisations à attribuer.
    * Pour attribuer plusieurs ensembles d’autorisations, choisissez l’action **Sélectionner des ensembles d’autorisations**, puis choisissez les ensembles à attribuer.

## Vérifier les autorisations dans un groupe de sécurité

Sur la page **Groupes de sécurité**, le volet Récapitulatif affiche les **Ensembles d’autorisations** attribués au groupe. Chaque utilisateur répertorié dans la fiche **Membres** a ces autorisations. L’action **Ensemble d’autorisations par groupe de sécurité** fournit une vue plus détaillée. Là, vous pouvez également explorer les autorisations individuelles dans chaque groupe de sécurité.

Les autorisations sont également disponibles sur la page **Utilisateurs**. Le volet Récapitulatif affiche les cartes **Ensembles d’autorisations du groupe de sécurité** et **Appartenances au groupe de sécurité** pour l’utilisateur sélectionné.

## Groupes de sécurité et groupes d’utilisateurs

> [!NOTE]
> Les groupes d’utilisateurs ne seront plus disponibles dans une prochaine version.

Les groupes de sécurité sont très similaires aux groupes d’utilisateurs actuellement disponibles. Cependant, les groupes d’utilisateurs ne sont pertinents que pour [!INCLUDE [prod_short](includes/prod_short.md)]. Les groupes de sécurité sont basés sur des groupes dans Microsoft Entra ID ou Windows Active Directory, selon que vous utilisez [!INCLUDE [prod_short](includes/prod_short.md)] en ligne ou en local, respectivement. Les groupes bénéficient aux administrateurs, car ils peuvent les utiliser avec d’autres applications Dynamics 365. Par exemple, si les commerciaux utilisent [!INCLUDE [prod_short](includes/prod_short.md)]et SharePoint, les administrateurs n’ont pas à recréer le groupe et ses membres.

### En option : Convertir des groupes d’utilisateurs en ensembles d’autorisations

Dans la première vague de lancement 2023 et les versions ultérieures, vous pouvez convertir des groupes d’utilisateurs en ensembles d’autorisations dans votre client. Les ensembles d’autorisations offrent les mêmes fonctionnalités que les groupes d’utilisateurs. Voilà quelques exemples :

* Vous pouvez utiliser le récapitulatif **Utilisateurs** pour gérer les autorisations des utilisateurs.
* Vous pouvez explorer le nom de l’ensemble d’autorisations pour ajouter d’autres ensembles d’autorisations à l’ensemble sur lequel vous travaillez. Pour en savoir plus, accédez à [Pour ajouter d’autres ensembles d’autorisations](ui-define-granular-permissions.md#to-add-other-permission-sets).

Utilisez le guide de configuration assistée de la **Migration du groupe d’utilisateurs** pour convertir vos groupes. Pour démarrer le guide, sur la page **Gestion des fonctionnalités**, recherchez **Fonctionnalité : Convertir les autorisations de groupe d’utilisateurs**, puis choisissez **Tous les utilisateurs** dans le champ **Activé pour**. Le guide de configuration assistée propose les options suivantes pour la conversion.

|Option  |Description  |
|---------|---------|
|Attribuer à l’utilisateur     | Affectez des autorisations directement aux groupes d’utilisateurs attribués au groupe, puis supprimez les affectations de leur groupe d’utilisateurs.        |
|Convertir en un ensemble d’autorisations     | Créez une autorisation pour les autorisations de chaque groupe d’utilisateurs. Le nouvel ensemble d’autorisations est attribué à tous les membres de chaque groupe d’utilisateurs.          |

### Les configurations de licence s’appliquent toujours

Vous pouvez configurer les autorisations dans [!INCLUDE [prod_short](includes/prod_short.md)] fonction des licences. Ces autorisations sont directement attribuées aux nouveaux utilisateurs. Ces configurations s’appliquent toujours, même si vous commencez à utiliser des groupes de sécurité.

Pour utiliser exclusivement des groupes de sécurité, nous vous recommandons de supprimer les configurations de licence. Pour en savoir plus sur les configurations de licence, accédez à [Créer des utilisateurs en fonction des licences](ui-how-users-permissions.md).

Vous pouvez supprimer des configurations de licence sur la page **Configuration de licence**. Choisissez une licence, puis supprimez tous les ensembles d’autorisations qui lui sont attribués.

## Voir aussi

[Création des utilisateurs en fonction des licences](ui-how-users-permissions.md)  
[Configuration de l’accès à Business Central dans Teams avec les licences Microsoft 365](admin-access-with-m365-license-setup.md)  
[En savoir plus sur les groupes et les droits d’accès dans Microsoft Entra ID](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Groupes de sécurité Microsoft Entra](/windows-server/identity/ad-ds/manage/understand-security-groups)  
