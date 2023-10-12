---
title: Intégration à Dynamics 365 Sales
description: Découvrez comment préparer Dynamics 365 Business Central pour l’intégrer à Dynamics 365 Sales.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'sales, crm, integration, integrating'
ms.date: 09/28/2023
ms.author: bholtorf
ms.custom: bap-template
---
# Intégration à Dynamics 365 Sales

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Le rôle de vendeur est souvent considéré comme tourné vers l’extérieur dans une entreprise. Toutefois, il peut être utile pour les vendeurs d’être en mesure de regarder à l’intérieur de l’entreprise et d’observer ce qu’il s’y passe en arrière-plan. En intégrant [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[crm_md](includes/crm_md.md)], vous pouvez donner cet aperçu à vos commerciaux. L’intégration permet aux individus de voir les informations dans [!INCLUDE[prod_short](includes/prod_short.md)] pendant qu’ils travaillent dans [!INCLUDE[crm_md](includes/crm_md.md)]. Par exemple, dans le cadre de la préparation d’un devis, il peut s’avérer utile de savoir si vous avez suffisamment de stock pour répondre à la commande. Pour plus d’informations, voir [Utiliser Dynamics 365 Sales depuis Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Cette rubrique décrit le processus d’intégration des versions en ligne de [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[prod_short](includes/prod_short.md)] au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Pour plus d’informations sur la configuration sur site, voir [Préparation de l’intégration à Dynamics 365 Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## Intégration au moyen de Dataverse
Pour faciliter la connexion et la synchronisation des données avec d’autres applications Dynamics 365, [!INCLUDE[prod_short](includes/prod_short.md)] s’intègre également avec [!INCLUDE[prod_short](includes/cds_long_md.md)]. Par exemple, vous pouvez vous connecter à [!INCLUDE[crm_md](includes/crm_md.md)], ou même des applications que vous générez vous-même. S’il s’agit de votre toute première intégration, vous devez l’effectuer au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Pour en savoir plus, consultez [Intégration à Dataverse](admin-common-data-service.md).

Si vous avez déjà intégré [!INCLUDE[crm_md](includes/crm_md.md)] à [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez continuer à synchroniser les données à l’aide de votre configuration. Cependant, si vous mettez à niveau ou désactivez votre intégration [!INCLUDE[crm_md](includes/crm_md.md)], vous devez vous connecter au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)] pour la réactiver. Pour en savoir plus, consultez [Mise à niveau d’une intégration à Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> La reconnexion au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)] applique les paramètres de synchronisation par défaut et remplace toute configuration dont vous disposez. Par exemple, les mappages de table par défaut sont appliqués.

## Paramètres d’intégration dédiés à une intégration [!INCLUDE[crm_md](includes/crm_md.md)]
L’intégration à [!INCLUDE[prod_short](includes/prod_short.md)] se produit au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)], et de nombreux paramètres et tables standard sont fournis. Outre les paramètres standard, certains sont dédiés à [!INCLUDE[crm_md](includes/crm_md.md)]. Les sections suivantes répertorient ces paramètres.

## Autorisations et rôles de sécurité pour les comptes d’utilisateur dans Sales
Lorsque vous installez la solution d’intégration, les autorisations pour le compte d’utilisateur d’intégration sont configurées. Si ces autorisations sont modifiées, vous devrez peut-être les réinitialiser. Vous pouvez le faire en réinstallant la solution d’intégration en choisissant **Redéployer la solution d’intégration** sur la page **Paramètres de la connexion Dynamics 365**. Les rôles de sécurité suivants sont déployés :

* Administrateur d’intégration Dynamics 365 Business Central
* Utilisateur d’intégration Dynamics 365 Business Central
* Utilisateur de disponibilité produit Dynamics 365 Business Central

### Paramètres de connexion dans le guide de configuration
Vous pouvez utiliser un guide de configuration assistée pour configurer rapidement la connexion et spécifier des fonctions avancées, comme le couplage entre les enregistrements.

