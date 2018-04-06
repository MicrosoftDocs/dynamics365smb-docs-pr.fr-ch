---
title: "Procédure : Paramétrer des relances livraison"
description: Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], vous pouvez utiliser des relances livraison pour rappeler aux fournisseurs les livraisons en retard.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 987794b94a5016b91327d17a4bca8dd3ad28bf8e
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-delivery-reminders"></a><span data-ttu-id="23e31-103">Configurer des relances livraison</span><span class="sxs-lookup"><span data-stu-id="23e31-103">Set Up Delivery Reminders</span></span>
<span data-ttu-id="23e31-104">Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], vous pouvez utiliser des relances livraison pour rappeler aux fournisseurs les livraisons en retard.</span><span class="sxs-lookup"><span data-stu-id="23e31-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can use purchase delivery reminders to remind vendors about overdue deliveries.</span></span> <span data-ttu-id="23e31-105">Pour créer des relances livraison pour les fournisseurs, vous devez configurer des données de base pour la création de relances livraison et des souches de numéros pour les relances livraison dans la fenêtre **Paramètres achats**.</span><span class="sxs-lookup"><span data-stu-id="23e31-105">To create delivery reminders for vendors, you must set up base data for delivery reminder creation and number series for the delivery reminders in the **Purchases & Payables Setup** window.</span></span>  

## <a name="to-set-up-delivery-reminders"></a><span data-ttu-id="23e31-106">Pour paramétrer des relances livraison</span><span class="sxs-lookup"><span data-stu-id="23e31-106">To set up delivery reminders</span></span>  

1.  <span data-ttu-id="23e31-107">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres achats**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="23e31-107">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="23e31-108">Dans le raccourci **Général**, dans le champ **Champ date rel. livr. par défaut**, spécifiez une des options suivantes comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="23e31-108">On the **General** FastTab, in the **Default Del. Rem. Date Field** field, specify one of the following options as described in the following table.</span></span>  

    |<span data-ttu-id="23e31-109">Option</span><span class="sxs-lookup"><span data-stu-id="23e31-109">Option</span></span>|<span data-ttu-id="23e31-110">Désignation</span><span class="sxs-lookup"><span data-stu-id="23e31-110">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="23e31-111">**Date réception demandée**</span><span class="sxs-lookup"><span data-stu-id="23e31-111">**Requested Receipt Date**</span></span>|<span data-ttu-id="23e31-112">Pour indiquer que la valeur de date dans le champ **Date réception demandée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="23e31-112">To specify that the date value in the **Requested Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="23e31-113">**Date réception confirmée**</span><span class="sxs-lookup"><span data-stu-id="23e31-113">**Promised Receipt Date**</span></span>|<span data-ttu-id="23e31-114">Pour indiquer que la valeur de date dans le champ **Date réception confirmée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="23e31-114">To specify that the date value in the **Promised Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="23e31-115">**Date réception prévue**</span><span class="sxs-lookup"><span data-stu-id="23e31-115">**Expected Receipt Date**</span></span>|<span data-ttu-id="23e31-116">Pour indiquer que la valeur de date dans le champ **Date réception prévue** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="23e31-116">To specify that the date value in the **Expected Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  

3.  <span data-ttu-id="23e31-117">Sur le raccourci **Numérotation**, renseignez les champs comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="23e31-117">On the **Numbering** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="23e31-118">Champ</span><span class="sxs-lookup"><span data-stu-id="23e31-118">Field</span></span>|<span data-ttu-id="23e31-119">Désignation</span><span class="sxs-lookup"><span data-stu-id="23e31-119">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="23e31-120">**Numéros relances livraison**</span><span class="sxs-lookup"><span data-stu-id="23e31-120">**Delivery Reminder Nos.**</span></span>|<span data-ttu-id="23e31-121">Code souche de numéros pour les relances livraison.</span><span class="sxs-lookup"><span data-stu-id="23e31-121">The number series code for delivery reminders.</span></span>|  
    |<span data-ttu-id="23e31-122">**Numéros relances livraison émis**</span><span class="sxs-lookup"><span data-stu-id="23e31-122">**Issued Delivery Reminder Nos.**</span></span>|<span data-ttu-id="23e31-123">Code souche de numéros pour les relances livraison émises.</span><span class="sxs-lookup"><span data-stu-id="23e31-123">The number series code for issued delivery reminders.</span></span>|  

4.  <span data-ttu-id="23e31-124">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="23e31-124">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="23e31-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23e31-125">See Also</span></span>  
 <span data-ttu-id="23e31-126">[relances livraison](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="23e31-126">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="23e31-127">[Configurer les conditions, niveaux et textes de relance livraison.](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span><span class="sxs-lookup"><span data-stu-id="23e31-127">[Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span></span>  
 <span data-ttu-id="23e31-128">[Affecter des codes de relance livraison à des fournisseurs](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="23e31-128">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 [<span data-ttu-id="23e31-129">Créer manuellement des relances livraison</span><span class="sxs-lookup"><span data-stu-id="23e31-129">Create Delivery Reminders Manually</span></span>](how-to-create-delivery-reminders-manually.md)

