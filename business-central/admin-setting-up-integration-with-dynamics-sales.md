---
title: Configuration des comptes d’utilisateur pour l’intégration à Microsoft Dataverse | Microsoft Docs
description: 'Découvrez comment configurer les comptes d’utilisateur que les applications utilisent pour échanger les données, et que les utilisateurs emploient pour accéder aux données et les synchroniser dans les applications.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: null
ms.date: 01/12/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Configuration des comptes d’utilisateur pour l’intégration à Microsoft Dataverse via la synchronisation des données

Cet article fournit un aperçu de la manière dont la configuration des comptes d’utilisateur requis pour intégrer [!INCLUDE[prod_short](includes/cds_long_md.md)] à [!INCLUDE[prod_short](includes/prod_short.md)].

## Configuration du compte d’utilisateur administrateur

Pour configurer la connexion entre [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[prod_short](includes/cds_long_md.md)], vous devez vous connecter à [!INCLUDE[prod_short](includes/prod_short.md)] avec un compte d’utilisateur qui est attribué à la licence [!INCLUDE[prod_short](includes/prod_short.md)] Essential ou [!INCLUDE[prod_short](includes/prod_short.md)] Premium. Nous utiliserons ce compte une fois pour installer et configurer certains composants requis.

> [!IMPORTANT]
> Lors de la configuration, il vous sera demandé de fournir des informations d’identification pour l’environnement [!INCLUDE[prod_short](includes/cds_long_md.md)]. Indiquez les identifiants d’un compte qui est un utilisateur sous licence et attribué au rôle de sécurité **Administrateur système** dans l’environnement [!INCLUDE[prod_short](includes/cds_long_md.md)] et d’administrateur général sur le locataire auquel l’environnement appartient. Ce compte n’a pas besoin de licence pour [!INCLUDE[prod_short](includes/prod_short.md)], car il ne sera utilisé que pour faire les tâches de configuration dans l’environnement [!INCLUDE[prod_short](includes/cds_long_md.md)].
>
> Une fois la configuration de la connexion terminée, vous pouvez supprimer cet utilisateur [!INCLUDE[prod_short](includes/cds_long_md.md)]. L’intégration continuera à utiliser le compte d’utilisateur qui est automatiquement créé spécialement pour l’intégration.

## Autorisations et rôles de sécurité pour les comptes d’utilisateur dans [!INCLUDE[prod_short](includes/cds_long_md.md)]

La solution d’intégration de base crée le rôle suivant dans [!INCLUDE [cds_long_md](includes/cds_long_md.md)] pour l’intégration :

* **Intégration Dataverse Business Central** – Vous permet de gérer la connexion entre [!INCLUDE [prod_short](includes/prod_short.md)] et [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. En général, cela est attribué uniquement au compte d’utilisateur automatiquement créé pour la synchronisation.

> [!NOTE]
> Seul l’utilisateur de l’application qui exécute l’intégration doit disposer du rôle **Business Central Dataverse Intégration** . L’utilisateur de l’application n’a pas besoin de licence [!INCLUDE [prod_short](includes/prod_short.md)] ou [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

Lorsque vous installez la solution d’intégration de base, elle configure les autorisations pour le compte d’utilisateur d’intégration. Si ces autorisations sont modifiées manuellement, vous pouvez les réinitialiser. Sélectionnez **Redéployer la solution d’intégration** sur la page **Configuration de la connexion Dataverse** pour réinstaller la solution d’intégration de base. Cette étape déploiera le rôle de sécurité Intégration Business Central.

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

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

### Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

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

## Voir aussi

[Intégration à Microsoft Dataverse](admin-common-data-service.md)  
[Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
