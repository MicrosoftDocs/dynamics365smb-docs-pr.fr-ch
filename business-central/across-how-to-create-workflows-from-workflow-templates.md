---
title: 'Procédure : créer des flux de travail à partir de modèles de flux de travail | Microsoft Docs'
description: Pour gagner du temps lors de la création de workflows, vous pouvez créer des workflows à partir de modèles de workflow existants.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b2ee2dcba364f7b89bae49c3f15f098c51d2c5a3
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913562"
---
# <a name="create-workflows-from-workflow-templates"></a>Créer des flux de travail à partir de modèles de flux de travail
Pour gagner du temps lors de la création de workflows, vous pouvez créer des workflows à partir de modèles de workflow existants.  

 Les modèles de workflow sont des workflows non modifiables qui existent dans la version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Les codes des modèles de workflow ajoutés par Microsoft ont le préfixe « MS- ».  

 Un autre moyen rapide de créer un workflow consiste à importer un workflow existant qui est stocké dans un fichier en dehors de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d’informations, voir [Exporter et importer des flux de travail](across-how-to-export-and-import-workflows.md).  

Sur la page **Workflow** , créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d’événement, et une réponse de workflow modérée par des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d’événement et de réponse qui sont les scénarios pris en charge par le code d’application. Pour plus d’informations, voir [Créer des flux de travail](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Pour créer un workflow à partir d’un modèle de workflow  
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Flux de travail** , puis sélectionnez le lien associé.  
2.  Choisissez l’action **Créer le flux de travail à partir du modèle** . La page **Modèles flux de travail** s’ouvre.  
3.  Sélectionnez un modèle de workflow et cliquez sur le bouton **OK** .  

     La page **Flux de travail** s’ouvre pour un nouveau flux de travail contenant toutes les informations du modèle sélectionné. La valeur du champ **Code** est étendue avec « -01 », par exemple, pour indiquer que ce premier workflow est créé à partir du modèle de workflow.  
4.  Créez ensuite le workflow en modifiant les étapes de workflow ou en ajoutant de nouvelles étapes. Pour plus d’informations, voir [Créer des flux de travail](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Voir aussi  
 [Créer des workflows](across-how-to-create-workflows.md)   
 [Exporter et importer des workflows](across-how-to-export-and-import-workflows.md)   
 [Afficher des instances d’étape de workflow archivées](across-how-to-view-archived-workflow-step-instances.md)   
 [Supprimer des workflows](across-how-to-delete-workflows.md)   
 [Procédure pas à pas : Configuration et utilisation d’un flux d’approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Paramétrage des workflows](across-set-up-workflows.md)   
 [Utilisation des workflows](across-use-workflows.md)   
 [Flux de travail](across-workflow.md)   
