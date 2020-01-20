---
title: Aperçu des tâches permettant de gérer la comptabilité fournisseur| Microsoft Docs
description: Décrit les tâches permettant de gérer la comptabilité fournisseur, par exemple, le paiement des créditeurs ou le lettrage de paiements sortants dans la comptabilité pour clôturer des factures ou des avoirs.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 01/13/2020
ms.author: edupont
ms.openlocfilehash: ea3091ecb79a345bf4bed9572e98de057cde38db
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/14/2020
ms.locfileid: "2954250"
---
# <a name="managing-payables"></a>Gestion des comptes fournisseur

Une grande partie de la gestion des comptes fournisseurs consiste à payer vos fournisseurs, ou à rembourse vos salariés de leurs dépenses. Vous pouvez utiliser les fonctions pour ajouter des lignes de paiement pour les factures achat échues sur la page **Feuille paiement** . Pour effectuer rapidement des transactions bancaires, vous pouvez exporter plusieurs lignes feuille paiement vers un fichier, puis télécharger ensuite ce fichier vers votre banque. Vous pouvez également effectuer des paiements par chèque, notamment pour transmettre des chèques en tant que paiements électroniques.

Une autre tâche courante consiste à lettrer les paiements sortants à leurs écritures comptables fournisseur ou salarié associées et de ce fait, clôturer les factures achat, les avoirs achat ou les comptes salariés comme payés. Vous pouvez effectuer cette tâche sur la page **Feuille rapprochement bancaire** en important un fichier de relevé bancaire pour enregistrer rapidement les paiements. Les paiements sont lettrés aux écritures client, fournisseur ou salarié ouvertes en faisant correspondre le texte de paiement et les informations d'écriture. Il existe plusieurs manières de vérifier et de modifier les correspondances avant de valider la feuille. Vous pouvez choisir de clôturer les écritures comptables compte bancaire ouvertes associées aux écritures comptables lettrées lorsque vous validez la feuille. Le compte bancaire est automatiquement rapproché lorsque tous les paiements sont lettrés.

Sinon, vous pouvez lettrer les paiements sortants manuellement sur la page **Feuille paiement** ou à partir des écritures comptables fournisseur ou salarié associées.

Le tableau suivant décrit une série de tâches associées aux comptes fournisseur et inclut des liens vers les rubriques qui les décrivent.

| Pour | Voir |
| --- | --- |
| Générez les paiements fournisseurs ou les remboursements salariés dus, préparez les paiements par chèque, et exportez les paiements vers un fichier bancaire lors de la validation. |[Effectuer des paiements](payables-make-payments.md) |
| Lettrer les paiements fournisseur automatiquement aux factures achat impayées en important un fichier de relevé bancaire. |[Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Lettrer les paiements fournisseur aux factures achat impayées manuellement. |[Rapprocher des paiements fournisseur avec la feuille paiement ou à partir des écritures comptables fournisseur](payables-how-apply-purchase-transactions-manually.md) |
|Pour une évaluation de stock correcte, affectez les coûts articles ajoutés, tels que le fret, la manutention, les assurances, et transport, que vous encourez lorsque vous achetez.|[Utiliser Frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md)|
|Remboursez les frais personnels des salariés pour les activités liées à l'entreprise en effectuant le paiement sur leur compte bancaire.|[Enregistrer et rembourser les frais des employés](finance-how-record-reimburse-employee-expenses.md)|

## <a name="see-related-training-at-microsoft-learnlearnpathsprocess-customer-vendor-payments-dynamics-365-business-central"></a>Voir la formation associée sur [Microsoft Learn](/learn/paths/process-customer-vendor-payments-dynamics-365-business-central/)

## <a name="see-also"></a>Voir aussi
[Achats](purchasing-manage-purchasing.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Utiliser des frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
