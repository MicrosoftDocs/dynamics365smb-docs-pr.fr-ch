---
title: Paramétrer la messagerie dans Business Central
description: Décrit comment connecter des comptes de messagerie à Business Central afin que vous puissiez envoyer des messages sortants sans avoir à ouvrir une autre application.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, email, Office 365, connector
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 791033d9b4077ad6e3bf37ab04956113183b5f2b
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440528"
---
# <a name="set-up-email"></a>Configurer la messagerie
Les utilisateurs au sein des entreprises envoient des informations et des documents, tels que des commandes vente et achat et des factures, par e-mail, au quotidien. Les administrateurs peuvent faciliter cette tâche en connectant un ou plusieurs comptes de messagerie à [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez donc envoyer des documents sans avoir à ouvrir une application de messagerie. Vous pouvez composer chaque message individuellement avec des outils de mise en forme de base, tels que des polices, des styles, des couleurs, etc., et ajouter des pièces jointes pouvant atteindre 100 Mo. Les administrateurs peuvent également configurer des présentations d’états qui incluent uniquement les informations clés des documents. Pour plus d’informations, voir [Envoyer des documents par e-mail](ui-how-send-documents-email.md).

Les capacités de messagerie dans [!INCLUDE[prod_short](includes/prod_short.md)] sont pour les messages sortants uniquement. Vous ne pouvez pas recevoir de réponses, c’est-à-dire qu’il n’y a pas de page de boîte de réception dans [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Vous pouvez utiliser les capacités de messagerie de [!INCLUDE[prod_short](includes/prod_short.md)] en ligne uniquement avec Exchange Online. Nous ne prenons pas en charge les scénarios hybrides, tels que la connexion de [!INCLUDE[prod_short](includes/prod_short.md)] en ligne vers une version locale d’Exchange.
> 
> Si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] en local, avant de pouvoir configurer la messagerie électronique, vous devez créer une inscription d’application pour [!INCLUDE[prod_short](includes/prod_short.md)] dans le portail Azure. L’enregistrement de l’application activera [!INCLUDE[prod_short](includes/prod_short.md)] pour autoriser et s’authentifier auprès de votre fournisseur de messagerie. Pour plus d’informations, voir [Configuration des e-mails pour Business Central en local](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). Dans [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, nous nous en chargeons pour vous.

## <a name="required-permissions"></a>Autorisations requises
Pour configurer la messagerie électronique, vous devez disposer de l’ensemble d’autorisations **PARAMÉTRAGE COURRIER**. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md). 

## <a name="adding-email-accounts"></a>Ajouter des comptes de messagerie
Vous ajoutez des comptes de messagerie via des extensions qui permettent aux comptes de différents fournisseurs de se connecter à [!INCLUDE[prod_short](includes/prod_short.md)]. Les extensions standard vous permettent d’utiliser des comptes de Microsoft Exchange Online, mais d’autres extensions peuvent être disponibles pour vous permettre de connecter des comptes d’autres fournisseurs, tels que Gmail.

Après avoir ajouté un compte de messagerie, vous pouvez spécifier des scénarios professionnels prédéfinis dans lesquels utiliser le compte pour envoyer des e-mails. Par exemple, vous pouvez spécifier que tous les utilisateurs envoient des documents de vente à partir d’un compte et achètent des documents à partir d’un autre. Pour plus d’informations, consultez [Attribuer des scénarios de messagerie aux comptes de messagerie](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

Le tableau suivant décrit les extensions de messagerie disponibles par défaut.

|Extension  |Description  |Exemples de scénario où utiliser  |
|---------|---------|---------|
|**Microsoft 365**|Tout le monde envoie des e-mails à partir d’une boîte aux lettres partagée dans Exchange Online.|Lorsque tous les messages proviennent du même service, par exemple, votre organisation commerciale envoie des messages à partir d’un compte sales@cronus.com. Cela nécessite que vous configuriez une boîte aux lettres partagée dans le centre d’administration Microsoft 365. Pour plus d’informations, consulter [Boîtes aux lettres partagées](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Utilisateur actuel**|Tout le monde envoie un e-mail à partir du compte de connexion habituel à [!INCLUDE[prod_short](includes/prod_short.md)].|Autorisez les communications à partir de comptes individuels.|
|**Autre (SMTP)**|Utilisez le protocole SMTP pour envoyer des e-mails.|Autorisez les communications via votre serveur de messagerie SMTP. |

> [!NOTE]
> Les extensions **Microsoft 365** et **Utilisateur actuel** utilisent les comptes que vous configurez pour les utilisateurs dans le centre d’administration Microsoft 365 pour votre abonnement à Microsoft 365. Pour envoyer des e-mails à l’aide des extensions, les utilisateurs doivent disposer d’une licence valide pour Exchange Online. 
>
> De plus, les utilisateurs externes, tels que les administrateurs délégués et les comptables externes, ne peuvent pas utiliser ces extensions pour envoyer des e-mails à partir de [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="legacy-smtp-settings-and-the-email---smtp-connector-extension"></a>Paramètres SMTP hérités et l’extension E-mail - Connecteur SMTP
Si vous utilisez déjà [!INCLUDE[prod_short](includes/prod_short.md)] et si vous avez configuré le courrier électronique via la configuration SMTP héritée, vous pouvez continuer à utiliser votre configuration en parallèle avec l’extension Email - Connecteur SMTP. Lorsque nous mettons à jour votre [!INCLUDE[prod_short](includes/prod_short.md)] vers la prochaine version, nous copierons vos anciens paramètres SMTP dans l’extension Email - Connecteur SMTP. Lorsque vous êtes prêt, votre administrateur peut activer les fonctionnalités de messagerie améliorées et vous commencerez à utiliser l’extension Email - Connecteur SMTP. Pour plus d’informations, voir [À propos de la gestion des fonctionnalités](/dynamics365/business-central/dev-itpro/administration/feature-management#about-feature-management). Cependant, il n’y a pas de synchronisation entre l’extension du connecteur SMTP et les paramètres hérités. Si vous modifiez les paramètres SMTP dans l’extension, vous devez effectuer les mêmes modifications dans la configuration SMTP héritée, ou vice versa.

> [!NOTE]
> Si vous avez des personnalisations qui reposent sur la configuration de messagerie SMTP héritée, il est possible que quelque chose se passe mal avec vos personnalisations si vous commencez à utiliser des extensions de messagerie. Nous vous recommandons de configurer et de tester les extensions avant d’activer le commutateur de fonctionnalité pour des fonctionnalités de messagerie améliorées.

> [!IMPORTANT]
> Si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] localement, vous pouvez utiliser OAuth 2.0 pour l’authentification, mais vous devez créer une inscription d’application dans le portail Azure, puis exécuter le guide de configuration assistée **Configurer Azure Active Directory** dans [!INCLUDE[prod_short](includes/prod_short.md)] pour vous connecter à Azure AD. Pour plus d’informations, consultez [Créer une inscription d’application pour Business Central dans le portail Azure](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).

## <a name="add-email-accounts"></a>Ajouter des comptes de messagerie
Le guide de configuration assistée **Configurer la messagerie** peut vous aider à démarrer rapidement avec les e-mails.

> [!NOTE]
> Vous devez disposer d’un compte de messagerie par défaut, même si vous n’ajoutez qu’un seul compte. Le compte par défaut sera utilisé pour tous les scénarios de messagerie qui ne sont pas attribués à un compte. Pour plus d’informations, consultez [Attribuer des scénarios de messagerie aux comptes de messagerie](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configurer les comptes de messagerie**, puis sélectionnez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Affecter des scénarios de messagerie aux comptes de messagerie
Les scénarios de messagerie sont des processus qui impliquent l’envoi d’un document, tel qu’une vente ou une commande d’achat, ou une notification, telle qu’une invitation à un comptable externe. Vous pouvez utiliser des comptes de messagerie spécifiques pour des scénarios spécifiques. Par exemple, vous pouvez spécifier que tous les utilisateurs envoient toujours les documents de vente à partir d’un compte, les documents d’achat d’un autre et les documents d’entrepôt ou de production à partir d’un troisième compte. Vous pouvez attribuer, réaffecter et supprimer des scénarios quand vous le souhaitez, mais vous ne pouvez affecter un scénario qu’à un seul compte de messagerie à la fois. Le compte de messagerie par défaut sera utilisé pour tous les scénarios qui ne sont pas attribués à un compte.
 
<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents"></a>Configurer des textes et des mises en page d’e-mail réutilisables pour les documents vente et achat
Vous pouvez utiliser des états pour inclure des informations clés provenant de documents de vente et d’achat dans des textes pour e-mails. Cette procédure décrit comment configurer l’état **Vente - Facture** pour les factures vente enregistrées, mais le processus est similaire pour les autres états.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Sélection des états - Ventes**, puis sélectionnez le lien associé.
2. Sur la page **Sélection des états : Ventes**, dans le champ **Utilisation**, sélectionnez **Facture**
3. Sur une nouvelle ligne, dans le champ **ID état**, sélectionnez, par exemple, l’état standard 1306.
4. Cochez la case **Utiliser pour le corps du message e-mail**.
5. Choisissez le champ **Disposition du corps du message e-mail** et sélectionnez une présentation dans la liste.

    Les présentations d’état définissent à la fois le style et le contenu du corps de message, y compris le texte tel qu’une situation ou des instructions qui précèdent les informations du document. Si votre organisation a plusieurs dispositions, vous pouvez visualiser toutes les présentations d’état disponibles si vous choisissez **Sélectionner dans la liste complète**.
6. Pour afficher ou modifier la disposition sur laquelle le texte du message est basé, sélectionnez la disposition sur la page **Dispositions état personnalisées**, puis cliquez sur **Mettre à jour la disposition**.
7. Si vous souhaitez proposer à vos clients de payer les ventes par voie électronique, vous pouvez configurer le service de paiement associé, comme Paypal par exemple, puis insérer également les informations et le lien Paypal dans le texte du message. Pour plus d’informations, voir [Activer les paiements client via Paypal](sales-how-enable-payment-service-extensions.md).
8. Choisissez le bouton **OK**.

Désormais, lorsque vous sélectionnez, par exemple, l’action **Envoyer** sur la page **Facture vente enregistrée**, le corps du message comporte les informations de document de l’état 1306 précédé d’un texte standard auquel sont appliqués des attributs de style en fonction de la présentation d’état que vous avez sélectionnée à l’étape 5.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Utilisation d’une adresse d’expéditeur de remplacement pour les courriers électroniques sortants
Si vous utilisez les paramètres SMTP hérités, vous pouvez utiliser les fonctionnalités **Envoyer en tant que** ou **Envoyer de la part de** sur Microsoft Exchange pour modifier l’adresse de l’expéditeur dans les messages sortants. [!INCLUDE[prod_short](includes/prod_short.md)] utilisera le compte SMTP pour s’authentifier auprès de Exchange, mais remplacera l’adresse de l’expéditeur par celle que vous spécifiez ou la modifiera avec "pour le compte de ».

Voici des exemples d’utilisation des fonctionnalités Envoyer en tant que et Envoyer de la part de dans [!INCLUDE[prod_short](includes/prod_short.md)] :

 * Lorsque vous envoyez des documents tels que des commandes d’achat ou des commandes clients à des fournisseurs et à des clients, vous souhaitez peut-être qu’ils apparaissent comme provenant d’une adresse _noreply@yourcompanyname.com_.
 * Lorsque votre flux de travail envoie une demande d’approbation par courrier électronique à l’aide de l’adresse électronique du demandeur.

> [!Note]
> Vous ne pouvez utiliser qu’un seul compte pour remplacer les adresses d’expéditeur. En d’autres termes, vous ne pouvez pas avoir une adresse de remplacement pour les processus d’achat et une autre pour les processus de vente.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Pour configurer l’adresse de l’expéditeur de remplacement pour tous les messages électroniques sortants
1. Dans le **Centre d’administration Exchange** pour votre compte Microsoft 365, recherchez la boîte aux lettres à utiliser comme adresse de substitution, puis copiez-la ou notez-la. Si vous avez besoin d’une nouvelle adresse, accédez à votre Centre d’administration Microsoft 365 pour créer un nouvel utilisateur et configurer sa boîte aux lettres.
2. Dans [!INCLUDE[prod_short](includes/prod_short.md)] sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramétrage courrier SMTP**, puis choisissez le lien associé.
3. Dans le champ **Envoyer en tant que**, entrez l’adresse de substitution.
4. Copiez ou notez l’adresse dans le champ **ID utilisateur**.
5. Dans le **Centre d’administration Exchange**, recherchez la boîte aux lettres à utiliser en tant qu’adresse de substitution, puis entrez l’adresse à partir du champ **ID utilisateur** dans le champ **Envoyer en tant que**. Pour plus d’informations, voir [Utiliser l’EAC pour attribuer des autorisations à des boîtes aux lettres individuelles](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Pour utiliser l’adresse de substitution dans les flux de travaux d’approbation
1. Dans [!INCLUDE[prod_short](includes/prod_short.md)] sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramétrage courrier SMTP**, puis choisissez le lien associé.
2. Copiez ou notez l’adresse dans le champ **ID utilisateur**.
3. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres utilisateur approbation**, puis choisissez le lien associé.
4. Dans le **Centre d’administration Exchange**, recherchez les boîtes aux lettres de chaque utilisateur répertorié dans la liste de la page **Paramètres utilisateur approbation**, et dans le champ **Envoyer en tant que**, entrez l’adresse du champ **ID utilisateur** de la page **Paramétrage courrier SMTP** dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour en savoir plus, reportez-vous à [Gérer les autorisations des destinataires](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. Dans [!INCLUDE[prod_short](includes/prod_short.md)] sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramétrage courrier SMTP**, puis choisissez le lien associé.
6. Pour activer la substitution, tournez le bouton bascule **Autoriser substitution émetteur**.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] déterminera quelle adresse afficher dans l’ordre suivant : <br><br> 1. L’adresse spécifiée dans le champ **E-mail** sur la page **Paramètres utilisateur approbation** pour les messages dans un flux de travail. <br> 2. L’adresse spécifiée dans le champ **Envoyer en tant que** sur la page **Paramétrage courrier SMTP**. <br> 3. L’adresse spécifiée dans le champ **ID utilisateur** sur la page **Paramétrage courrier SMTP**.

## <a name="set-up-document-sending-profiles"></a>Configurer des profils d’envoi de documents
Vous pouvez configurer une méthode préférée d’envoi de documents de vente pour chacun de vos clients afin de ne pas avoir à sélectionner une option d’envoi, comme l’envoi du document par e-mail ou sous forme de document électronique, chaque fois que vous envoyez un document. Pour plus d’informations, reportez vous à [Configurer des profils d’envoi de documents](sales-how-setup-document-send-profiles.md).

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Configurer les dossiers publics et les règles de connexion à la messagerie dans Exchange Online
Tirez le meilleur parti des communications entre les vendeurs et vos clients existants ou potentiels en suivant les échanges de courriers électroniques, puis en les transformant en opportunités exploitables. Pour plus d’informations, voir [Suivre les échanges de messages électroniques entre les vendeurs et les contacts](marketing-set-up-email-logging.md).  

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Ensuite, vous connectez [!INCLUDE[prod_short](includes/prod_short.md)] à Exchange Online. Pour plus d’informations, voir [Suivre les échanges de messages électroniques entre les vendeurs et les contacts](marketing-set-up-email-logging.md).  

## <a name="setting-up-email-for-business-central-on-premises"></a>Configuration de la messagerie sur site pour Business Central 
[!INCLUDE[prod_short](includes/prod_short.md)] sur site peut s’intégrer à des services basés sur Microsoft Azure. Par exemple, vous pouvez utiliser Cortana Intelligence pour des prévisions de trésorerie plus intelligentes, Power BI pour visualiser votre entreprise, et Exchange Online pour envoyer un e-mail. L’intégration avec ces services est basée sur l’enregistrement d’une application dans Azure Active Directory. L’enregistrement de l’application fournit des services d’authentification et d’autorisation pour les communications. Pour utiliser les fonctionnalités de messagerie dans [!INCLUDE[prod_short](includes/prod_short.md)] sur site, vous devez vous inscrire [!INCLUDE[prod_short](includes/prod_short.md)] en tant qu’application dans le portail Azure, puis connectez [!INCLUDE[prod_short](includes/prod_short.md)] à l’enregistrement de l’application. Les sections suivantes décrivent comment.

### <a name="create-an-app-registration-for-business-central-in-azure-portal"></a>Créer une inscription d’application pour Business Central dans le portail Azure
Les étapes pour inscrire [!INCLUDE[prod_short](includes/prod_short.md)] dans le portail Azure sont décrits dans [Enregistrer une application dans Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Les paramètres spécifiques aux fonctionnalités de messagerie sont les autorisations déléguées que vous accordez à l’inscription de votre application. Le tableau suivant répertorie les autorisations minimales.

|API / Nom d’autorisation  |Type  |Description  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Délégué|Connectez-vous et lisez le profil utilisateur.         |
|Microsoft Graph / Mail.ReadWrite |Délégué|Rédigez des messages électroniques.         |
|Microsoft Graph / Mail.Send|Délégué|Envoyez des messages.         |
|Microsoft Graph / offline_access|Délégué|Conservez le consentement à l’accès aux données.|

Si vous utilisez une configuration SMTP héritée ou le connecteur SMTP et que vous souhaitez utiliser OAuth pour l’authentification, les autorisations sont légèrement différentes. Le tableau suivant répertorie les autorisations.

|API / Nom d’autorisation  |Type  |Description  |
|---------|---------|---------|
|Microsoft Graph / offline_access|Délégué|Conservez le consentement à l’accès aux données.|
|Microsoft Graph / openid|Délégué|Connectez les utilisateurs.|
|Microsoft Graph / User.Read |Délégué|Connectez-vous et lisez le profil utilisateur.         |
|Microsoft Graph / SMTP.Send|Délégué|Envoyez des e-mails à partir de boîtes aux lettres en utilisant SMTP AUTH.         |
|Office 365 Exchange Online/ User.Read |Délégué|Connectez-vous et lisez le profil utilisateur.         |

Lorsque vous créez l’inscription de votre application, vous devez spécifier les informations suivantes. Vous en aurez besoin pour connecter [!INCLUDE[prod_short](includes/prod_short.md)] à l’enregistrement de votre application.
 
* ID de l’application (client) 
* Rediriger l’URI (facultatif)
* Le secret du client

Pour les instructions générales pour enregistrer une application, voir [Démarrage rapide : enregistrer une application avec la plateforme d’identité Microsoft](/azure/active-directory/develop/quickstart-register-app). 

> [!NOTE]
Si vous ne parvenez pas à utiliser la configuration SMTP héritée pour envoyer un e-mail après avoir connecté [!INCLUDE[prod_short](includes/prod_short.md)] à l’inscription de votre application, cela peut être dû au fait que SMTP AUTH n’est pas activé pour votre locataire. Nous vous recommandons d’utiliser à la place les connecteurs de messagerie Microsoft 365 et Utilisateur actuel, car ils utilisent les API Microsoft Graph Mail. Cependant, si vous devez utiliser la configuration SMTP, vous pouvez activer SMTP AUTH. Pour plus d’informations, consultez [Activer ou désactiver la soumission SMTP du client authentifié (SMTP AUTH) dans Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### <a name="connect-prod_short-to-your-app-registration"></a>Connecter l’application [!INCLUDE[prod_short](includes/prod_short.md)] à l’enregistrement de votre application
Après avoir enregistré votre application dans le portail Azure, dans [!INCLUDE[prod_short](includes/prod_short.md)], utilisez le guide de configuration assistée **Enregistrement AAD de l’application de messagerie** pour y connecter [!INCLUDE[prod_short](includes/prod_short.md)].

1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Enregistrement AAD de l’application de messagerie**, puis sélectionnez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Sinon, si vous vous connectez pour la première fois, vous pouvez exécuter le guide de configuration assistée **Configurer la messagerie**. Le guide aura besoin des informations pour vous connecter à l’enregistrement de votre application. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Azure Active Directory, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Azure AD Directory - Multitenant)** or **Accounts in any organizational directory (Any Azure AD Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Azure Active Directory, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/set-up-email/)

## <a name="see-also"></a>Voir aussi

[Boîtes aux lettres partagées dans Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions](ui-extensions.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)] en tant que boîte de réception professionnelle dans Outlook](admin-outlook.md)  
[Obtenir [!INCLUDE[prod_short](includes/prod_short.md)] sur mon appareil mobile](install-mobile-app.md)
[Obtenir [!INCLUDE[prod_short](includes/prod_short.md)] sur mon appareil mobile](install-mobile-app.md)
[Analyse de la télémétrie des e-mails (contenu d’administration)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
