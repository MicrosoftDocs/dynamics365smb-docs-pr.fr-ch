---
title: Paramétrage des workflows | Microsoft Docs
description: Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l’utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cfceeb302c825d32d132d446882e98b7f6b07e27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913953"
---
# <a name="setting-up-workflows"></a>Paramétrage des workflows
Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l’utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow. Pour plus d’informations, voir [Utilisation des workflows](across-use-workflows.md).  

 Avant de commencer à utiliser des workflows, vous devez configurer des utilisateurs de workflow et des utilisateurs approbation, spécifier comment les utilisateurs reçoivent des notifications concernant les étapes de workflow, puis créer les workflows, potentiellement précédés d’une personnalisation de code.  

 Sur la page **Workflow** , créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d’événement, et une réponse de workflow modérée par des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d’événement et de réponse qui sont les scénarios pris en charge par le code d’application.  

 Si un scénario d’entreprise requiert un événement ou une réponse de workflow qui n’est pas pris en charge, un partenaire Microsoft doit l’implémenter en personnalisant le code de l’application. Pour plus d’informations, voir [Procédure pas à pas : implémentation de nouveaux événements et réponses de flux de travail](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) dans l’Aide destinée aux développeurs et aux professionnels de l’informatique.

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|  
|Configurer des utilisateurs de workflows et des groupes d’utilisateurs.|[Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md)|  
|Configurer des utilisateurs de workflow qui participent à des workflow d’approbation.|[Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md)|  
|Spécifier comment les utilisateurs du workflow sont notifiés des étapes du workflow, y compris des demandes d’approbation.|[Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)|  
|Spécifiez si des utilisateurs sont notifiés par e-mail ou note et à quelle fréquence les notifications sont envoyées.|[Spécifier quand et comment recevoir des notifications](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Personnalisez le contenu des e-mails de notification en modifiant l’état 1320, notification par e-mail.|[Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md)|  
|Configurer un serveur SMTP pour activer une communication entrante et sortante de [!INCLUDE[d365fin](includes/d365fin_md.md)] par e-mail|[Configurer la messagerie](admin-how-setup-email.md)|
|Spécifier les différentes étapes d’un workflow par les événements du workflow de connexion avec des réponses du workflow.|[Créer des workflows](across-how-to-create-workflows.md)|  
|Utiliser des modèles de workflow pour créer des workflows.|[Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md)|  
|Partager des workflows avec d’autres bases de données [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Exporter et importer des workflows](across-how-to-export-and-import-workflows.md)|  
|Apprendre comment configurer un workflow pour des documents vente avec approbation en suivant la procédure de bout en bout.|[Procédure pas à pas : Configuration et utilisation d’un flux d’approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Ajouter la prise en charge d’un scénario d’entreprise qui requiert de nouveaux événements ou réponses de workflow en personnalisant le code de l’application.|[Procédure pas à pas : implémentation de nouveaux événements et réponses de flux de travail](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="example-of-an-approval-workflow"></a>Exemple de flux de travail approbation
Cette vidéo montre comment configurer un flux de travail qui exigera qu’une personne demande l’approbation d’une autre personne avant de pouvoir modifier les informations sur un client existant ou de créer un nouveau client.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-also"></a>Voir aussi  
 [Utilisation des workflows](across-use-workflows.md)   
 [Flux de travail](across-workflow.md)   
 [Procédure pas à pas : Configuration et utilisation d’un flux d’approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Utilisation de Business Central](ui-work-product.md)
