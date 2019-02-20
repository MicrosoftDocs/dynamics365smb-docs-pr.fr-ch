---
title: "Aperçu des tâches permettant de gérer la comptabilité client | Microsoft Docs"
description: "Décrit les tâches permettant de gérer les clients et d'appliquer les paiements aux écritures comptables client ou fournisseur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 11/28/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: 5621345418f8da0165fa5685fd3b4a50dd43ae9d
ms.contentlocale: fr-ch
ms.lasthandoff: 11/29/2018

---
# <a name="managing-receivables"></a>Gestion des comptes client
Une étape normale de n'importe quelle opération financière consiste à rapprocher des comptes bancaires, ce qui nécessite de lettrer les paiements entrants avec des écritures fournisseur ou client pour clôturer les factures vente et les avoirs achat comme payés.

Bien que la plupart des clients dans les environnements B2B payent un certain temps après la livraison en laissant les factures vente validées ouvertes jusqu'à ce qu'elles soient clôturées (lettrées) par le département Comptabilité client à réception du paiement, certaines factures vente peuvent être payées immédiatement, par exemple avec PayPal. Ces factures sont immédiatement lettrées comme payées lors de leur validation et n'apparaissent donc pas comme paiements à traiter dans la Comptabilité client. Pour plus d'informations, voir [Facturation des ventes](sales-how-invoice-sales.md), par exemple.  

Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], l'une des méthodes les plus rapides pour enregistrer les paiements à partir de la page **Feuille rapprochement bancaire** consiste à importer un fichier ou un flux de relevé bancaire. Les paiements sont lettrés pour ouvrir des écritures client ou fournisseur selon les correspondances entre le texte de paiement et les informations d'écriture. Vous pouvez consulter et modifier les correspondances avant de valider la feuille, puis clôturer les écritures comptables banque pour les écritures comptables lorsque vous validez la feuille. Le compte bancaire est rapproché lorsque tous les paiements sont lettrés.

D'autres pages vous permettent de lettrer des paiements ou de rapprocher des comptes bancaires :

* La page **Rapprochements bancaires** qui vous permet de rapprocher des comptes bancaires en mettant en correspondance les lignes de relevé bancaire importées avec les écritures comptables compte bancaire du système. Vous pouvez également rapprocher des paiements par chèque. Pour plus d'informations, reportez vous à [Rapprocher des comptes bancaires séparément](bank-how-reconcile-bank-accounts-separately.md). Vous ne pouvez pas lettrer des paiements.
* La page **Enregistrement de paiement** qui vous permet de lettrer manuellement les paiements reçus en liquide, par chèque ou par transaction bancaire par rapport à une liste générée de documents vente impayés. Notez que cette fonctionnalité est uniquement disponible pour les documents vente. Vous ne pouvez pas lettrer des paiements sortants, et vous ne pouvez pas rapprocher des comptes bancaires.
* La page **Feuille règlement** où vous pouvez valider manuellement les réceptions dans un compte général, client ou autre en saisissant une ligne règlement. Vous pouvez soit lettrer la réception ou le remboursement avec une ou plusieurs écritures ouvertes avant de valider la feuille règlement, ou à partir des écritures comptables client. Vous ne pouvez pas rapprocher des comptes bancaires.  

Les autres aspects de la gestion des comptes client comprennent le recouvrement des soldes échus, y compris les intérêts de retard et des relances, et de définir les comptes bancaires pour autoriser le retrait des paiements des clients de leur compte automatiquement.

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

| Pour | Voir |
| --- | --- |
| Lettrer des paiements aux écritures comptables client ou fournisseur ouvertes sur la base d'un fichier ou flux de relevé bancaire importé, et rapprocher le compte bancaire lorsque tous les paiements sont lettrés. |[Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
|Configurez des mappages entre le texte des paiements et des comptes de débit, de crédit et de contrepartie spécifiques afin que ces paiements soient validés dans les comptes spécifiés lorsque vous validez la feuille rapprochement bancaire.|[Mapper du texte sur les paiements récurrents aux comptes pour un rapprochement automatique](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)|
|Sur la page **Lettrage paiement**, visualisez toutes les écritures ouvertes candidates au paiement et pour afficher les informations détaillées pour chaque écriture sur la correspondance des données sur laquelle une application de paiement est basée.|[Réviser ou lettrer les paiements manuellement après un lettrage automatique](receivables-how-review-apply-payments-auto-application.md)|
| Lettrer les paiements aux écritures comptables client ouvertes selon la saisie manuelle dans la liste des documents vente échus. |[Rapprocher les paiements client manuellement à partir de la liste des documents vente échus](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Valider les règlements ou les remboursements pour les clients dans la feuille règlement et lettrer aux écritures comptables client, à partir de la feuille ou des écritures comptables validées. |[Rapprocher les paiements client manuellement](receivables-how-apply-sales-transactions-manually.md) |
| Rappeler aux clients les soldes échus, calculer les intérêts et les intérêts de retard, et gérer les comptes clients. |[Collecte des soldes restants](receivables-collect-outstanding-balances.md) |
| Prévoyez quand les paiements seront exécutés en retard pour les documents vente. | [Extension Prévisions de retard de paiement](ui-extensions-late-payment-prediction.md) |
|Avec le consentement de votre client, collectez les paiements directement à partir du compte bancaire du client en euro uniquement.|[Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md)|
|Bloquer la saisie ou la validation d'un client sur des documents, par exemple à cause de l'insolvabilité.|[Bloquer des clients](receivables-how-block-customers.md)|
|Assurez-vous de connaître le coût des articles expédiés en affectant les coûts articles ajoutés, tels que le fret, la manutention, les assurances, et transport, que vous encourez après la vente.|[Utiliser Frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md)|
|Configurer une valeur de tolérance selon laquelle le système clôt une facture même si le règlement, tenant compte d'éventuelles remises, ne couvre pas intégralement le montant de la facture.|[Utilisation des écarts de règlement et des écarts d'escompte](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Voir aussi
[Ventes](sales-manage-sales.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

