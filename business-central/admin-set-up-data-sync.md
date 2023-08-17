---
title: Configurer des sociétés pour synchroniser les données de base
description: Découvrez comment configurer une ou plusieurs sociétés pour synchroniser les données de base.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---

# <a name="get-ready-to-synchronize-master-data"></a>Préparation à la synchronisation des données principales

Lorsqu’au moins deux sociétés utilisent certaines des mêmes données principales, vous pouvez synchroniser les données plutôt que de les ajouter manuellement dans chaque société. Par exemple, la synchronisation des données est particulièrement utile lorsque vous créez des filiales.

Les données de base incluent les paramètres et les informations non transactionnelles sur les entités commerciales. Par exemple, les clients, les fournisseurs, les articles et les employés. Les données fournissent un contexte pour les transactions commerciales. Voici quelques exemples de données de base pour un client :

* Name
* Numéro d’identification
* Adresse
* Conditions de paiement
* Limite de crédit

Vous configurez la synchronisation dans les succursales. À l’aide d’un modèle d’extraction, les filiales extraient les données de l’entreprise source dont elles ont besoin pour faire affaire avec elles. Après avoir configuré la synchronisation et synchronisé les données pour la première fois, vous êtes prêt. Les entrées de la file d’attente mettent à jour les enregistremetns couplés dans les filiales lorsque quelqu’un apporte des modifications à la société source.

## <a name="uni-directional-synchronization-only"></a>Synchronisation unidirectionnelle uniquement

Vous pouvez synchroniser uniquement les données de la société source vers les filiales en mode pull. Les filiales ne peuvent pas envoyer de données à l’entreprise source.

> [!NOTE]
> Bien que cela soit possible, nous vous déconseillons de configurer la synchronisation bidirectionnelle. C’est-à-dire la synchronisation des données de la société source vers les filiales, et des filiales vers la société source. La synchronisation des données dans les deux sens peut entraîner des conflits ou des remplacements indésirables.

## <a name="before-you-start"></a>Avant de commencer

Ce sont les conditions requises pour configurer la synchronisation.

* Toutes les entreprises doivent être dans le même environnement.
* L’utilisateur qui configure la filiale doit disposer de la licence de type **Essential**, **Premium** ou **Basic ISV**.

> [!NOTE]
> La licence Team Member et la licence Administrateur interne vous permettent d’accéder, mais pas de modifier les enregistrements, elles ne peuvent donc pas être utilisées pour configurer la synchronisation. La licence d’administrateur délégué ne vous permet pas de planifier des tâches en arrière-plan, vous ne pourrez donc pas terminer la configuration.

## <a name="specify-the-source-company"></a>Spécifier la société source

Les premières étapes consistent à spécifier la société qui sera la source de données et à activer la synchronisation. Les filiales extraient les données de la société source.

