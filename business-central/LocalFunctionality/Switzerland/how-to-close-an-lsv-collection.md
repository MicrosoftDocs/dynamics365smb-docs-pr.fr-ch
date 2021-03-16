---
title: 'Procédure : Fermer un prélèvement LSV'
description: Vous devez fermer les collections Lastschrift Verfahren (LSV+) pour écrire les fichiers LSV qui peuvent être envoyés à la banque pour le prélèvement des paiements. Lorsque vous fermez un prélèvement, le prélèvement est terminé et les validations dans la feuille LSV sont combinées.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2e9cc07dc1afd328472008d3f2e5e902bba90bef
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384006"
---
# <a name="close-an-lsv-collection"></a><span data-ttu-id="f3070-104">Fermer prélèvement LSV</span><span class="sxs-lookup"><span data-stu-id="f3070-104">Close an LSV Collection</span></span>
<span data-ttu-id="f3070-105">Vous devez fermer les collections Lastschrift Verfahren (LSV+) pour écrire les fichiers LSV qui peuvent être envoyés à la banque pour le prélèvement des paiements.</span><span class="sxs-lookup"><span data-stu-id="f3070-105">You must close Lastschrift Verfahren (LSV+) collections to write LSV files that can be sent to the bank for payment collection.</span></span> <span data-ttu-id="f3070-106">Lorsque vous fermez un prélèvement, le prélèvement est terminé et les validations dans la feuille LSV sont combinées.</span><span class="sxs-lookup"><span data-stu-id="f3070-106">When you close a collection, the collection is complete, and the postings in the LSV journal are combined.</span></span>  

<span data-ttu-id="f3070-107">Lorsque le prélèvement est terminé, le numéro de prélèvement actuel est affecté dans la feuille LSV, en fonction du dernier prélèvement.</span><span class="sxs-lookup"><span data-stu-id="f3070-107">When the collection is complete, the current collection number is assigned in the LSV journal, based on the last collection.</span></span> <span data-ttu-id="f3070-108">Ce numéro LSV est transféré vers les écritures client pour toutes les factures ouvertes.</span><span class="sxs-lookup"><span data-stu-id="f3070-108">This LSV number is transferred to the customer entries for all outstanding invoices.</span></span> <span data-ttu-id="f3070-109">Le fichier de prélèvement peut être reconstruit à tout moment en utilisant le numéro LSV.</span><span class="sxs-lookup"><span data-stu-id="f3070-109">The collection file can be reconstructed at any time using the LSV number.</span></span> <span data-ttu-id="f3070-110">Le champ **En attente** est également renseigné avec **LSV** dans les écritures client pour éviter de dupliquer des écritures ouvertes.</span><span class="sxs-lookup"><span data-stu-id="f3070-110">The **On Hold** field is also populated with **LSV** in the customer entries to avoid the duplication of open entries.</span></span> <span data-ttu-id="f3070-111">Pour plus d'informations, voir la table **Feuille LSV** et la table **Écriture comptable client**.</span><span class="sxs-lookup"><span data-stu-id="f3070-111">For more information, see the **LSV Journal** table and the **Cust. Ledger Entry** table.</span></span> <span data-ttu-id="f3070-112">Vous pouvez également rouvrir un prélèvement clôturé.</span><span class="sxs-lookup"><span data-stu-id="f3070-112">You can also reopen a closed collection.</span></span>  

## <a name="to-close-an-lsv-collection"></a><span data-ttu-id="f3070-113">Pour fermer un prélèvement LSV</span><span class="sxs-lookup"><span data-stu-id="f3070-113">To close an LSV collection</span></span>  

