---
title: "Procédure : créer des commandes spéciales | Microsoft Docs"
description: "Vous pouvez créer une commande spéciale pour un article spécifique non présent en stock à expédier à un client particulier. Le fournisseur expédie l'article à votre entrepôt et vous pouvez ensuite l'expédier à votre client seul ou avec d'autres articles issus d'autres commandes."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2ebd7ed1c2ae9426b481edabbb8e4957073a5d21
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-special-orders"></a>Créer des commandes spéciales
Vous pouvez créer une commande spéciale pour un article spécifique non présent en stock à expédier à un client particulier. Le fournisseur expédie l'article à votre entrepôt et vous pouvez ensuite l'expédier à votre client seul ou avec d'autres articles issus d'autres commandes.  

Dans le cadre d'une commande spéciale, la commande achat et la commande vente sont liées pour s'assurer que l'article non stocké précis est prélevé et expédié au client.  

Pour pouvoir utiliser cette fonction, vous devez d'abord configurer les fiches client, fournisseur, et article nécessaires à la commande.  

## <a name="to-create-a-special-order"></a>Pour créer une commande spéciale  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente**, puis sélectionnez le lien connexe.  
2. Sélectionnez l'action **Nouveau**. Créez et renseignez une  commande vente pour l'article. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).
3.  Sous le raccourci **Lignes**, renseignez la ligne vente. Dans le champ **Procédure achat**, sélectionnez une procédure achat dont le champ **Commande spéciale** est sélectionné.

    Vous devez maintenant créer une commande achat à partir d'une demande achat.  
4. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Demande achat**, puis sélectionnez le lien connexe.  
5. Choisissez l'action **Commande spéciale**, puis choisissez l'option **Extraire commandes vente**.  
6.  Dans la fenêtre **Extraire commandes vente**, affichez les résultats dans lesquels le **N° document** correspond au numéro de commande vente. Cliquez sur le bouton **OK**. Une ligne demande achat est créée pour l'article.  
7.  Dans la ligne demande achat, sélectionnez **Nouveau** dans le champ **Message d'action**.  
8.  Dans la fenêtre **Demande achat**, sélectionnez l'action **Traiter messages d'action**. La fenêtre **Traiter messages d'action - Demande** s'affiche. Cliquez sur le bouton **OK**.  

    Le message qui s'affiche indique que les commandes achat ont été créées. Cliquez sur le bouton **OK**.  

Une commande achat créée comme commande spéciale pour une commande client est respectée par le système de planification lorsqu'il équilibre l'offre et la demande. Ainsi, la commande achat (approvisionnement) reste liée à la commande vente (demande), même si cette commande achat pourrait approvisionner une autre demande antérieure. Pour plus d'informations, voir [Détails de conception : méthodes de réapprovisionnement](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Vous ne pouvez pas utiliser la fonctionnalité de commande spéciale si l'élément est déjà réservé. Par conséquent, pour les articles qui sont vendus en commandes spéciales, assurez\-vous que le champ **Réserver** sur la fiche article n'est pas défini sur **Toujours**.  

## <a name="see-also"></a>Voir aussi  
[Utiliser des articles non stockés](inventory-how-work-nonstock-items.md)  
[Ventes](sales-manage-sales.md)  
[Effectuer des livraisons directes](sales-how-drop-shipment.md)   
[Détails de conception : méthodes de réapprovisionnement](design-details-reservation-order-tracking-and-action-messaging.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

