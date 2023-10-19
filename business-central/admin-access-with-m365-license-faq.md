---
title: FAQ sur l’accès avec les licences Microsoft 365
description: Obtenez des réponses aux questions courantes sur l’accès à Business Central avec des licences Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: faq
ms.date: 09/28/2023
ms.custom: bap-template
---
# <a name="access-with-microsoft-365-licenses-faq"></a>FAQ sur l’accès avec les licences Microsoft 365

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Les utilisateurs peuvent accéder aux données de Business Central dans Microsoft Teams à l’aide de leur licence Microsoft 365. Cet article répond aux questions fréquemment posées par les administrateurs, les consultants et autres. Les développeurs doivent se référer à la FAQ des développeurs. Pour toute question sur l’intégration de Business Central avec Microsoft Teams, accédez à la [FAQ Teams](teams-faq.md).

## [Autorisations](#tab/permissions) 

### <a name="can-i-proactively-configure-different-starting-permissions-for-different-groups-of-users"></a>Puis-je configurer de manière proactive différentes autorisations de démarrage pour différents groupes d’utilisateurs ?

Pas actuellement. Business Central ne permet de configurer qu’un seul groupe d’autorisations attribuées à tous les utilisateurs Microsoft 365 quand ils se connectent à Business Central pour la première fois.

### <a name="can-i-proactively-configure-permissions-profiles-and-settings-for-individual-users-before-they-sign-in"></a>Puis-je configurer de manière proactive les autorisations, les profils et les paramètres des utilisateurs individuels avant qu’ils ne se connectent ?

Oui. Cela peut être réalisé via des groupes de sécurité. En appliquant un groupe de sécurité à un environnement, vous définissez l’ensemble total d’utilisateurs ayant accès à cet environnement. Ce groupe de sécurité peut inclure des utilisateurs avec une licence Business Central et des utilisateurs avec une licence Microsoft 365. À la prochaine mise à jour des utilisateurs depuis Microsoft 365 dans la liste **Utilisateurs**, les enregistrements d’utilisateurs Microsoft 365 seront créés. Vous pouvez ensuite attribuer des groupes d’utilisateurs, des autorisations, des profils et d’autres paramètres avant qu’ils ne se connectent.

### <a name="after-a-user-signs-in-can-i-change-which-objects-they-have-access-to"></a>Une fois qu’un utilisateur s’est connecté, puis-je modifier les objets auxquels il a accès ?

Oui. Une fois qu’un utilisateur s’est connecté pour la première fois et que son enregistrement d’utilisateur a été approvisionné, les administrateurs gèrent ces utilisateurs comme n’importe quel autre utilisateur de Business Central. Par exemple, ils peuvent ajouter ou supprimer des autorisations sur différents objets. Si vous modifiez les ensembles d’autorisations attribués à la licence Microsoft 365 dans la page Configuration de la licence, la modification n’affectera que les prochains utilisateurs qui se connectent pour la première fois.

### <a name="how-do-i-prevent-access-to-sensitive-tables"></a>Comment empêcher l’accès aux tables sensibles ?

Business Central offre un modèle d’autorisation puissant et flexible où les administrateurs peuvent définir des ensembles d’autorisations qui accordent l’accès à des objets spécifiques, des processus métier ou des rôles entiers. Pour empêcher l’accès aux tables sensibles, vous pouvez créer des ensembles d’autorisations personnalisés qui excluent l’autorisation d’accès aux objets sensibles. Pour plus d’informations sur l’exclusion d’autorisations, voir [Créer un ensemble d’autorisations](ui-define-granular-permissions.md).  

### <a name="instead-of-customizing-the-license-configuration-can-i-customize-a-user-group"></a>Au lieu de personnaliser la configuration de la licence, puis-je personnaliser un groupe d’utilisateurs ?

Oui. L’ajout d’ensembles d’autorisations au groupe d’utilisateurs internes Microsoft Teams dans Business Central a le même effet net que l’ajout d’ensembles d’autorisations à la licence Microsoft 365, tant que la licence Microsoft 365 continue d’être mappée à ce groupe d’utilisateurs. Cette approche présente l’avantage supplémentaire que les ensembles d’autorisations sont toujours synchronisés avec les membres du groupe chaque fois que vous modifiez le groupe d’utilisateurs.

