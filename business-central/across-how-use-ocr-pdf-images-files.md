---
title: Utiliser le service OCR pour convertir les fichiers PDF en factures électroniques
description: Décrit la manière dont vous pouvez utiliser un service OCR pour convertir des fichiers PDF ou image entrants en documents électroniques.
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a><a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques

À partir de fichiers PDF ou image reçus de vos partenaires commerciaux, un service externe de reconnaissance optique de caractères (OCR, Optical Character Recognition) génère des documents électroniques pouvant être convertis en enregistrements de document dans [!INCLUDE[prod_short](includes/prod_short.md)]. Par exemple, lorsque vous recevez une facture au format PDF de votre fournisseur, vous pouvez [l’envoyer au service OCR à partir de la page **Documents entrants**](#to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page).

Au lieu d’envoyer le fichier de la page **Documents entrants**, le service OCR peut proposer l’option de [traiter les fichiers transférés à une adresse e-mail dédiée](#to-send-a-pdf-or-image-file-to-the-ocr-service-by-email). Ensuite, lorsque vous recevez le document électronique, un enregistrement de document entrant associé est créé automatiquement dans [!INCLUDE[prod_short](includes/prod_short.md)].

Après quelques secondes, le service OCR enverra le fichier traité à la page **Documents entrants** en tant qu’enregistrement de document électronique qui peut être [converti en facture achat pour le fournisseur](#to-receive-the-resulting-electronic-document-from-the-ocr-service), une facture vente, un avoir ou une écriture feuille.

Comme le service OCR est basé sur la reconnaissance optique, il est probable qu’il interprète de manière incorrecte les caractères des fichiers PDF ou image lorsqu’il traite pour la première fois les documents d’un fournisseur donné, par exemple. Il peut ne pas interpréter le logo de la société comme le nom du fournisseur ou il peut mal interpréter le montant total sur un reçu en raison de sa disposition. Pour éviter ces erreurs à l’avenir, vous pouvez les corriger dans une version distincte de la page **Document entrant**. Vous envoyez ensuite les corrections au service OCR de manière à ce qu’il interprète correctement les caractères et les champs spécifiques la prochaine fois qu’il traite un document PDF ou image pour le même fournisseur. Pour plus d’informations, reportez-vous à [Former le service OCR pour éviter les erreurs](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Le trafic de fichiers à destination et en provenance du service OCR est traité par une entrée de file d’attente de travaux dédiée. Cette file d’attente des tâches est créée automatiquement lorsque vous activez la connexion au service OCR externe. Pour plus d’informations, voir [Configurer des documents entrants](across-how-setup-income-documents.md).

> [!NOTE]
> La fonction OCR est assurée par des fournisseurs externes. Choisissez un package de services adapté à votre organisation et/ou votre pays/région. Vous trouverez des services compatibles avec [!INCLUDE[prod_short](includes/prod_short.md)] et des détails sur les fonctionnalités disponibles sur [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a><a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a>Pour envoyer un fichier PDF ou image au service OCR à partir de la page Documents entrants

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Documents entrants**, puis choisissez le lien associé.
2. Créez un enregistrement de document entrant et joignez le fichier. Pour plus d’informations, voir [Créer des enregistrements document entrant](across-how-create-income-document-records.md).  
3. Sur la page **Documents entrants**, sélectionnez une ou plusieurs lignes, puis sélectionnez l’action **Envoyer à la file d’attente des travaux**.

   La valeur dans le champ **Statut OCR** passe à **Prêt**. Le fichier PDF ou image joint est envoyé au service OCR par la file projets en fonction du planning, à condition qu’il n’existe aucune erreur.
4. Sinon, sur la page **Documents entrants**, sélectionnez une ou plusieurs lignes, puis sélectionnez l’action **Envoyer au service OCR** pour envoyer immédiatement les fichiers au traitement.

   La valeur du champ **Statut OCR** passe à **Envoyé**, s’il n’existe aucune erreur.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a><a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>Pour envoyer un fichier PDF ou image au service OCR par e-mail

À partir de votre application de messagerie, vous pouvez transférer un e-mail au fournisseur de service OCR en joignant le fichier PDF ou image. Pour plus d’informations sur l’adresse e-mail d’envoi, reportez-vous au site Web du fournisseur de service OCR.

Puisqu’aucun enregistrement de document entrant n’existe pour le fichier, un enregistrement est automatiquement créé sur la page **Documents entrants** lorsque le service OCR envoie le document électronique résultant. Pour plus d’informations, voir [Créer des enregistrements document entrant](across-how-create-income-document-records.md).

> [!NOTE]  
> Si vous utilisez une tablette ou un téléphone, vous pouvez envoyer le fichier au service OCR dès que vous avez pris une photo du document, ou vous pouvez créer un document entrant directement. Pour plus d’informations, voir [Créer un enregistrement de document entrant en prenant une photo](across-how-create-income-document-records.md#create-an-incoming-document-record-by-taking-a-photo).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a><a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>Réceptionner le document électronique résultant du service ORC

Le document électronique qui est créé par le service OCR à partir du fichier PDF ou image est automatiquement réceptionné sur la page **Documents entrants** par l’entrée de la file d’attente des travaux qui est configurée lorsque vous activez le service OCR.

Si vous n’utilisez pas de file d’attente des travaux, ou si vous souhaitez recevoir un document OCR finalisé avant l’échéance indiquée par la file d’attente des travaux, vous pouvez choisir l’action **Recevoir du service OCR**. Cette option vous permettra d’obtenir tous les documents finalisés par le service OCR.

> [!NOTE]  
> Si le service OCR est configuré de telle façon qu’une vérification manuelle des documents traités est exigée, le champ **Statut OCR** affichera donc **En attente de vérification**. Dans ce cas, procédez comme suit pour vous connecter au site Web du service OCR et vérifier manuellement un document OCR.

1. Dans le champ **Statut OCR**, sélectionnez le lien hypertexte **En attente de vérification**.
2. Sur le site Web du service OCR, connectez-vous à l’aide des identifiants de votre compte de service OCR. Pour plus d’informations, reportez-vous à [Configurer un service OCR](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

   Les informations concernant le document OCR sont affichées, vous présentant à la fois le contenu source du fichier PDF ou image ainsi que les valeurs de champ OCR correspondantes.
3. Examinez les valeurs de champ et modifiez ou saisissez des valeurs dans les champs identifiés comme à vérifier par le service OCR.
4. Cliquez sur le bouton **OK**. Le processus OCR est terminé et le document électronique résultant est envoyé à la page **Documents entrants** dans [!INCLUDE[prod_short](includes/prod_short.md)], selon l’échéance de la file d’attente des travaux.
5. Répétez les étapes 2 à 4 pour tout autre document OCR à vérifier.

Désormais, vous pouvez poursuivre la création d’enregistrements de documents pour les documents électroniques reçus dans [!INCLUDE[prod_short](includes/prod_short.md)], manuellement ou automatiquement. Pour plus d’informations, voir la procédure suivante. Vous pouvez également [connecter le nouvel enregistrement de document entrant à des documents validés ou non validés existants](across-how-connect-disconnect-income-document-records.md) afin que le fichier source soit facilement accessible dans [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a><a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Pour créer une facture achat à partir d’un document électronique réceptionné depuis le service OCR

La procédure suivante décrit comment créer un enregistrement facture achat à partir d’une facture fournisseur reçue en pièce jointe provenant du service OCR. La procédure est identique lorsque vous créez, par exemple, une ligne feuille comptabilité à partir d’un justificatif de frais ou un retour vente d’un client.

> [!NOTE]  
> Les champs **Description** et **N°** des lignes document créées ne seront pas complétées tant que vous n’aurez pas mappé tout d’abord le texte trouvé sur le document OCR avec les deux champs dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous pouvez effectuer ce mappage en tant que références article, pour les lignes document de type Article. Pour plus d’informations, voir [Utiliser les références article](inventory-how-use-item-cross-refs.md). Vous pouvez également utiliser la fonction **Mappage de texte à compte**. Pour plus d’informations, reportez-vous à [Mapper du texte sur un document entrant à un fournisseur, une comptabilité ou un compte bancaire spécifique](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Sélectionnez la ligne du document entrant, puis sélectionnez l’action **Créer document**.

Une facture achat sera créée dans [!INCLUDE[prod_short](includes/prod_short.md)] selon les informations disponibles sur le document électronique du fournisseur provenant du service OCR. Ces informations sont insérées dans la nouvelle facture achat en fonction du mappage que vous avez défini comme référence ou sous forme de mappage de texte à compte.

Les erreurs de validation, généralement associées à des données erronées ou manquantes dans [!INCLUDE[prod_short](includes/prod_short.md)], seront affichées sur le raccourci **Erreurs et avertissements**. Pour plus d’informations, voir [Gérer des erreurs lors de la réception de documents électroniques](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### <a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a><a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a>Pour associer du texte sur un document entrant à un compte fournisseur spécifique

Pour les documents entrants, vous utilisez généralement l’action **Mapper le texte avec le compte** pour définir qu’un certain texte sur une facture fournisseur en provenance du service OCR est mappé avec un certain compte fournisseur. À l’avenir, toute partie de la description du document entrant qui existe en tant que texte de mappage signifie que le champ **Numéro de fournisseur** sur le document résultant ou les lignes feuille de type *Compte général* sont remplis avec le fournisseur en question.

Outre le mappage avec un compte fournisseur ou des comptes généraux, vous pouvez également effectuer un mappage de texte sur un compte bancaire. Cette option est utile, par exemple, pour les documents électroniques des dépenses qui sont déjà payées, et pour lesquelles vous souhaitez créer une ligne feuille comptabilité qui est prête à être validée sur un compte bancaire.

1. Sélectionnez la ligne document entrant appropriée, puis choisissez l’action **Mapper le texte avec le compte**. La page **Mappage de texte à compte** s’affiche.
2. Dans le champ **Texte de mappage**, saisissez le texte affiché sur les factures fournisseur pour lesquelles vous souhaitez créer des documents achat ou des lignes feuille. Vous pouvez entrer jusqu’à 50 caractères.
3. Dans le champ **N° fournisseur**, entrez le fournisseur pour lequel le document achat ou la ligne feuille sera créée.
4. Dans le champ **N° cpte débit**, entrez le compte général de type débit qui sera inséré sur le document achat ou la ligne feuille qui en résulte de type Compte général.
5. Dans le champ **N° cpte crédit**, entrez le compte général de type crédit qui sera inséré sur le document achat ou la ligne feuille qui en résulte de type Compte général.

   > [!NOTE]
   > N’utilisez pas **Type origine solde** et les champs **N° origine solde** en relation avec les documents entrants. Ils sont utilisés à des fins de rapprochement de paiement automatique uniquement. Pour plus d’informations, reportez-vous à [Mapper du texte sur les paiements récurrents aux comptes pour un rapprochement automatique](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).
6. Répétez les étapes 2 à 5 pour tout le texte des documents entrants pour lesquels vous souhaitez créer automatiquement des documents.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a><a name="to-handle-errors-when-receiving-electronic-documents"></a>Gérer les erreurs lors de la réception de documents électroniques

1. Sur la page **Documents entrants**, sélectionnez la ligne pour un document électronique en provenance du service OCR et contenant des erreurs, indiquées par la valeur *Erreur* dans le champ **Statut OCR**.
2. Sélectionnez l’option **Modifier** pour ouvrir la page **Document entrant**.
3. Sur le raccourci **Erreurs et avertissements**, sélectionnez le message, puis choisissez l’action **Ouvrir l’enregistrement associé**.
4. La page contenant les données erronées ou manquantes, comme une fiche fournisseur avec la valeur champ manquant, s’ouvre.
5. Corrigez l’erreur ou les erreurs en suivant les instructions de chaque message d’erreur.
6. Traitez maintenant le document électronique entrant en cliquant à nouveau sur le bouton **Créer manuellement**.
7. Répétez les étapes 5 et 6 pour toute erreur restante jusqu’à ce que le document électronique puisse être envoyé avec succès.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a><a name="to-train-the-ocr-service-to-avoid-errors"></a>Pour former le service OCR à éviter les erreurs

Comme le service OCR est basé sur la reconnaissance optique, il peut interpréter de manière incorrecte les caractères des fichiers PDF ou image lorsqu’il traite pour la première fois les documents d’un certain fournisseur, par exemple. Il peut ne pas interpréter le logo de la société comme le nom du fournisseur, ou il peut mal interpréter le montant total sur un reçu de dépenses en raison de sa disposition. Pour éviter que ces erreurs se propagent, vous pouvez corriger les données reçues par le service OCR et envoyer les commentaires au service.

La page **Correction des données OCR**, que vous ouvrez à partir de la page **Document entrant**, affiche les champs du raccourci **Informations financières** dans deux colonnes, une avec les données OCR modifiables et une avec les données OCR en lecture seule. Lorsque vous sélectionnez le bouton **Envoyer des commentaires OCR**, le contenu de la page **Correction des données OCR** est envoyé au service OCR. La prochaine fois que le service traite les fichiers PDF ou image contenant les données en question, vos corrections seront intégrées pour améliorer la reconnaissance de document.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Documents entrants**, puis choisissez le lien associé.
2. Ouvrez un enregistrement de document entrant contenant les données reçues du service OCR que vous souhaitez corriger.
3. Sur la page **Document entrant**, sélectionnez l’action **Corriger les données OCR**.
4. Sur la page **Correction des données OCR**, remplacez les données de la colonne modifiable pour chaque champ dont la valeur est incorrecte.
5. Pour annuler les corrections effectuées depuis l’ouverture de la page **Correction des données OCR**, sélectionnez l’action **Réinitialiser les données OCR**.
6. Pour envoyer les corrections au service OCR, sélectionnez l’action **Envoyer des commentaires OCR**.
7. Pour enregistrer les corrections, fermez la page **Correction des données OCR**.

Les champs du raccourci **Informations financières** de la page **Document entrant** sont mis à jour avec les nouvelles valeurs que vous avez entrées à l’étape 4.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/incoming-documents-dynamics-365-business-central/) associée

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Créer des enregistrements document entrant](across-how-create-income-document-records.md)
[Créer des enregistrements document entrant directement à partir de documents et d’écritures](across-how-connect-disconnect-income-document-records.md)
[Documents entrants](across-income-documents.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
