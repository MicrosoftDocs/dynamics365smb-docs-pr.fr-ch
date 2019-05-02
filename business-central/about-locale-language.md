---
title: Fonctionnalité multilingue et localisation | Microsoft Docs
description: Découvrez comment la langue et les paramètres régionaux influencent votre expérience dans Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture
ms.date: 11/19/2018
ms.author: edupont
ms.openlocfilehash: 218b1b825501d64bef9d65640f922e690df3108f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821115"
---
# <a name="changing-language-and-locale"></a><span data-ttu-id="0142a-103">Modification de la langue et des paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="0142a-103">Changing Language and Locale</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="0142a-104">est pris en charge dans plusieurs marchés et est disponible dans les langues requises par ces marchés.</span><span class="sxs-lookup"><span data-stu-id="0142a-104">is supported in a number of markets and available in the languages that those markets require.</span></span> <span data-ttu-id="0142a-105">Cela résulte de la prise en charge de plusieurs langues au moment de l'exécution, en plus de la prise en charge des exigences légales dans les marchés pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0142a-105">This is a result of support for multiple languages at runtime in combination with support for legal requirements in the supported markets.</span></span> <span data-ttu-id="0142a-106">Cela signifie que [!INCLUDE[d365fin](includes/d365fin_md.md)] peut être affiché en plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="0142a-106">This means that [!INCLUDE[d365fin](includes/d365fin_md.md)] can present itself in different languages.</span></span> <span data-ttu-id="0142a-107">Vous pouvez modifier la langue utilisée pour l'affichage des textes et ce changement est immédiat une fois que le système vous a déconnecté et reconnecté automatiquement.</span><span class="sxs-lookup"><span data-stu-id="0142a-107">You can change the language that is used to display texts, and the change is immediate, once you have been automatically signed out and in again.</span></span> <span data-ttu-id="0142a-108">Le paramètre ne s'applique qu'à vous et non aux autres utilisateurs de votre société.</span><span class="sxs-lookup"><span data-stu-id="0142a-108">The setting applies to you and not to everyone else in your company.</span></span>  

