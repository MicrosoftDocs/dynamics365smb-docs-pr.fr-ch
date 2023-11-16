---
title: Configuration d’imprimantes à impression universelle
description: Découvrez comment utiliser l’impression universelle pour assurer l’impression cloud dans Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---

# <a name="set-up-universal-print-printers"></a>Configuration d’imprimantes à impression universelle

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

L′impression universelle est un service basé sur un abonnement Microsoft 365 qui s′exécute entièrement sur Microsoft Azure. Il vous offre une gestion centralisée des imprimantes via le portail Impression universelle. [!INCLUDE[prod_short](includes/prod_short.md)] met les imprimantes configurées dans l′impression universelle à la disposition des utilisateurs clients via l′extension **Intégration d′impression universelle**.

![Configuration de l′impression universelle.](media/Universal-Print-arch.png)

La configuration complète nécessite que vous travailliez dans Microsoft Azure, en utilisant le [Portail Azure](https://portal.azure.com), et dans [!INCLUDE[prod_short](includes/prod_short.md)]. La configuration est divisée en deux tâches principales, comme décrit dans cet article :

1. Dans Microsoft Azure, configurez l’Impression universelle et ajoutez les imprimantes que vous souhaitez utiliser dans Business Central dans un partage d’impression. Consultez [cette section](#set-up-universal-print-and-printers-in-microsoft-azure).
2. Dans [!INCLUDE[prod_short](includes/prod_short.md)], ajoutez les imprimantes à partir des partages d’impression dans l’Impression universelle. Consultez [cette section](#add-printers-in-business-central-online) pour une connexion en ligne ou [celle-ci](#add-printers-in-business-central-on-premises) pour une connexion sur site.

## <a name="prerequisites"></a>Conditions préalables

- Imprimantes prises en charge

  [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge les mêmes imprimantes que l′impression universelle, qui peuvent être des imprimantes compatibles ou non compatibles avec l′impression universelle. Les imprimantes non compatibles ne peuvent pas communiquer directement avec l′impression universelle, elles nécessitent donc un logiciel de connecteur supplémentaire, fourni par l′impression universelle. Certaines imprimantes plus anciennes peuvent ne pas être prises en charge. 

- Impression universelle :

  - Un abonnement/licence à l′impression universelle pour votre organisation.

    En savoir plus sur l’[Licence d’impression universelle](/universal-print/fundamentals/universal-print-license).

  - Vous disposez des rôles **Administrateur d’imprimante** (ou Gestionnaire d’imprimante) et **Administrateur global** dans Azure.

    Pour gérer l′impression universelle, votre compte doit avoir les rôles **Administrateur d’imprimante** (ou Gestionnaire d’imprimante) et **Administrateur général** dans Microsoft Entra ID. Ces rôles ne sont nécessaires que pour gérer l′impression universelle. Ils ne sont pas requis par les personnes chargées de la configuration des imprimantes à partir de [!INCLUDE[prod_short](includes/prod_short.md)].

- [!INCLUDE[prod_short](includes/prod_short.md)] en ligne et sur site :

  - 1re vague de lancement 2021 de [!INCLUDE[prod_short](includes/prod_short.md)] ou ultérieure.
  - L′extension **Intégration d′impression universelle** est installée.

    Cette extension est publiée et installée par défaut dans le cadre de [!INCLUDE[prod_short](includes/prod_short.md)] Online et sur site. Vous pouvez vérifier s′il est installé sur la page **Gestion des extensions**. En savoir plus sur [Installation et désinstallation d’extensions dans Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] sur site uniquement :
  - L’authentification NavUserPassword ou Microsoft Entra ID est configurée.
    > [!NOTE]
    >  L’extension Universal Print ne prend pas en charge l’authentification de service à service (S2S). Il nécessite un utilisateur connecté pour envoyer des travaux d’impression au service Universal Print via l’API Graph.
  - Une application pour Business Central est enregistrée dans votre abonné Microsoft Entra et [!INCLUDE[prod_short](includes/prod_short.md)].

    Comme d′autres services Azure qui fonctionnent avec [!INCLUDE[prod_short](includes/prod_short.md)], l′impression universelle nécessite un enregistrement d′application pour [!INCLUDE[prod_short](includes/prod_short.md)] dans Microsoft Entra ID. L’enregistrement de l’application fournit des services d’authentification et d’autorisation entre [!INCLUDE[prod_short](includes/prod_short.md)] et l′impression universelle.

    Votre déploiement utilise peut-être déjà une inscription d′application pour d′autres services Azure, comme Power BI. Si tel est le cas, utilisez également l′enregistrement d′application existant pour l′impression universelle, au lieu d′en ajouter un nouveau. La seule chose que vous devez faire, dans ce cas, est de modifier l′inscription de l′application pour inclure les autorisations d′impression appropriées pour l′API Microsoft Graph : **PrinterShare.ReadBasic.All**, **PrintJob.Create** et **PrintJob.ReadBasic.** 

    Pour enregistrer une application et définir les autorisations appropriées, suivez les étapes décrites dans [Enregistrer une application dans Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

## <a name="set-up-universal-print-and-printers-in-microsoft-azure"></a>Configurer l′impression universelle et des imprimantes dans Microsoft Azure

Avant de pouvoir commencer à gérer les imprimantes de l′impression universelle dans Business Central, vous devez effectuer plusieurs tâches pour que l′impression universelle soit opérationnelle dans Azure avec les imprimantes que vous souhaitez utiliser.

Pour obtenir des instructions détaillées sur la configuration, consultez [Premiers pas : configurer l′impression universelle](/universal-print/fundamentals/universal-print-getting-started) dans la documentation de l′impression universelle. Voici un aperçu des étapes à suivre. La plupart de ces étapes sont effectuées dans le portail Azure.

1. Attribuez des licences de l′impression universelle à vous-même et aux autres utilisateurs.

    La manière dont vous attribuez la licence varie selon que vous intégrez à Business Central Online ou sur site.

    - Avec [!INCLUDE[prod_short](includes/prod_short.md)] Online, vous attribuez des licences à l′aide du centre d′administration Microsoft 365.

      En savoir plus sur [Aide du Centre d′administration Microsoft – Attribuer des licences aux utilisateurs](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Avec [!INCLUDE[prod_short](includes/prod_short.md)] en local, vous attribuez des licences dans votre client à l′aide du portail Azure.

      Pour en savoir plus, consultez [Attribuer ou supprimer des licences dans le portail Azure](/azure/active-directory/fundamentals/license-users-groups).

2. Installez le connecteur de l′impression universelle pour enregistrer les imprimantes qui ne peuvent pas communiquer directement avec l′impression universelle.

    La plupart des imprimantes du marché ne peuvent pas communiquer directement avec l′impression universelle. Aussi, vous devez installer le connecteur d’impression universelle. Pour plus d′informations, consultez [Installation du connecteur d′impression universel](/universal-print/fundamentals/universal-print-connector-installation).

3. Enregistrez vos imprimantes dans l′impression universelle.

    L′enregistrement d′une imprimante permet à l′imprimante universelle de détecter l′imprimante.

    - Pour les imprimantes qui peuvent communiquer directement avec l′impression universelle, suivez les étapes fournies par le fabricant de l′imprimante.

    - Pour les autres imprimantes, enregistrez les imprimantes à l′aide du connecteur d′impression universelle. 

      En savoir plus sur l’[enregistrement de l’imprimante](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Modifier les propriétés de l′imprimante (facultatif)

    Une fois l′imprimante enregistrée, vous pouvez afficher et modifier les propriétés de l′imprimante, comme les préférences par défaut.

    Pour plus d’informations, voir [Gestion des paramètres de l’imprimante à l’aide du portail d’impression universelle](/universal-print/portal/configure-printer-settings).

5. Partagez les imprimantes avec les utilisateurs.

    Toute imprimante que vous souhaitez utiliser dans [!INCLUDE[prod_short](includes/prod_short.md)] devra être ajoutée à un *partage d’imprimante* dans l′impression universelle. Tout utilisateur ayant besoin d’accéder à l’imprimante doit être ajouté en tant que membre du partage d’imprimante. En savoir plus sur [Partager une imprimante](/universal-print/portal/share-printers).

    > [!TIP]
    > Vous pouvez toujours ajouter ou supprimer des utilisateurs ultérieurement. En savoir plus sur [Autorisations de l’imprimante](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).

6. Activez la conversion de documents.

    L′impression universelle rend le contenu pour l′impression au format XPS. Certaines imprimantes existantes sur le marché ne prennent pas en charge le rendu du contenu XPS ; dans de nombreux cas, uniquement au format PDF. L′impression sur ces imprimantes échouera à moins que l′impression universelle ne soit configuré pour convertir les documents au format pris en charge par l′imprimante.

    En savoir plus sur [Présentation de la conversion de documents](/universal-print/portal/document-conversion).

Vous êtes maintenant prêt à ajouter les imprimantes à [!INCLUDE[prod_short](includes/prod_short.md)], configurez les imprimantes par défaut pour les états et imprimez.  

## <a name="add-printers-in-business-central-online"></a>Ajouter des imprimantes dans Business Central Online

Une fois les imprimantes configurées et partagées dans l′impression universelle, vous êtes prêt à les ajouter à [!INCLUDE[prod_short](includes/prod_short.md)] pour les utiliser. Il existe deux façons d′ajouter des imprimantes à impression universelle. Vous pouvez ajouter les imprimantes toutes à la fois ou individuellement, une à la fois.

L′ajout d′imprimantes individuellement vous permet de configurer plusieurs fois la même imprimante d′impression universelle dans [!INCLUDE[prod_short](includes/prod_short.md)]. Ensuite, pour chaque imprimante ajoutée, vous pouvez modifier les paramètres d′impression, tels que le bac à papier, le format et l′orientation. De cette façon, vous pouvez configurer des imprimantes pour différents états et documents qui ont des exigences de sortie spéciales.

> [!NOTE]
> Utilisez-vous [!INCLUDE[prod_short](includes/prod_short.md)] sur site ? Si c’est le cas, passez à la [section suivante](#add-printers-in-business-central-on-premises) ; la première configuration est légèrement différente.  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Gestion des imprimantes**, puis sélectionnez le lien associé.
2. Sélectionnez **l′impression universelle**, puis l’une des options suivantes :

   - **Ajouter toutes les imprimantes l′impression universelle** pour ajouter toutes les imprimantes qui ne sont pas déjà ajoutées. Vous pouvez utiliser cette option même si des imprimantes ont déjà été ajoutées.
   - **Ajouter une imprimante à impression universelle** pour ajouter une imprimante spécifique.  
3. Suivez les instructions à l’écran.

    - Si vous avez choisi **Ajouter toutes les imprimantes à l′impression universelle**, la configuration **Ajouter des imprimantes universelles** démarre. 

    - Si vous avez choisi **Ajouter une imprimante à l′impression universelle**, la page **Paramètre de l′imprimante universelle** s′affiche. Remplissez le champ **Nom**, la sélection **...** à côté du champ **Partager l′impression en impression universelle** pour sélectionner le partage d’imprimante contenant l’imprimante pour l′impression universelle. Renseignez les champs restants le cas échéant. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Une fois qu′une imprimante a été ajoutée, vous pouvez afficher et modifier ses paramètres à partir de la page **Gestion des imprimantes**. Sélectionnez simplement l′imprimante, puis choisissez **Modifier les paramètres de l′imprimante**.

## <a name="add-printers-in-business-central-on-premises"></a>Ajouter des imprimantes dans Business Central sur site

<!--With [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, unlike online, users aren't automatically authenticated with the registered app in Azure used for the Universal Print service. So, before any Business Central user (including admins) can add or even use Universal Print printers, they'll have to authenticate with the Azure app and grant access to the Universal Print service. The following procedure describes how to initiate this authentication flow. Each user typically only has to do this task once.-->

Avant qu’un utilisateur ne puisse ajouter ou utiliser des imprimantes Impression universelle dans Business Central, il doit autoriser l’accès aux services Azure utilisés par l’Impression universelle et lui accorder l’autorisation d’accéder à des données et à des opérations telles que :

- Connexion et lecture du profil utilisateur
- Lecture des informations de base sur les travaux d’impression
- Création de travaux d’impression

Cela se fait généralement la première fois qu’il se connecte à l’application inscrite dans Azure utilisée pour l’Impression universelle. Dans Business Central Online, ce flux d’autorisation s’effectue de manière transparente, sans interaction de l’utilisateur. Mais Business Central sur site fonctionne différemment. Il nécessite que vous, ou tout autre utilisateur souhaitant utiliser des imprimantes Impression universelle, lanciez le flux d’authentification&mdash;généralement, une seule fois. La manière la plus directe est décrite dans les étapes suivantes. Un moyen moins direct consiste à se connecter à un autre service intégré qui utilise la même application inscrite dans Azure, comme Power BI ou OneDrive. Chaque utilisateur n’a généralement à effectuer cette tâche qu’une seule fois.

> [!NOTE]
> Si vous êtes un administrateur, nous vous recommandons d’effectuer cette tâche avant les autres utilisateurs. Ensuite, informez les utilisateurs qui auront besoin d’utiliser des imprimantes Impression universelle de la manière de procéder. Si l’application enregistrée dans Azure pour l’Impression universelle nécessite le consentement de l’administrateur pour les autorisations d’API, il est plus simple que vous accordiez le consentement au nom de l’organisation. Vous pouvez accorder le consentement de l’administrateur à partir du portail Azure ou lorsque vous exécutez les étapes qui suivent. 

<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->
### <a name="connect-to-universal-print-for-the-first-time"></a>Première connexion à Impression universelle

Effectuez ces étapes pour vous connecter au service Impression universelle pour la première fois.

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Gestion des imprimantes**, puis sélectionnez le lien associé.
2. Sélectionnez **Impression universelle** > **Ajouter toutes les imprimantes à l’impression universelle** pour démarrer le guide d’installation assistée **Ajouter des imprimantes pour l’impression universelle** (assistant).
3. Suivez les instructions à l’écran jusqu’à ce que vous arriviez à la page **AUTORISATIONS DU SERVICE MICROSOFT ENTRA**.

    <!--The MICROSOFT ENTRA SERVICE PERMISSIONS page appears. You'll be prompted to give consent to Azure Services. You'll be lead through the process of verifying your Microsoft Entra ID setup, checking your Universal Print license, and then adding the printers.-->

   ![Affiche la page AUTORISATIONS DU SERVICE MICROSOFT ENTRA](media/azure-ad-services-permissions.png "Affiche la page AUTORISATIONS DU SERVICE MICROSOFT ENTRA")

4. Sélectionnez le lien **Autoriser les services Azure**.

   1. Si la page **Autorisation demandée** s’affiche, lisez-la attentivement et sélectionnez **Accepter** pour accepter et continuer. Si vous êtes administrateur, vous pouvez sélectionner **Consentement au nom de l’organisation** si vous souhaitez donner votre consentement pour tous les utilisateurs.

      ![Affiche la page des autorisations de requête Azure](media/azure-ad-permissions-requested.png "Page des autorisations de requête Azure").

   2. Si vous y êtes invité, connectez-vous en utilisant votre nom et votre mot de passe.

5. Une fois le processus d’autorisation terminé avec succès, vous revenez à la page **Ajouter des imprimantes pour l’impression universelle**. Sélectionnez **Suivant** > **Terminer** pour terminer la configuration.

Une fois qu′une imprimante a été ajoutée, vous pouvez afficher et modifier ses paramètres à partir de la page **Gestion des imprimantes**. Sélectionnez simplement l′imprimante, puis choisissez **Modifier les paramètres de l′imprimante**.

Une fois la connexion initiale terminée, vous pouvez utiliser les imprimantes Impression universelle pour imprimer des états et d’autres travaux d’impression. Pour plus d’informations, consultez [Impression d’un état](ui-work-report.md#PrintReport). Si vous souhaitez ajouter, supprimer ou modifier des imprimantes, revenez simplement à la page **Gestion d’impression** et sélectionnez **Impression universelle**.

## <a name="common-problems-and-resolutions"></a>Problèmes courants et solutions

Dans cette section, vous découvrirez les problèmes courants que les utilisateurs peuvent rencontrer lorsqu’ils tentent de configurer ou d’utiliser des imprimantes Impression universelle.

### <a name="you-dont-have-access-to-the-printer-your-printer"></a>Vous n’avez pas accès à l’imprimante \<your-printer\>.

Si un utilisateur reçoit ce message lorsqu’il essaie d’imprimer un document sur une imprimante Impression universelle, cela peut être dû à l’une des conditions suivantes :

- L’utilisateur n’a pas de licence Impression universelle attribuée à son compte Microsoft 365 ou Azure Active AD. 
- L’utilisateur n’est pas affecté au partage d’imprimante dans l’Impression universelle.
- (Sur site) L’inscription de l’application Azure utilisée pour l’Impression universelle ne fonctionne pas ou a récemment changé depuis la dernière fois que l’utilisateur s’est connecté.
- (Sur site) L’utilisateur ne s’est pas encore connecté à l’application inscrite dans Azure pour l’application Impression universelle et a consenti pour la première fois.

## <a name="there-was-an-error-fetching-printers-shared-to-you"></a>Une erreur s’est produite lors de l’extraction des imprimantes partagées avec vous.

Si un utilisateur reçoit ce message lorsqu’il essaie d’ajouter une imprimante Impression universelle à partir de la page **Gestion des imprimantes**, c’est généralement parce qu’il ne s’est pas encore connecté à l’application inscrite dans Azure pour l’application Impression universelle et a consenti pour la première fois. 
<!--
### <a name="troubleshooting"></a>Troubleshooting

#### <a name="you-dont-see-the-a-printer-in-the"></a>You don't see the a printer in the

The printer is not shared in Universal Print.

### <a name="you-get-an-error-when-tryong-to-add-all-or-a-single-printer"></a>You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## <a name="could-not-upload-the-document-to-print-job-50"></a>Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps




-->

## <a name="next-steps"></a>Étapes suivantes
[Paramétrer des imprimantes par défaut](ui-specify-printer-selection-reports.md).

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble des imprimantes](admin-printer-setup-overview.md)  
[Paramétrer des imprimantes de messagerie](admin-printer-setup-email.md)
[Imprimer un état](ui-work-report.md#PrintReport)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exécuter des traitements par lots](ui-how-run-batch-jobs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
