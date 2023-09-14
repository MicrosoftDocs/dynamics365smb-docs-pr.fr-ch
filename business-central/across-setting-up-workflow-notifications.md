---
title: Configuration de notifications de flux de travail d’approbation
description: "Cet article vous explique comment configurer des notifications de flux de travail pour alerter un utilisateur qu’un événement s’est produit auquel il doit réagir\_; une réponse de flux de travail est requise."
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: bholtorf
---
# Notifications flux de travail approbation

Configurez vos flux de travail pour avertir automatiquement les utilisateurs lorsque leur attention est requise pour une étape de ce flux de travail. Pour un grand nombre de réponses du flux de travail, il s’agit de notifier un utilisateur qu’un événement s’est produit et qu’il doit agir dessus.

Par exemple, vous pouvez définir que l’utilisateur 2, l’approbateur, reçoit une notification chaque fois que l’utilisateur 1 demande l’approbation d’un nouvel enregistrement. À l’étape suivante du flux de travail, l’utilisateur 2 est averti après que l’utilisateur 3 a approuvé l’enregistrement afin de démarrer un traitement connexe de l’enregistrement. Avec les étapes de flux de travail concernant des approbations, chaque notification est liée à une écriture d’approbation. En savoir plus sur [Flux de travail](across-workflow.md).  

> [!NOTE]  
> La version par défaut de [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge des notifications comme des e-mails et des notes internes.  

> [!IMPORTANT]  
> Toutes les notifications du workflow sont envoyées à l’aide d’une file projets. Assurez-vous que la file projets dans votre installation est configurée pour traiter les notifications du flux de travail, et que la case à cocher **Démarrer automatiquement à partir du serveur** est activée. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

## Configurer les notifications

Vous pouvez configurer différents aspects des notifications du workflow dans les emplacements suivants :  

* Notification d’approbateur

  Pour des flux de travail d’approbation, configurez les destinataires des notifications du flux de travail en renseignant une ligne sur la page **Paramètres utilisateur approbation** pour chaque utilisateur qui fait partie du flux de travail.  

  Par exemple, si l’utilisateur 2 est spécifié dans le champ **ID Approbateur** sur la ligne de l’utilisateur 1, alors la notification de demande d’approbation est envoyée à l’utilisateur 2. En savoir plus sur [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md). 
  
* Tableaux de notification

  Vous configurez quand et comment les utilisateurs reçoivent des notifications de flux de travail en renseignant la page **Tableau de notification** pour chaque utilisateur du flux de travail. En savoir plus sur [Spécifier quand et comment recevoir les notifications de flux de travail](across-how-to-specify-when-and-how-to-receive-notifications.md). 
  
* Personnaliser les notifications par e-mail

  Si vous le souhaitez, vous pouvez personnaliser le contenu des e-mails de notification en modifiant l’état 1320, notification par e-mail. En savoir plus sur [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).  

  > [!NOTE]
  > Si vous souhaitez utiliser l’e-mail comme méthode de notification, vous devez configurer l’adresse e-mail de l’expéditeur et du destinataire dans [!INCLUDE [prod_short](includes/prod_short.md)]. En savoir plus sur [Configurer les e-mails](admin-how-setup-email.md).
  
* Options de réponse

  Vous configurez un contenu spécifique et des règles d’une notification de flux de travail lorsque vous créez le flux de travail en question. Sélectionnez l’option de personnalisation sur la page **Réponses de flux de travail** pour la réponse de flux de travail qui représente la notification. En savoir plus à partir de l’étape 9 de la section [Créer des flux de travail](across-how-to-create-workflows.md#to-create-a-workflow). 
  
* Notifier l’expéditeur

  Pour les flux de travail d’approbation, ajoutez une étape de réponse de flux de travail pour informer l’expéditeur lorsque la demande a été approuvée ou rejetée. En savoir plus à partir de l’étape 9 de la section [Créer des flux de travail](across-how-to-create-workflows.md#to-create-a-workflow).   

## Voir la [formation Microsoft](/training/modules/create-workflows/) associée

## Voir aussi

[Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md)  
[Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md)  
[Spécifier quand et comment recevoir des notifications](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Créer des flux de travail approbation](across-how-to-create-workflows.md)  
[Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md)  
[Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)  
[Configurer la messagerie](admin-how-setup-email.md)  
[Procédure pas à pas : configuration et utilisation d’un flux d’approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Flux de travail](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
