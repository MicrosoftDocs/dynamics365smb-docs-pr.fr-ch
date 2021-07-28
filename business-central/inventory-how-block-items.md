---
title: Comment bloquer des articles pour la vente ou pour l’achat
description: Vous pouvez bloquer un article pour la saisie sur des lignes de documents de vente ou d’achat, et vous pouvez le bloquer pour la validation dans n’importe quelle transaction.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 744d19675fe3ae95bcbaa56d6e8555ac734180e6
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441183"
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
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2.  Sélectionnez l’article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué à la vente**.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Pour bloquer un article pour la saisie sur des lignes achat  
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2.  Sélectionnez l’article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué à l’achat**.  

## <a name="to-block-an-item-from-being-posted"></a>Pour bloquer un article à valider
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Sélectionnez l’article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué**.

## <a name="see-also"></a>Voir aussi  
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Stock](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]