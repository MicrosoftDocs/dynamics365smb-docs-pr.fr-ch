---
title: Paramétrage imprimantes
description: Découvrez comment configurer des imprimantes que vous pouvez utiliser pour les rapports et les documents et les différentes fonctionnalités d’impression disponibles dans Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing, email printing, cloud printing, Universal Print
ms.search.form: 8900, 9018, 9022
ms.date: 06/24/2021
ms.author: jswymer
ms.openlocfilehash: 317e90976aed760f55fc7122483377e8df11c906
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/23/2022
ms.locfileid: "8335177"
---
# <a name="set-up-printers"></a>Paramétrage imprimantes

Impression de documents et de rapports à partir de [!INCLUDE[prod_short](includes/prod_short.md)] est une tâche importante pour les utilisateurs professionnels. Les utilisateurs voudront généralement envoyer des travaux d′impression directement à l′une des imprimantes de votre organisation&mdash; peu importe quel client ou application [!INCLUDE[prod_short](includes/prod_short.md)] ils utilisent. Parce que [!INCLUDE[prod_short](includes/prod_short.md)] Online est un service cloud, il ne peut pas atteindre directement les imprimantes locales connectées aux appareils des utilisateurs, mais il peut se connecter à des imprimantes compatibles cloud.

Pour répondre à vos besoins d′impression, [!INCLUDE[prod_short](includes/prod_short.md)] offre les fonctionnalités suivantes :

|Fonctionnalité|Description|Client web| Application mobile|Application pour Teams|
|-------|-----------|----------|-----------|--------------|
|Impression universelle|L′impression universelle est une solution de gestion d′imprimante disponible en tant que service cloud de Microsoft. Avec cette fonction, vous pouvez configurer vos imprimantes dans l′impression universelle, puis les enregistrer pour une utilisation dans [!INCLUDE[prod_short](includes/prod_short.md)]. Cette fonctionnalité nécessite un abonnement d′impression universelle et l′extension **Intégration d′impression universelle**|![fonctionne en ligne.](media/check.png)|![fonctionne en ligne.](media/check.png)|![fonctionne en ligne](media/check.png)|
|Impression par e-mail|Cette fonction vous permet de configurer des imprimantes compatibles avec la messagerie électronique. [!INCLUDE[prod_short](includes/prod_short.md)] envoie ensuite les travaux d′impression à une imprimante à l′aide de l′adresse e-mail de l′imprimante. Cette fonction nécessite des imprimantes compatibles avec la messagerie électronique et l′extension **Envoyer à une imprimante e-mail**.|![fonctionne en ligne.](media/check.png)|![fonctionne en ligne](media/check.png)|![fonctionne en ligne](media/check.png)|
|Impression du navigateur|Les travaux d′impression sont gérés par la fonctionnalité d′impression du navigateur de l′utilisateur. Si aucune imprimante cloud n’est installée et configurée ou si une imprimante installée échoue, l’impression reprend par défaut les options d’impression du navigateur. Le champ **Imprimante** de la page de demande de rapport affichera *(Géré par le navigateur)*.|![fonctionne en ligne](media/check.png)|||

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] prend également en charge les extensions d′imprimante personnalisées qui ajoutent encore plus de fonctionnalités d′impression. Ainsi, si des extensions d′imprimante personnalisées sont installées, votre application peut inclure des fonctionnalités d′impression qui ne sont pas décrites dans cet article. 

## <a name="set-up-universal-print"></a>Configurer l′impression universelle

L′impression universelle est un service basé sur un abonnement Microsoft 365 qui s′exécute entièrement sur Microsoft Azure. Il vous offre une gestion centralisée des imprimantes via le portail Impression universelle. [!INCLUDE[prod_short](includes/prod_short.md)] met les imprimantes configurées dans l′impression universelle à la disposition des utilisateurs clients via l′extension **Intégration d′impression universelle**.

![Configuration de l′impression universelle.](media/Universal-Print-arch.png)

