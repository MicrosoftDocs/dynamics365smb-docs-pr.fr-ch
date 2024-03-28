---
title: "Procédure\_: créer des commandes spéciales"
description: Découvrez comment créer une commande spéciale pour un article de catalogue spécifique à expédier à un client particulier.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-special-orders"></a>Créer des commandes spéciales

Vous pouvez créer une commande spéciale pour un article de catalogue spécifique à expédier à un client particulier. Le fournisseur expédie l’article à votre entrepôt et vous pouvez ensuite l’expédier à votre client seul ou avec d’autres articles issus d’autres commandes.  

Dans le cadre d’une commande spéciale, la commande achat et la commande vente sont liées pour s’assurer que l’article de catalogue précis est prélevé et expédié au client.  

Pour pouvoir utiliser cette fonction, vous devez d’abord configurer les fiches client, fournisseur, et article nécessaires à la commande.  

## <a name="to-create-a-special-order"></a>Pour créer une commande spéciale

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commande vente**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**. Créez et renseignez une commande vente pour l’article. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).
3.  Sous le raccourci **Lignes**, renseignez la ligne vente. Dans le champ **Procédure achat**, sélectionnez une procédure achat dont le champ **Commande spéciale** est sélectionné.

    Vous devez maintenant créer une commande achat à partir d’une demande achat.  
4. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Demande d’achat**, puis sélectionnez le lien associé.  
5. Choisissez l’action **Commande spéciale**, puis choisissez l’option **Extraire commandes vente**.  
6.  Sur la page **Extraire commandes vente**, affichez les résultats dans lesquels le **N° document** correspond au numéro de commande vente. Cliquez sur le bouton **OK**. Une ligne demande achat est créée pour l’article.  
7.  Dans la ligne demande achat, sélectionnez **Nouveau** dans le champ **Message d’action**.  
8.  Sur la page **Demande achat**, sélectionnez l’action **Traiter messages d’action**. La page **Traiter messages d’action - Demande** s’affiche. Choisissez le bouton **OK**.  

    Le message qui s’affiche indique que les commandes achat ont été créées. Cliquez sur le bouton **OK**.  

Une commande achat créée comme commande spéciale pour une commande client est respectée par le système de planification lorsqu’il équilibre l’offre et la demande. Ainsi, la commande achat (approvisionnement) reste liée à la commande vente (demande), même si cette commande achat pourrait approvisionner une autre demande antérieure. Pour plus d’informations, voir [Détails de conception : méthodes de réapprovisionnement](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Vous ne pouvez pas utiliser la fonctionnalité de commande spéciale si l’élément est déjà réservé. Par conséquent, pour les articles qui sont vendus en commandes spéciales, assurez\-vous que le champ **Réserver** sur la fiche article n’est pas défini sur **Toujours**.  

## <a name="see-also"></a>Voir aussi

[Utilisation des articles de catalogue](inventory-how-work-nonstock-items.md)  
[Ventes](sales-manage-sales.md)  
[Effectuer des livraisons directes](sales-how-drop-shipment.md)   
[Détails de conception : méthodes de réapprovisionnement](design-details-reservation-order-tracking-and-action-messaging.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
