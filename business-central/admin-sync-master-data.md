---
title: Gérer la synchronisation des données principales
description: Découvrez comment gérer la synchronisation des données principales.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# <a name="manage-master-data-synchronization"></a>Gérer la synchronisation des données principales

Après avoir configuré la synchronisation des données principales et effectué la première synchronisation, les enregistrements des tables sélectionnées sont couplés et une entrée de file d’attente des tâches récurrentes est créée pour chaque table. Les entrées de la file d’attente des tâches synchronisent automatiquement les données dans les filiales lorsqu’un utilisateur apporte une modification dans la société source. Sinon, vous n’avez rien à faire.

> [!NOTE]
> Par défaut, les entrées de la file d’attente des tâches sont planifiées pour s’exécuter toutes les minutes et vous ne pouvez pas modifier la planification.

Cependant, parfois, les choses tournent mal et certaines situations exigent gestion et investigation. Par exemple, si des utilisateurs modifient le même enregistrement à la fois dans la société source et dans une filiale, la synchronisation échoue afin que vous puissiez spécifier la bonne modification. Ou, la société source peut installer une extension qui modifie le schéma de l’une des tables que vous synchronisez en ajoutant un champ ou deux. Si vous souhaitez synchroniser les nouveaux champs dans les filiales, vous devrez installer les mêmes extensions et mettre à jour les schémas des tables dans leur configuration.

Cet article décrit les outils que vous pouvez utiliser pour assurer le bon fonctionnement de la synchronisation.

## <a name="investigate-the-status-of-synchronization"></a>Examiner le statut de la synchronisation

Deux actions sur la page **Tables de synchronisation** peuvent vous aider à surveiller votre synchronisation :

* **Projets de synchronisation d’intégration**
* **Écritures file d’attente des travaux**

La table suivante décrit les actions.

|Page  |Description  |
|---------|---------|
|**Projets de synchronisation d’intégration**     | Ouvrez la page **Tâches de synchronisation de l’intégration** pour rechercher ce qui s’est passé à chaque exécution d’une entrée de file d’attente des tâches. Pour approfondir les détails sur les nouveaux enregistrements qui ont été ajoutés, ou découvrir pourquoi un enregistrement n’a pas pu être synchronisé, choisissez les numéros dans les colonnes **Inséré** ou **Échec**. Vous pouvez également utiliser cette page pour effacer les anciens enregistrements dont vous n’avez peut-être pas besoin. Pour en savoir plus sur le nettoyage, consultez [Nettoyer les anciennes entrées](#clean-up-old-entries).        |
|**Écritures file d’attente des travaux**     | Accédez aux détails de l’entrée de la file d’attente des tâches qui synchronise les données d’une table sélectionnée. Par exemple, utilisez cette page pour gérer le statut de l’entrée de la file d’attente des tâches. Pour en savoir plus sur les entrées de la file d’attente des tâches, accédez à [Utiliser les files d’attente des tâches pour planifier des tâches](admin-job-queues-schedule-tasks.md).     |

> [!NOTE]
> Si vous trouvez une erreur sur la page **Tâches de synchronisation de l’intégration** que vous ne pouvez pas résoudre vous-même, si vous contactez votre partenaire ou Microsoft pour obtenir de l’aide, il est utile de fournir le message d’erreur et les informations sur la pile d’appels.

## <a name="synchronize-modified-records"></a>Synchroniser les enregistrements modifiés

Si vous modifiez un paramètre pour une table ou un champ dans une filiale, vous devez mettre à jour la synchronisation. Par exemple, si vous décidez de cocher la case **Remplacer les changements locaux** sur un champ pour permettre aux données de la société source de remplacer les changements locaux. Pour mettre à jour la synchronisation, utilisez l’action **Synchroniser les enregistrements modifiés** sur la page **Tables de synchronisation**.

## <a name="update-table-schemas"></a>Mettre à jour les schémas de table

Si la société source modifie une table, par exemple en ajoutant un champ que vous souhaitez synchroniser, les filiales doivent mettre à jour leurs mappages de champs. Sur la page **Champs de synchronisation**, utilisez l’action **Mettre à jour les champs**. 

## <a name="enable-or-disable-couplings-between-records"></a>Activer ou désactiver les couplages entre enregistrements

Pour démarrer ou arrêter le couplage sur des enregistrements spécifiques d’une table, sur la page **Champs de synchronisation**, choisissez les champs, puis utilisez les actions **Activer** ou **Désactiver**. 

> [!TIP]
> Un moyen rapide d’activer ou de désactiver plusieurs champs en même temps consiste à les sélectionner dans la liste, puis à utiliser les actions **Activer** ou **Désactiver**.

## <a name="adding-extensions"></a>Ajout d’extensions

Si la société source installe une nouvelle extension, la filiale doit également l’installer si elle souhaite synchroniser les données pour celle-ci. La filiale peut utiliser l’action **Mettre à jour les champs** sur la page **Champs de synchronisation** pour ajouter les tables de l’extension à la liste.

> [!NOTE]
> Certaines tables obtiennent des données de tables liées. Si vous ajoutez une extension qui n’inclut pas les tables liées, les champs de ces tables ne seront pas disponibles. Vérifiez que vous avez ajouté toutes les tables associées.

## <a name="clean-up-old-entries"></a>Nettoyer les anciennes entrées

Au fil du temps, le nombre d’entrées dans le journal de synchronisation deviendra important, vous voudrez peut-être faire un peu de ménage pour supprimer les entrées inutiles. Pour faciliter le nettoyage des anciennes entrées, la page **Tâches de synchronisation de l’intégration** offre les actions suivantes :

* **Supprimer les écritures datant de plus de 7 jours**
* **Supprimer toutes les écritures**

<!--
## <a name="recreate-a-deleted-job-queue-entry"></a>Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## <a name="see-also"></a>Voir aussi

[Se préparer à synchroniser les données principales](admin-set-up-data-sync.md)
