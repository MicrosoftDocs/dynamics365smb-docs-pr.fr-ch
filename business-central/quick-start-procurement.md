---
title: Démarrage rapide Approvisionnement (contient une vidéo)
description: Découvrez comment remplir les premiers champs critiques concernant les fournisseurs dans Business Central afin de pouvoir commencer à acheter des produits et des services.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: quickstart
ms.search.form: '26, 27, 50, 56'
ms.date: 09/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="procurement-quick-start"></a>Démarrage rapide Approvisionnement

Pour pouvoir acheter des produits et des services, vous devez d’abord configurer des fournisseurs. Une fois cela fait, vous pouvez commencer à enregistrer les commandes achat et à recevoir les factures.  

## <a name="set-up-vendors"></a>Configurer des fournisseurs

La vidéo suivante vous montre comment configurer un fournisseur dans [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

### <a name="set-up-a-new-vendor"></a>Configurer un nouveau fournisseur

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

Pour plus d’informations et apprendre les autres choses que vous pouvez faire lorsque vous enregistrez des fournisseurs, consultez [Enregistrer de nouveaux fournisseurs](purchasing-how-register-new-vendors.md).  

## <a name="create-new-purchase-orders"></a>Créer des commandes achat

Lorsque vous achetez quelque chose auprès d’un fournisseur, vous avez deux options. La première, et la plus simple, consiste simplement à créer une facture achat. Toutefois, vous devez utiliser les commandes achat si votre processus de vente exige que vous enregistriez des réceptions partielles d’une quantité de commande, par exemple, si la quantité totale n’était pas disponible auprès du fournisseur.

La vidéo suivante vous montre comment créer une commande achat dans [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

### <a name="to-create-a-purchase-order"></a>Pour créer une commande achat

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes achat**, puis choisissez le lien associé.  

2. Sur la page **Commandes achat**, sélectionnez l’action **Nouveau** pour créer une commande achat.

3. Dans le champ **Nom fournisseur**, entrez le nom d’un fournisseur existant.

    D’autres champs de la page **En-tête achat** sont désormais renseignés avec les informations standard sur le fournisseur sélectionné.  

4. Renseignez les champs restants de la page **Commande achat**, selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Vous êtes maintenant prêt à renseigner les lignes commande achat avec les articles ou ressources que vous avez achetés au fournisseur.

5. Dans le raccourci **Lignes**, dans le champ **N° article**, entrez le numéro d’un article de stock ou d’un service.

6. Dans le champ **Quantité**, indiquez le nombre d’articles à acheter.

    Le champ **Montant ligne** est mis à jour pour indiquer la valeur du champ **Coût unitaire direct** multipliée par la valeur du champ **Quantité**.

7. Dans le champ **Montant remise commande**, entrez un montant qui doit être déduit de la valeur indiquée dans le champ **Total TTC** au bas de la commande.

8. Lorsque vous recevez les articles ou services achetés, sélectionnez **Valider**.

Pour plus d’informations et d’autres choses que vous pouvez faire lors de la création d’une commande achat, consultez [Achat](purchasing-manage-purchasing.md).  

## <a name="create-a-purchase-invoice"></a>Créer une facture achat

Vous créez une facture achat pour enregistrer le coût des achats et suivre les créances. La création d’une facture achat est similaire à la création d’une commande achat.

### <a name="how-to-create-and-post-a-purchase-invoice"></a>Procédure : créer et valider une facture achat

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 3.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures achat**, puis sélectionnez le lien associé.  
2. Sur la page **Facture achat**, sélectionnez l’action **Nouveau** pour créer une facture achat.
3. Dans le champ **Fournisseur**, entrez le nom d’un fournisseur existant.

    D’autres champs de la page **Facture achat** sont désormais renseignés avec les informations standard sur le fournisseur sélectionné.

4. Renseignez les champs restants de la page **Facture achat**, selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Vous êtes maintenant prêt à renseigner les lignes facture achat avec les articles ou ressources que vous avez achetés au fournisseur.

5. Dans le raccourci **Lignes**, dans le champ **N° article**, entrez le numéro d’un article de stock ou d’un service.
6. Dans le champ **Quantité**, indiquez le nombre d’articles à acheter.

    Le champ **Montant ligne** est mis à jour pour indiquer la valeur du champ **Coût unitaire direct** multipliée par la valeur du champ **Quantité**.

7. Dans le champ **Montant remise facture**, entrez un montant qui doit être déduit de la valeur indiquée dans le champ **Total TTC** au bas de la facture.

8. Lorsque vous recevez les articles ou services achetés, sélectionnez **Valider**.

L’achat est désormais visible dans le stock, les écritures ressource et les enregistrements financiers, et le paiement fournisseur est activé. La facture achat est supprimée de la liste des factures achat et remplacée par un nouveau document dans la liste des factures achat validées.  

Pour plus d’informations et d’autres choses que vous pouvez faire lors de la création d’une facture achat, consultez [Enregistrer les achats avec les factures achat](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Voir aussi

[Démarrage rapide de Business Central](quick-start-business-central.md)  
[Vue d’ensemble des achats](Purchasing-manage-purchasing.md)  
[Enregistrer les achats avec les factures achat](purchasing-how-record-purchases.md)  
