---
title: Définir les codes des relations d'affaires dans les contacts| Microsoft Docs
description: Utilisez les relations d'affaires dans Business Central pour vous aider avec le marketing et désigner les rapports établis avec vos prospects, clients, notamment les banques ou les prestataires de services.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: cb600ea688a856f481d84604d6966231fe7f536d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821008"
---
# <a name="setting-up-business-relations-on-contacts"></a><span data-ttu-id="8cd52-103">Configuration des relations d'affaires sur des contacts</span><span class="sxs-lookup"><span data-stu-id="8cd52-103">Setting Up Business Relations on Contacts</span></span>
<span data-ttu-id="8cd52-104">Les relations d'affaires vous permettent d'indiquer les rapports établis avec vos contacts, tels que les prospects, les banques, les consultants, les prestataires de services, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="8cd52-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="8cd52-105">L'utilisation des relations d'affaires sur les contacts processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="8cd52-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="8cd52-106">Tout d'abord, vous définissez le code relation d'affaires.</span><span class="sxs-lookup"><span data-stu-id="8cd52-106">First, you define the business relation code.</span></span> <span data-ttu-id="8cd52-107">Vous ne devez effectuer cette étape qu'une seule fois pour chaque relation d'affaires.</span><span class="sxs-lookup"><span data-stu-id="8cd52-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="8cd52-108">Une fois que vous disposez d'un code relation d'affaires, vous pouvez commencer à affecter le code aux sociétés contact.</span><span class="sxs-lookup"><span data-stu-id="8cd52-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="8cd52-109">Si vous souhaitez synchroniser vos contacts avec des fournisseurs, des clients ou des comptes bancaires dans d'autres parties de l'application, vous pouvez configurer une relation d'affaires.</span><span class="sxs-lookup"><span data-stu-id="8cd52-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="8cd52-110">Pour définir un code relation d'affaires</span><span class="sxs-lookup"><span data-stu-id="8cd52-110">To define a business relation code</span></span>
<span data-ttu-id="8cd52-111">Le code relation d'affaires définit une catégorie ou un type de relation d'affaires, telles que BANQUE ou Avocat.</span><span class="sxs-lookup"><span data-stu-id="8cd52-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="8cd52-112">Vous pouvez disposer de plusieurs codes relation d'affaires.</span><span class="sxs-lookup"><span data-stu-id="8cd52-112">You can have several business relation codes.</span></span> <span data-ttu-id="8cd52-113">Pour définir la relation d'affaires, vous utilisez la page **Relations d'affaires**.</span><span class="sxs-lookup"><span data-stu-id="8cd52-113">To define the business relation, you use the **Business Relations** page.</span></span>

1. <span data-ttu-id="8cd52-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Relations d'affaires**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="8cd52-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="8cd52-115">Sélectionnez l'action **Nouveau**, et entrez un code et une désignation.</span><span class="sxs-lookup"><span data-stu-id="8cd52-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="8cd52-116">Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.</span><span class="sxs-lookup"><span data-stu-id="8cd52-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignBusRelContact"></a> <span data-ttu-id="8cd52-117">Pour affecter des relations d'affaires à un contact</span><span class="sxs-lookup"><span data-stu-id="8cd52-117">To assign business relations to a contact</span></span>
<span data-ttu-id="8cd52-118">Vous ne pouvez pas affecter de relations d'affaires à un individu, mais uniquement à des sociétés.</span><span class="sxs-lookup"><span data-stu-id="8cd52-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="8cd52-119">Ouvrez le contact.</span><span class="sxs-lookup"><span data-stu-id="8cd52-119">Open the contact.</span></span>
2. <span data-ttu-id="8cd52-120">Sélectionnez l'action **Société**, puis l'action **Relations d'affaires**.</span><span class="sxs-lookup"><span data-stu-id="8cd52-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="8cd52-121">La page **Relations d'affaires contact** s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="8cd52-121">The **Contact Business Relations** page opens.</span></span>
3. <span data-ttu-id="8cd52-122">Dans le champ **Code relation d'affaires**, sélectionnez la relation d'affaires à affecter.</span><span class="sxs-lookup"><span data-stu-id="8cd52-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="8cd52-123">Répétez ces étapes pour chaque relation d'affaires à affecter.</span><span class="sxs-lookup"><span data-stu-id="8cd52-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="8cd52-124">Vous pouvez également affecter des relations d'affaires à partir de la liste des contacts en suivant la même procédure.</span><span class="sxs-lookup"><span data-stu-id="8cd52-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="8cd52-125">Le nombre de relations d'affaires que vous avez affectées au contact s'affiche dans le champ **Nbre relations d'affaires** de la section **Segmentation** de la page **Contact**.</span><span class="sxs-lookup"><span data-stu-id="8cd52-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="8cd52-126">Une fois que vous avez affecté des relations d'affaires à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments.</span><span class="sxs-lookup"><span data-stu-id="8cd52-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="8cd52-127">Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="8cd52-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8cd52-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cd52-128">See Also</span></span>
<span data-ttu-id="8cd52-129">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8cd52-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>