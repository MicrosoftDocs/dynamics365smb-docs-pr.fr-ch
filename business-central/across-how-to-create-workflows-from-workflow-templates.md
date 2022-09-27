---
title: 'Procédure : créer des flux de travail à partir de modèles de flux de travail'
description: Pour gagner du temps lors de la création de nouveaux flux de travail, vous pouvez créer des flux de travail non modifiables à partir de modèles de flux de travail avec pour préfixe « MS- ».
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 988e3ad6185e06bbe82f21005e64ad9bada051a5
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9535009"
---
# <a name="create-workflows-from-workflow-templates"></a>Créer des flux de travail à partir de modèles de flux de travail

Pour gagner du temps lors de la création de flux de travail, vous pouvez créer des flux de travail à partir de modèles de flux de travail existants.  

Les modèles de flux de travail sont des flux de travail non modifiables qui existent dans la version par défaut de [!INCLUDE[prod_short](includes/prod_short.md)]. Les codes des modèles de flux de travail créés par Microsoft ont le préfixe « MS- ».  

Un autre moyen rapide de créer un flux de travail consiste à importer un flux de travail existant qui est stocké dans un fichier en dehors de [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Exporter et importer des flux de travail](across-how-to-export-and-import-workflows.md).  

Sur la page **Flux de travail**, créez un flux de travail en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de flux de travail modéré par des conditions d’événement, et une réponse de flux de travail modérée par des options de réponse. Définissez les étapes de flux de travail en renseignez les champs des lignes de flux de travail à partir de listes fixes de valeurs d’événement et de réponse qui sont les scénarios pris en charge par le code d’application. Pour plus d’informations, voir [Créer des flux de travail](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template"></a>Pour créer un flux de travail à partir d’un modèle de flux de travail

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Flux de travail**, puis choisissez le lien associé.  
2. Choisissez l’action **Créer flux de travail à partir du modèle**. La page **Modèles flux de travail** s’ouvre.  
3. Sélectionnez un modèle de flux de travail et cliquez sur le bouton **OK**.  

   La page **Flux de travail** s’ouvre pour un nouveau flux de travail contenant toutes les informations du modèle sélectionné. La valeur du champ **Code** est étendue avec « -01 », par exemple, « -01 » pour indiquer que ce premier flux de travail est créé à partir du modèle de flux de travail.  
4. Créez ensuite le flux de travail en modifiant les étapes de flux de travail ou en ajoutant de nouvelles étapes. Pour plus d’informations, voir [Créer des flux de travail](across-how-to-create-workflows.md).  

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/create-workflows/) associée

## <a name="see-also"></a>Voir aussi

[Créer des flux de travail](across-how-to-create-workflows.md)  
[Exporter et importer des flux de travail](across-how-to-export-and-import-workflows.md)  
[Afficher des instances d’étape de flux de travail archivées](across-how-to-view-archived-workflow-step-instances.md)  
[Supprimer des flux de travail](across-how-to-delete-workflows.md)  
[Procédure pas à pas : Configuration et utilisation d’un flux d’approbation d’achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Paramétrage des flux de travail](across-set-up-workflows.md)  
[Utiliser des flux de travail](across-use-workflows.md)  
[Flux de travail](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
