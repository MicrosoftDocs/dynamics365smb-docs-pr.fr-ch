---
title: Attribuer des dispositions de documents aux clients ou aux fournisseurs
description: Utilisez les dispositions de document pour contrôler l’apparence et le format des documents tels que les factures et les commandes que vous envoyez aux clients et aux fournisseurs.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '21, 9650'
ms.date: 04/07/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Définir des présentations de document pour les clients et les fournisseurs

Les dispositions de document utilisent des dispositions de rapport pour définir l’apparence des documents que vous envoyez aux clients et aux fournisseurs. Business Central fournit des dispositions standard, mais vous pouvez également personnaliser des dispositions personnalisées pour chacun de vos partenaires commerciaux. Pour plus d’informations, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md). Vous sélectionnez des dispositions de document standard et personnalisées à partir des fiches client et fournisseur en choisissant l’action **Dispositions des documents**. La valeur dans le champ **Activité** définit le processus pour lequel la disposition du document est utilisée. Par exemple, pour les clients, vous pouvez utiliser les types de dispositions de document **Rappel**, **Expédition** et **Confirmation**.

Les dispositions de documents peuvent également vous faire gagner du temps lorsque vous envoyez des documents aux contacts des clients ou des fournisseurs par e-mail. Pour chaque disposition que vous attribuez au client ou au contact, vous pouvez spécifier une ou plusieurs adresses e-mail de contact. Par exemple, vous pouvez envoyer une facture aux contacts achats et entrepôt du client. L’ajout d’adresses e-mail de contact est facile. Sur la page **Présentations document**, l’action **Sélectionner une adresse e-mail dans Contacts** vous permet de choisir dans une liste les adresses e-mail de contact que vous avez enregistrés pour le client ou le fournisseur. Vous pouvez également ajouter des adresses e-mail manuellement. Si vous entrez plusieurs adresses, séparez-les par un point-virgule et n’ajoutez pas d’espaces entre les adresses.

Avant de pouvoir définir la présentation de document à utiliser pour les processus ainsi que le contact auquel envoyer le document, vous devez charger tous les rapports (documents) disponibles dans la page **Sélection des états**. Vous pouvez charger rapidement les documents en utilisant l’action **Copier à partir de la sélection de rapport** sur la page **Dispositions de document**.

Les étapes de la section suivante décrivent comment définir des dispositions de document vente sur la page **Fiche client**. Pour les fournisseurs, les étapes sont les mêmes pour la page **Fiche fournisseur**.

## <a name="to-load-the-standard-document-layouts-for-sales-documents-for-a-customer"></a>Pour charger les modèles de document standard pour les documents de vente d’un client

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Ouvrez la page **Fiche client** pour le client, puis choisissez l’action **Dispositions de document**.
3. Sur la page **Présentations document**, choisissez l’action **Copier à partir de la sélection des états**.

La page **Dispositions de document** affiche toutes les dispositions disponibles pour les documents vente. 

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Pour sélectionner une présentation de rapport personnalisée à utiliser pour la présentation du document vente

Si vous n’avez pas encore créé de disposition de rapport personnalisée pour le type de document, vous devez d’abord le faire. Pour plus d’informations, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Ouvrez la page **Fiche client** pour le client, puis choisissez l’action **Dispositions de document**.
3. Sur la page **Présentations document**, sur la ligne d’une présentation de rapport pour laquelle vous souhaitez utiliser une présentation personnalisée, choisissez le champ **Description présentation personnalisée**.
4. Sur la page **Dispositions rapport personnalisées**, sélectionnez la disposition de document que vous souhaitez utiliser pour le type de document vente. Pour plus d’informations, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).

## <a name="to-specify-which-contact-will-receive-which-document-layout-for-a-customer"></a>Pour spécifier le contact qui recevra la disposition de document pour un client

Pour gagner du temps lorsque vous envoyez des documents aux contacts des clients et des fournisseurs par e-mail, spécifiez leurs adresses e-mail sur les modèles de document. Par exemple, vous pouvez toujours envoyer les relevés client à leurs contacts comptables et les commandes vente à leurs acheteurs ou les commandes achat aux vendeurs des fournisseurs.

1. Sur la page **Présentations document**, sur la ligne d’une présentation de rapport que vous souhaitez envoyer à un contact spécifique pour le client, choisissez l’action **Sélectionner une adresse e-mail dans Contacts**.
2. Sur la page **Contacts**, sélectionnez un ou plusieurs contacts, puis choisissez **OK**.

## <a name="see-also"></a>Voir aussi

[Mettre à jour les présentations d’état personnalisées](ui-update-report-layouts.md)  
[Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md)  
[Importer et exporter une présentation d’état ou de document personnalisée](ui-how-import-and-export-report-layout.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Gestion des présentations d’état](ui-manage-report-layouts.md)  
[Utiliser des états, des traitements par lots et des XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