> [!NOTE]
> Lorsque vous activez la synchronisation, [!INCLUDE [prod_short](includes/prod_short.md)] crée et planifie les entrées de la file d’attente des travaux qui synchronisent les données. Il peut sembler que les entrées synchronisent immédiatement les données, mais ce n’est pas le cas. Les entrées de la file d’attente des travaux créées ne synchronisent que les enregistrements couplés, et à ce stade, vous ne l’avez pas encore configuré. La synchronisation commence après [Activer ou désactiver des tables et des champs](#enable-or-disable-tables-and-fields) et [Synchroniser pour la première fois](#synchronize-for-the-first-time).

1. Dans une filiale, sélectionnez l’icône ![Ampoule qui ouvre la fonction Fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres Gestion des données principales**, puis choisissez le lien associé.
1. Dans le champ **Société source**, spécifiez la société à partir de laquelle vous allez extraire les modifications.
1. Activez le bouton bascule **Activer la synchronisation**.
1. Dans la boîte de dialogue de confirmation, sélectionnez **OK**. [!INCLUDE [prod_short](includes/prod_short.md)] trouve les tables et les champs disponibles depuis la société source.

L’étape suivante consiste à activer les tables et les champs pour la synchronisation.

## <a name="enable-or-disable-tables-and-fields"></a>Activer ou désactiver des tables et des champs

Pour gagner du temps, [!INCLUDE [prod_short](includes/prod_short.md)] fournit une liste de tableaux que les entreprises synchronisent souvent. Par défaut, ces tables sont activées pour la synchronisation. Vous pouvez les modifier, les désactiver ou les supprimer comme bon vous semble. Pour gagner du temps supplémentaire, certains champs des tables sont déjà désactivés, car ils ne sont probablement pas pertinents pour la filiale.

> [!NOTE]
> Si une ou plusieurs extensions sont installées dans la société source, lorsqu’une filiale configure la synchronisation, la page **Tables de synchronisation** inclut les tables des extensions, et vous pouvez accéder à leurs champs. Cependant, si la société source ajoute une extension après la mise en place de la synchronisation, chaque filiale doit ajouter manuellement les tables. Pour en savoir plus sur l’ajout de tables, accédez à [Ajouter ou supprimer des tables de la liste des tables de synchronisation](#add-or-delete-tables-from-the-synchronization-tables-list). Pour en savoir plus sur les extensions de [!INCLUDE [prod_short](includes/prod_short.md)], accédez à [Développer des extensions dans Visual Studio Code](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview#developing-extensions-in-visual-studio-code).

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Paramètres Gestion des données principales**, puis choisissez le lien associé.
1. Choisissez l’action **Tables de synchronisation**.
1. Renseignez les champs selon vos besoins. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Le champ **Filtre de table** est utile pour contrôler ce qu’il faut synchroniser pour une table. Vous pouvez configurer des filtres pour synchroniser uniquement lorsque certaines conditions sont remplies. Par exemple, vous pouvez ajouter des filtres qui spécifient que vous synchronisez uniquement les fournisseurs d’une certaine région. Ou, les clients qui utilisent une certaine devise.
>
> Si la filiale a déjà des données dans ses tables, un autre bon moyen de définir des critères de synchronisation consiste à mettre en place un couplage basé sur les correspondances. Pour en savoir plus sur la correspondance, accédez à [Utiliser le couplage par correspondance](#use-match-based-coupling).

1. Pour activer les champs pour une table, choisissez la table, puis l’action **Champs**.
1. Renseignez les champs selon vos besoins. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Un moyen rapide d’activer ou de désactiver plusieurs champs en même temps consiste à les sélectionner dans la liste, puis à utiliser les actions **Activer** ou **Désactiver**.

### <a name="use-match-based-coupling"></a>Utiliser le couplage par correspondance

Vous pouvez spécifier les données à synchroniser pour une table en faisant correspondre les enregistrements en fonction de critères. Sur la page **Configuration de la gestion des données principales**, choisissez l’action **Couplage par correspondance** pour ouvrir la page **Sélectionner les critères de couplage**. Vous pouvez définir les critères suivants pour votre correspondance :

* S’il faut synchroniser après avoir couplé des enregistrements.
* S’il faut créer un enregistrement dans la filiale si aucune correspondance non couplée unique ne peut être trouvée en utilisant les critères de correspondance. Pour activer cette fonctionnalité, activez l’action **Créer si impossible de trouver une correspondance**.
* Les champs à utiliser pour faire correspondre les enregistrements et si la correspondance est sensible à la casse.
* Hiérarchisez l’ordre de recherche des enregistrements en spécifiant une priorité de correspondance. [!INCLUDE [prod_short](includes/prod_short.md)] recherchera une correspondance dans l’ordre croissant en fonction de la priorité de correspondance. Une valeur vide est égale à la priorité 0, qui est la priorité la plus élevée. Les champs avec la priorité 0 sont pris en compte en premier.

## <a name="synchronize-for-the-first-time"></a>Synchroniser pour la première fois

Lorsque vous êtes prêt, sur la page **Configuration de la gestion des données de référence**, choisissez l’action **Démarrer la synchronisation initiale**. Sur la page **Synchronisation initiale des données principale**, choisissez le type de synchronisation que vous souhaitez utiliser pour chaque table.

* Si vous avez déjà des enregistrements dans la société source et les filiales, et que vous souhaitez faire correspondre des enregistrements existants, choisissez l’action **Utiliser le couplage par correspondance**. [!INCLUDE [prod_short](includes/prod_short.md)] fait correspondre les enregistrements de la filiale avec les enregistrements de la société source. Les correspondances sont basées sur des critères de correspondance que vous définissez. Pour plusieurs tables par défaut, [!INCLUDE [prod_short](includes/prod_short.md)] a déjà mis en correspondance les enregistrements existants en utilisant leur clé primaire, mais vous pouvez modifier cela si vous le souhaitez. Vous pouvez également laisser la synchronisation créer des enregistrements dans la filiale pour les enregistrements de la société source que la filiale n’a pas. Pour en savoir plus sur la correspondance, accédez à [Utiliser le couplage par correspondance](#use-match-based-coupling).
* Si vous choisissez **Exécuter la synchronisation complète**, la synchronisation crée des enregistrements pour tous les enregistrements de la société source qui ne sont pas encore couplés. Par exemple, cette option est utile dans les scénarios suivants :

    * La filiale n’a pas de données dans la table.
    * Vous souhaitez ajouter des enregistrements de la société source sans correspondance.  

Après avoir choisi l’option à utiliser, choisissez l’action **Démarrer tout** pour lancer la synchronisation.

Pendant que la synchronisation est en cours, la colonne **Statut de la tâche** sur la page **Synchronisation complète initiale des données de référence** affiche le statut de chaque entrée de la file d’attente des tâches. Appuyez sur **F5** sur votre clavier pour mettre à jour le statut.

> [!TIP]
> Les tables se synchronisent dans un ordre prédéfini. Si la synchronisation est bloquée sur une table, sélectionnez la table, puis choisissez l’action **Redémarrer** pour la relancer.

Pour accéder aux détails, tels que le nombre d’enregistrements insérés ou modifiés, choisissez la valeur dans la colonne **Statut de la tâche** pour ouvrir la page **Vue - Tâches de synchronisation d’intégration**. Pour les enregistrements qui ont été insérés, vous pouvez choisir le numéro dans la colonne **Inséré** pour accéder à plus de détails sur les nouveaux enregistrements.

## <a name="add-or-delete-tables-from-the-synchronization-tables-list"></a>Ajouter ou supprimer des tables de la liste des tables de synchronisation

### <a name="add-a-table"></a>Ajouter une table

> [!IMPORTANT]
> Bien que les tables contenant des données transactionnelles soient disponibles dans la liste, telles que les tables contenant des entrées comptables, vous ne devez pas les sélectionner. La synchronisation fonctionne uniquement pour les tables contenant des données non transactionnelles.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Tables de synchronisation**, puis choisissez le lien associé.
1. Sélectionnez **Nouveau**, puis choisissez la table à ajouter.
1. Renseignez les champs selon vos besoins. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

### <a name="delete-a-table"></a>Supprimer une table

> [!NOTE]
> Si vous supprimez un enregistrement dans la société source, il n’est pas également supprimé dans la filiale. Cela permet d’éviter la perte indésirable de données. La filiale peut décider de supprimer la table si elle le souhaite.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  saisissez **Tables de synchronisation**, puis choisissez le lien associé.
1. Cliquez sur l’action **Supprimer**.

## <a name="use-export-and-import-to-share-a-synchronization-setup"></a>Utiliser l’exportation et l’importation pour partager une configuration de synchronisation

Si vous configurez plusieurs filiales qui utilisent les mêmes paramètres de synchronisation ou des paramètres similaires, vous gagnez du temps. Configurez une filiale, puis exportez sa configuration dans un fichier .xml. Le fichier contient l’intégralité de la configuration, y compris les mappages de tables et de champs et les critères de filtrage. Vous pouvez ensuite importer le fichier dans la filiale suivante. Pour importer ou exporter une configuration, sur la page **Configuration de la gestion des données de référence**, utilisez les actions **Importer** ou **Exporter**.

## <a name="see-also"></a>Voir aussi

[Gérer la synchronisation des données principales](admin-sync-master-data.md)
