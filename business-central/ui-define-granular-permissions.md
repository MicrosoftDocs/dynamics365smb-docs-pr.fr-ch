---
title: Définir des autorisations granulaires
description: Cet article décrit comment définir des autorisations granulaires et affecter à chaque utilisateur les ensembles d’autorisations dont il a besoin pour effectuer son travail.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
ms.service: dynamics-365-business-central
---

# Attribuer des autorisations aux utilisateurs et aux groupes

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Le système de sécurité [!INCLUDE[prod_short](includes/prod_short.md)] contrôle les objets auxquels un utilisateur peut accéder dans chaque base de données ou environnement, en combinaison avec la licence de l’utilisateur attribuée. Vous pouvez spécifier pour chaque utilisateur s’il peut lire, modifier ou saisir des données dans les objets de base de données. Pour des informations détaillées, voir [Sécurité des données](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) dans le contenu pour développeurs et administrateurs pour [!INCLUDE[prod_short](includes/prod_short.md)].

Avant d’attribuer des autorisations à des utilisateurs et à des groupes d’utilisateurs, vous devez définir ceux qui peuvent se connecter en créant des utilisateurs en fonction de leur licence. Pour plus d’informations, voir [Créer des utilisateurs conformément aux licences](ui-how-users-permissions.md).

Dans [!INCLUDE[prod_short](includes/prod_short.md)], il existe deux niveaux d’autorisations pour les objets de base de données :

- les autorisations globales en fonction de la licence, également appelées « droit » ;

  Les licences incluent des ensembles d’autorisations par défaut. À partir la 1re vague de lancement 2022, les administrateurs peuvent personnaliser ces autorisations par défaut pour les types de licence concernés. Pour plus d’informations, voir [Configurer les autorisations en fonction des licences](ui-how-users-permissions.md#licensespermissions).  

- Autorisations détaillées que vous attribuez dans [!INCLUDE[prod_short](includes/prod_short.md)].

Cet article décrit comment vous pouvez définir, utiliser et appliquer des autorisations dans [!INCLUDE [prod_short](includes/prod_short.md)] pour changer la configuration par défaut.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Pour plus d’informations, voir [Accès administrateur délégué à Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)] en ligne inclut des groupes d’utilisateurs par défaut qui sont attribués automatiquement aux utilisateurs en fonction de leur licence. Vous pouvez modifier la configuration par défaut en modifiant ou en ajoutant des groupes de sécurité, des ensembles d’autorisations et des autorisations. Le tableau suivant décrit les principaux scénarios de modification des autorisations par défaut.  

