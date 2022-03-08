---
title: Utilisation de Business Central avec Outlook | Microsoft Docs
description: Ce service bénéficie d’une intégration complète à Microsoft 365, ce qui vous permet de gérer tous vos interactions et messages d’affaires avec les clients et les fournisseurs directement dans Outlook.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 08/13/2021
ms.author: jswymer
ms.openlocfilehash: 5de1ae4dc96419d848103a8b4ea9e11113793242
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589702"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Utilisation de Business Central en tant que boîte de réception professionnelle dans Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] offre un complément qui vous aide à gérer les interactions commerciales avec vos clients et fournisseurs, directement dans Microsoft Outlook. Avec le complément [!INCLUDE[prod_short](includes/prod_short.md)] pour Outlook, vous pouvez afficher des informations financières associées à des clients et des fournisseurs, ainsi que créer et envoyer des documents financiers, comme des devis et des factures.

Le complément [!INCLUDE[prod_short](includes/prod_short.md)] se compose de deux compléments distincts qui offrent les fonctionnalités suivantes :

- Panorama des contacts

   Ce complément vous permet d’examiner des informations [!INCLUDE[prod_short](includes/prod_short.md)] sur le client ou le fournisseur dans les e-mails Outlook et les rendez-vous du calendrier. Il vous permet également de créer et d’envoyer des documents professionnels [!INCLUDE[prod_short](includes/prod_short.md)], tels que devis et factures, à un contact.

