---
title: Dépanner les flux de travail automatisés
description: Découvrez comment dépanner la connexion entre Business Central et Power Automate lorsque vous créez un flux de travail automatisé.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions, Power Automate,'
ms.date: 08/04/2022
ms.author: edupont
---

# Dépanner les flux de travail automatisés [!INCLUDE[prod_short](includes/prod_short.md)]

Lorsque vous vous connectez [!INCLUDE [prod_short](includes/prod_short.md)] avec Power Automate pour créer des flux de travail automatisés, des messages d’erreur peuvent apparaitre. Cet article fournit des suggestions de solution aux problèmes récurrents.

## Le flux ne s’exécute pas sur tous les enregistrements créés ou modifiés

### Problème

Si un événement crée ou modifie de nombreux enregistrements, le flux ne s’exécute pas sur certains ou sur tous les enregistrements.

### Cause possible

Actuellement, le nombre d’enregistrements traités par un flux est limité. Si plus de 100 enregistrements sont créés ou modifiés en 30 secondes, le flux n’est pas déclenché.

> [!NOTE]
> Pour les développeurs, le déclenchement du flux se fait par les notifications webhook et cette limitation est due à la façon dont le connecteur Business Central gère les notifications `collection`. En savoir plus sur [Utilisation des webhooks dans Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) dans l’aide pour les développeurs et les administrateurs.

## Erreur « Ensemble d’entités introuvable »

### Problème

Lorsque vous créez un flux Power Automate en utilisant un déclencheur d’approbation [!INCLUDE[prod_short](includes/prod_short.md)], comme *Lorsque l’approbation d’un document achat est exigée*, un message d’erreur identique au suivant peut apparaitre :

`Entity set not found: \<name\>`

L’espace réservé `\<name\>` correspond au nom du service Web manquant, comme *workflowWebhookSubscriptions* ou *workflowPurchaseDocumentLines*.

### Cause possible

L’utilisation de Power Automate pour les approbations nécessite que certains objets de page et de codeunit soient publiés en tant que services Web. Par défaut, la plupart des objets requis sont publiés en tant que services Web pour vous. Mais dans certains cas, votre environnement a peut-être été personnalisé pour que ces objets ne soient plus publiés.

### Corriger

Allez à la page **Services Web** et assurez-vous que les objets suivants sont publiés en tant que services Web. Il devrait y avoir une entrée dans la liste pour chaque objet, avec la case **Publié** cochée.  

| Type d’objet | ID d’objet | Nom de l’objet | Nom du service |
|--|--|--|--|
| Codeunit | 1544 | WorkflowWebhookSubscription | WorkflowActionResponse |
| Page | 6408 | workflowCustomers | workflowCustomers |
| Page | 6406 | workflowGenJournalBatches | workflowGenJournalBatches |
| Page | 6407 | workflowGenJournalLines | workflowGenJournalLines |
| Page | 6409 | workflowItems | workflowItems |
| Page | 6405 | Entité de ligne document achat | workflowPurchaseDocumentLines |
| Page | 6404 | workflowPurchaseDocuments | workflowPurchaseDocuments |
| Page | 6403 | Entité de ligne document vente | workflowSalesDocumentLines |
| Page | 6402 | workflowSalesDocuments | workflowSalesDocuments |
| Page | 6410 | workflowVendors | workflowVendors |
| Page | 831 | workflowWebhookSubscriptions | workflowWebhookSubscriptions |

> [!NOTE]
> La valeur **Nom du service** doit être exactement comme indiqué dans le tableau. Ne modifiez ni ne traduisez le nom du service.

Pour plus d’informations sur la publication des services Web, voir [Publier un service Web](across-how-publish-web-service.md).

## Voir la formation associée sur [Microsoft Learn](/learn/modules/use-power-automate/).

## Voir aussi

[Utiliser les flux Power Automate dans [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)  
[Flux de travail](across-workflow.md)  
[Configurer des flux de travail automatisés](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Activer les flux instantanés](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  
[Gérer les flux Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
