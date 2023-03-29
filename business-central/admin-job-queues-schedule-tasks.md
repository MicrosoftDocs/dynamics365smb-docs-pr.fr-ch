---
title: Planifier des projets à exécuter automatiquement
description: 'Les tâches planifiées sont gérées par la file d’attente des travaux. Ces projets exécutent des états et des codeunits. Vous pouvez définir des projets à exécuter une fois, ou sur une base récurrente.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '672, 673, 674, 671'
ms.date: 10/01/2021
ms.author: edupont
---
# Utiliser des files d’attente des travaux pour planifier des tâches

La page Écritures file d’attente des travaux permet aux utilisateurs de planifier et d’exécuter des états et codeunits spécifiques. Vous pouvez définir des projets à exécuter une fois, ou sur une base récurrente. Par exemple, vous souhaiterez peut-être exécuter l’état **Statistiques vente * commerciaux** sur une base hebdomadaire, pour suivre les ventes par vendeur chaque semaine, ou exécuter le codeunit **Déléguer les demandes d’approbation** quotidiennement, pour empêcher les documents de s’empiler ou de bloquer le flux de travail.

La page **Écritures file d’attente des travaux** répertorie tous les projets existants. Si vous ajoutez une nouvelle écriture de file d’attente de travaux que vous souhaitez planifier, vous devez fournir certaines informations. Par exemple :

* Le type d’objet que vous souhaitez exécuter, tel qu’un rapport ou une codeunit. Vous devez être autorisé à exécuter le rapport ou la codeunit en question.
* Le nom et l’ID objet de l’objet. 
* Les paramètres pour spécifier le comportement de la file d’attente des travaux. Par exemple, vous pouvez ajouter un paramètre pour envoyer uniquement des commandes vente validées. 
* Quand et à quelle fréquence l’écriture de la file d’attente des travaux sera exécutée.

> [!IMPORTANT]  
> Si vous bénéficiez de l’ensemble d’autorisations SUPER qui est fourni avec [!INCLUDE[prod_short](includes/prod_short.md)], vous disposez des autorisations pour exécuter tous les objets inclus dans votre licence. Si vous disposez du rôle Administrateur délégué, vous pouvez créer et planifier des écritures de file d’attente de travaux, mais seuls les administrateurs et les utilisateurs sous licence peuvent les exécuter. Les utilisateurs disposant de la licence Appareil ne peuvent pas créer ni exécuter d’écritures de file d’attente de travaux.

Une fois les files d’attente des travaux configurées et en cours de exécution, le statut est modifié comme suit au cours de chaque période d’abonnement :

* **En attente**  
* **Prêt**  
* **En cours**  
* **Erreur**  
* **Terminé**  

Une fois qu’un travail s’est terminé correctement, il est supprimé de la liste d’écritures file d’attente des travaux, sauf en cas de projet récurrent. Pour les travaux récurrents, le champ **Heure de début (au plus tôt)** est ajusté pour afficher la prochaine heure d’exécution planifiée pour le projet.  

## Surveiller le statut ou les erreurs dans la file d’attente des travaux

Les données générées par la file d’attente des travaux sont stockées dans la base de données, de sorte que vous pouvez résoudre les erreurs de la file d’attente des travaux.  

Pour chaque entrée de file d’attente de travaux, vous pouvez afficher et modifier l’état. Lorsque vous créez une écriture file d’attente des travaux, son statut est défini sur **En attente**. Vous pouvez définir le statut sur **Prêt** et revenir à **En attente**, par exemple. Sinon, les informations de statut sont mises à jour automatiquement.

Le tableau suivant décrit les valeurs du champ **Statut**.

| Statut | Désignation |
|--|--|
| Prêt | L’écriture file d’attente des travaux est prête à être exécutée. |
| En cours | L’écriture file d’attente des travaux est en cours. Ce champ est mis à jour lors de l’exécution de la file d’attente des travaux. |
| En suspens | Le statut par défaut de l’écriture file d’attente des travaux lorsqu’elle est créée. Choisissez **Attribuer le statut Prêt** pour modifier le statut sur **Préparer**. Choisissez l’action **Définir sur Suspendu** pour rétablir le statut sur **En attente**. |
| Erreur | Un problème est survenu. Choisissez **Afficher erreur** pour afficher le message d’erreur. |
| PROD FINIS | L’écriture file d’attente des travaux est complète. |

> [!Tip]  
> Les écriture de la file d’attente des tâches cessent de s’exécuter en cas d’erreur. Par exemple, cela peut être un problème lorsqu’une entrée se connecte à un service externe, tel qu’un flux bancaire. Si le service est temporairement indisponible et que l’entrée de la file d’attente des travaux ne peut pas se connecter, l’entrée affichera une erreur et cessera de s’exécuter. Vous devrez redémarrer manuellement l’entrée de la file d’attente des travaux. Cependant, les champs **Nombre maximal de tentatives** et **Délai de réexécution (sec.)** peuvent vous aider à éviter cette situation. Le champ **Nombre maximal de tentatives** vous permet de spécifier combien de fois l’entrée de la file d’attente des travaux peut échouer avant qu’elle n’arrête d’essayer de s’exécuter. Le champ **Délai de réexécution (sec.)** vous permet de spécifier la durée, en secondes, entre les tentatives. La combinaison de ces deux champs peut maintenir l’entrée de la file d’attente des travaux en cours d’exécution jusqu’à ce que le service externe soit disponible.