### <a name="when-a-business-central-user-shares-a-record-in-teams-do-they-grant-new-permissions"></a>Quand un utilisateur de Business Central partage un enregistrement dans Teams, accorde-t-il de nouvelles autorisations ?

Non. Cette action n’est pas la même que le partage d’un lien vers un document SharePoint où la personne qui partage le document peut choisir d’accorder l’autorisation à d’autres. Dans Business Central, seuls les administrateurs peuvent configurer et attribuer des autorisations. Par rapport au partage de documents SharePoint, cela équivaut à choisir l’option « Partager avec les personnes disposant d’un accès existant ».

### <a name="does-this-feature-support-row-level-security"></a>Cette fonctionnalité prend-elle en charge la sécurité au niveau des lignes ?

Oui. Même si une personne accédant à un enregistrement dans Teams avec sa licence Microsoft 365 peut disposer des autorisations d’objet de table et de page correctes, les autorisations au niveau de la ligne seront appliquées si elles ont été implémentées pour cette table.  

### <a name="if-i-configure-permissions-that-include-write-access-will-users-be-able-to-write-in-teams"></a>Si je configure des autorisations incluant un accès en écriture, les utilisateurs pourront-ils écrire dans Teams ?

Si vous configurez Business Central pour attribuer un ensemble d’autorisations qui inclut l’insertion, la modification ou la suppression de l’accès à un ou plusieurs objets, les utilisateurs disposant de cet ensemble d’autorisations ne pourront toujours pas écrire dans Teams quand ils n’ont qu’une licence Microsoft 365. Le service Business Central applique un accès en lecture seule, quelle que soit l’autorisation d’insertion, de modification ou de suppression que vous attribuez.  

Même si Business Central fournit ce niveau de protection, nous vous recommandons toujours d’éviter les ensembles d’autorisations avec accès en écriture. Cela évite les problèmes en aval quand les utilisateurs changent de rôle ou acquièrent de nouvelles licences.  

## [Installation et configuration](#tab/setup)

### <a name="why-is-the-setting-to-enable-access-not-available-for-my-environment"></a>Pourquoi le paramètre d’activation de l’accès n’est-il pas disponible pour mon environnement ?

L’activation de l’accès avec les licences Microsoft 365 n’est disponible que pour les environnements Business Central de la plate-forme version 21.1 ou ultérieure. Quand votre environnement est mis à niveau vers cette version minimale, le paramètre devient automatiquement disponible. Pour vérifier la version de votre environnement, accédez à la page des détails de l’environnement pour l’environnement dans le centre d’administration Business Central. Sinon, connectez-vous à l’environnement et accédez à la page **Aide et support** du menu **Aide**.

### <a name="can-i-access-business-central-on-premises-with-microsoft-365-licenses"></a>Puis-je accéder à Business Central localement avec des licences Microsoft 365 ?

Non, ce n’est pas pris en charge. Business Central affiche une erreur quand les utilisateurs tentent d’accéder aux enregistrements Business Central localement dans Teams.

### <a name="what-is-the-employee-profile"></a>Quel est le profil de l’employé ?

Le profil **Employé** affiché dans la page de liste **Profils (Rôles)** a été introduit avec la mise à jour 21.1. Il s’agit du profil par défaut attribué aux utilisateurs qui accèdent à Business Central avec leur licence Microsoft 365. Ce profil est destiné aux personnes d’une organisation qui n’ont pas de rôle spécifique dans Business Central et qui ont uniquement besoin d’afficher les données qui ont été partagées avec elles.

### <a name="what-is-the-teams-users-user-group"></a>Qu’est-ce que le groupe d’utilisateurs Teams Users ?

Le groupe **Utilisateurs internes Microsoft Teams** affiché sur la page **Groupes d’utilisateurs** a été introduit avec la mise à jour 21.1. Ce groupe est le groupe d’utilisateurs par défaut attribué aux utilisateurs qui accèdent à Business Central avec leur licence Microsoft 365. Le groupe d’utilisateurs est destiné aux personnes de la même organisation où Business Central est hébergé qui collaborent dans Microsoft Teams.  

