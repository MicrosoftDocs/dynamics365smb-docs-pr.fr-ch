---
title: "Transfert automatique et écritures combinées | Microsoft Docs"
description: "En comptabilité analytique, vous pouvez transférer les écritures comptables vers un type de coût à l'aide d'une validation combinée. Vous pouvez spécifier si un type de coût reçoit des écritures combinées dans le champ **Combiner écritures** dans la définition du type de coût. Le tableau suivant décrit les différentes options."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f4796d9796788d2fbbf5706688aec75a4ed9a6d8
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="automatic-transfer-and-combined-entries"></a>Transfert automatique et écritures combinées
En comptabilité analytique, vous pouvez transférer les écritures comptables vers un type de coût à l'aide d'une validation combinée. Vous pouvez spécifier si un type de coût reçoit des écritures combinées dans le champ **Combiner écritures** dans la définition du type de coût. Le tableau suivant décrit les différentes options.  

|Combiner des écritures|Désignation|  
|---------------------|-----------------|  
|Aucune|Chaque écriture comptable est transférée individuellement vers le type de coût correspondant.|  
|Jour|Les écritures comptables, dont la date de validation est identique, sont transférées en une seul écriture vers le type de coût correspondant.|  
|Mois|Toutes les écritures comptables du même mois calendaire sont transférées en une seul écriture vers le type de coût correspondant.|  

> [!IMPORTANT]  
>  Si vous avez coché la case **Transférer automatiquement à partir de la compta** dans la fenêtre **Paramètres comptabilité analytique**, [!INCLUDE[d365fin](includes/d365fin_md.md)] met à jour la comptabilité analytique après chaque validation comptable. Les écritures combinées ne sont pas possibles.  

## <a name="see-also"></a>Voir aussi  
 [Transférer les écritures comptables vers les écritures de coûts](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Critères de transfert des écritures comptables vers les écritures de coûts](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Résultats du transfert](finance-results-of-the-transfer.md)   
 [Transfert et validation des écritures de coûts](finance-transfer-and-post-cost-entries.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

