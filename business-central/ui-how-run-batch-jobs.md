---
title: Exécuter des traitements par lots et des ports XML
description: 'Vous exécutez des traitements par lots pour traiter les données et mettre à jour les informations, par exemple, pour élaborer des activités périodiques de comptabilité, ou effectuer des calculs.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process'
ms.search.form: '672, 676, 682'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Exécuter des traitements par lots et des ports XML

Un traitement par lots est une routine qui traite les données par lots, par exemple le traitement par lots **Ajuster taux de change**. Certains traitements par lots exécutent des activités périodiques de comptabilité, telles que la clôture des comptes de gestion à la fin d’un exercice comptable. De nombreux traitements par lots exécutent des calculs, telles que le calcul des intérêts de retard, l’ajustement du taux de change et le calcul des prix unitaires.

Un traitement par lots est similaire à un état, sauf qu’il utilise les résultats obtenus pour mettre à jour les informations directement plutôt que d’imprimer les résultats.

Vous pouvez planifier l’exécution d’un traitement par lot. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

## Pour exécuter un traitement par lots
1. Pour ouvrir la page de demande du traitement par lots concerné, sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez le nom du travail par lots, puis choisissez le lien associé.
2. Si un raccourci **Options** est disponible pour le traitement par lots, renseignez-en les champs pour déterminer les tâches effectuées par le traitement par lots.
3. La page peut inclure un ou plusieurs raccourcis avec des filtres que vous pouvez utiliser pour limiter les données incluses dans le traitement par lots. Pour cela, entrez des critères dans les filtres suggérés ou ajoutez des filtres supplémentaires.
4. Pour démarrer le traitement par lots, cliquez sur le bouton **OK**.

## Voir aussi
[Tri, recherche et filtrage de listes](ui-enter-criteria-filters.md)  
[Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]