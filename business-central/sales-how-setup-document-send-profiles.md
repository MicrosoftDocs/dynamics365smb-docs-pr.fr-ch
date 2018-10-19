---
title: "Paramétrer les méthodes préférées d'envoi des documents vente | Microsoft Docs"
description: "Décrit comment configurer la méthode préférée de chaque client pour l'envoi de documents vente, par exemple par e-mail, au format PDF, sous forme de document électronique, etc."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c18edefc22d96f2c4037f7f51cca488e04c35d92
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-document-sending-profiles"></a><span data-ttu-id="a5602-103">Configurer des profils d'envoi de documents</span><span class="sxs-lookup"><span data-stu-id="a5602-103">Set Up Document Sending Profiles</span></span>
<span data-ttu-id="a5602-104">Vous pouvez associer chaque client avec une méthode par défaut d'envoi de documents vente, afin d'éviter d'avoir à sélectionner une option d'envoi chaque fois que vous sélectionnez l'action **Valider et envoyer**.</span><span class="sxs-lookup"><span data-stu-id="a5602-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="a5602-105">Dans la fenêtre **Profils d'envoi de documents**, configurez différents profils d'envoi que vous pouvez sélectionner dans le champ **Profil d'envoi de documents** d'une fiche client.</span><span class="sxs-lookup"><span data-stu-id="a5602-105">In the **Document Sending Profiles** window, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="a5602-106">Vous pouvez cocher la case **Par défaut** pour spécifier que le profil d'envoi du document est le profil par défaut pour tous les clients, sauf pour les clients dont le champ **Profil d'envoi de documents** est renseigné avec un autre profil d'envoi.</span><span class="sxs-lookup"><span data-stu-id="a5602-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="a5602-107">Lorsque vous sélectionnez l'action **Valider et envoyer** dans un document vente, la boîte de dialogue **Valider et envoyer la confirmation** affiche le profil d'envoi utilisé, soit celui créé pour le client, soit le profil par défaut pour tous les clients.</span><span class="sxs-lookup"><span data-stu-id="a5602-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="a5602-108">Dans la boîte de dialogue, vous pouvez modifier le profil d'envoi du document vente.</span><span class="sxs-lookup"><span data-stu-id="a5602-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="a5602-109">Pour plus d'informations, reportez-vous à [Facturer des ventes](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="a5602-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="a5602-110">Configurer un profil d'envoi de documents</span><span class="sxs-lookup"><span data-stu-id="a5602-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="a5602-111">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Profils d'envoi de documents**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="a5602-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="a5602-112">Dans la fenêtre **Profils d'envoi de documents**, sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="a5602-112">In the **Document Sending Profiles** window, choose the **New** action.</span></span>
3. <span data-ttu-id="a5602-113">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="a5602-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="a5602-114">Spécifier un profil d'envoi pour une fiche client</span><span class="sxs-lookup"><span data-stu-id="a5602-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="a5602-115">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Clients**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="a5602-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="a5602-116">Ouvrez la fiche du client pour laquelle vous souhaitez configurer un profil d'envoi.</span><span class="sxs-lookup"><span data-stu-id="a5602-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="a5602-117">Dans le champ **Profil d'envoi de documents**, sélectionnez un profil configuré comme décrit dans la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="a5602-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5602-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5602-118">See Also</span></span>
[<span data-ttu-id="a5602-119">Définition des ventes</span><span class="sxs-lookup"><span data-stu-id="a5602-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="a5602-120">Ventes</span><span class="sxs-lookup"><span data-stu-id="a5602-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="a5602-121">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a5602-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

