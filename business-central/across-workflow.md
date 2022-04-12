---
title: Flux de travail dans Dynamic 365 Business Central
description: Utilisez les flux de travail qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches système, telles que la comptabilisation automatique, peuvent être incluses en tant qu’étapes de flux de travail.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 9cfdcc9bbf8e24675c6894b8ca2efbf10129d990
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511196"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Flux de travail dans Dynamics 365 Business Central

Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l’utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du flux de travail.  

 Sur la page **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d’événement, et une réponse de workflow modérée par des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d’événement et de réponse qui sont les scénarios pris en charge par le code d’application.  

 La version générique de [!INCLUDE[prod_short](includes/prod_short.md)] inclut plusieurs workflows préconfigurés, représentés par des modèles de workflow que vous pouvez copier pour créer des workflows. Le code des modèles de workflow ajoutés par Microsoft a le préfixe « MS- ». Pour plus d’informations, voir la liste des modèles de flux de travail sur la page Modèles flux de travail.  

 Si un scénario d’entreprise requiert un événement ou une réponse de flux de travail qui n’est pas pris en charge, vous pouvez utiliser Power Automate ou travailler avec un partenaire Microsoft pour personnaliser le code de l’application. Pour plus d’informations, voir [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] dans un flux automatisé](across-how-use-financials-data-source-flow.md).

Tout modèle de flux de travail que vous créez avec Power Automate est ajouté à la liste des modèles de flux de travail dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Utiliser Business Central dans un flux automatisé](across-how-use-financials-data-source-flow.md).  

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|  
|Configurer des utilisateurs du workflow, spécifier comment les utilisateurs sont notifiés et créer des workflows. Pour de nouveaux workflows pour des scénarios non pris en charge, implémentez les éléments requis du workflow en personnalisant le code d’application.|[Paramétrage des workflows](across-set-up-workflows.md)|  
|Activer des workflows, agir sur les notifications du workflow, notamment les approbations de demandes et approuver des demandes pour effectuer une étape du workflow. Archiver et supprimer des workflows.|[Utiliser des workflows](across-use-workflows.md)|  

## <a name="see-also"></a>Voir aussi

[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Gestion des projets](projects-manage-projects.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]