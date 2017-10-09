---
title: "Procédure : Vérifier les numéros d'identification intracomm. | Microsoft Docs"
description: "Vous pouvez utiliser un service Web UE pour vérifier que les numéros d'identification intracomm. saisis sur les fiches client, fournisseur ou contact sont valides."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a><span data-ttu-id="df8e9-103">Procédure : Vérifier les numéros d'identification intracomm.</span><span class="sxs-lookup"><span data-stu-id="df8e9-103">How to: Verify VAT Registration Numbers</span></span>
<span data-ttu-id="df8e9-104">Vous pouvez utiliser un service Web UE pour vérifier que les numéros d'identification intracomm. saisis sur les fiches client, fournisseur ou contact sont valides.</span><span class="sxs-lookup"><span data-stu-id="df8e9-104">You can use an EU web service to verify that VAT registration numbers that you enter on customer, vendor, or contact cards are valid.</span></span>  

 <span data-ttu-id="df8e9-105">Lorsque vous modifiez le champ **N° identif. intracomm.**d'une fiche pour laquelle la valeur du champ **Code pays/région** est un pays ou une région de l'UE, le nouveau numéro d'identification intra-communautaire et votre code utilisateur sont consignés dans la fenêtre **Journal identif. intracomm.**.</span><span class="sxs-lookup"><span data-stu-id="df8e9-105">When you modify the **VAT Registration No.** field on a card where the value in the **Country/Region Code** field is an EU country/region, then the new VAT registration number and your user ID are logged in the **VAT Registration Log** window.</span></span> <span data-ttu-id="df8e9-106">Vous vérifiez un numéro d'identification intracomm. en choisissant le bouton **Vérifier n° d'identification** de la fenêtre **Journal identif. intracomm.**.</span><span class="sxs-lookup"><span data-stu-id="df8e9-106">You verify a VAT registration number by choosing the **Verify Registration No.** button in the **VAT Registration Log** window.</span></span> <span data-ttu-id="df8e9-107">Une nouvelle ligne est créée chaque fois que vous utilisez la fonction de vérification.</span><span class="sxs-lookup"><span data-stu-id="df8e9-107">A new line is created every time you use the verification function.</span></span> <span data-ttu-id="df8e9-108">Si le numéro a pu être vérifié, le champ **Statut** indique **Valide**.</span><span class="sxs-lookup"><span data-stu-id="df8e9-108">If the number could be verified, the **Status** field contains **Valid**.</span></span> <span data-ttu-id="df8e9-109">Si le numéro n'a pu être vérifié, le champ **Statut** indique **Non valide**, et vous devez modifier le numéro dans le champ **N° identif. intracomm.** de la fiche et lancer une nouvelle fois la fonction de vérification.</span><span class="sxs-lookup"><span data-stu-id="df8e9-109">If the number could not be verified, the **Status** field contains **Invalid**, and you must then change the number in the **VAT Registration No.** field on the card and start the verification function again.</span></span>  

 <span data-ttu-id="df8e9-110">L'URL du service Web par défaut est définie dans le champ **URL de validation de n° id. intracomm.** dans la fenêtre **Paramètres comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="df8e9-110">The URL of the default web service is set up in the **VAT Reg. No. Validation URL** field in the **General Ledger Setup** window.</span></span>  

 <span data-ttu-id="df8e9-111">Dans le tableau **Format n° identif. intracomm.**, vous pouvez modifier pour chaque pays/région les différents formats du numéro d'identification intracomm. que les utilisateurs sont autorisés à saisir dans le champ **N° identif. intracomm.**</span><span class="sxs-lookup"><span data-stu-id="df8e9-111">In the **VAT Registration No. Format** table, you can change for each country/region the different formats of VAT registration number that users are allowed to enter in the **VAT Registration No.** field.</span></span>  

