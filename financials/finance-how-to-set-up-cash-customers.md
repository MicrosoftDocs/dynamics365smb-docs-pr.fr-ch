---
title: "Procédure : configurer des clients effectuant un achat au comptoir | Microsoft Docs"
description: "Cette rubrique décrit les étapes pour configurer un client qui paie en espèces."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: a6be13d3f2fcc683e8d711691f9d994f64458f85
ms.contentlocale: fr-ch
ms.lasthandoff: 04/16/2018

---
# <a name="set-up-cash-customers"></a><span data-ttu-id="d8c52-103">Configurer des clients effectuant un achat au comptoir</span><span class="sxs-lookup"><span data-stu-id="d8c52-103">Set Up Cash Customers</span></span>
<span data-ttu-id="d8c52-104">Vous ne pouvez pas créer une facture sans numéro de client.</span><span class="sxs-lookup"><span data-stu-id="d8c52-104">You cannot create an invoice without a customer number.</span></span> <span data-ttu-id="d8c52-105">Ceci est valable même si vous effectuez une vente au comptoir et que vous n'avez rien à enregistrer dans un compte client.</span><span class="sxs-lookup"><span data-stu-id="d8c52-105">This is true, even if you make a cash sale and do not have anything to record in a customer account.</span></span>  

## <a name="to-set-up-a-cash-customer"></a><span data-ttu-id="d8c52-106">Pour configurer des clients effectuant un achat en espèces</span><span class="sxs-lookup"><span data-stu-id="d8c52-106">To set up a cash customer</span></span>  
1. <span data-ttu-id="d8c52-107">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Client**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="d8c52-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d8c52-108">Créez une fiche **Client**.</span><span class="sxs-lookup"><span data-stu-id="d8c52-108">Create a new **Customer** card.</span></span> <span data-ttu-id="d8c52-109">Pour plus d'informations, reportez vous à [Enregistrer de nouveaux clients](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="d8c52-109">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>
3. <span data-ttu-id="d8c52-110">Dans le champ **N°**,</span><span class="sxs-lookup"><span data-stu-id="d8c52-110">In the **No.**</span></span> <span data-ttu-id="d8c52-111">, saisissez par exemple **Espèces**.</span><span class="sxs-lookup"><span data-stu-id="d8c52-111">field, enter **Cash**, for example.</span></span>  
4. <span data-ttu-id="d8c52-112">Dans le champ **Nom**, saisissez par exemple **Vente au comptoir**.</span><span class="sxs-lookup"><span data-stu-id="d8c52-112">In the **Name** field, enter **Cash Sale**, for example.</span></span>  
5. <span data-ttu-id="d8c52-113">Sur le raccourcie **Facturation**, renseignez les champs **Groupe compta. client** et **Groupe compta. marché**.</span><span class="sxs-lookup"><span data-stu-id="d8c52-113">On the **Invoicing** FastTab, fill in the **Customer Posting Group** and the **Gen. Bus. Posting Group** fields.</span></span>  

   <span data-ttu-id="d8c52-114">Vous avez alors configuré un client contenant suffisamment d'informations de facturation.</span><span class="sxs-lookup"><span data-stu-id="d8c52-114">Now you have set up a customer that contains sufficient information for invoicing.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d8c52-115">Vous avez peut-être choisi un groupe comptabilisation également utilisé pour les ventes à crédit nationales.</span><span class="sxs-lookup"><span data-stu-id="d8c52-115">You may have chosen a posting group that is also used for domestic credit sales.</span></span> <span data-ttu-id="d8c52-116">Si vous souhaitez mettre à jour des données séparées sur les ventes au comptoir, par exemple avec un compte client ou fournisseur spécial, vous pouvez configurer un groupe comptabilisation supplémentaire à cet effet.</span><span class="sxs-lookup"><span data-stu-id="d8c52-116">If you want to maintain separate data on cash sales, for example, with a special sales or receivables account, you can set up an extra posting group for this purpose.</span></span>  
>   
>  <span data-ttu-id="d8c52-117">Vous devez saisir le numéro d'un compte client pour le groupe comptabilisation, même si le solde de ce compte est toujours de 0 après la validation d'une facture.</span><span class="sxs-lookup"><span data-stu-id="d8c52-117">You must enter a number for a receivables account for the posting group, even though the balance in this account will always be 0 after you post an invoice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d8c52-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8c52-118">See Also</span></span>
[<span data-ttu-id="d8c52-119">Gestion des comptes client</span><span class="sxs-lookup"><span data-stu-id="d8c52-119">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="d8c52-120">[Enregistrer de nouveaux clients](sales-how-register-new-customers.md)  </span><span class="sxs-lookup"><span data-stu-id="d8c52-120">[Register New Customers](sales-how-register-new-customers.md)  </span></span>  
[<span data-ttu-id="d8c52-121">Finances</span><span class="sxs-lookup"><span data-stu-id="d8c52-121">Finance</span></span>](finance.md)  


