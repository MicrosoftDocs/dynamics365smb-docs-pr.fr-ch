---
title: Utilisation de Microsoft Dataverse
description: "Introduction à l’intégration et à l’utilisation de Microsoft Dataverse et ses composants pour se connecter à d’autres applications Dynamics\_365."
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.date: 06/14/2021
---

# Intégration à Microsoft Dataverse

Les applications métier utilisent souvent des données provenant de plusieurs sources. [!INCLUDE[prod_short](includes/cds_long_md.md)] combine les données en un seul ensemble de logique qui facilite la connexion d’autres applications Dynamics 365 telles que [!INCLUDE[crm_md](includes/crm_md.md)] ou votre propre application créée sur [!INCLUDE[prod_short](includes/cds_long_md.md)] à [!INCLUDE[prod_short_md](includes/prod_short.md)]. Pour en savoir plus sur [!INCLUDE[prod_short](includes/cds_long_md.md)], consultez [Qu’est-ce que Dataverse ?](/powerapps/maker/common-data-service/data-platform-intro)

Les étapes suivantes offrent un aperçu des étapes pour intégrer [!INCLUDE[prod_short](includes/cds_long_md.md)] à [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Ces tâches exigent le rôle de sécurité **Administrateur système** dans [!INCLUDE[prod_short](includes/cds_long_md.md)] et [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Affectez les licences pour [!INCLUDE[prod_short](includes/cds_long_md.md)] aux utilisateurs [!INCLUDE[prod_short](includes/prod_short.md)] qui utiliseront les applications intégrées.

2. Configurez une connexion vers [!INCLUDE[prod_short](includes/cds_long_md.md)]. Pour en savoir plus, consultez [Se connecter à Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synchronisez les données entre les applications. Pour plus d’informations, voir la rubrique [Synchronisation de Business Central et de Dataverse](admin-synchronizing-business-central-and-sales.md). 

## Mise en route de [!INCLUDE[prod_short](includes/cds_long_md.md)]

Pour prendre en main [!INCLUDE[prod_short](includes/cds_long_md.md)], vous avez besoin d’un compte Microsoft Power Apps. Si vous ne disposez pas encore d’un compte Power Apps, vous pouvez en obtenir un gratuitement en visitant [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) et en cliquant sur le lien **Démarrer gratuitement**. Pour en savoir plus sur la prise en main de [!INCLUDE[prod_short](includes/cds_long_md.md)], consultez le module [Mise en route avec le module Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) de la formation Microsoft.

## Synchronisation des données bidirectionnelle ou unidirectionnelle

Selon les besoins de votre activité, vous pouvez configurer l’intégration pour synchroniser les données vers ou depuis une application métier Dynamics 365 vers une autre, ou dans les deux directions en quasi temps réel au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Par exemple, si vous intégrez [!INCLUDE[prod_short](includes/prod_short.md)] à [!INCLUDE[crm_md](includes/crm_md.md)] au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)], un vendeur peut créer une commande vente dans [!INCLUDE[crm_md](includes/crm_md.md)] et la commande est synchronisée avec [!INCLUDE[prod_short](includes/prod_short.md)]. Inversement, à partir de [!INCLUDE[crm_md](includes/crm_md.md)], le vendeur peut consulter les informations de [!INCLUDE[prod_short](includes/prod_short.md)] sur la disponibilité de l’article sur la commande. 

## Entités standard et personnalisées

[!INCLUDE[prod_short](includes/cds_long_md.md)] stocke en toute sécurité les données dans un ensemble de tables, qui sont des ensembles d’enregistrements similaires à la façon dont une table stocke des données dans une base de données. [!INCLUDE[prod_short](includes/cds_long_md.md)] comprend un ensemble de base de tables standard qui couvrent des scénarios typiques, mais vous pouvez également créer des tables personnalisées dédiées à votre organisation. Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez afficher les tables standard et personnalisées en cours de synchronisation sur la page Mappages de table d’intégration.

## À propos de la solution d’intégration de base Business Central

La solution d’intégration de base est un élément clé de l’intégration. La solution ajoute les rôles et niveaux d’accès requis aux comptes d’utilisateur pour l’intégration et crée les tables nécessaires au mappage de la société [!INCLUDE[prod_short](includes/prod_short.md)] au centre de profit dans [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Par défaut, le guide de configuration assistée **Configurer la connexion [!INCLUDE[prod_short](includes/cds_long_md.md)]** importera la solution. Pour ce faire, le guide de configuration utilise un compte d’utilisateur d’administrateur que vous indiquez. Ce compte doit être un utilisateur valide dans [!INCLUDE[prod_short](includes/cds_long_md.md)] avec le rôle de sécurité suivant :

* Administrateur système  

Pour en savoir plus, consultez [Configuration des comptes d’utilisateur pour l’intégration à [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) et [Créer des utilisateurs dans Microsoft Dynamics 365 (online) et attribuer les rôles de sécurité](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Le compte d’administrateur n’est utilisé qu’une seule fois lors de la configuration en raison de modifications de paramètres apportées par la solution d’intégration de base dans [!INCLUDE[prod_short](includes/cds_long_md.md)]. Une fois la solution importée, le compte n’est plus nécessaire. L’intégration continue à utiliser le compte d’utilisateur qui est automatiquement créé spécialement pour l’intégration.

Outre la personnalisation de [!INCLUDE[prod_short](includes/cds_long_md.md)], la solution crée également les rôles suivants dans [!INCLUDE[prod_short](includes/cds_long_md.md)] pour l’intégration :

* **Administrateur d’intégration** : permet aux utilisateurs de gérer la connexion entre [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[prod_short](includes/cds_long_md.md)]. En général, cela est attribué uniquement au compte d’utilisateur automatiquement créé pour la synchronisation.  
* **Utilisateur d’intégration** : permet aux utilisateurs d’accéder aux données synchronisées. En général, cela est attribué au compte d’utilisateur automatiquement créé pour la synchronisation et aux autres utilisateurs devant consulter les données synchronisées ou y accéder.

Pour plus de détails sur chaque rôle, tels que les autorisations et les niveaux d’accès, voir [Configuration de comptes d’utilisateurs pour l’intégration avec [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Lors de la configuration de la connexion, les mappages de table d’intégration nécessaires à la synchronisation des données sont créés. Les entités dans [!INCLUDE[prod_short](includes/cds_long_md.md)] sont mappées à des tables et des champs de table dans Business Central au moyen de tables d’intégration. Pour en savoir plus, consultez [Mappage d’entité standard pour la synchronisation](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## Voir la [formation Microsoft](/training/modules/use-model-driven-apps-common-data-service/) associée

## Voir aussi

[Modèles de propriété de données](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
