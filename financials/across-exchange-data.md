---
title: "Échanger des données | Microsoft Docs"
description: "Vous pouvez échanger des données entre Finance and Operations, Business edition et des fichiers ou flux externes en relation avec des tâches courantes d'entreprise, comme l'envoi et la réception de documents électroniques et l'importation et l'exportation de fichiers bancaires."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5e9e0d0d7850d6f66a16bfe46363e57292d88fb6
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="exchanging-data"></a>Échange de données
Vous pouvez échanger des données entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et des fichiers ou flux externes en relation avec des tâches courantes d'entreprise, comme l'envoi et la réception de documents électroniques et l'importation et l'exportation de fichiers bancaires.  

Avant de pouvoir envoyer et recevoir des documents électroniques ou importer et exporter des fichiers bancaires, vous devez configurer l'infrastructure d'échange de données pour traiter les fichiers de données ou flux concernés. En outre, vous devez configurer des domaines associées. Ceux-ci incluent les données de base des clients à qui vous envoyez des factures électroniques et le service conversion données bancaires dans le cas où vous distribuez des conversions de fichiers bancaires à un fournisseur de service externe. Pour plus d'informations, voir [Configurer un échange de données](across-set-up-data-exchange.md).  

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|  
|Convertir les enregistrements de document vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)] en un format standardisé et envoyez\-les en tant que documents électroniques que vos clients peuvent recevoir dans leur système.|[Envoyer des documents électroniques](sales-how-to-send-electronic-documents.md)|  
|Envoyer des fichiers PDF ou image à un fournisseur de services ROC, et les recevoir en tant que documents électroniques pouvant être convertis en enregistrements de document dans [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques](across-how-use-ocr-pdf-images-files.md)|  
|Recevoir des documents électroniques, du service OCR ou du service d'échange de document, dans un format standardisé que vous convertissez en enregistrements de document appropriés dans [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Recevoir et convertir des documents électroniques](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Importer un fichier de relevé bancaire dans la fenêtre **Feuille rapprochement bancaire** comme première étape en rapprochement des paiements ou dans la fenêtre **Rapprochement bancaire** comme première étape de rapprochement des comptes bancaires.|[Configurer le service de flux de la Envestnet Yodlee Bank](bank-how-setup-bank-statement-service.md)|  
|Exporter des paiements à partir de la fenêtre **Feuille paiement** vers un fichier bancaire que vous transférez sur votre compte bancaire électronique pour traitement.|[Exporter des paiements vers un fichier bancaire](payables-how-export-payments-bank-file.md)|
|Effectuer des paiements électroniques conformément à la norme de virement SEPA de l'UE.|[Exécution de paiements avec le service de conversion de données bancaires ou un virement SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Demander à votre banque de transférer les montants de paiement des comptes bancaires de vos clients vers le compte de votre société en fonction de votre configuration du prélèvement automatique SEPA.|[Créer des écritures de collection prélèvement automatique SEPA et les exporter vers un fichier bancaire](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Utiliser un fournisseur de services de taux de change des devises pour mettre à jour la fenêtre **Devises**.|[Mettre à jour des taux de change devise](finance-how-update-currencies.md)|  
|Consulter les éléments de fichier mappés aux champs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] lors de l'importation de fichiers de déclaration SEPA CAMT.|[Mappage de champs lors de l'importation de fichiers SEPA CAMT](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Consulter les champs de [!INCLUDE[d365fin](includes/d365fin_md.md)] mappés à des éléments de fichier lorsque vous exportez des fichiers de paiement à l'aide de la fonction Service conversion données bancaires.|[Mappage de champs lors de l'exportation de fichiers de paiement à l'aide du service conversion données bancaires](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Voir aussi  
[Configuration de l'échange de données](across-set-up-data-exchange.md)  
[Échanger des données par voir électronique](across-data-exchange.md)  
[Facturer des ventes](sales-how-invoice-sales.md)   
[Enregistrer des achats](purchasing-how-record-purchases.md)  
[Documents entrants](across-income-documents.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  

