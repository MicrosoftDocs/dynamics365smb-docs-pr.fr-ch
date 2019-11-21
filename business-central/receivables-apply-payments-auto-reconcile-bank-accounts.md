---
title: Rapprocher des comptes bancaires et des lettrage de paiements | Microsoft Docs
description: Décrit les tâches de rapprochement de vos comptes bancaires, client, et fournisseur, valider des règlements ou des frais, et lettrer des paiements automatiquement.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 60a3cd3398e8a90160ab311dba1ae75fe70305b2
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692526"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Lettrage automatique des paiements et rapprochement des comptes bancaires
Vous devez régulièrement rapprocher vos comptes bancaires, créances client et créances fournisseur dans Project en lettrant les paiements enregistrés au niveau de la banque à leurs factures impayées et avoirs associés ou à d'autres écritures ouvertes dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Vous pouvez effectuer cette tâche sur la page **Feuille rapprochement bancaire** en important un fichier ou un flux de relevé bancaire pour enregistrer rapidement les paiements. Les paiements sont lettrés pour ouvrir des écritures client ou fournisseur selon les correspondances entre le texte de paiement et les informations d'écriture. Vous pouvez réviser et modifier les lettrages automatiques avant de valider la feuille. Vous pouvez choisir de clôturer les écritures comptables compte bancaire ouvertes associées aux écritures comptables lettrées lorsque vous validez la feuille. Le compte bancaire est automatiquement rapproché lorsque tous les paiements sont lettrés.

Vous pouvez également rapprocher des comptes bancaires sans rapprocher simultanément des paiements. Vous effectuez ce travail sur la page **Rapprochement bancaire**. Pour plus d'informations, reportez vous à [Rapprocher des comptes bancaires séparément](bank-how-reconcile-bank-accounts-separately.md).   

Pour importer des relevés bancaires en tant que flux bancaire, vous devez d'abord configurer et activer le service Envestnet Yodlee Bank Feeds, puis associer vos comptes bancaires aux comptes bancaires connexes en ligne. Pour plus d'informations, voir [Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

Vous pouvez également utiliser l'extension AMC Banking 365 Fundamentals pour convertir un fichier de relevé bancaire, à partir de n'importe quel format, en flux de données que vous pouvez importer dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Utilisation de l'extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

| Pour | Voir |
| --- | --- |
| Lettrer des paiements aux écritures comptables client ou fournisseur ouvertes en important un relevé bancaire, et rapprocher le compte bancaire lorsque tous les paiements sont lettrés. |[Rapprocher les paiements à l'aide de l'application automatique](receivables-how-reconcile-payments-auto-application.md) |
| Appliquer manuellement les paiements en affichant les informations détaillées sur les données de correspondance et des suggestions d'écritures ouvertes candidates à l'application des paiements. |[Réviser ou lettrer les paiements après un lettrage automatique](receivables-how-review-apply-payments-auto-application.md) |
| Résoudre les paiements qui ne peuvent pas être lettrés automatiquement à leurs écritures comptables ouvertes associées. Par exemple si les montants sont différents ou si une écriture comptable associée n'existe pas. |[Rapprocher les paiements qui ne peuvent pas être lettrés automatiquement](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Lier le texte des paiements à un client spécifique, fournisseur ou comptes généraux pour toujours valider les réceptions récurrentes en liquide ou les dépenses vers ces comptes quand ils ne peuvent être appliqués à aucun document. |[Mapper du texte sur les paiements récurrents aux comptes pour un rapprochement automatique](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a>Voir aussi
[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
