---
title: "Détails de conception\_: Validation d’ordre de fabrication | Microsoft Docs"
description: 'Comme pour la validation d’ordre d’assemblage, les composants consommés et le temps du poste utilisé sont convertis et sortis en tant qu’article produit lorsque l’ordre de fabrication est terminé.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-production-order-posting" />Détails de conception : validation d’ordre de fabrication
Comme pour la validation d’ordre d’assemblage, les composants consommés et le temps du poste utilisé sont convertis et sortis en tant qu’article produit lorsque l’ordre de fabrication est terminé. Pour plus d’informations, voir [Détails de conception : modes évaluation stock](design-details-assembly-order-posting.md). Toutefois, le flux des coûts des ordres d’assemblage est moins complexe, notamment parce que la validation du coût d’assemblage ne se produit qu’une fois et ne génère donc pas de stock encours.


Les transactions se produisant pendant le processus de fabrication peuvent être suivies à travers les étapes suivantes :  

1.  Achat de matériels et autres entrées de fabrication.  
2.  Conversion en travaux en cours.  
3.  Conversion en stock de produits finis.  
4.  Vente des produits finis.  

Par conséquent, outre les comptes stock réguliers, une société manufacturière doit déterminer trois comptes de stock distincts pour enregistrer les transactions à différentes étapes de la production.  

|Compte stocks|Désignation|  
|-----------------------|---------------------------------------|  
|**Compte matières premières**|Inclut le coût de matières premières achetées mais pas encore transférées vers la production. Le solde dans le compte de matières premières indique le coût des matières premières disponibles.<br /><br /> Lorsque les matières premières entrent dans le service de production, le coût des matières est transféré du compte Matières premières au compte TEC.|  
|**Compte en-cours**|Additionne les coûts exposés pendant la production dans la période comptable. Le compte TEC est débité du coût de matières premières qui sont transférées à partir de l’entrepôt des matières premières, le coût du travail direct effectué, et les frais généraux de fabrication encourus.<br /><br /> Le compte TEC est crédité pour le coût de fabrication total d’unités qui sont renseignées dans l’usine et transférées vers l’entrepôt des produits finis.|  
|**Compte de produits finis**|Ce compte inclut le coût total de fabrication d’unités qui sont renseignées mais pas encore vendues. Au moment de la vente, le coût des unités vendues est transféré du compte de produits finis sur le compte coût des biens vendus.|  

La valeur du stock est calculée en suivant les coûts de toutes les augmentations et diminutions, comme exprimé par l’équation suivante :  

* valeur du stock = solde d’ouverture du stock + valeur de toutes les entrées - valeur de toutes les sorties  

Selon le type de stock, les augmentations et diminutions sont représentées par des transactions différentes.  

||Entrées|Sorties|  
|-|---------------|---------------|  
|**Stock de matières premières**|-   Achats nets de matériel<br />-   Production de produits semi-finis<br />-   Consommation négative|Consommation matière|  
|**Stock en-cours**|-   Consommation matière<br />-   Consommation de capacité<br />-   Frais généraux matière|Production de produits finis (coût de produits fabriqués)|  
|**Stock de produits finis**|Production de produits finis (coût de produits fabriqués)|-   Ventes (coût des biens vendus)<br />-   Production négative|  
|**Stock de matières premières**|-   Achats nets de matériel<br />-   Production de produits semi-finis<br />-   Consommation négative|Consommation matière|  

Les valeurs des augmentations et des diminutions sont stockées dans les différents types de stock manufacturé de la même manière que pour le stock acheté. Chaque fois qu’une transaction d’entrée de stock ou de sortie a lieu, une écriture comptable article et une écriture comptable correspondante sont créées pour le montant. Pour plus d’informations, voir [Détails de conception : comptabilisation stock](design-details-inventory-posting.md).  

Bien que les valeurs des transactions qui sont liées aux produits achetés soient validées uniquement en tant qu’écritures comptables article comportant des écritures valeur associées, les transactions liées aux articles fabriqués sont validées en tant qu’écritures comptables capacité comportant des écritures valeur associées, en plus des écritures comptables article.  

## <a name="posting-structure" />Structure de validation
Valider les ordres de fabrication sur le stock en-cours implique la production, la consommation et la capacité.  

Le schéma suivant montre les routines de validation impliquées dans le codeunit 22.  

![Routines de validation des ordres de fabrication.](media/design_details_inventory_costing_14_production_posting_1.png "Routines de validation des ordres de fabrication")  

