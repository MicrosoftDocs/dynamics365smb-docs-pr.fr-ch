---
title: Recevoir et convertir des documents électroniques
description: Cette rubrique décrit comment recevoir des documents électroniques directement des partenaires commerciaux ou d’un service OCR.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '189, 190, 191'
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="receive-and-convert-electronic-documents"></a>Réception et conversion des documents électroniques

> [!NOTE]
> Le contenu de cet article s’applique uniquement aux versions de Dynamics 365 Business Central sorties avant la 2e vague de lancement 2023. Dans la 2e vague de lancement 2023, une nouvelle fonctionnalité pour les documents électroniques est incluse. Pour en savoir plus, consultez [Configurer des documents électroniques](finance-how-setup-edocuments.md). 


La version générique de [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge la réception de factures et d’avoirs électroniques au format PEPPOL, qui est pris en charge par les principaux fournisseurs de services d’échange de documents. Pour recevoir une facture d’un fournisseur en tant que document électronique PEPPOL, traitez le document sur la page Documents entrants pour le convertir en facture achat ou en ligne feuille comptabilité dans [!INCLUDE[prod_short](includes/prod_short.md)].

Outre la réception de documents électroniques directement des partenaires commerciaux, vous pouvez recevoir des documents électroniques d’un service OCR qui a converti vos fichiers PDF ou image en documents électroniques.  

Avant de pouvoir recevoir des documents électroniques via le service d’échange de documents, vous devez configurer différentes données de base, telles que les informations sur la société, les fournisseurs, les articles et les unités de mesure. Celles-ci sont utilisées pour identifier les partenaires commerciaux et les articles lors de la conversion des données en fichier document entrant dans des champs dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, reportez vous à [Configurer un service d’échange de document](across-how-to-set-up-a-document-exchange-service.md).  

Avant de pouvoir recevoir des documents électroniques via le service ROC, vous devez configurer et activer la connexion de service préconfigurée. Pour plus d’informations, voir [Configurer des documents entrants](across-how-setup-income-documents.md).  

Le trafic des documents électroniques dans et hors de [!INCLUDE[prod_short](includes/prod_short.md)] est géré par la fonctionnalité File projets. Avant de pouvoir recevoir des documents électroniques, la file projets appropriée doit être démarrée.  

Vous pouvez démarrer la conversion des documents électroniques manuellement, comme décrit dans cette procédure, ou vous pouvez activer un flux de travail pour convertir les documents électroniques automatiquement lorsque vous les recevez. La version générique de [!INCLUDE[prod_short](includes/prod_short.md)] comprend un modèle de workflow, *Du document électronique entrant via le service OCR au workflow de factures achat ouvertes*, qui est prêt à être copié dans un workflow et activé. Pour plus d’informations, voir [Flux de travail](across-workflow.md).  

> [!NOTE]  
> Lorsque vous convertissez des documents électroniques reçus du service ROC en documents ou lignes feuille dans [!INCLUDE[prod_short](includes/prod_short.md)], plusieurs lignes du document source seront résumées sur une ligne. La ligne unique sera de type Compte général et les champs **Description** et **N°** (compte général) seront vides. La valeur du champ **Montant** est égal au montant total hors TVA de toutes les lignes du document source.  
>
> Pour vous assurer que les champs **Description** et **N°** sont remplis, vous pouvez choisir le bouton **Mapper le texte avec le compte** sur la page **Documents entrants** pour définir qu’un texte de facture donné doit toujours être associé à un compte de débit ou crédit donné dans la comptabilité. Ultérieurement, le champ **Description** des lignes document ou feuille créées à partir d’un document électronique pour ce fournisseur ou client sera renseigné avec le texte spécifié et le champ **N°** (compte général) avec le compte en question.  
>
> Au lieu de créer un mappage à un compte général, vous pouvez également créer un mappage à un compte bancaire. Ceci est utile, par exemple, pour les documents électroniques des dépenses qui sont déjà payées lorsque vous souhaitez créer une ligne feuille comptabilité qui est prête à être validée sur un compte bancaire.  

La procédure suivante décrit comment recevoir une facture fournisseur et la convertir en une facture achat dans [!INCLUDE[prod_short](includes/prod_short.md)]. La procédure est la même lorsque vous convertissez une facture fournisseur en une ligne feuille comptabilité.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice"></a>Pour recevoir une facture électronique et la convertir en une facture achat

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Documents entrants**, puis choisissez le lien associé.  

2. Sélectionnez la ligne de l’enregistrement du document entrant qui représente une nouvelle facture électronique entrante, puis sélectionnez l’action **Modifier**.  

    Sur la page **Fiche document entrant**, le fichier XML est joint, et la plupart des champs sont préremplis avec les informations de la facture électronique. Pour plus d’informations, voir [Créer des enregistrements document entrant](across-how-create-income-document-records.md).  

3. Dans le champ **Type échange de données**, sélectionnez **PEPPOL - Facture** ou **OCR - Facture** selon la source du document électronique.  

4. Pour mapper le texte de la facture fournisseur à un compte débit spécifique, sous l’onglet **Actions**, dans le groupe **Général**, choisissez **Mapper le texte avec le compte**, puis renseignez la page **Feuille activité correspondance texte et compte**.  

5. Choisissez l’action **Créer document**.  

    Une facture achat est créée dans [!INCLUDE[prod_short](includes/prod_short.md)] sur la base des informations du document électronique.  

    Les erreurs de validation, généralement associées à des données de base erronées ou manquantes dans [!INCLUDE[prod_short](includes/prod_short.md)], seront affichées dans le raccourci **Messages d’erreur**.  

## <a name="see-also"></a>Voir aussi

[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Documents entrants](across-income-documents.md)  
[Configurer l’envoi et la réception de documents électroniques](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Échanger des données par voir électronique](across-data-exchange.md)   
[Fonctionnalités marché](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
