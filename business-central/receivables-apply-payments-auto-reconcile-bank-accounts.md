---
title: Rapprocher des comptes bancaires et des lettrage de paiements | Microsoft Docs
description: Décrit les tâches de rapprochement de vos comptes bancaires, client, et fournisseur, valider des règlements ou des frais, et lettrer des paiements automatiquement.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e89a21ddecdce2bab0da44c447612a24d2173ec7
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5394139"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Lettrage automatique des paiements et rapprochement des comptes bancaires
Vous devez régulièrement rapprocher vos comptes bancaires, créances client et créances fournisseur en lettrant les paiements enregistrés au niveau de la banque à leurs factures impayées et avoirs associés ou à d’autres écritures ouvertes dans [!INCLUDE[prod_short](includes/prod_short.md)].  

Vous pouvez effectuer cette tâche sur la page **Feuille rapprochement bancaire**, par exemple, en important un fichier ou un flux de relevé bancaire pour enregistrer rapidement les paiements. Les paiements sont lettrés pour ouvrir des écritures client ou fournisseur selon les correspondances entre le texte de paiement et les informations d’écriture. Vous pouvez réviser et modifier les lettrages automatiques avant de valider la feuille. Vous pouvez choisir de clôturer les écritures comptables compte bancaire ouvertes associées aux écritures comptables lettrées lorsque vous validez la feuille. Le compte bancaire est automatiquement rapproché lorsque tous les paiements sont lettrés.

La logique qui gère la correspondance automatique du texte de paiement avec les informations d’écriture est configurée sur la page **Règles lettrage paiement** comme une série de règles hiérarchisées que vous pouvez modifier.

Vous pouvez également rapprocher des comptes bancaires sans rapprocher simultanément des paiements. Vous effectuez ce travail sur la page **Rapprochement bancaire**. Pour plus d’informations, voir [Rapprocher des comptes bancaires](bank-how-reconcile-bank-accounts-separately.md).   

Pour importer des relevés bancaires en tant que flux bancaire, vous devez d’abord configurer et activer le service Envestnet Yodlee Bank Feeds, puis associer vos comptes bancaires aux comptes bancaires connexes en ligne. Pour plus d’informations, voir [Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

Vous pouvez également utiliser l’extension AMC Banking 365 Fundamentals pour convertir un fichier de relevé bancaire, à partir de n’importe quel format, en flux de données que vous pouvez importer dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Utilisation de l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

| Pour | Voir |
| --- | --- |
| Lettrer des paiements aux écritures comptables client ou fournisseur ouvertes en important un relevé bancaire, et rapprocher le compte bancaire lorsque tous les paiements sont lettrés. |[Rapprocher les paiements à l’aide de l’application automatique](receivables-how-reconcile-payments-auto-application.md) |
| Appliquer manuellement les paiements en affichant les informations détaillées sur les données de correspondance et des suggestions d’écritures ouvertes candidates à l’application des paiements. |[Réviser ou lettrer les paiements après un lettrage automatique](receivables-how-review-apply-payments-auto-application.md) |
| Résoudre les paiements qui ne peuvent pas être lettrés automatiquement à leurs écritures comptables ouvertes associées. Par exemple si les montants sont différents ou si une écriture comptable associée n’existe pas. |[Rapprocher les paiements qui ne peuvent pas être lettrés automatiquement](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Lier le texte des paiements à un client spécifique, fournisseur ou comptes généraux pour toujours valider les réceptions récurrentes en liquide ou les dépenses vers ces comptes quand ils ne peuvent être appliqués à aucun document. |[Mapper du texte sur des paiements récurrents avec des comptes pour un rapprochement automatique](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Configurez les règles pour définir comment les paiements/transactions bancaires doivent être automatiquement lettrés avec leurs écritures comptables ouvertes associées lorsque vous utilisez la fonction **Lettrer automatiquement** sur la page **Feuille rapprochement bancaire**.|[Définir des règles pour le lettrage automatique des paiements](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/use-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi
[Rapprochement des comptes bancaires](bank-how-reconcile-bank-accounts-separately.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]