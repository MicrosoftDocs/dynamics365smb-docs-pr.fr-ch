---
title: "Enregistrer et rembourser les frais personnels des salariés pour les activités commerciales | Microsoft Docs"
description: "Validez les dépenses des employés avec la feuille comptabilité sur le compte de l'employé et validez par la suite un paiement sur le compte bancaire de l'employé pour rembourser les frais liés à l'entreprise."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: 0e10011c598678134cb7badbd9a3be97751b4424
ms.contentlocale: fr-ch
ms.lasthandoff: 10/17/2017

---
# <a name="how-to-record-and-reimburse-employees-expenses"></a>Procédure : enregistrer et rembourser les frais des employés
[!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge les transactions des employés de la même manière que pour les fournisseurs. Par conséquent, les groupes comptabilisation des salariés existent pour s'assurer que les écritures comptables d'un salarié sont validées dans les comptes appropriés de la comptabilité.

> [!NOTE]  
> Les transactions des employés ne peuvent être validées que dans la devise société. Les paiements de remboursement aux employés ne prennent pas en charge les remises et les écarts de règlement.

Si les salariés dépensent leur propre argent pendant les activités commerciales, vous pouvez valider les frais sur le compte du salarié. Vous pouvez ensuite rembourser le salarié en faisant un paiement sur le compte bancaire du salarié, de la même façon que vous payez des fournisseurs.

## <a name="to-record-an-employees-expense"></a>Pour enregistrer les frais des salariés
Validez les frais salarié dans la fenêtre **Feuille comptabilité**.
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles comptabilité**, puis sélectionnez le lien connexe.
2. Ouvrez la feuille comptabilité appropriée. Pour plus d'informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).
3. Sur une nouvelle ligne feuille, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Répétez l'étape 3 pour tous les frais que le salarié a supportés.

    > [!TIP]  
    > Si vous souhaitez saisir les lignes de dépenses au-dessus d'une ligne compte contrepartie du compte bancaire de l'employé, activez la case à cocher **Suggérer le montant contrepartie** de la ligne pour votre lot dans la fenêtre **Noms feuilles comptabilité**. Puis le champ **Montant** de la ligne compte contrepartie est automatiquement prérempli avec la valeur requise pour équilibrer les dépenses.
5. Choisissez l'action **Valider** pour enregistrer les frais sur le compte du salarié.

## <a name="to-reimburse-an-employee"></a>Pour rembourser un employé
Vous remboursez des salariés en validant les paiements sur leur compte bancaire dans la fenêtre **Feuille paiement**.
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles paiement**, puis sélectionnez le lien connexe.
2. Ouvrez la feuille comptabilité paiement appropriée. Pour plus d'informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).
3. Renseignez les champs selon vos besoins. Pour plus d'informations, reportez-vous à [Effectuer des paiements](payables-make-payments.md).
4. Sinon, choisissez l'action **Proposer paiements aux salariés** pour insérer automatiquement des lignes feuille pour les remboursements salarié en attente.
5. Sélectionnez l'action **Valider** pour enregistrer le remboursement.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Pour rapprocher les remboursements avec les écritures comptables du salarié
Appliquez les paiements des employés à leurs écritures comptables salariés ouvertes de la même façon que vous le faites pour les paiements des fournisseurs, par exemple dans la fenêtre **Feuille rapprochement bancaire**, en fonction des écritures de relevé bancaire connexes. Pour plus d'informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md). Sinon, vous pouvez effectuer une application manuelle dans la fenêtre **Écritures comptables salariés**. Pour plus d'informations, consultez [Procédure : rapprocher les paiements fournisseur manuellement](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Voir aussi
[Procédure : Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Procédure : inversion d'une validation](finance-how-reverse-journal-posting.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

