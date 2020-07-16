---
title: Intégration à Dynamics 365 Sales | Microsoft Docs
description: Découvrez comment préparer Dynamics 365 Business Central pour l'intégrer à Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 06/30/2020
ms.author: bholtorf
ms.openlocfilehash: c42393145fc921c85570e0829c0953757981b53e
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529028"
---
# <a name="integrating-with-dynamics-365-sales"></a>Intégration à Dynamics 365 Sales

Le rôle de vendeur est souvent considéré comme tourné vers l'extérieur dans une entreprise. Toutefois, il peut être utile pour les vendeurs d'être en mesure de regarder à l'intérieur de l'entreprise et d'observer ce qu'il s'y passe en arrière-plan. En intégrant [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)], vous pouvez donner à vos vendeurs cet aperçu en leur permettant de visualiser les informations dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pendant qu'ils travaillent dans [!INCLUDE[crm_md](includes/crm_md.md)]. Par exemple, dans le cadre de la préparation d'un devis, il peut s'avérer utile de savoir si vous avez suffisamment de stock pour répondre à la commande. Pour plus d'informations, voir [Utilisation de Dynamics 365 Sales depuis Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Cette rubrique décrit le processus d'intégration des versions en ligne de [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)] au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)]. Pour plus d'informations sur la configuration sur site, voir [Préparation de l'intégration à Dynamics 365 Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-common-data-service"></a>Intégration au moyen de Common Data Service
[!INCLUDE[d365fin](includes/d365fin_md.md)] s'intègre également à [!INCLUDE[d365fin](includes/cds_long_md.md)], ce qui facilite la connexion et la synchronisation des données avec d'autres applications Dynamics 365 telles que [!INCLUDE[crm_md](includes/crm_md.md)], voire des applications que vous créez vous-même. S'il s'agit de votre toute première intégration, nous vous recommandons de l'effectuer au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)]. Pour en savoir plus, consultez [Intégration à Common Data Service](admin-common-data-service.md).

Si vous avez déjà intégré [!INCLUDE[crm_md](includes/crm_md.md)] à [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez continuer à synchroniser les données à l'aide de votre configuration. Cependant, si vous mettez à niveau ou désactivez votre intégration [!INCLUDE[crm_md](includes/crm_md.md)], vous devez vous connecter au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)] pour la réactiver. Pour en savoir plus, consultez [Mise à niveau d'une intégration à Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> La reconnexion au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)] applique les paramètres de synchronisation par défaut et remplace toute configuration dont vous disposez. Par exemple, les mappages de table par défaut sont appliqués.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Paramètres d'intégration dédiés à une intégration [!INCLUDE[crm_md](includes/crm_md.md)]
L'intégration à [!INCLUDE[d365fin](includes/d365fin_md.md)] se produit au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)], et de nombreux paramètres et entités standard sont fournis par l'intégration. Outre les paramètres standard, certains sont dédiés à [!INCLUDE[crm_md](includes/crm_md.md)]. Les sections suivantes les répertorient.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Autorisations et rôles de sécurité pour les comptes d'utilisateur dans Sales
Lorsque vous installez la solution d'intégration, les autorisations pour le compte d'utilisateur d'intégration sont configurées. Si ces autorisations sont modifiées, vous devrez peut-être les réinitialiser. Vous pouvez le faire en réinstallant la solution d'intégration en choisissant **Redéployer la solution d'intégration** sur la page **Paramètres de la connexion Dynamics 365**. Les rôles de sécurité suivants sont déployés :

* Administrateur d'intégration Dynamics 365 Business Central
* Utilisateur d'intégration Dynamics 365 Business Central
* Utilisateur de disponibilité produit Dynamics 365 Business Central

### <a name="connection-settings-in-the-setup-guide"></a>Paramètres de connexion dans le guide de configuration
Vous pouvez utiliser un guide de configuration assistée pour configurer rapidement la connexion et spécifier des fonctions avancées, comme le couplage entre les enregistrements.

1. Choisissez **Configuration et extensions**, puis **Configuration assistée**.
2. Sélectionnez **Configurer la connexion Dynamics 365 Sales** pour lancer le guide de configuration assistée.
3. Renseignez les champs selon vos besoins.
4. Éventuellement, des paramètres avancés peuvent améliorer la sécurité et activer des fonctionnalités supplémentaires telles que le traitement des commandes vente et la visualisation des niveaux de stock. Le tableau suivant décrit les paramètres avancés.  

