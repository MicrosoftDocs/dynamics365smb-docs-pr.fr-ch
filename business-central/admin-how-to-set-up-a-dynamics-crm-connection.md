---
title: Se connecter à Common Data Service | Microsoft Docs
description: Vous pouvez intégrer d’autres applications à Business Central au moyen de Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 51f04f690483fd5b0c3f093ac5f8e2694ca3fdd9
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924643"
---
# <a name="connect-to-common-data-service"></a>Se connecter à Common Data Service

Cette rubrique décrit comment configurer une connexion entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. En règle générale, les entreprises créent la connexion pour intégrer et synchroniser des données avec une autre application métier Dynamics 365 telle que [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Avant de commencer

Avant de créer la connexion, quelques informations doivent être préparées :  

* L’URL pour l’environnement [!INCLUDE[cds_long_md](includes/cds_long_md.md)] auquel vous souhaitez vous connecter. Si vous utilisez le guide de configuration assistée **Paramétrage de la connexion CDS** pour créer la connexion, nous découvrirons vos environnements, mais vous pouvez également saisir l’URL d’un autre environnement dans votre abonné.  
* Le nom d’utilisateur et le mot de passe d’un compte ayant les autorisations administrateur dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

> [!Note]
> Ces étapes décrivent la procédure pour la version en ligne de [!INCLUDE[d365fin](includes/d365fin_md.md)].
> Si vous utilisez Business Central sur site et que vous n’utilisez pas de compte Azure Active Directory pour vous connecter à [!INCLUDE [cds_long_md](includes/cds_long_md.md)], vous devez également spécifier un nom d’utilisateur et un mot de passe d’un compte d’utilisateur pour l’intégration. Ce compte est appelé le compte « d’utilisateur d’intégration ». Si vous utilisez un compte Azure Active Directory, le compte d’utilisateur d’intégration n’est pas requis ou affiché. L’utilisateur d’intégration sera configuré automatiquement et ne nécessite pas de licence.

## <a name="set-up-a-connection-to-cds_long_md"></a>Configurer une connexion vers [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

Pour tous les types d’authentification autres que l’authentification Microsoft 365, configurez votre connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] sur la page **Paramétrage de la connexion CDS** . Pour l’authentification Microsoft 365, il est recommandé d’utiliser le guide de configuration assistée **Configurer la connexion Common Data Service** . Le guide facilite la configuration de la connexion et spécifie les fonctions avancées telles que le modèle de propriété et la synchronisation initiale.  

> [!IMPORTANT]
> Pendant la configuration de la connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)], l’administrateur sera invité à accorder les autorisations suivantes à l’application Azure enregistrée nommée [!INCLUDE[d365fin](includes/d365fin_md.md)] Intégration à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] :
>
> * **Accès [!INCLUDE[cds_long_md](includes/cds_long_md.md)] comme vous** une autorisation est nécessaire afin que [!INCLUDE[d365fin](includes/d365fin_md.md)] puisse, au nom de l’administrateur, créer automatiquement un utilisateur d’application d’intégration [!INCLUDE[d365fin](includes/d365fin_md.md)] sans licence non interactive, attribuer des rôles de sécurité à cet utilisateur et déployer [!INCLUDE[d365fin](includes/d365fin_md.md)] la solution d’intégration de base CDS à [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Cette autorisation n’est utilisée qu’une seule fois pendant la configuration de la connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * **Avoir un accès complet à Dynamics 365 [!INCLUDE[d365fin](includes/d365fin_md.md)]** une autorisation est nécessaire donc [!INCLUDE[d365fin](includes/d365fin_md.md)] l’utilisateur d’application d’intégration créé automatiquement peut accéder aux données [!INCLUDE[d365fin](includes/d365fin_md.md)] qui seront synchronisées.  
> * Une autorisation **Connectez-vous et lisez votre profil** est nécessaire pour vérifier que l’utilisateur qui se connecte a bien le rôle de sécurité Administrateur système affecté dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> En donnant son consentement au nom de l’organisation, l’administrateur autorise l’application Azure enregistrée appelée [!INCLUDE[d365fin](includes/d365fin_md.md)] Intégration à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] à synchroniser les données en utilisant les informations d’identification de l’utilisateur d’application d’intégration [!INCLUDE[d365fin](includes/d365fin_md.md)] automatiquement créé.

### <a name="to-use-the-set-up-common-data-service-connection-assisted-setup-guide"></a>Pour utiliser le guide de configuration assistée Configurer la connexion Common Data Service

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration assistée** , puis sélectionnez le lien associé.
2. Sélectionnez **Configurer la connexion Common Data Service** pour lancer le guide de configuration assistée.
3. Renseignez les champs selon vos besoins.

### <a name="to-create-or-maintain-the-connection-manually"></a>Pour créer ou conserver manuellement la connexion

