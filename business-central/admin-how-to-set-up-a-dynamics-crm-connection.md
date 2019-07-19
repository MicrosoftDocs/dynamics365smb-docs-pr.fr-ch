---
title: Se connecter à Dynamics 365 for Sales | Microsoft Docs
description: Vous pouvez procéder à l'intégration à Dynamics 365 for Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/06/2019
ms.author: bholtorf
ms.openlocfilehash: dfcb664d352683566df233d6b9b95900f2d76a5a
ms.sourcegitcommit: f2e3b571eab6e01d9f5aa8ef47056b6bd313dcbd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/13/2019
ms.locfileid: "1629657"
---
# <a name="set-up-a-connection-to-dynamics-365-for-sales"></a>Configurer une connexion vers Dynamics 365 for Sales
Pour procéder à l'intégration à [!INCLUDE[crm_md](includes/crm_md.md)], vous devez configurer une connexion entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085501]

## <a name="before-you-start"></a>Avant de commencer
Avant de commencer à connecter les applications, voici quelques informations utiles qu'il convient de préparer :  

* Une URL pour votre application [!INCLUDE[crm_md](includes/crm_md.md)]. Une façon rapide d'obtenir l'URL consiste à ouvrir [!INCLUDE[crm_md](includes/crm_md.md)] et à copier l'URL, puis à la coller dans le champ **URL Dynamics 365 for Sales** dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. [!INCLUDE[d365fin](includes/d365fin_md.md)] corrigera le formatage pour vous.  
* Un nom d'utilisateur et un mot de passe d'un compte utilisateur utilisés uniquement pour l'intégration.  
* Le nom d'utilisateur et le mot de passe du compte ont les autorisations de l'administrateur.  

> [!Note]
> Ces étapes décrivent la procédure pour la version en ligne de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-test-and-enable-a-connection-to-includecrmmdincludescrmmdmd"></a>Configurer, tester et activer une connexion vers [!INCLUDE[crm_md](includes/crm_md.md)]  
Pour tous les types d'authentification autres que l'authentification Office 365, configurez votre connexion à Dynamics 365 for Sales sur la page **Configuration de la connexion Microsoft Dynamics 365 for Sales**. Pour l'authentification Office 365, vous pouvez également utiliser le guide de configuration assistée **Configurer la connexion Dynamics 365 for Sales**, qui vous aidera à fournir les informations requises.

### <a name="to-use-an-assisted-setup-guide"></a>Pour utiliser un guide de configuration assistée
Le guide de configuration assistée **Configurer la connexion Dynamics 365 for Sales** vous permet de configurer la connexion et de préciser s'il convient d'activer des fonctions avancées, comme le couplage entre les enregistrements.

1. Choisissez **Configuration et extensions**, puis **Configuration assistée**.
2. Sélectionnez **Configurer la connexion Dynamics 365 for Sales** pour lancer le guide de configuration assistée.
3. Renseignez les champs selon vos besoins.
4. Éventuellement, des paramètres avancés peuvent améliorer la sécurité et activer des fonctionnalités supplémentaires de [!INCLUDE[crm_md](includes/crm_md.md)], telles que le traitement de la commande vente et la visualisation des niveaux de stock. Le tableau suivant décrit les paramètres avancés.  

