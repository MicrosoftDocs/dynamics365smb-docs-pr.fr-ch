---
title: Planifier des projets à exécuter automatiquement | Microsoft Docs
description: Les tâches planifiées sont gérées par la file d'attente des travaux. Ces projets exécutent des états et des codeunits. Vous pouvez définir des projets à exécuter une fois, ou sur une base récurrente.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: fc2c2de39c3391a430adda72a841b01897235f68
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196702"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Utiliser des files d'attente des travaux pour planifier des tâches
Des files d'attente des travaux dans [!INCLUDE[d365fin](includes/d365fin_md.md)] permettent aux utilisateurs de planifier et d'exécuter des états et codeunits spécifiques. Vous pouvez définir des projets à exécuter une fois, ou sur une base récurrente. Par exemple, vous pouvez être amené à exécuter l'état **Vendeurs : Statistiques ventes** chaque semaine pour suivre les ventes hebdomadaires d'un vendeur, ou vous pouvez être amené à exécuter le codeunit **Traiter file att. e-mails serv** chaque jour pour vérifier si des e mails adressés aux clients concernant leurs commandes service sont envoyés en temps utile.

La page **Écritures file d'attente des travaux** répertorie tous les projets existants. Si vous ajoutez une nouvelle écriture file d'attente des travaux que vous voulez planifier, vous devez spécifier des informations sur le type d'objet à exécuter, par exemple un état ou un codeunit et le nom et l'ID de l'objet que vous voulez exécuter. Vous pouvez également ajouter des paramètres pour spécifier le comportement de la file d'attente des travaux. Par exemple, vous pouvez ajouter un paramètre pour envoyer uniquement des commandes vente validées. Vous devez être autorisé à exécuter l'état ou le codeunit spécifié, sans quoi une erreur est renvoyée lors de l'exécution de la file projets.  

Une file d'attente des travaux peut comporter plusieurs écritures correspondant aux projets que la file gère et exécute. Les informations contenues dans les écritures spécifient le codeunit ou l'état exécuté, la date et le nombre de fois de l'exécution d'une écriture, la catégorie dans laquelle le projet s'exécute et comment il s'exécute.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Pour paramétrer la validation en arrière-plan avec les files d'attente des travaux
Les files d'attente des travaux sont un outil efficace pour planifier l'exécution des processus d'entreprises en arrière-plan, par exemple lorsque plusieurs utilisateurs essaient de valider des commandes vente, mais uniquement une commande à la fois. Sinon, vous pouvez planifier des validations à des heures pratiques pour votre organisation. Par exemple, il peut sembler raisonnable dans votre activité d'exécuter certaines routines lorsque la plupart de la saisie de données de la journée est achevée.

