---
title: Utilisation de Business Central avec Outlook
description: 'Ce service bénéficie d’une intégration complète à Microsoft 365, ce qui vous permet de gérer tous vos interactions et messages d’affaires avec les clients et les fournisseurs directement dans Outlook.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, mail, Microsoft 365'
ms.date: 04/21/2022
ms.author: jswymer
---
# <a name="use-business-central-as-your-business-inbox-in-outlook" />Utiliser Business Central en tant que boîte de réception professionnelle dans Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] offre un complément qui vous aide à gérer les interactions commerciales avec vos clients et fournisseurs, directement dans Microsoft Outlook. Avec le complément [!INCLUDE[prod_short](includes/prod_short.md)] pour Outlook, vous pouvez afficher des informations financières associées à des clients et des fournisseurs, ainsi que créer et envoyer des documents financiers, comme des devis et des factures.

Le complément [!INCLUDE[prod_short](includes/prod_short.md)] se compose de deux compléments distincts qui offrent les fonctionnalités suivantes :

- Panorama des contacts

   Ce complément vous permet d’examiner des informations [!INCLUDE[prod_short](includes/prod_short.md)] sur le client ou le fournisseur dans les e-mails Outlook et les rendez-vous du calendrier. Il vous permet également de créer et d’envoyer des documents professionnels [!INCLUDE[prod_short](includes/prod_short.md)], tels que devis et factures, à un contact.

