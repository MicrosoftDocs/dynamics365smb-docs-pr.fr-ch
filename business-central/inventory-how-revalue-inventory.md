---
title: Créer des nouvelles écritures valeur pour des articles dans le stock| Microsoft Docs
description: Décrit comment réévaluer ou amortir les entrées valeur d’un ou de plusieurs articles dans le stock en validant leur valeur calculée courante.
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'costing, inventory cost, value entries'
ms.search.forms: '5803,'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="revalue-inventory"></a>Réévaluer le stock
Pour réévaluer ou amortir un article ou une écriture comptable article spécifique, vous devez utiliser la feuille réévaluation.

## <a name="to-revalue-inventory"></a>Pour réévaluer le stock
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille réévaluation**, puis choisissez le lien associé.
2. Choisissez l’action **Calculer valeur stock**.
3. Sur la page **Calculer valeur stock**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Choisissez le bouton **OK**.
5. Sur chaque ligne de la page **Feuille réévaluation**, indiquez le nouveau coût unitaire dans le champ **Coût unitaire (réévalué)**. Vous pouvez aussi indiquer le nouveau montant total dans le champ **Valeur stock (réévaluée)**.

    Les champs appropriés sont automatiquement mis à jour. Remarque : le champ **Montant** affiche la modification réelle de la valeur du stock pour l’écriture comptable article sélectionnée. Il calcule la différence entre les champs **Valeur stock (calculée)** et **Valeur stock (réévaluée)**.
6. Lorsque vous avez renseigné toutes les lignes de la feuille réévaluation, choisissez l’action **Valider**.

Les nouvelles écritures valeur sont alors créées pour refléter les réévaluations que vous avez validées. Vous pouvez visualiser les nouvelles valeurs dans les fiches article concernées.

## <a name="see-also"></a>Voir aussi
[Détails de conception : réévaluation](design-details-revaluation.md)  
[Stock](inventory-manage-inventory.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
