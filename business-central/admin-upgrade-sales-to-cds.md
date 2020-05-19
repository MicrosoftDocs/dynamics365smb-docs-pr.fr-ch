---
title: Mise à niveau d'une intégration à Dynamics 365 Sales | Microsoft Docs
description: Découvrez comment préparer Dynamics 365 Business Central pour l'intégrer à Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 84e335bacbfec965968d6a6839fe1eb407ab089d
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324141"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="251f8-103">Mise à niveau d'une intégration à Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="251f8-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="251f8-104">s'intègre à [!INCLUDE[d365fin](includes/cds_long_md.md)], ce qui facilite la connexion et la synchronisation des données avec d'autres applications Dynamics 365 telles que [!INCLUDE[crm_md](includes/crm_md.md)], voire des applications que vous créez vous-même.</span><span class="sxs-lookup"><span data-stu-id="251f8-104">integrates with [!INCLUDE[d365fin](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="251f8-105">S'il s'agit de votre toute première intégration, nous vous recommandons de l'effectuer au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="251f8-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <span data-ttu-id="251f8-106">Pour en savoir plus, consultez [Intégration à Common Data Service](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="251f8-106">For more information, see [Integration with Common Data Service](admin-common-data-service.md).</span></span>

<span data-ttu-id="251f8-107">Si vous avez déjà intégré [!INCLUDE[crm_md](includes/crm_md.md)] à [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez continuer à synchroniser les données à l'aide de votre configuration.</span><span class="sxs-lookup"><span data-stu-id="251f8-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="251f8-108">Cependant, si vous mettez à niveau [!INCLUDE[d365fin](includes/d365fin_md.md)] ou désactivez votre intégration [!INCLUDE[crm_md](includes/crm_md.md)], vous devez vous connecter au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)] pour la réactiver.</span><span class="sxs-lookup"><span data-stu-id="251f8-108">However, if you upgrade [!INCLUDE[d365fin](includes/d365fin_md.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="251f8-109">La reconnexion au moyen de [!INCLUDE[d365fin](includes/cds_long_md.md)] applique les paramètres de synchronisation par défaut et remplace toute configuration dont vous disposez.</span><span class="sxs-lookup"><span data-stu-id="251f8-109">Reconnecting through [!INCLUDE[d365fin](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="251f8-110">Par exemple, les mappages de table par défaut sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="251f8-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a><span data-ttu-id="251f8-111">Pour mettre à niveau votre connexion afin d'utiliser Common Data Service</span><span class="sxs-lookup"><span data-stu-id="251f8-111">To upgrade your connection to use Common Data Service</span></span>
1. <span data-ttu-id="251f8-112">Ouvrez la page **Paramètres de la connexion Microsoft Dynamics 365**, puis choisissez le bouton bascule **Activer** pour désactiver votre connexion existante à [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="251f8-112">Open the **Microsoft Dynamics 365 Connection Setup** page, choose the **Enable** toggle to turn off your existing connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="251f8-113">Ouvrez la page **Paramétrage de la connexion Common Data Service**, puis choisissez le bouton bascule **Activer** pour activer la connexion.</span><span class="sxs-lookup"><span data-stu-id="251f8-113">Open the **Common Data Service Connection Setup** page, and choose the **Enable** toggle to turn on the connection.</span></span>
  
   <span data-ttu-id="251f8-114">Après avoir activé la connexion CDS, la solution d'intégration de base Business Central CDS est déployée dans Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="251f8-114">After you enable the CDS connection, the Business Central CDS Base Integration Solution is deployed to Common Data Service.</span></span>
3. <span data-ttu-id="251f8-115">Sur la page Paramètres de la connexion Microsoft Dynamics 365, choisissez le bouton bascule Activer pour activer la connexion à [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="251f8-115">On the Microsoft Dynamics 365 Connection Setup page, choose the Enable toggle to turn on the connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   <span data-ttu-id="251f8-116">Après avoir activé la connexion Sales, la solution d'intégration Business Central est déployée dans Sales.</span><span class="sxs-lookup"><span data-stu-id="251f8-116">After you enable the Sales connection, the Business Central Integration Solution is deployed to Sales.</span></span> <span data-ttu-id="251f8-117">Cela permet l'intégration à des entités dédiées à [!INCLUDE[crm_md](includes/crm_md.md)] telles que les commandes vente, les devis et les factures.</span><span class="sxs-lookup"><span data-stu-id="251f8-117">This enables integration with entities that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
4. <span data-ttu-id="251f8-118">Choisissez **Redéployer la solution d'intégration** pour installer et configurer la solution d'intégration Business Central mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="251f8-118">Choose **Redeploy Integration Solution** to install and configure the upgraded Business Central Integration Solution.</span></span>
5. <span data-ttu-id="251f8-119">Sur la page **Paramètres de connexion Sales**, choisissez **Utiliser le paramétrage de synchronisation par défaut** pour initialiser les mappages de table d'intégration pour [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="251f8-119">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="251f8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="251f8-120">See Also</span></span>
[<span data-ttu-id="251f8-121">Intégration à Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="251f8-121">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="251f8-122">Intégration à Common Data Service</span><span class="sxs-lookup"><span data-stu-id="251f8-122">Integrating with Common Data Service</span></span>](admin-common-data-service.md)