|Champ|Description|
|-----|-----------|
|**Importer une solution Dynamics 365 Sales**|Activez cette fonctionnalité pour installer et configurer la solution d'intégration dans [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic-->|
|**Publier le service Web de disponibilité des articles**|Laissez les utilisateurs de [!INCLUDE[crm_md](includes/crm_md.md)] voir la disponibilité des articles (produits) en stock dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cela nécessite qu'un compte d'utilisateur [!INCLUDE[d365fin](includes/d365fin_md.md)] ait une clé d'accès aux services Web. L'affectation de la clé est un processus en deux étapes. Sur le compte d'utilisateur dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez choisir l'action **Modifier la clé de service Web**. Dans le guide de configuration assistée Configuration de la connexion Dynamics 365 Sales, vous devez préciser l'URL de service Web OData Dynamics 365 Business Central et fournir les identifiants d'utilisateur [!INCLUDE[d365fin](includes/d365fin_md.md)] pour accéder au service. Pour plus d'informations, reportez-vous à la rubrique [Services Web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**URL du service Web OData Business Central**|Si vous activez le service Web pour visualiser la disponibilité des articles, l'URL du service Web OData est renseignée pour vous.|
|**Nom d'utilisateur du service Web OData Business Central**|Il s'agit du nom du compte d'utilisateur [!INCLUDE[d365fin](includes/d365fin_md.md)] que [!INCLUDE[crm_md](includes/crm_md.md)] utilise pour récupérer les informations concernant la disponibilité des articles dans [!INCLUDE[d365fin](includes/d365fin_md.md)] via le service Web OData.|
|**Clé d'accès du service Web OData Business Central**|Il s'agit de la clé d'accès pour le compte d'utilisateur que [!INCLUDE[crm_md](includes/crm_md.md)] utilise pour obtenir des informations concernant la disponibilité des articles depuis [!INCLUDE[d365fin](includes/d365fin_md.md)] via le service Web OData. La clé est assignée à l'utilisateur choisi dans le champ **Nom d'utilisateur du service Web OData Business Central**. Pour obtenir la clé, sélectionnez le bouton **Rechercher la valeur** en regard du nom d'utilisateur, sélectionnez l'utilisateur, puis **Gérer** et enfin **Modifier**. Sur la fiche d'utilisateur, sélectionnez **Actions**, **Authentification**, puis choisissez **Modifier la clé du service Web**.|
|**Activer l'intégration de la commande vente**|Quand les utilisateurs créent des commandes vente dans [!INCLUDE[crm_md](includes/crm_md.md)] et exécutent les commandes dans [!INCLUDE[d365fin](includes/d365fin_md.md)], cela intègre le processus dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d'informations, voir [Activer l'intégration du traitement des commandes client](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Cela suppose que vous fournissiez des informations d'identification pour un compte utilisateur de l'administrateur dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d'informations, reportez-vous à la rubrique [Gestion des données de commandes vente spéciales](marketing-integrate-dynamicscrm.md#handling-sales-order-data).|
|**Activer la connexion CDS**|Activez la connexion vers [!INCLUDE[d365fin](includes/cds_long_md.md)].|
|**Version du SDK Dynamics 365**|Cela est pertinent uniquement si vous l'intégrez à une version locale de [!INCLUDE[crm_md](includes/crm_md.md)]. Il s'agit du kit de développement logiciel Dynamics 365 (également appelé Xrm) que vous utilisez pour connecter [!INCLUDE[d365fin](includes/d365fin_md.md)] à [!INCLUDE[crm_md](includes/crm_md.md)]. La version doit être compatible à la version du SDK utilisée par [!INCLUDE[crm_md](includes/crm_md.md)], et identique ou plus récente que la version utilisée par [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Paramètres de connexion sur la page Paramètres de la connexion Microsoft Dynamics 365 
Saisissez les informations suivantes pour la connexion de [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)].

|Champ|Description|
|-----|-----------|
|**URL Dynamics 365 Sales**|L'URL de votre instance de [!INCLUDE[crm_md](includes/crm_md.md)]. Elle permet aux utilisateurs d'ouvrir les enregistrements correspondants dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à partir des enregistrements dans [!INCLUDE[crm_md](includes/crm_md.md)], tels qu'un compte ou un produit. Les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] s'ouvrent dans [!INCLUDE[d365fin](includes/d365fin_md.md)].|
|**Service Web Disponibilité article activé**|Autorisez les utilisateurs de [!INCLUDE[crm_md](includes/crm_md.md)] à voir la disponibilité des articles (produits) en stock dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si vous activez cette fonctionnalité, vous devez également fournir un nom d'utilisateur et une clé d'accès afin que [!INCLUDE[crm_md](includes/crm_md.md)] utilise le service Web OData pour demander la disponibilité des articles (produits). Pour plus d'informations, reportez-vous à la rubrique [Services Web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**URL du service Web OData Dynamics 365 Business Central**|Si vous activez le service Web de disponibilité des articles, l'URL du service Web OData est renseignée pour vous. Définissez ce champ sur l'URL de l'instance [!INCLUDE[d365fin](includes/d365fin_md.md)] à utiliser.<br /><br /> Pour rétablir le champ sur l'URL par défaut pour le [!INCLUDE[d365fin](includes/d365fin_md.md)], sélectionnez **Réinitialiser l'URL du client Web**.<br /><br /> Ce champ n'est utile que si la solution d'intégration de [!INCLUDE[d365fin](includes/d365fin_md.md)] est installée dans [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Nom d'utilisateur du service Web OData Dynamics 365 Business Central**|Il s'agit du nom du compte d'utilisateur que le [!INCLUDE[crm_md](includes/crm_md.md)] utilise pour récupérer les informations concernant la disponibilité des articles dans [!INCLUDE[d365fin](includes/d365fin_md.md)] via le service Web OData.|
|**Clé d'accès au service Web OData Dynamics 365 Business Central**|Il s'agit de la clé d'accès pour le compte d'utilisateur que le [!INCLUDE[crm_md](includes/crm_md.md)] utilise pour obtenir des informations concernant la disponibilité des articles depuis [!INCLUDE[d365fin](includes/d365fin_md.md)] via le service Web OData. La clé est assignée à l'utilisateur choisi dans le champ **Nom d'utilisateur du service Web OData Dynamics 365 Business Central**. Pour obtenir la clé, sélectionnez le bouton **Rechercher la valeur** en regard du nom d'utilisateur, sélectionnez l'utilisateur, puis **Gérer** et enfin **Modifier**. Sur la fiche d'utilisateur, sélectionnez **Actions**, **Authentification**, puis choisissez **Modifier la clé du service Web**.|
|**Version du SDK Dynamics 365**|Si vous procédez à l'intégration avec une version locale de [!INCLUDE[crm_md](includes/crm_md.md)], utilisez le kit de développement logiciel Dynamics 365 (également appelé Xrm) pour connecter [!INCLUDE[d365fin](includes/d365fin_md.md)] à [!INCLUDE[crm_md](includes/crm_md.md)]. La version que vous sélectionnez doit être compatible avec la version du SDK utilisée par [!INCLUDE[crm_md](includes/crm_md.md)]. Cette version est égale ou plus récente que la version utilisée par [!INCLUDE[crm_md](includes/crm_md.md)].|-->

Outre les paramètres ci-dessus, saisissez les paramètres suivants pour [!INCLUDE[crm_md](includes/crm_md.md)].

|Champ|Description|
|-----|-----|
|**L'intégration des commandes vente est activée**|Laissez les utilisateurs envoyer les commandes vente et les devis activés dans [!INCLUDE[crm_md](includes/crm_md.md)], et les visualiser et les traiter dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cela intègre le processus dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d'informations, voir [Activer l'intégration du traitement des commandes client](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).|
|**Créer automatiquement des commandes vente**|Permet de créer une commande vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)] lorsqu'un utilisateur en crée et en envoie une dans [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Traiter automatiquement les devis**|Permet de traiter un devis dans [!INCLUDE[d365fin](includes/d365fin_md.md)] lorsqu'un utilisateur en crée et en active un dans [!INCLUDE[crm_md](includes/crm_md.md)].|

<!--
### User Account Settings
Integrate with Business Central through Common Data Service requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Mappage d'entité Sales standard pour la synchronisation
Les entités dans [!INCLUDE[crm_md](includes/crm_md.md)], telles que des commandes, sont intégrées aux types d'entités équivalents dans [!INCLUDE[d365fin](includes/d365fin_md.md)], tels que des commandes vente. Pour utiliser les données [!INCLUDE[crm_md](includes/crm_md.md)], vous configurez des liens, appelés couplages entre les entités dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)].

Le tableau suivant répertorie le mappage standard entre les entités dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] que [!INCLUDE[d365fin](includes/d365fin_md.md)] fournit.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[crm_md](includes/crm_md.md)]|Direction de synchronisation|Filtre par défaut|
|-------------------------------------------|--------------------------------------|-----------------|--------------|
|Unité de mesure|Groupe d'unités|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Article ;|Produit|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtre contact Sales : le **Type de produit** est **Stock de vente**|
|Ressource|Produit|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtre contact Sales : le **Type de produit** est **Services**|
|Groupe prix client|Liste des prix|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Prix vente|Tarifs produit|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|Filtre contact [!INCLUDE[d365fin](includes/d365fin_md.md)] : le champ **Code de vente** n'est pas vide, le champ **Type de vente** est défini sur **Groupe prix client**|
|Opportunité|Opportunité|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |
|En-tête facture vente|Facturer|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Ligne facture vente|Produit facture|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|En-tête de commande vente|Ecriture réservation|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|Filtre en-tête de vente [!INCLUDE[d365fin](includes/d365fin_md.md)] : le champ **Type de document** est défini sur Commande, le champ **Statut** est défini sur Lancé.|
|Remarques Commande vente|Remarques Commande vente|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |

