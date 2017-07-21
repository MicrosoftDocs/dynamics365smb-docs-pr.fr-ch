---
title: "Aperçu des tâches permettant de gérer la comptabilité fournisseur| Microsoft Docs"
description: "Décrit les tâches permettant de gérer la comptabilité fournisseur, par exemple, le paiement des créditeurs ou le lettrage de paiements sortants dans la comptabilité pour clôturer des factures ou des avoirs."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9684a91268927a4f1f4d249fef019c8f6ac00325
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a>Gestion des comptes fournisseur
Une grande partie de la gestion des comptes fournisseur consiste à payer les fournisseurs. Vous pouvez utiliser les fonctions pour ajouter des lignes de paiement pour les factures achat échues dans la fenêtre **Feuille paiement** . Pour effectuer rapidement des transactions bancaires, vous pouvez exporter plusieurs lignes feuille paiement vers un fichier, puis télécharger ensuite ce fichier vers votre banque. Vous pouvez également effectuer des paiements par chèque, notamment pour transmettre des chèques en tant que paiements électroniques.

Une autre tâche courante consiste à lettrer les paiements sortants à leurs écritures comptables fournisseur associées et de ce fait clôturer les factures achat ou les avoirs achat comme payés. Vous pouvez effectuer cette tâche dans la fenêtre **Feuille rapprochement bancaire** en important un fichier de relevé bancaire pour enregistrer rapidement les paiements. Les paiements sont lettrés pour ouvrir des écritures client ou fournisseur en faisant correspondre le texte de paiement et les informations d'écriture. Il existe plusieurs manières de vérifier et de modifier les correspondances avant de valider la feuille. Vous pouvez choisir de clôturer les écritures comptables compte bancaire ouvertes associées aux écritures comptables lettrées lorsque vous validez la feuille. Le compte bancaire est automatiquement rapproché lorsque tous les paiements sont lettrés.

Sinon, vous pouvez lettrer les paiements sortants manuellement dans la fenêtre **Feuille paiement** ou à partir des écritures comptables fournisseur associées.

Le tableau suivant décrit une série de tâches associées aux comptes fournisseur et inclut des liens vers les rubriques qui les décrivent.

| Pour | Voir |
| --- | --- |
| Générer des paiements fournisseur échus classés par ordre de priorité en fonction des escomptes et des pénalités de retard. Éventuellement, exporter les paiements vers un fichier bancaire lors de la validation. |[Exécuter des paiements](payables-make-payments.md) |
| Lettrer les paiements fournisseur automatiquement aux factures achat impayées en important un fichier de relevé bancaire. |[Procédure : lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Lettrer les paiements fournisseur aux factures achat impayées manuellement. |[Procédure : rapprocher les paiements fournisseur manuellement](payables-how-apply-purchase-transactions-manually.md) |
|Pour une évaluation de stock correcte, affectez les coûts articles ajoutés, tels que le fret, la manutention, les assurances, et transport, que vous encourez lorsque vous achetez.|[Procédure : Utiliser Frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md)|

## <a name="see-also"></a>Voir aussi
[Achats](purchasing-manage-purchasing.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Procédure : Utiliser Frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

