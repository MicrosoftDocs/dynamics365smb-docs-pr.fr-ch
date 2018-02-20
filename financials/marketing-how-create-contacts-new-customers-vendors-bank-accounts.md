---
title: "Créer un client ou un fournisseur à partir d'un contact| Microsoft Docs"
description: "Vous pouvez enregistrer un contact existant comme client, fournisseur, ou compte bancaire à l'aide des données existantes et spécifier une relation d'affaires."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0c4cf74ef7b0b2e48a8608a0859a71b919e46397
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a><span data-ttu-id="b546b-103">Créer un client, un fournisseur ou un compte bancaire à partir d'un contact</span><span class="sxs-lookup"><span data-stu-id="b546b-103">Create a Customer, Vendor, or Bank Account From a Contact</span></span>
<span data-ttu-id="b546b-104">Vous pouvez enregistrer certains de vos contacts existants en tant que clients, fournisseurs ou comptes bancaires.</span><span class="sxs-lookup"><span data-stu-id="b546b-104">You may want to record some of your existing contacts as customers, vendors, or bank accounts.</span></span> <span data-ttu-id="b546b-105">Créer un client, un fournisseur ou un compte bancaire à partir d'un contact vous permet d'utiliser des données existantes.</span><span class="sxs-lookup"><span data-stu-id="b546b-105">Creating a customer, vendor, or bank account from a contact enables you use existing data.</span></span> <span data-ttu-id="b546b-106">Lorsque vous créez un client, un fournisseur ou un compte bancaire de cette façon, celui-ci est synchronisé avec le contact.</span><span class="sxs-lookup"><span data-stu-id="b546b-106">When you create a customer, vendor, or bank account this way, it is synchronized with the contact.</span></span> <span data-ttu-id="b546b-107">Avec la synchronisation les informations communes entre les contacts et les clients, les fournisseurs ou les comptes bancaires sont identiques.</span><span class="sxs-lookup"><span data-stu-id="b546b-107">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>

<span data-ttu-id="b546b-108">Avant de pouvoir enregistrer des contacts de cette manière, vous devez spécifier un code relation d'affaires pour les clients, les fournisseurs et les comptes bancaires dans la fenêtre **Paramètres marketing**.</span><span class="sxs-lookup"><span data-stu-id="b546b-108">Before you can record contacts this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="b546b-109">Si vous devez enregistrer des contacts en tant que comptes bancaires, vous devez également spécifier des souches de numéros pour les comptes bancaires dans la fenêtre **Paramètres comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="b546b-109">If you will be recording contacts as bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a><span data-ttu-id="b546b-110">Pour créer un contact comme client, fournisseur ou compte bancaire</span><span class="sxs-lookup"><span data-stu-id="b546b-110">To create a contact as a customer, vendor, or bank account</span></span>
1. <span data-ttu-id="b546b-111">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Contacts**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="b546b-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="b546b-112">Sélectionnez le contact que vous souhaitez créer comme client, fournisseur ou compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="b546b-112">Select the contact you want to create as a customer, vendor, or bank account.</span></span>
3. <span data-ttu-id="b546b-113">Sélectionnez l'action **Créer comme**, puis sélectionnez **Client**, **Fournisseur** ou **Banque**.</span><span class="sxs-lookup"><span data-stu-id="b546b-113">Choose the **Create As** action, and then choose either **Customer**, **Vendor**, or **Bank**.</span></span>
4. <span data-ttu-id="b546b-114">Répondez par l'affirmative au message qui s'affiche.</span><span class="sxs-lookup"><span data-stu-id="b546b-114">Confirm the subsequent message.</span></span>

<span data-ttu-id="b546b-115">Les informations du contact sont transférées depuis la fiche **Contact** vers la fiche **Compte bancaire**, **Client** ou **Fournisseur**.</span><span class="sxs-lookup"><span data-stu-id="b546b-115">The contact information is transferred from the **Contact** card to the **Bank Account** card, the **Customer** card, or the **Vendor** card.</span></span> <span data-ttu-id="b546b-116">Vous pouvez ajouter des informations spécifiques à chacune des fiches, telles que des informations sur les factures ou les paiements.</span><span class="sxs-lookup"><span data-stu-id="b546b-116">You may want to add specific information to each of the cards, such as invoicing and payment details.</span></span>

## <a name="see-also"></a><span data-ttu-id="b546b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b546b-117">See Also</span></span>
[<span data-ttu-id="b546b-118">Création de sociétés contact</span><span class="sxs-lookup"><span data-stu-id="b546b-118">Create Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="b546b-119">Création de personnes contact</span><span class="sxs-lookup"><span data-stu-id="b546b-119">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="b546b-120">Paramétrage de la Gestion des relations</span><span class="sxs-lookup"><span data-stu-id="b546b-120">Setting Up Relationship Management</span></span>](marketing-setup-marketing.md)  
[<span data-ttu-id="b546b-121">Synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="b546b-121">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="b546b-122">Associer des contacts avec des clients, des fournisseurs ou des comptes bancaires existants</span><span class="sxs-lookup"><span data-stu-id="b546b-122">Link Contacts to Existing Customers, Vendors, or Bank Accounts</span></span>](marketing-how-link-contact.md)  
[<span data-ttu-id="b546b-123">Affecter des relations d'affaires à un contact</span><span class="sxs-lookup"><span data-stu-id="b546b-123">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="b546b-124">Utilisation de Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="b546b-124">Working with Finance and Operations, Business edition</span></span>](ui-work-product.md)

