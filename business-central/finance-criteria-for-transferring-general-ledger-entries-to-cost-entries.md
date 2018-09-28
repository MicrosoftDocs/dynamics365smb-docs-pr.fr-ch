---
title: "Critères de transfert des écritures comptables vers les écritures de coûts | Microsoft Docs"
description: "Il est important de comprendre les critères pour le transfert des écritures comptables aux écritures de coûts. Lors du transfert, le traitement par lots pour **Transférer les écritures comptables vers CA** applique les critères suivants pour déterminer si les écritures comptables sont transférées et comment."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b1ac9d3d0ab7022d5a11ad1642cf496d07bc81ce
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a>Critères de transfert des écritures comptables vers les écritures de coûts
Il est important de comprendre les critères pour le transfert des écritures comptables aux écritures de coûts. Lors du transfert, le traitement par lots pour **Transférer les écritures comptables vers CA** applique les critères suivants pour déterminer si les écritures comptables sont transférées et comment.  

Les écritures comptables sont transférées si :  

-   Les écritures ont des sections analytiques correspondant à un centre de coûts ou à un coût associé.  
-   Les écritures ont des sections analytiques correspondant à un centre de coûts et à un coût associé. Pour ces écritures, le centre de coûts est prioritaire. Vous pouvez ainsi éviter qu'un type de coût apparaisse à la fois dans un coût associé et dans un centre de coûts, ce qui le comptabiliserait deux fois dans les statistiques.  
-   Le numéro de document dans les écritures est vide. C'est pourquoi, il s'affichera avec le numéro de document 0000 dans les écritures de coûts.  
-   Les écritures sont transférées vers un type de coût qui autorise les écritures combinées. Ces écritures sont transférées ainsi sur une base mensuelle ou journalière.  

Les écritures comptables ne sont pas transférées si :  

-   Les écritures ont des sections analytiques ne correspondant ni à un centre de coûts ni à un coût associé.  
-   Les écritures sont égales à zéro.  
-   Les écritures ont un compte général qui a été supprimé.  
-   Les écritures ont un compte général qui n'est pas du type **Comptes de gestion**.  
-   Les écritures ont un compte général sans type de coût affecté.  
-   La date de validation des écritures est antérieure à **Date début pour transfert comptabilité**.  
-   Les écritures ont été validées avec une date de clôture. Il s'agit généralement des écritures qui redéfinissent le solde des comptes de gestion sur la fin de l'exercice.  

## <a name="see-also"></a>Voir aussi  
[Comptabilité pour les coûts](finance-manage-cost-accounting.md)  
 [Transférer les écritures comptables vers les écritures de coûts](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Transfert et validation des écritures de coûts](finance-transfer-and-post-cost-entries.md)   
 [À propos de la comptabilité analytique](finance-about-cost-accounting.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

