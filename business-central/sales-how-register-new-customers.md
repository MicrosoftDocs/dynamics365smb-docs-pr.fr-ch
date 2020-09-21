---
title: Créer une fiche client pour enregistrer de nouveaux clients | Microsoft Docs
description: Décrit comment créer une fiche client pour enregistrer des informations sur chaque nouveau client ou client auquel vous vendez.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 06/24/2020
ms.author: edupont
ms.openlocfilehash: 3e25756cff974e0db835f5e3ed3247dff6d7624a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780900"
---
# <a name="register-new-customers"></a><span data-ttu-id="d7608-103">Enregistrer de nouveaux clients</span><span class="sxs-lookup"><span data-stu-id="d7608-103">Register New Customers</span></span>

<span data-ttu-id="d7608-104">Les clients sont l'origine de vos revenus.</span><span class="sxs-lookup"><span data-stu-id="d7608-104">Customers are the source of your income.</span></span> <span data-ttu-id="d7608-105">Chaque client auquel vous vendez un élément doit être enregistré en tant que fiche client.</span><span class="sxs-lookup"><span data-stu-id="d7608-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="d7608-106">Les fiches client contiennent les informations nécessaires à la vente de biens au client.</span><span class="sxs-lookup"><span data-stu-id="d7608-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="d7608-107">Pour plus d'informations, voir [Facturer des ventes](sales-how-invoice-sales.md) et [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="d7608-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="d7608-108">Avant de pouvoir enregistrer de nouveaux clients, vous devez configurer divers codes vente que vous pouvez sélectionner lorsque vous renseignez les fiches client.</span><span class="sxs-lookup"><span data-stu-id="d7608-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="d7608-109">Pour plus d'informations, reportez-vous à [Définition des ventes](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="d7608-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a><span data-ttu-id="d7608-110">Ajout de nouveaux clients</span><span class="sxs-lookup"><span data-stu-id="d7608-110">Adding new customers</span></span>

<span data-ttu-id="d7608-111">Pour enregistrer un nouveau client, vous devez remplir une fiche client.</span><span class="sxs-lookup"><span data-stu-id="d7608-111">To register a new customer, you must fill in a customer card.</span></span> <span data-ttu-id="d7608-112">Vous pouvez créer des modèles pour différents profils de clients ou ajouter des clients sans modèles.</span><span class="sxs-lookup"><span data-stu-id="d7608-112">You can establish templates for different customer profiles, or you can add customers without templates.</span></span>  

> [!NOTE]  
> <span data-ttu-id="d7608-113">Si des modèles client existent pour différents types de clients, une page s'affiche lorsque vous créez une nouvelle fiche client à partir de laquelle vous pouvez sélectionner un modèle client approprié.</span><span class="sxs-lookup"><span data-stu-id="d7608-113">If customer templates exist for different customer types, then a page appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="d7608-114">Si un seul modèle client existe, les nouvelles fiches client utiliseront toujours ce modèle.</span><span class="sxs-lookup"><span data-stu-id="d7608-114">If only one customer template exists, then new customer cards always use that template.</span></span>  

### <a name="to-create-a-new-customer-card"></a><span data-ttu-id="d7608-115">Pour créer une fiche client</span><span class="sxs-lookup"><span data-stu-id="d7608-115">To create a new customer card</span></span>

1. <span data-ttu-id="d7608-116">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Clients**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="d7608-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d7608-117">Sur la page **Clients**, sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="d7608-117">On the **Customers** page, choose the **New** action.</span></span>

    <span data-ttu-id="d7608-118">Si un seul modèle client existe, une nouvelle fiche client avec certains champs renseignés à l'aide des informations provenant du modèle s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="d7608-118">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="d7608-119">Si plusieurs modèles client existent, une page s'affiche et vous permet de sélectionner un modèle client.</span><span class="sxs-lookup"><span data-stu-id="d7608-119">If more than one customer template exists, then a page opens from which you can select a customer template.</span></span> <span data-ttu-id="d7608-120">Dans ce cas, suivez les deux étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7608-120">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="d7608-121">Sur la page **Sélectionnez un modèle pour un nouveau client**, sélectionnez le modèle que vous souhaitez utiliser pour la nouvelle fiche client.</span><span class="sxs-lookup"><span data-stu-id="d7608-121">On the **Select a template for a new customer** page, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="d7608-122">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7608-122">Choose the **OK** button.</span></span> <span data-ttu-id="d7608-123">Une fiche client avec certains champs contenant les informations provenant de ce modèle s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="d7608-123">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="d7608-124">Renseignez ou modifiez les champs de la fiche client selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="d7608-124">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="d7608-125">Sur le raccourci **Prix vente**, vous pouvez afficher les prix spéciaux ou les remises accordées au client si certains critères sont réunis, par exemple l'article, la quantité minimum commande ou la date de fin.</span><span class="sxs-lookup"><span data-stu-id="d7608-125">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="d7608-126">Chaque ligne représente un prix spécial ou une remise ligne.</span><span class="sxs-lookup"><span data-stu-id="d7608-126">Each row represents a special price or line discount.</span></span> <span data-ttu-id="d7608-127">Chaque colonne représente un critère qui doit s'appliquer pour garantir le prix spécial que vous saisissez dans le champ **Prix** ou la remise ligne que vous saisissez dans le champ **% remise ligne**.</span><span class="sxs-lookup"><span data-stu-id="d7608-127">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="d7608-128">Pour plus d'informations, reportez-vous à [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="d7608-128">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="d7608-129">Le client est désormais enregistré, et la fiche client est prête à être utilisée sur les documents vente.</span><span class="sxs-lookup"><span data-stu-id="d7608-129">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="d7608-130">Si vous souhaitez utiliser cette fiche client comme modèle lorsque vous créez de nouvelles fiches client, enregistrez-la comme modèle.</span><span class="sxs-lookup"><span data-stu-id="d7608-130">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="d7608-131">Pour plus d'informations, reportez-vous à la section suivante.</span><span class="sxs-lookup"><span data-stu-id="d7608-131">For more information, see the following section.</span></span>  

### <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="d7608-132">Pour enregistrer la fiche client en tant que modèle</span><span class="sxs-lookup"><span data-stu-id="d7608-132">To save the customer card as a template</span></span>

1. <span data-ttu-id="d7608-133">Sur la page **Fiche client**, sélectionnez l'action **Sauvegarder comme modèle**.</span><span class="sxs-lookup"><span data-stu-id="d7608-133">On the **Customer Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="d7608-134">La page **Modèle client** s'ouvre et affiche la fiche client comme modèle.</span><span class="sxs-lookup"><span data-stu-id="d7608-134">The **Customer Template** page opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="d7608-135">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="d7608-135">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="d7608-136">Pour réutiliser les axes analytiques dans les modèles, sélectionnez l'action **Axes analytiques**.</span><span class="sxs-lookup"><span data-stu-id="d7608-136">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="d7608-137">La page **Modèles axe** s'ouvre et affiche tous les codes axe qui sont définis pour le client.</span><span class="sxs-lookup"><span data-stu-id="d7608-137">The **Dimension Templates** page opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="d7608-138">Modifiez ou entrez les codes axe s'appliquant aux nouvelles fiches client créées à l'aide du modèle.</span><span class="sxs-lookup"><span data-stu-id="d7608-138">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="d7608-139">Lorsque vous avez terminé le nouveau modèle client, cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7608-139">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="d7608-140">Le modèle client est ajouté à la liste des modèles client. Vous pouvez ainsi l'utiliser pour créer des fiches client.</span><span class="sxs-lookup"><span data-stu-id="d7608-140">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="deleting-customer-cards"></a><span data-ttu-id="d7608-141">Suppression de fiches client</span><span class="sxs-lookup"><span data-stu-id="d7608-141">Deleting customer cards</span></span>

<span data-ttu-id="d7608-142">Si vous avez enregistré une transaction pour un client, vous ne pouvez pas supprimer la carte car les écritures comptables peuvent être nécessaires pour l'audit.</span><span class="sxs-lookup"><span data-stu-id="d7608-142">If you have posted a transaction for a customer, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="d7608-143">Pour supprimer des fiches client avec des écritures comptables, contactez le partenaire Microsoft pour le faire via le code.</span><span class="sxs-lookup"><span data-stu-id="d7608-143">To delete customer cards with ledger entries, contact to Microsoft partner to do so through code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d7608-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7608-144">See Also</span></span>

[<span data-ttu-id="d7608-145">Définition des modes de règlement</span><span class="sxs-lookup"><span data-stu-id="d7608-145">Defining Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="d7608-146">Fusionner l'enregistrement des doublons</span><span class="sxs-lookup"><span data-stu-id="d7608-146">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="d7608-147">Création des souches de numéros</span><span class="sxs-lookup"><span data-stu-id="d7608-147">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="d7608-148">Ventes</span><span class="sxs-lookup"><span data-stu-id="d7608-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="d7608-149">Définition des ventes</span><span class="sxs-lookup"><span data-stu-id="d7608-149">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="d7608-150">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d7608-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
