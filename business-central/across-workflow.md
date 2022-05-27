---
title: Flux de travail dans Dynamic 365 Business Central
description: Utilisez les fonctionnalités de flux de travail intégrées pour configurer des flux de travail approbation afin de compléter les flux de travail automatisés basés sur Power Automate. Vous pouvez configurer des étapes pour affecter des tâches à différentes personnes dans le cadre des différentes tâches de processus métier.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/12/2022
ms.author: edupont
ms.openlocfilehash: 84d4a87a0edab18be342b9ed5732de0350a31645
ms.sourcegitcommit: bc645e7ecb1940a85b2c433aa894d3494c9b10df
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743686"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Flux de travail dans Dynamics 365 Business Central

Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l’utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow.  

La version par défaut de [!INCLUDE [prod_short](includes/prod_short.md)] prend en charge 3 types de flux de travail :

* Les flux de travail approbation automatisés basés sur des modèles de flux de travail intégrés  

  Dans la page **Modèles flux de travail**, vous affichez tous les flux de travail disponibles. La version d’essai de [!INCLUDE[prod_short](includes/prod_short.md)] inclut plusieurs flux de travail préconfigurés, représentés par des modèles de flux de travail que vous pouvez copier pour créer des flux de travail. Lorsque vous ouvrez un modèle de flux de travail depuis la page **Modèles flux de travail** et que le nom du flux de travail commence par *MS-*, le modèle de flux de travail est ajouté par Microsoft.  
* Les flux automatisés que vous configurez vous-même  

  Tout modèle de flux de travail que vous créez avec Power Automate est ajouté à la liste des modèles de flux de travail dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Utiliser Business Central dans les flux Power Automate](across-how-use-financials-data-source-flow.md).  
* Flux déclenchés manuellement à partir de l’action **Automatiser** ([!INCLUDE [prod_short](includes/prod_short.md)] en ligne uniquement). Pour plus d’informations, voir [Flux instantanés manuels](across-how-use-financials-data-source-flow.md#manual-instant-flows).  

## <a name="power-automate-flows"></a>Flux Power Automate

Pour [!INCLUDE [prod_short](includes/prod_short.md)] en ligne, vous pouvez vous inscrire à Power Automate et créer de puissants flux automatisés exécutables dans [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] dans les flux Power Automate](across-how-use-financials-data-source-flow.md).  

## <a name="automated-approval-workflows"></a>Les flux de travail approbation automatisés

Créez un flux de travail approbation en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d’événement, et une réponse de workflow modérée par des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d’événement et de réponse qui sont les scénarios pris en charge par le code d’application.  

Si un scénario métier nécessite un événement de flux de travail ou une réponse qui n’est pas pris(e) en charge dans la version par défaut, inscrivez-vous à Power Automate. Pour plus d’informations, voir [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] dans les flux Power Automate](across-how-use-financials-data-source-flow.md). Sinon, obtenez une application ou collaborez avec un partenaire Microsoft pour personnaliser le code de l’application.  

Pour configurer et utiliser des flux de travail qui ne sont pas définis dans Power Automate, consultez les articles suivants :  

|**Pour**|**Voir**|  
|------------|-------------|  
|Configurer des utilisateurs du workflow, spécifier comment les utilisateurs sont notifiés et créer des workflows. Pour de nouveaux workflows pour des scénarios non pris en charge, implémentez les éléments requis du workflow en personnalisant le code d’application.|[Configuration des workflows](across-set-up-workflows.md)|  
|Activer des workflows, agir sur les notifications du workflow, notamment les approbations de demandes et approuver des demandes pour effectuer une étape du workflow. Archiver et supprimer des workflows.|[Utiliser des workflows](across-use-workflows.md)|  

## <a name="see-also"></a>Voir aussi

[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Gestion des projets](projects-manage-projects.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] dans les flux Power Automate](across-how-use-financials-data-source-flow.md)  
[Dépanner les flux de travail automatisés [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]