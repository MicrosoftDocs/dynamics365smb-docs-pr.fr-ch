---
title: "Procédure : gérer les budgets de projets| Microsoft Docs"
description: "Décrit comment gérer les budgets pour les projets."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 9a351b581e0312d21b04db43a85243b8a5afb0e3
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-job-budgets"></a>Procédure : Gérer les budgets de projets
Vous pouvez configurer un budget pour chaque projet. Le budget permet de planifier les ressources que vous affectez à un projet. Il peut s'agir d'un budget général avec peu d'écritures ou plus détaillé avec des écritures réparties par niveau d'activité. Vous pouvez alors comparer les montants budgétés avec l'activité réelle telle qu'elle a été enregistrée dans la feuille projet. En surveillant les différences entre l'activité réelle et celle budgétée, vous pouvez contrôler un projet en cours et améliorer la qualité des projets futurs en réduisant le risque de sous-estimation des coûts.

La procédure suivante décrit comment estimer les coûts budgétés lors de la planification. Pour plus d'informations sur l'enregistrement budgété par rapport aux prix et aux coûts réels du projet, voir [Procédure : Enregistrer l'utilisation pour les projets](projects-how-record-job-usage.md).  

## <a name="JobBudgetCosts"></a> Pour estimer les coûts budgétés d'un projet
Lorsqu'un client souhaite connaître le prix d'un projet qui sera facturé en fonction de l'activité, vous devez déterminer les coûts budgétés du projet. Réalisez cette opération dans la fenêtre **Lignes tâche projet**.

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Projets**, puis sélectionnez le lien associé.  
2. Ouvrez le projet approprié.
3. Sélectionnez une ligne tâche de type Validation, puis cliquez sur **Lignes planning projet**.
4. Sur une nouvelle ligne, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

Reportez-vous aux informations suivantes pour le champ **Type ligne**.  

| Type ligne | Désignation |
| --- | --- |
| **Budget et Facturable** |Les montants coût et prix entrés sur la ligne planning sont les coûts budgétés pour la ligne planning donnée. Le prix sera facturé. |
| **Budget** |Le client ne doit pas payer l'utilisation. L'activité n'est pas transférée à une facture, mais sera encore utilisée dans le calcul de TEC. |
| **Facturable** |Le client doit payer l'utilisation. L'utilisation est transférée à la facture, sur la base de la quantité spécifiée dans le champ Qté. à transférer à facturer. |

**Remarque** : Le champ **Date planning** de la ligne planning contient la date prévue de l'achèvement et de la validation de l'activité associée à cette ligne planning. C'est aussi la date à laquelle la ligne planning peut être transférée à une facture vente et être validée.  

**Remarque** : Quand vous renseignez le champ **Quantité**, toutes les informations prix total et coût total seront désormais calculées et renseignées pour cette ligne planning. Vous pouvez modifier ces informations à tout moment.

Dans la fenêtre **Fiche projet**, vous pouvez désormais voir un résumé des coûts budgétés totaux, des prix budgétés, du coût facturable et du prix facturable pour chaque tâche.

Pour plus d'informations sur l'enregistrement budgété par rapport aux prix et aux coûts réels du projet, voir [Procédure : Enregistrer l'utilisation pour les projets](projects-how-record-job-usage.md).

## <a name="see-also"></a>Voir aussi
[Gestion de projets](projects-manage-projects.md)  
[Finance](finance.md)  
[Achats](purchasing-manage-purchasing.md)         
[Ventes](sales-manage-sales.md)      
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

