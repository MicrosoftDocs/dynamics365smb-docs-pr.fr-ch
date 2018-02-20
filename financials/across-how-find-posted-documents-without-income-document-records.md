---
title: "Rechercher des documents sans pièces jointes| Microsoft Docs"
Description: You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c355657821f5f4d18c707d296d9607cf5ec60442
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="00741-102">Rechercher des enregistrements validés sans enregistrements document entrant</span><span class="sxs-lookup"><span data-stu-id="00741-102">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="00741-103">Depuis les fenêtres **Plan comptable** et **Écritures comptables**, vous pouvez utiliser la fonction de recherche pour rechercher les écritures comptables pour des documents achat et vente validés qui n'ont pas d'enregistrement de document entrant, puis les lier de façon centralisée à des enregistrements existants ou en créer de nouveaux avec des fichiers joints.</span><span class="sxs-lookup"><span data-stu-id="00741-103">From the **Chart of Accounts** and **General Ledger Entries** windows, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="00741-104">Rechercher des enregistrements validés sans enregistrements document entrant</span><span class="sxs-lookup"><span data-stu-id="00741-104">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="00741-105">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Plan comptable**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="00741-105">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="00741-106">Sélectionnez une ligne pour un compte général pour les écritures comptables duquel vous souhaitez voir les documents ventes et achats validés sans enregistrement document entrant, puis sélectionnez l'action **Documents validés sans document entrant**.</span><span class="sxs-lookup"><span data-stu-id="00741-106">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="00741-107">Sinon, sélectionnez l'action **Écritures comptables**.</span><span class="sxs-lookup"><span data-stu-id="00741-107">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="00741-108">Dans la fenêtre **Écritures comptables**, sélectionnez l'action **Documents validés sans documents entrants**.</span><span class="sxs-lookup"><span data-stu-id="00741-108">In the **General Ledger Entries** window, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="00741-109">La fenêtre **Documents validés sans document entrant** s'ouvre et affiche des documents achat et vente validés sans enregistrement document entrant représenté par des écritures comptables du compte général pour lequel vous avez ouvert la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="00741-109">The **Posted Documents without Incoming Document** window opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the window for.</span></span> <span data-ttu-id="00741-110">Au maximum, la fenêtre affiche 1 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="00741-110">The window can show a maximum of 1000 lines.</span></span> <span data-ttu-id="00741-111">Par défaut, le champ **Filtre date** contient donc un filtre qui limite l'affichage des lignes à celles dont les écritures ont une date comptabilisation comprise entre le début de la période comptable et la date de travail.</span><span class="sxs-lookup"><span data-stu-id="00741-111">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="00741-112">Lier des documents recherchés à des enregistrements document entrant existants</span><span class="sxs-lookup"><span data-stu-id="00741-112">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="00741-113">Dans la fenêtre **Documents validés sans document entrant**, sélectionnez la ligne d'un document valisé que vous souhaitez lier à un enregistrement document entrant existant, puis sélectionnez l'action **Sélectionner le document entrant**.</span><span class="sxs-lookup"><span data-stu-id="00741-113">In the **Posted Documents without Incoming Document** window, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="00741-114">Dans la fenêtre **Documents entrants**, sélectionnez l'enregistrement document entrant que vous souhaitez lier au document validé trouvé, puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="00741-114">In the **Incoming Documents** window, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="00741-115">Dans la fenêtre **Documents validés sans document entrant**, l'enregistrement document entrant sélectionné est désormais lié au document validé, comme vous pouvez le constater dans le récapitulatif **Fichiers du document entrant**.</span><span class="sxs-lookup"><span data-stu-id="00741-115">In the **Posted Documents without Incoming Document** window, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="00741-116">Si un enregistrement document entrant approprié n'existe pas dans la fenêtre **Documents entrants**, vous pouvez le créer.</span><span class="sxs-lookup"><span data-stu-id="00741-116">If a relevant incoming document record does not exist in the **Incoming Documents** window, then you can create it.</span></span> <span data-ttu-id="00741-117">Pour plus d'informations, voir [Créer des enregistrements document entrant](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="00741-117">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="00741-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00741-118">See Also</span></span>
[<span data-ttu-id="00741-119">Traiter les documents entrants</span><span class="sxs-lookup"><span data-stu-id="00741-119">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="00741-120">Documents entrants</span><span class="sxs-lookup"><span data-stu-id="00741-120">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="00741-121">Achats</span><span class="sxs-lookup"><span data-stu-id="00741-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="00741-122">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="00741-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

