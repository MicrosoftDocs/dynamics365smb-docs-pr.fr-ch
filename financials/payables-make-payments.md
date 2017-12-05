---
title: "Aperçu des tâches permettant de gérer les paiements aux fournisseurs| Microsoft Docs"
description: "Décrit les tâches permettant de gérer les paiements aux fournisseurs ou aux créditeurs, y compris la validation de lignes paiement et d'obtenir un aperçu du solde échu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: c8766d42b579397e63676c1d46fb8a03cbe24aae
ms.contentlocale: fr-ch
ms.lasthandoff: 10/17/2017

---
# <a name="making-payments"></a>Effectuer des paiements
Lorsque vous effectuez des paiements aux fournisseurs ou des remboursements aux salariés, vous validez les lignes paiement associées dans la fenêtre **Feuille paiement**. Vous pouvez utiliser la fonction **Proposer paiements fournisseur** pour rechercher les paiements fournisseurs échus. Vous pouvez également utiliser l'état **Fourn. : Échéancier** pour obtenir un aperçu des paiements fournisseurs échus.

À partir de la feuille de paiements, vous pouvez imprimer des chèques informatiques ou effectuer un enregistrement lorsque les chèques sont rédigés. Si vous sélectionnez **Informatique** dans le champ **Mode émission paiement**, toutes les lignes représentant des chèques doivent être imprimées avant que les lignes feuille puissent être validées.

Lorsque les paiements sont validés, vous pouvez les exporter-vers un fichier bancaire à télécharger vers votre banque pour traitement.

Une fois les paiements effectués au niveau de votre banque, vous devez les lettrer avec les écritures comptables fournisseur ou salarié ouvertes correspondantes. Vous pouvez le faire manuellement ou en important un fichier de relevé bancaire et en lettrant les paiements automatiquement. Pour plus d'informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

| Pour | Voir |
| --- | --- |
|Utilisez la fenêtre **Feuille paiement**, qui est fondée sur la feuille comptabilité, pour valider les paiements aux fournisseurs ou aux salariés.|[Utilisation de feuilles comptabilité](ui-work-general-journals.md)|
| Utiliser une fonction pour proposer des paiements fournisseur en fonction de critères sélectionnés, tels que la date d'échéance, la possibilité d'escompte et vos liquidités. |[Procédure : proposer des paiements fournisseur](payables-how-suggest-vendor-payments.md) |
|Remboursez les frais personnels des salariés pour les activités liées à l'entreprise en effectuant le paiement sur leur compte bancaire.|[Procédure : enregistrer et rembourser les frais des employés](finance-how-record-reimburse-employee-expenses.md)|
| Émettre des chèques pour les paiements fournisseur, sous forme de documents imprimés ou de chèques informatiques. Annuler des chèques avant ou après la validation. |[Procédure : utilisation des chèques](payables-how-work-checks.md) |
| Payez le fournisseur en liquide ou par chèque et validez le paiement lorsque vous validez la facture. |[Procédure : établir rapidement des factures achat](finance-how-to-settle-purchase-invoices-promptly.md) |
| Assurez-vous que la banque efface uniquement les chèques et les montants validés en envoyant un fichier contenant des informations de paiement, du chèque et du fournisseur. |[Procédure : exporter des fichiers Positive Pay](finance-how-positive-pay.md) |
|Exporter des paiements à partir de la fenêtre **Feuille paiement** vers un fichier bancaire que vous téléchargez vers votre banque pour traitement, y compris un transfert électronique de fond (EFT) en Amérique du Nord. |[Procédure : exportation de paiements vers un fichier bancaire](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a>Voir aussi
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Achats](purchasing-manage-purchasing.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

