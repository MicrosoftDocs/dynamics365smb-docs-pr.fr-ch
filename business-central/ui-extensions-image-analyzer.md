---
title: Utilisation de l'extension d'analyseur Image | Microsoft Docs
description: Cette extension vous permet d'analyser des photos des contacts et des articles permettant de rechercher des attributs, afin de les trouver rapidement dans Business Central.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: 803d755a7caa470b97bf606f0f8916d0135d047e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821351"
---
# <a name="the-image-analyzer-extension"></a><span data-ttu-id="30067-103">Extension d'analyseur Image</span><span class="sxs-lookup"><span data-stu-id="30067-103">The Image Analyzer Extension</span></span>
<span data-ttu-id="30067-104">L'extension d'analyseur Image utilise les analyses d'image puissantes fournies par l'API Vision par ordinateur de Microsoft Cognitive Services pour détecter des attributs dans les images que vous importez pour des articles et des contacts, afin de les examiner et de les affecter facilement.</span><span class="sxs-lookup"><span data-stu-id="30067-104">The Image Analyzer extension uses powerful image analytics provided by the Computer Vision API for Microsoft Cognitive Services to detect attributes in the images that you import for items and contact persons, so you can easily review and assign them.</span></span> <span data-ttu-id="30067-105">Pour les articles, les attributs peuvent être si l'article est une table ou une voiture et, s'il est rouge ou bleu.</span><span class="sxs-lookup"><span data-stu-id="30067-105">For items, attributes could be whether the item is a table or a car, and whether it is red or blue.</span></span> <span data-ttu-id="30067-106">Pour les contacts, les attributs peuvent être le sexe ou l'âge.</span><span class="sxs-lookup"><span data-stu-id="30067-106">For contact persons, attributes can be gender or age.</span></span>

