---
title: Paramétrer la messagerie dans Business Central (contient une vidéo)
description: "Décrit comment connecter des comptes de messagerie à Business\_Central afin que vous puissiez envoyer des messages sortants sans avoir à ouvrir une autre application."
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, email, Office 365, connector'
ms.search.form: '1805, 9813, 9814, 1262, 1263'
ms.date: 07/17/2023
ms.author: bholtorf
---

# Configurer la messagerie

Les utilisateurs au sein des entreprises envoient des informations et des documents, tels que des commandes vente et achat et des factures, par e-mail, au quotidien. Les administrateurs peuvent se connecter à un ou plusieurs comptes de messagerie à [!INCLUDE[prod_short](includes/prod_short.md)]. Vous pouvez donc envoyer des documents sans avoir à ouvrir une application de messagerie. Vous pouvez composer chaque message individuellement avec des outils de mise en forme de base, tels que des polices, des styles, des couleurs, etc., et ajouter des pièces jointes pouvant atteindre 100 Mo. De plus, les présentations d’états permettent aux administrateurs d’inclure uniquement les informations clés des documents. En savoir plus sur [Envoyer des documents par e-mail](ui-how-send-documents-email.md).

Les capacités de messagerie dans [!INCLUDE[prod_short](includes/prod_short.md)] s’appliquent aux messages sortants uniquement. Vous ne pouvez pas recevoir de réponses, c’est-à-dire qu’il n’existe pas de page « Boîte de réception ».

> [!NOTE]
> Vous pouvez utiliser les capacités de messagerie de [!INCLUDE[prod_short](includes/prod_short.md)] en ligne uniquement avec Exchange Online. Nous ne prenons pas en charge les scénarios hybrides, tels que la connexion de [!INCLUDE[prod_short](includes/prod_short.md)] en ligne vers une version locale d’Exchange.
>
> Si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] en local, avant de pouvoir configurer la messagerie électronique, vous devez créer une inscription d’application pour [!INCLUDE[prod_short](includes/prod_short.md)] dans le portail Azure. L’enregistrement de l’application activera [!INCLUDE[prod_short](includes/prod_short.md)] pour autoriser et s’authentifier auprès de votre fournisseur de messagerie. En savoir plus sur [Configurer la messagerie pour Business Central local](admin-how-setup-email.md#set-up-email-for-business-central-on-premises) Dans [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, nous nous en chargeons pour vous.

## Conditions requises

Il y a des conditions requises pour la configuration et l’utilisation des fonctionnalités de messagerie.

* Pour configurer la messagerie électronique, vous devez disposer de l’ensemble d’autorisations **PARAMÉTRAGE COURRIER**. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).
* Chaque utilisateur qui utilisera les fonctionnalités de messagerie doit disposer d’une licence [!INCLUDE [prod_short](includes/prod_short.md)]. Par exemple, les administrateurs délégués et les utilisateurs invités ne peuvent pas utiliser le compte de messagerie du client.

## Ajouter des comptes de messagerie

Vous ajoutez des comptes de messagerie via des extensions qui permettent aux comptes de différents fournisseurs de se connecter à [!INCLUDE[prod_short](includes/prod_short.md)]. Les extensions standard vous permettent d’utiliser les comptes de Microsoft Exchange Online. Cependant, d’autres extensions vous permettant de connecter des comptes d’autres fournisseurs, tels que Gmail, peuvent être disponibles.

