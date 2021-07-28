---
title: Se connecter à Microsoft Dataverse
description: Configurez une connexion entre Business Central et Dataverse. Ln règle générale, les entreprises créent la connexion pour intégrer les données avec une autre application métier Dynamics 365.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: a29fb1e0a8e10e91a811914a9188548149d5125a
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441358"
---
# <a name="connect-to-microsoft-dataverse"></a>Se connecter à Microsoft Dataverse

[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Cette rubrique décrit comment configurer une connexion entre [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. En règle générale, les entreprises créent la connexion pour intégrer et synchroniser des données avec une autre application métier Dynamics 365 telle que [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Avant de commencer

Avant de créer la connexion, quelques informations doivent être préparées :  

* L’URL pour l’environnement [!INCLUDE[cds_long_md](includes/cds_long_md.md)] auquel vous souhaitez vous connecter. Si vous utilisez le guide de configuration assistée **Paramétrage de la connexion Dataverse** pour créer la connexion, nous découvrirons vos environnements, mais vous pouvez également saisir l’URL d’un autre environnement dans votre abonné.  
* Le nom d’utilisateur et le mot de passe d’un compte ayant les autorisations administrateur dans [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Si vous avez une vague de lancement 1 de 2020 [!INCLUDE[prod_short](includes/prod_short.md)] sur site, version 16.5, lisez l’article [Quelques problèmes connus](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Vous devrez effectuer la solution de contournement décrite avant de pouvoir créer votre connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* La devise société de l′entreprise dans [!INCLUDE[prod_short](includes/prod_short.md)] doit être identique à la devise de la transaction de base dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Une fois une transaction de base définie dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)], elle ne peut pas être changée. Pour plus d′informations, voir [Entité de devise de transaction (devise)](/powerapps/developer/data-platform/transaction-currency-currency-entity). Autrement dit, toutes les entreprises [!INCLUDE[prod_short](includes/prod_short.md)] que vous connectez à une organisation [!INCLUDE[cds_long_md](includes/cds_long_md.md)] doivent utiliser la même devise.

> [!IMPORTANT]
> Votre environnement [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ne doit pas être en mode Administration. Le mode Administration entraînera l’échec de la connexion car le compte d’utilisateur d’intégration pour la connexion ne dispose pas des autorisations d’administrateur. Pour plus d’informations, voir [Mode Administration](/power-platform/admin/admin-mode).

> [!Note]
> Ces étapes décrivent la procédure pour la version en ligne de [!INCLUDE[prod_short](includes/prod_short.md)].
> Si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] sur site et que vous n’utilisez pas de compte Azure Active Directory pour vous connecter à [!INCLUDE [cds_long_md](includes/cds_long_md.md)], vous devez également spécifier un nom d’utilisateur et un mot de passe d’un compte d’utilisateur pour l’intégration. Ce compte est appelé le compte « d’utilisateur d’intégration ». Si vous utilisez un compte Azure Active Directory, le compte d’utilisateur d’intégration n’est pas requis ou affiché. L’utilisateur d’intégration sera configuré automatiquement et ne nécessite pas de licence.

## <a name="set-up-a-connection-to-cds_long_md"></a>Configurer une connexion vers [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

Pour tous les types d’authentification autres que l’authentification Microsoft 365, configurez votre connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] sur la page **Paramétrage de la connexion Dataverse**. Pour l’authentification Microsoft 365, il est recommandé d’utiliser le guide de configuration assistée **Configurer la connexion Dataverse**. Le guide facilite la configuration de la connexion et spécifie les fonctions avancées telles que le modèle de propriété et la synchronisation initiale.  

> [!IMPORTANT]
> Pendant la configuration de la connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)], l’administrateur sera invité à accorder les autorisations suivantes à l’application Azure enregistrée nommée [!INCLUDE[prod_short](includes/prod_short.md)] Intégration à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] :
>
> * **Accédez à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] étant donné que votre** autorisation est nécessaire afin que [!INCLUDE[prod_short](includes/prod_short.md)] puisse, au nom de l’administrateur, créer automatiquement un utilisateur d’application d’intégration [!INCLUDE[prod_short](includes/prod_short.md)] sans licence non interactive, attribuer des rôles de sécurité à cet utilisateur et déployer [!INCLUDE[prod_short](includes/prod_short.md)] la solution d’intégration à [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Cette autorisation n’est utilisée qu’une seule fois pendant la configuration de la connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * **Avoir un accès complet à Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** une autorisation est nécessaire donc [!INCLUDE[prod_short](includes/prod_short.md)] l’utilisateur d’application d’intégration créé automatiquement peut accéder aux données [!INCLUDE[prod_short](includes/prod_short.md)] qui seront synchronisées.  
> * Une autorisation **Connectez-vous et lisez votre profil** est nécessaire pour vérifier que l’utilisateur qui se connecte a bien le rôle de sécurité Administrateur système affecté dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> En donnant son consentement au nom de l’organisation, l’administrateur autorise l’application Azure enregistrée appelée [!INCLUDE[prod_short](includes/prod_short.md)] Intégration à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] à synchroniser les données en utilisant les informations d’identification de l’utilisateur d’application d’intégration [!INCLUDE[prod_short](includes/prod_short.md)] automatiquement créé.

