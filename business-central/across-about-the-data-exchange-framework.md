---
title: À propos de l’infrastructure d’échange de données
description: Cet article explique comment utiliser l’infrastructure d’échange de données pour gérer l’échange de données dans des documents commerciaux tels que des factures avec vos partenaires commerciaux.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Data exchange framework, data files, data exchange, electronic document, invoice, Business Central, business document, standard-compliant file, OCR'
ms.search.form: '189,'
ms.date: 12/13/2023
ms.author: bholtorf
---
# À propos de l’infrastructure d’échange de données

Vous pouvez utiliser l’infrastructure d’échange de données pour gérer les échanges des documents commerciaux, des fichiers bancaires, des taux de change devise et tous les autres fichiers de données avec vos partenaires commerciaux ou les autorités.

En tant qu’administrateur ou partenaire Microsoft, vous pouvez utiliser l’infrastructure dans de nouvelles fonctionnalités d’intégration en configurant les données à échanger et comment les échanger. Par exemple, le format des fichiers utilisés pour l’échange de données bancaires, les documents électroniques, les taux de change de devises, et d’autres fichiers utilisés avec les systèmes ERP varient selon le fournisseur du fichier de données ou du flux, et selon le pays ou la région. [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge différents formats de fichiers bancaires et différentes normes de service de données. Pour assurer la prise en charge d’autres formats de documents électroniques, vous pouvez utiliser l’infrastructure d’échange de données.

 Les schémas suivantes indiquent l’architecture de l’infrastructure d’échange de données.  

 ![Infrastructure d’échange de données &#45; Importation.](media/across-data-exchange/dataexchangeframework_import.png)  

 ![Infrastructure d’échange de données &#45; Exportation.](media/across-data-exchange/dataexchangeframework_export.png)  

## Documents électroniques

Comme alternative à l’envoi par courrier électronique de documents métier sous forme de fichiers joints, vous pouvez les envoyer et les recevoir par voie électronique. Par « document électronique », on entend un fichier conforme aux normes représentant un document métier, comme une facture fournisseur que vous pouvez recevoir et convertir en facture achat dans [!INCLUDE[prod_short](includes/prod_short.md)]. Les partenaires commerciaux échangent des documents électroniques via des services externes d’échange de documents. Par défaut, [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge l’envoi et la réception de factures et d’avoirs électroniques au format PEPPOL, qui est pris en charge par les principaux fournisseurs de services d’échange de documents. Un grand fournisseur de services d’échange de documents, Tradeshift, est préconfiguré et prêt à être installé pour votre société. Pour prendre en charge d’autres formats de document électronique, vous devez créer de nouvelles définitions d’échange de données.  

À partir de fichiers PDF ou image représentant des documents entrants, un service OCR externe (reconnaissance optique de caractères) peut créer des documents électroniques pouvant être convertis en enregistrements de document dans [!INCLUDE[prod_short](includes/prod_short.md)], comme pour les documents électroniques PEPPOL. Par exemple, lorsque vous recevez une facture au format PDF de votre fournisseur, vous pouvez l’envoyer au service OCR à partir de la page **Documents entrants**. Après quelques secondes, vous recevrez le fichier sous forme de facture électronique pouvant être convertie en facture achat pour le fournisseur. Si vous envoyez le fichier au service OCR par courrier électronique, un enregistrement de document entrant est automatiquement créé lorsque vous recevez le document électronique.  

Pour envoyer, par exemple, une facture vente en tant que document PEPPOL électronique, sélectionnez l’option **Document électronique** dans la boîte de dialogue **Valider et envoyer**. Dans cette fenêtre, vous pouvez également définir le profil d’envoi de document par défaut du client. Au préalable, vous devez configurer différentes données de base, telles que les informations sur la société, les clients, les articles, et les unités de mesure. Celles-ci sont utilisées pour identifier les partenaires commerciaux et les articles lorsque vous convertissez les données des champs dans [!INCLUDE[prod_short](includes/prod_short.md)] en éléments dans le fichier document sortant. La conversion des données et l’envoi de la facture vente PEPPOL sont effectuées par des codeunits dédiés et des XMLports, représentés par le format de document électronique **PEPPOL**.  

Pour recevoir, par exemple, une facture d’un fournisseur en tant que document électronique PEPPOL, traitez le document sur la page **Documents entrants** pour le convertir en facture achat dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous pouvez configurer la fonctionnalité File projets pour le traitement régulier de ces fichiers ou vous pouvez lancer le processus manuellement. Au préalable, vous devez configurer différentes données de base, telles que les informations sur la société, les fournisseurs, les articles, et les unités de mesure. Celles-ci sont utilisées pour identifier les partenaires commerciaux et les articles lorsque vous convertissez les données des éléments du fichier document entrant dans les champs de [!INCLUDE[prod_short](includes/prod_short.md)]. La réception et la conversion des données de factures PEPPOL sont exécutées par l’infrastructure d’échange de données, représentée par la définition d’échange de données **PEPPOL - Facture**.  

  Pour recevoir, par exemple, une facture en tant que document ROC électronique, vous la traitez comme lorsque vous recevez un document PEPPOL électronique. La réception et la conversion de documents électroniques à partir du service ROC sont exécutées par l’infrastructure d’échange de données, représentée par la définition d’échange de données **ROC - Facture**.  

## Fichiers bancaires

Les formats de fichiers d’échange de données bancaire avec des applications de gestion d’entreprise varient selon le fournisseur du fichier et du pays ou de la région. [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge l’importation et l’exportation de fichiers bancaires de l’espace SEPA (Single Euro Payments Area). De plus, l’extension AMC Banking 365 Fundamentals vous permet de vous connecter à une extension AMC Banking 365 Fundamentals fournie par un fournisseur externe, AMC Consult. Pour plus d’informations, voir [Exécution de paiements avec l’extension AMC Banking 365 Fundamentals ou un virement SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md). Pour assurer la prise en charge d’autres formats de documents électroniques, vous pouvez utiliser l’infrastructure d’échange de données.  

Pour exporter des virements SEPA, choisissez le bouton **Exporter les paiements dans un fichier** sur la page **Feuille paiement**, puis téléchargez le fichier pour traiter les règlements à votre banque. Tout d’abord, vous devez configurer les différentes données de base, telles que le compte bancaire, les fournisseurs, et les modes de règlement. La conversion des données et l’exportation des données bancaires SEPA sont exécutées par un codeunit et un XMLport dédiés, représentés par la configuration importer/exporter de la banque **Virement SEPA**. Vous pouvez aussi définir l’extension AMC Banking 365 Fundamentals pour exécuter l’exportation, représentée par la définition d’échange de données de l’extension **AMC Banking 365 Fundamentals - Virement**.  

 Pour exporter des instructions de prélèvements automatiques SEPA, choisissez le bouton **Exporter fichier prélèvement** sur la page **Recouvrements prélèvement**, puis envoyez à votre banque pour collecter automatiquement les règlements client associés. Vous devez d’abord configurer les comptes bancaires, les clients, les mandats de prélèvements automatique, ainsi que les modes de règlement. La conversion des données et l’exportation des données bancaires SEPA sont exécutées par un codeunit et un XMLport dédiés, représentés par la configuration importer/exporter de la banque **Virement automatique SEPA**.  

 Pour importer des relevés bancaires SEPA, choisissez le bouton Importer relevé bancaire sur les pages **Feuille rapprochement bancaire** et **Rapprochement bancaire**, puis appliquez chaque écriture de relevé bancaire aux paiements ou écritures comptables bancaires, manuellement ou automatiquement. Vous devez d’abord configurer des comptes bancaires. L’importation et la conversion des données bancaires SEPA sont exécutées par l’infrastructure d’échange de données, représentée par la définition d’échange de données **SEPA CAMT**. Vous pouvez aussi définir l’extension AMC Banking 365 Fundamentals pour exécuter l’importation, représentée par la définition d’échange de données de l’extension **AMC Banking 365 Fundamentals - Relevé bancaire**.  

 En outre, les versions locales de [!INCLUDE[prod_short](includes/prod_short.md)] prennent en charge plusieurs autres formats de fichier pour importer/exporter des données bancaires, transactions de paie et autres données. Pour plus d’informations, consultez la page d’arrivée [Fonctionnalités locales](about-localization.md) pour votre pays/région dans l’aide.  

## Taux de change devise

vous pouvez configurer un service externe pour tenir vos taux de change des devises à jour. Le service qui fournit des taux de change des devises mis à jour est activé par une définition d’échange de données. Par conséquent, la page **Fiche Paramètres de mise à jour des taux de change** est une vue condensée de la page **Définition d’échange de données** de la définition d’échange de données en question.  

Pour tous les échanges de données dans les fichiers XML, vous pouvez préparer la configuration d’échange de données en chargeant le fichier schéma XML associé sur la page **Visionneuse de schéma XML**. Il s’agit de l’emplacement où vous pouvez sélectionner les éléments de données que vous souhaitez échanger avec [!INCLUDE[prod_short](includes/prod_short.md)], puis initialiser une définition d’échange de données ou générer un XMLport.

## Déclaration d’échanges de biens

[!INCLUDE[prod_short](includes/prod_short.md)] utilise la structure d’échange de données pour les rapports Échanges intracommunautaires où vous pouvez facilement créer des fichiers horodatés dans différents formats pour l’exportation. [!INCLUDE[prod_short](includes/prod_short.md)] contient des formats préparés pour les pays/régions localisés et pour la version par défaut. Mais vous pouvez modifier le rapport prêt à l’emploi ou créer le vôtre.

## Voir aussi

[Échanger des données par voir électronique](across-data-exchange.md)  
[Utilisation des schémas XML pour préparer des définitions d’échange de données](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Configuration de l’échange de données](across-set-up-data-exchange.md)  
[Documents entrants](across-income-documents.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
