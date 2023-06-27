---
title: Aperçu des tâches permettant de gérer les paiements aux fournisseurs
description: 'Décrit les tâches permettant de gérer les paiements aux fournisseurs ou aux créditeurs, y compris la validation de lignes paiement et d’obtenir un aperçu du solde échu.'
author: edupont04
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '254, 256, 1190, 1191, 1227, 1228, 1229'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="making-payments" />Effectuer des paiements

Lorsque vous effectuez des paiements aux fournisseurs ou aux clients, ou des remboursements aux salariés, vous validez les lignes paiement associées sur la page **Feuille paiement**. La feuille paiement est une feuille comptabilité qui est optimisée pour effectuer des paiements et inclut un certain nombre de fonctionnalités puissantes telles que la fonction **Proposer paiements fournisseur** qui rassemble les paiements fournisseurs échus, et l’état **Fourn. : Échéancier** qui affiche un aperçu des paiements fournisseur échus.  

Vous pouvez lancer le processus de paiement depuis des listes, des fiches, et des écritures comptables pour les fournisseurs, les clients, ainsi que les salariés. Chacune de ces pages a un bouton démarrant le flux de paiement et vous permettant de renseigner la feuille paiement.  

À partir de la feuille de paiements, vous pouvez imprimer des chèques informatiques ou effectuer un enregistrement lorsque les chèques sont rédigés. Si vous sélectionnez **Informatique** dans le champ **Mode émission paiement**, toutes les lignes représentant des chèques doivent être imprimées avant que les lignes feuille puissent être validées.

Lorsque les paiements sont validés, vous pouvez les exporter-vers un fichier bancaire à télécharger vers votre banque pour traitement.

Une fois les paiements effectués au niveau de votre banque, vous devez les lettrer avec les écritures comptables fournisseur ou salarié ouvertes correspondantes. Vous pouvez le faire manuellement ou en important un fichier de relevé bancaire et en lettrant les paiements automatiquement. Pour plus d’informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

| À | Voir |
| --- | --- |
|Comprendre les fonctions de base de la page **Feuille paiement**, qui est basée sur la feuille comptabilité, pour préparer la validation des paiements aux fournisseurs ou employés.|[Utiliser des feuilles comptabilité](ui-work-general-journals.md)|
|Valider les paiements aux fournisseurs ou aux salariés, et les remboursements aux clients et lettrer éventuellement les paiements aux factures/avoirs impayés pour les clôturer comme payés.|[Enregistrer des paiements et des remboursements](payables-how-post-payments-refunds.md)|
| Utiliser une fonction sur la page **Feuille paiement** pour proposer des paiements fournisseur en fonction de critères sélectionnés, tels que la date d’échéance, la possibilité d’escompte et vos liquidités. |[Proposer paiements fournisseur](payables-how-suggest-vendor-payments.md) |
| Émettre des chèques pour les paiements fournisseur ou les remboursements client, sous forme de documents imprimés ou de chèques informatiques. Annuler des chèques avant ou après la validation. |[Effectuer des paiements par chèque](payables-how-work-checks.md) |
|Effectuer des paiements électroniques conformément à la norme de virement SEPA de l’UE.|[Réalisation de paiements avec l’extension AMC Banking 365 Fundamentals ou le virement SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Payez un fournisseur en liquide ou par chèque et validez le paiement lorsque vous validez la facture. |[Établir rapidement des factures achat](finance-how-to-settle-purchase-invoices-promptly.md) |
| Assurez-vous que la banque efface uniquement les chèques et les montants validés en envoyant un fichier contenant des informations de paiement, du chèque et du fournisseur. |[Exporter un fichier Positive Pay](finance-how-positive-pay.md) |

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/paths/process-customer-vendor-payments-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi

[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Achats](purchasing-manage-purchasing.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
