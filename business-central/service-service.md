---
title: Gestion des services | Microsoft Docs
description: Apprenez à utiliser des fonctions conçues pour prendre en charge les opérations de l'atelier de réparation et du service clientèle.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f59383bc5c16ece42f1bd2d7e2eb6a2ca2c9b6c8
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311563"
---
# <a name="service-management"></a><span data-ttu-id="00cf2-103">Gestion des services</span><span class="sxs-lookup"><span data-stu-id="00cf2-103">Service Management</span></span>
> [!NOTE]
> <span data-ttu-id="00cf2-104">La fonctionnalité décrite dans ces rubrique et sous-rubriques n'est visible dans l'interface utilisateur que si vous avez l'expérience **Premium**.</span><span class="sxs-lookup"><span data-stu-id="00cf2-104">Functionality described in this topic and sub topics is only visible in the user interface if you have the **Premium** experience.</span></span> <span data-ttu-id="00cf2-105">Pour plus d'informations, voir [Modifier les fonctionnalités affichées](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="00cf2-105">For more information, see [Change Which Features are Displayed](ui-experiences.md).</span></span>

<span data-ttu-id="00cf2-106">L'offre d'un service continu aux clients est essentielle à toute transaction commerciale et peut être source de satisfaction et de fidélisation des clients, en complément des revenus.</span><span class="sxs-lookup"><span data-stu-id="00cf2-106">Providing ongoing service to customers is an important part of any business and one that can be a source of customer satisfaction and loyalty, in addition to revenue.</span></span> <span data-ttu-id="00cf2-107">Cependant, gérer et suivre des services n'est pas toujours facile ; [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut un ensemble d'outils qui simplifient ces tâches.</span><span class="sxs-lookup"><span data-stu-id="00cf2-107">However, managing and tracking service is not always easy, and [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a set of tools to help.</span></span> <span data-ttu-id="00cf2-108">Vous pouvez les utiliser dans divers scénarios d'entreprise : systèmes de distribution complexes du service clientèle, environnements de service industriel avec des nomenclatures, affectation d'un nombre important de techniciens de service avec des besoins en gestion des pièces de rechange.</span><span class="sxs-lookup"><span data-stu-id="00cf2-108">These tools are designed to support repair shop and field service operations, and can be used in business scenarios such as complex customer service distribution systems, industrial service environments with bills of materials, and high volume dispatching of service technicians with requirements for spare parts management.</span></span>  

 <span data-ttu-id="00cf2-109">Ces outils permettent de réaliser ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="00cf2-109">With these tools you can accomplish the following:</span></span>  

* <span data-ttu-id="00cf2-110">Planifier les appels de service et configurer les commandes service.</span><span class="sxs-lookup"><span data-stu-id="00cf2-110">Schedule service calls and set up service orders.</span></span>  
* <span data-ttu-id="00cf2-111">Assurer le suivi des pièces et fournitures de réparation.</span><span class="sxs-lookup"><span data-stu-id="00cf2-111">Track repair parts and supplies.</span></span>  
* <span data-ttu-id="00cf2-112">Affecter le personnel de service sur la base de leurs compétences et disponibilités.</span><span class="sxs-lookup"><span data-stu-id="00cf2-112">Assign service personnel based on skill and availability.</span></span>  
* <span data-ttu-id="00cf2-113">Fournir des estimations de service et des factures service.</span><span class="sxs-lookup"><span data-stu-id="00cf2-113">Provide service estimates and service invoices.</span></span>  

<span data-ttu-id="00cf2-114">En outre, vous pouvez standardiser le codage, configurer les contrats, appliquer une stratégie de remise et créer des calendriers pour les salariés en charge de la prestation de service.</span><span class="sxs-lookup"><span data-stu-id="00cf2-114">In addition, you can standardize coding, set up contracts, implement a discounting policy, and create route maps for service employees.</span></span>  

<span data-ttu-id="00cf2-115">En général, la gestion de services est constituée de deux éléments : la configuration et le paramétrage de votre système, et son utilisation pour les tarifs, contrats, commandes, affectation du personnel de service et planificateur de traitements.</span><span class="sxs-lookup"><span data-stu-id="00cf2-115">In general, there are two aspects to service management: configuring and setting up your system, and using it for pricing, contracts, orders, service personnel dispatch, and job scheduler.</span></span>  

<span data-ttu-id="00cf2-116">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="00cf2-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="00cf2-117">**Pour**</span><span class="sxs-lookup"><span data-stu-id="00cf2-117">**To**</span></span>|<span data-ttu-id="00cf2-118">**Voir**</span><span class="sxs-lookup"><span data-stu-id="00cf2-118">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="00cf2-119">Configurer la gestion des services (codes panne, stratégies, documents et modèles par défaut, etc).</span><span class="sxs-lookup"><span data-stu-id="00cf2-119">Set up Service Management, including fault codes, policies, default documents and templates.</span></span>|[<span data-ttu-id="00cf2-120">Paramétrage de la gestion des services</span><span class="sxs-lookup"><span data-stu-id="00cf2-120">Setting Up Service Management</span></span>](service-setup-service.md)|  
|<span data-ttu-id="00cf2-121">Gérer la tarification service, créer des articles de service et comprendre comment surveiller la progression.</span><span class="sxs-lookup"><span data-stu-id="00cf2-121">Manage service pricing, create service items, and understand how to monitor progress.</span></span>|[<span data-ttu-id="00cf2-122">Services de planification</span><span class="sxs-lookup"><span data-stu-id="00cf2-122">Planning Service</span></span>](service-plan-service.md)|  
|<span data-ttu-id="00cf2-123">Créer et gérer les accords contractuels entre vous et vos clients.</span><span class="sxs-lookup"><span data-stu-id="00cf2-123">Create and manage contractual agreements between you and your customers.</span></span>|[<span data-ttu-id="00cf2-124">Exécution des contrats de service</span><span class="sxs-lookup"><span data-stu-id="00cf2-124">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)|  
|<span data-ttu-id="00cf2-125">Fournir des services aux clients et facturer les commandes service.</span><span class="sxs-lookup"><span data-stu-id="00cf2-125">Provide service to customers, and invoice service orders.</span></span>|[<span data-ttu-id="00cf2-126">Exécution du service</span><span class="sxs-lookup"><span data-stu-id="00cf2-126">Delivering Service</span></span>](service-deliver-service.md)|  

## <a name="see-also"></a><span data-ttu-id="00cf2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00cf2-127">See Also</span></span>  
<span data-ttu-id="00cf2-128">[Gestion des comptes client](receivables-manage-receivables.md) </span><span class="sxs-lookup"><span data-stu-id="00cf2-128">[Managing Receivables](receivables-manage-receivables.md) </span></span>  
<span data-ttu-id="00cf2-129">[Projets](projects-how-create-jobs.md) </span><span class="sxs-lookup"><span data-stu-id="00cf2-129">[Jobs](projects-how-create-jobs.md) </span></span>  
<span data-ttu-id="00cf2-130">[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="00cf2-130">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] ](index.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
