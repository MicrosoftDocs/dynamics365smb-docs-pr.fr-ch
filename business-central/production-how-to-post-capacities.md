---
title: "Procédure de validation des capacités | Microsoft Docs"
description: "La feuille capacité vous permet de valider les capacités consommées qui ne sont pas affectées à l'ordre de fabrication. Par exemple, les travaux de maintenance doivent être affectés à une capacité, mais non à un ordre de fabrication."
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
ms.openlocfilehash: 6114149372b786c20ee7edbe13022abe688ed9a2
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="post-capacities"></a>Valider les capacités
La feuille capacité vous permet de valider les capacités consommées qui ne sont pas affectées à l'ordre de fabrication. Par exemple, les travaux de maintenance doivent être affectés à une capacité, mais non à un ordre de fabrication.  

## <a name="to-post-capacities"></a>Pour valider les capacités  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Feuilles temps non productif**, puis sélectionnez le lien connexe.  
2.  Renseignez les champs **Date comptabilisation** et **N° document**.  
3.  Dans le champ **Type**, entrez le type de capacité, **Poste de charge** ou **Centre de charge**, que vous validez.  
4.  Dans le champ **N°**, saisissez le nom du centre de charge ou du poste de charge.  
5.  Entrez les données nécessaires dans les autres champs, tels que **Heure début**, **Heure fin**, **Quantité**, et **Rebut**.  
6.  Choisissez l'action **Valider** pour valider les capacités.  

## <a name="to-view-work-center-ledger-entries"></a>Pour afficher les écritures comptables centre de charge  
Dans les fenêtres **Fiche centre de charge** et **Fiche poste de charge**, vous pouvez afficher les capacités validées en tant que résultat des ordres de fabrication terminés.    
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Centres de charge**, puis sélectionnez le lien connexe.  
2.  Ouvrez la fiche **Centre de charge** appropriée dans la liste, puis choisissez l'action **Écritures comptables capacité**.  

La fenêtre **Écritures comptables capacité** affiche les écritures validées relatives au centre de charge dans l'ordre de leur validation.   

## <a name="see-also"></a>Voir aussi  
[Production](production-manage-manufacturing.md)    
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)      
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