<span data-ttu-id="30067-107">L'analyseur Image propose des attributs basés sur des balises trouvées par l'API Vision par ordinateur et un niveau de confiance.</span><span class="sxs-lookup"><span data-stu-id="30067-107">Image Analyzer suggests attributes based on tags that the Computer Vision API finds, and a confidence level.</span></span> <span data-ttu-id="30067-108">Par défaut, il propose des attributs uniquement s'il est sûr à au moins 80 % que l'attribut est correct.</span><span class="sxs-lookup"><span data-stu-id="30067-108">By default, it suggests attributes only if it is at least 80% sure that the attribute is correct.</span></span> <span data-ttu-id="30067-109">Vous pouvez définir un autre niveau de confiance, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="30067-109">You can set another confidence level, if needed.</span></span> <span data-ttu-id="30067-110">Pour en savoir plus sur la manière dont les balises et le niveau de confiance sont déterminés, voir [API Vision par ordinateur](https://go.microsoft.com/fwlink/?linkid=851476).</span><span class="sxs-lookup"><span data-stu-id="30067-110">To learn more about how the tags and confidence level are determined, see [Computer Vision API](https://go.microsoft.com/fwlink/?linkid=851476).</span></span>  

<span data-ttu-id="30067-111">L'analyseur Image est gratuit dans [!INCLUDE[d365fin](includes/d365fin_md.md)], mais il existe une limite au nombre d'articles que vous pouvez analyser pendant une période donnée.</span><span class="sxs-lookup"><span data-stu-id="30067-111">Image Analyzer is free in [!INCLUDE[d365fin](includes/d365fin_md.md)], but there is a limit to the number of items that you can analyze during a certain period of time.</span></span> <span data-ttu-id="30067-112">Par défaut, vous pouvez analyser 100 images par mois.</span><span class="sxs-lookup"><span data-stu-id="30067-112">By default, you can analyze 100 images per month.</span></span>

<span data-ttu-id="30067-113">Après avoir activé l'extension, l'analyseur Image fonctionne chaque fois que vous importez une image à un article ou à un contact.</span><span class="sxs-lookup"><span data-stu-id="30067-113">After you enable the extension, Image Analyzer runs each time you import an image to an item or contact person.</span></span> <span data-ttu-id="30067-114">Vous pourrez consulter les attributs, le niveau de confiance et les détails immédiatement, et décider de gérer chaque attribut.</span><span class="sxs-lookup"><span data-stu-id="30067-114">You will see the attributes, confidence level, and details right away, and can decide what to do with each attribute.</span></span> <span data-ttu-id="30067-115">Si vous avez importé des images avant d'activer l'extension d'analyseur Image, vous devez consulter la fiche article ou contact et choisir l'action **Analyser l'image**.</span><span class="sxs-lookup"><span data-stu-id="30067-115">If you imported images before you enabled the Image Analyzer extension, you must go to the item or contact cards and choose the **Analyze Picture** action.</span></span>  

## <a name="privacy-notice"></a><span data-ttu-id="30067-116">Déclaration de confidentialité</span><span class="sxs-lookup"><span data-stu-id="30067-116">Privacy Notice</span></span>
<span data-ttu-id="30067-117">Cette extension utilise l'API Vision par ordinateur de Microsoft Cognitive Services, qui peut avoir différents niveaux d'engagements en matière de conformité par rapport à [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="30067-117">This extension uses the Computer Vision API from Microsoft Cognitive Services, which may have varying levels of compliance commitments than [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="30067-118">Lorsque vous activez l'extension Analyseur Image, les données client telles qu'une image de contact ou une image d'article sont envoyées à l'API Vision par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="30067-118">When you enable the Image Analyzer extension, Customer Data such as a contact image or an item image will be sent to the Computer Vision API.</span></span> <span data-ttu-id="30067-119">En installant cette extension, vous acceptez que cet ensemble limité de données soit envoyé à l'API Vision par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="30067-119">By installing this extension you agree for this limited set of data to be sent to the Computer Vision API.</span></span> <span data-ttu-id="30067-120">Notez que vous pouvez désactiver et désinstaller l'extension Analyseur Image à tout moment pour ne plus utiliser cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="30067-120">Note that you may disable, as well as uninstall, the Image Analyzer extension at any time to discontinue use of this functionality.</span></span> <span data-ttu-id="30067-121">Pour plus d'informations, voir [Centre de gestion de la confidentialité Microsoft](https://go.microsoft.com/fwlink/?linkid=851463).</span><span class="sxs-lookup"><span data-stu-id="30067-121">For more information, see [Microsoft Trust Center](https://go.microsoft.com/fwlink/?linkid=851463).</span></span>

## <a name="requirements"></a><span data-ttu-id="30067-122">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="30067-122">Requirements</span></span>
<span data-ttu-id="30067-123">Certaines exigences s'appliquent aux images :</span><span class="sxs-lookup"><span data-stu-id="30067-123">There are a few requirements for the images:</span></span>

* <span data-ttu-id="30067-124">Formats des images : JPEG, PNG, GIF, BMP</span><span class="sxs-lookup"><span data-stu-id="30067-124">Image formats: JPEG, PNG, GIF, BMP</span></span>  
* <span data-ttu-id="30067-125">Taille maxi. de fichier : inférieure à 4 Mo</span><span class="sxs-lookup"><span data-stu-id="30067-125">Maximum file size: Less than 4 MB</span></span>  
* <span data-ttu-id="30067-126">Dimensions des images : supérieure à 50 x 50 pixels</span><span class="sxs-lookup"><span data-stu-id="30067-126">Image dimensions: Greater than 50 x 50 pixels</span></span>  

## <a name="to-enable-image-analyzer"></a><span data-ttu-id="30067-127">Pour activer l'analyseur Image</span><span class="sxs-lookup"><span data-stu-id="30067-127">To enable Image Analyzer</span></span>
<span data-ttu-id="30067-128">L'extension d'analyseur Image est intégrée à [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="30067-128">The Image Analyzer extension is built-in to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="30067-129">Vous devez juste l'activer.</span><span class="sxs-lookup"><span data-stu-id="30067-129">You just need to turn it on.</span></span>

> [!NOTE]  
> <span data-ttu-id="30067-130">Pour activer l'extension d'analyseur Image, vous devez être un administrateur.</span><span class="sxs-lookup"><span data-stu-id="30067-130">To enable the Image Analyzer extension, you must be an administrator.</span></span> <span data-ttu-id="30067-131">Assurez-vous que vous disposez de l'ensemble d'autorisations d'utilisateur **SUPER**.</span><span class="sxs-lookup"><span data-stu-id="30067-131">Make sure that you are assigned the **SUPER** user permission set.</span></span>

1. <span data-ttu-id="30067-132">Pour activer l'extension d'analyseur Image, effectuez l'une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="30067-132">To enable the Image Analyzer extension, do one of the following:</span></span>

* <span data-ttu-id="30067-133">Ouvrez une fiche Article ou Contact.</span><span class="sxs-lookup"><span data-stu-id="30067-133">Open an item or contact card.</span></span> <span data-ttu-id="30067-134">Dans la barre de notification, choisissez **Analyser les images**, puis suivez la procédure du guide de configuration assistée.</span><span class="sxs-lookup"><span data-stu-id="30067-134">In the notification bar, choose **Analyze Images**, and then follow the steps in the assisted setup guide.</span></span>  
* <span data-ttu-id="30067-135">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Connexions au service**, puis sélectionnez **Paramètres d'analyse de l'image**.</span><span class="sxs-lookup"><span data-stu-id="30067-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Connections**, and then choose **Image Analysis Setup**.</span></span> <span data-ttu-id="30067-136">Activez la case à cocher **Activer l'analyseur Image**, puis suivez la procédure du guide de configuration assistée.</span><span class="sxs-lookup"><span data-stu-id="30067-136">Choose the **Enable Image Analyzer** check box, and then complete the steps in the assisted setup guide.</span></span>  

    > [!TIP]  
    > <span data-ttu-id="30067-137">La page **Configuration de l’analyse de l’image** vous permet également de modifier le degré de confiance des suggestions d'attribut.</span><span class="sxs-lookup"><span data-stu-id="30067-137">The **Image Analysis Setup** page is also where you can change the degree of confidence for attribute suggestions.</span></span> <span data-ttu-id="30067-138">Par exemple, si vous souhaitez avoir besoin d'un niveau de confiance supérieur, vous pouvez saisir un pourcentage plus élevé.</span><span class="sxs-lookup"><span data-stu-id="30067-138">For example, if you want to require a greater degree of confidence, you can enter a higher percentage.</span></span>

## <a name="to-analyze-an-image-of-an-item"></a><span data-ttu-id="30067-139">Pour analyser la photo d'un article</span><span class="sxs-lookup"><span data-stu-id="30067-139">To analyze an image of an item</span></span>
<span data-ttu-id="30067-140">Les étapes suivantes décrivent comment analyser une image importée avant que vous ayez activé l'extension d'analyseur Image.</span><span class="sxs-lookup"><span data-stu-id="30067-140">The following steps describe how to analyze an image that was imported before you enabled the Image Analyzer extension.</span></span>  

1. <span data-ttu-id="30067-141">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="30067-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="30067-142">Sélectionnez l'article, puis cliquez sur **Analyser l'image**.</span><span class="sxs-lookup"><span data-stu-id="30067-142">Choose the item, and then choose the **Analyze Picture** action.</span></span>  
3. <span data-ttu-id="30067-143">La page **Attributs d'analyseur Image** affiche les attributs détectés, le niveau de confiance, et d'autres détails sur l'attribut.</span><span class="sxs-lookup"><span data-stu-id="30067-143">The **Image Analyzer Attributes** page displays the detected attributes, the confidence level, and other details about the attribute.</span></span> <span data-ttu-id="30067-144">Utilisez les options **Action à effectuer** pour définir quelle action exécuter avec l'attribut.</span><span class="sxs-lookup"><span data-stu-id="30067-144">Use the **Action to perform** options to specify what to do with the attribute.</span></span>  

    > [!TIP]  
    > <span data-ttu-id="30067-145">Vous pouvez ajouter le nom de l'attribut à la description de l'article en choisissant **Ajouter à la description de l'article**.</span><span class="sxs-lookup"><span data-stu-id="30067-145">You can add the name of the attribute to the item description by choosing **Add to item description**.</span></span> <span data-ttu-id="30067-146">Par exemple, cela peut être utile pour ajouter rapidement un détail.</span><span class="sxs-lookup"><span data-stu-id="30067-146">For example, this can be useful for quickly adding detail.</span></span>  

## <a name="to-analyze-a-picture-of-a-contact-person"></a><span data-ttu-id="30067-147">Pour analyser la photo d'un contact</span><span class="sxs-lookup"><span data-stu-id="30067-147">To analyze a picture of a contact person</span></span>
<span data-ttu-id="30067-148">Les étapes suivantes décrivent comment analyser une image importée avant que vous ayez activé l'extension d'analyseur Image.</span><span class="sxs-lookup"><span data-stu-id="30067-148">The following steps describe how to analyze an image that was imported before you enabled the Image Analyzer extension.</span></span>  

1. <span data-ttu-id="30067-149">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Contacts**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="30067-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Contacts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="30067-150">Sélectionnez le contact, puis cliquez sur **Analyser l'image**.</span><span class="sxs-lookup"><span data-stu-id="30067-150">Choose the contact person, and then choose the **Analyze Picture** action.</span></span>  
3. <span data-ttu-id="30067-151">Sur le raccourci **Questionnaire profil**, consultez les suggestions, et faites des corrections si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="30067-151">On the **Profile Questionnaire** FastTab, review the suggestions, and make corrections if needed.</span></span>  

## <a name="blacklisting-suggested-attributes"></a><span data-ttu-id="30067-152">Placement des attributs suggérés sur la liste noire</span><span class="sxs-lookup"><span data-stu-id="30067-152">Blacklisting suggested attributes</span></span>
<span data-ttu-id="30067-153">Si l'analyse suggère un attribut que vous ne souhaitez pas voir, vous pouvez le mettre sur la liste noire.</span><span class="sxs-lookup"><span data-stu-id="30067-153">If the analysis suggests an attribute that you do not want to see you can blacklist the attribute.</span></span> <span data-ttu-id="30067-154">Faites attention, cependant.</span><span class="sxs-lookup"><span data-stu-id="30067-154">Use caution, however.</span></span> <span data-ttu-id="30067-155">Les attributs mis sur la liste noire ne sont pas proposés pour d'autres articles ou contacts.</span><span class="sxs-lookup"><span data-stu-id="30067-155">Blacklisted attributes are not suggested for other items or contact persons either.</span></span> <span data-ttu-id="30067-156">Si vous regrettez d'avoir placé un attribut sur la liste noire, vous pouvez choisir **Attributs mis sur la liste noire**, puis supprimer l'attribut de la liste.</span><span class="sxs-lookup"><span data-stu-id="30067-156">If you regret blacklisting an attribute, you can choose **Blacklisted Attributes**, and then delete the attribute from the list.</span></span>

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a><span data-ttu-id="30067-157">Pour utiliser vôtre propre compte pour l'API Vision par ordinateur</span><span class="sxs-lookup"><span data-stu-id="30067-157">To use your own account for the Computer Vision API</span></span>
<span data-ttu-id="30067-158">Vous pouvez également utiliser votre propre compte pour l'API Vision par ordinateur, par exemple, si vous souhaitez analyser plus d'images qu'autorisé.</span><span class="sxs-lookup"><span data-stu-id="30067-158">You can also use your own account for the Computer Vision API, for example, if you want to analyze more images than we allow.</span></span>  

1. <span data-ttu-id="30067-159">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration de l'analyseur Image**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="30067-159">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Image Analyzer Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="30067-160">Entrez l'**URI d'API** et la **clé d'API** que vous avez reçus pour l'API Vision par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="30067-160">Enter the **API URI** and **API Key** that you received for Computer Vision API.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="30067-161">Vous devez ajouter **/analyze** à la fin de l'URI d'API, si ce n'est pas déjà le cas.</span><span class="sxs-lookup"><span data-stu-id="30067-161">You must add **/analyze** at the end of the API URI, if it isn't already there.</span></span> <span data-ttu-id="30067-162">Par exemple : ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```</span><span class="sxs-lookup"><span data-stu-id="30067-162">For example: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.</span></span>

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a><span data-ttu-id="30067-163">Pour visualiser le nombre d'analyses restant pour la période en cours</span><span class="sxs-lookup"><span data-stu-id="30067-163">To see how many analyses you have left in the current period</span></span>
<span data-ttu-id="30067-164">Vous pouvez afficher le nombre d'analyses effectué, et le nombre restant, pour la période actuelle.</span><span class="sxs-lookup"><span data-stu-id="30067-164">You can view the number of analyses you've done, and how many you can still do, in the current period.</span></span>  

1. <span data-ttu-id="30067-165">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration de l'analyseur Image**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="30067-165">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Image Analyzer Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="30067-166">**Type limite**, **Valeur limite** et **Analyses effectuées** vous fournissent des informations sur l'utilisation.</span><span class="sxs-lookup"><span data-stu-id="30067-166">The **Limit type**, **Limit value**, and **Analyzes performed** provide the usage information.</span></span>  

## <a name="to-stop-using-the-image-analyzer-extension"></a><span data-ttu-id="30067-167">Pour arrêter d'utiliser l'extension d'analyseur Image</span><span class="sxs-lookup"><span data-stu-id="30067-167">To stop using the Image Analyzer extension</span></span>
1. <span data-ttu-id="30067-168">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Connexions au service**, puis sélectionnez **Configuration de l'analyseur Image**.</span><span class="sxs-lookup"><span data-stu-id="30067-168">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Connections**, and then choose **Image Analyzer Setup**.</span></span>  
2. <span data-ttu-id="30067-169">Désactivez la case à cocher **Activer l'analyseur Image**.</span><span class="sxs-lookup"><span data-stu-id="30067-169">Clear the **Enable Image Analyzer** check box.</span></span>  

## <a name="see-also"></a><span data-ttu-id="30067-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30067-170">See Also</span></span>
[<span data-ttu-id="30067-171">Utiliser les attributs d'article</span><span class="sxs-lookup"><span data-stu-id="30067-171">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
<span data-ttu-id="30067-172">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="30067-172">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="30067-173">Mise en route</span><span class="sxs-lookup"><span data-stu-id="30067-173">Getting Started</span></span>](product-get-started.md)  