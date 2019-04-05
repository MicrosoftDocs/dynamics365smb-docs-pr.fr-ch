---
title: Gérer les clients utilisant Dynamics 365 for Sales | Microsoft Docs
description: Vous pouvez utiliser Dynamics 365 for Sales depuis Business Central pour mapper les données et avoir une intégration et une synchronisation parfaites dans le processus allant du prospect à l'encaissement.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 01/24/2019
ms.author: edupont
ms.openlocfilehash: bba9fb9a83856cea43e4f4215e7c148b713252a9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821586"
---
# <a name="integrating-with-dynamics-365-for-sales"></a>Intégration à Dynamics 365 for Sales
Si vous utilisez Dynamics 365 for Sales for Customer Engagement, vous pouvez utiliser [!INCLUDE[d365fin](includes/d365fin_md.md)] pour le traitement des commandes et les finances et avoir une intégration transparente dans le processus allant du prospect à l'encaissement.

> [!NOTE]
> Cette rubrique considère que [!INCLUDE[d365fin](includes/d365fin_md.md)] et la solution Sales intégrée sont déployés dans un environnement SaaS. Il est possible de mélanger la version online et l aversion on-premises, mais cela nécessite une configuration spéciale. Pour plus d'informations, voir [Préparation de l'intégration à Dynamics 365 for Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Lorsque votre application est configurée pour s'intégrer à Sales, vous avez accès aux données Sales à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)] et inversement dans certains cas. L'intégration vous permet d'utiliser et de synchroniser les types de données communs aux deux services, par exemple clients, contacts et informations de vente, et mettre à jour les données dans les deux emplacements.  

Par exemple, les commerciaux dans Sales peuvent utiliser les tarifs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] lorsqu'ils créent une commande vente. Lorsque ils ajoutent l'article à la ligne commande vente dans Sales, ils peuvent également visualiser le niveau de stock (disponibilité) de l'article dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Inversement, les préparateurs de commandes dans [!INCLUDE[d365fin](includes/d365fin_md.md)] peuvent gérer les caractéristiques spéciales des commandes vente transférées automatiquement ou manuellement à partir de Sales, comme créer et valider automatiquement les lignes commande vente valides pour les articles ou les ressources qui ont été entrés dans Sales en tant que produits hors catalogue. Pour plus d'informations, voir la section « Gestion des données de commandes vente spéciales ».

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] s'intègre uniquement à Dynamics 365 for Sales. Les autres applications ou solutions dans Dynamics 365 qui modifient le flux de travail ou le modèle de données standard dans Sales, par exemple Project Service Automation, peuvent désactiver l'intégration entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et Sales.

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Mappage d'entité Sales standard pour la synchronisation
Les entités Sales, telles que les comptes, sont intégrées aux types d'enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] équivalents, tels que les clients. Pour utiliser les données Sales, vous définissez des mappages, appelés couplages, entre les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] et les enregistrements d'entité Sales. Par exemple, vou définissez un couplage entre un client spécifique dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et un compte correspondant dans Sales.

Le tableau suivant répertorie les types d'enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] (tables) et les entités Sales correspondantes qui peuvent être synchronisées.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|Ventes|Direction de synchronisation|Filtre par défaut|
|-------------------------------------------|-----|-------------------------|--------------|
|Vendeur/Acheteur|Utilisateur|Sales -> Business Central|Filtre contact Sales : le **Statut** est **Non**, l'**Utilisateur sous licence** est **Oui**, le Mode utilisateur de l'intégration est **Non**|
|Client|Compte|Business Central - > Sales et Sales - > Business Central|Filtre compte Sales : le **Type de relation** est **Client** et le **Statut** est **Actif**.|
|Contact|Contact|Business Central - > Sales et Sales - > Business Central|Filtre contact Business Central : le **Type** est **Personne** et le contact est affecté à une société. Filtre contact Sales : le contact est affecté à une société et le type de client parent est **Compte**.|
|Devise|Devise de transaction|Business Central -> Sales| |
|Unité|Groupe d'unités|Business Central -> Sales| |
|Article|Produit|Business Central - > Sales et Sales - > Business Central|Filtre contact Sales : le **Type de produit** est **Stock de vente**|
|Ressource|Produit|Business Central - > Sales et Sales - > Business Central|Filtre contact Sales : le **Type de produit** est **Services**|
|Groupe prix client|Liste des prix|Business Central -> Sales| |
|Prix vente|Tarifs produit|Business Central -> Sales|Filtre contact Business Central : le **Code vente** n'est pas vide, le **Type vente** est **Groupe prix client**|
|Opportunité|Opportunité|Business Central - > Sales et Sales - > Business Central| |
|En-tête facture vente|Facturer|Business Central -> Sales| |
|Ligne facture vente|Produit facture|Business Central -> Sales| |

