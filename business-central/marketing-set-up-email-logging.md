---
title: Config. identifiant messagerie
description: Apprenez à transformer les interactions de messagerie entre les vendeurs et les clients en véritables opportunités de vente.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect, opportunity, email'
ms.date: 03/22/2022
ms.search.form: '1680, 1811, 5076'
ms.author: bholtorf
---
# Suivre les échanges de messages électroniques entre les vendeurs et les contacts
Tirez le meilleur parti des communications entre les vendeurs et les clients en transformant les échanges de courriers électroniques en opportunités exploitables. [!INCLUDE[prod_short](includes/prod_short.md)] peut utiliser Exchange Online pour conserver un journal des messages entrants et sortants. Vous pouvez afficher et analyser le contenu de chaque message sur la page **Écritures journal interaction**.

> [!NOTE]
> Dans la première vague de lancement de 2022, nous avons rationalisé les processus de configuration de la connexion à la messagerie afin d’accroître la flexibilité et la sécurité. Si vous êtes un nouveau client utilisant cette version, vous utilisez la nouvelle expérience. Si vous êtes un client existant, l’utilisation ou non de la nouvelle expérience dépend du fait que votre administrateur a activé ou non la fonctionnalité **Connexion à la messagerie à l’aide de l′API Microsoft Graph** dans **Gestion des fonctionnalités**. Pour plus d’informations, voir [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management).