|À  |Voir  |
|---------|---------|
|Pour faciliter la gestion des autorisations pour plusieurs utilisateurs, vous pouvez les organiser en groupes de sécurité, puis affecter ou modifier un ensemble d’autorisations pour plusieurs utilisateurs en une seule action.| [Pour gérer les autorisations via des groupes d’utilisateurs](#to-manage-permissions-through-user-groups) |
|Pour gérer des ensembles d’autorisations pour des utilisateurs spécifiques | [Pour affecter des ensembles d’autorisations à des utilisateurs](#to-assign-permission-sets-to-users) |
|Pour savoir comment définir un ensemble d’autorisations|[Pour créer un ensemble d’autorisations](#to-create-a-permission-set)|
|Pour afficher ou résoudre les autorisations d’un utilisateur|[Pour afficher l’aperçu des autorisations d’un utilisateur](#to-get-an-overview-of-a-users-permissions)|
|Pour en savoir plus sur la sécurité au niveau des enregistrements|[Filtres de sécurité : pour limiter l’accès d’un utilisateur à des enregistrements spécifiques dans une table](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> Une façon plus vaste de définir les fonctionnalités auxquelles un utilisateur a accès consiste à définir le champ **Expérience** sur la page **Informations société**. Pour plus d’informations, voir [Modifier les fonctionnalités affichées](ui-experiences.md).
>
> Vous pouvez également définir les fonctionnalités disponibles aux utilisateurs dans l’interface utilisateur et la manière dont ils interagissent avec elles par le biais de pages. Pour ce faire, vous devez utiliser des profils, que vous attribuez à différents types d’utilisateurs en fonction de leur poste ou service. Pour en savoir plus, reportez-vous à [Gérer les profils](admin-users-profiles-roles.md) et [Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## Pour créer un ensemble d’autorisations

> [!NOTE]
> Dans la 2è vague de lancement 2022, nous avons simplifié l’ajout d’autorisations aux ensembles d’autorisations. Plutôt que d’ajouter des autorisations individuellement, vous pouvez ajouter des ensembles d’autorisations entiers. Si nécessaire, vous pouvez ensuite exclure des autorisations individuelles. Pour en savoir plus, voir [Pour ajouter d’autres ensembles d’autorisations](#to-add-other-permission-sets). Pour rendre cela possible, nous avons remplacé la page Ensemble d’autorisations par une nouvelle. Les principales différences sont les nouveaux volets **Ensembles d’autorisations** et **Résultats**, et le récapitulatif **Autorisations incluses**. Pour continuer à utiliser la page Autorisations remplacée, dans la page **Ensembles d’autorisations**, choisissez l’action **Autorisations (héritées)**.

La maintenance est également plus facile. Lorsque vous ajoutez une autorisation système, votre ensemble d’autorisations défini par l’utilisateur est automatiquement mis à jour avec toutes les modifications apportées par Microsoft à ces autorisations.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Ensembles d’autorisations**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Sur la nouvelle ligne, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Sélectionnez l’option **Autorisations**.
5. Sur la page **Ensemble d’autorisations**, dans le champ **Type**, incluez ou excluez les autorisations sur l’objet comme suit :

  Pour inclure l’autorisation, sélectionnez **Inclure**, puis choisissez le niveau d’accès à donner dans les champs **Autorisation de lecture**, **Autorisation d’insertion**, **Autorisation de modification**, **Autorisation de suppression** et **Autorisation d’exécution**. Le tableau suivant décrit les options.

  |Option|Désignation|Priorité|
  |------|-----------|-------|
  |**Vide**|L’utilisateur ne peut pas exécuter l’action sur l’objet.|Le moins élevé|  
  |**Oui**|L’utilisateur peut exécuter l’action sur l’objet.|Le plus élevé|
  |**Indirect**|L’utilisateur peut exécuter l’action sur l’objet, mais uniquement via un autre objet associé auquel l’utilisateur a un accès total. Pour plus d’informations, voir [Exemple - Autorisation indirecte](#example---indirect-permission) dans cet article, et [Propriété Autorisations](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property#example---indirect-permission) dans l’aide sur Developer and IT-Pro.|Deuxièmement plus élevé|
  
  Pour exclure l’autorisation, ou un ou plusieurs niveaux d’accès, choisissez **Exclure**, puis choisissez le niveau d’accès à accorder. Le tableau suivant décrit les options.

  |Option|Désignation|
  |------|-----------|-------|
  |**Vide**|Utilisez le niveau d’accès en fonction de la hiérarchie des autorisations dans l’ensemble.  |
  |**Exclure**|Supprimez le niveau d’accès spécifique de l’objet.|
  |**Réduire à Indirect**|Modifiez le niveau d’accès sur Indirect si des ensembles d’autorisations donnent un accès Direct à l’objet. Par exemple, choisissez cette option si l’ensemble d’autorisations donne un accès direct aux écritures comptables, mais vous ne voulez pas que les utilisateurs aient un accès complet aux écritures.|
  
  > [!NOTE]
  > Si une autorisation se trouve à la fois dans un ensemble d’autorisations qui est inclus et dans un ensemble d’autorisations qui est exclu, l’autorisation sera exclue.

6. Utilisez les champs **Type d’objet** et **ID d’objet** pour spécifier l’objet auquel vous donnez accès.

  > [!TIP]
  > Les nouvelles lignes affichent les valeurs par défaut. Par exemple, le champ **Type d’objet** contient **Données de table**, et le champ **ID d’objet** contient **0**. Les valeurs par défaut ne sont que des espaces réservés et ne sont pas utilisées. Vous devez choisir un type d’objet et un objet dans le champ **ID d’objet** avant de pouvoir créer une autre ligne.

7. Facultatif : si vous définissez des autorisations pour un type d’objet Données de table, dans le champ **Filtre de sécurité** vous pouvez filtrer les données auxquelles un utilisateur peut accéder dans les champs de la table sélectionnée. Par exemple, vous pouvez souhaiter laisser un utilisateur accéder uniquement aux enregistrements qui contiennent des informations relatives à un client particulier. Pour plus d’informations, voir [Les filtres de sécurité limitent l’accès d’un utilisateur à des enregistrements spécifiques dans une table](#security-filters-limit-a-users-access-to-specific-records-in-a-table) et [Utilisation des filtres de sécurité](/dynamics365/business-central/dev-itpro/security/security-filters).
8. Facultatif : sur le volet **Ensembles d’autorisations**, ajoutez un ou plusieurs autres ensembles d’autorisations. Pour en savoir plus, voir [Pour ajouter d’autres ensembles d’autorisations](#to-add-other-permission-sets).

> [!IMPORTANT]
> Soyez prudent lorsque vous attribuez **Insérer l’autorisation** ou **Modifier l’autorisation** dans la table **9001 Membre du groupe d’utilisateurs** ou **9003 Ensemble d’autorisations de groupe d’utilisateurs**. Tous les utilisateurs affectés à l’ensemble d’autorisations pourraient potentiellement s’attribuer eux-mêmes à d’autres groupes d’utilisateurs, qui à leur tour, pourraient leur donner involontairement des autorisations.

### Exemple- Autorisation indirecte

L’autorisation indirecte vous permet d’utiliser un objet uniquement au travers d’un autre objet. Par exemple, un utilisateur peut être autorisé à exécuter le codeunit 80 (Ventes-Valider). Le codeunit Ventes-Valider effectue de nombreuses tâches, parmi lesquelles modifier la table 37 (Ligne vente). Lorsque l’utilisateur valide un document vente, le codeunit Ventes-Valider, [!INCLUDE[prod_short](includes/prod_short.md)] vérifie si l’utilisateur est autorisé à modifier la table Ligne vente. S’il n’est pas autorisé, le codeunit ne peut pas effectuer ses tâches et l’utilisateur reçoit un message d’erreur. S’il est autorisé à le faire, le codeunit s’exécute.

L’utilisateur n’a toutefois pas besoin d’avoir un accès total au tableau Ligne vente pour exécuter le codeunit. Si une autorisation indirecte a été accordée à l’utilisateur pour la table Ligne vente, alors le codeunit Ventes-Valider s’exécute. Lorsqu’une autorisation indirecte est accordée à un utilisateur, celui-ci peut uniquement modifier la table Ligne vente en exécutant le codeunit Ventes-Valider ou un autre objet autorisé à modifier la table Ligne vente. L’utilisateur peut uniquement modifier la table Ligne vente lorsqu’il procède à partir des modules pris en charge. L’utilisateur ne peut pas exécuter cette fonctionnalité par inadvertance ou par malveillance en suivant d’autres méthodes.

### Pour ajouter d’autres ensembles d’autorisations

Développez un ensemble d’autorisations en y ajoutant d’autres ensembles d’autorisations. Ensuite, vous pouvez inclure ou exclure des autorisations spécifiques, ou des ensembles d’autorisations entiers, dans chaque ensemble que vous ajoutez. Cela inclut les autorisations dans les ensembles d’autorisations Extension et Type de système, qui ne sont pas autorisées autrement. Les exclusions s’appliquent uniquement à l’ensemble d’autorisations que vous développez. L’ensemble d’origine n’est pas concerné.

Sur la page **Ensemble d’autorisations**, ajoutez un ensemble d’autorisations sur le volet **Ensembles d’autorisations**. Le volet **Résultat** répertorie tous les ensembles d’autorisations ajoutés. Pour explorer les autorisations incluses dans un ensemble que vous avez ajouté, choisissez l’ensemble dans le volet Résultat et le récapitulatif **Autorisations incluses** affichera les autorisations.

Sur le volet **Résultat**, utilisez le champ **Statut d’inclusion** pour identifier les ensembles d’autorisations dans lesquels vous avez exclu des autorisations ou des ensembles d’autorisations. Si quelque chose a été exclu, le statut est défini sur **Partiel**.

Pour une vue globale des autorisations dans l’ensemble d’autorisations, choisissez l’option **Afficher toutes les autorisations**. La page **Autorisations étendues** affiche toutes les autorisations déjà attribuées à l’ensemble d’autorisations et les autorisations dans les ensembles d’autorisations ajoutés.

Pour exclure toutes les autorisations que vous avez ajoutées depuis un ensemble d’autorisations, sur le volet **Résultat**, sélectionnez la ligne, choisissez **Afficher plus d’options**, puis choisissez **Exclure**. Lorsque vous excluez un ensemble d’autorisations, une ligne est créée sur le volet **Ensembles d’autorisations** de type Exclu. Si vous avez exclu un ensemble d’autorisations, mais souhaitez l’inclure à nouveau, supprimez la ligne sur le volet **Ensembles d’autorisations**.

Pour exclure totalement ou partiellement une autorisation spécifique dans un ensemble que vous avez ajouté, sous **Autorisations**, créez une ligne pour l’objet. Les champs de niveau d’accès, Permission d’insertion, Permission de modification, etc. contiendront tous **Exclure**. Pour autoriser un certain niveau d’accès, choisissez l’option appropriée.

L’exclusion d’un ensemble d’autorisations exclut toutes les autorisations de l’ensemble. [!INCLUDE [prod_short](includes/prod_short.md)] calcule les autorisations comme suit :

1. Calculer la liste complète des autorisations incluses
2. Calculer la liste complète des autorisations exclues
3. Supprimer les autorisations exclues de la liste des autorisations incluses (la suppression d’une autorisation indirecte est identique à Réduire à indirecte)

## Pour copier un ensemble d’autorisations

Créez un nouvel ensemble d’autorisations en en copiant un autre. Le nouvel ensemble comprendra toutes les autorisations et tous les ensembles d’autorisations de l’ensemble que vous avez copié. La manière dont les autorisations et les ensembles d’autorisations sont organisés dans le nouvel ensemble d’autorisations diffère selon votre choix dans le champ **Copier l’opération**. Le tableau suivant décrit les options.

|Option  |Désignation  |
|---------|---------|
|**Copier par référence**     | Le jeu d’autorisations d’origine et tous les jeux d’autorisations qui lui ont été ajoutés sont répertoriés sur le volet **Résultats**.       |
|**Copie d’autorisation plate**  | Toutes les autorisations de tous les ensembles d’autorisations sont incluses dans une liste plate sur le **Volet des autorisations**. Les autorisations ne sont pas organisées par ensemble d’autorisations.        |
|**Cloner**     | Créez une copie exacte de l’ensemble d’autorisations d’origine.        |

1. Sur la page **Ensembles d’autorisations**, sélectionnez la ligne d’un ensemble d’autorisations à copier, puis sélectionnez l’action **Copier ensemble d’autorisations**.
2. Sur la page **Copier ensemble d’autorisations**, spécifiez le nom du nouvel ensemble d’autorisations.
3. Dans le champ **Copier l’opération**, indiquez comment organiser les autorisations dans le nouveau jeu d’autorisations.
4. Facultatif : si vous ajoutez un ensemble d’autorisations système, vous souhaiterez peut-être être averti si le nom ou le contenu de l’ensemble d’autorisations d’origine change dans une future version. Cela vous permet de déterminer si vous souhaitez mettre à jour votre ensemble d’autorisations défini par l’utilisateur. Pour recevoir une notification, activez le bouton à bascule **Notifier en cas de modification de l’ensemble d’autorisations**.

> [!NOTE]
> La notification exige que la notification **L’ensemble d’autorisations système d’origine a été modifié** est activée sur la page **Mes notifications**.

## Pour créer ou modifier des autorisations en enregistrant vos actions

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Ensembles d’autorisations**, puis choisissez le lien associé.

    Sinon, sur la page **Utilisateurs**, sélectionnez l’option **Ensembles d’autorisations**.
2. Sur la page **Ensembles d’autorisations**, cliquez sur l’option **Nouveau**.
3. Sur une nouvelle ligne, renseignez les champs selon vos besoins.
4. Sélectionnez l’option **Autorisations**.
5. Sur la page **Autorisations**, choisissez l’action **Enregistrer autorisations**, puis sélectionnez l’action **Démarrer**.  
    L’enregistrement doit être effectué soit en utilisant la fonction **Ouvrir cette page dans une nouvelle fenêtre** (contextuelle) pour avoir la fenêtre d’enregistrement **Autorisations** côte à côte, ou en travaillant dans le même onglet.  
    Un processus d’enregistrement démarre et capture désormais toutes vos actions dans l’interface utilisateur.
6. Accédez aux différentes pages et activités dans [!INCLUDE[prod_short](includes/prod_short.md)] auxquelles vous voulez que les utilisateurs avec cet ensemble d’autorisations puissent accéder. Vous devez exécuter les tâches pour lesquelles vous souhaitez enregistrer des autorisations.
7. Lorsque vous souhaitez terminer l’enregistrement, revenez sur la page **Autorisations** et choisissez l’option **Arrêter**.
8. Cliquez sur le bouton **Oui** pour ajouter les autorisations enregistrées au nouvel ensemble d’autorisations.
9. Pour chaque objet de la liste enregistrée, indiquez si les utilisateurs peuvent insérer, modifier ou supprimer des enregistrements dans les tables enregistrées.

### Pour exporter et importer un ensemble d’autorisations

Pour configurer rapidement des autorisations, vous pouvez importer les ensembles d’autorisations que vous avez exportés à partir d’un autre abonné [!INCLUDE[prod_short](includes/prod_short.md)].

Dans les environnements à plusieurs abonnés, un ensemble d’autorisations est importé dans un abonné spécifique. Autrement dit, la portée de l’importation est *Abonné*.

1. Dans le locataire 1, sur la page **Ensembles d’autorisations**, sélectionnez la ligne ou les lignes des ensembles d’autorisations à exporter, puis choisissez l’action **Exporter des ensembles d’autorisations**.

    Un fichier XML est créé dans le dossier de téléchargement de votre machine. Par défaut, son nom est *Exporter ensembles autorisations.xml*.

2. Dans le locataire 2, dans la page **Ensembles d’autorisations**, sélectionnez l’action **Importer des ensembles d’autorisations**.
3. Dans la boîte de dialogue **Importer des ensembles d’autorisations**, pensez à fusionner les ensembles d’autorisations existants avec les nouveaux ensembles d’autorisations dans le fichier XML.

    Si vous cochez la case **Mettre à jour les autorisations existantes**, les ensembles d’autorisations existants qui ont le même nom dans le fichier XML sont fusionnés avec les ensembles d’autorisations importés.

    Si vous ne cochez pas la case **Mettre à jour les autorisations existantes**, les ensembles d’autorisations qui ont le même nom dans le fichier XML sont ignorés lors de l’importation. Dans ce cas, vous êtes informé que des ensembles d’autorisations sont ignorés.

4. Dans la boîte de dialogue **Importer**, recherchez et sélectionnez le fichier XML à importer, puis choisissez l’action **Ouvrir**.

Les ensembles d’autorisations sont importés.

## Pour supprimer des autorisations obsolètes de tous les ensembles d’autorisations

Dans la page **Ensemble d’autorisations**, choisissez l’option **Supprimer les autorisations obsolètes**.

## Pour configurer des contraintes de temps pour les utilisateurs

Les administrateurs peuvent définir des périodes pendant lesquelles certains utilisateurs peuvent publier. Les administrateurs peuvent également spécifier si le système enregistre la durée de connexion des utilisateurs. De même, les administrateurs peuvent affecter des centres de gestion aux utilisateurs. Pour plus d’informations, voir [Utiliser les centres de gestion](inventory-responsibility-centers.md).

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres utilisateur**, puis choisissez le lien associé.
2. Sur la page **Paramètres utilisateur**, sélectionnez l’action **Nouveau**.
3. Dans le champ **ID utilisateur**, entrez l’ID d’un utilisateur, ou cliquez sur le champ pour visualiser tous les utilisateurs Windows actuels dans le système.
4. Renseignez les champs selon vos besoins.

## Pour gérer les autorisations via des groupes d’utilisateurs

Les groupes d’utilisateurs vous aident à gérer les ensembles d’autorisations dans toute l’entreprise. [!INCLUDE [prod_short](includes/prod_short.md)] en ligne inclut des groupes d’utilisateurs par défaut qui sont attribués automatiquement aux utilisateurs en fonction de leur licence. Vous pouvez ajouter manuellement des utilisateurs à un groupe d’utilisateurs et vous pouvez créer de nouveaux groupes d’utilisateurs en tant que copies de groupes existants.  

Commencez par créer un groupe d’utilisateurs. Ensuite, vous affectez des ensembles d’autorisations au groupe afin de définir l’objet auquel les utilisateurs du groupe peuvent accéder. Lorsque vous ajoutez un utilisateur au groupe, les ensembles d’autorisations définis pour le groupe s’appliquent à l’utilisateur.

Les ensembles d’autorisations attribués à un utilisateur via un groupe d’utilisateurs restent synchronisés. Une modification des autorisations du groupe d’utilisateurs est automatiquement propagée aux utilisateurs. Si vous supprimez un utilisateur d’un groupe d’utilisateurs, les autorisations concernées sont automatiquement révoquées.

### Pour ajouter des utilisateurs à un groupe d’utilisateurs

La procédure suivante explique comment créer manuellement des groupes d’utilisateurs. Pour créer automatiquement des groupes d’utilisateurs, voir [Pour copier un groupe d’utilisateurs et tous ses ensembles d’autorisations](#to-copy-a-user-group-and-all-its-permission-sets).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Groupes utilisateur**, puis choisissez le lien associé.

    1. Sinon, sur la page **Utilisateurs**, sélectionnez l’option **Groupes d’utilisateurs**.
2. Sur la page **Groupe d’utilisateurs**, sélectionnez l’action **Membres du groupe d’utilisateurs**.
3. Sur la page **Groupe d’utilisateurs**, choisissez l’action **Ajouter des utilisateurs**.

### Pour copier un groupe d’utilisateurs et tous ses ensembles d’autorisations

Pour définir rapidement un nouveau groupe d’utilisateurs, vous pouvez copier tous les ensembles d’autorisations d’un groupe d’utilisateurs existant vers un nouveau groupe d’utilisateurs.

> [!NOTE]
> Les membres du groupe d’utilisateurs ne sont pas copiés vers le nouveau groupe d’utilisateurs. Vous devez les ajouter manuellement ensuite. Pour plus d’informations, voir la section [Pour ajouter des utilisateurs à un groupe d’utilisateurs](#to-add-users-to-a-user-group).

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Groupes utilisateur**, puis choisissez le lien associé.
2. Sélectionnez le groupe d’utilisateurs à partir duquel vous souhaitez copier, puis choisissez l’action **Copier groupe d’utilisateurs**.
3. Dans le champ **Nouveau code du groupe d’utilisateurs**, spécifiez le nom du nouveau groupe, puis cliquez sur le bouton **OK**.

Le nouveau groupe d’utilisateurs est ajouté à la page **Groupes d’utilisateurs**. Ajoutez ensuite des utilisateurs. Pour plus d’informations, voir la section [Pour ajouter des utilisateurs à un groupe d’utilisateurs](#to-add-users-to-a-user-group).  

> [!IMPORTANT]
> Vous obtiendrez une erreur de validation si vous essayez d’attribuer un groupe d’utilisateurs à l’utilisateur qui fait référence à un ensemble d’autorisations défini dans une extension désinstallée. C’est parce que l’ID d’application de l’extension est validé chaque fois qu’il est référencé. Pour affecter ce groupe d’utilisateurs à un utilisateur, vous pouvez soit réinstaller l’extension, soit supprimer la référence de l’extension désinstallée de l’ensemble d’autorisations, soit supprimer cet ensemble d’autorisations du groupe d’utilisateurs.

### Pour affecter des ensembles d’autorisations à des groupes d’utilisateurs

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Groupes utilisateur**, puis choisissez le lien associé.
2. Sélectionnez le groupe d’utilisateurs auquel affecter des autorisations.  

    Tous les ensembles d’autorisations qui sont affectés à l’utilisateur sont affichés dans le récapitulatif **Ensemble d’autorisations utilisateur**.
3. Choisissez l’action **Ensemble d’autorisations utilisateur** pour ouvrir la page **Ensembles d’autorisations utilisateur**.
4. Sur la page **Ensembles d’autorisations utilisateur**, renseignez les champs, le cas échéant, sur une nouvelle ligne.

### Pour affecter un ensemble d’autorisations sur la page **Ensemble d’autorisations par groupe d’utilisateurs**

La procédure suivante explique comment affecter des ensembles d’autorisations à un groupe d’utilisateurs sur la page **Ensemble d’autorisations par groupe d’utilisateurs**.

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Utilisateurs**, puis choisissez le lien associé.
2. Sur la page **Utilisateurs**, sélectionnez l’utilisateur approprié, puis cliquez sur l’action **Ensemble d’autorisations par groupe d’utilisateurs**.
3. Dans la page **Ensemble d’autorisations par groupe d’utilisateurs**, sélectionnez le champ **[nom du groupe d’utilisateurs]** sur une ligne pour l’ensemble d’autorisations approprié pour affecter l’ensemble au groupe d’utilisateurs.
4. Activez la case à cocher **Tous les groupes d’utilisateurs** pour affecter l’ensemble d’autorisations à tous les groupes d’utilisateurs.

Vous pouvez aussi affecter des ensembles d’autorisations directement à un utilisateur.

## Pour affecter des ensembles d’autorisations à des utilisateurs

Un ensemble d’autorisations est une collection d’autorisations pour des objets de base de données spécifiques. Tous les utilisateurs doivent être affectés à une ou plusieurs séries d’autorisations avant de pouvoir accéder à [!INCLUDE[prod_short](includes/prod_short.md)].  

Une solution [!INCLUDE[prod_short](includes/prod_short.md)] contient des ensembles d’autorisations prédéfinis qui sont ajoutés par Microsoft ou par votre fournisseur de solutions. Vous pouvez également ajouter de nouveaux ensembles d’autorisations personnalisés pour répondre aux besoins de votre organisation. Pour plus d’informations, voir la section [Pour créer un ensemble d’autorisations](#to-create-a-permission-set).

> [!NOTE]
> Si vous ne souhaitez pas limiter l’accès d’un utilisateur plus que ce qui est déjà défini par la licence, vous pouvez attribuer à l’utilisateur un ensemble d’autorisations spéciales appelé SUPER. Cet ensemble d’autorisations garantit que l’utilisateur peut accéder à tous les objets spécifiés dans la licence.
>
> Un utilisateur disposant de la licence Essential et de l’ensemble d’autorisations SUPER a accès à davantage de fonctionnalités que les utilisateurs possédant la licence de membre d’équipe et l’ensemble d’autorisations SUPER.

Vous pouvez affecter des ensembles d’autorisations aux utilisateurs de deux manières :

- à partir de la page **Fiche utilisateur** en sélectionnant les ensembles d’autorisations à attribuer à l’utilisateur ;
- à partir de la page **Ensemble d’autorisations par utilisateur** en sélectionnant les utilisateurs auxquels un ensemble d’autorisations est attribué.

### Pour affecter un ensemble d’autorisations sur une fiche utilisateur

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Utilisateurs**, puis choisissez le lien associé.
2. Sélectionnez l’utilisateur auquel affecter des autorisations.
Tous les ensembles d’autorisations qui sont affectés à l’utilisateur sont affichés dans le récapitulatif **Ensemble d’autorisations utilisateur**.
3. Sélectionnez l’option **Modifier** pour ouvrir la page **Fiche utilisateur**.
4. Sur le raccourci **Ensembles d’autorisations utilisateur**, renseignez les champs, le cas échéant sur une nouvelle ligne. Pour plus d’informations, voir [Pour créer ou modifier des ensembles d’autorisations](ui-define-granular-permissions.md#to-create-a-permission-set).

   Utilisez le champ **Entreprise** pour appliquer l’ensemble d’autorisations définie à une entreprise spécifique. Si vous laissez le champ vide, cela s’applique à toutes les entreprises.

## Pour affecter un ensemble d’autorisations sur la page Ensemble d’autorisations par utilisateur

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Utilisateurs**, puis choisissez le lien associé.
2. Sur la page **Utilisateurs**, sélectionnez l’action **Ensemble d’autorisations par utilisateur**.
3. Sur la page **Ensemble d’autorisations par utilisateur**, activez la case à cocher **[nom d’utilisateur]** sur une ligne pour l’ensemble d’autorisations approprié pour affecter l’ensemble à l’utilisateur.

    Activez la case à cocher **Tous les utilisateurs** pour affecter l’ensemble d’autorisations à tous les utilisateurs.

## Pour afficher l’aperçu des autorisations d’un utilisateur

Vous ne pouvez afficher les autorisations effectives des autres utilisateurs que si les autorisations SUPER ou SECURITY vous sont attribuées. 

La page **Autorisations effectives** offre des informations supplémentaires sur la source de chaque autorisation. Par exemple, si la source est un groupe de sécurité ou si une autorisation est héritée. La page contient également une colonne où les administrateurs peuvent examiner les filtres de sécurité appliqués. Pour en savoir plus sur les filtres de sécurité, consultez [Les filtres de sécurité limitent l’accès d’un utilisateur à des enregistrements spécifiques dans une table](#security-filters-limit-a-users-access-to-specific-records-in-a-table).

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Utilisateurs**, puis choisissez le lien associé.
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
    > Pour une explication sur le classement, voir [Pour créer un ensemble d’autorisations](ui-define-granular-permissions.md#to-create-a-permission-set).  

4. Pour modifier un ensemble d’autorisations, dans la section **Par ensemble d’autorisations**, sur la ligne d’un ensemble d’autorisations approprié de type **Défini par l’utilisateur**, choisissez l’un des cinq champs de type d’accès et sélectionnez une valeur différente.

5. Pour modifier des autorisations individuelles dans l’ensemble d’autorisations, choisissez la valeur dans le champ **Ensemble d’autorisations** pour ouvrir la page **Autorisations**.

> [!NOTE]  
> Lorsque vous modifiez un ensemble d’autorisations, les modifications s’appliquent également à d’autres utilisateurs auxquels l’ensemble d’autorisations est affecté.

### Filtres de sécurité : pour limiter l’accès d’un utilisateur à des enregistrements spécifiques dans une table

Pour la sécurité au niveau des enregistrements dans [!INCLUDE[prod_short](includes/prod_short.md)], vous utilisez des filtres de sécurité pour limiter l’accès d’un l’utilisateur aux données dans une table. Vous créez des filtres de sécurité sur les données de la table. Un filtre de sécurité décrit un ensemble d’enregistrements dans une table auxquels un utilisateur a l’autorisation d’accéder. Vous pouvez indiquer, par exemple, qu’un utilisateur peut uniquement lire les enregistrements qui contiennent des informations relatives à un client particulier. Ainsi, l’utilisateur ne peut pas accéder aux enregistrements qui contiennent des informations sur d’autres clients. Pour plus d’informations, voir [Utilisation des filtres de sécurité](/dynamics365/business-central/dev-itpro/security/security-filters) dans le contenu d’administration.

## Affichage de la télémétrie des modifications d’autorisation

Vous pouvez configurer [!INCLUDE[prod_short](includes/prod_short.md)] pour envoyer les modifications apportées à l’autorisation à une ressource Application Insights dans Microsoft Azure. Ensuite, à l’aide d’Azure Monitor, vous créez des états et configurez des alertes sur les données collectées. Pour plus d’informations, voir les articles suivants dans l’aide pour les développeurs et les administrateurs [!INCLUDE[prod_short](includes/prod_short.md)] :

- [Surveillance et analyse de la télémétrie - Activation d’Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analyse de la télémétrie de surveillance des champs](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## Utilisateurs administrateurs délégués

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

## Voir aussi

[Créer des utilisateurs en fonction des licences](ui-how-users-permissions.md)  
[Gérer les profils](admin-users-profiles-roles.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Ajouter des utilisateurs à Microsoft 365 pour les entreprises](/microsoft-365/admin/add-users/add-users)  
[Sécurité et protection dans Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) dans l’aide sur Developer and IT-Pro  
[Affecter un ID télémétrie aux utilisateurs](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
