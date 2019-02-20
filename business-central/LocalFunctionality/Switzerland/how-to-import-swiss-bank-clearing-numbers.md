---
title: "Procédure : Importer des numéros de compensation d'une banque suisse"
description: "Les numéros de compensation bancaire sont les numéros uniques utilisés pour identifier chaque agence ou succursale bancaire dans l'annuaire bancaire. Ces informations sont nécessaires pour le paiement électronique. Ce fichier peut être téléchargé à partir du site Web SIX Interbank Clearing."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 1acac32a417f794801da50c866db2643ea0a4c2d
ms.openlocfilehash: 9c3be847165129894228a04bca9dbbc67b7091a4
ms.contentlocale: fr-ch
ms.lasthandoff: 01/22/2019

---
# <a name="import-swiss-bank-clearing-numbers"></a><span data-ttu-id="ff054-105">Importer des numéros de compensation d'une banque suisse</span><span class="sxs-lookup"><span data-stu-id="ff054-105">Import Swiss Bank Clearing Numbers</span></span>
<span data-ttu-id="ff054-106">Les numéros de compensation bancaire sont les numéros uniques utilisés pour identifier chaque agence ou succursale bancaire dans l'annuaire bancaire.</span><span class="sxs-lookup"><span data-stu-id="ff054-106">Bank clearing numbers are unique numbers used to identify each bank agency or branch in the bank directory.</span></span> <span data-ttu-id="ff054-107">Ces informations sont nécessaires pour le paiement électronique.</span><span class="sxs-lookup"><span data-stu-id="ff054-107">This information is required for electronic payment.</span></span> <span data-ttu-id="ff054-108">Ce fichier peut être téléchargé à partir du site Web [SIX Interbank Clearing](https://go.microsoft.com/fwlink/?LinkId=145121).</span><span class="sxs-lookup"><span data-stu-id="ff054-108">The file can be downloaded from the [SIX Interbank Clearing](https://go.microsoft.com/fwlink/?LinkId=145121) website.</span></span>  

<span data-ttu-id="ff054-109">Vous pouvez importer le fichier BC Bank Master - le fichier officiel des numéros de compensation bancaires suisses - pour mettre à jour les informations relatives au numéro de compensation bancaire dans l'annuaire bancaire.</span><span class="sxs-lookup"><span data-stu-id="ff054-109">You can import the BC Bank Master file—the official Swiss bank clearing number file—to update the bank clearing number information in the bank directory.</span></span> <span data-ttu-id="ff054-110">Lorsque vous importez le fichier de numéros de compensation bancaire, les données sont importées dans la table **Annuaire bancaire**, et les données existantes sont remplacées.</span><span class="sxs-lookup"><span data-stu-id="ff054-110">When you import the bank clearing number file, the data is imported to the **Bank Directory** table, and the existing data is overwritten.</span></span> <span data-ttu-id="ff054-111">Après avoir importé le fichier de numéros de compensation bancaire, vous pouvez définir le code établissement mis à jour pour les clients et les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="ff054-111">After importing the bank clearing number file, you can define the updated bank branch number for customers and vendors.</span></span> <span data-ttu-id="ff054-112">Pour plus d'informations, voir la table Compte bancaire client et la table Compte bancaire fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ff054-112">For more information, see the Customer Bank Account table and the Vendor Bank Account table.</span></span>  

## <a name="to-import-swiss-bank-clearing-numbers"></a><span data-ttu-id="ff054-113">Pour importer des numéros de compensation d'une banque suisse</span><span class="sxs-lookup"><span data-stu-id="ff054-113">To import Swiss bank clearing numbers</span></span>  