> [!WARNING]  
>  <span data-ttu-id="df8e9-112">Ce service Web utilise le protocole http, ce qui signifie que les données transférées à travers le service ne sont pas cryptées.</span><span class="sxs-lookup"><span data-stu-id="df8e9-112">This web service uses the http protocol, which means that data transferred through the service is not encrypted.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="df8e9-113">Vous pouvez rencontrer des temps d'arrêt pour ce service dont Microsoft n'est pas responsable, étant donné que le service fait partie d'un vaste réseau de l'UE de registres de TVA nationaux.</span><span class="sxs-lookup"><span data-stu-id="df8e9-113">You may experience downtime for this service for which Microsoft is not responsible, as the service is part of a broad EU network of national VAT registers.</span></span>  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a><span data-ttu-id="df8e9-114">Pour vérifier un numéro d'identification intracomm. à partir d'une fiche client</span><span class="sxs-lookup"><span data-stu-id="df8e9-114">To verify a VAT registration number from a customer card</span></span>  
<span data-ttu-id="df8e9-115">Les informations ci-dessous décrivent comment vérifier le numéro d'identification intracommunautaire d'un client.</span><span class="sxs-lookup"><span data-stu-id="df8e9-115">The following describes how to verify a VAT registration number for a customer.</span></span> <span data-ttu-id="df8e9-116">La procédure est identique pour un fournisseur ou un contact.</span><span class="sxs-lookup"><span data-stu-id="df8e9-116">The steps are similar for a vendor and a contact.</span></span>   
1.  <span data-ttu-id="df8e9-117">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="df8e9-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="df8e9-118">Ouvrez la fiche d'un client sur laquelle vous souhaitez vérifier le numéro d'identification intracomm.</span><span class="sxs-lookup"><span data-stu-id="df8e9-118">Open the card of a customer where you want to verify the VAT registration number.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="df8e9-119">Le champ **Code pays/région** de la fiche client doit contenir un pays/une région de l'UE.</span><span class="sxs-lookup"><span data-stu-id="df8e9-119">The **Country/Region Code** field on the customer card must contain an EU country/region.</span></span>  
3.  <span data-ttu-id="df8e9-120">Dans le raccourci **Facturation**, cliquez sur le bouton de zoom en regard du champ **N° identif. intracomm.**</span><span class="sxs-lookup"><span data-stu-id="df8e9-120">On the **Invoicing** FastTab, choose the DrillDown button next to the **VAT Registration No.** field.</span></span>  

    <span data-ttu-id="df8e9-121">La fenêtre **Journal identif. intracomm.** s'ouvre en affichant une ligne sur laquelle le champ **Statut** indique **Non vérifié**.</span><span class="sxs-lookup"><span data-stu-id="df8e9-121">The **VAT Registration Log** window opens showing one line where the **Status** field contains **Not Verified**.</span></span>  
4.  <span data-ttu-id="df8e9-122">Choisissez l'action **Vérifier n° d'identification**.</span><span class="sxs-lookup"><span data-stu-id="df8e9-122">Choose the **Verify Registration No.** action.</span></span>  

     <span data-ttu-id="df8e9-123">Une nouvelle ligne est créée si le champ **Statut** indique **Valide** ou **Non valide**.</span><span class="sxs-lookup"><span data-stu-id="df8e9-123">A new line is created where the **Status** field contains either **Valid** or **Invalid**.</span></span>  
5.  <span data-ttu-id="df8e9-124">Si le champ **Statut** indique **Non valide**, modifiez le numéro dans le champ **N° identif. intracomm.** sur la fiche, puis répétez les étapes 3 à 4.</span><span class="sxs-lookup"><span data-stu-id="df8e9-124">If the **Status** field contains **Invalid**, change the number in the **VAT Registration No.** field on the card, and then repeat steps 3 through 4.</span></span>  

## <a name="see-also"></a><span data-ttu-id="df8e9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df8e9-125">See Also</span></span>  
[<span data-ttu-id="df8e9-126">Finances</span><span class="sxs-lookup"><span data-stu-id="df8e9-126">Finance</span></span>](finance.md)  
[<span data-ttu-id="df8e9-127">Procédure : enregistrer de nouveaux clients</span><span class="sxs-lookup"><span data-stu-id="df8e9-127">How to: Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="df8e9-128">Procédure : enregistrer de nouveaux fournisseurs</span><span class="sxs-lookup"><span data-stu-id="df8e9-128">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="df8e9-129">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="df8e9-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

