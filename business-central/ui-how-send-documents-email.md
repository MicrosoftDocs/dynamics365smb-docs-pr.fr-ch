---
title: Paramétrer du contenu d'e-mail spécifique au document | Microsoft Docs
description: Vous pouvez définir le contenu à insérer dans le corps de l'e-mail, par exemple, un lien Paypal. Vous pouvez également joindre des documents aux e-mails.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, cover, body, PayPal, layout
ms.date: 05/13/2020
ms.author: edupont
ms.openlocfilehash: d80b76614ad0ddf901a288859d8e6595d908c7ae
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528000"
---
# <a name="send-documents-by-email"></a>Envoyer des documents par e-mail

Pour communiquer le contenu des documents commerciaux rapidement à vos partenaires commerciaux, par exemple les informations paiement sur les documents vente aux clients, vous pouvez utiliser la fonctionnalité de présentation des états pour définir le contenu spécifique aux documents qui est automatiquement inséré au corps du message. Pour plus d'informations, voir [Gestion des présentations de rapport et de document](ui-manage-report-layouts.md).

Pour activer les emails au sein de [!INCLUDE[d365fin](includes/d365fin_md.md)], démarrez le guide de configuration assistée **Configurer la messagerie** sur le tableau de bord.

Vous pouvez envoyer en pièce jointe à des e-mails virtuellement tous les types de documents directement à partir de la page qui affiche le document. Outre la pièce jointe, vous pouvez configurer des corps de message spécifique à des documents, avec des informations de base du document précédées d'un texte standard de salutations au destinataire du message et de présentation du document en question. Pour proposer à vos clients de payer les ventes par voie électronique à l'aide d'un service de paiement, comme Paypal par exemple, vous pouvez insérer les informations et le lien hypertexte Paypal dans le corps du message.

À partir de tous les documents pris en charge, vous initiez l'envoi d'e-mails en sélectionnant l'action **Envoyer** sur les documents validés, ou l'action **Valider et envoyer** sur les documents non validés.

Si le champ **E-mail** sur la page **Envoyer le document à** est défini sur **Oui (Afficher une invite pour le réglage des paramètres)**, la page **Envoyer e-mail** s'affiche. Le champ **À :** est prérempli avec le contact et le document est en pièce jointe sous forme de fichier PDF. Dans le champ **Corps**, vous pouvez saisir un texte manuellement ou faire en sorte que le champ contienne un corps de message spécifique au document que vous avez configuré.

La procédure suivante décrit comment définir l'état **Ventes : Facture** à utiliser pour les corps de message spécifiques à un document lorsque vous envoyez par e-mail des factures vente validées.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Pour configurer corps de message spécifique à un document pour les factures vente

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Sélection des états - Ventes**, puis sélectionnez le lien associé.
2. Sur la page **Sélection des états : Ventes**, dans le champ **Utilisation**, sélectionnez **Facture**
3. Sur une nouvelle ligne, dans le champ **ID état**, sélectionnez, par exemple, l'état standard 1306.
4. Cochez la case **Utiliser pour le corps du message e-mail**.
5. Choisissez le champ **Code présentation du corps du message e-mail** et sélectionnez une présentation dans la liste déroulante.

    Les présentations d'état définissent à la fois le style et le contenu du corps de message, y compris le texte standard qui précède les informations de base relatives au document dans le corps du message. Vous pouvez visualiser toutes les présentations d'état disponibles si vous choisissez le bouton **Sélectionner dans la liste complète** dans la liste déroulante.
6. Pour afficher ou modifier la présentation sur laquelle le corps du message est basé, sélectionnez la présentation sur la page **Présentations état personnalisées**, puis cliquez sur **Modifier présentation**.
7. Si vous souhaitez proposer à vos clients de payer les ventes par voie électronique, vous pouvez configurer le service de paiement associé, comme Paypal par exemple, puis insérer également les informations et le lien hypertexte Paypal dans le corps du message. Pour plus d'informations, voir [Activer les paiements client via Paypal](sales-how-enable-payment-service-extensions.md).
8. Choisissez le bouton **OK**.

