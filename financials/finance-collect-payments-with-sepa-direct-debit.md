---
title: "Prélèvement SEPA dans Dynamics 365 | Microsoft Docs"
description: "Vous pouvez collecter les paiements directement à partir du compte bancaire du client en fonction du format SEPA."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 0447e6c9f84457589df5cbc1efaecb2de24e7295
ms.contentlocale: fr-ch
ms.lasthandoff: 09/27/2017

---
# <a name="collecting-payments-with-sepa-direct-debit"></a>Recouvrement de paiements par prélèvement automatique SEPA
Avec le consentement de votre client, vous pouvez collecter les paiements directement à partir du compte bancaire du client en fonction du format SEPA.  

 Tout d'abord, définissez le format d'exportation du fichier bancaire qui indique à votre banque comment effectuer un prélèvement automatique. Ensuite, paramétrez le mode de paiement du client. Enfin, configurez le mandat de prélèvement qui reflète votre accord avec le client pour collecter leurs paiements pendant une certaine durée.  

 Pour demander à la banque de transférer le montant du paiement du compte bancaire du client vers le compte de votre société, vous créez une écriture de collection de prélèvement, qui conserve des informations sur les comptes bancaires, les factures de vente concernées et le mandat de prélèvement. Vous exportez ensuite un fichier XML basé sur l'écriture de collection, que vous envoyez à votre banque pour traitement. La banque vous communiquera tous les paiements impossibles à traiter, et vous devez rejeter manuellement les écritures de collection prélèvement automatique en question.  

 Vous pouvez définir des codes vente client standard avec les informations de mode et de mandat de prélèvement. Vous pouvez ensuite utiliser le traitement par lots **Créer factures client standard** pour générer plusieurs factures vente avec les informations de prélèvement automatique préremplies. Ceci peut être effectué manuellement ou automatiquement, en fonction de la date d'échéance du paiement.  

 Lorsque les paiements sont traités avec succès, tel que communiqué par votre banque, vous pouvez valider les réceptions de paiement directement à partir de la fenêtre **Écritures recouvrement prélèvement**, ou en déplaçant les lignes paiement vers la feuille où vous validez des réceptions de paiement, tels que la fenêtre **Feuille règlement**. Sinon, en fonction de votre processus de gestion de trésorerie, vous pouvez attendre et lettrer les paiements lors du rapprochement bancaire.  

> [!NOTE]  
>  Pour réunir les paiements à l'aide du prélèvement SEPA, la devise sur la facture vente doit être l'EURO.  

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.   

|**Pour**|**Voir**|  
|------------|-------------|  
|Préparez les formats de compte bancaire, les modes de paiement et les accords clients pour le prélèvement automatique SEPA.|[Procédure : configurer un prélèvement SEPA](finance-how-to-set-up-sepa-direct-debit.md)|  
|Demander à votre banque de transférer les montants de paiement des comptes bancaires de vos clients vers le compte de votre société en fonction de votre configuration du prélèvement automatique SEPA.|[Procédure : créer des écritures de collection prélèvement automatique SEPA et les exporter vers un fichier bancaire](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Paramétrez des codes vente client standard pour les factures de prélèvement automatique et générez des factures vente avec les informations de prélèvement automatique lorsque les factures sont échues.|[Procédure : Créer des lignes ventes et achat récurrentes](sales-how-work-standard-lines.md)|  
|Valider les paiements effectués comme prélèvements automatiques SEPA.|[Procédure : valider des réceptions règlement de prélèvement SEPA](finance-how-to-post-sepa-direct-debit-payment-receipts.md)|  

## <a name="see-also"></a>Voir aussi  
[Gestion des comptes client](receivables-manage-receivables.md)

