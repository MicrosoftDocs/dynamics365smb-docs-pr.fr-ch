---
title: Lier une commande vente à une commande achat pour une livraison directe | Microsoft Docs
description: Décrit comment créer une commande vente liée à une commande achat pour permettre la livraison directe du fournisseur au client.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7a87023445ea10aa19cc0cc4f60d76ce4cf3e365
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251249"
---
# <a name="make-drop-shipments"></a>Effectuer des livraisons directes
Lors d'une livraison directe, un ou plusieurs articles de l'un de vos fournisseurs sont livrés directement chez l'un de vos clients.

Lorsqu'une commande vente est marquée pour livraison directe, et lorsque vous créez une commande achat spécifiant le client dans le champ **N° donneur d'ordre** , vous pouvez ensuite associer les deux documents et par conséquent informer le fournisseur de procéder directement à l'envoi au client.

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Pour créer une commande vente pour des livraisons directes
Pour préparer une livraison directe, vous créez une commande vente pour un article, sauf que vous devez indiquer sur la ligne vente que la vente exige la livraison directe.

1. Créez une commande vente pour un article. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).
2. Sur la ligne commande vente pour l'article envoyé, cochez la case **Livraison directe**. Utilisez la fonction **Choisir les colonnes** si le champ n'est pas visible. Pour plus d'informations, voir [Personnalisation de votre espace de travail](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Pour créer la commande achat pour livraison directe
Pour préparer une livraison directe pour l'article mis en vente, vous créez une commande achat, comme à l'accoutumée, sauf que vous devez indiquer sur la commande achat qu'elle doit être envoyée à votre client et non pas à vous-même.

1. Créez une commande achat. Ne remplissez pas les champs sur les lignes. Pour plus d'informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md).
2. Dans le champ **N° donneur d'ordre** , sélectionnez le client auquel vous souhaitez vendre l'article en question.
3. Choisissez l'action **Livraisons directes**, puis choisissez l'option **Extraire commande vente**.
4. Sur la page **Liste des ventes**, sélectionnez la commande vente que vous avez préparée dans [Créer une commande vente pour livraison directe](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
5. Choisissez le bouton **OK**.

Les informations de ligne de la commande vente sont insérées sur la/les ligne(s) commande achat.

Vous pouvez maintenant informer le fournisseur quant à l'envoi des articles à votre client, par exemple en envoyant la commande achat au format PDF.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Pour afficher la commande achat associée à partir de la commande vente
* Sélectionnez la ligne commande vente livraison directe, choisissez l'action **Commande**, puis l'action **Livraison directe** et enfin l'action **Commande achat**.

## <a name="to-post-a-drop-shipment"></a>Pour valider une livraison directe
Lorsque le fournisseur a expédié les articles, vous pouvez valider la commande vente comme envoyée. Vous pouvez également valider la commande achat, mais uniquement avec l'option **Réceptionner** jusqu'à ce que la commande vente ait été facturée.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente**, puis sélectionnez le lien associé.
2. Ouvrez les commandes vente que vous avez créées dans [Pour créer une commande vente pour une livraison directe]().
3. Dans le champ **Qté à expédier**, spécifiez la quantité de commandes à envoyer, la quantité de commandes partielles ou totales.
4. Sélectionnez l'action **Valider** ou **Valider et envoyer**.
5. Sélectionnez l'option **Livrer** pour facturer ultérieurement ou l'option **Livrer et facturer** pour facturer immédiatement.

## <a name="see-also"></a>Voir aussi
[Créer des commandes spéciales](sales-how-to-create-special-orders.md)  
[Acheter des articles pour une vente](purchasing-how-purchase-products-sale.md)  
[Vendre des produits](sales-how-sell-products.md)  
[Enregistrer des achats](purchasing-how-record-purchases.md)  
[Ventes](sales-manage-sales.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
