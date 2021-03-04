---
title: Activités facultatives pour les périodes de clôture | Microsoft Docs
description: Cette rubrique décrit les processus et les activités facultatifs pour la clôture des périodes comptables dans Business Central.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 104f63e07e4bfd8945f73581a4fb7810f946304f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755582"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Aperçu des tâches de clôture des périodes comptables
[!INCLUDE[prod_short](includes/prod_short.md)] ne vous oblige pas à clôturer les périodes. Toutefois, il existe de nombreuses activités de clôture de période (fin de mois) que vous pouvez effectuer. Cette rubrique présente un aperçu des activités et des processus facultatifs pour les périodes de clôture.  

## <a name="general-ledger"></a>Écritures comptables
* Spécifiez des plages de date de validation à l’échelle du système.  

    Cela spécifie les dates entre lesquelles les validation sont autorisées. En fonction des besoins de votre activité, vous pouvez autoriser la validation au début du traitement de clôture d’exercice ou vers la fin. Pour plus d’informations, reportez vous à [Spécifier des périodes de validation](finance-how-specify-posting-periods.md).  
* Effectuez tous les ajustements comptables nécessaires.  
* Mettez à jour et validez les feuilles abonnement.  
  <!--* Process Consolidations-->
* Exécutez les tableaux d’analyse comme suit :  
  * Ouvrez la page **Tableau d’analyse**, puis sélectionnez l’action **Imprimer**.  

## <a name="sales-and-receivables"></a>Ventes
* Validez l’ensemble des commandes, factures, avoirs et retours vente.  
* Validez l’ensemble des feuilles règlement.  
* Mettez à jour et validez les feuilles abonnement associées aux ventes.  
* Rapprochez la comptabilité client de la comptabilité.  
* Exécutez le traitement par lots **Supprimer cdes vente facturées**.  

## <a name="purchases-and-payables"></a>Achats
* Validez l’ensemble des commandes, factures, avoirs et retours achat.  
* Validez l’ensemble des feuilles paiement.  
* Mettez à jour et validez les feuilles abonnement associées aux achats.  
* Générez l’état **Comptabilité fournisseur âgée** et rapprochez la comptabilité fournisseur de la comptabilité.  
* Exécutez le traitement par lots **Supprimer cdes achat facturées**.  

COMPTES D’IMMOBILISATIONS
* Validez que tous les frais de maintenance ont été validés via les feuilles immobilisation ou factures.
* Validez les ajustements.
* Validez l’appréciation.
* Validez l’amortissement.
* Mettez à jour et validez la feuille abonnement immobilisations.

Intersociétés
* Traitement des transactions intersociétés

## <a name="calculate-and-process-sales-tax"></a>Calculez et traitez la Sales Tax.
* Renseignez les déclarations de TVA.  

## <a name="see-also"></a>Voir aussi
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Clôture plans](year-close-books.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]