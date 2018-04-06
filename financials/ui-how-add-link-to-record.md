---
title: "Procédure de liaison d'un enregistrement à des informations ou programmes externes | Microsoft Docs"
description: "Joignez un lien hypertexte pointant vers un document ou un site Web à un enregistrement spécifique, tel qu'une fiche client ou un document."
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 876c91aad4463f499ca70d14ba4c0e649353e37b
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="104f2-103">Ajout de liens à des sites Web, documents ou programmes sur des enregistrements</span><span class="sxs-lookup"><span data-stu-id="104f2-103">Adding Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="104f2-104">Sur un enregistrement spécifique, comme une fiche client, un document ou une commande vente, vous pouvez ajouter un lien à un document, site Web ou programme externe.</span><span class="sxs-lookup"><span data-stu-id="104f2-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="104f2-105">Vous pouvez aussi sélectionner un lien qui ouvre un e-mail vierge adressé à un destinataire précis.</span><span class="sxs-lookup"><span data-stu-id="104f2-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="104f2-106">La page Fiche de certains enregistrements comme les fiches client ou fournisseur, dispose d'un champ **Page d'accueil** dans lequel vous pouvez entrer une adresse Internet (URL).</span><span class="sxs-lookup"><span data-stu-id="104f2-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="104f2-107">Pour insérer d'autres liens, vous pouvez utiliser la méthode décrite dans cet article.</span><span class="sxs-lookup"><span data-stu-id="104f2-107">To include other links, you can use the method described in this article.</span></span>

<span data-ttu-id="104f2-108">Un autre exemple est lorsque vous recevez des factures imprimées de fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="104f2-108">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="104f2-109">Vous pouvez les numériser et les enregistrer au format .pdf sur un site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="104f2-109">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="104f2-110">Ensuite, vous pouvez créer un lien d'une facture achat dans [!INCLUDE[d365fin_md](includes/d365fin_md.md)] vers la facture correspondante sur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="104f2-110">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="104f2-111">Vous pouvez aussi créer un lien depuis une fiche article vers la page correspondante du catalogue en ligne de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="104f2-111">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="104f2-112">Pour ajouter un lien sur un enregistrement</span><span class="sxs-lookup"><span data-stu-id="104f2-112">To add a link on a record</span></span>   

1.  <span data-ttu-id="104f2-113">Ouvrez l'enregistrement auquel vous voulez ajouter le lien, par exemple une fiche client ou une commande vente.</span><span class="sxs-lookup"><span data-stu-id="104f2-113">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="104f2-114">Pour associer le lien à une ligne spécifique, par exemple une ligne feuille, sélectionnez la ligne.</span><span class="sxs-lookup"><span data-stu-id="104f2-114">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="104f2-115">Choisissez l'action **Liens** pour ouvrir les fenêtres **Liens** qui affichent tous les liens actuels qui sont ajoutés à l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="104f2-115">Choose the **Links** action to open the **Links** windows that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="104f2-116">Pour ajouter un nouveau lien, choisissez **+nouveau**.</span><span class="sxs-lookup"><span data-stu-id="104f2-116">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="104f2-117">Dans le champ **Adresse du lien**, entrez</span><span class="sxs-lookup"><span data-stu-id="104f2-117">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="104f2-118">Pour créer un lien vers un fichier sur votre ordinateur ou réseau, entrez le chemin d'accès complet et le nom du fichier, par exemple **C:My Documentsinvoice1.doc**.</span><span class="sxs-lookup"><span data-stu-id="104f2-118">To link to a file on your computer or network, enter the full path and file name, such as  **C:My Documentsinvoice1.doc**.</span></span>
    -   <span data-ttu-id="104f2-119">Pour créer un lien vers un site Web, entrez l'adresse Internet (URL), par exemple **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="104f2-119">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="104f2-120">Pour créer un lien vers un site Web, entrez l'adresse Internet (URL), par exemple **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="104f2-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="104f2-121">Pour créer un lien vers un programme, entrez une chaîne spécifique pour ouvrir le programme.</span><span class="sxs-lookup"><span data-stu-id="104f2-121">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="104f2-122">Par exemple, pour ouvrir OneNote avec une page spécifique, entrez **onenote:///C:My Documentstest.one**.</span><span class="sxs-lookup"><span data-stu-id="104f2-122">For example, to open OneNote with a specific page, enter **onenote:///C:My Documentstest.one**.</span></span> <span data-ttu-id="104f2-123">Ou, pour ouvrir Outlook avec un e-mail vierge à destination d'un alias spécifique, entrez **mailto:testalias** .</span><span class="sxs-lookup"><span data-stu-id="104f2-123">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="104f2-124">Dans le champ **Désignation**, entrez les informations sur le lien.</span><span class="sxs-lookup"><span data-stu-id="104f2-124">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="104f2-125">Cliquez sur le bouton **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="104f2-125">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="104f2-126">Pour supprimer un lien dans un enregistrement</span><span class="sxs-lookup"><span data-stu-id="104f2-126">To delete a link from a record</span></span>  

<span data-ttu-id="104f2-127">Pour supprimer un lien, dans la fenêtre **Liens**, vous pouvez sélectionner **…**, puis **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="104f2-127">To delete a link, in the **Links** window, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="104f2-128">Si vous supprimez un enregistrement, par exemple, une ligne commande vente, une commande vente ou une fiche client, tous les liens contenus dans l'enregistrement sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="104f2-128">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="104f2-129">En revanche, si vous supprimez des enregistrements à l'aide d'un traitement par lots, par exemple, le traitement par lots **Supprimer cdes vente facturées**, les liens sont conservés dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="104f2-129">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="104f2-130">Pour supprimer les liens de la base de données, exécutez le codeunit **Supprimer les liens enregistrement orphelins**.</span><span class="sxs-lookup"><span data-stu-id="104f2-130">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="104f2-131">Pour ce faire, sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Supprimer les liens enregistrement orphelins**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="104f2-131">To do this, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="104f2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="104f2-132">See Also</span></span>  
<span data-ttu-id="104f2-133">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="104f2-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

