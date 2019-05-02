---
title: Paramétrage de la gestion des services | Microsoft Docs
description: Aperçu des tâches de paramétrage de la gestion des services en fonction de la manière dont vos partenaires gère leurs services.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service items, repairs, maintenance, fix
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: c4b8287c8e1c056bd45a30376e96aca1f8f4ddcc
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820567"
---
# <a name="setting-up-service-management"></a><span data-ttu-id="166ea-103">Paramétrage de la gestion des services</span><span class="sxs-lookup"><span data-stu-id="166ea-103">Setting Up Service Management</span></span>
<span data-ttu-id="166ea-104">Avant de pouvoir démarrer l'utilisation des fonctionnalités de gestion des services dans [!INCLUDE[d365fin](includes/d365fin_md.md)], il y a quelques éléments à configurer.</span><span class="sxs-lookup"><span data-stu-id="166ea-104">Before you can start using Service Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)], there are a few things to set up.</span></span> <span data-ttu-id="166ea-105">Par exemple, vous pouvez établir le codage des services standard, les codes symptôme et panne, ainsi que configurer les articles de service et les types d'article de service requis par le service clientèle.</span><span class="sxs-lookup"><span data-stu-id="166ea-105">For example, you can establish coding for standard services, symptoms, and fault codes, and the service items and service item types that your company's customer service needs require.</span></span>  

<span data-ttu-id="166ea-106">Lorsque vous configurez la gestion des services, vous devez choisir les services que vous allez fournir aux clients et les planifier.</span><span class="sxs-lookup"><span data-stu-id="166ea-106">When you set up Service Management, you must decide what services to offer customers and the schedule for those services.</span></span> <span data-ttu-id="166ea-107">Un service correspond à un type de travail exécuté par une ou plusieurs ressources et fourni à un client.</span><span class="sxs-lookup"><span data-stu-id="166ea-107">A service is a type of work performed by one or more resources and provided to a customer.</span></span> <span data-ttu-id="166ea-108">Ce peut être un type de réparation informatique.</span><span class="sxs-lookup"><span data-stu-id="166ea-108">For example, a service could be a type of computer repair.</span></span> <span data-ttu-id="166ea-109">Un article de service correspond à l'équipement ou l'article associé au service : par exemple, un ordinateur à réparer, installé chez un client spécifique.</span><span class="sxs-lookup"><span data-stu-id="166ea-109">A service item is the equipment or item needing servicing, for example, the computer needing repair, installed at a specific customer.</span></span> <span data-ttu-id="166ea-110">Vous pouvez configurer les services afin de les intégrer au groupe d'articles de réparation ou de maintenance associés.</span><span class="sxs-lookup"><span data-stu-id="166ea-110">You can set up services as part of a group of related repair or maintenance items.</span></span>  
  
<span data-ttu-id="166ea-111">Lorsque vous définissez un service, vous pouvez l'associer aux compétences requises pour l'exécuter.</span><span class="sxs-lookup"><span data-stu-id="166ea-111">When you define a service, you can associate it with the skills required to perform the service.</span></span> <span data-ttu-id="166ea-112">Afin d'optimiser l'efficacité des représentants du service clientèle, vous pouvez également configurer les directives incident et affecter les coûts de démarrage courants (coûts déplacement ou autres frais).</span><span class="sxs-lookup"><span data-stu-id="166ea-112">To help your service representatives be efficient, you can also set up real time troubleshooting guidelines and assign typical startup costs, such as travel costs or other fees.</span></span>  

<span data-ttu-id="166ea-113">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="166ea-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  
  