La procédure suivante décrit comment configurer manuellement la connexion sur la page **Paramétrage de la connexion CDS** . Il s’agit également de la page sur laquelle vous gérez les paramètres pour l’intégration.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrage de la connexion CDS** , puis sélectionnez le lien associé.
2. Saisissez les informations suivantes pour la connexion de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)].

    |Champ|Description|
    |-----|-----|
    |**URL Environnement**|Si vous possédez des environnements dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)], nous les trouverons lorsque vous exécuterez le guide de configuration. Si vous souhaitez vous connecter à un autre environnement dans un autre abonné, vous pouvez saisir les informations d’identification administrateur pour l’environnement et nous les découvrirons. |
    |**Activé**|Commencez avec l’intégration. Si vous n’activez pas la connexion tout de suite, les paramètres de connexion seront sauvegardés, mais les utilisateurs ne seront pas en mesure d’accéder aux données [!INCLUDE[cds_long_md](includes/cds_long_md.md)] à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vous pouvez revenir sur cette page et activer la connexion ultérieurement.  |

3. Dans le champ **Modèle de propriété** , choisissez si vous souhaitez une entité Équipe dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)] pour posséder de nouveaux enregistrements, ou un ou plusieurs utilisateurs spécifiques. Si vous choisissez **Personne** , vous devez indiquer chaque utilisateur. Si vous choisissez **Équipe** , le centre de profit par défaut BCI_Company s’affiche dans le champ **Centre de profit couplé** .

    <!--Need to verify the details in this table, are these specific to Sales maybe?-->
    Saisissez les paramètres avancés suivants.

    |Champ|Description|
    |-----|-----|
    |**Les utilisateurs [!INCLUDE[d365fin](includes/d365fin_md.md)] doivent être associés aux utilisateurs CDS**|Si vous utilisez le modèle de propriété Personne, spécifiez si les comptes d’utilisateur [!INCLUDE[d365fin](includes/d365fin_md.md)] doivent avoir des comptes d’utilisateur correspondants dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. **L’adresse électronique pour l’authentification Microsoft 365** de l’utilisateur [!INCLUDE[d365fin](includes/d365fin_md.md)] doit être identique à **l’adresse électronique principale** de l’utilisateur [!INCLUDE[crm_md](includes/crm_md.md)].<br /><br /> Si vous définissez la valeur sur **Oui** , les utilisateurs [!INCLUDE[d365fin](includes/d365fin_md.md)] qui n’ont pas un compte d’utilisateur [!INCLUDE[crm_md](includes/crm_md.md)] correspondant ne disposeront pas de fonctions d’intégration de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans l’interface utilisateur. L’accès aux données [!INCLUDE[crm_md](includes/crm_md.md)] directement à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)] se fait au nom du compte d’utilisateur [!INCLUDE[crm_md](includes/crm_md.md)].<br /><br /> Si vous définissez la valeur sur **Non** , tous les utilisateurs [!INCLUDE[d365fin](includes/d365fin_md.md)] disposeront de fonctions d’intégration de [!INCLUDE[crm_md](includes/crm_md.md)] dans l’interface utilisateur. L’accès aux données [!INCLUDE[crm_md](includes/crm_md.md)] directement à partir de [!INCLUDE[crm_md](includes/crm_md.md)] se fait au nom de l’utilisateur (intégration) de connexion.|
    |**Le vendeur Business Central actuel est associé à un utilisateur**|Indique si votre compte d’utilisateur correspond à un compte dans [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field-->|

4. Pour tester les paramètres de connexion, choisissez **Connexion** , puis **Tester la connexion** .  

    > [!NOTE]  
    > Si le chiffrement des données n’est pas activé dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous recevrez un message vous demandant si vous souhaitez l’activer. Pour activer le chiffrement des données, cliquez sur **Oui** et fournissez les informations requises. Sinon, sélectionnez **Non** . Vous pouvez activer le chiffrement des données ultérieurement. Pour plus d’informations, voir [Chiffrement des données dans Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) de l’aide sur Developer and Administration.  

5. Si la synchronisation de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] n’est pas déjà configurée, vous recevrez un message vous demandant si vous souhaitez utiliser les paramètres de synchronisation par défaut. Selon que vous souhaitez conserver ou non les enregistrements alignés dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)], sélectionnez **Oui** ou **Non** .

## <a name="show-me-the-process"></a>Afficher le processus

