---
title: À propos de la comptabilité analytique
description: La comptabilité analytique vous permet de cerner les coûts liés à l’exploitation d’un activié. Les informations sur la comptabilité analytique sont conçues pour analyser divers problèmes.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '1101, 1103, 1105, 1108, 1111, 1112, 1124, 1123'
ms.date: 08/23/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="about-cost-accounting"></a>À propos de la comptabilité analytique

La comptabilité analytique vous permet de cerner les coûts liés à l’exploitation d’un activié. Les informations sur la comptabilité analytique sont conçues pour analyser :  

- Les types de coûts encourus dans la gestion d’une entreprise  
- Emplacement des coûts encourus
- Qui prend en charge les coûts  

En comptabilité analytique, vous affectez des coûts réels et budgétés relatifs à l’exploitation, aux départements, aux produits et aux projets pour analyser la rentabilité de votre société.  

## <a name="workflow-in-cost-accounting"></a>Flux de travail en comptabilité analytique

La comptabilité analytique est constituée des composants principaux suivants :  

- Types de coûts, centres de coûts et coûts associés  
- Écritures de coûts et feuilles de coûts  
- Affectations des coûts  
- Budgets des coûts
- Rapports sur les coûts  

Le schéma suivant présente le flux de travail en comptabilité analytique.  

![Vue d’ensemble de la comptabilité analytique.](media/costaccountingoverview.png "CostAccountingOverview")  

## <a name="cost-types-cost-centers-and-cost-objects"></a>Types de coûts, centres de coûts et coûts associés

Vous définissez les types de coûts, les centres de coûts et les coûts associés pour analyser leur type, leur source et la personne qui les prend en charge.  

Tout d’abord, vous définissez un plan des types de coûts avec une structure et une fonctionnalité qui ressemblent au plan comptable général. Vous pouvez créer votre propre plan des types de coûts, ou le faire en transférant les comptes de gestion.  

Les centres de coûts sont les départements et les centres de profit responsables des coûts et des revenus. Le nombre de centres de coûts paramétrés en comptabilité analytique est souvent supérieur aux axes analytiques paramétrés en comptabilité. En règle générale, la comptabilité utilise uniquement les centres de coûts de premier niveau pour les coûts directs et les coûts initiaux. En comptabilité analytique, des centres de coûts supplémentaires sont créés pour des niveaux de ventilation supplémentaires.  

Les coûts associés sont les biens, les groupes de biens ou les services d’une société. Ce sont les « produits finis » d’une société qui prennent en charge les coûts.  

Vous pouvez lier les centres de coûts aux départements et les coûts associés aux projets au sein de la société. Dans la comptabilité, vous pouvez lier les centres de coûts et les coûts associés à tous les axes analytiques et les compléter avec les informations des sous-totaux et des titres.  

## <a name="cost-entries-and-cost-journals"></a>Écritures de coûts et feuilles de coûts

Les coûts opérationnelles peuvent être transférés vers la comptabilité. Vous pouvez transférer automatiquement les écritures à partir de la comptabilité vers les écritures de coûts à chaque validation. Vous pouvez également utiliser un traitement par lots pour transférer les écritures comptables vers les écritures de coûts en fonction de la validation récapitulative journalière ou mensuelle.  

Dans les feuilles de coûts, vous pouvez valider les coûts et les activités qui ne proviennent pas de la comptabilité ou qui ne sont pas générés par les affectations. Par exemple, vous pouvez valider les coûts opérationnels, les frais internes, les allocations et les écritures de correction entre les types de coûts, les centres de coûts et les coûts associés, de manière individuelle ou récurrente.  

## <a name="cost-allocations"></a>Affectations des coûts

Les affectations déplacent les coûts et les revenus entre les types de coûts, les centres de coûts et les coûts associés. Les frais généraux sont d’abord imputés aux centres de coûts, puis aux coûts associés. Par exemple, vous pouvez réaliser cette imputation dans un département des ventes, qui vend plusieurs biens simultanément. Les frais généraux du département, tels que les salaires, les fournitures et les frais de déplacement, sont initialement affectés au centre de coûts de vente, et sont ensuite répartis entre les différents produits (coûts associés) vendus, ainsi que sur les matériaux achetés (coûts directs) utilisés dans ces produits.

La base de ventilation utilisée et la précision de la définition de ventilation ont une incidence sur les résultats des affectations de coûts. La définition de la ventilation permet d’affecter les coûts depuis des centres de pré-coûts vers les centres de coûts principaux, puis depuis des centres de coûts vers des coûts associés.  

Chaque affectation comporte une source et au moins une cible. Vous pouvez affecter des valeurs réelles ou budgétées à l’aide de la méthode de ventilation statique qui repose sur une valeur définie, par exemple, les mètres carrés utilisés ou un ratio de ventilation prédéfini, comme 5:2:4. Vous pouvez également affecter des valeurs réelles ou budgétées à l’aide de la méthode de ventilation dynamique avec neuf bases de ventilation prédéfinies et 12 plages de dates dynamiques.  

## <a name="cost-budgets"></a>Budgets des coûts

De manière similaire à la budgétisation dans la comptabilité, vous pouvez créer des budgets pour planifier les coûts au cours d’une certaine période (un exercice, par exemple), qui peuvent être appliqués à un centre de coûts (département de l’entreprise) ou à un coût associé (produit ou service). Vous pouvez créer autant de budgets de coûts que nécessaire. Vous pouvez ensuite copier le budget de coûts vers le budget de comptabilité et vice versa. Et vous pouvez transférer des coûts budgétés en tant que coûts réels.

## <a name="cost-reporting"></a>Rapports sur les coûts

La plupart des états et des statistiques reposent sur les écritures de coûts validées. Vous pouvez définir le tri des résultats et utiliser des filtres pour définir les informations à afficher. Vous pouvez créer des états pour analyser la distribution des coûts. En outre, vous pouvez utiliser les états financiers standard pour définir le mode d’affichage du plan des types de coûts.  

## <a name="see-also"></a>Voir aussi

[Comptabilité pour les coûts](finance-manage-cost-accounting.md)  
[Finances](finance.md)  
[Terminologie de la comptabilité analytique](finance-terminology-in-cost-accounting.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