Les entités Sales et les tables [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisées sont définies par les écritures de mappage de table dans la table 5335, **Correspondance table intégration**. Vou pouvez afficher les mappages et définir les filtres à partir de la page 5335, **Correspondances table intégration**. Le mappage entre les champs des enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] et les champs des entités Sales est défini par les écritures de mappage de champ dans la table 5336, **Correspondance table intégration**, et avec la logique de mappage supplémentaire.

### <a name="field-mapping-for-the-sales-account-option"></a>Mappage de champ pour l'option Compte dans Sales
Trois tables dans [!INCLUDE[d365fin](includes/d365fin_md.md)] sont mappées aux champs d'option de l'entité **Compte**.   

Les enregistrements de la table qui ne sont pas liés aux options existant dans Sales sont ignorés pendant la synchronisation. Cela signifie que le champ **Option** est vide dans Sales.

Le tableau suivant décrit les mappages des tables Business Central pour le champ **Option** de l'entité **Compte**.

|Table|Champ Option de l'entité Compte dans Sales|
|----------------------|-------------------------------------------|
|Conditions de paiement|Conditions de paiement|
|Conditions de livraison|Adresse 1 : Conditions de transport|
|Transporteur|Adresse 1 : Mode de livraison|

### <a name="synchronization-rules"></a>Règles de synchronisation
Le tableau suivant décrit les règles qui contrôlent la synchronisation entre les tables Business Central et les entités Sales.

> [!NOTE]  
> Les modifications des données dans Sales qui sont exécutées par le compte de connexion Sales sont ignorées. Les modifications ne sont pas synchronisées. Il est donc recommandé de ne pas modifier les données à l'aide du compte de connexion Sales.

|Table|Règle|
|-----|----|
|Clients|Pour qu'un client puisse être synchronisé à un compte, le vendeur affecté au client doit être couplé à un utilisateur dans Sales. Ainsi, lorsque vous exécutez le projet de synchronisation CLIENTS - Dynamics 365 for Sales et que vous le configurez pour créer des enregistrements, assurez-vous de synchroniser les vendeurs avec les utilisateurs Sales avant de synchroniser les clients avec les comptes Sales. <br /> <br />Le projet de synchronisation Dynamics 365 for Sales - CLIENTS synchronise uniquement les comptes Sales dont le type de relation est Client.|
|Contacts|Seuls les contacts dans Sales qui sont associés à un compte sont créés dans Business Central. La valeur Code vendeur définit le propriétaire de l'entité couplée dans Sales.|
|Devises|Les devises sont couplées aux devises de transaction dans Sales conformément aux codes ISO. Seules les devises qui ont un code ISO standard seront couplées et synchronisées avec les devises de transaction.|
|Unités de mesure|Les unités de mesure sont synchronisées avec les groupes d'unités dans Sales. Une seule unité de mesure peut être définie dans le groupe d'unités.|
|Articles|Lors de la synchronisation d'articles avec des produits Sales, Business Central crée automatiquement une liste de prix dans Sales. Pour éviter les erreurs de synchronisation, vous ne devez pas modifier cette liste de prix manuellement.|
|Vendeurs|Les vendeurs sont couplés aux utilisateurs du système dans Sales. L'utilisateur doit être activé et sous licence et ne doit pas être l'utilisateur d'intégration. Notez qu'il s'agit de la première table qui doit être synchronisée, car elle est utilisée dans les clients, les contacts, les opportunités et les factures vente.|
|Ressources|Les ressources sont synchronisées avec les produits Sales dont le type de produit est Service.|
|Groupes prix client|Les groupes de prix client sont synchronisés avec les listes de prix dans Sales.|
|Prix de vente|Les prix de vente dont le type vente est Groupe prix client et dont le code vente est défini sont synchronisés avec les lignes de liste de prix dans Sales|
|Opportunités|Les opportunités sont synchronisées avec les opportunités dans Sales. La valeur Code vendeur définit le propriétaire de l'entité couplée dans Sales.|
|Factures vente enregistrées|Les factures vente validées sont synchronisées avec les factures vente. Pour qu'une facture puisse être synchronisée, il est préférable de synchroniser toutes les autres entités pouvant participer à la facture, depuis les vendeurs aux listes de prix. La valeur Code vendeur de l'en-tête de facture définit le propriétaire de l'entité couplée dans Sales.|