Vous pouvez spécifier des scénarios professionnels prédéfinis dans lesquels utiliser un compte de messagerie pour envoyer des e-mails. Par exemple, vous pouvez spécifier que tous les utilisateurs envoient des documents de vente à partir d’un compte et achètent des documents à partir d’un autre. En savoir plus sur [Affecter des scénarios de messagerie aux comptes de messagerie](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

Le tableau suivant décrit les extensions de messagerie disponibles par défaut.

|Extension  |Description  |Exemples de scénario où utiliser  |
|---------|---------|---------|
|**Connecteur Microsoft 365**|Tout le monde envoie des e-mails à partir d’une boîte aux lettres partagée dans Exchange Online.|Lorsque tous les messages proviennent du même service, par exemple, votre organisation commerciale envoie des messages à partir d’un compte sales@cronus.com. Cette option nécessite que vous configuriez une boîte aux lettres partagée dans le centre d’administration Microsoft 365. Pour plus d’informations, consulter [Boîtes aux lettres partagées](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Connecteur utilisateur actuel**|Tout le monde envoie un e-mail à partir du compte de connexion habituel à [!INCLUDE[prod_short](includes/prod_short.md)].|Autorisez les communications à partir de comptes individuels.|
|**Connecteur SMTP**|Utilisez le protocole SMTP pour envoyer des e-mails.|Autorisez les communications via votre serveur de messagerie SMTP. |

> [!NOTE]
> Les extensions **Connecteur Microsoft 365** et **Connecteur utilisateur actuel** utilisent les comptes que vous configurez pour les utilisateurs dans le centre d’administration Microsoft 365 pour votre abonnement Microsoft 365. Pour envoyer des e-mails à l’aide des extensions, les utilisateurs doivent disposer d’une licence valide pour Exchange Online. De plus, dans les environnements sandbox, ces extensions nécessitent que le paramètre **Autoriser les demandes HttpClient** soit activé. Pour vérifier s’il est activé pour ces extensions, rendez-vous sur la page **Gestion des extensions**, choisissez l’extension, puis choisissez l’option **Configurer**.

> Les utilisateurs externes, tels que les administrateurs délégués et les comptables externes, ne peuvent pas utiliser ces extensions pour envoyer des e-mails à partir de [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## Utiliser SMTP

Si vous souhaitez utiliser le protocole SMTP pour envoyer des e-mails à partir de [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez utiliser l’extension Connecteur SMTP. Lorsque vous configurez un compte qui utilise SMTP, le champ **Type d’expéditeur** est important. Si vous sélectionnez **Utilisateur spécifique**, les e-mails seront envoyés en utilisant le nom et d’autres informations du compte configuré. Cependant, si vous sélectionnez **Utilisateur actuel**, les e-mails seront envoyés à partir du compte de messagerie spécifié pour le compte de chaque utilisateur. La fonction Utilisateur actuel est similaire à la fonction Envoyer en tant que. Pour plus d’informations, voir [Utiliser une adresse d’expéditeur de remplacement pour les e-mails sortants](admin-how-setup-email.md#use-a-substitute-sender-address-on-outbound-email-messages). 

> [!IMPORTANT]
> Si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] local, vous pouvez utiliser le protocole OAuth 2.0 pour l’authentification. Vous devez créer un enregistrement d’application dans le portail Azure, puis exécuter le guide d’installation assisté **Configurer Azure Active Directory** dans [!INCLUDE[prod_short](includes/prod_short.md)] pour se connecter à Azure AD. Pour plus d’informations, consultez [Créer une inscription d’application pour Business Central dans le portail Azure](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).
>
> Exchange Online ne prend pas en charge l’authentification de base pour SMTP. Les clients qui utilisent actuellement l’authentification SMTP ne seront pas affectés par ce changement. Cependant, nous vous recommandons fortement d’utiliser la version la plus récente de [!INCLUDE [prod_short](includes/prod_short.md)] et de configurer l’authentification OAuth 2.0 pour SMTP. Nous n’ajouterons pas l’authentification basée sur les certificats pour les versions antérieures de [!INCLUDE [prod_short](includes/prod_short.md)], par exemple, version 14. Si vous ne pouvez pas configurer l’authentification OAuth 2.0, nous vous encourageons à explorer d’autres moyens si vous souhaitez utiliser la messagerie SMTP dans des versions antérieures.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## Utiliser le guide de configuration assistée Configurer la messagerie

Le guide de configuration assistée **Configurer la messagerie** peut vous aider à démarrer rapidement avec les e-mails.

> [!NOTE]
> Vous devez disposer d’un compte de messagerie par défaut, même si vous n’ajoutez qu’un seul compte. Le compte par défaut sera utilisé pour tous les scénarios de messagerie qui ne sont pas attribués à un compte. En savoir plus sur [Affecter des scénarios de messagerie aux comptes de messagerie](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Configurer les comptes de messagerie**, puis sélectionnez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## Affecter des scénarios de messagerie aux comptes de messagerie

Les scénarios de messagerie sont des processus qui impliquent l’envoi d’un document. Par exemple, une commande vente ou achat ou une notification, telle qu’une invitation à un comptable externe. Des comptes de messagerie spécifiques peuvent être utilisés pour des scénarios spécifiques. Par exemple, vous pouvez spécifier que tous les utilisateurs envoient toujours les documents de vente à partir d’un compte, les documents d’achat d’un autre et les documents d’entrepôt ou de production à partir d’un troisième compte. Vous pouvez attribuer, réattribuer et supprimer des scénarios quand vous le souhaitez. Un scénario ne peut être attribué qu’à un seul compte de messagerie à la fois. Le compte de messagerie par défaut sera utilisé pour tous les scénarios qui ne sont pas attribués à un compte.

Sur la page **Affectation des scénarios par e-mail**, vous pouvez sélectionner l’action **Définir les pièces jointes par défaut** pour ajouter des pièces jointes aux scénarios de messagerie. Les pièces jointes seront toujours disponibles lorsque vous composerez un e-mail pour un document lié au scénario. Chaque scénario d’e-mail peut avoir une ou plusieurs pièces jointes par défaut. Les pièces jointes par défaut sont automatiquement ajoutées aux e-mails pour le scénario d’e-mail. Par exemple, lorsque vous envoyez une commande client par e-mail, la pièce jointe par défaut spécifiée pour le scénario Commande vente sera ajoutée. Les pièces jointes par défaut s’affichent dans la section **Pièces jointes** au bas de la page **Composer un e-mail**. Vous pouvez ajouter manuellement des pièces jointes autres que par défaut à l’e-mail.

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

## Configurer des politiques d’affichage

Vous pouvez contrôler les messages électroniques auxquels un utilisateur peut accéder sur les pages Boîte d’envoi d’e-mails et E-mails envoyés.

Dans **Stratégies affichage e-mail utilisateur**, choisissez un utilisateur, puis choisissez l’une des options suivantes dans le champ **Stratégie d’affichage des e-mails** :

* **Afficher mes e-mails personnalisés** – L’utilisateur ne peut afficher que ses propres e-mails.
* **Afficher tous les e-mails** – L’utilisateur peut afficher tous les e-mails, y compris les e-mails envoyés par d’autres utilisateurs.
* **Afficher si accès à tous les enregistrements associés** – Cette stratégie d’affichage est utilisée si aucune autre stratégie n’est spécifiée. Un utilisateur peut afficher les e-mails envoyés par d’autres utilisateurs s’il a accès à l’enregistrement envoyé et à tous ceux qui y sont liés. Par exemple, l’utilisateur A a envoyé une facture vente validée à un client. L’utilisateur B peut voir l’e-mail s’il a accès à la fois à la facture et au client.
* **Afficher si accès à tous les enregistrements associés** – L’utilisateur peut afficher les e-mails envoyés par d’autres personnes s’il a accès à au moins un enregistrement lié à l’enregistrement envoyé. Par exemple, l’utilisateur A a envoyé une facture vente validée à un client. L’utilisateur B peut voir l’e-mail s’il a accès à la facture ou au client.

> [!NOTE]
> Si vous laissez le champ **Identifiant utilisateur** vide, puis sélectionnez l’action **Politique d’affichage des e-mails**, la politique d’affichage s’applique à tous les utilisateurs.

## Indiquer combien de messages peuvent être envoyés par un compte par minute

Certains fournisseurs de messagerie (FAI) limitent le nombre de messages électroniques pouvant être envoyés par un compte de messagerie en une seule fois, ou dans un certain laps de temps, ou les deux. Connue sous le nom de *limitation d’e-mails*, cette pratique permet aux FAI de contrôler le trafic sur leurs serveurs et d’empêcher le courrier indésirable. Si un compte de messagerie dépasse la limite, le FAI est susceptible de bloquer les messages. Pour être sûr que le nombre de messages envoyés depuis [!INCLUDE [prod_short](includes/prod_short.md)] respecte la limite de votre FAI, indiquez la limite pour chacun de vos comptes de messagerie.

La limite par défaut pour les types de comptes Microsoft 365 et Utilisateur actuel est 30, ce qui correspond à la limite définie par Exchange Online.

Il existe deux manières de définir la limite :

* Lorsque vous utilisez le guide de configuration assistée Configurer la messagerie électronique pour créer un nouveau compte, indiquez la limite dans le champ **Limite de taux par minute**.
* Pour les comptes de messagerie existants, indiquez la limite dans le champ **Limite de taux d’e-mail** du compte.

## Configurer des textes et dispositions d’e-mails réutilisables

Vous pouvez utiliser des états pour inclure des informations clés provenant de documents de vente, d’achat et de service dans des textes pour e-mails. Les dispositions d’état définissent le style et le contenu du texte de l’e-mail. Par exemple, le contenu peut être un message d’accueil ou des instructions qui précèdent les informations du document. Cette procédure décrit comment configurer l’état **Vente - Facture** pour les factures vente enregistrées, mais le processus est similaire pour les autres états.

> [!NOTE]
> Pour utiliser la mise en page afin de créer du contenu pour les e-mails, vous devez utiliser le type de fichier Word pour votre mise en page.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Sélection des états - Ventes**, puis sélectionnez le lien associé.
2. Sur la page **Sélection des états : Ventes**, dans le champ **Utilisation**, sélectionnez **Facture**
3. Sur une nouvelle ligne, dans le champ **ID état**, sélectionnez, par exemple, l’état standard 1306.
4. Cochez la case **Utiliser pour le corps du message e-mail**.
5. Choisissez le champ **Disposition du corps du message e-mail** et sélectionnez une présentation dans la liste.
6. Pour afficher ou modifier la disposition sur laquelle le texte du message est basé, sélectionnez la disposition sur la page **Dispositions état personnalisées**, puis cliquez sur **Mettre à jour la disposition**. Si vous personnalisez la disposition, utilisez l’action **Importer la disposition** pour télécharger la nouvelle disposition.
    > [!NOTE]
    > Pour personnaliser une disposition standard de l’état, telle que 1306, vous devez faire une copie de l’état. [!INCLUDE [prod_short](includes/prod_short.md)] vous permet de créer une copie quand vous importez une disposition personnalisée pour un état standard. Le nom de la nouvelle disposition personnalisée de votre état est précédé de « Copie de ».
7. Si vous souhaitez permettre aux clients d’utiliser un service de paiement, tel que PayPal, vous devez configurer le service. Ensuite, les informations et le lien PayPal sont insérés dans le texte de l’e-mail. Pour plus d’informations, voir [Activer les paiements client via Paypal](sales-how-enable-payment-service-extensions.md).
8. Choisissez le bouton **OK**.

Désormais, lorsque vous sélectionnez, par exemple, l’action **Envoyer** sur la page **Facture vente enregistrée**, le corps du message comporte les informations de document de l’état 1306 précédé d’un texte standard auquel sont appliqués des attributs de style en fonction de la présentation d’état que vous avez sélectionnée à l’étape 5.

## Utiliser une adresse d’expéditeur de substitution dans les messages électroniques sortants

Si vous utilisez l’extension Connecteur SMTP, vous pouvez utiliser les fonctionnalités **Envoyer en tant que** ou **Envoyer de la part de** sur Microsoft Exchange pour modifier l’adresse de l’expéditeur dans les messages sortants. [!INCLUDE[prod_short](includes/prod_short.md)] utilisera le compte SMTP pour s’authentifier auprès d’Exchange, mais remplacera l’adresse de l’expéditeur par celle que vous spécifiez ou la modifiera avec « pour le compte de ».

Lorsque vous configurez un compte et que vous souhaitez utiliser les fonctionnalités Exchange Envoyer en tant que ou Envoyer de la part de, dans le champ **Type d’expéditeur**, choisissez **Utilisateur spécifique**.

Vous pouvez également choisir **Utilisateur actuel** pour permettre aux utilisateurs d’envoyer des messages via le connecteur SMTP. Le message semblera avoir été envoyé à partir du compte de messagerie spécifié dans le champ Email de contact sur la carte utilisateur de l’utilisateur utilisé pour la connexion. Cependant, il fonctionnera de la même manière que la fonction Envoyer en tant que et sera envoyé à partir du compte spécifié dans la configuration du connecteur SMTP.

Voici des exemples d’utilisation des fonctionnalités Envoyer en tant que et Envoyer de la part de dans [!INCLUDE[prod_short](includes/prod_short.md)] :

* Vous pouvez souhaiter que les commandes achat ou les commandes vente que vous envoyez à des fournisseurs et à des clients apparaissent comme provenant d’une adresse _noreply@yourcompanyname.com_.
* Quand votre flux de travail envoie une demande d’approbation par courrier électronique à l’aide de l’adresse électronique du demandeur.

> [!Note]
> Vous ne pouvez utiliser qu’un seul compte pour remplacer les adresses d’expéditeur. En d’autres termes, vous ne pouvez pas avoir une adresse de remplacement pour les processus d’achat et une autre pour les processus de vente.

<!--
### To set up the substitute sender address for all outbound email messages
1. In the **Exchange admin center** for your Microsoft 365 account, find the mailbox to use as the substitute address, and then copy or make a note of the address. If you need a new address, go to your Microsoft 365 admin center to create a new user and set up their mailbox.
2. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
3. In the **Send As** field, enter the substitute address.
4. Copy or make a note of the address in the **User ID** field.
5. In the **Exchange admin center**, find the mailbox to use as the substitute address, and then enter the address from the **User ID** field in the **Send As** field. For more information, see [Use the EAC to assign permissions to individual mailboxes](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### To use the substitute address in approval workflows
1. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Copy or make a note of the address in the **User ID** field.
3. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Approval User Setup**, and then choose the related link.
4. In the **Exchange admin center**, find the mailboxes for each user listed in the **Approval User Setup** page, and in the **Send As** field enter the address from the **User ID** field of the **SMTP Email Setup** page in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Manage permissions for recipients](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
6. To enable substitution, turn on the **Allow Sender Substitution** toggle.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] will determine which address to display in the following order: <br><br> 1. The address specified in the **E-Mail** field on the **Approval User Setup** page for messages in a workflow. <br> 2. The address specified in the **Send As** field in the **SMTP Email Setup** page. <br> 3. The address specified in the **User ID** field in the **SMTP Email Setup** page. -->

## Configurer des profils d’envoi de documents

Vous pouvez gagner du temps en configurant une méthode préférée d’envoi des documents de vente pour chacun de vos clients. Vous n’aurez pas à sélectionner une option d’envoi, par exemple si vous souhaitez envoyer le document par e-mail ou sous forme de document électronique, chaque fois que vous envoyez un document. Pour plus d’informations, reportez vous à [Configurer des profils d’envoi de documents](sales-how-setup-document-send-profiles.md).

## Facultatif : Configurer la journalisation des e-mails dans Exchange Online

Tirez le meilleur parti des communications entre les vendeurs et vos clients existants ou potentiels. Vous pouvez suivre les échanges d’e-mails, puis les transformer en opportunités exploitables. En savoir plus sur [Suivre les échanges de messages électroniques entre les commerciaux et les contacts](marketing-set-up-email-logging.md).  
<!--
[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Next, you connect [!INCLUDE[prod_short](includes/prod_short.md)] with Exchange Online. For more information, see [Track Email Message Exchanges Between Salespeople and Contacts](marketing-set-up-email-logging.md).  -->

## Facultatif : surveillez l’utilisation de la messagerie et résolvez les échecs de la messagerie grâce à la télémétrie

Les administrateurs peuvent activer la fonction de télémétrie dans [!INCLUDE[prod_short](includes/prod_short.md)] pour obtenir des données sur l’utilisation et les défauts des différentes fonctionnalités du système. Pour la messagerie, nous enregistrons les opérations suivantes :

- Un e-mail a été envoyé avec succès  
- Une tentative d’envoi d’un e-mail a échoué   
- L’authentification auprès d’un serveur SMTP a réussi/échoué  
- La connexion auprès d’un serveur SMTP a réussi/échoué  

Vous pouvez utiliser ces données pour surveiller l’utilisation de la messagerie et pour résoudre les échecs associés. Pour en savoir plus, consultez [Analyse de la télémétrie de la messagerie (contenu administratif)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace).  

## Configurer la messagerie pour Business Central local

[!INCLUDE[prod_short](includes/prod_short.md)] sur site peut s’intégrer à des services basés sur Microsoft Azure. Par exemple, vous pouvez utiliser Cortana Intelligence pour des prévisions de trésorerie plus intelligentes, Power BI pour visualiser votre entreprise, et Exchange Online pour envoyer un e-mail. L’intégration avec ces services est basée sur l’enregistrement d’une application dans Azure Active Directory. L’enregistrement de l’application fournit des services d’authentification et d’autorisation pour les communications. Pour utiliser les fonctionnalités de messagerie dans [!INCLUDE[prod_short](includes/prod_short.md)] sur site, vous devez vous inscrire [!INCLUDE[prod_short](includes/prod_short.md)] en tant qu’application dans le portail Azure, puis connectez [!INCLUDE[prod_short](includes/prod_short.md)] à l’enregistrement de l’application. Les sections suivantes décrivent comment.

### Créer une inscription d’application pour Business Central dans le portail Azure

Les étapes pour inscrire [!INCLUDE[prod_short](includes/prod_short.md)] dans le portail Azure sont décrits dans [Enregistrer une application dans Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

> [!NOTE]
> Pour utiliser les fonctionnalités de messagerie, l’enregistrement de votre application doit utiliser une configuration mutualisée.

Les paramètres spécifiques aux fonctionnalités de messagerie sont les autorisations déléguées que vous accordez à l’inscription de votre application. Le tableau suivant répertorie les autorisations minimales.

|API / Nom d’autorisation  |Type  |Description  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Délégué|Connectez-vous et lisez le profil utilisateur.         |
|Microsoft Graph / Mail.ReadWrite |Délégué|Rédigez des messages électroniques.         |
|Microsoft Graph / Mail.Send|Délégué|Envoyez des messages.         |
|Microsoft Graph / offline_access|Délégué|Conservez le consentement à l’accès aux données.|

Si vous utilisez le connecteur SMTP et que vous souhaitez utiliser OAuth 2.0 pour l’authentification, les autorisations sont légèrement différentes. Le tableau suivant répertorie les autorisations.

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

En savoir plus sur les directives générales pour l’inscription d’une application sur [Démarrage rapide : enregistrer une application avec la plateforme d’identités Microsoft](/azure/active-directory/develop/quickstart-register-app).

> [!NOTE]
Si vous ne parvenez pas à utiliser le protocole SMTP pour envoyer un e-mail après avoir connecté [!INCLUDE[prod_short](includes/prod_short.md)] à l’inscription de votre application, cela peut être dû au fait que SMTP AUTH n’est pas activé pour votre locataire. Nous vous recommandons d’utiliser à la place les connecteurs de messagerie Microsoft 365 et Utilisateur actuel, car ils utilisent les API Microsoft Graph Mail. Cependant, si vous devez utiliser le protocole SMTP, vous pouvez activer SMTP AUTH. Pour plus d’informations, consultez [Activer ou désactiver la soumission SMTP du client authentifié (SMTP AUTH) dans Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### Connecter [!INCLUDE[prod_short](includes/prod_short.md)] à votre inscription d’application

Après avoir enregistré votre application dans le portail Azure, dans [!INCLUDE[prod_short](includes/prod_short.md)], utilisez la page **Enregistrement AAD de l’application de messagerie** pour y connecter [!INCLUDE[prod_short](includes/prod_short.md)].

1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], choisissez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Enregistrement AAD de l’application de messagerie**, puis sélectionnez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Sinon, si vous vous connectez pour la première fois, vous pouvez exécuter le guide de configuration assistée **Configurer la messagerie**. Dans ce cas, le guide inclura également la page Enregistrement AAD de l’application de messagerie pour ajouter les informations de connexion à l’enregistrement de votre application. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

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

## Voir la [formation Microsoft](/training/modules/set-up-email/) associée

## Voir aussi

[Boîtes aux lettres partagées dans Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions](ui-extensions.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] en tant que boîte de réception professionnelle dans Outlook](admin-outlook.md)  
[Obtention de [!INCLUDE[prod_short](includes/prod_short.md)] sur mon périphérique mobile](install-mobile-app.md)   
[Obtention de [!INCLUDE[prod_short](includes/prod_short.md)] sur mon périphérique mobile](install-mobile-app.md)   
[Analyse de la télémétrie de la messagerie (contenu administratif)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
