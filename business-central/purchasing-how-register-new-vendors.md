---
title: Créer une fiche fournisseur pour enregistrer de nouveaux fournisseurs | Microsoft Docs
description: Apprendre comment créer une fiche fournisseur pour enregistrer un nouveau fournisseur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4f9e1b532c223efa3ebd398bb32975805ac58171
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387789"
---
# <a name="register-new-vendors"></a><span data-ttu-id="71fe9-103">Enregistrer un nouveau fournisseur</span><span class="sxs-lookup"><span data-stu-id="71fe9-103">Register New Vendors</span></span>

<span data-ttu-id="71fe9-104">Les fournisseurs fournissent les produits que vous vendez.</span><span class="sxs-lookup"><span data-stu-id="71fe9-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="71fe9-105">Chaque fournisseur à qui vous achetez des biens doit être enregistré en tant que fiche fournisseur.</span><span class="sxs-lookup"><span data-stu-id="71fe9-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="71fe9-106">Avant de pouvoir enregistrer de nouveaux fournisseurs, vous devez configurer divers codes achat que vous pouvez sélectionner lorsque vous renseignez les fiches fournisseur.</span><span class="sxs-lookup"><span data-stu-id="71fe9-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="71fe9-107">Lorsque toutes les données de base requises sont créées, vous pouvez configurer des éléments supplémentaires sur le fournisseur, comme par exemple attribuer une priorité au fournisseur à des fins de paiement et répertorier les articles que les fournisseurs peuvent fournir.</span><span class="sxs-lookup"><span data-stu-id="71fe9-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="71fe9-108">Un autre groupe de tâches de configuration consiste à enregistrer vos accords concernant les remises, les prix et les modes de règlement.</span><span class="sxs-lookup"><span data-stu-id="71fe9-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="71fe9-109">Pour plus d’informations, reportez-vous à [Définition des achats](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="71fe9-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="71fe9-110">Les fiches fournisseur contiennent les informations requises pour acheter des produits au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="71fe9-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="71fe9-111">Pour plus d’informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md) et [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="71fe9-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="71fe9-112">Si des modèles fournisseur existent pour différents types de fournisseurs, une page s’affiche lorsque vous créez une fiche fournisseur à partir de laquelle vous pouvez sélectionner un modèle approprié.</span><span class="sxs-lookup"><span data-stu-id="71fe9-112">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="71fe9-113">Si un seul modèle fournisseur existe, les nouvelles fiches fournisseur utiliseront toujours ce modèle.</span><span class="sxs-lookup"><span data-stu-id="71fe9-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="71fe9-114">Pour créer une fiche fournisseur</span><span class="sxs-lookup"><span data-stu-id="71fe9-114">To create a new vendor card</span></span>

1. <span data-ttu-id="71fe9-115">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Fournisseurs**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="71fe9-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="71fe9-116">Sur la page **Fournisseurs**, choisissez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="71fe9-116">On the **Vendors** page, Choose **New**.</span></span>

    <span data-ttu-id="71fe9-117">Si plusieurs modèles de fournisseur existent, une page s’affiche et vous permet de sélectionner un modèle fournisseur.</span><span class="sxs-lookup"><span data-stu-id="71fe9-117">If more than one vendor template exists, then a page opens from which you can select a vendor template.</span></span> <span data-ttu-id="71fe9-118">Dans ce cas, suivez les deux étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="71fe9-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="71fe9-119">Sur la page **Sélectionnez un modèle pour un nouveau fournisseur**, sélectionnez le modèle que vous souhaitez utiliser pour la nouvelle fiche fournisseur.</span><span class="sxs-lookup"><span data-stu-id="71fe9-119">On the **Select a template for a new vendor** page, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="71fe9-120">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="71fe9-120">Choose the **OK** button.</span></span> <span data-ttu-id="71fe9-121">Une nouvelle fiche fournisseur avec certains champs contenant les informations provenant de ce modèle s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="71fe9-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="71fe9-122">Renseignez ou modifiez les champs de la fiche fournisseur selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="71fe9-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="71fe9-123">Si vous ne connaissez pas l’adresse de facturation qui sera utilisée pour chaque facture fournisseur, ne renseignez pas le champ **N° fournisseur**.</span><span class="sxs-lookup"><span data-stu-id="71fe9-123">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Vendor No.** field.</span></span> <span data-ttu-id="71fe9-124">Sélectionnez plutôt le numéro du fournisseur à payer après avoir configuré une demande de prix, une commande ou un en-tête facture.</span><span class="sxs-lookup"><span data-stu-id="71fe9-124">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="71fe9-125">Le fournisseur est désormais enregistré, et la fiche fournisseur est prête à être utilisée sur les documents d’achat.</span><span class="sxs-lookup"><span data-stu-id="71fe9-125">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="71fe9-126">Si vous souhaitez utiliser cette fiche fournisseur comme modèle lorsque vous créez de nouvelles fiches fournisseur, enregistrez-la comme modèle fournisseur.</span><span class="sxs-lookup"><span data-stu-id="71fe9-126">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="71fe9-127">Pour plus d’informations, reportez-vous à la section suivante.</span><span class="sxs-lookup"><span data-stu-id="71fe9-127">For more information, see the following section.</span></span>

