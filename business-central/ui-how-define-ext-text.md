---
title: Ajouter des lignes supplémentaires pour définir les descriptions étendues
description: Vous pouvez ajouter des lignes supplémentaires pour étendre le texte standard qui décrit un article, un compte général et d'autres données.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/08/2020
ms.author: edupont
ms.openlocfilehash: cf0418f4182e9d66da88af9262dd807a34dd3572
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782333"
---
# <a name="add-extended-text"></a><span data-ttu-id="32d25-103">Ajouter du texte étendu</span><span class="sxs-lookup"><span data-stu-id="32d25-103">Add Extended Text</span></span>

<span data-ttu-id="32d25-104">Vous pouvez étendre la description des articles, des unités de stockage, des comptes généraux et des ressources en ajoutant des lignes supplémentaires en tant que texte étendu.</span><span class="sxs-lookup"><span data-stu-id="32d25-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="32d25-105">Vous pouvez également définir des conditions d'utilisation des lignes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="32d25-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="32d25-106">La section suivante décrit comment ajouter du texte étendu à une description d'un élément.</span><span class="sxs-lookup"><span data-stu-id="32d25-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="32d25-107">Mais les mêmes étapes s'appliquent aux unités de stockage, aux comptes généraux et aux ressources.</span><span class="sxs-lookup"><span data-stu-id="32d25-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="32d25-108">Pour définir le texte étendu pour une description</span><span class="sxs-lookup"><span data-stu-id="32d25-108">To define extended text for an description</span></span>

1. <span data-ttu-id="32d25-109">Ouvrez la fiche correspondant à l'article auquel vous voulez ajouter du texte étendu, puis sélectionnez **Texte étendu**.</span><span class="sxs-lookup"><span data-stu-id="32d25-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="32d25-110">Renseignez les champs **Code** et **Désignation**.</span><span class="sxs-lookup"><span data-stu-id="32d25-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="32d25-111">Choisissez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="32d25-111">Choose the **New**.</span></span>
4. <span data-ttu-id="32d25-112">Renseignez le champ **Code langue** ou activez la case à cocher **Commun toutes langues** si vous utilisez des codes langue.</span><span class="sxs-lookup"><span data-stu-id="32d25-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="32d25-113">Renseignez les champs **Date début** et **Date fin** si vous souhaitez limiter les dates d'utilisation du texte étendu.</span><span class="sxs-lookup"><span data-stu-id="32d25-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="32d25-114">Dans le champ **Texte**, entrez le texte étendu.</span><span class="sxs-lookup"><span data-stu-id="32d25-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="32d25-115">Cochez les cases appropriées pour les types de documents où vous souhaitez imprimer le texte étendu.</span><span class="sxs-lookup"><span data-stu-id="32d25-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="32d25-116">Fermez la page.</span><span class="sxs-lookup"><span data-stu-id="32d25-116">Close the page.</span></span>

<span data-ttu-id="32d25-117">Vous pouvez maintenant ajouter ce texte étendu aux documents.</span><span class="sxs-lookup"><span data-stu-id="32d25-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="32d25-118">La procédure suivante explique comment ajouter du texte étendu à une commande vente, mais les mêmes étapes s'appliquent à tout autre document que vous avez spécifié pour le texte étendu.</span><span class="sxs-lookup"><span data-stu-id="32d25-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="32d25-119">Pour ajouter un texte d'article étendu à une ligne commande vente</span><span class="sxs-lookup"><span data-stu-id="32d25-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="32d25-120">Ouvrez une commande vente avec une ligne vente pour un article qui a étendu le texte défini.</span><span class="sxs-lookup"><span data-stu-id="32d25-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="32d25-121">Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="32d25-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="32d25-122">Sélectionnez la ligne en question, puis sélectionnez l'action **Insérer textes étendus**.</span><span class="sxs-lookup"><span data-stu-id="32d25-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="32d25-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32d25-123">See Also</span></span>

[<span data-ttu-id="32d25-124">Configuration de stock</span><span class="sxs-lookup"><span data-stu-id="32d25-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="32d25-125">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="32d25-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