### <a name="do-users-that-only-have-a-microsoft-365-license-show-up-in-the-users-list-in-business-central"></a>Les utilisateurs qui n’ont qu’une licence Microsoft 365 s’affichent-ils dans la liste des utilisateurs dans Business Central ?

Oui. Si vous appliquez des groupes de sécurité aux environnements, ces utilisateurs apparaîtront dans la liste des utilisateurs après que vous aurez utilisé l’action Mettre à jour les utilisateurs de Microsoft 365 dans la liste **Utilisateurs**. Si vous n’appliquez pas de groupes de sécurité, les enregistrements d’utilisateurs apparaissent dans la liste Utilisateurs après le premier accès à un enregistrement Business Central.

### <a name="does-this-feature-work-for-embed-isv-solutions"></a>Cette fonctionnalité fonctionne-t-elle pour les solutions ISV intégrées ?

Oui. Les utilisateurs disposant uniquement d’une licence Microsoft 365 peuvent également accéder aux enregistrements dans des environnements qui s’exécutent sous le domaine *.bc.dynamics.com.

## [Gestion des licences](#tab/license)

### <a name="can-a-customer-use-this-feature-if-they-dont-have-business-central"></a>Un client peut-il utiliser cette fonctionnalité s’il ne dispose pas de Business Central ?

L’accès à Business Central avec une licence Microsoft 365 est destiné aux organisations qui sont déjà abonnées à Business Central et exploitent un ou plusieurs environnements Business Central avec des utilisateurs Business Central sous licence. Il ne fournit aucune nouvelle fonctionnalité ni aucun droit d’utilisation aux clients Microsoft 365 qui n’ont pas de plan Business Central.

### <a name="how-does-this-help-me-manage-subscription-costs-in-my-organization"></a>Comment cela m’aide-t-il à gérer les coûts d’abonnement dans mon organisation ?

Pour maximiser la productivité et rationaliser leurs opérations, les PME achètent souvent Dynamics 365 Business Central avec Microsoft 365. Dans ce cas, la plupart des personnes reçoivent une licence Microsoft 365, mais seuls des rôles ou des personnes spécifiques reçoivent une licence Business Central. Business Central offre une flexibilité de licence afin que les clients ne paient que ce dont ils ont besoin :

