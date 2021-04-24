---
title: 'Procédure : Vente d’articles en stock dans des flux à assembler pour commande | Microsoft Docs'
description: Si l’article est configuré pour la fiche d’assemblage pour commande, le processus par défaut de commande vente considère que l’article n’est pas en stock et doit être assemblé pour cette commande vente spécifique. Par conséquent, un ordre d’assemblage lié est automatiquement créé lorsque vous ajoutez l’article à une ligne commande vente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e9c9ba52d6f4f4a7f9af82e381040e545e46f746
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770585"
---
# <a name="sell-inventory-items-in-assemble-to-order-flows"></a>Vente d’articles en stock dans des flux à assembler pour commande
Si le champ **Stratégie d’assemblage** de la fiche article d’un élément d’assemblage indique **Assembler pour commande**, le processus par défaut de commande vente considère que l’article n’est pas en stock et doit être assemblé pour cette commande vente spécifique. Par conséquent, un ordre d’assemblage lié est automatiquement créé lorsque vous ajoutez l’article à une ligne commande vente. Pour plus d’informations, reportez-vous à [Vente d’articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md). Toutefois, si une partie de la quantité sur commande vente est déjà disponible en stock, alors vous pouvez diminuer la quantité d’ordre d’assemblage en changeant le champ **Quantité à assembler pour commande** de la ligne commande vente.  

Ce scénario est rare parce que les articles à assembler pour commande sont toujours censés être personnalisés, et la probabilité qu’il soient en stock dans la configuration qui est demandée par un autre client est faible. Néanmoins, si une société a des quantités à assembler pour commande en stock à cause de retours ou d’annulations de commande, alors ces quantités doivent être prélevées et vendues avant que de nouvelles soient assemblées.  

> [!NOTE]  
>  Aucune fonctionnalité n’existe sur les commandes vente qui vous alerte automatiquement ou vous aide à déduire les quantités d’ordre d’assemblage qui sont déjà disponibles. Au lieu de cela, vous devez contrôler les informations de disponibilité, par exemple dans le récapitulatif **Détails ligne vente**.  

Une fonctionnalité identique est disponible lorsque vous vendez des éléments d’assemblage du stock et une partie ou l’ensemble de la quantité n’est pas disponible et peut être fournie dans un ordre d’assemblage. Pour plus d’informations, voir [Vente simultanée d’articles à assembler pour commande et d’articles en stock](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
>  Certaines règles s’appliquent au champ **Qté à expédier** sur les lignes commande vente qui contiennent une combinaison des quantités à assembler pour commande et les quantités en stock. Pour plus d’informations, voir la section Scénarios de combinaison dans [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md).  

Dans cette procédure, vous remplacez les quantités à assembler pour commande par les quantités en stock sur une ligne commande vente. Les étapes comprennent la vérification des disponibilités existantes, la détection de la quantité de l’ordre d’assemblage associé, puis la réservation de la quantité en stock pour s’assurer qu’elle est prélevée et expédiée pour la commande.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>pour vendre des articles en stock dans des flux à assembler pour commande  
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente**, puis sélectionnez le lien associé.  
2.  Créez une commande client. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).  
3.  Sur une ligne de commande vente pour un article à assembler pour commande, dans le champ **Quantité**, entrez la quantité demandée.  
4.  Dans le récapitulatif **Détails ligne vente**, déterminez si une partie ou la totalité de la quantité demandée est disponible.  
5.  Dans le champ **Quantité à assembler pour commande**, déduisez la quantité disponible de manière à ce que seule la quantité indisponible soit assemblée à la commande. Le champ **Quantité réservée** est diminué en conséquence pour refléter que la relation ordre pour ordre, ou la réservation, s’applique uniquement à la quantité à assembler.  
6.  Sur le raccourci **Lignes**, choisissez **Fonctions**, puis choisissez l’action **Réserver**.  
7.  Sur la page **Réservation**, sélectionnez la ou les lignes d’écriture comptable article qui contiennent des quantités disponibles, sélectionnez **Réserver à partir de la ligne courante**, puis sélectionnez le bouton **OK**.  

    Sur la page **Commande vente**, le champ **Quantité réservée** indique maintenant que l’ensemble de la quantité ligne commande est réservé. Le champ **Quantité à assembler pour commande** indique toujours la sous-quantité qui doit être assemblée.  

8.  Lancez la commande vente pour prélever les articles en stock et assembler les articles indisponibles. Pour plus d’informations, voir [Assembler des articles](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  Le champ **Code emplacement** de la commande vente peut être prérempli en fonction du champ **Code empl. exp. ass. pr comm.** ou du champ **Code empl. depuis assemblage** de la fiche magasin. Dans ce cas, le champ **Code emplacement** de la ligne commande vente peut être incorrect dans cette combinaison des quantités à assembler pour commande et à assembler pour stock. Il est judicieux de consulter le champ **Code emplacement** et de s’assurer que le placement fonctionne pour toutes les quantités. Sinon, entrez les deux quantités différentes sur des lignes commande vente distinctes.  

## <a name="see-also"></a>Voir aussi  
[Gestion des assemblages](assembly-assemble-items.md)  
[Réserver des articles](inventory-how-to-reserve-items.md)  
[Utiliser les nomenclatures](inventory-how-work-BOMs.md)  
[Stock](inventory-manage-inventory.md)  
[Détails de conception : gestion d’entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]