---
title: Mise à niveau d’une intégration à Dynamics 365 Sales
description: Apprenez à déplacer votre intégration Dynamics 365 Business Central avec Dynamics 365 Sales à la dernière version.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 69ffe6cea05cc28d1950481a07b064a3365f404e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386714"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="04a4c-103">Mise à niveau d’une intégration à Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="04a4c-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="04a4c-104">s’intègre à [!INCLUDE[prod_short](includes/cds_long_md.md)], ce qui facilite la connexion et la synchronisation des données avec d’autres applications Dynamics 365 telles que [!INCLUDE[crm_md](includes/crm_md.md)], voire des applications que vous créez vous-même.</span><span class="sxs-lookup"><span data-stu-id="04a4c-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="04a4c-105">S’il s’agit de votre toute première intégration, nous vous recommandons de l’effectuer au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="04a4c-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="04a4c-106">Pour en savoir plus, consultez [Intégration à Dataverse](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="04a4c-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="04a4c-107">Si vous avez déjà intégré [!INCLUDE[crm_md](includes/crm_md.md)] à [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez continuer à synchroniser les données à l’aide de votre configuration.</span><span class="sxs-lookup"><span data-stu-id="04a4c-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="04a4c-108">Cependant, si vous mettez à niveau [!INCLUDE[prod_short](includes/prod_short.md)] ou désactivez votre intégration [!INCLUDE[crm_md](includes/crm_md.md)], vous devez vous connecter au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)] pour la réactiver.</span><span class="sxs-lookup"><span data-stu-id="04a4c-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="04a4c-109">La reconnexion au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)] applique les paramètres de synchronisation par défaut et remplace toute configuration dont vous disposez.</span><span class="sxs-lookup"><span data-stu-id="04a4c-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="04a4c-110">Par exemple, les mappages de table par défaut sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="04a4c-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="04a4c-111">Pour mettre à niveau votre connexion afin d’utiliser Dataverse</span><span class="sxs-lookup"><span data-stu-id="04a4c-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="04a4c-112">Ouvrez la page **Paramétrage de la connexion Microsoft Dynamics 365**, puis désactivez le bouton bascule **Activé** pour se déconnecter de [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="04a4c-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="04a4c-113">Ouvrez la page **Paramétrage de la connexion Dataverse**, puis choisissez le bouton bascule **Activé** pour activer la connexion à [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="04a4c-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="04a4c-114">Après avoir activé la connexion, la solution d’intégration Business Central est déployée dans Dataverse.</span><span class="sxs-lookup"><span data-stu-id="04a4c-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="04a4c-115">Choisissez **Redéployer la solution d’intégration** pour réinstaller la solution d’intégration Business Central.</span><span class="sxs-lookup"><span data-stu-id="04a4c-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="04a4c-116">Sur la page **Configuration de la connexion Microsoft Dynamics 365**, choisissez le bouton bascule **Activé** pour activer la reconnexion à [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="04a4c-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="04a4c-117">Après avoir activé la connexion, la solution d’intégration Business Central est déployée dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="04a4c-117">After you enable the connection, the Business Central Integration Solution is deployed to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="04a4c-118">Cela permet l’intégration à des tables dédiées à [!INCLUDE[crm_md](includes/crm_md.md)] telles que les commandes vente, les devis et les factures.</span><span class="sxs-lookup"><span data-stu-id="04a4c-118">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="04a4c-119">Choisissez **Redéployer la solution d’intégration** pour réinstaller la solution d’intégration Business Central.</span><span class="sxs-lookup"><span data-stu-id="04a4c-119">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
6. <span data-ttu-id="04a4c-120">Sur la page **Paramètres de connexion Sales**, choisissez **Utiliser le paramétrage de synchronisation par défaut** pour initialiser les mappages de table d’intégration pour [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="04a4c-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="04a4c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04a4c-121">See Also</span></span>
[<span data-ttu-id="04a4c-122">Intégration à Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="04a4c-122">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="04a4c-123">Intégration à Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="04a4c-123">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]