---
title: Configurer des niveaux hiérarchiques pour les contacts| Microsoft Docs
description: Vous pouvez définir un niveau hiérarchique et l'affecter à vos contacts pour indiquer leur position au sein de leur société, par exemple, la direction générale.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 10/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: a3c3d33bf7ceaf2bd0f5fae4c4513b1769ed3092
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308851"
---
# <a name="set-up-organizational-levels-for-contact-persons"></a><span data-ttu-id="43a99-103">Configurer des niveaux hiérarchiques pour les personnes contact</span><span class="sxs-lookup"><span data-stu-id="43a99-103">Set Up Organizational Levels for Contact Persons</span></span>
<span data-ttu-id="43a99-104">Vous pouvez utiliser les niveaux hiérarchiques sur vos contacts pour qu'ils précisent leur position au sein de la société, par exemple, la direction générale.</span><span class="sxs-lookup"><span data-stu-id="43a99-104">You can use organizational levels on your contacts to specify which position they have in the company, for example, top management.</span></span> <span data-ttu-id="43a99-105">Vous pouvez utiliser ces informations lors de la saisie de données sur vos contacts.</span><span class="sxs-lookup"><span data-stu-id="43a99-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="43a99-106">L'utilisation de niveaux hiérarchiques sur les contacts est un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="43a99-106">Using organizational levels on contacts is a two-step process.</span></span> <span data-ttu-id="43a99-107">Tout d'abord, vous définissez le code de niveau hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="43a99-107">First, you define the organizational level code.</span></span> <span data-ttu-id="43a99-108">Vous ne devez effectuer cette étape qu'une seule fois pour niveau hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="43a99-108">You only have to perform this step one time for each organizational level.</span></span> <span data-ttu-id="43a99-109">Une fois que vous disposez d'un code de niveau hiérarchique, vous pouvez commencer à affecter ce code aux personnes contact.</span><span class="sxs-lookup"><span data-stu-id="43a99-109">Once you have an organizational level code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-an-organizational-level-code"></a><span data-ttu-id="43a99-110">Pour définir un code de niveau hiérarchique</span><span class="sxs-lookup"><span data-stu-id="43a99-110">To define an organizational level code</span></span>
<span data-ttu-id="43a99-111">Le code de niveau hiérarchique définit le type ou la catégorie du niveau hiérarchique, par exemple PDG ou DF.</span><span class="sxs-lookup"><span data-stu-id="43a99-111">The organizational level code defines the type or category of the organizational level, such a CEO  or CFO.</span></span> <span data-ttu-id="43a99-112">Vous pouvez disposer de plusieurs codes de niveau hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="43a99-112">You can have several organizational level codes.</span></span> <span data-ttu-id="43a99-113">Pour définir le niveau hiérarchique, vous utilisez la page **Niveaux organisationnels**.</span><span class="sxs-lookup"><span data-stu-id="43a99-113">To define the organizational level, you use the **Organizational Levels** page.</span></span>

1. <span data-ttu-id="43a99-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Niveaux hiérarchiques**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="43a99-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Organizational Levels**, and then choose the related link.</span></span>
2. <span data-ttu-id="43a99-115">Sélectionnez l'action **Nouveau**, et entrez un code et une désignation.</span><span class="sxs-lookup"><span data-stu-id="43a99-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="43a99-116">Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.</span><span class="sxs-lookup"><span data-stu-id="43a99-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-organizational-levels-to-a-contact-person"></a><span data-ttu-id="43a99-117">Pour affecter des niveaux hiérarchiques à une personne contact</span><span class="sxs-lookup"><span data-stu-id="43a99-117">To assign organizational levels to a contact person</span></span>
<span data-ttu-id="43a99-118">Vous pouvez affecter des niveaux hiérarchiques aux personnes contact, mais pas aux sociétés contact.</span><span class="sxs-lookup"><span data-stu-id="43a99-118">You can assign organizational levels to contact persons only, not contact companies.</span></span> <span data-ttu-id="43a99-119">Vous ne pouvez affecter qu'un niveau hiérarchique par contact.</span><span class="sxs-lookup"><span data-stu-id="43a99-119">You can only assign one organizational level to each contact.</span></span>

1. <span data-ttu-id="43a99-120">Ouvrez le contact.</span><span class="sxs-lookup"><span data-stu-id="43a99-120">Open the contact.</span></span>
2. <span data-ttu-id="43a99-121">Dans le champ **Niveaux organisationnels**, sélectionnez le code à affecter.</span><span class="sxs-lookup"><span data-stu-id="43a99-121">In the **Organizational Levels** field, select the code you want to assign.</span></span>

<span data-ttu-id="43a99-122">Une fois que vous avez affecté des niveaux hiérarchiques à vos contacts, vous pouvez utiliser ces données pour créer des segments.</span><span class="sxs-lookup"><span data-stu-id="43a99-122">After you have assigned organizational levels to your contacts, you can use this information to create segments.</span></span>

<span data-ttu-id="43a99-123">Une fois que vous avez affecté des responsabilités à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments.</span><span class="sxs-lookup"><span data-stu-id="43a99-123">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="43a99-124">Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="43a99-124">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="43a99-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43a99-125">See Also</span></span>
[<span data-ttu-id="43a99-126">Création de contacts</span><span class="sxs-lookup"><span data-stu-id="43a99-126">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="43a99-127">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="43a99-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