Désormais, lorsque vous sélectionnez, par exemple, l'action **Envoyer** sur la page **Facture vente enregistrée**, le corps du message comporte les informations de document de l'état 1306 précédé d'un texte standard auquel sont appliqués des attributs de style en fonction de la présentation d'état que vous avez sélectionnée à l'étape 5.

La procédure suivante décrit comment envoyer une facture vente validée en tant que message e-mail avec le document en pièce jointe sous forme de fichier PDF et avec un corps de message spécifique au document.

## <a name="to-send-documents-by-email"></a>Pour envoyer des documents par e-mail

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures vente enregistrées**, puis sélectionnez le lien associé.
2. Sélectionnez la facture vente validée appropriée, puis cliquez sur **Envoyer**. La page **Envoyer le document à** s'affiche.
3. Dans le champ **E-mail**, sélectionnez **Oui (Afficher une invite pour le réglage des paramètres)**. Pour plus d'informations, reportez vous à [Configurer des profils d'envoi de documents](sales-how-setup-document-send-profiles.md).
4. Choisissez le bouton **OK**. La page **Envoyer e-mail** s'affiche.
5. Dans le champ **À :**, entrez une adresse e-mail valide. La valeur par défaut est l'adresse e-mail du client.
6. Dans le champ **Objet**, saisissez un texte descriptif de l'objet. La valeur par défaut est le nom du client et le numéro de facture.
7. Dans le champ **Document joint**, la facture générée est jointe par défaut en tant que fichier PDF.
8. Dans le champ **Corps**, entrez un message court au destinataire.

    Si le corps d'un message spécifique à un document est configuré sur la page **Sélection des états : Ventes**, le champ **Corps** est renseigné automatiquement. Pour plus d'informations, voir [Pour configurer corps de message spécifique à un document pour les factures vente](ui-how-send-documents-email.md#to-set-up-a-document-specific-email-body-for-sales-invoices).
9. Cliquez sur le bouton **OK** pour envoyer l'e-mail.

> [!NOTE]  
> Si vous ne souhaitez pas spécifier les paramètres d'e-mail à chaque fois que vous envoyez un document par e-mail, vous pouvez sélectionner l'option **Oui (Utiliser les paramètres par défaut)** dans le champ **E-mail** de la page **Envoyer le document à**. Dans ce cas, la page **Envoyer e-mail** ne s'affiche pas. Reportez-vous à l'étape 4. Pour plus d'informations, reportez vous à [Configurer des profils d'envoi de documents](sales-how-setup-document-send-profiles.md).  

## <a name="documents-marked-as-printed-when-they-are-sent"></a>Documents marqués comme imprimés lors de leur envoi

Certains documents dans [!INCLUDE[prodshort](includes/prodshort.md)] comportent un champ qui spécifie la fréquence d'impression du document. Le champ est également mis à jour si vous n'imprimez pas le document mais l'envoyez par e-mail à la place. Le champ est même mis à jour si vous n'envoyez pas réellement le document, par exemple lorsque votre organisation n'a pas configuré de messagerie électronique, ou lorsque le contact auquel vous souhaitez envoyer le document n'a pas d'adresse e-mail répertoriée. Dans tous les scénarios, en ce qui concerne [!INCLUDE[prodshort](includes/prodshort.md)], le document est imprimé car un fichier PDF est généré.  

L'utilisateur peut ne pas voir ce fichier généré, mais c'est la raison pour laquelle le champ est mis à jour.

## <a name="see-also"></a>Voir aussi

[Gestion des présentations d'état et de document](ui-manage-report-layouts.md)  
[Configurer la messagerie](admin-how-setup-email.md)  
[Facturer des ventes](sales-how-invoice-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
