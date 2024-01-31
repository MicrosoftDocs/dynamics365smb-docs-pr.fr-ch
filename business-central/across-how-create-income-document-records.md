---
title: Créer des enregistrements document entrant
description: 'Utilisez différentes fonctions sur la page Documents entrants pour consulter les reçus de dépenses, gérer les tâches d’OCR, convertir les fichiers de documents entrants et joindre des fichiers externes.'
author: jswymer
ms.topic: how-to
ms-service: dynamics-365-business-central
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 03/2/2023
ms.author: jswymer
ms.custom: bap-template
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
---
# Créer des enregistrements document entrant

Sur la page **Documents entrants**, vous pouvez utiliser différentes fonctions pour examiner les reçus de dépenses, gérer les tâches ROC et convertir les fichiers document entrants, manuellement ou automatiquement, en documents ou lignes feuille appropriés. Les fichiers externes peuvent être joints à n’importe quelle étape du processus, notamment en ce qui concerne les documents validés et au fournisseur, au client qui en résulte, et dans les écritures comptables.

Pour enregistrer un document externe dans [!INCLUDE[prod_short](includes/prod_short.md)], vous devez créer ou terminer un enregistrement de document externe. Vous pouvez effectuer ces tâches manuellement ou prendre une photo du document externe pour créer l’enregistrement document entrant avec le fichier image joint.

Avant d’utiliser la fonctionnalité **Documents entrants**, vous devez exécuter la configuration requise. Pour plus d’informations, voir [Configurer des documents entrants](across-how-setup-income-documents.md).

## Approuver ou rejeter un document entrant

Si vous avez mis en place la fonction **Documents entrants** pour exiger une approbation pour créer des documents, les utilisateurs disposant des droits appropriés doivent approuver les enregistrements avant qu’ils ne soient traités. Pour plus d’informations, voir [Configurez des approbateurs des enregistrements de documents entrants](across-how-setup-income-documents.md#to-set-up-approvers-of-incoming-document-records).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Documents entrants**, puis choisissez le lien associé.
2. Sélectionnez la ligne contenant le document à approuver ou rejeter, puis sélectionnez l’action **Approuver** or **Rejeter**.

Si vous approuvez l’enregistrement document entrant, la case à cocher **Lancé** de la ligne document entrant est activée. L’utilisateur chargé de créer, par exemple, des factures achat peut continuer à traiter l’enregistrement.

## Créer un enregistrement de document entrant en prenant une photo

> [!NOTE]  
> La procédure suivante s’applique uniquement aux clients disposant de tablettes et de téléphones équipés de [!INCLUDE[prod_short](includes/prod_short.md)].

1. Dans le centre de rôles, sélectionnez la mosaïque **Créer le document entrant à partir de l’appareil photo**, puis passez à l’étape 4.
2. Sinon, sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Documents entrants**, puis choisissez le lien associé.
3. Sur la page **Documents entrants**, sélectionnez **Nouveau**, puis sélectionnez **Créer à partir de l’appareil photo**. L’appareil photo de la tablette ou du téléphone est activé.
4. Prenez une photo d’un document, tel qu’un reçu d’achat, que vous souhaitez traiter en tant que document entrant, puis sélectionnez le bouton **Utiliser**.

    Un enregistrement de document entrant est créé, avec l’image jointe.

## Joindre une image à un enregistrement de document entrant en prenant une photo

> [!NOTE]  
> La procédure suivante s’applique uniquement aux clients disposant de tablettes et de téléphones équipés de [!INCLUDE[prod_short](includes/prod_short.md)].

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Documents entrants**, puis choisissez le lien associé.
2. Ouvrez la fiche de l’enregistrement de document entrant existant.
3. Sur la page d’enregistrement de document, sélectionnez **Traiter**, puis sélectionnez **Joindre l’image de l’appareil photo**. L’appareil photo de la tablette ou du téléphone est activé.
4. Prenez une photo d’un document, tel qu’un reçu d’achat, que vous souhaitez traiter en tant que document entrant, puis sélectionnez le bouton **Utiliser**.

    L’image est jointe à l’enregistrement de document entrant.

## Créer un enregistrement document entrant manuellement

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Documents entrants**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**, puis l’action **Créer à partir d’un fichier**.  
3. Sur la page **Insérer un fichier**, effectuez l’une des étapes suivantes pour joindre un fichier qui représente le document entrant :

   [!INCLUDE[file-upload](includes/file-upload.md)]

4. Vous pouvez également choisir l’action **Nouveau** , puis suivre les étapes suivantes :

    1. Pour joindre un fichier, choisissez **Processus** > **Joindre un fichier**.
    2. Sur la page **Insérer un fichier**, faites glisser le fichier sélectionné qui représente le document entrant concerné ou sélectionnez **cliquez ici pour parcourir** pour trouver et ouvrir le fichier.
    3. Sur la page **Document entrant**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Voir aussi

[Utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques](across-how-use-ocr-pdf-images-files.md)
[Créer des enregistrements document entrant directement à partir de documents et d’écritures](across-how-connect-disconnect-income-document-records.md)
[Rechercher des enregistrements validés sans enregistrements document entrant](across-how-find-posted-documents-without-income-document-records.md)
[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