### <a name="synchronization-rules"></a>Règles de synchronisation
Le tableau suivant répertorie les règles qui contrôlent la synchronisation entre [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ces règles s'ajoutent à celles définies pour Common Data Service, qui s'appliquent également. Pour en savoir plus, consultez [Mappage d'entité standard](/dynamics365/business-central/admin-synchronizing-business-central-and-sales?branch=master-cds-crm#standard-entity-mapping-for-synchronization).

> [!NOTE]  
> Les modifications apportées aux données par le compte d'utilisateur d'intégration ne sont pas synchronisées. Par conséquent, nous vous avons recommandé de ne pas modifier les données lors de l'utilisation de ce compte. Pour en savoir plus, reportez-vous à la rubrique [Configuration des comptes d'utilisateur pour l'intégration à Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Table|Règle|
|-----|----|
|Unités de mesure|Les unités de mesure sont synchronisées avec les groupes d'unités dans [!INCLUDE[crm_md](includes/crm_md.md)]. Une seule unité de mesure peut être définie dans le groupe d'unités.|
|Articles|Lors de la synchronisation d'articles avec des produits [!INCLUDE[crm_md](includes/crm_md.md)], [!INCLUDE[d365fin](includes/d365fin_md.md)] crée automatiquement une liste de prix dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour éviter les erreurs de synchronisation, vous ne devez pas modifier cette liste de prix manuellement.|
|Ressources|Les ressources sont synchronisées avec les produits [!INCLUDE[crm_md](includes/crm_md.md)] dont le type de produit est Service.|
|Groupes prix client|Les groupes de prix client sont synchronisés avec les listes de prix dans Sales.|
|Prix de vente|Les prix de vente dont le type vente est Groupe prix client et dont le code vente est défini sont synchronisés avec les lignes de liste de prix dans [!INCLUDE[crm_md](includes/crm_md.md)].|
|Opportunités|Les opportunités sont synchronisées avec les opportunités dans [!INCLUDE[crm_md](includes/crm_md.md)]. La valeur Code vendeur définit le propriétaire de l'entité couplée dans [!INCLUDE[crm_md](includes/crm_md.md)].|
|Factures vente enregistrées|Les factures vente validées sont synchronisées avec les factures vente. Pour qu'une facture puisse être synchronisée, il est préférable de synchroniser toutes les autres entités pouvant participer à la facture, depuis les vendeurs aux listes de prix. La valeur Code vendeur de l'en-tête de facture définit le propriétaire de l'entité couplée dans Sales.|
|Commandes vente|Lorsque l'intégration des commandes vente est activée, les commandes vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)] qui sont créées à partir des commandes vente soumises dans [!INCLUDE[crm_md](includes/crm_md.md)] sont synchronisées avec les commandes vente dans INCLUDE SALES lorsqu’elles sont validées. Avant de synchroniser les commandes, nous vous recommandons de synchroniser tout d’abord toutes les entités associées à la commande, telles que les commerciaux et les listes de prix. Le champ Code vendeur de l'en-tête de commande définit le propriétaire de l'entité couplée dans [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Projets de synchronisation pour une intégration de Sales
Les projets sont exécutés dans l'ordre suivant pour éviter les dépendances de couplage entre les entités. Il s'agit de projets supplémentaires disponibles à partir de Common Data Service. Pour plus d'informations, voir [Utiliser des files d'attente des travaux pour planifier des tâches](/dynamics365/business-central/admin-job-queues-schedule-tasks).

1. Projet de synchronisation Dynamics 365 Sales - UNITÉDEMESURE  
2. Projet de synchronisation Dynamics 365 Sales - RESSOURCE-PRODUIT  
3. Projet de synchronisation Dynamics 365 Sales - ARTICLE-PRODUIT  
4. Projet de synchronisation Dynamics 365 Sales - GRPPRXCLI-PRIX.
5. Projet de synchronisation Dynamics 365 Sales - PRXVENTE-PRXPROD.
6. Projet de synchronisation Dynamics 365 Sales - FACTVENTEVALIDÉES-FACT.

### <a name="default-synchronization-job-queue-entries"></a>Écritures de file projets de synchronisation par défaut  
Le tableau suivant décrit les projets de synchronisation par défaut pour Sales.  

|Écriture file d'attente des travaux|Description|Sens|Mappage de table d'intégration|Fréquence de synchronisation par défaut (minutes)|Temps de veille pour inactivité par défaut (minutes)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|Projet de synchronisation Dynamics 365 Sales - UNITÉDEMESURE|Permet de synchroniser les groupes d'unités [!INCLUDE[crm_md](includes/crm_md.md)] avec les unités de mesure [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|UNITÉ DE MESURE|30|720<br> (12 heures)|
|Projet de synchronisation Dynamics 365 Sales - RESSOURCE-PRODUIT|Permet de synchroniser les produits [!INCLUDE[crm_md](includes/crm_md.md)] avec les ressources [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE-PRODUIT|30|720<br> (12 heures)|
|Projet de synchronisation Dynamics 365 Sales - ARTICLE - PRODUIT|Permet de synchroniser les produits [!INCLUDE[crm_md](includes/crm_md.md)] avec les articles [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|ARTICLE-PRODUIT|30|1440<br> (24 heures)|
|Projet de synchronisation Dynamics 365 Sales - GRPPRXCLI-PRIX|Permet de synchroniser les listes de prix de vente [!INCLUDE[crm_md](includes/crm_md.md)] avec les groupes de prix client [!INCLUDE[d365fin](includes/d365fin_md.md)].| |GROUPES DE PRIX CLIENT - LISTES DE PRIX DE VENTE|30|1440<br> (24 heures)|
|Projet de synchronisation Dynamics 365 Sales - PRXVENTE-PRXPRODUIT|Permet de synchroniser les prix de produit [!INCLUDE[crm_md](includes/crm_md.md)] avec les prix de vente [!INCLUDE[d365fin](includes/d365fin_md.md)].||PRIX DE PRODUIT - PRIX DE VENTE|30|1440<br> (24 heures)|
|Projet de synchronisation Dynamics 365 Sales - FACTVENTEVALIDEES-FACT|Permet de synchroniser les factures [!INCLUDE[crm_md](includes/crm_md.md)] avec les factures vente [!INCLUDE[d365fin](includes/d365fin_md.md)] validées.|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|FACTURES - FACTURES VENTE VALIDÉES|30|1440<br> (24 heures)|
|Synchronisation Statistiques client - Dynamics 365 Sales|Permet de mettre à jour les comptes [!INCLUDE[crm_md](includes/crm_md.md)] avec les données client [!INCLUDE[d365fin](includes/d365fin_md.md)] les plus récentes. Dans [!INCLUDE[crm_md](includes/crm_md.md)], ces informations s'affichent dans le formulaire de vue rapide **Statistiques de compte Business Central** des comptes couplés avec les clients [!INCLUDE[d365fin](includes/d365fin_md.md)].<br /><br /> Ces données peuvent être également mises à jour manuellement depuis chaque enregistrement du client. Pour en savoir plus, reportez-vous à la rubrique [Coupler et synchroniser manuellement les enregistrements](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Remarque :** cette file d'attente de projets est pertinente uniquement si la solution d'intégration [!INCLUDE[d365fin](includes/d365fin_md.md)] est installée dans [!INCLUDE[crm_md](includes/crm_md.md)]. |Non applicable|Non applicable|30|Non applicable| 


### <a name="note-for-on-premises-versions"></a>Remarque pour les versions locales
> [!Note]
> Si vous connectez une version locale de [!INCLUDE[d365fin](includes/d365fin_md.md)] à [!INCLUDE[crm_md](includes/crm_md.md)] et si vous souhaitez configurer une connexion à une instance [!INCLUDE[crm_md](includes/crm_md.md)] avec un type d'authentification spécifique, renseignez les champs du raccourci **Détails du type d'authentification**. Pour en savoir plus, reportez-vous à la rubrique [Utiliser les chaînes de connexion dans les outils XRM pour procéder à la connexion avec Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Cette étape n'est pas requise lors de la connexion d'une version en ligne de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Voir aussi  
[Configuration des comptes d'utilisateur pour intégration à [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Configurer une connexion vers [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Synchronisation de Business Central et de [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Préparation de l'intégration à Dynamics 365 Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)
