---
title: Affecter ou modifier des autorisations d'utilisateur | Microsoft Docs
description: "Décrit comment ajouter des utilisateurs d'Office 365 à Business Central, puis affecte des autorisations, des droits d'accès, et des paramètres de sécurité."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 03/16/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 6d350a064f134c4c29938005fea966dec7cca142
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="manage-users-and-permissions"></a>Gérer les utilisateurs et les autorisations
Pour ajouter des utilisateurs dans [!INCLUDE[d365fin](includes/d365fin_md.md)], l'administrateur Office 365 de votre société doit d'abord créer les utilisateurs dans le centre d’administration Office 365. Pour plus d'informations, voir [Ajouter des utilisateurs à Office 365 for business](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)

Une fois les utilisateurs créés dans Office 365, ils peuvent être importés dans la fenêtre **Utilisateurs** à l'aide de l'option **Récupérer des utilisateurs à partir d'Office 365**. Des ensembles d'autorisations sont affectés aux utilisateurs selon le plan qui leur est affecté dans Office 365.

Vous pouvez ensuite passer à l'affectation des ensembles d'autorisations aux utilisateurs pour définir à quels objets de base de données, et de ce fait, à quels éléments de l'interface utilisateur, ils ont accès et dans quelles sociétés. Vous pouvez ajouter des utilisateurs aux groupes d'utilisateurs. Cela facilite l'affectation des mêmes ensembles d'autorisations à plusieurs utilisateurs.

Un ensemble d'autorisations est une collection d'autorisations pour des objets spécifiques de la base de données. Tous les utilisateurs doivent être affectés à une ou plusieurs séries d’autorisations avant de pouvoir accéder à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Plusieurs ensembles d’autorisations prédéfinis sont fournis par défaut. Vous pouvez utiliser ces ensembles d'autorisations tels qu'ils ont été définis, modifier les propres ensembles d'autorisations, ou en créer d'autres.

Les administrateurs peuvent utiliser la fenêtre **Paramètres utilisateur** pour définir les périodes de temps pendant lesquelles les utilisateurs spécifiés peuvent valider, et spécifier également si le système enregistre la durée pendant laquelle les utilisateurs spécifiés ont ouvert une session.

## <a name="to-assign-permissions-to-a-user"></a>Pour affecter des autorisations à un utilisateur
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Utilisateurs**, puis sélectionnez le lien connexe.
2. Sélectionnez l'utilisateur auquel affecter des autorisations.
Tous les ensembles d’autorisations qui sont affectés à l’utilisateur sont affichés dans le récapitulatif **Ensemble d’autorisations utilisateur**.
3. Sélectionnez l'option **Modifier** pour ouvrir la fenêtre **Fiche utilisateur**.
4. Sur le raccourci **Ensembles d'autorisations utilisateur**, renseignez les champs, le cas échéant sur une nouvelle ligne. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Pour regrouper des utilisateurs dans des groupes d'utilisateurs
Vous pouvez définir des groupes d'utilisateurs pour vous aider à gérer les ensembles d'autorisations pour des groupes d'utilisateurs de votre société.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Utilisateurs**, puis sélectionnez le lien connexe.
2. Sinon, dans la fenêtre **Utilisateurs**, sélectionnez l'option **Groupes d'utilisateurs**.
3. Dans la fenêtre **Groupe d'utilisateurs**, sélectionnez l'action **Membres du groupe d'utilisateurs**.
6. Dans la fenêtre **Membres du groupe d'utilisateurs**, sélectionnez l'action **Ajouter utilisateurs**.
7. Pour ajouter de nouveaux ensembles d'autorisations ou des ensembles d'autorisations supplémentaires, dans la fenêtre **Groupes d'utilisateurs**, cliquez sur **Ensembles d'autorisations groupe d'utilisateurs**.
8. Dans la fenêtre **Ensembles d'autorisations groupe d'utilisateurs**, dans une nouvelle ligne, renseignez les champs selon vos besoins en sélectionnant parmi des ensembles d’autorisations existants.

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Pour copier un groupe d'utilisateurs et tous ses ensembles d'autorisations
Pour définir rapidement un nouveau groupe d'utilisateurs, vous pouvez copier tous les ensembles d'autorisations d'un groupe d'utilisateurs existant vers un nouveau groupe d'utilisateurs.

Les membres du groupe d'utilisateurs ne sont pas copié vers le nouveau groupe d'utilisateurs. Vous devez les ajouter manuellement ensuite.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Utilisateurs**, puis sélectionnez le lien connexe.
2. Sélectionnez le groupe d'utilisateurs à partir duquel vous souhaitez copier, puis choisissez l'action **Copier groupe d'utilisateurs**.
3. Dans le champ **Nouveau code du groupe d'utilisateurs**, spécifiez le nom du nouveau groupe, puis cliquez sur le bouton **OK**.

Le nouveau groupe d'utilisateurs est ajouté à la fenêtre **Groupes d'utilisateurs**. Ajoutez ensuite des utilisateurs. Pour plus d'informations, reportez-vous à la section « Pour regrouper des utilisateurs dans des groupes d'utilisateurs ».

## <a name="to-set-up-user-time-constraints"></a>Pour configurer des contraintes de temps utilisateur
Les administrateurs peuvent définir les périodes de temps pendant lesquelles les utilisateurs spécifiés peuvent valider, et spécifier également si le système enregistre la durée pendant laquelle les utilisateurs spécifiés ont ouvert une session. Les administrateurs peuvent également affecter des centres de gestion à des utilisateurs. Pour plus d'informations, voir [Utiliser les centres de gestion](inventory-responsibility-centers.md).

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres utilisateur**, puis choisissez le lien associé.
2. Dans la fenêtre **Paramètres utilisateur**, sélectionnez l'action **Nouveau**.
3. Dans le champ **ID utilisateur**, entrez l'ID d'un utilisateur, ou cliquez sur le champ pour visualiser tous les utilisateurs Windows actuels dans le système.
4. Renseignez les champs selon vos besoins.

## <a name="see-also"></a>Voir aussi
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Mise en route](product-get-started.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

