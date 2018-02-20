---
title: "Définir une méthode TEC et surveiller la progression du projet | Microsoft Docs"
descrition: Describes how you can create a work in process (WIP) method and calculate WIP to estimate the financial value of jobs while they are ongoing.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 07/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 22dc57e01941927dfc2077eb1e48645cfc7b56de
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="monitor-job-progress-and-performance"></a>Surveiller la progression et les performances
Au fur et à mesure de la progression du projet, les matières, ressources et autres frais sont consommés et doivent être validés dans le projet. La fonctionnalité Travaux en cours (TEC) permet d'estimer la valeur financière des projets dans la comptabilité au cours des projets. Dans de nombreux cas, vous pouvez valider les frais pour un projet avant de le facturer. Lorsque seuls les frais sont validés, l'état financier est incorrect. Pour en savoir plus, reportez-vous à [Comprendre les méthodes TEC](projects-understanding-wip.md).

Pour effectuer le suivi de la valeur dans la comptabilité, vous pouvez calculer les TEC et valider la valeur en comptabilité.

Vous pouvez calculer les TEC sur la base des éléments suivants :

* Valeur de coût
* Valeur des ventes
* Coût identifiable
* Pourcentage avancement
* Fin de contrat

Pour afficher le résultat avec une autre méthode, vous pouvez modifier la méthode et calculer les TEC de nouveau. Le calcul des TEC peut être exécuté un nombre illimité de fois. Le TEC est uniquement calculé, il n'est pas validé dans la comptabilité. Une fois les TEC calculés, vous pouvez effectuer une validation dans la comptabilité.

## <a name="to-create-a-job-wip-method"></a>Pour créer une méthode TEC projet
Vous pouvez créer une méthode TEC projet qui reflète les besoins de votre organisation. Après l'avoir créée, vous pouvez la configurer comme méthode par défaut de calcul TEC projet qui sera utilisée dans votre organisation.  

> [!NOTE]
> Après avoir utilisé la nouvelle méthode pour créer des écritures TEC, vous ne pouvez pas supprimer la méthode ou la modifier.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Méthodes TEC projet**, puis sélectionnez le lien connexe.  
2. Cliquez sur **Nouveau**, puis renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Fermez la fenêtre.   
4. Pour faire de cette nouvelle méthode la valeur par défaut, sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres projets**, puis sélectionnez le lien connexe.  
5. Dans le champ **Méthode TEC par défaut**, choisissez la méthode de la liste.

## <a name="to-define-a-wip-method-for-a-job"></a>Pour définir une méthode TEC pour un projet
Lorsque vous créez un projet, vous devez spécifier la méthode TEC projet qui s'applique. Dans certains cas, quelle méthode TEC projet utilisable a été paramétrée pour vous par défaut.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Projets**, puis choisissez le lien associé.
2. Sélectionnez l'action **Nouveau**. Pour plus d'informations, voir [Créer des projets](projects-how-create-jobs.md).  
3. Dans la fenêtre **Fiche projet**, dans le champ **Méthode TEC**, sélectionnez une méthode TEC dans la liste. Si une méthode par défaut a été définie, vous pouvez sélectionner une autre option si nécessaire.  

## <a name="to-calculate-wip"></a>Pour calculer les TEC :
Vous pouvez déterminer le montant TEC devant être validé dans les comptes de bilan pour la génération d'états de clôture d'exercice. Pour ce faire, utilisez le traitement par lots **Projet Calculer TEC**.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Méthodes TEC projet**, puis sélectionnez le lien connexe.  
2. Cliquez sur **Calculer TEC**.
3. Dans la fenêtre **Projet Calculer TEC**, renseignez les champs comme nécessaire.
4. Cliquez sur le bouton **OK**.  

> [!NOTE]  
>   Le traitement par lots calcule uniquement les TEC. Il n'est pas validé dans la comptabilité. Pour ce faire, exécutez le traitement par lots **Valider TEC en compta.** à l'issue du calcul. Pour plus d'informations, voir la procédure suivante.

## <a name="to-post-wip"></a>Pour valider les TEC
Quand vous avez calculé les TEC, vous pouvez les valider pour équilibrer les comptes bilan pour le reporting de fin de période. Pour ce faire, utilisez le traitement par lots **Projet Valider TEC en comptabilité**.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Méthodes TEC projet**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Projet Valider TEC en comptabilité**, renseignez les champs selon vos besoins.  
3. Cliquez sur le bouton **OK**.

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Pour visualiser les estimations projet et valider les mises à jour
Vous pouvez visualiser les activités projet jusqu'à leur achèvement en une étape. Pour ce faire, utilisez le traitement par lots **Projet Calc. activité restante** pour toutes les tâches jusqu'à la fin du projet.  

Cela vous permet de suivre vos estimations initiales, de les comparer aux résultats réels, ainsi que d'apporter des modifications et d'ajouter de nouvelles écritures, selon les besoins. Par exemple, alors que vous aviez estimé qu'un projet nécessitait 10 heures de travail, vous en avez effectué 15. Vous pouvez ajouter les cinq heures supplémentaires à la ligne feuille existante ou créer une ligne feuille pour les déclarer en tant qu'heures supplémentaires, ce qui constitue un autre type de tâche. Le coût et le prix appropriés sont calculés. Vous pouvez les valider dans la feuille.  

> [!NOTE]  
>   Les écritures article créent des écritures comptables article et diminuent les articles en stock. Le traitement par lots **Valider coûts ajustés** permet de transférer le coût du stock à la comptabilité. Les écritures ressource créent des écritures comptables ressource.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles projet**, puis sélectionnez le lien connexe.  
2. Sélectionnez une feuille projet appropriée, puis cliquez sur l'action **Calc. activité restante**.  
3. Dans la fenêtre **Projet Calc. activité restante**, entrez le numéro et la date de comptabilisation du document devant être insérés dans la feuille, puis sélectionnez le bouton **OK**.  
4. Mettez à jour la feuille avec toutes les modifications qui peuvent être nécessaires.  
5. Sélectionnez l'action **Valider**.

## <a name="to-view-job-ledger-entries"></a>Pour visualiser des écritures comptables projet
Toutes les écritures liées à des projets sont enregistrées dans des historiques des transactions projet et sont numérotées de manière séquentielle à partir de 1. L'historique des transactions projet permet d'obtenir un aperçu de toutes les écritures comptables projet.    

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles projet**, puis sélectionnez le lien connexe.
2. Sélectionnez un historique approprié, puis cliquez sur **Écritures projet**

Dans la fenêtre **Écritures comptables projet** vous pouvez passer en revue les écritures associées à un projet.  

## <a name="see-also"></a>Voir aussi
[Gestion des projets](projects-manage-projects.md)
[Gestion de l'évaluation stock](finance-manage-inventory-costs.md)   
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)         
[Ventes](sales-manage-sales.md)      
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

