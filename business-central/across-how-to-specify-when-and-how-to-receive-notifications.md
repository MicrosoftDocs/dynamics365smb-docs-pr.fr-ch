---
title: 'Procédure : spécifier quand et comment recevoir des notifications | Microsoft Docs'
description: Lorsque vous paramétrez des utilisateurs dans des flux de travail d’approbation, vous devez spécifier sur les pages Paramètres de notification et Tableau de notification quand et comment chaque utilisateur reçoit des notifications sur les étapes du flux de travail d’approbation. Les utilisateurs individuels peuvent également modifier leur paramètre de notification en choisissant le bouton Changer les paramètres de notification sur toute notification.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d96d094547b71fc722c06facb80a131786df0e58
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774626"
---
# <a name="specify-when-and-how-to-receive-notifications"></a>Spécifier quand et comment recevoir des notifications
Lorsque vous paramétrez des utilisateurs dans des flux de travail d’approbation, vous devez spécifier sur les pages **Paramètres de notification** et **Tableau de notification** quand et comment chaque utilisateur reçoit des notifications sur les étapes du flux de travail d’approbation. Les utilisateurs individuels peuvent également modifier leur paramètre de notification en choisissant le bouton **Changer les paramètres de notification** sur toute notification.  

> [!NOTE]
> Les notifications sont envoyées en fonction des paramètres de notification pour le destinataire, et non l’expéditeur. Cette distinction est importante, car cela signifie que lorsqu’un utilisateur demande une approbation dans le cadre d’un flux de travail, sa demande n’est pas nécessairement envoyée immédiatement. Elle est envoyée conformément aux paramètres de notification des approbateurs. 

 Avant de pouvoir paramétrer des préférences de notification d’un utilisateur approbation, vous devez configurer l’utilisateur en tant qu’utilisateur approbation. Pour plus d’informations, voir [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md).  

 Vous pouvez définir la présentation des e-mails de notification en personnalisant l’état 1320, notification par e-mail. Pour plus d’informations, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).  

 Pour un grand nombre d’étapes d’approbation du workflow, il s’agit de notifier des utilisateurs qu’un événement s’est produit et qu’ils peuvent agir dessus. Par exemple, sur une étape de workflow, l’événement peut être que l’Utilisateur 1 demande l’approbation d’un nouvel enregistrement. La réponse associée est qu’une notification est envoyée à l’Utilisateur 2, l’approbateur. Sur la prochaine étape de workflow, l’événement peut être que l’Utilisateur 2 approuve l’enregistrement. La réponse associée est qu’une notification est envoyée à l’Utilisateur 3 afin de commencer un processus avec l’enregistrement approuvé. Pour les étapes de workflow concernant des approbations, chaque notification est liée à une écriture d’approbation. Pour plus d’informations, voir [Flux de travail](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Spécifier quand et comment recevoir des notifications  

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres utilisateur approbation**, puis sélectionnez le lien associé.  
2.  Sélectionnez la ligne pour l’utilisateur pour lequel vous souhaitez paramétrer des préférences de notification, puis choisissez l’action **Paramètre de notification**.  
3.  Sur la page **Paramètres de notification**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Type de notification**|Spécifiez le type d’événement dont il s’agit dans la notification.<br /><br /> Sélectionnez l’une des options suivantes :<br /><br /> -   **Nouvel enregistrement** spécifie que la notification concerne un nouvel enregistrement, par exemple un document sur lequel l’utilisateur doit agir.<br />-   **Approbation** spécifie que la notification concerne une ou plusieurs demandes d’approbation.<br />-   **Échu** spécifie que l’objet de la notification est de rappeler aux utilisateurs qu’ils sont en retard pour agir sur un événement.|  
    |**Mode de notification**|Spécifiez si la notification est un e-mail ou une note interne.|

    Vous pouvez définir la présentation des e-mails de notification en personnalisant l’état 1320, notification par e-mail. Pour plus d’informations, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).

    À présent, vous avez spécifié la manière dont l’utilisateur reçoit des notifications. Continuez à spécifier lorsque l’utilisateur reçoit des notifications.  

4.  Choisissez l’action **Tableau de notification**.  
5.  Sur la page **Tableau de notification**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Répétition**|Spécifiez la périodicité à laquelle l’utilisateur reçoit des notifications.|  
    |**Heure**|Spécifiez à quelle heure du jour l’utilisateur reçoit les notifications lorsque la valeur du champ **Répétition** est différente de la valeur **Instantané**.|  
    |**Fréquence quotidienne**|Spécifiez quel type de jours l’utilisateur reçoit des notifications lorsque la valeur dans le champ **Répétition** est **Tous les jours**.<br /><br /> Sélectionnez **Jour de la semaine** pour recevoir des notifications chaque jour travaillé de la semaine. Sélectionnez **Tous les jours** pour recevoir des notifications tous les jours, y compris le week-end.|  
    |**Lundi** à **Dimanche**|Spécifiez quel type de jours l’utilisateur reçoit des notifications lorsque la valeur dans le champ **Répétition** est **Chaque semaine**.|  
    |**Date du mois**|Spécifiez si l’utilisateur reçoit des notifications le premier ou le dernier jour du mois, ou à une date spécifique du mois.|  
    |**Date de notification mensuelle**|Spécifiez à quelle date du mois l’utilisateur reçoit des notifications lorsque la valeur dans le champ **Date du mois** est **Personnalisé**.|  

## <a name="change-when-and-how-you-receive-notifications"></a>Modifier le moment et le mode de réception des notifications  
1.  Sur l’une des notifications que vous avez reçue, par e-mail ou par note, sélectionnez le bouton **Modifier les paramètres de notification**.  
2.  Sur la page **Paramètres de notification**, modifiez vos préférences de notification suivant les instructions de la procédure précédente.  

## <a name="see-also"></a>Voir aussi  
 [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md)   
 [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md)   
 [Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)   
 [Paramétrage des workflows](across-set-up-workflows.md)   
 [Utilisation des workflows](across-use-workflows.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]