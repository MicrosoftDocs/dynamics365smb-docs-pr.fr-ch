---
title: Config. identifiant messagerie | Microsoft Docs
description: Apprenez à transformer les interactions de messagerie entre les vendeurs et les clients en véritables opportunités de vente.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 59e5a37bc24c78ea9af9f5d518b98c2ada7764a4
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/04/2022
ms.locfileid: "8382640"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Suivre les échanges de messages électroniques entre les vendeurs et les contacts

Tirez le meilleur parti des communications entre les vendeurs et vos clients existants ou potentiels en suivant les échanges de courriers électroniques, puis en les transformant en opportunités exploitables. [!INCLUDE[prod_short](includes/prod_short.md)] peut utiliser Exchange Online pour conserver un journal des messages entrants et sortants. Vous pouvez afficher et analyser le contenu de chaque message sur la page **Écritures journal interaction**.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Configurer les dossiers publics et les règles de connexion à la messagerie dans Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Ensuite, vous connectez [!INCLUDE[prod_short](includes/prod_short.md)] à Exchange Online.

## <a name="setting-up-prod_short-to-log-email-messages"></a>Configuration de [!INCLUDE[prod_short](includes/prod_short.md)] pour enregistrer les messages électroniques

Commencez avec la connexion à la messagerie en deux étapes :

1. Connectez [!INCLUDE[prod_short](includes/prod_short.md)] à Exchange Online pour votre abonnement Microsoft 365. Exchange Online gère vos e-mails. Nous avons facilité cette étape en fournissant un guide de configuration assisté. Vous avez juste besoin de vos identifiants d’administrateur pour votre compte d’administrateur dans Microsoft 365. Pour commencer le guide, accédez à la page **Configuration assistée**, puis sélectionnez le guide **Configurer la journalisation des emails**.  

2. Assurez-vous que des adresses électroniques valides ont été entrées dans [!INCLUDE[prod_short](includes/prod_short.md)] pour vos commerciaux et vos contacts, selon qu’ils sont des clients potentiels ou existants. Pour ce faire, pour chaque client ou vendeur, ouvrez la fiche **Contact** ou **Vendeur/Acheteur** et regardez le champ **E-mail**.

> [!Tip]
> Une fois les étapes du guide terminées, vous pouvez vérifier si la connexion a réussi. Recherchez **Paramètres marketing**, **Accéder**, puis **Fonctions** et **Valider la configuration de la connexion à la messagerie**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Affichage des échanges de messages électroniques dans le journal des interactions

[!INCLUDE[prod_short](includes/prod_short.md)] crée une entrée sur la page **Journal des interactions** chaque fois qu’un vendeur et un contact échangent un message par courrier électronique. Pour afficher le journal des interactions, ouvrez la fiche **Contact** pour la personne, puis choisissez **Association**, **Historique**, et **Écritures feuille interaction**. Vous pouvez faire certaines choses avec chaque entrée de la feuille, par exemple :

