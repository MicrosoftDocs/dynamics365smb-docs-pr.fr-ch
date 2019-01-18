---
title: "Créer des sociétés contact| Microsoft Docs"
description: "Décrit comment créer un contact pour chaque nouvelle société ou société prospect avec laquelle vous collaborez ou entretenez des relations."
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
redirect_url: marketing-create-contact-companies
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 932ae29ff302390962bf9ca4dc48d2d76fce1ca2
ms.contentlocale: fr-ch
ms.lasthandoff: 12/11/2018

---
# <a name="create-contact-companies"></a><span data-ttu-id="7d7c5-103">Création de sociétés contact</span><span class="sxs-lookup"><span data-stu-id="7d7c5-103">Create Contact Companies</span></span>
<span data-ttu-id="7d7c5-104">Vous pouvez créer un contact pour chaque nouvelle société avec laquelle vous êtes en contact, par exemple un client, un fournisseur, un prospect, une banque, un cabinet d'avocats, un consultant, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-104">You can create a contact for each new company you interact with, for example, a customer, vendor, prospective customer, bank, law firm, consultant, and so on.</span></span>

<span data-ttu-id="7d7c5-105">Il existe deux méthodes permettant de créer un contact : à partir de zéro ou à partir d'un client, d'un fournisseur ou d'un compte bancaire existant.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-105">There are two ways to create a contact: from scratch or from an existing customer, vendor, or bank account.</span></span>

<span data-ttu-id="7d7c5-106">Avant de créer un contact, vous pouvez vérifier les paramètres sur la page **Paramètres Marketing**.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-106">Before creating a contact, you may want to check the settings on the **Marketing Setup** page.</span></span> <span data-ttu-id="7d7c5-107">Pour plus d'informations, voir [Paramétrage de la Gestion des relations](marketing-setup-marketing.md).</span><span class="sxs-lookup"><span data-stu-id="7d7c5-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="create-a-company-contact-from-scratch"></a><span data-ttu-id="7d7c5-108">Créer un contact société à partir de zéro</span><span class="sxs-lookup"><span data-stu-id="7d7c5-108">Create a company contact from scratch</span></span>
1. <span data-ttu-id="7d7c5-109">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Contacts**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d7c5-110">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-110">Choose the **New** action.</span></span>
3. <span data-ttu-id="7d7c5-111">Dans le champ **N°**, saisissez le numéro du contact.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-111">In the **No. field**, enter a number for the contact.</span></span>

    <span data-ttu-id="7d7c5-112">Si vous avez configuré une souche de numéros pour les contacts sur la page **Paramètres Marketing**, appuyez sur la touche Entrée pour sélectionner le numéro de contact suivant.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-112">Alternatively, if you have set up a number series for contacts on the **Marketing Setup** page, you can press the Enter key to select the next available contact number.</span></span>  
4. <span data-ttu-id="7d7c5-113">Définissez **Type** à **Société**.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-113">Set **Type** to **Company**.</span></span>
5. <span data-ttu-id="7d7c5-114">Renseignez les autres champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-114">Fill in the other fields as required.</span></span>

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a><span data-ttu-id="7d7c5-115">Pour créer un contact société à partir d'un client, d'un fournisseur ou d'un compte bancaire</span><span class="sxs-lookup"><span data-stu-id="7d7c5-115">To create a company contact from a customer, vendor, or bank account</span></span>
<span data-ttu-id="7d7c5-116">Si vous avez configuré plusieurs clients, fournisseurs et comptes bancaires, vous pouvez créer des contacts sur la base des données existantes.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-116">If you have already set up a number of customers, vendors, and bank accounts, you can create contacts on the basis of the existing data.</span></span> <span data-ttu-id="7d7c5-117">Lorsque vous créez un contact de cette façon, les informations de contact sont synchronisées avec les informations du client, du fournisseur ou du compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-117">When you create a contact this way, the contact information is synchronized with the customer, vendor, or bank account information.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7d7c5-118">Avant de créer des sociétés contact de cette manière, vous devez spécifier un code relation d'affaires pour les clients, les fournisseurs, ainsi que des comptes bancaires sur la page **Paramètres marketing**.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-118">Before you can create contact companies this way, you must specify a business relation code for customers, vendors, and bank accounts on the **Marketing Setup** page.</span></span> <span data-ttu-id="7d7c5-119">Si vous devez créer des contacts à partir de comptes bancaires, vous devez également spécifier des souches de numéros pour les comptes bancaires sur la page **Paramètres comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-119">If you will be creating contacts from a bank accounts, you must also specify numbers series for bank accounts on the **General Ledger Setup** page.</span></span>

