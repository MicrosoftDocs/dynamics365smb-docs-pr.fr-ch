---
title: "Gérer les interactions avec vos contacts| Microsoft Docs"
description: "Vous pouvez gérer tous les types de communication ou d'interactions entre votre société et vos contacts. Par exemple, une communication par lettre, par téléphone, lors de réunions, etc."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6fb3c1a19626c4cfa078f030a387e314ae2e0480
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="managing-interactions-with-contacts"></a><span data-ttu-id="d53ef-103">Gestion des interactions avec les contacts</span><span class="sxs-lookup"><span data-stu-id="d53ef-103">Managing Interactions With Contacts</span></span>
<span data-ttu-id="d53ef-104">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les interactions désignent tous les types de communication entre votre société et vos contacts.</span><span class="sxs-lookup"><span data-stu-id="d53ef-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], interactions are all types of communications between your company and your contacts.</span></span> <span data-ttu-id="d53ef-105">Par exemple, les communications peuvent s'effectuer par lettre, par e-mail, par télécopie,par téléphone, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="d53ef-105">For example, communications can be by letter, fax, email, telephone, meetings, and so on.</span></span>

<span data-ttu-id="d53ef-106">Le module de gestion des relations vous permet d'enregistrer toutes les interactions vente et marketing avec vos contacts afin d'effectuer le suivi des efforts mis en œuvre, et d'améliorer vos futures relations commerciales.</span><span class="sxs-lookup"><span data-stu-id="d53ef-106">The relationship management area enables you to record all the interactions you have with your contacts in order to keep track of the sales and marketing efforts you have directed at your contacts and to improve your future business interactions with them.</span></span> <span data-ttu-id="d53ef-107">La configuration de votre application pour enregistrer les interactions est constituée des tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="d53ef-107">Setting up your application to record interactions consists of these tasks:</span></span>

* <span data-ttu-id="d53ef-108">Configuration de modèles interaction</span><span class="sxs-lookup"><span data-stu-id="d53ef-108">Setting up interaction templates</span></span>  
* <span data-ttu-id="d53ef-109">Création d'interactions sur les contacts ou les segments</span><span class="sxs-lookup"><span data-stu-id="d53ef-109">Creating interactions on contacts or segments</span></span>  
* <span data-ttu-id="d53ef-110">Affichage et gestion des interactions enregistrées</span><span class="sxs-lookup"><span data-stu-id="d53ef-110">View and manage recorded interactions</span></span>  

##  <a name="setting-up-interaction-templates"></a><span data-ttu-id="d53ef-111">Configuration de modèles interaction</span><span class="sxs-lookup"><span data-stu-id="d53ef-111">Setting up Interaction Templates</span></span>
<span data-ttu-id="d53ef-112">Pour pouvoir créer et enregistrer des interactions, vous devez configurer des modèles interaction.</span><span class="sxs-lookup"><span data-stu-id="d53ef-112">Before you can create and record interactions, you must set up interaction templates.</span></span> <span data-ttu-id="d53ef-113">Lorsque vous créez des interactions, vous devez spécifier les modèles sur lesquels elles sont basées.</span><span class="sxs-lookup"><span data-stu-id="d53ef-113">When creating interactions, you must specify the interaction templates they are based on.</span></span> <span data-ttu-id="d53ef-114">Un modèle interaction est un prototype qui définit les caractéristiques de base d'une interaction.</span><span class="sxs-lookup"><span data-stu-id="d53ef-114">An interaction template is a model that defines the basic characteristics of an interaction.</span></span>
<span data-ttu-id="d53ef-115">Vous pouvez configurer un modèle interaction dans la fenêtre **Modèles interaction**.</span><span class="sxs-lookup"><span data-stu-id="d53ef-115">You set up an interaction template in the **Interaction Templates** window.</span></span>

<span data-ttu-id="d53ef-116">Une fois les données relatives au modèle interaction saisies, vous pouvez créer un document joint, par exemple un document Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="d53ef-116">After you have entered information about the interaction template, you can create an attachment, for example, a Microsoft Word document.</span></span> <span data-ttu-id="d53ef-117">Répétez les étapes pour chaque modèle interaction à configurer.</span><span class="sxs-lookup"><span data-stu-id="d53ef-117">Repeat the steps to set up as many interaction templates as you want.</span></span>  

## <a name="creating-interactions"></a><span data-ttu-id="d53ef-118">Création d'interactions</span><span class="sxs-lookup"><span data-stu-id="d53ef-118">Creating Interactions</span></span>
<span data-ttu-id="d53ef-119">Il existe deux méthodes d'enregistrement des interactions :</span><span class="sxs-lookup"><span data-stu-id="d53ef-119">There are two ways of recording interactions:</span></span>

