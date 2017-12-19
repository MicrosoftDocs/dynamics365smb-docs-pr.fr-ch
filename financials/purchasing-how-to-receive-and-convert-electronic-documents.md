---
title: "Recevoir et convertir des documents électroniques | Microsoft Docs"
description: "Vous pouvez recevoir des documents électroniques directement des partenaires commerciaux ou d'un service OCR."
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
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 8ae02f7a55f822751ae66b5b62013455aac87e48
ms.contentlocale: fr-ch
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-receive-and-convert-electronic-documents"></a>Procédure : recevoir et convertir des documents électroniques
La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge la réception de factures et d'avoirs électroniques au format PEPPOL, qui est pris en charge par les principaux fournisseurs de services d'échange de documents. Pour recevoir une facture d'un fournisseur en tant que document électronique PEPPOL, traitez le document dans la fenêtre Documents entrants pour le convertir en facture achat ou en ligne feuille comptabilité dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

 Outre la réception de documents électroniques directement des partenaires commerciaux, vous pouvez recevoir des documents électroniques d'un service OCR qui a converti vos fichiers PDF ou image en documents électroniques.  

 Avant de pouvoir recevoir des documents électroniques via le service d'échange de documents, vous devez configurer différentes données de base, telles que les informations sur la société, les fournisseurs, les articles et les unités de mesure. Celles-ci sont utilisées pour identifier les partenaires commerciaux et les articles lors de la conversion des données en fichier document entrant dans des champs dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, reportez vous à [Procédure : configurer un service d'échange de document](across-how-to-set-up-a-document-exchange-service.md).  

 Avant de pouvoir recevoir des documents électroniques via le service ROC, vous devez configurer et activer la connexion de service préconfigurée. Pour plus d'informations, reportez vous à [Procédure : configurer des documents entrants](across-how-setup-income-documents.md).  

 Le trafic des documents électroniques dans et hors de [!INCLUDE[d365fin](includes/d365fin_md.md)] est géré par la fonctionnalité File projets. Avant de pouvoir recevoir des documents électroniques, la file projets appropriée doit être démarrée.  

 Vous pouvez démarrer la conversion des documents électroniques manuellement, comme décrit dans cette procédure, ou vous pouvez activer un flux de travail pour convertir les documents électroniques automatiquement lorsque vous les recevez. La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] comprend un modèle de workflow, *Du document électronique entrant via le service OCR au workflow de factures achat ouvertes*, qui est prêt à être copié dans un workflow et activé. Pour plus d'informations, voir [Flux de travail](across-workflow.md).  

> [!NOTE]  
>  Lorsque vous convertissez des documents électroniques reçus du service ROC en documents ou lignes feuille dans [!INCLUDE[d365fin](includes/d365fin_md.md)], plusieurs lignes du document source seront résumées sur une ligne. La ligne unique sera de type Compte général et les champs **Description** et **N°** (compte général) seront vides. La valeur du champ **Montant** est égal au montant total hors TVA de toutes les lignes du document source.  
>   
>  Pour vous assurer que les champs **Description** et **N°** sont remplis, vous pouvez choisir le bouton **Mapper le texte avec le compte** dans la fenêtre **Documents entrants** pour définir qu'un texte de facture donné doit toujours être associé à un compte de débit ou crédit donné dans la comptabilité. Ultérieurement, le champ **Description** des lignes document ou feuille créées à partir d'un document électronique pour ce fournisseur ou client sera renseigné avec le texte spécifié et le champ **N°** (compte général) avec le compte en question.  
>   
>  Au lieu de créer un mappage à un compte général, vous pouvez également créer un mappage à un compte bancaire. Ceci est utile, par exemple, pour les documents électroniques des dépenses qui sont déjà payées lorsque vous souhaitez créer une ligne feuille comptabilité qui est prête à être validée sur un compte bancaire.  

 La procédure suivante décrit comment recevoir une facture fournisseur et la convertir en une facture achat dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. La procédure est la même lorsque vous convertissez une facture fournisseur en une ligne feuille comptabilité.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice"></a>Pour recevoir une facture électronique et la convertir en une facture achat  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Documents entrants**, puis sélectionnez le lien connexe.  

2.  Sélectionnez la ligne de l'enregistrement du document entrant qui représente une nouvelle facture électronique entrante, puis sous l'onglet **Accueil**, dans le groupe **Gérer**, sélectionnez **Modifier**.  

     Dans la fenêtre **Fiche document entrant**, le fichier XML est joint, et la plupart des champs sont préremplis avec les informations de la facture électronique. Pour plus d'informations, reportez vous à [Procédure : créer des enregistrements document entrant](across-how-create-income-document-records.md).  

3.  Dans le champ **Type échange de données**, sélectionnez **PEPPOL - Facture** ou **OCR - Facture** selon la source du document électronique.  

4.  Pour mapper le texte de la facture fournisseur à un compte débit spécifique, sous l'onglet **Actions**, dans le groupe **Général**, choisissez **Mapper le texte avec le compte**, puis renseignez la fenêtre **Feuille activité correspondance texte et compte**.  

5.  Sous l'onglet **Actions**, dans le groupe **Général**, sélectionnez **Créer un document**.  

     Une facture achat est créée dans [!INCLUDE[d365fin](includes/d365fin_md.md)] sur la base des informations du document électronique.  

     Les erreurs de validation, généralement associées à des données de base erronées ou manquantes dans [!INCLUDE[d365fin](includes/d365fin_md.md)], seront affichées dans le raccourci **Messages d'erreur**.  

## <a name="see-also"></a>Voir aussi  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Documents entrants](across-income-documents.md)  
[Procédure : Configurer l'envoi et la réception de documents électroniques](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Échanger des données par voir électronique](across-data-exchange.md)   
[Fonctionnalités marché](ui-across-business-areas.md)  

