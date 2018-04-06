---
title: Configuration des notifications de workflows | Microsoft Docs
description: "Pour un grand nombre de réponses de workflow, il s'agit de notifier un utilisateur qu'un événement s'est produit et qu'il doit agir dessus. Par exemple, dans une étape du workflow, l'événement peut être que l'utilisateur 1 demande l'approbation d'un nouvel enregistrement, et la réponse est qu'une notification est envoyée à l'utilisateur 2, l'approbateur. Dans l'étape suivante du workflow, l'événement peut être que l'utilisateur 2 approuve l'enregistrement, et la réponse est qu'une notification est envoyée à l'utilisateur 3 pour qu'il démarre le processus associé à l'enregistrement approuvé. Pour les étapes de flux de travail concernant des approbations, chaque notification est liée à une écriture d'approbation."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 351c079df25516a83de42d5fa12954b25ba5e63e
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-workflow-notifications"></a>Configuration de notifications de flux de travail
Pour un grand nombre de réponses de workflow, il s'agit de notifier un utilisateur qu'un événement s'est produit et qu'il doit agir dessus. Par exemple, dans une étape du workflow, l'événement peut être que l'utilisateur 1 demande l'approbation d'un nouvel enregistrement, et la réponse est qu'une notification est envoyée à l'utilisateur 2, l'approbateur. Dans l'étape suivante du workflow, l'événement peut être que l'utilisateur 2 approuve l'enregistrement, et la réponse est qu'une notification est envoyée à l'utilisateur 3 pour qu'il démarre le processus associé à l'enregistrement approuvé. Pour les étapes de flux de travail concernant des approbations, chaque notification est liée à une écriture d'approbation. Pour plus d'informations, voir [Flux de travail](across-workflow.md).  

> [!NOTE]  
>  La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge des notifications comme des e\-mails et des notes internes.  

> [!IMPORTANT]  
>  Toutes les notifications du workflow sont envoyées à l'aide d'une file projets. Assurez-vous que la file projets figure dans votre solution. Pour plus d'informations, voir [Utiliser des files d'attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

Vous pouvez configurer différents aspects des notifications du workflow dans les emplacements suivants :  

1.  Pour des workflows d'approbation, configurez les destinataires des notifications du workflow en renseignant une ligne dans la fenêtre **Paramètres utilisateur approbation** pour chaque utilisateur qui fait partie du workflow. Par exemple, si l'utilisateur 2 est spécifié dans le champ **ID Approbateur** sur la ligne de l'utilisateur 1, alors la notification de demande d'approbation est envoyée à l'utilisateur 1. Pour plus d'informations, voir [Configurer des utilisateurs d'approbation](across-how-to-set-up-approval-users.md).  
2.  Vous définissez quand et comment les utilisateurs reçoivent des notifications de workflow en renseignant la fenêtre **Tableau de notification** pour chaque utilisateur du workflow. Pour plus d'informations, voir [Spécifier quand et comment recevoir des notifications](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  Vous configurez le contenu général et la mise en forme des notifications, y compris les notifications concernant les réponses de workflow échues, en configurant des modèles de notification dans la fenêtre **Modèles de notification**. Vous pouvez utiliser les modèles par défaut fournis avec [!INCLUDE[d365fin](includes/d365fin_md.md)].  
4.  Vous configurez un contenu spécifique et des règles d'une notification de workflow lorsque vous créez le workflow en question. Pour effectuer cette opération, sélectionnez les options dans la fenêtre **Options réponse de flux de travail** pour la réponse de workflow qui représente la notification. Pour plus d'informations, reportez-vous à l'étape 9 dans [Créer des workflows](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Voir aussi  
 [Configurer des utilisateurs d'approbation](across-how-to-set-up-approval-users.md)   
 [Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md)   
 [Spécifier quand et comment recevoir des notifications](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Créer des workflows](across-how-to-create-workflows.md)   
 [Gérer les modèles de notification](across-how-to-manage-notification-templates.md)   
 [Utiliser des files d'attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)   
 [Configurer la messagerie](madeira-how-setup-email.md)   
 [Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Flux de travail](across-workflow.md)   

