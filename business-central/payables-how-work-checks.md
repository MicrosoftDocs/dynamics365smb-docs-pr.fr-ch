---
title: "Emettre, imprimer et annuler des chèques| Microsoft Docs"
description: "Décrit comment émettre des chèques à l'aide de la feuille paiement, imprimer des chèques, et annuler ou afficher les écritures comptables chèque dans Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 39b48fbd34b29db56b39712fbd2cbf5dc91fefc6
ms.contentlocale: fr-ch
ms.lasthandoff: 04/26/2018

---
# <a name="make-check-payments"></a>Effectuer des paiements par chèque
Vous pouvez émettre des chèques par voie électronique et manuelle dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ces deux méthodes utilisent la feuille paiement pour émettre des chèques aux fournisseurs. Vous pouvez également annuler des chèques et afficher les écritures comptables chèque.

La procédure suivante explique comment payer un fournisseur avec un chèque informatique en lettrant le paiement à la facture fournisseur appropriée, en imprimant le chèque et en validant le paiement comme payé. Il en résulte des écritures comptables fournisseur positives, lettrées aux écritures comptables banque négatives, et des chèques physiques qui seront traités dans la banque.

Vous pouvez payer avec deux types de chèques. Pour les deux types, le champ **Type compte contrepartie** ou **Type compte** doit contenir **Compte bancaire**.

- **Informatique** : sélectionnez cette option si vous souhaitez imprimer un chèque du montant de la ligne feuille paiement. Vous devez imprimer les chèques avant de pouvoir valider les lignes feuille. Vous pouvez uniquement sélectionner **Informatique** si
- **Manuel** : sélectionnez cette option si vous avez créé un chèque manuellement et que vous souhaitez créer une écriture comptable chèque correspondante de ce montant. Si vous utilisez cette option, vous ne pouvez pas imprimer le chèque.

> [!NOTE]  
> Pour s'assurer que la banque efface uniquement les chèques et les montants validés, vous pouvez envoyer un fichier contenant des informations de paiement, du chèque et du fournisseur. Pour plus d'informations, voir [Exporter des fichiers Positive Pay](finance-how-positive-pay.md).

Votre imprimante doit être correctement configurée pour les formulaires chèque, et vous devez définir la mise en page de chèque à utiliser. Pour plus d'informations, voir [Définir les mises en page de chèques](finance-how-define-check-layouts.md)

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Pour payer une facture fournisseur avec un chèque informatique
La section suivante décrit comment payer un fournisseur par chèque. La procédure est la même pour rembourser un client par chèque.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles paiement**, puis sélectionnez le lien connexe.
2. Renseignez les lignes feuille paiement. Pour plus d'informations, voir [Enregistrer des paiements et des remboursements](payables-how-post-payments-refunds.md).
3. Dans le champ **Code mode de règlement**, sélectionnez **Chèque**.
4. Dans le champ **Mode émission paiement**, sélectionnez **Informatique**.
5. Choisissez l'action **Imprimer chèque**.
6. Dans la fenêtre **Chèque**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Cliquez sur le bouton **Envoyer à**, sélectionnez l'option **Document PDF**, puis cliquez sur le bouton **OK**.

    Les chèques physiques peuvent maintenant être déposés à la banque pour traitement. Validez le paiement comme lettré au fournisseur et payé dans le système.
8. Sélectionnez l'action **Valider**.

Des écritures comptables fournisseur et des écritures comptables banque entièrement lettrées sont créées.

> [!NOTE]  
> Si vous souhaitez imprimer et payer des chèques en plusieurs devises sur des comptes bancaires différents, vous devez exécuter le traitement par lots **Imprimer chèque** pour chacune de ces devises et préciser le compte bancaire concerné.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Pour annuler des chèques imprimés qui ne sont pas validés
Vous pouvez annuler des chèques non validés après leur impression par l'intermédiaire de l'action **Annuler chèque** de la fenêtre **Feuille paiement**.

1. Dans la fenêtre **Feuille paiement**, sélectionnez **Annuler chèque**, puis sélectionnez les chèques à annuler.

## <a name="to-void-checks"></a>Pour annuler des chèques
Lorsque des paiements par chèque ont été validés, vous pouvez uniquement annuler des chèques à partir des écritures comptables banque ainsi obtenues.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Sélectionnez le compte bancaire approprié, sélectionnez l'action **Modifier**, puis l'action **Écritures comptables chèque**.
3. Dans la fenêtre **Écritures comptables chèque**, sélectionnez l'action **Annuler chèque**.
4. Cochez la case **Annuler chèque uniquement**.
5. Choisissez le bouton **OK**.

## <a name="to-view-a-summary-of-posted-checks"></a>Pour afficher un résumé des chèques validés
Si vous souhaitez examiner les chèques validés, par exemple pour vérifier plusieurs chèques payés à un fournisseur, vous pouvez utiliser l'état **Banque : Liste chèques émis**.
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Banque : Liste chèques émis**, puis sélectionnez le lien connexe.
2. Définissez les filtres appropriés, puis cliquez sur le bouton **Aperçu**.

## <a name="see-also"></a>Voir aussi
[Effectuer des paiements](payables-make-payments.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Exporter un fichier Positive Pay](finance-how-positive-pay.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

