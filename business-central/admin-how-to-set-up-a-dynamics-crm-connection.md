---
title: Se connecter à Microsoft Dataverse (contient une vidéo)
description: "Configurez une connexion entre Business\_Central et Dataverse. Ln règle générale, les entreprises créent la connexion pour intégrer les données avec une autre application métier Dynamics\_365."
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.search.forms: '7200, 7201'
ms.date: 03/22/2023
ms.author: bholtorf
---
# <a name="connect-to-microsoft-dataverse"></a><a name="connect-to-microsoft-dataverse"></a>Se connecter à Microsoft Dataverse

Cet article décrit comment configurer une connexion entre [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. En règle générale, les entreprises créent la connexion pour intégrer et synchroniser des données avec une autre application métier Dynamics 365 telle que [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a><a name="before-you-start"></a>Avant de commencer

Avant de créer la connexion, quelques informations doivent être préparées :  

* L’URL pour l’environnement [!INCLUDE[cds_long_md](includes/cds_long_md.md)] auquel vous souhaitez vous connecter. Si vous utilisez le guide de configuration assistée **Configuration de la connexion Dataverse** pour créer la connexion, nous trouverons vos environnements. Vous pouvez également entrer l’URL d’un autre environnement dans votre abonné.  
* Le nom d’utilisateur et le mot de passe d’un compte ayant les autorisations administrateur dans [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Si vous avez une vague de lancement 1 de 2020 [!INCLUDE[prod_short](includes/prod_short.md)] sur site, version 16.5, lisez l’article [Quelques problèmes connus](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Vous devrez effectuer la solution de contournement décrite avant de pouvoir créer votre connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* La devise société de l′entreprise dans [!INCLUDE[prod_short](includes/prod_short.md)] doit être identique à la devise de la transaction de base dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Après avoir effectué une transaction dans la devise de base dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)], vous ne pouvez pas la modifier. Pour plus d′informations, voir [Entité de devise de transaction (devise)](/powerapps/developer/data-platform/transaction-currency-currency-entity). Toutes les sociétés [!INCLUDE[prod_short](includes/prod_short.md)] que vous connectez à une organisation [!INCLUDE[cds_long_md](includes/cds_long_md.md)] doivent utiliser la même devise.

> [!IMPORTANT]
> Votre environnement [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ne doit pas être en mode Administration. Le mode Administration entraînera l’échec de la connexion car le compte d’utilisateur d’intégration pour la connexion ne dispose pas des autorisations d’administrateur. Pour plus d’informations, voir [Mode Administration](/power-platform/admin/admin-mode).

> [!Note]
> Ces étapes décrivent la procédure pour la version en ligne de [!INCLUDE[prod_short](includes/prod_short.md)].
> Si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] sur site et que vous n’utilisez pas de compte Azure Active Directory pour vous connecter à [!INCLUDE [cds_long_md](includes/cds_long_md.md)], vous devez également spécifier un nom d’utilisateur et un mot de passe d’un compte d’utilisateur pour l’intégration. Ce compte est appelé le compte « d’utilisateur d’intégration ». Si vous utilisez un compte Azure Active Directory, le compte d’utilisateur d’intégration n’est pas requis ou affiché. L’utilisateur d’intégration sera configuré automatiquement et ne nécessite pas de licence.

## <a name="set-up-a-connection-to-"></a><a name="set-up-a-connection-to-"></a>Configurer une connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

Pour tous les types d’authentification autres que l’authentification Microsoft 365, configurez votre connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] sur la page **Configuration de la connexion Dataverse**. Pour l’authentification Microsoft 365, il est recommandé d’utiliser le guide de configuration assistée **Paramétrage de la connexion Dataverse**. Le guide facilite la configuration de la connexion et spécifie les fonctions avancées telles que le modèle de propriété et la synchronisation initiale.  

> [!IMPORTANT]
> Pendant la configuration de la connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)], l’administrateur sera invité à accorder les autorisations suivantes à l’application Azure enregistrée nommée [!INCLUDE[prod_short](includes/prod_short.md)] Intégration à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] :
>
> * **Accédez à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] étant donné que votre** autorisation est nécessaire afin que [!INCLUDE[prod_short](includes/prod_short.md)] puisse, au nom de l’administrateur, créer automatiquement un utilisateur d’application d’intégration [!INCLUDE[prod_short](includes/prod_short.md)] sans licence non interactive, attribuer des rôles de sécurité à cet utilisateur et déployer [!INCLUDE[prod_short](includes/prod_short.md)] la solution d’intégration à [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Cette autorisation n’est utilisée qu’une seule fois pendant la configuration de la connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * **Avoir un accès complet à Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** une autorisation est nécessaire donc [!INCLUDE[prod_short](includes/prod_short.md)] l’utilisateur d’application d’intégration créé automatiquement peut accéder aux données [!INCLUDE[prod_short](includes/prod_short.md)] qui seront synchronisées.  
> * Une autorisation **Connectez-vous et lisez votre profil** est nécessaire pour vérifier que l’utilisateur qui se connecte a bien le rôle de sécurité Administrateur système affecté dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> En donnant son consentement au nom de l’organisation, l’administrateur autorise l’application Azure enregistrée appelée [!INCLUDE[prod_short](includes/prod_short.md)] Intégration à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] à synchroniser les données en utilisant les informations d’identification de l’utilisateur d’application d’intégration [!INCLUDE[prod_short](includes/prod_short.md)] automatiquement créé.

