---
title: "Détails de conception - Intégration avec le stock | Microsoft Docs"
description: "La zone d'application Warehouse Management et la zone d'application Inventory interagissent dans le stock physique et dans l'ajustement de stock ou entrepôt."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 00a12f3f2203ed3b22cfee1af6aa8f155ca5fe4b
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-integration-with-inventory"></a>Détails de conception : intégration avec le stock
La zone d'application Warehouse Management et la zone d'application Inventory interagissent dans le stock physique et dans l'ajustement de stock ou entrepôt.  
  
## <a name="physical-inventory"></a>Inventaire  
 La fenêtre **Feuille inventaire entrepôt** est utilisée avec la fenêtre **Feuille inventaire** pour tous les entrepôts avancés. Le stock au niveau de l'emplacement est calculé, et une liste imprimée est donnée au magasinier. La liste indique les articles dans lesquels les emplacements doivent être comptabilisés.  
  
 Le magasinier entre la quantité comptée dans la fenêtre **Feuille inventaire entrepôt** puis valide la feuille.  
  
 Si la quantité comptée est supérieure à la quantité de la ligne feuille, un mouvement est validé pour cette différence à partir de l'emplacement ajustement par défaut jusqu'à l'emplacement compté. Cela augmente la quantité dans l'emplacement compté et diminue la quantité dans l'emplacement d'ajustement par défaut.  
  
 Si la quantité comptée est inférieure à la quantité de la ligne feuille, un mouvement pour cette différence est validé à partir de l'emplacement compté jusqu'à l'emplacement d'ajustement par défaut. Cela diminue la quantité dans l'emplacement compté et augmente la quantité dans l'emplacement d'ajustement par défaut.  
  
 Dans les configurations d'entrepôt avancées, la valeur du champ **Quantité (calculée)** est extraite à partir des écritures comptables article et celle du champ **Qté (constatée)** est extraite à partir des écritures entrepôt, hors le contenu de l'emplacement ajustement. Le champ **Quantité** spécifie la différence entre les deux premiers champs, qui doit être égale au contenu de l'emplacement ajustement.  
  
 Lorsque vous validez la feuille stock physique, le stock et l'emplacement d'ajustement par défaut sont mis à jour.  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a>Ajustements d'entrepôt dans l'écriture article  
 Vous utilisez la fenêtre **Feuille article** et la fonction **Calculer ajustement entrepôt** pour ajuster le stock dans l'écriture article conformément à ajustement qui a été apporté sur la quantité d'un article dans un emplacement entrepôt. Pour créer un lien entre stock et l'entrepôt, vous devez définir un emplacement d'ajustement par défaut par magasin.  
  
 L'emplacement ajustement par défaut enregistre les articles dans l'entrepôt lorsque vous validez une entrée de stock. Toutefois, si vous validez une sortie, la quantité sur l'emplacement par défaut est également diminuée. Dans les deux cas, les écritures comptables article et les écritures entrepôt sont créées.  
  
> [!NOTE]  
>  L'emplacement ajustement n'est pas inclus dans le calcul de disponibilité.  
  
 Si vous souhaitez ajuster le contenu de l'emplacement, vous pouvez utiliser la feuille article entrepôt, à partir de laquelle vous pouvez saisir le numéro d'article, le code zone, le code emplacement et la quantité que vous voulez ajuster.  
  
 Si vous saisissez une quantité positive et validez la ligne, le stock enregistré dans les entrées de l'emplacement, et la quantité de l'emplacement ajustement par défaut diminue en conséquence.  
  
## <a name="see-also"></a>Voir aussi  
 [Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)   
 [Détails de conception : disponibilité dans l'entrepôt](design-details-availability-in-the-warehouse.md)