1. <span data-ttu-id="7d7c5-120">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez une des actions suivantes, selon l'emplacement à partir duquel vous souhaitez créer des contacts, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter one of the following, depending on from where you want to create contacts, and then choose the related link.</span></span>
   * <span data-ttu-id="7d7c5-121">**Créer contacts à partir des clients**</span><span class="sxs-lookup"><span data-stu-id="7d7c5-121">**Create Contacts from Customers**</span></span>
   * <span data-ttu-id="7d7c5-122">**Créer des contacts à partir des fournisseurs**</span><span class="sxs-lookup"><span data-stu-id="7d7c5-122">**Create Contacts from Vendors**</span></span>
   * <span data-ttu-id="7d7c5-123">**Créer des contacts à partir des comptes bancaires**</span><span class="sxs-lookup"><span data-stu-id="7d7c5-123">**Create Contacts from Bank Accounts**</span></span>
2. <span data-ttu-id="7d7c5-124">Sur la page de traitement par lots qui s'affiche, dans la section **Client**, **Fournisseur** ou **Compte bancaire**, définissez des filtres si vous souhaitez créer des contacts à partir de clients, de fournisseurs ou de comptes bancaires spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-124">In the batch job page that opens, in the **Customer**, **Vendor**, or **Bank Account** section, set filters if you want to create contacts from specific customers, vendors, or bank accounts.</span></span>
3. <span data-ttu-id="7d7c5-125">Pour démarrer la création de contacts, cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-125">Choose the **OK** button to start creating contacts.</span></span>

    <span data-ttu-id="7d7c5-126">Les numéros de contact suivants de la souche de numéros sont affectés aux nouveaux contacts.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-126">The next contact numbers in the number series are assigned to the new contacts.</span></span> <span data-ttu-id="7d7c5-127">La relation d'affaires des fournisseurs qui est spécifiée sur la page **Paramètres Marketing** est affectée aux contacts nouvellement créés.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-127">The business relation for vendors that is specified on the **Marketing Setup** page is assigned to the newly created contacts.</span></span>

> [!TIP]  
>   <span data-ttu-id="7d7c5-128">Vous pouvez également créer un client, un fournisseur ou un compte bancaire à partir d'un contact.</span><span class="sxs-lookup"><span data-stu-id="7d7c5-128">You can also create a customer, vendor, or bank account from a contact.</span></span> <span data-ttu-id="7d7c5-129">Pour plus d'informations, reportez-vous à [Créer un client, un fournisseur ou un compte bancaire à partir d'un contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="7d7c5-129">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7d7c5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d7c5-130">See Also</span></span>
[<span data-ttu-id="7d7c5-131">Synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="7d7c5-131">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="7d7c5-132">Affecter des relations d'affaires à un contact</span><span class="sxs-lookup"><span data-stu-id="7d7c5-132">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="7d7c5-133">Affecter des secteurs d'activité à un contact</span><span class="sxs-lookup"><span data-stu-id="7d7c5-133">Assign Industry Groups to a Contact</span></span>](marketing-industry-groups.md#AssignIndustryGroupContact)  
[<span data-ttu-id="7d7c5-134">Affecter des groupes de distribution à un contact</span><span class="sxs-lookup"><span data-stu-id="7d7c5-134">Assign Mailing Groups to a Contact</span></span>](marketing-mailing-groups.md#AssignMailGroupContact)  
[<span data-ttu-id="7d7c5-135">Création de personnes contact</span><span class="sxs-lookup"><span data-stu-id="7d7c5-135">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="7d7c5-136">Utilisation de Business Central</span><span class="sxs-lookup"><span data-stu-id="7d7c5-136">Working with Business Central</span></span>](ui-work-product.md)

