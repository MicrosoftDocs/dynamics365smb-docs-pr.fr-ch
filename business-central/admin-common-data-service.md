---
title: Utilisation de Common Data Service
description: Introduction à Common Data Service et ses composants.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.openlocfilehash: 85823e93b1d239bf4e59ec6a8872cdc4a2cef9c1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911595"
---
# <a name="integrating-with-common-data-service"></a>Intégration à Common Data Service

Les applications métier utilisent souvent des données provenant de plusieurs sources. [!INCLUDE[d365fin](includes/cds_long_md.md)] combine les données en un seul ensemble de logique qui facilite la connexion d’autres applications Dynamics 365 telles que [!INCLUDE[crm_md](includes/crm_md.md)] ou votre propre application créée sur [!INCLUDE[d365fin](includes/cds_long_md.md)] à [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Pour en savoir plus sur [!INCLUDE[d365fin](includes/cds_long_md.md)], consultez [Qu’est-ce que Common Data Service ?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

Les étapes suivantes offrent un aperçu des étapes pour intégrer [!INCLUDE[d365fin](includes/cds_long_md.md)] à [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Ces tâches exigent le rôle de sécurité **Administrateur système** dans [!INCLUDE[d365fin](includes/cds_long_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Affectez les licences pour [!INCLUDE[d365fin](includes/cds_long_md.md)] aux utilisateurs [!INCLUDE[d365fin](includes/d365fin_md.md)] qui utiliseront les applications intégrées.

2. Configurez une connexion vers [!INCLUDE[d365fin](includes/cds_long_md.md)]. Pour en savoir plus, consultez [Se connecter à Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synchronisez les données entre les applications. Pour plus d’informations, voir la rubrique [Synchronisation de Business Central et de Common Data Service](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-d365fin"></a>Mise en route de [!INCLUDE[d365fin](includes/cds_long_md.md)]
Pour prendre en main [!INCLUDE[d365fin](includes/cds_long_md.md)], vous avez besoin d’un compte Microsoft Power Apps. Si vous ne disposez pas encore d’un compte Power Apps, vous pouvez en obtenir un gratuitement en visitant [powerapps.com](https://web.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) et en cliquant sur le lien **Démarrer gratuitement** . Pour en savoir plus sur la prise en main de [!INCLUDE[d365fin](includes/cds_long_md.md)], consultez le module [Mise en route avec le module Common Data Service](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/) de Microsoft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Synchronisation des données bidirectionnelle ou unidirectionnelle
Selon les besoins de votre activité, vous pouvez configurer l’intégration pour synchroniser les données vers ou depuis une application métier Dynamics 365 vers une autre, ou dans les deux directions en quasi temps réel au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)]. Par exemple, si vous intégrez [!INCLUDE[d365fin](includes/d365fin_md.md)] à [!INCLUDE[crm_md](includes/crm_md.md)] au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)], un vendeur peut créer une commande vente dans [!INCLUDE[crm_md](includes/crm_md.md)] et la commande est synchronisée avec [!INCLUDE[d365fin](includes/d365fin_md.md)]. Inversement, à partir de [!INCLUDE[crm_md](includes/crm_md.md)], le vendeur peut consulter les informations de [!INCLUDE[d365fin](includes/d365fin_md.md)] sur la disponibilité de l’article sur la commande. 

## <a name="standard-and-custom-entities"></a>Entités standard et personnalisées
[!INCLUDE[d365fin](includes/cds_long_md.md)] stocke en toute sécurité les données dans un ensemble d’entités, qui sont des ensembles d’enregistrements similaires à la façon dont une table stocke des données dans une base de données. [!INCLUDE[d365fin](includes/cds_long_md.md)] comprend un ensemble de base d’entités standard qui couvrent des scénarios typiques, mais vous pouvez également créer des entités personnalisées dédiées à votre organisation. Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez afficher les entités standard et personnalisées en cours de synchronisation sur la page Mappages de table d’intégration.

## <a name="about-the-base-cds-integration-solution"></a>À propos de la solution d’intégration de base CDS

La solution d’intégration de base CDS est un élément clé de l’intégration. La solution ajoute les rôles et niveaux d’accès requis aux comptes d’utilisateur pour l’intégration et crée les entités nécessaires au mappage de la société [!INCLUDE[d365fin](includes/d365fin_md.md)] au centre de profit dans [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

Par défaut, le guide de configuration assistée **Configurer la connexion [!INCLUDE[d365fin](includes/cds_long_md.md)]** importera la solution. Pour ce faire, le guide de configuration utilise un compte d’utilisateur d’administrateur que vous indiquez. Ce compte doit être un utilisateur valide dans [!INCLUDE[d365fin](includes/cds_long_md.md)] avec le rôle de sécurité suivant :

* Administrateur système  

Pour en savoir plus, consultez [Configuration des comptes d’utilisateur pour l’intégration à [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) et [Créer des utilisateurs dans Microsoft Dynamics 365 (online) et attribuer les rôles de sécurité](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Le compte d’administrateur n’est utilisé qu’une seule fois lors de la configuration en raison de modifications de paramètres apportées par la solution de base CDS dans [!INCLUDE[d365fin](includes/cds_long_md.md)]. Une fois la solution importée, le compte n’est plus nécessaire. L’intégration continue à utiliser le compte d’utilisateur qui est automatiquement créé spécialement pour l’intégration.

Outre la personnalisation de [!INCLUDE[d365fin](includes/cds_long_md.md)], la solution crée également les rôles suivants dans [!INCLUDE[d365fin](includes/cds_long_md.md)] pour l’intégration :

* **Administrateur d’intégration**  : permet aux utilisateurs de gérer la connexion entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)]. En général, cela est attribué uniquement au compte d’utilisateur automatiquement créé pour la synchronisation.  
* **Utilisateur d’intégration**  : permet aux utilisateurs d’accéder aux données synchronisées. En général, cela est attribué au compte d’utilisateur automatiquement créé pour la synchronisation et aux autres utilisateurs devant consulter les données synchronisées ou y accéder.

Pour plus de détails sur chaque rôle, tels que les autorisations et les niveaux d’accès, voir [Configuration de comptes d’utilisateurs pour l’intégration avec [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Lors de la configuration de la connexion, les mappages de table d’intégration nécessaires à la synchronisation des données sont créés. Les entités dans Common Data Service sont mappées à des tables et des champs de table dans Business Central au moyen de tables d’intégration. Pour en savoir plus, consultez [Mappage d’entité standard pour la synchronisation](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).

## <a name="see-also"></a>Voir aussi
[Modèles de propriété de données](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Common Data Service](docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration) -->



