---
title: Paramétrer la messagerie dans Business Central | Microsoft Docs
description: Décrit l'utilisation du serveur SMTP de la société pour envoyer et recevoir des e-mails dans Business Central. Décrit également comment utiliser les paramètres du serveur de messagerie créés lors de l'abonnement à Office 365.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 90e119dc44a23bcd9dca7920d05538ac685a44f6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304627"
---
# <a name="set-up-email"></a>Configurer la messagerie
Pour recevoir et envoyer des e-mails dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez renseigner les champs sur la page Paramétrage courrier SMTP.

Au lieu de saisir les détails du serveur SMTP manuellement, vous pouvez utiliser la fonction **Appliquer les paramètres de serveur Office 365** pour les saisir à l'aide des informations de votre abonnement Office 365.

Vous pouvez configurer la messagerie manuellement, comme décrit ci-dessous, ou vous faire aider du guide de configuration assistée **Paramétrage d'e-mail**. Pour plus d'informations, voir [Préparation aux activités commerciales](ui-get-ready-business.md).  

## <a name="to-set-up-email"></a>Pour configurer la messagerie
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrage courrier SMTP**, puis sélectionnez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Si vous utilisez un compte nécessitant une authentification à deux facteurs, le mot de passe que vous entrez dans le champ **Mot de passe** doit être le même que celui que vous utilisez pour votre abonnement Office 365 et il doit être de type **Mot de passe de l'application**.
3. Sinon, choisissez l'option **Appliquer les paramètres du serveur Office 365** pour insérer les informations déjà définies pour votre abonnement Office 365.
4. Lorsque tous les champs sont correctement renseignés, choisissez **Tester paramétrage e-mail**.
5. Une fois le test réussi, fermez la page.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Utilisation d'une adresse d'expéditeur de remplacement pour les courriers électroniques sortants
Tous les e-mails sortants de [!INCLUDE[d365fin](includes/d365fin_md.md)] utiliseront l'adresse par défaut du compte que vous avez spécifié sur la page Paramétrage courrier SMTP, comme décrit ci-dessus. Vous pouvez cependant utiliser les fonctionnalités **Envoyer en tant que** ou **Envoyer de la part de** sur votre serveur Exchange pour modifier l’adresse de l’expéditeur dans les messages sortants. [!INCLUDE[d365fin](includes/d365fin_md.md)] utilisera le compte par défaut pour s'authentifier auprès de Exchange, mais remplacera l'adresse de l'expéditeur par celle que vous spécifiez ou la modifiera avec "pour le compte de".

Voici des exemples d'utilisation des fonctionnalités Envoyer en tant que et Envoyer de la part de dans [!INCLUDE[d365fin](includes/d365fin_md.md)] :

 * Lorsque vous envoyez des documents tels que des commandes d'achat ou des commandes clients à des fournisseurs et à des clients, vous souhaitez peut-être qu'ils apparaissent comme provenant d'une adresse _noreply@yourcompanyname.com_.
 * Lorsque votre flux de travail envoie une demande d'approbation par courrier électronique à l'aide de l'adresse électronique du demandeur.

> [!Note]
> Vous ne pouvez utiliser qu'un seul compte pour remplacer les adresses d'expéditeur. En d'autres termes, vous ne pouvez pas avoir une adresse de remplacement pour les processus d'achat et une autre pour les processus de vente.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Pour configurer l'adresse de l'expéditeur de remplacement pour tous les messages électroniques sortants
1. Dans le **Centre d'administration Exchange** pour votre compte Office 365, recherchez la boîte aux lettres à utiliser comme adresse de substitution, puis copiez-la ou notez-la. Si vous avez besoin d'une nouvelle adresse, accédez à votre Centre d'administration Microsoft 365 pour créer un nouvel utilisateur et configurer sa boîte aux lettres.
2. Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], choisissez l'icône ![l'ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrage courrier SMTP**, puis sélectionnez le lien associé.
3. Dans le champ **Envoyer en tant que**, entrez l'adresse de substitution.
4. Copiez ou notez l'adresse dans le champ **ID utilisateur**.
5. Dans le **Centre d'administration Exchange**, recherchez la boîte aux lettres à utiliser en tant qu'adresse de substitution, puis entrez l'adresse à partir du champ **ID utilisateur** dans le champ **Envoyer en tant que**. Pour en savoir plus, reportez-vous à [Gérer les autorisations des destinataires](https://docs.microsoft.com/en-us/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Pour utiliser l'adresse de substitution dans les flux de travaux d'approbation
1. Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], choisissez l'icône ![l'ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrage courrier SMTP**, puis sélectionnez le lien associé.
2. Copiez ou notez l'adresse dans le champ **ID utilisateur**.
3. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres utilisateur approbation**, puis sélectionnez le lien associé.
4. Dans le **Centre d'administration Exchange**, recherchez les boîtes aux lettres de chaque utilisateur répertorié dans la liste de la page **Paramètres utilisateur approbation**, et dans le champ **Envoyer en tant que**, entrez l'adresse du champ **ID utilisateur** de la page **Paramétrage courrier SMTP** dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour en savoir plus, reportez-vous à [Gérer les autorisations des destinataires](https://docs.microsoft.com/en-us/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], choisissez l'icône ![l'ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrage courrier SMTP**, puis sélectionnez le lien associé.
6. Pour activer la substitution, tournez le bouton bascule **Autoriser substitution émetteur**.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] déterminera quelle adresse afficher dans l'ordre suivant : <br><br> 1. L'adresse spécifiée dans le champ **E-mail** sur la page **Paramètres utilisateur approbation** pour les messages dans un flux de travail. <br> 2. L'adresse spécifiée dans le champ **Envoyer en tant que** sur la page **Paramétrage courrier SMTP**. <br> 3. L'adresse spécifiée dans le champ **ID utilisateur** sur la page **Paramétrage courrier SMTP**.


## <a name="see-also"></a>Voir aussi  
[Boîtes aux lettres partagées dans Exchange Online](https://docs.microsoft.com/en-us/exchange/collaboration-exo/shared-mailboxes)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant que boîte de réception professionnelle dans Outlook](admin-outlook.md)  
[Obtention de [!INCLUDE[d365fin](includes/d365fin_md.md)] sur mon périphérique mobile](install-mobile-app.md)