## <a name="setting-up-the-connection"></a>Configuration de la connexion
À partir de la page d'accueil, vous pouvez accéder au guide de configuration assistée **Paramètres de connexion Microsoft Dynamics 365** qui vous aide à configurer la connexion. Une fois cette opération effectuée, vous disposez d'un couplage facile des enregistrements Sales avec les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>   La section suivante explique la configuration assistée, mais vous pouvez effectuer les mêmes tâches manuellement sur la page **Paramètres de connexion Sales**.

Dans le guide de configuration assistée, vous pouvez choisir les données à synchroniser entre les deux services. Vous pouvez également spécifier que vous souhaitez importer votre solution Sales existante. Dans ce cas, vous devez indiquer les informations d'identification d'un compte utilisateur.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Configuration du compte utilisateur pour importer la solution
Pour importer une solution Sales existante, le guide d'installation utilise un compte administratif. Ce compte doit être un utilisateur valide dans Sales avec les rôles de sécurité suivants :

* Administrateur système  
* Personnalisateur de solution  

Pour plus d'informations, voir [Créer des utilisateurs dans Microsoft Dynamics 365 (online) et attribuer des rôles de sécurité](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) et [Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md).  

Ce compte est uniquement utilisé lors de la configuration. Une fois la solution importée dans [!INCLUDE[d365fin](includes/d365fin_md.md)], le compte n'est plus nécessaire.

### <a name="setting-up-the-user-account-for-synchronization"></a>Configuration du compte utilisateur pour la synchronisation
L'intégration est basée sur un compte utilisateur partagé. Ainsi dans votre abonnement Office 365, vous devez créer un utilisateur dédié utilisé pour la synchronisation entre les deux services. Ce compte doit déjà être un utilisateur valide dans Sales, mais vous n'avez pas à lui affecter de rôles de sécurité car le guide de configuration le fait pour vous. Vous devez spécifier ce compte utilisateur à une ou plusieurs reprises dans le guide de configuration, en fonction du nombre de synchronisation que vous souhaitez activer. Pour plus d'informations, voir [Créer des utilisateurs dans Microsoft Dynamics 365 (online) et attribuer des rôles de sécurité](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Si vous décidez d'activer la *disponibilité de l'article*, le compte utilisateur intégration doit disposer d'une clé d’accès rapide des services Web. Cette opération s'effectue en deux étapes dans la page [!INCLUDE[d365fin](includes/d365fin_md.md)] de ce compte utilisateur, vous devez cliquer sur le bouton **Modifier la clé de service web** et dans le guide de configuration de la connexion Sales, vous devez spécifier cet utilisateur en tant qu'utilisateur de service Web OData.

Si vous décidez d'activer l'*intégration des commandes vente*, vous devez spécifier un utilisateur qui peut gérer cette synchronisation - un utilisateur de l'intégration ou un compte utilisateur différent.

### <a name="coupling-records"></a>Enregistrements couplage
Dans le guide de configuration assistée, vous pouvez choisir la synchronisation entre les deux services. Mais ultérieurement, vous pouvez également configurer la synchronisation de types spécifiques de données. Cette action est appelée le *couplage*, et cette section fournit des recommandations pour les éléments dont vous devez tenir compte.

