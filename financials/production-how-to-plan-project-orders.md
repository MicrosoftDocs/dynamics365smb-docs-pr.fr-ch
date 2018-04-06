---
title: "Procédure de planification de projets de commandes | Microsoft Docs"
description: "Cette tâche de planification est lancée à partir d'une commande vente et utilise la fenêtre **Planification commande vente**. Une fois que vous avez créé un O.F. projet, vous pouvez le planifier davantage à l'aide de la fenêtre **Planning commande**."
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
ms.openlocfilehash: 27b2571df137b489a72673251fb5a176bfa771fe
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="plan-project-orders"></a>Planifier les O.F. projets
Cette tâche de planification est lancée à partir d'une commande vente et utilise la fenêtre **Planification commande vente**. Une fois que vous avez créé un O.F. projet, vous pouvez le planifier davantage à l'aide de la fenêtre **Planning commande**.  

## <a name="to-create-a-project-production-order"></a>Pour créer un O.F projet  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente**, puis sélectionnez le lien connexe.  
2.  Sélectionnez la commande vente qui représente le projet de production, puis choisissez l'action **Planning**.  
4.  Dans la fenêtre **Planification commande vente**, choisissez l'action **Créer O.F**.  
5.  Dans la fenêtre **Créer commande à partir des ventes**, dans le champ **Type O.F.**, sélectionnez **O.F. projet**.  
6.  Cliquez sur le bouton **Oui**.  
7.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Ordres de fabrication**, puis sélectionnez le lien connexe.
8. Ouvrez l'ordre de fabrication que vous venez de créer.  

    Notez que le champ **Type origine** de l'ordre de fabrication indique **En-tête vente** et l'ordre comporte plusieurs lignes, une pour chaque article de la ligne vente à produire.  
9. Sélectionnez l'action **Planification**.
10. Dans la fenêtre **Planning commande**, choisissez l'action **Actualiser** pour calculer la nouvelle demande.  

La ligne d'en-tête de commande de la commande projet s'affiche avec toutes les lignes de demandes non satisfaites développées en-dessous. Bien que l'ordre de fabrication contienne les lignes de plusieurs articles produits, la demande totale pour toutes les lignes d'O.F. est répertoriée sous une ligne d'en-tête de commande dans la fenêtre **Planning commande** et le nom du client d'origine s'affiche. Vous pouvez maintenant passer à la planification de la demande en vous reportant à [Planifier de nouvelles demandes commande par commande](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Les lignes de demandes de l'ordre de fabrication projet qui ont **Ordre de fabrication** dans leur champ **Système réappro.** représentent des ordres de fabrication sous-jacents. Après avoir généré ces ordres de fabrication, vous devez à nouveau calculer un planning dans la fenêtre **Planning ordre** pour identifier toute demande de composant non réalisée pour ceux-ci. Cela signifie que le lien projet n'est plus visible dans la fenêtre. Cependant, si vous utilisez la fonctionnalité Chaînage, alors vous pouvez passer en revue les commandes approvisionnement effectuées sous la commande vente d'origine.  

## <a name="see-also"></a>Voir aussi
[Planifié](production-planning.md)   
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)   
[Pratiques de configuration recommandées : planification de l'approvisionnement](setup-best-practices-supply-planning.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

