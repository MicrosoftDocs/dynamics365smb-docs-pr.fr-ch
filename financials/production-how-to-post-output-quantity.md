---
title: "Procédure de validation par lots de la production et des temps d'exécution | Microsoft Docs"
description: "La quantité produite représente l'avancée des travaux en prenant en compte la quantité achevée."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e885149e28c2e09dc244bc5c0a431e7b2fe047a5
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="batch-post-output-and-run-times"></a>Valider par lots la production et les temps d'exécution
La quantité produite représente l'avancée des travaux en prenant en compte la quantité achevée.  

> [!NOTE]
> Le stock est automatiquement mis à jour lorsque vous validez la quantité produite durant la dernière opération.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Pour valider les quantités produites pour une ou plusieurs lignes ordre de fabrication
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille production**, puis sélectionnez le lien connexe.  
2. Renseignez les champs en indiquant les données relatives à la fabrication et à la production. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Si l'opération est achevée, sélectionnez le champ **Terminé**.  

    Si l'entrepôt dans lequel les articles doivent être rangés utilise des emplacements mais pas le traitement de rangement,  affectez un code emplacement à la ligne feuille pour indiquer l'endroit où les articles doivent être placés dans l'entrepôt. Pour plus d'informations, voir [Rangement du résultat de fabrication ou d'assemblage](warehouse-how-to-put-away-production-output.md).  

4. Choisissez l'action **Valider** pour valider les opérations. La quantité produite est validée. L'article peut être expédié.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Pour valider les temps d'exécution pour une ou plusieurs lignes ordre de fabrication
Le temps d'exécution représente l'avancement des travaux en prenant en compte le temps de travail nécessaire.    

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille production**, puis sélectionnez le lien connexe.  
2. Renseignez les champs en indiquant les données relatives à la fabrication et à la production.  
3.  Si l'opération est achevée, sélectionnez le champ **Terminé**.  
4. Choisissez l'action **Valider** pour valider le temps passé par opération. Les écritures comptables capacité sont mises à jour pour les centres ou postes de charge utilisés.

## <a name="see-also"></a>Voir aussi  
[Production](production-manage-manufacturing.md)    
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)      
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

