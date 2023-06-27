---
title: Créer des enregistrements document entrant depuis Docs
description: Vous pouvez enregistrer des documents commerciaux externes en liant des fichiers document aux enregistrements document entrant associées.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries" />Créer des enregistrements document entrant directement à partir de documents et d’écritures

Vous pouvez enregistrer des documents commerciaux externes dans [!INCLUDE[prod_short](includes/prod_short.md)] en liant des fichiers document aux enregistrements document entrant associées. Si le document, une facture achat par exemple, n’était pas dès le départ un enregistrement document entrant, vous pouvez toujours créer et le lier à un enregistrement document entrant ultérieurement. Vous pouvez également joindre des fichiers document entrant à des documents achat et vente validés et à des écritures fournisseur, client et comptables à l’aide du récapitulatif **Fichiers document entrant** dans, par exemple, les pages **Factures achat enregistrées** et **Écritures comptables fournisseur**.

Depuis les pages **Plan comptable** et **Écritures comptables**, vous pouvez utiliser la fonction de recherche pour rechercher les écritures comptables pour des documents achat et vente validés qui n’ont pas d’enregistrement de document entrant, puis les lier de façon centralisée à des enregistrements existants ou en créer de nouveaux avec des fichiers joints. Pour plus d’informations, voir [Rechercher des enregistrements validés sans enregistrements document entrant](across-how-find-posted-documents-without-income-document-records.md).

Les procédures suivantes indiquent comment joindre un fichier à une écriture comptable fournisseur ou à une facture achat existante qui n’a pas été créée à partir d’un enregistrement document entrant. La même action permet de joindre un fichier à des documents achat ou vente validés.

## <a name="create-and-connect-an-incoming-document-record-from-a-purchase-invoice" />Créer et lier un enregistrement document entrant à partir d’une facture achat

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures achat**, puis sélectionnez le lien associé.
2. Sélectionnez la ligne de la facture achat à laquelle vous souhaitez joindre un fichier, puis sélectionnez l’action **Créer un document entrant à partir d’un fichier**.
3. Vous pouvez également sélectionner la ligne de la facture achat à laquelle vous souhaitez joindre un fichier, puis sélectionner l’action **Joindre fichier**.
4. Sur la page **Insérer un fichier**, sélectionnez le fichier qui représente le document entrant concerné, puis choisissez le bouton **Ouvrir**.

## <a name="create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry" />Créer et lier un enregistrement document entrant à partir d’une écriture comptable fournisseur

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Écritures comptables fournisseur**, puis sélectionnez le lien associé.
2. Sélectionnez une ligne d’une écriture comptable fournisseur à laquelle vous souhaitez joindre un fichier, puis sélectionnez l’action **Créer un document entrant à partir d’un fichier**.
3. Vous pouvez également sélectionner une ligne d’une une écriture comptable fournisseur à laquelle vous souhaitez joindre un fichier, puis sélectionner l’action **Joindre fichier**.
4. Sur la page **Insérer un fichier**, sélectionnez le fichier qui représente le document entrant concerné, puis choisissez le bouton **Ouvrir**.

## <a name="remove-a-connection-from-an-incoming-document-record-to-a-posted-document" />Pour supprimer la connexion d’un enregistrement document entrant à un document validé

Vous pouvez supprimer des fichiers joints de documents non validés à tout moment en supprimant l’enregistrement document entrant associé. Si le document est validé, vous devez d’abord supprimer la connexion de l’enregistrement document entrant.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Documents entrants**, puis choisissez le lien associé.
2. Sélectionnez la ligne correspondant à un enregistrement document entrant lié à un document validé que vous souhaitez supprimer, puis sélectionnez **Supprimer la référence à l’enregistrement**.

La connexion au document validé est supprimée. Vous pouvez maintenant connecter un autre enregistrement document entrant au document validé, comme cela est décrit dans cet article.

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/modules/incoming-documents-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi

[Créer des enregistrements document entrant](across-how-create-income-document-records.md)
[Utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques](across-how-use-ocr-pdf-images-files.md)
[Rechercher des enregistrements validés sans enregistrements document entrant](across-how-find-posted-documents-without-income-document-records.md)
[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