### <a name="to-use-the-dataverse-connection-setup-assisted-setup-guide"></a>Pour utiliser le guide de configuration assistée Paramétrage de la connexion Dataverse
Le guide de configuration de connexion Dataverse peut faciliter la connexion des applications et peut même vous aider à exécuter une synchronisation initiale. Si vous choisissez d’exécuter la synchronisation initiale, [!INCLUDE[prod_short](includes/prod_short.md)] examinera les données des deux applications et fournira des recommandations sur la manière d’aborder la synchronisation initiale. Le tableau suivant décrit les recommandations.

|Recommandation  |Description  |
|---------|---------|
|**Synchronisation complète**|Les données existent uniquement dans [!INCLUDE[prod_short](includes/prod_short.md)], ou seulement dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. La recommandation consiste à synchroniser toutes les données du service vers l’autre service.|
|**Aucune synchronisation**|Les données existent dans les deux applications et une synchronisation complète dupliquerait les données. La recommandation consiste à coupler les enregistrements.|
|**Dépendance non satisfaite**|Les données existent dans les deux applications, mais la ligne ou la table ne peut pas être synchronisée, car elle dépend d’une ligne ou d’une table qui a la recommandation Aucune synchronisation. Par exemple, si les clients ne peuvent pas être synchronisés, les données des contacts qui dépendent des données client ne peuvent pas non plus être synchronisées.|

> [!IMPORTANT]
> En règle générale, vous n’utilisez la synchronisation complète que lorsque vous intégrez les applications pour la première fois et qu’une seule application contient des données. La synchronisation complète peut être utile dans un environnement de démonstration, car elle crée et couple automatiquement des enregistrements dans chaque application, ce qui accélère le travail avec des données synchronisées. Cependant, vous devez exécuter une synchronisation complète uniquement si vous souhaitez une ligne dans [!INCLUDE[prod_short](includes/prod_short.md)] pour chaque ligne dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)] pour les mappages de table donnés. Sinon, le résultat peut être des enregistrements en double.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration assistée**, puis choisissez le lien associé.
2. Sélectionnez **Configurer la connexion à Microsoft Dataverse** pour lancer le guide de configuration assistée.
3. Renseignez les champs selon vos besoins.

