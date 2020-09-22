---
title: Configuration des notifications de workflows | Microsoft Docs
description: Pour un grand nombre de réponses de workflow, il s'agit de notifier un utilisateur qu'un événement s'est produit et qu'il doit agir dessus. Par exemple, dans une étape du workflow, l'événement peut être que l'utilisateur 1 demande l'approbation d'un nouvel enregistrement, et la réponse est qu'une notification est envoyée à l'utilisateur 2, l'approbateur. Dans l'étape suivante du workflow, l'événement peut être que l'utilisateur 2 approuve l'enregistrement, et la réponse est qu'une notification est envoyée à l'utilisateur 3 pour qu'il démarre le processus associé à l'enregistrement approuvé. Pour les étapes de flux de travail concernant des approbations, chaque notification est liée à une écriture d'approbation.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: e01ef26f54e3ae085b258fdaee808ec679e8cc48
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785836"
---
# <a name="setting-up-workflow-notifications"></a>Configuration de notifications de flux de travail
Pour un grand nombre de réponses de workflow, il s'agit de notifier un utilisateur qu'un événement s'est produit et qu'il doit agir dessus. Par exemple, dans une étape du workflow, l'événement peut être que l'utilisateur 1 demande l'approbation d'un nouvel enregistrement, et la réponse est qu'une notification est envoyée à l'utilisateur 2, l'approbateur. Dans l'étape suivante du workflow, l'événement peut être que l'utilisateur 2 approuve l'enregistrement, et la réponse est qu'une notification est envoyée à l'utilisateur 3 pour qu'il démarre le processus associé à l'enregistrement approuvé. Pour les étapes de flux de travail concernant des approbations, chaque notification est liée à une écriture d'approbation. Pour plus d'informations, voir [Flux de travail](across-workflow.md).  

> [!NOTE]  
>  La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge des notifications comme des e-mails et des notes internes.  

> [!IMPORTANT]  
>  Toutes les notifications du workflow sont envoyées à l'aide d'une file projets. Assurez-vous que la file projets dans votre installation est configurée pour traiter les notifications du flux de travail, et que la case à cocher **Démarrer automatiquement à partir du serveur** est activée. Pour plus d'informations, voir [Utiliser des files d'attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

Vous pouvez configurer différents aspects des notifications du workflow dans les emplacements suivants :  

1.  Pour des flux de travail d'approbation, configurez les destinataires des notifications du flux de travail en renseignant une ligne sur la page **Paramètres utilisateur approbation** pour chaque utilisateur qui fait partie du flux de travail. Par exemple, si l'utilisateur 2 est spécifié dans le champ **ID Approbateur** sur la ligne de l'utilisateur 1, alors la notification de demande d'approbation est envoyée à l'utilisateur 1. Pour plus d'informations, voir [Configurer des utilisateurs d'approbation](across-how-to-set-up-approval-users.md).  
2.  Vous configurez quand et comment les utilisateurs reçoivent des notifications de flux de travail en renseignant la page **Tableau de notification** pour chaque utilisateur du flux de travail. Pour plus d'informations, voir [Spécifier quand et comment recevoir des notifications](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  Si vus le souhaitez, vous pouvez personnaliser le contenu des e-mails de notification en modifiant l'état 1320, notification par e-mail. Pour plus d'informations, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).  
4.  Vous configurez un contenu spécifique et des règles d'une notification de workflow lorsque vous créez le workflow en question. Pour effectuer cette opération, sélectionnez les options sur la page **Options réponse de flux de travail** pour la réponse de flux de travail qui représente la notification. Pour plus d'informations, reportez-vous à l'étape 9 dans [Créer des workflows](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Voir aussi  
 [Configurer des utilisateurs d'approbation](across-how-to-set-up-approval-users.md)   
 [Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md)   
 [Spécifier quand et comment recevoir des notifications](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Créer des workflows](across-how-to-create-workflows.md)   
 [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md)   
 [Utiliser des files d'attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)   
 [Configurer la messagerie](admin-how-setup-email.md)   
 [Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Flux de travail](across-workflow.md)   
