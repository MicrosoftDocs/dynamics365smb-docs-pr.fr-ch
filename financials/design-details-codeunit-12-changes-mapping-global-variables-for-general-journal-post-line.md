---
title: "Détails de conception - Codeunit 12 Modifications des variables globales de mappage pour la ligne de validation de feuille comptabilité | Microsoft Docs"
description: "Les modifications suivantes ont été mis en œuvre dans cette version de Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d1199adb2912d88c545cabcc84d5c9bf27b0892a
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="codeunit-12-changes-mapping-global-variables-for-general-journal-post-line"></a>Codeunit 12 modifications : variables globales de mappage pour la ligne de validation de feuille comptabilité
Les modifications suivantes ont été mises en œuvre dans cette version de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Commentaires**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Enregistrement 98 ;|GLSetup@1009 : Enregistrement 98 ;|Inchangé|  
|SalesSetup@1010 : Enregistrement 311 ;||Passé à devises locales|  
|PurchSetup@1011 : Enregistrement 312 ;||Passé à devises locales|  
|AccountingPeriod@1012 : Enregistrement 50 ;||Passé à devises locales|  
|GLAcc@1013 : Enregistrement 15 ;||Passé à devises locales|  
|GLEntry@1014 : Enregistrement 17 ;|GlobalGLEntry@1014 : Enregistrement 17 ;|Renommée|  
|GLEntryTmp@1015 : Enregistrement PROVISOIRE 17 ;|TempGLEntryBuf@1010 : Enregistrement PROVISOIRE 17 ;|Renommée|  
|TempGLEntryVAT@1016 : Enregistrement PROVISOIRE 17 ;|TempGLEntryVAT@1016 : Enregistrement PROVISOIRE 17 ;|Inchangé|  
|OrigGLEntry@1017 : Enregistrement 17 ;||Supprimé|  
|VATPostingSetup@1019 : Enregistrement 325 ;||Passé à devises locales|  
|Cust@1020 : Enregistrement 18 ;||Passé à devises locales|  
|Vend@1021 : Enregistrement 23 ;||Passé à devises locales|  
|GenJnlLine@1022 : Enregistrement 81 ;||Passé à devises locales|  
|GLReg@1029 : Enregistrement 45 ;|GLReg@1029 : Enregistrement 45 ;|Inchangé|  
|CustPostingGr@1030 : Enregistrement 92 ;||Passé à devises locales|  
|VendPostingGr@1031 : Enregistrement 93 ;||Passé à devises locales|  
|Currency@1032 : Enregistrement 4 ;||Passé à devises locales|  
|AddCurrency@1033 : Enregistrement 4 ;|AddCurrency@1033 : Enregistrement 4 ;|Inchangé|  
|ApplnCurrency@1034 : Enregistrement 4 ;||Passé à devises locales|  
|CurrExchRate@1035 : Enregistrement 330 ;|CurrExchRate@1035 : Enregistrement 330 ;|Inchangé|  
|VATEntry@1038 : Enregistrement 254 ;|VATEntry@1038 : Enregistrement 254 ;|Inchangé|  
|BankAcc@1039 : Enregistrement 270 ;||Passé à devises locales|  
|BankAccLedgEntry@1040 : Enregistrement 271 ;||Passé à devises locales|  
|CheckLedgEntry@1041 : Enregistrement 272 ;||Passé à devises locales|  
|CheckLedgEntry2@1042 : Enregistrement 272 ;||Passé à devises locales|  
|BankAccPostingGr@1043 : Enregistrement 277 ;||Passé à devises locales|  
|GenJnlTemplate@1044 : Enregistrement 80 ;||Passé à devises locales|  
|TaxJurisdiction@1045 : Enregistrement 320 ;||Passé à devises locales|  
|TaxDetail@1046 : Enregistrement 322 ;|TaxDetail@1046 : Enregistrement 322 ;|Inchangé|  
|FAGLPostBuf@1047 : Enregistrement PROVISOIRE 5637 ;||Passé à devises locales|  
|UnrealizedCustLedgEntry@1084 : Enregistrement 21 ;|UnrealizedCustLedgEntry@1084 : Enregistrement 21 ;|Inchangé|  
|UnrealizedVendLedgEntry@1085 : Enregistrement 25 ;|UnrealizedVendLedgEntry@1085 : Enregistrement 25 ;|Inchangé|  
|GLEntryVATEntryLink@1087 : Enregistrement 253 ;|GLEntryVATEntryLink@1087 : Enregistrement 253 ;|Inchangé|  
|TempVATEntry@1088 : Enregistrement PROVISOIRE 254 ;|TempVATEntry@1088 : Enregistrement PROVISOIRE 254 ;|Inchangé|  
|ReversedGLEntryTemp@1089 : Enregistrement PROVISOIRE 17 ;||Déplacé dans Codeunit17|  
|CostAccSetup@1092 : Enregistrement 1108 ;||Passé à devises locales|  
|GenJnlCheckLine@1048 : Codeunit 11 ;|GenJnlCheckLine@1001 : Codeunit 11 ;|Inchangé|  
|ExchAccGLJnlLine@1049 : Codeunit 366 ;||Passé à devises locales|  
|FAJnlPostLine@1050 : Codeunit 5632 ;||Passé à devises locales|  
|SalesTaxCalculate@1051 : Codeunit 398 ;||Passé à devises locales|  
|GenJnlApply@1052 : Codeunit 225 ;||Passé à devises locales|  
|DimMgt@1053 : Codeunit 408 ;||Passé à devises locales|  
|JobPostLine@1028 : Codeunit 1001 ;||Passé à devises locales|  
|TransferGlEntriesToCA@1091 : Codeunit 1105 ;||Passé à devises locales|  
||PaymentToleranceMgt@1002 : Codeunit 426 ;|Ajouté|  
||AddCurrencyCode@1117 : Code[10];|Ajouté|  
|FiscalYearStartDate@1054 : Date ;|FiscalYearStartDate@1011 : Date ;|Inchangé|  
|NextEntryNo@1055 : Entier ;|NextEntryNo@1022 : Entier ;|Inchangé|  
|BalanceCheckAmount@1056 : Décimal ;|BalanceCheckAmount@1056 : Décimal ;|Inchangé|  
|BalanceCheckAmount2@1057 : Décimal ;|BalanceCheckAmount2@1057 : Décimal ;|Inchangé|  
|BalanceCheckAddCurrAmount@1058 : Décimal ;|BalanceCheckAddCurrAmount@1058 : Décimal ;|Inchangé|  
|BalanceCheckAddCurrAmount2@1059 : Décimal ;|BalanceCheckAddCurrAmount2@1059 : Décimal ;|Inchangé|  
|CurrentBalance@1060 : Décimal ;|CurrentBalance@1060 : Décimal ;|Inchangé|  
|SalesTaxBaseAmount@1061 : Décimal ;||Passé à devises locales|  
|TotalAddCurrAmount@1062 : Décimal ;|TotalAddCurrAmount@1062 : Décimal ;|Inchangé|  
|TotalAmount@1063 : Décimal ;|TotalAmount@1063 : Décimal ;|Inchangé|  
|UnrealizedRemainingAmountCust@1086 : Décimal ;|UnrealizedRemainingAmountCust@1086 : Décimal ;|Inchangé|  
|UnrealizedRemainingAmountVend@1074 : Décimal ;|UnrealizedRemainingAmountVend@1074 : Décimal ;|Inchangé|  
|NextVATEntryNo@1064 : Entier ;|NextVATEntryNo@1064 : Entier ;|Inchangé|  
|FirstNewVATEntryNo@1065 : Entier ;|FirstNewVATEntryNo@1065 : Entier ;|Inchangé|  
|NextTransactionNo@1066 : Entier ;|NextTransactionNo@1066 : Entier ;|Inchangé|  
|NextConnectionNo@1067 : Entier ;|NextConnectionNo@1067 : Entier ;|Inchangé|  
|InsertedTempGLEntryVAT@1068 : Entier ;|InsertedTempGLEntryVAT@1027 : Entier ;|Inchangé|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Inchangé|  
|LastLineNo@1070 : Entier ;||Supprimé|  
|LastDate@1071 : Date ;|LastDate@1021 : Date ;|Inchangé|  
|LastDocType@1072 : ' ,Paiement,Facture,Avoir,Intérêts,Relance' ;|LastDocType@1025 : ' ,Paiement,Facture,Avoir,Intérêts,Relance' ;|Inchangé|  
|NextCheckEntryNo@1073 : Entier ;|NextCheckEntryNo@1028 : Entier ;|Inchangé|  
|AddCurrGLEntryVATAmt@1075 : Décimal ;|AddCurrGLEntryVATAmt@1017 : Décimal ;|Inchangé|  
|CurrencyDate@1076 : Date ;|CurrencyDate@1020 : Date ;|Inchangé|  
|CurrencyFactor@1077 : Décimal ;|CurrencyFactor@1019 : Décimal ;|Inchangé|  
|UseCurrFactorOnly@1078 : Booléen ;|UseCurrFactorOnly@1078 : Booléen ;|Inchangé|  
|NonAddCurrCodeOccured@1079 : Booléen ;|NonAddCurrCodeOccured@1079 : Booléen ;|Inchangé|  
|FADimAlreadyChecked@1080 : Booléen ;|FADimAlreadyChecked@1080 : Booléen ;|Inchangé|  
|AllApplied@1081 : Booléen ;||Passé à devises locales|  
|OverrideDimErr@1018 : Booléen ;|OverrideDimErr@1018 : Booléen ;|Inchangé|  
|JobLine@1036 : Booléen ;|JobLine@1036 : Booléen ;|Inchangé|  
|Prepayment@1037 : Booléen ;||Supprimé|  
|CheckUnrealizedCust@1082 : Booléen ;|CheckUnrealizedCust@1082 : Booléen ;|Inchangé|  
|CheckUnrealizedVend@1083 : Booléen ;|CheckUnrealizedVend@1083 : Booléen ;|Inchangé|  
|GLEntryNo@1090 : Entier ;|GLEntryNo@1026 : Entier ;|Inchangé|  
||GLSetupRead@1015 : Booléen ;|Ajouté|  
||AmountRoundingPrecision@1012 : Décimal ;|Ajouté|  
||CrCardTransactionEntryNo@1013 : Entier ;|Ajouté|  

## <a name="see-also"></a>Voir aussi  
 [Détails de conception : modifications du codeunit 12 : modifications des procédures de validation de feuille comptabilité](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)

