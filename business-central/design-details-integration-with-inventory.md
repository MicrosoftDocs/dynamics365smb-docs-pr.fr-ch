---
title: Détails de conception - Intégration avec le stock | Microsoft Docs
description: La zone d'application Warehouse Management et la zone d'application Inventory interagissent dans le stock physique et dans l'ajustement de stock ou entrepôt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 72be8f95a77052c00e127913de67d6b1f3397852
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390014"
---
# <a name="design-details-integration-with-inventory"></a>Détails de conception : intégration avec le stock
La zone d'application Warehouse Management et la zone d'application Inventory interagissent dans le stock physique et dans l'ajustement de stock ou entrepôt.  
  
## <a name="physical-inventory"></a>Inventaire  
 La page **Feuille inventaire entrepôt** est utilisée avec la page **Feuille inventaire** pour tous les entrepôts avancés. Le stock au niveau de l'emplacement est calculé, et une liste imprimée est donnée au magasinier. La liste indique les articles dans lesquels les emplacements doivent être comptabilisés.  
  
 Le magasinier entre la quantité comptée sur la page **Feuille inventaire entrepôt** puis valide la feuille.  
  
 Si la quantité comptée est supérieure à la quantité de la ligne feuille, un mouvement est validé pour cette différence à partir de l'emplacement ajustement par défaut jusqu'à l'emplacement compté. Cela augmente la quantité dans l'emplacement compté et diminue la quantité dans l'emplacement d'ajustement par défaut.  
  
 Si la quantité comptée est inférieure à la quantité de la ligne feuille, un mouvement pour cette différence est validé à partir de l'emplacement compté jusqu'à l'emplacement d'ajustement par défaut. Cela diminue la quantité dans l'emplacement compté et augmente la quantité dans l'emplacement d'ajustement par défaut.  
  
 Dans les configurations d'entrepôt avancées, la valeur du champ **Quantité (calculée)** est extraite à partir des écritures comptables article et celle du champ **Qté (constatée)** est extraite à partir des écritures entrepôt, hors le contenu de l'emplacement ajustement. Le champ **Quantité** spécifie la différence entre les deux premiers champs, qui doit être égale au contenu de l'emplacement ajustement.  
  
 Lorsque vous validez la feuille stock physique, le stock et l'emplacement d'ajustement par défaut sont mis à jour.  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a>Ajustements d'entrepôt dans l'écriture article  
 Vous utilisez la page **Feuille article** et la fonction **Calculer ajustement entrepôt** pour ajuster le stock dans l'écriture article conformément à ajustement qui a été apporté sur la quantité d'un article dans un emplacement entrepôt. Pour créer un lien entre stock et l'entrepôt, vous devez définir un emplacement d'ajustement par défaut par magasin.  
  
 L'emplacement ajustement par défaut enregistre les articles dans l'entrepôt lorsque vous validez une entrée de stock. Toutefois, si vous validez une sortie, la quantité sur l'emplacement par défaut est également diminuée. Dans les deux cas, les écritures comptables article et les écritures entrepôt sont créées.  
  
> [!NOTE]  
>  L'emplacement ajustement n'est pas inclus dans le calcul de disponibilité.  
  
 Si vous souhaitez ajuster le contenu de l'emplacement, vous pouvez utiliser la feuille article entrepôt, à partir de laquelle vous pouvez saisir le numéro d'article, le code zone, le code emplacement et la quantité que vous voulez ajuster.  
  
 Si vous saisissez une quantité positive et validez la ligne, le stock enregistré dans les entrées de l'emplacement, et la quantité de l'emplacement ajustement par défaut diminue en conséquence.  
  
## <a name="see-also"></a>Voir aussi  
 [Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)   
 [Détails de conception : disponibilité dans l'entrepôt](design-details-availability-in-the-warehouse.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]