| <span data-ttu-id="166ea-114">Pour</span><span class="sxs-lookup"><span data-stu-id="166ea-114">To</span></span> | <span data-ttu-id="166ea-115">Voir</span><span class="sxs-lookup"><span data-stu-id="166ea-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="166ea-116">Configurer les codes qui affectent automatiquement les lignes des documents service pour les services que vous fournissez souvent.</span><span class="sxs-lookup"><span data-stu-id="166ea-116">Set up codes that automatically assign lines on service documents for services you deliver often.</span></span> |[<span data-ttu-id="166ea-117">Configurer des codes prestations standards</span><span class="sxs-lookup"><span data-stu-id="166ea-117">Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)|
| <span data-ttu-id="166ea-118">Définir les paramètres généraux qui contrôlent les aspects des processus de gestion des services.</span><span class="sxs-lookup"><span data-stu-id="166ea-118">Establish general settings that control aspects of Service Management Processes.</span></span>|[<span data-ttu-id="166ea-119">Configuration des processus de service</span><span class="sxs-lookup"><span data-stu-id="166ea-119">Configure Service Processes</span></span>](service-setup-service-processes.md)|
| <span data-ttu-id="166ea-120">Définir le mode de fonctionnement de votre organisation avec le reporting panne.</span><span class="sxs-lookup"><span data-stu-id="166ea-120">Define how your organization works with fault reporting.</span></span> |[<span data-ttu-id="166ea-121">Configurer le reporting panne</span><span class="sxs-lookup"><span data-stu-id="166ea-121">Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md) |
| <span data-ttu-id="166ea-122">Configurer les offres de service que votre société fournit aux clients.</span><span class="sxs-lookup"><span data-stu-id="166ea-122">Set up the service offerings that your company delivers to customers.</span></span>|[<span data-ttu-id="166ea-123">Configurer des offres de service</span><span class="sxs-lookup"><span data-stu-id="166ea-123">Set Up Service Offerings</span></span>](service-how-setup-service-offerings.md)|
| <span data-ttu-id="166ea-124">Fournir des instructions incident permettant aux représentants commerciaux de fournir un service plus rapide.</span><span class="sxs-lookup"><span data-stu-id="166ea-124">Provide troubleshooting guidelines that help service reps deliver faster service.</span></span> |[<span data-ttu-id="166ea-125">Configurer les processus incident</span><span class="sxs-lookup"><span data-stu-id="166ea-125">Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md) |
| <span data-ttu-id="166ea-126">Configurer l'affectation des ressources pour simplifier l'affectation de la ressource à une tâche service de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="166ea-126">Set up resource allocation to make it easy to assign the right resource to a service task.</span></span> |[<span data-ttu-id="166ea-127">Configurer l'affectation des ressources</span><span class="sxs-lookup"><span data-stu-id="166ea-127">Set Up Resource Allocation</span></span>](service-how-setup-resource-allocation.md) |
| <span data-ttu-id="166ea-128">Définir la tarification des services, et paramétrer des coûts service supplémentaires pour évaluer des commandes service.</span><span class="sxs-lookup"><span data-stu-id="166ea-128">Define pricing for services, and set up additional service costs to assess on service orders.</span></span> |[<span data-ttu-id="166ea-129">Configurer la tarification et les frais supplémentaires pour les services</span><span class="sxs-lookup"><span data-stu-id="166ea-129">Set Up Pricing and Additional Costs for Services</span></span>](service-how-setup-service-costs-pricing.md)|
| <span data-ttu-id="166ea-130">Définir la configuration pour suivre les heures ressource et les statuts commande service afin de prévoir les besoins en charges de travail et en service.</span><span class="sxs-lookup"><span data-stu-id="166ea-130">Set things up so you can track resource hours and service order status in order to forecast workloads and service needs.</span></span>|[<span data-ttu-id="166ea-131">Configurer des heures de travail et des heures de service</span><span class="sxs-lookup"><span data-stu-id="166ea-131">Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)|
| <span data-ttu-id="166ea-132">Configurer les options de statut de réparation pour surveiller la progression des réparations.</span><span class="sxs-lookup"><span data-stu-id="166ea-132">Set up repair status options so that you can monitor progress on repairs.</span></span> | [<span data-ttu-id="166ea-133">Paramétrer les statuts des commandes service et des réparations</span><span class="sxs-lookup"><span data-stu-id="166ea-133">Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)|
| <span data-ttu-id="166ea-134">Configurer un programme d'articles de prêt, en vue de pouvoir prêter un article de substitution lorsque vous travaillez avec un article de service.</span><span class="sxs-lookup"><span data-stu-id="166ea-134">Set up a loaner program, so you can lend a substitute while you work on a service item.</span></span> |[<span data-ttu-id="166ea-135">Configuration d'un programme d'articles de prêt</span><span class="sxs-lookup"><span data-stu-id="166ea-135">Set Up a Loaner Program</span></span>](service-how-setup-loaner-program.md) |
| <span data-ttu-id="166ea-136">Configurer les articles de service et les composants article de service.</span><span class="sxs-lookup"><span data-stu-id="166ea-136">Set up service items and service item components.</span></span> |[<span data-ttu-id="166ea-137">Configurer des articles de service</span><span class="sxs-lookup"><span data-stu-id="166ea-137">Set Up Service Items</span></span>](service-how-setup-service-items.md) |
| <span data-ttu-id="166ea-138">Définir les bases pour créer des contrats de service et des devis contrat.</span><span class="sxs-lookup"><span data-stu-id="166ea-138">Lay the groundwork for creating service contracts and contract quotes.</span></span> |[<span data-ttu-id="166ea-139">Configurer des contrats de service</span><span class="sxs-lookup"><span data-stu-id="166ea-139">Set Up Service Contracts</span></span>](service-how-setup-service-contracts.md) |

## <a name="see-also"></a><span data-ttu-id="166ea-140">Voir aussi .</span><span class="sxs-lookup"><span data-stu-id="166ea-140">See also</span></span>
[<span data-ttu-id="166ea-141">Gestion des services</span><span class="sxs-lookup"><span data-stu-id="166ea-141">Service Management</span></span>](service-service.md)  
[<span data-ttu-id="166ea-142">Mise en route</span><span class="sxs-lookup"><span data-stu-id="166ea-142">Getting Started</span></span>](product-get-started.md)  