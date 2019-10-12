---
title: Documents électroniques dans Business Central | Microsoft Docs
description: Présentation de l'envoi et de la réception de documents électroniques dans Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 209516aff6195901f06705d2a2fb27d7144c4a0a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300656"
---
# <a name="exchanging-data-electronically"></a>Échanger des données par voir électronique
Vous pouvez utiliser la structure d'échange de données pour échanger des documents commerciaux, des fichiers bancaires, des taux de change devise et tous autres fichiers de données avec vos partenaires commerciaux.

## <a name="electronic-documents"></a>Documents électroniques
Comme alternative à l'envoi par courrier électronique sous forme de fichiers joints, vous pouvez envoyer et recevoir des documents commerciaux par voie électronique. Par document électronique, on entend un fichier conforme aux normes représentant un document commercial comme une facture fournisseur que vous pouvez recevoir et convertir en facture achat dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. L'échange de documents électroniques entre deux partenaires commerciaux est exécuté par un fournisseur externe de services d'échange de documents. La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge l'envoi et la réception de factures et d'avoirs électroniques au format PEPPOL, qui est pris en charge par les principaux fournisseurs de services d'échange de documents. Un fournisseur principal de services d'échange de documents est préconfiguré et prêt à être installé pour votre société. Pour prendre en charge d'autres formats de document électronique, vous devez créer des définitions d'échange de données à l'aide de l'infrastructure d'échange de données.  

À partir de fichiers PDF ou image représentant des documents entrants, un service OCR externe (reconnaissance optique de caractères) peut créer des documents électroniques pouvant être convertis en enregistrements de document dans [!INCLUDE[d365fin](includes/d365fin_md.md)], comme pour les documents électroniques PEPPOL. Par exemple, lorsque vous recevez une facture au format PDF de votre fournisseur, vous pouvez l'envoyer au service OCR à partir de la page **Documents entrants**. Après quelques secondes, vous recevrez le fichier sous forme de facture électronique pouvant être convertie en facture achat pour le fournisseur. Si vous envoyez le fichier au service OCR par courrier électronique, un enregistrement de document entrant est automatiquement créé lorsque vous recevez le document électronique.  

Pour envoyer, par exemple, une facture vente en tant que document PEPPOL électronique, sélectionnez l'option **Document électronique** dans la boîte de dialogue **Valider et envoyer**. Dans cette fenêtre, vous pouvez également définir le profil d'envoi de document par défaut du client. Au préalable, vous devez configurer différentes données de base, telles que les informations sur la société, les clients, les articles, et les unités de mesure. Celles-ci sont utilisées pour identifier les partenaires commerciaux et les articles lorsque vous convertissez les données des champs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] en éléments dans le fichier document sortant. La conversion des données et l'envoi de la facture vente PEPPOL sont effectuées par des codeunits dédiés et des XMLports, représentés par le format de document électronique **PEPPOL**.  

Pour recevoir, par exemple, une facture d'un fournisseur en tant que document électronique PEPPOL, traitez le document sur la page **Documents entrants** pour le convertir en facture achat dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vous pouvez configurer la fonctionnalité File projets pour le traitement régulier de ces fichiers ou vous pouvez lancer le processus manuellement. Au préalable, vous devez configurer différentes données de base, telles que les informations sur la société, les fournisseurs, les articles, et les unités de mesure. Celles-ci sont utilisées pour identifier les partenaires commerciaux et les articles lorsque vous convertissez les données des éléments du fichier document entrant dans les champs de [!INCLUDE[d365fin](includes/d365fin_md.md)]. La réception et la conversion des données de factures PEPPOL sont exécutées par l'infrastructure d'échange de données, représentée par la définition d'échange de données **PEPPOL - Facture**.  

 Pour recevoir, par exemple, une facture en tant que document ROC électronique, vous la traitez comme lorsque vous recevez un document PEPPOL électronique. La réception et la conversion de documents électroniques à partir du service ROC sont exécutées par l'infrastructure d'échange de données, représentée par la définition d'échange de données **ROC - Facture**.  

## <a name="bank-files"></a>Fichiers bancaires  
 Les formats de fichiers d'échange de données bancaire avec des systèmes ERP varient selon le fournisseur du fichier et du pays/de la région. La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge l'importation et l'exportation de fichiers bancaires SEPA (espace unique de paiement en euros) et un service conversion données bancaires fourni par le fournisseur extérieur, AMC Consult. Pour assurer la prise en charge d'autres formats de documents électroniques, vous pouvez utiliser l'infrastructure d'échange de données.  

