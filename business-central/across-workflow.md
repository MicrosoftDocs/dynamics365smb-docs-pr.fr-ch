---
title: Workflow | Microsoft Docs
description: Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/22/2020
ms.author: sgroespe
ms.openlocfilehash: d0c7b95606c5bae844cc2f4d3048bee39467b7a4
ms.sourcegitcommit: 6200a08e91d507bab01d1d5b805fe8ea3f44a58a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/22/2020
ms.locfileid: "3496665"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Flux de travail dans Dynamics 365 Business Central

Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du flux de travail.  

 Sur la page **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d'événement, et une réponse de workflow modérée par des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application.  

 La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut plusieurs workflows préconfigurés, représentés par des modèles de workflow que vous pouvez copier pour créer des workflows. Le code des modèles de workflow ajoutés par Microsoft a le préfixe « MS- ». Pour plus d'informations, voir la liste des modèles de flux de travail sur la page Modèles flux de travail.  

 Si un scénario d'entreprise requiert un événement ou une réponse de flux de travail qui n'est pas pris en charge, vous pouvez utiliser Power Automate ou travailler avec un partenaire Microsoft pour personnaliser le code de l'application. Pour plus d'informations, voir [Utilisation de [!INCLUDE[prodshort](includes/prodshort.md)] dans un flux automatisé](across-how-use-financials-data-source-flow.md).

Tout modèle de flux de travail que vous créez avec Power Automate est ajouté à la liste des modèles de flux de travail dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Utilisation de Business Central dans un flux automatisé](across-how-use-financials-data-source-flow.md).  

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|  
|Configurer des utilisateurs du workflow, spécifier comment les utilisateurs sont notifiés et créer des workflows. Pour de nouveaux workflows pour des scénarios non pris en charge, implémentez les éléments requis du workflow en personnalisant le code d'application.|[Paramétrage des workflows](across-set-up-workflows.md)|  
|Activer des workflows, agir sur les notifications du workflow, notamment les approbations de demandes et approuver des demandes pour effectuer une étape du workflow. Archiver et supprimer des workflows.|[Utilisation des workflows](across-use-workflows.md)|  

## <a name="see-also"></a>Voir aussi

[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Gestion des projets](projects-manage-projects.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
