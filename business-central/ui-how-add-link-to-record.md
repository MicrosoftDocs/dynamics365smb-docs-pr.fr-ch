---
title: Ajouter des pièces jointes, des liens et des notes sur des enregistrements | Microsoft Docs
description: Joignez un lien hypertexte pointant vers un document ou un site Web à un enregistrement spécifique, tel qu’une fiche client ou un document.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3acc0113cb14170b84363ab40a803da8b7551c75
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771150"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="80862-103">Gérer les pièces jointes, les liens et les notes sur les fiches et les documents</span><span class="sxs-lookup"><span data-stu-id="80862-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="80862-104">Dans le Récapitulatif de la plupart des fiches et des documents, vous pouvez joindre des fichiers, ajouter des liens et rédiger des notes.</span><span class="sxs-lookup"><span data-stu-id="80862-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="80862-105">Pour les liens et les notes, vous pouvez également le faire sur la page de liste en sélectionnant d’abord la ligne associée.</span><span class="sxs-lookup"><span data-stu-id="80862-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="80862-106">Pour afficher ou modifier l’un de ces types d’informations jointes, vous devez d’abord ouvrir l’onglet **Pièces jointes** dans le Récapitulatif.</span><span class="sxs-lookup"><span data-stu-id="80862-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="80862-107">Le nombre situé derrière le titre de l’onglet indique le nombre de fichiers, liens ou notes attachés existants pour la fiche ou le document.</span><span class="sxs-lookup"><span data-stu-id="80862-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="80862-108">Les pièces jointes, les liens et les notes restent attachés au fur et à mesure du traitement de la fiche ou du document dans d’autres états, par exemple d’une commande client en cours à une facture client enregistrée.</span><span class="sxs-lookup"><span data-stu-id="80862-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="80862-109">Cependant, aucun type de document joint n’est sorti du système, par exemple lors de l’impression ou de l’enregistrement dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="80862-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="80862-110">Lorsque vous expédiez et facturez partiellement une commande vente ou achat, le document joint ne sera annexé qu’à la facture finale de cette commande.</span><span class="sxs-lookup"><span data-stu-id="80862-110">When you partially ship and invoice a sales or purchase order, the attachment will only be attached to the final invoice of the order.</span></span> <span data-ttu-id="80862-111">De même, lorsque vous facturez à l’aide de la fonction Reports, le document joint est annexé aux écritures comptables pour le document, mais pas pour les écritures report.</span><span class="sxs-lookup"><span data-stu-id="80862-111">Similarly, when you invoice using the Deferrals feature, the attachment is attached to the G/L entries for the document but not for the deferral entries.</span></span>
>
> <span data-ttu-id="80862-112">Si vous supprimez une commande avant qu'elle ne soit facturée, la pièce jointe est également supprimée.</span><span class="sxs-lookup"><span data-stu-id="80862-112">If you delete an order before it is invoiced, the attachment is also removed.</span></span> <span data-ttu-id="80862-113">Lorsque vous facturez des commandes achat à l'aide de l'action Obtenir des lignes de réception à partir d'une facture achat, la pièce jointe sur les commandes achat n'est pas ajoutée à la facture achat.</span><span class="sxs-lookup"><span data-stu-id="80862-113">When you invoice purchase orders using the Get Receipt Lines action from a purchase invoice, the attachment on the purchase orders is not added to the purchase invoice.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="80862-114">Pour joindre un fichier à une facture achat</span><span class="sxs-lookup"><span data-stu-id="80862-114">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="80862-115">Vous pouvez joindre tout type de fichier contenant du texte, des images ou des vidéos à une fiche ou à un document.</span><span class="sxs-lookup"><span data-stu-id="80862-115">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="80862-116">Ceci est utile, par exemple, lorsque vous souhaitez stocker la facture d’un fournisseur sous forme de fichier PDF sur la facture achat correspondante dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="80862-116">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="80862-117">Les fichiers joints à la fonction Documents entrants ne sont pas inclus dans l’onglet **Pièces jointes**. Pour plus d’informations, voir [Documents entrants](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="80862-117">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="80862-118">La procédure suivante se base sur une facture achat.</span><span class="sxs-lookup"><span data-stu-id="80862-118">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="80862-119">Les étapes sont similaires pour tous les autres documents et fiches pris en charge.</span><span class="sxs-lookup"><span data-stu-id="80862-119">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="80862-120">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures achat**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="80862-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="80862-121">Ouvrez les commandes ventes auxquelles vous souhaitez joindre un fichier.</span><span class="sxs-lookup"><span data-stu-id="80862-121">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="80862-122">Dans le Récapitulatif, ouvrez l’onglet **Pièces jointes**.</span><span class="sxs-lookup"><span data-stu-id="80862-122">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="80862-123">Choisissez la valeur associée au champ **Documents**, telle que « 0 ».</span><span class="sxs-lookup"><span data-stu-id="80862-123">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="80862-124">Sur la page **Documents joints**, dans le champ **Pièce jointe**, choisissez l’action **Sélectionner un fichier**.</span><span class="sxs-lookup"><span data-stu-id="80862-124">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** action.</span></span>
5. <span data-ttu-id="80862-125">Sélectionnez un fichier à n’importe quel emplacement, puis choisissez le bouton **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="80862-125">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="80862-126">Le fichier est désormais joint à la facture achat.</span><span class="sxs-lookup"><span data-stu-id="80862-126">The file is now attached to the purchase invoice.</span></span>