### <a name="to-use-the-dataverse-connection-setup-assisted-setup-guide"></a><a name="to-use-the-dataverse-connection-setup-assisted-setup-guide"></a>Pour utiliser le guide de configuration assistée Paramétrage de la connexion Dataverse

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

### <a name="to-create-or-maintain-the-connection-manually"></a><a name="to-create-or-maintain-the-connection-manually"></a>Pour créer ou conserver manuellement la connexion

La procédure suivante décrit comment configurer manuellement la connexion sur la page **Paramétrage de la connexion Dataverse**. C’est sur la page **Configuration de la connexion Dataverse** que vous gérez les paramètres d’intégration.

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration de la connexion Dataverse**, puis choisissez le lien associé.
2. Saisissez les informations suivantes pour la connexion de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] vers [!INCLUDE[prod_short](includes/prod_short.md)].

    |Champ|Description|
    |-----|-----|
    |**URL Environnement**|Si vous possédez des environnements dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)], nous les trouverons lorsque vous exécuterez le guide de configuration. Si vous souhaitez vous connecter à un autre environnement dans un autre abonné, vous pouvez saisir les informations d’identification administrateur pour l’environnement et nous les trouverons. |
    |**Activé**|Commencez avec l’intégration. Si vous n’activez pas la connexion tout de suite, les paramètres de connexion seront sauvegardés, mais les utilisateurs ne seront pas en mesure d’accéder aux données [!INCLUDE[cds_long_md](includes/cds_long_md.md)] à partir de [!INCLUDE[prod_short](includes/prod_short.md)]. Vous pouvez revenir sur cette page et activer la connexion ultérieurement.  |

3. Dans le champ **Modèle de propriété**, choisissez si vous souhaitez une table Équipe dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)] pour posséder de nouveaux enregistrements, ou un ou plusieurs utilisateurs spécifiques. Si vous choisissez **Personne**, vous devez indiquer chaque utilisateur. Si vous choisissez **Équipe**, le centre de profit par défaut s’affiche dans le champ **Centre de profit couplé**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

    <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you're using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who don't have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account won't have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field|-->
4. Pour tester les paramètres de connexion, choisissez **Connexion**, puis **Tester la connexion**.  

    > [!NOTE]  
    > Si le chiffrement des données n’est pas activé dans [!INCLUDE[prod_short](includes/prod_short.md)], vous recevrez un message vous demandant si vous souhaitez l’activer. Pour activer le chiffrement des données, cliquez sur **Oui** et fournissez les informations requises. Sinon, sélectionnez **Non**. Vous pouvez activer le chiffrement des données ultérieurement. Pour plus d’informations, voir [Chiffrement des données dans Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) de l’aide sur Developer and Administration.  
