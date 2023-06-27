---
title: Activités facultatives pour les périodes de clôture
description: Cette rubrique décrit les processus et les activités facultatifs pour la clôture des périodes comptables dans Business Central.
author: jswymer
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments'
ms.date: 08/29/2022
ms.author: jswymer
---
# <a name="overview-of-tasks-to-close-accounting-periods" />Aperçu des tâches de clôture des périodes comptables

[!INCLUDE[prod_short](includes/prod_short.md)] ne vous oblige pas à clôturer les périodes. Toutefois, il existe de nombreuses activités de clôture de période (fin de mois) que vous pouvez effectuer. Cette rubrique présente un aperçu des activités et des processus facultatifs pour les périodes de clôture.  

## <a name="general-ledger" />Écritures comptables

* Spécifiez des plages de date de validation à l’échelle du système.  

    Cela spécifie les dates entre lesquelles les validation sont autorisées. En fonction des besoins de votre activité, vous pouvez autoriser la validation au début du traitement de clôture d’exercice ou vers la fin. En savoir plus sur [Spécifier les périodes comptables](finance-how-specify-posting-periods.md).  
* Effectuez tous les ajustements comptables nécessaires.  
* Mettez à jour et validez les feuilles abonnement.  
  <!--* Process Consolidations-->
* Exécutez les états financiers comme suit :  
  * Ouvrez la page **États financiers**, puis sélectionnez l’action **Imprimer**.  

## <a name="sales-and-receivables" />Ventes

* Validez l’ensemble des commandes, factures, avoirs et retours vente.  
* Validez l’ensemble des feuilles règlement.  
* Mettez à jour et validez les  feuilles abonnement relatives aux ventes.  
* Rapprochez la comptabilité client de la comptabilité.  
* Exécutez le traitement par lots **Supprimer cdes vente facturées**.  

## <a name="purchases-and-payables" />Achats

* Validez l’ensemble des commandes, factures, avoirs et retours achat.  
* Validez l’ensemble des feuilles paiement.  
* Mettez à jour et validez les  feuilles abonnement relatives aux achats.  
* Générez l’état **Comptabilité fournisseur âgée** et rapprochez la comptabilité fournisseur de la comptabilité.  
* Exécutez le traitement par lots **Supprimer cdes achat facturées**.  

## <a name="fixed-assets" />Immobilisations

* Validez que tous les frais de maintenance ont été validés via les feuilles immobilisation ou factures.
* Validez les ajustements.
* Validez l’appréciation.
* Validez l’amortissement.
* Mettez à jour et validez la feuille abonnement immobilisations.

## <a name="intercompany" />Intersociétés

* Traitez les transactions intersociétés.

## <a name="calculate-and-process-sales-tax" />Calculer et traiter la taxe de vente

* Renseignez les déclarations de TVA.  

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/modules/close-fiscal-year-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi

[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Clôture plans](year-close-books.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