## <a name="to-view-an-attached-file"></a><span data-ttu-id="80862-127">Pour afficher un fichier joint</span><span class="sxs-lookup"><span data-stu-id="80862-127">To view an attached file</span></span>
1. <span data-ttu-id="80862-128">Dans le Récapitulatif, ouvrez l’onglet **Pièces jointes**.</span><span class="sxs-lookup"><span data-stu-id="80862-128">In the FactBox, open the **Attachments** tab.</span></span>
2. <span data-ttu-id="80862-129">Choisissez la valeur associée au champ **Documents**, telle que « 1 ».</span><span class="sxs-lookup"><span data-stu-id="80862-129">Choose the value behind the **Documents** field, such as "1".</span></span>
3. <span data-ttu-id="80862-130">Sur la page **Documents joints**, sélectionnez l’action **Aperçu**.</span><span class="sxs-lookup"><span data-stu-id="80862-130">On the **Attached Documents** page, choose the **Preview** action.</span></span>
4. <span data-ttu-id="80862-131">Ouvrez le fichier téléchargé.</span><span class="sxs-lookup"><span data-stu-id="80862-131">Open the downloaded file.</span></span>

## <a name="to-save-a-document-as-a-pdf-attachment"></a><span data-ttu-id="80862-132">Pour enregistrer un document en tant que pièce jointe PDF</span><span class="sxs-lookup"><span data-stu-id="80862-132">To save a document as a PDF attachment</span></span>
<span data-ttu-id="80862-133">Chaque fois que vous devez enregistrer un document en tant que fichier, vous pouvez utiliser l’action **Joindre en tant que PDF** pour capturer le contenu actuel du document sous forme de fichier PDF joint au récapitulatif du document.</span><span class="sxs-lookup"><span data-stu-id="80862-133">Whenever you need to save a document as a file, you can use the **Attach as PDF** action to capture the current document content as a PDF file attached to the FactBox of the document.</span></span> <span data-ttu-id="80862-134">Cela est utile, par exemple, lorsque des documents suivent plusieurs étapes d’un processus, comme un processus de vente ou un flux de travail approbation, et que vous souhaitez vous référer à une impression de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="80862-134">This is useful, for example, when documents follow multiple steps in a process, such as a sales process or an approval workflow, and you want to refer to a printout of the previous step.</span></span>

<span data-ttu-id="80862-135">La procédure suivante se base sur une commande vente.</span><span class="sxs-lookup"><span data-stu-id="80862-135">The following procedure is based on a sales order.</span></span> <span data-ttu-id="80862-136">Les étapes sont similaires pour tous les autres documents pris en charge.</span><span class="sxs-lookup"><span data-stu-id="80862-136">The steps are similar for all supported documents.</span></span>

1. <span data-ttu-id="80862-137">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="80862-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="80862-138">Sélectionnez une commande vente, puis l’action **Joindre en tant que PDF**.</span><span class="sxs-lookup"><span data-stu-id="80862-138">Select a sales order, and then choose the **Attach as PDF** action.</span></span>