1.  <span data-ttu-id="ff054-114">Choisissez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Annuaire bancaire**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="ff054-114">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Directory**, and choose the related link.</span></span>  
2.  <span data-ttu-id="ff054-115">Choisissez l'action **Importer l'annuaire bancaire**.</span><span class="sxs-lookup"><span data-stu-id="ff054-115">Choose the **Import Bank Directory** action.</span></span>  
3.  <span data-ttu-id="ff054-116">Dans la page **Importer l'annuaire bancaire**, dans le raccourci **Options**, sélectionnez le champ **Mettre à jour automatiquement les numéros de compensation** pour mettre à jour les numéros de compensation bancaire automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ff054-116">On the **Import Bank Directory** page, on the **Options** FastTab, select the **Automatically Update Clearing Numbers** field to update the bank clearing numbers automatically.</span></span>  
4.  <span data-ttu-id="ff054-117">Choisissez le bouton **Imprimer** ou le bouton **Aperçu** pour importer les numéros de compensation bancaire, puis, dans la page **Ouvrir**, localisez le fichier que vous avez téléchargé depuis le site Web SIX Interbank Clearing.</span><span class="sxs-lookup"><span data-stu-id="ff054-117">Choose the **Print** button or the **Preview** button to import the bank clearing numbers, and then, on the **Open** page, locate the file that you have downloaded from the SIX Interbank Clearing website.</span></span>
5. <span data-ttu-id="ff054-118">Cliquez sur le bouton **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="ff054-118">Choose the **Open** button.</span></span>  

    <span data-ttu-id="ff054-119">Si vous choisissez le bouton **Imprimer**, le contenu du fichier est imprimé.</span><span class="sxs-lookup"><span data-stu-id="ff054-119">If you choose the **Print** button, the contents of the file will be printed.</span></span> <span data-ttu-id="ff054-120">Si vous choisissez le bouton **Aperçu**, la table **Annuaire bancaire** sera mise à jour et un rapport dont les numéros de compensation auront été modifiés s'affichera.</span><span class="sxs-lookup"><span data-stu-id="ff054-120">If you choose the **Preview** button, the **Bank Directory** table will be updated and a report that has clearing numbers that have changed will be displayed.</span></span>  

<span data-ttu-id="ff054-121">La procédure suivante décrit comment définir des numéros d'établissement pour les comptes bancaires clients, mais les mêmes étapes s'appliquent également pour définir des numéros d'établissement pour les comptes bancaires fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ff054-121">The following procedure describes how to define bank branch numbers for customer bank accounts, but the same steps also apply for defining bank branch numbers for vendor bank accounts.</span></span>  

## <a name="to-define-bank-branch-numbers-for-customer-bank-accounts"></a><span data-ttu-id="ff054-122">Pour définir des numéros d'établissement pour les comptes bancaires clients</span><span class="sxs-lookup"><span data-stu-id="ff054-122">To define bank branch numbers for customer bank accounts</span></span>  

1.  <span data-ttu-id="ff054-123">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="ff054-123">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ff054-124">Sélectionnez le client pour lequel vous souhaitez créer les informations d'un compte bancaire, puis sélectionnez l'action **Comptes bancaires**.</span><span class="sxs-lookup"><span data-stu-id="ff054-124">Select the customer for whom you want to create bank account information, and then choose the **Bank Accounts** action.</span></span>  
3.  <span data-ttu-id="ff054-125">Dans la page **Liste comptes bancaires client**, sélectionnez le compte bancaire requis, puis cliquez sur l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="ff054-125">On the **Customer Bank Account List** page, select the required bank account, and then choose the **Edit** action.</span></span>  
4.  <span data-ttu-id="ff054-126">Sur le raccourci **Général**, renseignez le champ **Code établissement**.</span><span class="sxs-lookup"><span data-stu-id="ff054-126">On the **General** FastTab, in the **Bank Branch No.**</span></span> <span data-ttu-id="ff054-127">sélectionnez le numéro de l'agence ou de la succursale bancaire.</span><span class="sxs-lookup"><span data-stu-id="ff054-127">field, select the number of the bank agency or branch.</span></span>  
5.  <span data-ttu-id="ff054-128">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff054-128">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ff054-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff054-129">See Also</span></span>  
 <span data-ttu-id="ff054-130">[Paiements électroniques, Suisse](swiss-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="ff054-130">[Swiss Electronic Payments](swiss-electronic-payments.md) </span></span>  
 [<span data-ttu-id="ff054-131">Configuration des comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="ff054-131">Set Up Bank Accounts</span></span>](../../bank-how-setup-bank-accounts.md)

