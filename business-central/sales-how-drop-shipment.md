---
title: Faire des livraisons directes (contient une vidéo)
description: Décrit comment créer une commande vente liée à une commande achat pour permettre la livraison directe du fournisseur au client.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Effectuer des livraisons directes

Lors d’une livraison directe, un ou plusieurs articles de l’un de vos fournisseurs sont livrés directement chez l’un de vos clients.

Lorsqu’une commande vente est marquée pour la livraison directe, et lorsque vous créez une commande achat précisant le client dans le champ **Destinataire**, **Adresse client**, vous pouvez associer les deux documents pour demander au fournisseur de faire directement la livraison au client.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## Pour créer une commande vente pour des livraisons directes

Pour préparer une livraison directe, vous créez une commande vente pour un article et indiquer sur la ligne vente que la vente exige la livraison directe.

1. Créez une commande vente pour un article. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).
2. Sur la ligne commande vente pour l’article envoyé, cochez la case **Livraison directe**. 

> [!TIP]
> Par défaut, la case à cocher Livraison directe n’est pas disponible sur les lignes. Si ce n’est pas le cas, vous pouvez l’ajouter en personnalisant la section de page qui contient les lignes. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

## Pour créer la commande achat pour livraison directe

Pour préparer une livraison directe, vous indiquez sur la commande achat qu’elle doit être expédiée à votre client, et non à vous-même.

1. Créez une commande achat. Ne remplissez aucun champ sur les lignes. Pour plus d’informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md).
2. Dans le champ **Destinataire**, sélectionnez **Adresse client**.
3. Dans le champ **Client**, sélectionnez le client auquel vous vendez l’article.
4. Choisissez l’action **Livraisons directes**, puis choisissez l’option **Extraire commande vente**.
5. Sur la page **Liste des ventes**, sélectionnez la commande vente que vous avez préparée dans [Créer une commande vente pour livraison directe](#to-create-a-sales-order-for-drop-shipment).
6. Choisissez le bouton **OK**.

Les informations de ligne de la commande vente sont insérées sur la/les ligne(s) commande achat.

Vous pouvez maintenant demander à votre fournisseur d’expédier les articles directement au client. Par exemple, vous pouvez lui envoyer la commande par message électronique. 

Si votre fournisseur vous communique un numéro de suivi ou des informations similaires, vous pouvez ajouter ces informations dans une ligne de la commande achat de type *Commentaire*.  

## Pour créer plusieurs commandes achat pour des livraisons directes

Vous pouvez également utiliser la demande achat pour créer la commande achat du fournisseur. 

L’avantage d’utiliser la demande achat est qu’elle peut créer des commandes achat pour toutes les livraisons directes en attente. Cela signifie que vous n’avez pas à créer chacune individuellement.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Demandes achat**, puis choisissez le lien associé.
2. Choisissez l’action **Livraisons directes**, puis choisissez l’option **Extraire commande vente**.
3. Cliquez sur le bouton **OK**.
4. Passez en revue les lignes commande achat et, dans le champ **N° fournisseur**, sélectionnez le fournisseur qui fournit les marchandises requises. 
5. Choisissez l’action **Traiter messages d’action** pour convertir les lignes révisées en commande achat.

## Pour afficher la commande achat associée à partir de la commande vente

* Sélectionnez la ligne commande vente livraison directe, choisissez l’action **Commande**, puis l’action **Livraison directe** et enfin l’action **Commande achat**.

## Pour valider une livraison directe

Lorsque le fournisseur a expédié les articles, vous pouvez valider la commande vente comme envoyée. Vous pouvez également valider la commande achat, mais uniquement avec l’option **Réceptionner** jusqu’à ce que la commande vente ait été facturée.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.
2. Ouvrez les commandes vente que vous avez créées dans [Pour créer une commande vente pour une livraison directe](#to-create-a-sales-order-for-drop-shipment).
3. Dans le champ **Qté à expédier**, spécifiez la quantité de commandes à envoyer, la quantité de commandes partielles ou totales.
4. Sélectionnez l’action **Valider** ou **Valider et envoyer**.
5. Sélectionnez l’option **Livrer** pour facturer ultérieurement ou l’option **Livrer et facturer** pour facturer immédiatement.

## Voir aussi

[Création des commandes spéciales](sales-how-to-create-special-orders.md)  
[Achat des articles pour une vente](purchasing-how-purchase-products-sale.md)  
[Vente des produits](sales-how-sell-products.md)  
[Enregistrer des achats](purchasing-how-record-purchases.md)  
[Ventes](sales-manage-sales.md)  
[Stock](inventory-manage-inventory.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
