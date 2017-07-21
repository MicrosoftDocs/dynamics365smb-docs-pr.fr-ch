---
title: "Ajuster les coûts article manuellement| Microsoft Docs"
description: "Vous pouvez ajuster l'évaluation du stock d'un article à l'aide des méthodes FIFO ou d'évaluation stock moyen, par exemple, lorsque les coûts article sont modifiés pour des motifs autres que les transactions."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a1f682b60b7b9ae402c27093f13aa3db2368ed5b
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Procédure : ajuster les coûts article manuellement
Le coût d'un article (valeur du stock) que vous achetez et vendez ultérieurement peut changer au cours de sa durée de vie, par exemple parce que des frais de transport sont ajoutés à son coût d'achat après que vous ayez vendu l'article. L'ajustement des coûts est particulièrement utile dans les situations où vous vendez des biens avant de facturer leur achat. Pour toujours connaître la valeur du stock correcte, les coûts article doivent donc être ajustés régulièrement. Cela garantit que les statistiques vente et profit sont à jour et que les indicateurs clés financiers sont corrects.

Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les coûts article sont automatiquement ajustés chaque fois qu'un mouvement de stock se produit, par exemple lors de la validation d'une facture achat pour un article.

Vous pouvez également utiliser une fonction pour ajuster manuellement les coûts d'un ou de plusieurs articles. Cela est utile, par exemple, si vous savez que les coûts article ont changé pour d'autres raisons que des mouvements de stock.

Les coûts article sont ajustés selon la méthode FIFO ou d'évaluation stock moyen, selon la sélection effectuée dans la configuration assistée **Configurer ma société**. Pour plus d'informations, voir [Préparation aux activités commerciales](ui-get-ready-business.md).  

Si vous utilisez la méthode de coût FIFO, le coût unitaire d'un article est la valeur réelle de toute réception de l'article. Le stock est évalué avec la supposition que les premiers articles stockés sont ceux vendus en premier.

Si vous utilisez la méthode de l'évaluation stock moyen, le coût unitaire d'un article est calculé comme le coût unitaire moyen à chaque moment après un achat. Le stock est évalué avec la supposition que tous les stocks sont vendus simultanément.

La fonction d'ajustement des coûts traite uniquement les écritures valeur non encore ajustées. Si la fonction est confrontée à une situation où des coûts entrants modifiés doivent être transférés à des écritures sortantes associées, de nouvelles écritures valeur ajustées sont créées, sur la base des informations des écritures valeur d'origine, mais contenant le montant de l'ajustement. La fonction d'ajustement des coûts utilise la date comptabilisation de l'écriture valeur d'origine dans l'écriture ajustée, sauf si la date est comprise dans une période inventaire clôturée. Dans ce cas, le programme utilise la date début de la période d'inventaire ouverte suivante. Si aucune période inventaire n'est utilisée, la date du champ **Début période validation** de la fenêtre **Paramètres comptabilité** définira la date de comptabilisation de l'écriture ajustée.

Les modifications de la valeur stock découlant de la vente sont automatiquement rapprochées avec vos livres financiers lorsque vous validez des transactions article. Pour plus d'informations, voir la section « Rapprochement stock » de [Stock](inventory-manage-inventory.md).

## <a name="to-adjust-item-costs-manually"></a>Pour ajuster les coûts article manuellement
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Ajuster coûts : Écr. article**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Ajuster coûts - Écr. article**, spécifiez les articles pour lesquels ajuster les coûts.
3. Cliquez sur le bouton **OK**.

## <a name="see-also"></a>Voir aussi
[Stock](inventory-manage-inventory.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

