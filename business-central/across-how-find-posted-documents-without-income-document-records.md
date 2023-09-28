---
title: Rechercher des enregistrements validés sans document entrant
description: 'Vous pouvez rechercher des écritures comptables pour des documents achat et vente validés qui n’ont pas de documents électroniques entrants, tels que les factures importées.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
---
# Rechercher des enregistrements validés sans enregistrements document entrant

Depuis les pages **Plan comptable** et **Écritures comptables**, vous pouvez utiliser la fonction de recherche pour rechercher les écritures comptables pour des documents achat et vente validés qui n’ont pas d’enregistrement de document entrant, puis les lier de façon centralisée à des enregistrements existants ou en créer de nouveaux avec des fichiers joints.

## Rechercher des enregistrements validés sans enregistrements document entrant

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.
2. Sélectionnez une ligne pour un compte général pour les écritures comptables duquel vous souhaitez voir les documents ventes et achats validés sans enregistrement document entrant, puis sélectionnez l’action **Documents validés sans document entrant**.
3. Sinon, sélectionnez l’action **Écritures comptables**.
4. Sur la page **Écritures comptables**, sélectionnez l’action **Documents validés sans documents entrants**.

La page **Documents validés sans document entrant** s’ouvre et affiche des documents achat et vente validés sans enregistrement document entrant représenté par des écritures comptables du compte général pour lequel vous avez ouvert la page. Au maximum, la page affiche 1 000 lignes. Par défaut, le champ **Filtre date** contient donc un filtre qui limite l’affichage des lignes à celles dont les écritures ont une date comptabilisation comprise entre le début de la période comptable et la date de travail.

## Lier des documents recherchés à des enregistrements document entrant existants

1. Sur la page **Documents validés sans document entrant**, sélectionnez la ligne d’un document valisé que vous souhaitez lier à un enregistrement document entrant existant, puis sélectionnez l’action **Sélectionner le document entrant**.
2. Sur la page **Documents entrants**, sélectionnez l’enregistrement document entrant que vous souhaitez lier au document validé trouvé, puis sélectionnez le bouton **OK**.
3. Sur la page **Documents validés sans document entrant**, l’enregistrement document entrant sélectionné est désormais lié au document validé, comme vous pouvez le constater dans le récapitulatif **Fichiers du document entrant**.

Si un enregistrement document entrant approprié n’existe pas sur la page **Documents entrants**, vous pouvez le créer. Pour plus d’informations, voir [Créer des enregistrements document entrant](across-how-create-income-document-records.md).

## Voir aussi

[Créer des enregistrements document entrant](across-how-create-income-document-records.md)
[Utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques](across-how-use-ocr-pdf-images-files.md)
[Créer des enregistrements document entrant directement à partir de documents et d’écritures](across-how-connect-disconnect-income-document-records.md)
[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
