---
title: Terminologie en comptabilité analytique
description: 'Cette rubrique définit les termes clés utilisés dans la comptabilité analytique, tels que la clé de répartition et la source de répartition.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: 1123
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="terminology-in-cost-accounting"></a>Terminologie en comptabilité analytique

Cette rubrique définit les conditions principales qui sont utilisés en comptabilité analytique.  

## <a name="key-terms"></a>Conditions principales

 Le tableau suivant définit les conditions principales en comptabilité analytique.  

|**Terme**|**Définition**|  
|--------------|--------------------|  
|Clé de répartition|Une clé de ventilation est le principe de base pour affecter des coûts. En règle générale, il s’agit d’une quantité, par exemple les mètres carrés occupés, le nombre de salariés ou les heures de main-œuvre utilisées. Par exemple, deux départements, comptant respectivement 20 et 10 salariés, partagent les coûts pour la cantine. Les coûts sont répartis entre les départements à l’aide d’une clé de ventilation qui représente le nombre de salariés. 2/3 des coûts sont affectés au premier département, et le tiers restant est affecté au second département.|  
|Source affectation|La source d’affectation définit les coûts à affecter. Les affectations sont définies dans les tables de source et de cible d’affectation. Chaque affectation comporte une source et au moins une cible. Par exemple, tous les coûts de type Chauffage, qui est une source d’affectation, peuvent être affectés à l’atelier, à la production et aux centres de coûts, qui représentent trois cibles d’affectation.|  
|Cible affectation|Les cibles d’affectation déterminent où affecter ces coûts. Les affectations sont définies dans les tables de source et de cible d’affectation. Chaque affectation comporte une source et au moins une cible. Par exemple, tous les coûts de type Chauffage, qui est une source d’affectation, peuvent être affectés à l’atelier, à la production et aux centres de coûts, qui représentent trois cibles d’affectation.|  
|Comptabilité analytique|En comptabilité analytique, les coûts réels des opérations, des processus, des départements ou des marchandises sont enregistrés. Ces coûts sont affectés aux centres de coûts et aux coûts associés en utilisant diverses méthodes d’affectation des coûts. Les responsables ont recours aux statistiques et aux états, tels que la feuille de répartition des coûts et l’analyse du résultat financier, pour prendre des décisions et réduire les coûts. La comptabilité analytique extrait les données de la comptabilité générale, mais fonctionne indépendamment. Par conséquent, les transactions validées en comptabilité analytique n’affectent pas les données en comptabilité générale.|  
|Type coût|Le plan des types de coûts a la même fonction que le plan comptable général. La structure est souvent similaire. Par conséquent, vous pouvez transférer le plan comptable général vers le plan de types de coûts, puis le modifier. Le plan des types de coûts peut également être créé à partir de zéro.|  
|Centre de coûts|Les centres de coûts sont le plus souvent des départements et des centres de profit, en grande partie responsables des coûts et des revenus de la société. Les centres de coûts peuvent être synchronisés avec des axes analytiques en comptabilité générale. Vous pouvez également ajouter de nouveaux centres de coûts et définir leur propre méthode de tri avec des sous-totaux.|  
|Coûts associés|Les coûts associés correspondent aux produits, groupes de produits ou services, et produits finis d’une société, qui en définitive prennent en charge les coûts. Les coûts associés peuvent être synchronisés avec des axes analytiques en comptabilité générale. Vous pouvez également ajouter de nouveaux coûts associés et définir leur propre méthode de tri avec des sous-totaux.|  
|Affectation des coûts|L’affectation des coûts est un processus d’affectation des coûts aux centres de coûts ou aux coûts associés. Par exemple, le salaire du chauffeur de camion dans le département des ventes est affecté au centre de coûts du service de ventes. Il n’est pas nécessaire d’affecter le coût salarial à d’autres centres de coûts. Autre exemple : le coût d’un système informatique cher est affecté aux produits de la société qui utilisent ce système.|  
|Ventilation dynamique|Les ventilations dynamiques dépendent des bases de ventilation variables, comme le nombre de salariés du service ou la répartition des ventes du projet au cours d’une période déterminée. Il existe neuf bases de ventilation prédéfinies, que les utilisateurs peuvent définir à l’aide de cinq filtres.|  
|Coût direct|Les coûts directs sont les coûts qui peuvent être directement affectés à un coût associé, par exemple, l’achat d’équipement pour un produit spécifique.|  
|Coût fixe|Les coûts fixes sont les coûts qui ne dépendent pas du niveau des biens ou des services produits par la société. Ils sont temporels, comme le salaire ou le loyer réglé chaque mois, contrairement aux coûts variables, qui dépendent du volume et qui sont payés par quantité produite.|  
|Coût indirect|Les coûts indirects ne sont pas directement imputés à un coût associé, comme une fonction ou un produit donné. Les coûts indirects peuvent être fixes ou variables. Les coûts indirects peuvent être liés aux coûts de fiscalité, d’administration, de personnel et de sécurité, autrement dit, les frais généraux.|  
|Niveau|Le niveau est utilisé pour définir l’ordre d’allocation. Le niveau est défini par un numéro compris entre 1 et 99. La validation de ventilation suit l’ordre des niveaux. Par exemple, le niveau garantit que la première administration est affectée à l’atelier avant d’affecter l’atelier au véhicule et à la production.|  
|Ventilation statique|Les ventilations statiques dépendent d’un ensemble de valeurs fixe, par exemple, les mètres carrés utilisés ou un ratio de ventilation prédéfini, comme 5:2:4.|  
|Coût opérationnel|Les coûts opérationnels sont des dépenses récurrentes liées à l’exploitation d’une activité, d’un périphérique et d’un composant.|  
|Frais généraux|Les frais généraux font référence aux frais d’exploitation continus d’une activité. Les comptes de gestion sont constitués de coûts, à l’exception de la main-d’œuvre directe, des matières premières et des dépenses directes. Les frais généraux comprennent les frais comptables, la publicité, l’amortissement, les assurances, les intérêts, les frais juridiques, le loyer, les réparations, les approvisionnements, les taxes, les factures de téléphone, les frais de déplacement et les coûts de services.|  
|Coût variable par paliers|Les coûts variables par paliers sont parfois soumis à des variations importantes car ils concernent des achats en grande quantité qui ne peuvent pas être répartis dans le temps. Par exemple, un salarié peut produire 100 tables par mois. Son salaire est constant pour une plage de fabrication de 1 à 100 tables. Si la société souhaite obtenir 110 tables, la société a besoin de deux salariés. Le coût sera multiplié par deux.|  
|Part|La portion ou partie répartie dans les centres de coûts ou coûts associés.|  
|Pondération de clé de répartition|Les coûts sont affectés en fonction des clés de ventilation, qui peuvent être modifiées à l’aide d’un multiplicateur. <br />Par exemple, deux départements, comptant respectivement 20 et 10 salariés, partagent les coûts pour la cantine. Les coûts sont répartis entre les départements à l’aide d’une clé de ventilation qui représente le nombre de salariés se restaurant dans la cantine. Dans le premier département, seuls 5 salariés mangent à la cantine. Ainsi, le département a un multiplicateur de 0,25 %. La base de la ventilation est 20 x 0,25 = 5. Le nombre total de salariés mangeant à la cantine s’élève à 15. Un tiers des coûts sont affectés au premier département, et deux tiers sont affectés au second département.|  
|Coût variable|Les coûts variables sont des frais qui varient proportionnellement à l’activité d’une société. Les coûts variables représentent la somme de coûts marginaux dans toutes les unités produites. Les coûts fixes et les coûts variables constituent les deux composants des coûts totaux.|  
|Variante|Une variante est utilisée comme un libellé facultatif et défini par l’utilisateur pour les affectations. Son objectif consiste à filtrer les groupes d’affectation.|  

## <a name="see-also"></a>Voir aussi

 [À propos de la comptabilité analytique](finance-about-cost-accounting.md)  
 [Comptabilité pour les coûts](finance-manage-cost-accounting.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