- Affichez le contenu du message électronique échangé en sélectionnant **Traitement**, puis **Afficher les Documents joints**.
- Transformez un échange de courrier électronique en opportunité de vente. Si une entrée semble prometteuse, vous pouvez la transformer en opportunité, puis gérer son évolution vers une vente. Pour ce faire, sélectionnez l’écriture, **Traitement**, puis **Créer opportunité**. Pour plus d’informations, voir [Gérer des opportunités de vente](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>Connexion des versions locales à Microsoft Exchange

Vous pouvez vous connecter à [!INCLUDE[prod_short](includes/prod_short.md)] sur site vers Exchange sur site ou Exchange Online pour la connexion à la messagerie. Pour les deux versions d’Exchange, les paramètres de connexion sont disponibles sur la page **Configuration marketing**. Pour Exchange Online, vous pouvez également utiliser un guide de configuration assistée.

### <a name="connecting-to-exchange-on-premises"></a>Connexion à Exchange sur site

Pour connecter [!INCLUDE[prod_short](includes/prod_short.md)] sur site à Exchange sur site, sur la page **Configuration marketing**, vous pouvez utiliser **De base** comme **Type d’identification**, puis entrez les informations d’identification pour le compte d’utilisateur pour Exchange sur site. Puis activez le bouton bascule **Activé** pour commencer à enregistrer les e-mails.

### <a name="connecting-to-exchange-online"></a>Connexion à Exchange Online

Pour se connecter à Exchange Online, vous devez utiliser **OAuth2** comme **Type d’identification**. Vous devez également enregistrer une application dans Azure Active Directory et fournir l’ID d’application, le secret Key Vault et l’URL de redirection à utiliser. L’URL de redirection est pré-remplie et devrait fonctionner pour la plupart des installations. Pour plus d’informations, consultez Pour enregistrer une application dans Azure AD pour se connecter de Business Central à Exchange Online ci-dessous.

Vous devez configurer votre installation pour utiliser HTTPS. Pour plus d’informations, voir [Configuration de SSL pour sécuriser la connexion du client Web Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Si vous configurez votre serveur pour avoir une page d’accueil différente, vous pouvez changer l’URL. Le secret client sera enregistré sous forme de chaîne cryptée dans votre base de données.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Pour enregistrer une application dans Azure AD pour se connecter de Business Central à Exchange Online

Les étapes suivantes supposent que vous utilisez Azure Active Directory pour gérer les identités et les accès. Pour plus d’informations, voir [Démarrage rapide : enregistrer une application avec la plateforme d’identité Microsoft](/azure/active-directory/develop/quickstart-register-app). Si vous n’utilisez pas Azure Active Directory, voir [Utilisation d’un autre service de gestion des identités et des accès](marketing-set-up-email-logging.md#using-another-identity-and-access-management-service). 

1. Dans le portail Azure, sous **Gérer**, choisissez **Authentification**.
2. Sous **Rediriger les URL**, ajoutez l’URL de redirection suggérée sur la page de **Configuration marketing** dans [!INCLUDE[prod_short](includes/prod_short.md)]. Si l’URL de redirection sur la page Configuration marketing est vide, recherchez l’URL de redirection suggérée sur la page **Configuration assistée de la connexion à la messagerie**.

    > [!NOTE]
    > Si vous ne spécifiez pas l’URL de redirection, vous pouvez le faire plus tard en choisissant **Ajouter une plateforme**, puis en choisissant **Web** pour ajouter l’application Web et l’URL de redirection. 

3. Sous **Gérer**, choisissez **Manifeste**.
4. Localisez la propriété **requiredResourceAccess** dans le manifeste et ajoutez le code suivant entre crochets ([]) pour ajouter les autorisations requises. Pour plus d’informations, reportez vous à [Enregistrer votre application](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth#register-your-application).

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
8. Choisissez **Aperçu**, puis recherchez la valeur **ID application (client)**. Il s’agit de l’ID client de votre application. Vous devez le saisir soit sur la **page Configuration marketing**, dans le champ **ID client** ou stockez-le dans un stockage sécurisé et fournissez-le à un souscripteur d’événements.
9. Dans [!INCLUDE[prod_short](includes/prod_short.md)], configurez la journalisation des e-mails sur la page **Configuration marketing** ou utilisez le guide d’assistance au processus **Configuration assistée de la connexion à la messagerie**.
    * Fournissez l’adresse e-mail de l’utilisateur pour le compte duquel la tâche planifiée va se connecter à Exchange Online et traiter les e-mails. L’utilisateur doit avoir une licence valide pour Exchange Online.
    * Fournissez l’URL de votre Exchange Online. En règle générale, il s’agit du domaine que vous avez spécifié dans l’adresse e-mail de l’utilisateur.
    * Indiquez les champs **Chemin d’accès dossier attente** et **Chemin d’accès au dossier de stockage**.
10. Pour commencer à enregistrer les e-mails, activez le bouton bascule **Activé**.
11. Connectez-vous avec votre compte administrateur pour Azure Active Directory (ce compte doit avoir une licence valide pour Echange et être administrateur dans votre environnement Exchange Online). Une fois connecté, vous serez invité à autoriser votre application enregistrée à se connecter à Exchange Online au nom de l’organisation. Vous devez donner votre accord pour terminer la configuration.

   > [!NOTE]
   > Si vous n’êtes pas invité à vous connecter avec votre compte administrateur, c’est probablement parce que les fenêtres contextuelles sont bloquées. Pour vous connecter, autorisez les fenêtres contextuelles de https://login.microsoftonline.com.

### <a name="using-another-identity-and-access-management-service"></a>Utilisation d’un autre service de gestion des identités et des accès
Si vous n’utilisez pas Azure Active Directory pour gérer les identités et les accès, vous aurez besoin de l’aide d’un développeur. Si vous préférez stocker l’ID d’application et le secret dans un emplacement différent, vous pouvez laisser les champs ID client et Secret client vides et écrire une extension pour récupérer l’ID et le secret depuis l’emplacement. Vous pouvez fournir le secret lors de l’exécution en vous abonnant aux événements OnGetEmailLoggingClientId et OnGetEmailLoggingClientSecret dans codeunit 1641 « Configuration de la connexion à la messagerie ».

### <a name="to-stop-logging-email"></a>Pour arrêter la connexion à la messagerie
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration marketing**, puis choisissez le lien associé.
2. Désactivez le bouton bascule **Activé**.

## <a name="see-also"></a>Voir aussi
[Gestion des relations](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]