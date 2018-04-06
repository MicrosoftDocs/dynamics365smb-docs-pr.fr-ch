---
title: "Rechercher des documents sans pièces jointes| Microsoft Docs"
Description: You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: af0e886189750123dbee80e528e7c9d9b2c04f9f
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="find-posted-documents-without-incoming-document-records"></a>Rechercher des enregistrements validés sans enregistrements document entrant
Depuis les fenêtres **Plan comptable** et **Écritures comptables**, vous pouvez utiliser la fonction de recherche pour rechercher les écritures comptables pour des documents achat et vente validés qui n'ont pas d'enregistrement de document entrant, puis les lier de façon centralisée à des enregistrements existants ou en créer de nouveaux avec des fichiers joints.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>Rechercher des enregistrements validés sans enregistrements document entrant
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Plan comptable**, puis sélectionnez le lien connexe.
2. Sélectionnez une ligne pour un compte général pour les écritures comptables duquel vous souhaitez voir les documents ventes et achats validés sans enregistrement document entrant, puis sélectionnez l'action **Documents validés sans document entrant**.
3. Sinon, sélectionnez l'action **Écritures comptables**.
4. Dans la fenêtre **Écritures comptables**, sélectionnez l'action **Documents validés sans documents entrants**.

La fenêtre **Documents validés sans document entrant** s'ouvre et affiche des documents achat et vente validés sans enregistrement document entrant représenté par des écritures comptables du compte général pour lequel vous avez ouvert la fenêtre. Au maximum, la fenêtre affiche 1 000 lignes. Par défaut, le champ **Filtre date** contient donc un filtre qui limite l'affichage des lignes à celles dont les écritures ont une date comptabilisation comprise entre le début de la période comptable et la date de travail.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Lier des documents recherchés à des enregistrements document entrant existants
1. Dans la fenêtre **Documents validés sans document entrant**, sélectionnez la ligne d'un document valisé que vous souhaitez lier à un enregistrement document entrant existant, puis sélectionnez l'action **Sélectionner le document entrant**.
2. Dans la fenêtre **Documents entrants**, sélectionnez l'enregistrement document entrant que vous souhaitez lier au document validé trouvé, puis sélectionnez le bouton **OK**.
3. Dans la fenêtre **Documents validés sans document entrant**, l'enregistrement document entrant sélectionné est désormais lié au document validé, comme vous pouvez le constater dans le récapitulatif **Fichiers du document entrant**.

Si un enregistrement document entrant approprié n'existe pas dans la fenêtre **Documents entrants**, vous pouvez le créer. Pour plus d'informations, voir [Créer des enregistrements document entrant](across-how-create-income-document-records.md).

## <a name="see-also"></a>Voir aussi
[Traiter les documents entrants](across-process-income-documents.md)  
[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

