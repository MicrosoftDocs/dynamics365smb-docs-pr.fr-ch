---
title: "Procédure : Imprimer des factures ESR"
description: "Vous pouvez imprimer un bordereau paiement Einzahlungsschein mit Referenznummer (ESR) de plusieurs façons."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cda530f1b731937c44c615cc3e0dd739c4a76754
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="print-esr-invoices"></a><span data-ttu-id="3878a-103">Imprimer des factures ESR</span><span class="sxs-lookup"><span data-stu-id="3878a-103">Print ESR Invoices</span></span>
<span data-ttu-id="3878a-104">Vous pouvez imprimer un bordereau paiement Einzahlungsschein mit Referenznummer (ESR) des façons suivantes :</span><span class="sxs-lookup"><span data-stu-id="3878a-104">You can print an Einzahlungsschein mit Referenznummer (ESR) payment slip in the following ways:</span></span>  

- <span data-ttu-id="3878a-105">En tant que facture vente ESR.</span><span class="sxs-lookup"><span data-stu-id="3878a-105">As part of the sales invoice ESR.</span></span>  
- <span data-ttu-id="3878a-106">En tant que document séparé appelé coupon ESR.</span><span class="sxs-lookup"><span data-stu-id="3878a-106">As a separate document called an ESR coupon.</span></span>  

<span data-ttu-id="3878a-107">L'état ESR de la facture de vente correspond à la facture de vente accompagnée d'un coupon ESR supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="3878a-107">The sales invoice ESR report corresponds with the sales invoice that is accompanied by an additional ESR coupon.</span></span> <span data-ttu-id="3878a-108">En utilisant l'état sur les coupons ESR des ventes, vous pouvez imprimer le bordereau de dépôt bleu.</span><span class="sxs-lookup"><span data-stu-id="3878a-108">By using the sales ESR coupon report, you can print the blue deposit slip.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="3878a-109">Vous devez sélectionner une imprimante et sélectionner des paramètres lors de l'installation du module Paiement ESR pour imprimer le bordereau de versement correctement.</span><span class="sxs-lookup"><span data-stu-id="3878a-109">You must select a printer and select settings during the ESR payment module installation to print the deposit slip correctly.</span></span> <span data-ttu-id="3878a-110">Pour plus d'informations, voir la table Sélection de l'imprimante.</span><span class="sxs-lookup"><span data-stu-id="3878a-110">For more information, see the Printer Selection table.</span></span>  

<span data-ttu-id="3878a-111">La procédure suivante décrit comment imprimer des factures vente ESR, mais les mêmes étapes s'appliquent également pour imprimer des coupons ESR.</span><span class="sxs-lookup"><span data-stu-id="3878a-111">The following procedure describes how to print ESR sales invoices, but the same steps also apply for printing ESR coupons.</span></span>  

## <a name="to-print-esr-invoices"></a><span data-ttu-id="3878a-112">Pour imprimer des factures ESR</span><span class="sxs-lookup"><span data-stu-id="3878a-112">To print ESR invoices</span></span>  

1.  <span data-ttu-id="3878a-113">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Facture ESR**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="3878a-113">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoice ESR**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3878a-114">Dans le traitement par lots **Facture vente ESR**, sur le raccourci **Options**, renseignez les champs comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3878a-114">In the **Sales Invoice ESR** batch job, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="3878a-115">Champ</span><span class="sxs-lookup"><span data-stu-id="3878a-115">Field</span></span>|<span data-ttu-id="3878a-116">Désignation</span><span class="sxs-lookup"><span data-stu-id="3878a-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="3878a-117">**Nombre de copies**</span><span class="sxs-lookup"><span data-stu-id="3878a-117">**No. of copies**</span></span>|<span data-ttu-id="3878a-118">Saisissez le nombre requis de copies de rapport.</span><span class="sxs-lookup"><span data-stu-id="3878a-118">Enter the required number of report copies.</span></span>|  
    |<span data-ttu-id="3878a-119">**Banque ESR**</span><span class="sxs-lookup"><span data-stu-id="3878a-119">**ESR Bank**</span></span>|<span data-ttu-id="3878a-120">Sélectionnez le code banque ESR qui doit être imprimé dans l'état.</span><span class="sxs-lookup"><span data-stu-id="3878a-120">Select the ESR bank code that is to be printed in the report.</span></span><br /><br /> <span data-ttu-id="3878a-121">Si la valeur de ce champ est <Blank> et que le code mode de règlement ESR n'est pas défini dans la fenêtre **Configuration ESR**, la banque principale ESR sélectionnée dans la fenêtre **Configuration ESR** sera imprimée.</span><span class="sxs-lookup"><span data-stu-id="3878a-121">If the value in this field is <Blank> and the ESR payment method code is not defined in the **ESR Setup** window, then the ESR main bank selected in the **ESR Setup** window will be printed.</span></span>|  
    |<span data-ttu-id="3878a-122">**LogInteraction**</span><span class="sxs-lookup"><span data-stu-id="3878a-122">**LogInteraction**</span></span>|<span data-ttu-id="3878a-123">Spécifiez si les interactions avec vos contacts sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="3878a-123">Specify if the interactions that you have with your contacts will be logged.</span></span>|  
    |<span data-ttu-id="3878a-124">**Système ESR**</span><span class="sxs-lookup"><span data-stu-id="3878a-124">**ESR System**</span></span>|<span data-ttu-id="3878a-125">Sélectionnez le système ESR via lequel vous pouvez envoyer des coupons ESR aux clients.</span><span class="sxs-lookup"><span data-stu-id="3878a-125">Select the ESR system through which you can send new ESR coupons to customers.</span></span> <span data-ttu-id="3878a-126">Pour utiliser le système ESR utilisé par la banque que vous avez spécifié dans le champ **Banque ESR**, sélectionnez **En fonction de la banque ESR**.</span><span class="sxs-lookup"><span data-stu-id="3878a-126">To use the ESR system that is used by the bank that you have specified in **ESR Bank** field, select **Based on ESR Bank**.</span></span>|  

3.  <span data-ttu-id="3878a-127">Sélectionnez le bouton **Imprimer** pour imprimer l'état ou le bouton **Aperçu** pour l'afficher à l'écran.</span><span class="sxs-lookup"><span data-stu-id="3878a-127">Choose the **Print** button to print the report or choose the **Preview** button to view it on the screen.</span></span>  

<span data-ttu-id="3878a-128">Vous pouvez également réimprimer l'état ESR de la facture vente ou l'état du coupon ESR vente.</span><span class="sxs-lookup"><span data-stu-id="3878a-128">You can also reprint the sales invoice ESR report or sales ESR coupon report.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3878a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3878a-129">See Also</span></span>  
 <span data-ttu-id="3878a-130">[Paiements électroniques à l'aide de ESR+, Suisse](swiss-electronic-payments-using-esr.md) </span><span class="sxs-lookup"><span data-stu-id="3878a-130">[Swiss Electronic Payments Using ESR](swiss-electronic-payments-using-esr.md) </span></span>  
 [<span data-ttu-id="3878a-131">Importer des paiements ESR</span><span class="sxs-lookup"><span data-stu-id="3878a-131">Import ESR Payments</span></span>](how-to-import-esr-payments.md)

