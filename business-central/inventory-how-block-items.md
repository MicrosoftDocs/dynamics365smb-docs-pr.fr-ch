---
title: Comment bloquer des articles ou des variantes article dans les documents vente ou achat
description: 'Vous pouvez empêcher la saisie d’articles ou de variantes article sur des lignes de documents vente ou achat, ainsi que leur validation dans une transaction.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'item, variant, product'
ms.date: 08/22/2023
---
# <a name="block-items-or-item-variants-from-sales-or-purchasing"></a>Bloquer des articles ou des variantes article dans les documents vente ou achat

Vous pouvez empêcher la saisie d’articles ou de variantes article sur des lignes de documents vente ou achat, et vous pouvez empêcher leur validation dans des transactions. Par exemple, cela est utile lorsqu’un article présente un défaut connu. Si quelqu’un choisit un article ou une variante bloqué dans un document vente ou achat, un message l’informe que l’article est bloqué.

Le tableau suivant décrit ce qui se produit lorsque des articles ou des variantes sont bloqués.  

|Option|Description|  
|--------------------|------------|  
|**Ventes bloquées**|Vous ne pouvez pas choisir l’article ou la variante dans un document vente ou une feuille article vente.|  
|**Achats bloqués**|Vous ne pouvez pas choisir l’article ou la variante dans un document achat, une feuille article achat, ou dans les processus de planification achat.|  
|**Bloqué**|Vous ne pouvez pas inclure l’article ou la variante lorsque vous validez des transactions.|  

> [!NOTE]
> Les articles bloqués peuvent être retournés. Cela signifie qu’aucun des paramètres ci-dessus ne s’applique à des commandes retour et des avoirs.

Quand vous utilisez l’action **Copier à partir du document** pour créer des documents à partir de documents existants, vous êtes averti si des articles ou des variantes sur les lignes du document origine sont bloqués. Les lignes de document bloquées sont exclues du nouveau document et une notification affiche une vue d’ensemble de toutes les lignes de document bloquées dans le document source.

## <a name="to-block-an-item"></a>Pour bloquer un article

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Articles**, puis choisissez le lien associé.  
2. En fonction de ce que vous souhaitez faire, sélectionnez l’article, puis choisissez une ou plusieurs des cases à cocher suivantes :
    * **Bloqué**
    * **Ventes bloquées**
    * **Achats bloqués**  

## <a name="to-block-an-item-variant"></a>Pour bloquer une variante article

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Articles**, puis choisissez le lien associé.  
2. Sélectionnez l’article contenant une variante que vous souhaitez bloquer, choisissez **Variantes**, puis choisissez une ou plusieurs des cases suivantes :  
    * **Bloqué**
    * **Ventes bloquées**
    * **Achats bloqués**

## <a name="see-also"></a>Voir aussi

[Enregistrement des nouveaux articles](inventory-how-register-new-items.md)  
[Stock](inventory-manage-inventory.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
