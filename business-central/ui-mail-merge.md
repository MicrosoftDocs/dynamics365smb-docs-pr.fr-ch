---
title: Utilisation de modèles Word pour les communications en masse | Microsoft Docs
description: Les modèles Word peuvent faciliter la création groupée de documents personnalisés pour des entités spécifiques.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d29e29eca7dfc24ded51aed994ac7003fb4d30ab
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110969"
---
# <a name="using-word-templates-for-bulk-communication"></a><span data-ttu-id="73ce4-103">Utilisation de modèles Word pour la communication en masse</span><span class="sxs-lookup"><span data-stu-id="73ce4-103">Using Word Templates for Bulk Communication</span></span>
<span data-ttu-id="73ce4-104">Les modèles Microsoft Word peuvent faciliter la communication de masse avec des entités telles que les clients et les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="73ce4-104">Microsoft Word templates can make it easier to mass communicate with entities such as customers and vendors.</span></span> <span data-ttu-id="73ce4-105">Par exemple, vous pouvez créer des brochures pour alerter les clients sur une campagne de vente, des lettres pour informer les fournisseurs d'une nouvelle politique d'achat ou des invitations à attirer des contacts pour un événement à venir.</span><span class="sxs-lookup"><span data-stu-id="73ce4-105">For example, you can create brochures to alert customers about a sales campaign, letters to inform vendors about a new purchasing policy, or invitations to attract contacts to an upcoming event.</span></span>

> [!NOTE]
> <span data-ttu-id="73ce4-106">Vous pouvez utiliser les modèles Word uniquement sur les appareils avec Microsoft Word 2019 et sur lesquels le système d’exploitation Windows est installé.</span><span class="sxs-lookup"><span data-stu-id="73ce4-106">You can use Word templates only on devices with Microsoft Word 2019 and the Windows operating system installed.</span></span>

<span data-ttu-id="73ce4-107">Vous pouvez utiliser des entités dans [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données pour le modèle et ajouter des champs de fusion pour personnaliser les documents pour chaque entité.</span><span class="sxs-lookup"><span data-stu-id="73ce4-107">You can use entities in [!INCLUDE[prod_short](includes/prod_short.md)] as the data source for the template, and add merge fields to personalize documents for each entity.</span></span> <span data-ttu-id="73ce4-108">Les champs de fusion proviennent de l'entité dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="73ce4-108">The merge fields come from the entity in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="73ce4-109">Lorsque vous appliquez un modèle Word à une entité, les données des champs de fusion sont insérées dans le document.</span><span class="sxs-lookup"><span data-stu-id="73ce4-109">When you apply a Word template to an entity, data from the merge fields is inserted in the document.</span></span>

<span data-ttu-id="73ce4-110">Sur la page **Modèles Word**, vous pouvez utiliser un guide de configuration assistée pour télécharger un fichier ZIP contenant un DataSource.txt et un fichier de modèle Word pour une entité.</span><span class="sxs-lookup"><span data-stu-id="73ce4-110">On the **Word Templates** page, you can use an assisted setup guide to download a ZIP file that contains a DataSource.txt and a Word template file for an entity.</span></span> <span data-ttu-id="73ce4-111">Après avoir configuré le modèle et ajouté des champs de fusion, vous utilisez le même guide pour charger le modèle.</span><span class="sxs-lookup"><span data-stu-id="73ce4-111">After you set up the template and add merge fields, you use the same guide to upload the template.</span></span> <span data-ttu-id="73ce4-112">Vous ne pouvez utiliser que le modèle Word et les fichiers de source de données que vous téléchargez à partir de [!INCLUDE[prod_short](includes/prod_short.md)] et vous devez stocker les fichiers au même emplacement.</span><span class="sxs-lookup"><span data-stu-id="73ce4-112">You can only use the Word template and data source files that you download from [!INCLUDE[prod_short](includes/prod_short.md)], and you must store the files in the same location.</span></span>

> [!NOTE]
> <span data-ttu-id="73ce4-113">Lorsque vous choisissez une entité pour laquelle créer un modèle, la liste affiche toutes les entités dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="73ce4-113">When you choose an entity for which to create a template, the list shows all entities in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="73ce4-114">Cependant, vous ne pouvez pas créer de modèles pour toutes les entités.</span><span class="sxs-lookup"><span data-stu-id="73ce4-114">However, you cannot create templates for all entities.</span></span> <span data-ttu-id="73ce4-115">Si le nom d'une entité contient des caractères spéciaux, tels que **/**, **.**, **_**, ou **-**, vous ne pouvez pas créer de modèle pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="73ce4-115">If the name of an entity contains special characters, such as **/**, **.**, **_**, or **-**, you cannot create a template for it.</span></span> <span data-ttu-id="73ce4-116">Le nom de l'entité est indiqué dans la colonne **Légende de l'objet**.</span><span class="sxs-lookup"><span data-stu-id="73ce4-116">The name of the entity is shown in the **Object Caption** column.</span></span>

<span data-ttu-id="73ce4-117">Lorsque vous configurez le modèle dans Word, sur l'onglet **Publipostage** vous pouvez ajouter des champs de fusion en choisissant **Insérer un champ de fusion**.</span><span class="sxs-lookup"><span data-stu-id="73ce4-117">When you are setting up the template in Word, on the **Mailings** tab you can add merge fields by choosing **Insert Merge Field**.</span></span>

> [!NOTE]
> <span data-ttu-id="73ce4-118">Vous ne pouvez pas utiliser de champs de fusion si le nom du champ contient 40 caractères ou plus.</span><span class="sxs-lookup"><span data-stu-id="73ce4-118">You cannot use merge fields if the name of the field contains 40 characters or more.</span></span> <span data-ttu-id="73ce4-119">Par exemple, vous ne pouvez pas utiliser le champ Company__Information_Customs_Permit_Date car il comporte 40 caractères.</span><span class="sxs-lookup"><span data-stu-id="73ce4-119">For example, you cannot use the Company__Information_Customs_Permit_Date field because it has 40 characters.</span></span> 

<span data-ttu-id="73ce4-120">Lorsque votre modèle Word est prêt, sur la page **Modèles Word** vous pouvez choisir **Appliquer** pour générer les documents.</span><span class="sxs-lookup"><span data-stu-id="73ce4-120">When your Word template is ready, on the **Word Templates** page you can choose **Apply** to generate the documents.</span></span> <span data-ttu-id="73ce4-121">Vous pouvez créer un document contenant des sections pour chaque entité ou fractionner l'opération pour créer un document pour chaque entité.</span><span class="sxs-lookup"><span data-stu-id="73ce4-121">You can either create one document that contains sections for each entity, or split the operation to create a new document for each entity.</span></span>

## <a name="to-create-a-word-template"></a><span data-ttu-id="73ce4-122">Pour créer un modèle Word</span><span class="sxs-lookup"><span data-stu-id="73ce4-122">To create a Word template</span></span>
1. <span data-ttu-id="73ce4-123">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Modèles Word**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="73ce4-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Word Templates**, and then choose the related link.</span></span>
2. <span data-ttu-id="73ce4-124">Suivez les étapes du guide de configuration assistée.</span><span class="sxs-lookup"><span data-stu-id="73ce4-124">Follow the steps in the assisted setup guide.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="73ce4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73ce4-125">See Also</span></span>
[<span data-ttu-id="73ce4-126">Gestion des présentations d’état et de document</span><span class="sxs-lookup"><span data-stu-id="73ce4-126">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
