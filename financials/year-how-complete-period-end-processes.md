---
title: "Activités facultatives pour les périodes de clôture | Microsoft Docs"
description: "Cette rubrique décrit les processus et les activités facultatifs pour la clôture des périodes comptables dans Finance and Operations, Business edition."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 344e294083813d41b415ad07e6e8acdd3fe5047b
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Aperçu des tâches de clôture des périodes comptables
[!INCLUDE[d365fin](includes/d365fin_md.md)] ne vous oblige pas à clôturer les périodes. Toutefois, il existe de nombreuses activités de clôture de période (fin de mois) que vous pouvez effectuer. Cette rubrique présente un aperçu des activités et des processus facultatifs pour les périodes de clôture.  

## <a name="general-ledger"></a>Écritures comptables
* Spécifiez des plages de date de validation à l'échelle du système.  

    Cela spécifie les dates entre lesquelles les validation sont autorisées. En fonction des besoins de votre activité, vous pouvez autoriser la validation au début du traitement de clôture d'exercice ou vers la fin. Pour plus d'informations, reportez vous à [Spécifier des périodes de validation](finance-how-specify-posting-periods.md).  
* Effectuez tous les ajustements comptables nécessaires.  
* Mettez à jour et validez les feuilles abonnement.  
  <!--* Process Consolidations-->
* Exécutez les tableaux d'analyse comme suit :  
  * Ouvrez la fenêtre **Tableau d'analyse**, puis sélectionnez l'action **Imprimer**.  

## <a name="sales-and-receivables"></a>Ventes
* Validez l'ensemble des commandes, factures, avoirs et retours vente.  
* Validez l'ensemble des feuilles règlement.  
* Mettez à jour et validez les feuilles abonnement associées aux ventes.  
* Rapprochez la comptabilité client de la comptabilité.  
* Exécutez le traitement par lots **Supprimer cdes vente facturées**.  

## <a name="purchases-and-payables"></a>Achats
* Validez l'ensemble des commandes, factures, avoirs et retours achat.  
* Validez l'ensemble des feuilles paiement.  
* Mettez à jour et validez les feuilles abonnement associées aux achats.  
* Générez l'état **Comptabilité fournisseur âgée** et rapprochez la comptabilité fournisseur de la comptabilité.  
* Exécutez le traitement par lots **Supprimer cdes achat facturées**.  

COMPTES D'IMMOBILISATIONS
* Validez que tous les frais de maintenance ont été validés via les feuilles immobilisation ou factures.
* Validez les ajustements.
* Validez l'appréciation.
* Validez l'amortissement.
* Mettez à jour et validez la feuille abonnement immobilisations.

Intersociétés
* Traitement des transactions intersociétés

## <a name="calculate-and-process-sales-tax"></a>Calculez et traitez la Sales Tax.
* Renseignez les déclarations de TVA.  

## <a name="see-also"></a>Voir aussi
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Clôture plans](year-close-books.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