Vous pouvez obtenir cette opération en configurant la file projets pour exécuter différents états de validation par lots, par exemple, **TPL valider commandes vente**, **TPL valider factures vente**, **TPL valider retours vente** et les états **TPL valider avoirs vente**. Pour plus d'informations, voir [Pour créer une écriture file d'attente des travaux pour la validation de commande vente en arrière-plan](admin-job-queues-schedule-tasks.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge la validation en arrière-plan de toutes les ventes, achats, et documents service.

> [!NOTE]
> Certains travaux modifient les données identiques et ne doivent pas s'exécuter en simultané, car cela peut provoquer des conflits. Par exemple, les travaux d'arrière-plan des documents de vente tentent de modifier les données identiques en simultané. Les catégories de files d'attente des travaux permettent d'éviter ces types de conflits en garantissant que lorsqu'un travail est en cours d'exécution, un autre travail appartenant à la même catégorie de file d'attente des travaux ne s'exécutera pas avant la fin. Par exemple, un travail relevant d'une catégorie de file d'attente des travaux de vente attendra que tous les autres travaux liés aux ventes soient terminés. Vous spécifiez une catégorie de file d'attente des travaux sur le raccourci **Validation en arrière-plan** sur la page **Paramètre ventes**. 
> 
> [!INCLUDE[d365fin](includes/d365fin_md.md)] fournit des catégories de file d'attente des travaux pour les ventes, les achats et la comptabilité générale. Nous recommandons que l'une d'entre elles, ou celle que vous créez, soit toujours spécifiée. Si vous rencontrez des échecs en raison de conflits, pensez à configurer une catégorie pour toutes les ventes, les achats et la validation comptable en arrière-plan.

La procédure suivante explique comment configurer la validation en arrière-plan des commandes vente. La procédure est identique pour un achat et un service.  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres ventes**, puis sélectionnez le lien associé.
2. Sur la page **Paramètres ventes**, activez la case à cocher **Valider avec la file d'attente des travaux**.
3. Pour filtrer les écritures de file d'attente des travaux pour la validation de commandes vente, choisissez le champ **Code catégorie de la file d'attente des travaux**, puis sélectionnez la catégorie **Validvent**.

    Un objet de file d'attente de travaux, codeunit 88 **Validation des ventes via la file d'attente des travaux**, est créé. Pour l'activer, passez à la page **Écritures file d'attente des travaux**.
4. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Écritures file d'attente des travaux**, puis choisissez le lien associé.
5. Sur la page **Écritures file d'attente des travaux**, choisissez l'action **Nouveau**.
6. Dans le champ **Type objet à exécuter**, sélectionnez **Codeunit**.  
7. Dans le champ **ID objet à exécuter**, sélectionnez **88**. Les champs Description et Légende de l'objet à exécuter affichent le message de vente via la file d'attente des travaux.

    Aucune autre champ n'est valable pour ce scénario.
8. Choisissez l'action **Attribuer le statut Prêt**.
9. Pour vérifier que la file d'attente des travaux fonctionne comme prévu, validez une commande vente. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).
10. Vérifiez sur la page **Écritures journal file d'attente des travaux** si la commande vente a été validée avec succès. Pour plus d'informations, voir [Pour afficher le statut ou les erreurs dans la fille d'attente](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Si vous souhaitez également que des documents vente soient imprimés lorsqu'ils sont validés, sélectionnez la case à cocher **Valider et imprimer avec la file d'attente des travaux** sur la page **Paramètres ventes**.  

> [!IMPORTANT]  
> Si vous paramétrez un projet qui valide et imprime des documents et que l'imprimante affiche une boîte de dialogue, par exemple une demande d'informations d'identification ou un alerte à propos de la quantité faible d'encre, votre document est validé mais non imprimé. L'écriture file d'attente de travaux correspondante expire et la valeur du champ **Statut** devient **Erreur**. Par conséquent, nous vous recommandons de ne pas utiliser une configuration de l'imprimante nécessitant une interaction avec les boîtes de dialogue de l'imprimante relatives à la validation en arrière-plan.

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Pour créer une écriture file d'attente des travaux pour la validation par lots des commandes vente
La procédure suivante décrit comment définir le rapport **TPL valider commandes vente** pour une validation automatique des commandes vente lancées à 16 h 00 les jours de semaine.  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Écritures file d'attente des travaux**, puis choisissez le lien associé.  
2. Sélectionnez l'action **Nouveau**.  
3. Dans le champ **Type objet à exécuter**, sélectionnez **Rapport**.  
4. Dans le champ **ID objet à exécuter**, sélectionnez 296, **TPL valider commandes vente**.
5. Activez la case à cocher **Page requête état**.
6. Dans la page de demande **TPL valider commandes vente**, définissez ce qui est inclus lors de la validation automatique des commandes vente, puis sélectionnez le bouton **OK**.
7. Activez toutes les cases à cocher de **Exécuter le lundi** à **Exécuter le vendredi**.
8. Dans le champ **Heure début**, entrez 16 h 00.
9. Choisissez l'action **Attribuer le statut Prêt**.

Les commandes vente prêtes à la validation sont à présent validées chaque jour de la semaine à 16 h 00.

> [!NOTE]
> Si la file d'attente des travaux ne peut pas valider la commande vente, le statut passe à **Erreur**, et la commande vente est ajoutée à la liste des commandes vente que l'utilisateur doit traiter. Pour plus d'informations, voir [Pour afficher le statut ou les erreurs dans la fille d'attente](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Une fois les files d'attente des travaux configurées et en cours de exécution, le statut est modifié comme suit au cours de chaque période d'abonnement :

* **En attente**  
* **Prêt**  
* **En cours**  
* **Erreur**  
* **Terminé**  

Une fois qu'un projet s'est terminé correctement, il est supprimé de la liste d'écritures file d'attente des travaux, sauf en cas de projet récurrent. S'il s'agit d'un projet récurrent, le champ **Heure de début (au plus tôt)** est ajusté pour afficher la prochaine heure d'exécution planifiée pour le projet.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Pour visualiser le statut ou les erreurs dans la file d'attente des travaux
Les données qui sont générées lors de l'exécution d'une file d'attente des travaux sont stockées dans la base de données, de sorte que vous pouvez résoudre les erreurs de la file d'attente des travaux.

### <a name="to-view-status-for-any-job"></a>Pour visualiser le statut de tous les travaux
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Écritures file d'attente des travaux**, puis choisissez le lien associé.
2. Sur la page **Écritures file d'attente des travaux**, sélectionnez une écriture file d'attente des travaux, puis sélectionnez l'action **Écritures journal**.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Pour afficher un statut dans un document vente ou achat
1. Dans le document que vous avez essayé de valider avec la file d'attente des travaux, choisissez le champ **Statut de la file d'attente des travaux**, qui contient **Erreur**.
2. Examinez le message d’erreur et résolvez le problème.

## <a name="the-my-job-queue-part"></a>Composant Ma file d'attente des travaux
Le composant **Ma file d'attente des travaux** sur votre Tableau de bord répertorie les écritures files d'attente des travaux commencées par vous, mais qui ne sont pas terminées. Par défaut, le composant n'est pas visible et vous devez donc l'ajouter à votre tableau de bord. Pour plus d'informations, voir [Modifier les paramètres de base](ui-change-basic-settings.md).  

Le composant indique les documents avec votre ID dans le champ **Code utilisateur affecté** en cours de traitement ou en attente, y compris ceux associés à la validation en arrière-plan. Le composant peut vous indiquer rapidement s’il y a eu une erreur lors de la validation d’un document ou s’il existe des erreurs dans une écriture de file projet. Il vous permet également d'annuler une validation de document en cas de non exécution.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Pour afficher une erreur dans le composant Ma file d’attente des travaux
1. Sur une écriture indiquant le statut **Erreur**, sélectionnez l'action **Afficher erreur**.
2. Examinez le message d’erreur et résolvez le problème.

## <a name="security"></a>Sécurité  
Les écritures file d'attente des travaux s'exécutent sur la base d'autorisations. Ces autorisations doivent permettre l'exécution de l'état ou du codeunit.  

Lorsqu'une file d'attente des travaux est activée manuellement, elle s'exécute avec les informations d'identification de l'utilisateur. Lorsqu'une file d'attente des travaux est activée en tant que tâche planifiée, elle s'exécute avec les informations d'identification de l'instance du serveur. Un projet s'exécute avec les informations d'identification de la file d'attente des travaux qui l'active. L'utilisateur qui a créé cette écriture file d'attente des travaux doit toutefois disposer d'autorisations. Lorsqu'un projet est exécuté dans la session utilisateur (par exemple, durant la validation en arrière plan), il est exécuté avec les informations d'identification de l'utilisateur qui a créé ce projet.  

> [!IMPORTANT]  
>  Si vous utilisez l'ensemble d'autorisations SUPER qui est fourni avec [!INCLUDE[d365fin](includes/d365fin_md.md)], les utilisateurs et vous-même disposez des autorisations pour exécuter tous les objets. Dans ce cas, l'accès accordé à chaque utilisateur est uniquement limité par les autorisations relatives aux données.  

## <a name="using-job-queues-effectively"></a>Utilisation efficace des files d'attente des travaux  
L'enregistrement des écritures file d'attente des travaux possède plusieurs champs dont l'objectif est d'exécuter des paramètres dans un codeunit que vous avez indiqué comme devant être exécuté avec une file d'attente des travaux. Cela signifie également que les codeunits devant être exécutés via la file d'attente des travaux doivent être indiqués avec l'enregistrement des écritures file d'attente des travaux en tant que paramètre dans le déclencheur **OnRun**. Un niveau de sécurité supplémentaire est ainsi assuré, car les utilisateurs ne peuvent pas exécuter de codeunits aléatoires via la file d'attente des travaux. Si l'utilisateur doit transmettre des paramètres à un état, il n'a d'autre choix que celui d'inclure l'exécution de l'état dans un codeunit, lequel analyse ensuite les paramètres d'entrée et les intègre dans l'état avant de l'exécuter.  

## <a name="scheduling-synchronization-between-d365fin-and-d365fin"></a>Planification de la synchronisation entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)]
Si vous avez intégré [!INCLUDE[d365fin](includes/d365fin_md.md)] à [!INCLUDE[d365fin](includes/cds_long_md.md)], vous pouvez utiliser la file d'attente des travaux pour planifier à quel moment vous souhaitez synchroniser les données des enregistrements que vous avez couplés dans les deux applications métier. Selon la direction et les règles que vous avez définies pour l'intégration, les tâches de synchronisation peuvent également créer des enregistrements dans l'application de destination pour correspondre à ceux de la source. Par exemple, si un vendeur crée un contact dans [!INCLUDE[crm_md](includes/crm_md.md)], la tâche de synchronisation peut créer ce contact pour le vendeur couplé dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Planification d'une synchronisation entre Business Central et Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

## <a name="see-also"></a>Voir aussi  
[Administration](admin-setup-and-administration.md)  
[Configuration de Business Central](setup.md)  
[Modifier les paramètres de base](ui-change-basic-settings.md)  
