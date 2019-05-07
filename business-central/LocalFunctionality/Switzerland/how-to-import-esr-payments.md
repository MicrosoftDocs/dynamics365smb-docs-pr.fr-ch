---
title: 'Procédure : Importer des paiements ESR'
description: Après avoir reçu le paiement d'un client, vous recevez un fichier contenant des informations sur les factures payées. Vous pouvez recevoir ce fichier de votre banque par voie électronique, ou par courrier électronique.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e2646bd97589ed96d40a7fd4a58bd79351020d12
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "922132"
---
# <a name="import-esr-payments"></a><span data-ttu-id="be11c-104">Importer des paiements ESR</span><span class="sxs-lookup"><span data-stu-id="be11c-104">Import ESR Payments</span></span>
<span data-ttu-id="be11c-105">Après avoir reçu le paiement d'un client, vous recevez un fichier contenant des informations sur les factures payées.</span><span class="sxs-lookup"><span data-stu-id="be11c-105">After you receive payment from a customer, you receive a file that contains information about paid invoices.</span></span> <span data-ttu-id="be11c-106">Vous pouvez recevoir ce fichier de votre banque par voie électronique, ou par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="be11c-106">You can receive this file from your bank electronically, or by mail.</span></span>  

<span data-ttu-id="be11c-107">Vous pouvez importer les données de facture Einzahlungsschein mit Referenznummer (ESR) issues du fichier, imprimer les données en utilisant l'état ESR de la facture de vente ou le rapport de coupon ESR des ventes, et les vérifier avant de les valider.</span><span class="sxs-lookup"><span data-stu-id="be11c-107">You can import the Einzahlungsschein mit Referenznummer (ESR) invoice data from the file, print the data by using the sales invoice ESR report or the sales ESR coupon report, and verify before posting.</span></span> <span data-ttu-id="be11c-108">Pour plus d'informations, reportez-vous à [Imprimer des factures ESR](how-to-print-esr-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="be11c-108">For more information, see [Print ESR Invoices](how-to-print-esr-invoices.md).</span></span>  

## <a name="to-import-esr-payments"></a><span data-ttu-id="be11c-109">Pour importer des paiements ESR</span><span class="sxs-lookup"><span data-stu-id="be11c-109">To import ESR payments</span></span>  

1.  <span data-ttu-id="be11c-110">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles règlement**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="be11c-110">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cash Receipt Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="be11c-111">Dans le champ **Nom de la feuille**, sélectionnez le nom de feuille comptabilité requis.</span><span class="sxs-lookup"><span data-stu-id="be11c-111">In the **Batch Name** field, select the required journal batch.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="be11c-112">La feuille doit être vide avant l'importation du fichier ESR.</span><span class="sxs-lookup"><span data-stu-id="be11c-112">The journal must be empty before you import the ESR file.</span></span> <span data-ttu-id="be11c-113">Vous ne pouvez pas importer plusieurs fichiers ESR dans la même feuille règlement.</span><span class="sxs-lookup"><span data-stu-id="be11c-113">You cannot import more than one ESR file into the same cash receipt journal.</span></span>  

3.  <span data-ttu-id="be11c-114">Choisissez l'action **Lire le fichier ESR**.</span><span class="sxs-lookup"><span data-stu-id="be11c-114">Choose the **Read ESR File** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="be11c-115">Si vous avez défini plusieurs banques ESR, un message d'avertissement s'affiche pour vous inviter à choisir la banque concernée.</span><span class="sxs-lookup"><span data-stu-id="be11c-115">If you have defined more than one ESR bank, a warning message displays instructing you to choose the relevant bank.</span></span> <span data-ttu-id="be11c-116">Pour plus d'informations, voir la table Configuration ESR.</span><span class="sxs-lookup"><span data-stu-id="be11c-116">For more information, see the ESR Setup table.</span></span>  

4.  <span data-ttu-id="be11c-117">Cliquez sur le bouton **Oui**, puis sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="be11c-117">Choose the **Yes** button, and then choose the **OK** button.</span></span>  

<span data-ttu-id="be11c-118">Les informations sur le paiement sont importées vers les lignes feuille.</span><span class="sxs-lookup"><span data-stu-id="be11c-118">The payments information is imported to the journal lines.</span></span> <span data-ttu-id="be11c-119">Les paiements sont automatiquement appliqués aux factures respectives selon des numéros de référence ESR uniques.</span><span class="sxs-lookup"><span data-stu-id="be11c-119">The payments are automatically applied to the respective invoices according to unique ESR reference numbers.</span></span>  

## <a name="see-also"></a><span data-ttu-id="be11c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be11c-120">See Also</span></span>  
 <span data-ttu-id="be11c-121">[Paiements électroniques à l'aide de ESR+, Suisse](swiss-electronic-payments-using-esr.md) </span><span class="sxs-lookup"><span data-stu-id="be11c-121">[Swiss Electronic Payments Using ESR](swiss-electronic-payments-using-esr.md) </span></span>  
 [<span data-ttu-id="be11c-122">Imprimer des factures ESR</span><span class="sxs-lookup"><span data-stu-id="be11c-122">Print ESR Invoices</span></span>](how-to-print-esr-invoices.md)
