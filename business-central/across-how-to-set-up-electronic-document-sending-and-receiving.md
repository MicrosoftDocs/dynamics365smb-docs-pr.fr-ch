---
title: Procédure de configuration de l’envoi et de la réception de documents électroniques | Microsoft Docs
description: 'Comme alternative à l’envoi par courrier électronique sous forme de fichiers joints, vous pouvez envoyer et recevoir des documents commerciaux par voie électronique.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# Configurer l’envoi et la réception de documents électroniques

Comme alternative à l’envoi par courrier électronique sous forme de fichiers joints, vous pouvez envoyer et recevoir des documents commerciaux par voie électronique. Par document électronique, on entend un fichier conforme aux normes représentant un document commercial comme une facture fournisseur que vous pouvez recevoir et convertir en facture achat dans [!INCLUDE[prod_short](includes/prod_short.md)]. L’échange de documents électroniques entre deux partenaires commerciaux est exécuté par un fournisseur externe de services d’échange de documents. La version générique de [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge l’envoi et la réception de factures et d’avoirs électroniques au format PEPPOL, qui est pris en charge par les principaux fournisseurs de services d’échange de documents. Un fournisseur principal de services d’échange de documents est préconfiguré et prêt à être installé pour votre société.  

À partir de fichiers PDF ou image représentant des documents entrants, un service OCR externe (reconnaissance optique de caractères) peut créer des documents électroniques pouvant être convertis en enregistrements de document dans [!INCLUDE[prod_short](includes/prod_short.md)], comme pour les documents électroniques PEPPOL. Par exemple, lorsque vous recevez une facture au format PDF de votre fournisseur, vous pouvez l’envoyer au service OCR à partir de la page **Documents entrants**. Après quelques secondes, vous recevrez le fichier sous forme de facture électronique pouvant être convertie en facture achat pour le fournisseur. Si vous envoyez le fichier au service OCR par courrier électronique, un enregistrement de document entrant est automatiquement créé lorsque vous recevez le document électronique.  

Le format de document électronique **PEPPOL** est préconfiguré pour vous permettre d’envoyer les factures et des avoirs électroniques au format PEPPOL. Au préalable, vous devez configurer différentes données de base, telles que les informations sur la société, les clients, les articles, et les unités de mesure. Ceux-ci sont utilisés pour identifier les partenaires commerciaux et les articles lors de la conversion des données dans des champs dans [!INCLUDE[prod_short](includes/prod_short.md)] en éléments figurant dans le fichier document sortant. Enfin, vous devez sélectionner le format sur la page **Format de document électronique** pour chaque client à qui vous enverrez des documents électroniques PEPPOL. Pour plus d’informations, voir [Envoyer des documents électroniques](sales-how-to-send-electronic-documents.md).  

Les définitions d’échange de données **PEPPOL - Facture** et **PEPPOL – Avoir** sont préconfigurées pour vous permettre de recevoir les factures électroniques et les avoirs au format PEPPOL. Au préalable, vous devez configurer différentes données de base, telles que les informations sur la société, les fournisseurs, les articles, et les unités de mesure. Celles-ci sont utilisées pour identifier les partenaires commerciaux et les articles lors de la conversion des données en fichier document entrant dans des champs dans [!INCLUDE[prod_short](includes/prod_short.md)]. Enfin, vous devez sélectionner la définition d’échange de données sur la page **Documents entrants** pour chaque document électronique entrant que vous souhaitez convertir en document achat dans [!INCLUDE[prod_short](includes/prod_short.md)].  

La définition d’échange de données **OCR - Facture** est préconfigurée pour vous permettre de recevoir des documents électroniques générés par le service OCR. Pour recevoir, par exemple, une facture en tant que document OCR électronique, vous configurez une date principale, puis traitez le document comme lorsque vous recevez un document PEPPOL électronique. Pour en savoir plus, voir [Utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques](across-how-use-ocr-pdf-images-files.md).  

Les services préconfigurés pour l’échange de documents et pour le service OCR doivent être activés avant l’envoi ou la réception. Pour plus d’informations, reportez vous à [Configurer un service d’échange de document](across-how-to-set-up-a-document-exchange-service.md).  

La rubrique contient les procédures suivantes :  

* Configurer la société pour l’envoi et la réception de documents électroniques  
* Configurer la comptabilisation TVA pour l’envoi et la réception de documents électroniques  
* Configurer les pays/régions pour l’envoi et la réception de documents électroniques  
* Configurer les articles pour l’envoi et la réception de documents électroniques  
* Configurer les unités de mesure pour l’envoi et la réception de documents électroniques  
* Configurer les clients pour l’envoi d’un document électronique  
* Sélectionner le format de document électronique **PEPPOL** pour l’envoi d’un document électronique  
* Configurer les fournisseurs pour la réception d’un document électronique  
* Sélectionner la définition d’échange de données **PEPPOL - Facture** pour la réception d’un document électronique  
* Configurer le compte général pour utiliser de nouvelles lignes facture achat pour des articles non\-identifiables et des non\-articles  

### Configurer la société pour l’envoi et la réception de documents électroniques

1. Dans la zone **Rechercher**, saisissez **Informations société**, puis sélectionnez le lien associé.  
2. Dans le raccourci **Général**, renseignez les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identifiez votre société.<br /><br /> Par exemple, lorsque vous envoyez des factures électroniques au format PEPPOL, la valeur de ce champ est utilisée pour remplir l’élément **EndPointID** dans le nœud **AccountingSupplierParty** dans le fichier. Le numéro est basé sur le standard GS1, qui est conforme à ISO 6523.|  
    |**N° identif. intracomm.**|Spécifiez le numéro d’identification intra-communautaire.|  
    |**Centre de gestion**|Si votre société est configurée avec un centre de gestion, assurez-vous que le champ **Code pays/région** est renseigné.|  

### Configurer la comptabilisation TVA pour l’envoi et la réception de documents électroniques

1. Dans la zone **Rechercher**, saisissez **Paramètres compta. TVA**, puis sélectionnez le lien associé.  
2. Pour chaque ligne des paramètres validation TVA que vous utiliserez pour des documents électroniques, renseignez le champ comme décrit dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Catégorie de taxe**|Spécifiez la catégorie de TVA.<br /><br /> Par exemple, lorsque vous envoyez des factures électroniques au format PEPPOL, la valeur de ce champ est utilisée pour remplir l’élément **TaxApplied** dans le nœud **AccountingSupplierParty** dans le fichier. Le numéro est basé sur le UNCL5305 standard.|  

### Configurer les pays/régions pour l’envoi et la réception de documents électroniques

1. Dans la zone **Rechercher**, saisissez **Pays/Régions**, puis choisissez le lien associé.  
2. Pour chaque pays/région avec lequel vous échangerez des documents électroniques, renseignez le champ comme décrit dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Régime de TVA**|Identifiez l’organisme national qui émet le numéro d’identification intra-communautaire du pays\/de la région en relation avec l’envoi de document électronique.<br /><br /> Par exemple, lorsque vous envoyez des factures électroniques au format PEPPOL, la valeur de ce champ est utilisée pour remplir l’attribut **SchemeID** pour l’élément **EndPointID** sous, à la fois le nœud **AccountingSupplierParty** et le **AccountingCustomerParty** dans le fichier.<br /><br /> Le champ **Régime de TVA** n’est utilisé que si le champ **GLN** sur la page **Informations société** n’est pas renseigné. **Remarque :** la valeur du champ **Code** sur la page **Pays\/Régions** doit être conforme à ISO 3166\-1:Alpha2.|  

### Configurer les articles pour l’envoi et la réception de documents électroniques

1. Dans la boîte de dialogue **Rechercher**, entrez **Articles**, puis sélectionnez le lien associé.  
2. Pour chaque article que vous achetez ou vendez sur des documents électroniques, renseignez le champ comme décrit dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**GTIN**|Identifie l’article en relation avec l’envoi et la réception de document électronique. Pour le format PEPPOL, le champ est utilisé comme suit :<br /><br /> Si l’élément **StandardItemIdentification\/ID** a l’attribut **SchemeID** défini sur **GTIN**, alors l’élément est mappé au champ **GTIN** de la fiche article.|  

### Configurer les unités de mesure pour l’envoi et la réception de documents électroniques

1. Dans la zone **Rechercher**, entrez **Unité de mesure**, puis choisissez le lien associé.  
2. Pour chaque unité de mesure que vous utiliserez pour articles sur des documents électroniques, renseignez le champ comme décrit dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code norme internationale**|Spécifiez le code de l’unité de mesure exprimé en fonction de la norme UNECERec20 en relation avec l’envoi des documents électroniques.<br /><br /> Par exemple, lorsque vous envoyez des factures électroniques au format PEPPOL, la valeur de ce champ est utilisée pour remplir l’attribut **unitCode** de l’élément **InvoicedQuantity** dans le nœud **InvoiceLine**. **Remarque :** si le champ **Unité** de la ligne vente est vide, la valeur UNECERe20 standard de la « pièce » \(H87\) est insérée par défaut. Pour plus d’informations et pour obtenir une liste des codes unité de mesure valides, reportez-vous à la [Recommandation n° 20 \- Units of Measure used in International Trade (Unités de mesure utilisées sur le marché international)](https://www.unece.org/fileadmin/DAM/cefact/recommendations/rec20/rec20_rev3_Annex2e.pdf).|  

### Configurer les clients pour l’envoi d’un document électronique

1. Dans la zone **Rechercher**, saisissez **Clients**, puis sélectionnez le lien associé.  
2. Pour chaque client à qui vous enverrez un document électronique, renseignez les champs comme décrit dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identifiez le client.<br /><br /> Par exemple, lorsque vous envoyez des factures électroniques au format PEPPOL, la valeur de ce champ est utilisée pour remplir l’élément **EndPointID** dans le nœud **AccountingCustomerParty** dans le fichier. Le numéro est basé sur le standard GS1, qui est conforme à ISO 6523.<br /><br /> Si le champ **GLN** est vide, la valeur du champ **N° identif. intracomm.** est utilisée.|  
    |**N° identif. intracomm.**|Spécifiez le numéro d’identification intra-communautaire du client. **Astuce :** dans les versions localisées prises en charge, choisissez le bouton Analyser pour utiliser le service Web qui vérifie si le numéro existe dans le registre national des sociétés.|  
    |**Centre de gestion**|Si le client est configuré avec un centre de gestion, assurez-vous que le champ **Code pays/région** est renseigné.|  

    Vous pouvez configurer chaque client avec une méthode préférée d’envoi de documents commerciaux, afin d’éviter d’avoir à sélectionner une option d’envoi chaque fois que vous envoyez un document au client. Pour plus d’informations, reportez vous à [Configurer des profils d’envoi de documents](sales-how-setup-document-send-profiles.md).  

### Sélectionner le format de document électronique PEPPOL pour l’envoi d’un document électronique  
1. Dans la zone **Rechercher**, entrez **Profils d’envoi de documents**, puis choisissez le lien associé.  
2. Ouvrez un profil existant d’envoi de document, ou créez-en un. Pour plus d’informations, reportez vous à [Configurer des profils d’envoi de documents](sales-how-setup-document-send-profiles.md).  
3. Sur la page **Profil d’envoi de documents**, choisissez le **Format électronique**, sélectionnez la ligne associée à PEPPOL, puis sélectionnez **OK**.  
4. Dans le champ **Document électronique**, sélectionnez **Oui (via le service d’échange de documents)**.  

    > [!NOTE]  
    >  [!INCLUDE[prod_short](includes/prod_short.md)] détecte automatiquement si le document est une facture ou un avoir et applique le format PEPPOL en conséquence.  

5. Pour que ce profil d’envoi de document s’applique à tous les clients, activez la case à cocher **Par défaut** sur le raccourci **Général**. Pour que cette opération ne s’applique qu’à des clients spécifiques, renseignez le champ **Profil d’envoi de documents** des fiches article en question. Pour plus d’informations, reportez vous à [Configurer des profils d’envoi de documents](sales-how-setup-document-send-profiles.md).  

    Vous pouvez désormais envoyer le document électronique contenant des données converties. Pour plus d’informations, voir [Envoyer des documents électroniques](sales-how-to-send-electronic-documents.md).  

### Configurer les fournisseurs pour la réception d’un document électronique  
1. Dans la zone **Rechercher**, entrez **Fournisseurs**, puis sélectionnez le lien associé.  
2. Pour chaque fournisseur de qui vous recevrez un document électronique, renseignez les champs comme décrit dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identifiez le fournisseur.<br /><br /> Par exemple, lorsque vous recevez des factures électroniques au format PEPPOL, la valeur de ce champ est utilisée pour remplir l’élément **EndPointID** dans le nœud **AccountingSupplierParty** dans le fichier. Le numéro est basé sur le standard GS1, qui est conforme à ISO 6523.<br /><br /> Si le champ **GLN** est vide, la valeur du champ **N° identif. intracomm.** est utilisée.|  
    |**N° identif. intracomm.**|Spécifiez le numéro d’identification intra-communautaire du fournisseur. **Astuce :** dans les versions localisées prises en charge, choisissez le bouton Analyser pour utiliser le service Web qui vérifie si le numéro existe dans le registre national des sociétés.|  
    |**Centre de gestion**|Si le fournisseur est configuré avec un centre de gestion, assurez-vous que le champ **Code pays/région** est renseigné.|  

### Sélectionner la définition d’échange de données PEPPOL – Facture pour la réception d’un document électronique  
1. Dans la zone **Rechercher**, entrez **Documents entrants**, puis sélectionnez le lien associé.  
2. Sur la ligne du document électronique que vous souhaitez recevoir et convertir, choisissez le champ **Type d’échange de données**, puis sélectionnez **PEPPOLINVOICE**.  

     Si le document à recevoir est un avoir, sélectionnez **PEPPOLCREDITMEMO**.  

    Vous pouvez désormais recevoir le document électronique en démarrant le processus de conversion de données sur la page **Documents entrants**. Pour plus d’informations; voir [Recevoir et convertir des documents électroniques](purchasing-how-to-receive-and-convert-electronic-documents.md).  

### Configurer le compte général pour utiliser de nouvelles lignes facture achat pour des articles non identifiables et des non-articles  
1. Dans la zone **Rechercher**, entrez **Paramètres achats**, puis choisissez le lien associé.  
2. Sous le raccourci **Comptes par défaut**, renseignez le champ comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Compte général pour lignes non-article**|Spécifie le compte G/L inséré automatiquement dans les lignes d’achat créées à partir de documents électroniques lorsque la ligne de document entrant ne contient pas d’article identifiable. Une ligne document entrant sans GTIN ni numéro d’article du fournisseur sera convertie en ligne achat de type **Compte général** et le champ **N°**. de la ligne achat affichera le compte que vous sélectionnez dans le champ **Compte général pour lignes non-article**.<br /><br /> Si vous laissez le champ **Compte général pour lignes non-article** vide et que le document entrant possède des lignes sans articles identifiables, alors le document d’achat ne sera pas créé. Un message d’erreur vous donnera des instructions pour remplir le champ **Compte général pour lignes non-article** avant de pouvoir terminer la tâche.|  

## Voir la [formation Microsoft](/training/modules/electronic-documents-dynamics-365-business-central/index) associée

## Voir aussi  
[Échanger des données par voir électronique](across-data-exchange.md)   
[Facturer des ventes](sales-how-invoice-sales.md)   
[Enregistrer des achats](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