> [!NOTE]
> Si vous n’êtes pas invité à vous connecter avec votre compte administrateur, c’est probablement parce que les fenêtres contextuelles sont bloquées. Pour vous connecter, autorisez les fenêtres contextuelles de `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Pour créer ou conserver manuellement la connexion

La procédure suivante décrit comment configurer manuellement la connexion sur la page **Paramétrage de la connexion Dataverse**. Il s’agit également de la page sur laquelle vous gérez les paramètres pour l’intégration.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration de la connexion Dataverse**, puis choisissez le lien associé.
2. Saisissez les informations suivantes pour la connexion de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] vers [!INCLUDE[prod_short](includes/prod_short.md)].

    |Champ|Description|
    |-----|-----|
    |**URL Environnement**|Si vous possédez des environnements dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)], nous les trouverons lorsque vous exécuterez le guide de configuration. Si vous souhaitez vous connecter à un autre environnement dans un autre abonné, vous pouvez saisir les informations d’identification administrateur pour l’environnement et nous les découvrirons. |
    |**Activé**|Commencez avec l’intégration. Si vous n’activez pas la connexion tout de suite, les paramètres de connexion seront sauvegardés, mais les utilisateurs ne seront pas en mesure d’accéder aux données [!INCLUDE[cds_long_md](includes/cds_long_md.md)] à partir de [!INCLUDE[prod_short](includes/prod_short.md)]. Vous pouvez revenir sur cette page et activer la connexion ultérieurement.  |

3. Dans le champ **Modèle de propriété**, choisissez si vous souhaitez une table Équipe dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)] pour posséder de nouveaux enregistrements, ou un ou plusieurs utilisateurs spécifiques. Si vous choisissez **Personne**, vous devez indiquer chaque utilisateur. Si vous choisissez **Équipe**, le centre de profit par défaut s’affiche dans le champ **Centre de profit couplé**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

    <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field-->|
4. Pour tester les paramètres de connexion, choisissez **Connexion**, puis **Tester la connexion**.  

    > [!NOTE]  
    > Si le chiffrement des données n’est pas activé dans [!INCLUDE[prod_short](includes/prod_short.md)], vous recevrez un message vous demandant si vous souhaitez l’activer. Pour activer le chiffrement des données, cliquez sur **Oui** et fournissez les informations requises. Sinon, sélectionnez **Non**. Vous pouvez activer le chiffrement des données ultérieurement. Pour plus d’informations, voir [Chiffrement des données dans Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) de l’aide sur Developer and Administration.  
5. Si la synchronisation de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] n’est pas déjà configurée, vous recevrez un message vous demandant si vous souhaitez utiliser les paramètres de synchronisation par défaut. Selon que vous souhaitez conserver ou non les enregistrements alignés dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)] et [!INCLUDE[prod_short](includes/prod_short.md)], sélectionnez **Oui** ou **Non**.

<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="upgrade-connections-from-business-central-online-to-use-certificate-based-authentication"></a>Mettre à niveau les connexions de Business Central Online pour utiliser l’authentification basée sur les certificats
> [!NOTE]
> Cette section s’applique uniquement aux locataires Business Central Online par Microsoft. Les locataires en ligne hébergés par les développeurs de logiciels indépendants et les installations locales ne sont pas affectés.

En avril 2022, [!INCLUDE[cds_long_md](includes/cds_long_md.md)] désapprouve le type d’authentification Office365 (nom d’utilisateur/mot de passe). Pour en savoir plus, voir [ Abandon du type d’authentification Office365](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). De plus, en mars 2022, [!INCLUDE[prod_short](includes/prod_short.md)] abandonne l’utilisation de l’authentification service à service basée sur le secret client pour les locataires en ligne, et nécessitera l’utilisation de l’authentification service à service basée sur un certificat pour les connexions à [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Les locataires en ligne [!INCLUDE[cds_long_md](includes/cds_long_md.md)] hébergés par les éditeurs de logiciels indépendants et les installations locales peuvent continuer à utiliser l’authentification Office365 configurée par leur partenaire Microsoft.

Pour éviter de perturber les intégrations, _vous devez mettre à niveau_ la connexion pour utiliser l’authentification par certificat. Bien que le changement soit prévu pour mars 2022, nous vous recommandons fortement de mettre à niveau dès que possible. Les étapes suivantes décrivent comment effectuer une mise à niveau vers l’authentification par certificat. 

### <a name="to-upgrade-your-business-central-online-connection-to-use-certificate-based-authentication"></a>Pour mettre à niveau votre connexion de Business Central Online pour utiliser l’authentification basée sur les certificats
> [!NOTE]
> L’authentification basée sur les certificats est disponible dans la 1ère vague de lancement Business Central 2021 et versions ultérieures. Si vous utilisez une version antérieure, vous devez planifier une mise à jour vers la première vague de la version de Business Central 2021 avant mars 2022. Pour plus d’informations, consultez [Planification des mises à jour](/dynamics365/business-central/dev-itpro/administration/update-rollout-timeline#scheduling-updates). Si vous rencontrez des problèmes, contactez votre partenaire ou l’assistance.

1. Dans le [Centre d’administration Business Central]/dynamics365/business-central/dev-itpro/administration/tenant-admin-center), vérifiez que vous utilisez la 1ère vague de lancement Business Central 2021 ou versions ultérieures (version 18 ou ultérieure).
2. Selon que vous intégrez ou non à Dynamics 365 Sales, effectuez l’une des opérations suivantes :
   * Si vous le faites, ouvrez la page **Configuration de la connexion Microsoft Dynamics 365**.
   * Si vous ne le faites pas, ouvrez la page **Configuration de la connexion Dataverse**.
3. Choisissez **Connexion**, puis **Utiliser l’authentification par certificat** pour mettre à niveau la connexion afin d’utiliser l’authentification basée sur un certificat.
4. Connectez-vous avec les informations d’identification d’administrateur pour Dataverse. La connexion devrait prendre moins d’une minute.

> [!NOTE]
> Vous devez répéter ces étapes dans chaque environnement [!INCLUDE[prod_short](includes/prod_short.md)], y compris les environnements de production et de bac à sable, et dans chaque entreprise où vous êtes connecté à [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

## <a name="connecting-on-premises-versions"></a>Connexion des versions locales

Pour connecter [!INCLUDE[prod_short](includes/prod_short.md)] sur site à [!INCLUDE[cds_long_md](includes/cds_long_md.md)], vous devez spécifier quelques informations sur la page **Configuration de la connexion Dataverse**.

Si vous souhaitez vous connecter à l’aide d’un compte Azure Active Directory (Azure AD), vous devez enregistrer une application dans Azure AD et fournir l’ID d’application, le secret Key Vault et l’URL de redirection à utiliser. L’URL de redirection est pré-remplie et devrait fonctionner pour la plupart des installations. Vous devez configurer votre installation pour utiliser HTTPS. Pour plus d’informations, voir [Configuration de SSL pour sécuriser la connexion du client Web Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Si vous configurez votre serveur pour avoir une page d’accueil différente, vous pouvez toujours changer l’URL. Le secret client sera enregistré sous forme de chaîne cryptée dans votre base de données. 

### <a name="prerequisites"></a>Conditions préalables

Dataverse doit utiliser l′un des types d′authentification suivants :

* Office365 (hérité)

  > [!IMPORTANT]
  > À compter d′avril 2022, Office365 (hérité) ne sera plus pris en charge. Pour plus d′informations, consultez [Modifications importantes (déconseillées) à venir dans Power Apps, Power Automate et les applications d′engagement client](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).
* Office365 (moderne, basé sur le secret client OAuth2)
* OAuth

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-dataverse"></a>Pour enregistrer une application dans Azure AD pour se connecter de Business Central à Dataverse

Les étapes suivantes supposent que vous utilisez Azure AD pour gérer les identités et les accès. Pour plus d’informations sur l’enregistrement d’une application dans Azure AD, voir [Démarrage rapide : enregistrer une application avec la plateforme d’identité Microsoft](/azure/active-directory/develop/quickstart-register-app). 

1. Dans le portail Azure, sous **Gérer** dans le volet de navigation, choisissez **Authentification**.  
2. Sous **Rediriger les URL**, ajoutez l’URL de redirection suggérée sur la page de **Configuration de la connexion Dataverse** dans [!INCLUDE[prod_short](includes/prod_short.md)].
3. Sous **Gérer**, choisissez **Autorisations d’API**.
4. Sous **Autorisations configurées**, choisissez **Ajouter une autorisation**, puis ajoutez des autorisations déléguées sur l’onglet **API Microsoft** comme suit :
    * Pour Business Central, ajoutez les autorisations **Financials.ReadWrite.All**.
    * Pour Dynamics CRM, ajoutez les autorisations **user_impersonation**.  

    > [!NOTE]
    > Le nom de l’API Dynamics CRM peut changer.

5. Sous **Gérer**, choisissez **Certificats et secrets**, puis créez un nouveau secret pour votre application. Vous utiliserez le secret soit dans [!INCLUDE[prod_short](includes/prod_short.md)], dans le champ **Secret client** sur la page **Configuration de la connexion Dataverse** ou stockez-le dans un stockage sécurisé et fournissez-le dans un souscripteur d’événements, comme décrit précédemment dans cette rubrique.
6. Choisissez **Aperçu**, puis recherchez la valeur **ID application (client)**. Il s’agit de l’ID client de votre application. Vous devez le saisir soit sur la page **Configuration de la connexion Dataverse** dans le champ **ID client** ou stockez-le dans un stockage sécurisé et fournissez-le à un souscripteur d’événements.
7. Dans [!INCLUDE[prod_short](includes/prod_short.md)], sur la page **Configuration de la connexion Dataverse**, dans le champ **URL Environnement**, saisissez l’URL de votre environnement [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
8. Pour activer la connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)], activez le bouton bascule **Activé**.
9. Connectez-vous avec votre compte administrateur pour Azure Active Directory (ce compte doit avoir une licence valide pour [!INCLUDE[cds_long_md](includes/cds_long_md.md)] et être administrateur dans votre environnement [!INCLUDE[cds_long_md](includes/cds_long_md.md)]). Une fois connecté, vous serez invité à autoriser votre application enregistrée à se connecter à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] au nom de l’organisation. Vous devez donner votre accord pour terminer la configuration.

   > [!NOTE]
   > Si vous n’êtes pas invité à vous connecter avec votre compte administrateur, c’est probablement parce que les fenêtres contextuelles sont bloquées. Pour vous connecter, autorisez les fenêtres contextuelles de `https://login.microsoftonline.com`.

### <a name="to-disconnect-from-cds_long_md"></a>Pour se déconnecter de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration de la connexion Dataverse**, puis choisissez le lien associé.
2. Sur la page **Paramétrage de la connexion Dataverse**, désactivez le bouton bascule **Activé**.  

## <a name="see-also"></a>Voir aussi

[Afficher le statut d’une synchronisation](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]