- Affichage de document

   Lorsqu’un document commercial est envoyé dans un e-mail, le complément fournit un lien direct vers le document commercial réel dans [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="get-started" />Démarrer

1. La première chose à faire est d’installer le complément [!INCLUDE[prod_short](includes/prod_short.md)] dans Outlook. Votre administrateur a peut-être déjà installé le complément pour vous. Donc, si vous n’êtes pas sûr, vérifiez auprès de votre administrateur ou passez à l’étape suivante pour vérifier s’il est installé.

    Si le complément n’a pas été installé pour vous, consultez [Installer le complément pour votre propre usage](admin-outlook.md#install). 

2. Une fois le complément installé, vous pouvez accéder au complément **[!INCLUDE[prod_short](includes/prod_short.md)]** depuis n’importe quel message électronique ou rendez-vous de calendrier nouveau ou existant dans Outlook.

    Commencez par vous connecter à Outlook et ouvrir un message électronique. Ensuite, si vous utilisez l’application Outlook, accédez au ruban et recherchez **[!INCLUDE[prod_short](includes/prod_short.md)]**.  Ou si vous utilisez Outlook sur le Web, en haut ou en bas du message électronique, recherchez ![l’icône du complément Business Central dans Outlook.](media/outlook-business-central-icon.png) ou accédez aux autres actions ![Afficher d’autres actions pour un e-mail dans Outlook.](media/outlook-more-actions-button.png) .

    ![Accédez aux compléments Business Central dans Outlook.](media/outlook-business-central-addin.png)

   Si vous avez installé le complément par vous-même et que vous avez choisi de recevoir un exemple d’e-mail, consultez votre boîte de réception pour trouver l’e-mail de bienvenue. Cet e-mail fournit des informations pour vous aider à démarrer.

La première fois que vous utiliserez le complément, dans le volet de compléments de [!INCLUDE[prod_short](includes/prod_short.md)], vous serez peut-être invité à vous connecter. Dans ce cas, sélectionnez **Se connecter maintenant** et suivez les instructions à l’écran pour vous connecter à Business Central à l’aide de votre compte.

> [!TIP]
> Si vous utilisez le nouvel Outlook sur le Web, vous pouvez épingler **[!INCLUDE[prod_short](includes/prod_short.md)]** de sorte qu’il soit toujours immédiatement visible au lieu d’avoir à accéder au bouton Autres actions ; cela facilite la visualisation des informations sur les contacts pendant que vous naviguez entre différents e-mails.

Pour plus d’informations, voir [Utiliser des compléments dans Outlook sur le Web](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

## <a name="work-with-contacts-and-documents-using-the-contact-insights-add-in" />Utilisation de contacts et de documents à l’aide du complément Contact Insights

Imaginons que vous receviez un e-mail d’un client souhaitant obtenir un devis pour certains articles. Directement dans Outlook, vous pouvez ouvrir le complément [!INCLUDE[prod_short](includes/prod_short.md)], qui identifie l’expéditeur comme un client, et ouvre la fiche client de cette société. À partir de ce tableau de bord, vous pouvez afficher des informations générales relatives au client et rechercher davantage de détails dans des documents spécifiques. Vous pouvez également effectuer des recherches approfondies dans l’historique des ventes du client. S’il s’agit d’un nouveau contact, vous pouvez le créer en tant que tel dans [!INCLUDE[prod_short](includes/prod_short.md)] sans quitter Outlook.  

Dans le complément, vous pouvez créer un devis et l’envoyer à ce client sans quitter Outlook. Toutes les informations dont vous avez besoin pour envoyer le devis sont disponibles dans votre boîte de réception professionnelle dans Outlook. Une fois les données saisies, vous pouvez valider le devis et l’envoyer par e-mail. [!INCLUDE[prod_short](includes/prod_short.md)] génère un fichier .PDF avec le devis et le joint au message électronique que vous rédigez dans le complément.  

De même, si vous recevez un e-mail d’un fournisseur, vous pouvez utiliser le complément pour travailler avec les fournisseurs et les factures achat.  

Il arrive parfois que vous souhaitiez visualiser davantage de champs que ceux qui s’affichent dans le complément, par exemple si vous souhaitez renseigner des lignes dans une facture. Afin de vous bénéficier d’un espace de travail plus important, vous pouvez ouvrir le complément sur une page distincte. Il s’agit toujours d’Outlook, mais vous disposez de davantage d’espace. Au fur et à mesure que vous saisissez des données pour le document dans l’affichage contextuel, les modifications sont automatiquement enregistrées. Les sections suivantes vous guident à travers certaines tâches de base pour vous donner une compréhension générale de son utilisation.

> [!TIP]
> Les tâches expliquent comment utiliser le complément à partir d’un e-mail. Mais vous pouvez faire la même chose à partir d’un rendez-vous du calendrier dans Outlook.

### <a name="look-up-a-business-contact-when-composing-an-email" />Rechercher un contact professionnel lors de la rédaction d’un e-mail

1. Créez un nouveau message électronique.
2. Dans le ruban, accédez à **[!INCLUDE[prod_short](includes/prod_short.md)]** et sélectionnez **Contact Insights**. Ou si vous utilisez Outlook sur le Web, allez au bas du message et sélectionnez ![l’icône du complément Business Central dans Outlook.](media/outlook-business-central-icon.png) > **Contact Insights**.
3. Dans le volet de complément **[!INCLUDE[prod_short](includes/prod_short.md)]** qui s’ouvre, recherchez et choisissez le contact souhaité.

    Un aperçu du contact s’affiche dans le volet et le contact est ajouté dans la ligne **À** de l’e-mail.

### <a name="view-and-change-the-contact-details-or-switch-company" />Afficher et modifier les coordonnées ou changer de société

La barre d’action en haut du volet de compléments [!INCLUDE[prod_short](includes/prod_short.md)] comprend plusieurs actions qui vous permettent d’approfondir les détails du contact et de changer des choses.

![Barre d’action du complément Business Central dans Outlook.](media/outlook-addin-action-bar.png)

Par exemple, vous pouvez ouvrir les coordonnées complètes telles que vous les verriez dans [!INCLUDE[prod_short](includes/prod_short.md)]. Si vous travaillez avec plus d’une entreprise [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez facilement basculer d’une entreprise à l’autre.

### <a name="track-incoming-documents" />Suivi des documents entrants

Peut-être que vous utilisez la liste **Documents entrants** dans [!INCLUDE[prod_short](includes/prod_short.md)] pour suivre les documents à traiter que les fournisseurs vous envoient, tels qu’une facture d’achat à payer. Si vous le faites, vous pouvez facilement créer des enregistrements de documents entrants à partir du complément Outlook et inclure les pièces jointes des e-mails.

1. Lorsque vous recevez un e-mail d’un fournisseur avec une pièce jointe, sélectionnez ![l’icône du complément Business Central dans Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Contact Insights**.  

2. Dans la barre d’action du complément, choisissez **Afficher d’autres actions**, puis sélectionnez **Envoyer dans les documents entrants…** .  

### <a name="create-and-send-new-document-to-a-contact" />Créer et envoyer un nouveau document à un contact

1. Dans le ruban ou en bas de l’e-mail, sélectionnez ![l’icône du complément Business Central dans Outlook](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Nouveau**, puis choisissez le type de document que vous souhaitez créer, par exemple **Devis**.
2. Modifiez le document dans le volet de complément **[!INCLUDE[prod_short](includes/prod_short.md)]**.
3. Lorsque le document est prêt à être envoyé au contact, dans la barre d’action, choisissez **Afficher d’autres actions**, puis sélectionnez l’action **Envoyer par e-mail**.

### <a name="attach-files-to-records" />Joindre des fichiers aux enregistrements

Votre boîte de réception sert souvent de source de fichiers entrants qui lancent ou débloquent des workflows. Les fichiers peuvent inclure des éléments tels que des paiements de facture en PDF, des photos de marchandises ou des exigences dans un document Word. Lorsque vous travaillez dans Outlook avec des enregistrements Business Central tels que des fournisseurs, des clients, des factures d’achat ou des bons de commande, vous pouvez joindre ces fichiers aux enregistrements.

Il existe plusieurs façons de joindre des fichiers. Une façon consiste à télécharger des fichiers depuis votre appareil. L’autre méthode consiste à télécharger des fichiers joints à un e-mail. Par exemple, supposons que vous receviez un e-mail contenant des fichiers d’un contact. Le complément affichera automatiquement l’enregistrement de contact qui correspond à l’expéditeur de l’e-mail. À partir de là, vous pouvez accéder à un document pour le contact, comme la dernière commande client. Une fois que vous avez identifié la commande à laquelle l’e-mail se rapporte, vous devez télécharger rapidement les fichiers de l’e-mail vers cette commande.

![Cette vidéo montre comment ajouter des pièces jointes d’un e-mail à des enregistrements dans Business Central.](media/outlook-attach-files.png)

Après avoir joint un fichier, vos collègues peuvent instantanément télécharger et afficher le fichier à partir du récapitulatif **Pièces jointes** dans n’importe lequel de leurs clients Business Central. Ou, ils peuvent ouvrir le fichier dans OneDrive pour partager et collaborer avec leur département.

#### <a name="how-to-attach-a-file" />Comment joindre un fichier

1. Ouvrez l’e-mail, choisissez l’![Icône du complément Business Central dans Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Contact Insights**.
2. Dans la barre d’action du complément, choisissez **Afficher d’autres actions** > **Pièces jointes**.

    La page **Documents joints** s’ouvre pour répertorier tous les documents déjà joints à l’enregistrement.
3. Choisissez **Fichiers joints...**, puis choisissez l’une des options suivantes :

   - Choisissez **Joindre à partir du courrier** pour télécharger tous les fichiers ou une sélection de fichiers joints à l’e-mail.
   - Choisissez **Télécharger à partir du fichier** pour télécharger un ou plusieurs fichiers depuis votre appareil.

> [!NOTE]
> Vous ne pouvez pas joindre de fichiers à tous les enregistrements. Cette fonction est disponible pour les enregistrements qui utilisent le récapitulatif **Pièces jointes**, tel qu’un fournisseur, un client, une facture d’achat ou une commande client.

## <a name="view-a-document-from-an-email-using-the-document-view-add-in" />Afficher un document à partir d’un e-mail à l’aide du complément Affichage de document

Qu’il s’agisse d’un e-mail que vous avez envoyé ou reçu, vous pouvez afficher n’importe quel document [!INCLUDE[prod_short](includes/prod_short.md)], tel qu’un devis, directement dans Outlook. À partir de là, vous pouvez apporter des modifications et accéder aux informations associées&mdash;tout comme vous le feriez à l’intérieur de [!INCLUDE[prod_short](includes/prod_short.md)].

Si vous utilisez l’application Outlook, sélectionnez simplement le **Lien vers le document** en haut du message électronique. Pour Outlook sur le Web, recherchez le lien de référence du document dans le message électronique. Le texte du lien de référence inclura le numéro du document, qui est basé sur la souche de numéros utilisée dans [!INCLUDE[prod_short](includes/prod_short.md)]. Par exemple, le lien vers un devis serait quelque chose comme **Devis S-QUO1000**.  

> [!TIP]
> À partir la 1re vague de lancement 2022, les documents s’ouvrent dans une nouvelle fenêtre de navigateur avec toutes les fonctionnalités que vous connaissez de [!INCLUDE [prod_short](includes/prod_short.md)]. Vous pouvez naviguer d’un document à une liste et inversement, ouvrir des listes dans Excel, envoyer des documents à imprimer et exécuter ou prévisualiser des états associés. Vous disposez également de tous les raccourcis clavier familiers lorsque vous ouvrez des documents à partir d’Outlook.  


## <a name="see-related-microsoft-trainingtrainingmodulesalternative-interfaces-dynamics-365-business-centralindex" />Voir la [formation Microsoft](/training/modules/alternative-interfaces-dynamics-365-business-central/index) associée

## <a name="see-also" />Voir aussi

[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Obtention de Business Central sur mon périphérique mobile](install-mobile-app.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Finances](finance.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Configuration minimale requise pour Outlook](product-requirements.md#outlook)  
[Utiliser des compléments dans Outlook sur le Web](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
