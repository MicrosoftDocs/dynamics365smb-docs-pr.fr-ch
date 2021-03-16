---
title: 'Procédure : Importer les codes postaux suisses'
description: Vous pouvez réimporter le dernier fichier des codes postaux et l'utiliser pour mettre la table Code postal à jour. Le fichier Code postal peut être téléchargé du site Web de la Poste suisse. Après avoir importé le dernier code postal, vous pouvez définir des codes postaux pour des clients ou des fournisseurs.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 278ed697f3380633d6d35387ed7eeb3ed6b15c6c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383978"
---
# <a name="import-swiss-post-codes"></a><span data-ttu-id="ce51a-105">Importer les codes postaux suisses</span><span class="sxs-lookup"><span data-stu-id="ce51a-105">Import Swiss Post Codes</span></span>
<span data-ttu-id="ce51a-106">Vous pouvez réimporter le dernier fichier des codes postaux et l'utiliser pour mettre la table **Code postal** à jour.</span><span class="sxs-lookup"><span data-stu-id="ce51a-106">You can import the latest post code file and use it to update the **Post Code** table.</span></span> <span data-ttu-id="ce51a-107">Le fichier Code postal peut être téléchargé du site Web de la [Poste suisse](https://go.microsoft.com/fwlink/?LinkId=150292).</span><span class="sxs-lookup"><span data-stu-id="ce51a-107">The post code file can be downloaded from the [Swiss Post](https://go.microsoft.com/fwlink/?LinkId=150292) website.</span></span> <span data-ttu-id="ce51a-108">Après avoir importé le dernier code postal, vous pouvez définir des codes postaux pour des clients ou des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="ce51a-108">After importing the latest post code, you can define post codes for customers or vendors.</span></span> <span data-ttu-id="ce51a-109">Pour plus d'informations, reportez vous à [Enregistrer de nouveaux fournisseurs](../../purchasing-how-register-new-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="ce51a-109">For more information, see [Register New Vendors](../../purchasing-how-register-new-vendors.md).</span></span>  

## <a name="to-import-post-codes"></a><span data-ttu-id="ce51a-110">Pour importer des codes postaux</span><span class="sxs-lookup"><span data-stu-id="ce51a-110">To import post codes</span></span>  

1.  <span data-ttu-id="ce51a-111">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Codes postaux**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="ce51a-111">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Post Codes**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ce51a-112">Sélectionnez l'action **Importer codes postaux**.</span><span class="sxs-lookup"><span data-stu-id="ce51a-112">Choose the **Import Post Codes** action.</span></span>  
3.  <span data-ttu-id="ce51a-113">Dans la page **Importer codes postaux**, dans le champ **Nom fichier**, entrez le nom du fichier Code postal que vous souhaitez importer avec la table **Code postal**.</span><span class="sxs-lookup"><span data-stu-id="ce51a-113">On the **Import Post Codes** page, in the **Filename** field, enter the name of the post code file that you want to import to the **Post Code** table.</span></span>  
4.  <span data-ttu-id="ce51a-114">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce51a-114">Choose the **OK** button.</span></span>  

    <span data-ttu-id="ce51a-115">Les dernières informations de code postal sont importées.</span><span class="sxs-lookup"><span data-stu-id="ce51a-115">The latest post code information is imported.</span></span>  

<span data-ttu-id="ce51a-116">La procédure suivante décrit comment définir les codes postaux pour les clients, mais les mêmes étapes s'appliquent également pour définir les codes postaux pour les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="ce51a-116">The following procedure describes how to define post codes for customers, but the same steps also apply to defining post codes for vendors.</span></span>  

## <a name="to-define-post-codes-for-customers"></a><span data-ttu-id="ce51a-117">Pour définir des codes postaux pour les clients</span><span class="sxs-lookup"><span data-stu-id="ce51a-117">To define post codes for customers</span></span>  

1.  <span data-ttu-id="ce51a-118">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Clients**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="ce51a-118">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ce51a-119">Sélectionnez le client pour lequel vous souhaitez définir un code postal, puis sélectionnez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="ce51a-119">Select the customer for whom you want to define a post code, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="ce51a-120">Dans la page **Fiche client**, dans le raccourci **Général**, dans le champ **Code postal**, sélectionnez le code postal pour l'adresse du client.</span><span class="sxs-lookup"><span data-stu-id="ce51a-120">On the **Customer Card** page, on the **General** FastTab, in the **Post Code** field, select the post code for the customer's address.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ce51a-121">Lorsque vous sélectionnez le code postal, les champs **Ville** et **Code pays/région** fournissent automatiquement des informations dans la table **Code postal**.</span><span class="sxs-lookup"><span data-stu-id="ce51a-121">When you select the post code, the **City** and **Country/Region Code** fields populate automatically with the information from the **Post Code** table.</span></span> <span data-ttu-id="ce51a-122">Pour plus d'informations, reportez vous à [Enregistrer de nouveaux clients](../../sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="ce51a-122">For more information, see [Register New Customers](../../sales-how-register-new-customers.md).</span></span>  

4.  <span data-ttu-id="ce51a-123">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce51a-123">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce51a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce51a-124">See Also</span></span>   
 <span data-ttu-id="ce51a-125">[Documents vente et Documents achat, Suisse](swiss-purchase-documents-and-sales-documents.md) </span><span class="sxs-lookup"><span data-stu-id="ce51a-125">[Swiss Purchase Documents and Sales Documents](swiss-purchase-documents-and-sales-documents.md) </span></span>  
 <span data-ttu-id="ce51a-126">[Imprimer la liste des prélèvements de stock d'une commande vente](how-to-print-an-inventory-picking-list-from-a-sales-order.md) </span><span class="sxs-lookup"><span data-stu-id="ce51a-126">[Print an Inventory Picking List from a Sales Order](how-to-print-an-inventory-picking-list-from-a-sales-order.md) </span></span>  
 [<span data-ttu-id="ce51a-127">Enregistrer un nouveau fournisseur</span><span class="sxs-lookup"><span data-stu-id="ce51a-127">Register New Vendors</span></span>](../../purchasing-how-register-new-vendors.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]