---
title: Gestion des comptes fournisseur| Microsoft Docs
description: Gestion des comptes fournisseur
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 92b16c52589a07661d9ff080e9ef8a0f6be633f7
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


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

## <a name="see-also"></a>Voir aussi
[Achats](purchasing-manage-purchasing.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

