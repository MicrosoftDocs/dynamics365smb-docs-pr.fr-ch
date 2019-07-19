---
title: Procédure de liaison d'un enregistrement à des informations ou programmes externes | Microsoft Docs
description: Joignez un lien hypertexte pointant vers un document ou un site Web à un enregistrement spécifique, tel qu'une fiche client ou un document.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/12/2019
ms.author: jswymer
ms.openlocfilehash: 781f43daf6482c7e29696dc7a03aa021550cde7d
ms.sourcegitcommit: f2e3b571eab6e01d9f5aa8ef47056b6bd313dcbd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/13/2019
ms.locfileid: "1629772"
---
# <a name="add-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="8a1b6-103">Ajouter des liens à des sites Web, documents ou programmes sur des enregistrements</span><span class="sxs-lookup"><span data-stu-id="8a1b6-103">Add Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="8a1b6-104">Sur un enregistrement spécifique, comme une fiche client, un document ou une commande vente, vous pouvez ajouter un lien à un document, site Web ou programme externe.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="8a1b6-105">Vous pouvez aussi sélectionner un lien qui ouvre un e-mail vierge adressé à un destinataire précis.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="8a1b6-106">La page Fiche de certains enregistrements comme les fiches client ou fournisseur, dispose d'un champ **Page d'accueil** dans lequel vous pouvez entrer une adresse Internet (URL).</span><span class="sxs-lookup"><span data-stu-id="8a1b6-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="8a1b6-107">Pour insérer d'autres liens, vous pouvez utiliser la méthode décrite dans cet article.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-107">To include other links, you can use the method described in this article.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="8a1b6-108">Actuellement, cette capacité est disponible uniquement dans les déploiements locaux [!INCLUDE [prodshort](includes/prodshort.md)] avec le client Dynamics NAV Windows hérité.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-108">Currently, this capability is available only in [!INCLUDE [prodshort](includes/prodshort.md)] on-premises deployments with the legacy Dynamics NAV Windows client.</span></span>  

<span data-ttu-id="8a1b6-109">Un autre exemple est lorsque vous recevez des factures imprimées de fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-109">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="8a1b6-110">Vous pouvez les numériser et les enregistrer au format .pdf sur un site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-110">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="8a1b6-111">Ensuite, vous pouvez créer un lien d'une facture achat dans [!INCLUDE[d365fin_md](includes/d365fin_md.md)] vers la facture correspondante sur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-111">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="8a1b6-112">Vous pouvez aussi créer un lien depuis une fiche article vers la page correspondante du catalogue en ligne de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-112">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="8a1b6-113">Pour ajouter un lien sur un enregistrement</span><span class="sxs-lookup"><span data-stu-id="8a1b6-113">To add a link on a record</span></span>   

1.  <span data-ttu-id="8a1b6-114">Ouvrez l'enregistrement auquel vous voulez ajouter le lien, par exemple une fiche client ou une commande vente.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-114">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="8a1b6-115">Pour associer le lien à une ligne spécifique, par exemple une ligne feuille, sélectionnez la ligne.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-115">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="8a1b6-116">Choisissez l'action **Liens** pour ouvrir les pages **Liens** qui affichent tous les liens actuels qui sont ajoutés à l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-116">Choose the **Links** action to open the **Links** pages that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="8a1b6-117">Pour ajouter un nouveau lien, choisissez **+nouveau**.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-117">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="8a1b6-118">Dans le champ **Adresse du lien**, entrez</span><span class="sxs-lookup"><span data-stu-id="8a1b6-118">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="8a1b6-119">Pour créer un lien vers un fichier sur votre ordinateur ou réseau, entrez le chemin d'accès complet et le nom du fichier, par exemple **C:\Mes documents\invoice1.doc**.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-119">To link to a file on your computer or network, enter the full path and file name, such as  **C:\My Documents\invoice1.doc**.</span></span>
    -   <span data-ttu-id="8a1b6-120">Pour créer un lien vers un site Web, entrez l'adresse Internet (URL), par exemple **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="8a1b6-121">Pour créer un lien vers un programme, entrez une chaîne spécifique pour ouvrir le programme.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-121">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="8a1b6-122">Par exemple, pour ouvrir OneNote avec une page spécifique, entrez **onenote:///C:\Mes documents/test.one**.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-122">For example, to open OneNote with a specific page, enter **onenote:///C:\My Documents/test.one**.</span></span> <span data-ttu-id="8a1b6-123">Ou, pour ouvrir Outlook avec un e-mail vierge à destination d'un alias spécifique, entrez **mailto:testalias** .</span><span class="sxs-lookup"><span data-stu-id="8a1b6-123">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="8a1b6-124">Dans le champ **Désignation**, entrez les informations sur le lien.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-124">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="8a1b6-125">Cliquez sur le bouton **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-125">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="8a1b6-126">Pour supprimer un lien dans un enregistrement</span><span class="sxs-lookup"><span data-stu-id="8a1b6-126">To delete a link from a record</span></span>  

<span data-ttu-id="8a1b6-127">Pour supprimer un lien, sur la page **Liens**, vous pouvez sélectionner **…**, puis **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-127">To delete a link, on the **Links** page, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="8a1b6-128">Si vous supprimez un enregistrement, par exemple, une ligne commande vente, une commande vente ou une fiche client, tous les liens contenus dans l'enregistrement sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-128">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="8a1b6-129">En revanche, si vous supprimez des enregistrements à l'aide d'un traitement par lots, par exemple, le traitement par lots **Supprimer cdes vente facturées**, les liens sont conservés dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-129">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="8a1b6-130">Pour supprimer les liens de la base de données, exécutez le codeunit **Supprimer les liens enregistrement orphelins**.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-130">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="8a1b6-131">Pour cela, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer les liens enregistrement orphelins**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-131">To do this, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="8a1b6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a1b6-132">See Also</span></span>  
<span data-ttu-id="8a1b6-133">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8a1b6-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
