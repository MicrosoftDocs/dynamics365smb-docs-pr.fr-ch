---
title: "Procédure : Bloquer des articles de stock pour les ventes ou les achats"
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
ms.date: 02/02/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f11991333f4d9ebaf890b23841d9d90f929fdf98
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="block-inventory-items-for-sales-or-purchases"></a>Bloquer des articles de stock pour les ventes ou les achats
Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], un article peut être signalé comme bloqué pour la vente, bloqué pour l'achat ou bloqué dans tous les cas.  

Le tableau suivant illustre ce qui se produit lorsque les articles sont bloqués.  

|Article marqué comme|Résultat|  
|--------------------|------------|  
|**Bloqué à la vente**|Vous ne pouvez pas utiliser l'article dans un document vente ou dans une feuille article vente.|  
|**Bloqué à l'achat**|Vous ne pouvez pas utiliser l'article dans un document achat, dans une feuille article d'achat, ou dans les processus de planification achat.|  
|**Bloqué**|Vous ne pouvez pas utiliser l'article pour une transaction d'article. Pour plus d'informations sur le blocage d'un article pour quelle que raison possible, voir Fiche article.|  

## <a name="to-block-inventory-items-for-sales"></a>Pour bloquer des articles de stock à l'achat  

1.  Cliquez sur l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'article que vous souhaitez bloquer, puis choisissez l'action **Modifier**.  
3.  Pour bloquer l'article sélectionné pour des transactions de vente, dans le raccourci **Prix et vente**, sélectionnez la case à cocher **Vente bloquée**.  
4.  Cliquez sur le bouton **OK**.  

## <a name="to-block-inventory-items-for-purchase"></a>Pour bloquer des articles de stock à la vente  

1.  Cliquez sur l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'article que vous souhaitez bloquer, puis choisissez l'action **Modifier**.  
3.  Pour bloquer un article pour des transactions d'achat, dans le raccourci **Réapprovisionnement**, sélectionnez la case à cocher **Achat bloqué**.  
4.  Cliquez sur le bouton **OK**.  

Vous recevrez un message d'erreur si vous essayez d'effectuer les opérations suivantes :  

- Entrez les lignes vente et les lignes achat dans les documents vente et les documents achat pour les articles bloqués. Pour plus d'informations, voir la table Ligne Vente et la table Ligne Achat.  
- Créez des lignes dans une feuille article pour les articles bloqués. Pour plus d'informations, reportez-vous à la fenêtre Feuille article.  
- Validez les mouvements de stock pour les articles bloqués.  

## <a name="see-also"></a>Voir aussi  
 [Gestion des stocks, Suisse](swiss-inventory-management.md)   
 [Copier des articles existants pour créer de nouveaux articles](how-to-copy-existing-items-to-new-items.md)   
 [Désactiver le suivi des coûts article](how-to-deactivate-item-cost-tracking.md)

