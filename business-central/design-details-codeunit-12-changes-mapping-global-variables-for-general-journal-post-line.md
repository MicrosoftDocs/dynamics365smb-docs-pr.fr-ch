---
title: Changements dans le mappage des variables globales pour la publication dans Codeunit 12
description: Dans les versions précédentes, codeunit 12 a été modifié pour aider à améliorer les performances de publication à partir du journal général. Découvrez les modifications apportées aux variables globales.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/28/2020
ms.author: edupont
ms.openlocfilehash: bb041e7be2a0c644d1c19e34b892bd9480123734
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390539"
---
# <a name="historical-changes-to-codeunit-12-mapping-global-variables-for-general-journal-post-line"></a>Historique des modifications du codeunit 12 : variables globales de mappage pour la ligne de validation de feuille comptabilité

Les modifications suivantes ont été mises en œuvre dans les versions de [!INCLUDE [navnow_md](includes/navnow_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Commentaires**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Record 98;|GLSetup@1009 : Record 98 ;|Inchangé|  
|SalesSetup@1010 : Record 311;||Passé à devises locales|  
|PurchSetup@1011 : Record 312;||Passé à devises locales|  
|AccountingPeriod@1012 : Record 50;||Passé à devises locales|  
|GLAcc@1013 : Record 15;||Passé à devises locales|  
|GLEntry@1014 : Record 17;|GlobalGLEntry@1014 : Record 17;|Renommée|  
|GLEntryTmp@1015 : TEMPORARY Record 17;|TempGLEntryBuf@1010 : TEMPORARY Record 17;|Renommée|  
|TempGLEntryVAT@1016 : TEMPORARY Record 17;|TempGLEntryVAT@1016 : TEMPORARY Record 17;|Inchangé|  
|OrigGLEntry@1017 : Record 17;||Supprimée|  
|VATPostingSetup@1019 : Record 325;||Passé à devises locales|  
|Cust@1020 : Record 18;||Passé à devises locales|  
|Vend@1021 : Record 23;||Passé à devises locales|  
|GenJnlLine@1022 : Record 81;||Passé à devises locales|  
|GLReg@1029 : Record 45;|GLReg@1029 : Record 45;|Inchangé|  
|CustPostingGr@1030 : Record 92;||Passé à devises locales|  
|VendPostingGr@1031 : Record 93;||Passé à devises locales|  
|Currency@1032 : Record 4;||Passé à devises locales|  
|AddCurrency@1033 : Record 4;|AddCurrency@1033 : Record 4;|Inchangé|  
|ApplnCurrency@1034 : Record 4;||Passé à devises locales|  
|CurrExchRate@1035 : Record 330;|CurrExchRate@1035 : Record 330;|Inchangé|  
|VATEntry@1038 : Record 254;|VATEntry@1038 : Record 254;|Inchangé|  
|BankAcc@1039 : Record 270;||Passé à devises locales|  
|BankAccLedgEntry@1040 : Record 271;||Passé à devises locales|  
|CheckLedgEntry@1041 : Record 272;||Passé à devises locales|  
|CheckLedgEntry2@1042 : Record 272;||Passé à devises locales|  
|BankAccPostingGr@1043 : Record 277;||Passé à devises locales|  
|GenJnlTemplate@1044 : Record 80;||Passé à devises locales|  
|TaxJurisdiction@1045 : Record 320;||Passé à devises locales|  
|TaxDetail@1046 : Record 322;|TaxDetail@1046 : Record 322;|Inchangé|  
|FAGLPostBuf@1047 : TEMPORARY Record 5637;||Passé à devises locales|  
|UnrealizedCustLedgEntry@1084 : Record 21;|UnrealizedCustLedgEntry@1084 : Record 21;|Inchangé|  
|UnrealizedVendLedgEntry@1085 : Record 25;|UnrealizedVendLedgEntry@1085 : Record 25;|Inchangé|  
|GLEntryVATEntryLink@1087 : Record 253;|GLEntryVATEntryLink@1087 : Record 253;|Inchangé|  
|TempVATEntry@1088 : TEMPORARY Record 254;|TempVATEntry@1088 : TEMPORARY Record 254;|Inchangé|  
|ReversedGLEntryTemp@1089 : TEMPORARY Record 17;||Déplacé dans Codeunit17|  
|CostAccSetup@1092 : Record 1108;||Passé à devises locales|  
|GenJnlCheckLine@1048 : Codeunit 11;|GenJnlCheckLine@1001 : Codeunit 11;|Inchangé|  
|ExchAccGLJnlLine@1049 : Codeunit 366;||Passé à devises locales|  
|FAJnlPostLine@1050 : Codeunit 5632;||Passé à devises locales|  
|SalesTaxCalculate@1051 : Codeunit 398;||Passé à devises locales|  
|GenJnlApply@1052 : Codeunit 225;||Passé à devises locales|  
|DimMgt@1053 : Codeunit 408;||Passé à devises locales|  
|JobPostLine@1028 : Codeunit 1001;||Passé à devises locales|  
|TransferGlEntriesToCA@1091 : Codeunit 1105;||Passé à devises locales|  
||PaymentToleranceMgt@1002 : Codeunit 426;|Ajouté|  
||AddCurrencyCode@1117 : Code[10];|Ajouté|  
|FiscalYearStartDate@1054 : Date;|FiscalYearStartDate@1011 : Date;|Inchangé|  
|NextEntryNo@1055 : Integer;|NextEntryNo@1022 : Integer;|Inchangé|  
|BalanceCheckAmount@1056 : Decimal;|BalanceCheckAmount@1056 : Decimal;|Inchangé|  
|BalanceCheckAmount2@1057 : Decimal;|BalanceCheckAmount2@1057 : Decimal;|Inchangé|  
|BalanceCheckAddCurrAmount@1058 : Decimal;|BalanceCheckAddCurrAmount@1058 : Decimal;|Inchangé|  
|BalanceCheckAddCurrAmount2@1059 : Decimal;|BalanceCheckAddCurrAmount2@1059 : Decimal;|Inchangé|  
|CurrentBalance@1060 : Decimal;|CurrentBalance@1060 : Decimal;|Inchangé|  
|SalesTaxBaseAmount@1061 : Decimal;||Passé à devises locales|  
|TotalAddCurrAmount@1062 : Decimal;|TotalAddCurrAmount@1062 : Decimal;|Inchangé|  
|TotalAmount@1063 : Decimal;|TotalAmount@1063 : Decimal;|Inchangé|  
|UnrealizedRemainingAmountCust@1086 : Decimal;|UnrealizedRemainingAmountCust@1086 : Decimal;|Inchangé|  
|UnrealizedRemainingAmountVend@1074 : Decimal;|UnrealizedRemainingAmountVend@1074 : Decimal;|Inchangé|  
|NextVATEntryNo@1064 : Integer;|NextVATEntryNo@1064 : Integer;|Inchangé|  
|FirstNewVATEntryNo@1065 : Integer;|FirstNewVATEntryNo@1065 : Integer;|Inchangé|  
|NextTransactionNo@1066 : Integer;|NextTransactionNo@1066 : Integer;|Inchangé|  
|NextConnectionNo@1067 : Integer;|NextConnectionNo@1067 : Integer;|Inchangé|  
|InsertedTempGLEntryVAT@1068 : Integer;|InsertedTempGLEntryVAT@1027 : Integer;|Inchangé|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Inchangé|  
|LastLineNo@1070 : Integer;||Supprimée|  
|LastDate@1071 : Date;|LastDate@1021 : Date;|Inchangé|  
|LastDocType@1072 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|LastDocType@1025 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|Inchangé|  
|NextCheckEntryNo@1073 : Integer;|NextCheckEntryNo@1028 : Integer;|Inchangé|  
|AddCurrGLEntryVATAmt@1075 : Decimal;|AddCurrGLEntryVATAmt@1017 : Decimal;|Inchangé|  
|CurrencyDate@1076 : Date;|CurrencyDate@1020 : Date;|Inchangé|  
|CurrencyFactor@1077 : Decimal;|CurrencyFactor@1019 : Decimal;|Inchangé|  
|UseCurrFactorOnly@1078 : Boolean;|UseCurrFactorOnly@1078 : Boolean;|Inchangé|  
|NonAddCurrCodeOccured@1079 : Boolean;|NonAddCurrCodeOccured@1079 : Boolean;|Inchangé|  
|FADimAlreadyChecked@1080 : Boolean;|FADimAlreadyChecked@1080 : Boolean;|Inchangé|  
|AllApplied@1081 : Boolean;||Passé à devises locales|  
|OverrideDimErr@1018 : Boolean;|OverrideDimErr@1018 : Boolean;|Inchangé|  
|JobLine@1036 : Boolean;|JobLine@1036 : Boolean;|Inchangé|  
|Prepayment@1037 : Boolean;||Supprimée|  
|CheckUnrealizedCust@1082 : Boolean;|CheckUnrealizedCust@1082 : Boolean;|Inchangé|  
|CheckUnrealizedVend@1083 : Boolean;|CheckUnrealizedVend@1083 : Boolean;|Inchangé|  
|GLEntryNo@1090 : Integer;|GLEntryNo@1026 : Integer;|Inchangé|  
||GLSetupRead@1015 : Boolean;|Ajouté|  
||AmountRoundingPrecision@1012 : Decimal;|Ajouté|  
||CrCardTransactionEntryNo@1013 : Integer;|Ajouté|  

## <a name="see-also"></a>Voir aussi  
 [Détails de conception : modifications du codeunit 12 : modifications des procédures de validation de feuille comptabilité](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]