1. Choisissez **Configuration et extensions**, puis **Configuration assistée**.
2. Sélectionnez **Configurer la connexion Dynamics 365 Sales** pour lancer le guide de configuration assistée.
3. Renseignez les champs selon vos besoins.
4. En option, il existe des paramètres avancés qui peuvent améliorer la sécurité et activer davantage de fonctionnalités. Le tableau suivant décrit les paramètres avancés.  

| Champ | Désignation |
|--|--|
| **Importer une solution Dynamics 365 Sales** | Installez cette fonctionnalité pour installer et configurer la solution d’intégration dans [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
|**Synchroniser automatiquement la disponibilité article**|Spécifie que la file d’attente des travaux de disponibilité de l’article doit être planifiée. La file d’attente des travaux s’exécute toutes les 30 minutes et met à jour la disponibilité des éléments couplés.|
| **Activer l’intégration de la commande vente** | Quand les utilisateurs créent des commandes vente dans [!INCLUDE[crm_md](includes/crm_md.md)] et exécutent les commandes dans [!INCLUDE[prod_short](includes/prod_short.md)], ce paramètre intègre le processus dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d’informations, voir [Activer l’intégration du traitement des commandes client](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Vous devez fournir des informations d’identification pour un compte d’utilisateur de l’administrateur dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d’informations, reportez-vous à la rubrique [Gestion des données de commandes vente spéciales](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
|**Activer la connexion à Dynamics 365 Sales** | Activez la connexion vers [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Version du SDK Dynamics 365** | Cela est pertinent uniquement si vous l’intégrez à une version locale de [!INCLUDE[crm_md](includes/crm_md.md)]. Il s’agit du kit de développement logiciel Dynamics 365 (SDK) (également appelé Xrm) que vous utilisez pour connecter [!INCLUDE[prod_short](includes/prod_short.md)] à [!INCLUDE[crm_md](includes/crm_md.md)]. La version doit être compatible à la version du SDK utilisée par [!INCLUDE[crm_md](includes/crm_md.md)], et identique ou plus récente que la version utilisée par [!INCLUDE[crm_md](includes/crm_md.md)]. |

### Paramètres de connexion sur la page Paramètres de la connexion Microsoft Dynamics 365

Saisissez les informations suivantes pour la connexion de [!INCLUDE[prod_short](includes/prod_short.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)].

| Champ | Désignation |
|--|--|
|**URL Dynamics 365 Sales**|L’URL de votre instance de [!INCLUDE[crm_md](includes/crm_md.md)]. Ce paramètre permet aux utilisateurs d’ouvrir les enregistrements dans [!INCLUDE[prod_short](includes/prod_short.md)] qui correspondent aux enregistrements dans [!INCLUDE[crm_md](includes/crm_md.md)]. Par exemple, un compte ou un produit. Les enregistrements [!INCLUDE[prod_short](includes/prod_short.md)] s’ouvrent dans [!INCLUDE[prod_short](includes/prod_short.md)].|
|**Synchroniser automatiquement la disponibilité article**|Spécifie que la file d’attente des travaux de disponibilité de l’article doit être planifiée. La file d’attente des travaux s’exécute toutes les 30 minutes et met à jour la disponibilité des éléments couplés.|
|**Version du SDK Dynamics 365**|Si vous procédez à l’intégration avec une version locale de [!INCLUDE[crm_md](includes/crm_md.md)], utilisez le kit de développement logiciel (SDK) Dynamics 365 (également appelé Xrm) pour connecter [!INCLUDE[prod_short](includes/prod_short.md)] à [!INCLUDE[crm_md](includes/crm_md.md)]. La version que vous sélectionnez doit être compatible avec la version du SDK utilisée par [!INCLUDE[crm_md](includes/crm_md.md)]. Cette version est égale ou plus récente que la version utilisée par [!INCLUDE[crm_md](includes/crm_md.md)].|

Outre les paramètres ci-dessus, saisissez les paramètres suivants pour [!INCLUDE[crm_md](includes/crm_md.md)].

| Champ | Description |
|--|--|
| **L’intégration des commandes vente est activée** | Laissez les utilisateurs envoyer les commandes vente et les devis activés dans [!INCLUDE[crm_md](includes/crm_md.md)], et les visualiser et les traiter dans [!INCLUDE[prod_short](includes/prod_short.md)]. Ce paramètre intègre le processus dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d’informations, voir [Activer l’intégration du traitement des commandes client](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Créer automatiquement des commandes vente** | Permet de créer une commande vente dans [!INCLUDE[prod_short](includes/prod_short.md)] lorsqu’un utilisateur en crée et en envoie une dans [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Traiter automatiquement les devis** | Permet de traiter un devis dans [!INCLUDE[prod_short](includes/prod_short.md)] lorsqu’un utilisateur en crée et en active un dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d’informations, reportez-vous à la rubrique [Gestion des données de devis spéciales](/dynamics365/business-central/marketing-integrate-dynamicscrm?tabs=new-experience#handling-sales-quotes-data). |
|**Synchronisation bidirectionnelle des commandes vente**|Synchronisez les commandes client dans les deux sens. Par exemple, si un client change d’avis sur le produit ou la quantité qu’il a commandé dans [!INCLUDE[crm_md](includes/crm_md.md)], vous pouvez archiver le document de vente et en créer un autre dans [!INCLUDE[prod_short](includes/prod_short.md)]. Il en est de même pour les modifications dans [!INCLUDE[prod_short](includes/prod_short.md)]. Par exemple, lorsque les prix, les montants de taxe ou les dates d’expédition prévues changent, les modifications sont automatiquement synchronisées dans [!INCLUDE[crm_md](includes/crm_md.md)]. La synchronisation bilatérale permet de tenir vos vendeurs informés des dernières modifications et du statut des devis et des commandes.|

<!--
### User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### Mappage d’entité Sales standard pour la synchronisation

Les entités dans [!INCLUDE[crm_md](includes/crm_md.md)], telles que des commandes, sont intégrées aux types de tables équivalents dans [!INCLUDE[prod_short](includes/prod_short.md)], tels que des commandes vente. Pour utiliser les données [!INCLUDE[crm_md](includes/crm_md.md)], vous configurez des liens, appelés couplages entre les tables dans [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[crm_md](includes/crm_md.md)].

Le tableau suivant répertorie le mappage standard entre les tables dans [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] que [!INCLUDE[prod_short](includes/prod_short.md)] fournit.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Direction de synchronisation | Filtre par défaut |
|--|--|--|--|
| Unité | Groupe d’unités | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Article ; | Produit | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtre contact Sales : le **Type de produit** est **Stock de vente** |
| Ressource | Produit | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtre contact Sales : le **Type de produit** est **Services** |
| Unité article | UdM CRM |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
| Unité ressource | UdM CRM |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]||
| Groupe d’unités | CRM Uomschedule | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ||
| Groupe prix client | Liste des prix | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Prix vente | Tarifs produit | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | Filtre contact [!INCLUDE[prod_short](includes/prod_short.md)] : le champ **Code de vente** n’est pas vide, le champ **Type de vente** est défini sur **Groupe prix client** |
| Opportunité | Opportunité | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| En-tête facture vente | Facturer | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Ligne facture vente | Produit facture | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| En-tête de commande vente | Commande vente | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] <br><br> Pour synchroniser dans les deux sens, vous devez activer le bouton bascule **Synchronisation bidirectionnelle des commandes vente** sur la page **Paramètres de la connexion Dynamics 365**.| Filtre en-tête de vente [!INCLUDE[prod_short](includes/prod_short.md)] : le champ **Type de document** est défini sur Commande, le champ **Statut** est défini sur Lancé. |
| Remarques Commande vente | Remarques Commande vente | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

> [!NOTE]
> Les mappages des tables Unité article, Unité ressource et Groupe d’unités ne sont disponibles que si l’administrateur a activé le commutateur de fonctionnalité **Mise à jour des fonctionnalités : synchronisation de plusieurs unités avec Dynamics 365 Sales** sur la page **Gestion des fonctionnalités**. Pour plus d’informations, consultez [Synchronisation des articles et des ressources avec des produits dans différentes unités](admin-prepare-dynamics-365-for-sales-for-integration.md#synchronizing-items-and-resources-with-products-with-different-units-of-measure).

## Synchronisation des articles et des ressources avec des produits dans différentes unités
Les entreprises produisent ou achètent souvent les articles dans une unité, puis les vendent dans une autre. Pour synchroniser des articles qui utilisent plusieurs unités, vous devez activer le commutateur de fonctionnalité **Mise à jour des fonctionnalités : synchronisation de plusieurs unités avec Dynamics 365 Sales** sur la page **Gestion des fonctionnalités**. 

Quand vous activez la fonctionnalité, une table Groupe d’unités est créée et affectée à chaque article et ressource dans [!INCLUDE[prod_short](includes/prod_short.md)]. Les tables vous permettent de mapper les tables Groupe d’unités, Unité article et Unité ressource dans [!INCLUDE[prod_short](includes/prod_short.md)] au groupe d’unités de Dynamics 365 Sales dans [!INCLUDE[crm_md](includes/crm_md.md)]. L’image suivante montre les mappages.

:::image type="content" source="media/unit group 1.png" alt-text="Mappages de tables pour les groupes d’unités":::

Vous pouvez créer plusieurs unités pour chaque groupe d’unités et affecter les groupes aux produits dans [!INCLUDE[crm_md](includes/crm_md.md)]. Ensuite, vous pourrez synchroniser les produits avec des articles et des ressources dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous pouvez coupler manuellement des unités article ou des unités ressource à un groupe d’unités. Lorsque vous le faites, si le groupe d’unités article ou ressource n’est pas couplé à un groupe d’unités dans [!INCLUDE[crm_md](includes/crm_md.md)], par exemple, parce que le groupe de base n’existait pas, [!INCLUDE[prod_short](includes/prod_short.md)] créera automatiquement le groupe d’unités dans [!INCLUDE[crm_md](includes/crm_md.md)].

### Mappage d’articles et de ressources avec des produits
Lorsque vous activez le commutateur de fonctionnalité **Mise à jour des fonctionnalités : synchronisation de plusieurs unités avec Dynamics 365 Sales**, ce qui suit se produit :

* Des mappages sont créés pour les articles et les ressources.
* Les mappages existants sont supprimés. <!--which mappings?-->
* Une mise à niveau des données crée des groupes d’unités pour les articles et les ressources.

Pour utiliser les nouveaux mappages, vous devez synchroniser les groupes d’unités, l’unité article et l’unité ressource. Vous devez également resynchroniser les articles et les ressources. 

> [!NOTE]
> [!INCLUDE[crm_md](includes/crm_md.md)] ne vous permet pas de modifier un groupe d’unités pour un produit. Par conséquent, vous devez supprimer vos produits et découpler les articles et les ressources, puis synchroniser en créant des produits dans [!INCLUDE[crm_md](includes/crm_md.md)]. 

Les étapes suivantes décrivent les étapes de démarrage du mappage des groupes d’unités :

1. Assurez-vous que les produits de [!INCLUDE[crm_md](includes/crm_md.md)] ne sont pas associés à des articles ou des ressources dans [!INCLUDE[prod_short](includes/prod_short.md)]. S’ils le sont, accédez aux pages **Articles** et/ou **Ressources** et utilisez les options de filtrage pour sélectionner les enregistrements associés. Ensuite, choisissez l’action **Dynamics 365 Sales** et sélectionnez **Découpler**. Cette action planifie une tâche en arrière-plan pour découpler les enregistrements. Pendant que le travail est en cours d’exécution, vous pouvez vérifier son statut en utilisant l’action **Journal de synchronisation**. Pour plus d’informations, voir [Couplage et synchronisation](admin-how-to-couple-and-synchronize-records-manually.md). 
2. Du fait que des produits seront créés dans [!INCLUDE[crm_md](includes/crm_md.md)] avec de nouveaux groupes d’unités, pour éviter les noms en double, effectuez l’une des étapes suivantes :
    
    * Renommez vos produits, puis supprimez-les de [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d’informations, voir [Supprimer des produits (Centre des ventes)](/dynamics365/sales-enterprise/retire-product). Pour modifier en bloc vos produits dans Microsoft Excel, connectez-vous à Power Apps, choisissez votre environnement, rendez-vous sur la table **Produit** et choisissez l’onglet **Données**. Effacez tous les filtres appliqués. Dans le groupe **Données**, choisissez l’action **Modifier les données dans Excel**. Ajoutez un préfixe ou un suffixe aux produits couplés, puis supprimez-les.
    * Retirez vos produits et supprimez-les. 

3. Suivez ces étapes pour synchroniser **Groupes d’unités**, **Unité**, **Articles**, et **Ressources** :
    1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la page **Paramètres de la connexion Dynamics 365 Sales**.
    2. Utilisez l’action **Exécuter la synchronisation complète** pour ouvrir la page **Révision de synchr. complète Dataverse**.
    3. Pour les mappages **UDM ARTICLE**, **UDM RESSOURCE**, ET **GROUPE D’UNITÉS**, choisissez l’action **Recommander la synchronisation complète**.
    4. Sélectionnez l’action **Synchroniser tout**.

    > [!NOTE]
    > Pour les mappages qui n’ont pas encore été entièrement synchronisés, cette action les synchronisera entièrement. Pour empêcher ces mappages de se synchroniser, supprimez les mappages de la page. Cela les supprime uniquement de la synchronisation complète actuelle et ne supprime pas les mappages.
    
5. Choisir le mappage **ARTICLE-PRODUIT**, puis choisissez l’action **Redémarrage**. Le redémarrage crée des produits à partir des articles dans [!INCLUDE[crm_md](includes/crm_md.md)], et attribue un nouveau groupe d’unités spécifique à l’article.
6. Choisir le mappage **RESSOURCE-PRODUIT**, puis choisissez l’action **Redémarrage**. Le redémarrage crée des produits à partir des ressources dans [!INCLUDE[crm_md](includes/crm_md.md)], et attribue un nouveau groupe d’unités spécifique aux ressources.

### Règles de synchronisation

Le tableau suivant répertorie les règles qui contrôlent la synchronisation entre [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[prod_short](includes/prod_short.md)]. Ces règles s’ajoutent à celles définies pour Dataverse, qui s’appliquent également. Pour en savoir plus, consultez [Mappage d’entité standard](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

> [!NOTE]  
> Les modifications apportées aux données par le compte d’utilisateur d’intégration ne sont pas synchronisées. Par conséquent, nous vous avons recommandé de ne pas modifier les données lors de l’utilisation de ce compte. Pour en savoir plus, reportez-vous à la rubrique [Configuration des comptes d’utilisateur pour l’intégration à Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Table|Règle|
|-----|----|
|Unités de mesure|Les unités de mesure sont synchronisées avec les groupes d’unités dans [!INCLUDE[crm_md](includes/crm_md.md)]. Une seule unité de mesure peut être définie dans le groupe d’unités.|
|Articles|Lors de la synchronisation d’articles avec des produits [!INCLUDE[crm_md](includes/crm_md.md)], [!INCLUDE[prod_short](includes/prod_short.md)] crée automatiquement une liste de prix dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour éviter les erreurs de synchronisation, vous ne devez pas modifier cette liste de prix manuellement.|
|Ressources|Les ressources sont synchronisées avec les produits [!INCLUDE[crm_md](includes/crm_md.md)] dont le type de produit est Service.|
|Groupes prix client|Les groupes de prix client sont synchronisés avec les listes de prix dans Sales.|
|Prix de vente|Les prix de vente dont le type vente est Groupe prix client et dont le code vente est défini sont synchronisés avec les lignes de liste de prix dans [!INCLUDE[crm_md](includes/crm_md.md)].|
|Opportunités|Les opportunités sont synchronisées avec les opportunités dans [!INCLUDE[crm_md](includes/crm_md.md)]. La valeur Code vendeur définit le propriétaire de la table couplée dans [!INCLUDE[crm_md](includes/crm_md.md)].|
|Factures vente enregistrées|Les factures vente validées sont synchronisées avec les factures vente. Pour qu’une facture puisse être synchronisée, il est préférable de synchroniser toutes les autres tables pouvant participer à la facture, depuis les vendeurs aux listes de prix. La valeur Code vendeur de l’en-tête de facture définit le propriétaire de la table couplée dans Sales.|
|Commandes vente|Lorsque l’intégration des commandes vente est activée, les commandes vente dans [!INCLUDE[prod_short](includes/prod_short.md)] qui sont créées à partir des commandes vente soumises dans [!INCLUDE[crm_md](includes/crm_md.md)] sont synchronisées avec les commandes vente dans [!INCLUDE[crm_md](includes/crm_md.md)] quand elles sont validées. Avant de synchroniser les commandes, nous vous recommandons de synchroniser tout d’abord toutes les tables associées à la commande, telles que les commerciaux et les listes de prix. Le champ Code vendeur de l’en-tête de commande définit le propriétaire de la table couplée dans [!INCLUDE[crm_md](includes/crm_md.md)].|

### Projets de synchronisation pour une intégration de Sales

Les projets sont exécutés dans l’ordre suivant pour éviter les dépendances de couplage entre les tables. Il s’agit d’autres projets disponibles à partir de Dataverse. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](./admin-job-queues-schedule-tasks.md).

1. Projet de synchronisation Dynamics 365 Sales - UNITÉDEMESURE  
2. Projet de synchronisation Dynamics 365 Sales - RESSOURCE-PRODUIT  
3. Projet de synchronisation Dynamics 365 Sales - ARTICLE-PRODUIT  
4. Projet de synchronisation Dynamics 365 Sales - GRPPRXCLI-PRIX.
5. Projet de synchronisation Dynamics 365 Sales - PRXVENTE-PRXPROD.
6. Projet de synchronisation Dynamics 365 Sales - FACTVENTEVALIDÉES-FACT.

### Écritures de file projets de synchronisation par défaut

Le tableau suivant décrit les projets de synchronisation par défaut pour Sales.  

|Écriture file d’attente des travaux|Description|Sens|Mappage de table d’intégration|Fréquence de synchronisation par défaut (minutes)|Temps de veille pour inactivité par défaut (minutes)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|Projet de synchronisation Dynamics 365 Sales - UNITÉDEMESURE|Permet de synchroniser les groupes d’unités [!INCLUDE[crm_md](includes/crm_md.md)] avec les unités de mesure [!INCLUDE[prod_short](includes/prod_short.md)].|De [!INCLUDE[prod_short](includes/prod_short.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|UNITÉ|30|720<br> (12 heures)|
|Projet de synchronisation Dynamics 365 Sales - RESSOURCE-PRODUIT|Permet de synchroniser les produits [!INCLUDE[crm_md](includes/crm_md.md)] avec les ressources [!INCLUDE[prod_short](includes/prod_short.md)].|De [!INCLUDE[prod_short](includes/prod_short.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE-PRODUIT|30|720<br> (12 heures)|
|Projet de synchronisation Dynamics 365 Sales - ARTICLE - PRODUIT|Permet de synchroniser les produits [!INCLUDE[crm_md](includes/crm_md.md)] avec les articles [!INCLUDE[prod_short](includes/prod_short.md)].|De [!INCLUDE[prod_short](includes/prod_short.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|ARTICLE-PRODUIT|30|1440<br> (24 heures)|
|Projet de synchronisation Dynamics 365 Sales - GRPPRXCLI-PRIX|Permet de synchroniser les listes de prix de vente [!INCLUDE[crm_md](includes/crm_md.md)] avec les groupes de prix client [!INCLUDE[prod_short](includes/prod_short.md)].| |GROUPES DE PRIX CLIENT - LISTES DE PRIX DE VENTE|30|1440<br> (24 heures)|
|Projet de synchronisation Dynamics 365 Sales - PRXVENTE-PRXPRODUIT|Permet de synchroniser les prix de produit [!INCLUDE[crm_md](includes/crm_md.md)] avec les prix de vente [!INCLUDE[prod_short](includes/prod_short.md)].||PRIX DE PRODUIT - PRIX DE VENTE|30|1440<br> (24 heures)|
|Projet de synchronisation Dynamics 365 Sales - FACTVENTEVALIDEES-FACT|Permet de synchroniser les factures [!INCLUDE[crm_md](includes/crm_md.md)] avec les factures vente [!INCLUDE[prod_short](includes/prod_short.md)] validées.|De [!INCLUDE[prod_short](includes/prod_short.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|FACTURES - FACTURES VENTE VALIDÉES|30|1440<br> (24 heures)|
|Synchronisation Statistiques client - Dynamics 365 Sales|Permet de mettre à jour les comptes [!INCLUDE[crm_md](includes/crm_md.md)] avec les données client [!INCLUDE[prod_short](includes/prod_short.md)] les plus récentes. Dans [!INCLUDE[crm_md](includes/crm_md.md)], ces informations s’affichent dans le formulaire de vue rapide **Statistiques de compte Business Central** des comptes couplés avec les clients [!INCLUDE[prod_short](includes/prod_short.md)].<br /><br /> Ces données peuvent être également mises à jour manuellement depuis chaque enregistrement du client. Pour en savoir plus, reportez-vous à la rubrique [Coupler et synchroniser manuellement les enregistrements](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Remarque :** cette file d’attente de projets est pertinente uniquement si la solution d’intégration [!INCLUDE[prod_short](includes/prod_short.md)] est installée dans [!INCLUDE[crm_md](includes/crm_md.md)]. |Non applicable|Non applicable|30|Non applicable| 

## Connexion aux versions locales de la 1ère vague de lancement de Business Central 2019 et Microsoft Dynamics NAV 2018
L’équipe Microsoft Power Platform a [annoncé](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse) qu’elle définit comme obsolète le type d’authentification Office365. Si vous utilisez une version de [!INCLUDE[prod_short](includes/prod_short.md)] en locale antérieure à la 1ère vague de lancement 2019 de Business Central, vous devez utiliser le type d’authentification OAuth pour vous connecter à [!INCLUDE[crm_md](includes/crm_md.md)] en ligne. Les étapes de cette section décrivent comment établir la connexion aux versions de produit suivantes :

* 1ère vague de lancement 2019 de Business Central
* Microsoft Dynamics NAV 2018

### Conditions préalables

- Vous devez avoir un abonnement Microsoft Azure. Un compte d’évaluation fonctionnera pour l’enregistrement de l’application.
- [!INCLUDE[crm_md](includes/crm_md.md)] est configuré pour utiliser l’un des types d’authentification suivants :

   - Office365 (hérité)

     > [!IMPORTANT]
     > À compter d′avril 2022, Office365 (hérité) ne sera plus pris en charge. Pour plus d′informations, consultez [Modifications importantes (déconseillées) à venir dans Power Apps, Power Automate et les applications d′engagement client](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   - OAuth

### Pour connecter la 1ère vague de lancement 2019 Business Central et Dynamics NAV 2018

1. Importez la solution d’intégration Microsoft Dynamics 365 Business Central dans votre environnement [!INCLUDE[crm_md](includes/crm_md.md)]. La solution d’intégration est disponible dans le dossier CrmCustomization de votre DVD d’installation [!INCLUDE[prod_short](includes/prod_short.md)] ou Dynamics NAV 2018. Selon la version de votre produit, importez l’une des solutions suivantes :

   * Pour [!INCLUDE[prod_short](includes/prod_short.md)], le dossier contient les solutions DynamicsNAVIntegrationSolution_v9 et DynamicsNAVIntegrationSolution_v91. . La solution à importer dépend de la version de [!INCLUDE[crm_md](includes/crm_md.md)] à laquelle vous êtes connecté. [!INCLUDE[crm_md](includes/crm_md.md)] en ligne nécessite la solution d’intégration DynamicsNAVIntegrationSolution_v91.
   * Pour Dynamics NAV 2018, installez la solution DynamicsNAVIntegrationSolution.

2. Créez un utilisateur d’intégration non interactif dans votre environnement [!INCLUDE[crm_md](includes/crm_md.md)] et attribuez à l’utilisateur les rôles de sécurité suivants. Pour en savoir plus, reportez-vous à la rubrique [Créer un compte d’utilisateur non interactif](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Administrateur d’intégration Dynamics 365 Business Central
   * Utilisateur d’intégration Dynamics 365 Business Central

   > [!Important]
   > Cet utilisateur ne doit pas avoir le rôle de sécurité Administrateur système. De plus, vous ne pouvez pas utiliser le compte d’administrateur système en tant qu’utilisateur d’intégration.

3.  Dans le portail Azure, créez une inscription d’application pour [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, consultez [Enregistrer une application dans Microsoft Entra ID](/powerapps/developer/data-platform/walkthrough-register-app-azure-active-directory). 
  
   > [!NOTE]
   > Nous vous recommandons d’enregistrer l’application dans le même locataire que votre environnement Dataverse afin que vous n’ayez pas à consentir à ce que l’application accède à l’environnement. Si vous enregistrez l’application dans un autre environnement, vous devez vous connecter à Microsoft Entra ID en utilisant le compte administrateur de votre environnement Dataverse et donner votre consentement.
   >
   > De plus, l’application que vous enregistrez ne doit pas avoir de secret. Connecter une application avec un secret à Dataverse est disponible uniquement dans la 1ère vague de lancement 2020 de Business Central et versions ultérieures.
  
4. Selon la version de votre produit, faites l’une des étapes suivantes :

    * Dans [!INCLUDE[prod_short](includes/prod_short.md)], rechercher **Configuration de la connexion Microsoft Dynamics 365**, puis choisissez le lien associé. 
    * Dans Dynamics NAV 2018, recherchez **Configuration de la connexion Microsoft Dynamics 365 for Sales**, puis choisissez le lien associé.

5. Dans le champ **Type d’authentification**, choisissez l’option pour OAuth. 
6. Choisissez la version du SDK CRM qui correspond à la version de la solution que vous avez importée à l’étape 1.

   > [!NOTE]
   > Cette étape n’est pertinente que pour [!INCLUDE[prod_short](includes/prod_short.md)].

7. Saisissez l’URL de votre environnement [!INCLUDE[crm_md](includes/crm_md.md)], puis entrez le nom d’utilisateur et le mot de passe de l’utilisateur d’intégration. 

   * Dans [!INCLUDE[prod_short](includes/prod_short.md)], utilisez le champ **Adresse du serveur**.
   * Dans Dynamics NAV 2018, utilisez le champ **URL Dynamics 365 Sales**.

8. Dans le champ **Chaîne de connexion**, spécifiez l’ID de l’enregistrement de l’application. Ce champ a deux jetons dans lesquels l’ID de votre application doit être spécifié.

   |Jeton           |Description  |
   |----------------|-------------|
   |**AppId**       |Définissez l’ID de l’application.      |
   |**RedirectUri** |Définissez l’ID de l’application, mais ajoutez le préfixe **app://**.         |

    **Exemple** L’exemple suivant montre une chaîne de connexion.

    ```
    AuthType=OAuth;Username=jsmith@contoso.onmicrosoft.com;Password=****;Url=https://contosotest.crm.dynamics.com;AppId=<your AppId>;RedirectUri=app://<your AppId>;TokenCacheStorePath=;LoginPrompt=Auto
    ```
9. Activez la connexion.

> [!Note]
> Si vous souhaitez configurer une connexion à une instance [!INCLUDE[crm_md](includes/crm_md.md)] avec un type d’authentification spécifique, renseignez les champs du raccourci **Détails du type d’authentification**. Pour plus d’informations, consultez [Authentification avec les services web Microsoft Dataverse](/powerapps/developer/data-platform/authentication). Cette étape n’est pas requise lors de la connexion d’une version en ligne de [!INCLUDE[prod_short](includes/prod_short.md)].

## Voir aussi

[Configuration des comptes d’utilisateur pour intégration à [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Configurer une connexion vers [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Synchronisation de Business Central et de [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Préparation de l’intégration à Dynamics 365 Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]
