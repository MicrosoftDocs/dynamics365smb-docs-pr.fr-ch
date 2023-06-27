---
title: Description des processus Assembler pour commande et Assembler pour stock
description: Découvrez comment assembler des articles pour des commandes vente ou pour les garder en stock pour les ventes futures.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock" />Description des processus Assembler pour commande et Assembler pour stock

[!INCLUDE [prod_short](includes/prod_short.md)] vous permet de fournir des éléments d’assemblage des manières suivantes :

* Assembler pour commande  
* Assembler pour stock  

## <a name="assemble-to-order" />Assembler pour commande

Utilisez le processus Assembler pour commande pour les articles que vous ne souhaitez pas stocker. Par exemple, pour les raisons suivantes :

* Vous allez personnalisez des articles en fonction des besoins des clients.
* Vous souhaitez minimiser le coût des stocks disponibles.

La liste suivante décrit certains des avantages du processus Assembler pour commande :  

* Personnaliser les éléments d’assemblage lors d’une prise de commande vente.  
* Aperçu de la disponibilité de l’élément d’assemblage et de ses composants.  
* Réserver des composants d’assemblage immédiatement afin de garantir le traitement de la commande.  
* Déterminer la rentabilité de la commande personnalisée par le calcul multi-niveau du prix et du coût.  
* Intégration à l’entrepôt pour faciliter l’assemblage et l’expédition.  
* Utiliser le processus Assembler pour commande lorsque vous créez un devis client ou une commande cadre vente.  
* Combiner les quantités de stock et les quantités à assembler pour commande.  

Dans le processus Assembler pour commande, vous assemblez des articles pour une commande vente. Il existe un lien un-à-un entre l’ordre d’assemblage et la commande vente.  