### Pour visualiser le statut de tous les travaux

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Écritures file d’attente des travaux**, puis sélectionnez le lien associé.
2. Sur la page **Écritures file d’attente des travaux**, sélectionnez une écriture file d’attente des travaux, puis sélectionnez l’action **Écritures journal**.  

> [!TIP]
> Vous pouvez également voir le statut des écritures file d’attente des travaux en utilisant Application Insights dans Microsoft Azure pour une analyse plus approfondie basée sur la télémétrie. Pour plus d’informations, voir [Surveillance et analyse de la télémétrie](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) et [Analyse de la télémétrie de suivi du cycle de vie de la file d’attente des travaux](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) dans le contenu [!INCLUDE [prod_short](includes/prod_short.md)] pour développeurs et administrateurs.

## Afficher les tâches planifiées

La page **Tâches planifiées** dans [!INCLUDE [prod_short](includes/prod_short.md)] indique quelles tâches sont prêtes à être exécutées dans la file d’attente des travaux. La page affiche également des informations sur l’entreprise dans laquelle chaque tâche est configurée pour s’exécuter. Cependant, seules les tâches marquées comme appartenant à l’environnement actuel peuvent s’exécuter.  

Par exemple, toutes les tâches planifiées s’arrêtent si l’entreprise se trouve dans un environnement qui est une copie d’un autre environnement. Utilisez la page **Tâches planifiées** pour définir les tâches comme prêtes à être exécutées dans la file d’attente des travaux.  

> [!NOTE]
> Les administrateurs internes et les utilisateurs sous licence peuvent planifier l’exécution des tâches. Les administrateurs délégués peuvent configurer et programmer des tâches à exécuter, mais seuls les utilisateurs sous licence peuvent les exécuter.

## Composant Ma file d’attente des travaux

Le composant **Ma file d’attente des travaux** sur votre Tableau de bord répertorie les écritures files d’attente des travaux que vous avez commencées, mais qui ne sont pas terminées. Par défaut, le composant n’est pas affiché, mais vous pouvez l’ajouter à votre tableau de bord. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).  

Le composant affiche les informations suivantes :

* Quels documents ayant votre ID dans le champ **Code utilisateur affecté** sont en cours de traitement ou en attente, y compris ceux validés à l’arrière-plan. 
* S’il y a eu une erreur lors de la validation d’un document ou dans l’entrée de la file d’attente des travaux. 

Le composant Ma file d’attente des travaux permet également d’annuler une validation de document.

### Pour afficher une erreur dans le composant Ma file d’attente des travaux

1. Sur une écriture indiquant le statut **Erreur**, sélectionnez l’action **Afficher erreur**.
2. Examinez le message d’erreur et résolvez le problème.

## Exemples de ce qui peut être planifié à l’aide de la file d’attente des travaux

### Planifier des états

Vous pouvez planifier ou traiter par lots un état à exécuter à une date et une heure spécifiques. Les états prévus ou les traitements par lots sont entrés dans la file projets et traités au moment prévu, comme les autres projets. Vous devez choisir l’option **Planifié** après avoir cliqué sur l’action **Envoyer à**, puis vous devez entrer des informations telles que l’imprimante, l’heure et la date, et la récurrence.  

Pour en savoir plus, consultez [Planifier un état à exécuter](ui-work-report.md#ScheduleReport)

### Planifier la synchronisation entre [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[prod_short](includes/cds_long_md.md)]

Si vous avez intégré [!INCLUDE[prod_short](includes/prod_short.md)] avec [!INCLUDE[prod_short](includes/cds_long_md.md)], la file d’attente des travaux vous permet de planifier à quel moment synchroniser les données. Selon la direction et les règles que vous avez définies, l’entrée de la file d’attente des tâches peut créer des enregistrements dans une application pour faire correspondre les enregistrements dans l’autre. Un bon exemple est lorsque vous enregistrez un contact dans [!INCLUDE[crm_md](includes/crm_md.md)], l’entrée de la file d’attente peut configurer ce contact pour vous dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Planification d’une synchronisation entre Business Central et Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### Planifier la validation des commande vente et achat

Vous pouvez utiliser les entrées de la file d’attente des travaux pour planifier l’exécution des processus métier en arrière-plan. Par exemple, les tâches en arrière-plan sont utiles quand plusieurs utilisateurs valident des commandes vente en même temps, mais qu’une seule commande peut être traitée à la fois. Pour plus d’informations, voir [Pour paramétrer la validation en arrière-plan avec les files d’attente des travaux](ui-batch-posting.md#to-set-up-background-posting-with-job-queues)

## Surveiller la file d’attente des travaux avec la télémétrie

En tant qu’administrateur, vous pouvez utiliser [Application Insights](/azure/azure-monitor/app/app-insights-overview) pour recueillir et analyser la télémétrie que vous pouvez utiliser pour identifier les problèmes. Pour plus d’informations, consultez [Surveillance et analyse de la télémétrie](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) dans le contenu pour développeurs et administrateurs.  

## Voir aussi

[Administration](admin-setup-and-administration.md)  
[Configuration de Business Central](setup.md)  
[Modifier les paramètres de base](ui-change-basic-settings.md)  
[Analyse de la télémétrie de suivi du cycle de vie de la file d’attente des travaux](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]