---
title: "Configurer des recherches Web pour des sociétés contact| Microsoft Docs"
description: "Vous pouvez définir des sources Internet ou Web et les affecter à une société contact pour identifier la manière dont vous souhaitez rechercher des informations sur vos contacts."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 8106eeca31fb5a5c4528d47a27f897454d5dac58
ms.contentlocale: fr-ch
ms.lasthandoff: 12/11/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="af044-103">Configuration de recherches Web pour des sociétés contact</span><span class="sxs-lookup"><span data-stu-id="af044-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="af044-104">Vous pouvez utiliser les recherches Web avec vos sociétés contact afin d'identifier, par exemple, des moteurs de recherche et des sites Web que vous souhaitez utiliser pour rechercher des informations relatives aux contacts.</span><span class="sxs-lookup"><span data-stu-id="af044-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="af044-105">Lorsque vous affectez des recherches Web, vous spécifiez le moteur de recherche et les mots recherchés que l'application doit utiliser pour trouver les données demandées.</span><span class="sxs-lookup"><span data-stu-id="af044-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="af044-106">L'utilisation des recherches Web au niveau des contacts est un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="af044-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="af044-107">Tout d'abord, vous définissez le code recherche Web.</span><span class="sxs-lookup"><span data-stu-id="af044-107">First, you define the web source code.</span></span> <span data-ttu-id="af044-108">Vous ne devez effectuer cette étape qu'une seule fois pour chaque recherche Web.</span><span class="sxs-lookup"><span data-stu-id="af044-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="af044-109">Une fois que vous disposez d'un code recherche Web, vous pouvez commencer à affecter ce code aux personnes contact.</span><span class="sxs-lookup"><span data-stu-id="af044-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="af044-110">Pour définir un code recherche Web</span><span class="sxs-lookup"><span data-stu-id="af044-110">To define a web source code</span></span>
1. <span data-ttu-id="af044-111">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Recherche Web**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="af044-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="af044-112">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="af044-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="af044-113">Renseignez les champs **Code**, **Désignation** et **URL**.</span><span class="sxs-lookup"><span data-stu-id="af044-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="af044-114">Tapez %1 dans le champ **URL** pour insérer un espace réservé correspondant au mot recherché dans l'URL.</span><span class="sxs-lookup"><span data-stu-id="af044-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="af044-115">Lorsque vous lancez la recherche Web à partir d'un contact, le %1 est automatiquement remplacé par le mot recherché (par exemple le nom de la société) que vous avez saisi sur la page **Recherche contacts Web**.</span><span class="sxs-lookup"><span data-stu-id="af044-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered on the **Contact Web Sources** page.</span></span>

<span data-ttu-id="af044-116">Répétez ces étapes pour chaque recherche Web à configurer.</span><span class="sxs-lookup"><span data-stu-id="af044-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="af044-117">Pour affecter une recherche Web à une société contact</span><span class="sxs-lookup"><span data-stu-id="af044-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="af044-118">Lorsque vous affectez des recherches Web, vous spécifiez le moteur de recherche et les mots recherchés que l'application doit utiliser pour trouver les données demandées.</span><span class="sxs-lookup"><span data-stu-id="af044-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="af044-119">Ouvrez le contact.</span><span class="sxs-lookup"><span data-stu-id="af044-119">Open the contact.</span></span>
2. <span data-ttu-id="af044-120">Sélectionnez l'action **Société**, puis l'action **Recherche Web**.</span><span class="sxs-lookup"><span data-stu-id="af044-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="af044-121">La page **Recherche contact Web** s'affiche.</span><span class="sxs-lookup"><span data-stu-id="af044-121">The **Contact Web Sources** page opens.</span></span>
3. <span data-ttu-id="af044-122">Dans le champ **Code recherche web**, sélectionnez la recherche Web à affecter.</span><span class="sxs-lookup"><span data-stu-id="af044-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="af044-123">Dans le champ **Mot recherché**, saisissez le mot recherché à utiliser pour trouver les données.</span><span class="sxs-lookup"><span data-stu-id="af044-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="af044-124">Répétez ces étapes pour chaque recherche Web à affecter.</span><span class="sxs-lookup"><span data-stu-id="af044-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="af044-125">Vous pouvez également affecter des recherches web à partir de la page **Liste des contacts** en suivant la même procédure.</span><span class="sxs-lookup"><span data-stu-id="af044-125">You can also assign web sources from the **Contact List** page by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="af044-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af044-126">See Also</span></span>
[<span data-ttu-id="af044-127">Création de sociétés contact</span><span class="sxs-lookup"><span data-stu-id="af044-127">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="af044-128">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af044-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