Pour exporter des virements SEPA, choisissez le bouton **Exporter les paiements dans un fichier** sur la page **Feuille paiement**, puis téléchargez le fichier pour traiter les règlements à votre banque. Tout d'abord, vous devez configurer les différentes données de base, telles que le compte bancaire, les fournisseurs, et les modes de règlement. La conversion des données et l'exportation des données bancaires SEPA sont exécutées par un codeunit et un XMLport dédiés, représentés par la configuration importer/exporter de la banque **Virement SEPA**. Vous pouvez aussi définir le Service conversion données bancaires pour exécuter l'exportation, représentée par la définition d'échange de données **Service conversion données bancaires**.  

Pour exporter des instructions de prélèvements automatiques SEPA, choisissez le bouton **Exporter fichier prélèvement** sur la page **Recouvrements prélèvement**, puis envoyez à votre banque pour collecter automatiquement les règlements client associés. Vous devez d'abord configurer les comptes bancaires, les clients, les mandats de prélèvements automatique, ainsi que les modes de règlement. La conversion des données et l'exportation des données bancaires SEPA sont exécutées par un codeunit et un XMLport dédiés, représentés par la configuration importer/exporter de la banque **Virement automatique SEPA**.  

Pour importer des relevés bancaires SEPA, choisissez le bouton Importer relevé bancaire sur les pages **Feuille rapprochement bancaire** et **Rapprochement bancaire**, puis appliquez chaque écriture de relevé bancaire aux paiements ou écritures comptables bancaires, manuellement ou automatiquement. Vous devez d'abord configurer des comptes bancaires. L'importation et la conversion des données bancaires SEPA sont exécutées par l'infrastructure d'échange de données, représentée par la définition d'échange de données **SEPA CAMT**. Vous pouvez aussi définir le Service conversion données bancaires pour exécuter l'importation, représentée par la définition d'échange de données **Service conversion données bancaires – Relevé bancaire**.  

 En outre, les versions locales de [!INCLUDE[d365fin](includes/d365fin_md.md)] prennent en charge plusieurs autres formats de fichier pour importer/exporter des données bancaires, transactions de paie et autres données. Pour plus d'informations, reportez-vous à la section d'aide « Fonctionnalités locales » dans la version spécifique à votre pays de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="currency-exchange-rates"></a>Taux de change devise  
vous pouvez configurer un service externe pour tenir vos taux de change des devises à jour. Le service qui fournit des taux de change des devises mis à jour est activé par une définition d'échange de données. Par conséquent, la page **Fiche Paramètres de mise à jour des taux de change** est une vue condensée de la page **Définition d'échange de données** de la définition d'échange de données en question.  

Pour tous les échanges de données dans les fichiers XML, vous pouvez préparer la configuration d'échange de données en chargeant le fichier schéma XML associé sur la page **Visionneuse de schéma XML**. Il s'agit de l'emplacement où vous pouvez sélectionner les éléments de données que vous souhaitez échanger avec [!INCLUDE[d365fin](includes/d365fin_md.md)], puis initialiser une définition d'échange de données ou générer un XMLport.  

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

|Pour|Voir|  
|--------|---------|  
|Apprendre la manière dont l'infrastructure d'échange de données fonctionne.|[À propos de l'infrastructure d'échange de données](across-about-the-data-exchange-framework.md)|  
|Préparez-vous à l'échange de données dans un fichier en réutilisant le fichier de schéma XML. Configurez des définitions d'échange de données. Configurez les données de base pour l'envoi d'un document électronique. Configurez plusieurs champs bancaires importer/exporter.|[Configuration de l'échange de données](across-set-up-data-exchange.md)|  
|Selon les paramètres d'échange de données, envoyez des factures PEPPOL, recevez des factures PEPPOL, importez des relevés bancaires, et exportez des fichiers de paiement bancaire.|[Échange de données](across-exchange-data.md)|  

## <a name="see-also"></a>Voir aussi  
[À propos de l'infrastructure d'échange de données](across-about-the-data-exchange-framework.md)  
[Utiliser des schémas XML pour préparer des définitions d'échange de données](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Configuration de l'échange de données](across-set-up-data-exchange.md)  
[Échange de données](across-exchange-data.md)  
[Documents entrants](across-income-documents.md)  
[Fonctionnalités marché](ui-across-business-areas.md)
