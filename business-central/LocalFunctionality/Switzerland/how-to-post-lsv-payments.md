---
title: 'Procédure : Valider les paiements LSV+'
description: Vous pouvez valider les paiements après avoir reçu l'avis de paiement Lastschrift Verfahren (LSV+) de la banque.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: d7646d77b5e266e58f9022f4cf9e7130e7dd0559
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "827311"
---
# <a name="post-lsv-payments"></a><span data-ttu-id="81070-103">Valider les paiements LSV+</span><span class="sxs-lookup"><span data-stu-id="81070-103">Post LSV+ Payments</span></span>
<span data-ttu-id="81070-104">Vous pouvez valider les paiements après avoir reçu l'avis de paiement Lastschrift Verfahren (LSV+) de la banque.</span><span class="sxs-lookup"><span data-stu-id="81070-104">You can post payments after you have received Lastschrift Verfahren (LSV+) payment advice from the bank.</span></span>  

## <a name="to-post-lsv-payments"></a><span data-ttu-id="81070-105">Pour valider les paiements LSV+</span><span class="sxs-lookup"><span data-stu-id="81070-105">To post LSV+ payments</span></span>  

1.  <span data-ttu-id="81070-106">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles règlement**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="81070-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cash Receipt Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="81070-107">Sélectionnez la feuille requise, puis cliquez sur l'action **Modifier journal**.</span><span class="sxs-lookup"><span data-stu-id="81070-107">Select the required journal, and then choose the **Edit Journal** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="81070-108">Vous pouvez sélectionner le nom de feuille pour LSV dans laquelle le compte contrepartie concerné est défini.</span><span class="sxs-lookup"><span data-stu-id="81070-108">You can select the journal batch for LSV where the balance account you want to address is defined.</span></span> <span data-ttu-id="81070-109">Vous ne pouvez pas importer plusieurs fichiers lignes feuille LSV dans la même feuille règlement.</span><span class="sxs-lookup"><span data-stu-id="81070-109">You cannot import more than one LSV journal line into the same cash receipt journal.</span></span> <span data-ttu-id="81070-110">Pour plus d'informations, reportez-vous à la page Feuille règlement.</span><span class="sxs-lookup"><span data-stu-id="81070-110">For more information, see the Cash Receipt Journal page.</span></span>  

3.  <span data-ttu-id="81070-111">Sélectionnez l'action **Obtenir à partir de la feuille LSV**.</span><span class="sxs-lookup"><span data-stu-id="81070-111">Choose the **Get From LSV Journal** action.</span></span>  
4.  <span data-ttu-id="81070-112">Dans la page **Liste feuilles LSV**, sélectionnez la ligne feuille LSV que vous souhaitez importer avec la feuille règlement.</span><span class="sxs-lookup"><span data-stu-id="81070-112">On the **LSV Journal List** page, select the LSV journal line that you want to import to the cash receipt journal.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="81070-113">Vous pouvez importer uniquement des lignes feuille où le champ **Statut LSV** est défini sur **Fichier créé**.</span><span class="sxs-lookup"><span data-stu-id="81070-113">You can only import journal lines where the **LSV Status** field is set to **File Created**.</span></span>  

5.  <span data-ttu-id="81070-114">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="81070-114">Choose the **OK** button.</span></span>  

    <span data-ttu-id="81070-115">La ligne feuille LSV est importée dans la feuille règlement.</span><span class="sxs-lookup"><span data-stu-id="81070-115">The LSV journal line is imported into the cash receipt journal.</span></span> <span data-ttu-id="81070-116">La valeur du champ **Statut LSV** dans la page **Liste feuilles LSV** passe de **Fichier créé** à **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="81070-116">The value in the **LSV Status** field on the **LSV Journal List** page changes from **File Created** to **Finished**.</span></span>  

    <span data-ttu-id="81070-117">Vous pouvez vérifier les paiements importés et les comparer à votre option de paiement bancaire dans la page **Feuille règlement**.</span><span class="sxs-lookup"><span data-stu-id="81070-117">You can check the imported payments, and compare them with your bank payment advice on the **Cash Receipt Journal** page.</span></span> <span data-ttu-id="81070-118">Vous pouvez également supprimer les lignes paiement qui ne peuvent pas être traitées par la banque, et pour lesquelles vous devez continuer avec le client manuellement.</span><span class="sxs-lookup"><span data-stu-id="81070-118">You can also delete the payment lines that could not be processed by the bank, and for which you must follow up with the customer manually.</span></span>  

6.  <span data-ttu-id="81070-119">Sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="81070-119">Choose the **Post** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="81070-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81070-120">See Also</span></span>  
 <span data-ttu-id="81070-121">[Paiements électroniques à l'aide de LSV+, Suisse](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="81070-121">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 <span data-ttu-id="81070-122">[Traiter un prélèvement LSV](how-to-process-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="81070-122">[Process an LSV Collection](how-to-process-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="81070-123">[Fermer prélèvement LSV](how-to-close-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="81070-123">[Close an LSV Collection](how-to-close-an-lsv-collection.md) </span></span>  
 [<span data-ttu-id="81070-124">Exporter des paiements en mode LSV</span><span class="sxs-lookup"><span data-stu-id="81070-124">Export Payments Using LSV</span></span>](how-to-export-payments-using-lsv.md) 