- Affichage de document

   Lorsqu’un document commercial est envoyé dans un e-mail, le complément fournit un lien direct vers le document commercial réel dans [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="get-started"></a>Démarrer

1. La première chose à faire est d’installer le complément [!INCLUDE[prod_short](includes/prod_short.md)] dans Outlook. Votre administrateur a peut-être déjà installé le complément pour vous. Donc, si vous n’êtes pas sûr, vérifiez auprès de votre administrateur ou passez à l’étape suivante pour vérifier s’il est installé.

    Si le complément n’a pas été installé pour vous, consultez [Installer le complément pour votre propre usage](admin-outlook.md#install). 

2. Une fois le complément installé, vous pouvez accéder au complément **[!INCLUDE[prod_short](includes/prod_short.md)]** depuis n’importe quel message électronique ou rendez-vous de calendrier nouveau ou existant dans Outlook.

    Commencez par vous connecter à Outlook et ouvrir un message électronique. Ensuite, si vous utilisez l’application Outlook, accédez au ruban et recherchez **[!INCLUDE[prod_short](includes/prod_short.md)]**.  Ou si vous utilisez Outlook sur le Web, en haut ou en bas du message électronique, recherchez ![l’icône du complément Business Central dans Outlook.](media/outlook-business-central-icon.png) ou accédez aux autres actions ![Afficher d’autres actions pour un e-mail dans Outlook.](media/outlook-more-actions-button.png) .

    ![Accédez aux compléments Business Central dans Outlook.](media/outlook-business-central-addin.png)

   Si vous avez installé le complément par vous-même et que vous avez choisi de recevoir un exemple d’e-mail, consultez votre boîte de réception pour trouver l’e-mail de bienvenue. Cet e-mail fournit des informations pour vous aider à démarrer.

La première fois que vous utiliserez le complément, dans le volet de compléments de [!INCLUDE[prod_short](includes/prod_short.md)], vous serez peut-être invité à vous connecter. Dans ce cas, sélectionnez **Se connecter maintenant** et suivez les instructions à l’écran pour vous connecter à Business Central à l’aide de votre compte.

> [!TIP]
> Si vous utilisez le nouvel Outlook sur le Web, vous pouvez épingler **[!INCLUDE[prod_short](includes/prod_short.md)]** de sorte qu’il soit toujours immédiatement visible au lieu d’avoir à accéder au bouton Autres actions ; cela facilite la visualisation des informations sur les contacts pendant que vous naviguez entre différents e-mails.

Pour plus d’informations, voir [Utilisation des compléments dans Outlook sur le Web](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

## <a name="work-with-contacts-and-documents-using-the-contact-insights-add-in"></a>Utilisation de contacts et de documents à l’aide du complément Contact Insights

Imaginons que vous receviez un e-mail d’un client souhaitant obtenir un devis pour certains articles. Directement dans Outlook, vous pouvez ouvrir le complément [!INCLUDE[prod_short](includes/prod_short.md)], qui identifie l’expéditeur comme un client, et ouvre la fiche client de cette société. À partir de ce tableau de bord, vous pouvez afficher des informations générales relatives au client, ainsi que rechercher davantage de détails dans des documents spécifiques. Vous pouvez également effectuer des recherches approfondies dans l’historique des ventes du client. S’il s’agit d’un nouveau contact, vous pouvez le créer en tant que tel dans [!INCLUDE[prod_short](includes/prod_short.md)] sans quitter Outlook.  

Dans le complément, vous pouvez créer un devis et l’envoyer à ce client sans quitter Outlook. Toutes les informations dont vous avez besoin pour envoyer le devis sont disponibles dans votre boîte de réception professionnelle dans Outlook. Une fois les données saisies, vous pouvez valider le devis et l’envoyer par e-mail. [!INCLUDE[prod_short](includes/prod_short.md)] génère un fichier .PDF avec le devis et le joint au message électronique que vous rédigez dans le complément.  

De même, si vous recevez un e-mail d’un fournisseur, vous pouvez utiliser le complément pour travailler avec les fournisseurs et les factures achat.  

Il arrive parfois que vous souhaitiez visualiser davantage de champs que ceux qui s’affichent dans le complément, par exemple si vous souhaitez renseigner des lignes dans une facture. Afin de vous bénéficier d’un espace de travail plus important, vous pouvez ouvrir le complément sur une page distincte. Il s’agit toujours d’Outlook, mais vous disposez de davantage d’espace. Au fur et à mesure que vous saisissez des données pour le document dans l’affichage contextuel, les modifications sont automatiquement enregistrées. Les sections suivantes vous guident à travers certaines tâches de base pour vous donner une compréhension générale de son utilisation.

> [!TIP]
> Les tâches expliquent comment utiliser le complément à partir d’un e-mail. Mais vous pouvez faire la même chose à partir d’un rendez-vous du calendrier dans Outlook.

### <a name="look-up-a-business-contact-when-composing-an-email"></a>Rechercher un contact professionnel lors de la rédaction d’un e-mail

1. Créez un nouveau message électronique.
2. Dans le ruban, accédez à **[!INCLUDE[prod_short](includes/prod_short.md)]** et sélectionnez **Contact Insights**. Ou si vous utilisez Outlook sur le Web, allez au bas du message et sélectionnez ![l’icône du complément Business Central dans Outlook.](media/outlook-business-central-icon.png) > **Contact Insights**.
3. Dans le volet de complément **[!INCLUDE[prod_short](includes/prod_short.md)]** qui s’ouvre, recherchez et choisissez le contact souhaité.

    Un aperçu du contact s’affiche dans le volet et le contact est ajouté dans la ligne **À** de l’e-mail.

### <a name="view-and-change-the-contact-details-or-switch-company"></a>Afficher et modifier les coordonnées ou changer de société

La barre d’action en haut du volet de compléments [!INCLUDE[prod_short](includes/prod_short.md)] comprend plusieurs actions qui vous permettent d’approfondir les détails du contact et de changer des choses.

![Barre d’action du complément Business Central dans Outlook.](media/outlook-addin-action-bar.png)

Par exemple, vous pouvez ouvrir les coordonnées complètes telles que vous les verriez dans [!INCLUDE[prod_short](includes/prod_short.md)]. Si vous travaillez avec plus d’une entreprise [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez facilement basculer d’une entreprise à l’autre.

### <a name="track-incoming-documents"></a>Suivi des documents entrants 

Peut-être que vous utilisez la liste **Documents entrants** dans [!INCLUDE[prod_short](includes/prod_short.md)] pour suivre les documents à traiter que les fournisseurs vous envoient, tels qu’une facture d’achat à payer. Si vous le faites, vous pouvez facilement créer des enregistrements de documents entrants à partir du complément Outlook et inclure les pièces jointes des e-mails.

1. Lorsque vous recevez un e-mail d’un fournisseur avec une pièce jointe, sélectionnez ![l’icône du complément Business Central dans Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Contact Insights**. 

2. Dans la barre d’action du complément, choisissez **Afficher d’autres actions**, puis sélectionnez **Envoyer dans les documents entrants…**. 

### <a name="create-and-send-new-document-to-a-contact"></a>Créer et envoyer un nouveau document à un contact

1. Dans le ruban ou en bas de l’e-mail, sélectionnez ![l’icône du complément Business Central dans Outlook](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Nouveau**, puis choisissez le type de document que vous souhaitez créer, par exemple **Devis**.
2. Modifiez le document dans le volet de complément **[!INCLUDE[prod_short](includes/prod_short.md)]**.
3. Lorsque le document est prêt à être envoyé au contact, dans la barre d’action, choisissez **Afficher d’autres actions**, puis sélectionnez l’action **Envoyer par e-mail**.

## <a name="view-a-document-from-an-email-using-the-document-view-add-in"></a>Afficher un document à partir d’un e-mail à l’aide du complément Affichage de document

Qu’il s’agisse d’un e-mail que vous avez envoyé ou reçu, vous pouvez afficher n’importe quel document [!INCLUDE[prod_short](includes/prod_short.md)], tel qu’un devis, directement dans Outlook. À partir de là, vous pouvez apporter des modifications et accéder aux informations associées&mdash;tout comme vous le feriez à l’intérieur de [!INCLUDE[prod_short](includes/prod_short.md)].

Si vous utilisez l’application Outlook, sélectionnez simplement le **Lien vers le document** en haut du message électronique. Pour Outlook sur le Web, recherchez le lien de référence du document dans le message électronique. Le texte du lien de référence inclura le numéro du document, qui est basé sur la souche de numéros utilisée dans [!INCLUDE[prod_short](includes/prod_short.md)]. Par exemple, le lien vers un devis serait quelque chose comme **Devis S-QUO1000**.

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Obtention de Business Central sur mon périphérique mobile](install-mobile-app.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Finances](finance.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Configuration minimale requise pour Outlook](product-requirements.md#outlook)  
[Utilisation des compléments dans Outlook sur le Web](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]