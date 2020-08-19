---
title: 'Procédure : Paramétrer des relances livraison'
description: Dans Business Central, vous pouvez utiliser des relances livraison pour rappeler aux fournisseurs les livraisons en retard.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/23/2020
ms.author: sgroespe
ms.openlocfilehash: 3fe1a3dca9a5ab1d561ff0ad9c1b4f2ab45dc990
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676647"
---
# <a name="set-up-delivery-reminders"></a><span data-ttu-id="03cee-103">Configurer des relances livraison</span><span class="sxs-lookup"><span data-stu-id="03cee-103">Set Up Delivery Reminders</span></span>

<span data-ttu-id="03cee-104">Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], vous pouvez utiliser des relances livraison pour rappeler aux fournisseurs les livraisons en retard.</span><span class="sxs-lookup"><span data-stu-id="03cee-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can use purchase delivery reminders to remind vendors about overdue deliveries.</span></span> <span data-ttu-id="03cee-105">Pour créer des relances livraison pour les fournisseurs, vous devez configurer des données de base pour la création de relances livraison et des souches de numéros pour les relances livraison dans la page **Paramètres achats**.</span><span class="sxs-lookup"><span data-stu-id="03cee-105">To create delivery reminders for vendors, you must set up base data for delivery reminder creation and number series for the delivery reminders on the **Purchases & Payables Setup** page.</span></span>  

## <a name="to-set-up-delivery-reminders"></a><span data-ttu-id="03cee-106">Pour paramétrer des relances livraison</span><span class="sxs-lookup"><span data-stu-id="03cee-106">To set up delivery reminders</span></span>  

1. <span data-ttu-id="03cee-107">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres achats**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="03cee-107">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="03cee-108">Dans le raccourci **Général**, dans le champ **Champ date rel. livr. par défaut**, spécifiez une des options suivantes comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="03cee-108">On the **General** FastTab, in the **Default Del. Rem. Date Field** field, specify one of the following options as described in the following table.</span></span>  

    |<span data-ttu-id="03cee-109">Option</span><span class="sxs-lookup"><span data-stu-id="03cee-109">Option</span></span>|<span data-ttu-id="03cee-110">Désignation</span><span class="sxs-lookup"><span data-stu-id="03cee-110">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="03cee-111">**Date réception demandée**</span><span class="sxs-lookup"><span data-stu-id="03cee-111">**Requested Receipt Date**</span></span>|<span data-ttu-id="03cee-112">Pour indiquer que la valeur de date dans le champ **Date réception demandée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="03cee-112">To specify that the date value in the **Requested Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="03cee-113">**Date réception confirmée**</span><span class="sxs-lookup"><span data-stu-id="03cee-113">**Promised Receipt Date**</span></span>|<span data-ttu-id="03cee-114">Pour indiquer que la valeur de date dans le champ **Date réception confirmée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="03cee-114">To specify that the date value in the **Promised Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="03cee-115">**Date réception prévue**</span><span class="sxs-lookup"><span data-stu-id="03cee-115">**Expected Receipt Date**</span></span>|<span data-ttu-id="03cee-116">Pour indiquer que la valeur de date dans le champ **Date réception prévue** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="03cee-116">To specify that the date value in the **Expected Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  

3. <span data-ttu-id="03cee-117">Sur le raccourci **Numérotation**, renseignez les champs comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="03cee-117">On the **Numbering** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="03cee-118">Champ</span><span class="sxs-lookup"><span data-stu-id="03cee-118">Field</span></span>|<span data-ttu-id="03cee-119">Désignation</span><span class="sxs-lookup"><span data-stu-id="03cee-119">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="03cee-120">**Numéros relances livraison**</span><span class="sxs-lookup"><span data-stu-id="03cee-120">**Delivery Reminder Nos.**</span></span>|<span data-ttu-id="03cee-121">Code souche de numéros pour les relances livraison.</span><span class="sxs-lookup"><span data-stu-id="03cee-121">The number series code for delivery reminders.</span></span>|  
    |<span data-ttu-id="03cee-122">**Numéros relances livraison émis**</span><span class="sxs-lookup"><span data-stu-id="03cee-122">**Issued Delivery Reminder Nos.**</span></span>|<span data-ttu-id="03cee-123">Code souche de numéros pour les relances livraison émises.</span><span class="sxs-lookup"><span data-stu-id="03cee-123">The number series code for issued delivery reminders.</span></span>|  

4. <span data-ttu-id="03cee-124">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="03cee-124">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="03cee-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03cee-125">See Also</span></span>

[<span data-ttu-id="03cee-126">relances livraison</span><span class="sxs-lookup"><span data-stu-id="03cee-126">Delivery Reminders</span></span>](delivery-reminders.md)  
[<span data-ttu-id="03cee-127">Configurer les conditions, niveaux et textes de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="03cee-127">Set Up Delivery Reminder Terms, Levels, and Text</span></span>](how-to-set-up-delivery-reminder-terms-levels-and-text.md)  
[<span data-ttu-id="03cee-128">Affecter des codes de relance livraison à des fournisseurs</span><span class="sxs-lookup"><span data-stu-id="03cee-128">Assign Delivery Reminder Codes to Vendors</span></span>](how-to-assign-delivery-reminder-codes-to-vendors.md)  
[<span data-ttu-id="03cee-129">Créer manuellement des relances livraison</span><span class="sxs-lookup"><span data-stu-id="03cee-129">Create Delivery Reminders Manually</span></span>](how-to-create-delivery-reminders-manually.md)
