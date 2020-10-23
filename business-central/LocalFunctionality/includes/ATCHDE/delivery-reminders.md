---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1e7cb126ea06d96bd130d644948d08fd7e2e1a11
ms.sourcegitcommit: 428f180604e5afcf94fa0e92a0615f58c88e13cd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/02/2020
ms.locfileid: "3959654"
---
<span data-ttu-id="037c9-101">Les relances livraison sont utilisées pour suivre les envois des fournisseurs en retard et pour rappeler aux fournisseurs les livraisons en retard.</span><span class="sxs-lookup"><span data-stu-id="037c9-101">Delivery reminders are used to track overdue vendor shipments and to remind vendors about overdue deliveries.</span></span> <span data-ttu-id="037c9-102">Pour créer des relances livraison, vous devez configurer ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="037c9-102">To create delivery reminders, you must set up the following:</span></span>

- <span data-ttu-id="037c9-103">Conditions de relance livraison</span><span class="sxs-lookup"><span data-stu-id="037c9-103">Delivery reminder terms</span></span>  

    <span data-ttu-id="037c9-104">Les conditions de relance livraison sont identifiées par un code qui doit être affecté aux fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="037c9-104">Delivery reminder terms are identified by a code that must be assigned to vendors.</span></span> <span data-ttu-id="037c9-105">Pour utiliser plusieurs combinaisons de paramètres, vous devez configurer un code pour chaque paramètre séparément.</span><span class="sxs-lookup"><span data-stu-id="037c9-105">To use more than one combination of settings, you must set up a code for each setting separately.</span></span> <span data-ttu-id="037c9-106">Vous pouvez configurer autant de conditions relance livraison que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="037c9-106">You can set up any number of delivery reminder terms.</span></span>  

- <span data-ttu-id="037c9-107">Niveaux de relance livraison</span><span class="sxs-lookup"><span data-stu-id="037c9-107">Delivery reminder levels</span></span>  

    <span data-ttu-id="037c9-108">Pour chaque condition de relance livraison, vous devez au préalable configurer des niveaux de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="037c9-108">For every delivery reminder term, you must set up delivery reminder levels.</span></span> <span data-ttu-id="037c9-109">Ces niveaux déterminent la fréquence à laquelle les relances livraison peuvent être créées pour une condition spécifique.</span><span class="sxs-lookup"><span data-stu-id="037c9-109">These levels determine how often delivery reminders can be created for a specific term.</span></span> <span data-ttu-id="037c9-110">Le niveau 1 correspond à la première relance créée pour une livraison échue.</span><span class="sxs-lookup"><span data-stu-id="037c9-110">Level 1 is the first delivery reminder that you create for an overdue delivery.</span></span> <span data-ttu-id="037c9-111">Le niveau 2 correspond à la deuxième relance livraison, etc.</span><span class="sxs-lookup"><span data-stu-id="037c9-111">Level 2 is the second delivery reminder, and so on.</span></span> <span data-ttu-id="037c9-112">Lorsque les relances livraison sont créées, le nombre de relances créées précédemment est pris en compte, et le nombre actuel est utilisé pour appliquer des conditions.</span><span class="sxs-lookup"><span data-stu-id="037c9-112">When delivery reminders are created, the number of reminders that were created previously is considered, and the current number is used to apply terms.</span></span>  

- <span data-ttu-id="037c9-113">Message textuels de relance livraison</span><span class="sxs-lookup"><span data-stu-id="037c9-113">Delivery reminder texts messages</span></span>  

    <span data-ttu-id="037c9-114">Vous devez configurer des messages texte de relance livraison pour chaque niveau de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="037c9-114">You must set up delivery reminder text messages for every delivery reminder level.</span></span> <span data-ttu-id="037c9-115">Il existe deux types de messages texte de relance livraison : début et fin.</span><span class="sxs-lookup"><span data-stu-id="037c9-115">There are two types of delivery reminder text messages: beginning and ending.</span></span> <span data-ttu-id="037c9-116">Le message texte de début est imprimé dans la section En-tête, avant la liste des écritures marquées pour la relance.</span><span class="sxs-lookup"><span data-stu-id="037c9-116">The beginning text message is printed under the header section, before the list of entries that are marked for reminder.</span></span> <span data-ttu-id="037c9-117">Le message texte fin est imprimé après cette liste.</span><span class="sxs-lookup"><span data-stu-id="037c9-117">The ending text message is printed after this list.</span></span>  

<span data-ttu-id="037c9-118">Après avoir configuré les conditions, les niveaux et les textes de livraison, vous devez affecter les codes relance livraison appropriés à vos fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="037c9-118">After you have set up the delivery terms, levels, and texts, you must assign the relevant delivery reminder codes to your vendors.</span></span>  

<span data-ttu-id="037c9-119">Vous pouvez créer les relances livraison manuellement ou automatiquement.</span><span class="sxs-lookup"><span data-stu-id="037c9-119">You can create delivery reminders manually or automatically.</span></span> <span data-ttu-id="037c9-120">Vous pouvez utiliser le traitement par lots **Créer une relance de livraison** pour créer des relances livraison automatiquement de sorte que vous pouvez sélectionner les commandes achat pour lesquelles des relances livraison doivent être créées.</span><span class="sxs-lookup"><span data-stu-id="037c9-120">You can use the **Create Delivery Reminder** batch job to create delivery reminders automatically so that you can select the purchase orders for which delivery reminders must be created.</span></span>  

<span data-ttu-id="037c9-121">Vous pouvez également suivre les documents en rapport avec les lignes commande achat et les lignes commande vente.</span><span class="sxs-lookup"><span data-stu-id="037c9-121">You can also track documents in relation to purchase order lines and sales order lines.</span></span>  

[!INCLUDE[d365fin](../../../includes/d365fin_md.md)] <span data-ttu-id="037c9-122">fournit les états suivants :</span><span class="sxs-lookup"><span data-stu-id="037c9-122">provides the following reports:</span></span>  

- <span data-ttu-id="037c9-123">**Relance livraison publiée** - Pour afficher les relances livraison des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="037c9-123">**Issued Delivery Reminder** - To view the delivery reminders for vendors.</span></span>  
- <span data-ttu-id="037c9-124">**Relance livraison - Test** - Pour vérifier les relances livraison avant de les valider.</span><span class="sxs-lookup"><span data-stu-id="037c9-124">**Delivery Reminder - Test** - To verify the delivery reminders before you issue them.</span></span>  
