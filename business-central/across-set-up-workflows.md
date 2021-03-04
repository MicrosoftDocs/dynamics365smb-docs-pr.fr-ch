---
title: Configuration des workflows
description: Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Découvrez les différentes étapes à suivre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/14/2020
ms.author: edupont
ms.openlocfilehash: a104065d8f52ca9d1bb9221cd43917253c640ca4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754249"
---
# <a name="set-up-workflows"></a>Configuration des workflows

Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l’utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow. Pour plus d’informations, voir [Utilisation des workflows](across-use-workflows.md).  

 Avant de commencer à utiliser des workflows, vous devez configurer des utilisateurs de workflow et des utilisateurs approbation, spécifier comment les utilisateurs reçoivent des notifications concernant les étapes de workflow, puis créer les workflows, potentiellement précédés d’une personnalisation de code.  

 Sur la page **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d’événement, et une réponse de workflow modérée par des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d’événement et de réponse qui sont les scénarios pris en charge par le code d’application.  

 Si un scénario d’entreprise requiert un événement ou une réponse de workflow qui n’est pas pris en charge, un partenaire Microsoft doit l’implémenter via le code, ou vous pouvez configurer un workflow avec Power Automate. Pour en savoir plus, voir [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] dans un workflow automatique](across-how-use-financials-data-source-flow.md) ou [Événements dans AL](/dynamics365/business-central/dev-itpro/developer/devenv-events-in-al) dans l’aide du développeur, respectivement.

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|  
|Configurer des utilisateurs de workflows et des groupes d’utilisateurs.|[Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md)|  
|Configurer des utilisateurs de workflow qui participent à des workflow d’approbation.|[Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md)|  
|Spécifier comment les utilisateurs du workflow sont notifiés des étapes du workflow, y compris des demandes d’approbation.|[Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)|  
|Spécifiez si des utilisateurs sont notifiés par e-mail ou note et à quelle fréquence les notifications sont envoyées.|[Spécifier quand et comment recevoir des notifications](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Personnalisez le contenu des e-mails de notification en modifiant l’état 1320, notification par e-mail.|[Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md)|  
|Configurer un serveur SMTP pour activer une communication entrante et sortante de [!INCLUDE[prod_short](includes/prod_short.md)] par e-mail|[Configurer la messagerie](admin-how-setup-email.md)|
|Spécifier les différentes étapes d’un workflow par les événements du workflow de connexion avec des réponses du workflow.|[Créer des workflows](across-how-to-create-workflows.md)|  
|Utiliser des modèles de workflow pour créer des workflows.|[Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md)|  
|Partager des workflows avec d’autres bases de données [!INCLUDE[prod_short](includes/prod_short.md)].|[Exporter et importer des workflows](across-how-to-export-and-import-workflows.md)|  
|Apprendre comment configurer un workflow pour des documents vente avec approbation en suivant la procédure de bout en bout.|[Procédure pas à pas : configuration et utilisation d’un flux d’approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow"></a>Exemple de flux de travail approbation
Cette vidéo montre comment configurer un flux de travail qui exigera qu’une personne demande l’approbation d’une autre personne avant de pouvoir modifier les informations sur un client existant ou de créer un nouveau client.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-also"></a>Voir aussi  
 [Utilisation des workflows](across-use-workflows.md)   
 [Flux de travail](across-workflow.md)   
 [Procédure pas à pas : Configuration et utilisation d’un flux d’approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Utilisation de Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]