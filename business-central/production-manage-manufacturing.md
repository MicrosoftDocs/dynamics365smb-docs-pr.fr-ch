---
title: Exécution de la production
description: 'Lorsque la demande est planifiée et les matières ont été produites conformément aux nomenclatures de production, les opérations de production réelles peuvent commencer et être exécutées selon la séquence définie par la gamme O.F.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5406, 5407, 5728, 8903, 9011, 9012, 9013, 9041, 9044, 9047, 9323, 9324, 9325, 9326, 9327, 99000784, 99000785'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Production

> [!NOTE]
> La fonctionnalité décrite dans ces rubrique et sous-rubriques n’est visible dans l’interface utilisateur que si vous avez l’expérience **Premium**. Pour plus d’informations, voir [Modifier les fonctionnalités affichées](ui-experiences.md).

Lorsque la demande est planifiée et les matières ont été produites conformément aux nomenclatures de production, les opérations de production réelles peuvent commencer et être exécutées selon la séquence définie par la gamme O.F.  

Une grande partie de l’exécution de la production, du point de vue du système, consiste à valider la production dans la base de données pour indiquer l’avancement ainsi qu’à mettre à jour le stock avec les articles finis. La validation de la production peut être effectuée manuellement en renseignant et en validant les lignes feuille après les opérations de production. La validation peut également être automatisée en utilisant la consommation en amont. Dans ce cas, la consommation de matières est automatiquement validée en même temps que la production lors du changement du statut de l’ordre de fabrication en Terminé.  

Outre la feuille de validation de la production pour plusieurs ordres de fabrication, vous pouvez utiliser la page **Feuille production** pour valider la consommation et/ou la production d’une ligne O.F.

Avant de pouvoir commencer à produire des articles, vous devez procéder à divers paramétrages, tels que les centres de charge, les gammes et les nomenclatures de production. Pour plus d’informations, voir [Paramétrage de la production](production-configure-production-processes.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|  
|Comprendre le fonctionnement des ordres de fabrication.|[À propos des ordres de fabrication](production-about-production-orders.md)|
|Créer manuellement des ordres de fabrication.|[Créer des ordres de fabrication](production-how-to-create-production-orders.md)|
|Confier à un sous-traitant toutes les opérations ou les opérations sélectionnées dans un ordre de fabrication.|[Sous-traiter la production](production-how-to-subcontract-manufacturing.md)|
|Enregistrer et valider la production, ainsi que la consommation matière et temps, pour une seule ligne O.F. lancé.|[Valider la consommation et la production pour une ligne ordre de fabrication lancé](production-how-to-register-consumption-and-output.md)|  
|Valider par lots la quantité de composants utilisés par opération dans une feuille qui peut traiter plusieurs ordres de fabrication planifiés.|[Valider par lots la consommation](production-how-to-post-consumption.md)|
|Valider la quantité de produits finis et le temps passé par opération dans une feuille qui peut traiter plusieurs ordres de fabrication lancés.|[Valider par lots la production et les temps d’exécution](production-how-to-post-output-quantity.md)|
|Annuler la production, par exemple à cause d’un montant incorrect et d’erreurs de saisie.  |[Contrepasser la validation de production](production-how-to-reverse-output-posting.md)|  
|Valider le nombre d’articles produits dans chaque opération terminée qui ne sont pas considérés comme produits finis, mais comme rebuts.|[Valider le rebut](production-how-to-post-scrap.md)|
|Afficher la charge de l’atelier en tant que résultat des ordres de fabrication planifiés fermes et lancés.|[Afficher la charge des centres de charge et des postes de charge](production-how-to-view-the-load-on-work-centers.md)|  
|Utiliser la page **Feuille capacité** pour valider les capacités consommées qui ne sont pas affectées à un ordre de fabrication, telles que les travaux de maintenance.|[Valider les capacités](production-how-to-post-capacities.md)|  
|Calculer et ajuster le coût des articles finis et des composants consommés à des fins de rapprochement bancaire.|[À propos des coûts des O.F. terminés](finance-about-finished-production-order-costs.md)|  

## Voir aussi

[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]