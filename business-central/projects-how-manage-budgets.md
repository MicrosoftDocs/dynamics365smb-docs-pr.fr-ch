---
title: Paramétrer et gérer un budget pour un projet
description: Décrit comment planifier des ressources et prévoir et contrôler les coûts d’un projet en définissant un budget pour chaque projet.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project budget, forecast'
ms.search.form: '1002, 1007'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="manage-job-budgets"></a><a name="manage-job-budgets"></a><a name="manage-job-budgets"></a>Gérer les budgets de projets

Vous pouvez configurer un budget pour chaque projet. Le budget permet de planifier les ressources que vous affectez à un projet. Il peut s’agir d’un budget général avec peu d’écritures ou plus détaillé avec des écritures réparties par niveau d’activité. Vous pouvez alors comparer les montants budgétés avec l’activité réelle telle qu’elle a été enregistrée dans la feuille projet. En surveillant les différences entre l’activité réelle et celle budgétée, vous pouvez contrôler un projet en cours et améliorer la qualité des projets futurs en réduisant le risque de sous-estimation des coûts.

La procédure suivante décrit comment estimer les coûts budgétés lors de la planification. Pour plus d’informations sur l’enregistrement budgété par rapport aux prix et aux coûts réels du projet, voir [Enregistrer l’utilisation pour les projets](projects-how-record-job-usage.md).  

## <a name="to-estimate-the-budgeted-costs-for-a-job"></a><a name="to-estimate-the-budgeted-costs-for-a-job"></a><a name="to-estimate-the-budgeted-costs-for-a-job"></a><a name="JobBudgetCosts"></a> Pour estimer les coûts budgétés d’un projet
Lorsqu’un client souhaite connaître le prix d’un projet qui sera facturé en fonction de l’activité, vous devez déterminer les coûts budgétés du projet. Réalisez cette opération sur la page **Lignes tâche projet**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Projets**, puis choisissez le lien associé.  
2. Ouvrez le projet approprié.
3. Sélectionnez une ligne tâche de type Validation, puis cliquez sur **Lignes planning projet**.
4. Sur une nouvelle ligne, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

Reportez-vous aux informations suivantes pour le champ **Type ligne**.  

| Type ligne | Désignation |
| --- | --- |
| **Budget et Facturable** |Les montants coût et prix entrés sur la ligne planning sont les coûts budgétés pour la ligne planning donnée. Le prix sera facturé. |
| **Budget** |Le client ne doit pas payer l’utilisation. L’activité n’est pas transférée à une facture, mais sera encore utilisée dans le calcul de TEC. |
| **Facturable** |Le client doit payer l’utilisation. L’activité est transférée à la facture, sur la base de la quantité spécifiée dans le champ Qté à transférer à facturer. |

> [!NOTE]  
> Le champ **Date livraison planifiée** de la ligne planning contient la date prévue de l’achèvement et de la validation de l’activité associée à cette ligne planning. C’est aussi la date à laquelle la ligne planning peut être transférée à une facture vente et être validée. <br /><br /> Sur la tâche projet sous-jacente de la page **Fiche suiveuse**, les champs **Date début** et **Date fin** contiennent respectivement la valeur du champ **Date livraison planifiée** sur les lignes planning projet les plus récentes et les dernières de la page **Lignes planning projet** associée.

> [!NOTE]  
>   Quand vous renseignez le champ **Quantité**, toutes les informations prix total et coût total seront désormais calculées et renseignées pour cette ligne planning. Vous pouvez modifier ces informations à tout moment.

Sur la page **Fiche projet**, vous pouvez désormais voir un résumé des coûts budgétés totaux, des prix budgétés, du coût facturable et du prix facturable pour chaque tâche.

Pour plus d’informations sur l’enregistrement budgété par rapport aux prix et aux coûts réels du projet, voir [Enregistrer l’utilisation pour les projets](projects-how-record-job-usage.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/set-up-job-planning-lines/) associée

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Gestion de projets](projects-manage-projects.md)  
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