La vidéo suivante décrit les étapes pour connecter [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

## <a name="connecting-on-premises-versions"></a>Connexion des versions locales

Pour connecter [!INCLUDE[d365fin](includes/d365fin_md.md)] sur site à [!INCLUDE[cds_long_md](includes/cds_long_md.md)], vous devez spécifier quelques informations sur la page **Configuration de la connexion Common Data Service** .

Si vous souhaitez vous connecter à l’aide d’un compte Azure Active Directory (Azure AD), vous devez enregistrer une application dans Azure AD et fournir l’ID d’application, le secret Key Vault et l’URL de redirection à utiliser. L’URL de redirection est pré-remplie et devrait fonctionner pour la plupart des installations. Vous devez configurer votre installation pour utiliser HTTPS. Pour plus d’informations, voir [Configuration de SSL pour sécuriser la connexion du client Web Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Si vous configurez votre serveur pour avoir une page d’accueil différente, vous pouvez toujours changer l’URL. Le secret client sera enregistré sous forme de chaîne cryptée dans votre base de données.  

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-common-data-service"></a>Pour enregistrer une application dans Azure AD pour se connecter de Business Central à Common Data Service

Les étapes suivantes supposent que vous utilisez Azure AD pour gérer les identités et les accès. Pour plus d’informations sur l’enregistrement d’une application dans Azure AD, voir [Démarrage rapide : enregistrer une application avec la plateforme d’identité Microsoft](/azure/active-directory/develop/quickstart-register-app). Si vous n’utilisez pas Azure AD, voir [Utilisation d’un autre service de gestion des identités et des accès](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-identity-and-access-management-service).  

1. Dans le portail Azure, sous **Gérer** dans le volet de navigation, choisissez **Authentification** .  
2. Sous **Rediriger les URL** , ajoutez l’URL de redirection suggérée sur la page de **Configuration de la connexion Common Data Service** dans [!INCLUDE[d365fin](includes/d365fin_md.md)].
3. Sous **Gérer** , choisissez **Autorisations d’API** .
4. Sous **Autorisations configurées** , choisissez **Ajouter une autorisation** , puis ajoutez des autorisations déléguées sur l’onglet **API Microsoft** comme suit :
    * Pour Business Central, ajoutez les autorisations **Financials.ReadWrite.All** .
    * Pour Dynamics CRM, ajoutez les autorisations **user_impersonation** .  

    > [!NOTE]
    > Le nom de l’API Dynamics CRM peut changer.

5. Sous **Gérer** , choisissez **Certificats et secrets** , puis créez un nouveau secret pour votre application. Vous utiliserez le secret soit dans [!INCLUDE[d365fin](includes/d365fin_md.md)], dans le champ **Secret client** sur la page **Configuration de la connexion Common Data Service** ou stockez-le dans un stockage sécurisé et fournissez-le dans un souscripteur d’événements, comme décrit précédemment dans cette rubrique.
6. Choisissez **Aperçu** , puis recherchez la valeur **ID application (client)** . Il s’agit de l’ID client de votre application. Vous devez le saisir soit sur la page **Configuration de la connexion Common Data Service** dans le champ **ID client** ou stockez-le dans un stockage sécurisé et fournissez-le à un souscripteur d’événements.
7. Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], sur la page **Configuration de la connexion Common Data Service** , dans le champ **URL Environnement** , saisissez l’URL de votre environnement [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
8. Pour activer la connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)], activez le bouton bascule **Activé** .
9. Connectez-vous avec votre compte administrateur pour Azure Active Directory (ce compte doit avoir une licence valide pour [!INCLUDE[cds_long_md](includes/cds_long_md.md)] et être administrateur dans votre environnement [!INCLUDE[cds_long_md](includes/cds_long_md.md)]). Une fois connecté, vous serez invité à autoriser votre application enregistrée à se connecter à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] au nom de l’organisation. Vous devez donner votre accord pour terminer la configuration.

   > [!NOTE]
   > Si vous n’êtes pas invité à vous connecter avec votre compte administrateur, c’est probablement parce que les fenêtres contextuelles sont bloquées. Pour vous connecter, autorisez les fenêtres contextuelles de `https://login.microsoftonline.com`.

#### <a name="using-another-identity-and-access-management-service"></a>Utilisation d’un autre service de gestion des identités et des accès

Si vous n’utilisez pas Azure Active Directory pour gérer les identités et les accès, vous aurez besoin de l’aide d’un développeur. Si vous préférez stocker l’ID d’application et le secret dans un emplacement différent, vous pouvez laisser les champs ID client et Secret client vides et écrire une extension pour récupérer l’ID et le secret depuis l’emplacement. Vous pouvez fournir le secret lors de l’exécution en vous abonnant aux événements OnGetCDSConnectionClientId et OnGetCDSConnectionClientSecret dans codeunit 7201 « CDS Integration Impl. »

### <a name="to-disconnect-from-cds_long_md"></a>Pour se déconnecter de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrage de la connexion CDS** , puis sélectionnez le lien associé.
2. Sur la page **Paramétrage de la connexion CDS** , désactivez le bouton bascule **Activé** .  

## <a name="see-also"></a>Voir aussi

[Afficher le statut d’une synchronisation](admin-how-to-view-synchronization-status.md)  
