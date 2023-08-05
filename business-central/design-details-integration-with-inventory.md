---
title: "Détails de conception\_: intégration avec le stock"
description: Les zones d’application Warehouse Management et Inventory interagissent dans le stock physique et dans l’ajustement de stock ou entrepôt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# Détails de conception : intégration avec le stock

Les fonctionnalités Warehouse Management et Inventory interagissent dans le stock physique et dans l’ajustement de stock ou entrepôt.  

## Inventaire  

La page **Feuille inventaire entrepôt** est utilisée avec la page **Feuille inventaire** pour tous les entrepôts avancés. Le stock au niveau de l’emplacement est calculé, et une liste imprimée est donnée au magasinier. La liste indique les articles dans lesquels les emplacements doivent être comptabilisés.  
  
Le magasinier entre la quantité comptée sur la page **Feuille inventaire entrepôt** puis valide la feuille.  
  
Si la quantité comptée est supérieure à la quantité de la ligne feuille, un mouvement est validé pour cette différence à partir de l’emplacement ajustement par défaut jusqu’à l’emplacement compté. Cela augmente la quantité dans l’emplacement compté et diminue la quantité dans l’emplacement d’ajustement par défaut.  
  
Si la quantité comptée est inférieure à la quantité de la ligne feuille, un mouvement pour cette différence est validé à partir de l’emplacement compté jusqu’à l’emplacement d’ajustement par défaut. Cela diminue la quantité dans l’emplacement compté et augmente la quantité dans l’emplacement d’ajustement par défaut.  
  
Dans les configurations d’entrepôt avancées, la valeur du champ **Quantité (calculée)** est extraite à partir des écritures comptables article et celle du champ **Qté (constatée)** est extraite à partir des écritures entrepôt, hors le contenu de l’emplacement ajustement. Le champ **Quantité** spécifie la différence entre les deux premiers champs, qui doit être égale au contenu de l’emplacement ajustement.  
  
Lorsque vous validez la feuille stock physique, le stock et l’emplacement d’ajustement par défaut sont mis à jour.  

[!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]
  
## Ajustements d’entrepôt dans l’écriture article  

Vous utilisez la page **Feuille article** et la fonction **Calculer ajustement entrepôt** pour ajuster le stock dans l’écriture article conformément à ajustement qui a été apporté sur la quantité d’un article dans un emplacement entrepôt. Pour créer un lien entre stock et l’entrepôt, vous devez définir un emplacement d’ajustement par défaut par magasin.  
  
L’emplacement ajustement par défaut enregistre les articles dans l’entrepôt lorsque vous validez une entrée de stock. Toutefois, si vous validez une sortie, la quantité sur l’emplacement par défaut est également diminuée. Dans les deux cas, les écritures comptables article et les écritures entrepôt sont créées.  
  
> [!NOTE]  
> Les calculs d’inventaire n’incluent pas le bac d’ajustement.  
  
Pour ajuster le contenu de l’emplacement, utilisez une feuille article entrepôt, à partir de laquelle vous pouvez saisir le numéro d’article, le code zone, le code emplacement et la quantité que vous voulez ajuster.  
  
Si vous saisissez une quantité positive et validez la ligne, le stock enregistré dans les entrées de l’emplacement, et la quantité de l’emplacement ajustement par défaut diminue en conséquence.  
  
## Voir aussi  

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)  
[Détails de conception : disponibilité dans l’entrepôt](design-details-availability-in-the-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]