5. Si la synchronisation de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] n’est pas déjà configurée, vous recevrez un message vous demandant si vous souhaitez utiliser les paramètres de synchronisation par défaut. Selon que vous souhaitez conserver ou non les enregistrements alignés dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)] et [!INCLUDE[prod_short](includes/prod_short.md)], sélectionnez **Oui** ou **Non**.

<!--
## <a name="show-me-the-process"></a><a name="show-me-the-process"></a>Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="customize-the-match-based-coupling"></a><a name="customize-the-match-based-coupling"></a>Personnaliser le couplage par correspondance

À partir de la 2e vague de lancement de 2021, un administrateur peut saisir des critères pour coupler des enregistrements en fonction de correspondances. Vous pouvez lancer l’algorithme de correspondance des enregistrements à partir des emplacements suivants dans [!INCLUDE [prod_short](includes/prod_short.md)] :

* Les pages de liste qui affichent les enregistrements synchronisés avec [!INCLUDE [cds_long_md](includes/cds_long_md.md)], telles que les pages Clients et Articles.  

    Sélectionnez plusieurs enregistrements, puis choisissez l’action **Associé**, choisissez **Dataverse**, choisissez **Couplage**, puis choisissez **Couplage par correspondance**.

    Lorsque vous démarrez le processus de couplage par correspondance à partir d’une liste de données de base, une tâche de couplage est planifiée directement après que vous ayez spécifié les critères de couplage.  
* La page **Révision synchronisation complète Dataverse**.  

    Lorsque le processus de synchronisation complet détecte que vous avez des enregistrements découplés à la fois dans [!INCLUDE [prod_short](includes/prod_short.md)] et [!INCLUDE [cds_long_md](includes/cds_long_md.md)], un lien **Sélectionner les critères de couplage** apparaît pour la table d’intégration.  

    Vous pouvez lancer le processus **Exécuter la synchronisation complète** depuis les pages **Configuration de la connexion Dataverse** et **Configuration de la connexion Dynamics 365**. Vous pouvez également le lancer dans le guide de configuration assistée **Configurer une connexion à Dataverse** lorsque vous avez terminé votre configuration.  

    Lorsque vous lancez le processus de couplage par correspondance à partir de la page **Révision synchronisation complète Dataverse**, une tâche de couplage est planifiée après que vous ayez terminé la configuration.  
* La liste **Mappages de table d’intégration**.  

    Sélectionnez un mappage, choisissez l’action **Couplage**, puis choisissez **Couplage par correspondance**.

    Lorsque vous lancez le processus de couplage par correspondance à partir du mappage d’une table d’intégration, une tâche de couplage s’exécute pour tous les enregistrements non couplés dans le mappage. Vous pouvez également sélectionner des enregistrements non couplés dans la liste pour exécuter la tâche uniquement pour ces enregistrements.

Dans les trois cas, la page **Sélectionner les critères de couplage** s’ouvre pour vous permettre de définir les critères de couplage pertinents. Dans cette page, personnalisez le couplage avec les tâches suivantes :

