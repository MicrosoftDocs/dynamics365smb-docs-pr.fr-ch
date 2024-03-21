---
title: Vente d’articles en stock dans des flux à assembler pour commande
description: Les articles à assembler pour commande sont assemblés pour les commandes vente via un ordre d’assemblage.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.service: dynamics-365-business-central
---
# Vendre des éléments de stocks dans des flux à assembler pour commande

Si le champ **Stratégie d’assemblage** de la fiche article d’un élément d’assemblage indique **Assembler pour commande**, le processus par défaut de commande vente considère que l’article n’est pas en stock et doit être assemblé pour les commandes vente. Quand vous ajoutez l’article à une ligne d’une commande vente, [!INCLUDE [prod_short](includes/prod_short.md)] crée un ordre d’assemblage lié à la commande vente. Pour en savoir plus sur la vente d’articles à assembler pour commande, consultez [Vente d’articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md). Toutefois, si une partie de la quantité sur commande vente est déjà disponible en stock, vous pouvez diminuer la quantité d’ordre d’assemblage en changeant le champ **Quantité à assembler pour commande** de la ligne commande vente.  

Il est relativement rare que les entreprises vendent des articles en stock en tant qu’articles assemblés pour commande. Les articles à assembler pour commande ne sont généralement pas standard. Ils sont personnalisés pour répondre aux exigences spécifiques des clients. Cependant, vous pouvez avoir des quantités d’articles assemblés pour commande en stock en raison de retours ou d’annulations de commandes. Ces quantités doivent être prélevées et vendues avant que les nouvelles ne soient assemblées.  

> [!NOTE]  
> Pour vérifier si les articles assemblés pour commande sont déjà disponibles pour les ordres d’assemblage, utilisez le récapitulatif **Détails ligne vente** sur la commande client.  

Vous pouvez faire des choses similaires lorsque vous vendez des éléments d’assemblage à partir du stock et que tout ou partie de la quantité n’est pas disponible. Vous pouvez fournir la quantité manquante via un ordre d’assemblage. Pour plus d’informations sur la vente d’articles en stock et assemblés, consultez [Vente simultanée d’articles à assembler pour commande et d’articles en stock](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
> Des règles s’appliquent au champ **Qté à expédier** sur les lignes commande vente qui contiennent une combinaison des quantités à assembler pour commande et les quantités en stock. Pour en savoir plus sur les règles, consultez [Scénarios de combinaison](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Dans cette procédure, vous remplacez les quantités à assembler pour commande par les quantités en stock sur une ligne commande vente. Les étapes suivantes donnent une vue d’ensemble :

1. Déterminer la disponibilité.
2. Réduire cette quantité à partir de l’ordre d’assemblage lié.
3. Réserver la quantité en stock pour vous assurer qu’elle est prélevée et expédiée pour la commande.  

## pour vendre des articles en stock dans des flux à assembler pour commande

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Créez une commande client. Pour plus d’informations sur la créations de commandes vente, consultez [Vendre des produits](sales-how-sell-products.md).  
3. Sur une ligne de commande vente contenant un article à assembler pour commande, dans le champ **Quantité**, entrez la quantité.  
4. Dans le récapitulatif **Détails ligne vente**, déterminez si une partie ou la totalité de la quantité est disponible.  
5. Dans le champ **Quantité à assembler pour commande**, déduisez la quantité disponible de manière à ce que seule la quantité indisponible soit assemblée à la commande. Le champ **Quantité réservée** est diminué en conséquence pour refléter que la relation ordre pour ordre, ou la réservation, s’applique uniquement à la quantité à assembler.  
6. Sur le raccourci **Lignes**, choisissez **Fonctions**, puis choisissez l’action **Réserver**.  
7. Sur la page **Réservation**, sélectionnez la ou les lignes d’écriture comptable article qui contiennent des quantités disponibles, sélectionnez **Réserver à partir de la ligne courante**, puis sélectionnez le bouton **OK**.  

    Sur la page **Commande vente**, le champ **Quantité réservée** indique maintenant que la quantité entière de la ligne commande est réservée. Le champ **Quantité à assembler pour commande** indique toujours la quantité à assembler.  

8. Lancez la commande vente pour rendre les articles disponibles pour le prélèvement et pour l’assemblage des articles indisponibles. Pour en savoir plus sur les éléments d’assemblage, consultez [Assembler des articles](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Le champ **Code emplacement** de la commande vente peut contenir la valeur provenant des champs **Code empl. exp. ass. pr comm.** ou **Code empl. depuis assemblage** de la fiche magasin. Si c’est le cas, le champ **Code emplacement** de la ligne commande vente peut être incorrect pour cette combinaison des quantités à assembler pour commande et à assembler pour stock. Il est bon de revérifier que l’emplacement dans le champ **Code emplacement** fonctionne pour toutes les quantités. Sinon, entrez les deux quantités différentes sur des lignes commande vente distinctes.  

## Voir aussi

[Gestion nomenclature d’assemblage](assembly-assemble-items.md)  
[Réservation des articles](inventory-how-to-reserve-items.md)  
[Utilisation des nomenclatures d’élément d’assemblage](assembly-how-work-assembly-boms.md)  
[Stock](inventory-manage-inventory.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
