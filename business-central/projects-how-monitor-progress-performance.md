---
title: Surveiller la progression et les performances
description: Décrit la manière dont vous pouvez créer une méthode de travaux en cours (TEC) et calculer les TEC pour estimer la valeur financière des projets lorsqu’ils sont en cours.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
---
# Surveiller la progression et les performances

Grâce à la fonctionnalité encours (WIP), vous pouvez estimer la valeur financière des projets en cours dans la comptabilité.

Au fur et à mesure de la progression du projet, les matières et ressources sont consommées et les frais qui en découlent doivent être validés dans le projet. Dans de nombreux cas, vous pouvez valider les frais pour un projet avant la facturation. Cependant, lorsque seuls les frais sont validés, l’état financier est incorrect. Pour suivre la valeur réelle du projet, il faut calculer l’encours et le valider dans la comptabilité. En savoir plus sur [Comprendre les méthodes TEC](projects-understanding-wip.md).

Vous pouvez calculer les TEC sur la base des éléments suivants :

* Valeur de coût
* Valeur des ventes
* Coût identifiable
* Pourcentage d’achèvement
* Contrat complété

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## Créer une méthode TEC projet

Créez une méthode TEC projet qui répondent aux besoins de votre organisation et définissez-la comme la méthode TEC projet par défaut.  

> [!NOTE]
> Après avoir utilisé la nouvelle méthode pour créer des écritures TEC, vous ne pouvez pas modifier ou supprimer cette méthode.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **méthodes TEC projet**, puis choisissez le lien associé.  
2. Cliquez sur **Nouveau**, puis renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Fermez la page.   
4. Pour faire de cette nouvelle méthode la méthode par défaut, sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **paramètres projets**, puis choisissez le lien associé.  
5. Dans le champ **Méthode TEC par défaut**, choisissez la méthode de la liste.

## Définir une méthode TEC pour un projet

Lorsque vous créez un projet, vous devez spécifier la méthode TEC projet qui s’applique. Dans certains cas, la méthode TEC projet que vous utilisez est déjà définie par défaut.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **projets**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**. En savoir plus sur [Créer des projets](projects-how-create-jobs.md).  
3. Sur la page **Fiche projet**, dans le champ **Méthode TEC**, sélectionnez une méthode TEC dans la liste. Si une méthode par défaut a été définie, vous pouvez sélectionner une autre option si nécessaire.  

### Définir une méthode TEC pour une tâche projet

Vous pouvez définir une méthode TEC pour une tâche, exclure certaines tâches du calcul TEC, ou regrouper des tâches pour les calculer ensemble. 

Si vous souhaitez calculer le TEC pour chaque tâche individuellement, la validation TEC fournit des dimensions définies pour les tâches spécifiques.

Le **Total TEC** spécifie les tâches projet à regrouper lors du calcul TEC et de la réception. Dans n’importe quel groupe de tâches, il faut une tâche répondant à deux conditions :
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Possède un **Total TEC** défini sur *Total*. (Si aucune tâche projet n’a de **Total TEC** défini sur *Total*, la valeur *Total* est configurée automatiquement sur la dernière ligne tâche projet lors du calcul des TEC pour la première fois.)

* Possède un numéro **N° tâche projet** correspondant au numéro final du groupe ou de la plage de tâches projet.

Le tableau suivant décrit trois options :

| Champ | Désignation |
|--|--|
| **\<blank\>** | Laissez le champ vierge si la tâche projet fait partie d’un groupe de tâches. |
| **Total** | Définit la plage ou le groupe de tâches incluses dans le calcul des TEC et de la réception. Au sein du groupe, n’importe quelle tâche projet dont le **Type tâche projet** est réglé sur **Validation** est incluse dans le total TEC, à moins que le champ **Total TEC** soit défini sur **Exclu**. |
| **Exclu** | S’applique uniquement à une tâche dont le **Type tâche projet** est **Validation**, auquel cas la tâche n’est pas incluse dans le calcul TEC et la réception. |

Dans l’exemple suivant, les tâches projet sont réparties en deux groupes de totaux TEC, montrant le fonctionnement du champ **Total TEC** :

