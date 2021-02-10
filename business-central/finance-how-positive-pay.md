---
title: Exporter des fichiers Positive Pay| Microsoft Docs
description: Vous pouvez vous assurer que la banque efface uniquement les chèques et les montants validés en exportant un fichier Positive Pay contenant des informations de paiement et fournisseur.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8856ee09ae728d685d3f57786abc29d9aca93778
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750870"
---
# <a name="export-a-positive-pay-file"></a><span data-ttu-id="c5421-103">Exporter un fichier Positive Pay</span><span class="sxs-lookup"><span data-stu-id="c5421-103">Export a Positive Pay File</span></span>
<span data-ttu-id="c5421-104">Pour vous assurer que votre banque efface uniquement les chèques et les montants validés, vous pouvez exporter un fichier Positive Pay contenant des informations fournisseur, un numéro de chèque, un montant de paiement que vous envoyez à la banque pour référence lorsque vous traitez les paiements.</span><span class="sxs-lookup"><span data-stu-id="c5421-104">To make sure that your bank only clears validated checks and amounts, you can export a Positive Pay file that contains vendor information, check number, and payment amount, which you send to the bank for reference when you process payments.</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="c5421-105">est préconfiguré pour prendre en charge les fichiers Positive Pay de la Bank of America et de la City Bank.</span><span class="sxs-lookup"><span data-stu-id="c5421-105">is preconfigured to support Positive Pay files for Bank of America and City Bank.</span></span>

## <a name="to-set-up-a-bank-account-for-positive-pay"></a><span data-ttu-id="c5421-106">Pour configurer une banque pour Positive Pay</span><span class="sxs-lookup"><span data-stu-id="c5421-106">To set up a bank account for Positive Pay</span></span>
1. <span data-ttu-id="c5421-107">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Compte bancaire**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="c5421-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="c5421-108">Ouvrez la fiche de la banque pour laquelle vous souhaitez utiliser Positive Pay.</span><span class="sxs-lookup"><span data-stu-id="c5421-108">Open the card for the bank that you want to use Positive Pay for.</span></span>
3. <span data-ttu-id="c5421-109">Dans le champ **Code exportation Positive Pay**, entrez POSPAYBANK.</span><span class="sxs-lookup"><span data-stu-id="c5421-109">In the **Positive Pay Export Code** field, enter POSPAYBANK.</span></span>
4. <span data-ttu-id="c5421-110">Fermez la page.</span><span class="sxs-lookup"><span data-stu-id="c5421-110">Close the page.</span></span>

## <a name="to-export-a-positive-pay-file"></a><span data-ttu-id="c5421-111">Pour exporter un fichier Positive Pay</span><span class="sxs-lookup"><span data-stu-id="c5421-111">To export a Positive Pay file</span></span>
1. <span data-ttu-id="c5421-112">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Comptes bancaires**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="c5421-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="c5421-113">Sélectionnez le compte bancaire pour lequel vous voulez exporter un fichier Positive Pay.</span><span class="sxs-lookup"><span data-stu-id="c5421-113">Select the bank account that you want to export a Positive Pay file for.</span></span>
3. <span data-ttu-id="c5421-114">Choisissez l’option **Exportation Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="c5421-114">Choose **Positive Pay Export** action.</span></span>

    <span data-ttu-id="c5421-115">La page **Exportation Positive Pay** s’ouvre et affiche les paiements qui ont été effectués pour le compte bancaire depuis la dernière date de téléchargement, comme indiqué dans les champs **Date dernier téléchargement** et **Heure dernier téléchargement**.</span><span class="sxs-lookup"><span data-stu-id="c5421-115">The **Positive Pay Export** page opens displaying payments that have been made for the bank account since the last upload date, as shown in the **Last Upload Date** and **Last Upload Time** fields.</span></span>