<span data-ttu-id="80862-139">Un fichier PDF avec le contenu actuel de la commande vente est ajouté à l’onglet **Pièces jointes** du récapitulatif.</span><span class="sxs-lookup"><span data-stu-id="80862-139">A PDF file with the current content of the sales order is added to the **Attachments** tab in the FactBox.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="80862-140">Pour ajouter un lien à partir d’une fiche article</span><span class="sxs-lookup"><span data-stu-id="80862-140">To add a link from an item card</span></span>
<span data-ttu-id="80862-141">Vous pouvez ajouter un lien à partir d’une fiche ou d’un document à n’importe quelle URL ou n’importe quel chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="80862-141">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="80862-142">Ceci est utile, par exemple, lorsque vous souhaitez lier une fiche article au catalogue d’articles du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="80862-142">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="80862-143">La procédure suivante se base sur une fiche article.</span><span class="sxs-lookup"><span data-stu-id="80862-143">The following procedure is based on an item card.</span></span> <span data-ttu-id="80862-144">Les étapes sont similaires pour toutes les autres fiches et tous les documents pris en charge.</span><span class="sxs-lookup"><span data-stu-id="80862-144">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="80862-145">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="80862-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="80862-146">Sélectionnez l’article à partir duquel vous souhaitez ajouter un lien, puis choisissez l’onglet **Pièces jointes** dans le Récapitulatif.</span><span class="sxs-lookup"><span data-stu-id="80862-146">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="80862-147">Dans la section **Liens**, choisissez l’icône **+**.</span><span class="sxs-lookup"><span data-stu-id="80862-147">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="80862-148">Entrez le lien dans le champ **Adresse du lien**.</span><span class="sxs-lookup"><span data-stu-id="80862-148">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="80862-149">Le lien doit être une URL Internet ou intranet valide.</span><span class="sxs-lookup"><span data-stu-id="80862-149">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="80862-150">Dans le champ **Description**, entrez les informations sur le lien.</span><span class="sxs-lookup"><span data-stu-id="80862-150">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="80862-151">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="80862-151">Choose the **OK** button.</span></span>

<span data-ttu-id="80862-152">Le lien est maintenant attaché à la fiche article.</span><span class="sxs-lookup"><span data-stu-id="80862-152">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="80862-153">Pour écrire une note sur une commande client</span><span class="sxs-lookup"><span data-stu-id="80862-153">To write a note on a sales order</span></span>
<span data-ttu-id="80862-154">Vous pouvez écrire une note sur un document ou une ficher, par exemple pour communiquer des instructions spéciales aux autres utilisateurs du document ou de la fiche.</span><span class="sxs-lookup"><span data-stu-id="80862-154">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="80862-155">Vous pouvez inclure des liens et des URL de fichier dans les notes.</span><span class="sxs-lookup"><span data-stu-id="80862-155">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="80862-156">Les notes sur l’onglet **Pièces jointes** ne sont pas liées à la fonctionnalité de notes internes, qui est principalement utilisée pour communiquer entre les utilisateurs de workflows.</span><span class="sxs-lookup"><span data-stu-id="80862-156">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="80862-157">Pour plus d’informations, reportez-vous à [Configuration de notifications de flux de travail](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="80862-157">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="80862-158">La procédure suivante se base sur une commande vente.</span><span class="sxs-lookup"><span data-stu-id="80862-158">The following procedure is based on a sales order.</span></span> <span data-ttu-id="80862-159">Les étapes sont similaires pour tous les autres documents et fiches pris en charge.</span><span class="sxs-lookup"><span data-stu-id="80862-159">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="80862-160">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="80862-160">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="80862-161">Sélectionnez la commande vente pour laquelle vous souhaitez écrire une note, puis choisissez l’onglet **Pièces jointes** dans le Récapitulatif.</span><span class="sxs-lookup"><span data-stu-id="80862-161">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="80862-162">Dans la section **Notes**, choisissez l’icône **+**.</span><span class="sxs-lookup"><span data-stu-id="80862-162">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="80862-163">Dans le champ **Note**, écrivez n’importe quel texte, par exemple « Ceci est une commande urgente ».</span><span class="sxs-lookup"><span data-stu-id="80862-163">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="80862-164">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="80862-164">Choose the **OK** button.</span></span>

<span data-ttu-id="80862-165">La note est maintenant jointe à la commande client.</span><span class="sxs-lookup"><span data-stu-id="80862-165">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="80862-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80862-166">See Also</span></span>  
<span data-ttu-id="80862-167">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="80862-167">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="80862-168">Documents entrants</span><span class="sxs-lookup"><span data-stu-id="80862-168">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="80862-169">Configuration de notifications de workflow</span><span class="sxs-lookup"><span data-stu-id="80862-169">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]