|N° tâche projet|Désignation|Type tâche projet|Champ **Total TEC**|  
|------------------|----------------------|----------------------|----------------------|  
|1 000|Préparation|Début total|\<blank\>|
|1010|.    Nettoyage|Valider|**Exclu**|
|1099|Total préparation|Fin total|\<blank\>|
|1100|Moquette|Début total|\<blank\>|
|1110|.    Encollage sol|Valider|**Exclu**|
|1120|.    Disposition moquette|Valider|\<blank\>|
|1199|Total moquette|Fin total|\<blank\>|
|1200|Terminer|Début total|\<blank\>|
|1210|.    Aspirateur moquette|Valider|\<blank\>|
|1299|Total fin|Fin total|**Total**|
|1300|Correction erreur|Début total|\<blank\>|
|1310|.    Correction erreur|Valider|\<blank\>|
|1399|Total correction erreur|Fin total|**Total**|

Vous remarquerez les choses suivantes :

* De *1000* à *1299* : les TEC sont calculés séparément pour ce groupe de tâches projet. Notez cependant que deux des tâches, 1010 et 1110, sont exclues du calcul TEC car leur type de tâche projet est **Validation**.

* De *1300* à *1399* : les TEC sont calculés séparément pour ce groupe de tâches projet.

## Calculer TEC

Vous pouvez déterminer le montant TEC à valider dans les comptes de bilan pour la génération d’états de clôture d’exercice. Utilisez le traitement par lots **Projet Calculer TEC**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **projet calculer TEC**, puis choisissez le lien associé.  
2. Cliquez sur **Calculer TEC**.
3. Sur la page **Projet Calculer TEC**, renseignez les champs comme nécessaire.
4. Cliquez sur le bouton **OK**.  

> [!NOTE]  
>   Ce traitement par lots calcule uniquement le TEC et ne le valide pas dans la comptabilité. Pour le valider, exécutez le traitement par lots **Valider TEC en compta.** à l’issue du calcul TEC. Consultez la procédure ci-dessous pour en savoir plus.

## Valider TEC

Quand vous avez calculé les TEC, vous pouvez les valider pour équilibrer les comptes bilan pour le reporting de fin de période. Pour ce faire, utilisez le traitement par lots **Projet Valider TEC en comptabilité**.

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **projet valider TEC en comptabilité**, puis choisissez le lien associé.  
2. Sur la page **Projet Valider TEC en comptabilité**, renseignez les champs selon vos besoins.  
3. Cliquez sur le bouton **OK**.

## Calculer et valider les écritures d’achèvement du projet

À la fin des activités d’un projet (validation et facturation comprises), vous devez le mettre à jour pour définir le **Statut** du projet sur **Terminé**. Ensuite, vous devez contrepasser tous les travaux en cours validés antérieurement dans la comptabilité.

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **projets**, puis choisissez le lien associé.  
2. Sélectionnez un projet ouvert, puis cliquez sur **Modifier**.
3. Dans le champ **Statut**, sélectionnez **Terminé**.
4. Suivez les étapes d’aide pour calculer et valider le TEC. Vous pouvez également suivre les étapes 5 et 6 pour le faire manuellement.  
5. Cliquez sur **Calculer TEC**.
6. Sur la page **Projet Calculer TEC**, renseignez les champs comme nécessaire.  

     Les écritures TEC projet créées par le traitement par lots auront la case **Projet terminé** cochée pour indiquer qu’il s’agit d’écritures d’achèvement.  
7. Cliquez sur **Projet Valider TEC en comptabilité**.
8. Sur la page **Projet Valider TEC en comptabilité**, renseignez les champs selon vos besoins.  

     Les écritures comptabilité TEC projet créées par le traitement par lots verront la case **Projet terminé** cochée pour indiquer qu’il s’agit d’écritures d’achèvement.

## Visualiser des écritures comptables projet

Toutes les écritures liées à des projets sont enregistrées dans des historiques des transactions projet et sont numérotées de manière séquentielle, à partir de 1. L’historique des transactions projet permet d’obtenir un aperçu de toutes les écritures comptables projet.    

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **registres projet**, puis choisissez le lien associé.
2. Sélectionnez un historique approprié, puis cliquez sur **Écritures projet**

Sur la page **Écritures comptables projet** vous pouvez passer en revue les écritures associées à un projet.  

## Voir aussi

[Procédure pas à pas : calcul des travaux en cours pour un projet](walkthrough-calculating-work-in-process-for-a-job.md)
[Gestion des projets](projects-manage-projects.md)  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
