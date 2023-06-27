---
title: Vente simultanée d’articles à assembler pour commande et d’articles en stock
description: 'Si une partie d’un article à assembler pour stock n’est pas disponible, vous pouvez créer un ordre d’assemblage pour la quantité restante.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Vente simultanée d’articles à assembler pour commande et d’articles en stock

Si le champ **Stratégie d’assemblage** de la fiche article d’un élément d’assemblage indique **Assembler pour stock**, le processus de commande vente se base sur l’hypothèse que l’article est déjà assemblé et peut être prélevé du stock, s’il est disponible. Par conséquent, aucun ordre d’assemblage n’est automatiquement créé et n’est lié à la ligne commande vente. Toutefois, si une partie ou la totalité de la quantité n’est pas disponible, vous pouvez créer un ordre d’assemblage pour la quantité restante. Pour ce faire, remplissez le champ **Qté. à assembler pour commande** sur la ligne commande vente. Ce paramètre vous permet d’assembler l’article pour commande même s’il est configuré pour être assemblé pour stock.  

Vous disposez d’une flexibilité similaire lorsque vous vendez des articles à assembler pour commande et qu’une partie de la quantité est déjà en stock. Vous devrez déduire cette quantité de l’ordre d’assemblage. Pour en savoir plus sur la vente d’articles en stock, consultez [Vente d’articles en stock dans des flux à assembler pour commande](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
> Des règles s’appliquent au champ **Qté à expédier** sur les lignes commande vente qui contiennent une combinaison des quantités à assembler pour commande et les quantités en stock. Pour en savoir plus sur les règles, consultez [Scénarios de combinaison](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

> [!NOTE]  
> La procédure suivante n’inclut pas les étapes de commande vente que vous devez suivre avant de créer un ordre d’assemblage pour les quantités indisponibles.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Pour vendre des articles à assembler pour commande et des articles de stock ensemble

1. Sur une ligne commande vente pour un article à assembler pour stock, entrez une quantité dans le champ **Quantité** qui est supérieure au stock. La page **Vérifier disponibilité** s’affiche. Pour en savoir plus sur la disponibilité des articles, consultez [Afficher la disponibilité des articles](inventory-how-availability-overview.md).
2. Dans le champ **Quantité à assembler pour commande**, entrez la valeur du champ **Quantité totale**.  
3. Exécutez toutes les modifications nécessaires aux composants d’assemblage. Learn more at [Vente d’articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).  
4. Lancez la commande vente pour rendre les articles disponibles pour le prélèvement et pour l’assemblage des articles indisponibles. Pour en savoir plus sur les étapes d’assemblage standard, consultez [Assembler des articles](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Le champ **Code emplacement** de la commande vente peut contenir la valeur provenant des champs **Code empl. exp. ass. pr comm.** ou **Code empl. depuis assemblage** de la fiche magasin. Si c’est le cas, le champ **Code emplacement** de la ligne commande vente peut être incorrect pour cette combinaison des quantités à assembler pour commande et à assembler pour stock. Il est bon de revérifier que l’emplacement dans le champ **Code emplacement** fonctionne pour toutes les quantités. Sinon, entrez les deux quantités différentes sur des lignes commande vente distinctes.  

## <a name="see-also"></a>Voir aussi

[Gestion des assemblages](assembly-assemble-items.md)  
[Utilisation des nomenclatures d’assemblage](assembly-how-work-assembly-boms.md)  
[Stock](inventory-manage-inventory.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
