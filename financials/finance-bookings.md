---
title: "Facturer vos réservations dans Dynamics 365| Microsoft Docs"
description: "Apprenez comment vous pouvez effectuer la facturation en vrac des réservations Microsoft dans Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 06/14/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1f1a1645ba27a3b42d67c11f7472c283ca44dbd1
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a><span data-ttu-id="490ae-103">Facturation en vrac pour les réservations Microsoft dans [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="490ae-103">Bulk Invoicing for Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="490ae-104">Si votre société utilise l'application Réservations d'Office 365, vous pouvez effectuer la facturation en vrac des rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="490ae-104">If your company uses the Bookings app in Office 365, you can do bulk invoicing for appointments.</span></span> <span data-ttu-id="490ae-105">La page **Réservations non facturées** de [!INCLUDE[d365fin](includes/d365fin_md.md)] fournit une liste des réservations effectuées par la société.</span><span class="sxs-lookup"><span data-stu-id="490ae-105">The **Uninvoiced Bookings** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a list of the company's completed bookings.</span></span> <span data-ttu-id="490ae-106">Cette page vous permet de rapidement sélectionner les rendez-vous à facturer et de créer des factures provisoires pour les services fournis.</span><span class="sxs-lookup"><span data-stu-id="490ae-106">In this page you can quickly select the appointments that you want to invoice and create draft invoices for the services provided.</span></span>  

## <a name="connect-to-bookings"></a><span data-ttu-id="490ae-107">Connexion à Réservations</span><span class="sxs-lookup"><span data-stu-id="490ae-107">Connect to Bookings</span></span>
<span data-ttu-id="490ae-108">Pour connecter votre [!INCLUDE[d365fin](includes/d365fin_md.md)] à Réservations, vous devez indiquer votre société Réservations, quoi synchroniser avec Réservations, la fréquence de la synchronisation et les modèles à utiliser.</span><span class="sxs-lookup"><span data-stu-id="490ae-108">To connect your [!INCLUDE[d365fin](includes/d365fin_md.md)] with Bookings, you must specify your Bookings company, what to synchronize with Bookings, how often to synchronize, and which templates to use.</span></span> <span data-ttu-id="490ae-109">Vous définissez ces informations sur la page **Paramètres synch. réservations**, que vous pouvez lancer depuis la page **Configuration de la synchronisation Exchange**, que vous pouvez rechercher à l'aide de [Rechercher](ui-search.md).</span><span class="sxs-lookup"><span data-stu-id="490ae-109">You set up this information in the **Booking Sync. Setup** page, which you can launch from the **Exchange Sync. Setup** page, which you can find through [Search](ui-search.md).</span></span>  

<span data-ttu-id="490ae-110">Par exemple, si vous souhaitez synchroniser des clients entre Réservations et [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez spécifier le modèle par défaut à utiliser pour ajouter de nouveaux clients à [!INCLUDE[d365fin](includes/d365fin_md.md)] selon les clients de votre société de Réservations.</span><span class="sxs-lookup"><span data-stu-id="490ae-110">For example, if you want to synchronize customers between Bookings and [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the default template to use to add new customers in [!INCLUDE[d365fin](includes/d365fin_md.md)] based on the customers in your Bookings company.</span></span>  

## <a name="invoice-appointments"></a><span data-ttu-id="490ae-111">Facturer les rendez-vous</span><span class="sxs-lookup"><span data-stu-id="490ae-111">Invoice Appointments</span></span>
<span data-ttu-id="490ae-112">Lorsqu'il est temps d'envoyer les factures pour les réservations terminées, vous consultez la page **Réservations non facturées**.</span><span class="sxs-lookup"><span data-stu-id="490ae-112">When it is time to send invoices for the completed bookings, you go to the **Uninvoiced Bookings** page.</span></span> <span data-ttu-id="490ae-113">Selon le nombre de fois où les informations sont synchronisées, la liste est long ou courte.</span><span class="sxs-lookup"><span data-stu-id="490ae-113">Depending on how often the information is synchronized, the list is long or short.</span></span> <span data-ttu-id="490ae-114">Vous pouvez créer des factures pour toutes les réservations de la liste ou une réservation à la fois.</span><span class="sxs-lookup"><span data-stu-id="490ae-114">You can create invoices for all bookings in the list or one booking at a time.</span></span> <span data-ttu-id="490ae-115">Vous pouvez sélectionner une ou plusieurs écritures dans la liste et facturer celles-ci uniquement.</span><span class="sxs-lookup"><span data-stu-id="490ae-115">You can select one or more entries in the list and invoice those only.</span></span>  

<span data-ttu-id="490ae-116">Le prise en charge de la facturation des rendez-vous dans Réservations est plus simple que le flux de travail plus complet consistant à utiliser des devis, des commandes vente, et des factures vente.</span><span class="sxs-lookup"><span data-stu-id="490ae-116">The support for invoicing appointments from Bookings is simpler than the fuller workflow of working with sales quotes, sales orders, and sales invoices.</span></span> <span data-ttu-id="490ae-117">Pour plus d'informations, reportez-vous à [Procédure : facturer des ventes](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="490ae-117">For more information, see [How to: Invoice Sales](sales-how-invoice-sales.md).</span></span> <span data-ttu-id="490ae-118">Vous pouvez choisir de vendre vos services à l'aide de [!INCLUDE[d365fin](includes/d365fin_md.md)] ou d'utiliser Réservations, selon les besoins de votre activité.</span><span class="sxs-lookup"><span data-stu-id="490ae-118">You can choose to sell your services using [!INCLUDE[d365fin](includes/d365fin_md.md)] or choose to use Bookings, depending on your business needs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="490ae-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="490ae-119">See Also</span></span>
[<span data-ttu-id="490ae-120">Finances</span><span class="sxs-lookup"><span data-stu-id="490ae-120">Finance</span></span>](finance.md)  
[<span data-ttu-id="490ae-121">Procédure : facturer des ventes</span><span class="sxs-lookup"><span data-stu-id="490ae-121">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="490ae-122">Définition des ventes</span><span class="sxs-lookup"><span data-stu-id="490ae-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="490ae-123">Réservations Microsoft</span><span class="sxs-lookup"><span data-stu-id="490ae-123">Microsoft Bookings</span></span>](https://products.office.com/en-us/business/scheduling-and-booking-app)  

