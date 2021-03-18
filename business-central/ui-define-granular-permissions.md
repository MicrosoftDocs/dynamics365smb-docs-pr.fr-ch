---
title: Définir les autorisations granulaires | Microsoft Docs
description: Décrit comment accorder aux utilisateurs l’accès aux objets en leur attribuant des ensembles d’autorisations.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 48547fbe3cb2bb7cf509c1b0720cb6ccfc58cd97
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385889"
---
# <a name="assign-permissions-to-users-and-groups"></a>Attribuer des autorisations aux utilisateurs et aux groupes

Le système de sécurité de [!INCLUDE[prod_short](includes/prod_short.md)] vous permet de contrôler les objets auxquels un utilisateur peut accéder dans chaque base de données ou environnement. Vous pouvez spécifier pour chaque utilisateur s’il peut lire, modifier ou entrer des données dans les objets de base de données sélectionnés. Pour des informations détaillées, voir [Sécurité des données](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) dans l’aide sur Developer and IT-Pro pour [!INCLUDE[prod_short](includes/prod_short.md)].

Avant d’attribuer des autorisations à des utilisateurs et à des groupes d’utilisateurs, vous devez définir ceux qui peuvent se connecter en créant des utilisateurs en fonction de la licence définie dans le Centre d’administration Microsoft 365. Pour plus d’informations, voir [Créer des utilisateurs conformément aux licences](ui-how-users-permissions.md).

Dans [!INCLUDE[prod_short](includes/prod_short.md)], il existe deux niveaux d’autorisations pour les objets de base de données :

- les autorisations globales en fonction de la licence, également appelées « droit » ;
- les autorisations plus détaillées attribuées de l’intérieur [!INCLUDE[prod_short](includes/prod_short.md)].

