---
title: "Exécuter la production | Microsoft Docs"
description: "Lorsque la demande est planifiée et les matières ont été produites conformément aux nomenclatures de production, les opérations de production réelles peuvent commencer et être exécutées selon la séquence définie par la gamme O.F."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 61c89c50b549a802df1973538edb83d3baf328e4
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="manufacturing"></a>Production
Lorsque la demande est planifiée et les matières ont été produites conformément aux nomenclatures de production, les opérations de production réelles peuvent commencer et être exécutées selon la séquence définie par la gamme O.F.  

Une grande partie de l'exécution de la production, du point de vue du système, consiste à valider la production dans la base de données pour indiquer l'avancement ainsi qu'à mettre à jour le stock avec les articles finis. La validation de la production peut être effectuée manuellement en renseignant et en validant les lignes feuille après les opérations de production. La validation peut également être automatisée en utilisant la consommation en amont. Dans ce cas, la consommation de matières est automatiquement validée en même temps que la production lors du changement du statut de l'ordre de fabrication en Terminé.  

Outre la feuille de validation de la production pour plusieurs ordres de fabrication, vous pouvez utiliser la fenêtre **Feuille production** pour valider la consommation et/ou la production d'une ligne O.F.  

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.   

|**Pour**|**Voir**|  
|------------|-------------|  
|Comprendre le fonctionnement des ordres de fabrication.|[À propos des ordres de fabrication](production-about-production-orders.md)|
|Créer manuellement des ordres de fabrication.|[Procédure : créer des ordres de fabrication](production-how-to-create-production-orders.md)|
|Confier à un sous-traitant toutes les opérations ou les opérations sélectionnées dans un ordre de fabrication.|[Procédure : sous-traiter la production](production-how-to-subcontract-manufacturing.md)|
|Enregistrer et valider la production, ainsi que la consommation matière et temps, pour une seule ligne O.F. lancé.|[Procédure : valider la consommation et la production pour une ligne ordre de fabrication lancé](production-how-to-register-consumption-and-output.md)|  
|Valider par lots la quantité de composants utilisés par opération dans une feuille qui peut traiter plusieurs ordres de fabrication planifiés.|[Procédure : valider par lots la consommation](production-how-to-post-consumption.md)|
|Valider la quantité de produits finis et le temps passé par opération dans une feuille qui peut traiter plusieurs ordres de fabrication lancés.|[Procédure : valider par lots la production et les temps d'exécution](production-how-to-post-output-quantity.md)|  
|Valider le nombre d'articles produits dans chaque opération terminée qui ne sont pas considérés comme produits finis, mais comme rebuts.|[Procédure : valider le rebut](production-how-to-post-scrap.md)|
|Afficher la charge de l'atelier en tant que résultat des ordres de fabrication planifiés fermes et lancés.|[Procédure : afficher la charge des centres de charge et des postes de charge](production-how-to-view-the-load-on-work-centers.md)|      
|Utiliser la fenêtre **Feuille capacité** pour valider les capacités consommées qui ne sont pas affectées à un ordre de fabrication, telles que les travaux de maintenance.|[Procédure : valider les capacités](production-how-to-post-capacities.md)|  
|Calculer et ajuster le coût des articles finis et des composants consommés à des fins de rapprochement bancaire.|[À propos des coûts des O.F. terminés](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a>Voir aussi  
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)      
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

