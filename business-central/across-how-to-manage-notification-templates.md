---
title: "Procédure : gérer les modèles de notification | Microsoft Docs"
description: "Des notifications sont envoyées aux utilisateurs du workflow pour les informer des étapes à suivre ou du statut des étapes du workflow. Vous configurez qui reçoit des notifications et quand, en définissant des utilisateurs approbation, le calendrier de notification des utilisateurs, et les réponses de workflow concernées afin de déterminer les destinataires de notifications. Pour plus d'informations, reportez-vous à [Configuration de notifications de flux de travail](across-setting-up-workflow-notifications.md)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 31a6cd72e7e7c3fda27803a995b7282c8a2c3751
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="manage-notification-templates"></a>Gérer les modèles de notification
Des notifications sont envoyées aux utilisateurs du workflow pour les informer des étapes à suivre ou du statut des étapes du workflow. Vous configurez qui reçoit des notifications et quand, en définissant des utilisateurs approbation, le calendrier de notification des utilisateurs, et les réponses de workflow concernées afin de déterminer les destinataires de notifications. Pour plus d'informations, reportez-vous à [Configuration de notifications de flux de travail](across-setting-up-workflow-notifications.md).  

 Les notifications sont créés à partir de modèles qui définissent leur contenu et leur mise en forme. Vous pouvez exporter le contenu d'un modèle de notification, le modifier, puis l'importer dans le même modèle de notification ou un nouveau. Ceci est décrit dans les procédures suivantes.  

 La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] contient trois modèles de notification : une pour les demandes d'approbation ; une pour les nouveaux enregistrements ; et une pour les demandes d'approbation échues. Les trois modèles de notification prédéfinis prennent en charge l'**e-mail** et la **note** comme méthode de notification. Pour afficher le contenu des trois modèles de notification, consultez la section « Contenu des modèles de notification » dans cette rubrique.

## <a name="to-create-a-new-notification-template"></a>Créer un modèle de notification  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Modèles de notification**, puis sélectionnez le lien associé.  
2.  Dans la fenêtre **Modèles de notification**, cliquez sur l'action **Nouveau**.  
3.  Renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Identifiez le modèle de notification.|  
    |**Description**|Décrivez le modèle de notification.|  
    |**Mode de notification**|Spécifiez si la notification est envoyée comme un e-mail ou une note.|  
    |**Type**|Spécifiez le processus d'entreprise dont cette notification sera l'objet.<br /><br /> Sélectionnez un des types suivants :<br /><br /> -   **Approbation** spécifie que le modèle est utilisé pour notifier des utilisateurs au sujet de workflows d'approbation.<br />-   **Nouvel enregistrement** spécifie que le modèle est utilisé pour notifier les approbateurs lorsque un nouvel enregistrement, comme une fiche client, a besoin d'être approuvé.<br />-   **Échu** spécifie que le modèle est utilisé pour notifier des utilisateurs au sujet de demandes d'approbation échues.|  
    |**Par défaut**|Spécifiez si le modèle de notification sera utilisé par défaut.|  

## <a name="to-modify-a-notification-template"></a>Modifier un modèle de notification  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Modèles de notification**, puis sélectionnez le lien associé.  
2.  Dans la fenêtre **Modèles de notification**, sélectionnez le modèle de notification que vous souhaitez modifier.  
3.  Choisissez l'action **Exporter le contenu d'un modèle**.  
4.  Dans la fenêtre **Exporter fichier**, choisissez le bouton **Enregistrer**, puis nommez et enregistrez le fichier HTML à l'emplacement approprié.  
5.  Effectuez un clic droit sur le fichier, choisissez **Ouvrir avec**, puis choisissez le programme approprié.  

    > [!NOTE]  
    >  Le contenu des modèles de notification de type e-mail sont au format HTML. Le contenu des modèles de notification de type note sont en format TXT.  
6.  Modifiez le contenu du modèle de notification en ajoutant, modifiant ou supprimant des variables de paramètre afin de définir le contenu souhaité, puis sauvegardez-le. Pour plus d'information, consultez la section « Contenu des modèles de notification ».  

    Continuez pour importer le contenu modifié dans le même modèle de notification ou dans un nouveau.  
7.  Pour modifier le modèle de notification que vous avez exporté, dans la fenêtre **Modèles de notification**, choisissez le modèle sélectionné lors que l'étape 2.  

    Vous pouvez également importer le contenu de modèle modifié dans un nouveau modèle de notification. Pour ce faire, suivez la procédure « Créer un modèle de notification », puis sélectionnez un nouveau modèle de notification.  
8.  Choisissez l'action **Importer le contenu d'un modèle**.  
9. Si vous modifiez un modèle de notification existant, choisissez le bouton **Oui** sur le message qui vous demande de remplacer le modèle existant.  
10. Dans la fenêtre **Sélectionner un fichier à importer**, choisissez le fichier HTML que vous avez modifié au cours de l'étape 6, puis choisissez le bouton **Ouvrir**.  

Le nouveau modèle de notification ou le modèle existant situé dans la fenêtre **Modèles de notification** est désormais mis à jour avec le contenu modifié.  

### <a name="content-of-the-notification-templates"></a>Contenu des modèles de notification  
Les trois types de modèles de notification, **Nouvel enregistrement**, **Approbation** et **Échu**, ont des contenus différents.  

Les valeurs de paramètre sont insérées automatiquement dans les notification selon le type de modèle de notification.  

#### <a name="new-record"></a>Nouvel enregistrement  
 ![NAV&#95;notification&#95;template&#95;new&#95;record&#95;type](media/nav_notification_template_new_record.png "NAV_notification_template_new_record")  

#### <a name="approval"></a>Approbation  
 ![NAV&#95;notification&#95;template&#95;approval&#95;type](media/nav_notification_template_approval_type.png "NAV_notification_template_approval_type")  

#### <a name="overdue"></a>Échu  
 ![NAV&#95;notification&#95;overdue&#95;type](media/nav_notification_overdue_type.png "NAV_notification_overdue_type")  

## <a name="see-also"></a>Voir aussi  
 [Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)   
 [Configurer la messagerie](admin-how-setup-email.md)   
 [Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md)   
 [Configurer des utilisateurs d'approbation](across-how-to-set-up-approval-users.md)   
 [Créer des workflows](across-how-to-create-workflows.md)   
 [Utiliser des files d'attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)   
 [Flux de travail](across-workflow.md)   