1.  <span data-ttu-id="f3070-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Liste feuilles LSV**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f3070-114">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **LSV Journal List**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f3070-115">Sélectionnez la ligne feuille requise, puis sélectionnez l'action **Modifier la date comptabilisation**.</span><span class="sxs-lookup"><span data-stu-id="f3070-115">Select the required journal line, and then choose the **Modify Posting Date** action.</span></span> <span data-ttu-id="f3070-116">La valeur du champ **Date de crédit** à l'aide de la valeur suggérée lors du prélèvement LSV.</span><span class="sxs-lookup"><span data-stu-id="f3070-116">This will modify the value in the **Credit Date** field by using the value suggested during the LSV collection.</span></span>  
3.  <span data-ttu-id="f3070-117">Dans le champ **Nouvelle date**, saisissez la nouvelle date.</span><span class="sxs-lookup"><span data-stu-id="f3070-117">In the **New Date** field, enter the new date.</span></span>  
4.  <span data-ttu-id="f3070-118">Choisissez \*l'action \*Clôturer le prélèvement\*\*.</span><span class="sxs-lookup"><span data-stu-id="f3070-118">Choose the **Close Collection* action*.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f3070-119">Les champs du raccourci **Options** pour le traitement par lots **Prélèvement de fin LSV** ne peuvent pas être modifiés, et correspondent à la ligne feuille sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="f3070-119">The fields on the **Options** FastTab for the **LSV Close Collection** batch job cannot be modified, and correspond to the selected journal line.</span></span>  

5.  <span data-ttu-id="f3070-120">Choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3070-120">Choose the **OK** button.</span></span>  

    <span data-ttu-id="f3070-121">Dans la page **Liste feuilles LSV**, la valeur du champ **Statut LSV** passe de **Modifier** à **Lancé**.</span><span class="sxs-lookup"><span data-stu-id="f3070-121">On the **LSV Journal List** page, the value in the **LSV Status** field is changed from **Edit** to **Released**.</span></span> <span data-ttu-id="f3070-122">Les lignes feuille ne peuvent plus être modifiées.</span><span class="sxs-lookup"><span data-stu-id="f3070-122">The journal lines can no longer be modified.</span></span>  

## <a name="to-reopen-an-lsv-collection"></a><span data-ttu-id="f3070-123">Pour rouvrir un prélèvement LSV</span><span class="sxs-lookup"><span data-stu-id="f3070-123">To reopen an LSV collection</span></span>  

1.  <span data-ttu-id="f3070-124">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Liste feuilles LSV**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f3070-124">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **LSV Journal List**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f3070-125">Sélectionnez la ligne feuille appropriée pour laquelle vous voulez rouvrir le prélèvement, choisissez l'action **Rouvrir le prélèvement**.</span><span class="sxs-lookup"><span data-stu-id="f3070-125">Select the required journal line for which you want to reopen the collection, on then choose the **Reopen Collection** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f3070-126">Vous ne pouvez rouvrir le prélèvement que si vous n'avez pas encore envoyé le fichier LSV+ à la banque.</span><span class="sxs-lookup"><span data-stu-id="f3070-126">You can only reopen the collection if you have not yet submitted the LSV+ file to the bank.</span></span>  

3.  <span data-ttu-id="f3070-127">Choisissez le bouton **Oui** pour confirmer la réouverture du prélèvement.</span><span class="sxs-lookup"><span data-stu-id="f3070-127">Choose the **Yes** button to confirm the reopening of the collection.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f3070-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3070-128">See Also</span></span>  
 <span data-ttu-id="f3070-129">[Paiements électroniques à l'aide de LSV+, Suisse](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="f3070-129">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 <span data-ttu-id="f3070-130">[Traiter un prélèvement LSV](how-to-process-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="f3070-130">[Process an LSV Collection](how-to-process-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="f3070-131">[Valider des paiements LSV+](how-to-post-lsv-payments.md) </span><span class="sxs-lookup"><span data-stu-id="f3070-131">[Post LSV+ Payments](how-to-post-lsv-payments.md) </span></span>  
 [<span data-ttu-id="f3070-132">Exporter des paiements en mode LSV</span><span class="sxs-lookup"><span data-stu-id="f3070-132">Export Payments Using LSV</span></span>](how-to-export-payments-using-lsv.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]