<span data-ttu-id="0142a-109">Par exemple, si vous utilisez la version canadienne de [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez afficher l'interface utilisateur en anglais et en français, mais pour tous les autres aspects de l'application, il s'agit toujours de la version canadienne de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0142a-109">For example, if you are using the Canadian version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can see the user interface in English and in French, but it is still the Canadian version of [!INCLUDE[d365fin](includes/d365fin_md.md)] in all other aspects.</span></span> <span data-ttu-id="0142a-110">Elle diffère, par exemple, de la version de [!INCLUDE[d365fin](includes/d365fin_md.md)] destinée au Royaume-Uni.</span><span class="sxs-lookup"><span data-stu-id="0142a-110">It is not the same as, say, [!INCLUDE[d365fin](includes/d365fin_md.md)] in the United Kingdom.</span></span>  

<span data-ttu-id="0142a-111">Pour modifier la langue de l'interface utilisateur, accédez à la page **Mes paramètres**.</span><span class="sxs-lookup"><span data-stu-id="0142a-111">To change the language of the user interface, go to the **My Settings** page.</span></span> <span data-ttu-id="0142a-112">Pour plus d'informations, voir [Modification des paramètres de base](ui-change-basic-settings.md#language).</span><span class="sxs-lookup"><span data-stu-id="0142a-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md#language).</span></span>  

<span data-ttu-id="0142a-113">La modification des textes stockés sous forme de données d'application n'appartient pas à la fonctionnalité multilingue.</span><span class="sxs-lookup"><span data-stu-id="0142a-113">Changing the texts that are stored as application data is not part of the multilanguage capability.</span></span> <span data-ttu-id="0142a-114">C'est une question de conception de l'application.</span><span class="sxs-lookup"><span data-stu-id="0142a-114">This is an application design issue.</span></span> <span data-ttu-id="0142a-115">Il s'agit par exemple de textes tels que le nom des articles du stock ou les commentaires concernant un client.</span><span class="sxs-lookup"><span data-stu-id="0142a-115">Examples of such texts are the names of items in the inventory or the comments for a customer.</span></span> <span data-ttu-id="0142a-116">En d'autres termes, ces types de texte ne sont pas traduits.</span><span class="sxs-lookup"><span data-stu-id="0142a-116">In other words, these types of text are not translated.</span></span>  

> [!NOTE]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="0142a-117">ne prend en charge qu'un jeu de caractères unique pour les données.</span><span class="sxs-lookup"><span data-stu-id="0142a-117">only supports a single character set for data.</span></span> <span data-ttu-id="0142a-118">Aussi, il se peut que certains caractères ne soient pas pris en charge dans votre abonné et vous pouvez rencontrer des problèmes de récupération des données saisies à l'aide d'un autre jeu de caractères.</span><span class="sxs-lookup"><span data-stu-id="0142a-118">Therefore some characters may not be supported in your tenant, and you may experience problems when retrieving data that was entered using a different character set.</span></span> <span data-ttu-id="0142a-119">Par exemple, votre abonné peut ne prendre en charge que les caractères anglais et russes, et si vous entrez des données dans une autre langue, elles peuvent ne pas être stockées correctement.</span><span class="sxs-lookup"><span data-stu-id="0142a-119">For instance, your tenant may support only English and Russian characters and if you enter data in a different language, it may not be stored correctly.</span></span> <span data-ttu-id="0142a-120">Vous devez contacter votre administrateur système pour connaître les langues prises en charge pour votre client [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0142a-120">You should contact your system administrator to make sure you understand which languages are supported for your [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="changing-the-locale"></a><span data-ttu-id="0142a-121">Modification des paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="0142a-121">Changing the Locale</span></span>
<span data-ttu-id="0142a-122">Les paramètres régionaux diffèrent des exigences linguistiques et légales des marchés locaux.</span><span class="sxs-lookup"><span data-stu-id="0142a-122">Locale is different from both language and legal requirements in local markets.</span></span> <span data-ttu-id="0142a-123">Les paramètres régionaux déterminent la manière dont vos données s'affichent en termes de séparateur de virgule, aligné à gauche ou à droite, et certains autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="0142a-123">Locale determines how your data presents itself in terms of comma separator, aligned to the left or to the right, and certain other settings.</span></span> <span data-ttu-id="0142a-124">Les paramètres régionaux déterminent également certains éléments du système dans le navigateur, par exemple l'action permettant de créer un élément dans une liste.</span><span class="sxs-lookup"><span data-stu-id="0142a-124">The locale also determines some of the system elements in the browser, such as the action to create a new item in a list, for example.</span></span>  

<span data-ttu-id="0142a-125">Vous pouvez modifier les paramètres régionaux dans l'onglet du navigateur que vous utilisez pour travailler dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0142a-125">You can change the locale in the browser tab that you are using to work in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0142a-126">Les modifications ne s'appliquent qu'à vous et non aux autres utilisateurs de votre société.</span><span class="sxs-lookup"><span data-stu-id="0142a-126">the change applies only to you and not to the other users in your company.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="0142a-127">Lorsque vous modifiez les paramètres régionaux, une longue liste de langues et de paramètres régionaux s'affiche.</span><span class="sxs-lookup"><span data-stu-id="0142a-127">When you change the locale, you will see a long list of languages and locales.</span></span> <span data-ttu-id="0142a-128">Toutefois, seuls les paramètres régionaux sont utilisés dans la version actuelle de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0142a-128">However, only the locale setting is used in the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="0142a-129">Pour modifier les paramètres régionaux, accédez à la page **Mes paramètres**.</span><span class="sxs-lookup"><span data-stu-id="0142a-129">To change the locale, go to the **My Settings** page.</span></span> <span data-ttu-id="0142a-130">Pour plus d'informations, voir [Modification des paramètres de base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="0142a-130">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

## <a name="languages-of-the-included365finincludesd365finmdmd-help"></a><span data-ttu-id="0142a-131">Langues de l'aide de [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="0142a-131">Languages of the [!INCLUDE[d365fin](includes/d365fin_md.md)] Help</span></span>
<span data-ttu-id="0142a-132">Le contenu de l'aide pour la fonctionnalité de base de [!INCLUDE[d365fin](includes/d365fin_md.md)] est publié sur le site de Microsoft Docs et est disponible dans de nombreuses langues différentes.</span><span class="sxs-lookup"><span data-stu-id="0142a-132">The Help content for the core functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] publishes to the Microsoft Docs site and available in a number of different languages.</span></span> <span data-ttu-id="0142a-133">Si vous accédez aux documents au sein de [!INCLUDE[d365fin](includes/d365fin_md.md)], le contenu s'affichera dans votre langue.</span><span class="sxs-lookup"><span data-stu-id="0142a-133">If you access the docs from inside [!INCLUDE[d365fin](includes/d365fin_md.md)], the content will display in your language.</span></span> <span data-ttu-id="0142a-134">Si une page spécifique n'est pas encore disponible dans votre langue, elle s'affichera en anglais.</span><span class="sxs-lookup"><span data-stu-id="0142a-134">If a particular page is not available in your language yet, it will be shown in English.</span></span>

### <a name="how-do-i-change-the-language"></a><span data-ttu-id="0142a-135">Comment puis-je modifier la langue ?</span><span class="sxs-lookup"><span data-stu-id="0142a-135">How Do I Change the Language?</span></span>
<span data-ttu-id="0142a-136">C'est simple - accédez au bas de la page du navigateur et choisissez le symbole de globe dans le coin inférieur gauche.</span><span class="sxs-lookup"><span data-stu-id="0142a-136">It's simple - scroll to the bottom of the browser page and choose the globe symbol in the bottom left corner.</span></span>

> [!NOTE]  
> <span data-ttu-id="0142a-137">La liste indique toutes les langues qui sont prises en charge par le site Microsoft Docs.</span><span class="sxs-lookup"><span data-stu-id="0142a-137">The list shows all languages that are supported by the Microsoft Docs site.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="0142a-138">est disponible dans un nombre limité de pays/régions, mais le contenu de l'aide est disponible dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="0142a-138">is available in a limited number of countries/regions, but the Help content is made available in more languages.</span></span> <span data-ttu-id="0142a-139">Toutefois, le contenu de l'aide n'est pas disponible dans toutes les langues prises en charge par le site Microsoft Docs.</span><span class="sxs-lookup"><span data-stu-id="0142a-139">However, the Help content is not available in all languages that the Microsoft Docs site supports.</span></span>

## <a name="see-also"></a><span data-ttu-id="0142a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0142a-140">See Also</span></span>  
[<span data-ttu-id="0142a-141">Modification des paramètres de base</span><span class="sxs-lookup"><span data-stu-id="0142a-141">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="0142a-142">Mise en route</span><span class="sxs-lookup"><span data-stu-id="0142a-142">Getting Started</span></span>](product-get-started.md)  