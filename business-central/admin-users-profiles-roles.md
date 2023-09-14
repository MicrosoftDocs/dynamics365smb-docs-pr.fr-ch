---
title: Gestion des utilisateurs et des rôles
description: "Découvrez comment gérer les profils utilisateur et les tableaux de bord dans Business\_Central. Les profils permettent aux administrateurs de définir et de gérer de manière centralisée ce que les utilisateurs peuvent voir et faire."
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/11/2023
ms.custom: bap-template
ms.search.form: 9171
---
# Gérer les profils d’utilisateur

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Attribuez tous les utilisateurs à des profils qui reflètent :

* Leur rôle commercial
* Le service où ils travaillent
* Un autre type de catégorisation

Les profils permettent aux administrateurs de définir et de gérer de manière centralisée ce à quoi différents types d’utilisateurs peuvent accéder dans [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> L’utilisation professionnelle classique d’un profil est un rôle. Un profil est donc nommé *Profil (rôle)* dans l’interface utilisateur.

En tant qu’administrateur, vous créez et gérez des profils sur la page **Profils (rôles)**. Chaque profil dispose d’une carte dans laquelle vous gérez les paramètres du rôle associé. Pour cet exemple, la carte contient les informations suivantes :

* Nom du rôle
* Préférences client
* Tableau de bord utilisé par le profil

Pour plus d’informations sur les paramètres utilisateur et les tableaux de bord, voir [Modifier les paramètres de base](ui-change-basic-settings.md).

Avant de pouvoir administrer des profils d’utilisateurs, il convient de les créer et de les ajouter via le Centre d’administration Microsoft 365. Vous pouvez ensuite attribuer des autorisations à chaque utilisateur ou groupe d’utilisateurs. Les autorisations définissent les fonctionnalités auxquelles les utilisateurs peuvent accéder. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).

## Personnalisation de page

Vous pouvez personnaliser les mises en page d’un profil afin que tous les utilisateurs auxquels ce profil a été attribué voient les pages personnalisées. En tant qu’administrateur, vous devez personnaliser les pages en utilisant les mêmes fonctionnalités que les utilisateurs lorsqu’ils personnalisent. Pour plus d’informations, voir [Personnaliser des pages pour les profils](ui-personalization-manage.md).

## Pour créer un profil

Si vous ne pouvez pas copier un profil existant, vous pouvez en créer un manuellement.

1. Choisissez l’icône ![age ou état pour la recherche.](media/ui-search/search_small.png "Icône Page ou état pour la recherche") entrez **Profils (Rôles)**, puis sélectionnez le lien associé.  
2. Sur la page **Profils (rôles)**, sélectionnez l’action **Nouveau**.  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Si vous souhaitez qu’un profil particulier ne soit disponible que pour des utilisateurs très spécifiques, vous pouvez définir le champ **Description** sur `Navigation menu only.`. De cette façon, le profil est exclu de la liste des rôles disponibles dans **Mes paramètres**.

## Pour copier un profil

Pour gagner du temps, vous pouvez créer un nouveau profil en copiant un profil existant. Copiez celui qui a des paramètres similaires à celui que vous voulez créer.

> [!NOTE]
> Lorsque vous copiez un profil, toutes les personnalisations de page impliquées sont également copiées, qu’elles soient créées par l’utilisateur ou dérivées d’extensions.

1. Sur la page **Profils (rôles)**, sélectionnez la ligne d’un profil à copier, puis sélectionnez l’action **Copier le profil**.
2. Renseignez les champs **ID profil** et **Nom complet**, puis cliquez sur le bouton **OK**.
3. Sur la page **Profils (rôles)**, ouvrez la fiche du profil nouvellement créée, puis modifiez les autres champs si nécessaire.

## Pour modifier un profil

Vous pouvez modifier un profil en modifiant les champs de la page **Profil (rôle)**. Toutefois, les modifications apportées ne seront pas visibles par l’utilisateur auquel le profil a été attribué tant qu’il ne se sera pas déconnecté/reconnecté.