Pour faciliter la gestion des autorisations pour plusieurs utilisateurs, vous pouvez les organiser en groupes d’utilisateurs et ainsi affecter ou modifier un ensemble d’autorisations pour plusieurs utilisateurs en une seule action. Pour plus d’informations, voir [Pour gérer les autorisations via les groupes d’utilisateurs](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Une autre méthode permettant de définir les fonctionnalités auxquelles un utilisateur a accès consiste à définir le champ **Expérience** sur la page **Informations société**. Pour plus d’informations, voir [Modifier les fonctionnalités affichées](ui-experiences.md).
>
> Vous pouvez également définir ce que les utilisateurs voient dans l’interface utilisateur et la manière dont ils interagissent avec les fonctionnalités autorisées par le biais de pages. Pour ce faire, vous devez utiliser des profils, que vous attribuez à différents types d’utilisateurs en fonction de leur poste ou service. Pour en savoir plus, reportez-vous à [Gérer les profils](admin-users-profiles-roles.md) et [Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## <a name="to-assign-permission-sets-to-users"></a>Pour affecter des ensembles d’autorisations à des utilisateurs

Un ensemble d’autorisations est une collection d’autorisations pour des objets de base de données spécifiques. Tous les utilisateurs doivent être affectés à une ou plusieurs séries d’autorisations avant de pouvoir accéder à [!INCLUDE[prod_short](includes/prod_short.md)].

Une solution [!INCLUDE[prod_short](includes/prod_short.md)] contient souvent plusieurs ensembles d’autorisations prédéfinis qui sont ajoutés par Microsoft ou par votre fournisseur de solutions. Vous pouvez également ajouter de nouveaux ensembles d’autorisations personnalisés pour répondre aux besoins de votre organisation. Pour plus d’informations, voir [Pour créer ou modifier des ensembles d’autorisations](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

> [!NOTE]
> Si vous ne souhaitez pas limiter l’accès d’un utilisateur plus que ce qui est déjà défini par la licence, vous pouvez attribuer à l’utilisateur un ensemble d’autorisations spéciales appelé SUPER. Cet ensemble d’autorisations garantit que l’utilisateur peut accéder à tous les objets spécifiés dans la licence.
>
> Un utilisateur disposant de la licence Essential et de l’ensemble d’autorisations SUPER a accès à davantage de fonctionnalités que les utilisateurs possédant la licence de membre d’équipe et l’ensemble d’autorisations SUPER.

Vous pouvez affecter des ensembles d’autorisations aux utilisateurs de deux manières :

- à partir de la page **Fiche utilisateur** en sélectionnant les ensembles d’autorisations à attribuer à l’utilisateur ;
- à partir de la page **Ensemble d’autorisations par utilisateur** en sélectionnant les utilisateurs auxquels un ensemble d’autorisations est attribué.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Pour affecter un ensemble d’autorisations sur une fiche utilisateur

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
2. Sélectionnez l’utilisateur auquel affecter des autorisations.
Tous les ensembles d’autorisations qui sont affectés à l’utilisateur sont affichés dans le récapitulatif **Ensemble d’autorisations utilisateur**.
3. Sélectionnez l’option **Modifier** pour ouvrir la page **Fiche utilisateur**.
4. Sur le raccourci **Ensembles d’autorisations utilisateur**, renseignez les champs, le cas échéant sur une nouvelle ligne. Pour plus d’informations, voir [Pour créer ou modifier des ensembles d’autorisations](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Pour affecter un ensemble d’autorisations sur la page Ensemble d’autorisations par utilisateur

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
2. Sur la page **Utilisateurs**, sélectionnez l’utilisateur approprié, puis cliquez sur l’action **Ensemble d’autorisations par utilisateur**.
3. Sur la page **Ensemble d’autorisations par utilisateur**, activez la case à cocher **[nom d’utilisateur]** sur une ligne pour l’ensemble d’autorisations approprié pour affecter l’ensemble à l’utilisateur.
4. Activez la case à cocher **Tous les utilisateurs** pour affecter l’ensemble d’autorisations à tous les utilisateurs.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Pour afficher l’aperçu des autorisations d’un utilisateur

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
2. Ouvrez la fiche de l’utilisateur approprié.
3. Sélectionnez l’option **Autorisations effectives**.

    La section **Autorisations** répertorie tous les objets de base de données auxquels l’utilisateur a accès. Vous ne pouvez pas modifier cette section.

    La section **Par ensemble d’autorisations** affiche les ensembles d’autorisations affectés via lesquels les autorisations sont accordées à l’utilisateur, la source et le type d’ensemble d’autorisations, et l’étendue des différents types d’accès sont autorisés.

    Pour chaque ligne sélectionnée dans la section **Autorisations**, la section **Par ensemble d’autorisations** affiche les ensembles d’autorisations ou les ensembles via lesquels l’autorisation est accordée. Dans cette section, vous pouvez modifier la valeur de chacun des cinq champs de types d’accès, **Lecture**, **Insertion**, **Modification**, **Suppression** et **Exécution**.

    > [!NOTE]  
    > Seuls les ensembles d’autorisations de type **Défini par l’utilisateur** peuvent être modifiés.
    >
    > Les lignes du droit source proviennent de la licence d’abonnement. Les valeurs d’autorisation du droit sont prioritaires sur les valeurs des autres ensembles d’autorisations si elles ont un rang supérieur. Une valeur dans un ensemble d’autorisations de non droit qui a un rang supérieur à la valeur associée dans le droit sera entourée de parenthèses pour indiquer qu’elle n’est pas effective car elle est outrepassée par le droit.
    >
    > Pour une explication sur le classement, voir [Pour créer ou modifier des autorisations](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

4. Pour modifier un ensemble d’autorisations, dans la section **Par ensemble d’autorisations**, sur la ligne d’un ensemble d’autorisations approprié de type **Défini par l’utilisateur**, choisissez l’un des cinq champs de type d’accès et sélectionnez une valeur différente.

5. Pour modifier des autorisations individuelles dans l’ensemble d’autorisations, choisissez la valeur dans le champ **Ensemble d’autorisations** pour ouvrir la page **Autorisations**. Suivez la procédure décrite dans [Pour créer ou modifier des autorisations](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Lorsque vous modifiez un ensemble d’autorisations, les modifications s’appliquent également à d’autres utilisateurs auxquels l’ensemble d’autorisations est affecté.

## <a name="to-create-or-modify-a-permission-set"></a>Pour créer ou modifier un ensemble d’autorisations

Les ensembles d’autorisations fonctionnent comme des conteneurs d’autorisations, de sorte que vous puissiez gérer facilement plusieurs autorisations en un enregistrement.

> [!NOTE]  
> Une solution [!INCLUDE[prod_short](includes/prod_short.md)] contient souvent plusieurs ensembles d’autorisations prédéfinis qui sont ajoutés par Microsoft ou par votre fournisseur de logiciels. Ces ensembles d’autorisations sont de type **Système** ou **Extension**. Vous ne pouvez pas créer ou modifier ces types d’ensembles d’autorisations ou les autorisations qu’ils contiennent. Cependant, vous pouvez les copier pour définir vos propres ensembles d’autorisations et autorisations.
>
> Les ensembles d’autorisations que les utilisateurs créent, nouveaux ou copies, sont de type **Défini par l’utilisateur** et peuvent être modifiés.

### <a name="to-create-new-permission-set-from-scratch"></a>Pour créer un nouvel ensemble d’autorisations à partir de zéro

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Ensembles d’autorisations**, puis sélectionnez le lien associé.
2. Pour un créer un ensemble d’autorisations, choisissez l’action **Nouveau**.
3. Sur la nouvelle ligne, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Lorsque vous avez créé un ensemble d’autorisations, vous devez ajouter les autorisations réelles. Pour plus d’informations, voir [Pour créer ou modifier des autorisations manuellement](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-copy-a-permission-set"></a>Pour copier un ensemble d’autorisations

Vous pouvez également utiliser une fonction de copie pour déplacer rapidement toutes les autorisations d’un autre ensemble d’autorisations vers un nouvel ensemble d’autorisations.

> [!NOTE]  
> Si un ensemble d’autorisations système que vous avez copié est modifié, vous serez informé (selon la sélection effectuée), de sorte que vous pouvez choisir s’il est approprié de copier ou de saisir les modifications dans votre ensemble d’autorisations défini par l’utilisateur.

1. Sur la page **Ensembles d’autorisations**, sélectionnez la ligne d’un ensemble d’autorisations à copier, puis sélectionnez l’action **Copier ensemble d’autorisations**.
2. Sur la page **Copier ensemble d’autorisations**, spécifiez le nom du nouvel ensemble d’autorisations, puis cliquez sur le bouton **OK**.
3. Activez la case à cocher **Notification en cas de modifications de l’ensemble d’autorisations** si vous souhaitez conserver un lien entre les ensembles d’autorisations originaux et copiés. Le lien est ensuite utilisé pour vous informer si le nom ou le contenu de l’ensemble d’autorisations original change dans une version future vers laquelle la solution est mise à niveau ultérieurement.

Le nouvel ensemble d’autorisations, contenant toutes les autorisations de l’ensemble d’autorisations copié, est ajouté en tant que nouvelle ligne sur la page **Ensembles d’autorisations**. Vous pouvez maintenant modifier les autorisations dans le nouvel ensemble d’autorisations. Notez que les lignes sont triées alphabétiquement dans chaque type.

### <a name="to-export-and-import-a-permission-set"></a>Pour exporter et importer un ensemble d’autorisations

Pour configurer rapidement des autorisations, vous pouvez importer des ensembles d’autorisations que vous avez exportés d’un autre locataire [!INCLUDE[prod_short](includes/prod_short.md)].

Dans les environnements multi-locataires, un ensemble d’autorisations sera importé dans un locataire spécifique, c’est-à-dire que la portée de l’importation est "Locataire".

1. Dans le locataire 1, sur la page **Ensembles d’autorisations**, sélectionnez la ligne ou les lignes des ensembles d’autorisations à exporter, puis choisissez l’action **Exporter des ensembles d’autorisations**.

    Un fichier xml est créé dans le dossier de téléchargement de votre machine. Par défaut, il est nommé "Exporter des ensembles d’autorisations.xml"

2. Dans le locataire 2, dans la page **Ensembles d’autorisations**, sélectionnez l’action **Importer des ensembles d’autorisations**.
3. Dans la page de la boîte de dialogue **Importer des ensembles d’autorisations**, envisagez de fusionner les ensembles d’autorisations existants avec de nouveaux ensembles d’autorisations dans le fichier xml.

    Si vous sélectionnez **Mettre à jour les autorisations existantes**, les ensembles d’autorisations existants portant le même nom que ceux qui existent dans le fichier xml seront fusionnés avec les ensembles d’autorisations importés.

    Si vous ne cochez pas la case **Mettre à jour les autorisations existantes**, les ensembles d’autorisations portant le même nom que ceux qui existent dans le fichier xml seront ignorés lors de l’importation. Dans ce cas, vous serez informé des ensembles d’autorisations qui sont ignorés.

4. Dans la boîte de dialogue **Importer**, recherchez et sélectionnez le fichier xml à importer, puis choisissez l’action **Ouvrir**.

Les ensembles d’autorisations sont importés.

## <a name="to-create-or-modify-permissions-manually"></a>Pour créer ou modifier des autorisations manuellement

Cette procédure explique comment ajouter ou modifier des autorisations manuellement. Vous pouvez aussi avoir des autorisations générées automatiquement suite à vos actions dans l’interface utilisateur. Pour plus d’informations, voir [Pour créer ou modifier des autorisations en enregistrant vos actions](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions).

> [!NOTE]
> Lorsque vous modifiez une autorisation et ainsi l’ensemble d’autorisations associé, les modifications s’appliquent également à d’autres utilisateurs auxquels l’ensemble d’autorisations est affecté.

1. Sur la page **Ensembles d’autorisations**, sélectionnez la ligne d’un ensemble d’autorisations, puis sélectionnez l’action **Autorisations**.
2. Sur la page **Autorisations**, créez une ligne ou modifiez les champs d’une ligne existante.

Dans chacun des cinq champs de types d’accès, **Lecture**, **Insertion**, **Modification**, **Suppression**, et **Exécution**, vous pouvez sélectionner l’une des trois options d’autorisation suivantes :

|Option|Désignation|Priorité|
|------|-----------|-------|
|**Oui**|L’utilisateur peut exécuter l’action sur l’objet en question.|Le plus élevé|
|**Indirect**|L’utilisateur peut exécuter l’action sur l’objet en question mais uniquement via un autre objet associé auquel l’utilisateur a un accès total. Pour plus d’informations sur les autorisations indirectes, voir [Propriété Autorisations](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property) dans l’aide sur Developer and IT-Pro|Deuxièmement plus élevé|
|**Vide**|L’utilisateur ne peut pas exécuter l’action sur l’objet en question.|Le moins élevé|

### <a name="example---indirect-permission"></a>Exemple- Autorisation indirecte

L’autorisation indirecte vous permet d’utiliser un objet uniquement au travers d’un autre objet.
Par exemple, un utilisateur peut être autorisé à exécuter le codeunit 80 (Ventes-Valider). Le codeunit Ventes-Valider effectue de nombreuses tâches, parmi lesquelles modifier la table 37 (Ligne vente). Lorsque l’utilisateur valide un document vente, le codeunit Ventes-Valider, [!INCLUDE[prod_short](includes/prod_short.md)] vérifie si l’utilisateur est autorisé à modifier la table Ligne vente. S’il n’est pas autorisé à le faire, le codeunit ne peut pas effectuer ses tâches et l’utilisateur reçoit un message d’erreur. S’il est autorisé à le faire, le codeunit s’exécute.

L’utilisateur n’a toutefois pas besoin d’avoir entièrement accès à la table Ligne vente pour exécuter le codeunit. Si une autorisation indirecte a été accordée à l’utilisateur pour la table Ligne vente, alors le codeunit Ventes-Valider s’exécute. Lorsqu’une autorisation indirecte est accordée à un utilisateur, celui-ci peut uniquement modifier la table Ligne vente en exécutant le codeunit Ventes-Valider ou un autre objet autorisé à modifier la table Ligne vente. L’utilisateur peut uniquement modifier la table Ligne vente lorsqu’il procède à partir des modules pris en charge. L’utilisateur ne peut pas exécuter cette fonctionnalité par inadvertance ou par malveillance en suivant d’autres méthodes.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Pour créer ou modifier des autorisations en enregistrant vos actions

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Ensembles d’autorisations**, puis sélectionnez le lien associé.
2. Sinon, sur la page **Utilisateurs**, sélectionnez l’option **Ensembles d’autorisations**.
3. Sur la page **Ensembles d’autorisations**, cliquez sur l’option **Nouveau**.
4. Sur une nouvelle ligne, renseignez les champs selon vos besoins.
5. Sélectionnez l’option **Autorisations**.
6. Sur la page **Autorisations**, choisissez l’action **Enregistrer autorisations**, puis sélectionnez l’action **Démarrer**.

    Cette opération démarre processus d’enregistrement qui capture toutes vos actions dans l’interface utilisateur.
7. Accédez aux différentes pages et activités dans [!INCLUDE[prod_short](includes/prod_short.md)] auxquelles vous voulez que les utilisateurs avec cet ensemble d’autorisations puissent accéder. Vous devez exécuter les tâches pour lesquelles vous souhaitez enregistrer des autorisations.
8. Lorsque vous souhaitez terminer l’enregistrement, revenez sur la page **Autorisations** et choisissez l’option **Arrêter**.
9. Cliquez sur le bouton **Oui** pour ajouter les autorisations enregistrées au nouvel ensemble d’autorisations.
10. Pour chaque objet de la liste enregistrée, indiquez si les utilisateurs peuvent insérer, modifier ou supprimer des enregistrements dans les tables enregistrées.

## <a name="security-filters---to-limit-a-users-access-to-specific-records-in-a-table"></a>Filtres de sécurité : pour limiter l’accès d’un utilisateur à des enregistrements spécifiques dans une table

Pour la sécurité au niveau des enregistrements dans [!INCLUDE[prod_short](includes/prod_short.md)], vous utilisez des filtres de sécurité pour limiter l’accès d’un l’utilisateur aux données dans une table. Vous créez des filtres de sécurité sur les données de la table. Un filtre de sécurité décrit un ensemble d’enregistrements dans une table auxquels un utilisateur a l’autorisation d’accéder. Vous pouvez indiquer, par exemple, qu’un utilisateur peut uniquement lire les enregistrements qui contiennent des informations relatives à un client particulier. Cela signifie que l’utilisateur ne peut pas accéder aux enregistrements qui contiennent des informations sur d’autres clients. Pour plus d’informations, voir [Utilisation des filtres de sécurité](/dynamics365/business-central/dev-itpro/security/security-filters) dans l’aide sur Developer and IT Pro.

## <a name="to-manage-permissions-through-user-groups"></a>Pour gérer les autorisations via des groupes d’utilisateurs

Vous pouvez définir des groupes d’utilisateurs pour vous aider à gérer les ensembles d’autorisations pour des groupes d’utilisateurs de votre société.

Commencez par créer un groupe d’utilisateurs. Ensuite, vous affectez des ensembles d’autorisations au groupe afin de définir l’objet auquel les utilisateurs du groupe peuvent accéder. Lorsque vous ajoutez un utilisateur au groupe, les ensembles d’autorisations définis pour le groupe s’appliquent à l’utilisateur.

Les ensembles d’autorisations attribués à un utilisateur via un groupe d’utilisateurs restent synchronisés afin qu’une modification des autorisations du groupe d’utilisateurs soit automatiquement propagée à l’utilisateur. Si vous supprimez un utilisateur d’un groupe d’utilisateurs, les autorisations concernées sont automatiquement révoquées.

### <a name="to-group-users-in-user-groups"></a>Pour regrouper des utilisateurs dans des groupes d’utilisateurs

La procédure suivante explique comment créer manuellement des groupes d’utilisateurs. Pour créer automatiquement des groupes d’utilisateurs, voir [Pour copier un groupe d’utilisateurs et tous ses ensembles d’autorisations](ui-define-granular-permissions.md#to-copy-a-user-group-and-all-its-permission-sets).

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Groupes d’utilisateurs**, puis sélectionnez le lien associé.
2. Sinon, sur la page **Utilisateurs**, sélectionnez l’option **Groupes d’utilisateurs**.
3. Sur la page **Groupe d’utilisateurs**, sélectionnez l’action **Membres du groupe d’utilisateurs**.
4. Sur la page **Groupe d’utilisateurs**, choisissez l’action **Ajouter des utilisateurs**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Pour copier un groupe d’utilisateurs et tous ses ensembles d’autorisations

Pour définir rapidement un nouveau groupe d’utilisateurs, vous pouvez copier tous les ensembles d’autorisations d’un groupe d’utilisateurs existant vers un nouveau groupe d’utilisateurs.

> [!NOTE]
> Les membres du groupe d’utilisateurs ne sont pas copiés vers le nouveau groupe d’utilisateurs. Vous devez les ajouter manuellement ensuite. Pour plus d’informations, reportez-vous à [Pour regrouper des utilisateurs dans des groupes d’utilisateurs](ui-define-granular-permissions.md#to-group-users-in-user-groups).

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Groupes d’utilisateurs**, puis sélectionnez le lien associé.
2. Sélectionnez le groupe d’utilisateurs à partir duquel vous souhaitez copier, puis choisissez l’action **Copier groupe d’utilisateurs**.
3. Dans le champ **Nouveau code du groupe d’utilisateurs**, spécifiez le nom du nouveau groupe, puis cliquez sur le bouton **OK**.

Le nouveau groupe d’utilisateurs est ajouté à la page **Groupes d’utilisateurs**. Ajoutez ensuite des utilisateurs. Pour plus d’informations, voir [Pour regrouper des utilisateurs dans des groupes d’utilisateurs](ui-define-granular-permissions.md#to-group-users-in-user-groups).  

### <a name="to-assign-permission-sets-to-user-groups"></a>Pour affecter des ensembles d’autorisations à des groupes d’utilisateurs

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Groupes d’utilisateurs**, puis sélectionnez le lien associé.
2. Sélectionnez le groupe d’utilisateurs auquel affecter des autorisations.
Tous les ensembles d’autorisations qui sont affectés à l’utilisateur sont affichés dans le récapitulatif **Ensemble d’autorisations utilisateur**.
3. Choisissez l’action **Ensemble d’autorisations utilisateur** pour ouvrir la page **Ensembles d’autorisations utilisateur**.
4. Sur la page **Ensembles d’autorisations utilisateur**, renseignez les champs, le cas échéant, sur une nouvelle ligne.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Pour affecter un ensemble d’autorisations sur la page **Ensemble d’autorisations par groupe d’utilisateurs**

La procédure suivante explique comment affecter des ensembles d’autorisations à un groupe d’utilisateurs sur la page **Ensemble d’autorisations par groupe d’utilisateurs**.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis sélectionnez le lien associé.
2. Sur la page **Utilisateurs**, sélectionnez l’utilisateur approprié, puis cliquez sur l’action **Ensemble d’autorisations par groupe d’utilisateurs**.
3. Sur la page **Ensemble d’autorisations par groupe d’utilisateurs**, activez la case à cocher **[nom groupe d’utilisateurs]** sur une ligne pour l’ensemble d’autorisations approprié pour affecter l’ensemble au groupe d’utilisateurs.
4. Activez la case à cocher **Tous les groupes d’utilisateurs** pour affecter l’ensemble d’autorisations à tous les groupes d’utilisateurs.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Pour supprimer des autorisations obsolètes de tous les ensembles d’autorisations

1. Dans la page **Ensemble d’autorisations**, choisissez l’option **Supprimer les autorisations obsolètes**.

## <a name="to-set-up-user-time-constraints"></a>Pour configurer des contraintes de temps utilisateur

Les administrateurs peuvent définir les périodes de temps pendant lesquelles les utilisateurs spécifiés peuvent valider, et spécifier également si le système enregistre la durée pendant laquelle les utilisateurs spécifiés ont ouvert une session. Les administrateurs peuvent également affecter des centres de gestion à des utilisateurs. Pour plus d’informations, voir [Utiliser les centres de gestion](inventory-responsibility-centers.md).

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres utilisateur**, puis sélectionnez le lien associé.
2. Sur la page **Paramètres utilisateur**, sélectionnez l’action **Nouveau**.
3. Dans le champ **ID utilisateur**, entrez l’ID d’un utilisateur, ou cliquez sur le champ pour visualiser tous les utilisateurs Windows actuels dans le système.
4. Renseignez les champs selon vos besoins.


## <a name="viewing-permission-changes-telemetry"></a>Affichage de la télémétrie des modifications d’autorisation 

Vous pouvez configurer [!INCLUDE[prod_short](includes/prod_short.md)] pour envoyer les modifications apportées à l’autorisation à une ressource Application Insights dans Microsoft Azure. Ensuite, à l’aide d’Azure Monitor, vous créez des états et configurez des alertes sur les données collectées. Pour plus d’informations, voir les articles suivants dans l’aide [!INCLUDE[prod_short](includes/prod_short.md)] dédiée aux développeurs et professionnels de l’informatique.

- [Surveillance et analyse de la télémétrie - Activation d’Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analyse de la télémétrie de surveillance des champs](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="see-also"></a>Voir aussi

[Créer des utilisateurs en fonction des licences](ui-how-users-permissions.md)  
[Gérer les profils](admin-users-profiles-roles.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Ajouter des utilisateurs à Microsoft 365 pour les entreprises](https://aka.ms/CreateOffice365Users)  
[Sécurité et protection dans Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) dans l’aide sur Developer and IT-Pro


[!INCLUDE[footer-include](includes/footer-banner.md)]