---
title: Configuration des comptes d'utilisateur pour l'intégration à Common Data Service | Microsoft Docs
description: Découvrez comment configurer les comptes d'utilisateur que les applications utilisent pour échanger les données, et que les utilisateurs emploient pour accéder aux données et les synchroniser dans les applications.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: ad10aa53b4fe6a8b9b65ad798c206fa251e08a7a
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196510"
---
# <a name="setting-up-user-accounts-for-integrating-with-common-data-service"></a>Configuration des comptes d'utilisateur pour intégration à Common Data Service
Cet article fournit un aperçu de la manière dont la configuration des comptes d'utilisateur requis pour intégrer [!INCLUDE[d365fin](includes/cds_long_md.md)] à [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="setting-up-the-administrator-user-account"></a>Configuration du compte d'utilisateur administrateur
Vous devez ajouter votre compte d'utilisateur administrateur pour [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant qu'utilisateur dans [!INCLUDE[d365fin](includes/cds_long_md.md)]. Lorsque vous configurez la connexion entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)], nous utilisons ce compte une fois pour installer et configurer certains composants requis. <!--Verify this-->

## <a name="setting-up-the-user-account-for-the-integration"></a>Configuration du compte d'utilisateur pour l'intégration
Vous devez créer un compte d'utilisateur dédié dans votre abonnement Office 365 que [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)] peuvent utiliser pour synchroniser les données. Ce compte d'utilisateur doit pouvoir se connecter à [!INCLUDE[d365fin](includes/cds_long_md.md)]. Autrement dit, cet utilisateur doit avoir une licence pour [!INCLUDE[d365fin](includes/cds_long_md.md)] et au moins un rôle de sécurité doit lui être affecté dans [!INCLUDE[d365fin](includes/cds_long_md.md)]. <!--not sure that this applies as described [here](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). For more information about how to create users in [!INCLUDE[d365fin](includes/cds_long_md.md)], see [Manage security, users, and teams](https://go.microsoft.com/fwlink/?LinkID=616518). --> Une fois la connexion configurée, [!INCLUDE[d365fin](includes/d365fin_md.md)] affectera au compte d'utilisateur les rôles de sécurité nécessaires dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

<!--![Assisted setup guide showing place to enter synchronization user credentials](media/sync-user-setup.png "Visualization assisted setup wizard page showing place to enter synchronization user credentials")-->

> [!IMPORTANT]  
> N'utilisez pas le compte administrateur pour la synchronisation [!INCLUDE[d365fin](includes/cds_long_md.md)]. Cela interromprait la synchronisation.

## <a name="permissions-and-security-roles-for-user-accounts-in-d365fin"></a>Autorisations et rôles de sécurité pour les comptes d'utilisateur dans [!INCLUDE[d365fin](includes/cds_long_md.md)]
Lorsque vous installez la solution d'intégration de base CDS, les autorisations pour le compte d'utilisateur d'intégration sont configurées. Si ces autorisations sont modifiées, vous devrez peut-être les réinitialiser. Vous pouvez le faire en réinstallant la solution d'intégration de base CDS en choisissant **Redéployer la solution d'intégration** sur la page **Paramétrage de la connexion Common Data Service**. Le rôle de sécurité Intégration Business Central CDS est déployé.


<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)].

### Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

#### Integration User
The following table displays the minimum permissions on each tab for each security role that is required for the integration user.

##### Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## <a name="see-also"></a>Voir aussi  
[Intégration à Common Data Service](admin-common-data-service.md)  
[Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
