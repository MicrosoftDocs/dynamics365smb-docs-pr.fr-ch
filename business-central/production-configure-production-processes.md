---
title: Configuration des processus de production
description: 'Pour convertir des matières en articles finis produits, vous devez configurer des ressources de production, telles que les nomenclatures, les gammes, les opérateurs machines et les machines, dans le système.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000768, 99000779, 99000780, 99000866'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setting-up-manufacturing"></a><a name="setting-up-manufacturing"></a>Paramétrage de la production

Pour convertir des matières en articles finis produits, vous devez configurer des ressources de production, telles que les nomenclatures, les gammes, les opérateurs machines et les machines, dans le système.

Les opérateurs et les machines sont représentés dans le système comme des postes de charge pouvant être organisés en centres de charge et groupes de centres de charge. Lorsque ces ressources sont établies, elles peuvent être chargées avec des opérations en fonction des nomenclatures matières et de la structure (gamme) opératoire définies pour l’article, et en fonction de la capacité du poste ou centre de charge. Vous pouvez également configurer la capacité de production de chaque ressource. La capacité est définie par le temps de travail disponible dans les postes et centres de charge, et est gérée par des calendriers pour chaque niveau. Un calendrier centre de charge spécifie les jours ouvrés et les heures de travail, les équipes, les jours fériés et les absences déterminant la capacité disponible brute du centre de charge (généralement mesurée en minutes). Tout cela est déterminé par les valeurs d’efficacité et de capacité définies.  

Une fois que vous avez paramétré la production, vous pouvez planifier et exécuter des ordres de fabrication. Pour plus d’informations, voir [Planification](production-planning.md) et [Production](production-manage-manufacturing.md).  

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

|**Pour**|**Voir**|  
|------------|-------------|  
|Configurer les fonctionnalités de fabrication, telles que la définition des heures de travail atelier et la sélection des paramètres de planification.|Page **Paramètres production**.|
|Dans l’onglet **Planification** de la page **Paramètres production**, définissez les paramètres de planification globale qui remplacent les paramètres définis sur les fiches d’articles individuelles.|[Détails de conception : paramètres de planification](design-details-planning-parameters.md)|
|Définir une semaine de travail standard dans le département Production en termes d’heures de début et de fin de chaque journée de travail et des équipes associées.|[Créer des calendriers usine](production-how-to-create-work-center-calendars.md)|  
|Organiser les exigences et les valeurs fixes des ressources de production en centres de charge ou postes de charge pour régir leur production.|[Configurer les centres de charge et les postes de charge](production-how-to-set-up-work-and-machine-centers.md)|
|Organiser les opérations de fabrication dans l’ordre requis et les affecter aux centres ou postes de charge avec les temps de travail nécessaires.|[Créer des gammes](production-how-to-create-routings.md)|
|Organiser des composants de production ou des produits semi-finis sous un article parent produit et certifier la nomenclature d’exécution dans les centres de charge.|[Créer des nomenclatures de production](production-how-to-create-production-boms.md)|
|Vérifier que la quantité appropriée de composants est disponible lorsque des articles produits sont stockés dans une unité de mesure mais produits dans une autre.|[Utiliser les unités de lot de fabrication](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Définir des familles d’articles produits ayant des processus de fabrication similaires pour réduire la consommation. Par exemple, quatre pièces du même article et dix pièces d’un autre peuvent être fabriquées simultanément à partir d’une plaque.|[Utiliser les familles de production](production-how-work-family.md)|
|Utiliser des tâches standard pour simplifier la création de gammes en associant rapidement des informations supplémentaires aux opérations récurrentes.|[Configurer des lignes gamme standard](production-how-set-up-standard-routing-lines.md)|  
|Préparez les centres de charge et les gammes à représenter les opérations de production sous-traitées.|[Sous-traiter la production](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Production](production-manage-manufacturing.md)  
[Planifié](production-planning.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