> [!Caution]
> Ne renommez pas de profil lorsque les utilisateurs auxquels ce profil a été attribué sont connectés, car ils risquent de constater un blocage et de devoir redémarrer.

## Pour affecter un profil à un utilisateur

Les utilisateurs peuvent s’attribuer eux-mêmes un rôle (représentant un profil) en choisissant le champ **Rôle** sur la page **Mes paramètres**. En tant qu’administrateur, vous pouvez en faire de même avec la page **Profils (rôles)**.

1. Sur la page **Profils (rôles)**, sélectionnez le profil à attribuer, puis sélectionnez l’action **Liste des personnalisations utilisateur**.
2. Sur la page **Personnalisations utilisateur**, sélectionnez l’utilisateur à qui attribuer le profil, puis sélectionnez l’action **Modifier**.
3. Dans le champ **ID profil**, sélectionnez le profil approprié.

> [!NOTE]
> Si vous attribuez un autre profil à un utilisateur, toutes les personnalisations effectuées par l’utilisateur avec le profil précédent sont conservées.

## Pour définir les paramètres utilisateur d’un profil

Sur la page **Mes paramètres**, les utilisateurs peuvent définir le comportement de base de leur compte, tel que le Tableau de bord, la langue et les notifications qu’ils reçoivent. Pour plus d’informations, voir [Modifier les paramètres de base](ui-change-basic-settings.md).

En tant qu’administrateur, vous pouvez définir les paramètres d’un profil. Les paramètres s’appliquent à tous les utilisateurs affectés au rôle.

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Profils (Rôles)**, puis sélectionnez le lien associé.
2. Sélectionnez la ligne du profil pour lequel vous souhaitez modifier les paramètres utilisateur, puis choisissez l’action **Liste de personnalisations utilisateur**.
3. Sur la page **Personnalisations utilisateur**, ouvrez la fiche de l’utilisateur dont vous souhaitez modifier les paramètres.
4. Sur la page **Fiche de personnalisation utilisateur**, modifiez les champs si nécessaire.

## Pour activer un profil

Lorsque vous créez un profil, vous pouvez définir si, où et comment le profil et ses informations sont mis à la disposition des utilisateurs.

Sur la page **Profil (rôle)**, activez les cases à cocher suivantes :

* **Activé** pour spécifier si le rôle associé est visible dans la page **Rôles disponibles** pour être choisi par les utilisateurs.  
* **Utiliser comme profil par défaut** pour spécifier le profil qui s’applique aux utilisateurs auxquels aucun rôle spécifique n’est attribué.
* **Désactiver la personnalisation** pour spécifier si les utilisateurs du rôle associé peuvent personnaliser leur espace de travail.
* **Afficher dans l’explorateur de rôles** pour spécifier si les actions sur les fonctionnalités métier incluses dans le profil sont affichées dans la vue étendue de l’explorateur de rôles, une vue d’ensemble des fonctionnalités. Pour en savoir plus, consultez [Recherche de pages avec l’explorateur de rôles](ui-role-explorer.md).

## Pour exporter des profils

