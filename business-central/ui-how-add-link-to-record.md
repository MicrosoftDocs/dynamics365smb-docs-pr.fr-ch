---
title: Ajouter des pièces jointes, des liens et des notes sur des enregistrements | Microsoft Docs
description: Joignez un lien hypertexte pointant vers un document ou un site Web à un enregistrement spécifique, tel qu'une fiche client ou un document.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 84d58193fa7ee272b372403d63702348fbfb1f77
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315291"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="26ef7-103">Gérer les pièces jointes, les liens et les notes sur les fiches et les documents</span><span class="sxs-lookup"><span data-stu-id="26ef7-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="26ef7-104">Dans le Récapitulatif de la plupart des fiches et des documents, vous pouvez joindre des fichiers, ajouter des liens et rédiger des notes.</span><span class="sxs-lookup"><span data-stu-id="26ef7-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="26ef7-105">Pour les liens et les notes, vous pouvez également le faire sur la page de liste en sélectionnant d’abord la ligne associée.</span><span class="sxs-lookup"><span data-stu-id="26ef7-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="26ef7-106">Pour afficher ou modifier l’un de ces types d’informations jointes, vous devez d’abord ouvrir l'onglet **Pièces jointes** dans le Récapitulatif.</span><span class="sxs-lookup"><span data-stu-id="26ef7-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="26ef7-107">Le nombre situé derrière le titre de l'onglet indique le nombre de fichiers, liens ou notes attachés existants pour la fiche ou le document.</span><span class="sxs-lookup"><span data-stu-id="26ef7-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="26ef7-108">Les pièces jointes, les liens et les notes restent attachés au fur et à mesure du traitement de la fiche ou du document dans d'autres états, par exemple d'une commande client en cours à une facture client enregistrée.</span><span class="sxs-lookup"><span data-stu-id="26ef7-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="26ef7-109">Notez cependant qu'aucun type de pièce jointe n'est sorti du système, par exemple lors de l'impression ou de l'enregistrement dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="26ef7-109">Note, however, that none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="26ef7-110">Pour joindre un fichier à une facture achat</span><span class="sxs-lookup"><span data-stu-id="26ef7-110">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="26ef7-111">Vous pouvez joindre tout type de fichier contenant du texte, des images ou des vidéos à une fiche ou à un document.</span><span class="sxs-lookup"><span data-stu-id="26ef7-111">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="26ef7-112">Ceci est utile, par exemple, lorsque vous souhaitez stocker la facture d’un fournisseur sous forme de fichier PDF sur la facture achat correspondante dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="26ef7-112">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="26ef7-113">Les fichiers joints à la fonction Documents entrants ne sont pas inclus dans l'onglet **Pièces jointes**. Pour plus d'informations, voir [Documents entrants](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="26ef7-113">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="26ef7-114">La procédure suivante se base sur une commande vente.</span><span class="sxs-lookup"><span data-stu-id="26ef7-114">The following procedure is based on a sales order.</span></span> <span data-ttu-id="26ef7-115">Les étapes sont similaires pour tous les autres documents et fiches pris en charge.</span><span class="sxs-lookup"><span data-stu-id="26ef7-115">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="26ef7-116">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures achat**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="26ef7-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="26ef7-117">Ouvrez les commandes ventes auxquelles vous souhaitez joindre un fichier.</span><span class="sxs-lookup"><span data-stu-id="26ef7-117">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="26ef7-118">Dans le Récapitulatif, ouvrez l'onglet **Pièces jointes**.</span><span class="sxs-lookup"><span data-stu-id="26ef7-118">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="26ef7-119">Choisissez la valeur associée au champ **Documents**, telle que « 0 ».</span><span class="sxs-lookup"><span data-stu-id="26ef7-119">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="26ef7-120">Sur la page **Documents joints**, dans le champ **Pièce jointe**, choisissez le bouton **Sélectionner un fichier**.</span><span class="sxs-lookup"><span data-stu-id="26ef7-120">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="26ef7-121">Sélectionnez un fichier à n'importe quel emplacement, puis choisissez le bouton **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="26ef7-121">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="26ef7-122">Le fichier est désormais joint à la facture achat.</span><span class="sxs-lookup"><span data-stu-id="26ef7-122">The file is now attached to the purchase invoice.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="26ef7-123">Pour ajouter un lien à partir d'une fiche article</span><span class="sxs-lookup"><span data-stu-id="26ef7-123">To add a link from an item card</span></span>
<span data-ttu-id="26ef7-124">Vous pouvez ajouter un lien à partir d'une fiche ou d'un document à n’importe quelle URL ou n’importe quel chemin d'accès.</span><span class="sxs-lookup"><span data-stu-id="26ef7-124">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="26ef7-125">Ceci est utile, par exemple, lorsque vous souhaitez lier une fiche article au catalogue d'articles du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="26ef7-125">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="26ef7-126">La procédure suivante se base sur une fiche article.</span><span class="sxs-lookup"><span data-stu-id="26ef7-126">The following procedure is based on an item card.</span></span> <span data-ttu-id="26ef7-127">Les étapes sont similaires pour toutes les autres fiches et tous les documents pris en charge.</span><span class="sxs-lookup"><span data-stu-id="26ef7-127">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="26ef7-128">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="26ef7-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="26ef7-129">Sélectionnez l'article à partir duquel vous souhaitez ajouter un lien, puis choisissez l'onglet **Pièces jointes** dans le Récapitulatif.</span><span class="sxs-lookup"><span data-stu-id="26ef7-129">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="26ef7-130">Dans la section **Liens**, choisissez l'icône **+**.</span><span class="sxs-lookup"><span data-stu-id="26ef7-130">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="26ef7-131">Entrez le lien dans le champ **Adresse du lien**.</span><span class="sxs-lookup"><span data-stu-id="26ef7-131">In the **Link Address** field, enter the link.</span></span>

    - <span data-ttu-id="26ef7-132">Pour créer un lien vers un fichier sur votre ordinateur ou réseau, entrez le chemin d'accès complet et le nom du fichier, par exemple **C:\Mes documents\invoice1.doc**.</span><span class="sxs-lookup"><span data-stu-id="26ef7-132">To link to a file on your computer or network, enter the full path and file name, such as **C:\My Documents\invoice1.doc**.</span></span>
    - <span data-ttu-id="26ef7-133">Pour créer un lien vers un site Web, entrez l'adresse Internet (URL), par exemple **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="26ef7-133">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    - <span data-ttu-id="26ef7-134">Pour créer un lien vers un programme, entrez une chaîne spécifique pour ouvrir le programme.</span><span class="sxs-lookup"><span data-stu-id="26ef7-134">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="26ef7-135">Par exemple, pour ouvrir Outlook avec un e-mail vierge à destination d'un alias spécifique, entrez **mailto:testalias** .</span><span class="sxs-lookup"><span data-stu-id="26ef7-135">For example, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5. <span data-ttu-id="26ef7-136">Dans le champ **Description**, entrez les informations sur le lien.</span><span class="sxs-lookup"><span data-stu-id="26ef7-136">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="26ef7-137">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="26ef7-137">Choose the **OK** button.</span></span>

<span data-ttu-id="26ef7-138">Le lien est maintenant attaché à la fiche article.</span><span class="sxs-lookup"><span data-stu-id="26ef7-138">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="26ef7-139">Pour écrire une note sur une commande client</span><span class="sxs-lookup"><span data-stu-id="26ef7-139">To write a note on a sales order</span></span>
<span data-ttu-id="26ef7-140">Vous pouvez écrire une note sur un document ou une ficher, par exemple pour communiquer des instructions spéciales aux autres utilisateurs du document ou de la fiche.</span><span class="sxs-lookup"><span data-stu-id="26ef7-140">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="26ef7-141">Vous pouvez inclure des liens et des URL de fichier dans les notes.</span><span class="sxs-lookup"><span data-stu-id="26ef7-141">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="26ef7-142">Les notes sur l'onglet **Pièces jointes** ne sont pas liées à la fonctionnalité de notes internes, qui est principalement utilisée pour communiquer entre les utilisateurs de workflows.</span><span class="sxs-lookup"><span data-stu-id="26ef7-142">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="26ef7-143">Pour plus d'informations, reportez-vous à [Configuration de notifications de flux de travail](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="26ef7-143">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="26ef7-144">La procédure suivante se base sur une commande vente.</span><span class="sxs-lookup"><span data-stu-id="26ef7-144">The following procedure is based on a sales order.</span></span> <span data-ttu-id="26ef7-145">Les étapes sont similaires pour tous les autres documents et fiches pris en charge.</span><span class="sxs-lookup"><span data-stu-id="26ef7-145">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="26ef7-146">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="26ef7-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="26ef7-147">Sélectionnez la commande vente pour laquelle vous souhaitez écrire une note, puis choisissez l'onglet **Pièces jointes** dans le Récapitulatif.</span><span class="sxs-lookup"><span data-stu-id="26ef7-147">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="26ef7-148">Dans la section **Notes**, choisissez l'icône **+**.</span><span class="sxs-lookup"><span data-stu-id="26ef7-148">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="26ef7-149">Dans le champ **Note**, écrivez n’importe quel texte, par exemple « Ceci est une commande urgente ».</span><span class="sxs-lookup"><span data-stu-id="26ef7-149">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="26ef7-150">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="26ef7-150">Choose the **OK** button.</span></span>

<span data-ttu-id="26ef7-151">La note est maintenant jointe à la commande client.</span><span class="sxs-lookup"><span data-stu-id="26ef7-151">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="26ef7-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26ef7-152">See Also</span></span>  
<span data-ttu-id="26ef7-153">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26ef7-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="26ef7-154">Documents entrants</span><span class="sxs-lookup"><span data-stu-id="26ef7-154">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="26ef7-155">Configuration de notifications de workflow</span><span class="sxs-lookup"><span data-stu-id="26ef7-155">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
