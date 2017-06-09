---
title: "Procédure : connecter et déconnecter des enregistrements document entrant à partir de documents et d&quot;écritures| Microsoft Docs"
description: "Procédure : connecter et déconnecter des enregistrements document entrant à partir de documents et d&quot;écritures"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 05/12/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d29979de3643cbe542f31d3bc67ee0f47effcd4a
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-connect-and-disconnect-incoming-document-records-from-documents-and-entries"></a>Procédure : connecter et déconnecter des enregistrements document entrant à partir de documents et d'écritures
Vous pouvez enregistrer des documents commerciaux externes dans [!INCLUDE[d365fin](includes/d365fin_md.md)] en liant des fichiers document aux enregistrements document entrant associées. Si le document, une facture achat par exemple, n'était pas dès le départ un enregistrement document entrant, vous pouvez toujours créer et le lier à un enregistrement document entrant ultérieurement. Vous pouvez également joindre des fichiers document entrant à des documents achat et vente validés et à des écritures fournisseur, client et comptables à l'aide du récapitulatif **Fichiers document entrant** dans, par exemple, les fenêtres **Factures achat enregistrées** et **Écritures comptables fournisseur**.

Depuis les fenêtres **Plan comptable** et **Écritures comptables**, vous pouvez utiliser la fonction de recherche pour rechercher les écritures comptables pour des documents achat et vente validés qui n'ont pas d'enregistrement de document entrant, puis les lier de façon centralisée à des enregistrements existants ou en créer de nouveaux avec des fichiers joints. Pour plus d'informations, reportez-vous à [Procédure : Rechercher des enregistrements validés sans enregistrements document entrant](across-how-find-posted-documents-without-income-document-records.md).

Les procédures suivantes indiquent comment joindre un fichier à une facture achat existante qui n'a pas été créée à partir d'un enregistrement document entrant et comment joindre un fichier à une écriture comptable fournisseur. La même action permet de joindre un fichier à des documents achat ou vente validés.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Créer et lier un enregistrement document entrant à partir d'une facture achat
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Factures achat**, puis sélectionnez le lien associé.
2. Sélectionnez la ligne de la facture achat à laquelle vous souhaitez joindre un fichier, puis sélectionnez l'action **Créer un document entrant à partir d'un fichier**.
3. Vous pouvez également sélectionner la ligne de la facture achat à laquelle vous souhaitez joindre un fichier, puis sélectionner l'action **Joindre fichier**.
4. Dans la fenêtre **Insérer un fichier**, sélectionnez le fichier qui représente le document entrant concerné, puis choisissez le bouton **Ouvrir**.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Créer et lier un enregistrement document entrant à partir d'une écriture comptable fournisseur
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Écritures comptables fournisseur**, puis sélectionnez le lien associé.
2. Sélectionnez une ligne d'une écriture comptable fournisseur à laquelle vous souhaitez joindre un fichier, puis sélectionnez l'action **Créer un document entrant à partir d'un fichier**.
3. Vous pouvez également sélectionner une ligne d'une une écriture comptable fournisseur à laquelle vous souhaitez joindre un fichier, puis sélectionner l'action **Joindre fichier**.
4. Dans la fenêtre **Insérer un fichier**, sélectionnez le fichier qui représente le document entrant concerné, puis choisissez le bouton **Ouvrir**.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>Pour supprimer la connexion d'un enregistrement document entrant à un document validé
Vous pouvez supprimer des fichiers joints de documents non validés à tout moment en supprimant l'enregistrement document entrant associé. Si le document est validé, vous devez d'abord supprimer la connexion de l'enregistrement document entrant.

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Documents entrants**, puis sélectionnez le lien associé.
2. Sélectionnez la ligne correspondant à un enregistrement document entrant lié à un document validé que vous souhaitez supprimer, puis sélectionnez **Supprimer la référence à l'enregistrement**.

La connexion au document validé est supprimée. Vous pouvez maintenant connecter un autre enregistrement document entrant au document validé, comme cela est décrit dans cette rubrique.

## <a name="see-also"></a>Voir aussi
[Traiter les documents entrants](across-process-income-documents.md)  
[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

