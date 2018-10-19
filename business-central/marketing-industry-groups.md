---
title: "Paramétrer des secteurs d'activité pour des sociétés contact| Microsoft Docs"
description: "Décrit comment définir un secteur d'activité et l'affecter à une société contact, par exemple, le marché de détail ou l'industrie automobile."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f1927938bc7e882902d8f609242c529e0ba29cd1
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-industry-groups-for-contact-companies"></a><span data-ttu-id="040ad-103">Configurer des secteurs d'activité pour des sociétés contact</span><span class="sxs-lookup"><span data-stu-id="040ad-103">Set Up Industry Groups for Contact Companies</span></span>
<span data-ttu-id="040ad-104">Les secteurs d'activité vous permettent d'indiquer le type de secteur auquel vos contacts appartiennent, par exemple la grande distribution et l'industrie automobile.</span><span class="sxs-lookup"><span data-stu-id="040ad-104">You use industry groups to indicate the type of industry to which your contacts belong, for example, the retail industry or the automobile industry.</span></span>

<span data-ttu-id="040ad-105">L'utilisation secteurs d'activité sur les contacts est un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="040ad-105">Using industry groups on contacts is a two-step process.</span></span> <span data-ttu-id="040ad-106">Tout d'abord, vous définissez le code secteur d'activité.</span><span class="sxs-lookup"><span data-stu-id="040ad-106">First, you define the industry group code.</span></span> <span data-ttu-id="040ad-107">Vous ne devez effectuer cette étape qu'une seule fois pour chaque secteur d'activité.</span><span class="sxs-lookup"><span data-stu-id="040ad-107">You only have to perform this step one time for each industry group.</span></span> <span data-ttu-id="040ad-108">Une fois que vous disposez d'un code secteur d'activité, vous pouvez commencer à affecter le code aux sociétés contact.</span><span class="sxs-lookup"><span data-stu-id="040ad-108">Once you have an industry group code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="040ad-109">Si vous souhaitez synchroniser vos contacts avec des fournisseurs, des clients ou des comptes bancaires dans d'autres parties de l'application, vous pouvez configurer une relation d'affaires.</span><span class="sxs-lookup"><span data-stu-id="040ad-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-an-industry-group-code"></a><span data-ttu-id="040ad-110">Pour définir un code secteur d'activité</span><span class="sxs-lookup"><span data-stu-id="040ad-110">To define an industry group code</span></span>
<span data-ttu-id="040ad-111">Le code secteur d'activité définit le type ou la catégorie du groupe, par exemple PUB pour la publicité, ou PRESSE pour la télévision et la radio.</span><span class="sxs-lookup"><span data-stu-id="040ad-111">The industry group code defines the type or category of the group, such as ADVERT for advertising, or PRESS, for TV and radio.</span></span> <span data-ttu-id="040ad-112">Vous pouvez disposer de plusieurs codes secteur d'activité.</span><span class="sxs-lookup"><span data-stu-id="040ad-112">You can have several industry group codes.</span></span> <span data-ttu-id="040ad-113">Pour définir les secteurs d'activité, utilisez la fenêtre **Secteurs d'activité**.</span><span class="sxs-lookup"><span data-stu-id="040ad-113">To define the industry groups, you use the **Industry Groups** window.</span></span>

1. <span data-ttu-id="040ad-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Secteurs d'activité**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="040ad-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Industry Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="040ad-115">Sélectionnez l'action **Nouveau**, et entrez un code et une désignation.</span><span class="sxs-lookup"><span data-stu-id="040ad-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="040ad-116">Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.</span><span class="sxs-lookup"><span data-stu-id="040ad-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignIndustryGroupContact"></a> <span data-ttu-id="040ad-117">Pour affecter des secteurs d'activité à un contact</span><span class="sxs-lookup"><span data-stu-id="040ad-117">To assign industry groups to a contact</span></span>
<span data-ttu-id="040ad-118">Vous ne pouvez pas affecter de secteurs d'activité à une personne contact, mais uniquement à des sociétés.</span><span class="sxs-lookup"><span data-stu-id="040ad-118">You cannot assign industry groups to a contact person - only companies.</span></span>

1. <span data-ttu-id="040ad-119">Ouvrez le contact.</span><span class="sxs-lookup"><span data-stu-id="040ad-119">Open the contact.</span></span>
2. <span data-ttu-id="040ad-120">Sélectionnez l'action **Société**, puis l'action **Secteurs d'activité**.</span><span class="sxs-lookup"><span data-stu-id="040ad-120">Choose the **Company** action, and then the **Industry Groups** action.</span></span> <span data-ttu-id="040ad-121">La fenêtre **Secteur d'activité contact** s'affiche.</span><span class="sxs-lookup"><span data-stu-id="040ad-121">The **Contact Industry Groups** window opens.</span></span>
3. <span data-ttu-id="040ad-122">Dans le champ **Code secteurs d'activité**, sélectionnez le secteur d'activité à affecter.</span><span class="sxs-lookup"><span data-stu-id="040ad-122">In the **Industry Groups Code** field, select the industry groups you want to assign.</span></span>

<span data-ttu-id="040ad-123">Répétez ces étapes pour chaque secteur d'activité à affecter.</span><span class="sxs-lookup"><span data-stu-id="040ad-123">Repeat these steps to assign as many industry groups as you want.</span></span> <span data-ttu-id="040ad-124">Vous pouvez également affecter des secteurs d'activité à partir de la liste des contacts en suivant la même procédure.</span><span class="sxs-lookup"><span data-stu-id="040ad-124">You can also assign industry groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="040ad-125">Le nombre de secteurs d'activité que vous avez affectés au contact s'affiche dans le champ **Nbre secteurs d'activité** de la section **Segmentation** de la fenêtre **Contact**.</span><span class="sxs-lookup"><span data-stu-id="040ad-125">The number of industry groups that you have assigned to the contact is displayed in the **No. of Industry Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="040ad-126">Une fois que vous avez affecté des secteurs d'activité à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments.</span><span class="sxs-lookup"><span data-stu-id="040ad-126">After you have assigned industry groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="040ad-127">Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="040ad-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="040ad-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="040ad-128">See Also</span></span>
[<span data-ttu-id="040ad-129">Création de sociétés contact</span><span class="sxs-lookup"><span data-stu-id="040ad-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="040ad-130">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="040ad-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