Vous pouvez exporter des profils depuis [!INCLUDE[prod_short](includes/prod_short.md)], par exemple pour les réutiliser dans un autre abonné. Les profils sont exportés vers un fichier zip contenant des fichiers AL. Vous pouvez réutiliser les fichiers AL pour développer des extensions. Pour plus d’informations, voir [Utiliser le client pour créer des profils et des personnalisations de page](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Sur la page **Profils (rôles)**, choisissez l’action **Exporter des profils**.

    Cette action exporte un fichier zip contenant les fichiers AL pour tous les profils.

## Pour importer des profils

Vous pouvez importer des profils ayant été exportés depuis [!INCLUDE[prod_short](includes/prod_short.md)]. La procédure d’importation est plus ou moins l’inverse de la procédure d’exportation de profils. Pour en savoir plus, consultez [Pour exporter des profils](admin-users-profiles-roles.md#to-export-profiles).

1. Sur la page **Profils (rôles)**, choisissez l’action **Importer des profils**.
2. Suivez les étapes de l’assistant **Importer des profils**.

    Si vous souhaitez uniquement importer des profils spécifiques, utilisez le champ **Sélection** pour les indiquer.
3. Cliquez sur le bouton **Importer les sélections**.

    Cette action importe un fichier zip contenant les fichiers AL pour les profils sélectionnés.

## Pour supprimer un profil

Vous pouvez supprimer un profil en choisissant l’action **Supprimer** sur la page **Profils (rôles)**. Cependant, les limitations suivantes s’appliquent :

* Vous ne pouvez pas supprimer un profil attribué à un utilisateur ou à un groupe d’utilisateurs.
*-* Vous ne pouvez pas supprimer les profils provenant d’extensions. L’extension doit d’abord être désinstallée.
*-* Vous ne pouvez supprimer qu’un profil à la fois.

## Pour supprimer toutes les personnalisations effectuées par un utilisateur

Vous pouvez supprimer toutes les modifications qu’un utilisateur a apportées aux pages. Supprimer les modifications peut être utile, par exemple, si un employé a changé de rôle et n’en a plus besoin. Les suppressions ramènent la mise en page à ce qui est défini par le profil.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Personnalisations utilisateur**, puis choisissez le lien associé.

    La page **Personnalisations utilisateur** répertorie tous les utilisateurs qui ont apporté des personnalisations.

2. Ouvrez la fiche d’un utilisateur dont vous souhaitez supprimer les personnalisations.
3. Sur la page **Fiche de personnalisation utilisateur**, choisissez l’action **Effacer les pages personnalisées**, puis acceptez le message qui apparaît.

L’utilisateur verra les modifications lors de sa prochaine connexion.

Vous pouvez également supprimer toutes les personnalisations de page pour un profil. Pour plus d’informations, voir [Supprimer toutes les personnalisations d’un profil](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## Pour supprimer des personnalisations pour des pages spécifiques

Vous pouvez supprimer les personnalisations qu’un ou plusieurs utilisateurs ont apportées à des pages spécifiques. Supprimer des personnalisations peut être utile, par exemple, si un processus d’entreprise modifié signifie qu’une personnalisation ne peut plus être utilisée. Les suppressions ramènent la mise en page à ce qui est défini par le profil.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Personnalisations de la page utilisateur**, puis choisissez le lien associé.

    La page **Personnalisations des pages utilisateur** répertorie toutes les pages qui ont été personnalisées et l’utilisateur à qui elles appartiennent.

    > [!Note]
    > Une coche dans le champ **Personnalisation héritée** indique si la personnalisation a été effectuée dans une ancienne version de [!INCLUDE[prod_short](includes/prod_short.md)], qui a traité la personnalisation de manière différente. Les utilisateurs qui essaient de personnaliser ces pages sont empêchés de le faire, à moins qu’ils ne choisissent de déverrouiller la page. Pour plus d’informations, voir [Pourquoi la personnalisation d’une page est bloquée](ui-personalization-locked.md).

2. Sélectionnez la ligne de la personnalisation de la page à supprimer, puis sélectionnez l’action **Supprimer**.

L’utilisateur les verra les modifications lors de sa prochaine connexion.  

Vous pouvez également supprimer toutes les personnalisations de page individuelle pour un profil. Pour plus d’informations, voir [Supprimer la personnalisation de pages spécifiques d’un profil](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## Gestion des sessions utilisateur

En tant qu’administrateur de [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, vous pouvez gérer les sessions utilisateur dans le centre d’administration. Pour plus d’informations, voir [Gérer les sessions](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions) dans le contenu d’administration.  

Pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site, vous pouvez gérer des sessions à l’aide de SQL Server Management Studio, par exemple. Pour plus d’informations, voir [Documentation technique SQL Server](/sql/sql-server).  

## Voir la [formation Microsoft](/training/modules/users-security-dynamics-365-business-central/) associée

## Voir aussi

[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  
[Personnaliser les pages pour les profils](ui-personalization-manage.md)  
[Personnaliser votre espace de travail](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