* <span data-ttu-id="d53ef-120">Créez manuellement des interactions liées à un contact unique ou à un segment.</span><span class="sxs-lookup"><span data-stu-id="d53ef-120">You can manually create interactions that are linked to a single contact or to a segment.</span></span> <span data-ttu-id="d53ef-121">Pour plus d'informations, reportez-vous à [Créer des interactions sur les contacts et les segments](marketing-how-create-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="d53ef-121">For more information, see [Create Interactions on Contacts and Segments](marketing-how-create-interactions.md).</span></span>  
* <span data-ttu-id="d53ef-122">Vous pouvez enregistrer automatiquement les interactions lorsque vous effectuez des opérations dans l'application, telles que l'impression d'une facture ou d'un devis.</span><span class="sxs-lookup"><span data-stu-id="d53ef-122">You can automatically record interactions when you perform actions in the application, for example, when you print an invoice, or quote.</span></span> <span data-ttu-id="d53ef-123">Pour plus d'informations, reportez-vous à [Enregistrer automatiquement les interactions avec les contacts](marketing-auto-record-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="d53ef-123">For more information, see [Automatically Record Interactions with Contacts](marketing-auto-record-interactions.md).</span></span>

## <a name="viewing-and-managing-recorded-interactions"></a><span data-ttu-id="d53ef-124">Affichage et gestion des interactions enregistrées</span><span class="sxs-lookup"><span data-stu-id="d53ef-124">Viewing and Managing Recorded Interactions</span></span>
<span data-ttu-id="d53ef-125">Dans la fenêtre **Écritures journal interaction**, vous pouvez afficher toutes les interactions enregistrées qui n'ont pas été supprimées.</span><span class="sxs-lookup"><span data-stu-id="d53ef-125">You can view all the recorded interactions that have not been deleted in the **Interaction Log Entries** window.</span></span> <span data-ttu-id="d53ef-126">Vous pouvez ouvrir cette fenêtre de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="d53ef-126">You can open this window by:</span></span>

* <span data-ttu-id="d53ef-127">À l'aide de l'icône **Page ou état pour la recherche** pour effectuer des recherches sur **Écritures journal interaction**.</span><span class="sxs-lookup"><span data-stu-id="d53ef-127">Using the **Search for Page or Report** icon to search on **Interaction Log Entries**.</span></span>
* <span data-ttu-id="d53ef-128">En sélectionnant l'action **Écritures journal interaction** sur un contact ou un segment.</span><span class="sxs-lookup"><span data-stu-id="d53ef-128">Choosing the **Interaction Log Entries** action on a contact or segment.</span></span>
  <span data-ttu-id="d53ef-129">La fenêtre **Écriture journal interaction** répertorie les interactions que vous créez manuellement et celles que l'application enregistre automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d53ef-129">The **Interaction Log Entry** window contains the interactions you create manually and the interactions that the application records automatically.</span></span>

<span data-ttu-id="d53ef-130">Cette fenêtre vous permet d'effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d53ef-130">In this window, you can:</span></span>

* <span data-ttu-id="d53ef-131">Afficher le statut des interactions.</span><span class="sxs-lookup"><span data-stu-id="d53ef-131">View the status of interactions.</span></span>
* <span data-ttu-id="d53ef-132">Marquer les interactions comme annulées.</span><span class="sxs-lookup"><span data-stu-id="d53ef-132">Mark interactions as canceled.</span></span>

<span data-ttu-id="d53ef-133">Vous pouvez supprimer les écritures journal interaction ayant été annulées.</span><span class="sxs-lookup"><span data-stu-id="d53ef-133">You can delete interaction log entries that have been canceled.</span></span> <span data-ttu-id="d53ef-134">Pour supprimer des écritures journal interaction, sélectionnez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Supprimer les écritures journal interaction annulées**, puis sélectionnez le lien connexes et renseignez les informations.</span><span class="sxs-lookup"><span data-stu-id="d53ef-134">To delete interaction log entries, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Canceled Interaction Log Entries**, and then choose the related link, and then fill in the information.</span></span>

## <a name="see-also"></a><span data-ttu-id="d53ef-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d53ef-135">See Also</span></span>
[<span data-ttu-id="d53ef-136">Gestion de contacts</span><span class="sxs-lookup"><span data-stu-id="d53ef-136">Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="d53ef-137">Gestion des opportunités de ventes</span><span class="sxs-lookup"><span data-stu-id="d53ef-137">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="d53ef-138">Utilisation de Business Central</span><span class="sxs-lookup"><span data-stu-id="d53ef-138">Working with Business Central</span></span>](ui-work-product.md)  

