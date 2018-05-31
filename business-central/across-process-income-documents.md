---
title: Traiter les documents entrants| Microsoft Docs
description: "Pour enregistrer un document externe, comme un PDF, dans Business Central, vous devez d'abord créer ou terminer un enregistrement de document externe."
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
ms.openlocfilehash: b6de34be2f16cf0b9130bc88495f27536a9d5080
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="processing-incoming-documents"></a>Traitement des documents entrants
Pour enregistrer un document externe dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez d'abord créer ou terminer un enregistrement de document externe. Vous pouvez effectuer cette opération manuellement ou prendre une photo du document externe puis créer l'enregistrement document entrant avec le fichier image joint.

À partir de fichiers PDF ou image reçus de vos partenaires commerciaux, un service externe de reconnaissance optique de caractères (OCR, Optical Character Recognition) génère des documents électroniques pouvant être convertis en enregistrements de document dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Par exemple, lorsque vous recevez une facture au format PDF de votre fournisseur, vous pouvez l'envoyer au service OCR à partir de la fenêtre **Documents entrants**. Sinon, vous pouvez envoyer le fichier au service OCR par e-mail. Ensuite, lorsque vous recevez le document électronique, un enregistrement de document entrant associé est créé automatiquement. Après quelques secondes, vous recevrez le fichier du service OCR en tant que facture électronique pouvant être convertie en facture achat pour le fournisseur.

| Pour | Voir |
| --- | --- |
| Créer des enregistrements document entrant manuellement ou automatiquement en prenant une photo d'un reçu papier, par exemple. |[Créer des enregistrements document entrant](across-how-create-income-document-records.md) |
| Utilisez un service OCR pour convertir les fichiers PDF et image en documents électroniques qui peuvent être convertis en factures achat dans [!INCLUDE[d365fin](includes/d365fin_md.md)], par exemple. Former le service OCR à éviter les erreurs la prochaine fois qu'il traite des données similaires. |[Utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques](across-how-use-ocr-pdf-images-files.md) |
| Connecter ou supprimer des enregistrements document entrant pour n'importe quel document vente ou achat non validé et à tout client, fournisseur ou écriture comptable à partir du document ou de l'écriture. |[Créer des enregistrements document entrant directement à partir de documents et d'écritures](across-how-connect-disconnect-income-document-records.md) |
| Depuis les fenêtres **Plan comptable** et **Écritures comptables**, utiliser la fonction de recherche pour rechercher les écritures comptables pour des documents validés qui n'ont pas d'enregistrement de document entrant, puis les lier de façon centralisée à des enregistrements existants ou en créer de nouveaux avec des fichiers joints. |[Rechercher des enregistrements validés sans enregistrements document entrant](across-how-find-posted-documents-without-income-document-records.md) |
| Obtenir une meilleure vue d'ensemble en définissant les enregistrements de document entrant sur Traité afin de les supprimer de la vue par défaut. |[Gérer de nombreux enregistrements document entrant](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Voir aussi
[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
