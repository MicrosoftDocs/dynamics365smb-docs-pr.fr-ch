---
title: Établissement d’un devis de vente Assembler pour commande
description: Vous pouvez utiliser la gestion nomenclature d’assemblage pour personnaliser un élément d’assemblage sur la demande d’un client au cours du processus de vente.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Établissement d’un devis de vente Assembler pour commande

Vous pouvez utiliser la gestion nomenclature d’assemblage pour personnaliser un élément d’assemblage sur la demande d’un client au cours du processus de vente. Pour plus d’informations, reportez-vous à [Vente d’articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).  

Lorsque vous vendez tout autre type d’article, vous pouvez également créer un devis pour un élément d’assemblage personnalisé avant de le convertir en commande vente. Ce processus implique plusieurs étapes supplémentaires lorsque vous le comparez à la création d’un devis normal et il recourt à une variation d’un ordre d’assemblage associé, qui est un devis d’assemblage.

> [!NOTE]  
>  Comme tous les types de devis, les quantités sur les devis d’assemblage ne sont pas utilisées en termes de disponibilité, planification ou réservations.  

## Créer un devis pour un article à assembler pour commande

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Devis**, puis sélectionnez le lien associé.  
2.  Créez une ligne devis avec une ligne pour un élément d’assemblage. Pour plus d’informations, voir [Créer des devis](sales-how-make-offers.md).  
3.  Dans le champ **Quantité à assembler pour commande**, entrez la quantité entière.

    > [!NOTE]  
    >  Vous ne devez pas établir un devis pour une quantité partielle. Par conséquent, vous devez entrer la même quantité que vous avez saisie dans le champ **Quantité** de la ligne devis.  

4.  Sur le raccourci **Lignes**, sélectionnez **Ligne**, puis **Assembler pour commande** et **Lignes d’assemblage pour commande**. Sinon, choisissez le champ **Quantité à assembler pour commande** sur la ligne.  
5.  Sur la page **Lignes d’assemblage pour commande**, vérifiez ou modifiez les lignes d’assemblage pour commande en fonction du devis demandé par le client. Des informations supplémentaires sont disponibles en choisissant **Afficher document** pour ouvrir la commande devis ouverte complète. Vous ne pouvez pas modifier le contenu de la plupart des champs, et vous ne pouvez pas valider.  
6.  Lorsque vous avez ajusté les lignes d’ordre d’assemblage en fonction du devis, fermez la page **Lignes d’assemblage pour commande** pour revenir à la page **Devis**.  
7.  Si le client accepte le devis, créez une commande vente pour l’élément d’assemblage qui a fait l’objet du devis. Pour plus d’informations, voir [Créer des devis](sales-how-make-offers.md). Le devis d’assemblage associé et toutes les personnalisations sont liées à cette nouvelle commande vente à préparer pour l’assemblage de l’article ou des articles à vendre.  

## Voir aussi

[Gestion nomenclature d’assemblage](assembly-assemble-items.md)  
[Utilisation des nomenclatures d’élément d’assemblage](assembly-how-work-assembly-boms.md)  
[Stock](inventory-manage-inventory.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
