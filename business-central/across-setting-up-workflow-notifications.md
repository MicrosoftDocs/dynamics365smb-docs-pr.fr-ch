---
title: Configuration de notifications de flux de travail
description: Cet article vous explique comment configurer des notifications de flux de travail pour alerter un utilisateur qu’un événement s’est produit auquel il doit réagir ; une réponse de flux de travail est requise.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 9405af9c52b17ab34fded263692e3294ed8aaf11
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533983"
---
# <a name="workflow-notifications"></a>Notifications flux de travail

Configurez vos flux de travail pour avertir automatiquement les utilisateurs lorsque leur attention est requise pour une étape de ce flux de travail. Pour un grand nombre de réponses de workflow, il s’agit de notifier un utilisateur qu’un événement s’est produit et qu’il doit agir dessus.

Par exemple, vous pouvez définir que l'utilisateur 2, l'approbateur, reçoit une notification chaque fois que l'utilisateur 1 demande l'approbation d'un nouvel enregistrement. À l'étape suivante du flux de travail, l'utilisateur 3 est averti après que l'utilisateur 2 a approuvé l'enregistrement afin de démarrer un traitement connexe de l'enregistrement. Avec les étapes de flux de travail concernant des approbations, chaque notification est liée à une écriture d’approbation. Pour plus d’informations, voir [Flux de travail](across-workflow.md).  

> [!NOTE]  
> La version par défaut de [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge des notifications comme des e-mails et des notes internes.  

> [!IMPORTANT]  
> Toutes les notifications du workflow sont envoyées à l’aide d’une file projets. Assurez-vous que la file projets dans votre installation est configurée pour traiter les notifications du flux de travail, et que la case à cocher **Démarrer automatiquement à partir du serveur** est activée. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Configurer les notifications

Vous pouvez configurer différents aspects des notifications du workflow dans les emplacements suivants :  

* Notification d’approbateur

    Pour des flux de travail d’approbation, configurez les destinataires des notifications du flux de travail en renseignant une ligne sur la page **Paramètres utilisateur approbation** pour chaque utilisateur qui fait partie du flux de travail.  

    Par exemple, si l’utilisateur 2 est spécifié dans le champ **ID Approbateur** sur la ligne de l’utilisateur 1, alors la notification de demande d’approbation est envoyée à l’utilisateur 2. Pour plus d’informations, voir [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md).  
* Tableaux de notification

    Vous configurez quand et comment les utilisateurs reçoivent des notifications de flux de travail en renseignant la page **Tableau de notification** pour chaque utilisateur du flux de travail. Pour plus d’informations, voir [Spécifier quand et comment recevoir des notifications](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Personnaliser les notifications par e-mail

    Si vous le souhaitez, vous pouvez personnaliser le contenu des e-mails de notification en modifiant l’état 1320, notification par e-mail. Pour plus d’informations, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).  

    > [!NOTE]
    > Si vous souhaitez utiliser l’e-mail comme méthode de notification, vous devez configurer l’adresse e-mail de l’expéditeur et du destinataire dans [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Configurer l’adresse e-mail](admin-how-setup-email.md).

* Options de réponse

    Vous configurez un contenu spécifique et des règles d’une notification de workflow lorsque vous créez le workflow en question. Sélectionnez l'option de personnalisation sur la page **Réponses de flux de travail** pour la réponse de flux de travail qui représente la notification. Pour plus d’informations, reportez-vous à l’étape 9 dans [Créer des workflows](across-how-to-create-workflows.md#to-create-a-workflow).  

* Notifier l’expéditeur

    Pour les flux de travail d’approbation, ajoutez une étape de réponse de flux de travail pour informer l’expéditeur lorsque la demande a été approuvée ou rejetée. Pour plus d’informations, reportez-vous à l’étape 9 dans [Créer des workflows](across-how-to-create-workflows.md#to-create-a-workflow).  

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/create-workflows/) associée

## <a name="see-also"></a>Voir aussi

[Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md)  
[Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md)  
[Spécifier quand et comment recevoir des notifications](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Créer des workflows](across-how-to-create-workflows.md)  
[Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md)  
[Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)  
[Configurer la messagerie](admin-how-setup-email.md)  
[Procédure pas à pas : configuration et utilisation d’un flux d’approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Flux de travail](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
