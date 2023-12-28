---
title: Nettoyer les données avec des stratégies de rétention
description: Vous pouvez spécifier la fréquence à laquelle vous souhaitez supprimer certains types de données.
author: brentholtorf
ms.topic: conceptual
ms.author: bholtorf
ms.search.keywords: 'delete, data, retention, policy, policies'
ms.search.form: '3903, 3901'
ms.date: 12/15/2023
ms.custom: bap-template
---
# <a name="define-retention-policies"></a>Définir des stratégies de rétention

Cet article décrit comment les administrateurs peuvent définir des stratégies de rétention pour spécifier à quelle fréquence ils souhaitent supprimer les données obsolètes dans les tables contenant des entrées de journal et des enregistrements archivés. Par exemple, le nettoyage des entrées de journal peut faciliter l’utilisation des données plus pertinentes. Les stratégies peuvent supprimer des données en fonction d’une date d’expiration ou vous pouvez ajouter des filtres pour inclure uniquement certaines données expirées.

## <a name="required-setups-and-permissions"></a>Paramètres et autorisations obligatoires

Avant de pouvoir créer des stratégies de rétention, vous devez configurer les tables à inclure et les périodes de conservation des données.

|Configuration  |Désignation  |
|---------|---------|
|**Tables autorisées**     |Nous fournissons une liste des tables à inclure dans les stratégies de rétention. Si vous souhaitez ajouter des tables d’une extension à une stratégie de rétention, un développeur doit ajouter leurs tables à la liste. Pour en savoir plus, voir [Inclure votre extension dans une stratégie de rétention](admin-data-retention-policies.md#include-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Périodes de rétention**     |Spécifiez les périodes pendant lesquelles les données doivent être conservées dans les tables dans une stratégie. Les périodes déterminent la fréquence à laquelle les données sont supprimées.         |

En outre, vous devez disposer des autorisations d’utilisateur **AVANCÉ** ou de l’ensemble d’autorisations de **configuration de la stratégie de rétention**. Les utilisateurs disposant de l’ensemble d’autorisations Configuration de la stratégie de rétention peuvent définir des stratégies de rétention pour les tables. C’est vrai, même s’ils ne disposent pas des autorisations de lecture et de suppression pour les tables. L’entrée de la file d’attente des tâches doit s’exécuter en tant qu’utilisateur disposant des autorisations nécessaires pour lire et supprimer les données. Ne pas accorder l’ensemble d’autorisations de configuration de la stratégie de rétention aux utilisateurs qui ne devraient pas être autorisés à supprimer des données.

> [!NOTE]
> Si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] en local, et que vous souhaitez essayer les stratégies de rétention dans la base de données de démonstration Cronus, vous devez effectuer certaines opérations. La société de démonstration ne contient pas de tables que vous pouvez utiliser avec des stratégies de rétention, vous devez donc les ajouter. Pour ce faire, créez une société vierge dans la base de données de démonstration. Dans la nouvelle société, importez le package de configuration RapidStart pour votre pays/région qui correspond au package standard NAV17.0.W1.ENU.STANDARD.rapidstart. Les données de configuration des stratégies de rétention seront disponibles dans la nouvelle société.

### <a name="create-retention-periods"></a>Créer des périodes de rétention

Les périodes de rétention peuvent être aussi longues ou aussi courtes que vous le souhaitez. Pour créer des périodes de rétention, sur la page **Stratégies de rétention**, utilisez l’action **Durée de rétention**. Les périodes que vous définissez sont disponibles pour toutes les stratégies.

> [!NOTE]
> Pour des raisons de conformité, nous avons défini une période de rétention minimale pour certaines tables. Si vous définissez une période de rétention plus courte que le minimum requis, un message affiche la période obligatoire.

### <a name="set-up-a-retention-policy"></a>Configurer une stratégie de rétention

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Stratégies de rétention**, puis choisissez le lien associé.
2. Dans le champ **ID table**, sélectionnez la table que vous souhaitez inclure dans la stratégie.
3. Dans le champ **Durée de rétention**, spécifiez la durée pendant laquelle conserver les données dans la table.
4. Facultatif : Pour appliquer la stratégie à des données spécifiques dans une table, désactivez le bouton **Appliquer à tous les enregistrements**. Le raccourci **Stratégie de rétention des enregistrements** s’affiche, dans lequel vous pouvez définir des filtres pour créer des sous-jeux de données pour chaque ligne. Pour en savoir plus, consultez [Filtrage](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Chaque ligne a sa propre période de rétention. Si vous spécifiez des périodes de rétention différentes pour les mêmes données, la période la plus longue est utilisée. En outre, certaines tables contiennent des filtres que vous ne pouvez ni modifier ni supprimer. Pour vous aider à identifier ces filtres, ils apparaissent dans une police de couleur plus claire.

#### <a name="video-guidance"></a>Guidage vidéo

Cette vidéo fournit un exemple de la façon de mettre en place une politique de rétention.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fLeJ]

