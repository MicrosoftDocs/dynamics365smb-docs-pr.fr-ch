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
ms.openlocfilehash: 9cd00cd3b3cb55ce3af35bd82284570b86720d63
ms.sourcegitcommit: 0c6f4382fad994fb6aea9dcde3b2dc25382c5968
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484276"
---
# <a name="setting-up-user-accounts-for-integrating-with-common-data-service"></a><span data-ttu-id="e094f-103">Configuration des comptes d'utilisateur pour intégration à Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e094f-103">Setting Up User Accounts for Integrating with Common Data Service</span></span>
<span data-ttu-id="e094f-104">Cet article fournit un aperçu de la manière dont la configuration des comptes d'utilisateur requis pour intégrer [!INCLUDE[d365fin](includes/cds_long_md.md)] à [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e094f-104">This article provides an overview of how to set up the user accounts that are required to integrate [!INCLUDE[d365fin](includes/cds_long_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="setting-up-the-administrator-user-account"></a><span data-ttu-id="e094f-105">Configuration du compte d'utilisateur administrateur</span><span class="sxs-lookup"><span data-stu-id="e094f-105">Setting Up the Administrator User Account</span></span>
<span data-ttu-id="e094f-106">Vous devez ajouter votre compte d'utilisateur administrateur pour [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant qu'utilisateur dans [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e094f-106">You must add your administrator user account for [!INCLUDE[d365fin](includes/d365fin_md.md)] as a user in [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <span data-ttu-id="e094f-107">Lorsque vous configurez la connexion entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)], nous utilisons ce compte une fois pour installer et configurer certains composants requis.</span><span class="sxs-lookup"><span data-stu-id="e094f-107">When you set up the connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[d365fin](includes/cds_long_md.md)] we will use this account one time to install and configure some required components.</span></span> 

## <a name="permissions-and-security-roles-for-user-accounts-in-d365fin"></a><span data-ttu-id="e094f-108">Autorisations et rôles de sécurité pour les comptes d'utilisateur dans [!INCLUDE[d365fin](includes/cds_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="e094f-108">Permissions and Security Roles for User Accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]</span></span>
<span data-ttu-id="e094f-109">Lorsque vous installez la solution d'intégration de base CDS, les autorisations pour le compte d'utilisateur d'intégration sont configurées.</span><span class="sxs-lookup"><span data-stu-id="e094f-109">When you install the CDS Base Integration Solution, permissions for the integration user account are configured.</span></span> <span data-ttu-id="e094f-110">Si ces autorisations sont modifiées manuellement, vous pouvez les réinitialiser.</span><span class="sxs-lookup"><span data-stu-id="e094f-110">If those permissions are changed manually you can reset them.</span></span> <span data-ttu-id="e094f-111">Vous pouvez le faire en réinstallant la solution d'intégration de base CDS en choisissant **Redéployer la solution d'intégration** sur la page **Paramétrage de la connexion Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="e094f-111">You can do that by reinstalling the CDS Base Integration Solution by choosing **Redeploy Integration Solution** on the **Common Data Service Connection Setup** page.</span></span> <span data-ttu-id="e094f-112">Le rôle de sécurité Intégration Business Central CDS est déployé.</span><span class="sxs-lookup"><span data-stu-id="e094f-112">The Business Central CDS Integration security role is deployed.</span></span>

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

### Minimum Permissions for automatically created [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration application user.

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

## <a name="see-also"></a><span data-ttu-id="e094f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e094f-113">See Also</span></span>  
[<span data-ttu-id="e094f-114">Intégration à Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e094f-114">Integrating with Common Data Service</span></span>](admin-common-data-service.md)  
[<span data-ttu-id="e094f-115">Intégration à Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="e094f-115">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
