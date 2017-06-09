---
title: "Procédure : exécuter des traitements par lots | Microsoft Docs"
description: Apprendre le fonctionnement du traitement par lots dans Dynamics 365 for Financials.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1f4678ce0cfb18a746374226bb33020f70bf874d
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-run-batch-jobs"></a>Procédure : exécuter des traitements par lots
Un traitement par lots est une routine qui traite les données par lots, par exemple le traitement par lots **Ajuster taux de change**. Certains traitements par lots exécutent des activités périodiques de comptabilité, telles que la clôture des comptes de gestion à la fin d'un exercice comptable. De nombreux traitements par lots exécutent des calculs, telles que le calcul des intérêts de retard, l'ajustement du taux de change et le calcul des prix unitaires.

Un traitement par lots est similaire à un état, sauf qu'il utilise les résultats obtenus pour mettre à jour les informations directement plutôt que d'imprimer les résultats.

## <a name="to-run-a-batch-job"></a>Pour exécuter un traitement par lots
1. Pour ouvrir le formulaire de sélection du traitement par lots concerné, dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez le nom du traitement par lots, puis sélectionnez le lien connexe.
2. Si un raccourci **Options** est disponible pour le traitement par lots, renseignez-en les champs pour déterminer les tâches effectuées par le traitement par lots.
3. La fenêtre peut inclure un ou plusieurs raccourcis avec des filtres que vous pouvez utiliser pour limiter les données incluses dans le traitement par lots. Pour cela, entrez des critères dans les filtres suggérés ou ajoutez des filtres supplémentaires.
4. Pour démarrer le traitement par lots, cliquez sur le bouton **OK**.

## <a name="see-also"></a>Voir aussi
[Saisir les critères pour les filtres](ui-enter-criteria-filters.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