## <a name="apply-retention-policies"></a>Appliquer des stratégies de rétention

Vous pouvez utiliser une entrée de file d’attente de tâches pour appliquer des stratégies de rétention afin de supprimer automatiquement les données, ou vous pouvez appliquer manuellement des stratégies.

Pour appliquer automatiquement une stratégie de rétention, créez et activez simplement une stratégie. Lorsque vous activez une stratégie, [!INCLUDE [prod_short](includes/prod_short.md)] crée une entrée de file d’attente de tâches qui applique les stratégies de rétention en fonction de la période de rétention. Toutes les stratégies de rétention utiliseront la même entrée de file d’attente de tâches. Par défaut, l’entrée de la file d’attente des tâches applique la stratégie tous les jours à 02 h 00. Vous pouvez modifier la valeur par défaut, mais si vous le faites, nous vous recommandons de l’exécuter en dehors des heures d’ouverture. Pour en savoir plus, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md). 

Vous pouvez appliquer manuellement une stratégie en utilisant l’action **Appliquer manuellement** sur la page **Stratégies de rétention**. Si vous souhaitez toujours appliquer une stratégie manuellement, activez le bouton de basculement **Manuel**. L’entrée de la file d’attente des tâches ne tiendra pas compte de la stratégie lors de son exécution.

## <a name="view-retention-policy-log-entries"></a>Afficher des entrées du journal des stratégies de rétention

Vous pouvez afficher l’activité liée aux stratégies de rétention dans la page **Journal des stratégies de rétention**. Par exemple, des entrées sont créées lorsqu’une stratégie est appliquée ou si des erreurs se sont produites.

## <a name="include-your-extension-in-a-retention-policy-requires-help-from-a-developer"></a>Incluez votre extension dans une stratégie de rétention (nécessite l’aide d’un développeur)

Par défaut, les stratégies de rétention couvrent uniquement [!INCLUDE[prod_short](includes/prod_short.md)] la liste que nous fournissons. Vous pouvez supprimer les tables par défaut de la liste et ajouter des tables qui vous appartiennent. Autrement dit, vous ne pouvez pas ajouter une table que vous n’avez pas créée vous-même. Par exemple, vous ne pouvez pas ajouter d’autres tables à partir de [!INCLUDE[prod_short](includes/prod_short.md)] ou à partir d’une extension que vous avez achetée.

Pour ajouter vos tables à la liste des tables autorisées, un développeur doit ajouter du code. Par exemple, codeunit du programme d’installation pour l’extension (un codeunit avec le sous-type *install* ).

Lorsqu’un développeur ajoute une table, il peut spécifier des filtres obligatoires et par défaut. Les filtres obligatoires ne peuvent pas être supprimés ou modifiés ultérieurement lorsque vous ajoutez des tables pour définir une stratégie de rétention. Les filtres par défaut ne sont que des suggestions.

Voici des exemples de la façon d’ajouter une table à la liste des tables autorisées avec et sans filtres obligatoires ou par défaut. Pour un exemple plus complexe, voir codeunit 3999 « Reten. Pol. Install – BaseApp ».

```al
 trigger OnInstallAppPerCompany()
    var
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
    begin
        RetenPolAllowedTables.AddAllowedTable(Database::"Retention Policy Log Entry");
    end;
```

L’exemple suivant inclut un filtre obligatoire.

```al
 trigger OnInstallAppPerCompany()
    var
        ChangeLogEntry: Record "Change Log Entry";
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
        RetentionPeriod: Enum "Retention Period Enum";
        RecRef: RecordRef;
        TableFilters: JsonArray;
        Enabled: Boolean;
        Mandatory: Boolean;
    begin
        ChangeLogEntry.Reset();
        ChangeLogEntry.SetFilter("Field Log Entry Feature", '%1|%2', ChangeLogEntry."Field Log Entry Feature"::"Monitor Sensitive Fields", ChangeLogEntry."Field Log Entry Feature"::All);
        RecRef.GetTable(ChangeLogEntry);
        Enabled := true;
        Mandatory := true;
        RetenPolAllowedTables.AddTableFilterToJsonArray(TableFilters, RetentionPeriod::"28 Days", ChangeLogEntry.FieldNo(SystemCreatedAt), Enabled, Mandatory, RecRef);
        RetenPolAllowedTables.AddAllowedTable(Database::"Change Log Entry", ChangeLogEntry.FieldNo(SystemCreatedAt), TableFilters);
    end;
```

Une fois qu’un développeur a ajouté des tables à la liste, un administrateur peut les inclure dans une stratégie de rétention. 

## <a name="see-also"></a>Voir aussi

[Analyse de la télémétrie de suivi des stratégies de rétention](/dynamics365/business-central/dev-itpro/administration/telemetry-retention-policy-trace)  
[Audit des modifications dans Business Central](across-log-changes.md)  
[Filtrage](ui-enter-criteria-filters.md#filtering)  
[Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
