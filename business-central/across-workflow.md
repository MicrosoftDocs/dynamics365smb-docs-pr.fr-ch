---
title: Flux de travail dans Dynamics 365 Business Central
description: Utilisez les fonctionnalités de flux de travail intégrées pour configurer des flux de travail approbation afin de compléter les flux de travail automatisés basés sur Power Automate. Vous pouvez configurer des étapes pour affecter des tâches à différentes personnes dans le cadre des différentes tâches de processus métier.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: ecaaf9bbb56e1c1b47f9f617319b32f32a2920fd
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585637"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Flux de travail dans Dynamics 365 Business Central

Vous pouvez configurer et utiliser des flux de travail qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du flux de travail, précédées ou suivies des tâches de l’utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow.

La version par défaut de [!INCLUDE [prod_short](includes/prod_short.md)] prend en charge 3 types de flux de travail :

* Les flux de travail approbation basés sur des modèles de flux de travail intégrés

  Dans la page **Modèles flux de travail**, vous affichez tous les flux de travail disponibles. La version d’essai de [!INCLUDE[prod_short](includes/prod_short.md)] inclut plusieurs flux de travail préconfigurés, représentés par des modèles de flux de travail que vous pouvez copier pour créer des flux de travail. Lorsque vous ouvrez un modèle de flux de travail depuis la page **Modèles flux de travail** et que le nom du flux de travail commence par *MS-*, le modèle de flux de travail est ajouté par Microsoft.
  
* Les flux Power Automate que vous configurez vous-même

  Tout modèle de flux de travail que vous créez avec Microsoft Power Automate est ajouté à la liste des modèles de flux de travail dans [!INCLUDE[prod_short](includes/prod_short.md)]. En savoir plus sur [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] dans des flux Power Automate](across-how-use-financials-data-source-flow.md). 
  
* Flux instantanés déclenchés manuellement à partir de l’action **Automatiser** ([!INCLUDE [prod_short](includes/prod_short.md)] en ligne uniquement).

  Créez et déclenchez manuellement un flux Power Automate sur un enregistrement [!INCLUDE[prod_short](includes/prod_short.md)], tel qu’un client, un article ou une commande client, avec des options pour manipuler les informations à la fois en interne et en externe (à l’aide d’outils intégrés). Consultez la section [Flux instantanés](across-how-use-financials-data-source-flow.md#instant-flows).

## <a name="power-automate-flows"></a>Flux Power Automate

Avec [!INCLUDE [prod_short](includes/prod_short.md)] en ligne, vous pouvez vous inscrire à Power Automate pour créer de puissants flux de travail automatisés. Vous pouvez exécuter ces flux de travail dans [!INCLUDE [prod_short](includes/prod_short.md)], en connectant les sources de données internes et externes et les outils, sans connaissances en matière de codage.

Les flux Power Automate peuvent être déclenchés par des événements (tels que la création, la modification ou la suppression d’un enregistrement ou d’un document) et exécutés selon un calendrier défini par l’utilisateur ou à la demande (appelé **Flux instantané**).

## <a name="approval-workflows"></a>Flux de travail d’approbation

Créez un flux de travail approbation en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de flux de travail modéré par des conditions d’événement, et une réponse de flux de travail modérée par des options de réponse. Définissez les étapes de flux de travail en renseignez les champs des lignes de flux de travail à partir de listes fixes de valeurs d’événement et de réponse qui sont les scénarios pris en charge par le code d’application.<!--What are the "values"? Can we give an example?-->

Les exemples d’événements de flux de travail approbation incluent, entre autres, la création de bons de commande/devis/factures, les modifications de prix et les modifications de fournisseur ou de client.

[!INCLUDE[workflow](includes/workflow.md)]

| **Pour** | **Voir** |
|--|--|
| Configurer des utilisateurs du flux de travail approbation, spécifier comment les utilisateurs sont notifiés et créer des flux de travail. (Pour de nouveaux flux de travail pour des scénarios non pris en charge, implémentez les éléments requis du flux de travail en personnalisant le code d’application.) | [Configurer les flux de travail approbation](across-set-up-workflows.md) |
| Activer des flux de travail approbation, agir sur les notifications du flux de travail, notamment la demande et l’approbation d’une étape de flux de travail. Archiver et supprimer des workflows. | [Utilisation des flux d’approbation](across-use-workflows.md) |
| Intégrez les données de l’entreprise avec les flux de travail Power Automate, en utilisant à la fois des sources internes et externes et des événements pour créer et automatiser des tâches ou des flux de travail. | [Utiliser les flux Power Automate dans [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/create-workflows/) associée

## <a name="see-also"></a>Voir aussi

[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Gestion des projets](projects-manage-projects.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Dépanner les flux de travail automatisés [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
