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
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: e60b7d875ebd0a598908f37a59a49953c61479f1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821136"
---
# <a name="managing-users-and-permissions"></a>Gestion des utilisateurs et des autorisations
Pour ajouter des utilisateurs dans [!INCLUDE[d365fin](includes/d365fin_md.md)], l'administrateur Office 365 de votre société doit d'abord créer les utilisateurs dans le centre d’administration Office 365. Pour plus d'informations, voir [Ajouter des utilisateurs à Office 365 for business](https://aka.ms/CreateOffice365Users).

Une fois les utilisateurs créées dans Office 365, ils peuvent être importés sur la page **Utilisateurs** de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Des ensembles d'autorisations sont affectés aux utilisateurs selon le plan qui leur est affecté dans Office 365. Pour des informations détaillées sur la gestion des licences, voir [Guide des licences Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

Vous pouvez ensuite passer à l'affectation des ensembles d'autorisations aux utilisateurs pour définir à quels objets de base de données, et de ce fait, à quels éléments de l'interface utilisateur, ils ont accès et dans quelles sociétés. Vous pouvez ajouter des utilisateurs aux groupes d'utilisateurs. Cela facilite l'affectation des mêmes ensembles d'autorisations à plusieurs utilisateurs.

Un ensemble d'autorisations est une collection d'autorisations pour des objets spécifiques de la base de données. Tous les utilisateurs doivent être affectés à une ou plusieurs séries d’autorisations avant de pouvoir accéder à [!INCLUDE[d365fin](includes/d365fin_md.md)].