4. <span data-ttu-id="c5421-116">Dans le champ **Date limite téléchargement**, spécifiez une date avant laquelle les paiements ne sont pas inclus dans le fichier exporté.</span><span class="sxs-lookup"><span data-stu-id="c5421-116">In the **Cutoff Upload Date** field, specify a date before which payments are not included in the exported file.</span></span>
5. <span data-ttu-id="c5421-117">Sélectionnez l’option **Exporter**.</span><span class="sxs-lookup"><span data-stu-id="c5421-117">Choose the **Export** action.</span></span>
6. <span data-ttu-id="c5421-118">Sur la page **Exporter fichier**, choisissez le bouton **Enregistrer**, puis enregistrez le fichier à l’emplacement approprié.</span><span class="sxs-lookup"><span data-stu-id="c5421-118">On the **Export File** page, choose the **Save** button, and then save the file to a convenient location.</span></span>
7. <span data-ttu-id="c5421-119">Téléchargez le fichier sur votre site bancaire électronique.</span><span class="sxs-lookup"><span data-stu-id="c5421-119">Upload the file to your electronic bank site.</span></span>
8. <span data-ttu-id="c5421-120">Notez ou copiez le numéro de confirmation qui s’affiche lorsque le téléchargement du fichier est terminé.</span><span class="sxs-lookup"><span data-stu-id="c5421-120">Write down or copy the confirmation number that is displayed when the file upload is successful.</span></span>

<span data-ttu-id="c5421-121">Pour afficher les enregistrements Positive Pay exportés</span><span class="sxs-lookup"><span data-stu-id="c5421-121">To view exported Positive Pay records</span></span>

1. <span data-ttu-id="c5421-122">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Compte bancaire**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="c5421-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="c5421-123">Sélectionnez le compte bancaire pour lequel vous voulez afficher l’enregistrement d’exportation de Positive Pay.</span><span class="sxs-lookup"><span data-stu-id="c5421-123">Select the bank account that you want to view Positive Pay export records for.</span></span>
3. <span data-ttu-id="c5421-124">Choisissez l’option **Écritures Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="c5421-124">Choose the **Positive Pay Entries** action.</span></span>

    <span data-ttu-id="c5421-125">Sur la page **Écritures Positive Pay**, vous pouvez afficher tous les enregistrements d’exportation de Positive Pay pour le compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="c5421-125">On the **Positive Pay Entries** page, you can see all the Positive Pay export records for the bank account.</span></span>
4. <span data-ttu-id="c5421-126">Dans le champ **Numéro de confirmation**, entrez, pour chaque enregistrement d’exportation, le numéro de confirmation que vous recevez lorsque le téléchargement du fichier vers la banque est terminé.</span><span class="sxs-lookup"><span data-stu-id="c5421-126">In the **Confirmation Number** field, enter, for each export record, the confirmation number that you receive when the file upload to the bank is successful.</span></span>
5. <span data-ttu-id="c5421-127">Pour afficher les lignes de paiement associées, choisissez l’option **Détails écriture Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="c5421-127">To view the related payment lines, choose the **Positive Pay Entry Details** action.</span></span>

<span data-ttu-id="c5421-128">Pour réexporter les fichiers Positive Pay</span><span class="sxs-lookup"><span data-stu-id="c5421-128">To reexport Positive Pay files</span></span>

1. <span data-ttu-id="c5421-129">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Compte bancaire**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="c5421-129">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="c5421-130">Sélectionnez le compte bancaire pour lequel vous voulez réeexporter les fichiers Positive Pay.</span><span class="sxs-lookup"><span data-stu-id="c5421-130">Select the bank account that you want to reexport Positive Pay files for.</span></span>
3. <span data-ttu-id="c5421-131">Choisissez l’option **Écritures Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="c5421-131">Choose the **Positive Pay Entries** action.</span></span>
4. <span data-ttu-id="c5421-132">Sélectionnez la ligne du fichier d’exportation Positive Pay à réexporter.</span><span class="sxs-lookup"><span data-stu-id="c5421-132">Select the line for the Positive Pay export file that you want to reexport.</span></span>
5. <span data-ttu-id="c5421-133">Sur la page **Écritures Positive Pay**, choisissez l’option **Réexporter Positive Pay dans un fichier**.</span><span class="sxs-lookup"><span data-stu-id="c5421-133">On the **Positive Pay Entries** page, choose the **Reexport Positive Pay to File** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5421-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5421-134">See Also</span></span>
[<span data-ttu-id="c5421-135">Finances</span><span class="sxs-lookup"><span data-stu-id="c5421-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="c5421-136">Configuration de Finance</span><span class="sxs-lookup"><span data-stu-id="c5421-136">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="c5421-137">Utilisation de feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="c5421-137">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="c5421-138">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c5421-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