Par exemple, si vous souhaitez afficher les comptes Sales en tant que clients dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez coupler les deux types d'enregistrements. Ce n'est pas très compliqué, vous devez ouvrir la page **Liste des clients** dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et il existe une action dans le ruban pour coupler ces données avec Sales. Puis vous devez spécifier quels clients [!INCLUDE[d365fin](includes/d365fin_md.md)] correspondent à quels comptes dans Sales.

Dans certains domaines, la fonctionnalité vous demande de coupler certains ensembles de données avant d'autres ensembles de données comme illustré dans la liste suivante :

* Clients et comptes  
  * Coupler d'abord des vendeurs avec des utilisateurs Sales  
* Articles et ressources  
  * Coupler d'abord des unités de mesure avec des groupes d'unités Sales  
* Prix des articles et des ressources  
  * Coupler d'abord des groupes tarifs client avec des prix Sales  

> [!NOTE]  
>   Si vous utilisez des tarifs en devises étrangères, assurez-vous de coupler des devises avec des devises de transaction Sales.

Dans Sales, les commandes vente dépendent d'informations supplémentaires comme les clients, les unités de mesure, les devis, les groupes tarifs client, les articles et/ou les ressources. Pour assurer une intégration transparente avec les commandes vente, vous devez d'abord coupler des clients, des unités de mesure, des devises, des groupes tarifs client, des articles et/ou des ressources.

### <a name="synchronizing-records-fully"></a>Synchronisation complète des enregistrements
À la fin du guide de configuration assistée, vous pouvez sélectionner l'action **Exécuter une synchronisation complète** pour démarrer la synchronisation de tous les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] avec tous les enregistrements associés de la solution Sales connectée. Sur la page **Synchronisation complète CRM. Révision**, sélectionnez l'action **Démarrer**. La synchronisation commence à exécuter les projets en fonction des dépendances. Par exemple, les enregistrements de devise sont synchronisés avant les enregistrements client. La synchronisation complète peut durer longtemps et s'exécutera donc en arrière-plan afin que vous puissiez continuer à utiliser [!INCLUDE[d365fin](includes/d365fin_md.md)].

Pour vérifier la progression des projets individuels lors d'une synchronisation complète, accédez au champ **Statut écriture file d'attente des travaux**, **Statut projet Vers la table int.** ou **Statut projet À partir de la table int.** sur la page **Synchronisation complète CRM. Révision**.

Sur la page **Paramétrage de la connexion Microsoft Dynamics 365**, vous pouvez obtenir des détails sur la synchronisation complète à tout moment. À partir de cette page, vous pouvez aussi ouvrir la page **Correspondances table intégration** pour afficher les détails des tables dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et dans la solution Sales à synchroniser.

## <a name="handling-special-sales-order-data"></a>Gestion des données de commandes vente spéciales
Les commandes vente dans Sales seront transférées automatiquement à [!INCLUDE[d365fin](includes/d365fin_md.md)] si vous sélectionnez la case à cocher **Créer automatiquement des commandes vente** sur la page **Paramètres de la connexion Microsoft Dynamics 365**. Pour ces commandes vente, le champ **Nom** de la commande d'origine est transféré et associé au champ **Numéro de document externe** de la commande vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ceci peut également fonctionner si la commande vente d'origine indique les biens hors catalogue, c'est-à-dire les articles ou les ressources qui ne sont enregistrés dans aucun produit. Dans ce cas, vous devez renseigner les champs **Type produit hors catalogue** et **N° produit hors catalogue** sur la page **Paramètres ventes**, de sorte que ces ventes de produits non enregistrées soient mappées à un nombre donné d'articles/de ressources pour l'analyse financière.

Si la désignation de l'article sur la commande vente d'origine est très longue, alors une ligne commande vente supplémentaire de type Commentaire est créée pour stocker le texte intégral de la commande vente dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Voir aussi
[Préparation pour intégrer à Dynamics 365 for Sales On-premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)  
[Gestion des relations](marketing-relationship-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modification des fonctionnalités affichées](ui-experiences.md)  
[Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md)    
[Intégrer l'organisation et les utilisateurs dans Dynamics 365 (en ligne)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
