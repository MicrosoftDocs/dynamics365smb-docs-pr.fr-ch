---
title: Démarrage rapide des ventes (contient une vidéo)
description: Découvrez comment remplir les premiers champs critiques concernant les produits et les clients dans Business Central afin de pouvoir démarrer vos processus de vente.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.date: 09/29/2021
ms.author: bholtorf
---

# <a name="sales-quick-start"></a>Démarrage rapide des ventes

Pour pouvoir vendre des produits et des services, vous devez d’abord configurer des articles et des clients. Une fois cela fait, vous pouvez commencer à enregistrer les commandes vente et à envoyer les factures.

## <a name="set-up-items-to-sell"></a>Configurer des articles à vendre

Cette vidéo montre comment configurer un article à vendre dans [!INCLUDE[prod_short](includes/prod_short.md)].

<br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE47eLx?rel=0]

### <a name="set-up-a-new-item"></a>Configurer un nouvel article

[!INCLUDE[create_new_item](includes/create_new_item.md)]

Pour plus d’informations et apprendre les autres choses que vous pouvez faire lorsque vous configurez des articles, consultez [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).  

## <a name="set-up-customers"></a>Configurer des clients

Cette vidéo montre comment configurer un nouveau client dans [!INCLUDE[prod_short](includes/prod_short.md)].  

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

### <a name="set-up-a-new-customer"></a>Configurer un nouveau client

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Pour plus d’informations et apprendre les autres choses que vous pouvez faire lorsque vous configurez des clients, consultez [Enregistrer de nouveaux clients](sales-how-register-new-customers.md)

## <a name="create-a-sales-order"></a>Créer une commande vente

Lorsque vous vendez quelque chose à un client, vous avez deux options. La première, et la plus simple, consiste simplement à créer une facture vente. Cependant, si votre processus de vente est plus complexe, par exemple si vous vous trouvez dans des situations où vous n’expédiez que des parties d’une quantité commandée, vous utilisez une commande vente.

### <a name="to-create-a-sales-order"></a>Pour créer une commande vente

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 10.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.
2. Sélectionnez **Nouveau** pour créer une écriture.
3. Dans le champ **Client**, entrez le nom d’un client existant.

    D’autres champs de la page **Commande vente** sont désormais renseignés avec les informations standard sur le client sélectionné.  

4. Renseignez les champs restants de la page **Commande vente**, selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. Sous le raccourci **Lignes**, dans le champ **Type**, sélectionnez le type de produit, de frais ou de transaction à valider pour le client avec la ligne vente.

6. Dans le champ **N°**, saisissez le numéro d’un article de stock ou d’un service.

7. Dans le champ **Quantité**, saisissez le nombre d’articles à vendre.

8. Dans le champ **% remise ligne**, saisissez un pourcentage si vous souhaitez accorder au client une remise sur le produit.

9. Pour ajouter un commentaire sur la ligne commande que le client peut afficher dans la commande vente imprimée, saisissez un commentaire dans le champ **Description** sur une ligne vierge.

10. Répétez les étapes 5 à 9 pour chaque article que vous souhaitez à vendre au client.

11. Pour expédier seulement une partie de la quantité commandée, entrez la quantité dans le champ **Qté à expédier**. La valeur est copiée dans le champ **Qté à facturer**.

12. Pour facturer seulement une partie de la quantité expédiée, entrez la quantité dans le champ **Qté à facturer**. La quantité doit être inférieure à la valeur du champ **Qté à expédier**.

13. Lorsque les lignes commande vente sont renseignées, sélectionnez l’action **Valider et envoyer**.

Pour plus d’informations et voir d’autres choses que vous pouvez faire lors de la création de commandes vente, voir [Vendre des produits avec une commande client](sales-how-sell-products.md).  

## <a name="create-a-sales-invoice"></a>Créer une facture vente

Lorsque vous créez et validez une facture vente, vous créez non seulement la facture que vous envoyez au client, mais vous créez également les écritures de quantité et de valeur associées dans [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="to-create-and-post-a-sales-invoice"></a>Pour créer et valider une facture vente

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 20.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures vente**, puis sélectionnez le lien associé.  

2. Sélectionnez **Nouveau** pour créer une écriture.

3. Dans le champ **Client**, entrez le nom d’un client existant.

4. Renseignez les champs restants de la page **Facture vente**, selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. Sous le raccourci **Lignes**, dans le champ **Type**, sélectionnez le type de produit, de frais ou de transaction à valider pour le client avec la ligne vente.

6. Dans le champ **N°**, sélectionnez un enregistrement à valider en fonction de la valeur du champ **Type**.

7. Dans le champ **Quantité**, entrez le nombre d’unités du produit, de frais ou de la transaction que la ligne enregistre pour le client.  

8. Si vous souhaitez accorder une remise, saisissez un pourcentage dans le champ **% remise ligne**. La valeur du champ **Montant ligne** est mise à jour en conséquence.  

9. Répétez les étapes 5 à 8 pour chaque produit ou frais que vous souhaitez facturer au client.  

10. Dans le champ **Montant remise facture**, entrez un montant qui doit être déduit de la valeur indiquée dans le champ **Total TTC**.

11. Lorsque les lignes facture vente sont renseignées, sélectionnez l’action **Valider et envoyer**.  

Pour plus d’informations et d’autres choses que vous pouvez faire lors de la création d’une facture vente client, consultez [Facturer des ventes](sales-how-invoice-sales.md)

## <a name="see-also"></a>Voir aussi

[Démarrage rapide de Business Central](quick-start-business-central.md)  
[Vue d’ensemble des ventes](sales-manage-sales.md)  
[Vente de produits avec une commande vente client](sales-how-sell-products.md)  
[Facturer des ventes](sales-how-invoice-sales.md)  
