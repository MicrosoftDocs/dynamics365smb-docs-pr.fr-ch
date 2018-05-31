---
title: "Procédure de contrepassation de la validation de production | Microsoft Docs"
description: "Il arrive qu'une validation de production doive être contrepassée. C'est le cas, par exemple, si une erreur de saisie de données a été commise et qu'une quantité de production incorrecte a été validée pour un ordre de fabrication."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f2430dcf45303e04baad406880783ab0f74dd4f2
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="reverse-output-posting"></a>Contrepasser la validation de production
Il arrive qu'une validation de production doive être contrepassée. C'est le cas, par exemple, si une erreur de saisie de données a été commise et qu'une quantité de production incorrecte a été validée pour un ordre de fabrication.  

## <a name="to-reverse-an-output-posting"></a>Pour contrepasser une validation de production  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille production**, puis sélectionnez le lien connexe. Sélectionnez votre lot.  
2. Renseignez les champs selon vos besoins. Pour plus d'informations, voir [Valider par lots la production et les temps d'exécution](production-how-to-post-output-quantity.md).
3.  Dans le champ **Ecriture lettrage**, sélectionnez l'écriture comptable article associée. Cette action contrepasse les écritures comptables capacité et article.  
4. Validez la contrepassation en validant la feuille.  

Les écritures de la feuille production sont validées dans les écritures article comme un ajustement positif.  

## <a name="see-also"></a>Voir aussi  
 [Production](production-manage-manufacturing.md)    
 [Paramétrage de la production](production-configure-production-processes.md)  
 [Planifié](production-planning.md)      
 [STOCKS ET EN-COURS](inventory-manage-inventory.md)  
 [Achats](purchasing-manage-purchasing.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
