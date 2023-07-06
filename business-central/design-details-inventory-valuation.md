---
title: Détails de conception - Évaluation du stock | Microsoft Docs
description: L’évaluation du stock est la détermination du coût d’un article de stock.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-inventory-valuation"></a><a name="design-details-inventory-valuation"></a><a name="design-details-inventory-valuation"></a>Détails de conception : évaluation du stock
L’évaluation du stock est la détermination du coût qui est affecté à un article du stock, comme exprimé par l’équation suivante.  

Fin inventaire = Début inventaire + achats nets – coût des biens vendus  

Le calcul de l’évaluation du stock utilise le champ **Coût total (réel)** des écritures valeur pour l’article. Les écritures sont classées en fonction du type d’écriture correspondant aux composants de coût, au coût direct, au coût indirect, à l’écart, à la réévaluation et à l’arrondi de coût. Pour plus d’informations, voir [Détails de conception : composants des coûts](design-details-cost-components.md).  

Les entrées sont lettrées les unes en fonction des autres, soit par un lettrage fixe, soit en fonction du principe général coût-flux défini par le mode d’évaluation du stock. Une écriture de sortie de stock peut être lettrée avec plusieurs écritures d’entrée avec des dates comptabilisation différentes et éventuellement différents coûts d’acquisition. Pour plus d’informations, voir [Détails de conception : traçabilité](design-details-item-application.md). Par conséquent, le calcul de la valeur de stock d’une date donnée est basée sur l’ajout des écritures valeur positives et négatives.  

## <a name="inventory-valuation-report"></a><a name="inventory-valuation-report"></a><a name="inventory-valuation-report"></a>État Évaluation du stock
Pour calculer la valeur du stock dans le rapport **Évaluation du stock**, le rapport commence par calculer la valeur de stock de l’article à une date de début donnée. Il ajoute la valeur des entrées de stock et soustrait la valeur des sorties de stock jusqu’à une date fin donnée. Le résultat final est la valeur stock à la date fin. L’état calcule ces valeurs en additionnant les valeurs dans le champ **Coût total (réel)** dans les écritures valeur, à l’aide des dates comptabilisation en tant que filtres.  

L’état imprimé affiche toujours les montants réels, c’est-à-dire le coût des écritures qui ont été validées comme étant facturées. L’état imprime également le coût prévu des écritures validées comme étant réceptionnées ou livrées, si vous sélectionnez le champ Inclure coûts prévus sur le raccourci Options.  

> [!IMPORTANT]  
>  Les valeurs dans le rapport **Évaluation du stock** sont rapprochées au compte Inventory dans la comptabilité, ce qui signifie que les écritures valeur en question ont été validées en comptabilité.  

> [!IMPORTANT]  
>  Les montants des colonnes **Valeur** de l’état sont basés sur la date de comptabilisation des transactions d’un article.  

## <a name="inventory-valuation---wip-report"></a><a name="inventory-valuation---wip-report"></a><a name="inventory-valuation---wip-report"></a>Évaluation du stock - État des travaux en cours
Une société manufacturière doit déterminer la valeur de trois types de stock :  

* Stock de matières premières  
* Stock en-cours  
* Stock de produits finis  

La valeur du stock TEC est déterminée par l’équation suivante :  

* Fin stock en-cours = début stock en-cours + coût de fabrication – coût des produits fabriqués  

À l’instar du stock des achats, les écritures valeur constituent la base de l’évaluation du stock. Le calcul est effectué à l’aide des valeurs du champ **Coût total (réel)** des écritures valeur article et de capacité associées à un ordre de fabrication.  

L’objectif de l’évaluation du stock TEC est de déterminer la valeur des articles dont la fabrication n’a pas encore été terminée à une date donnée. Par conséquent, la valeur stock TEC est basée sur les écritures valeur associées à la consommation et aux écritures comptables de capacité. Les écritures comptables de consommation doivent être entièrement facturées à la date de l’évaluation. Par conséquent, l’état **Inventory Valuation – WIP** indique les coûts représentant la valeur stock TEC pour deux catégories : consommation et capacité.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi
[Détails de conception : rapprochement de comptabilité](design-details-reconciliation-with-the-general-ledger.md)   
[Détails de conception : réévaluation](design-details-revaluation.md)   
[Détails de conception : validation d’ordre de fabrication](design-details-production-order-posting.md)
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
