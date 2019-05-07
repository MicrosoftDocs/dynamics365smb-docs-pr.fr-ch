---
title: 'Procédure : transférer les écritures comptables vers les écritures de coûts | Microsoft Docs'
description: Vous pouvez transférer les écritures comptables aux écritures de coûts.
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
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: a33fb434cc239de951d18783911c879587a3ace0
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/16/2019
ms.locfileid: "939049"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="09146-103">Transférer les écritures comptables vers les écritures de coûts</span><span class="sxs-lookup"><span data-stu-id="09146-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="09146-104">Vous pouvez transférer les écritures comptables aux écritures de coûts.</span><span class="sxs-lookup"><span data-stu-id="09146-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="09146-105">Avant d'exécuter le transfert des écritures comptables vers des écritures de coûts, vous devez vous y préparer pour éviter toute validation manuelle de correction.</span><span class="sxs-lookup"><span data-stu-id="09146-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="09146-106">Pour préparer le transfert</span><span class="sxs-lookup"><span data-stu-id="09146-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="09146-107">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres comptabilité analytique**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="09146-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="09146-108">Sur la page **Paramètres comptabilité analytique**, vérifiez que le champ **Date début pour transfert comptabilité** est défini sur la valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="09146-108">On the **Cost Accounting Setup** page, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="09146-109">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable des types de coûts**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="09146-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="09146-110">Sur la page **Fiche type de coût**, vérifiez que le champ **Plage compte général** est lié correctement de sorte que chaque type de coût récupère les écritures de la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="09146-110">On the **Cost Type Card** page, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="09146-111">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="09146-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="09146-112">Pour chaque compte général approprié, sur la page **Fiche compte général**, dans le raccourci Comptabilité analytique, vérifiez que le champ **N° type coût**</span><span class="sxs-lookup"><span data-stu-id="09146-112">For each relevant general ledger account, on the **G/L Account Card** page, verify that the **Cost Type No.**</span></span> <span data-ttu-id="09146-113">est lié correctement à un type de coût.</span><span class="sxs-lookup"><span data-stu-id="09146-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="09146-114">Pour plus d'informations, voir [Configuration du contrôle de gestion](finance-set-up-cost-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="09146-114">For more information, see [Setting Up Cost Accounting](finance-set-up-cost-accounting.md).</span></span>  
7.  <span data-ttu-id="09146-115">Vérifiez que toutes les écritures comptables appropriées comprennent des sections analytiques correspondant à un centre de coûts et à un coût associé.</span><span class="sxs-lookup"><span data-stu-id="09146-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="09146-116">Pour transférer les écritures comptables vers les écritures de coûts</span><span class="sxs-lookup"><span data-stu-id="09146-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="09146-117">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Transférer les écritures comptables vers CA**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="09146-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="09146-118">Cliquez sur le bouton **Oui** pour démarrer le transfert.</span><span class="sxs-lookup"><span data-stu-id="09146-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="09146-119">Le processus transfère toutes les écritures comptables qui n'ont pas déjà été transférées.</span><span class="sxs-lookup"><span data-stu-id="09146-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="09146-120">Lors du transfert, le processus crée des connexions dans les écritures des tables **Écriture de coûts** et **Registre de coûts**.</span><span class="sxs-lookup"><span data-stu-id="09146-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="09146-121">Cela permet d'identifier l'origine des écritures de coûts.</span><span class="sxs-lookup"><span data-stu-id="09146-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="09146-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09146-122">See Also</span></span>  
<span data-ttu-id="09146-123">[Transfert et validation des écritures de coûts](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="09146-123">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
[<span data-ttu-id="09146-124">Paramétrage du contrôle de gestion</span><span class="sxs-lookup"><span data-stu-id="09146-124">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)   
