---
title: Plusieurs contrats | Microsoft Docs
description: Selon les accords de votre niveau de service avec un client, vous pouvez avoir à gérer un article de service sous plusieurs contrats de service.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 58e92211695ea3a8d8c4137c699794f935c1bc69
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820446"
---
# <a name="multiple-contracts"></a><span data-ttu-id="87045-103">Plusieurs contrats</span><span class="sxs-lookup"><span data-stu-id="87045-103">Multiple Contracts</span></span>
<span data-ttu-id="87045-104">Selon les accords de votre niveau de service avec un client, vous pouvez avoir à gérer un article de service sous plusieurs contrats de service.</span><span class="sxs-lookup"><span data-stu-id="87045-104">Depending on your service level agreements with a customer, you may have to handle a service item under more than one service contract.</span></span>  
  
<span data-ttu-id="87045-105">En gérant un article de service sous plusieurs contrats, vous pouvez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="87045-105">By handling a service item under multiple contracts, you can do the following:</span></span>  
  
* <span data-ttu-id="87045-106">Émettre différents contrats pour un même article de service.</span><span class="sxs-lookup"><span data-stu-id="87045-106">Issue different contracts for the same service item.</span></span>  
* <span data-ttu-id="87045-107">Assurer la maintenance des composants séparément.</span><span class="sxs-lookup"><span data-stu-id="87045-107">Service parts separately.</span></span>  
* <span data-ttu-id="87045-108">Envisager les différentes compétences qui sont requises pour assurer la maintenance de différents aspects d'un article de service, comme les composants mécaniques et les logiciels.</span><span class="sxs-lookup"><span data-stu-id="87045-108">Consider different skills that are required to service different aspects of a service item, such as mechanical components and software.</span></span>  
* <span data-ttu-id="87045-109">Spécifier des délais de réponse et fréquences de maintenance différents pour les composants d'un article de service.</span><span class="sxs-lookup"><span data-stu-id="87045-109">Specify different response times and frequencies in servicing different parts of a service item.</span></span>  
* <span data-ttu-id="87045-110">Indiquer différents types d'activité à exécuter sur un article de service si celui-ci demande différents types de maintenance à des moments différents.</span><span class="sxs-lookup"><span data-stu-id="87045-110">Address different kinds of activities to be performed on a service item when the service item requires different types of service in different time periods.</span></span>  
* <span data-ttu-id="87045-111">Sélectionner et affecter un numéro contrat adéquat à une ligne article de service lorsque vous créez une commande service.</span><span class="sxs-lookup"><span data-stu-id="87045-111">Select and assign an appropriate contract number to a service item line when you are creating a service order.</span></span>  
* <span data-ttu-id="87045-112">Gérer les informations financières pertinentes portant sur les articles de service et les accords de niveau de service.</span><span class="sxs-lookup"><span data-stu-id="87045-112">Handle relevant financial information about service items and service level agreements.</span></span>  
  
<span data-ttu-id="87045-113">Vous pouvez vous inspirer des exemples suivants d'utilisation de la fonctionnalité de contrats multiples.</span><span class="sxs-lookup"><span data-stu-id="87045-113">You can consider the following examples of using the multiple contracts functionality.</span></span>  
  
## <a name="creating-multiple-contracts-per-service-item"></a><span data-ttu-id="87045-114">Création de plusieurs contrats par article de service</span><span class="sxs-lookup"><span data-stu-id="87045-114">Creating Multiple Contracts per Service Item</span></span>  
<span data-ttu-id="87045-115">Vous pouvez créer manuellement un contrat de service ou un devis contrat pour des articles de service déjà enregistrés dans des contrats non annulés appartenant à un même client.</span><span class="sxs-lookup"><span data-stu-id="87045-115">You can manually create a service contract or contract quote for service items already registered in non-canceled contracts owned by the same customer.</span></span> <span data-ttu-id="87045-116">Pour cela, utilisez la procédure standard de création de contrats de service et de devis contrat de service.</span><span class="sxs-lookup"><span data-stu-id="87045-116">To do this, follow the standard procedure of creating service contracts and service contract quotes.</span></span> <span data-ttu-id="87045-117">Pour plus d'informations, voir [Utiliser des contrats de service et des devis contrat de service](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span><span class="sxs-lookup"><span data-stu-id="87045-117">For more information, see [Work with Service Contracts and Service Contract Quotes](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span></span>  
  
<span data-ttu-id="87045-118">Lorsque vous ajoutez un article de service à une ligne contrat déjà enregistrée dans d'autres contrats de service ou devis contrat, un message d'avertissement est affiché indiquant que l'article de service appartient déjà à un ou plusieurs contrats de service ou devis contrat.</span><span class="sxs-lookup"><span data-stu-id="87045-118">When you add a service item on a contract line that is registered in other service contracts or contract quotes, a warning message is displayed stating that the service item already belongs to one or more service contracts or contract quotes.</span></span> <span data-ttu-id="87045-119">Si vous confirmez ce message, toutes les informations pertinentes de l'article de service sont copiées dans une ligne contrat nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="87045-119">If you confirm this message, all relevant service item information is copied to a newly created contract line.</span></span>  
  
## <a name="copying-documents"></a><span data-ttu-id="87045-120">Copie de documents</span><span class="sxs-lookup"><span data-stu-id="87045-120">Copying Documents</span></span>  
<span data-ttu-id="87045-121">Vous pouvez créer automatiquement un contrat service ou un devis contrat pour des articles de service déjà enregistrés dans d'autres contrats de service ou devis contrat à l'aide de l'action **Copier document**.</span><span class="sxs-lookup"><span data-stu-id="87045-121">You can automatically create a service contract or contract quote for service items that are already registered in other service contracts or contract quotes by using the **Copy Document** action.</span></span>  
  
## <a name="creating-service-orders-for-multiple-contracts"></a><span data-ttu-id="87045-122">Création de commandes service pour plusieurs contrats</span><span class="sxs-lookup"><span data-stu-id="87045-122">Creating Service Orders for Multiple Contracts</span></span>  
<span data-ttu-id="87045-123">Vous pouvez manuellement créer une commande service pour un article de service qui est enregistré dans plusieurs contrats actifs.</span><span class="sxs-lookup"><span data-stu-id="87045-123">You can manually create a service order for a service item that is registered in multiple active contracts.</span></span> <span data-ttu-id="87045-124">Un contrat service est actif lorsqu'il est signé et non expiré.</span><span class="sxs-lookup"><span data-stu-id="87045-124">A service contract is active when it is signed and not expired.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="87045-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87045-125">See Also</span></span>  
[<span data-ttu-id="87045-126">Exécution des contrats de service</span><span class="sxs-lookup"><span data-stu-id="87045-126">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)  
[<span data-ttu-id="87045-127">Créer commande service</span><span class="sxs-lookup"><span data-stu-id="87045-127">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
