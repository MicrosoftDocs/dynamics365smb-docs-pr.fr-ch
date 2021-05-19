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
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 772052fc88e0b8be7ec5276600b0c237e2d2f8b2
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025823"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="eacfe-103">Mise à niveau d’une intégration à Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="eacfe-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="eacfe-104">s’intègre à [!INCLUDE[prod_short](includes/cds_long_md.md)], ce qui facilite la connexion et la synchronisation des données avec d’autres applications Dynamics 365 telles que [!INCLUDE[crm_md](includes/crm_md.md)], voire des applications que vous créez vous-même.</span><span class="sxs-lookup"><span data-stu-id="eacfe-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="eacfe-105">S’il s’agit de votre toute première intégration, nous vous recommandons de l’effectuer au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eacfe-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="eacfe-106">Pour en savoir plus, consultez [Intégration à Dataverse](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="eacfe-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="eacfe-107">Si vous avez déjà intégré [!INCLUDE[crm_md](includes/crm_md.md)] à [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez continuer à synchroniser les données à l’aide de votre configuration.</span><span class="sxs-lookup"><span data-stu-id="eacfe-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="eacfe-108">Cependant, si vous mettez à niveau [!INCLUDE[prod_short](includes/prod_short.md)] ou désactivez votre intégration [!INCLUDE[crm_md](includes/crm_md.md)], vous devez vous connecter au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)] pour la réactiver.</span><span class="sxs-lookup"><span data-stu-id="eacfe-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="eacfe-109">La reconnexion au moyen de [!INCLUDE[prod_short](includes/cds_long_md.md)] applique les paramètres de synchronisation par défaut et remplace toute configuration dont vous disposez.</span><span class="sxs-lookup"><span data-stu-id="eacfe-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="eacfe-110">Par exemple, les mappages de table par défaut sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="eacfe-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="eacfe-111">Pour mettre à niveau votre connexion afin d’utiliser Dataverse</span><span class="sxs-lookup"><span data-stu-id="eacfe-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="eacfe-112">Ouvrez la page **Paramétrage de la connexion Microsoft Dynamics 365**, puis désactivez le bouton bascule **Activé** pour se déconnecter de [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eacfe-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="eacfe-113">Ouvrez la page **Paramétrage de la connexion Dataverse**, puis choisissez le bouton bascule **Activé** pour activer la connexion à [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eacfe-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="eacfe-114">Après avoir activé la connexion, la solution d’intégration Business Central est déployée dans Dataverse.</span><span class="sxs-lookup"><span data-stu-id="eacfe-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="eacfe-115">Choisissez **Redéployer la solution d’intégration** pour réinstaller la solution d’intégration Business Central.</span><span class="sxs-lookup"><span data-stu-id="eacfe-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="eacfe-116">Sur la page **Configuration de la connexion Microsoft Dynamics 365**, choisissez le bouton bascule **Activé** pour activer la reconnexion à [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eacfe-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="eacfe-117">Après avoir activé la connexion, la solution d’intégration Business Central est déployée dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="eacfe-117">After you enable the connection, the Business Central Integration Solution is deployed to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="eacfe-118">Cela permet l’intégration à des tables dédiées à [!INCLUDE[crm_md](includes/crm_md.md)] telles que les commandes vente, les devis et les factures.</span><span class="sxs-lookup"><span data-stu-id="eacfe-118">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="eacfe-119">Choisissez **Redéployer la solution d’intégration** pour réinstaller la solution d’intégration Business Central.</span><span class="sxs-lookup"><span data-stu-id="eacfe-119">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
6. <span data-ttu-id="eacfe-120">Sur la page **Paramètres de connexion Sales**, choisissez **Utiliser le paramétrage de synchronisation par défaut** pour initialiser les mappages de table d’intégration pour [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eacfe-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="eacfe-121">En utilisant l′action **Utiliser le paramétrage de synchronisation par défaut**, les mappages de table d′intégration par défaut sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="eacfe-121">Using the **Use Default Synchronization Setup** action will apply the default integration table mappings.</span></span> <span data-ttu-id="eacfe-122">Tous les mappages personnalisés sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="eacfe-122">All custom mappings will be overwritten.</span></span> <span data-ttu-id="eacfe-123">Pour conserver des mappages personnalisés, nous vous recommandons de les exporter vers Excel ou de discuter avec votre partenaire Microsoft des autres moyens permettant de conserver vos mappages personnalisés.</span><span class="sxs-lookup"><span data-stu-id="eacfe-123">If you have custom mappings that you want to keep, we recommend that you export them to Excel or talk to your Microsoft partner about other ways to keep your custom mappings.</span></span>    

## <a name="see-also"></a><span data-ttu-id="eacfe-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eacfe-124">See Also</span></span>
[<span data-ttu-id="eacfe-125">Intégration à Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="eacfe-125">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="eacfe-126">Intégration à Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="eacfe-126">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]