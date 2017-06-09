---
title: Gestion des comptes bancaires| Microsoft Docs
description: Gestion des comptes bancaires
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 29dc32cd4bc1f745a576c6265bd7264e8108276a
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="managing-bank-accounts"></a>Gestion des comptes bancaires
Vous devez rapprocher régulièrement vos écritures comptables banque dans [!INCLUDE[d365fin](includes/d365fin_md.md)] avec les transactions bancaires associées dans les comptes bancaires de votre banque, puis valider le solde sur votre compte bancaire. Vous pouvez effectuer cette tâche soit dans le cadre du traitement des paiements représentés sur un relevé bancaire dans la **Feuille rapprochement bancaire**. Sinon, vous pouvez effectuer la tâche séparément du traitement des paiements, dans la fenêtre **Rapprochement bancaire**, qui prend en charge des écritures comptables chèque. Dans les deux cas, vous renseignez les fenêtres en important le relevé bancaire dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Parfois, vous devez transférer les montants entre comptes bancaires dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pour refléter les transferts effectués au niveau de votre banque. Vous effectuez cette tâche dans la fenêtre **Feuille comptabilité**, de différentes manières en fonction de la devise des fonds.

Avant de pouvoir gérer des comptes bancaires, vous devez configurer chaque compte bancaire en tant que fiche compte bancaire. En outre, vous devez configurer les services électroniques que vous pouvez utiliser pour l'importation de relevés bancaires et l'exportation de fichiers de paiement. Pour plus d'informations, reportez vous à [Configuration de comptes bancaires](bank-setup-banking.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

| Pour | Voir |
| --- | --- |
| Rapprocher des comptes bancaires en relation avec le traitement des paiements dans la fenêtre **Feuille rapprochement bancaire**. |[Procédure : lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Rapprocher des comptes bancaires, y compris les écritures comptables chèque, en tant que tâche distincte dans la fenêtre **Rapprochement bancaire**. |[Procédure : rapprocher des comptes bancaires séparément](bank-how-reconcile-bank-accounts-separately.md) |
| Valider des transferts entre comptes bancaires dans la même devise ou dans des devises différentes. |[Procédure : transfert de fonds à la banque](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Voir aussi
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)    
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  