* Choisissez les champs à utiliser pour faire correspondre les enregistrements [!INCLUDE [prod_short](includes/prod_short.md)] avec les entités [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Vous pouvez spécifier si la correspondance est sensible à la casse.  

* Spécifiez s’il faut synchroniser après avoir couplé des enregistrements. Si les enregistrements utilisent le mappage bidirectionnel, vous pouvez également spécifier ce qui se produit si des conflits sont répertoriés sur la page **Résoudre les conflits de mise à jour**.  

* Hiérarchisez l’ordre de recherche des enregistrements en spécifiant une *priorité de correspondance* pour les champs de mappage pertinents. [!INCLUDE [prod_short](includes/prod_short.md)] recherchera une correspondance dans l’ordre croissant en fonction de la valeur du champ **Priorité de correspondance**. Une valeur vide dans le champ **Priorité de correspondance** est égale à la priorité 0, qui est la priorité la plus élevée. Les champs avec la priorité 0 sont pris en compte en premier.  

* Spécifiez s’il faut créer une nouvelle instance d’entité dans [!INCLUDE [cds_long_md](includes/cds_long_md.md)] au cas où aucune correspondance non couplée unique ne peut être trouvée en utilisant les critères de correspondance. Pour activer cette fonctionnalité, choisissez l’action **Créer si impossible de trouver une correspondance**.  

### <a name="view-the-results-of-the-coupling-job"></a><a name="view-the-results-of-the-coupling-job"></a>Voir les résultats de la tâche de couplage

Pour afficher les résultats de la tâche de couplage, ouvrez la page **Mappages de table d’intégration**, sélectionnez le mappage pertinent, choisissez l’action **Couplage**, puis choisissez l’action **Journal des tâches de couplage d’intégration**.  

Si les enregistrements n’ont pas pu être couplés, vous pouvez choisir la valeur de la colonne **Échec** pour ouvrir une liste d’erreurs décrivant pourquoi cela s’est produit.  

En général, le couplage échoue pour les raisons suivantes :

* Aucun critère de correspondance n’a été défini

    Exécutez à nouveau le couplage par correspondance, mais n’oubliez pas de définir les critères de couplage.

* Aucune correspondance n’a été trouvée pour les champs spécifiés dans les critères de correspondance

    Répétez le couplage en utilisant différents champs.

* Plusieurs correspondances ont été trouvées pour plusieurs enregistrements en fonction des champs spécifiés dans les critères de correspondance  

    Répétez le couplage en utilisant différents champs.

* Une correspondance a été trouvée, mais l’enregistrement est déjà couplé à un enregistrement dans [!INCLUDE [prod_short](includes/prod_short.md)]  

    Répétez le couplage en utilisant différents champs ou recherchez pourquoi cette entité [!INCLUDE [cds_long_md](includes/cds_long_md.md)] est couplée à l’enregistrement dans [!INCLUDE [prod_short](includes/prod_short.md)].

> [!TIP]
> Pour vous aider à avoir une vue d’ensemble de la progression du couplage, le champ **Couplé à Dataverse** indique si un enregistrement est couplé à une entité [!INCLUDE [cds_long_md](includes/cds_long_md.md)] . Vous pouvez utiliser le champ **Couplé à Dataverse** pour filtrer la liste des enregistrements que vous synchronisez.

## <a name="upgrade-connections-from-business-central-online-to-use-certificate-based-authentication"></a><a name="upgrade-connections-from-business-central-online-to-use-certificate-based-authentication"></a>Mettre à niveau les connexions de Business Central Online pour utiliser l’authentification basée sur les certificats

> [!NOTE]
> Cette section s’applique uniquement aux locataires [!INCLUDE[prod_short](includes/prod_short.md)] en ligne hébergés par Microsoft. Les locataires en ligne hébergés par les développeurs de logiciels indépendants et les installations locales ne sont pas affectés.

En avril 2022, [!INCLUDE[cds_long_md](includes/cds_long_md.md)] abandonne le type d’authentification Office365 (nom d’utilisateur/mot de passe). Pour en savoir plus, voir [ Abandon du type d’authentification Office365](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). De plus, en mars 2022, [!INCLUDE[prod_short](includes/prod_short.md)] abandonne l’utilisation de l’authentification de service à service basée sur le secret client pour les abonnés en ligne. Vous devez utiliser l’authentification de service à service basée sur un certificat pour les connexions à [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Les abonnés [!INCLUDE[prod_short](includes/prod_short.md)] Online hébergés par les éditeurs de logiciels indépendants et les installations sur site peuvent continuer à utiliser l’authentification basée sur le secret client pour l’authentification.

Pour éviter de perturber les intégrations, _vous devez mettre à niveau_ la connexion pour utiliser l’authentification par certificat. Bien que le changement soit prévu pour mars 2022, nous vous recommandons fortement de mettre à niveau dès que possible. Les étapes suivantes décrivent comment effectuer une mise à niveau vers l’authentification par certificat. 

### <a name="to-upgrade-your-business-central-online-connection-to-use-certificate-based-authentication"></a><a name="to-upgrade-your-business-central-online-connection-to-use-certificate-based-authentication"></a>Pour mettre à niveau votre connexion de Business Central Online pour utiliser l’authentification basée sur les certificats

1. Selon que vous intégrez ou non à Dynamics 365 Sales, effectuez l’une des opérations suivantes :
   * Si vous le faites, ouvrez la page **Configuration de la connexion Microsoft Dynamics 365**.
   * Si vous ne le faites pas, ouvrez la page **Configuration de la connexion Dataverse**.
2. Choisissez **Connexion**, puis **Utiliser l’authentification par certificat** pour mettre à niveau la connexion afin d’utiliser l’authentification basée sur un certificat.
3. Connectez-vous avec les informations d’identification d’administrateur pour Dataverse. La connexion doit prendre moins d’une minute.

> [!NOTE]
> Vous devez répéter ces étapes dans chaque environnement [!INCLUDE[prod_short](includes/prod_short.md)], y compris les environnements de production et de bac à sable, et dans chaque entreprise où vous êtes connecté à [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

## <a name="connecting-on-premises-versions"></a><a name="connecting-on-premises-versions"></a>Connexion des versions locales

Pour connecter [!INCLUDE[prod_short](includes/prod_short.md)] sur site à [!INCLUDE[cds_long_md](includes/cds_long_md.md)], vous devez spécifier quelques informations sur la page **Configuration de la connexion Dataverse**.

Pour se connecter à l’aide d’un compte Azure Active Directory (Azure AD), vous devez enregistrer une application dans Azure AD. Vous devrez fournir l’ID de l’application, le secret du coffre de clés et l’URL de redirection à utiliser. L’URL de redirection est pré-remplie et devrait fonctionner pour la plupart des installations. Vous devez configurer votre installation pour utiliser HTTPS. Pour plus d’informations, voir [Configuration de SSL pour sécuriser la connexion du client Web Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Si vous configurez votre serveur pour avoir une page d’accueil différente, vous pouvez changer l’URL. Le secret client sera enregistré sous forme de chaîne cryptée dans votre base de données. 

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-dataverse"></a><a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-dataverse"></a>Pour enregistrer une application dans Azure AD pour se connecter de Business Central à Dataverse

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
6. Choisissez **Aperçu**, puis recherchez la valeur **ID application (client)**. Cet ID est l’ID client de votre application. Vous devez le saisir soit sur la page **Configuration de la connexion Dataverse** dans le champ **ID client** ou stockez-le dans un stockage sécurisé et fournissez-le à un souscripteur d’événements.
7. Dans [!INCLUDE[prod_short](includes/prod_short.md)], sur la page **Configuration de la connexion Dataverse**, dans le champ **URL Environnement**, saisissez l’URL de votre environnement [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
8. Pour activer la connexion à [!INCLUDE[cds_long_md](includes/cds_long_md.md)], activez le bouton bascule **Activé**.
9. Connectez-vous avec votre compte administrateur pour Azure Active Directory (ce compte doit avoir une licence valide pour [!INCLUDE[cds_long_md](includes/cds_long_md.md)] et être administrateur dans votre environnement [!INCLUDE[cds_long_md](includes/cds_long_md.md)]). Une fois connecté, vous serez invité à autoriser votre application enregistrée à se connecter à [!INCLUDE[cds_long_md](includes/cds_long_md.md)] au nom de l’organisation. Vous devez donner votre accord pour terminer la configuration.

   > [!NOTE]
   > Si vous n’êtes pas invité à vous connecter avec votre compte administrateur, c’est probablement parce que les fenêtres contextuelles sont bloquées. Pour vous connecter, autorisez les fenêtres contextuelles de `https://login.microsoftonline.com`.

### <a name="to-disconnect-from-"></a><a name="to-disconnect-from-"></a>Pour se déconnecter de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration de la connexion Dataverse**, puis choisissez le lien associé.
2. Sur la page **Paramétrage de la connexion Dataverse**, désactivez le bouton bascule **Activé**.  

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Afficher le statut d’une synchronisation](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
