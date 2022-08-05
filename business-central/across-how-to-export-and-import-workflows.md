---
title: 'Procédure : exporter et importer des flux de travail | Microsoft Docs'
description: Pour transférer des flux de travail vers d’autres bases de données Business Central, par exemple pour gagner du temps lors de la création de flux de travail, vous pouvez exporter et importer des flux de travail.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1a52d4b4bff0f96023b6206e6cb8cad3d9e59276
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129945"
---
# <a name="export-and-import-workflows"></a>Exporter et importer des flux de travail

Pour transférer des flux de travail vers d’autres bases de données [!INCLUDE[prod_short](includes/prod_short.md)], par exemple pour gagner du temps lors de la création de flux de travail, vous pouvez exporter et importer des flux de travail.  

Un autre moyen rapide de créer des flux de travail consiste à les créer à partir de modèles de flux de travail. Pour plus d’informations, reportez-vous à la rubrique [Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md).  

Sur la page **Flux de travail**, créez un flux de travail en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de flux de travail modéré par des conditions d’événement, et une réponse de flux de travail modérée par des options de réponse. Définissez les étapes de flux de travail en renseignez les champs des lignes de flux de travail à partir de listes fixes de valeurs d’événement et de réponse qui sont les scénarios pris en charge par le code d’application. Pour plus d’informations, voir [Créer des flux de travail](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Pour exporter un flux de travail

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Flux de travail**, puis choisissez le lien associé.  
2. Sélectionnez un flux de travail, puis sélectionnez l’action **Exporter vers un fichier**.  

## <a name="to-import-a-workflow"></a>Pour importer un flux de travail

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Flux de travail**, puis choisissez le lien associé.  
2. Choisissez l’action **Importer à partir d’un fichier**.  
3. Sur la page **Importer**, cliquez sur le bouton **Choisir**, sélectionnez le fichier XML contenant le flux de travail, puis choisissez le bouton **Ouvrir** .  

> [!CAUTION]  
> Si le code du flux de travail existe déjà dans la base de données, les étapes du flux de travail sont remplacées par celles du flux de travail importé.  

## <a name="see-also"></a>Voir aussi

[Créer des flux de travail](across-how-to-create-workflows.md)  
[Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md)  
[Afficher des instances d’étape de flux de travail archivées](across-how-to-view-archived-workflow-step-instances.md)  
[Supprimer des flux de travail](across-how-to-delete-workflows.md)  
[Procédure pas à pas : Configuration et utilisation d’un flux d’approbation d’achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Paramétrage des flux de travail](across-set-up-workflows.md)  
[Utiliser des flux de travail](across-use-workflows.md)  
[Flux de travail](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]