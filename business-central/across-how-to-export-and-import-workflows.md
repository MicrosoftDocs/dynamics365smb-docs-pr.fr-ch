---
title: 'Procédure : exporter et importer des flux de travail | Microsoft Docs'
description: Pour transférer des workflows vers d’autres bases de données Business Central, par exemple pour gagner du temps lors de la création de workflows, vous pouvez exporter et importer des workflows.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fc49fd08099823a3ab1adc02a006820fb4898e90
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438347"
---
# <a name="export-and-import-workflows"></a>Exporter et importer des workflows
Pour transférer des workflows vers d’autres bases de données [!INCLUDE[prod_short](includes/prod_short.md)], par exemple pour gagner du temps lors de la création de workflows, vous pouvez exporter et importer des workflows.  

 Un autre moyen rapide de créer des workflows consiste à les créer à partir de modèles de workflow. Pour plus d’informations, reportez-vous à la rubrique [Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md).  

 Sur la page **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d’événement, et une réponse de workflow modérée par des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d’événement et de réponse qui sont les scénarios pris en charge par le code d’application. Pour plus d’informations, voir [Créer des flux de travail](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Pour exporter un workflow  
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Flux de travail**, puis choisissez le lien associé.  
2.  Sélectionnez un flux de travail, puis sélectionnez l’action **Exporter vers un fichier**.  
3.  Sur la page **Exporter fichier**, cliquez sur le bouton **Enregistrer**.  
4.  Sur la page **Exporter**, sélectionnez un emplacement de fichier, puis choisissez le bouton **Enregistrer**.  

## <a name="to-import-a-workflow"></a>Pour importer un workflow  
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Flux de travail**, puis choisissez le lien associé.  
2.  Choisissez l’action **Importer à partir d’un fichier**.  
3.  Sur la page **Importer**, sélectionnez le fichier XML contenant le flux de travail, puis choisissez le bouton **Ouvrir**.  

> [!CAUTION]  
>  Si le code du workflow existe déjà dans la base de données, les étapes du workflow sont remplacées avec celles du workflow importé.  

## <a name="see-also"></a>Voir aussi  
 [Créer des workflows](across-how-to-create-workflows.md)   
 [Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md)   
 [Afficher des instances d’étape de workflow archivées](across-how-to-view-archived-workflow-step-instances.md)   
 [Supprimer des workflows](across-how-to-delete-workflows.md)   
 [Procédure pas à pas : Configuration et utilisation d’un flux d’approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Paramétrage des workflows](across-set-up-workflows.md)   
 [Utilisation des workflows](across-use-workflows.md)   
 [Flux de travail](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]