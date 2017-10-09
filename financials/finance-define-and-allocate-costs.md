---
title: "Définition et Répartition des coûts | Microsoft Docs"
description: "Les affectations de coûts déplacent les coûts et les revenus entre les types de coûts, les centres de coûts et les coûts associés. Vous pouvez définir autant d'affectations que nécessaire."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 050b0bd997629ca189cfbe035e361de7a252d079
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="defining-and-allocating-costs"></a>Définition et répartition des coûts
Les affectations de coûts déplacent les coûts et les revenus entre les types de coûts, les centres de coûts et les coûts associés. Vous pouvez définir autant d'affectations que nécessaire. Chaque affectation comporte les éléments suivants :  

-   Une source affectation.  
-   Une ou plusieurs cibles d'affectation.  

La source d'affectation détermine les coûts à affecter, tandis que les cibles d'affectation déterminent l'emplacement des coûts à affecter. Par exemple, les coûts pour le type de coût Fournitures non stockables représentent une source de ventilation. Vous affectez tous les coûts de fournitures non stockables à trois centres de coûts : Atelier, Production, et Vente. Ces centres de coûts sont les cibles d'affectation.  

Pour chaque source d'affectation, vous définissez un niveau d'affectation, une période de validité et une variante comme identifiant de regroupement. Vous pouvez utiliser un traitement par lots pour définir des filtres afin de sélectionner les définitions d'affectation, puis exécuter les affectations des coûts automatiquement.  

Pour chaque cible d'affectation, vous définissez une base de ventilation. La base de ventilation peut être statique ou dynamique.  

-   Les bases de ventilation statique dépendent d'une valeur définie, par exemple, les mètres carrés utilisés ou un ratio de ventilation prédéfini, comme 5:2:4.  
-   Les bases de ventilation dynamique dépendent de valeurs variables, telles que le nombre de salariés dans un centre de coût ou les revenus de vente d'un coût associé pour une période donnée.  

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

|À|Voir|  
|--------|---------|  
|Configurez la source d'affectation et ses cibles.|[Procédure : configurer la source d'affectation et ses cibles](finance-how-to-set-up-allocation-source-and-targets.md)|  
|Configurez plusieurs filtres pour les bases de ventilation dynamique.|[Définition de filtres pour les bases de ventilation dynamique](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|Consultez un exemple sur le mode de définition d'une ventilation statique.|[Exemple de scénario : Définition des ventilations statiques en fonction du ratio d'affectation](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|Consultez un exemple sur le mode de définition d'une ventilation dynamique.|[Exemple de scénario : Définition des ventilations dynamiques sur la base des articles vendus](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a>Voir aussi  
 [Paramétrage du contrôle de gestion](finance-set-up-cost-accounting.md)   
 [Transfert et validation des écritures de coûts](finance-transfer-and-post-cost-entries.md)   
 [Comptabilité pour les coûts](finance-manage-cost-accounting.md)   
 [Terminologie en comptabilité analytique](finance-terminology-in-cost-accounting.md)   
 [À propos de la comptabilité analytique](finance-about-cost-accounting.md)

