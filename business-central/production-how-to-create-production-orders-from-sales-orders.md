---
title: Créer des ordres de fabrication à partir de commandes achat
description: Découvrez différentes façons de créer des ordres de fabrication pour les articles produits directement à partir des commandes vente.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '99000883, 99000884,'
---
# <a name="create-production-orders-from-sales-orders" />Créer des ordres de fabrication à partir de commandes achat

Vous pouvez créer des ordres de fabrication pour les articles produits directement à partir des commandes vente.  

## <a name="to-create-a-production-order-from-a-sales-order" />Pour créer un ordre de fabrication à partir d’une commande achat

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Sélectionnez la commande vente pour laquelle vous voulez créer un ordre de fabrication.  
3. Sélectionnez l’action **Planification**. La page **Planification commande vente** affiche la disponibilité de l’article.  
4. Sélectionnez l’action **Créer O.F**.  
5. Sélectionnez le statut et le type de commande.  
6. Choisissez le bouton **Oui** pour créer un ou plusieurs ordres de fabrication pour les lignes ayant **Ordre de fabrication** dans le champ **Système réapprovisionnement**.

    > [!NOTE]  
    > Les lignes de demandes qui ont **Ordre de fabrication** dans le champ **Système réappro.** représentent des ordres de fabrication sous-jacents. Après avoir généré ces ordres de fabrication, n’oubliez pas d’identifier toute demande de composants non satisfaite. Utilisez la page **Planning commande** ou l’action **Replanifier** pour identifier la demande non satisfaite.
    >
    > Lorsque vous créez des ordres de fabrication pour des commandes client avec la page Planification commande vente, des liens ordre pour ordre sont appliqués entre la demande et l’approvisionnement. Lorsque les liens ordre pour ordre existent, le système de planification n’inclut pas d’approvisionnement ou de stock lié dans la procédure d’équilibrage. Pour en savoir plus sur l’équilibrage, consultez [Liens ordre pour ordre](design-details-central-concepts-of-the-planning-system.md#order-to-order-links).

## <a name="order-type" />Type de commande

Le tableau suivant décrit deux manières de créer des ordres de fabrication.

|Option|Description|
|------|-----------|
|O.F. article|Un ordre de fabrication est créé pour chaque article représenté par une ligne sur la page **Planification commande vente**.|
|O.F. projet|Un ordre de fabrication multiligne est créé pour tous les articles représentés par des lignes sur la page **Planification commande vente**. Lorsque vous utilisez des O.F. projet, le champ **Type de source** de l’ordre de fabrication contient **En-tête vente**. L’ordre comporte une ligne pour chaque article de ligne de vente qui doit être produit.|

## <a name="see-also" />Voir aussi

[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)  
[Pratiques de configuration recommandées : planification de l’approvisionnement](setup-best-practices-supply-planning.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
