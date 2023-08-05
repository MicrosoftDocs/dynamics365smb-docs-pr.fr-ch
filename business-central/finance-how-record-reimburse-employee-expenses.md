---
title: Enregistrer et rembourser les frais des employés
description: Validez les dépenses des employés avec la feuille comptabilité sur le compte de l’employé et validez par la suite un paiement sur le compte bancaire de l’employé pour rembourser les frais liés à l’entreprise.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.search.form: '63, 234, 625, 5224, 5237, 5238, 5239, 5240'
ms.date: 06/16/2021
ms.author: edupont
---
# Enregistrer et rembourser les frais des employés

[!INCLUDE[prod_short](includes/prod_short.md)] prend en charge les transactions des employés de la même manière que pour les fournisseurs. Par conséquent, les groupes comptabilisation des salariés existent pour s’assurer que les écritures comptables d’un salarié sont validées dans les comptes appropriés de la comptabilité.

> [!NOTE]  
> Les transactions des employés ne peuvent être validées que dans la devise société. Les paiements de remboursement aux employés ne prennent pas en charge les remises et les écarts de règlement.

Si les salariés dépensent leur propre argent pendant les activités commerciales, vous pouvez valider les frais sur le compte du salarié. Vous pouvez ensuite rembourser le salarié en faisant un paiement sur le compte bancaire du salarié, de la même façon que vous payez des fournisseurs.  

> [!TIP]
> Cet article explique comment enregistrer les frais dans les livres et comment rembourser l’employé. Votre organisation peut avoir un portail ou une application où les employés peuvent soumettre leurs notes de frais.

[!INCLUDE [prod_short](includes/prod_short.md)] est suffisamment flexible pour s’adapter à de nombreuses pratiques différentes. Les numéros de compte exacts à utiliser dépendent de la configuration et des processus de votre organisation.  

## Pour enregistrer les frais des salariés

Validez les frais salarié sur la page **Feuille comptabilité**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles comptabilité**, puis choisissez le lien associé.  
2. Ouvrez la feuille comptabilité appropriée. Pour en savoir plus, voir [Utiliser des feuilles comptabilité](ui-work-general-journals.md).
3. Sur une nouvelle ligne feuille, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Répétez l’étape 3 pour tous les frais que le salarié a supportés.

    > [!TIP]  
    > Si vous souhaitez saisir les lignes de dépenses au-dessus d’une ligne compte contrepartie du compte bancaire de l’employé, activez la case à cocher **Suggérer le montant contrepartie** de la ligne pour votre lot sur la page **Noms feuilles comptabilité**. Puis le champ **Montant** de la ligne compte contrepartie est automatiquement prérempli avec la valeur requise pour équilibrer les dépenses.
5. Choisissez l’action **Valider** pour enregistrer les frais sur le compte du salarié.

## Pour rembourser un employé

Vous remboursez des salariés en validant les paiements sur leur compte bancaire sur la page **Feuille paiement**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles paiement**, puis choisissez le lien associé.
2. Ouvrez la feuille comptabilité paiement appropriée. Pour en savoir plus, voir [Utiliser des feuilles comptabilité](ui-work-general-journals.md).
3. Renseignez les champs selon vos besoins. Pour plus d’informations, voir [Effectuer des paiements](payables-make-payments.md).
4. Sinon, choisissez l’action **Proposer paiements aux salariés** pour insérer automatiquement des lignes feuille pour les remboursements salarié en attente.
5. Sélectionnez l’action **Valider** pour enregistrer le remboursement.  

## Pour rapprocher les remboursements avec les écritures comptables du salarié

Appliquez les paiements des employés à leurs écritures comptables salariés ouvertes de la même façon que vous le faites pour les paiements des fournisseurs, par exemple sur la page **Feuille rapprochement bancaire**, en fonction des écritures de relevé bancaire connexes. Pour plus d’informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md). Sinon, vous pouvez effectuer une application manuelle sur la page **Écritures comptables salariés**. Pou plus d’informations, voir [Rapprocher des paiements fournisseur avec la feuille paiement ou à partir des écritures comptables fournisseur](payables-how-apply-purchase-transactions-manually.md).  

## Voir aussi

[Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md)  
[Utiliser des feuilles comptabilité](ui-work-general-journals.md)  
[Inverser des validations feuille et annuler les réceptions/envois](finance-how-reverse-journal-posting.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]