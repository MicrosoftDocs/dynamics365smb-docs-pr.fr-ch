---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 34d9ddd0c3afc97beb19c6c4c9441770656ef6e9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771508"
---
<span data-ttu-id="fcc05-101">Dans [!INCLUDE[prod_short](../../../includes/prod_short.md)], vous pouvez utiliser des relances livraison pour rappeler aux fournisseurs les livraisons en retard.</span><span class="sxs-lookup"><span data-stu-id="fcc05-101">In [!INCLUDE[prod_short](../../../includes/prod_short.md)], you can use purchase delivery reminders to remind vendors about overdue deliveries.</span></span> <span data-ttu-id="fcc05-102">Pour créer des relances livraison pour les fournisseurs, vous devez configurer des données de base pour la création de relances livraison et des souches de numéros pour les relances livraison dans la page **Paramètres achats**.</span><span class="sxs-lookup"><span data-stu-id="fcc05-102">To create delivery reminders for vendors, you must set up base data for delivery reminder creation and number series for the delivery reminders on the **Purchases & Payables Setup** page.</span></span>  

## <a name="to-set-up-delivery-reminders"></a><span data-ttu-id="fcc05-103">Pour paramétrer des relances livraison</span><span class="sxs-lookup"><span data-stu-id="fcc05-103">To set up delivery reminders</span></span>  

1. <span data-ttu-id="fcc05-104">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres achats**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="fcc05-104">Choose the ![Lightbulb that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fcc05-105">Dans le champ **Champ date rel. livr. par défaut**, spécifiez une des options suivantes comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fcc05-105">In the **Default Del. Rem. Date Field** field, specify one of the options described in the following table.</span></span>  

    |<span data-ttu-id="fcc05-106">Option</span><span class="sxs-lookup"><span data-stu-id="fcc05-106">Option</span></span>|<span data-ttu-id="fcc05-107">Description</span><span class="sxs-lookup"><span data-stu-id="fcc05-107">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="fcc05-108">**Date réception demandée**</span><span class="sxs-lookup"><span data-stu-id="fcc05-108">**Requested Receipt Date**</span></span>|<span data-ttu-id="fcc05-109">Spécifie que la valeur de date dans le champ **Date réception demandée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="fcc05-109">Specifies that the date value in the **Requested Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="fcc05-110">**Date réception confirmée**</span><span class="sxs-lookup"><span data-stu-id="fcc05-110">**Promised Receipt Date**</span></span>|<span data-ttu-id="fcc05-111">Spécifie que la valeur de date dans le champ **Date réception confirmée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="fcc05-111">Specifies that the date value in the **Promised Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="fcc05-112">**Date réception prévue**</span><span class="sxs-lookup"><span data-stu-id="fcc05-112">**Expected Receipt Date**</span></span>|<span data-ttu-id="fcc05-113">Spécifie que la valeur de date dans le champ **Date réception prévue** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="fcc05-113">Specifies that the date value in the **Expected Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  

3. <span data-ttu-id="fcc05-114">Renseignez les champs supplémentaires comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fcc05-114">Fill in additional fields as described in the following table.</span></span>  

    |<span data-ttu-id="fcc05-115">Champ</span><span class="sxs-lookup"><span data-stu-id="fcc05-115">Field</span></span>|<span data-ttu-id="fcc05-116">Description</span><span class="sxs-lookup"><span data-stu-id="fcc05-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="fcc05-117">**Numéros relances livraison**</span><span class="sxs-lookup"><span data-stu-id="fcc05-117">**Delivery Reminder Nos.**</span></span>|<span data-ttu-id="fcc05-118">Code souche de numéros pour les relances livraison.</span><span class="sxs-lookup"><span data-stu-id="fcc05-118">The number series code for delivery reminders.</span></span>|  
    |<span data-ttu-id="fcc05-119">**Numéros relances livraison émis**</span><span class="sxs-lookup"><span data-stu-id="fcc05-119">**Issued Delivery Reminder Nos.**</span></span>|<span data-ttu-id="fcc05-120">Code souche de numéros pour les relances livraison émises.</span><span class="sxs-lookup"><span data-stu-id="fcc05-120">The number series code for issued delivery reminders.</span></span>|  

4. <span data-ttu-id="fcc05-121">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="fcc05-121">Choose the **OK** button.</span></span>  
