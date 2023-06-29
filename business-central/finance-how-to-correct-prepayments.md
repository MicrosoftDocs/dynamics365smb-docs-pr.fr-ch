---
title: Corriger des acomptes
description: Vous pouvez apporter une correction à une commande après avoir validé une facture d’acompte pour la commande et ajouter de nouvelles lignes à une commande après avoir émis un acompte.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '44, 48, 42, 50, 52, 9305, 9307'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="correct-prepayments"></a><a name="correct-prepayments"></a>Corriger des acomptes

Vous pouvez apporter une correction à une commande après avoir validé une facture acompte pour la commande. Vous pouvez ajouter des lignes à une commande après avoir émis un acompte, puis vous pouvez valider une autre facture acompte, mais vous ne pouvez pas supprimer une ligne d’une commande après avoir facturé un acompte pour la ligne.  

> [!TIP]
> Si vous avez enregistré une facture de prépaiement pour une facture vente que vous corrigez ou annulez ensuite, vous devez également corriger ou annuler le prépaiement.

## <a name="to-correct-a-prepayment"></a><a name="to-correct-a-prepayment"></a>Pour corriger des acomptes

La procédure suivante explique comment émettre un avoir acompte pour annuler tous les acomptes facturés pour une commande vente.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Ouvrez la commande vente appropriée.
3. Choisissez l’action **Acompte**, puis l’action **Valider avoir acompte** ou **Valider et imprimer avoir acompte**.  
4. Sur la page **Avoir vente**, continuez à corriger les écritures appropriées, comme pour toute avoir vente. Pour plus d’informations, reportez-vous à [Traiter les retours ou annulations de ventes](sales-how-process-sales-returns-cancellations.md).  

    > [!NOTE]  
    > Pour réduire le montant dans le champ **Montant ligne**, vous devez commencer par augmenter le pourcentage d’acompte sur la ligne afin que la valeur du champ **Montant ligne acompte** ne soit pas réduite au point d’être inférieure à la valeur du champ **Fact. montant acompte**.

5. Pour valider une facture acompte pour les nouvelles lignes dans l’avoir vente, sélectionnez l’action **Acompte**, puis l’action **Valider facture acompte** ou **Publier et imprimer facture acompte**.  
6. Pour émettre une autre facture acompte, augmentez le montant d’acompte sur une ou plusieurs lignes, puis validez la facture acompte. Une nouvelle facture est créée pour la différence entre les montants d’acompte facturés et le nouveau montant d’acompte.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/prepayment-invoices-dynamics-365-business-central/) associée

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Facturation d’acomptes](finance-invoice-prepayments.md)  
[Procédure pas à pas : configuration et facturation d’acomptes](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