|Champ|Description|
|-----|-----|
|**Importer la solution Dynamics 365 for Sales**|Activez cette fonctionnalité pour installer et configurer la solution d'intégration dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour en savoir plus, reportez-vous à la rubrique [À propos de la solution d'intégration Business Central](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|
|**Publier le service Web de disponibilité des articles**|Laissez les utilisateurs de [!INCLUDE[crm_md](includes/crm_md.md)] voir la disponibilité des articles (produits) en stock dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cela nécessite que le compte d'utilisateur [!INCLUDE[d365fin](includes/d365fin_md.md)] ait une clé d'accès aux services Web. L'affectation de la clé est un processus en deux étapes. Sur le compte d'utilisateur dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez choisir l'action **Modifier la clé de service Web**. Dans le guide de configuration assistée Configurer la connexion Dynamics 365 for Sales, vous devez préciser l'URL de service Web OData Dynamics 365 Business Central et fournir les identifiants d'utilisateur [!INCLUDE[d365fin](includes/d365fin_md.md)] pour accéder au service. Pour plus d'informations, reportez-vous à la rubrique [Services Web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**URL du service Web OData Dynamics 365 Business Central**|Si vous activez le service Web de disponibilité des articles, l'URL du service Web OData est renseignée pour vous.|
|**Nom d'utilisateur du service Web OData Dynamics 365 Business Central**|Il s'agit du nom du compte d'utilisateur [!INCLUDE[d365fin](includes/d365fin_md.md)] que le [!INCLUDE[crm_md](includes/crm_md.md)] utilise pour récupérer les informations concernant la disponibilité des articles dans [!INCLUDE[d365fin](includes/d365fin_md.md)] via le service Web OData.|
|**Clé d'accès au service Web OData Dynamics 365 Business Central**|Il s'agit de la clé d'accès pour le compte d'utilisateur que le [!INCLUDE[crm_md](includes/crm_md.md)] utilise pour obtenir des informations concernant la disponibilité des articles depuis [!INCLUDE[d365fin](includes/d365fin_md.md)] via le service Web OData. La clé est assignée à l'utilisateur choisi dans le champ **Nom d'utilisateur du service Web OData Dynamics 365 Business Central**. Pour obtenir la clé, sélectionnez le bouton **Rechercher la valeur** en regard du nom d'utilisateur, sélectionnez l'utilisateur, puis **Gérer** et enfin **Modifier**. Sur la fiche d'utilisateur, sélectionnez **Actions**, **Authentification**, puis choisissez **Modifier la clé du service Web**.|
|**Activer l'intégration de la commande vente**|Lorsque des personnes créent des commandes vente dans [!INCLUDE[crm_md](includes/crm_md.md)], copiez les commandes vers [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cela suppose que vous fournissiez des informations d'identification pour un compte utilisateur de l'administrateur dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d'informations, reportez-vous à la rubrique [Gestion des données de commandes vente spéciales](marketing-integrate-dynamicscrm.md#handling-sales-order-data).|
|**Activer la connexion Dynamics 365 for Sales**|Activez la connexion vers [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Version du SDK Dynamics 365**|Cela est pertinent uniquement si vous l'intégrez à une version locale de [!INCLUDE[crm_md](includes/crm_md.md)]. Il s'agit du kit de développement logiciel Dynamics 365 (également appelé Xrm) que vous utilisez pour connecter [!INCLUDE[d365fin](includes/d365fin_md.md)] à [!INCLUDE[crm_md](includes/crm_md.md)]. La version doit être compatible à la version du SDK utilisée par [!INCLUDE[crm_md](includes/crm_md.md)], et identique ou plus récente que la version utilisée par [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> Le guide de configuration assistée **Configurer la connexion Dynamics 365 for Sales** affecte automatiquement les rôles de sécurité **Administrateur d'intégration** et **Utilisateur d'intégration** au compte utilisateur utilisé pour l'intégration. 

### <a name="to-create-or-maintain-the-connection-manually"></a>Pour créer ou conserver manuellement la connexion
La procédure suivante décrit comment renseigner manuellement les champs sur la page **Configuration de la connexion Microsoft Dynamics 365 for Sales**. Il s'agit également de la page sur laquelle vous gérez les paramètres pour l'intégration.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration de la connexion Microsoft Dynamics 365**, puis choisissez le lien associé.
2. Saisissez les informations suivantes pour la connexion de [!INCLUDE[crm_md](includes/crm_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Champ|Description|
|-----|-----|
|**URL Dynamics 365 for Sales**|L'URL pour votre instance de [!INCLUDE[crm_md](includes/crm_md.md)]. Pour obtenir l'URL, ouvrez [!INCLUDE[crm_md](includes/crm_md.md)], copiez l'URL depuis la barre d'adresses de votre navigateur, puis collez l'URL dans le champ. [!INCLUDE[d365fin](includes/d365fin_md.md)] veillera à ce que le format soit correct.|
|**Nom d'utilisateur** et **Mot de passe**|Il s'agit des informations d'identification du compte d'utilisateur dédié à l'intégration. Pour en savoir plus, reportez-vous à la rubrique [Configuration des comptes d'utilisateur pour l'intégration à Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).|
|**Activé**|Commencez avec l'intégration. Si vous n'activez pas la connexion tout de suite, les paramètres de connexion seront sauvegardés, mais les utilisateurs ne seront pas en mesure d'accéder aux données [!INCLUDE[crm_md](includes/crm_md.md)] à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vous pouvez revenir sur cette page et activer la connexion ultérieurement.  |
|**Version du SDK Dynamics 365**|Si vous procédez à l'intégration avec une version locale de [!INCLUDE[crm_md](includes/crm_md.md)], utilisez le kit de développement logiciel Dynamics 365 (également appelé Xrm) pour connecter [!INCLUDE[d365fin](includes/d365fin_md.md)] à [!INCLUDE[crm_md](includes/crm_md.md)]. La version que vous sélectionnez doit être compatible avec la version du SDK utilisée par [!INCLUDE[crm_md](includes/crm_md.md)]. Cette version est égale ou plus récente que la version utilisée par [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> Si vous connectez une version locale de [!INCLUDE[d365fin](includes/d365fin_md.md)] à [!INCLUDE[crm_md](includes/crm_md.md)] et si vous souhaitez configurer une connexion à une instance [!INCLUDE[crm_md](includes/crm_md.md)] avec un type d'authentification spécifique, complétez les champs sur le raccourci **Détails du type d'authentification**. Pour en savoir plus, reportez-vous à la rubrique [Utiliser les chaînes de connexion dans les outils XRM pour procéder à la connexion avec Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Cette étape n'est pas requise lors de la connexion d'une version en ligne de [!INCLUDE[d365fin](includes/d365fin_md.md)].

3. Saisissez les informations suivantes pour la connexion de [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)].

|Champ|Description|
|-----|-----|
|**URL du client web Dynamics 365 Business Central**|L'URL de votre instance de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Elle permet aux utilisateurs de [!INCLUDE[crm_md](includes/crm_md.md)] d'ouvrir les enregistrements correspondants dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à partir des enregistrements [!INCLUDE[crm_md](includes/crm_md.md)], tels qu'un compte ou un produit. Les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] s'ouvrent dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Définissez ce champ sur l'URL de l'instance [!INCLUDE[d365fin](includes/d365fin_md.md)] à utiliser.<br /><br /> Pour rétablir le champ sur l'URL par défaut pour le [!INCLUDE[d365fin](includes/d365fin_md.md)], sélectionnez **Réinitialiser l'URL du client Web**.<br /><br /> Ce champ n'est utile que si la solution d'intégration de [!INCLUDE[d365fin](includes/d365fin_md.md)] est installée dans [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Service Web Disponibilité article activé**|Laissez les utilisateurs de [!INCLUDE[crm_md](includes/crm_md.md)] voir la disponibilité des articles (produits) en stock dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si vous activez cette fonctionnalité, vous devez également fournir un nom d'utilisateur et une clé d'accès afin que [!INCLUDE[crm_md](includes/crm_md.md)] utilise le service Web OData pour demander la disponibilité des articles (produits). Pour plus d'informations, reportez-vous à la rubrique [Services Web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**URL du service Web OData Dynamics 365 Business Central**|Si vous activez le service Web de disponibilité des articles, l'URL du service Web OData est renseignée pour vous.|
|**Nom d'utilisateur du service Web OData Dynamics 365 Business Central**|Il s'agit du nom du compte d'utilisateur que le [!INCLUDE[crm_md](includes/crm_md.md)] utilise pour récupérer les informations concernant la disponibilité des articles dans [!INCLUDE[d365fin](includes/d365fin_md.md)] via le service Web OData.|
|**Clé d'accès au service Web OData Dynamics 365 Business Central**|Il s'agit de la clé d'accès pour le compte d'utilisateur que le [!INCLUDE[crm_md](includes/crm_md.md)] utilise pour obtenir des informations concernant la disponibilité des articles depuis [!INCLUDE[d365fin](includes/d365fin_md.md)] via le service Web OData. La clé est assignée à l'utilisateur choisi dans le champ **Nom d'utilisateur du service Web OData Dynamics 365 Business Central**. Pour obtenir la clé, sélectionnez le bouton **Rechercher la valeur** en regard du nom d'utilisateur, sélectionnez l'utilisateur, puis **Gérer** et enfin **Modifier**. Sur la fiche d'utilisateur, sélectionnez **Actions**, **Authentification**, puis choisissez **Modifier la clé du service Web**.|

4. Saisissez les paramètres suivants pour [!INCLUDE[crm_md](includes/crm_md.md)].

|Champ|Description|
|-----|-----|
|**L'intégration des commandes vente est activée**|Laissez les utilisateurs envoyer les commandes vente et les devis activés dans [!INCLUDE[crm_md](includes/crm_md.md)], et les visualiser et les traiter dans [!INCLUDE[d365fin](includes/d365fin_md.md)].|
|**Créer automatiquement des commandes vente**|Permet de créer une commande vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)] lorsqu'un utilisateur en crée et en envoie une dans [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Traiter automatiquement les devis**|Permet de traiter un devis dans [!INCLUDE[d365fin](includes/d365fin_md.md)] lorsqu'un utilisateur en crée et en active un dans [!INCLUDE[crm_md](includes/crm_md.md)].|

5. Saisissez les paramètres avancés suivants.

|Champ|Description|
|-----|-----|
|**Les utilisateurs [!INCLUDE[d365fin](includes/d365fin_md.md)] doivent correspondre aux utilisateurs Dynamics 365 for Sales**|Spécifiez si les comptes d'utilisateur [!INCLUDE[d365fin](includes/d365fin_md.md)] doivent avoir des comptes d'utilisateur correspondants dans [!INCLUDE[crm_md](includes/crm_md.md)]. L'**adresse électronique pour l'authentification Office 365** de l'utilisateur [!INCLUDE[d365fin](includes/d365fin_md.md)] doit être identique à l'**adresse électronique principale** de l'utilisateur [!INCLUDE[crm_md](includes/crm_md.md)].<br /><br /> Si vous définissez la valeur sur **Oui**, les utilisateurs [!INCLUDE[d365fin](includes/d365fin_md.md)] qui n'ont pas un compte d'utilisateur [!INCLUDE[crm_md](includes/crm_md.md)] correspondant ne disposeront pas de fonctions d'intégration de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans l'interface utilisateur. L'accès aux données [!INCLUDE[crm_md](includes/crm_md.md)] directement à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)] se fait au nom du compte d'utilisateur [!INCLUDE[crm_md](includes/crm_md.md)].<br /><br /> Si vous définissez la valeur sur **Non**, tous les utilisateurs [!INCLUDE[d365fin](includes/d365fin_md.md)] disposeront de fonctions d'intégration de [!INCLUDE[crm_md](includes/crm_md.md)] dans l'interface utilisateur. L'accès aux données [!INCLUDE[crm_md](includes/crm_md.md)] directement à partir de [!INCLUDE[crm_md](includes/crm_md.md)] se fait au nom de l'utilisateur (intégration) de connexion.|
|**L'utilisateur Business Central actuel est associé à un utilisateur Dynamics 365 for Sales**|Indique si votre compte d'utilisateur correspond à un compte dans [!INCLUDE[crm_md](includes/crm_md.md)]|

6. Pour tester les paramètres de connexion, choisissez **Tester la connexion**.  

    > [!NOTE]  
    >  Si le chiffrement des données n'est pas activé dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous recevrez un message vous demandant si vous souhaitez l'activer. Pour activer le chiffrement des données, cliquez sur **Oui** et fournissez les informations requises. Sinon, sélectionnez **Non**. Vous pouvez activer le chiffrement des données ultérieurement. Pour plus d'informations, voir [Chiffrement des données dans Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) de l'aide sur Developer and IT Pro.  

7. Si la synchronisation de [!INCLUDE[crm_md](includes/crm_md.md)] n'est pas déjà configurée, vous recevrez un message vous demandant si vous souhaitez utiliser les paramètres de synchronisation par défaut. Selon que vous souhaitez conserver ou non les enregistrements alignés dans [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)], sélectionnez **Oui** ou **Non**.

> [!Note]
> La connexion à Dynamics 365 for Sales à l'aide de la page Paramètres de la connexion **Microsoft Dynamics 365 for Sales** peut nécessiter que vous affectiez les rôles de sécurité Administrateur d'intégration et Utilisateur d'intégration au compte utilisateur utilisé pour l'intégration. Pour plus d'informations, voir [Attribuer un rôle de sécurité à un utilisateur](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user).


> [!Note]
> La connexion à Dynamics 365 for Sales à l'aide de la page **Paramètres de la connexion Microsoft Dynamics 365 for Sales** peut nécessiter que vous [affectiez les rôles de sécurité **Administrateur d'intégration** et **Utilisateur d'intégration**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user) au compte utilisateur utilisé pour l'intégration.


### <a name="to-disconnect-from-includecrmmdincludescrmmdmd"></a>Pour se déconnecter de [!INCLUDE[crm_md](includes/crm_md.md)]  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration de la connexion Microsoft Dynamics 365 for Sales**, puis choisissez le lien associé.
2. Sur la page **Configuration de la connexion Microsoft Dynamics 365 for Sales**, décochez la case **Activé**.  

<!--## Install the [!INCLUDE[d365fin](includes/d365fin_md.md) Integration Solution
[!INCLUDE[d365fin](includes/d365fin_md.md)] includes a solution that enables users to access coupled records, such as customers and items, from records in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts and products. The solution adds a link to the pages in [!INCLUDE[crm_md](includes/crm_md.md)] to open the coupled [!INCLUDE[d365fin](includes/d365fin_md.md)] record. The solution also displays information from [!INCLUDE[d365fin](includes/d365fin_md.md)]on certain entities in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts. Installing this solution is optional. <!--"Solution" sounds old school. Is it an app, or an add-in, or an extension?


1.  From [!INCLUDE[d365fin](includes/d365fin_md.md)] installation media \(DVD\), copy the DynamicsNAVIntegrationSolution.zip file to your computer.  

     The DynamicsNAVIntegrationSolution.zip file is located in the **CrmCustomization** folder. This file is the solution package.   

2.  In [!INCLUDE[crm_md](includes/crm_md.md)], import the DynamicsNAVIntegrationSolution.zip as a solution.  

     This step adds the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity and **[!INCLUDE[d365fin](includes/d365fin_md.md) Account Statistics** entity in the system and additional items such as [!INCLUDE[d365fin](includes/d365fin_md.md)] integration security roles.  

     For more information about how to manage solutions in [!INCLUDE[crm_md](includes/crm_md.md)], [http://go.microsoft.com/fwlink/?LinkID=616519](http://go.microsoft.com/fwlink/?LinkID=616519).  

3.  Optional: Set up the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity to display in the **Settings** area of [!INCLUDE[crm_md](includes/crm_md.md)].  

     This enables [!INCLUDE[crm_md](includes/crm_md.md)] users who are assigned the **[!INCLUDE[d365fin](includes/d365fin_md.md) Admin** role to modify the entity in [!INCLUDE[crm_md](includes/crm_md.md)]. For more information about how to modify entities in [!INCLUDE[crm_md](includes/crm_md.md)], see [View or edit entity information](http://go.microsoft.com/fwlink/?LinkID=616521).  

4.  Assign the **[!INCLUDE[d365fin](includes/d365fin_md.md) Integration Administrator** role to the user account for the connection to [!INCLUDE[d365fin](includes/d365fin_md.md)].  

5.  Assign the **Business Central Integration User** role to all users who will use the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution.  

If you install the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution after you have set up the connection to [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must modify the connection setup to point to the URL.-->

<!--of the [!INCLUDE[nav_web_md](../developer/includes/nav_web_md.md)]. For more information, see [How to: Set Up a Microsoft Dynamics 365 for Sales Connection]() -->

<!--
# View Item Availability - Support Matrix
For most versions of [!INCLUDE[d365fin](includes/d365fin_md.md) and Dynamics 365 for Sales, you can view availability figures for items across the integrated products. The following table shows which version combinations support viewing item availability.

| |Dynamics 365 for Sales version|2015/Update 1/Online|2016/Update 1/Online|Dynamics 365 for Sales|
|-|---------------------|---------------------|--------------------------|-----------------|
|**Dynamics NAV version**|
|**2016**||Not supported|Not supported|Not supported|
|**2017**||Not supported - Install from 2016|Supported|Supported|
|**Dynamics 365 for Financials**||Not supported - Install from 2016|Supported|Supported|


> [Note]
> You can obtain item availability support for combinations of Dynamics CRM 2015 and Business Central by running the DynamicsNAVIntegrationSolution.zip file on the Business Central product DVD.

For more information, see [System Requirements for Business Central](../deployment/system-requirement-business-central.md).

-->

## <a name="see-also"></a>Voir aussi  
[Afficher le statut d'une synchronisation](admin-how-to-view-synchronization-status.md)  
