---
title: "Procédure de création d'en-têtes d'ordre de fabrication | Microsoft Docs"
description: "Vous pouvez créer manuellement un ordre de fabrication. Pour cela, la première étape est de créer un en-tête O.F."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3ffbe781830a492256be864bace38bbef3050596
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="create-production-order-headers"></a>Créer des en-têtes O.F.
Vous pouvez créer manuellement un ordre de fabrication. Pour cela, la première étape est de créer un en-tête O.F.

Les ordres de fabrication sont généralement créés automatiquement par une fonction de planification pour répondre à une demande connue. Pour plus d'informations, voir [Planification](production-planning.md).   

La procédure suivante s'appuie sur un ordre de fabrication planifié ferme. Vous pouvez aussi créer des ordres de fabrication dotés d'un autre statut.  

## <a name="to-create-a-production-order-header"></a>Pour créer un en-tête O.F.  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **O.F. planifiés fermes**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'action **Nouveau**.  
3.  Dans le champ **N°**, insérez le numéro suivant de la souche.  
4.  Dans le champ **Type origine**, sélectionnez la source de l'ordre de fabrication.

    Vous pouvez choisir de produire une famille d'articles. Pour plus d'informations, voir [Utiliser les familles de production](production-how-work-family.md).
5.  Dans le champ **N° origine**, sélectionnez le numéro d'article, la famille, ou l'en-tête vente pour lequel l'ordre de fabrication doit être créé.  
6.  Renseignez les champs **Quantité** et **Délai** en fonction de vos spécifications.  

Lorsque les exigences de production évoluent, comme les composants ou les opérations, vous pouvez replanifier rapidement l'ordre de fabrication. Pour plus d'informations, voir [Replanifier ou actualiser directement des ordres de fabrication](production-how-to-replan-refresh-production-orders.md). 

## <a name="see-also"></a>Voir aussi  
[Production](production-manage-manufacturing.md)    
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)      
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

