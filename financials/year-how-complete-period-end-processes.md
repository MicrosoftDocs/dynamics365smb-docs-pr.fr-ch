---
title: "Clôture périodes | Microsoft Docs"
description: "Explique les processus permettant de clôturer une période."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 03/21/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1d0af3dbc94c32447facfbd24747ddc140cc1691
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="closing-periods"></a>Clôture périodes
[!INCLUDE[d365fin](includes/d365fin_md.md)] ne vous oblige pas à clôturer les périodes. Toutefois, il existe de nombreuses activités de clôture de période (fin de mois) que vous pouvez effectuer. Cette rubrique présente un aperçu des activités et des processus facultatifs pour les périodes de clôture.  

## <a name="general-ledger"></a>Écritures comptables
* Spécifiez des plages de date de validation à l'échelle du système.  

    Cela spécifie les dates entre lesquelles les validation sont autorisées. En fonction des besoins de votre activité, vous pouvez autoriser la validation au début du traitement de clôture d'exercice ou vers la fin. Pour plus d'informations, reportez vous à [Procédure: spécifier des périodes de validation](finance-how-specify-posting-periods.md).  
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

<!-- ### Fixed Assets
* Post all maintenance costs have been posted through the fixed asset journals or invoices.
* Post adjustments.
* Post appreciation.
* Post depreciation.
* Update and post the recurring fixed asset journal.-->

<!--### Intercompany
* Process Intercompany Postings.-->

## <a name="calculate-and-process-sales-tax"></a>Calculez et traitez la Sales Tax.
* Renseignez les déclarations de TVA.  

## <a name="see-also"></a>Voir aussi
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Clôture plans](year-close-books.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

