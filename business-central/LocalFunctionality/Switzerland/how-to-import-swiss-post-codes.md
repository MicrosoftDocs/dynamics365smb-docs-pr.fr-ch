---
title: 'Procédure : Importer les codes postaux suisses'
description: Vous pouvez réimporter le dernier fichier des codes postaux et l'utiliser pour mettre la table Code postal à jour. Le fichier Code postal peut être téléchargé du site Web de la Poste suisse. Après avoir importé le dernier code postal, vous pouvez définir des codes postaux pour des clients ou des fournisseurs.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 01ecd2261852cb236fb0fede6a9761dde2f2e0e5
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878813"
---
# <a name="import-swiss-post-codes"></a><span data-ttu-id="3d418-105">Importer les codes postaux suisses</span><span class="sxs-lookup"><span data-stu-id="3d418-105">Import Swiss Post Codes</span></span>
<span data-ttu-id="3d418-106">Vous pouvez réimporter le dernier fichier des codes postaux et l'utiliser pour mettre la table **Code postal** à jour.</span><span class="sxs-lookup"><span data-stu-id="3d418-106">You can import the latest post code file and use it to update the **Post Code** table.</span></span> <span data-ttu-id="3d418-107">Le fichier Code postal peut être téléchargé du site Web de la [Poste suisse](https://go.microsoft.com/fwlink/?LinkId=150292).</span><span class="sxs-lookup"><span data-stu-id="3d418-107">The post code file can be downloaded from the [Swiss Post](https://go.microsoft.com/fwlink/?LinkId=150292) website.</span></span> <span data-ttu-id="3d418-108">Après avoir importé le dernier code postal, vous pouvez définir des codes postaux pour des clients ou des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="3d418-108">After importing the latest post code, you can define post codes for customers or vendors.</span></span> <span data-ttu-id="3d418-109">Pour plus d'informations, reportez vous à [Enregistrer de nouveaux fournisseurs](../../purchasing-how-register-new-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="3d418-109">For more information, see [Register New Vendors](../../purchasing-how-register-new-vendors.md).</span></span>  

## <a name="to-import-post-codes"></a><span data-ttu-id="3d418-110">Pour importer des codes postaux</span><span class="sxs-lookup"><span data-stu-id="3d418-110">To import post codes</span></span>  

1.  <span data-ttu-id="3d418-111">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Codes postaux**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3d418-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Post Codes**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3d418-112">Sélectionnez l'action **Importer codes postaux**.</span><span class="sxs-lookup"><span data-stu-id="3d418-112">Choose the **Import Post Codes** action.</span></span>  
3.  <span data-ttu-id="3d418-113">Dans la page **Importer codes postaux**, dans le champ **Nom fichier**, entrez le nom du fichier Code postal que vous souhaitez importer avec la table **Code postal**.</span><span class="sxs-lookup"><span data-stu-id="3d418-113">On the **Import Post Codes** page, in the **Filename** field, enter the name of the post code file that you want to import to the **Post Code** table.</span></span>  
4.  <span data-ttu-id="3d418-114">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d418-114">Choose the **OK** button.</span></span>  

    <span data-ttu-id="3d418-115">Les dernières informations de code postal sont importées.</span><span class="sxs-lookup"><span data-stu-id="3d418-115">The latest post code information is imported.</span></span>  

<span data-ttu-id="3d418-116">La procédure suivante décrit comment définir les codes postaux pour les clients, mais les mêmes étapes s'appliquent également pour définir les codes postaux pour les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="3d418-116">The following procedure describes how to define post codes for customers, but the same steps also apply to defining post codes for vendors.</span></span>  

## <a name="to-define-post-codes-for-customers"></a><span data-ttu-id="3d418-117">Pour définir des codes postaux pour les clients</span><span class="sxs-lookup"><span data-stu-id="3d418-117">To define post codes for customers</span></span>  

1.  <span data-ttu-id="3d418-118">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Clients**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="3d418-118">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3d418-119">Sélectionnez le client pour lequel vous souhaitez définir un code postal, puis sélectionnez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="3d418-119">Select the customer for whom you want to define a post code, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="3d418-120">Dans la page **Fiche client**, dans le raccourci **Général**, dans le champ **Code postal**, sélectionnez le code postal pour l'adresse du client.</span><span class="sxs-lookup"><span data-stu-id="3d418-120">On the **Customer Card** page, on the **General** FastTab, in the **Post Code** field, select the post code for the customer's address.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="3d418-121">Lorsque vous sélectionnez le code postal, les champs **Ville** et **Code pays/région** fournissent automatiquement des informations dans la table **Code postal**.</span><span class="sxs-lookup"><span data-stu-id="3d418-121">When you select the post code, the **City** and **Country/Region Code** fields populate automatically with the information from the **Post Code** table.</span></span> <span data-ttu-id="3d418-122">Pour plus d'informations, reportez vous à [Enregistrer de nouveaux clients](../../sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="3d418-122">For more information, see [Register New Customers](../../sales-how-register-new-customers.md).</span></span>  

4.  <span data-ttu-id="3d418-123">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d418-123">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3d418-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d418-124">See Also</span></span>   
 <span data-ttu-id="3d418-125">[Documents vente et Documents achat, Suisse](swiss-purchase-documents-and-sales-documents.md) </span><span class="sxs-lookup"><span data-stu-id="3d418-125">[Swiss Purchase Documents and Sales Documents](swiss-purchase-documents-and-sales-documents.md) </span></span>  
 <span data-ttu-id="3d418-126">[Imprimer la liste des prélèvements de stock d'une commande vente](how-to-print-an-inventory-picking-list-from-a-sales-order.md) </span><span class="sxs-lookup"><span data-stu-id="3d418-126">[Print an Inventory Picking List from a Sales Order](how-to-print-an-inventory-picking-list-from-a-sales-order.md) </span></span>  
 [<span data-ttu-id="3d418-127">Enregistrer un nouveau fournisseur</span><span class="sxs-lookup"><span data-stu-id="3d418-127">Register New Vendors</span></span>](../../purchasing-how-register-new-vendors.md)  
