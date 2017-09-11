---
title: "Créer une fiche fournisseur pour enregistrer de nouveaux fournisseurs | Microsoft Docs"
description: "Apprendre comment créer une fiche fournisseur pour enregistrer un nouveau fournisseur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 78710d796ed73d7b4c2505f6cbb8c7d5f41d7320
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-register-new-vendors"></a><span data-ttu-id="6ed28-103">Procédure : enregistrer de nouveaux fournisseurs</span><span class="sxs-lookup"><span data-stu-id="6ed28-103">How to: Register New Vendors</span></span>
<span data-ttu-id="6ed28-104">Les fournisseurs fournissent les produits que vous vendez.</span><span class="sxs-lookup"><span data-stu-id="6ed28-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="6ed28-105">Chaque fournisseur à qui vous achetez des biens doit être enregistré en tant que fiche fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6ed28-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="6ed28-106">Avant de pouvoir enregistrer de nouveaux fournisseurs, vous devez configurer divers codes achat que vous pouvez sélectionner lorsque vous renseignez les fiches fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6ed28-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="6ed28-107">Lorsque toutes les données de base requises sont créées, vous pouvez configurer des éléments supplémentaires sur le fournisseur, comme par exemple attribuer une priorité au fournisseur à des fins de paiement et répertorier les articles que les fournisseurs peuvent fournir.</span><span class="sxs-lookup"><span data-stu-id="6ed28-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="6ed28-108">Un autre groupe de tâches de configuration consiste à enregistrer vos accords concernant les remises, les prix et les modes de règlement.</span><span class="sxs-lookup"><span data-stu-id="6ed28-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="6ed28-109">Pour plus d'informations, reportez-vous à [Définition des achats](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="6ed28-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="6ed28-110">Les fiches fournisseur contiennent les informations requises pour acheter des produits au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6ed28-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="6ed28-111">Pour plus d'informations, reportez-vous à [Procédure : enregistrer des achats](purchasing-how-record-purchases.md) et à [Procédure : enregistrer de nouveaux articles](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="6ed28-111">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md) and [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="6ed28-112">Si des modèles fournisseur existent pour différents types de fournisseurs, une fenêtre s'affiche lorsque vous créez une fiche fournisseur à partir de laquelle vous pouvez sélectionner un modèle approprié.</span><span class="sxs-lookup"><span data-stu-id="6ed28-112">If vendor templates exist for different vendor types, then a window appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="6ed28-113">Si un seul modèle fournisseur existe, les nouvelles fiches fournisseur utiliseront toujours ce modèle.</span><span class="sxs-lookup"><span data-stu-id="6ed28-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="6ed28-114">Pour créer une fiche fournisseur</span><span class="sxs-lookup"><span data-stu-id="6ed28-114">To create a new vendor card</span></span>
1. <span data-ttu-id="6ed28-115">Sur la page d'accueil, sélectionnez **Fournisseurs** pour ouvrir la liste des fournisseur existants.</span><span class="sxs-lookup"><span data-stu-id="6ed28-115">On the Home page, choose **Vendors** to open the list of existing vendors.</span></span>  
2. <span data-ttu-id="6ed28-116">Dans la fenêtre **Fournisseurs**, sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="6ed28-116">In the **Vendors** window, Choose **New**.</span></span>

    <span data-ttu-id="6ed28-117">Si plusieurs modèles de fournisseur existent, une fenêtre s'affiche et vous permet de sélectionner un modèle fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6ed28-117">If more than one vendor template exists, then a window opens from which you can select a vendor template.</span></span> <span data-ttu-id="6ed28-118">Dans ce cas, suivez les deux étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6ed28-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="6ed28-119">Dans la fenêtre **Sélectionnez un modèle pour un nouveau fournisseur**, sélectionnez le modèle que vous souhaitez utiliser pour la nouvelle fiche fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6ed28-119">In the **Select a template for a new vendor** window, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="6ed28-120">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ed28-120">Choose the **OK** button.</span></span> <span data-ttu-id="6ed28-121">Une nouvelle fiche fournisseur avec certains champs contenant les informations provenant de ce modèle s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="6ed28-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="6ed28-122">Renseignez ou modifiez les champs de la fiche fournisseur selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="6ed28-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="6ed28-123">Le fournisseur est désormais enregistré, et la fiche fournisseur est prête à être utilisée sur les documents d'achat.</span><span class="sxs-lookup"><span data-stu-id="6ed28-123">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="6ed28-124">Si vous souhaitez utiliser cette fiche fournisseur comme modèle lorsque vous créez de nouvelles fiches fournisseur, enregistrez-la comme modèle fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6ed28-124">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="6ed28-125">Pour plus d'informations, reportez-vous à la section suivantes.</span><span class="sxs-lookup"><span data-stu-id="6ed28-125">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="6ed28-126">Pour enregistrer la fiche fournisseur en tant que modèle</span><span class="sxs-lookup"><span data-stu-id="6ed28-126">To save the vendor card as a template</span></span>
1. <span data-ttu-id="6ed28-127">Dans la fenêtre **Fiche fournisseur**, sélectionnez l'action **Sauvegarder comme modèle**.</span><span class="sxs-lookup"><span data-stu-id="6ed28-127">In the **Vendor Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="6ed28-128">La fenêtre **Modèle fournisseur** s'ouvre et affiche la fiche fournisseur comme modèle.</span><span class="sxs-lookup"><span data-stu-id="6ed28-128">The **Vendor Template** window opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="6ed28-129">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="6ed28-129">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="6ed28-130">Pour réutiliser les axes analytiques dans les modèles, sélectionnez l'action **Axes analytiques**.</span><span class="sxs-lookup"><span data-stu-id="6ed28-130">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="6ed28-131">La fenêtre **Modèles axe** s'ouvre et affiche tous les codes axe qui sont définis pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6ed28-131">The **Dimension Templates** window opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="6ed28-132">Modifiez ou entrez les codes axe s'appliquant aux nouvelles fiches fournisseur créées à l'aide du modèle.</span><span class="sxs-lookup"><span data-stu-id="6ed28-132">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="6ed28-133">Lorsque vous avez terminé le nouveau modèle fournisseur, cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ed28-133">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="6ed28-134">Le modèle fournisseur est ajouté à la liste des modèles fournisseur. Vous pouvez ainsi l'utiliser pour créer des fiches fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6ed28-134">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ed28-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ed28-135">See Also</span></span>
[<span data-ttu-id="6ed28-136">Achats</span><span class="sxs-lookup"><span data-stu-id="6ed28-136">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="6ed28-137">[Procédure : enregistrer des achats](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="6ed28-137">[How to: Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="6ed28-138">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6ed28-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

