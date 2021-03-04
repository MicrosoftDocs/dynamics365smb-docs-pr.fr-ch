---
title: Comment bloquer des articles pour la vente ou pour l’achat
description: Vous pouvez empêcher qu’un article soit utilisé, par exemple, dans des documents de vente ou d’achat.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f958600a47daa12a665975d6c41e214fca7cf5ad
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914116"
---
# <a name="block-items-from-sales-or-purchasing"></a>Bloquer des articles pour la vente ou pour l’achat
Vous pouvez bloquer un article pour la saisie sur des lignes de documents de vente ou d’achat, et vous pouvez le bloquer pour la validation dans n’importe quelle transaction. Par exemple, cela est utile lorsqu’un article présente un défaut connu. Si quelqu’un choisit un article bloqué sur un document de vente ou d’achat, un message l’informera que l’article est bloqué.

Le tableau suivant décrit ce qui se produit lorsque les articles sont bloqués.  

|Option|Description|  
|--------------------|------------|  
|**Bloqué à la vente**|Vous ne pouvez pas saisir l’article dans un document vente ou dans une feuille article vente.|  
|**Bloqué à l’achat**|Vous ne pouvez pas saisir l’article dans un document achat, dans une feuille article d’achat, ou dans les processus de planification achat.|  
|**Bloqué**|Vous ne pouvez pas utiliser l’article pour une transaction d’article.|  

> [!NOTE]
> Les articles bloqués peuvent être retournés. Cela signifie qu’aucun des paramètres ci-dessus ne s’applique lorsque l’article est utilisé sur des commandes retour et des avoirs.

Lorsque vous utilisez la fonction **Copier à partir du document** pour créer des documents à partir de documents existants, vous êtes averti si des articles sur les lignes du document source sont bloqués. Les lignes de document bloquées sont exclues du nouveau document et une notification affiche une vue d’ensemble de toutes les lignes de document bloquées dans le document source.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Pour bloquer un article pour la saisie sur des lignes vente  
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles** , puis sélectionnez le lien associé.  
2.  Sélectionnez l’article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué à la vente** .  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Pour bloquer un article pour la saisie sur des lignes achat  
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles** , puis sélectionnez le lien associé.  
2.  Sélectionnez l’article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué à l’achat** .  

## <a name="to-block-an-item-from-being-posted"></a>Pour bloquer un article à valider
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles** , puis sélectionnez le lien associé.
2. Sélectionnez l’article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué** .

## <a name="see-also"></a>Voir aussi  
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Stock](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]