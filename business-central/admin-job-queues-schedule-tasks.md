---
title: Planifier des projets à exécuter automatiquement
description: Les tâches planifiées sont gérées par la file d’attente des travaux. Ces projets exécutent des états et des codeunits. Vous pouvez définir des projets à exécuter une fois, ou sur une base récurrente.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/12/2021
ms.author: edupont
ms.openlocfilehash: 074a110a4aac42d9b6058e377c45de0c23409bb2
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470277"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Utiliser des files d’attente des travaux pour planifier des tâches

Des files d’attente des travaux dans [!INCLUDE[prod_short](includes/prod_short.md)] permettent aux utilisateurs de planifier et d’exécuter des états et codeunits spécifiques. Vous pouvez définir des projets à exécuter une fois, ou sur une base récurrente. Par exemple, vous souhaiterez peut-être exécuter l’état **Statistiques vente commerciaux** sur une base hebdomadaire, pour suivre les ventes par vendeur chaque semaine, ou vous pouvez exécuter le codeunit **Déléguer les demandes d’approbation** quotidiennement, pour empêcher les documents de s’empiler ou de bloquer le flux de travail.

La page **Écritures file d’attente des travaux** répertorie tous les projets existants. Si vous ajoutez une nouvelle écriture file d’attente des travaux que vous voulez planifier, vous devez spécifier des informations sur le type d’objet à exécuter, par exemple un état ou un codeunit et le nom et l’ID de l’objet que vous voulez exécuter. Vous pouvez également ajouter des paramètres pour spécifier le comportement de la file d’attente des travaux. Par exemple, vous pouvez ajouter un paramètre pour envoyer uniquement des commandes vente validées. Vous devez être autorisé à exécuter l’état ou le codeunit spécifié, sans quoi une erreur est renvoyée lors de l’exécution de la file projets.  
> [!IMPORTANT]  
> Si vous utilisez l’ensemble d’autorisations SUPER qui est fourni avec [!INCLUDE[prod_short](includes/prod_short.md)], les utilisateurs et vous-même disposez des autorisations pour exécuter tous les objets dans la licence. Cela n’est toujours pas suffisant pour les administrateurs délégués ou les utilisateurs disposant d’une licence de périphérique, qui ne peuvent pas créer des entrées de file d’attente de travaux.

Une file d’attente des travaux peut comporter plusieurs écritures correspondant aux projets que la file gère et exécute. Les informations contenues dans les écritures spécifient le codeunit ou l’état exécuté, la date et le nombre de fois de l’exécution d’une écriture, la catégorie dans laquelle le projet s’exécute et comment il s’exécute.  

Une fois les files d’attente des travaux configurées et en cours de exécution, le statut est modifié comme suit au cours de chaque période d’abonnement :

* **En attente**  
* **Prêt**  
* **En cours**  
* **Erreur**  
* **Terminé**  

Une fois qu’un projet s’est terminé correctement, il est supprimé de la liste d’écritures file d’attente des travaux, sauf en cas de projet récurrent. S’il s’agit d’un projet récurrent, le champ **Heure de début (au plus tôt)** est ajusté pour afficher la prochaine heure d’exécution planifiée pour le projet.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Pour visualiser le statut ou les erreurs dans la file d’attente des travaux

Les données qui sont générées lors de l’exécution d’une file d’attente des travaux sont stockées dans la base de données, de sorte que vous pouvez résoudre les erreurs de la file d’attente des travaux.  
Pour chaque entrée de file d’attente de travaux, vous pouvez afficher et modifier l’état. Lorsque vous créez une écriture file d’attente des travaux, son statut est défini sur **En attente**. Vous pouvez définir le statut sur **Prêt** et revenir à **En attente**, par exemple. Sinon, les informations de statut sont mises à jour automatiquement.

Le tableau suivant décrit les valeurs du champ **Statut**.

| Statut | Description |
|--|--|
| Prêt | Indique que l’écriture file d’attente des travaux est prête à être exécutée. |
| En cours | Indique que l’écriture file d’attente des travaux est en cours. Ce champ est mis à jour lors de l’exécution de la file d’attente des travaux. |
| En attente | Par défaut. Indique le statut de l’écriture file d’attente des travaux lorsqu’elle est créée. Choisissez **Attribuer le statut Prêt** pour modifier le statut sur **Préparer**. Choisissez **Ensemble en attente** ou **Suspendre** pour ramener le statut **En attente**. |
| Erreur | Indique qu’il y a une erreur. Choisissez **Afficher erreur** pour visualiser le message d’erreur. |
| Terminé | Indique que l’écriture file d’attente des travaux est complète. |

