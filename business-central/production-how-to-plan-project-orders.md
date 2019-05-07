---
title: Procédure de planification de projets de commandes | Microsoft Docs
description: Cette tâche de planification est lancée à partir d'une commande vente et utilise la page **Planification commande vente**. Une fois que vous avez créé un O.F. projet, vous pouvez le planifier davantage à l'aide de la page **Planning commande**.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 30fcb660632a529d907ffd675087960ef8ca6674
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "916916"
---
# <a name="plan-project-orders"></a>Planifier les O.F. projets
Cette tâche de planification est lancée à partir d'une commande vente et utilise la page **Planification commande vente**. Une fois que vous avez créé un O.F. projet, vous pouvez le planifier davantage à l'aide de la page **Planning commande**.  

## <a name="to-create-a-project-production-order"></a>Pour créer un O.F projet  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente**, puis sélectionnez le lien associé.  
2.  Sélectionnez la commande vente qui représente le projet de production, puis choisissez l'action **Planning**.  
4.  Sur la page **Planification commande vente**, choisissez l'action **Créer O.F**.  
5.  Sur la page **Créer commande à partir des ventes**, sélectionnez **O.F. projet** dans le champ **Type O.F**.  
6.  Cliquez sur le bouton **Oui**.  
7.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Ordres de production**, puis sélectionnez le lien associé.
8. Ouvrez l'ordre de fabrication que vous venez de créer.  

    Notez que le champ **Type origine** de l'ordre de fabrication indique **En-tête vente** et l'ordre comporte plusieurs lignes, une pour chaque article de la ligne vente à produire.  
9. Sélectionnez l'action **Planification**.
10. Sur la page **Planning commande**, choisissez l'action **Actualiser** pour calculer la nouvelle demande.  

La ligne d'en-tête de commande de la commande projet s'affiche avec toutes les lignes de demandes non satisfaites développées en-dessous. Bien que l'ordre de fabrication contienne les lignes de plusieurs articles produits, la demande totale pour toutes les lignes d'O.F. est répertoriée sous une ligne d'en-tête de commande sur la page **Planning commande** et le nom du client d'origine s'affiche. Vous pouvez maintenant passer à la planification de la demande en vous reportant à [Planifier de nouvelles demandes commande par commande](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Les lignes de demandes de l'ordre de fabrication projet qui ont **Ordre de fabrication** dans leur champ **Système réappro.** représentent des ordres de fabrication sous-jacents. Après avoir généré ces ordres de fabrication, vous devez à nouveau calculer un planning sur la page **Planning ordre** pour identifier toute demande de composant non réalisée pour ceux-ci. Cela signifie que le lien projet n'est plus visible sur la page. Cependant, si vous utilisez la fonctionnalité Chaînage, alors vous pouvez passer en revue les commandes approvisionnement effectuées sous la commande vente d'origine.  

## <a name="see-also"></a>Voir aussi
[Planifié](production-planning.md)   
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)   
[Pratiques de configuration recommandées : planification de l'approvisionnement](setup-best-practices-supply-planning.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
