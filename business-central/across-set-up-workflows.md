---
title: Configuration des workflows (contient une vidéo)
description: Configurez des flux de travail, des utilisateurs de flux de travail et des utilisateurs d’approbation pour connecter les tâches du système de processus métier effectuées par ces différents utilisateurs.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 7676e05255c31bd2b9906951d98d1a87622a0fcf
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530286"
---
# <a name="set-up-workflows"></a>Configuration des workflows

Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du flux de travail, précédées ou suivies des tâches de l’utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow. Pour plus d’informations, voir [Utiliser des workflows](across-use-workflows.md).  

Avant de commencer à utiliser des workflows, vous devez configurer des utilisateurs de workflow et des utilisateurs d'approbation, spécifier comment les utilisateurs reçoivent des notifications concernant les étapes de workflow, puis créer les workflows.  

Sur la page **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de flux de travail modéré par des conditions d’événement, et une réponse de flux de travail modérée par des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d’événement et de réponse qui sont les scénarios pris en charge par le code d’application.  

[!INCLUDE[workflow](includes/workflow.md)]

Le tableau suivant décrit une série de tâches et inclut des liens vers les articles qui les décrivent.  

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
|Apprendre comment configurer un workflow pour des documents vente avec approbation en suivant la procédure de bout en bout.|[Procédure pas à pas : Configuration et utilisation d’un flux d’approbation d’achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow"></a>Exemple de flux de travail approbation

Cette vidéo montre comment configurer un flux de travail qui exigera qu’un utilisateur demande l’approbation d’une autre personne avant de pouvoir modifier les informations sur un client existant ou de créer un nouveau client.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/create-workflows/) associée

## <a name="see-also"></a>Voir aussi

[Utiliser des flux de travail](across-use-workflows.md)  
[Flux de travail](across-workflow.md)  
[Procédure pas à pas : Configuration et utilisation d’un flux d’approbation d’achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Utiliser Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
