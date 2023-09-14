---
title: "Procédure\_: exporter et importer des flux de travail approbation"
description: "Pour transférer des flux de travail vers d’autres bases de données Business\_Central, par exemple pour gagner du temps lors de la création de flux de travail, vous pouvez exporter et importer des flux de travail."
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
---
# <a name="export-and-import-approval-workflows"></a>Exporter et importer des flux de travail approbation

Pour transférer des flux de travail vers d’autres bases de données [!INCLUDE[prod_short](includes/prod_short.md)], par exemple pour gagner du temps lors de la création de flux de travail, vous pouvez exporter et importer des flux de travail.  

Un autre moyen rapide de créer des flux de travail consiste à les utiliser à partir de modèles de flux de travail. En savoir plus sur [Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md).  

Sur la page **Flux de travail**, créez un flux de travail en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de flux de travail modéré par des conditions d’événement, et une réponse de flux de travail modérée par des options de réponse. Définissez les étapes de flux de travail en renseignez les champs des lignes de flux de travail à partir de listes fixes de valeurs d’événement et de réponse qui sont les scénarios pris en charge par le code d’application. En savoir plus sur [Créer des flux de projet](across-how-to-create-workflows.md).  

## <a name="export-a-workflow"></a>Exporter un flux de travail

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Flux de travail**, puis choisissez le lien associé.  
2. Sélectionnez un flux de travail, puis sélectionnez l’action **Exporter vers un fichier**.  

## <a name="import-a-workflow"></a>Importer un flux de travail

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Flux de travail**, puis choisissez le lien associé.  
2. Choisissez l’action **Importer à partir d’un fichier**.  
3. Sur la page **Importer**, sélectionnez **Choisir**, choisissez le fichier XML contenant le flux de travail, puis sélectionnez **Ouvrir**.  

> [!CAUTION]  
> Si le code du flux de travail existe déjà dans la base de données, les étapes du flux de travail sont remplacées par celles du flux de travail importé.  

## <a name="see-also"></a>Voir aussi

[Créer des flux de travail approbation](across-how-to-create-workflows.md)  
[Créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md)  
[Afficher des instances d’étape de flux de travail archivées](across-how-to-view-archived-workflow-step-instances.md)  
[Suppression des flux d’approbation](across-how-to-delete-workflows.md)  
[Procédure pas à pas : Configuration et utilisation d’un flux d’approbation d’achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Configurer les flux de travail approbation](across-set-up-workflows.md)  
[Utilisation des flux d’approbation](across-use-workflows.md)  
[Flux de travail](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