Sur la page **Fiche utilisateur**, vous pouvez ouvrir la page **Autorisations effectives** pour connaître les autorisations de l'utilisateur et les ensembles d'autorisations qui lui sont accordés. Vous pouvez également modifier les détails d'autorisation pour les ensembles d'autorisations de type **Défini par l'utilisateur**. Pour plus d'informations, voir [Pour afficher ou modifier les autorisations d'un utilisateur](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

Les administrateurs peuvent utiliser la page **Paramètres utilisateur** pour définir les périodes de temps pendant lesquelles les utilisateurs spécifiés peuvent valider, et spécifier également si le système enregistre la durée pendant laquelle les utilisateurs spécifiés ont ouvert une session.

Un autre système qui définit ce à quoi les utilisateurs peuvent accéder est le paramètre Expérience. Pour plus d'informations, voir [Modification des fonctionnalités affichées](ui-experiences.md).

## <a name="to-add-a-user-in-business-central"></a>Pour ajouter un utilisateur dans Business Central
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Utilisateurs**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Obtenir les utilisateurs d'Office 365**.

Tout nouvel utilisateur créé pour votre abonnement Office 365 est ajouté à la page **Utilisateurs**.

## <a name="to-group-users-in-user-groups"></a>Pour regrouper des utilisateurs dans des groupes d'utilisateurs
Vous pouvez définir des groupes d'utilisateurs pour vous aider à gérer les ensembles d'autorisations pour des groupes d'utilisateurs de votre société.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Groupes d'utilisateurs**, puis sélectionnez le lien associé.
2. Sinon, sur la page **Utilisateurs**, sélectionnez l'option **Groupes d'utilisateurs**.
3. Sur la page **Groupe d'utilisateurs**, sélectionnez l'action **Membres du groupe d'utilisateurs**.
4. Sur la page **Groupe d'utilisateurs**, choisissez l'action **Ajouter des utilisateurs**.

Quand des utilisateurs ou des groupes d'utilisateurs sont créés, vous devez affecter des ensembles d'autorisations à chacun pour définir les objets auxquels un utilisateur peut accéder. Premièrement, vous devez planifier les autorisations appropriées dans les ensembles d'autorisations. Pour plus d'informations, voir [Pour afficher ou modifier les autorisations d'un utilisateur](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Pour copier un groupe d'utilisateurs et tous ses ensembles d'autorisations
Pour définir rapidement un nouveau groupe d'utilisateurs, vous pouvez copier tous les ensembles d'autorisations d'un groupe d'utilisateurs existant vers un nouveau groupe d'utilisateurs.

Les membres du groupe d'utilisateurs ne sont pas copié vers le nouveau groupe d'utilisateurs. Vous devez les ajouter manuellement ensuite.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Groupes d'utilisateurs**, puis sélectionnez le lien associé.
2. Sélectionnez le groupe d'utilisateurs à partir duquel vous souhaitez copier, puis choisissez l'action **Copier groupe d'utilisateurs**.
3. Dans le champ **Nouveau code du groupe d'utilisateurs**, spécifiez le nom du nouveau groupe, puis cliquez sur le bouton **OK**.

Le nouveau groupe d'utilisateurs est ajouté à la page **Groupes d'utilisateurs**. Ajoutez ensuite des utilisateurs. Pour plus d'informations, reportez-vous à [Pour regrouper des utilisateurs dans des groupes d'utilisateurs](ui-how-users-permissions.md#to-group-users-in-a-user-group).  

## <a name="to-set-up-user-time-constraints"></a>Pour configurer des contraintes de temps utilisateur
Les administrateurs peuvent définir les périodes de temps pendant lesquelles les utilisateurs spécifiés peuvent valider, et spécifier également si le système enregistre la durée pendant laquelle les utilisateurs spécifiés ont ouvert une session. Les administrateurs peuvent également affecter des centres de gestion à des utilisateurs. Pour plus d'informations, voir [Utiliser les centres de gestion](inventory-responsibility-centers.md).

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres utilisateur**, puis sélectionnez le lien associé.
2. Sur la page **Paramètres utilisateur**, sélectionnez l'action **Nouveau**.
3. Dans le champ **ID utilisateur**, entrez l'ID d'un utilisateur, ou cliquez sur le champ pour visualiser tous les utilisateurs Windows actuels dans le système.
4. Renseignez les champs selon vos besoins.

## <a name="to-create-or-modify-a-permission-set"></a>Pour créer ou modifier un ensemble d'autorisations
Les ensembles d'autorisations fonctionnent comme des conteneurs d'autorisations, de sorte que vous puissiez gérer facilement plusieurs autorisations en un enregistrement. Lorsque vous avez créé un ensemble d'autorisations, vous devez ajouter les autorisations réelles. Pour plus d'informations, voir [Pour créer ou modifier des autorisations](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).

> [!NOTE]  
> Une solution [!INCLUDE[d365fin](includes/d365fin_md.md)] contient souvent plusieurs ensembles d'autorisations prédéfinis qui sont ajoutés par Microsoft ou par votre fournisseur de logiciels. Ces ensembles d'autorisations sont de type **Système** ou **Extension**. Vous ne pouvez pas créer ou modifier ces types d'ensembles d'autorisations ou les autorisations qu'ils contiennent. Cependant, vous pouvez les copier pour définir vos propres ensembles d'autorisations et autorisations. <br /><br />
Les ensembles d'autorisations que les utilisateurs créent, nouveaux ou copies, sont de type **Défini par l'utilisateur** et peuvent être modifiés.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Ensembles d'autorisations**, puis sélectionnez le lien associé.
2. Pour un créer un ensemble d'autorisations, choisissez l'action **Nouveau**.
3. Sur la nouvelle ligne, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-copy-a-permission-set"></a>Pour copier un ensemble d'autorisations
Lorsque vous créez des ensembles d'autorisations, vous pouvez utiliser une fonction de copie pour déplacer rapidement toutes les autorisations d'un autre ensemble d'autorisations vers un nouvel ensemble d'autorisations.

> [!NOTE]  
> Si un ensemble d'autorisations système que vous avez copié est modifié, vous serez informé (selon la sélection effectuée), de sorte que vous pouvez choisir s'il est approprié de copier ou de saisir les modifications dans votre ensemble d'autorisations défini par l'utilisateur.

1. Sur la page **Ensembles d'autorisations**, sélectionnez la ligne d'un ensemble d'autorisations à copier, puis sélectionnez l'action **Copier ensemble d'autorisations**.
2. Sur la page **Copier ensemble d'autorisations**, spécifiez le nom du nouvel ensemble d'autorisations, puis cliquez sur le bouton **OK**.
3. Activez la case à cocher **Notification en cas de modifications de l'ensemble d’autorisations** si vous souhaitez conserver un lien entre les ensembles d'autorisations originaux et copiés. Le lien est ensuite utilisé pour vous informer si le nom ou le contenu de l'ensemble d'autorisations original change dans une version future vers laquelle la solution est mise à niveau ultérieurement.

Le nouvel ensemble d'autorisations, contenant toutes les autorisations de l'ensemble d'autorisations copié, est ajouté en tant que nouvelle ligne sur la page **Ensembles d'autorisations**. Notez que les lignes sont triées alphabétiquement dans chaque type.

## <a name="to-create-or-modify-permissions-manually"></a>Pour créer ou modifier des autorisations manuellement
Cette procédure explique comment ajouter ou modifier des autorisations manuellement. Vous pouvez aussi avoir des ensembles d'autorisations générés automatiquement suite à vos actions dans l'interface utilisateur. Pour plus d'informations, reportez-vous à [Pour créer ou modifier des ensembles d'autorisations en enregistrant vos actions](ui-how-users-permissions.md#to-create-or-modify-permission-sets-by-recording-your-actions).

1. Sur la page **Ensembles d'autorisations**, sélectionnez la ligne d'un ensemble d'autorisations, puis sélectionnez l'action **Autorisations**.
2. Sur la page **Autorisations**, créez une ligne ou modifiez les champs d'une ligne existante.

Dans chacun des cinq champs de types d'accès, **Lecture**, **Insertion**, **Modification**, **Suppression**, et **Exécution**, vous pouvez sélectionner l'une des trois options d'autorisation suivantes :

|Option|Désignation|Priorité|
|------|-----------|
|**Oui**|L'utilisateur peut exécuter l'action sur l'objet en question.|Le plus élevé|
|**Indirect**|L'utilisateur peut exécuter l'action sur l'objet en question mais uniquement via un autre objet associé auquel l'utilisateur a un accès total.|Deuxièmement plus élevé|
|**Vide**|L'utilisateur ne peut pas exécuter l'action sur l'objet en question.|Le moins élevé|

### <a name="example---indirect-permission"></a>Exemple- Autorisation indirecte
L'autorisation indirecte vous permet d'utiliser un objet uniquement au travers d'un autre objet.
Par exemple, un utilisateur peut être autorisé à exécuter le codeunit 80 (Ventes-Valider). Le codeunit Ventes-Valider effectue de nombreuses tâches, parmi lesquelles modifier la table 37 (Ligne vente). Lorsque l'utilisateur valide un document vente, le codeunit Ventes-Valider, [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie si l'utilisateur est autorisé à modifier la table Ligne vente. S'il n'est pas autorisé à le faire, le codeunit ne peut pas effectuer ses tâches et l'utilisateur reçoit un message d'erreur. S'il est autorisé à le faire, le codeunit s'exécute.

L'utilisateur n'a toutefois pas besoin d'avoir entièrement accès à la table Ligne vente pour exécuter le codeunit. Si une autorisation indirecte a été accordée à l'utilisateur pour la table Ligne vente, alors le codeunit Ventes-Valider s'exécute. Lorsqu'une autorisation indirecte est accordée à un utilisateur, celui-ci peut uniquement modifier la table Ligne vente en exécutant le codeunit Ventes-Valider ou un autre objet autorisé à modifier la table Ligne vente. L'utilisateur peut uniquement modifier la table Ligne vente lorsqu'il procède à partir des modules pris en charge. L'utilisateur ne peut pas exécuter cette fonctionnalité par inadvertance ou par malveillance en suivant d'autres méthodes.

### <a name="to-limit-a-users-access-to-specific-records-in-a-table"></a>Pour limiter l'accès d'un utilisateur à des enregistrements spécifiques dans une table
Pour la sécurité au niveau des enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous utilisez des filtres de sécurité pour limiter l'accès d'un l'utilisateur aux données dans une table. Vous créez des filtres de sécurité sur les données de la table. Un filtre de sécurité décrit un ensemble d'enregistrements dans une table auxquels un utilisateur a l'autorisation d'accéder. Vous pouvez indiquer, par exemple, qu'un utilisateur peut uniquement lire les enregistrements qui contiennent des informations relatives à un client particulier. Cela signifie que l'utilisateur ne peut pas accéder aux enregistrements qui contiennent des informations sur d'autres clients. Pour plus d'informations, voir [Utilisation des filtres de sécurité](/dynamics365/business-central/dev-itpro/security/security-filters) dans l'aide sur Developer and IT Pro.


## <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Pour créer ou modifier des ensembles d'autorisations en enregistrant vos actions
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Ensembles d'autorisations**, puis sélectionnez le lien associé.
2.  Sinon, sur la page **Utilisateurs**, sélectionnez l'option **Ensembles d'autorisations**.
3.  Sur la page **Ensembles d'autorisations**, cliquez sur l'option **Nouveau**.
4.  Sur une nouvelle ligne, renseignez les champs selon vos besoins.
5.  Sélectionnez l'option **Autorisations**.
6.  Sur la page **Autorisations**, choisissez l'action **Enregistrer autorisations**, puis sélectionnez l'action **Démarrer**.

    Cette opération démarre processus d'enregistrement qui capture toutes vos actions dans l'interface utilisateur.
7.  Accédez aux différentes pages et activités dans [!INCLUDE[d365fin](includes/d365fin_md.md)] auxquelles vous voulez que les utilisateurs avec cet ensemble d'autorisations puissent accéder. Vous devez exécuter les tâches pour lesquelles vous souhaitez enregistrer des autorisations.
8.  Lorsque vous souhaitez terminer l'enregistrement, revenez sur la page **Autorisations** et choisissez l'option **Arrêter**.
9.  Cliquez sur le bouton **Oui** pour ajouter les autorisations enregistrées au nouvel ensemble d'autorisations.
10. Pour chaque objet de la liste enregistrée, indiquez si les utilisateurs peuvent insérer, modifier ou supprimer des enregistrements dans les tables enregistrées.

> [!NOTE]  
> Lorsque vous modifiez une autorisation et ainsi l'ensemble d'autorisations associé, les modifications s'appliquent également à d'autres utilisateurs auxquels l'ensemble d'autorisations est affecté.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Pour affecter des ensembles d'autorisations aux utilisateurs ou groupes d'utilisateurs
Vous pouvez affecter des autorisations aux utilisateurs de deux manières :
- Définir les ensembles d'autorisations sur la fiche utilisateur d'un utilisateur.
- Activez la case à cocher d'un utilisateur, dans une colonne, pour un ensemble d'autorisations associé, sur une ligne, sur la page **Ensemble d'autorisations par utilisateur**.
    Avec cette méthode, vous pouvez également affecter des ensembles d'autorisations à des groupes d'utilisateurs.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Pour affecter un ensemble d'autorisations sur une fiche utilisateur
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Utilisateurs**, puis sélectionnez le lien associé.
2. Sélectionnez l'utilisateur auquel affecter des autorisations.
Tous les ensembles d’autorisations qui sont affectés à l’utilisateur sont affichés dans le récapitulatif **Ensemble d’autorisations utilisateur**.
3. Sélectionnez l'option **Modifier** pour ouvrir la page **Fiche utilisateur**.
4. Sur le raccourci **Ensembles d'autorisations utilisateur**, renseignez les champs, le cas échéant sur une nouvelle ligne. Pour plus d'informations, voir [Pour créer ou modifier des ensembles d'autorisations](ui-how-users-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Pour affecter un ensemble d'autorisations sur la page **Ensemble d'autorisations par utilisateur**  
La procédure suivante explique comment affecter des ensembles d'autorisations à un utilisateur sur la page **Ensemble d'autorisations par utilisateur**. Les étapes sont similaires sur la page **Ensemble d'autorisations par groupe d'utilisateurs**.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Utilisateurs**, puis sélectionnez le lien associé.
2. Sur la page **Utilisateurs**, sélectionnez l'utilisateur approprié, puis cliquez sur l'action **Ensemble d'autorisations par utilisateur**.
3. Sur la page **Ensemble d'autorisations par utilisateur**, activez la case à cocher **[nom d'utilisateur]** sur une ligne pour l'ensemble d'autorisations approprié pour affecter l'ensemble à l'utilisateur.
4. Activez la case à cocher **Tous les utilisateurs** pour affecter l'ensemble d'autorisations à tous les utilisateurs.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Pour afficher l'aperçu des autorisations d'un utilisateur
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Utilisateurs**, puis sélectionnez le lien associé.
2. Ouvrez la fiche de l'utilisateur approprié.
3. Sélectionnez l'option **Autorisations effectives**.

    La section **Autorisations** répertorie tous les objets de base de données auxquels l'utilisateur a accès. Vous ne pouvez pas modifier cette section.

    La section **Par ensemble d'autorisations** affiche les ensembles d'autorisations affectés via lesquels les autorisations sont accordées à l'utilisateur, la source et le type d'ensemble d'autorisations, et l'étendue des différents types d'accès sont autorisés.

    Pour chaque ligne sélectionnée dans la section **Autorisations**, la section **Par ensemble d'autorisations** affiche les ensembles d'autorisations ou les ensembles via lesquels l'autorisation est accordée. Dans cette section, vous pouvez modifier la valeur de chacun des cinq champs de types d'accès, **Lecture**, **Insertion**, **Modification**, **Suppression** et **Exécution**.   

    > [!NOTE]  
    > Seuls les ensembles d'autorisations de type **Défini par l'utilisateur** peuvent être modifiés.<br /><br />
    > Les lignes du droit source proviennent du plan d'abonnement. Les valeurs d’autorisation du droit sont prioritaires sur les valeurs des autres ensembles d’autorisations si elles ont un rang supérieur. Une valeur dans un ensemble d'autorisations de non droit qui a un rang supérieur à la valeur associée dans le droit sera entourée de parenthèses pour indiquer qu'elle n'est pas effective car elle est outrepassée par le droit. Pour une explication sur le classement, voir [Pour créer ou modifier des autorisations](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

4. Pour modifier un ensemble d'autorisations, dans la section **Par ensemble d'autorisations**, sur la ligne d'un ensemble d'autorisations approprié de type **Défini par l'utilisateur**, choisissez l'un des cinq champs de type d'accès et sélectionnez une valeur différente.

5. Pour modifier des autorisations individuelles dans l'ensemble d'autorisations, choisissez la valeur dans le champ **Ensemble d'autorisations** pour ouvrir la page **Autorisations**. Suivez la procédure décrite dans [Pour créer ou modifier des autorisations](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Lorsque vous modifiez un ensemble d'autorisations, les modifications s'appliquent également à d'autres utilisateurs auxquels l'ensemble d'autorisations est affecté.

## <a name="see-also"></a>Voir aussi
[Sécurité et protection dans Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Comprendre les utilisateurs, les profils et les tableaux de bord](admin-users-profiles-roles.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Modification des fonctionnalités affichées](ui-experiences.md)  
[Administration](admin-setup-and-administration.md)  
[Ajouter des utilisateurs à Office 365 for business](https://aka.ms/CreateOffice365Users)  
[Guide des licences Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing)
