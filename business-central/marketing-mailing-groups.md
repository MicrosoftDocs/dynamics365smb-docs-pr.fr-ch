---
title: Configurer des groupes de distribution pour des contacts| Microsoft Docs
description: Vous pouvez utiliser les groupes distribution pour identifier les groupes contacts qui doivent recevoir les mêmes informations, par exemple, pour une campagne marketing ou une promotion.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: fb9c540819279d042685ad69c790e36e71dcfbed
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238294"
---
# <a name="set-up-mailing-groups-for-contacts"></a><span data-ttu-id="f5143-103">Configurer des groupes de distribution pour les contacts.</span><span class="sxs-lookup"><span data-stu-id="f5143-103">Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="f5143-104">Les groupes distribution vous permettent d'identifier les groupes de contacts qui doivent recevoir les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="f5143-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="f5143-105">Par exemple, vous pouvez configurer un groupe de distribution pour les contacts auxquels vous souhaitez envoyer un avis de déménagement, ou un autre groupe auquel envoyer des cadeaux pour les fêtes de fin d'année.</span><span class="sxs-lookup"><span data-stu-id="f5143-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="f5143-106">L'utilisation des groupes de distribution sur les contacts est un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="f5143-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="f5143-107">Tout d'abord, vous définissez le code groupe de distribution.</span><span class="sxs-lookup"><span data-stu-id="f5143-107">First, you define the mailing group code.</span></span> <span data-ttu-id="f5143-108">Vous ne devez effectuer cette étape qu'une seule fois pour chaque groupe de distribution.</span><span class="sxs-lookup"><span data-stu-id="f5143-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="f5143-109">Une fois que vous disposez d'un code groupe de distribution, vous pouvez commencer à affecter ce code aux sociétés contact.</span><span class="sxs-lookup"><span data-stu-id="f5143-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="f5143-110">Pour définir des codes groupe de distribution</span><span class="sxs-lookup"><span data-stu-id="f5143-110">To define mailing group codes</span></span>
<span data-ttu-id="f5143-111">Le code groupe de distribution définit le type ou la catégorie du groupe, telles que DÉMÉNAGEMENT pour un déménagement des bureaux, ou CADEAU pour le cadeau de fêtes de fin d'année.</span><span class="sxs-lookup"><span data-stu-id="f5143-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="f5143-112">Vous pouvez disposer de plusieurs codes secteur d'activité.</span><span class="sxs-lookup"><span data-stu-id="f5143-112">You can have several industry group codes.</span></span> <span data-ttu-id="f5143-113">Pour définir les groupes de distribution, utilisez la page **Groupes de distribution**.</span><span class="sxs-lookup"><span data-stu-id="f5143-113">To define the industry groups, you use the **Mailing Groups** page.</span></span>

1. <span data-ttu-id="f5143-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Groupes de distribution**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f5143-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="f5143-115">Sélectionnez l'action **Nouveau**, et entrez un code et une désignation.</span><span class="sxs-lookup"><span data-stu-id="f5143-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="f5143-116">Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.</span><span class="sxs-lookup"><span data-stu-id="f5143-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignMailGroupContact"></a> <span data-ttu-id="f5143-117">Pour affecter des groupes de distribution à un contact</span><span class="sxs-lookup"><span data-stu-id="f5143-117">To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="f5143-118">Ouvrez le contact.</span><span class="sxs-lookup"><span data-stu-id="f5143-118">Open the contact.</span></span>
2. <span data-ttu-id="f5143-119">Sélectionnez l'action **Groupes de distribution**.</span><span class="sxs-lookup"><span data-stu-id="f5143-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="f5143-120">La sur la page **Groupes distribution contact** s'affiche.</span><span class="sxs-lookup"><span data-stu-id="f5143-120">The **Contact Mailing Groups** page opens.</span></span>
3. <span data-ttu-id="f5143-121">Dans le champ **Code groupes de distribution**, sélectionnez le groupe de distribution à affecter.</span><span class="sxs-lookup"><span data-stu-id="f5143-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="f5143-122">Répétez ces étapes pour chaque groupe de distribution à affecter.</span><span class="sxs-lookup"><span data-stu-id="f5143-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="f5143-123">Vous pouvez également affecter des groupes de distribution à partir de la liste des contacts en suivant la même procédure.</span><span class="sxs-lookup"><span data-stu-id="f5143-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="f5143-124">Le nombre de groupes de distribution affectés au contact s'affiche dans le champ **Nbre groupes de distribution** de la section **Segmentation** de la page **Contact**.</span><span class="sxs-lookup"><span data-stu-id="f5143-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="f5143-125">Une fois que vous avez affecté des groupes de distribution à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments.</span><span class="sxs-lookup"><span data-stu-id="f5143-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="f5143-126">Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="f5143-126">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f5143-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5143-127">See Also</span></span>
[<span data-ttu-id="f5143-128">Création de contacts</span><span class="sxs-lookup"><span data-stu-id="f5143-128">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="f5143-129">Utilisation de Business Central</span><span class="sxs-lookup"><span data-stu-id="f5143-129">Working with Business Central</span></span>](ui-work-product.md)
