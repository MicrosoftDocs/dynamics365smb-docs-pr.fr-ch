---
title: Comment bloquer des articles pour la vente ou pour l'achat
description: "Dans Business Central, un article peut être signalé comme bloqué pour la vente, bloqué pour l'achat ou bloqué dans tous les cas."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/23/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: c6f10f8252c00bf0a599f9fa794ee36c41ce92be
ms.openlocfilehash: 2f8be478dda62fef2cb34397de488f45d4fcfc0c
ms.contentlocale: fr-ch
ms.lasthandoff: 07/30/2018

---
# <a name="block-items-from-sales-or-purchasing"></a>Bloquer des articles pour la vente ou pour l'achat
Vous pouvez bloquer un article pour la saisie dans des lignes de vente ou d'achat, et vous pouvez le bloquer pour la validation dans n'importe quelle transaction.  

Le tableau suivant illustre ce qui se produit lorsque les articles sont bloqués.  

|Option|Désignation|  
|--------------------|------------|  
|**Bloqué à la vente**|Vous ne pouvez pas saisir l'article dans un document vente ou dans une feuille article vente.|  
|**Bloqué à l'achat**|Vous ne pouvez pas saisir l'article dans un document achat, dans une feuille article d'achat, ou dans les processus de planification achat.|  
|**Bloqué**|Vous ne pouvez pas utiliser l'article pour une transaction d'article. Pour plus d'informations sur le blocage d'un article pour quelle que raison possible, voir Fiche article.|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Pour bloquer un article pour la saisie sur des lignes vente  

1.  Cliquez sur l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué à la vente**.  

Si vous essayez de saisir l'article sur un document vente ou une ligne feuille, vous recevez désormais un message d'erreur indiquant que l'article est bloqué.

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Pour bloquer un article pour la saisie sur des lignes achat  

1.  Cliquez sur l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué à l'achat**.  

Si vous essayez de saisir l'article sur un document achat ou une ligne feuille, vous recevez désormais un message d'erreur indiquant que l'article est bloqué.

## <a name="to-block-an-item-from-being-posted"></a>Pour bloquer un article à valider
1. Cliquez sur l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.
2. Sélectionnez l'article que vous souhaitez bloquer, puis sélectionnez la case à cocher **Bloqué**.

Si vous essayez de valider tout type de transaction pour l'article, un message d'erreur indiquant que l'article est bloqué s'affiche désormais.

## <a name="see-also"></a>Voir aussi  
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  