- Les utilisateurs nécessitant un accès complet à Business Central se voient généralement attribuer une licence Business Central Essentials ou Business Central Premium. 
- Les utilisateurs nécessitant un accès en écriture limité se voient généralement attribuer une licence de membre de l’équipe Business Central.
- Tous les autres employés de l’organisation qui n’ont besoin de lire qu’occasionnellement les données commerciales partagées avec eux peuvent le faire s’ils disposent d’une licence Microsoft 365. Il n’est pas nécessaire de leur attribuer une licence de membre de l’équipe. D’autres options de gestion des licences sont disponibles. Pour plus d’informations, téléchargez et lisez le [guide des licences Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

### <a name="is-this-100-free-of-charge"></a>Est-ce 100 % gratuit ?
 
Non L’accès aux données de Business Central dans Microsoft Teams nécessite que chaque utilisateur dispose d’une licence Business Central ou d’une licence Microsoft 365 de la liste des plans pris en charge.

### <a name="does-this-work-with-microsoft-365-trials-and-business-central-trials"></a>Cela fonctionne-t-il avec les versions d’essai de Microsoft 365 et de Business Central ?

Oui. Si un utilisateur se voit attribuer une licence Microsoft 365 à partir d’une version d’essai d’un plan pris en charge, il peut également accéder aux enregistrements Business Central dans Teams. Il est alors possible pour les clients d’essayer les applications de productivité et métier de Microsoft en collaboration, et permet aux vendeurs et consultants partenaires de démontrer facilement cette fonctionnalité. Par exemple, les partenaires peuvent approvisionner leurs propres locataires Microsoft Entra à partir de [https://aka.ms/CDX](https://aka.ms/CDX) qui incluent des versions d’essai Microsoft 365 et Business Central pour faire la démonstration de Business Central.

### <a name="the-list-of-licenses-in-business-central-shows-a-microsoft-365-license-whats-that"></a>La liste des licences dans Business Central affiche une licence Microsoft 365. Qu’est-ce-que c’est ?

La page **Configuration des licences** dans Business Central affiche les différents types de licences qui peuvent donner accès au service Business Central. Dans la version 21, Microsoft a ajouté Microsoft 365 à cette liste une nouvelle façon d’accéder à Business Central. Cette liste de licences n’implique pas que votre organisation ait acheté des abonnements à l’une de ces licences ou que votre organisation a activé l’accès via ces licences.

### <a name="do-i-need-to-acquire-a-new-type-of-microsoft-365-license-for-this-feature-to-work"></a>Dois-je acquérir un nouveau type de licence Microsoft 365 pour que cette fonctionnalité fonctionne ?

Microsoft n’a pas créé de licences ou de plans pour alimenter cette fonctionnalité. Cette fonctionnalité repose entièrement sur les plans et licences Microsoft 365 existants. Si vous êtes déjà abonné à l’un des plans Microsoft 365 pris en charge, vous disposez déjà de ce nouveau droit d’utilisation. Sinon, si vous ne vous abonnez pas à Microsoft 365 aujourd’hui, vous pouvez vous inscrire à Microsoft 365 Business Premium ou à des plans similaires ici. 

### <a name="how-do-i-find-out-which-users-have-only-a-microsoft-365-license"></a>Comment savoir quels utilisateurs n’ont qu’une licence Microsoft 365 ?

Il existe plusieurs façons. Dans le centre d’administration Microsoft 365, accédez à la **liste des utilisateurs actifs** et consultez la colonne **licences**. Dans Business Central, accédez à la liste **Utilisateurs**, choisissez l’un des utilisateurs et affichez le Récapitulatif **Licences**.  

### <a name="how-do-i-filter-the-users-list-in-business-central-to-see-users-that-only-have-a-microsoft-365-license"></a>Comment filtrer la liste des utilisateurs dans Business Central pour voir les utilisateurs qui n’ont qu’une licence Microsoft 365 ?

Cette tâche n’est actuellement pas possible à l’aide d’un filtre ou d’une vue de liste. Cependant, vous pouvez sélectionner un utilisateur dans la liste et afficher le Récapitulatif des licences qui inclura uniquement Microsoft 365, si l’utilisateur ne possède qu’une licence Microsoft 365.

### <a name="what-about-users-that-have-both-a-microsoft-365-license-and-a-business-central-license"></a>Qu’en est-il des utilisateurs qui possèdent à la fois une licence Microsoft 365 et une licence Business Central ?

Quand plusieurs licences sont attribuées à un utilisateur, les droits d’utilisation de licence supérieurs l’emportent sur les droits d’utilisation de licence inférieurs au moment de l’accès à Business Central. Dans ce cas, la licence Business Central donne à l’utilisateur plus de droits d’utilisateur. Ainsi, les utilisateurs peuvent lire et écrire des enregistrements Business Central dans Teams et accéder au client web Business Central dans le navigateur, comme tout autre détenteur de licence Business Central. Si des ensembles d’autorisations spécifiques ont été configurés pour la licence Microsoft 365, l’utilisateur obtient les ensembles d’autorisations configurés combinés avec les ensembles d’autorisations de la licence Business Central ou qui ont déjà été attribués à l’utilisateur.

### <a name="is-this-licensing-related-to-the-business-central-team-member-license"></a>Cette licence est-elle liée à la licence de membre de l’équipe Business Central ?

Il n’y a aucune relation entre les licences de membres de l’équipe Business Central et l’accès à Business Central dans Microsoft Teams à l’aide de licences Microsoft 365. Bien que Microsoft Teams et sa documentation fassent référence aux personnes d’une équipe en tant que *membres de l’équipe*, il s’agit d’un terme collectif désignant un groupe d’utilisateurs Microsoft Teams. Il ne fait pas référence aux licences Business Central.

### <a name="does-business-central-enforce-any-of-the-constraints"></a>Business Central applique-t-il l’une des contraintes ?

Oui, toutes les contraintes de plate-forme et les exigences minimales, y compris les exigences de licence, sont appliquées par la plate-forme Business Central. Cela guide les utilisateurs avec des messages d’erreur spécifiques pour les aider à dépanner leur configuration et à prévenir les abus. Par exemple, si un utilisateur qui ne dispose que d’une licence Microsoft 365 tente d’accéder au client web Business Central dans le navigateur, l’accès sera refusé et un message d’erreur s’affichera. 

## [Utilisation](#tab/usage)
 
### <a name="can-i-access-records-on-teams-for-ios-and-teams-for-android"></a>Puis-je accéder aux enregistrements sur Teams pour iOS et Teams pour Android ?

Actuellement, il n’est pas possible d’accéder aux données de Business Central sur le mobile Teams en utilisant uniquement une licence Microsoft 365. Microsoft travaille à l’activation de cette fonctionnalité sous peu. 

### <a name="how-do-users-change-their-personal-settings-in-my-settings"></a>Comment les utilisateurs modifient-ils leurs paramètres personnels dans Mes paramètres ?

Quand un utilisateur accède à Business Central pour la première fois en utilisant uniquement sa licence Microsoft 365, ses paramètres utilisateur tels que la langue, le fuseau horaire et les paramètres régionaux sont automatiquement définis en fonction des paramètres de son système d’exploitation ou de son navigateur. Les administrateurs peuvent modifier ces paramètres depuis Business Central pour chaque utilisateur. 

### <a name="what-determines-the-choice-of-language-when-you-sign-in-for-the-first-time"></a>Qu’est-ce qui détermine le choix de la langue quand vous vous connectez pour la première fois ?

La langue avec laquelle vous utilisez Business Central est définie en fonction de divers facteurs, notamment le client Teams via lequel vous avez accédé à Business Central pour la première fois. Pour l’application de bureau Teams, Teams pour iOS et Teams pour Android, la langue du système d’exploitation est appliquée. Pour Teams pour le web, la langue du navigateur est appliquée. Dans tous les cas, la langue Teams n’est pas prise en compte. 

### <a name="why-cant-i-activate-some-of-the-colored-links-in-tabs-and-card-details"></a>Pourquoi ne puis-je pas activer certains des liens colorés dans les onglets et les détails de la carte ?

Les liens exploitables sur les pages Business Central sont souvent affichés sous la forme de liens hypertexte en gras qui peuvent être activés pour aller ailleurs ou exécuter une opération. Au niveau technique, ces liens sont généralement implémentés sous forme de valeurs de champ sans légende qui déclenchent du code et où le choix du style reflète souvent l’état. Quand les utilisateurs accèdent aux pages Business Central avec leur licence Microsoft 365, les liens sont stylisés comme s’ils étaient exploitables. Mais ils ne peuvent pas être activés, car cette licence n’offre pas de droits d’utilisation pour exécuter des actions.  

### <a name="why-cant-i-activate-page-notification-actions"></a>Pourquoi ne puis-je pas activer les actions de notification de page ?

Les notifications contextuelles affichées sur les pages sont souvent accompagnées de liens exploitables. Quand les utilisateurs accèdent aux pages Business Central avec leur licence Microsoft 365, ces liens s’affichent, mais ne peuvent pas être activés, car cette licence n’offre pas de droits d’utilisation pour exécuter des actions. Au niveau technique, ces liens sont mis en œuvre sous forme d’actions.

### <a name="can-microsoft-365-users-remove-tabs"></a>Les utilisateurs Microsoft 365 peuvent-ils supprimer des onglets ?

Oui. N’importe qui dans la conversation instantanée ou le canal peut supprimer des onglets créés par d’autres. La suppression d’un onglet ne supprime ni n’affecte les données dans Business Central, mais l’onglet sera supprimé pour tous les utilisateurs de la conversation instantanée ou du canal.

### <a name="if-i-cant-filter-will-i-still-see-a-filtered-list-that-was-created-by-others"></a>Si je ne peux pas filtrer, verrai-je toujours une liste filtrée créée par d’autres ?

Les utilisateurs accédant à Business Central avec leur licence Microsoft 365 n’ont pas les droits d’utilisation pour filtrer à l’aide du volet de filtre ou appliquer des vues de liste. Mais si un autre utilisateur a créé un onglet contenant une page de liste filtrée, les utilisateurs Microsoft 365 verront également les filtres appliqués à l’onglet.

---

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de l’accès à Business Central avec les licences Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Configuration de l’accès avec les licences Microsoft 365](admin-access-with-m365-license-setup.md)  
