---
title: "Paramétrage des workflows | Microsoft Docs"
description: "Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/20/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e6e662ee13db1f9002e1c3e74a0d15e2aa2e2a98
ms.openlocfilehash: d837fb0b85f3b62c82fb63596e1299ffdd252b23
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-workflows"></a>Paramétrage des workflows
Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow. Pour plus d'informations, voir [Utilisation des workflows](across-use-workflows.md).  

 Avant de commencer à utiliser des workflows, vous devez configurer des utilisateurs de workflow et des utilisateurs approbation, spécifier comment les utilisateurs reçoivent des notifications concernant les étapes de workflow, puis créer les workflows, potentiellement précédés d'une personnalisation de code.  

 Dans la fenêtre **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d'événement, et une réponse de workflow modérée par des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application.  

 Si un scénario d'entreprise requiert un événement ou une réponse de workflow qui n'est pas pris en charge, un partenaire Microsoft doit l'implémenter en personnalisant le code de l'application. Pour plus d'informations, voir [Procédure pas à pas : implémentation de nouveaux événements et réponses de flux de travail](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) dans l'Aide destinée aux développeurs et aux professionnels de l'informatique.

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|  
|Configurer des utilisateurs de workflows et des groupes d'utilisateurs.|[Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md)|  
|Configurer des utilisateurs de workflow qui participent à des workflow d'approbation.|[Configurer des utilisateurs d'approbation](across-how-to-set-up-approval-users.md)|  
|Spécifier comment les utilisateurs du workflow sont notifiés des étapes du workflow, y compris des demandes d'approbation.|[Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)|  
|Spécifier quand des utilisateurs reçoivent des notifications et s'il faut regrouper les notifications au cours d'une période afin de réduire le nombre de notifications.|[Spécifier quand et comment recevoir des notifications](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Configurer la mise en forme et le contenu général de nouveaux e\-mails de notifications du flux de travail, ou exporter, modifier, puis réimporter des modèles existants.|[Gérer les modèles de notification](across-how-to-manage-notification-templates.md)|  
|Configurer un serveur SMTP pour activer une communication entrante et sortante de [!INCLUDE[d365fin](includes/d365fin_md.md)] par e-mail|[Configurer la messagerie](madeira-how-setup-email.md)|
|Spécifier les différentes étapes d'un workflow par les événements du workflow de connexion avec des réponses du workflow.|[Créer des workflows](across-how-to-create-workflows.md)|  
|Utiliser des modèles de workflow pour créer des workflows.|[Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md)|  
|Partager des workflows avec d'autres bases de données [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Exporter et importer des workflows](across-how-to-export-and-import-workflows.md)|  
|Apprendre comment configurer un workflow pour des documents vente avec approbation en suivant la procédure de bout en bout.|[Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Ajouter la prise en charge d'un scénario d'entreprise qui requiert de nouveaux événements ou réponses de workflow en personnalisant le code de l'application.|[Procédure pas à pas : implémentation de nouveaux événements et réponses de flux de travail](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="see-also"></a>Voir aussi  
 [Utilisation des workflows](across-use-workflows.md)   
 [Flux de travail](across-workflow.md)   
 [Procédure pas à pas : configuration et utilisation d'un flux d'approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Utilisation de Financials](ui-work-product.md)

