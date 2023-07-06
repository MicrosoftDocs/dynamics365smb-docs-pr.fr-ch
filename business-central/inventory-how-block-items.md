---
title: Comment bloquer des articles pour la vente ou pour l’achat
description: 'Vous pouvez bloquer un article pour la saisie sur des lignes de documents de vente ou d’achat, et vous pouvez le bloquer pour la validation dans n’importe quelle transaction.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/03/2022
ms.author: bholtorf
---
# <a name="block-items-from-sales-or-purchasing"></a><a name="block-items-from-sales-or-purchasing"></a><a name="block-items-from-sales-or-purchasing"></a>Bloquer des articles pour la vente ou pour l’achat

Vous pouvez bloquer un article pour la saisie sur des lignes de documents de vente ou d’achat, et vous pouvez le bloquer pour la validation dans les transactions. Par exemple, cela est utile lorsqu’un article présente un défaut connu. Si quelqu’un choisit un article bloqué sur un document de vente ou d’achat, un message l’informera que l’article est bloqué.

Le tableau suivant décrit ce qui se produit lorsque les articles sont bloqués.  

|Option|Désignation|  
|--------------------|------------|  
|**Bloqué à la vente**|Vous ne pouvez pas saisir l’article dans un document vente ou dans une feuille article vente.|  
|**Bloqué à l’achat**|Vous ne pouvez pas saisir l’article dans un document achat, dans une feuille article d’achat, ou dans les processus de planification achat.|  
|**Bloqué**|Vous ne pouvez pas inclure l’article dans les transactions.|  

> [!NOTE]
> Les articles bloqués peuvent être retournés. Cela signifie qu’aucun des paramètres ci-dessus ne s’applique à des commandes retour et des avoirs.

Quand vous utilisez l’action **Copier à partir du document** pour créer des documents à partir de documents existants, vous êtes averti si des articles sur les lignes du document source sont bloqués. Les lignes de document bloquées sont exclues du nouveau document et une notification affiche une vue d’ensemble de toutes les lignes de document bloquées dans le document source.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><a name="to-block-an-item-from-being-entered-on-sales-lines"></a><a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Pour bloquer un article pour la saisie sur des lignes vente

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2. Sélectionnez l’article à bloquer, puis cochez la case **Bloqué à la vente**.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Pour bloquer un article pour la saisie sur des lignes achat

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2. Sélectionnez l’article à bloquer, puis cochez la case **Bloqué à l’achat**.  

## <a name="to-block-an-item-from-being-posted"></a><a name="to-block-an-item-from-being-posted"></a><a name="to-block-an-item-from-being-posted"></a>Pour bloquer un article à valider

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Sélectionnez l’article à bloquer, puis cochez la case **Bloqué**.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Stock](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
