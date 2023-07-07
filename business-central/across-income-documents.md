---
title: Utiliser des documents entrants
description: 'Vous pouvez gérer les documents commerciaux externes entrants, tels que des reçus de paiement ou des fichiers PDF, gérer des tâches OCR, et convertir des fichiers en documents électroniques et enregistrements.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="incoming-documents"></a>Documents entrants

Les documents provenant d’entreprises externes peuvent arriver dans votre société sous forme de pièce jointe à un e-mail, ou de copie papier que vous pouvez scanner vers un fichier. Ce scénario est classique dans le cas des achats, lorsque ces fichiers de documents entrants sont des reçus de paiements pour des dépenses ou de petits achats.

Sur la page **Documents entrants**, vous pouvez utiliser différentes fonctions pour examiner les reçus de dépenses, gérer les tâches ROC et convertir les fichiers document entrants, manuellement ou automatiquement, en documents ou lignes feuille appropriés. Les fichiers externes peuvent être joints à n’importe quelle étape du processus, notamment en ce qui concerne les documents validés et au fournisseur, au client qui en résulte, et dans les écritures comptables.

## <a name="usage-scenario"></a>Scénario d’utilisation

Vous pouvez enregistrer les fichiers ou copies papier reçus de vos partenaires commerciaux dans [!INCLUDE[prod_short](includes/prod_short.md)] et créer un enregistrement de document. Par exemple, une facture achat ou vente, un avoir ou une ligne feuille.

Chargez les fichiers reçus (ou utilisez la caméra de l’appareil pour en prendre une photo) et créez des entrées pour représenter les documents externes. De manière facultative, à partir de fichiers PDF ou image, un service OCR externe (Reconnaissance optique de caractères) peut générer des documents électroniques qui peuvent ensuite être convertis en enregistrements au sein de [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> La fonction OCR est assurée par des fournisseurs externes. Choisissez un package de services adapté à votre organisation et/ou votre pays/région. Vous trouverez des services compatibles avec [!INCLUDE[prod_short](includes/prod_short.md)] et des détails sur les fonctionnalités disponibles sur [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

Par exemple, lorsque vous recevez une facture au format PDF de votre fournisseur, vous pouvez l’envoyer au service OCR à partir de la page **Documents entrants**. Alternativement, certains fournisseurs OCR offrent la possibilité de traiter les fichiers transmis à une adresse e-mail dédiée, qui crée ensuite automatiquement un enregistrement de document entrant associé. Après quelques secondes, vous recevrez le fichier du service OCR en tant que facture électronique pouvant être convertie en facture achat pour le fournisseur.

> [!TIP]
> Créez des enregistrements de documents entrants dans [!INCLUDE[prod_short](includes/prod_short.md)] directement à partir des e-mails envoyés par les fournisseurs à l’aide du complément Outlook. Pour plus d’informations, voir [Utiliser Business Central en tant que boîte de réception professionnelle dans Outlook](work-outlook-addin.md).

## <a name="incoming-document-features"></a>Fonctionnalités de document entrant

Le processus de document entrant est composé des activités principales suivantes :

* Enregistrez les documents externes dans [!INCLUDE[prod_short](includes/prod_short.md)] en créant des lignes sur la page **Documents entrants** de l’une des manières suivantes :
  * Manuellement, à partir d’un PC ou d’un périphérique mobile, de l’une des manières suivantes :
    * Utilisez le bouton **Créer à partir d’un fichier**, chargez un fichier, puis renseignez les champs appropriés sur la page **Document entrant**.
    * Utilisez le bouton **Nouveau**, renseignez les champs appropriés sur la page **Document entrant**, puis joignez manuellement le fichier associé.
    * À partir d’une tablette ou d’un téléphone, utilisez le bouton **Créer à partir de l’appareil photo** pour créer un enregistrement de document entrant à l’aide de la caméra intégrée de l’appareil.
  * Automatiquement en recevant le document du service OCR en tant que document électronique après avoir chargé ou envoyé par e-mail le fichier PDF ou image associé à un service OCR. Le raccourci **Informations financières** est automatiquement renseigné sur la page **Document entrant**.
* Utilisez un service OCR externe pour convertir des fichiers PDF ou image en documents électroniques pouvant être convertis en enregistrements de document dans [!INCLUDE[prod_short](includes/prod_short.md)].
* Créez des documents ou des lignes feuille comptabilité à partir d’enregistrements document entrants en saisissant les informations telles que vous les lisez à partir des fichiers document entrants.
* Joignez des fichiers document entrant à des documents vente et achat de tout statut, notamment au fournisseur, client, et écritures comptables qui résultent de la validation.
* Affichez les enregistrements document entrant et leurs pièces jointes à partir de tout document achat et vente ou de toute écriture, ou recherchez toutes les écritures comptables sans enregistrement document entrant sur la page **Plan comptable**.

> [!NOTE]
> Les fichiers joints à des fiches et des documents dans l’onglet **Pièces jointes** ne sont pas inclus dans la page **Documents entrants**. Pour plus d’informations, voir [Gérer les pièces jointes, les liens et les notes sur les fiches et les documents](ui-how-add-link-to-record.md).

| À | Voir |
| --- | --- |
| Configurez la fonctionnalité **Documents entrants** et le service OCR. |[Configurer des documents entrants](across-how-setup-income-documents.md) |
| Créer des enregistrements document entrant manuellement ou automatiquement en prenant une photo d’un reçu papier, par exemple. |[Créer des enregistrements document entrant](across-how-create-income-document-records.md) |
| Utilisez un service OCR pour convertir les fichiers PDF et image en documents électroniques qui peuvent être convertis en factures achat dans [!INCLUDE[prod_short](includes/prod_short.md)], par exemple. Former le service OCR à éviter les erreurs la prochaine fois qu’il traite des données similaires. |[Utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques](across-how-use-ocr-pdf-images-files.md) |
| Connecter ou supprimer des enregistrements document entrant pour n’importe quel document vente ou achat non validé et à tout client, fournisseur ou écriture comptable à partir du document ou de l’écriture. |[Créer des enregistrements document entrant directement à partir de documents et d’écritures](across-how-connect-disconnect-income-document-records.md) |
| Depuis les pages **Plan comptable** et **Écritures comptables**, utiliser la fonction de recherche pour rechercher les écritures comptables pour des documents validés qui n’ont pas d’enregistrement de document entrant, puis les lier de façon centralisée à des enregistrements existants ou en créer de nouveaux avec des fichiers joints. |[Rechercher des enregistrements validés sans enregistrements document entrant](across-how-find-posted-documents-without-income-document-records.md) |
| Obtenir une meilleure vue d’ensemble en définissant les enregistrements de document entrant sur *Traité* afin de les supprimer de la vue par défaut. |[Gérer de nombreux enregistrements document entrant](across-how-manage-many-income-document-records.md) |

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/incoming-documents-dynamics-365-business-central/) associée

## <a name="see-also"></a>Voir aussi

[Achats](purchasing-manage-purchasing.md)  
[Modifier les documents validés](across-edit-posted-document.md)  
[Échanger des données par voir électronique](across-data-exchange.md)  
[Intégration de Business Central et OneDrive Entreprise](across-onedrive-overview.md)  
[Utiliser Business Central en tant que boîte de réception professionnelle dans Outlook](work-outlook-addin.md)  
[Envoyer des documents et des e-mails](ui-how-send-documents-email.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