Le schéma suivant montre les associations entre les écritures générées et les objets de coût.  

![Flux d’écritures de production.](media/design_details_inventory_costing_14_production_posting_2.png "Flux d’écritures de production")  

L’écriture comptable capacité décrit la consommation de la capacité en termes d’unités de temps, alors que l’écriture valeur associée décrit la valeur de la consommation de capacité spécifique.  

L’écriture comptable article décrit la consommation ou la production de matière en termes de quantités, alors que l’écriture valeur associée décrit la valeur de consommation ou production de cette matière spécifique.  

Une écriture valeur qui décrit la valeur du stock en-cours peut être associée à l’une des combinaisons suivantes de coûts associés :  

-   Une ligne O.F., un centre ou un poste de charge, et une écriture comptable capacité.  
-   Une ligne O.F., un article et une écriture comptable article.  
-   Uniquement une ligne O.F.  

Pour plus d’informations sur la manière dont les coûts de fabrication et d’assemblage sont validés dans la comptabilité, reportez-vous à [Détails de conception : comptabilisation stock](design-details-inventory-posting.md).  

## <a name="capacity-posting" />Validation de capacité
Valider la production à partir de la dernière ligne gamme O.F. a pour résultat la création d’une écriture comptable capacité pour le produit fini, en plus de son entrée de stock.  

 L’écriture comptable capacité est un enregistrement du temps qui a été passé à fabriquer l’article. L’écriture valeur liée décrit l’augmentation de la valeur stock TEC, qui est la valeur du coût de conversion. Pour plus d’informations, consultez « À partir de la comptabilité capacité » dans [Détails de conception : Comptes de la comptabilité](design-details-accounts-in-the-general-ledger.md).  

## <a name="production-order-costing" />Évaluation des coûts de l’ordre de fabrication
 Pour contrôler le stock et les coûts de production, une société manufacturière doit mesurer le coût des ordres de fabrication, car le coût standard prédéterminé de chaque article produit est capitalisé dans le bilan. Pour plus d’informations sur la raison pour laquelle les articles produits utilisent le mode évaluation stock Standard, reportez-vous à [Détails de conception : modes évaluation stock](design-details-costing-methods.md).  

> [!NOTE]  
>  Dans des environnements qui n’utilisent pas le mode évaluation stock standard, le coût réel plutôt que le coût standard des articles produits est capitalisé sur le bilan.  

Le coût réel d’un ordre de fabrication comprend les composants coût suivants :  

-   Coût matière réel  
-   Coût opératoire ou coût de sous-traitance réel  
-   Frais généraux matière  

Ces coûts réels sont validés sur la commande de production et comparés au coût standard pour calculer les variations. Les écarts sont calculés pour chaque composant des coûts article : matières premières, capacité, sous-traitant, frais généraux opératoires et frais généraux de fabrication. Les écarts peuvent être analysés pour déterminer les problèmes, comme les déchets excessifs en traitement.  

Dans des environnements de coût standard, l’évaluation du stock d’un ordre de fabrication est basée sur le mécanisme suivant :  

1.  Lorsque la dernière opération de routage est validée, le coût de l’ordre de fabrication est validé dans l’écriture article et défini sur le coût prévu.  

    Ce coût correspond à la quantité produite validée dans la feuille de production multipliée par le coût standard qui est copié à partir de la fiche article. Le coût est traité en tant que coût prévu jusqu’à ce que l’ordre de fabrication soit terminé. Pour plus d’informations, voir [Détails de conception : validation du coût prévu](design-details-expected-cost-posting.md).  

    > [!NOTE]  
    >  Ceci diffère de la validation d’ordre d’assemblage, qui valide toujours les coûts réels. Pour plus d’informations, voir [Détails de conception : modes évaluation stock](design-details-assembly-order-posting.md).  
2.  Lorsque l’ordre de fabrication est défini sur **Finished**, la commande est facturée en exécutant le traitement par lots **Adjust Cost-Item Entries**. Par conséquent, le coût total de la commande est calculé en fonction du coût standard des matières et de la capacité consommées. Les écarts entre les coûts standard calculés et les coûts de production réels sont calculés et enregistrés.  

## <a name="see-also" />Voir aussi
 [Détails de conception : évaluation stock](design-details-inventory-costing.md)   
 [Détails de conception : validation d’ordre d’assemblage](design-details-assembly-order-posting.md)  
 [Gestion des coûts ajustés](finance-manage-inventory-costs.md) [Finance](finance.md)  
 [Utiliser Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
