---
title: "Procédure d'utilisation des familles d'articles dans la production | Microsoft Docs"
description: "Lorsque vous personnalisez un calendrier principal pour votre société ou pour l'un de ses partenaires commerciaux, votre tâche consiste essentiellement à modifier le statut des jours ouvrés et chômés."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 060c58991ae48ba768f5c1c0bd7442228e6bc976
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-production-families"></a>Procédure : utiliser les familles de production
Une famille de production est un groupe d'articles distincts dont la relation repose sur la similitude de leur processus de fabrication. Si vous formez des familles de production, certains articles peuvent être fabriqués plusieurs fois au cours d'une production, ce qui optimise la consommation de matière.

Dans le champ **Quantité** de la fenêtre **Famille**, entrez la quantité à produire lorsque l'ensemble de la famille a été fabriquée une fois.

## <a name="example"></a>Exemple :
Dans les processus de découpe, quatre pièces du même article et dix pièces d'un autre peuvent être fabriquées simultanément à partir d'une plaque. La machine à découpe découpe les 14 pièces en une seule fois.

Le regroupement d'éléments en familles de production permet de réduire la quantité perte car ce qui devrait normalement constituer un rebut définitif, lors de la fabrication de grosses pièces, est utilisé pour fabriquer de petits articles.

## <a name="to-set-up-a-production-family"></a>Pour configurer une famille de production
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Familles**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-familily"></a>Pour produire selon une famille de production
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **O.F. planifiés fermes**, puis sélectionnez le lien connexe.
2. Créez un ordre de fabrication. Pour plus d'informations, voir [Procédure : créer des ordres de fabrication](production-how-to-create-production-orders.md).
3. Dans le champ **Type origine**, sélectionnez **Famille**.  
4. Dans le champ **N° origine**, sélectionnez la famille de production appropriée.

## <a name="see-also"></a>Voir aussi
[Procédure : créer des nomenclatures de production](production-how-to-create-production-boms.md)  
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[Planifié](production-planning.md)   
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

