---
title: Configurer l'échange de données | Microsoft Docs
description: Configurez l'infrastructure d'échange de données dans Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 759a6045440b7f15c7b87d3aff83c2447abd6ce2
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244760"
---
# <a name="setting-up-data-exchange"></a>Configuration de l'échange de données
Avant de pouvoir envoyer et recevoir des documents électroniques ou importer et exporter des fichiers bancaires, vous devez configurer l'infrastructure d'échange de données pour traiter les fichiers concernés. En outre, vous devez configurer des zones associées, telles que les données de base pour les clients à qui vous envoyez des factures électroniques ou le service conversion données bancaires si vous utilisez le fournisseur externe de services de conversion de vos fichiers bancaires. Pour plus d'informations, voir [Échanger des données par voir électronique](across-data-exchange.md).  

 Lorsque [!INCLUDE[d365fin](includes/d365fin_md.md)] est configuré pour échanger des données avec les fichiers externes, les utilisateurs peuvent utiliser les paramètres pour les tâches courantes de l'entreprise, comme l'envoi et la réception de documents électroniques et l'importation et l'exportation de fichiers bancaires.  

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|  
|Configurer le service préconfiguré d'échange de documents pour activer l'envoi et la réception de documents électroniques depuis et vers [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Configurer un service d'échange de document](across-how-to-set-up-a-document-exchange-service.md)|  
|Configurer le service OCR préconfiguré pour convertir des fichiers PDF ou image en documents électroniques pouvant être convertis en enregistrements de document dans [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Configurer des documents entrants](across-how-setup-income-documents.md)|  
|Configurer un des deux services préconfigurés pour les taux de change mis à jour pour insérer les taux de change de devise les plus récents sur la page **Devises**.|[Mettre à jour des taux de change devise](finance-how-update-currencies.md)|  
|Configurer différentes données de base, telles que les informations sur la société, les clients, les fournisseurs, les articles et les unités de mesure associés au mappage des données dans [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Configurer l'envoi et la réception de documents électroniques](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Configurer un compte bancaire, un fournisseur et une feuille paiement pour le virement SEPA.|[Configurer des virements SEPA](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Préparez les formats de compte bancaire, les modes de paiement et les accords clients pour le prélèvement automatique SEPA.|[Configurer un prélèvement SEPA](finance-how-to-set-up-sepa-direct-debit.md)|  
|Paramétrer l'authentification de l'utilisateur et l'URL du fournisseur de services de conversion de données bancaires qui est nécessaire pour que les fichiers bancaires soient convertis au format de votre banque.|[Configurer le service de conversion de données bancaires](bank-how-setup-bank-data-conversion-service.md)|  
|Configurer et activer un service externe qui vous permet d'importer des relevés bancaires, directement sous forme de flux bancaires.|[Configurer le service de relevés bancaires](bank-how-setup-bank-statement-service.md)|  
|Une fois le service de relevés bancaires activé, lier les comptes bancaires dans [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Configuration des comptes bancaires](bank-how-setup-bank-accounts.md)|  
|Préparer à configurer une nouvelle définition d'échange de données pour un fichier ou flux de données à l'aide du schéma XML du fichier pour préremplir le raccourci **Définitions de colonnes** de la page **Définitions échange comptabilité**.|[Utiliser des schémas XML pour préparer des définitions d'échange de données](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Configurer l'infrastructure d'échange de données pour permettre aux utilisateurs de recevoir un nouveau format de documents achat, d'envoyer un nouveau format de documents vente, d'importer un nouveau fichier bancaire, ou autre échange de données.|[Configurer les définitions d'échange de données](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Voir aussi  
[Échanger des données par voir électronique](across-data-exchange.md)  
[Échange de données](across-exchange-data.md)   
[Documents entrants](across-income-documents.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