### <a name="to-view-status-for-any-job"></a>Pour visualiser le statut de tous les travaux
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Écritures file d’attente des travaux**, puis choisissez le lien associé.
2. Sur la page **Écritures file d’attente des travaux**, sélectionnez une écriture file d’attente des travaux, puis sélectionnez l’action **Écritures journal**.  

> [!TIP]
> Avec [!INCLUDE [prod_short](includes/prod_short.md)] en ligne, vous pouvez également afficher l’état des entrées de la file d’attente des travaux en utilisant Application Insights dans Microsoft Azure. Pour plus d’informations, consultez [Analyse de la télémétrie de suivi du cycle de vie de la file d’attente des travaux](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) dans le contenu dédié à l’équipe Administration et aux développeurs [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="the-my-job-queue-part"></a>Composant Ma file d’attente des travaux
Le composant **Ma file d’attente des travaux** sur votre Tableau de bord répertorie les écritures files d’attente des travaux commencées par vous, mais qui ne sont pas terminées. Par défaut, le composant n’est pas visible et vous devez donc l’ajouter à votre tableau de bord. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).  

Le composant indique les documents avec votre ID dans le champ **Code utilisateur affecté** en cours de traitement ou en attente, y compris ceux associés à la validation en arrière-plan. Le composant peut vous indiquer rapidement s’il y a eu une erreur lors de la validation d’un document ou s’il existe des erreurs dans une écriture de file projet. Il vous permet également d’annuler une validation de document en cas de non exécution.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Pour afficher une erreur dans le composant Ma file d’attente des travaux
1. Sur une écriture indiquant le statut **Erreur**, sélectionnez l’action **Afficher erreur**.
2. Examinez le message d’erreur et résolvez le problème.


## <a name="examples-of-what-can-be-scheduled-using-job-queue"></a>Exemples de ce qui peut être planifié à l’aide de la file d’attente des travaux

### <a name="schedule-reports"></a>Planifier des états

Vous pouvez planifier ou traiter par lots un état à exécuter à une date et une heure spécifiques. Les états prévus ou les traitements par lots sont entrés dans la file projets et traités au moment prévu, comme les autres projets. Vous devez choisir l’option **Planifié** après avoir cliqué sur l’action **Envoyer à**, puis vous devez entrer des informations telles que l’imprimante, l’heure et la date, et la récurrence.  

Pour en savoir plus, consultez [Planifier un état à exécuter](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between-prod_short-and-prod_short"></a>Planifier la synchronisation entre [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[prod_short](includes/cds_long_md.md)]

Si vous avez intégré [!INCLUDE[prod_short](includes/prod_short.md)] à [!INCLUDE[prod_short](includes/cds_long_md.md)], vous pouvez utiliser la file d’attente des travaux pour planifier à quel moment vous souhaitez synchroniser les données des enregistrements que vous avez couplés dans les deux applications métier. Selon la direction et les règles que vous avez définies pour l’intégration, les tâches de synchronisation peuvent également créer des enregistrements dans l’application de destination pour correspondre à ceux de la source. Par exemple, si un vendeur crée un contact dans [!INCLUDE[crm_md](includes/crm_md.md)], la tâche de synchronisation peut créer ce contact pour le vendeur couplé dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Planification d’une synchronisation entre Business Central et Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-the-posting-of-sales-and-purchase-orders"></a>Planifier la validation des commande vente et achat

Les files d’attente des travaux sont un outil efficace pour planifier l’exécution des processus d’entreprises en arrière-plan, par exemple lorsque plusieurs utilisateurs essaient de valider des commandes vente, mais uniquement une commande à la fois.  

Pour plus d’informations, voir [Pour paramétrer la validation en arrière-plan avec les files d’attente des travaux](ui-batch-posting.md#to-set-up-background-posting-with-job-queues)

## <a name="see-also"></a>Voir aussi

[Administration](admin-setup-and-administration.md)  
[Configuration de Business Central](setup.md)  
[Modifier les paramètres de base](ui-change-basic-settings.md)  
[Analyse de la télémétrie de suivi du cycle de vie de la file d’attente des travaux](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]