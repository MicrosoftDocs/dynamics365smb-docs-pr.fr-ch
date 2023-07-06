---
title: Mappage de champ pour exporter des fichiers de paiement bancaire | Microsoft Docs
description: 'Lorsque vous exportez des fichiers de paiement à l’aide de l’extension AMC Banking 365 Fundamentals, les données que vous exportez sont exposées au fournisseur de service.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="field-mapping-when-exporting-payment-files-using-the-amc-banking-365-fundamentals-extension"></a><a name="field-mapping-when-exporting-payment-files-using-the-amc-banking-365-fundamentals-extension"></a><a name="field-mapping-when-exporting-payment-files-using-the-amc-banking-365-fundamentals-extension"></a>Mappage de champ lors de l’exportation de fichiers de paiement à l’aide de l’extension AMC Banking 365 Fundamentals
Lorsque vous exportez des fichiers de paiement à l’aide de l’extension AMC Banking 365 Fundamentals, les données que vous exportez sont exposées au fournisseur de service. Le fournisseur de service est responsable de la confidentialité de ces données. Pour plus d’informations sur l’extension AMC Banking 365 Fundamentals, voir [Utiliser l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

> [!CAUTION]  
>  Lorsque vous exportez des fichiers de paiement à l’aide de l’extension AMC Banking 365 Fundamentals, certaines de vos données métier sont exposées au fournisseur du service. Le fournisseur de service, AMC Consult A/S, est responsable de la confidentialité de ces données. Pour plus d’informations, reportez\-vous à [Politique de confidentialité AMC](https://go.microsoft.com/fwlink/?LinkId=510158).  

> [!NOTE]
> Dans la version générique de [!INCLUDE[prod_short](includes/prod_short.md)], un fournisseur global de services pour convertir les données bancaires dans n’importe quel format de fichier que votre banque requiert est paramétré et connecté. Dans les versions nord-américaines, le même service peut être utilisé pour envoyer des fichiers de paiement sous forme de transfert de fonds électronique (EFT), par exemple le réseau ACH (Automated Clearing House), mais avec un processus légèrement différent.

Le tableau suivant répertorie les champs de [!INCLUDE[prod_short](includes/prod_short.md)] à partir desquels vous pouvez exporter des données.  

|Champ associé|Champ dans Tableau|Table|Description|  
|------------------|--------------------|-----------|---------------------------------------|  
|N° créditeur|N° créditeur|Compte bancaire|L’identifiant affecté à votre société par votre banque pour encaisser les paiements|  
|N° cpte bancaire émetteur|N° compte bancaire/IBAN|Compte bancaire|Le numéro du compte bancaire de votre société (IBAN ou autre) qui est spécifié sur la fiche compte bancaire|  
|Standard compensation bancaire émetteur|Standard compensation bancaire|Compte bancaire|Le registre national des noms de banque utilisé pour le compte bancaire de l’émetteur|  
|Code compensation bancaire émetteur|Code compensation bancaire|Compte bancaire|L’identifiant de la banque de l’émetteur en rapport avec le registre des noms de banque utilisé|  
|BIC banque émetteur|Code BIC|Compte bancaire|L’identificateur BIC du compte bancaire de l’émetteur|  
|Devise compte bancaire émetteur|Code devise|Compte bancaire|Le code devise du compte bancaire émetteur|  
|Numéro de document|Numéro de document|Ligne feuille comptabilité|Le numéro de document de la ligne paiement|  
|N° ligne doc. ext. lettrage|N° ligne doc. ext. lettrage|Ligne feuille comptabilité|Le numéro de document externe de la facture ou de l’avoir sur lequel la ligne paiement est appliquée|  
|ID destinataire|Le n° de compte.|Ligne feuille comptabilité|Le numéro de client ou fournisseur qui est spécifié sur la ligne paiement.|  
|Type de règlement|Type paiem. conversion données bancaires|Mode de règlement|Le type de virement bancaire, à savoir national ou international|  
|Référence paiement|Référence paiement|Ligne feuille comptabilité|La référence de paiement de la ligne paiement|  
|Adresse destinataire|Adresse|Client/Fournisseur|L’adresse du bénéficiaire qui est spécifiée sur la fiche client ou fournisseur|  
|Ville destinataire|Ville|Client/Fournisseur|La ville du bénéficiaire qui est spécifiée sur la fiche client ou fournisseur|  
|Nom destinataire|Nom|Client/Fournisseur|Le nom du bénéficiaire qui est spécifié sur la fiche client ou fournisseur|  
|Code pays/région destinataire|Code pays/région|Client/Fournisseur|Le code pays/région du bénéficiaire qui est spécifié sur la fiche client ou fournisseur|  
|Code postal destinataire|Code postal|Client/Fournisseur|Le code postal du bénéficiaire qui est spécifié sur la fiche client ou fournisseur|  
|N° cpte bancaire destinataire|N° compte bancaire/IBAN|Comte bancaire du client/Compte bancaire du fournisseur|Le numéro du compte bancaire du bénéficiaire (IBAN ou autre) qui est spécifié sur la fiche du compte bancaire du client ou du fournisseur|  
|Code compensation bancaire destinataire|Standard compensation bancaire|Comte bancaire du client/Compte bancaire du fournisseur|Le registre national des noms de banque utilisé pour le compte bancaire du bénéficiaire|  
|Std compensation bancaire destinataire|Code compensation bancaire|Comte bancaire du client/Compte bancaire du fournisseur|L’identifiant du compte bancaire bénéficiaire en rapport avec le registre des noms de banque qui est utilisé|  
|Adresse messagerie destinataire|E-Mail|Client/Fournisseur|Adresse électronique du destinataire|  
|Message au destinataire 1|Message au destinataire|Ligne feuille comptabilité|Le message au destinataire qui est spécifié sur la ligne règlement|  
|Montant|Montant|Ligne feuille comptabilité|Le montant sur la ligne de paiement|  
|Code devise|Code devise|Ligne feuille comptabilité|Le code devise sur la ligne paiement.|  
|Date transfert|Date comptabilisation|Ligne feuille comptabilité|La date comptabilisation de la ligne paiement.|  
|Montant facture|Montant initial|Écriture comptable client/fournisseur|Le montant sur l’écriture à laquelle le paiement est appliqué|  
|Date facture|Date document|Écriture comptable client/fournisseur|La date de facture sur l’écriture à laquelle le paiement est appliqué|  
|Adresse banque destinataire|Adresse|Comte bancaire du client/Compte bancaire du fournisseur|L’adresse du compte bancaire du bénéficiaire qui est spécifiée sur la fiche du compte bancaire du client ou du fournisseur|  
|L’adresse du compte bancaire du bénéficiaire qui est spécifiée sur la fiche du compte bancaire du client ou du fournisseur|Ville|Comte bancaire du client/Compte bancaire du fournisseur|La ville du compte bancaire du bénéficiaire qui est spécifiée sur la fiche du compte bancaire du client ou du fournisseur|  
|Nom banque destinataire|Nom|Comte bancaire du client/Compte bancaire du fournisseur|Le nom du compte bancaire du bénéficiaire qui est spécifié sur la fiche du compte bancaire du client ou du fournisseur|  
|Pays/région banque destinataire|Code pays/région|Comte bancaire du client/Compte bancaire du fournisseur|Le pays/la région du compte bancaire du bénéficiaire qui est spécifié sur la fiche du compte bancaire du client ou du fournisseur|  
|Code postal banque destinataire|Code postal|Comte bancaire du client/Compte bancaire du fournisseur|Le code postal du compte bancaire du bénéficiaire qui est spécifié sur la fiche du compte bancaire du client ou du fournisseur|  
|Adresse banque émetteur|Adresse|Compte bancaire|L’adresse du compte bancaire de l’émetteur qui est spécifiée sur la fiche compte bancaire|  
|Ville banque émetteur|Ville|Compte bancaire|La ville du compte bancaire de l’émetteur qui est spécifiée sur la fiche compte bancaire|  
|Nom banque émetteur|Nom|Compte bancaire|Le nom du compte bancaire de l’émetteur qui est spécifié sur la fiche compte bancaire|  
|Pays/région banque émetteur|Code pays/région|Compte bancaire|Le pays/la région du compte bancaire de l’émetteur qui est spécifié sur la fiche compte bancaire|  
|Code postal banque émetteur|Code postal|Compte bancaire|Le code postal du compte bancaire de l’émetteur qui est spécifié sur la fiche compte bancaire|  
|Modèle feuille comptabilité|Nom modèle feuille|Ligne feuille comptabilité|Le modèle de la feuille comptabilité qui est utilisé pour la ligne paiement|  
|Nom feuille comptabilité|Nom feuille|Ligne feuille comptabilité|Le nom du lot feuille comptabilité qui est utilisé pour la ligne paiement|  
|Nom banque émetteur - Conv. données|Nom banque – Conv. données|Compte bancaire|Nom du compte bancaire de l’émetteur qui est demandé par l’extension AMC Banking 365 Fundamentals et qui est spécifié sur la fiche compte bancaire|  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi
[Configuration de l’échange de données](across-set-up-data-exchange.md)  
[Échanger des données par voie électronique](across-data-exchange.md)
[Utiliser l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)   
[Réaliser des paiements avec l’extension AMC Banking 365 Fundamentals ou le virement SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
