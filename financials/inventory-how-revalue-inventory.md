---
title: "Procédure : réévaluer le stock| Microsoft Docs"
description: "Décrit comment réévaluer ou amortir la valeur d&quot;un ou de plusieurs articles dans le stock en validant leur valeur calculée courante."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0f7137b3ac4e2c68c1c9a9b94b3ba73e0438a4a9
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-revalue-inventory"></a>Procédure : Réévaluer le stock
Pour réévaluer ou amortir un article ou une écriture comptable article spécifique, vous devez utiliser la feuille réévaluation.

## <a name="to-revalue-inventory"></a>Pour réévaluer le stock
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Feuille réévaluation**, puis sélectionnez le lien associé.
2. Choisissez l'action **Calculer valeur stock**.
3. Dans la fenêtre **Calculer valeur stock**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Cliquez sur le bouton **OK**.
5. Sur chaque ligne de la fenêtre **Feuille réévaluation**, indiquez le nouveau coût unitaire dans le champ **Coût unitaire (réévalué)**. Vous pouvez aussi indiquer le nouveau montant total dans le champ **Valeur stock (réévaluée)**.

    Les champs appropriés sont automatiquement mis à jour. Remarque : le champ **Montant** affiche la modification réelle de la valeur du stock pour l'écriture comptable article sélectionnée. Il calcule la différence entre les champs **Valeur stock (calculée)** et **Valeur stock (réévaluée)**.
6. Lorsque vous avez renseigné toutes les lignes de la feuille réévaluation, choisissez l'action **Valider**.

Les nouvelles écritures valeur sont alors créées pour refléter les réévaluations que vous avez validées. Vous pouvez visualiser les nouvelles valeurs dans les fiches article concernées.

## <a name="see-also"></a>Voir aussi
[Stock](inventory-manage-inventory.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

