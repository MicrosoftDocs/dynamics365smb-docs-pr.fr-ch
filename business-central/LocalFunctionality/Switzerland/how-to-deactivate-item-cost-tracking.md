---
title: "Procédure : Désactiver le suivi des coûts article"
description: "Lorsque le stock n'est pas suivi pour un article, le coût article n'est pas forcément suivi, et une écriture comptable article n'est pas forcément créée."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: c6f10f8252c00bf0a599f9fa794ee36c41ce92be
ms.openlocfilehash: abf481ae651863e5ec290aacb58684980c31edbe
ms.contentlocale: fr-ch
ms.lasthandoff: 07/30/2018

---
# <a name="deactivate-item-cost-tracking"></a>Désactiver le suivi des coûts article
Lorsque le stock n'est pas suivi pour un article, le coût article n'est pas forcément suivi, et une écriture comptable article n'est pas forcément créée.  

Vous pouvez désactiver le coût de l'article suivant pour un article. Généralement, le suivi des coûts des articles doit être désactivé pour les articles consommables, tels que les déchets de papier et pour les services comptabilisés comme des articles, tels que les frais de stationnement à tarif fixe. Le suivi du coût des articles devrait être désactivé pour les articles pour lesquels le suivi pourrait être trompeur. Les articles pour lesquels suivre des coûts article a été désactivé sont exclus de la réservation, de la vérification de disponibilité, de la traçabilité et des systèmes de planification matière.  

## <a name="to-deactivate-item-cost-tracking"></a>Pour désactiver le suivi des coûts article  

1.  Cliquez sur l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'article requis, puis cliquez sur l'action **Modifier**.  
3.  Sur le raccourci **Général**, cochez la case **Pas de stockage**.  

    Une écriture comptable article n'est pas créée lorsque vous validez une transaction pour cet article. Pour plus d'informations, voir la table Écriture comptable article.  

    > [!NOTE]  
    >  Vous ne pouvez pas sélectionner la case à cocher **Pas de stock** sur un article pour lequel les écritures comptables article ont déjà été validées.  

4.  Choisissez le bouton **OK**.  

## <a name="see-also"></a>Voir aussi  
 [Gestion des stocks, Suisse](swiss-inventory-management.md)

