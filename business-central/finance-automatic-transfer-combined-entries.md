---
title: Transfert automatique et écritures combinées | Microsoft Docs
description: En comptabilité analytique, vous pouvez transférer les écritures comptables vers un type de coût à l'aide d'une validation combinée. Vous pouvez spécifier si un type de coût reçoit des écritures combinées dans le champ **Combiner écritures** dans la définition du type de coût. Le tableau suivant décrit les différentes options.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 6f58e569bea6a42a9ee695095ce308e7a69e2a8d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820411"
---
# <a name="automatic-transfer-and-combined-entries"></a>Transfert automatique et écritures combinées
En comptabilité analytique, vous pouvez transférer les écritures comptables vers un type de coût à l'aide d'une validation combinée. Vous pouvez spécifier si un type de coût reçoit des écritures combinées dans le champ **Combiner écritures** dans la définition du type de coût. Le tableau suivant décrit les différentes options.  

|Combiner des écritures|Désignation|  
|---------------------|-----------------|  
|Aucune|Chaque écriture comptable est transférée individuellement vers le type de coût correspondant.|  
|Jour|Les écritures comptables, dont la date de validation est identique, sont transférées en une seul écriture vers le type de coût correspondant.|  
|Mois|Toutes les écritures comptables du même mois calendaire sont transférées en une seul écriture vers le type de coût correspondant.|  

> [!IMPORTANT]  
>  Si vous avez coché la case **Transférer automatiquement à partir de la compta** sur la page **Paramètres comptabilité analytique**, [!INCLUDE[d365fin](includes/d365fin_md.md)] met à jour la comptabilité analytique après chaque validation comptable. Les écritures combinées ne sont pas possibles.  

## <a name="see-also"></a>Voir aussi  
 [Transfert et validation des écritures de coûts](finance-transfer-and-post-cost-entries.md)   
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