La configuration complète nécessite que vous travailliez dans Microsoft Azure, en utilisant le [Portail Azure](https://portal.azure.com), et dans [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="supported-printers"></a>Imprimantes prises en charge

[!INCLUDE[prod_short](includes/prod_short.md)] prend en charge les mêmes imprimantes que l′impression universelle, qui peuvent être des imprimantes compatibles ou non compatibles avec l′impression universelle. Les imprimantes non compatibles ne peuvent pas communiquer directement avec l′impression universelle, elles nécessitent donc un logiciel de connecteur supplémentaire, fourni par l′impression universelle. Certaines imprimantes plus anciennes peuvent ne pas être prises en charge. 

<!-- TODO If not installed, go to AppSource -->

### <a name="prerequisites"></a>Conditions préalables

**Pour [!INCLUDE[prod_short](includes/prod_short.md)]**

- 1re vague de lancement 2021 de [!INCLUDE[prod_short](includes/prod_short.md)] ou ultérieure
- L′extension **Intégration d′impression universelle** est installée

    Cette extension est publiée et installée par défaut dans le cadre de [!INCLUDE[prod_short](includes/prod_short.md)] Online et sur site.  Vous pouvez vérifier s′il est installé sur la page **Gestion des extensions**. Pour plus d’informations, consultez [Installation et désinstallation d’extensions dans Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] sur site :
  - L’authentification NavUserPassword ou Azure Active Directory (AD) est configurée
  - Une application pour Business Central est enregistrée dans votre abonné Azure AD et [!INCLUDE[prod_short](includes/prod_short.md)]

      Comme d′autres services Azure qui fonctionnent avec [!INCLUDE[prod_short](includes/prod_short.md)], l′impression universelle nécessite une inscription d′application pour [!INCLUDE[prod_short](includes/prod_short.md)] dans Azure Active Directory (Azure AD). L’enregistrement de l’application fournit des services d’authentification et d’autorisation entre [!INCLUDE[prod_short](includes/prod_short.md)] et l′impression universelle.

      Votre déploiement utilise peut-être déjà une inscription d′application pour d′autres services Azure, comme Power BI. Si tel est le cas, utilisez également l′enregistrement d′application existant pour l′impression universelle, au lieu d′en ajouter un nouveau. La seule chose que vous devez faire, dans ce cas, est de modifier l′inscription de l′application pour inclure les autorisations d′impression appropriées pour l′API Microsoft Graph.

      Pour enregistrer une application et définir les autorisations appropriées, suivez les étapes décrites dans [Enregistrer une application dans Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

**Pour l′impression universelle**

- Un abonnement/licence à l′impression universelle pour votre organisation.

    Pour plus d′informations, consultez [Licence d′impression universelle](/universal-print/fundamentals/universal-print-license).

- Vous avez les rôles **Gestion des imprimantes** et **Administrateur général** dans Azure.

    Pour gérer l′impression universelle, votre compte doit avoir les rôles **Gestion des imprimantes** et **Administrateur général** dans Azure AD. Ces rôles ne sont nécessaires que pour gérer l′impression universelle. Les utilisateurs ne sont pas tenus d′utiliser les imprimantes de [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="set-up-universal-print-and-add-printers-in-microsoft-azure"></a>Configurer l′impression universelle et ajouter des imprimantes dans Microsoft Azure

Avant de pouvoir commencer à gérer les imprimantes de l′impression universelle dans Business Central, vous devez effectuer plusieurs tâches pour que l′impression universelle soit opérationnel dans Azure avec les imprimantes que vous souhaitez utiliser.

Pour obtenir des instructions détaillées sur la configuration, consultez [Premiers pas : configurer l′impression universelle](/universal-print/fundamentals/universal-print-getting-started) dans la documentation de l′impression universelle. Voici un aperçu des étapes à suivre. La plupart de ces étapes sont effectuées dans le portail Azure.

1. Attribuez des licences de l′impression universelle à vous-même et aux autres utilisateurs.

    La manière dont vous attribuez la licence varie selon que vous intégrez à Business Central Online ou sur site.

    - Avec [!INCLUDE[prod_short](includes/prod_short.md)] Online, vous attribuez des licences à l′aide du centre d′administration Microsoft 365.

      Pour plus d′informations, consultez [Aide du Centre d′administration Microsoft – Attribuer des licences aux utilisateurs](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Avec [!INCLUDE[prod_short](includes/prod_short.md)] local, vous attribuez des licences dans votre client Azure à l′aide du portail Azure.

      Pour plus d′informations, consultez [Azure Directory – Attribuez ou supprimez des licences dans le portail Azure Active Directory](/azure/active-directory/fundamentals/license-users-groups).

2. Installez le connecteur de l′impression universelle pour enregistrer les imprimantes qui ne peuvent pas communiquer directement avec l′impression universelle.

    La plupart des imprimantes du marché ne peuvent pas communiquer directement avec l′impression universelle. Vous devrez installer le connecteur l′impression universelle pour ces imprimantes. Pour plus d′informations, consultez [Installation du connecteur d′impression universel](/universal-print/fundamentals/universal-print-connector-installation).

3. Enregistrez vos imprimantes dans l′impression universelle.

    L′enregistrement d′une imprimante permet à l′imprimante universelle de détecter l′imprimante.

    - Pour les imprimantes qui peuvent communiquer directement avec l′impression universelle, suivez les étapes fournies par le fabricant de l′imprimante.

    - Pour les autres imprimantes, enregistrez les imprimantes à l′aide du connecteur d′impression universelle. 

      Pour plus d’informations, voir [Enregistrement d′une imprimante](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Modifier les propriétés de l′imprimante (facultatif)

    Une fois l′imprimante enregistrée, vous pouvez afficher et modifier les propriétés de l′imprimante, comme les préférences par défaut.

    Pour plus d’informations, voir [Gestion des paramètres de l’imprimante à l’aide du portail d’impression universelle](/universal-print/portal/configure-printer-settings).

5. Partagez les imprimantes.

    Toute imprimante que vous souhaitez utiliser [!INCLUDE[prod_short](includes/prod_short.md)] devra être partagé dans l′impression universelle.

    <!--For more information, see [Share a Printer](/universal-print/fundamentals/universal-print-printer-permissions#share-a-printer). -->

    Pour plus d’informations, voir [Partager une imprimante](/universal-print/portal/share-printers).

6. Donnez aux utilisateurs l′autorisation pour accéder aux imprimantes partagées.

    <!--For more information, see [Printer Permissions](/universal-print/fundamentals/universal-print-printer-permissions#printer-permissions).-->

    Pour plus d’informations, voir [Autorisations d′une imprimante](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).


7. Activez la conversion de documents.

    L′impression universelle rend le contenu pour l′impression au format XPS. Certaines imprimantes existantes sur le marché ne prennent pas en charge le rendu de contenu XPS&mdash; dans de nombreux cas, uniquement au format PDF. L′impression sur ces imprimantes échouera à moins que l′impression universelle ne soit configuré pour convertir les documents au format pris en charge par l′imprimante.

    Pour plus d′informations, consultez [Présentation de la conversion de documents](/universal-print/portal/document-conversion).

Vous êtes maintenant prêt à ajouter les imprimantes à [!INCLUDE[prod_short](includes/prod_short.md)], configurez les imprimantes par défaut pour les rapports et imprimez.  

### <a name="add-universal-printer-printers-to-business-central"></a>Ajouter des imprimantes d′impression universelle à Business Central

Une fois les imprimantes configurées et partagées dans l′impression universelle, vous êtes prêt à les utiliser dans Business Central. Il existe deux façons d′ajouter des imprimantes à impression universelle. Vous pouvez ajouter les imprimantes toutes à la fois ou individuellement, une à la fois.

L′ajout d′imprimantes individuellement vous permet de configurer plusieurs fois la même imprimante d′impression universelle dans Business Central. Ensuite, pour chaque imprimante ajoutée, vous pouvez modifier les paramètres d′impression, tels que le bac à papier, le format et l′orientation. De cette façon, vous pouvez configurer des imprimantes pour différents rapports et documents qui ont des exigences de sortie spéciales.
  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Gestion des imprimantes**, puis sélectionnez le lien associé.
2. Sélectionnez **l′impression universelle**, puis l’une des options suivantes :

    - **Ajouter toutes les imprimantes l′impression universelle** pour ajouter toutes les imprimantes qui ne sont pas déjà ajoutées. Vous pouvez utiliser cette option même si des imprimantes ont déjà été ajoutées. 

    - **Ajouter une imprimante à impression universelle** pour ajouter une imprimante spécifique.  
3. Suivez les instructions à l’écran.

    - Si vous avez choisi **Ajouter toutes les imprimantes à l′impression universelle**, la configuration **Ajouter des imprimantes universelles** démarre. <!--This setup leads you through the process of verifying your Azure AD setup (for on-premises), checking your Universal Print license, and then finally adding the printers.-->

    - Si vous avez choisi **Ajouter une imprimante à l′impression universelle**, la page **Paramètre de l′imprimante universelle** s′affiche. Remplissez le champ **Nom**, la sélection **...** à côté du champ **Partager l′impression en impression universelle** pour sélectionner l′imprimante d′impression universelle. Renseignez les champs restants le cas échéant. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
  
    Ces actions vérifient votre configuration Azure AD (pour sur site), vérifiez que vous disposez d′une licence d′impression universelle, puis ajoutez enfin les imprimantes.

    > [!NOTE]
    > Pour les sites locaux, s′il s′agit de la première connexion à l′impression universelle, la page AUTORISATIONS AZURE ACTIVE DIRECTORY SERVICE s′affiche et vous serez invité à donner votre consentement aux services Azure. Vous ne devez accorder votre consentement qu’une seule fois.

Une fois qu′une imprimante a été ajoutée, vous pouvez afficher et modifier ses paramètres à partir de **Gestion des imprimantes**. Sélectionnez simplement l′imprimante, puis choisissez **Modifier les paramètres de l′imprimante**. 

<!--
### Troubleshooting

#### You don't see the a printer in the 

The printer is not shared in Universal Print.

### You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps

## You don't have access to the printer

- You have not been assigned a Up license
- You have not been given access to the printer in UP.
- (On-prem) The app registration has been broken
-->
## <a name="set-up-email-print"></a>Configurer l′impression d′e-mails

### <a name="prerequisites"></a>Conditions préalables

- 1re vague de lancement 2020 de [!INCLUDE[prod_short](includes/prod_short.md)] ou ultérieure
- L′extension **Envoyer à une imprimante e-mail** est installée

    Cette extension est installée par défaut. Pour plus d′informations sur l′installation d′extensions, consultez 
- La fonctionnalité de messagerie est configurée.

   Pour plus d’informations, voir [Configurer la messagerie](admin-how-setup-email.md).

### <a name="add-an-email-printer"></a>Ajouter une imprimante par e-mail

La page **Gestion des imprimantes** affiche les imprimantes configurées actuellement. La page vous donne également accès à la page **Paramètres** pour chaque imprimante pour modifier une configuration existante ou configurer une nouvelle imprimante.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Gestion des imprimantes**, puis sélectionnez le lien associé.
2. Sélectionner **Imprimer par e-mail**, puis choisissez **Ajouter une imprimante e-mail**.
3. Sur la page **Paramètres de l′imprimante par e-mail**, renseignez les champs nécessaires. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Vous devez sélectionner manuellement le format de papier approprié pour une imprimante, car aucune imprimante locale ni aucun paramètre utilisateur ne peuvent être stockés.
    >
    > Sachez que l’extension Imprimante par e-mail est définie par défaut sur le format de papier **A4**, qui n’est pas adapté en Amérique du Nord, par exemple.

### <a name="privacy-notice"></a>Déclaration de confidentialité

Si vous utilisez l’extension Imprimante par e-mail, tout ou partie des travaux d’impression sont envoyés à l’adresse e-mail configurée pour l’imprimante. Nous vous recommandons vivement d’associer un ID e-mail unique à un périphérique d’impression en utilisant uniquement les services officiels fournis par le fabricant du matériel, tels que HP ePrint, KonicaMinolta EveryonePrint ou Epson Email Print.

Prenez toutes les précautions de confidentialité nécessaires, notamment en veillant à configurer correctement les autorisations, les paramètres de confidentialité et les stratégies de conservation de la solution d’impression d’e-mails. Il est de votre responsabilité de fournir une adresse e-mail correcte, vérifiée et opérationnelle. Pour en savoir plus, consultez la [Déclaration de confidentialité Microsoft](https://privacy.microsoft.com/privacystatement).


## <a name="set-up-default-printers"></a><a name="default"></a>Paramétrer des imprimantes par défaut

Il existe plusieurs façons de configurer les imprimantes qui seront utilisées par défaut pour les travaux d′impression. Une imprimante par défaut est utile si vous utilisez différents états nécessitant différentes imprimantes en raison de leur placement dans la société ou de leurs capacités d’impression.

### <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Définir une imprimante comme imprimante par défaut pour tous les travaux d′impression

La page **Gestion des imprimantes** vous permet de configurer une imprimante comme imprimante par défaut pour tous les travaux d′impression. Vous pouvez spécifier l′imprimante par défaut pour vous uniquement ou pour tous les utilisateurs.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Gestion des imprimantes**, puis sélectionnez le lien associé.

    > [!TIP]
    > Vous pouvez également ouvrir la page **Gestion des imprimantes** de la page **Sélections d′imprimantes** en choisissant **Gestion des imprimantes**.  
2. Sur la page **Gestion des imprimantes**, sélectionnez une imprimante dans la liste, choisissez **Gérer**, puis choisi **Définir comme imprimante par défaut** ou bien **Définir comme imprimante par défaut pour tous les utilisateurs**.

> [!NOTE]
> La configuration d′une imprimante par défaut à partir de la **Gestion des imprimantes** ajoutera une entrée dans les **Sélections d′imprimantes**.

### <a name="set-a-default-printer-for-specific-reports"></a>Définir une imprimante par défaut pour des rapports spécifiques

La page **Sélections d′imprimantes** vous permet de spécifier l′imprimante qu′un rapport utilisera par défaut. Les imprimantes par défaut sont définies sur la base d′un compte utilisateur. Vous pouvez définir une imprimante par défaut pour vous-même, un autre utilisateur ou tous les utilisateurs.

> [!IMPORTANT]
> Pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site, la page **Sélections d′imprimantes** ne peut être utilisée que pour les imprimantes cloud définies par les extensions d′imprimante, telles que les imprimantes Impression par e-mail et l′impression universelle. Elle ne peut pas être utilisée pour les imprimantes locales.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Sélections d’imprimantes**, puis sélectionnez le lien associé. Sinon, sur la page **Gestion des imprimantes**, sélectionnez une imprimante, puis l’action **Sélections d’imprimantes**.
2. Choisissez l’action **Nouveau** pour ajouter une sélection d’imprimante pour un état spécifique.
3. Renseignez les champs selon vos besoins.

L’état spécifié est désormais configuré pour être imprimé sur l’imprimante sélectionnée par défaut.

> [!NOTE]
> Lorsque vous imprimez le rapport en question, vous pouvez en sélectionner un autre à l′aide du champ **Impression** sur la page de demande.

> [!NOTE]
> Si vous ne configurez pas un état pour une imprimante spécifique sur la page **Sélections d’imprimantes**, il est imprimé sur l’imprimante par défaut de la société, comme défini sur la page **Gestion des imprimantes**.

Vous pouvez ou l’administrateur peut également utiliser la page **Sélections d’imprimantes** pour définir d’autres variantes d’impression pour les utilisateurs et les états. Le tableau suivant décrit les combinaisons de valeurs nécessaires pour spécifier une autre configuration d’impression pour un état.

|Pour                                                 |Définir les valeurs suivantes                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Imprimer un état sur une imprimante spécifique pour tous les utilisateurs |Spécifiez une valeur dans les champs **ID état** et **Nom de l’imprimante** et ne renseignez pas le champ **ID utilisateur**.|
|Imprimer tous les états sur une imprimante spécifique pour un utilisateur spécifique|Spécifiez une valeur dans les champs **ID utilisateur** et **Nom de l’imprimante** et ne renseignez pas le champ **ID état**. Cette entrée fait la même chose que l′action **Définir comme imprimante par défaut** sur la page **Gestion d′impression**.|
|Définir l’imprimante par défaut pour tous les rapports de tous les utilisateurs|Spécifiez une valeur dans le champ **Nom de l’imprimante** et ne renseignez pas les champs **ID utilisateur** et **ID état**. Cette entrée fait la même chose que l′action **Définir comme imprimante par défaut pour tous les utilisateurs** sur la page **Gestion d′impression**.|
|Imprimer un état spécifique sur l’imprimante par défaut de l’utilisateur|Spécifiez une valeur dans le champ **ID état** et ne renseignez pas les champs **Nom de l’imprimante** et **ID utilisateur**.|
|Imprimer un état spécifique sur une imprimante spécifique pour un utilisateur spécifique|Spécifiez une valeur dans les trois champs.|

> [!NOTE]
> Des sélections d’imprimantes plus spécifiques prévalent sur des sélections d’imprimantes plus générales. Par exemple, une sélection d’imprimante ayant des valeurs dans les champs **ID utilisateur**, **ID état** et **Nom de l’imprimante** prévaut sur une sélection d’imprimante ayant des entrées vides dans le champ **ID utilisateur** ou **ID état**.

### <a name="choosing-the-printer-when-running-a-report"></a>Choix de l’imprimante pendant l’exécution d’un rapport
Au lieu d’utiliser l’imprimante par défaut lors de l’exécution d’un rapport, vous pouvez remplacer ce paramètre à partir de la page de demande. Choisissez simplement l’imprimante que vous souhaitez utiliser pour cette invocation du rapport dans le menu déroulant **Imprimante**.

### <a name="sizing-print-jobs"></a>Dimensionnement des travaux d’impression

L’impression cloud est conçue pour des documents de taille raisonnable. La plupart des services cloud, y compris PrintNode et HP ePrint, ont une limite de 10 Mo par tâche. Si vous devez imprimer des rapports plus volumineux, vous devrez peut-être les diviser en plusieurs impressions.

## <a name="see-also"></a>Voir aussi

[Impression d’un état](ui-work-report.md#PrintReport)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exécuter des traitements par lots](ui-how-run-batch-jobs.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
