---
title: "Procédure : Imprimer la liste des prélèvements de stock d'une commande vente"
description: Vous pouvez imprimer une liste des prélèvements des stocks directement à partir d'une commande client, des ventes, de la facture et d'autres documents de vente sortants.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 47ae132d862d2c05bef4ea0d0af26688bdd16588
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758232"
---
# <a name="print-the-picking-list"></a>Imprimer la liste des prélèvements
Vous pouvez imprimer une liste des prélèvements des stocks directement à partir d'une commande client, d'une facture vente, ou d'autres documents qui déclenchent l'expédition des articles.

Ce rapport est généralement utilisé dans les entreprises sans fonctionnalité dédiée à la gestion des entrepôts, de sorte qu'un stock peut simplement afficher ou imprimer la liste des prélèvements à partir du document de vente associé. Dans les entreprises avec un volume plus élevé ou des processus plus complexes, le prélèvement est planifié et effectué dans des documents d'entrepôt dédiés. Pour plus d'informations, voir [Prélèvement d'articles](warehouse-pick-items.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>Pour imprimer la liste des prélèvements à partir d'une commande vente  
La procédure suivante se base sur une commande vente. Les étapes sont similaires pour tous les documents de vente pouvant être utilisés pour lancer l'expédition d'articles.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), saisissez **Commandes vente**, puis sélectionnez le lien associé.  
2. Ouvrez une commande vente pour laquelle vous souhaitez sélectionner des articles.  
3. Choisir l'action **Rapport**, puis choisissez l'action **Liste de prélèvement par ordre**.  
4. Sélectionnez le bouton **Imprimer** pour imprimer la liste de prélèvements, ou le bouton **Aperçu** pour l'afficher à l'écran.

Vous pouvez également enregistrer la liste des prélèvements en tant que document, par exemple, pour l'envoyer à quelqu'un ou pour l'ajouter en tant que pièce jointe à la commande client. Pour plus d'informations, voir [Gérer les pièces jointes, les liens et les notes sur les fiches et les documents](ui-how-add-link-to-record.md).

> [!NOTE]
> Si vous avez utilisé la fonction **Éclater nomenclature** sur la commande client, seuls les composants de l'élément d'assemblage associé sont affichés dans le rapport. Pour plus d'informations, reportez-vous à [Utiliser les nomenclatures](inventory-how-work-BOMs.md).

## <a name="see-also"></a>Voir aussi  
[Stock](inventory-manage-inventory.md)  
[Prélèvement d'articles](warehouse-pick-items.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]