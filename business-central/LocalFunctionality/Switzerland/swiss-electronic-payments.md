---
title: 'Paiements électroniques, Suisse'
description: Les améliorations suisses vous permettent d'envoyer des factures aux clients par voie électronique. Les factures sont présentées et payées directement à l'aide du logiciel bancaire en ligne du client.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 03/22/2022
ms.author: edupont
---
# <a name="swiss-electronic-payments"></a>Paiements électroniques, Suisse

[!INCLUDE[prod_short](../../includes/prod_short.md)] vous permet d'envoyer des factures aux clients par voie électronique. Les factures sont présentées et payées directement à l'aide du logiciel bancaire en ligne du client.  

## <a name="electronic-payment-methods"></a>Modes de paiement électronique

Vous pouvez effectuer des paiements électroniques en utilisant les modes suivants :  

- Einzahlungsschein mit Referenznummer (ESR)  
- Lastschrift Verfahren (LSV+)  
- Virements SEPA  

## <a name="esr"></a>ESR

ESR est un service de prélèvement électronique qui utilise des bordereaux de paiement pour prélever de l'argent. C'est le système de paiement électronique standard créé par la Poste suisse. Vous pouvez imprimer des bordereaux de paiement ESR en tant que pièces jointes à une facture, calculer des numéros de référence ESR et importer des fichiers ESR contenant des informations de paiement provenant de banques. Pour plus d'informations, voir [Paiements électroniques suisses avec le mode ESR](how-to-print-esr-invoices.md). Vous pouvez également effectuer des paiements ESR et ESR+ à l'aide de la version de la banque de ce mode de règlement, intitulé Bank-ESR (BESR).  

## <a name="lsv"></a>LSV+

LSV+ est un service de prélèvement utilisé pour traiter les paiements. Les sociétés peuvent lancer des paiements client directement de la banque du client à l'aide du prélèvement. Vous pouvez demander et encaisser des paiements clients en utilisant le prélèvement au format banque LSV+ ou au format PostFinance DebitDirect. Pour plus d'informations, voir [Paiements électroniques suisses avec le mode LSV+](swiss-electronic-payments-using-lsv-.md).  

## <a name="sepa-credit-transfers"></a>Virements SEPA

Pour exporter des paiements selon la norme SEPA, vous devez utiliser un compte bancaire. Sur ces comptes bancaires, le champ **Groupe compta. banque** doit spécifier le compte général pertinent. De cette façon, les écritures du grand livre associées seront cohérentes avec les écritures générées pour les modes de paiement suisses. Pour plus d'informations sur l'exportation des paiements SEPA, voir [Procédure : créer des écritures de collection prélèvement automatique SEPA et les exporter vers un fichier bancaire](../../finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file).  

### <a name="iban-and-qr-iban"></a><a name="iban-qr"></a>IBAN et QR-IBAN

En Suisse, les demandes de paiement basées sur les virements SEPA peuvent inclure un code IBAN normal pour le compte bancaire ou un code QR-IBAN. Pour plus d'informations, voir [Gestion des QR-factures](ui-extensions-qr-bill-management.md).  

Le type d'IBAN du compte bancaire du destinataire doit correspondre au type de référence du paiement sur l'écriture lorsque vous tentez de payez un fournisseur. Si la référence de paiement est une référence QR, [!INCLUDE [prod_short](../../includes/prod_short.md)] va vérifier que l'IBAN du compte bancaire fournisseur est un code QR-IBAN. Si la référence du paiement est une référence du créditeur, cet IBAN doit être un IBAN normal.  

> [!TIP]
> Si un fournisseur utilise régulièrement les deux types de comptes, créez plusieurs comptes bancaires fournisseur et utilisez-les en conséquence. Pour plus d'information, voir [Utilisation de plusieurs comptes bancaires comme émetteurs de QR-factures](ui-extensions-qr-bill-management.md#multiplebankaccounts).

## <a name="see-also"></a>Voir aussi

[Gestion des QR-factures dans la version suisse](ui-extensions-qr-bill-management.md)  
[Importer des numéros de compensation d'une banque suisse](how-to-import-swiss-bank-clearing-numbers.md)  
[Paiements électroniques à l'aide de ESR+, Suisse](swiss-electronic-payments-using-esr.md)  
[Imprimer des factures ESR](how-to-print-esr-invoices.md)  
[Paiements électroniques suisses avec LSV+](swiss-electronic-payments-using-lsv-.md)  
[Fonctionnalité locale, Suisse](switzerland-local-functionality.md)  
[Effectuer des paiements](../../payables-make-payments.md)
[Créer des écritures de collection prélèvement automatique SEPA et les exporter vers un fichier bancaire](../../finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
