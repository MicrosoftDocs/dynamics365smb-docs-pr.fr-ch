---
title: Spécifier quand et comment recevoir des notifications de workflow
description: Lorsque vous configurez des utilisateurs dans des workflows d’approbation, vous pouvez spécifier comment et quand chaque utilisateur d’approbation reçoit des notifications.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 6812fa270066b03fa64a7d8c664ef4df8d28eff0
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102514"
---
# <a name="specify-when-and-how-to-receive-workflow-notifications"></a>Spécifier quand et comment recevoir des notifications de workflow
Lorsque vous configurez des utilisateurs d’approbation dans des workflows où vous souhaitez que quelqu’un approuve les modifications, par exemple lorsque des enregistrements sont créés ou lorsque quelqu’un demande une approbation, vous devez spécifier comment et quand l’utilisateur d’approbation sera averti. Par exemple, vous pouvez spécifier qu’un utilisateur d’approbation recevra immédiatement un e-mail lorsque quelqu’un créera un client. Sinon, vous pouvez programmer les notifications à envoyer, par exemple, sur une base hebdomadaire ou mensuelle.

Les personnes peuvent également modifier leur paramètre de notification en choisissant le bouton **Changer les paramètres de notification** sur toute notification.  

> [!NOTE]
> Les notifications sont envoyées en fonction des paramètres de notification pour le destinataire, et non l’expéditeur. Cette distinction est importante, car cela signifie que lorsqu’un utilisateur demande une approbation dans le cadre d’un flux de travail, sa demande n’est pas nécessairement envoyée immédiatement. Au lieu de cela, elle sera remise selon le calendrier de notification spécifié dans les paramètres de notification de l’approbateur. 

Avant de pouvoir paramétrer des préférences de notification d’un utilisateur approbation, vous devez configurer l’utilisateur en tant qu’utilisateur approbation. Pour plus d’informations, voir [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md).  

Vous pouvez définir la présentation des e-mails de notification en personnalisant l’état 1320, notification par e-mail. Pour plus d’informations, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).  

> [!NOTE]
> Si vous souhaitez utiliser l’e-mail comme méthode de notification, vous devez configurer l’adresse e-mail de l’expéditeur et du destinataire dans [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Configurer l’adresse e-mail](admin-how-setup-email.md).

## <a name="steps-in-workflows"></a>Étapes de workflows 
Pour un grand nombre d’étapes d’approbation du workflow, il s’agit de notifier des utilisateurs qu’un événement s’est produit et qu’ils peuvent agir dessus. Par exemple, sur une étape de workflow, l’événement peut être que l’Utilisateur 1 demande l’approbation d’un nouvel enregistrement. La réponse associée est qu’une notification est envoyée à l’Utilisateur 2, l’approbateur. Sur la prochaine étape de workflow, l’événement peut être que l’Utilisateur 2 approuve l’enregistrement. La réponse associée est qu’une notification est envoyée à l’Utilisateur 3 afin de commencer un processus avec l’enregistrement approuvé. Pour les étapes de workflow concernant des approbations, chaque notification est liée à une écriture d’approbation. Pour plus d’informations, voir [Flux de travail](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Spécifier quand et comment recevoir des notifications  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres utilisateur approbation**, puis choisissez le lien associé.  
2.  Sélectionnez la ligne pour l’utilisateur pour lequel vous souhaitez paramétrer des préférences de notification, puis choisissez l’action **Paramètre de notification**.  
3.  Sur la page **Paramètres de notification**, renseignez les champs comme indiqué dans le tableau suivant.  

    > [!NOTE]
    > Si vous ouvrez la page **Configuration des notifications** de la page **Paramètres utilisateur d’approbation**, la configuration de la notification est liée à l’utilisateur d’approbation. L’utilisateur d’approbation recevra toujours des notifications de workflow en fonction de cette configuration de notification. Si vous utilisez Tell Me pour ouvrir la page **Configuration des notifications**, la configuration de la notification s’appliquera à tous les utilisateurs.  

    |Champ|Description|  
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