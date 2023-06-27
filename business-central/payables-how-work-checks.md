---
title: 'Emettre, imprimer et annuler des chèques'
description: "Décrit comment émettre des chèques à l’aide de la feuille paiement, imprimer des chèques, et annuler ou afficher les écritures comptables chèque dans Business\_Central."
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment journal, print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256, 404,'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="make-check-payments"></a>Effectuer des paiements par chèque

Vous pouvez émettre des chèques par voie électronique et manuelle dans [!INCLUDE[prod_short](includes/prod_short.md)]. Ces deux méthodes utilisent la feuille paiement pour émettre des chèques aux fournisseurs. Vous pouvez également annuler des chèques et afficher les écritures comptables chèque.

La procédure suivante explique comment payer un fournisseur avec un chèque informatique en lettrant le paiement à la facture fournisseur appropriée, en imprimant le chèque et en validant le paiement comme payé. Il en résulte des écritures comptables fournisseur positives, lettrées aux écritures comptables banque négatives, et des chèques physiques qui seront traités dans la banque.

Vous pouvez payer avec deux types de chèques. Pour les deux types, le champ **Type compte contrepartie** ou **Type compte** doit contenir **Compte bancaire**.

- **Informatique** : sélectionnez cette option si vous souhaitez imprimer un chèque du montant de la ligne feuille paiement. Vous devez imprimer les chèques avant de pouvoir valider les lignes feuille.
- **Manuel** : sélectionnez cette option si vous avez créé un chèque manuellement et que vous souhaitez créer une écriture comptable chèque correspondante de ce montant. Si vous utilisez cette option, vous ne pouvez pas imprimer le chèque.

> [!NOTE]  
> Pour s’assurer que la banque efface uniquement les chèques et les montants validés, vous pouvez envoyer un fichier contenant des informations de paiement, du chèque et du fournisseur. Pour plus d’informations, voir [Exporter des fichiers Positive Pay](finance-how-positive-pay.md).

> [!IMPORTANT]
> Votre imprimante doit être correctement configurée pour les formulaires chèque, et vous devez définir la mise en page de chèque à utiliser. Pour plus d’informations, voir [Sélectionner une mise en page de chèque](finance-how-define-check-layouts.md). Vous pouvez également envoyer le chèque au format PDF, par exemple.  

Vous pouvez imprimer jusqu’à 10 factures sur une page pour un talon de chèque. Si un chèque s’applique à plus de 10 factures, lorsque vous imprimez le talon, nous annulons le chèque sur la première page et imprimons le mot NUL sur le chèque. Nous imprimons ensuite les factures restantes et le montant total du chèque sur la deuxième page.

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Pour payer une facture fournisseur avec un chèque informatique

La section suivante décrit comment payer un fournisseur par chèque. La procédure est la même pour rembourser un client par chèque.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles paiement**, puis choisissez le lien associé.
2. Renseignez les lignes feuille paiement. Pour plus d’informations, voir [Enregistrer des paiements et des remboursements](payables-how-post-payments-refunds.md).
3. Dans le champ **Code mode de règlement**, sélectionnez **Chèque**.
4. Dans le champ **Mode émission paiement**, sélectionnez **Informatique**.
5. Choisissez l’action **Imprimer chèque**.
6. Renseignez les champs nécessaires sur la page **Chèque**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Si votre imprimante est configurée pour imprimer des chèques, choisissez le bouton **Imprimer**. Sinon, choisissez le bouton **Envoyer à**, sélectionnez l’option **Document PDF**, puis cliquez sur le bouton **OK** et imprimez le document PDF.

    Les chèques physiques peuvent maintenant être envoyés aux fournisseurs pour traitement. Validez le paiement comme lettré au fournisseur et payé dans le système.
8. Sélectionnez l’action **Valider**.

Des écritures comptables fournisseur et des écritures comptables banque entièrement lettrées sont créées.

> [!NOTE]  
> Si vous souhaitez imprimer et payer des chèques en plusieurs devises sur des comptes bancaires différents, vous devez exécuter le traitement par lots **Imprimer chèque** pour chacune de ces devises et préciser le compte bancaire concerné.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Pour annuler des chèques imprimés qui ne sont pas validés

Vous pouvez annuler des chèques non validés après leur impression par l’intermédiaire de l’action **Annuler chèque** sur la page **Feuille paiement**.

1. Sur la page **Feuille paiement**, sélectionnez **Annuler chèque**, puis sélectionnez les chèques à annuler.

## <a name="to-void-checks"></a>Pour annuler des chèques

Lorsque des paiements par chèque ont été validés, vous pouvez uniquement annuler des chèques à partir des écritures comptables banque ainsi obtenues.

> [!IMPORTANT]
> Si le chèque est appliqué à une facture, annulez d’abord le chèque afin que la facture puisse être remboursée, puis annulez le chèque. Si le chèque a été imprimé et n’a pas payé de facture, choisissez **Annuler chèque uniquement** comme décrit dans cette section.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Sélectionnez le compte bancaire approprié, sélectionnez l’action **Modifier**, puis l’action **Écritures comptables chèque**.
3. Sur la page **Écritures comptables chèque**, sélectionnez l’action **Annuler chèque**.
4. Cochez la case **Annuler chèque uniquement**.
5. Cliquez sur le bouton **OK**.

## <a name="to-view-a-summary-of-posted-checks"></a>Pour afficher un résumé des chèques validés

Si vous souhaitez examiner les chèques validés, par exemple pour vérifier plusieurs chèques payés à un fournisseur, vous pouvez utiliser l’état **Banque : Liste chèques émis**.
1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Compte bancaire : Liste chèques émis**, puis sélectionnez le lien associé.
2. Définissez les filtres appropriés, puis cliquez sur le bouton **Aperçu**.

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/use-checks-dynamics-365-business-central/) associée

## <a name="see-also"></a>Voir aussi

[Effectuer des paiements](payables-make-payments.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Exporter un fichier Positive Pay](finance-how-positive-pay.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