Quand vous entrez l’article à assembler pour commande dans une ligne commande vente, un ordre d’assemblage est automatiquement créé. L’ordre d’assemblage est basé sur la ligne vente et ses lignes sont basées sur la nomenclature d’assemblage de l’article. La quantité de composants sur la nomenclature d’assemblage est multipliée par la quantité commandée. La page **Lignes Assembler pour commande** affiche des détails sur les lignes de commande d’assemblage liées. Les détails peuvent vous aider à personnaliser l’élément d’assemblage. La date de livraison est basée sur la disponibilité des composants. Pour en savoir plus sur l’assemblage d’articles pour les commandes vente, consultez [Vente d’articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
> Bien que cette tâche ne fasse pas partie du processus par défaut, vous pouvez vendre des quantités de stock et des quantités à assembler pour commande sur la même commande vente. Pour en savoir plus sur la combinaison d’articles en stock et d’articles à assembler pour commande, consultez [Vente d’articles en stock dans des flux à assembler pour commande](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

Pour spécifier qu’un article est assemblé pour commande, dans le champ **Stratégie d’assemblage** sur la page **Fiche article** pour l’article, choisissez **Assembler pour commande**.  

## <a name="assemble-to-stock" />Assembler pour stock

Utilisez le processus Assembler pour stock pour les articles que vous assemblez et stockez pour les ventes futures. Les articles à assembler pour stock sont des articles standard, tels que des kits emballés, que vous ne personnalisez pas. Vous pouvez également consommer ces articles en tant que composants de sous-assemblage. Les articles sont prélevés et traités comme des articles individuels et sont traités comme des articles de production finis. Pour en savoir plus sur les éléments d’assemblage, consultez [Assembler des articles](assembly-how-to-assemble-items.md).  

Lorsque vous spécifiez un article à assembler pour stock sur une ligne vente, l’article est traité comme tout autre article vendu à partir du stock. Par exemple, [!INCLUDE [prod_short](includes/prod_short.md)] vérifie uniquement la disponibilité de l’article assemblé, et non de ses composants.  

> [!NOTE]  
> Bien que cette tâche ne fasse pas partie du processus par défaut, vous pouvez assembler un article pour commande même s’il est configuré pour être assemblé pour stock. Pour plus d’informations, voir [Vente simultanée d’articles à assembler pour commande et d’articles en stock](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Pour spécifier qu’un article est assemblé pour stock, dans le champ **Stratégie d’assemblage** sur la page **Fiche article** pour l’article, choisissez **Assembler pour stock**.  

## <a name="combination-scenarios" />Scénarios de combinaison

Lorsque les quantités à assembler pour commande et des quantités en stock sont combinées sur une commande vente, les quantités à assembler pour commande doivent être expédiées en premier.  

Si un ordre d’assemblage est lié à une ligne commande vente, la valeur du champ **Qté vers Assembler pour commande** sur la ligne commande vente est copiée dans le champ **Quantité à assembler** via le champ **Quantité** dans l’ordre d’assemblage. Learn more at [Vente d’articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).  

La valeur du champ **Quantité à assembler** est liée au champ **Qté à expédier** sur la ligne commande vente. Cette relation gère la façon dont vous expédiez des quantités partielles et complétez les quantités à assembler pour commande :

* Lorsque la quantité totale sur la ligne commande vente est assemblée pour commande
* Dans les scénarios de combinaison où une partie de la quantité est assemblée pour commande et une autre partie est expédiée à partir du stock.

Le scénario de combinaison permet la flexibilité pour les expéditions partielles. Vous pouvez utiliser le champ **Quantité à assembler** pour spécifier la quantité à expédier partiellement à partir du stock et à assembler pour commande.  

Si toute la quantité de la ligne vente doit être assemblée pour commande et expédiée, la valeur du champ **Qté à expédier** est copiée dans le champ **Quantité à assembler** de l’ordre d’assemblage lié lorsque vous modifiez la quantité à expédier. Cette mise à jour assure que la quantité expédiée est entièrement approvisionnée par la quantité à assembler pour commande.  

Toutefois, dans les scénarios de combinaison, la valeur du champ **Qté à expédier** n’est pas copiée dans le champ **Quantité à assembler** de l’ordre d’assemblage. Au lieu de cela, une valeur par défaut est insérée dans le champ **Quantité à assembler**. La valeur est calculée à partir du champ **Qté à expédier** pour assurer que les quantités assemblées pour commande sont expédiées en premier.

Pour utiliser une valeur autre que celle par défaut, par exemple parce que vous souhaitez uniquement assembler une quantité supérieure ou inférieure à celle indiquée dans le champ **Qté à expédier**, vous pouvez modifier le champ **Quantité à assembler**, mais uniquement dans le cadre de règles prédéfinies, comme illustré ci-dessous.  

Par exemple, la raison pour laquelle vous voudriez modifier la quantité à assembler peut être liée au souhait de valider partiellement l’expédition des quantités en stock avant d’expédier le résultat de l’assemblage.  

Les tables suivantes expliquent les règles qui définissent les valeurs minimale et maximale que vous pouvez saisir dans le champ **Quantité à assembler** pour spécifier une valeur autre que celle par défaut dans un scénario de combinaison. Le tableau affiche un scénario de combinaison dont le champ **Qté. à expédier** de la ligne commande vente liée passe de 7 à 4 ; le champ **Quantité à assembler** prend donc par défaut la valeur 4.  

**Ligne commande vente**

|                | **Quantité** | **Qté à expédier** | **Qté vers Assembler pour commande** | **Qté expédiée** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Valeur initiale**| 10          | 7                | 7                             | 0                    |
|**Modification**      |              | 4                |                               |                      |

**En-tête d’ordre d’assemblage**

|                | **Quantité** | **Qté à expédier** | **Qté vers Assembler pour commande** | **Qté expédiée** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Valeur initiale**| 7           | 7                | 0                             | 7                    |
|**Modification**      |              | 4 (valeur insérée par défaut)|                         |                      |

D’après cet exemple, vous pouvez modifier le champ **Quantité à assembler** comme suit :  

* La quantité minimum que vous pouvez saisir est 1. Vous devez assembler au moins une unité pour pouvoir vendre les quatre, en supposant que les trois autres soient disponibles dans le stock.  
* La quantité maximum que vous pouvez saisir est 4. Cette limite garantit que vous n’assemblez pas plus d’articles que nécessaire pour la vente.  

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/paths/assemble-items-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi

[Gestion des assemblages](assembly-assemble-items.md)  
[Utilisation des nomenclatures d’assemblage](assembly-how-work-assembly-boms.md)  
[Stock](inventory-manage-inventory.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
