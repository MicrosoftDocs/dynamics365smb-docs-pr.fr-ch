---
title: "Définir les codes des relations d'affaires dans les contacts| Microsoft Docs"
description: "Utilisez les relations d'affaires dans Financials pour vous aider avec le marketing et désigner les rapports établis avec vos prospects, clients, notamment les banques ou les prestataires de services."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7d0f189ac233ea4da72136858a343dfaa7e88883
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-business-relations-on-contact-companies"></a><span data-ttu-id="56a5c-103">Configuration des relations d'affaires sur des sociétés contact</span><span class="sxs-lookup"><span data-stu-id="56a5c-103">Setting Up Business Relations on Contact Companies</span></span>
<span data-ttu-id="56a5c-104">Les relations d'affaires vous permettent d'indiquer les rapports établis avec vos contacts, tels que les prospects, les banques, les consultants, les prestataires de services, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="56a5c-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="56a5c-105">L'utilisation des relations d'affaires sur les contacts processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="56a5c-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="56a5c-106">Tout d'abord, vous définissez le code relation d'affaires.</span><span class="sxs-lookup"><span data-stu-id="56a5c-106">First, you define the business relation code.</span></span> <span data-ttu-id="56a5c-107">Vous ne devez effectuer cette étape qu'une seule fois pour chaque relation d'affaires.</span><span class="sxs-lookup"><span data-stu-id="56a5c-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="56a5c-108">Une fois que vous disposez d'un code relation d'affaires, vous pouvez commencer à affecter le code aux sociétés contact.</span><span class="sxs-lookup"><span data-stu-id="56a5c-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="56a5c-109">Si vous souhaitez synchroniser vos contacts avec des fournisseurs, des clients ou des comptes bancaires dans d'autres parties de l'application, vous pouvez configurer une relation d'affaires.</span><span class="sxs-lookup"><span data-stu-id="56a5c-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="56a5c-110">Pour définir un code relation d'affaires</span><span class="sxs-lookup"><span data-stu-id="56a5c-110">To define a business relation code</span></span>
<span data-ttu-id="56a5c-111">Le code relation d'affaires définit une catégorie ou un type de relation d'affaires, telles que BANQUE ou Avocat.</span><span class="sxs-lookup"><span data-stu-id="56a5c-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="56a5c-112">Vous pouvez disposer de plusieurs codes relation d'affaires.</span><span class="sxs-lookup"><span data-stu-id="56a5c-112">You can have several business relation codes.</span></span> <span data-ttu-id="56a5c-113">Pour définir la relation d'affaires, vous utilisez la fenêtre **Relations d'affaires**.</span><span class="sxs-lookup"><span data-stu-id="56a5c-113">To define the business relation, you use the **Business Relations** window.</span></span>

1. <span data-ttu-id="56a5c-114">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Relations d'affaires**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="56a5c-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="56a5c-115">Sélectionnez l'action **Nouveau**, et entrez un code et une désignation.</span><span class="sxs-lookup"><span data-stu-id="56a5c-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="56a5c-116">Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.</span><span class="sxs-lookup"><span data-stu-id="56a5c-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="56a5c-117"><a name="AssignBusRelContact"></a> Pour affecter des relations d'affaires à un contact</span><span class="sxs-lookup"><span data-stu-id="56a5c-117"><a name="AssignBusRelContact"></a> To assign business relations to a contact</span></span>
<span data-ttu-id="56a5c-118">Vous ne pouvez pas affecter de relations d'affaires à un individu, mais uniquement à des sociétés.</span><span class="sxs-lookup"><span data-stu-id="56a5c-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="56a5c-119">Ouvrez le contact.</span><span class="sxs-lookup"><span data-stu-id="56a5c-119">Open the contact.</span></span>
2. <span data-ttu-id="56a5c-120">Sélectionnez l'action **Société**, puis l'action **Relations d'affaires**.</span><span class="sxs-lookup"><span data-stu-id="56a5c-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="56a5c-121">La fenêtre **Relations d'affaires contact** s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="56a5c-121">The **Contact Business Relations** window opens.</span></span>
3. <span data-ttu-id="56a5c-122">Dans le champ **Code relation d'affaires**, sélectionnez la relation d'affaires à affecter.</span><span class="sxs-lookup"><span data-stu-id="56a5c-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="56a5c-123">Répétez ces étapes pour chaque relation d'affaires à affecter.</span><span class="sxs-lookup"><span data-stu-id="56a5c-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="56a5c-124">Vous pouvez également affecter des relations d'affaires à partir de la liste des contacts en suivant la même procédure.</span><span class="sxs-lookup"><span data-stu-id="56a5c-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="56a5c-125">Le nombre de relations d'affaires que vous avez affectées au contact s'affiche dans le champ **Nbre relations d'affaires** de la section **Segmentation** de la fenêtre **Contact**.</span><span class="sxs-lookup"><span data-stu-id="56a5c-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="56a5c-126">Une fois que vous avez affecté des relations d'affaires à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments.</span><span class="sxs-lookup"><span data-stu-id="56a5c-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="56a5c-127">Pour plus d'informations, reportez-vous à [Procédure : ajouter des contacts à des segments](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="56a5c-127">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="56a5c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56a5c-128">See Also</span></span>
[<span data-ttu-id="56a5c-129">Création de sociétés contact</span><span class="sxs-lookup"><span data-stu-id="56a5c-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="56a5c-130">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="56a5c-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

