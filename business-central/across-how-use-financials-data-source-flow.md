---
title: Utiliser Business Central dans les flux Power Automate
description: Configurer et utiliser les flux Power Automate qui créent ou modifient les données Business Central.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: f1128a9fb4e9643286e4305695e1d40719d86301
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079339"
---
# <a name="use-prod_short-in-power-automate-flows"></a>Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] dans les flux Power Automate

Vous pouvez utiliser vos données [!INCLUDE[prod_short](includes/prod_short.md)] en tant que partie du flux de travail dans Microsoft Power Automate. Créez vos propres flux et connectez-vous à vos données avec le connecteur [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Vous devez disposer d’un compte valide avec [!INCLUDE[prod_short](includes/prod_short.md)] et avec Power Automate.  

> [!TIP]
> Outre Power Automate, vous pouvez utiliser les modèles de flux de travail approbation dans [!INCLUDE[prod_short](includes/prod_short.md)]. Bien qu’il existe deux systèmes de flux de travail distincts, tous les modèles de flux de travail approbation que vous créez dans Power Automate sont ajoutés à la liste des flux de travail dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Flux de travail](across-workflow.md).  

## <a name="automated-workflows"></a>Flux de travail automatisés

Avec Power Automate, vous pouvez créer des flux métiers directement en interne et vous appuyer sur des développeurs citoyens. Pour plus d’informations, voir [Configurer des flux de travail automatisés](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) dans le contenu d’administration.  

## <a name="manual-instant-flows"></a>Flux instantanés manuels

À compter de mai 2022, un administrateur de [!INCLUDE [prod_short](includes/prod_short.md)] en ligne peut [activer une fonctionnalité](admin-feature-management.md) pour permettre d’exécuter un flux Power Automate de la plupart des pages. Pour plus d’informations, voir [Configurer des flux de travail automatisés](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) dans le contenu d’administration.  

Une fois l’administrateur connecté à [!INCLUDE [prod_short](includes/prod_short.md)] avec Power Automate, vous affichez tous les flux ajoutés par votre organisation lorsque vous sélectionnez l’action **Automatiser** dans les pages concernées. Exécutez les flux sans quitter [!INCLUDE [prod_short](includes/prod_short.md)].  

Ces flux de travail automatisés s’ouvrent dans un volet à l’intérieur de [!INCLUDE [prod_short](includes/prod_short.md)] en ligne afin que vous restiez dans le contexte du processus métier dans lequel vous vous trouviez. Dans certaines pages, l’action **Automatiser** se cache sous le menu **Plus d’options**, trouvez-la, sélectionnez l’élément de menu **Power Automate**, puis sélectionnez le lien approprié pour déclencher le flux de travail. La connexion à Power Automate est déjà configurée pour vous.  

La plupart des flux vous demandent de remplir un champ ou deux avant de sélectionner l’action **Exécuter le flux**.  

> [!TIP]
> Si vous n’affichez pas l’action **Automatiser**, il est possible que [!INCLUDE [prod_short](includes/prod_short.md)] ne soit pas encore configuré pour utiliser Power Automate. Pour plus d’informations, demandez à votre administrateur.

## <a name="add-more-automated-flows-and-manual-instant-flows"></a>Ajouter plus de flux automatisés et de flux instantanés manuels

Vous pouvez créer des flux sur le site Web [powerautomate.microsoft.com](https://powerautomate.microsoft.com). Toutefois, si votre administrateur a activé la possibilité d’exécuter des flux Power Automate à partir de [!INCLUDE [prod_short](includes/prod_short.md)] en ligne, vous pouvez démarrer la création d’un flux à partir de l’action **Automatiser** sur les pages concernées. Dans certaines pages, l’action **Automatiser** se cache sous le menu **Plus d’options**, trouvez-la, sélectionnez l’élément de menu **Power Automate**, puis sélectionnez l’action **Créer un flux**. Power Automate s’ouvre alors dans un nouvel onglet du navigateur et vous êtes automatiquement connecté.

## <a name="manage-workflows"></a>Gérer les flux de travail

Vous pouvez obtenir un aperçu de tous les flux de travail auxquels vous avez accès en sélectionnant l’action **Gérer les flux de travail** dans le menu **Power Automate**. La liste s’ouvre dans un nouvel onglet du navigateur et vous êtes automatiquement connecté à Power Automate. Là, vous affichez la date de dernière exécution pour chaque flux.  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/use-power-automate/)

## <a name="see-also"></a>Voir aussi

[Dépanner les flux de travail automatisés [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  
[Se préparer aux activités commerciales](ui-get-ready-business.md)  
[Flux de travail](across-workflow.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  
[Configurer [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finances](finance.md)  
[Configurer des flux de travail automatisés](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]