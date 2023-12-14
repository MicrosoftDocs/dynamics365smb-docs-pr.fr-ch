---
title: Intégrer à Microsoft Dataverse via la synchronisation des données
description: "Introduction à l’intégration et à l’utilisation de Microsoft Dataverse et ses composants pour se connecter à d’autres applications Dynamics\_365."
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 06/28/2023
ms.custom: bap-template
---

# <a name="integrate-with-microsoft-dataverse-via-data-sync"></a>Intégrer à Microsoft Dataverse via la synchronisation des données

Les applications métier utilisent souvent des données provenant de plusieurs sources. [!INCLUDE[prod_short](includes/cds_long_md.md)] combine les données dans un seul ensemble de logique qui facilite la connexion [!INCLUDE[prod_short](includes/prod_short.md)] à d’autres applications Dynamics 365. Par exemple, [!INCLUDE[crm_md](includes/crm_md.md)] ou votre propre application basée sur [!INCLUDE[prod_short](includes/cds_long_md.md)]. Pour en savoir plus sur [!INCLUDE[prod_short](includes/cds_long_md.md)], accédez à [Qu’est-ce que Dataverse ?](/powerapps/maker/common-data-service/data-platform-intro).

Les étapes suivantes offrent un aperçu des étapes pour intégrer [!INCLUDE[prod_short](includes/cds_long_md.md)] à [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Ces tâches exigent le rôle de sécurité **Administrateur système** dans [!INCLUDE[prod_short](includes/cds_long_md.md)] et [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Affectez les licences pour [!INCLUDE[prod_short](includes/cds_long_md.md)] aux utilisateurs [!INCLUDE[prod_short](includes/prod_short.md)] qui utiliseront les applications intégrées.

2. Configurez une connexion vers [!INCLUDE[prod_short](includes/cds_long_md.md)]. Pour en savoir plus, consultez [Se connecter à Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synchronisez les données entre les applications. Pour plus d’informations, voir la rubrique [Synchronisation de Business Central et de Dataverse](admin-synchronizing-business-central-and-sales.md). 

## <a name="get-started-with-"></a>Mise en route avec [!INCLUDE[prod_short](includes/cds_long_md.md)]

Pour prendre en main [!INCLUDE[prod_short](includes/cds_long_md.md)], vous avez besoin d’un compte Microsoft Power Apps. Si vous ne disposez pas encore d’un compte Power Apps, vous pouvez en obtenir un gratuitement en visitant [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) et en cliquant sur le lien **Démarrer gratuitement**. Pour en savoir plus sur la prise en main de [!INCLUDE[prod_short](includes/cds_long_md.md)], consultez le module [Mise en route avec le module Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) de la formation Microsoft.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Synchronisation des données bidirectionnelle ou unidirectionnelle

Vous pouvez synchroniser les données vers ou depuis une application métier Dynamics 365 vers une autre, ou dans les deux directions en quasi temps réel au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Par exemple, si vous intégrez [!INCLUDE[prod_short](includes/prod_short.md)] à [!INCLUDE[crm_md](includes/crm_md.md)], un vendeur peut créer une commande vente dans [!INCLUDE[crm_md](includes/crm_md.md)] et la commande est synchronisée avec [!INCLUDE[prod_short](includes/prod_short.md)]. Inversement, à partir de [!INCLUDE[crm_md](includes/crm_md.md)], le vendeur peut consulter la disponibilité de l’article sur la commande dans [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="standard-and-custom-entities"></a>Entités standard et personnalisées

[!INCLUDE[prod_short](includes/cds_long_md.md)] stocke en toute sécurité les données dans un ensemble de tables, qui sont des ensembles d’enregistrements similaires à la façon dont une table stocke des données dans une base de données. [!INCLUDE[prod_short](includes/cds_long_md.md)] comprend un ensemble de base de tables standard qui couvrent des scénarios typiques, mais vous pouvez également créer des tables personnalisées dédiées à votre organisation. Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez afficher les tables standard et personnalisées en cours de synchronisation sur la page Mappages de table d’intégration.

## <a name="about-the-business-central-base-integration-solution"></a>À propos de la solution d’intégration de base Business Central

La solution d’intégration de base est un élément clé de l’intégration. La solution ajoute les rôles et niveaux d’accès requis aux comptes d’utilisateur pour l’intégration et crée les tables nécessaires au mappage de la société [!INCLUDE[prod_short](includes/prod_short.md)] au centre de profit dans [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Par défaut, le guide de configuration assistée **Configurer la connexion [!INCLUDE[prod_short](includes/cds_long_md.md)]** importe la solution. Pour ce faire, le guide de configuration utilise un compte d’utilisateur d’administrateur que vous indiquez. Ce compte doit être un utilisateur valide dans [!INCLUDE[prod_short](includes/cds_long_md.md)] avec le rôle de sécurité suivant :

* Administrateur système  

Pour en savoir plus sur les comptes utilisateur, consultez les articles suivants :

* [Configuration des comptes d’utilisateur pour intégration à [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) 
* [Créer des utilisateurs dans Microsoft Dynamics 365 (online) et attribuer des rôles de sécurité](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Le compte d’administrateur n’est utilisé qu’une seule fois lors de la configuration en raison de modifications de paramètres apportées par la solution d’intégration de base dans [!INCLUDE[prod_short](includes/cds_long_md.md)]. Une fois la solution importée, le compte n’est plus nécessaire. L’intégration continue à utiliser le compte d’utilisateur qui est automatiquement créé spécialement pour l’intégration.

Outre la personnalisation de [!INCLUDE[prod_short](includes/cds_long_md.md)], la solution crée également les rôles suivants dans [!INCLUDE[prod_short](includes/cds_long_md.md)] pour l’intégration :

* **Administrateur d’intégration** : permet aux utilisateurs de gérer la connexion entre [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[prod_short](includes/cds_long_md.md)]. En général, ce rôle est attribué uniquement au compte d’utilisateur automatiquement créé pour la synchronisation.  
* **Utilisateur d’intégration** : permet aux utilisateurs d’accéder aux données synchronisées. En règle générale, vous attribuez ce rôle aux comptes d’utilisateur suivants :

  * Les comptes d’utilisateurs créés automatiquement pour la synchronisation.
  * Autres utilisateurs qui ont besoin d’accéder aux données synchronisées.

Pour plus de détails sur chaque rôle, tels que les autorisations et les niveaux d’accès, accédez à [Configuration de comptes d’utilisateurs pour l’intégration avec [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Lors de la configuration de la connexion, vous créez mappages de table d’intégration nécessaires à la synchronisation des données. Les entités dans [!INCLUDE[prod_short](includes/cds_long_md.md)] sont mappées à des tables et des champs de table dans [!INCLUDE [prod_short](includes/prod_short.md)] au moyen de tables d’intégration. Pour en savoir plus sur les mappages, accédez à [Mappage d’entité standard pour la synchronisation](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="handle-differences-in-local-and-base-transaction-currencies"></a>Gérer les différences entre les devises locales et de base des transactions

Vous pouvez vous connecter à un environnement [!INCLUDE[prod_short](includes/cds_long_md.md)] dont la devise de base est différente de la devise locale dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous établissez la connexion dans [!INCLUDE[prod_short](includes/prod_short.md)] sur la page **Configuration de la connexion Dataverse** ou en utilisant le guide de configuration assistée **Configurer la connexion à Dataverse**.

Pour pouvoir vous connecter, assurez-vous que le paramètre de devise de base de la transaction dans [!INCLUDE[prod_short](includes/cds_long_md.md)] a la devise définie sur la page **Devises** dans [!INCLUDE [prod_short](includes/prod_short.md)], et au moins un taux de change est spécifié pour la devise sur la page **Taux de change des devises**.

Prenons un exemple. Vous vous connectez [!INCLUDE[prod_short](includes/cds_long_md.md)] avec l’euro (EUR) défini comme devise locale sur la page **Configuration de la comptabilité** vers un environnement [!INCLUDE[prod_short](includes/cds_long_md.md)] dont la devise de transaction de base est définie sur le dollar américain (USD). Vous aurez besoin d’avoir USD sur la page **Devises** dans [!INCLUDE [prod_short](includes/prod_short.md)] et le taux de change approprié. 

Lorsque vous activez la connexion à [!INCLUDE[prod_short](includes/cds_long_md.md)], [!INCLUDE [prod_short](includes/prod_short.md)] ajoute sa devise locale à l’entité **Devise** dans [!INCLUDE[prod_short](includes/cds_long_md.md)] avec le taux de change du champ **Facteur de devise** sur la page **Taux de change de la devise**.

La synchronisation des devises est unidirectionnelle, de [!INCLUDE [prod_short](includes/prod_short.md)] vers [!INCLUDE [!INCLUDE[prod_short](includes/cds_long_md.md)], les montants monétaires sont convertis et synchronisés comme suit :

* Les montants dans la devise de base [!INCLUDE[prod_short](includes/cds_long_md.md)] sont convertis dans la devise locale [!INCLUDE [prod_short](includes/prod_short.md)] en fonction du dernier taux de change synchronisé depuis [!INCLUDE [prod_short](includes/prod_short.md)].
* Les montants dans la devise locale [!INCLUDE [prod_short](includes/prod_short.md)] se synchronisent avec la devise locale [!INCLUDE [prod_short](includes/prod_short.md)] dans l’une des autres devises (non de base) dans [!INCLUDE[prod_short](includes/cds_long_md.md)].

## <a name="see-also"></a>Voir aussi

[Modèles de propriété de données](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