> [!IMPORTANT]
> Pour [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, la nouvelle expérience exige que [!INCLUDE[prod_short](includes/prod_short.md)] et Exchange Online soient sur le même abonné.

## Pour configurer la connexion à la messagerie
Ces étapes diffèrent selon que votre administrateur a activé ou non la fonctionnalité **Connexion à la messagerie à l’aide de l′API Microsoft Graph**. Si la mise à jour des fonctionnalités n’est pas activée, suivez les étapes de l’onglet **Expérience actuelle**.

## [Expérience actuelle](#tab/current-experience)

### Configurer les dossiers publics et les règles de connexion à la messagerie dans Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Ensuite, vous connectez [!INCLUDE[prod_short](includes/prod_short.md)] à Exchange Online.

## [Nouvelle expérience](#tab/new-experience)
### Configurer une boîte aux lettres et des règles partagées pour la connexion à la messagerie dans Exchange Online

> [!NOTE]
> Ces étapes nécessitent un accès administrateur pour Exchange Online.

Préparez une boîte aux lettres partagée dans le Centre d’administration Exchange. Vous pouvez aussi utiliser Exchange Online PowerShell. Pour plus d’informations, voir [Créer une boîte aux lettres partagée](/microsoft-365/admin/email/create-a-shared-mailbox) ou [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Si vous utilisez Exchange Management PowerShell, vos modifications sont visibles dans le Centre d’administration Exchange après un certain délai. Le retard peut être de plusieurs heures.

### Ajouter un compte d’utilisateur pour les membres de la boîte aux lettres partagée
Le compte que vous utiliserez pour la connexion à la messagerie est un compte Exchange Online. La tâche planifiée va utiliser le compte pour se connecter à une boîte aux lettres partagée et traiter les e-mails. Ce compte ne doit pas être associé à une personne en particulier. Ajoutez le compte de messagerie aux membres de la boîte aux lettres partagée. Pour plus d’informations, voir [Utiliser l’EAC pour modifier la délégation de boîte aux lettres partagée](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### Autoriser les autres utilisateurs à voir les e-mails enregistrés
Vous pouvez autoriser un autre utilisateur à ouvrir un e-mail dans Exchange lié à une écriture du journal d’interaction de [!INCLUDE[prod_short](includes/prod_short.md)]. Pour ce faire, donnez l’autorisation ``Read`` à l’utilisateur sur le dossier **Archiver** dans la boîte aux lettres partagée. Pour plus d’informations, voir [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### Créer des règles de flux de messagerie
Les règles de flux de messagerie recherchent des conditions spécifiques sur les messages et prennent des mesures en conséquence. Créez deux règles de flux de messagerie en fonction des informations de la table suivante. Pour plus d’informations, voir [Gérer les règles de flux de messagerie dans Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) et [Actions des règles de flux de messagerie dans Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Objet  |Name  |Appliquer cette règle si...  |Procédez comme suit...  |
|---------|---------|---------|---------|
|Une règle pour les e-mails entrants     |Consigner les e-mails envoyés à cette organisation|L’expéditeur est situé en dehors de l’organisation, et le destinataire est situé au sein de l’organisation|Cci le compte de messagerie spécifié pour la boîte aux lettres partagée.|
|Une règle pour les e-mails sortants     |Consigner les e-mails envoyés à partir de cette organisation|L’expéditeur est situé au sein de l’organisation, et le destinataire est situé en dehors de l’organisation.|Cci le compte de messagerie spécifié pour la boîte aux lettres partagée.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] traite uniquement les messages du dossier Boîte de réception dans la boîte aux lettres partagée. Si une règle déplace des messages de la boîte de réception vers un autre dossier, ces messages ne seront pas traités. De plus, les messages du dossier Courriers indésirables sont également ignorés. 

---

## Configurer [!INCLUDE[prod_short](includes/prod_short.md)] pour enregistrer les messages électroniques
Ces étapes sont les mêmes pour les expériences actuelles et nouvelles.

Commencez avec la connexion à la messagerie en deux étapes :

1. Connectez [!INCLUDE[prod_short](includes/prod_short.md)] à Exchange Online pour votre abonnement Microsoft 365. Exchange Online gère vos e-mails. Nous avons facilité cette étape en fournissant un guide de configuration assisté. Vous avez juste besoin de vos identifiants d’administrateur pour votre compte d’administrateur dans Microsoft 365. Pour commencer le guide, accédez à la page **Configuration assistée**, puis sélectionnez le guide **Configurer la journalisation des emails**.  

2. Assurez-vous que les adresses e-mail de vos commerciaux et de vos contacts dans [!INCLUDE[prod_short](includes/prod_short.md)] sont valides. Pour ce faire, pour chaque client ou vendeur, ouvrez la fiche **Contact** ou **Vendeur/Acheteur** et regardez le champ **E-mail**.

> [!Tip]
> Une fois les étapes du guide terminées, vous pouvez vérifier si la connexion a réussi. Selon que vous utilisez l’expérience actuelle ou nouvelle, effectuez l’une des étapes suivantes : 
>
> * **Expérience actuelle** : Recherchez **Paramètres marketing**, choisissez **Accéder**, puis **Fonctions** et **Valider la configuration de la connexion à la messagerie**.
> * **Nouvelle expérience** : Recherchez **Connexion à la messagerie**, choisissez **Actions**, puis **Contrôler la configuration**.

## Affichage des échanges de messages électroniques dans le journal des interactions

[!INCLUDE[prod_short](includes/prod_short.md)] crée une entrée sur la page **Journal des interactions** chaque fois qu’un vendeur et un contact échangent un message par courrier électronique. Pour afficher le journal des interactions, ouvrez la fiche **Contact** pour la personne, puis choisissez **Association**, **Historique**, et **Écritures feuille interaction**. Vous pouvez faire certaines choses avec chaque entrée de la feuille, par exemple :

- Affichez le contenu du message électronique échangé en sélectionnant **Traitement**, puis **Afficher les Documents joints**.
- Transformez un échange de courrier électronique en opportunité de vente. Si une entrée semble prometteuse, vous pouvez la transformer en opportunité, puis gérer son évolution vers une vente. Pour transformer un échange de courrier électronique en opportunité, choisissez l’entrée, puis **Traiter**, et **Créer opportunité**. Pour plus d’informations, voir [Gérer des opportunités de vente](marketing-manage-sales-opportunities.md).

## Limites des boîtes aux lettres et des dossiers dans Exchange Online
Il existe des limites de boîtes aux lettres et de dossiers dans Exchange Online, telles que les limites de tailles de dossier et le nombre de messages. Pour plus d’informations, voir [Limites pour Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) et [Limites pour les dossiers publics dans Exchange Server](/Exchange/collaboration/public-folders/limits?view=exchserver-2019).

[!INCLUDE[prod_short](includes/prod_short.md)] stocke les messages électroniques enregistrés dans un dossier dans Exchange Online. [!INCLUDE[prod_short](includes/prod_short.md)] stocke également un lien vers chaque message enregistré. Les liens ouvrent les messages enregistrés dans Exchange Online à partir des pages Écritures journal interaction, Fiche contact et Fiche vendeurs dans [!INCLUDE[prod_short](includes/prod_short.md)]. Si un message enregistré est déplacé dans un autre dossier, le lien est rompu. Par exemple, un message peut être déplacé manuellement ou Exchange Online peut démarrer automatiquement la fonction AutoSplit lorsqu’une limite de stockage est atteinte.

Les étapes suivantes peuvent vous aider à éviter de rompre les liens vers les messages dans Exchange Online.

1. Ne déplacez pas les messages existants vers un autre dossier après avoir modifié les paramètres de configuration de la connexion à la messagerie. En gardant les messages existants là où ils se trouvent, vous conservez les liens. Les liens vers les messages dans le nouveau dossier sont valides.
2. Évitez d’atteindre les limites des boîtes aux lettres et des dossiers. Si vous êtes sur le point d’atteindre une limite, procédez comme suit :
    1. Configurez une nouvelle boîte aux lettres partagée (nouvelle expérience) ou un nouveau dossier partagé (expérience actuelle) dans Exchange Online.
    2. Mettez à jour les règles de flux de messagerie dans Exchange Online.
    3. Mettre à jour la configuration de la connexion à la messagerie dans Business Central en conséquence

## Se connecter aux versions locales vers Microsoft Exchange

Vous pouvez vous connecter à [!INCLUDE[prod_short](includes/prod_short.md)] sur site vers Exchange sur site ou Exchange Online pour la connexion à la messagerie. Pour les deux versions d’Exchange, les paramètres de connexion sont disponibles sur la page **Configuration marketing**. Pour Exchange Online, vous pouvez également utiliser un guide de configuration assistée.

> [!IMPORTANT]
> La nouvelle expérience ne prend pas en charge de connexion à Exchange sur site. Si vous devez utiliser Exchange sur site, n’activez pas la mise à jour des fonctionnalités pour la nouvelle expérience.

## Se connecter à Exchange sur site
## [Expérience actuelle](#tab/current-experience)
Pour connecter [!INCLUDE[prod_short](includes/prod_short.md)] sur site à Exchange sur site, sur la page **Configuration marketing**, vous pouvez utiliser **De base** comme **Type d’identification**, puis entrez les informations d’identification pour le compte d’utilisateur pour Exchange sur site. Puis activez le bouton bascule **Activé** pour commencer à enregistrer les e-mails.

## [Nouvelle expérience](#tab/new-experience)
La nouvelle expérience ne prend pas en charge les connexions à Exchange sur site.

---

## Se connecter à Exchange Online
Pour se connecter à Exchange Online, vous devez enregistrer une application dans Azure Active Directory. Vous devez fournir l’ID de l’application, le secret du coffre de clés et l’URL de redirection à utiliser. L’URL de redirection est pré-définie et devrait fonctionner pour la plupart des installations. Pour plus d’informations, consultez [Enregistrer une application dans Azure AD pour se connecter de Business Central à Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Vous devez aussi utiliser **OAuth2** comme **Type d’identification**. Vous devez également enregistrer une demande dans Azure Active Directory. Vous devez fournir l’ID de l’application, le secret du coffre de clés et l’URL de redirection à utiliser. L’URL de redirection est pré-remplie et devrait fonctionner pour la plupart des installations. Pour plus d’informations, consultez Pour enregistrer une application dans Azure AD pour se connecter de Business Central à Exchange Online ci-dessous.

Vous devez configurer votre installation pour utiliser HTTPS. Pour plus d’informations, voir [Configuration de SSL pour sécuriser la connexion du client Web Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Si vous configurez votre serveur pour avoir une page d’accueil différente, vous pouvez changer l’URL. Le secret client sera enregistré sous forme de chaîne cryptée dans votre base de données.

### Pour enregistrer une application dans Azure AD pour se connecter de Business Central à Exchange Online
Les étapes suivantes supposent que vous utilisez Azure Active Directory pour gérer les identités et les accès. Pour plus d’informations, voir [Démarrage rapide : enregistrer une application avec la plateforme d’identité Microsoft](/azure/active-directory/develop/quickstart-register-app). 

## [Expérience actuelle](#tab/current-experience) 
Les étapes suivantes supposent que vous utilisez Azure Active Directory pour gérer les identités et les accès. Pour plus d’informations, voir [Démarrage rapide : enregistrer une application avec la plateforme d’identité Microsoft](/azure/active-directory/develop/quickstart-register-app). Si vous n’utilisez pas Azure Active Directory, voir [Utiliser un autre service de gestion des identités et des accès](marketing-set-up-email-logging.md#use-another-identity-and-access-management-service). 

1. Dans le portail Azure, sous **Gérer**, choisissez **Authentification**.
2. Sous **Rediriger les URL**, ajoutez l’URL de redirection suggérée sur la page de **Configuration marketing** dans [!INCLUDE[prod_short](includes/prod_short.md)]. Si l’URL de redirection sur la page Configuration marketing est vide, recherchez l’URL de redirection suggérée sur la page **Configuration assistée de la connexion à la messagerie**.

    > [!NOTE]
    > Si vous ne spécifiez pas l’URL de redirection, vous pouvez le faire plus tard en choisissant **Ajouter une plateforme**, puis en choisissant **Web** pour ajouter l’application Web et l’URL de redirection. 

3. Sous **Gérer**, choisissez **Manifeste**.
4. Localisez la propriété **requiredResourceAccess** dans le manifeste et ajoutez le code suivant entre crochets ([]) pour ajouter les autorisations requises. Pour plus d’informations, reportez-vous à [Enregistrer votre application](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth#register-your-application).

```
{
    "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    "resourceAccess": [
        {
            "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
            "type": "Scope"
        },
        {
            "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
            "type": "Role"
        }
    ]
}
```

5. Choisissez **Enregistrer**.
6. Sous **Gérer**, choisissez **Autorisations API**, puis confirmez que les autorisations suivantes sont répertoriées :  

    * EWS.AccessAsUser.All
    * full_access_as_app

7. Sous **Gérer**, choisissez **Certificats et secrets**, puis créez un nouveau secret pour votre application. Vous utiliserez le secret dans [!INCLUDE[prod_short](includes/prod_short.md)], dans le champ **Secret client** sur la page **Configuration marketing**, ou stockez-le dans un stockage sécurisé et fournissez-le à un souscripteur d’événements.
8. Choisissez **Aperçu**, puis recherchez la valeur **ID application (client)**. La valeur **ID de l’application (client)** est l’ID client de votre application. Vous devez saisir l’ID client soit sur la **page Configuration marketing**, dans le champ **ID client** ou stockez-le dans un stockage sécurisé et fournissez-le à un souscripteur d’événements.
9. Dans [!INCLUDE[prod_short](includes/prod_short.md)], configurez la journalisation des e-mails sur la page **Configuration marketing** ou utilisez le guide d’assistance au processus **Configuration assistée de la connexion à la messagerie**.
    * Fournissez l’adresse e-mail de l’utilisateur pour le compte duquel la tâche planifiée va se connecter à Exchange Online et traiter les e-mails. L’utilisateur doit avoir une licence valide pour Exchange Online.
    * Fournissez l’URL de votre Exchange Online. En règle générale, il s’agit du domaine que vous avez spécifié dans l’adresse e-mail de l’utilisateur.
    * Indiquez les champs **Chemin d’accès dossier attente** et **Chemin d’accès au dossier de stockage**.
10. Pour commencer à enregistrer les e-mails, activez le bouton bascule **Activé**.
11. Connectez-vous avec votre compte administrateur pour Azure Active Directory (ce compte doit avoir une licence valide pour Echange et être administrateur dans votre environnement Exchange Online). Une fois connecté, vous devez autoriser votre application enregistrée à se connecter à Exchange Online au nom de l’organisation. Vous devez donner votre accord pour terminer la configuration.

   > [!NOTE]
   > Si vous n’êtes pas invité à vous connecter avec votre compte administrateur, c’est probablement parce que les fenêtres contextuelles sont bloquées. Pour vous connecter, autorisez les fenêtres contextuelles de https://login.microsoftonline.com.

## [Nouvelle expérience](#tab/new-experience)
1. Dans le portail Azure, sous **Gérer**, choisissez **Authentification**.
2. Sous **Rediriger les URL**, ajoutez l’URL de redirection suggérée sur la page de **Connexion à la messagerie** dans [!INCLUDE[prod_short](includes/prod_short.md)]. Si le champ de l’URL de redirection sur la page Connexion à la messagerie est vide, recherchez l’URL de redirection suggérée sur la page **Configuration assistée**. Pour ouvrir la page, sur la page **Connexion à la messagerie**, choisissez **Actions**, puis **Configuration assistée**.

    > [!NOTE]
    > Si vous ne spécifiez pas l’URL de redirection, vous pouvez le faire plus tard en choisissant **Ajouter une plateforme**, puis en choisissant **Web** pour ajouter l’application Web et l’URL de redirection.

3. Sous **Gérer**, choisissez **Autorisations API**, et choisissez **Microsoft Graph**, puis **Autorisations déléguées**.
4. Utilisez le champ de recherche pour trouver et sélectionner **Courrier**, puis ajoutez l’autorisation **Mail.ReadWrite.Shared**. 
5. Sous **Gérer**, choisissez **Certificats et secrets**, puis créez un nouveau secret pour votre application. Vous utiliserez le secret soit dans le champ **Secret client** de la page **Connexion à la messagerie** dans [!INCLUDE[prod_short](includes/prod_short.md)].
6. Choisissez **Aperçu**, puis recherchez la valeur **ID application (client)**. Il s’agit de l’ID client de votre application. Vous devez le saisir dans le champ **ID client** de la page **Connexion à la messagerie**.
7. Dans [!INCLUDE[prod_short](includes/prod_short.md)], configurez la connexion à la messagerie sur la page **Connexion à la messagerie** ou utilisez le guide d’assistance **Configuration assistée**.

### Utiliser un autre service de gestion des identités et des accès
Si vous n’utilisez pas Azure Active Directory pour gérer les identités et les accès, vous aurez besoin de l’aide d’un développeur. Si vous préférez stocker l’ID d’application et le secret dans un emplacement différent, vous pouvez laisser les champs ID client et Secret client vides et écrire une extension pour récupérer l’ID et le secret depuis l’emplacement. Vous pouvez fournir le secret lors de l’exécution en vous abonnant aux événements OnGetEmailLoggingClientId et OnGetEmailLoggingClientSecret dans codeunit 1641 « Configuration de la connexion à la messagerie ».

---

## Pour démarrer la connexion à la messagerie
1. Pour commencer à enregistrer les e-mails, sur la page **Connexion à la messagerie**, activez le bouton de basculement **Activé**.
2. Connectez-vous à l’aide d’un compte Exchange Online que la tâche planifiée va utiliser le compte pour se connecter à une boîte aux lettres partagée et traiter les e-mails.

    > [!NOTE]
    > Si vous n’êtes pas invité à vous connecter avec votre compte Exchange Online , c’est probablement parce que les fenêtres contextuelles sont bloquées. Pour vous connecter, autorisez les fenêtres contextuelles de https://login.microsoftonline.com.

## Pour arrêter la connexion à la messagerie
## [Expérience actuelle](#tab/current-experience)
1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration marketing**, puis choisissez le lien associé.
1. Désactivez le bouton bascule **Activé**.

## [Nouvelle expérience](#tab/new-experience)
1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Connexion à la messagerie**, puis sélectionnez le lien associé.
2. Désactivez le bouton bascule **Activé**.

---

## Pour modifier le compte utilisateur utilisé pour la connexion à la messagerie
Si vous utilisez la nouvelle expérience, vous pouvez modifier le compte utilisateur utilisé pour la connexion à la messagerie. L’expérience actuelle ne le supporte pas.

## [Expérience actuelle](#tab/current-experience) 
Désactivez votre configuration actuelle, modifiez l’utilisateur sur la page **Connexion à la messagerie**, puis réactivez la connexion à la messagerie. Vous pouvez également exécuter à nouveau un guide de configuration assistée.

## [Nouvelle expérience](#tab/new-experience)
### [!INCLUDE[prod_short](includes/prod_short.md)] Online
1. Connectez-vous à [!INCLUDE[prod_short](includes/prod_short.md)] avec le compte utilisé par la tâche planifiée pour se connecter à une boîte aux lettres partagée et traiter les e-mails. Ce compte doit avoir accès à [!INCLUDE[prod_short](includes/prod_short.md)] et Exchange Online.
2. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Connexion à la messagerie**, puis sélectionnez le lien associé. 
3. Choisissez **En rapport**, puis **Écriture file d’attente des travaux**.
4. Redémarrez la tâche de **Connexion à la messagerie**.

### [!INCLUDE[prod_short](includes/prod_short.md)] sur site
1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Connexion à la messagerie**, puis sélectionnez le lien associé. 
2. Choisissez **Actions**, puis **Renouveler le jeton**.
3. Connectez-vous à l’aide d’un compte Exchange Online que la tâche planifiée va utiliser le compte pour se connecter à une boîte aux lettres partagée et traiter les e-mails.



## Voir aussi
[Gestion des relations](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]