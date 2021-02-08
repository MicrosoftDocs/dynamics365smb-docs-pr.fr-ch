---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b2d0a0ff1106431701b8d22c8c8e36f1701cfc39
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747533"
---
<span data-ttu-id="60738-101">Dans [!INCLUDE[prod_short](../../../includes/prod_short.md)], vous pouvez utiliser des relances livraison pour rappeler aux fournisseurs les livraisons en retard.</span><span class="sxs-lookup"><span data-stu-id="60738-101">In [!INCLUDE[prod_short](../../../includes/prod_short.md)], you can use purchase delivery reminders to remind vendors about overdue deliveries.</span></span> <span data-ttu-id="60738-102">Pour créer des relances livraison pour les fournisseurs, vous devez configurer des données de base pour la création de relances livraison et des souches de numéros pour les relances livraison dans la page **Paramètres achats**.</span><span class="sxs-lookup"><span data-stu-id="60738-102">To create delivery reminders for vendors, you must set up base data for delivery reminder creation and number series for the delivery reminders on the **Purchases & Payables Setup** page.</span></span>  

## <a name="to-set-up-delivery-reminders"></a><span data-ttu-id="60738-103">Pour paramétrer des relances livraison</span><span class="sxs-lookup"><span data-stu-id="60738-103">To set up delivery reminders</span></span>  

1. <span data-ttu-id="60738-104">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres achats**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="60738-104">Choose the ![Lightbulb that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="60738-105">Dans le champ **Champ date rel. livr. par défaut**, spécifiez une des options suivantes comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="60738-105">In the **Default Del. Rem. Date Field** field, specify one of the options described in the following table.</span></span>  

    |<span data-ttu-id="60738-106">Option</span><span class="sxs-lookup"><span data-stu-id="60738-106">Option</span></span>|<span data-ttu-id="60738-107">Description</span><span class="sxs-lookup"><span data-stu-id="60738-107">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="60738-108">**Date réception demandée**</span><span class="sxs-lookup"><span data-stu-id="60738-108">**Requested Receipt Date**</span></span>|<span data-ttu-id="60738-109">Spécifie que la valeur de date dans le champ **Date réception demandée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="60738-109">Specifies that the date value in the **Requested Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="60738-110">**Date réception confirmée**</span><span class="sxs-lookup"><span data-stu-id="60738-110">**Promised Receipt Date**</span></span>|<span data-ttu-id="60738-111">Spécifie que la valeur de date dans le champ **Date réception confirmée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="60738-111">Specifies that the date value in the **Promised Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="60738-112">**Date réception prévue**</span><span class="sxs-lookup"><span data-stu-id="60738-112">**Expected Receipt Date**</span></span>|<span data-ttu-id="60738-113">Spécifie que la valeur de date dans le champ **Date réception prévue** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="60738-113">Specifies that the date value in the **Expected Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  

3. <span data-ttu-id="60738-114">Renseignez les champs supplémentaires comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="60738-114">Fill in additional fields as described in the following table.</span></span>  

    |<span data-ttu-id="60738-115">Champ</span><span class="sxs-lookup"><span data-stu-id="60738-115">Field</span></span>|<span data-ttu-id="60738-116">Description</span><span class="sxs-lookup"><span data-stu-id="60738-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="60738-117">**Numéros relances livraison**</span><span class="sxs-lookup"><span data-stu-id="60738-117">**Delivery Reminder Nos.**</span></span>|<span data-ttu-id="60738-118">Code souche de numéros pour les relances livraison.</span><span class="sxs-lookup"><span data-stu-id="60738-118">The number series code for delivery reminders.</span></span>|  
    |<span data-ttu-id="60738-119">**Numéros relances livraison émis**</span><span class="sxs-lookup"><span data-stu-id="60738-119">**Issued Delivery Reminder Nos.**</span></span>|<span data-ttu-id="60738-120">Code souche de numéros pour les relances livraison émises.</span><span class="sxs-lookup"><span data-stu-id="60738-120">The number series code for issued delivery reminders.</span></span>|  

4. <span data-ttu-id="60738-121">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="60738-121">Choose the **OK** button.</span></span>  