### <a name="deleting-vendor-cards"></a><span data-ttu-id="71fe9-128">Suppression de cartes de fournisseur</span><span class="sxs-lookup"><span data-stu-id="71fe9-128">Deleting Vendor Cards</span></span>
<span data-ttu-id="71fe9-129">Si vous avez enregistré une transaction pour un fournisseur, vous ne pouvez pas supprimer la carte car les écritures comptables peuvent être nécessaires pour l’audit.</span><span class="sxs-lookup"><span data-stu-id="71fe9-129">If you have posted a transaction for a vendor, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="71fe9-130">Pour supprimer des fiches fournisseur avec des écritures comptables, contactez le partenaire Microsoft pour le faire via le code.</span><span class="sxs-lookup"><span data-stu-id="71fe9-130">To delete vendor cards with ledger entries, contact to Microsoft partner to do so through code.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="71fe9-131">Pour enregistrer la fiche fournisseur en tant que modèle</span><span class="sxs-lookup"><span data-stu-id="71fe9-131">To save the vendor card as a template</span></span>
1. <span data-ttu-id="71fe9-132">Sur la page **Fiche fournisseur**, sélectionnez l’action **Sauvegarder comme modèle**.</span><span class="sxs-lookup"><span data-stu-id="71fe9-132">On the **Vendor Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="71fe9-133">La page **Modèle fournisseur** s’ouvre et affiche la fiche fournisseur comme modèle.</span><span class="sxs-lookup"><span data-stu-id="71fe9-133">The **Vendor Template** page opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="71fe9-134">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="71fe9-134">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="71fe9-135">Pour réutiliser les axes analytiques dans les modèles, sélectionnez l’action **Axes analytiques**.</span><span class="sxs-lookup"><span data-stu-id="71fe9-135">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="71fe9-136">La page **Modèles axe** s’ouvre et affiche tous les codes axe qui sont définis pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="71fe9-136">The **Dimension Templates** page opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="71fe9-137">Modifiez ou entrez les codes axe s’appliquant aux nouvelles fiches fournisseur créées à l’aide du modèle.</span><span class="sxs-lookup"><span data-stu-id="71fe9-137">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="71fe9-138">Lorsque vous avez terminé le nouveau modèle fournisseur, cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="71fe9-138">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="71fe9-139">Le modèle fournisseur est ajouté à la liste des modèles fournisseur. Vous pouvez ainsi l’utiliser pour créer des fiches fournisseur.</span><span class="sxs-lookup"><span data-stu-id="71fe9-139">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="71fe9-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71fe9-140">See Also</span></span>
[<span data-ttu-id="71fe9-141">Fusionner l’enregistrement des doublons</span><span class="sxs-lookup"><span data-stu-id="71fe9-141">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="71fe9-142">Création des souches de numéros</span><span class="sxs-lookup"><span data-stu-id="71fe9-142">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="71fe9-143">Achats</span><span class="sxs-lookup"><span data-stu-id="71fe9-143">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="71fe9-144">[Enregistrer des achats](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="71fe9-144">[Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="71fe9-145">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="71fe9-145">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]